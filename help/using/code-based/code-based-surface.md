---
title: Superficie basata su codice
description: Scopri cos’è una superficie di esperienza basata su codice
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: e9181c333fb9188cdfcee3fd96c1d3bb94b8dd75
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 42%

---

# Superfici di esperienza basate su codice {#code-based-surface}

## Che cos’è una superficie? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="Aggiungere l’URI della superficie per il componente"
>abstract="Se l’implementazione non è per il Web, iOS o Android, oppure se devi eseguire il targeting di URI specifici, immetti un URI di superficie, che è un identificatore univoco che si dirige all’entità in cui desideri distribuire l’esperienza. Assicurati di immettere un URI di superficie che corrisponda a quello utilizzato nella tua implementazione."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="Creare una configurazione di esperienza basata su codice per altre piattaforme"

Un&#39;esperienza basata su codice **surface** è qualsiasi entità progettata per l&#39;interazione dell&#39;utente o del sistema, identificata in modo univoco da un [URI](#surface-uri). La superficie è specificata nell&#39;implementazione [dell&#39;applicazione](code-based-prerequisites.md#implementation-prerequisites) e deve corrispondere alla superficie a cui si fa riferimento nella [configurazione del canale esperienza basata su codice](code-based-configuration.md).

Una superficie può essere vista come un contenitore a qualsiasi livello gerarchico con un’entità (punto di contatto) esistente.

* Può essere una pagina web, un’app mobile, un’app desktop o una posizione di contenuto specifica all’interno di un’entità più grande (ad esempio un `div`) o un pattern di visualizzazione non standard (ad esempio, un chiosco o un banner per app desktop).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Può anche estendersi a contenitori di contenuto specifici per scopi non di visualizzazione o visualizzazione astratta (ad esempio, BLOB JSON consegnati ai servizi).

* Può anche essere una superficie con caratteri jolly che corrisponde a una varietà di definizioni di superficie client (ad esempio, la posizione di un’immagine principale su ogni pagina del sito web potrebbe tradursi in un URI di superficie come: web://mydomain.com/*#hero_image).

## Identificatore di superficie {#surface-uri}

Un **URI di superficie** funge da identificatore preciso per indirizzare elementi o componenti distinti dell&#39;interfaccia utente in un&#39;applicazione. Fondamentalmente, un URI di superficie è composto da più sezioni:

1. **Tipo**: web, app mobile, sportello bancomat, chiosco, tvcd, servizio ecc.
1. **Proprietà**: URL pagina o pacchetto di app
1. **Contenitore**: posizione nell’attività pagina/app

La tabella seguente elenca alcuni esempi di definizione di URI di superficie per vari dispositivi.

**Web e dispositivi mobili**

| Tipo | URI | Descrizione |
| --------- | ----------- | ------- | 
| Web | `web://domain.com/path/page.html#element` | Rappresenta un singolo elemento all’interno di una pagina specifica di un dominio specifico, dove un elemento può essere un’etichetta come negli esempi seguenti: hero_banner, top_nav, menu, piè di pagina, ecc. |
| App iOS | `mobileapp://com.vendor.bundle/activity#element` | Rappresenta un elemento specifico all’interno dell’attività di un’app nativa, ad esempio un pulsante o un altro elemento della vista. |
| App Android | `mobileapp://com.vendor.bundle/#element` | Rappresenta un elemento specifico di un’app nativa. |

**Altri tipi di dispositivi**

| Tipo | URI | Descrizione |
| --------- | ----------- | ------- | 
| Desktop | `desktop://com.vendor.bundle/#element` | Rappresenta un elemento specifico all’interno di un’applicazione, ad esempio un pulsante, un menu, un banner principale e così via. |
| App TV | `tvcd://com.vendor.bundle/#element` | Rappresenta un elemento specifico all’interno di un bundle di app per dispositivi collegati a smart TV o TV. |
| Servizio | `service://servicename/#element` | Rappresenta un processo lato server o altra entità manuale. |
| Chiosco | `kiosk://location/screen#element` | Esempio di possibili ulteriori tipi di superficie che possono essere aggiunti facilmente. |
| ATM | `atm://location/screen#element` | Esempio di possibili ulteriori tipi di superficie che possono essere aggiunti facilmente. |

**Superfici jolly**

| Tipo | URI | Descrizione |
| --------- | ----------- | ------- | 
| Web jolly | `wildcard:web://domain.com/*#element` | Superficie jolly: rappresenta un singolo elemento in ciascuna pagina in un dominio specifico. |
| Web jolly | `wildcard:web://*domain.com/*#element` | Superficie jolly: rappresenta un singolo elemento in ciascuna pagina di tutti i domini che finiscono con “domain.com”. |

## Composizione URI {#uri-composition}

In [!DNL Journey Optimizer], il canale di esperienza basato su codice supporta due tipi di implementazioni del cliente:

* In base a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} per i tuoi siti Web o a [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} per le tue app mobili;
* Lato server o ibrido tramite [API server Edge Network AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"}.

>[!NOTE]
>
>Ulteriori informazioni sui prerequisiti di implementazione in [questa sezione](code-based-prerequisites.md#implementation-prerequisites).

Utilizzando esperienze basate su codice, puoi modificare il contenuto nelle posizioni granulari <!--(such as a specific location on a page, or inside a mobile native app)--> che sono identificate in modo univoco da [!DNL Journey Optimizer] utilizzando [URI di superficie](#surface-uri).

Questi URI di superficie sono composti e gestiti a seconda del metodo di implementazione:

* **Web/Mobile SDK**: lo sviluppatore Web/Mobile deve definire queste posizioni granulari come stringhe semplici, perché Web/Mobile SDK è in grado di comporre automaticamente l&#39;URI di superficie in base all&#39;URL/ID app corrente e alla stringa di posizione.

* **API di Edge Network**: lo sviluppatore di app/pagine deve definire URI di superficie completi che includano il percorso completo e la posizione in cui verrà utilizzato il contenuto, perché in questo tipo di implementazione sono necessari URI completi.

Per questo motivo, quando crei una configurazione del canale esperienza basata su [codice](code-based-configuration.md), puoi specificare la superficie in due modi in base alla piattaforma selezionata:

* Per le piattaforme **[!UICONTROL Web]**, **[!UICONTROL iOS]** e **[!UICONTROL Android]**, è necessario immettere l&#39;**URL/ID app** e un **percorso o percorso** per comporre la superficie. Ulteriori informazioni sulla configurazione di esperienze basate su codice per piattaforme [web](code-based-configuration.md#web) e [mobile](code-based-configuration.md#mobile)

* Se la piattaforma è **[!UICONTROL Altro]**, devi immettere l&#39;**URI di superficie** completo, come negli esempi [precedenti](#surface-uri). Ulteriori informazioni sulla configurazione di esperienze basate su codice per [altre](code-based-configuration.md#other) piattaforme
