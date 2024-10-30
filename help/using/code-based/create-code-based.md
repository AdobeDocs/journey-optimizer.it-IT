---
title: Creare esperienze basate su codice
description: Learn how to create code-based experiences in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '1802'
ht-degree: 6%

---

# Creare esperienze basate su codice {#create-code-based}

In [!DNL Journey Optimizer] è possibile creare esperienze basate su codice in un percorso o in una campagna.

I dettagli su guardrail e consigli specifici per esperienze basate su codice sono disponibili in [questa pagina](code-based-prerequisites.md).

## Add a code-based experience through a journey or a campaign {#create-code-based-experience}

To start building your code-based experience through a journey or a campaign, follow the steps below.

>[!BEGINTABS]

>[!TAB ]

Per aggiungere un&#39;attività **esperienza basata su codice** a un percorso, eseguire la procedura seguente:

1. [Crea un percorso](../building-journeys/journey-gs.md).

1. Avvia il percorso con un&#39;attività [Event](../building-journeys/general-events.md) o [Read Audience](../building-journeys/read-audience.md).

1. Trascina e rilascia un&#39;attività **[!UICONTROL Esperienza basata su codice]** dalla sezione **[!UICONTROL Azioni]** della palette.

   ![](assets/code-based-activity-journey.png)

   >[!NOTE]
   >
   >Poiché **l&#39;esperienza basata su codice** è un&#39;attività messaggio in entrata, viene fornita con un&#39;attività **Wait** di 3 giorni. [Ulteriori informazioni](../building-journeys/wait-activity.md#auto-wait-node)

1. ********

1. [](code-based-configuration.md)

   ![](assets/code-based-activity-config.png)

1. Seleziona il pulsante **[!UICONTROL Modifica contenuto]** e modifica il contenuto come desiderato utilizzando l&#39;editor di personalizzazione. [Ulteriori informazioni](#edit-code)

   È inoltre possibile utilizzare un modello di contenuto esistente come base per il contenuto del codice. I modelli disponibili per la scelta hanno l’ambito HTML o JSON in base alla configurazione del canale scelta in precedenza. [Scopri come utilizzare i modelli di contenuto](../content-management/use-content-templates.md)

1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Ulteriori informazioni](../building-journeys/about-journey-activities.md)

1. Once your code-base experience is ready, finalize the configuration and publish your journey to activate it. [Ulteriori informazioni](../building-journeys/publishing-the-journey.md)

Per ulteriori informazioni su come configurare un percorso, consultare [questa pagina](../building-journeys/journey-gs.md).

>[!TAB Creare un’esperienza basata su codice campagna]

Per iniziare a creare la tua **esperienza basata su codice** tramite una campagna, segui la procedura riportata di seguito.

1. Create a campaign. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Select the type of campaign that you want to execute

   * **** **** They are configured and executed from the user interface.

   * **** Le campagne attivate da API hanno lo scopo di inviare **messaggi di marketing** o **messaggi transazionali**, ovvero messaggi inviati in seguito a un&#39;azione eseguita da un individuo: reimpostazione della password, acquisto del carrello, ecc. [Scopri come attivare una campagna utilizzando le API](../campaigns/api-triggered-campaigns.md)

