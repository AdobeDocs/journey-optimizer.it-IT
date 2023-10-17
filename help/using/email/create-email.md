---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio e-mail
description: Scopri come creare un’e-mail in Journey Optimizer
feature: Email
topic: Content Management
role: User
level: Beginner
keywords: creazione, e-mail, avvio, percorso, campagna
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: cd8ce89dd6ed9c60d41e9f83ccfb080bdb4a19f9
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 9%

---

# Creare un messaggio e-mail {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Creazione di e-mail"
>abstract="Definisci i parametri dell’e-mail in tre semplici passaggi."

Per creare un messaggio e-mail in [!DNL Journey Optimizer], segui la procedura indicata di seguito.

## Creazione di un messaggio e-mail in un percorso o in una campagna {#create-email-journey-campaign}

Aggiungi un **[!UICONTROL E-mail]** a un percorso o a una campagna e segui i passaggi riportati di seguito in base al tuo caso.

>[!BEGINTABS]

>[!TAB Aggiungere un messaggio e-mail a un percorso]

1. Apri il percorso, quindi trascina e rilascia una **[!UICONTROL E-mail]** attività da **[!UICONTROL Azioni]** nella palette.

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria).

1. Scegli la [superficie e-mail](email-settings.md) da utilizzare.

   ![](assets/email_journey.png)

   Per impostazione predefinita, il campo è precompilato con l’ultima superficie utilizzata dall’utente per quel canale.

