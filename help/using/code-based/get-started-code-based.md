---
title: Introduzione alle esperienze basate su codice
description: Scopri le esperienze basate su codice in Journey Optimizer
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 60c74bcc5e33afa354a2380d3e6f490a4c2c3e6d
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 7%

---

# Introduzione al canale basato su codice {#get-sarted-code-based}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione di guida:

* **[Introduzione al canale basato su codice](get-started-code-based.md)**
* [Prerequisiti basati su codice](code-based-prerequisites.md)
* [Esempi di implementazione basati su codice](code-based-implementation-samples.md)
* [Creare esperienze basate su codice](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Il canale di esperienza basato su codice è attualmente disponibile come versione beta solo per alcuni utenti. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.

[!DNL Journey Optimizer] ti consente di personalizzare e testare le esperienze che desideri fornire ai clienti in tutti i tuoi punti di contatto come: app web, app mobili, app desktop, console video, dispositivi connessi alla TV, smart TV, chioschi, sportelli bancomat, assistenti vocali, dispositivi IoT, ecc.

Con il **esperienza basata su codice** funzionalità, puoi definire le esperienze in entrata utilizzando un editor non visivo semplice e intuitivo. Consente di inserire e modificare elementi specifici in posizioni singole e più granulari delle app o delle pagine web, indipendentemente dal tipo di applicazione utilizzata, anziché applicare modifiche all’intero contenuto.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

Quando [creare una campagna](../campaigns/create-campaign.md#configure), seleziona **Esperienza basata su codice (Beta)** come azione e definire le impostazioni di base.

>[!NOTE]
>
>Se questa è la prima volta che crei un’esperienza web, assicurati di seguire i prerequisiti descritti in [questa sezione](code-based-prerequisites.md).

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
<a href="code-based-prerequisites.md"><strong>Prerequisiti</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Non frequente" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Creare un’esperienza basata su codice</strong></a>
</div>
<p></td>
<td>
<a href="create-code-based.md#edit-code">
<img alt="Convalida" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="create-code-based.md#edit-code"><strong>Modifica il codice</strong></a>
</div>
<p>
</td>
</tr></table>



<!--[Learn how to create a code-based campaign in this video](#video)-->

## Quando utilizzare canali basati su codice rispetto ad altri canali {#code-based-vs-other-channels}

### Basato su codice e altri canali

Quando utilizzare il canale basato su codice anziché l’altro [!DNL Journey Optimizer] canali?

* È possibile utilizzare le esperienze basate su codice in qualsiasi momento quando non si accede alla proprietà digitale tramite un browser web o un’app mobile, nei casi in cui probabilmente è possibile utilizzare meglio [!DNL Journey Optimizer] [canale web](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} canale.

* È possibile utilizzare il canale basato su codice in alternativa al [!DNL Journey Optimizer] canale web se il sito web non può essere caricato in [web visual editor](../web/author-web.md){target="_blank"} or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} che attiva l’authoring visivo per il canale web.

* È inoltre possibile utilizzare il canale basato su codice come alternativa al [!DNL Journey Optimizer] canali web o in-app in caso di implementazione basata su API, headless o lato server.

### Canale basato su codice e canale web

Per eseguire casi di utilizzo web, puoi utilizzare il canale web o l’esperienza basata su codice, ma a seconda del contesto, uno sarebbe più appropriato dell’altro. Le principali differenze sono elencate di seguito in modo da poter prendere una decisione informata su cosa utilizzare quando.

**Web**
* Modifica il contenuto utilizzando [editor visivo](../web/author-web.md){target="_blank"}.
* Hai bisogno di [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* Il canale web consente di modificare tutto ciò che si trova sulla pagina e dispone di un elenco predefinito di azioni che puoi utilizzare per apportare modifiche. [Ulteriori informazioni](../web/author-web.md){target="_blank"}
* È facile da configurare e andare veloce.
* È incentrato sull’addetto al marketing.

**Esperienza basata su codice**
* Modifica il contenuto utilizzando [Editor espressioni](create-code-based.md#edit-code).
* L’esperienza basata sul codice richiede un lavoro di sviluppo precedente sull’implementazione per garantire che le superfici possano interpretare e distribuire i contenuti pubblicati ai margini tramite [!DNL Journey Optimizer] per queste superfici. [Ulteriori informazioni](#surface-definition)
* Richiede una maggiore pianificazione e può modificare solo gli elementi specificati dagli sviluppatori. Pertanto, è essenziale identificare i componenti (banner Home, immagine protagonista, barra dei menu, ecc.) sulle superfici che devono essere modificate per la personalizzazione o il testing e collabora con il team di sviluppo per creare l’implementazione necessaria per gestire queste modifiche.
* Ti consente di utilizzare il contenuto del codice JSON.
* È incentrato sugli sviluppatori.

## Come funziona {#how-it-works}

>[!CAUTION]
>
>Questa funzione è destinata agli sviluppatori e/o agli utenti esperti. Può essere utilizzato da esperti di marketing con alcune competenze di scrittura del codice, purché le implementazioni di superficie e la configurazione iniziale siano gestite dal team di sviluppo.

Per modificare il contenuto utilizzando [!DNL Journey Optimizer] funzionalità di esperienza basata su codice, le pagine o le app devono essere instrumentate. Per farlo, devi dichiarare in anticipo le singole posizioni specifiche (denominate &quot;[superfici](#surface-definition)&quot;) nel punto in cui desideri inserire o sostituire il contenuto<!--HOW??-->.

>[!NOTE]
>
>Attualmente il contenuto associato a una superficie può essere solo HTML o JSON. <!--WILL COME LATER: text, image or another format depending on the application-->

I passaggi chiave per implementare una campagna basata su codice sono i seguenti.

1. Definisci un [superficie](#surface-definition), che è fondamentalmente la posizione in cui desideri aggiungere l’esperienza basata su codice e creare una campagna in [!DNL Journey Optimizer] utilizzando questa superficie. [Scopri come](create-code-based.md#create-code-based-campaign)

1. Componi un’esperienza specificando il contenuto per la superficie selezionata utilizzando [!DNL Journey Optimizer] Editor espressioni. [Scopri come](create-code-based.md#edit-code)

1. Il team di implementazione dell’app effettua chiamate API o SDK esplicite per recuperare il contenuto delle superfici denominate, ad esempio &quot;Testo banner&quot; o &quot;Cassetto 1 Recommendations&quot;, o punti decisionali non correlati all’interfaccia utente in un’applicazione, ad esempio &quot;Parametri dell’algoritmo di ricerca&quot;. In questo caso, il team di implementazione è responsabile del rendering o dell’interpretazione e dell’azione sul contenuto restituito.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## Che cos&#39;è una superficie? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definire una superficie esperienza basata su codice"
>abstract="Una superficie basata su codice è qualsiasi entità progettata per l&#39;interazione dell&#39;utente o del sistema, identificata in modo univoco da un URI."

A **superficie esperienza basata su codice** è qualsiasi entità progettata per l’interazione con l’utente o il sistema<!--ask Robert to explain further-->, identificato in modo univoco da un **URI**.

In altre parole, una superficie può essere vista come un contenitore a qualsiasi livello gerarchico con un’entità (punto di contatto) esistente.<!--good idea to illustrate how it can be seen, but to clarify-->

* Può essere una pagina web, un’app mobile, un’app desktop o una posizione di contenuto specifica all’interno di un’entità più grande (ad esempio un `div`) o un modello di visualizzazione non standard (ad esempio, un chiosco o un banner per app desktop).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Può anche estendersi a specifici contenitori di contenuto per scopi non di visualizzazione o visualizzazione astratta (ad esempio, BLOB JSON consegnati ai servizi).

* Può anche essere una superficie con caratteri jolly che corrisponde a una varietà di definizioni di superficie client (ad esempio, una posizione di immagine protagonista su ogni pagina del sito web potrebbe tradursi in un URI di superficie come: web://mydomain.com/*#hero_image).

Fondamentalmente, un URI di superficie è composto da più sezioni:
1. **Tipo**: web, mobileapp, servizio, chiosco, tvcd, ecc.
1. **Proprietà**: bundle di dominio o app
1. **Percorso**: attività pagina/app ± posizione nella pagina/attività app <!--to clarify-->

La tabella seguente elenca alcuni esempi di definizione di URI di superficie per vari dispositivi.

| Tipo | URI | Descrizione |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | Rappresenta un singolo percorso e una singola pagina di un sito Web. |
| Web | web://domain.com/path/page.html#element | Rappresenta un singolo elemento all’interno di una pagina specifica di un dominio specifico. |
| Web | web://domain.com/*#element | Superficie con caratteri jolly: rappresenta un singolo elemento in ciascuna pagina sotto un dominio specifico. |
| Desktop | desktop://com.vendor.bundle | Rappresenta un&#39;applicazione desktop specifica. |
| Desktop | desktop://com.vendor.bundle#element | Rappresenta un elemento specifico all’interno di un’applicazione, ad esempio un pulsante, un menu, un banner principale e così via. |
| App iOS | ios://com.vendor.bundle | Rappresenta un’app mobile specifica per una singola piattaforma, in questo caso l’app iOS. |
| App iOS | ios://com.vendor.bundle/activity | Rappresenta un’attività specifica (visualizzazione) all’interno di un’app mobile. |
| App iOS | ios://com.vendor.bundle/activity#element | Rappresenta un elemento specifico all’interno di un’attività, ad esempio un pulsante o un altro elemento di visualizzazione. |
| App Android | android://com.vendor.bundle | Rappresenta un’app mobile specifica per una singola piattaforma, in questo caso un’app Android. |
| app tvOS | tvos://com.vendor.bundle | Rappresenta un&#39;app tvOS specifica. |
| App TV | tvcd://com.vendor.bundle | Rappresenta un&#39;app per dispositivi collegati a smart TV o TV specifica - ID bundle. |
| Servizio | service://servicename | Rappresenta un processo lato server o altra entità manuale. |
| Chiosco | kiosk://location/screen | Esempio di possibili tipi di superficie aggiuntivi che possono essere aggiunti facilmente. |
| ATM | atm://location/screen | Esempio di possibili tipi di superficie aggiuntivi che possono essere aggiunti facilmente. |