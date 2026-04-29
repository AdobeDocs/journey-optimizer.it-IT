---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla configurazione e-mail
description: Ulteriori informazioni sulla configurazione e-mail in  [!DNL Journey Optimizer]
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: e-mail, configurazione, superficie, sottodomini
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: 9274277872e34f47e05be1acfe248a3b3303cb13
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 84%

---

# Introduzione alla configurazione e-mail {#get-starte-email-config}

Per inviare e-mail tramite percorsi e campagne in [!DNL Journey Optimizer], devi seguire diversi passaggi di configurazione.

1. Per garantire la recapitabilità ottimale e proteggere la reputazione, inizia **delegando a Adobe i sottodomini** con cui invierai le e-mail con [!DNL Journey Optimizer]. Questi sottodomini determineranno elementi quali le pagine web da tracciare e gli URL della pagina mirror. [Ulteriori informazioni](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Crea pool IP per **raggruppare gli indirizzi IP** per i quali è stato eseguito il provisioning con la tua istanza. [Ulteriori informazioni](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Crea **configurazioni dei canali** e seleziona il canale **[!UICONTROL e-mail]**. [Ulteriori informazioni](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. In ogni configurazione dei canali e-mail, configura tutti i **parametri tecnici** necessari per inviare e-mail. [Ulteriori informazioni](email-settings.md)

   * In questo punto è possibile selezionare il sottodominio da utilizzare per inviare le e-mail e i pool IP da associare alla configurazione. [Ulteriori informazioni](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * Il **[!UICONTROL Prefisso e-mail Da]** e il **[!UICONTROL Prefisso e-mail di errore]** utilizzano il [sottodominio delegato](../configuration/about-subdomain-delegation.md) attualmente selezionato. Facoltativamente, **[!UICONTROL Nome mittente]** e **[!UICONTROL Indirizzo e-mail mittente]** possono identificare un&#39;altra parte trasmittente (indirizzo completo **Mittente**, non associato al suffisso del sottodominio). [Ulteriori informazioni](header-parameters.md#sender-header)

   ![](assets/preset-header.png)

1. Determina quali **campi di esecuzione** utilizzare in priorità per i destinatari quando sono disponibili più indirizzi in Adobe Experience Platform. [Ulteriori informazioni](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Gestisci il numero di giorni durante i quali vengono eseguiti **nuovi tentativi** prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
