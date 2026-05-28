---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva di Journey Optimizer per l’ingegnere dati
description: In qualità di ingegnere dati, scopri di più su come utilizzare Journey Optimizer
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
TQID: https://experienceleague.adobe.com/BAnAycmwv9oD4On4LSMwm7bBRKOuw5Tbv5a-r3ND-Dw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: af7571a6-3ddb-4c1c-abdf-4d4dde592140
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 991
ht-degree: 100%

---

# Introduzione per data engineer {#data-engineer}

In qualità di **data architect** o **data engineer**, devi impostare e gestire i dati del profilo cliente e altre origini dati che alimentano le esperienze orchestrate da [!DNL Journey Optimizer]. Ciò include l’integrazione di tutti i dati cliente e aziendali, provenienti da origini web, CRM o offline, in una visualizzazione unificata a 360° del cliente. Puoi modellare i dati del profilo cliente e i dati aziendali in schemi, configurare connettori di origine per l’acquisizione dei dati e garantire un flusso di dati fluido per abilitare insight e coinvolgimento cliente in tempo reale. Una volta che l’[amministratore di sistema](administrator.md) ti avrà concesso l’accesso e avrà preparato il tuo ambiente, puoi iniziare a utilizzare [!DNL Adobe Journey Optimizer].

>[!NOTE]
>
>Ulteriori informazioni sull’**acquisizione dei dati** nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=it){target="_blank"}.

>[!TIP]
>
>I dati in Journey Optimizer sono per te una novità? Inizia con la panoramica di [Introduzione alla gestione dei dati](../../data/gs-data.md) per comprendere schemi, set di dati, identità, il modello del frammento di profilo e l’elenco di controllo completo sulla preparazione dei dati prima di approfondire la configurazione.

## Passaggi fondamentali per la configurazione dei dati

Segui questi passaggi per impostare la base dati per Journey Optimizer:

1. **Creare lo spazio dei nomi di identità**. In Adobe [!DNL Journey Optimizer], le **Identità** collegano i consumatori tra dispositivi e canali creando un grafo identità. Il grafo identità collegato viene utilizzato per personalizzare le esperienze in base alle interazioni tra tutti i punti di contatto aziendali. Ulteriori informazioni su identità e spazi dei nomi di identità sono disponibili [in questa pagina](../../audience/get-started-identity.md).

   Inoltre, configura **identificatori supplementari** per consentire allo stesso profilo di inserire più istanze percorso in base a identificatori secondari come ID ordine o ID prenotazione. Scopri gli [identificatori supplementari](../../building-journeys/supplemental-identifier.md).

1. **Creare schemi** e abilitarli per i profili. Uno schema è un set di regole che rappresentano e convalidano la struttura e il formato dei dati. In pratica, gli schemi forniscono una definizione astratta di un oggetto reale (ad esempio una persona) e delineano i dati da includere in ogni istanza di tale oggetto (ad esempio nome, cognome, compleanno e così via).

   * Per percorsi e campagne standard, utilizza gli [schemi XDM](../../data/get-started-schemas.md)
   * Per le campagne orchestrate, crea [schemi relazionali](../../orchestrated/gs-schemas.md) per consentire la segmentazione di più entità

1. **Creare set di dati** e abilitarli per i profili. Un set di dati è un costrutto di archiviazione e gestione per una raccolta di dati, in genere una tabella, che contiene uno schema (colonne) e dei campi (righe). I set di dati contengono anche metadati che descrivono vari aspetti dei dati memorizzati. Una volta creato un set di dati, puoi mapparlo su uno schema esistente e aggiungervi dati. Ulteriori informazioni sui set di dati sono disponibili [in questa pagina](../../data/get-started-datasets.md).

   Per scenari avanzati, prepara **set di dati per le ricerche runtime** per arricchire l’esecuzione del percorso con dati in tempo reale da set di dati dei record. Scopri la [ricerca nei set di dati](../../building-journeys/dataset-lookup.md).

1. **Configurare i connettori di origine**. Adobe Journey Optimizer consente l’acquisizione di dati da fonti esterne e allo stesso tempo di strutturare, etichettare e migliorare i dati in entrata utilizzando i servizi di Platform. È possibile acquisire dati da diverse origini, ad esempio applicazioni Adobe, archivi basati su cloud, database e molte altre. Ulteriori informazioni sui connettori di origine sono disponibili [in questa pagina](../get-started-sources.md).

