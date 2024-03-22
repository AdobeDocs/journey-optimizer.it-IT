---
title: Introduzione alle esperienze basate su codice
description: Scopri le esperienze basate su codice in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 3c9952f2e57c45d5bbd78d70ae7d401bc4555abe
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 81%

---

# Introduzione al canale basato su codice {#get-sarted-code-based}

[!DNL Journey Optimizer] consente di personalizzare e testare le esperienze che desideri fornire ai clienti in tutti i tuoi punti di contatto: app web, app mobili, app desktop, console video, dispositivi Connected TV, smart TV, chioschi, sportelli automatici, assistenti vocali, dispositivi IoT, ecc.

Con la funzionalità per **esperienza basata su codice**, puoi definire le esperienze in entrata utilizzando un editor non visivo semplice e intuitivo. Questo consente di inserire e modificare elementi specifici in posizioni singole e più granulari delle app o delle pagine web, indipendentemente dal tipo di applicazione utilizzata, anziché applicare modifiche all’intero contenuto.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!NOTE]
>
>* Se questa è la prima volta che crei un’esperienza basata su codice, assicurati di seguire i prerequisiti descritti in [questa sezione](code-based-prerequisites.md).
>
>* Attualmente in [!DNL Journey Optimizer] puoi creare esperienze basate su codice solo utilizzando **campagne**.
>
>>* Il canale di esperienza basato su codice non è disponibile per le organizzazioni che hanno acquistato l’Adobe **Healthcare Shield** e **Privacy e sicurezza** offerte aggiuntive.

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

* È possibile utilizzare le esperienze basate su codice in qualsiasi momento quando non si accede alla proprietà digitale tramite un browser web o un’app mobile; in questi ultimi casi, infatti, è spesso preferibile utilizzare il [canale Web](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} di [!DNL Journey Optimizer].

