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
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Introduzione agli avvisi {#alerts}

Durante la creazione di percorsi e campagne, utilizza il pulsante **Avvisi** per verificare e risolvere gli errori prima di eseguirli o pubblicarli. Scopri come risolvere i problemi dei percorsi in [questa pagina](../building-journeys/troubleshooting.md). Scopri come rivedere le campagne in [questa pagina](../campaigns/review-activate-campaign.md).

È inoltre possibile abbonarsi agli avvisi di sistema di Adobe Journey Optimizer come descritto in questa pagina.

## Accedere e sottoscrivere gli avvisi {#alerting-capabilities}

In caso di errore, puoi ricevere gli avvisi di sistema nel centro notifiche di Journey Optimizer (avvisi in-app) e/o ricevere un messaggio e-mail.

Dal menu **Avvisi**, puoi visualizzare gli avvisi disponibili e abbonarti. Quando viene raggiunto un determinato set di condizioni nelle operazioni (ad esempio un potenziale problema quando il sistema supera una soglia), i messaggi di avviso vengono inviati a tutti gli utenti dell’organizzazione che si sono iscritti a tali condizioni.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Ulteriori informazioni sugli avvisi in Adobe Experience Platform sono disponibili nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=it){target="_blank"}.

Nel menu a sinistra, nella sezione **Amministrazione**, fare clic su **Avvisi**. Sono disponibili due avvisi preconfigurati per Journey Optimizer: l&#39;avviso [Errore azione personalizzata Percorso](#alert-custom-actions) e l&#39;avviso [Attivatore lettura pubblico non riuscito](#alert-read-audiences). Questi avvisi sono descritti di seguito.

È possibile sottoscrivere ogni singolo avviso dall&#39;interfaccia utente selezionando l&#39;opzione **Sottoscrivi** dalla dashboard **Avvisi**. Utilizza lo stesso metodo per annullare l’abbonamento.

![](assets/alert-subscribe.png)

È inoltre possibile sottoscrivere avvisi tramite [Notifiche evento I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}. Le regole di avviso sono organizzate in pacchetti di abbonamento diversi. Gli abbonamenti agli eventi corrispondenti agli avvisi specifici di Journey Optimizer sono descritti di seguito.

Se si verifica un comportamento imprevisto, viene inviata una notifica di avviso agli abbonati. In base alle preferenze utente, gli avvisi vengono inviati tramite e-mail e/o direttamente all’interno del centro notifiche di Journey Optimizer, nell’angolo in alto a destra dell’interfaccia utente. Per impostazione predefinita, è abilitato solo l’avviso in-app. Per abilitare gli avvisi e-mail, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.

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

Il nome della sottoscrizione all&#39;evento di I/O corrispondente all&#39;avviso di azione personalizzata è **Errore Percorso azione personalizzata**.

## Attivatore Read Audience Non Riuscito {#alert-read-audiences}

Questo avviso ti avvisa se un&#39;attività **Read Audience** non ha elaborato alcun profilo 10 minuti dopo l&#39;ora di esecuzione pianificata. Questo errore può essere causato da problemi tecnici o perché il pubblico è vuoto.

![](assets/alerts1.png)

Gli avvisi sulle attività **Read Audience** si applicano solo ai percorsi ricorrenti. **Le attività Read Audience** nei percorsi live che hanno una pianificazione per l&#39;esecuzione di **Once** o **As soon as possible** vengono ignorate.

Gli avvisi in **Read Audience** vengono risolti quando un profilo entra nel nodo **Read Audience**.

Il nome della sottoscrizione all&#39;evento di I/O corrispondente all&#39;avviso **Read Audience Trigger Unsuccess** è **Percorso di ritardo, errori e errori di lettura del pubblico**.

## Risoluzione dei problemi {#alert-troubleshooting}

Per risolvere i problemi relativi agli avvisi di **Read Audience**, controlla il numero di tipi di pubblico nell&#39;interfaccia di Experience Platform.

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

Per risolvere i problemi relativi agli avvisi di **Azione personalizzata**:

* Controlla l’azione personalizzata utilizzando la modalità di test in un altro percorso:

  ![](assets/alert-troubleshooting-2.png)

* Controlla il report di percorso per visualizzare i motivi dell’errore durante l’azione.

  ![](assets/alert-troubleshooting-3.png)

* Controlla il tuo stepEvents di percorso per cercare ulteriori informazioni su &quot;failureReason&quot;.

* Controlla la configurazione dell’azione personalizzata e verifica che l’autenticazione sia ancora valida. Esegui un controllo manuale con Postman, ad esempio.