1. **Creare profili di test**. I profili di test sono necessari quando si utilizza la [modalità di test](../../building-journeys/testing-the-journey.md) in un percorso e per [visualizzare in anteprima e verificare i messaggi](../../content-management/preview-test.md) prima di inviarli. I passaggi per creare i profili di test sono descritti [in questa pagina](../../audience/creating-test-profiles.md).

1. **Configurare gli attributi calcolati** (facoltativo). Crea attributi derivati dai dati del profilo per semplificare la segmentazione e la personalizzazione. Gli attributi calcolati calcolano automaticamente metriche complesse come “acquisti totali negli ultimi 90 giorni” o “valore medio dell’ordine”. Scopri gli [attributi calcolati](../../audience/computed-attributes.md).

1. **Set di dati di esportazione messaggi** (facoltativo). Quando l’esportazione dei messaggi è abilitata a livello di configurazione dei canali, i contenuti delle e-mail e degli SMS inviati, vengono esportati automaticamente in un set di dati dedicato di Experience Platform per finalità di conformità, archiviazione o analisi a valle. Informazioni sull’[esportazione dei messaggi](../../configuration/message-export.md).

Inoltre, per poter inviare messaggi nei percorsi, devi configurare **[!UICONTROL Origini dati]**, **[!UICONTROL Eventi]** e **[!UICONTROL Azioni]**. Per ulteriori informazioni, consulta [questa sezione](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* La configurazione dell‘**origine dati** consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive le quali verranno utilizzate nei percorsi. Per ulteriori informazioni sulle origini dati, consulta [questa sezione](../../datasource/about-data-sources.md).

* **Eventi** ti consente di attivare i tuoi percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso. Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API per l’acquisizione in streaming per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. Per ulteriori informazioni sugli eventi, consulta [questa sezione](../../event/about-events.md).

* [!DNL Journey Optimizer] viene fornito con funzionalità per i messaggi incorporate: puoi creare i messaggi all’interno di un percorso e progettare il contenuto. Se per l’invio di messaggi utilizzi un sistema di terze parti, ad esempio Adobe Campaign, è possibile creare un‘**azione personalizzata**. Per ulteriori informazioni sulle azioni, consulta [questa sezione](../../action/action.md).

## Monitorare e analizzare i dati del percorso

Una volta che i percorsi sono in esecuzione, puoi eseguire query sugli eventi dei passaggi del percorso nel data lake per monitorare le prestazioni, risolvere i problemi e analizzare il comportamento dei clienti. Utilizzare le query SQL per analizzare:

* Modelli di entrata e uscita del profilo
* Tassi di errore e motivi di eliminazione
* Prestazioni del processo di esportazione Leggi pubblico
* Metriche delle prestazioni delle azioni personalizzate
* Stati e ostacoli dell’istanza percorso

Esplora gli esempi di query pronti all’uso [per l’analisi dei percorsi](../../reports/query-examples.md) per iniziare a utilizzare l’analisi dei dati e la risoluzione dei problemi.

## Collaborare tra ruoli

Il lavoro di configurazione dei dati è essenziale per gli altri team:

>[!BEGINTABS]

>[!TAB Lavorare con gli amministratori]

Collabora con gli [amministratori](administrator.md) per accesso e governance:

* Richiedi le autorizzazioni necessarie per la gestione dei dati e la creazione di schemi
* Coordina l’accesso alla sandbox per sviluppo e test
* Allinea i criteri di governance dei dati e la gestione del consenso
* Analizza i criteri di conservazione dei dati e i requisiti di archiviazione

>[!TAB Lavorare con gli sviluppatori]

Collabora con gli [sviluppatori](developer.md) sulla struttura dei dati e sugli eventi:

* Fornisci schemi XDM e strutture di eventi necessari per l’implementazione
* Definisci quali eventi devono essere inviati e il formato payload richiesto
* Allinea i requisiti di raccolta dati e agli standard di qualità dei dati
* Testa la consegna di eventi insieme all’acquisizione di dati

>[!TAB Lavorare con i marketer]

Collabora con i [marketer](marketer.md) su tipi di pubblico e dati:

* Crea attributi calcolati per la personalizzazione e la segmentazione
* Crea tipi di pubblico in base ai requisiti di campagna e percorso
* Crea schemi relazionali per campagne orchestrate
* Supporta la segmentazione di più entità per casi d’uso avanzati

>[!ENDTABS]
