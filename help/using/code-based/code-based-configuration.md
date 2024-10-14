---
title: Configurazione basata su codice
description: Creare una configurazione basata su codice
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: e3c597f66436e8e0e22d06f1905fc7ca9a9dd570
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 30%

---

# Configurare l’esperienza basata su codice in anteprima {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definire una configurazione di esperienza basata su codice"
>abstract="Una configurazione basata su codice definisce il percorso e la posizione all’interno dell’applicazione, identificati in modo univoco da un URI nell’implementazione dell’applicazione, in cui il contenuto verrà consegnato e utilizzato."

Prima di [creare la tua esperienza](create-code-based.md), devi creare una configurazione di esperienza basata su codice in cui definisci dove verranno consegnati e utilizzati i contenuti all&#39;interno dell&#39;applicazione.

Una configurazione di esperienza basata su codice deve fare riferimento alla superficie, che è fondamentalmente la posizione in cui desideri eseguire il rendering delle modifiche. A seconda della piattaforma selezionata, è necessario immettere una posizione o un percorso oppure l&#39;URI della superficie completa. [Ulteriori informazioni](#surface-definition)

## Creare una configurazione di esperienza basata su codice {#create-code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Immetti la posizione specifica"
>abstract="Questo campo specifica la destinazione esatta sulla pagina o all’interno dell’app a cui desideri che gli utenti accedano. Potrebbe trattarsi di una sezione o di una pagina specifica all’interno della struttura di navigazione."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="Definisci un URL per la creazione e l’anteprima dei contenuti"
>abstract="Questo campo assicura che le pagine generate o associate dalla regola abbiano un URL designato, essenziale sia per la creazione che per l’anteprima efficace del contenuto."

Per creare una configurazione del canale esperienza basata su codice, effettua le seguenti operazioni:

1. Accedi al menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**, quindi fai clic su **[!UICONTROL Crea configurazione canale]**.

   ![](assets/code_config_1.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri di sottolineatura `_`, punto`.` e trattino `-`.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla configurazione, è possibile selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto (OLAC)](../administration/object-based-access.md)

