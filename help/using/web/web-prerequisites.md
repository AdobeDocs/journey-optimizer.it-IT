---
title: Prerequisiti per il canale Web
description: Per poter accedere e creare pagine web nell’interfaccia utente di Journey Optimizer, segui i prerequisiti riportati in questa pagina
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 1f9841ddd039a7591f396e38d8a93ed840d6879e
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 5%

---

# Prerequisiti e guardrail {#web-prerequisites}

Per poter accedere e creare pagine Web nell&#39;interfaccia utente [!DNL Journey Optimizer], attenersi ai prerequisiti seguenti:

* Per aggiungere modifiche al sito web, devi disporre di un’implementazione specifica. [Ulteriori informazioni](#implementation-prerequisites)

* Per accedere al Web Designer [!DNL Journey Optimizer], è necessario che sia installata un&#39;estensione del browser Google Chrome specifica. [Ulteriori informazioni](#visual-authoring-prerequisites)

* Affinché l&#39;esperienza Web venga distribuita correttamente, assicurati di definire le impostazioni Adobe Experience Platform dettagliate [qui](#delivery-prerequisites).

* Per abilitare il reporting per il canale web, devi assicurarti che il set di dati utilizzato nel flusso di dati dell’implementazione web sia incluso anche nella configurazione di reporting. [Ulteriori informazioni](#experiment-prerequisites)

>[!NOTE]
>
>Quando esegui il targeting di profili pseudonimi (visitatori non autenticati) con le pagine web, puoi impostare un valore TTL (Time-To-Live) per l’eliminazione automatica del profilo, in modo da gestire il conteggio dei profili coinvolgibili e i costi associati. [Ulteriori informazioni](../start/guardrails.md#profile-management-inbound)

## Prerequisiti per l’implementazione {#implementation-prerequisites}

Sono supportati due tipi di implementazioni per abilitare l’authoring e la distribuzione di campagne canale web sulle proprietà web:

* Solo lato client: per aggiungere modifiche al sito Web, è necessario implementare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} nel sito Web.

  >[!NOTE]
  >
  >Verifica che la versione di [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/release-notes){target="_blank"} sia 2.16 o successiva.

* Modalità ibrida: è possibile utilizzare l&#39;[API server AEP Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=it){target="_blank"} per richiedere la personalizzazione lato server; la risposta viene fornita a Adobe Experience Platform Web SDK per eseguire il rendering delle modifiche lato client. Per ulteriori informazioni, consulta la [documentazione sulle API server di Adobe Experience Platform per Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=it){target="_blank"}. Per ulteriori informazioni sulla modalità ibrida, consulta alcuni esempi di implementazione in [questo post di blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>L’implementazione solo lato server non è attualmente supportata con il canale web. Se hai un&#39;implementazione solo lato server per le pagine Web, puoi utilizzare invece il [canale di esperienza basato su codice](../code-based/get-started-code-based.md).

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}.-->

## Prerequisiti per l’authoring visivo {#visual-authoring-prerequisites}

>[!CONTEXTUALHELP]
>id="ajo_web_browser_extension"
>title="Creare una regola di corrispondenza delle pagine"
>abstract="Per accedere al designer web di [!DNL Journey Optimizer], è necessario che sia installata un’estensione specifica del browser: Visual Editing Helper di Adobe Experience Cloud, disponibile solo in Google Chrome o Microsoft Edge."

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Per poter aprire, creare e visualizzare in anteprima le pagine Web in modo affidabile nel Web designer [!DNL Journey Optimizer], è necessario che nel browser sia installata l&#39;estensione del browser [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}.

>[!CAUTION]
>
>Google Chrome e Microsoft Edge sono attualmente gli unici browser che supportano la creazione di pagine Web in [!DNL Journey Optimizer].

### Installare l’estensione Helper per editing video {#install-visual-editing-helper}

Per scaricare e installare l’estensione del browser Helper per editing video, effettua le seguenti operazioni.

1. Apri una nuova scheda nel browser (Google Chrome o Microsoft Edge).

1. Vai al [Google Chrome Web Store](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Se utilizzi Microsoft Edge, seleziona **[!UICONTROL Consenti estensioni da altri store]** nel banner superiore. In questo modo sarà possibile aggiungere estensioni dal Chrome Web Store a Microsoft Edge.

1. Cerca e passa all&#39;estensione del browser [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}.

1. Fai clic su **[!UICONTROL Aggiungi a Chrome]** > **[!UICONTROL Aggiungi estensione]**.

   >[!NOTE]
   >
   >Se utilizzi Microsoft Edge, l&#39;estensione verrà aggiunta ad Edge anche se il pulsante è etichettato come **[!UICONTROL Aggiungi a Chrome]**.

1. Assicurati che l’estensione del browser Helper per editing video sia abilitata correttamente nella barra degli strumenti del browser.

   ![](assets/web-visual-editing-extension-edge.png)

Helper per editing video di Adobe Experience Cloud ora viene attivato automaticamente quando si apre un sito Web in [!DNL Journey Optimizer] [Web Designer](web-visual-editor.md) per l&#39;authoring potente.

L’estensione non dispone di impostazioni condizionali e gestisce automaticamente tutte le impostazioni, incluse le impostazioni dei cookie SameSite.

>[!NOTE]
>
>Alcuni siti Web potrebbero non essere aperti in modo affidabile nella finestra di progettazione Web [!DNL Journey Optimizer] per uno dei motivi seguenti:
>
> * Il sito web ha dei criteri di sicurezza rigidi.
> * Il sito web si trova in un iframe.
> * Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (il sito è interno).

### Risoluzione dei problemi di mancato caricamento del sito Web {#troubleshooting}

Quando si utilizza il Web designer Adobe [!DNL Journey Optimizer], se si tenta di caricare un sito Web che non riesce, viene visualizzato un messaggio per suggerirti di installare l&#39;[estensione del browser Helper per editing video](#install-visual-editing-helper).

1. Assicurati che l’estensione del browser Helper per editing video sia installata correttamente.

1. Se il sito Web continua a funzionare in modo imprevisto, verificare che nel browser siano consentiti i cookie di terze parti. In caso contrario, la pagina Web non potrà essere caricata nel Web Designer [!DNL Journey Optimizer].

Per le pagine in autenticazione, se la pagina di accesso non viene caricata o se dopo aver tentato di accedere non hai ancora effettuato l’accesso:

1. Provare ad accedere in una nuova scheda del browser e passare alla pagina desiderata, quindi copiare l&#39;URL e provare ad aprirlo nel Web Designer [!DNL Journey Optimizer].

2. Se non riesci ancora a caricare il sito Web nella finestra di progettazione Web di [!DNL Journey Optimizer], contatta l&#39;Assistenza clienti Adobe per segnalare il problema, assicurandoti di specificare l&#39;URL errato.

## Prerequisiti per la consegna {#delivery-prerequisites}

Affinché l’esperienza web possa essere consegnata correttamente, è necessario definire le seguenti impostazioni:

* Nella [raccolta dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}, assicurati di avere uno stream di dati definito, ad esempio nel servizio **[!UICONTROL Adobe Experience Platform]** hai l&#39;opzione **[!UICONTROL Adobe Journey Optimizer]** abilitata.

  In questo modo gli eventi in entrata Journey Optimizer vengono gestiti correttamente da Adobe Experience Platform Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=it){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}, assicurati di avere abilitato un criterio di unione con l&#39;opzione **[!UICONTROL Criterio di unione attivo su Edge]**. A questo scopo, seleziona un criterio dal menu Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Profili]** > **[!UICONTROL Criteri di unione]**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it#configure){target="_blank"}

  Questo criterio di unione viene utilizzato da [!DNL Journey Optimizer] canali in entrata per attivare e pubblicare correttamente le campagne in entrata sul server Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* Per risolvere i problemi relativi alla distribuzione delle esperienze Web Journey Optimizer, puoi utilizzare la visualizzazione **Edge Delivery** in **Adobe Experience Platform Assurance**. Questo plug-in consente di esaminare in dettaglio le chiamate di richiesta, verificare se si verificano le chiamate edge previste come previsto ed esaminare i dati del profilo, tra cui le mappe di identità, le appartenenze ai segmenti e le impostazioni di consenso. Inoltre, puoi rivedere le attività per le quali la richiesta si è qualificata e identificare quelle per le quali non si è qualificata.

  L&#39;utilizzo del plug-in **Edge Delivery** consente di ottenere le informazioni necessarie per comprendere e risolvere in modo efficace le implementazioni in entrata.

  [Ulteriori informazioni sulla visualizzazione Edge Delivery](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery)

## Prerequisiti per la generazione di rapporti {#experiment-prerequisites}

Per abilitare il reporting per il canale web, è necessario assicurarsi che il [set di dati](../data/get-started-datasets.md) utilizzato nell&#39;implementazione Web [flusso di dati](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=it){target="_blank"} sia incluso anche nella configurazione del reporting.

In altre parole, durante la configurazione del reporting, se aggiungi un set di dati non presente nel flusso di dati web, i dati web non verranno visualizzati nei rapporti.

Scopri come aggiungere set di dati per il reporting in [questa sezione](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Il set di dati viene utilizzato in sola lettura dal sistema di reporting [!DNL Journey Optimizer] e non influisce sulla raccolta o sull&#39;acquisizione dei dati.

Se **non** utilizza i seguenti [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"} predefiniti per lo schema del set di dati: `AEP Web SDK ExperienceEvent` e `Consumer Experience Event` (come definito in [questa pagina](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html?lang=it#add-field-groups){target="_blank"}), assicurati di aggiungere i seguenti gruppi di campi: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` e `Web Details`. Questi sono necessari per il reporting di [!DNL Journey Optimizer] in quanto tengono traccia di quali campagne e percorsi partecipano ogni profilo.

[Ulteriori informazioni sulla configurazione del reporting](../reports/reporting-configuration.md)

>[!NOTE]
>
>L’aggiunta di questi gruppi di campi non influisce sulla normale raccolta di dati. Viene aggiunto solo per le pagine in cui è in esecuzione una campagna o un percorso, lasciando invariati tutti gli altri tracciamenti.

## Domini con marchio per le risorse {#branded-domains-for-assets}

Durante l&#39;authoring delle esperienze Web, se si aggiungono contenuti provenienti dalla libreria [Adobe Experience Manager Assets](../integrations/assets.md), è necessario impostare il sottodominio che verrà utilizzato per pubblicare tali contenuti. [Ulteriori informazioni](web-delegated-subdomains.md)
