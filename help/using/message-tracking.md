---
title: Track your messages
description: Scopri come aggiungere collegamenti e tenere traccia dei messaggi inviati
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: c6db89093e1ec5b7d9fe084cec58b8b7664c6ab2
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 3%

---

# Aggiungere link e tenere traccia dei messaggi {#tracking}

Utilizzo [!DNL Journey Optimizer] aggiungere collegamenti al contenuto e tenere traccia dei messaggi inviati per monitorare il comportamento dei destinatari.

## Abilita tracciamento {#enable-tracking}

You can enable tracking at the email message level by checking the **[!UICONTROL Open Tracking for email]** and/or **[!UICONTROL Click Tracking for email]** options when [creating your message](create-message.md).

![](assets/message-tracking.png)

>[!NOTE]
>
>Entrambe le opzioni sono abilitate per impostazione predefinita.

In questo modo puoi tenere traccia del comportamento dei destinatari attraverso:

* **[!UICONTROL Open Tracking for email]**: Messaggi aperti.
* **[!UICONTROL Click Tracking for email]**: Fai clic sui collegamenti in un’e-mail.

## Inserire collegamenti {#insert-links}

Durante la progettazione di un messaggio, puoi aggiungere collegamenti al contenuto.

>[!NOTE]
>
>Quando [tracciamento abilitato](#enable-tracking), vengono tracciati tutti i collegamenti inclusi nel contenuto del messaggio.

Per inserire collegamenti nel contenuto delle e-mail, segui la procedura seguente:

1. Seleziona un elemento e fai clic su **[!UICONTROL Insert link]** dalla barra degli strumenti contestuale.

   ![](assets/message-tracking-insert-link.png)

1. Scegli il tipo di collegamento che desideri creare:

   * **[!UICONTROL External link]**: Inserisci un collegamento a un URL esterno.

   * **[!UICONTROL Unsubscription link]**: Inserisci un collegamento per non ricevere comunicazioni dal tuo marchio. Ulteriori informazioni sulla gestione delle rinunce sono disponibili in [questa sezione](consent.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Inserisci un collegamento per visualizzare il contenuto dell’e-mail in un browser web. [Ulteriori informazioni](#mirror-page).

   * **[!UICONTROL Opt-out]**: Inserisci un collegamento per consentire agli utenti di annullare rapidamente l’iscrizione alle tue comunicazioni senza dover confermare l’rinuncia. [Ulteriori informazioni](#one-click-opt-out-link).

   ![](assets/message-tracking-links.png)

1. Puoi personalizzare i tuoi collegamenti. Ulteriori informazioni sugli URL personalizzati in [questa sezione](personalization/personalization-syntax.md#perso-urls).

1. Salva le modifiche.

1. Una volta creato il collegamento, puoi comunque modificarlo dal **[!UICONTROL Component settings]** a destra.

   * Fai clic sull’icona a forma di matita per modificare il collegamento.
   * Puoi scegliere di sottolineare il collegamento o meno selezionando l’opzione corrispondente.

   ![](assets/message-tracking-link-settings.png)

## Collegamento a una pagina speculare {#mirror-page}

La pagina speculare è una pagina HTML accessibile online tramite un browser web. Il contenuto è identico a quello dell’e-mail.

Per aggiungere un collegamento a una pagina speculare nell’e-mail, [inserire un collegamento](#insert-links) e seleziona **[!UICONTROL Mirror page]** come tipo di collegamento.

![](assets/message-tracking-mirror-page.png)

La pagina speculare viene creata automaticamente.

>[!NOTE]
>
>Non puoi modificare il collegamento generato automaticamente.

Una volta inviata l’e-mail, quando i destinatari fanno clic sul collegamento della pagina speculare, il contenuto dell’e-mail viene visualizzato nel browser Web predefinito.

>[!NOTE]
>
>In [prova](preview.md#send-proofs) inviato ai profili di test, il collegamento alla pagina speculare non è attivo. Viene attivato solo nei messaggi finali.

Il periodo di conservazione per una pagina speculare è di 60 giorni. Dopo tale ritardo, la pagina speculare non sarà più disponibile.

## Collegamento di rinuncia con un clic {#one-click-opt-out-link}

Per consentire ai destinatari di annullare rapidamente l’iscrizione alla ricezione di comunicazioni dal brand, puoi inserire un collegamento di rinuncia con un solo clic nel contenuto dell’e-mail. Questa capacità impedisce agli utenti di essere reindirizzati a una pagina di destinazione in cui devono confermare la propria scelta, il che velocizza il processo di annullamento dell’abbonamento.

Per aggiungere un collegamento di rinuncia all’e-mail, segui la procedura seguente.

1. [Inserire un collegamento](#insert-links) e seleziona **[!UICONTROL Opt-out]** come tipo di collegamento.

   ![](assets/message-tracking-opt-out.png)

1. Seleziona la modalità di applicazione della rinuncia: a livello di canale, identità o abbonamento.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: La rinuncia si applica ai messaggi futuri inviati alla destinazione del profilo (ad esempio l’indirizzo e-mail) per il canale corrente. Se più destinazioni sono associate a un profilo, la rinuncia si applica a tutte le destinazioni (ad esempio gli indirizzi e-mail) nel profilo di quel canale.
   * **[!UICONTROL Identity]**: The opt-out applies to future messages sent to the specific target (i.e. email address) being used for the current message.
   * **[!UICONTROL Subscription]**: La rinuncia si applica ai messaggi futuri associati a un elenco di sottoscrizione specifico. Questa opzione può essere selezionata solo se il messaggio corrente è associato a un elenco di sottoscrizioni.

1. Enter the URL of the landing page where the user will be redirected once unsubscribed. Questa pagina è disponibile solo per confermare che la rinuncia è stata eseguita correttamente.

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puoi personalizzare i tuoi collegamenti. Ulteriori informazioni sugli URL personalizzati in [questa sezione](personalization/personalization-syntax.md).

1. Salva le modifiche.

Una volta inviato il messaggio, se i destinatari fanno clic sul collegamento di rinuncia, vengono immediatamente esclusi.

## Gestire il tracciamento {#manage-tracking}

La [E-mail Designer](create-email-content.md) consente di gestire gli URL tracciati, ad esempio modificando il tipo di tracciamento per ogni collegamento.

1. Fai clic sul pulsante **[!UICONTROL Links]** per visualizzare l’elenco di tutti gli URL del contenuto che verranno tracciati.

   Questo elenco consente di avere una visualizzazione centralizzata e di individuare ogni URL nel contenuto dell’e-mail.

1. Per modificare un collegamento, fai clic sull’icona a forma di matita corrispondente.

   ![](assets/message-tracking-edit-links.png)

1. Puoi modificare la **[!UICONTROL Tracking Type]** se necessario:


   ![](assets/message-tracking-edit-a-link.png)

   Per ogni URL tracciato, puoi impostare la modalità di tracciamento su uno dei seguenti valori:

   * **[!UICONTROL Tracked]**: Attiva il tracciamento su questo URL.
   * **[!UICONTROL Opt out]**: Considera questo URL come un URL di rinuncia o di annullamento dell’abbonamento.
   * **[!UICONTROL Mirror page]**: Considers this URL is a mirror page URL.
   * **[!UICONTROL Never]**: Non attiva mai il tracciamento di questo URL. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

The number of messages that have been opened and the number of links that have been clicked are listed in the [Executions tab](message-monitoring.md).

Reporting on openings and clicks is available in the [Email Live report](reports/email-live-report.md) and in the [Email Global report](reports/email-global-report.md).
