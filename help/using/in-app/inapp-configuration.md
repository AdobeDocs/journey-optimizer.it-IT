---
title: Configurazione in-app
description: Scopri come configurare l’ambiente per l’invio di messaggi in-app con Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 9%

---

# Configurare un canale in-app {#inapp-configuration}

Prima di inviare messaggi in-app, devi configurare il canale in-app in [!DNL Adobe Experience Platform Data Collection].

1. Dal tuo [!DNL Adobe Experience Platform Data Collection] account, accedere al **[!UICONTROL Datastream]** menu e fai clic su **[!UICONTROL Nuovo datastream]**. Per ulteriori informazioni sulla creazione del datastream, consulta [questa pagina](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. Seleziona la [!DNL Adobe Experience Platform] servizio.

   [!DNL Edge Segmentation], [!DNL Offer Decisioning] e [!DNL Adobe Journey Optimizer] deve essere selezionato.

   ![](assets/inapp_config_6.png)

1. Quindi, accedi al **[!UICONTROL Superfici dell&#39;app]** menu, quindi fai clic su **[!UICONTROL Creare una superficie dell’app]**.

   ![](assets/inapp_config_1.png)

1. Aggiungi un nome al tuo **[!UICONTROL Superficie dell&#39;app]**.

1. Dall’elenco a discesa Apple iOS , digita il **iOS Bundle ID**. Fai riferimento a [Documentazione di Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) per ulteriori informazioni su **ID bundle**.

   ![](assets/inapp_config_2.png)

1. Dal menu a discesa Android, digita il tuo **Nome del pacchetto Android**. Fai riferimento a [Documentazione Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) per ulteriori informazioni su **Nome pacchetto**.

1. Fai clic su **[!UICONTROL Salva]** al termine della configurazione del **[!UICONTROL Superficie dell&#39;app]**.

   ![](assets/inapp_config_3.png)

   Le **[!UICONTROL Superficie dell&#39;app]** Sarà ora disponibile quando crei una nuova campagna con un messaggio in-app. [Ulteriori informazioni](create-in-app.md)

1. Dopo aver creato la superficie dell’app, devi ora creare una proprietà mobile.

   Fai riferimento a [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) per la procedura dettagliata.

   ![](assets/inapp_config_4.png)

1. Dal menu Estensioni della proprietà appena creata, installa le seguenti estensioni:

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * Garanzia AEP
   * Consenso
   * Identifica
   * Core mobile
   * Profilo

   Fai riferimento a [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) per la procedura dettagliata.

   ![](assets/inapp_config_5.png)

Il canale in-app è ora configurato. Puoi iniziare a inviare messaggi in-app ai tuoi utenti.

**Argomenti correlati:**

* [Creare un messaggio in-app](create-in-app.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Progettare un messaggio in-app](design-in-app.md)
* [Rapporto in-app](inapp-report.md)
