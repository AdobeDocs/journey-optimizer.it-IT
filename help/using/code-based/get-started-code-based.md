---
title: Introduzione alle esperienze basate su codice
description: Scopri le esperienze basate su codice in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
TQID: https://experienceleague.adobe.com/ZOCKgdEGK0G3GOhNbwxSXVOQo0We6-QdjzItFtZ5T3E
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037id: a984631b-2bae-4860-9b15-69c41a799dcb
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f88eedcc-cf3e-46b8-9e94-0293589325f3id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 1246
ht-degree: 79%

---

# Introduzione al canale basato su codice {#get-started-code-based}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri in che modo il canale basato su codice ti consente di distribuire contenuti personalizzati in posizioni granulari all’interno delle app e delle pagine web e quando utilizzarlo rispetto ad altri canali.

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] consente di personalizzare e testare le esperienze che desideri fornire ai clienti in tutti i tuoi punti di contatto: app web, app mobili, app desktop, console video, dispositivi Connected TV, smart TV, chioschi, sportelli automatici, assistenti vocali, dispositivi IoT, ecc.

Con la funzionalità per **esperienza basata su codice**, puoi definire le esperienze in entrata utilizzando un editor non visivo semplice e intuitivo. Questo consente di inserire e modificare elementi specifici in posizioni singole e più granulari delle app o delle pagine web, indipendentemente dal tipo di applicazione utilizzata, anziché applicare modifiche all’intero contenuto.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Consigli specifici per le esperienze basate su codice sono descritte in [questa pagina](code-based-prerequisites.md).


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ In [questa sezione](../experience-decisioning/experience-decisioning-uc.md) è presentato un caso d’uso end-to-end che mostra come utilizzare gli esperimenti di contenuto per confrontare le decisioni con il canale di esperienza basata su codice.

## Casi d’uso {#use-cases}

Il canale basato su codice funziona al meglio quando il caso d’uso va oltre quanto può supportare un editor visivo e hai a disposizione risorse di sviluppo per generare e mantenere l’implementazione.

| Beneficio | Perché | Casi d’uso di esempio |
| --- | --- | --- |
| Personalizzazione approfondita | Supporta dati logici complessi e in tempo reale oltre a quelli esposti dagli editor visivi | Personalization basato su inventario in tempo reale o contesto utente |
| Integrazione con sistemi esterni | I contenuti possono essere composti utilizzando dati provenienti da sistemi esterni | Promozioni basate su meteo, offerte basate su inventario in tempo reale |
| Flussi di lavoro condizionali avanzati e con più passaggi | Non limitato alle azioni predefinite dei canali visivi | Logica decisionale in più passaggi tra punti di contatto |
| Superare i limiti della piattaforma | Consente agli sviluppatori di creare elementi interattivi personalizzati | Componenti dell’interfaccia utente personalizzati non supportati dai canali predefiniti |
| Maggiore flessibilità delle campagne | Il contenuto e la logica sono definiti dalla tua implementazione | Proprietà digitali headless, basate su API o non basate su browser |

## Quando non utilizzare {#when-not-to-use}

Il canale basato su codice richiede un impegno di sviluppo, pertanto non è la scelta giusta per ogni scenario. Considera un altro canale nelle seguenti situazioni:

* La campagna è rapida o semplice e può essere creata con un canale senza codice come web o in-app, senza alcun sforzo di sviluppo
* Non sono disponibili risorse per sviluppatori o un ambiente di test per generare e convalidare un’implementazione personalizzata
* La timeline o il budget sono limitati per lo sviluppo personalizzato, in quanto le esperienze basate su codice richiedono una pianificazione più anticipata
* La messaggistica standard si adatta già alle funzionalità di canale integrate, rendendo superfluo lo sviluppo personalizzato
* La manutenzione a lungo termine del codice personalizzato è un problema, in quanto le superfici e le implementazioni richiedono un supporto continuo da parte degli sviluppatori

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
* Richiede una maggiore pianificazione ed è possibile modificare solo gli elementi specificati dagli sviluppatori. Pertanto, è essenziale identificare i componenti (banner Home, immagine hero, barra dei menu, ecc.) delle applicazioni che devono essere modificati per la personalizzazione o il test e collaborare con il team di sviluppo per realizzare l’implementazione necessaria per gestire tali modifiche.
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


