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
source-git-commit: 62c0c1f46b5bd575102d9f27037cb6add1355ba2
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 22%

---

# Attivazione del pubblico in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puoi selezionare nelle campagne e nei percorsi qualsiasi pubblico generato utilizzando le definizioni dei segmenti, il caricamento personalizzato, i flussi di lavoro di composizione o la Composizione federata del pubblico.

>[!AVAILABILITY]
>
>L’utilizzo dei tipi di pubblico e degli attributi della composizione del pubblico non è attualmente disponibile con Healthcare Shield o Privacy and Security Shield. [Scopri come utilizzare gli attributi di arricchimento del pubblico in Journey Optimizer](../audience/about-audiences.md#enrichment)

## Ritardo di attivazione del pubblico {#activation}

I tipi di pubblico sono pronti per essere utilizzati in Journey Optimizer al termine dell’acquisizione. Sebbene questo avvenga in genere entro un’ora, è soggetto ad alcune variabilità. I tipi di pubblico risultanti dalle composizioni devono essere disponibili 24 ore dopo la pubblicazione.

Per i tipi di pubblico risultanti da processi di segmentazione in batch, l’attivazione può essere ritardata a causa della variabilità dell’acquisizione in batch. Per i percorsi Read-audience pianificati quotidianamente, puoi definire una finestra temporale nelle proprietà del percorso per garantire che siano disponibili nuovi dati sul pubblico prima dell’esecuzione del percorso. Se il processo di segmentazione non viene completato entro l’intervallo di tempo definito, il percorso verrà ignorato fino alla sua occorrenza successiva. [Scopri come pianificare un percorso Read-audience](../building-journeys/read-audience.md)

## Caricamento personalizzato e composizione federata del pubblico

Per i tipi di pubblico con caricamento personalizzato e Composizione federata del pubblico, tieni presente i seguenti guardrail:

* **Supporto per anteprima e bozza:** Al momento, l&#39;anteprima e la bozza non sono supportate per i tipi di pubblico creati mediante caricamento CSV o Composizione di pubblico federato. Tieni presente questo aspetto durante la pianificazione delle campagne.

* **Esecuzione del targeting di nuovi profili:** Quando non viene trovata una corrispondenza tra un record e un profilo del servizio profili unificato, viene creato un nuovo profilo vuoto. Questo profilo è collegato agli attributi di arricchimento memorizzati nel data lake. Poiché questo nuovo profilo è vuoto, i campi di targeting utilizzati in genere in Journey Optimizer (ad esempio, personalEmail.address, mobilePhone.number) sono vuoti e quindi non possono essere utilizzati per il targeting.

  Per risolvere questo problema, puoi specificare il &quot;campo di esecuzione&quot; (o &quot;indirizzo di esecuzione&quot; a seconda del canale) nella configurazione del canale come &quot;identityMap&quot;. In questo modo l’attributo scelto come identità nella creazione del pubblico sarà quello utilizzato per il targeting in Journey Optimizer.

* **Record attivati e unione identità:** tutti i record nel pubblico vengono attivati, inclusi eventuali duplicati. Durante la prossima esportazione del profilo Unified Profile Service, questi record passeranno attraverso l’unione delle identità. Di conseguenza, il numero di record attivati può differire dal numero di profili dopo l’unione di identità.

## Pubblico di destinazione in [!DNL Journey Optimizer]

Puoi sfruttare i tipi di pubblico in **[!DNL Journey Optimizer]** in modi diversi:

* Scegli un pubblico per una **campagna**: il messaggio viene inviato a tutti i singoli utenti appartenenti al pubblico selezionato. [Scopri come definire il pubblico di una campagna](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilizza un&#39;attività di orchestrazione **Read audience** in un percorso per fare in modo che tutti i singoli utenti del pubblico entrino nel percorso e ricevano i messaggi inclusi nel percorso. Supponiamo che tu abbia un pubblico di tipo “cliente silver”. Con questa attività, puoi fare in modo che tutti i clienti silver entrino in un percorso e inviare loro una serie di messaggi personalizzati. [Scopri come configurare un’attività Leggi pubblico](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  >[!NOTE]
  >
  >Qualsiasi percorso che utilizza un pubblico dalla composizione del pubblico o dal caricamento personalizzato nell’attività &quot;Read Audience&quot; (Leggi pubblico) avrà attributi di profilo aggiornati come l’ultima valutazione batch. Ciò include il consenso/la soppressione nel percorso.

* Utilizza l’attività **Condizione** in un percorso per generare condizioni basate sull’iscrizione al pubblico. [Scopri come utilizzare i tipi di pubblico nelle condizioni](../building-journeys/condition-activity.md#using-a-segment).

* Utilizza l&#39;attività evento **Qualificazione del pubblico** in un percorso per consentire ai singoli utenti di entrare o proseguire nel percorso in base alle entrate e alle uscite del pubblico Adobe Experience Platform. Ad esempio, puoi fare in modo che tutti i nuovi clienti silver entrino in un percorso e inviare loro messaggi. Per ulteriori informazioni su come utilizzare questa attività, fai riferimento a [Scopri come configurare un’attività di qualificazione del pubblico](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >A causa della natura batch dei tipi di pubblico creati utilizzando flussi di lavoro di composizione, caricamento personalizzato o composizione di pubblico federato, non puoi indirizzare questi tipi di pubblico in un’attività &quot;Qualificazione del pubblico&quot;. Solo i tipi di pubblico creati utilizzando le definizioni dei segmenti possono essere utilizzati in questa attività.
