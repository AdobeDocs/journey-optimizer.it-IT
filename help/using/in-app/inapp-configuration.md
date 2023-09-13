---
title: Configurazione in-app
description: Scopri come configurare l’ambiente per inviare messaggi in-app con Journey Optimizer
role: Admin
level: Intermediate
keywords: in-app, messaggio, configurazione, piattaforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 6f92f9ce0a4785f0359658f00150d283f1326900
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 6%

---

# Configurare un canale in-app {#inapp-configuration}

Prima di inviare messaggi in-app, devi configurare il canale in-app in [!DNL Adobe Experience Platform Data Collection].

1. Dal tuo [!DNL Adobe Experience Platform Data Collection] account, accedere a **[!UICONTROL Datastream]** e fai clic su **[!UICONTROL Nuovo flusso di dati]**. Per ulteriori informazioni sulla creazione di flussi di dati, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html).

1. Seleziona la [!DNL Adobe Experience Platform] servizio.

   [!DNL Edge Segmentation] e [!DNL Adobe Journey Optimizer] deve essere selezionato.

   ![](assets/inapp_config_6.png)

   >[!NOTE]
   >
   >Per abilitare gli esperimenti di contenuto per il canale in-app, è necessario assicurarsi che il [set di dati](../data/get-started-datasets.md) utilizzato nell’app [flusso di dati](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=it){target="_blank"} è presente anche nella configurazione di reporting, altrimenti i dati in-app non verranno visualizzati nei rapporti dell’esperimento sui contenuti. [Scopri come aggiungere set di dati](../campaigns/reporting-configuration.md#add-datasets)
   >
   >Il set di dati viene utilizzato in sola lettura da [!DNL Journey Optimizer] e non influisce sulla raccolta o l’acquisizione dei dati.

1. Quindi, accedi a **[!UICONTROL Superfici app]** e fai clic su **[!UICONTROL Crea superficie app]**.

   >[!NOTE]
   >
   > Hai bisogno di **Gestire la configurazione dell’app** autorizzazione ad avere accesso al **[!UICONTROL Superfici app]** menu. Per ulteriori informazioni, consulta [questo video](#video).

   ![](assets/inapp_config_1.png)

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

**Argomenti correlati:**

* [Creare un messaggio in-app](create-in-app.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Progettare un messaggio in-app](design-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report.md#inapp-report)


## Video sulle procedure{#video}

* Il video seguente mostra come assegnare il **Gestire la configurazione dell’app** autorizzazione per accedere al menu Superfici app.

  +++Guarda il video

  >[!VIDEO](https://video.tv.adobe.com/v/3421607)

+++


