---
title: Creare esperienze basate su codice
description: Scopri come creare esperienze basate su codice in Journey Optimizer
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

## Aggiungere un’esperienza basata su codice tramite un percorso o una campagna {#create-code-based-experience}

Per iniziare a creare l’esperienza basata su codice tramite un percorso o una campagna, segui i passaggi seguenti.

>[!BEGINTABS]

>[!TAB Aggiungi un&#39;esperienza basata su codice a un percorso]

Per aggiungere un&#39;attività **esperienza basata su codice** a un percorso, eseguire la procedura seguente:

1. [Crea un percorso](../building-journeys/journey-gs.md).

1. Avvia il percorso con un&#39;attività [Event](../building-journeys/general-events.md) o [Read Audience](../building-journeys/read-audience.md).

1. Trascina e rilascia un&#39;attività **[!UICONTROL Esperienza basata su codice]** dalla sezione **[!UICONTROL Azioni]** della palette.

   ![](assets/code-based-activity-journey.png)

   >[!NOTE]
   >
   >Poiché **l&#39;esperienza basata su codice** è un&#39;attività messaggio in entrata, viene fornita con un&#39;attività **Wait** di 3 giorni. [Ulteriori informazioni](../building-journeys/wait-activity.md#auto-wait-node)

1. Immetti un **[!UICONTROL Etichetta]** e una **[!UICONTROL Descrizione]** per il messaggio.

1. Seleziona o crea la [configurazione esperienza basata su codice](code-based-configuration.md) da utilizzare.

   ![](assets/code-based-activity-config.png)

1. Seleziona il pulsante **[!UICONTROL Modifica contenuto]** e modifica il contenuto come desiderato utilizzando l&#39;editor di personalizzazione. [Ulteriori informazioni](#edit-code)

   È inoltre possibile utilizzare un modello di contenuto esistente come base per il contenuto del codice. I modelli disponibili per la scelta hanno l’ambito HTML o JSON in base alla configurazione del canale scelta in precedenza. [Scopri come utilizzare i modelli di contenuto](../content-management/use-content-templates.md)

1. Se necessario, completa il flusso di percorso trascinando altre azioni o eventi. [Ulteriori informazioni](../building-journeys/about-journey-activities.md)

1. Quando l’esperienza basata su codice è pronta, finalizza la configurazione e pubblica il percorso per attivarla. [Ulteriori informazioni](../building-journeys/publishing-the-journey.md)

Per ulteriori informazioni su come configurare un percorso, consultare [questa pagina](../building-journeys/journey-gs.md).

>[!TAB Creare un’esperienza basata su codice campagna]

Per iniziare a creare la tua **esperienza basata su codice** tramite una campagna, segui la procedura riportata di seguito.

1. Creare una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Seleziona il tipo di campagna da eseguire

   * **[!UICONTROL Pianificato - Marketing]**: esegui la campagna immediatamente o in una data specificata. Le campagne pianificate hanno lo scopo di inviare **messaggi di marketing**. Vengono configurati ed eseguiti dall’interfaccia utente di.

   * **[!UICONTROL Attivato da API - Marketing/Transazionale]**: esegui la campagna utilizzando una chiamata API. Le campagne attivate da API hanno lo scopo di inviare **messaggi di marketing** o **messaggi transazionali**, ovvero messaggi inviati in seguito a un&#39;azione eseguita da un individuo: reimpostazione della password, acquisto del carrello, ecc. [Scopri come attivare una campagna utilizzando le API](../campaigns/api-triggered-campaigns.md)

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

1. Dall&#39;attività di percorso o dalla schermata dell&#39;edizione della campagna, selezionare **[!UICONTROL Modifica codice]**.

   ![](assets/code-based-campaign-edit-code.png)

1. Verrà aperto l&#39;[editor di personalizzazione](../personalization/personalization-build-expressions.md). Si tratta di un’interfaccia non visiva per la creazione di esperienze che consente di creare il codice.

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


1. Fai clic su **[!UICONTROL Salva e chiudi]** per confermare le modifiche.

Ora, non appena lo sviluppatore effettua una chiamata API o SDK per recuperare il contenuto per la superficie definita nella configurazione del canale, le modifiche verranno applicate alla pagina web o all’app.

## Testare l’esperienza basata sul codice {#test-code-based-experience}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Visualizzare l’esperienza basata su codice in anteprima"
>abstract="Ottieni una simulazione dell’aspetto che avrà l’esperienza basata su codice."

Per visualizzare un’anteprima dell’esperienza basata su codice modificata, segui i passaggi indicati di seguito.

>[!CAUTION]
>
>Devi disporre di profili di test per simulare quali offerte verranno consegnate. Scopri come [creare profili di test](../audience/creating-test-profiles.md).

1. Nel percorso o nella campagna, dall&#39;editor di personalizzazione o dalla schermata Modifica contenuto, seleziona **[!UICONTROL Simula contenuto]**.

   ![](assets/code-based-campaign-simulate.png)

1. Fare clic su **[!UICONTROL Gestisci profili di test]** per selezionare uno o più profili di test.

1. Viene visualizzata un’anteprima dell’esperienza basata su codice modificata.

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
>title="Anteprima dell’esperienza mobile basata su codice sul dispositivo"
>abstract="Esegui la scansione del codice QR o copia il collegamento per visualizzarne l’anteprima sul dispositivo. Una volta collegato, inserire il pin sul dispositivo. Per visualizzare le modifiche apportate a ogni aggiornamento dei collegamenti di anteprima, potrebbe essere necessario riavviare l&#39;app."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_refresh"
>title="Aggiorna il collegamento di anteprima per riflettere la visualizzazione corrente"
>abstract="L’anteprima sul dispositivo mostrerà il contenuto al momento della creazione o dell’aggiornamento del collegamento di anteprima. Se hai modificato il contenuto o selezionato un profilo di test o un trattamento diverso, aggiorna l’anteprima in modo che rifletta la vista corrente."

Quando crei esperienze basate su codice per pagine web o app mobili, puoi visualizzare in anteprima le tue esperienze personalizzate direttamente sul browser o sui dispositivi mobili, per vedere come si presentano su dispositivi reali.

>[!WARNING]
>
>Anteprima sul dispositivo non disponibile quando si utilizzano [criteri di decisione](../experience-decisioning/create-decision.md) o [personalizzazione](../personalization/personalization-build-expressions.md) attributi contestuali.

1. Dalla schermata **[!UICONTROL Simula]**, fai clic sul pulsante **[!UICONTROL Apri opzioni di anteprima]**. Le opzioni di anteprima dipendono dalla piattaforma selezionata nella [configurazione basata su codice](code-based-configuration.md#create-code-based-configuration).

1. Se si utilizza una [piattaforma Web](code-based-configuration.md#web) nella configurazione basata su codice, il campo di sola lettura **[!UICONTROL URL anteprima dispositivo]** contiene l&#39;URL immesso per la configurazione del canale corrente.

   ![](assets/preview-on-device-web.png)

   Puoi effettuare le seguenti operazioni:

   * Seleziona il pulsante **[!UICONTROL Copia collegamento]** e incolla il collegamento in una scheda del browser. Puoi anche condividere il collegamento con il tuo team e le parti interessate, che possono visualizzare in anteprima la nuova esperienza in qualsiasi browser prima che le modifiche vengano pubblicate.

   * Fai clic su **[!UICONTROL Apri in una nuova scheda]** per aprire il collegamento nel browser corrente.

   * Esegui la scansione del codice QR con il tuo dispositivo mobile per aprire il collegamento di anteprima su un browser mobile.

1. Se utilizzi [Piattaforme mobili](code-based-configuration.md#mobile) (iOS / Android) nella configurazione basata su codice, il campo **[!UICONTROL Deeplink]** di sola lettura è precompilato con il valore **[!UICONTROL URL anteprima]** immesso nella configurazione del canale per la piattaforma selezionata.

   Passa dalle schede **[!UICONTROL iOS]** alle schede **[!DNL Android]** per visualizzare in anteprima la tua esperienza per la piattaforma che preferisci.

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

   Quando aggiorni il contenuto o selezioni un profilo di test o un trattamento diverso, il collegamento di anteprima viene aggiornato automaticamente. Puoi copiare il collegamento in diverse schede del browser e confrontare le esperienze.

## Rendi attiva l’esperienza basata su codice {#code-based-experience-live}

>[!IMPORTANT]
>
> Se la campagna è soggetta a un criterio di approvazione, dovrai richiedere l’approvazione per poter attivare le esperienze basate su codice. [Ulteriori informazioni](../test-approve/gs-approval.md)

Dopo aver definito l&#39;esperienza basata su codice e aver modificato il contenuto come desiderato utilizzando l&#39;[editor basato su codice](#edit-code), puoi attivare il percorso o la campagna per rendere le modifiche visibili al pubblico.

Puoi anche visualizzare in anteprima il contenuto dell’esperienza basata su codice prima di renderlo live. [Ulteriori informazioni](#test-code-based-experience)

>[!NOTE]
>
>Se attivi un percorso o una campagna basati su codice che influisce sulle stesse pagine di un altro percorso o campagna già live, tutte le modifiche verranno applicate al contenuto.
>
>Se più percorsi o campagne basati su codice aggiornano gli stessi elementi del contenuto, il percorso o la campagna con priorità più elevata ha la precedenza.

Una volta che il percorso o la campagna basati su codice è attiva, il team di implementazione dell&#39;app è responsabile di effettuare chiamate API o SDK esplicite per recuperare il contenuto per le superfici definite nella [configurazione esperienza basata su codice](code-based-configuration.md) selezionata. Ulteriori informazioni sulle diverse implementazioni del cliente in [questa sezione](code-based-implementation-samples.md).

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

1. Seleziona **[!UICONTROL Attiva]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Ulteriori informazioni sull&#39;attivazione delle campagne in [questa sezione](../campaigns/review-activate-campaign.md).

La campagna basata su codice assume lo stato **[!UICONTROL Live]** ed è ora visibile al pubblico selezionato. Ogni destinatario della campagna può visualizzare le modifiche aggiunte al contenuto.

>[!NOTE]
>
>Dopo aver fatto clic su **[!UICONTROL Attiva]**, potrebbero essere necessari fino a 15 minuti perché le modifiche siano disponibili in tempo reale.
>
>Se hai definito una pianificazione per una campagna basata su codice, questa avrà lo stato **[!UICONTROL Pianificato]** fino al raggiungimento della data e dell&#39;ora di inizio.

## Interrompere un percorso o una campagna basata su codice {#stop-code-based-experience}

Quando un’esperienza basata su codice è attiva, puoi interromperla per impedire al pubblico di visualizzare le modifiche. Segui i passaggi seguenti.

1. Seleziona un percorso o una campagna live dal rispettivo elenco.

1. Esegui l’azione pertinente in base al caso:

   * Dal menu principale della campagna, seleziona **[!UICONTROL Interrompi campagna]**.

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
