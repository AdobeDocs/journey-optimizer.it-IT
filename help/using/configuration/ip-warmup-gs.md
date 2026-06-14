---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai piani di preparazione IP
description: Scopri come implementare un piano di preparazione IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, recapitabilità
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
TQID: https://experienceleague.adobe.com/xjJKrCXUmQY5sZu2w-B09agQh-tb4qkSXM0Vh2-TDnc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 35%

---

# Introduzione ai piani di preparazione IP {#ip-warmup-gs}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri in che modo i piani di riscaldamento IP ti aiutano ad aumentare progressivamente il volume di invio per creare la reputazione del mittente e scopri i passaggi chiave per implementarne uno in Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Con [!DNL Journey Optimizer] è possibile eseguire facilmente flussi di lavoro di riscaldamento IP direttamente dall&#39;interfaccia utente in modo standardizzato ed efficiente, seguendo le best practice per una consegna ottimale. Quando le e-mail vengono inviate utilizzando una nuova piattaforma, i provider di servizi Internet (ISP) possono ritenere sospetti gli indirizzi IP che non vengono riconosciuti. Se grandi quantità di e-mail vengono inviate improvvisamente da un nuovo indirizzo IP, gli ISP spesso le contrassegnano come spam.

Per evitare che i messaggi di una tua nuova campagna vengano contrassegnati come spam, puoi aumentare progressivamente il volume inviato utilizzando la funzione Piano di preparazione IP. Questa nuova opzione del menu **[!UICONTROL Amministrazione]** consente di automatizzare la gestione dei volumi e di semplificare il processo di riscaldamento senza richiedere complesse configurazioni di percorso.

>[!NOTE]
>
>Prima di implementare il piano di riscaldamento IP, scopri nozioni di base sul recapito messaggi, creazione di reputazione e best practice in questa [guida del recapito messaggi di riscaldamento IP](ip-warmup-deliverability-guide.md).

➡️ [Scopri come creare ed eseguire un piano di riscaldamento IP in questo video](#video)

>[!AVAILABILITY]
>
>Questa funzionalità può essere abilitata solo su sandbox di tipo produzione.

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

I passaggi chiave per implementare un piano di preparazione IP sono i seguenti:

1. Crea una o più campagne con l’opzione Preparazione IP abilitata. [Ulteriori informazioni](ip-warmup-campaign.md)

1. Crea un piano di preparazione IP in [!DNL Journey Optimizer] e carica il foglio Excel preparato con l’aiuto del tuo consulente di recapitabilità. [Ulteriori informazioni](ip-warmup-plan.md)

1. Seleziona una campagna per ogni fase del piano e attiva le esecuzioni corrispondenti. [Ulteriori informazioni](ip-warmup-execution.md)

## Video dimostrativo {#video}

Scopri come creare ed eseguire un piano di preparazione IP.

>[!VIDEO](https://video.tv.adobe.com/v/3432637/?learn=on)

>[!NOTE]
>
>Ulteriori informazioni sull&#39;aumento della reputazione e-mail con la preparazione degli indirizzi IP nella [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it).

## Risorse aggiuntive {#additional-resources}

Esplora questi utili post di blog per una guida più approfondita sul riscaldamento dell’IP:

* [Guida al recapito messaggi di Adobe Journey Optimizer: da Zero Reputation a Inbox Hero](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950) - Guida completa sui concetti fondamentali della reputazione, calendari di riscaldamento, monitoraggio e procedure consigliate per la risoluzione dei problemi.

* [Informazioni su come impostare il riscaldamento dell&#39;IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949): scopri le nozioni di base per la configurazione dei piani di riscaldamento dell&#39;IP e le best practice per una corretta implementazione.

* [Funzionalità avanzate nei piani di riscaldamento IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958) - Scopri le funzionalità avanzate e i controlli granulari per ottimizzare la tua strategia di riscaldamento IP.

* [Risoluzione dei problemi di riscaldamento dell&#39;IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952) - Trova soluzioni ai problemi comuni, ad esempio ritardi del pubblico, e scopri i meccanismi di esecuzione intelligente dei tentativi.