1. Completa i passaggi per creare una campagna, ad esempio le proprietà della campagna, [pubblico](../audience/about-audiences.md) e [pianificazione](../campaigns/create-campaign.md#schedule). Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

1. Seleziona l&#39;azione **[!UICONTROL Esperienza basata su codice]**.

1. Seleziona o crea la configurazione dell&#39;esperienza basata su codice. [Ulteriori informazioni](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

1. Modifica i contenuti come desideri utilizzando l’editor di personalizzazione. [Ulteriori informazioni](#edit-code)

   È inoltre possibile utilizzare un modello di contenuto esistente come base per il contenuto del codice. I modelli disponibili per la scelta hanno l’ambito HTML o JSON in base alla configurazione del canale scelta in precedenza. [Scopri come utilizzare i modelli di contenuto](../content-management/use-content-templates.md)

   <!--![](assets/code-based-campaign-edit-content.png)-->

Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Modificare il contenuto del codice {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="Utilizzare l’editor di personalizzazione"
>abstract="Inserisci e modifica il codice che desideri consegnare come parte di questa azione di esperienza basata su codice."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html?lang=it" text="Introduzione all’editor di personalizzazione"

1. ****

   ![](assets/code-based-campaign-edit-code.png)

1. [](../personalization/personalization-build-expressions.md) Si tratta di un’interfaccia non visiva per la creazione di esperienze che consente di creare il codice.

1. Puoi passare dalla modalità di authoring di HTML a JSON e viceversa.

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >La modifica della modalità di authoring comporterà la perdita di tutto il codice corrente; assicurati quindi di cambiare modalità prima di iniziare l’authoring.

1. Immetti il codice in base alle esigenze. Puoi sfruttare l&#39;editor di personalizzazione [!DNL Journey Optimizer] con tutte le sue funzionalità di personalizzazione e authoring. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

1. Se necessario, puoi aggiungere frammenti di espressione HTML o JSON. [Scopri come](../personalization/use-expression-fragments.md)

   Puoi anche salvare parte del contenuto del codice come frammento. [Scopri come](../content-management/fragments.md#save-as-expression-fragment)

1. Con esperienze basate su codice, puoi utilizzare la funzione Decisioning. Seleziona l&#39;icona **[!UICONTROL Criterio decisione]** dalla barra a sinistra e fai clic su **[!UICONTROL Aggiungi criterio decisione]**. [Ulteriori informazioni](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >Decisioning è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.


1. ****

Now as soon as your developer makes an API or SDK call to fetch content for the surface defined in your channel configuration, the changes will be applied to your web page or app.

## Testare l’esperienza basata sul codice {#test-code-based-experience}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Visualizzare l’esperienza basata su codice in anteprima"
>abstract="Ottieni una simulazione dell’aspetto che avrà l’esperienza basata su codice."

Per visualizzare un’anteprima dell’esperienza basata su codice modificata, segui i passaggi indicati di seguito.

>[!CAUTION]
>
>Devi disporre di profili di test per simulare quali offerte verranno consegnate. Scopri come [creare profili di test](../audience/creating-test-profiles.md).

1. ****

   ![](assets/code-based-campaign-simulate.png)

1. ****

1. A preview of your modified code-based experience is displayed.

Informazioni dettagliate su come selezionare profili di test e visualizzare in anteprima il contenuto sono disponibili in [questa sezione](../content-management/preview.md).

### Anteprima sul dispositivo {#preview-on-device}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device"
>title="Visualizzare in anteprima l’esperienza basata su codice su un dispositivo reale"
>abstract="Visualizza un’anteprima delle tue esperienze personalizzate direttamente sul browser o sui dispositivi mobili, per visualizzarne l’aspetto su dispositivi reali."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_web"
>title="Anteprima dell’esperienza web basata su codice sul dispositivo"
>abstract="Esegui la scansione del codice QR o copia il collegamento per visualizzarne l’anteprima sul dispositivo."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_mobile"
>title="Preview your code-based mobile experience on device"
>abstract="Scan the QR code or copy the link to preview on device. Una volta collegato, inserire il pin sul dispositivo. Per visualizzare le modifiche apportate a ogni aggiornamento dei collegamenti di anteprima, potrebbe essere necessario riavviare l&#39;app."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_refresh"
>title="Aggiorna il collegamento di anteprima per riflettere la visualizzazione corrente"
>abstract="L’anteprima sul dispositivo mostrerà il contenuto al momento della creazione o dell’aggiornamento del collegamento di anteprima. Se hai modificato il contenuto o selezionato un profilo di test o un trattamento diverso, aggiorna l’anteprima in modo che rifletta la vista corrente."

When building code-based experiences for web pages or mobile apps, you can preview your personalized experiences right on your browser or on your mobile devices, in order to see how these experiences look on real devices.

>[!WARNING]
>
>[](../experience-decisioning/create-decision.md)[](../personalization/personalization-build-expressions.md)

1. Dalla schermata **[!UICONTROL Simula]**, fai clic sul pulsante **[!UICONTROL Apri opzioni di anteprima]**. Le opzioni di anteprima dipendono dalla piattaforma selezionata nella [configurazione basata su codice](code-based-configuration.md#create-code-based-configuration).

1. Se si utilizza una [piattaforma Web](code-based-configuration.md#web) nella configurazione basata su codice, il campo di sola lettura **[!UICONTROL URL anteprima dispositivo]** contiene l&#39;URL immesso per la configurazione del canale corrente.

   ![](assets/preview-on-device-web.png)

   Puoi effettuare le seguenti operazioni:

   * **** You can also share the link with your team and stakeholders, who can preview the new experience in any browser before the changes go live.

   * ****

   * Scan the QR code with your mobile device to open the preview link on a mobile browser.

1. [](code-based-configuration.md#mobile)********

   ******[!DNL Android]**

   ![](assets/preview-on-device-mobile.png)

   Puoi effettuare le seguenti operazioni:

   * Seleziona il pulsante **[!UICONTROL Copia collegamento]** e condividi il collegamento con il tuo team e le parti interessate, che possono visualizzare in anteprima la nuova esperienza in qualsiasi browser mobile prima che le modifiche vengano pubblicate.

   * Esegui la scansione del codice QR con il tuo dispositivo mobile per aprire il collegamento di anteprima direttamente nell’app mobile. Per stabilire la sessione [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/implement-assurance){target="_blank"} è necessario immettere il PIN sul dispositivo.

     >[!NOTE]
     >
     >**Adobe Experience Platform Assurance** è un prodotto di Adobe Experience Cloud che consente di verificare, verificare, simulare e convalidare le modalità di raccolta dei dati o di gestione delle esperienze nell&#39;app mobile. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/home){target="_blank"}

1. Vengono generati collegamenti di anteprima per il profilo di test selezionato e, se utilizzi [Esperimento contenuti](../content-management/content-experiment.md) nel tuo percorso o campagna, per il trattamento selezionato.

   <!--If you have modified the content or selected a different treatment or test profile, scroll down to the bottom of the **[!UICONTROL Preview on device]** pop-up and click **[!UICONTROL Refresh preview link]** to reflect the current state.

   ![](assets/preview-on-device-refresh.png)-->

   <!--When creating a content experiment, you need to select a given treatment and click the **[!UICONTROL Simulate content]** button to obtain the link corresponding to that treatment, then select another treatment, click the **[!UICONTROL Simulate content]** button to obtain a new preview link, and so on.-->

   When updating the content, or selecting a different test profile or treatment, the preview link is automatically refreshed. You can copy the link into different browser tabs, and compare the experiences.

## Make your code-based experience live {#code-based-experience-live}

>[!IMPORTANT]
>
> If your campaign is subject to an approval policy, you will need to request approval in order to be able to activate your code-based experiences. [Ulteriori informazioni](../test-approve/gs-approval.md)

Dopo aver definito l&#39;esperienza basata su codice e aver modificato il contenuto come desiderato utilizzando l&#39;[editor basato su codice](#edit-code), puoi attivare il percorso o la campagna per rendere le modifiche visibili al pubblico.

You can also preview your code-based experience content before making it live. [Ulteriori informazioni](#test-code-based-experience)

>[!NOTE]
>
>If you activate a code-based journey/campaign impacting the same pages as another journey or campaign which is already live, all the changes will be applied to your content.
>
>If multiple code-based journeys or campaigns update the same element(s) of your content, the highest priority journey/campaign takes precedence.

[](code-based-configuration.md) [](code-based-implementation-samples.md)

### Publish un percorso basato su codice {#publish-code-based-journey}

Per rendere live le tue esperienze basate su codice da un percorso, segui i passaggi indicati di seguito.

1. Verifica che il percorso sia valido e che non ci siano errori. [Ulteriori informazioni](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)

1. Dal percorso, seleziona l&#39;opzione **[!UICONTROL Publish]**, che si trova nel menu a discesa in alto a destra.

   ![](assets/code-based-journey-publish.png)

   >[!NOTE]
   >
   >Ulteriori informazioni sulla pubblicazione di percorsi in [questa sezione](../building-journeys/publishing-the-journey.md).

Il percorso basato su codice accetta lo stato **[!UICONTROL Live]** ed è ora visibile al pubblico selezionato. Ogni destinatario del percorso può visualizzare le modifiche.

>[!NOTE]
>
>Dopo aver fatto clic su **[!UICONTROL Publish]**, potrebbero essere necessari fino a 15 minuti perché le modifiche siano disponibili in tempo reale.

### Attivare una campagna basata su codice {#activate-code-based-campaign}

1. Dalla campagna basata su codice, seleziona **[!UICONTROL Verifica per attivare]**.

   ![](assets/code-based-campaign-review.png)

1. Se necessario, seleziona e modifica il contenuto, le proprietà, la configurazione, il pubblico e la pianificazione.

1. ****

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >[](../campaigns/review-activate-campaign.md)

**** Each recipient of your campaign can see the modifications you added to your content.

>[!NOTE]
>
>****
>
>****

## Interrompere un percorso o una campagna basata su codice {#stop-code-based-experience}

When a code-based experience is live, you can stop it to prevent your audience from seeing your modifications. Segui i passaggi seguenti.

1. Select a live journey or campaign from the respective list.

1. Perform the relevant action according to your case:

   * ****

     ![](assets/code-based-campaign-stop.png)

   * Dal menu principale del percorso, fare clic sul pulsante **[!UICONTROL Altro]** e selezionare **[!UICONTROL Interrompi]**.

     ![](assets/code-based-journey-stop.png)

1. Le modifiche aggiunte non saranno più visibili al pubblico definito.

>[!NOTE]
>
>Una volta interrotto un percorso o una campagna basato su codice, non puoi più modificarlo o attivarlo. Puoi solo duplicarlo e attivare il percorso o la campagna duplicati.

<!--Reporting TBC

## Check the code-based experience reports {#check-code-based-reports}

Once your code-based experience is live, you can check the **[!UICONTROL Code-based]** tab of the  [Journey report](../reports/journey-global-report-cja.md#web-cja) and [Campaign report](../reports/campaign-global-report-cja.md#web) to compare elements such as the number of experiences delivered to your audience, and the number of engagements with your content.-->

<!--## Code-based reports

You can access code-based journey or campaign reports from the summary screen.

Global reports display events that occurred at least two hours ago and cover events over a selected time period. In comparison, Live reports focus on events that took place within the past 24 hours, with a minimum time interval of two minutes from the event occurrence.

### Code-based live report {#live-report-code-based}

From your campaign **[!UICONTROL Live report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages. [Learn more on live report](../reports/campaign-live-report.md)

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your code-based experiences, such as:

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**:  total number of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (impressions, unique impressions and interactions) for the last 24 hours.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.
+++

### Code-based global report {#global-report-code-based}

Code-based campaign global report can be accessed directly from your journey or campaign with the **[!UICONTROL View report]** button. [Learn more on global report](../reports/campaign-global-report-cja.md)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages.

![](assets/code-based-campaign-global-report.png)

Add image TBC

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your experiences, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the experience was delivered.

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**: percentage of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (unique impressions, impressions and interactions) for the concerned period.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.
+++

TBC video if existing

## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
