---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai set di dati
description: Scopri come utilizzare i set di dati Adobe Experience Platform in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: piattaforma, data lake, creare, lake, set di dati, profilo
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
TQID: https://experienceleague.adobe.com/VYD0k1jjQB-7iEShgFWKDfaVl5BFvtnxxjSrqBiYThw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 8d00060a8801a0d29a86894494b9fd7a69f30d88
workflow-type: tm+mt
source-wordcount: 1032
ht-degree: 76%

---

# Introduzione ai set di dati {#datasets-gs}

Tutti i dati acquisiti in Adobe Experience Platform vengono mantenuti all’interno del Data Lake come set di dati. Un set di dati è un costrutto di archiviazione e gestione per una raccolta di dati, in genere una tabella, che contiene uno schema (colonne) e dei campi (righe).

## Guardrail e limitazioni

* A partire dal 1° novembre 2024, la segmentazione in streaming non supporterà più l’utilizzo di eventi di invio e apertura dai set di dati di feedback e tracciamento di [!DNL Journey Optimizer]. Per implementare la quota limite o la gestione dell’affaticamento, utilizza le regole di business Ulteriori dettagli sono disponibili in [questa sezione](../conflict-prioritization/rule-sets.md), inclusa una spiegazione del caso d’uso per la limitazione giornaliera [qui](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510){target="_blank"}.

* A partire da febbraio 2025, è in corso l’introduzione di un guardrail time-to-live (TTL) nei set di dati generati dal sistema Journey Optimizer. [Ulteriori informazioni](datasets-ttl.md)

## Accedere ai set di dati {#access}

L&#39;area di lavoro **Set di dati** nell&#39;interfaccia utente [!DNL Adobe Journey Optimizer] consente di esplorare i dati e creare set di dati. Per aprire il dashboard Set di dati, seleziona **Set di dati** nel menu di navigazione a sinistra.

![](assets/datasets-home.png)

Seleziona la scheda **Sfoglia** per visualizzare l’elenco di tutti i set di dati disponibili per la tua organizzazione. Vengono visualizzati i dettagli di ciascun set di dati elencato, compresi il nome, lo schema a cui il set di dati aderisce e lo stato dell’ultima esecuzione di acquisizione. Per impostazione predefinita, vengono visualizzati solo i set di dati che hai acquisito. Se desideri visualizzare i set di dati generati dal sistema, abilita il pulsante di attivazione/disattivazione **Mostra set di dati di sistema** dal filtro.

![](assets/ajo-system-datasets.png)


Seleziona il nome di un set di dati per accedere alla relativa schermata di attività set di dati e vedi i dettagli del set di dati selezionato. La scheda attività include un grafico che mostra il tasso di utilizzo dei messaggi e un elenco di batch con esito positivo o negativo.

Per visualizzare l&#39;anteprima di un set di dati, seleziona **Anteprima set di dati** nell&#39;angolo in alto a destra dello schermo per visualizzare in anteprima il batch con esito positivo più recente in questo set di dati. Quando un set di dati è vuoto, il collegamento di anteprima viene disattivato.

![](assets/dataset-preview.png)

## [!DNL Journey Optimizer] set di dati di sistema {#system-datasets}

In questa sezione sono elencati i set di dati di sistema utilizzati da [!DNL Journey Optimizer]. Per visualizzare l’elenco completo dei campi e degli attributi di ogni schema, consulta il [dizionario dello schema di Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it){target="_blank"}.

>[!CAUTION]
>
> I set di dati di sistema **non devono essere modificati**. Qualsiasi modifica viene ripristinata automaticamente ad ogni aggiornamento del prodotto.

* Generazione dei rapporti

   * _Generazione rapporti - Set di dati evento del feedback dei messaggi_: log di consegna dei messaggi. Informazioni su tutte le consegne di messaggi da Journey Optimizer a scopo di generazione rapporti e creazione di pubblico. Anche il feedback dagli ISP dell’e-mail sui mancati recapiti viene registrato in questo set di dati.
   * _Generazione rapporti - Set di dati evento esperienza di tracciamento e-mail_: registri di interazione per il canale e-mail utilizzato a scopo di generazione rapporti e creazione di pubblico. Le informazioni memorizzate notificano le azioni eseguite dall’utente finale tramite e-mail (aperture, clic, ecc.).
   * _Generazione rapporti - Set di dati evento esperienza di tracciamento push_: registri di interazione per il canale push, utilizzato a scopo di generazione rapporti e creazione di pubblico. Le informazioni memorizzate notificano le azioni eseguite dall’utente finale sulle notifiche push.
   * _Generazione rapporti - Evento passaggio percorso_: acquisisce tutti gli eventi esperienza per i passaggi dei percorsi generati da Journey Optimizer per essere utilizzati da servizi come il reporting. È fondamentale anche per la creazione di rapporti in Customer Journey Analytics per l’analisi YoY. Collegato a metadati percorso.
   * _Generazione rapporti - Percorsi_: set di dati di metadati che raccoglie informazioni di ogni passaggio in un percorso.
   * _Generazione rapporti - Ccn_: set di dati evento di feedback che memorizza i log di consegna per le e-mail Ccn. Da utilizzare a scopo di generazione rapporti.