1. Seleziona **[!UICONTROL Azione di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

1. Seleziona il canale **esperienza basata su codice**.

   ![](assets/code_config_2.png)

1. Seleziona la piattaforma per la quale verrà applicata l’esperienza basata su codice:

   * [Web](#web)
   * [iOS e/o Android](#mobile)
   * [Altro](#other)

   >[!NOTE]
   >
   >Puoi selezionare diverse piattaforme. Quando si selezionano più piattaforme, il contenuto viene distribuito a tutte le pagine o app selezionate.

1. Scegliere il formato previsto dall&#39;applicazione per questa posizione particolare. Verrà utilizzato per creare l’esperienza basata su codice in campagne e percorsi.

   ![](assets/code_config_4.png)

1. Fai clic su **[!UICONTROL Invia]** per salvare le modifiche.

Ora puoi selezionare questa configurazione durante [la creazione di un&#39;esperienza basata su codice](create-code-based.md) nelle campagne e nei percorsi.

>[!NOTE]
>
>Il team di implementazione dell’app è responsabile dell’esecuzione di chiamate API o SDK esplicite per recuperare il contenuto per le superfici definite nella configurazione dell’esperienza basata su codice selezionata. Ulteriori informazioni sulle diverse implementazioni del cliente in [questa sezione](code-based-implementation-samples.md).

### Piattaforme web {#web}

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="Definire un URL per l’authoring e l’anteprima dei contenuti"
>abstract="Questo campo assicura che le pagine generate o associate dalla regola abbiano un URL designato, essenziale sia per la creazione che per l’anteprima efficace del contenuto."

Per definire le impostazioni di configurazione dell’esperienza basata su codice per le piattaforme web, segui i passaggi indicati di seguito.

1. Selezionare una delle opzioni seguenti:

   * **[!UICONTROL Pagina singola]** - Se desideri applicare le modifiche esclusivamente a una singola pagina, immetti un **[!UICONTROL URL pagina]**.

     ![](assets/code_config_single_page.png)

   * **[!UICONTROL Regola di corrispondenza pagine]** - Per eseguire il targeting di più URL che corrispondono alla stessa regola, genera una o più regole. [Ulteriori informazioni](../web/web-configuration.md#web-page-matching-rule)

     <!--This could be used to apply changes universally across a website, such as updating a hero banner across all pages or adding a top image to display on every product page.-->

     Ad esempio, se desideri modificare gli elementi visualizzati in tutte le pagine del sito Web Luma relative alle donne, seleziona **[!UICONTROL Dominio]** > **[!UICONTROL Inizia con]** > `luma` e **[!UICONTROL Pagina]** > **[!UICONTROL Contiene]** > `women`.

     ![](assets/code_config_matching_rules.png)

1. Per l’URL di anteprima vale quanto segue:

   * Se viene immesso un URL di una singola pagina, questo verrà utilizzato per l’anteprima e non è necessario immettere un altro URL.
   * Se è selezionata una [regola corrispondente alle pagine](../web/web-configuration.md#web-page-matching-rule), devi immettere un **[!UICONTROL URL predefinito per l&#39;authoring e l&#39;anteprima]** che verrà utilizzato per visualizzare l&#39;anteprima dell&#39;esperienza nel browser.

     ![](assets/code_config_matching_rules_preview.png)

1. Il campo **[!UICONTROL Posizione a pagina]** specifica la destinazione esatta all&#39;interno del sito Web a cui si desidera che gli utenti accedano. Potrebbe trattarsi di una sezione o di una pagina specifica nella struttura di navigazione del sito.

   ![](assets/code_config_location_on_page.png)

### Piattaforme mobili (iOS e Android) {#mobile}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="Immetti l&#39;ID dell&#39;app"
>abstract="Immetti l’ID dell’app per un’identificazione e una configurazione precise all’interno dell’ambiente operativo dell’applicazione, garantendo un’integrazione e funzionalità senza soluzione di continuità."

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="Immetti l&#39;URL per l&#39;anteprima del contenuto"
>abstract="Questo campo è essenziale per abilitare la simulazione e l’anteprima del contenuto direttamente sul dispositivo all’interno dell’applicazione."

Per definire le impostazioni di configurazione dell’esperienza basata su codice per le piattaforme mobili, segui i passaggi indicati di seguito.

1. Immetti **[!UICONTROL ID app]**. Questo consente un’identificazione e una configurazione accurate all’interno dell’ambiente operativo dell’app e garantisce l’integrazione e la funzionalità senza interruzioni.

1. Specifica il percorso o la posizione **[!UICONTROL nell&#39;app]**. Questo campo specifica la destinazione esatta all’interno dell’app a cui desideri che gli utenti accedano. Potrebbe trattarsi di una sezione o di una pagina specifica nella struttura di navigazione dell’app.

   ![](assets/code_config_3.png){width="500"}

1. Compila il campo **[!UICONTROL URL anteprima]** per abilitare le anteprime su dispositivo. Questo URL informa il servizio di anteprima dell&#39;URL specifico da utilizzare quando si attiva un&#39;anteprima<!--on device. Learn more-->.

   L’URL di anteprima è un collegamento profondo configurato dallo sviluppatore dell’app all’interno dell’app. In questo modo, gli URL che corrispondono allo schema di collegamento profondo si apriranno all’interno dell’app anziché in un browser web per dispositivi mobili. Contatta il tuo sviluppatore di app per ottenere lo schema di collegamento profondo configurato per la tua app.

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

### Altre piattaforme {#other}

Per definire le impostazioni di configurazione dell’esperienza basata su codice per altre piattaforme (come console video, dispositivi collegati alla TV, smart TV, chioschi, sportelli bancomat, assistenti vocali, dispositivi IoT e così via), segui la procedura riportata di seguito.

1. Seleziona **[!UICONTROL Altro]** come piattaforma se la tua implementazione non è per Web, iOS o Android oppure se devi eseguire il targeting di URI specifici.

1. Immettere l&#39;**[!UICONTROL URI superficie]**. [Ulteriori informazioni](#surface-definition)

   ![](assets/code_config_5.png)

   >[!CAUTION]
   >
   >Assicurati di immettere un URI di superficie che corrisponda a quello utilizzato nella tua implementazione. In caso contrario, non sarà possibile consegnare le modifiche.

1. **[!UICONTROL Se necessario, aggiungere un altro URI di superficie]**. Puoi aggiungere fino a 10 URI.

   >[!NOTE]
   >
   >Quando si aggiungono più URI, il contenuto viene distribuito a tutti i componenti elencati.

## Che cos&#39;è un URI di superficie? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="Aggiungere l’URI della superficie per il componente"
>abstract="Se l’implementazione non è per il Web, iOS o Android, oppure se devi eseguire il targeting di URI specifici, immetti un URI di superficie, che è un identificatore univoco che si dirige all’entità in cui desideri distribuire l’esperienza. Assicurati di immettere un URI di superficie che corrisponda a quello utilizzato nella tua implementazione."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/code-based-configuration#other" text="Creare una configurazione di esperienza basata su codice per altre piattaforme"

Un&#39;esperienza basata su codice **surface** è qualsiasi entità progettata per l&#39;interazione utente o di sistema, identificata in modo univoco da un **URI**. La superficie è specificata nell&#39;implementazione dell&#39;applicazione e deve corrispondere alla superficie a cui si fa riferimento nella configurazione del canale esperienza basato su codice.

Una superficie può essere vista come un contenitore a qualsiasi livello gerarchico con un’entità (punto di contatto) esistente.

* Può essere una pagina web, un’app mobile, un’app desktop o una posizione di contenuto specifica all’interno di un’entità più grande (ad esempio un `div`) o un pattern di visualizzazione non standard (ad esempio, un chiosco o un banner per app desktop).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Può anche estendersi a contenitori di contenuto specifici per scopi non di visualizzazione o visualizzazione astratta (ad esempio, BLOB JSON consegnati ai servizi).

* Può anche essere una superficie con caratteri jolly che corrisponde a una varietà di definizioni di superficie client (ad esempio, la posizione di un’immagine principale su ogni pagina del sito web potrebbe tradursi in un URI di superficie come: web://mydomain.com/*#hero_image).

Quando crei una configurazione del canale esperienza basata su codice, puoi specificare la superficie in due modi in base alla piattaforma selezionata:

* Per le piattaforme **[!UICONTROL Web]**, **[!UICONTROL iOS]** e **[!UICONTROL Android]**, è necessario immettere una **posizione o un percorso** per comporre la superficie.

* Se la piattaforma è **[!UICONTROL Altro]**, è necessario immettere l&#39;**URI di superficie** completo, come negli esempi seguenti.

Un URI di superficie funge da identificatore preciso che si dirige verso elementi o componenti distinti dell’interfaccia utente all’interno di un’applicazione. Fondamentalmente, un URI di superficie è composto da più sezioni:

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
