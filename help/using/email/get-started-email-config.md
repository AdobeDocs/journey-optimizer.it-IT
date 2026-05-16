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
TQID: https://experienceleague.adobe.com/mVdk2WGb0rL06j1cmNEh4fj0JC-hwuro8ku-0Yv02N8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: cf64c7f6-7428-4ae5-b158-8df9771f38f4id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 229
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
