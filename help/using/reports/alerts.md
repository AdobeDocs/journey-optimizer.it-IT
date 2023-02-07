---
solution: Journey Optimizer
product: journey optimizer
title: Avvisi
description: Scopri come gestire gli avvisi
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: d5be5ba43351e3143fce7f64878baceb8507d7f8
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 6%

---

# Guida introduttiva agli avvisi {#alerts}

Journey Optimizer sfrutta le funzionalità di avvisi di Adobe Experience Platform. Questo consente di accedere agli avvisi del sistema tramite l’interfaccia utente. Puoi visualizzare gli avvisi disponibili e abbonarti. Quando viene raggiunto un determinato insieme di condizioni nelle operazioni (ad esempio un potenziale problema in caso di superamento di una soglia da parte del sistema), i messaggi di avviso vengono inviati a tutti gli utenti dell’organizzazione che vi si sono abbonati. Questi messaggi possono ripetersi in un intervallo di tempo predefinito fino alla risoluzione dell’avviso.

Ulteriori informazioni sugli avvisi in Adobe Experience Platform [documentazione](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=it).
Per informazioni su come sottoscrivere e configurare gli avvisi, consulta questo articolo [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

Nel menu a sinistra, sotto **Amministrazione**, fai clic su **Avvisi**. È disponibile un avviso preconfigurato per Journey Optimizer. Questo avviso ti avviserà se un nodo del segmento letto non ha elaborato alcun profilo durante l’intervallo di tempo definito.

![](assets/alerts1.png)

Se si verifica un comportamento imprevisto, una notifica di avviso viene inviata agli abbonati all’avviso tramite e-mail, nell’angolo in alto a destra dell’interfaccia.

![](assets/alerts2.png)

Quando [visualizzazione delle regole di avviso nell’interfaccia utente di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), puoi abbonarti a ogni regola singolarmente. Durante l’abbonamento agli avvisi tramite [Notifiche evento I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)Tuttavia, le regole di avviso sono organizzate in diversi pacchetti di abbonamento. Il nome della sottoscrizione dell’evento I/O corrispondente all’avviso Leggi segmento è: &quot;Ritardi, errori ed errori del segmento letti dal Percorso&quot;.

>[!WARNING]
>
>Questi avvisi si applicano solo ai percorsi live. Gli avvisi non verranno attivati per percorsi in modalità di test.
