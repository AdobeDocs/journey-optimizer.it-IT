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
source-git-commit: 01bc2351b08fc7226c5e5633820f476c8621e404
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 1%

---

# Introduzione agli avvisi {#alerts}

## Funzionalità di avviso {#alerting-capabilities}

Puoi accedere agli avvisi di sistema tramite l’interfaccia utente o ricevere un messaggio e-mail in caso di errore. Dalla sezione **Avvisi** , puoi visualizzare gli avvisi disponibili e abbonarti. Quando viene raggiunto un determinato set di condizioni nelle operazioni (ad esempio un potenziale problema quando il sistema supera una soglia), i messaggi di avviso vengono inviati a tutti gli utenti dell’organizzazione che si sono iscritti a tali condizioni.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Ulteriori informazioni sugli avvisi in Adobe Experience Platform in [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=it){target="_blank"}.

Nel menu a sinistra, sotto **Amministrazione**, fai clic su **Avvisi**. Per Journey Optimizer sono disponibili due avvisi preconfigurati: [Azione personalizzata percorso non riuscita](#alert-custom-actions) avviso e [Trigger di lettura segmento non riuscito](#alert-read-audiences) attenzione. Questi avvisi sono descritti di seguito.

È possibile iscriversi a ogni avviso singolarmente dall’interfaccia utente, selezionando la **Abbonati** opzione dalla **Avvisi** dashboard. Utilizza lo stesso metodo per annullare l’abbonamento.

![](assets/alert-subscribe.png)

Puoi anche abbonarti agli avvisi tramite [Notifiche di eventi di I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}Tuttavia, le regole di avviso sono organizzate in pacchetti di abbonamento diversi.

Se si verifica un comportamento imprevisto, viene inviata una notifica di avviso agli abbonati. In base alle preferenze utente, gli avvisi vengono inviati tramite e-mail o direttamente all’interno del centro notifiche di Journey Optimizer, nell’angolo in alto a destra dell’interfaccia utente.

Quando viene risolto un avviso, gli abbonati ricevono una notifica &quot;Risolto&quot;.

>[!WARNING]
>
>Gli avvisi specifici di Adobe Journey Optimizer si applicano solo a **live** percorsi. Gli avvisi non vengono attivati per i percorsi in modalità di test.

## Azione personalizzata percorso non riuscita {#alert-custom-actions}

Questo avviso ti avvisa se un’azione personalizzata non riesce. Riteniamo che si sia verificato un errore in cui si è verificato più dell’1% di errori in una specifica azione personalizzata negli ultimi 5 minuti. Questo viene valutato ogni 30 secondi.

![](assets/alerts-custom-action.png)

Gli avvisi sulle azioni personalizzate vengono risolti quando, negli ultimi 5 minuti:

* l’azione personalizzata non contiene errori (o errori al di sotto della soglia dell’1%),

* In alternativa, nessun profilo ha raggiunto l’azione personalizzata.

Il nome dell’abbonamento all’evento di I/O corrispondente all’avviso di azione personalizzato è **Azione personalizzata percorso non riuscita**.

## Trigger di lettura segmento non riuscito {#alert-read-audiences}

Questo avviso ti avvisa se **Leggi segmento** l’attività non ha elaborato alcun profilo 10 minuti dopo l’ora di esecuzione pianificata. Questo errore può essere causato da problemi tecnici o perché il pubblico è vuoto.

![](assets/alerts1.png)

Avvisi su **Leggi segmento** Le attività sono applicabili solo ai percorsi ricorrenti. **Leggi segmento** attività in percorsi live che hanno una pianificazione da eseguire **Una volta** o **Appena possibile** vengono ignorati.

Avvisi su **Leggi segmento** vengono risolti quando un profilo entra in **Leggi segmento** nodo.

Il nome dell’abbonamento all’evento di I/O corrispondente al **Leggi segmento** l&#39;avviso è **Ritardi, errori ed errori percorsi nella lettura del segmento**.
