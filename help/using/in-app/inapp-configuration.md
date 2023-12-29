---
title: Prerequisiti per il canale in-app
description: Scopri come configurare l’ambiente per inviare messaggi in-app con Journey Optimizer
role: Admin
feature: In App
level: Intermediate
keywords: in-app, messaggio, configurazione, piattaforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 6%

---

# Prerequisiti per il canale in-app {#inapp-configuration}

## Prerequisiti per la consegna {#delivery-prerequisites}

Affinché i messaggi in-app vengano recapitati correttamente, è necessario definire le seguenti impostazioni:

* In [Raccolta dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}, assicurati di avere un flusso di dati definito, ad esempio sotto **[!UICONTROL Adobe Experience Platform]** del servizio Adobe Experience Platform Edge e **[!UICONTROL Adobe Journey Optimizer]** opzione abilitata.

  In questo modo gli eventi in entrata Journey Optimizer vengono gestiti correttamente da Adobe Experience Platform Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/inapp_config_6.png)

* In entrata [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}, make sure you have the default merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Questo criterio di unione è utilizzato da [!DNL Journey Optimizer] canali in entrata per attivare e pubblicare correttamente le campagne in entrata sul server Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it){target="_blank"}

  ![](assets/inapp_config_8.png)

## Prerequisiti per la configurazione del canale {#channel-prerequisites}

1. Accedere a **[!UICONTROL Superfici app]** e fai clic su **[!UICONTROL Crea superficie app]**.

1. Aggiungi un nome al tuo **[!UICONTROL Superficie app]**.

   ![](assets/inapp_config_2b.png)

1. Dalla sezione **[!UICONTROL Apple iOS]** , configura la tua app mobile per Apple iOS.

+++ Ulteriori informazioni

   1. Digita il tuo **[!UICONTROL ID bundle iOS]**. Fai riferimento a [Documentazione di Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) per ulteriori informazioni su **ID bundle**.

   1. (facoltativo) Scegli la **[!UICONTROL Sandbox]** dove desideri inviare notifiche push. La scelta di una sandbox specifica richiede le autorizzazioni di accesso necessarie.

      Per ulteriori informazioni sulla gestione delle sandbox, consulta [questa pagina](../administration/sandboxes.md#assign-sandboxes).

   1. Abilita **[!UICONTROL Credenziali push]** per trascinare e rilasciare il file .p8 auth key, se necessario.

      È inoltre possibile abilitare **[!UICONTROL Immetti manualmente le credenziali push]** per copiare e incollare direttamente il tasto di autenticazione APNs.

   1. Immetti il **[!UICONTROL ID chiave]** e **[!UICONTROL ID team]**.

      ![](assets/inapp_config_2.png)

+++

1. Dalla sezione **[!UICONTROL Android]** , configura la tua app mobile per Android.

+++ Ulteriori informazioni

   1. Digita il tuo **[!UICONTROL Nome pacchetto Android]**. Fai riferimento a [Documentazione Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) per ulteriori informazioni su **Nome pacchetto**.

   1. (facoltativo) Scegli la **[!UICONTROL Sandbox]** dove desideri inviare notifiche push. La scelta di una sandbox specifica richiede le autorizzazioni di accesso necessarie.

      Per ulteriori informazioni sulla gestione delle sandbox, consulta [questa pagina](../administration/sandboxes.md#assign-sandboxes).

   1. Abilita **[!UICONTROL Credenziali push]** per trascinare e rilasciare il file della chiave privata .json, se necessario.

      È inoltre possibile abilitare **[!UICONTROL Immetti manualmente le credenziali push]** per copiare e incollare direttamente la chiave privata FCM.

      ![](assets/inapp_config_7.png)

1. Clic **[!UICONTROL Salva]** al termine della configurazione del **[!UICONTROL Superficie app]**.

   ![](assets/inapp_config_3.png)

   Il tuo **[!UICONTROL Superficie app]** sarà ora disponibile quando crei una nuova campagna con un messaggio in-app. [Ulteriori informazioni](create-in-app.md)

1. Dopo aver creato la superficie dell’app, ora devi creare una proprietà mobile.

   Fai riferimento a [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) procedura dettagliata.

   ![](assets/inapp_config_4.png)

1. Dal menu Estensioni della proprietà appena creata, installa le seguenti estensioni:

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP Assurance
   * Consenso
   * Identità
   * Core mobile
   * Profilo

   Fai riferimento a [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) procedura dettagliata.

   ![](assets/inapp_config_5.png)

Il canale in-app è ora configurato. Puoi iniziare a inviare messaggi in-app agli utenti.

## Prerequisiti per l’esperimento sui contenuti {#experiment-prerequisites}

Per abilitare gli esperimenti di contenuto per il canale in-app, è necessario assicurarsi che il [set di dati](../data/get-started-datasets.md) utilizzato nell’implementazione in-app [flusso di dati](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} è incluso anche nella configurazione di reporting.

In altre parole, quando configuri la generazione di rapporti sull’esperimento, se aggiungi un set di dati non presente nello stream di dati web, i dati web non vengono visualizzati nei rapporti sull’esperimento del contenuto.

Scopri come aggiungere set di dati per il reporting degli esperimenti sui contenuti in [questa sezione](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Il set di dati viene utilizzato in sola lettura da [!DNL Journey Optimizer] e non influisce sulla raccolta o l’acquisizione dei dati.

Se sei **non** utilizzando le seguenti opzioni predefinite [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), assicurati di aggiungere i seguenti gruppi di campi: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, e `Web Details`. Questi sono necessari per [!DNL Journey Optimizer] generazione di rapporti sugli esperimenti di contenuto mentre tengono traccia degli esperimenti e dei trattamenti a cui partecipa ciascun profilo.

>[!NOTE]
>
>L’aggiunta di questi gruppi di campi non influisce sulla normale raccolta di dati. Viene aggiunto solo per le pagine in cui è in esecuzione un esperimento, lasciando invariati tutti gli altri tracciamenti.

## Video sulle procedure{#video}

* Il video seguente mostra come assegnare il **Gestire la configurazione dell’app** autorizzazione per accedere al menu Superfici app.

  +++Guarda il video

  >[!VIDEO](https://video.tv.adobe.com/v/3421607)

+++

**Argomenti correlati:**

* [Creare un messaggio in-app](create-in-app.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Progettare un messaggio in-app](design-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report.md#inapp-report)

