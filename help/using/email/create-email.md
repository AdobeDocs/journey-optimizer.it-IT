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
source-git-commit: 5f2ccb102d08151da5616ef42559164f29542e5d
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 11%

---

# Creare un messaggio e-mail {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Creazione di e-mail"
>abstract="Definisci la riga dell&#39;oggetto dell’e-mail e apri E-mail Designer per creare il contenuto dell’e-mail."

## Aggiungi un&#39;azione e-mail {#email-action}

Per creare un messaggio e-mail in [!DNL Journey Optimizer], aggiungi un&#39;azione **[!UICONTROL E-mail]** a un percorso o a una campagna. Quindi segui i passaggi seguenti, a seconda del tuo caso.

>[!BEGINTABS]

>[!TAB Aggiungi un&#39;e-mail a un percorso]

1. Apri il percorso, quindi trascina e rilascia un&#39;attività **[!UICONTROL E-mail]** dalla sezione **[!UICONTROL Azioni]** della palette.

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria).

1. Scegli o crea la [configurazione e-mail](email-settings.md).

   ![](assets/email_journey.png)

   Per impostazione predefinita, il campo è precompilato con l’ultima configurazione utilizzata dall’utente per quel canale.

>[!NOTE]
>
>Puoi utilizzare l’opzione Ottimizzazione del tempo di invio per prevedere il momento migliore per inviare il messaggio in modo da massimizzare il coinvolgimento in base alle percentuali storiche di apertura e clic. [Scopri come utilizzare l&#39;ottimizzazione dell&#39;ora di invio](../building-journeys/send-time-optimization.md)

Per ulteriori informazioni su come configurare un percorso, consultare [questa pagina](../building-journeys/journey-gs.md).

>[!TAB Aggiungere un messaggio e-mail a una campagna]

1. Crea una nuova campagna pianificata o attivata da API e seleziona **[!UICONTROL Invia e-mail]** come azione.

1. Completa i passaggi per creare una campagna e-mail, ad esempio le proprietà della campagna, [pubblico](../audience/about-audiences.md) e [pianificazione](../campaigns/campaign-schedule.md#action-campaign-schedule).

   ![](assets/email_campaign_steps.png)

1. Seleziona l&#39;azione **[!UICONTROL E-mail]**.

1. Seleziona o crea la configurazione e-mail. [Ulteriori informazioni](email-settings.md)

   ![](assets/email_campaign.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Importare il contenuto dell’e-mail {#define-email-content}

<!-- update the quarry component with right ID value-->

>[!CONTEXTUALHELP]
>id="test_id"
>title="Configurare il contenuto dell’e-mail"
>abstract="Crea il contenuto dell’e-mail. Definisci l’oggetto, quindi usa E-mail Designer per creare e personalizzare il corpo dell’e-mail."

Dopo aver aggiunto l’azione e-mail al percorso o alla campagna, è necessario definire il contenuto dell’e-mail, inclusi l’oggetto, le informazioni sul mittente e il corpo dell’e-mail tramite E-mail Designer. Segui questi passaggi:

1. Dalla schermata di configurazione del percorso o della campagna, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** per configurare il contenuto dell&#39;e-mail. [Ulteriori informazioni](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. Attiva **[!UICONTROL Abilita decisioning]** se desideri aggiungere criteri di decisione nel messaggio e-mail.

   I criteri di decisione sono contenitori per le offerte che sfruttano il motore di decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico. [Scopri come aggiungere un criterio di decisione in un messaggio e-mail](../experience-decisioning/create-decision.md#create-decision)

   ![](assets/../../experience-decisioning/assets/decision-policy-enable.png)

   >[!AVAILABILITY]
   >
   >Per il momento, la creazione di criteri di decisione nelle e-mail è disponibile in Disponibilità limitata. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

1. Nella sezione **[!UICONTROL Intestazione]**, controlla i campi **[!UICONTROL Da nome]**, **[!UICONTROL Da e-mail]** e **[!UICONTROL Ccn]**. Sono configurati nella configurazione e-mail selezionata. [Ulteriori informazioni](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. Aggiungi un oggetto per il messaggio. Per configurare e personalizzare l&#39;oggetto con l&#39;editor di personalizzazione, fare clic sull&#39;icona **[!UICONTROL Apri finestra di dialogo per personalizzazione]**. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

   >[!NOTE]
   >
   >L’oggetto è obbligatorio. Non deve includere interruzioni di riga.

1. Fai clic sul pulsante **[!UICONTROL Modifica corpo dell&#39;e-mail]** per accedere al Designer e-mail e iniziare a creare il contenuto. [Ulteriori informazioni](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. Se ti trovi in una campagna, puoi anche fare clic sul pulsante **[!UICONTROL Editor di codice]** per scrivere il codice del tuo contenuto in HTML semplice utilizzando la finestra popup visualizzata.

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

* **Avvisi** fai riferimento a consigli e best practice, ad esempio:

   * **[!UICONTROL Il collegamento di rinuncia non è presente nel corpo dell&#39;e-mail]**: è consigliabile aggiungere un collegamento di annullamento all&#39;abbonamento nel corpo dell&#39;e-mail. Scopri come configurarlo in [questa sezione](../privacy/opt-out.md#opt-out-decision-management).

     >[!NOTE]
     >
     >I messaggi e-mail di tipo marketing devono includere un collegamento di rinuncia, che non è invece necessario per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]**) è definita al livello [configurazione canale](email-settings.md#email-type) e durante la [creazione del messaggio](#create-email-journey-campaign) da un percorso o una campagna.

   * **[!UICONTROL La versione testuale di HTML è vuota]**: non dimenticare di definire una versione testuale del corpo dell&#39;e-mail, in quanto verrà utilizzata quando non sarà possibile visualizzare il contenuto di HTML. Scopri come creare la versione del testo in [questa sezione](text-version-email.md).

   * **[!UICONTROL Nel corpo dell&#39;e-mail è presente un collegamento vuoto]**: verifica che tutti i collegamenti presenti nell&#39;e-mail siano corretti. Scopri come gestire contenuti e collegamenti in [questa sezione](content-from-scratch.md).

   * **[!UICONTROL La dimensione dell&#39;e-mail ha superato il limite di 100 KB]**: per una consegna ottimale, assicurati che la dimensione dell&#39;e-mail non superi i 100 KB. Scopri come modificare il contenuto delle e-mail in [questa sezione](content-from-scratch.md).

* **Gli errori** impediscono di testare o attivare il percorso o la campagna finché non vengono risolti, ad esempio:

   * **[!UICONTROL Manca la riga dell&#39;oggetto]**: la riga dell&#39;oggetto dell&#39;e-mail è obbligatoria. Scopri come definirlo e personalizzarlo in [questa sezione](create-email.md).

  <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL La versione e-mail del messaggio è vuota]**: questo errore viene visualizzato quando il contenuto dell&#39;e-mail non è stato configurato. Scopri come progettare contenuti e-mail in [questa sezione](get-started-email-design.md).

   * **[!UICONTROL la configurazione non esiste]**: non puoi utilizzare il messaggio se la configurazione selezionata viene eliminata dopo la creazione del messaggio. Se si verifica questo errore, selezionare un&#39;altra configurazione nel messaggio **[!UICONTROL Proprietà]**. Ulteriori informazioni sulle configurazioni dei canali in [questa sezione](../configuration/channel-surfaces.md).

>[!CAUTION]
>
>Per poter testare o attivare il percorso o la campagna tramite l&#39;e-mail, è necessario risolvere tutti gli avvisi di **errore**.

## Controllare e inviare l’e-mail

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarne l’anteprima, inviare bozze e controllarne il rendering nei client desktop, mobili e basati su Web più diffusi. Se hai incluso contenuti personalizzati, puoi verificare come questi vengono visualizzati nel messaggio utilizzando i dati del profilo di test.

>[!NOTE]
>
>Oltre ai profili di test, [!DNL Journey optimizer] consente anche di testare diverse varianti del contenuto visualizzandolo in anteprima e inviando bozze utilizzando dati di input di esempio caricati da un file CSV / JSON o aggiunti manualmente. [Scopri come simulare varianti di contenuto](../test-approve/simulate-sample-input.md)

A questo scopo, fai clic su **[!UICONTROL Simula contenuto]**, quindi aggiungi un profilo di test per verificare il messaggio utilizzando i dati del profilo di test.

![](assets/email_designer_edit_simulate.png)

Informazioni dettagliate su come selezionare profili di test e visualizzare in anteprima il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

Quando l&#39;e-mail è pronta, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) e attivala per inviare il messaggio.

>[!NOTE]
>
>Per tenere traccia del comportamento dei destinatari tramite aperture e/o interazioni e-mail, assicurati che le opzioni dedicate nella sezione **[!UICONTROL Tracciamento]** siano abilitate nella [attività e-mail](../building-journeys/journeys-message.md) del percorso o nella [campagna](../campaigns/create-campaign.md) e-mail.<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] personalization editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

