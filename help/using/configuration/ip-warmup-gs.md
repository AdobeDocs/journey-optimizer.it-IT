---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai piani di preparazione IP
description: Scopri come implementare un piano di preparazione IP
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: IP, recapitabilità
hide: true
hidefromtoc: true
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: 82c189545ab4f37a2e4b1044c0b8cfeb539aed13
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 100%

---

# Introduzione ai piani di preparazione IP {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* **[Introduzione alla preparazione dell’IP](ip-warmup-gs.md)**
* [Creare campagne di preparazione IP](ip-warmup-campaign.md)
* [Creare un piano di preparazione IP](ip-warmup-plan.md)
* [Eseguire il piano di preparazione IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La funzione di preparazione IP è attualmente disponibile come versione beta solo per alcuni utenti. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.

Con [!DNL Journey Optimizer], è possibile eseguire facilmente flussi di lavoro di preparazione IP direttamente dall’interfaccia utente in modo standardizzato ed efficiente, seguendo le best practice per una recapitabilità ottimale.

>[!CAUTION]
>
>Questa funzione si applica solo al canale E-mail.

Quando le e-mail vengono inviate utilizzando una nuova piattaforma, i provider di servizi Internet (ISP) possono ritenere sospetti gli indirizzi IP che non vengono riconosciuti. Se grandi quantità di e-mail vengono inviate improvvisamente da un nuovo indirizzo IP, gli ISP spesso le contrassegnano come spam.

Per evitare che i messaggi di una tua nuova campagna vengano contrassegnati come spam, puoi aumentare progressivamente il volume inviato utilizzando la funzione Piano di preparazione IP. Questa nuova opzione disponibile nel menu **[!UICONTROL Amministrazione]** agevola questo compito in modo consolidato, senza dover creare complessi percorsi giornalieri. Facilitando lo sviluppo della fase iniziale, consente di ridurre il tasso complessivo di indirizzi non validi.

>[!NOTE]
>
>Per ulteriori informazioni su come aumentare la reputazione e-mail con la preparazione degli indirizzi IP, consulta la [Guida alle best practice per la recapitabilità](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it).

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
