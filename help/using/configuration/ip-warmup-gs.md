---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai piani di riscaldamento IP
description: Scopri come implementare un piano di riscaldamento IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pool, gruppo, sottodomini, recapito messaggi
hide: true
hidefromtoc: true
source-git-commit: 53be033ff0474cbafff71ed36194c18627234fd4
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---

# Introduzione ai piani di riscaldamento IP {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione di guida:

* **[Introduzione al riscaldamento dell’IP](ip-warmup-gs.md)**
* [Creare campagne di riscaldamento IP](ip-warmup-campaign.md)
* [Creare un piano di riscaldamento IP](ip-warmup-plan.md)
* [Eseguire il piano di riscaldamento IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La funzione di riscaldamento IP è attualmente disponibile come versione beta solo per alcuni utenti. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.

Con [!DNL Journey Optimizer], è possibile eseguire facilmente flussi di lavoro di riscaldamento IP direttamente dall’interfaccia utente in modo standardizzato ed efficiente, seguendo le best practice per una consegna ottimale.

>[!CAUTION]
>
>Questa funzione si applica solo al canale e-mail.

Quando le e-mail vengono inviate utilizzando una nuova piattaforma, i provider di servizi Internet (ISP) sospettano che gli indirizzi IP non siano riconosciuti. Se grandi quantità di e-mail vengono inviate improvvisamente, gli ISP spesso le contrassegnano come spam.

Per evitare di essere contrassegnati come spam, puoi aumentare progressivamente il volume inviato utilizzando la funzione del piano di riscaldamento IP. Una nuova opzione in **[!UICONTROL Amministrazione]** consente di farlo in modo più fluido invece di creare percorsi giornalieri complessi. Ciò dovrebbe garantire un regolare sviluppo della fase di avvio e consentirti di ridurre il tasso complessivo di indirizzi non validi.

>[!NOTE]
>
>Ulteriori informazioni su come aumentare la reputazione e-mail con la preparazione degli indirizzi IP nel [Guida alle best practice per la consegna](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

I passaggi chiave per implementare un piano di riscaldamento IP sono i seguenti:

1. Devi innanzitutto creare una o più campagne con l’opzione di riscaldamento IP abilitata. [Ulteriori informazioni](ip-warmup-campaign.md) <!--this is usually done by a marketer persona??)-->

1. Crea un piano di riscaldamento IP e carica il tuo piano. [Ulteriori informazioni](ip-warmup-plan.md) <!--this is usually done by a deliverability consultant??-->

1. Seleziona una campagna per ogni fase del piano e attiva le esecuzioni corrispondenti. [Ulteriori informazioni](ip-warmup-running.md)
