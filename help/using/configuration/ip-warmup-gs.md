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
source-git-commit: 5e0d683bf52df4992773c6147b9e418241777e5d
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 73%

---

# Introduzione ai piani di preparazione IP {#ip-warmup-gs}

Con [!DNL Journey Optimizer] è possibile eseguire facilmente flussi di lavoro di riscaldamento IP direttamente dall&#39;interfaccia utente in modo standardizzato ed efficiente, seguendo le best practice per una consegna ottimale. Quando le e-mail vengono inviate utilizzando una nuova piattaforma, i provider di servizi Internet (ISP) possono ritenere sospetti gli indirizzi IP che non vengono riconosciuti. Se grandi quantità di e-mail vengono inviate improvvisamente da un nuovo indirizzo IP, gli ISP spesso le contrassegnano come spam.

Per evitare che i messaggi di una tua nuova campagna vengano contrassegnati come spam, puoi aumentare progressivamente il volume inviato utilizzando la funzione Piano di preparazione IP. Questa nuova opzione disponibile nel menu **[!UICONTROL Amministrazione]** agevola questo compito in modo consolidato, senza dover creare complessi percorsi giornalieri.

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

## Video introduttivo {#video}

Scopri come creare ed eseguire un piano di preparazione IP.

>[!VIDEO](https://video.tv.adobe.com/v/3432637/?learn=on)

>[!NOTE]
>
>Ulteriori informazioni sull&#39;aumento della reputazione e-mail con la preparazione degli indirizzi IP nella [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it).
