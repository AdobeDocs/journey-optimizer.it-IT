---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio e-mail
description: Scopri come creare un’e-mail in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 4%

---

# Creare un messaggio e-mail {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Creazione di e-mail"
>abstract="Definisci i parametri e-mail in tre semplici passaggi."

Per creare un messaggio e-mail in [!DNL Journey Optimizer], segui i passaggi seguenti.

## Creare un messaggio e-mail in un percorso o in una campagna {#create-email-journey-campaign}

Aggiungi un **[!UICONTROL E-mail]** a un percorso o a una campagna e segui i passaggi riportati di seguito in base al tuo caso.

>[!BEGINTABS]

>[!TAB Aggiungere un’e-mail a un percorso]

1. Apri il percorso, quindi trascina e rilascia una **[!UICONTROL E-mail]** attività dal **[!UICONTROL Azioni]** della palette.

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria).

1. Scegli la [superficie e-mail](email-settings.md) da utilizzare.

   ![](assets/email_journey.png)

>[!NOTE]
>
>Se invii un’e-mail da un percorso, puoi sfruttare la funzione di ottimizzazione del momento di invio di Adobe Journey Optimizer per prevedere il momento migliore per l’invio del messaggio per massimizzare il coinvolgimento in base ai tassi storici di apertura e clic. [Scopri come utilizzare l’ottimizzazione per i tempi di invio](../building-journeys/journeys-message.md#send-time-optimization)

Per ulteriori informazioni su come configurare un percorso, consulta [questa pagina](../building-journeys/journey-gs.md).

>[!TAB Aggiungere un messaggio e-mail a una campagna]

1. Crea una nuova campagna pianificata o attivata dall’API e seleziona **[!UICONTROL E-mail]** come tua azione.

1. Scegli la [superficie e-mail](email-settings.md) da utilizzare.

   ![](assets/email_campaign.png)

1. Fai clic su **[!UICONTROL Crea]**.

1. Completa i passaggi per creare una campagna e-mail, ad esempio le proprietà della campagna, [pubblico](../segment/about-segments.md)e [pianificazione](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Definire il contenuto dell’e-mail {#define-email-content}

1. Dalla schermata di configurazione del percorso o della campagna, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** per configurare il contenuto dell’e-mail. [Ulteriori informazioni](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. In **[!UICONTROL Intestazione]** della sezione **[!UICONTROL Modifica contenuto]** schermo, **[!UICONTROL Nome mittente]**, **[!UICONTROL Da e-mail]** e **[!UICONTROL CCN]** Il campo proviene dall’area e-mail selezionata. [Ulteriori informazioni](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. È possibile aggiungere un oggetto. Digita testo normale direttamente nel campo corrispondente o utilizza il [Editor espressioni](../personalization/personalization-build-expressions.md) per personalizzare l’oggetto.

1. Fai clic sul pulsante **[!UICONTROL Modifica corpo del messaggio e-mail]** per iniziare a creare il contenuto utilizzando il pulsante [!DNL Journey Optimizer] E-mail Designer. [Ulteriori informazioni](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. Se ti trovi in una campagna, puoi anche fare clic sul pulsante **[!UICONTROL Editor di codice]** per codificare il proprio contenuto in HTML semplice utilizzando la finestra a comparsa visualizzata.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Se il contenuto è già stato creato o importato tramite E-mail Designer, verrà visualizzato in HTML.

## Controllare gli avvisi {#check-email-alerts}

Durante la progettazione dei messaggi, gli avvisi vengono visualizzati nell’interfaccia (in alto a destra dello schermo) quando mancano le impostazioni chiave.

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>In caso contrario, non è stato rilevato alcun avviso.

Le impostazioni e gli elementi controllati dal sistema sono elencati di seguito. Troverai anche informazioni su come adattare la configurazione per risolvere i problemi corrispondenti.

Possono verificarsi due tipi di avvisi:

* **Avvisi** consulta raccomandazioni e best practice, ad esempio:

   * **[!UICONTROL Il collegamento di rinuncia non è presente nel corpo dell’e-mail]**: è consigliabile aggiungere un collegamento per l’annullamento dell’abbonamento al corpo dell’e-mail. Scopri come configurarlo in [questa sezione](../privacy/opt-out.md#opt-out-management).

      >[!NOTE]
      >
      >I messaggi e-mail di tipo marketing devono includere un collegamento di rinuncia, che non è necessario per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]**) è definita nella [superficie del canale](email-settings.md#email-type) livello e quando [creazione del messaggio](#create-email-journey-campaign) da un percorso o una campagna.

   * **[!UICONTROL La versione del testo di HTML è vuota]**: non dimenticare di definire una versione testuale del corpo dell’e-mail, in quanto verrà utilizzata quando non è possibile visualizzare il contenuto di HTML. Scopri come creare la versione di testo in [questa sezione](text-version-email.md).

   * **[!UICONTROL Il collegamento vuoto è presente nel corpo dell’e-mail]**: controlla che tutti i collegamenti presenti nell’e-mail siano corretti. Scopri come gestire contenuti e collegamenti in [questa sezione](content-from-scratch.md).

   * **[!UICONTROL La dimensione dell’e-mail ha superato il limite di 100 KB]**: per una consegna ottimale, assicurati che la dimensione dell’e-mail non superi i 100 KB. Scopri come modificare il contenuto delle e-mail in [questa sezione](content-from-scratch.md).

* **Errori** impedisce il test o l’attivazione del percorso o della campagna purché non siano risolti, ad esempio:

   * **[!UICONTROL Riga oggetto mancante]**: la riga dell’oggetto dell’e-mail è obbligatoria. Scopri come definirlo e personalizzarlo in [questa sezione](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL La versione del messaggio e-mail è vuota]**: questo errore viene visualizzato quando il contenuto dell’e-mail non è stato configurato. Scopri come progettare il contenuto delle e-mail in [questa sezione](get-started-email-design.md).

   * **[!UICONTROL La superficie non esiste]**: non puoi utilizzare il messaggio se la superficie selezionata viene eliminata dopo la creazione del messaggio. Se si verifica questo errore, seleziona un’altra superficie nel messaggio **[!UICONTROL Proprietà]**. Ulteriori informazioni sulle superfici dei canali in [questa sezione](../configuration/channel-surfaces.md).


>[!CAUTION]
>
>Per poter testare o attivare il percorso o la campagna utilizzando l’e-mail, devi risolvere tutti **errore** avvisi

## Anteprima e invio del messaggio e-mail

Una volta definito il contenuto del messaggio, puoi visualizzarlo in anteprima per controllare il rendering del messaggio e-mail e controllare le impostazioni di personalizzazione con i profili di test. [Ulteriori informazioni](preview.md)

![](assets/email_designer_edit_simulate.png)

Quando il tuo messaggio e-mail è pronto, completa la configurazione del tuo [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md), e attivalo per inviare il messaggio.

>[!NOTE]
>
>Per tenere traccia del comportamento dei destinatari tramite le aperture e/o le interazioni e-mail, assicurati che le opzioni dedicate nel **[!UICONTROL Tracking]** la sezione è abilitata nel percorso [attività e-mail](../building-journeys/journeys-message.md) o nell’e-mail [campagna](../campaigns/create-campaign.md).<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] Expression editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

