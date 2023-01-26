---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sugli schemi ExperienceEvent per eventi di percorso
description: Scopri gli schemi ExperienceEvent per eventi di percorso
feature: Schemas
topic: Administration
role: Admin
level: Intermediate
keywords: schemi, XDM, piattaforma, streaming, acquisizione, percorso
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 3%

---

# Informazioni sugli schemi ExperienceEvent per [!DNL Journey Optimizer] Eventi {#about-experienceevent-schemas}

[!DNL Journey Optimizer] Gli eventi sono eventi esperienza XDM che vengono inviati a Adobe Experience Platform tramite Streaming Ingestion.

Pertanto, un importante prerequisito per la configurazione di eventi per [!DNL Journey Optimizer] L’utente ha familiarità con Experience Data Model (o XDM) di Adobe Experience Platform e con le modalità di composizione degli schemi XDM Experience Event, nonché con le modalità di streaming dei dati in formato XDM in Adobe Experience Platform.

## Requisiti dello schema per [!DNL Journey Optimizer] Eventi  {#schema-requirements}

Il primo passaggio nella configurazione di un evento per [!DNL Journey Optimizer] assicurati di disporre di uno schema XDM definito per rappresentare l’evento e di un set di dati creato per registrare le istanze dell’evento in Adobe Experience Platform. Disporre di un set di dati per i tuoi eventi non è strettamente necessario, ma l’invio degli eventi a un set di dati specifico ti consentirà di mantenere la cronologia degli eventi degli utenti per riferimenti e analisi futuri, quindi è sempre una buona idea. Se non disponi già di uno schema e di un set di dati appropriati per l’evento, entrambe le attività possono essere eseguite nell’interfaccia Web di Adobe Experience Platform.

![](assets/schema1.png)

Qualsiasi schema XDM utilizzato per [!DNL Journey Optimizer] gli eventi devono soddisfare i seguenti requisiti:

* Lo schema deve essere della classe ExperienceEvent XDM.

   ![](assets/schema2.png)

* Per gli eventi generati dal sistema, lo schema deve includere il gruppo di campi ID evento Orchestration. [!DNL Journey Optimizer] utilizza questo campo per identificare gli eventi utilizzati nei percorsi.

   ![](assets/schema3.png)

* Dichiara un campo di identità per identificare i singoli profili nell’evento. Se non viene specificata alcuna identità, è possibile utilizzare una mappa di identità. Queste operazioni non sono consigliate.

   ![](assets/schema4.png)

* Se desideri che questi dati siano disponibili per la ricerca in un secondo momento in un Percorso, contrassegna lo schema e il set di dati per il profilo.

   ![](assets/schema5.png)

   ![](assets/schema6.png)

* Puoi includere campi di dati per acquisire altri dati contestuali da includere con l’evento, ad esempio informazioni sull’utente, il dispositivo da cui è stato generato l’evento, la posizione o qualsiasi altra circostanza significativa correlata all’evento.

   ![](assets/schema7.png)

   ![](assets/schema8.png)

## Sfruttare le relazioni tra schemi{#leverage_schema_relationships}

Adobe Experience Platform consente di definire relazioni tra schemi per utilizzare un set di dati come tabella di ricerca per un altro.

Supponiamo che il modello dati del brand abbia uno schema che cattura gli acquisti. Inoltre è disponibile uno schema per il catalogo dei prodotti. Puoi acquisire l’ID prodotto nello schema di acquisto e utilizzare una relazione per cercare dettagli di prodotto più completi dal catalogo prodotti. Ciò ti consente di creare un segmento per tutti i clienti che hanno acquistato un laptop, ad esempio, senza dover elencare esplicitamente tutti gli ID dei laptop o acquisire ogni singolo dettaglio di prodotto nei sistemi transazionali.

Per definire una relazione, è necessario disporre di un campo dedicato nello schema di origine, in questo caso il campo ID prodotto nello schema di acquisto. Questo campo deve fare riferimento al campo ID prodotto nello schema di destinazione. Le tabelle di origine e di destinazione devono essere abilitate per i profili e lo schema di destinazione deve avere tale campo comune definito come identità principale.

Ecco lo schema del catalogo prodotti abilitato per il profilo con l’ID prodotto definito come identità principale.

![](assets/schema9.png)

Ecco lo schema di acquisto con la relazione definita nel campo ID prodotto .

![](assets/schema10.png)

>[!NOTE]
>
>Ulteriori informazioni sulle relazioni dello schema nel [Documentazione di Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html?lang=en).

In Journey Optimizer puoi quindi sfruttare tutti i campi delle tabelle collegate:

* durante la configurazione di un evento aziendale o unitario, [Leggi tutto](../event/experience-event-schema.md#unitary_event_configuration)
* quando si utilizzano condizioni in un percorso, [Leggi tutto](../event/experience-event-schema.md#journey_conditions_using_event_context)
* nella personalizzazione dei messaggi, [Leggi tutto](../event/experience-event-schema.md#message_personalization)
* nella personalizzazione personalizzata delle azioni, [Leggi tutto](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### Matrici{#relationships_limitations}

È possibile definire una relazione di schema su un array di stringhe, ad esempio un elenco di ID prodotto.

![](assets/schema15.png)

Tuttavia, non è possibile definire una relazione di schema con un attributo all’interno di un array di oggetti, ad esempio un elenco di informazioni di acquisto (ID prodotto, nome prodotto, prezzo, sconto). I valori di ricerca non saranno disponibili nei percorsi (condizioni, azioni personalizzate, ecc.) e la personalizzazione dei messaggi.

![](assets/schema16.png)

### Configurazione evento{#unitary_event_configuration}

I campi dello schema collegati sono disponibili nella configurazione di un evento unitario e aziendale:

* quando esplori i campi dello schema evento nella schermata di configurazione dell’evento.
* quando si definisce una condizione per gli eventi generati dal sistema.

![](assets/schema11.png)

I campi collegati non sono disponibili:

* nella formula della chiave evento
* in condizione id evento (eventi basati su regole)

Per scoprire come configurare un evento unitario, consulta questo [page](../event/about-creating.md).

### Condizioni di percorso che utilizzano il contesto dell’evento{#journey_conditions_using_event_context}

Puoi utilizzare i dati di una tabella di ricerca collegata a un evento utilizzato in un percorso per la creazione di condizioni (editor di espressioni).

Aggiungi una condizione in un percorso, modifica l’espressione e apri il nodo dell’evento nell’editor espressioni.

![](assets/schema12.png)

Per scoprire come definire le condizioni di percorso, consulta questo [page](../building-journeys/condition-activity.md).

### Personalizzazione dei messaggi{#message_personalization}

I campi collegati sono disponibili quando si personalizza un messaggio. I campi correlati vengono visualizzati nel contesto passato dal percorso al messaggio.

![](assets/schema14.png)

Per scoprire come personalizzare un messaggio con informazioni sul percorso contestuale, consulta questo [page](../personalization/personalization-use-case.md).

### Personalizzazione di azioni personalizzata con contesto evento percorso{#custom_action_personalization_with_journey_event_context}

I campi collegati sono disponibili durante la configurazione dei parametri delle azioni di un’attività azione personalizzata del percorso.

![](assets/schema13.png)

Per informazioni sull’utilizzo delle azioni personalizzate, consulta [page](../building-journeys/using-custom-actions.md).
