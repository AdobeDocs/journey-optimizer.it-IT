---
title: Introduzione alle esperienze basate su codice
description: Scopri le esperienze basate su codice in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '855'
ht-degree: 100%

---

# Introduzione al canale basato su codice {#get-started-code-based}

[!DNL Journey Optimizer] consente di personalizzare e testare le esperienze che desideri fornire ai clienti in tutti i tuoi punti di contatto: app web, app mobili, app desktop, console video, dispositivi Connected TV, smart TV, chioschi, sportelli automatici, assistenti vocali, dispositivi IoT, ecc.

Con la funzionalità per **esperienza basata su codice**, puoi definire le esperienze in entrata utilizzando un editor non visivo semplice e intuitivo. Questo consente di inserire e modificare elementi specifici in posizioni singole e più granulari delle app o delle pagine web, indipendentemente dal tipo di applicazione utilizzata, anziché applicare modifiche all’intero contenuto.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Consigli specifici per le esperienze basate su codice sono descritte in [questa pagina](code-based-prerequisites.md).


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ In [questa sezione](../experience-decisioning/experience-decisioning-uc.md) è presentato un caso d’uso end-to-end che mostra come utilizzare gli esperimenti di contenuto per confrontare le decisioni con il canale di esperienza basata su codice.

## Quando utilizzare il canale Basato su codice rispetto ad altri canali {#code-based-vs-other-channels}

### Basato su codice e altri canali

Quando utilizzare il canale Basato su codice anziché gli altri canali di [!DNL Journey Optimizer]?

* È possibile utilizzare le esperienze basate su codice in qualsiasi momento quando non si accede alla proprietà digitale tramite un browser web o un’app mobile; in questi ultimi casi, infatti, è spesso preferibile utilizzare il [canale Web](../web/get-started-web.md){target="_blank"} di [!DNL Journey Optimizer] o la [messaggistica in-app](../../rp_landing_pages/in-app-landing-page.md){target="_blank"} di [!DNL Journey Optimizer].

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* Puoi utilizzare il canale basato su codice come alternativa ai canali Web o In-app di [!DNL Journey Optimizer] in caso di implementazioni basate su API, headless o lato server.

* Puoi anche sfruttare il canale basato su codice nelle applicazioni mobili native come alternativa al canale in-app, se desideri modificare il contenuto all’interno dell’app nativa invece di visualizzare modali, popup o sovrapposizioni.

### Canale Basato su codice e canale Web {#code-based-vs-web}

Per casi di utilizzo web, puoi utilizzare il canale web o l’esperienza basata su codice, ma a seconda del contesto, uno può essere più appropriato dell’altro. Le principali differenze elencate di seguito ti aiuteranno a decidere quale canale scegliere in base alle tue esigenze.

**Web**

* Modifica il contenuto utilizzando l’editor visivo [Designer web](../web/web-visual-editor.md){target="_blank"} o l’[editor non visivo](../web/web-non-visual-editor.md) web.
* È necessario [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}, un’implementazione lato client.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* Il canale Web consente di modificare tutto ciò che si trova sulla pagina e dispone di un elenco preimpostato di azioni che puoi utilizzare per apportare modifiche. [Ulteriori informazioni](../web/web-visual-editor.md){target="_blank"}
* È facile e veloce da configurare.
* È incentrato sul ruolo di marketer.

**Esperienza basata su codice**

