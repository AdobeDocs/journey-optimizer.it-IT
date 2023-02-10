---
solution: Journey Optimizer
product: journey optimizer
title: Avvisi
description: Scopri come gestire gli avvisi
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 731eb471c5765b0d3efbc9354c64c32cc5e56516
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 8%

---

# Guida introduttiva agli avvisi {#alerts}

Journey Optimizer sfrutta le funzionalità di avvisi di Adobe Experience Platform. Questo consente di accedere agli avvisi del sistema tramite l’interfaccia utente. Puoi visualizzare gli avvisi disponibili e abbonarti. Quando viene raggiunto un determinato insieme di condizioni nelle operazioni (ad esempio un potenziale problema in caso di superamento di una soglia da parte del sistema), i messaggi di avviso vengono inviati a tutti gli utenti dell’organizzazione che vi si sono abbonati. Questi messaggi possono ripetersi in un intervallo di tempo predefinito fino alla risoluzione dell’avviso.

Ulteriori informazioni sugli avvisi in Adobe Experience Platform [documentazione](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=it).
Per informazioni su come sottoscrivere e configurare gli avvisi, consulta questo articolo [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

Nel menu a sinistra, sotto **Amministrazione**, fai clic su **Avvisi**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Se si verifica un comportamento imprevisto, una notifica di avviso viene inviata agli abbonati all’avviso tramite e-mail, nell’angolo in alto a destra dell’interfaccia.

<!--![](assets/alerts2.png)-->

Quando [visualizzazione delle regole di avviso nell’interfaccia utente di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), puoi abbonarti a ogni regola singolarmente. Durante l’abbonamento agli avvisi tramite [Notifiche evento I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)Tuttavia, le regole di avviso sono organizzate in diversi pacchetti di abbonamento.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
