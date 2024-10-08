---
title: Configurazione basata su codice
description: Creare una configurazione basata su codice
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 50%

---

# Configurare l’esperienza basata su codice in anteprima {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="ID app"
>abstract="Fornisci l’ID dell’app per la sua corretta identificazione e configurazione nell’ambiente operativo dell’app, in modo da garantire integrazione e funzionalità dirette."

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Posizione sulla pagina"
>abstract="Il campo Posizione o percorso nell’app specifica la destinazione esatta all’interno dell’app a cui gli utenti dovranno accedere. Potrebbe trattarsi di una sezione o di una pagina specifica nella struttura di navigazione dell’app."

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="URI di superficie"
>abstract="Un URI di superficie funge da identificatore preciso per indirizzare elementi o componenti distinti dell’interfaccia utente all’interno di un’applicazione."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="URL predefinito per authoring e anteprima"
>abstract="Questo campo assicura che le pagine generate o associate dalla regola abbiano un URL designato, essenziale sia per la creazione che per l’anteprima efficace del contenuto."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="URL predefinito per authoring e anteprima"
>abstract="Questo campo assicura che le pagine generate o associate dalla regola abbiano un URL designato, essenziale sia per la creazione che per l’anteprima efficace del contenuto."

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="URL di anteprima"
>abstract="Questo campo è essenziale per abilitare la simulazione e l’anteprima del contenuto direttamente sul dispositivo all’interno dell’applicazione."

## Creare una configurazione dei canali {#reatte-code-based-configuration}

Per creare una configurazione di canale, effettua le seguenti operazioni:

1. Accedi al menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**, quindi fai clic su **[!UICONTROL Crea configurazione canale]**.

   ![](assets/code_config_1.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri di sottolineatura `_`, punto`.` e trattino `-`.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla configurazione, è possibile selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

1. Seleziona **[!UICONTROL Azione di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

1. Seleziona **Canale esperienza basata su codice**.

   ![](assets/code_config_2.png)

1. Seleziona la piattaforma per la quale verrà applicata l’esperienza basata su codice.

1. Per il Web:

   * Specifica un **[!UICONTROL URL pagina]** per applicare le modifiche esclusivamente a una singola pagina.

   * In alternativa, crea una **[!UICONTROL regola di corrispondenza pagine]** per eseguire il targeting di più URL che corrispondono alla regola specificata. Ad esempio, potrebbe essere utilizzato per applicare modifiche universalmente a un sito web, ad esempio per aggiornare un banner hero in tutte le pagine o aggiungere un’immagine superiore da visualizzare su ogni pagina di prodotto. [Ulteriori informazioni](../web/web-configuration.md)

1. Per iOS e Android:

   * Immetti **[!UICONTROL ID app]** e **[!UICONTROL Posizione o percorso nell&#39;app]**.

     ![](assets/code_config_3.png){width="500"}

1. Seleziona Altro come piattaforma se l’implementazione non è per Web, iOS o Android oppure se devi eseguire il targeting di URI specifici. Quando si scelgono più piattaforme o si aggiungono più URI, il contenuto viene distribuito a tutte le pagine o app selezionate.

   * Immettere l&#39;**[!UICONTROL URI superficie]**.

   >[!CAUTION]
   >
   >Assicurati che l’URI di superficie utilizzato nella campagna basata su codice corrisponda a quello utilizzato nella tua implementazione. In caso contrario, le modifiche non verranno consegnate.

1. Compila il campo **[!UICONTROL URL anteprima]** per abilitare le anteprime su dispositivo. Questo URL informa il servizio di anteprima dell’URL specifico da utilizzare quando si attiva un’anteprima.

   * Per il Web:

      * Se viene immesso un URL di una singola pagina, verrà utilizzato per l’anteprima.
      * Se è selezionata una regola di corrispondenza della pagina, devi immettere un URL di anteprima predefinito che verrà utilizzato per visualizzare l’anteprima dell’esperienza nel browser.

   * Per piattaforme mobili (iOS/Android):

      * L’URL di anteprima è un collegamento diretto configurato dallo sviluppatore dell’app all’interno dell’app. In questo modo, gli URL corrispondenti allo schema del collegamento diretto si apriranno all’interno dell’app anziché in un browser web per dispositivi mobili. Contatta il tuo sviluppatore di app per ottenere lo schema di deep link configurato per la tua app.

+++  Le seguenti risorse possono essere utili per configurare collegamenti profondi per l’implementazione dell’app

      * Per Android:

         * [Creare deep link al contesto dell’app](https://developer.android.com/training/app-links/deep-linking)

      * Per iOS:

         * [Definizione di uno schema URL personalizzato per l’app](https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app)

         * [Supporto dei collegamenti universali nell’app](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)

+++

   >[!NOTE]
   >
   >In caso di problemi durante l&#39;anteprima dell&#39;esperienza, consulta [questa documentazione](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/troubleshooting#app-does-not-open-link).

1. Scegli il formato previsto dall’applicazione in quella particolare posizione. Verrà utilizzato per creare l’esperienza basata su codice in campagne e percorsi.

1. Invia le modifiche.

Ora puoi selezionare la configurazione durante la creazione dell’esperienza basata su codice.


## Che cos’è una superficie? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definire una configurazione di esperienza basata su codice"
>abstract="Una configurazione basata su codice definisce il percorso e la posizione all’interno dell’applicazione, identificati in modo univoco da un URI nell’implementazione dell’applicazione, in cui il contenuto verrà consegnato e utilizzato."

Una **superficie esperienza basata su codice** è qualsiasi entità progettata per l&#39;interazione dell&#39;utente o del sistema, identificata in modo univoco da un URI. La superficie è specificata nell’implementazione dell’applicazione e deve corrispondere a quella composta nella configurazione del canale esperienza basato su codice.

Durante la creazione di una configurazione del canale di esperienza basata su codice, per le piattaforme Web, iOS e Android devi immettere un percorso e una posizione per comporre la superficie; se la piattaforma è Altro, invece, devi immettere l’URI completo, come negli esempi seguenti.

In altre parole, una superficie può essere vista come un contenitore a qualsiasi livello gerarchico con un’entità (punto di contatto) esistente.<!--good idea to illustrate how it can be seen, but to clarify-->

* Può essere una pagina web, un’app mobile, un’app desktop o una posizione di contenuto specifica all’interno di un’entità più grande (ad esempio un `div`) o un pattern di visualizzazione non standard (ad esempio, un chiosco o un banner per app desktop).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Può anche estendersi a contenitori di contenuto specifici per scopi non di visualizzazione o visualizzazione astratta (ad esempio, BLOB JSON consegnati ai servizi).

* Può anche essere una superficie con caratteri jolly che corrisponde a una varietà di definizioni di superficie client (ad esempio, la posizione di un’immagine principale su ogni pagina del sito web potrebbe tradursi in un URI di superficie come: web://mydomain.com/*#hero_image).

Fondamentalmente, un URI di superficie è composto da più sezioni:
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
