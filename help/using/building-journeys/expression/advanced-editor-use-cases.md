---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzo dell’editor di espressioni avanzate
description: Scopri come creare espressioni avanzate
feature: Journeys
role: Developer
level: Experienced
hide: true
hidefromtoc: true
keywords: espressione, condizione, casi d’uso, eventi
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 2%

---


# Esempi di espressioni avanzate{#advanced-expression-examples}

L’editor di espressioni avanzate può essere utilizzato per creare condizioni che consentono di filtrare gli utenti nei percorsi. Queste condizioni ti consentono di eseguire il targeting degli utenti in base a ora, data, posizione, durata, in modo che possano essere indirizzati nuovamente nel percorso.

>[!CAUTION]
>
>L’utilizzo di eventi di esperienza nelle espressioni/condizioni di percorso non è supportato. Se il caso d’uso richiede l’utilizzo di eventi esperienza, considera metodi alternativi. [Ulteriori informazioni](../exp-event-lookup.md)


## Creazione delle condizioni per gli eventi esperienza


>[!CAUTION]
>
>L’utilizzo di eventi di esperienza nelle espressioni/condizioni di percorso non è supportato. Se il caso d’uso richiede l’utilizzo di eventi esperienza, considera metodi alternativi. [Ulteriori informazioni](../exp-event-lookup.md)
>



L’editor di espressioni avanzate è obbligatorio per eseguire query su serie temporali come un elenco di acquisti o clic sui messaggi passati. Tali query non possono essere eseguite utilizzando l’editor semplice.

>[!NOTE]
>
>Gli eventi iniziano con @, le origini dati con #.

Gli eventi di esperienza vengono recuperati da Adobe Experience Platform come raccolta in ordine cronologico inverso, quindi:

* la prima funzione restituirà l’evento più recente
* last function restituirà quella più vecchia.

Ad esempio, supponiamo che tu voglia indirizzare i clienti con un abbandono del carrello negli ultimi 7 giorni per inviare un messaggio quando il cliente si avvicina a un negozio, con un’offerta sugli articoli che voleva fossero in negozio.

**È necessario creare le seguenti condizioni:**

Innanzitutto, rivolgiti ai clienti che hanno navigato nel negozio online ma non hanno finalizzato l’ordine negli ultimi 7 giorni.

**L&#39;espressione cerca un valore specificato in un valore stringa:**

`In ("addToCart", #{field reference from experience event})`

**L&#39;espressione cerca tutti gli eventi per l&#39;utente specificato negli ultimi 7 giorni:**

Quindi seleziona tutti gli eventi di aggiunta al carrello che non si sono trasformati in un completePurchase.

>[!NOTE]
>
>Per inserire rapidamente i campi nell’espressione, fai doppio clic sul campo nel pannello a sinistra dell’editor.

La marca temporale specificata funge da valore data/ora, la seconda da numero di giorni.

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

Questa espressione restituisce un valore booleano.

**Ora creiamo un&#39;espressione per verificare che il prodotto sia disponibile**

* In Inventory, questa espressione cerca il campo quantità di un prodotto e specifica che deve essere maggiore di 0.

`#{Inventory.fieldgroup3.quantity} > 0`

* A destra, vengono specificati i valori necessari. In questo caso, è necessario recuperare la posizione del negozio, mappata dalla posizione dell’evento &quot;ArriveLumaStudio&quot;:

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* E specificare SKU, utilizzando la funzione `first` per recuperare l&#39;interazione &quot;addToCart&quot; più recente:

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

Da lì puoi aggiungere un altro percorso nel percorso per quando il prodotto non è in negozio e inviare una notifica con l’offerta di coinvolgimento. Configura i messaggi di conseguenza e utilizza i dati di personalizzazione per migliorare il target del messaggio.

## Esempi di manipolazioni delle stringhe con l’editor di espressioni avanzate

**In condizioni**

Questa condizione recupera solo gli eventi di recinto geografico attivati in &quot;Arlington&quot;:

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Spiegazione: Si tratta di un confronto stringhe rigoroso (distinzione maiuscole/minuscole), equivalente a una query in modalità semplice che utilizza `equal to` con `Is sensitive` selezionato.

La stessa query con `Is sensitive` deselezionato genererà la seguente espressione in modalità avanzata:

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**In azioni**

L’espressione seguente ti consente di definire l’ID del sistema di gestione delle relazioni con i clienti in un campo di personalizzazione delle azioni:

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Spiegazione: In questo esempio vengono utilizzate le funzioni `substr` e `lastIndexOf` per rimuovere le parentesi graffe che racchiudono l&#39;ID CRM passato con un evento di avvio dell&#39;app mobile.


Per ulteriori informazioni su come utilizzare l&#39;editor di espressioni avanzate, guarda [questo video](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html?lang=it).