* È possibile utilizzare il canale Basato su codice in alternativa al canale Web di [!DNL Journey Optimizer] se il sito web non può essere caricato nel [Designer web](../web/edit-web-content.md#work-with-web-designer){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} che attiva l’authoring visivo per il canale Web.

* Inoltre, il canale Basato su codice può essere usato in alternativa ai canali Web o In-app di [!DNL Journey Optimizer] in caso di implementazioni basate su API, headless o lato server.

### Canale Basato su codice e canale Web

Per casi di utilizzo web, puoi utilizzare il canale web o l’esperienza basata su codice, ma a seconda del contesto, uno può essere più appropriato dell’altro. Le principali differenze elencate di seguito ti aiuteranno a decidere quale canale scegliere in base alle tue esigenze.

**Web**
* Modifica il contenuto utilizzando l’editor visivo [Designer web](../web/edit-web-content.md#work-with-web-designer){target="_blank"}.
* È necessario utilizzare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* Il canale Web consente di modificare tutto ciò che si trova sulla pagina e dispone di un elenco preimpostato di azioni che puoi utilizzare per apportare modifiche. [Ulteriori informazioni](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* È facile e veloce da configurare.
* È incentrato sul ruolo di marketer.

**Esperienza basata su codice**
* Modifica il contenuto utilizzando l’[editor di espressioni](create-code-based.md#edit-code).
* Prima di creare esperienze basate su codice, è necessario intervenire a livello di sviluppo sulla propria implementazione affinché le superfici possano interpretare e consegnare i contenuti pubblicati nell’ambiente Edge da [!DNL Journey Optimizer] per queste superfici. [Ulteriori informazioni](#surface-definition)
* Richiede una maggiore pianificazione ed è possibile modificare solo gli elementi specificati dagli sviluppatori. Pertanto, è essenziale identificare i componenti (banner Home, immagine hero, barra dei menu, ecc.) sulle superfici che devono essere modificati per la personalizzazione o il testing e collaborare con il team di sviluppo per creare l’implementazione necessaria per gestire queste modifiche.
* Consente di utilizzare contenuti creati con codice JSON.
* È incentrata sugli sviluppatori.

## Come funziona {#how-it-works}

>[!CAUTION]
>
>Questa funzione è destinata agli sviluppatori e/o utenti esperti. Può essere utilizzata da marketer con alcune competenze di scrittura del codice, purché le implementazioni di superficie e la configurazione iniziale siano gestite dal team di sviluppo.

Per modificare il contenuto utilizzando la funzionalità di esperienza basata su codice di [!DNL Journey Optimizer], le pagine o le app devono essere strumentate. Per farlo, è necessario specificare in anticipo le singole posizioni (denominate “[superfici](#surface-definition)”) nel punto in cui desideri inserire o sostituire il contenuto<!--HOW??-->.

>[!NOTE]
>
>Attualmente il contenuto associato a una superficie può essere solo HTML o JSON. <!--WILL COME LATER: text, image or another format depending on the application-->

I passaggi chiave per implementare una campagna basata su codice sono i seguenti.

1. Definisci una [superficie](#surface-definition), che, in sostanza, è la posizione in cui desideri aggiungere l’esperienza basata su codice e crea una campagna in [!DNL Journey Optimizer] utilizzando tale superficie. [Scopri come](create-code-based.md#create-code-based-campaign)

1. Comporre un’esperienza specificando il contenuto per la superficie selezionata utilizzando l’Editor espressioni di [!DNL Journey Optimizer]. [Scopri come](create-code-based.md#edit-code)

1. Il team di implementazione dell’app effettua chiamate API o SDK esplicite per recuperare il contenuto delle superfici denominate, ad esempio “Testo banner” o “Area 1 Consigli”, o punti decisionali non correlati all’interfaccia utente in un’applicazione, ad esempio “Parametri dell’algoritmo di ricerca”. In questo caso, il team di implementazione è responsabile del rendering o dell’interpretazione e dell’azione sul contenuto restituito.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## Che cos’è una superficie? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definizione di una superficie esperienza basata su codice"
>abstract="Una superficie basata su codice è qualsiasi entità progettata per l’interazione dell’utente o del sistema, identificata in modo univoco da un URI."

Una **superficie esperienza basata su codice** è qualsiasi entità progettata per l’interazione con l’utente o il sistema<!--ask Robert to explain further-->, identificata in modo univoco da un **URI**.

In altre parole, una superficie può essere vista come un contenitore a qualsiasi livello gerarchico con un’entità (punto di contatto) esistente.<!--good idea to illustrate how it can be seen, but to clarify-->

* Può essere una pagina web, un’app mobile, un’app desktop o una posizione di contenuto specifica all’interno di un’entità più grande (ad esempio un `div`) o un pattern di visualizzazione non standard (ad esempio, un chiosco o un banner per app desktop).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Può anche estendersi a contenitori di contenuto specifici per scopi non di visualizzazione o visualizzazione astratta (ad esempio, BLOB JSON consegnati ai servizi).

* Può anche essere una superficie con caratteri jolly che corrisponde a una varietà di definizioni di superficie client (ad esempio, la posizione di un’immagine principale su ogni pagina del sito web potrebbe tradursi in un URI di superficie come: web://mydomain.com/*#hero_image).

Fondamentalmente, un URI di superficie è composto da più sezioni:
1. **Tipo**: web, mobileapp, atm, chiosco, tvcd, servizio, ecc.
1. **Proprietà**: URL della pagina o bundle dell’app
1. **Contenitore**: posizione nell’attività pagina/app

Le tabelle seguenti elencano alcuni esempi di definizione di URI di superficie per vari dispositivi.

**Web e dispositivi mobili**

| Tipo | URI | Descrizione |
| --------- | ----------- | ------- | 
| Web | web://domain.com/path/page.html#element | Rappresenta un singolo elemento all’interno di una pagina specifica di un dominio specifico, dove un elemento può essere un’etichetta come negli esempi seguenti: hero_banner, top_nav, menu, piè di pagina, ecc. |
| App iOS | mobileapp://com.vendor.bundle/activity#element | Rappresenta un elemento specifico all’interno di un’attività nativa dell’app, ad esempio un pulsante o un altro elemento di visualizzazione. |
| App Android | mobileapp://com.vendor.bundle#element | Rappresenta un elemento specifico di un&#39;app nativa. |

**Altri tipi di dispositivi**

| Tipo | URI | Descrizione |
| --------- | ----------- | ------- | 
| Desktop | desktop://com.vendor.bundle#element | Rappresenta un elemento specifico all’interno di un’applicazione, ad esempio un pulsante, un menu, un banner principale e così via. |
| App TV | tvcd://com.vendor.bundle#element | Rappresenta un elemento specifico all’interno di un’app per dispositivi connessi a smart TV o TV - ID bundle. |
| Servizio | service://servicename#element | Rappresenta un processo lato server o altra entità manuale. |
| Chiosco | kiosk://location/screen#element | Esempio di possibili ulteriori tipi di superficie che possono essere aggiunti facilmente. |
| ATM | atm://location/screen#element | Esempio di possibili ulteriori tipi di superficie che possono essere aggiunti facilmente. |

**Superfici con caratteri jolly**

| Tipo | URI | Descrizione |
| --------- | ----------- | ------- | 
| Web con caratteri jolly | carattere jolly:web://domain.com/`*`#element | Superficie con caratteri jolly: rappresenta un singolo elemento in ciascuna pagina in un dominio specifico. |
| Web con caratteri jolly | carattere jolly:web://`*`domain.com/`*`#element | Superficie con caratteri jolly: rappresenta un singolo elemento in ciascuna pagina sotto tutti i domini che terminano con &quot;domain.com&quot;. |


