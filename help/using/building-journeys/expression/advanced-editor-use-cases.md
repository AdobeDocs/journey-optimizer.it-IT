---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzo dell’editor di espressioni avanzate
description: Scopri come creare espressioni avanzate
feature: Journeys
role: Developer
level: Experienced
hide: true
keywords: espressione, condizione, casi d’uso, eventi
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UUeCcATC7MFHsLuI8TPoVHqwVe9GOXUq3U3RoAG-a1o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
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

## Filtraggio delle marche temporali nelle espressioni

Quando si fa riferimento a più eventi di attività del carrello, specifica una finestra di marca temporale iniziale e finale per evitare di raccogliere i dati storici. Ad esempio:

```json
toDateTimeOnly(currentDataPackField.timestamp) >= toDateTimeOnly(@event{poc_UDXCartAddSavedCheckOutEv.timestamp})
AND
toDateTimeOnly(currentDataPackField.timestamp) < toDateTimeOnly(nowWithDelta(4, "hours"))
```

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

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina vengono forniti esempi pratici di utilizzo dell&#39;editor di espressioni avanzate per creare condizioni di percorso che filtrano gli utenti in base all&#39;attività del carrello, allo stato dell&#39;inventario, agli eventi di recinto geografico, alle manipolazioni delle stringhe e alle finestre di marca temporale.

**Intenti:**

* Crea una condizione di abbandono carrello utilizzando `in()` e `inLastDays()` per il targeting degli utenti che hanno aggiunto elementi ma non hanno completato l&#39;acquisto entro 7 giorni
* Filtra le raccolte di eventi esperienza per finestra di marca temporale per evitare l’acquisizione di dati storici
* Applica confronti di stringhe con distinzione tra maiuscole e minuscole e senza distinzione tra maiuscole e minuscole ai campi evento del recinto geografico
* Estrarre e manipolare gli ID CRM dagli eventi di avvio dell&#39;app mobile tramite `substr` e `lastIndexOf`
* Verificare la disponibilità di magazzino dei prodotti confrontando un campo quantità con una soglia
* Combinare più espressioni booleane utilizzando la logica `and` / `not` nelle condizioni di percorso

**Glossario:**

* **Editor espressioni avanzate**: interfaccia di Journey Optimizer per la scrittura di espressioni complesse a livello di codice tramite funzioni, operatori e riferimenti di campo *(specifico per prodotto)*
* **currentDataPackField**: variabile di loop utilizzata per l&#39;iterazione delle raccolte di origini dati in `all()`, `first()` o `last()` funzioni *(specifiche del prodotto)*
* **inLastDays(timestamp, N)**: funzione data che restituisce true se la marca temporale specificata rientra negli ultimi N giorni *(specifico per prodotto)*
* **Eventi esperienza**: record di dati comportamentali di serie temporali memorizzati in Adobe Experience Platform, recuperati in ordine cronologico inverso *(specifico per prodotto)*

**Guardrail:**

* L’utilizzo diretto di eventi esperienza nelle espressioni/condizioni del percorso non è supportato; è invece necessario utilizzare metodi alternativi come attributi calcolati o segmenti di pubblico
* Utilizza l’editor di espressioni avanzate (non l’editor semplice) per le query su dati di serie temporali come raccolte di acquisti o clic
* Facendo doppio clic su un campo nel pannello a sinistra, questo viene inserito rapidamente nell’espressione; evita di digitare manualmente i percorsi dei campi per ridurre gli errori
* Le espressioni che eseguono query sugli eventi di esperienza restituiscono un valore booleano; assicurati che la logica a valle preveda un tipo booleano

**Terminologia:**

* Nome canonico: Editor espressioni avanzate — Acronimo: none — varianti: editor espressioni, editor avanzato
* Sinonimi: &quot;addToCart&quot; = &quot;interazione di aggiunta al carrello&quot;; &quot;completePurchase&quot; = &quot;evento di completamento acquisto&quot;
* Non confondere: eventi (con prefisso `@`) ≠ origini dati (con prefisso `#`)

**Domande frequenti:**

* **D: perché devo utilizzare l&#39;editor avanzato invece dell&#39;editor semplice per le query di abbandono del carrello?** — L&#39;editor semplice non è in grado di eseguire query sugli insiemi di serie temporali. L&#39;editor avanzato è necessario per le funzioni di raccolta `all()`, `first()` e `last()`.
* **D: come si fa riferimento all&#39;evento &quot;addToCart&quot; più recente in un&#39;espressione?** — Utilizzare la funzione `first()` nella raccolta di eventi esperienza filtrata da `productInteraction == "addToCart"`, poiché gli eventi vengono restituiti in ordine cronologico inverso.
* **D: come posso fare in modo che in un confronto di stringhe non venga fatta distinzione tra maiuscole e minuscole nell&#39;editor avanzato?** — Utilizzare la funzione `equalIgnoreCase()` anziché l&#39;operatore `==`.
* **D: qual è lo scopo dell&#39;aggiunta di una finestra di marca temporale durante la query degli eventi del carrello?** — la specifica di una marca temporale di inizio e di fine impedisce il recupero dei dati storici che non rientrano nella finestra di attività prevista.
* **D: come rimuovere le parentesi graffe da una stringa ID CRM passata in un evento?** — Utilizzare `substr()` in combinazione con `lastIndexOf()` per estrarre il contenuto tra parentesi graffe.

+++
