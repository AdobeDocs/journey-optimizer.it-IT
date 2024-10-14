---
title: Introduzione alle esperienze basate su codice
description: Scopri le esperienze basate su codice in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: e3c597f66436e8e0e22d06f1905fc7ca9a9dd570
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 83%

---

# Introduzione al canale basato su codice {#get-sarted-code-based}

[!DNL Journey Optimizer] consente di personalizzare e testare le esperienze che desideri fornire ai clienti in tutti i tuoi punti di contatto: app web, app mobili, app desktop, console video, dispositivi Connected TV, smart TV, chioschi, sportelli automatici, assistenti vocali, dispositivi IoT, ecc.

Con la funzionalità per **esperienza basata su codice**, puoi definire le esperienze in entrata utilizzando un editor non visivo semplice e intuitivo. Questo consente di inserire e modificare elementi specifici in posizioni singole e più granulari delle app o delle pagine web, indipendentemente dal tipo di applicazione utilizzata, anziché applicare modifiche all’intero contenuto.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>I dettagli su guardrail e consigli specifici per esperienze basate su codice sono disponibili in [questa pagina](code-based-prerequisites.md).


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Lead" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>Come funziona</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="Convalida" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>Guardrail e prerequisiti</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Non frequente" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Creare un’esperienza web</strong></a>
</div>
<p></td>
<td>
<a href="code-based-implementation-samples.md">
<img alt="Convalida" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>Esempi di implementazione</strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## Quando utilizzare il canale Basato su codice rispetto ad altri canali {#code-based-vs-other-channels}

### Basato su codice e altri canali

Quando utilizzare il canale Basato su codice anziché gli altri canali di [!DNL Journey Optimizer]?

* È possibile utilizzare le esperienze basate su codice in qualsiasi momento quando non si accede alla proprietà digitale tramite un browser web o un’app mobile; in questi ultimi casi, infatti, è spesso preferibile utilizzare il [canale Web](../web/get-started-web.md){target="_blank"} di [!DNL Journey Optimizer] o la [messaggistica in-app](../in-app/get-started-in-app.md){target="_blank"} di [!DNL Journey Optimizer].

* È possibile utilizzare il canale basato su codice in alternativa al canale Web di [!DNL Journey Optimizer] se il sito web non può essere caricato nell’editor visivo del [Designer web](../web/edit-web-content.md#work-with-web-designer){target="_blank"} o nel caso in cui non sia possibile utilizzare l’[estensione del browser](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} che attiva l’authoring visivo per il canale Web.

* Inoltre, il canale Basato su codice può essere usato in alternativa ai canali Web o In-app di [!DNL Journey Optimizer] in caso di implementazioni basate su API, headless o lato server.

### Canale Basato su codice e canale Web {#code-based-vs-web}

Per casi di utilizzo web, puoi utilizzare il canale web o l’esperienza basata su codice, ma a seconda del contesto, uno può essere più appropriato dell’altro. Le principali differenze elencate di seguito ti aiuteranno a decidere quale canale scegliere in base alle tue esigenze.

**Web**

* Modifica il contenuto utilizzando l’editor visivo [Designer web](../web/edit-web-content.md#work-with-web-designer){target="_blank"}.
* Hai bisogno dell’implementazione di [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} e dell’estensione [Helper per editing video di Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} installata nel browser web. [Ulteriori informazioni](../web/web-prerequisites.md){target="_blank"}
* Il canale Web consente di modificare tutto ciò che si trova sulla pagina e dispone di un elenco preimpostato di azioni che puoi utilizzare per apportare modifiche. [Ulteriori informazioni](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* È facile e veloce da configurare.
* È incentrato sul ruolo di marketer.

**Esperienza basata su codice**

* Modifica il contenuto utilizzando l’[editor di personalizzazione](create-code-based.md#edit-code).
* Per creare esperienze basate su codice, è necessario un precedente lavoro di sviluppo sulla propria implementazione affinché che le applicazioni possano interpretare e consegnare i contenuti pubblicati nell’ambiente Edge da [!DNL Journey Optimizer] per queste posizioni. [Ulteriori informazioni](code-based-configuration.md#surface-definition)
* Richiede una maggiore pianificazione ed è possibile modificare solo gli elementi specificati dagli sviluppatori. Pertanto, è essenziale identificare i componenti (banner Home, immagine hero, barra dei menu, ecc.) nelle applicazioni che devono essere modificati per la personalizzazione o il testing e collaborare con il team di sviluppo per creare l’implementazione necessaria per gestire queste modifiche.
* Consente di utilizzare contenuti creati con codice JSON.
* È incentrata sugli sviluppatori.

## Come funziona {#how-it-works}

>[!CAUTION]
>
>Questa funzione è destinata agli sviluppatori e/o utenti esperti. Può essere utilizzato da esperti di marketing con competenze di scrittura del codice, purché le configurazioni dei canali e la configurazione iniziale siano gestite dal team di sviluppo.

Per modificare il contenuto utilizzando la funzionalità di esperienza basata su codice di [!DNL Journey Optimizer], le pagine o le app devono essere strumentate. A questo scopo, devi dichiarare in anticipo le singole posizioni specifiche (denominate &quot;[superfici](code-based-configuration.md#surface-definition)&quot;) in cui desideri inserire o sostituire il contenuto.

>[!NOTE]
>
>Attualmente il contenuto associato a una configurazione può essere solo HTML o JSON.

I passaggi chiave per implementare una campagna basata su codice sono i seguenti.

1. Definisci una [superficie](code-based-configuration.md#surface-definition) nell&#39;implementazione dell&#39;applicazione, ovvero la posizione in cui desideri aggiungere l&#39;esperienza basata sul codice, e crea una configurazione del canale di esperienza basata sul codice che faccia riferimento a tale posizione. [Scopri come](code-based-configuration.md#create-code-based-configuration)

1. Creare un percorso o una campagna in [!DNL Journey Optimizer] utilizzando questa configurazione. [Scopri come](create-code-based.md#create-code-based-campaign)

1. Componi un’esperienza specificando il contenuto per la configurazione selezionata utilizzando l’editor di personalizzazione di [!DNL Journey Optimizer]. [Scopri come](create-code-based.md#edit-code)

1. Il team di implementazione dell’app effettua chiamate API o SDK esplicite per recuperare il contenuto delle superfici denominate, ad esempio “Testo banner” o “Area 1 Consigli”, o punti decisionali non correlati all’interfaccia utente in un’applicazione, ad esempio “Parametri dell’algoritmo di ricerca”. In questo caso, il team di implementazione è responsabile del rendering o dell’interpretazione e dell’azione sul contenuto restituito. [Ulteriori informazioni](code-based-implementation-samples.md)