>[!NOTE]
>
>Se invii un’e-mail da un percorso, puoi sfruttare la funzione di ottimizzazione dell’ora di invio di Adobe Journey Optimizer per prevedere il momento migliore per inviare il messaggio in modo da massimizzare il coinvolgimento in base alle percentuali storiche di apertura e clic. [Scopri come utilizzare l’ottimizzazione dell’ora di invio](../building-journeys/journeys-message.md#send-time-optimization)

Per ulteriori informazioni su come configurare un percorso, consulta [questa pagina](../building-journeys/journey-gs.md).

>[!TAB Aggiungere un messaggio e-mail a una campagna]

1. Crea una nuova campagna pianificata o attivata da API e seleziona **[!UICONTROL E-mail]** come azione.

1. Scegli la [superficie e-mail](email-settings.md) da utilizzare.

   ![](assets/email_campaign.png)

1. Fai clic su **[!UICONTROL Crea]**.

1. Completa i passaggi per creare una campagna e-mail, ad esempio le proprietà della campagna, [pubblico](../audience/about-audiences.md), e [pianificazione](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Definire il contenuto dell’e-mail {#define-email-content}

<!-- update the quarry component with right ID value-->

>[!CONTEXTUALHELP]
>id="test_id"
>title="Configurare il contenuto dell’e-mail"
>abstract="Crea il contenuto dell’e-mail. Definisci l’oggetto, quindi usa E-mail Designer per creare e personalizzare il corpo dell’e-mail."

1. Dalla schermata di configurazione del percorso o della campagna, fai clic su **[!UICONTROL Modifica contenuto]** per configurare il contenuto dell’e-mail. [Ulteriori informazioni](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. In **[!UICONTROL Intestazione]** sezione del **[!UICONTROL Modifica contenuto]** schermo, la **[!UICONTROL Nome mittente]**, **[!UICONTROL Da e-mail]** e **[!UICONTROL CCN]** provengono dalla superficie e-mail selezionata. [Ulteriori informazioni](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. È possibile aggiungere un oggetto. Digitare testo normale direttamente nel campo corrispondente oppure utilizzare [Editor espressioni](../personalization/personalization-build-expressions.md) per personalizzare l’oggetto.

1. Fai clic su **[!UICONTROL Modifica corpo dell’e-mail]** per iniziare a creare i contenuti utilizzando [!DNL Journey Optimizer] E-mail Designer. [Ulteriori informazioni](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. Se ti trovi in una campagna, puoi anche fare clic sul pulsante **[!UICONTROL Editor di codice]** per codificare il proprio contenuto in plain HTML utilizzando la finestra a comparsa visualizzata.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Se hai già creato o importato contenuti tramite E-mail Designer, questi verranno visualizzati in HTML.

## Controllare gli avvisi {#check-email-alerts}

Durante la progettazione dei messaggi, gli avvisi vengono visualizzati nell’interfaccia (in alto a destra dello schermo) quando mancano le impostazioni chiave.

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>Se questo pulsante non è visualizzato, non è stato rilevato alcun avviso.

Le impostazioni e gli elementi controllati dal sistema sono elencati di seguito. Troverai anche informazioni su come adattare la configurazione per risolvere i problemi corrispondenti.

Possono verificarsi due tipi di avvisi:

* **Avvisi** consulta consigli e best practice, ad esempio:

   * **[!UICONTROL Il collegamento di rinuncia non è presente nel corpo dell’e-mail]**: è consigliabile aggiungere un collegamento di annullamento all’abbonamento nel corpo dell’e-mail. Scopri come configurarlo in [questa sezione](../privacy/opt-out.md#opt-out-management).

     >[!NOTE]
     >
     >I messaggi e-mail di tipo marketing devono includere un collegamento di rinuncia, che non è necessario per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]**) è definito nella sezione [superficie di canale](email-settings.md#email-type) livello e quando [creazione del messaggio](#create-email-journey-campaign) da un percorso o da una campagna.

   * **[!UICONTROL La versione testo di HTML è vuota]**: non dimenticare di definire una versione di testo del corpo dell’e-mail, in quanto verrà utilizzato quando non è possibile visualizzare il contenuto di HTML. Scopri come creare la versione di testo in [questa sezione](text-version-email.md).

   * **[!UICONTROL Il corpo dell’e-mail contiene un collegamento vuoto]**: verifica che tutti i collegamenti presenti nell’e-mail siano corretti. Scopri come gestire contenuti e collegamenti in [questa sezione](content-from-scratch.md).

   * **[!UICONTROL La dimensione dell’e-mail ha superato il limite di 100 KB]**: per una consegna ottimale, assicurati che le dimensioni dell’e-mail non superino i 100 KB. Scopri come modificare il contenuto delle e-mail in [questa sezione](content-from-scratch.md).

* **Errori** impedisci di testare o attivare il percorso o la campagna finché non vengono risolti, ad esempio:

   * **[!UICONTROL Manca l’oggetto]**: la riga dell’oggetto dell’e-mail è obbligatoria. Scopri come definirlo e personalizzarlo in [questa sezione](create-email.md).

  <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL La versione e-mail del messaggio è vuota]**: questo errore viene visualizzato quando il contenuto dell’e-mail non è stato configurato. Scopri come progettare contenuti e-mail in [questa sezione](get-started-email-design.md).

   * **[!UICONTROL La superficie non esiste]**: non puoi utilizzare il messaggio se la superficie selezionata viene eliminata dopo la creazione del messaggio. Se si verifica questo errore, seleziona un’altra superficie nel messaggio **[!UICONTROL Proprietà]**. Ulteriori informazioni sulle superfici di canale in [questa sezione](../configuration/channel-surfaces.md).

>[!CAUTION]
>
>Per poter testare o attivare il percorso o la campagna tramite l’e-mail, devi risolvere tutto **errore** avvisi.

## Anteprima e invio dell’e-mail

Una volta definito il contenuto del messaggio, puoi visualizzarne l’anteprima per controllare il rendering dell’e-mail e verificare le impostazioni di personalizzazione con i profili di test. [Ulteriori informazioni](preview.md)

![](assets/email_designer_edit_simulate.png)

Quando l’e-mail è pronta, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md)e attivarlo per inviare il messaggio.

>[!NOTE]
>
>Per tenere traccia del comportamento dei destinatari attraverso le aperture e/o le interazioni e-mail, assicurati che le opzioni dedicate nella **[!UICONTROL Tracciamento]** sono abilitate nel percorso di [attività e-mail](../building-journeys/journeys-message.md) o nell’e-mail [campagna](../campaigns/create-campaign.md).<!--to move?-->

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

