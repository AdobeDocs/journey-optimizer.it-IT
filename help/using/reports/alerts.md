---
solution: Journey Optimizer
product: journey optimizer
title: Avvisi
description: Scopri come gestire gli avvisi
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: ddf9465fb940706fb38dc05038336ac22abecbc0
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Introduzione agli avvisi {#alerts}

## Accedere e sottoscrivere gli avvisi {#alerting-capabilities}

In caso di errore, puoi ricevere gli avvisi di sistema nel centro notifiche di Journey Optimizer (avvisi in-app) e/o ricevere un messaggio e-mail.

Dalla sezione **Avvisi** , puoi visualizzare gli avvisi disponibili e abbonarti. Quando viene raggiunto un determinato set di condizioni nelle operazioni (ad esempio un potenziale problema quando il sistema supera una soglia), i messaggi di avviso vengono inviati a tutti gli utenti dell’organizzazione che si sono iscritti a tali condizioni.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Ulteriori informazioni sugli avvisi in Adobe Experience Platform in [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=it){target="_blank"}.

Nel menu a sinistra, sotto **Amministrazione**, fai clic su **Avvisi**. Per Journey Optimizer sono disponibili due avvisi preconfigurati: [Azione personalizzata percorso non riuscita](#alert-custom-actions) avviso e [Attivatore Read Audience Non Riuscito](#alert-read-audiences) attenzione. Questi avvisi sono descritti di seguito.

È possibile iscriversi a ogni avviso singolarmente dall’interfaccia utente, selezionando la **Abbonati** opzione dalla **Avvisi** dashboard. Utilizza lo stesso metodo per annullare l’abbonamento.

![](assets/alert-subscribe.png)

Puoi anche abbonarti agli avvisi tramite [Notifiche di eventi di I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}. Le regole di avviso sono organizzate in pacchetti di abbonamento diversi. Gli abbonamenti agli eventi corrispondenti agli avvisi specifici di Journey Optimizer sono descritti di seguito.

Se si verifica un comportamento imprevisto, viene inviata una notifica di avviso agli abbonati. In base alle preferenze utente, gli avvisi vengono inviati tramite e-mail e/o direttamente all’interno del centro notifiche di Journey Optimizer, nell’angolo in alto a destra dell’interfaccia utente. Per impostazione predefinita, è abilitato solo l’avviso in-app. Per abilitare gli avvisi e-mail, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.

Quando viene risolto un avviso, gli abbonati ricevono una notifica &quot;Risolto&quot;.

>[!CAUTION]
>
>Gli avvisi specifici di Adobe Journey Optimizer si applicano solo a **live** percorsi. Gli avvisi non vengono attivati per i percorsi in modalità di test.

## Azione personalizzata percorso non riuscita {#alert-custom-actions}

Questo avviso ti avvisa se un’azione personalizzata non riesce. Riteniamo che si sia verificato un errore in cui si è verificato più dell’1% di errori in una specifica azione personalizzata negli ultimi 5 minuti. Questo viene valutato ogni 30 secondi.

![](assets/alerts-custom-action.png)

Gli avvisi sulle azioni personalizzate vengono risolti quando, negli ultimi 5 minuti:

* l’azione personalizzata non contiene errori (o errori al di sotto della soglia dell’1%),

* oppure, nessun profilo ha raggiunto l’azione personalizzata.

Il nome dell’abbonamento all’evento di I/O corrispondente all’avviso di azione personalizzato è **Azione personalizzata percorso non riuscita**.

## Attivatore Read Audience Non Riuscito {#alert-read-audiences}

Questo avviso ti avvisa se **Read Audience** l’attività non ha elaborato alcun profilo 10 minuti dopo l’ora di esecuzione pianificata. Questo errore può essere causato da problemi tecnici o perché il pubblico è vuoto.

![](assets/alerts1.png)

Avvisi su **Read Audience** Le attività sono applicabili solo ai percorsi ricorrenti. **Read Audience** attività in percorsi live che hanno una pianificazione da eseguire **Una volta** o **Appena possibile** vengono ignorati.

Avvisi su **Read Audience** vengono risolti quando un profilo entra in **Read Audience** nodo.

Il nome dell’abbonamento all’evento di I/O corrispondente al **Attivatore Read Audience Non Riuscito** l&#39;avviso è **Ritardi, errori ed errori del pubblico di lettura percorso**.

## Risoluzione dei problemi {#alert-troubleshooting}

Per risolvere i problemi **Read Audience** avvisi, controlla il conteggio del pubblico nell’interfaccia di Experienci Platform.

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

Per risolvere i problemi **Azione personalizzata** avvisi:

* Controlla l’azione personalizzata utilizzando la modalità di test in un altro percorso:

  ![](assets/alert-troubleshooting-2.png)

* Controlla il report di percorso per visualizzare i motivi dell’errore durante l’azione.

  ![](assets/alert-troubleshooting-3.png)

* Controlla il tuo stepEvents di percorso per cercare ulteriori informazioni su &quot;failureReason&quot;.
* Controlla la configurazione dell’azione personalizzata e verifica che l’autenticazione sia ancora valida. Esegui un controllo manuale con Postman, ad esempio.