* Consenso

  _Set di dati del servizio di consenso_: memorizza le informazioni sul consenso di un profilo.

* Esportazione dei messaggi

  _Set di dati esportazione messaggi AJO_: memorizza il contenuto dei messaggi e-mail e SMS inviati a scopo di esportazione. I record vengono conservati per 7 giorni di calendario dall’acquisizione. Disponibile solo per le organizzazioni che hanno acquistato il componente aggiuntivo Esportazione messaggi. [Ulteriori informazioni](../configuration/message-export.md)

* Intelligent Services

  _Punteggi di ottimizzazione dei tempi di invio/Punteggi di coinvolgimento_: punteggi di output dell’IA per la gestione dei percorsi cliente.

* In entrata

  _Set di dati evento attività in entrata AJO_: memorizza gli eventi attività in entrata per i messaggi in entrata ricevuti in [!DNL Journey Optimizer].

>[!NOTE]
>
>Per poter acquisire i messaggi in arrivo in questo set di dati, un profilo deve disporre di almeno un messaggio inviato da [!DNL Journey Optimizer].

## Creare set di dati{#create-datasets}

L’aggiunta di dati a [!DNL Adobe Experience Platform] è la base per la creazione di un profilo. Potrai quindi sfruttare i profili in [!DNL Adobe Journey Optimizer]. Definisci innanzitutto gli schemi, utilizza gli strumenti ETL per preparare e standardizzare i dati, quindi crea i set di dati in base agli schemi.

Puoi creare un set di dati da uno schema o da un file CSV. Informazioni dettagliate su come creare set di dati sono disponibili nella documentazione di [!DNL Adobe Experience Platform]:

* [Creare un set di dati con uno schema esistente](https://experienceleague.adobe.com/it/docs/experience-platform/catalog/datasets/user-guide#schema){target="_blank"}
* [Mappare un file CSV su uno schema XDM esistente](https://experienceleague.adobe.com/it/docs/experience-platform/ingestion/tutorials/map-csv/existing-schema){target="_blank"}

In questo video, scopri come creare un set di dati, mapparlo su uno schema, aggiungervi dati e confermare che i dati sono stati acquisiti.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## Governance dei dati

In un set di dati, sfoglia la scheda **Governance dei dati** per controllare le etichette a livello di set di dati e di campo. La governance dei dati classifica i dati in base al tipo di criteri applicabili.

Una delle funzionalità principali di [!DNL Adobe Experience Platform] è quella di unire i dati provenienti da più sistemi aziendali per consentire agli addetti al marketing di identificare, comprendere e coinvolgere meglio i clienti. Questi dati possono essere soggetti a restrizioni di utilizzo definite dalla tua organizzazione o da normative legali. È quindi importante assicurarsi che le operazioni sui dati siano conformi ai criteri di utilizzo dei dati.

[!DNL Adobe Experience Platform Data Governance] consente di gestire i dati dei clienti e di garantire la conformità a normative, restrizioni e criteri applicabili all’utilizzo dei dati. Svolge un ruolo chiave all’interno di Experience Platform a vari livelli, tra cui catalogazione, derivazione dei dati, etichettatura dell’utilizzo dei dati, criteri di utilizzo dei dati e controllo dell’utilizzo dei dati per le azioni di marketing.

Ulteriori informazioni sulla governance dei dati e sulle etichette per l’utilizzo dei dati sono disponibili nella [documentazione sulla governance dei dati](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html?lang=it){target="_blank"}

## Esempi e casi d’uso {#samples}

* [Tutorial: inserire dati in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=it){target="_blank"}
* [Caso d&#39;uso end-to-end](../audience/creating-test-profiles.md) - Crea uno schema, un set di dati e acquisisci dati per aggiungere profili di test in [!DNL Adobe Journey Optimizer]
* [Esempi di query](../data/datasets-query-examples.md) - [!DNL Adobe Journey Optimizer] set di dati e casi d&#39;uso correlati.

>[!MORELIKETHIS]
>
>* [Introduzione alla gestione dei dati in Journey Optimizer](gs-data.md)
>* [Documentazione sui set di dati](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=it){target="_blank"}
>* [Documentazione sull&#39;acquisizione dei dati](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=it){target="_blank"}.
>* [Best practice per l&#39;adesione alle licenze di gestione dati](https://experienceleague.adobe.com/it/docs/experience-platform/landing/license/data-management-best-practices#data-management-best-practices){target="_blank"}