* Modifica il contenuto utilizzando l’[editor di personalizzazione](create-code-based.md#edit-code).
* È necessario [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}, implementazione lato client, oppure [AEP Edge Network Server API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=it){target="_blank"}, implementazione lato server.
* Per creare esperienze basate su codice, è necessario un precedente lavoro di sviluppo sulla propria implementazione affinché che le applicazioni possano interpretare e consegnare i contenuti pubblicati nell’ambiente Edge da [!DNL Journey Optimizer] per queste posizioni. [Ulteriori informazioni](code-based-surface.md)
* Richiede una maggiore pianificazione ed è possibile modificare solo gli elementi specificati dagli sviluppatori. Pertanto, è essenziale identificare i componenti (banner Home, immagine hero, barra dei menu, ecc.) delle applicazioni che devono essere modificate per personalizzazione o test e collaborare con il team di sviluppo per creare l’implementazione necessaria per gestire queste modifiche.
* Consente di utilizzare contenuti creati con codice JSON.
* È incentrata sugli sviluppatori.

## Come funziona {#how-it-works}

>[!CAUTION]
>
>Questa funzione è destinata agli sviluppatori e/o utenti esperti. Può essere utilizzata da marketer con alcune competenze nella scrittura del codice, purché le configurazioni di canale e la configurazione iniziale siano gestite dal team di sviluppo.

Per modificare il contenuto utilizzando la funzionalità di esperienza basata su codice di [!DNL Journey Optimizer], le pagine o le app devono essere strumentate. Per farlo, è necessario specificare in anticipo le singole posizioni (denominate “[superfici](code-based-surface.md)”) nel punto in cui desideri inserire o sostituire il contenuto.

>[!NOTE]
>
>Attualmente il contenuto associato a una configurazione può essere solo HTML o JSON.

I passaggi chiave per creare e consegnare un’esperienza basata su codice sono i seguenti.

1. Assicurati di seguire i prerequisiti specifici per il canale. [Ulteriori informazioni](code-based-prerequisites.md)

1. Definisci una [superficie](code-based-surface.md#surface-definition) nell’implementazione dell’applicazione, che è fondamentalmente la posizione in cui desideri aggiungere la tua esperienza.

1. Crea una configurazione di canale basata su codice che fa riferimento a tale posizione. [Scopri come](code-based-configuration.md#create-code-based-configuration)

1. Creare un percorso o una campagna in [!DNL Journey Optimizer] utilizzando questa configurazione. [Scopri come](create-code-based.md#create-code-based-experience)

1. Componi un’esperienza specificando il contenuto per la configurazione selezionata utilizzando l’editor di personalizzazione di [!DNL Journey Optimizer]. [Scopri come](create-code-based.md#edit-code)

1. Testare l’esperienza basata su codice. [Scopri come](test-code-based.md)

1. Pubblicarla. [Scopri come](publish-code-based.md)

1. Una volta che il percorso o la campagna dell’esperienza basata su codice sono live, l’implementazione dell’app o della pagina che richiede il contenuto per la superficie deve essere pronta affinché il contenuto venga recuperato e visualizzato.

   >[!INFO]
   >
   >Per garantirlo, il team di implementazione dell’app effettua chiamate API o SDK esplicite per recuperare il contenuto per la superficie definita nella configurazione basata su codice, come “Testo banner” o “Area 1 Consigli”, o punti decisionali non correlati all’interfaccia utente in un’applicazione, ad esempio “Parametri dell’algoritmo di ricerca”. <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [Ulteriori informazioni](code-based-implementation-samples.md)

## Risorse aggiuntive

* **[Creare esperienze basate su codice](create-code-based.md)**: scopri come creare e configurare campagne e percorsi basati su codice per le implementazioni personalizzate.
* **[Configurare un canale basato su codice](code-based-configuration.md)**: imposta le configurazioni dell’esperienza basata su codice con le impostazioni di superficie e di implementazione corrette.
* **[Prerequisiti basati su codice](code-based-prerequisites.md)**: informazioni sui requisiti tecnici e le risorse per sviluppatori necessarie per l’implementazione.
* **[Testare le esperienze basate su codice](test-code-based.md)**: scopri come visualizzare in anteprima e testare le esperienze basate su codice prima di pubblicarle.
* **[Esempi di implementazione](code-based-implementation-samples.md)**: esplora esempi di codice e pattern di implementazione per vari casi d’uso.
* **[Tutorial sulle esperienze basate su codice](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/create-a-code-based-experience-campaign){target="_blank"}**: esplora i tutorial video dettagliati sulle funzioni basate su codice e le best practice.

