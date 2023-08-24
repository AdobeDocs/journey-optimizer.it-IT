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
source-git-commit: 6386a5ee5a0d1f221beab67f43636c599531736a
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 4%

---

# Introduzione agli avvisi {#alerts}

Journey Optimizer sfrutta le funzionalità di avviso di Adobe Experience Platform. Questo consente di accedere agli avvisi di sistema tramite l’interfaccia utente. Puoi visualizzare gli avvisi disponibili e abbonarti.

Quando viene raggiunto un determinato set di condizioni nelle operazioni (ad esempio un potenziale problema quando il sistema supera una soglia), i messaggi di avviso vengono inviati a tutti gli utenti dell’organizzazione che si sono iscritti a tali condizioni.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Ulteriori informazioni sugli avvisi in Adobe Experience Platform [documentazione](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=it).

Per informazioni su come abbonarsi agli avvisi e configurarli, consulta questa sezione [pagina](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>Alcune modifiche progettuali sono in corso per l’avviso &quot;Attivazione del pubblico non riuscita&quot;, pertanto per il momento questo avviso è in pausa ed è stato temporaneamente rimosso dall’interfaccia utente. Una volta rilasciate queste modifiche, l’avviso verrà nuovamente visualizzato e potrai abbonarti.

Nel menu a sinistra, sotto **Amministrazione**, fai clic su **Avvisi**. È disponibile un avviso preconfigurato per Journey Optimizer. Questo avviso ti avvisa se un’azione personalizzata non riesce. Riteniamo che si sia verificato un errore in cui si è verificato più dell’1% di errori in una specifica azione personalizzata negli ultimi 5 minuti. Questo viene valutato ogni 30 secondi.

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Se si verifica un comportamento imprevisto, viene inviata una notifica di avviso agli abbonati dell’avviso tramite e-mail o direttamente all’interno di Journey Optimizer, nell’angolo in alto a destra dell’interfaccia, in base alle preferenze dell’utente.

Quando viene risolto un avviso, viene visualizzata una notifica &quot;Risolto&quot;. Per l’avviso di azione personalizzata, questo può accadere per due motivi:
* Negli ultimi 5 minuti non si sono verificati errori nell’azione personalizzata (o errori al di sotto della soglia dell’1%).
* Nessun profilo ha raggiunto l&#39;azione personalizzata.

Quando [visualizzazione delle regole di avviso nell’interfaccia utente di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), puoi abbonarti a ogni regola singolarmente. Quando si sottoscrivono avvisi tramite [Notifiche di eventi di I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)Tuttavia, le regole di avviso sono organizzate in pacchetti di abbonamento diversi. Il nome dell’abbonamento all’evento di I/O corrispondente all’avviso di azione personalizzata è: &quot;Errore Percorso azione personalizzata&quot;.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>Questi avvisi si applicano solo ai percorsi live. Gli avvisi non verranno attivati per i percorsi in modalità di test.

