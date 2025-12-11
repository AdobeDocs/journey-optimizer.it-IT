---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui tipi di pubblico di Adobe Experience Platform
description: Scopri come utilizzare i tipi di pubblico di Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: 1d32db0103fd4f2afcd021cff5e8491515c86d65
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 13%

---

# Attivazione del pubblico in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puoi selezionare nelle campagne e nei percorsi qualsiasi pubblico generato utilizzando le definizioni dei segmenti, il caricamento personalizzato, i flussi di lavoro di composizione o la Composizione federata del pubblico.

## Guardrail e limitazioni {#guardrails}

* **Healthcare Shield o Privacy and Security Shield** - L&#39;utilizzo di tipi di pubblico e attributi dalla composizione del pubblico non è attualmente disponibile con Healthcare Shield o Privacy and Security Shield. [Scopri come utilizzare gli attributi di arricchimento del pubblico in [!DNL Journey Optimizer]](../audience/about-audiences.md#enrichment)

* **Caricamento personalizzato e composizione pubblico federato** - Per i tipi di pubblico Caricamento personalizzato e Composizione pubblico federato, tieni presente i seguenti guardrail:

   * **Supporto per anteprima e bozza:** Al momento, l&#39;anteprima e la bozza non sono supportate per i tipi di pubblico creati mediante caricamento CSV o Composizione di pubblico federato. Tieni presente questo aspetto durante la pianificazione delle campagne.

   * **Esecuzione del targeting di nuovi profili:** Quando non viene trovata una corrispondenza tra un record e un profilo del servizio profili unificato, viene creato un nuovo profilo vuoto. Questo profilo è collegato agli attributi di arricchimento memorizzati nel data lake. Poiché questo nuovo profilo è vuoto, i campi di targeting utilizzati in genere in [!DNL Journey Optimizer] (ad esempio, personalEmail.address, mobilePhone.number) sono vuoti. Pertanto, questi campi non possono essere utilizzati per il targeting.

     Per risolvere questo problema, puoi specificare il &quot;campo di esecuzione&quot; (o &quot;indirizzo di esecuzione&quot; a seconda del canale) nella configurazione del canale come &quot;identityMap&quot;. In questo modo l&#39;attributo scelto come identità durante la creazione del pubblico sarà quello utilizzato per il targeting in [!DNL Journey Optimizer].

   * **Record attivati e unione identità:** tutti i record nel pubblico vengono attivati, inclusi eventuali duplicati. Durante la prossima esportazione del profilo del servizio profili unificato, questi record passano attraverso l’unione di identità. Di conseguenza, il numero di record attivati può differire dal numero di profili dopo l’unione di identità.

## Ritardo di attivazione del pubblico {#activation}

I tipi di pubblico sono pronti per essere utilizzati in [!DNL Journey Optimizer] al termine dell&#39;acquisizione. Sebbene questo avvenga in genere entro un’ora, è soggetto ad alcune variabilità. I tipi di pubblico risultanti dalle composizioni devono essere disponibili 24 ore dopo la pubblicazione.

Per i tipi di pubblico risultanti da processi di segmentazione in batch, l’attivazione può essere ritardata a causa della variabilità dell’acquisizione in batch. Per i percorsi Read-audience pianificati quotidianamente, puoi definire una finestra temporale nelle proprietà del percorso per garantire che siano disponibili nuovi dati sul pubblico prima dell’esecuzione del percorso.

Se il processo di segmentazione non viene completato entro l’intervallo di tempo definito, il percorso verrà ignorato fino alla sua occorrenza successiva. [Scopri come pianificare un percorso Read-audience](../building-journeys/read-audience.md)

## Pubblico di destinazione in [!DNL Journey Optimizer]

Puoi sfruttare i tipi di pubblico in **[!DNL Journey Optimizer]** in modi diversi:

* Scegli un pubblico per una **campagna**: il messaggio viene inviato a tutti i singoli utenti appartenenti al pubblico selezionato. [Scopri come definire il pubblico di una campagna](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilizza un&#39;attività di orchestrazione **Read audience** in un percorso per fare in modo che tutti i singoli utenti del pubblico entrino nel percorso e ricevano i messaggi inclusi nel percorso. Supponiamo che tu abbia un pubblico di tipo “cliente silver”. Con questa attività, puoi fare entrare in un percorso tutti i clienti silver. Puoi quindi inviare loro una serie di messaggi personalizzati. [Scopri come configurare un’attività Leggi pubblico](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  Per i percorsi che utilizzano tipi di pubblico da composizione del pubblico o caricamento personalizzato, gli attributi del profilo sono aggiornati quanto l’ultima valutazione batch all’ingresso del percorso. Tuttavia, dopo un&#39;attività **Wait**, il percorso aggiorna gli attributi del profilo da Unified Profile Service (UPS), recuperando i dati disponibili più recenti, il che significa che gli attributi del profilo possono cambiare durante l&#39;esecuzione del percorso. [Ulteriori informazioni sull&#39;aggiornamento del profilo dopo un&#39;attività Attendi](../building-journeys/wait-activity.md#profile-refresh)

* Utilizza l’attività **Condizione** in un percorso per generare condizioni basate sull’iscrizione al pubblico. [Scopri come utilizzare i tipi di pubblico nelle condizioni](../building-journeys/condition-activity.md#using-a-segment).

* Utilizza l&#39;attività evento **Qualificazione del pubblico** in un percorso per consentire ai singoli utenti di entrare o proseguire nel percorso in base alle entrate e alle uscite del pubblico Adobe Experience Platform. Ad esempio, puoi fare in modo che tutti i nuovi clienti silver entrino in un percorso e inviare loro messaggi. [Scopri come configurare un&#39;attività di qualificazione del pubblico](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >A causa della natura batch dei tipi di pubblico creati utilizzando flussi di lavoro di composizione, caricamento personalizzato o composizione di pubblico federato, non puoi indirizzare questi tipi di pubblico in un’attività &quot;Qualificazione del pubblico&quot;. Solo i tipi di pubblico creati utilizzando le definizioni dei segmenti possono essere utilizzati in questa attività.

## Attivazione di tipi di pubblico non supportati in [!DNL Journey Optimizer]

Solo i tipi di pubblico generati con **definizione segmento**, **composizioni pubblico**, **caricamento personalizzato (file CSV)** e **composizione pubblico federato** possono essere indirizzati direttamente ai percorsi e alle campagne di Journey Optimizer. [Ulteriori informazioni sui tipi di pubblico disponibili](../audience/about-audiences.md#types)

Se devi eseguire il targeting dei profili di un pubblico non supportato, ad esempio un pubblico di Customer Journey Analytics, devi racchiuderli in una nuova definizione di segmento nel portale del pubblico. Informazioni dettagliate su come aggiungere tipi di pubblico in una definizione di segmento sono disponibili nella [documentazione di Segment Builder](https://experienceleagu;e.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#adding-audiences){target="_blank"}

Al termine, attendi che la valutazione della segmentazione sia completata per utilizzarla nei percorsi e nelle campagne.
