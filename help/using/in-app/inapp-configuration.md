---
title: Prerequisiti e configurazione del canale in-app
description: Scopri come configurare l’ambiente per inviare messaggi in-app con Journey Optimizer
role: Admin
feature: In App
level: Intermediate
keywords: in-app, messaggio, configurazione, piattaforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 9%

---

# Prerequisiti e configurazione {#inapp-configuration}

## Passaggi di configurazione {#inapp-steps}

Per inviare messaggi in-app nei tuoi percorsi e nelle tue campagne con [!DNL Journey Optimizer], devi eseguire i seguenti passaggi di configurazione.

1. Assicurati di disporre delle autorizzazioni corrette per le campagne Journey Optimizer prima di iniziare, anche se prevedi di utilizzare i messaggi in-app solo nei percorsi. Sono ancora necessarie le autorizzazioni per la campagna. [Ulteriori informazioni](../campaigns/get-started-with-campaigns.md#campaign-prerequisites).
È necessario concedere un&#39;autorizzazione specifica per accedere al menu **Superfici app** nella raccolta dati di Adobe Experience Platform. Ulteriori informazioni in [questo video](#video).
1. Abilita Adobe Journey Optimizer nello stream di dati di raccolta dati Adobe Experience Platform e verifica il criterio di unione predefinito in Adobe Experience Platform, come descritto in [Prerequisiti per la consegna](#delivery-prerequisites) di seguito.
1. Crea e configura una superficie app nella raccolta dati di Adobe Experience Platform, come descritto in [questa sezione](#channel-prerequisites).
1. Se utilizzi esperimenti di contenuto, assicurati di seguire i requisiti elencati in [questa sezione](#experiment-prerequisite).

Al termine, puoi creare, configurare e inviare il tuo primo messaggio in-app. Scopri come farlo in [questa sezione](create-in-app.md).

## Prerequisiti per la consegna {#delivery-prerequisites}

Affinché i messaggi in-app vengano recapitati correttamente, è necessario definire le seguenti impostazioni:

* Nella [raccolta dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}, assicurati di avere uno stream di dati definito, ad esempio nel servizio **[!UICONTROL Adobe Experience Platform]** hai l&#39;opzione Adobe Experience Platform Edge e **[!UICONTROL Adobe Journey Optimizer]** abilitata.

  In questo modo gli eventi in entrata Journey Optimizer vengono gestiti correttamente da Adobe Experience Platform Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/inapp_config_6.png)

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}, assicurati di aver abilitato l&#39;opzione **[!UICONTROL Criterio di unione attivo su Edge]** per i criteri di unione predefiniti. A questo scopo, seleziona un criterio nel menu di Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Profili]** > **[!UICONTROL Criteri di unione]**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Questo criterio di unione viene utilizzato da [!DNL Journey Optimizer] canali in entrata per attivare e pubblicare correttamente le campagne in entrata sul server Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it){target="_blank"}

  >[!NOTE]
  >
  >Quando utilizzi un criterio di unione personalizzato **[!UICONTROL Preferenza set di dati]**, assicurati di aggiungere il set di dati **[!UICONTROL Percorso in entrata]** all&#39;interno del criterio di unione specificato.

  ![](assets/inapp_config_8.png)

* Per risolvere i problemi relativi alla distribuzione delle esperienze Journey Optimizer Mobile, puoi utilizzare la visualizzazione **Edge Delivery** in **Adobe Experience Platform Assurance**. Questo plug-in consente di esaminare in dettaglio le chiamate di richiesta, verificare se si verificano le chiamate edge previste come previsto ed esaminare i dati del profilo, tra cui le mappe di identità, le appartenenze ai segmenti e le impostazioni di consenso. Inoltre, puoi rivedere le attività per le quali la richiesta si è qualificata e identificare quelle per le quali non si è qualificata.

  L&#39;utilizzo del plug-in **Edge Delivery** consente di ottenere le informazioni necessarie per comprendere e risolvere in modo efficace le implementazioni in entrata.

  [Ulteriori informazioni sulla visualizzazione Edge Delivery](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery)

## Prerequisiti per la configurazione del canale {#channel-prerequisites}

1. Accedi al menu **[!UICONTROL Superfici app]** e fai clic su **[!UICONTROL Crea superficie app]**.

1. Aggiungi un nome alla **[!UICONTROL superficie app]**.

   ![](assets/inapp_config_2b.png)

1. Dal menu a discesa **[!UICONTROL Apple iOS]**, configura la tua app mobile per Apple iOS.

+++ Ulteriori informazioni

   1. Digita il tuo **[!UICONTROL ID bundle iOS]**. Per ulteriori informazioni su **ID bundle**, consulta la [documentazione di Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids).

   1. (facoltativo) Scegli la **[!UICONTROL Sandbox]** da cui desideri inviare le notifiche push. La scelta di una sandbox specifica richiede le autorizzazioni di accesso necessarie.

      Per ulteriori informazioni sulla gestione delle sandbox, consulta [questa pagina](../administration/sandboxes.md#assign-sandboxes).

   1. Abilita l&#39;opzione **[!UICONTROL Invia credenziali]** per trascinare e rilasciare il file della chiave di autenticazione .p8, se necessario.

      Puoi anche abilitare l&#39;opzione **[!UICONTROL Immetti manualmente le credenziali push]** per copiare e incollare direttamente la chiave di autenticazione APNs.

   1. Immetti **[!UICONTROL ID chiave]** e **[!UICONTROL ID team]**.

      ![](assets/inapp_config_2.png)

+++

1. Dal menu a discesa **[!UICONTROL Android]**, configura la tua app mobile per Android.

+++ Ulteriori informazioni

   1. Digita il nome del pacchetto **[!UICONTROL Android]**. Per ulteriori informazioni su **Nome pacchetto**, consulta la [documentazione di Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores).

   1. (facoltativo) Scegli la **[!UICONTROL Sandbox]** da cui desideri inviare le notifiche push. La scelta di una sandbox specifica richiede le autorizzazioni di accesso necessarie.

      Per ulteriori informazioni sulla gestione delle sandbox, consulta [questa pagina](../administration/sandboxes.md#assign-sandboxes).

   1. Abilita l&#39;opzione **[!UICONTROL Invia credenziali]** per trascinare e rilasciare il file della chiave privata .json, se necessario.

      Puoi anche abilitare l&#39;opzione **[!UICONTROL Immetti manualmente le credenziali push]** per copiare e incollare direttamente la chiave privata FCM.

      ![](assets/inapp_config_7.png)

1. Fai clic su **[!UICONTROL Salva]** al termine della configurazione della **[!UICONTROL superficie app]**.

   ![](assets/inapp_config_3.png)

   La **[!UICONTROL superficie app]** sarà ora disponibile quando crei una nuova campagna con un messaggio in-app. [Ulteriori informazioni](create-in-app.md)

1. Dopo aver creato la superficie dell’app, ora devi creare una proprietà mobile.

   Per la procedura dettagliata, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile).

   ![](assets/inapp_config_4.png)

1. Dal menu Estensioni della proprietà appena creata, installa le seguenti estensioni:

   * Edge Network Adobe Experience Platform
   * Adobe Journey Optimizer
   * AEP Assurance
   * Consenso
   * Identità
   * Core mobile
   * Profilo

   Per la procedura dettagliata, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension).

   ![](assets/inapp_config_5.png)

Il canale in-app è ora configurato. Puoi iniziare a inviare messaggi in-app agli utenti.

## Prerequisiti per l’esperimento sui contenuti {#experiment-prerequisites}

Per abilitare gli esperimenti di contenuto per il canale in-app, devi assicurarti che il [set di dati](../data/get-started-datasets.md) utilizzato nell&#39;implementazione in-app [flusso di dati](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} sia incluso anche nella configurazione di reporting.

In altre parole, quando configuri la generazione di rapporti sull’esperimento, se aggiungi un set di dati non presente nello stream di dati web, i dati web non vengono visualizzati nei rapporti sull’esperimento del contenuto.

Scopri come aggiungere set di dati per i rapporti sull’esperimento dei contenuti in [questa sezione](../content-management/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Il set di dati viene utilizzato in sola lettura dal sistema di reporting [!DNL Journey Optimizer] e non influisce sulla raccolta o sull&#39;acquisizione dei dati.

Se **non** utilizza i seguenti [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"} predefiniti per lo schema del set di dati: `AEP Web SDK ExperienceEvent` e `Consumer Experience Event` (come definiti in [questa pagina](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), assicurati di aggiungere i seguenti gruppi di campi: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` e `Web Details`. Questi sono necessari per il reporting dell&#39;esperimento di contenuto [!DNL Journey Optimizer], in quanto tengono traccia degli esperimenti e dei trattamenti a cui partecipa ogni profilo.

>[!NOTE]
>
>L’aggiunta di questi gruppi di campi non influisce sulla normale raccolta di dati. Viene aggiunto solo per le pagine in cui è in esecuzione un esperimento, lasciando invariati tutti gli altri tracciamenti.

## Video introduttivo{#video}

Il video seguente mostra come assegnare l&#39;autorizzazione **Gestione configurazione app** per accedere al menu Superfici app.

>[!VIDEO](https://video.tv.adobe.com/v/3421607)


**Argomenti correlati:**

* [Creare un messaggio in-app](create-in-app.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Progettare un messaggio in-app](design-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report.md#inapp-report)

