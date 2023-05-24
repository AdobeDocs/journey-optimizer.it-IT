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
source-git-commit: 1832f3395b07580e62f32c886a0a4256267b2970
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 6%

---

# Introduzione agli avvisi {#alerts}

Journey Optimizer sfrutta le funzionalità di avviso di Adobe Experience Platform. Questo consente di accedere agli avvisi di sistema tramite l’interfaccia utente. Puoi visualizzare gli avvisi disponibili e abbonarti.

Quando viene raggiunto un determinato set di condizioni nelle operazioni (ad esempio un potenziale problema quando il sistema supera una soglia), i messaggi di avviso vengono inviati a tutti gli utenti dell’organizzazione che si sono iscritti a tali condizioni. Questi messaggi possono ripetersi in un intervallo di tempo predefinito fino alla risoluzione dell&#39;avviso.

Ulteriori informazioni sugli avvisi in Adobe Experience Platform [documentazione](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=it).
Per informazioni su come abbonarsi agli avvisi e configurarli, consulta questa sezione [pagina](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>Alcune modifiche progettuali sono in corso per l’avviso &quot;Attivatore Leggi segmento non riuscito&quot;, pertanto per il momento questo avviso è in pausa ed è stato temporaneamente rimosso dall’interfaccia utente. Una volta rilasciate queste modifiche, l’avviso verrà nuovamente visualizzato e potrai abbonarti.

Nel menu a sinistra, sotto **Amministrazione**, fai clic su **Avvisi**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Se si verifica un comportamento imprevisto, viene inviata una notifica di avviso agli abbonati dell’avviso tramite e-mail, nell’angolo in alto a destra dell’interfaccia.

<!--![](assets/alerts2.png)-->


Quando [visualizzazione delle regole di avviso nell’interfaccia utente di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), puoi abbonarti a ogni regola singolarmente. Quando si sottoscrivono avvisi tramite [Notifiche di eventi di I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)Tuttavia, le regole di avviso sono organizzate in pacchetti di abbonamento diversi.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
