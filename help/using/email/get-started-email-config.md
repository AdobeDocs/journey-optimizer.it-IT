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
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: ht
source-wordcount: '211'
ht-degree: 100%

---

# Introduzione alla configurazione e-mail {#get-starte-email-config}

Per inviare e-mail tramite percorsi e campagne in [!DNL Journey Optimizer], devi seguire diversi passaggi di configurazione.

1. Per garantire un recapito messaggi ottimale e proteggere la reputazione, inizia delegando ad Adobe i sottodomini con cui invierai le e-mail con [!DNL Journey Optimizer]. Questi sottodomini determineranno elementi quali le pagine web da tracciare e gli URL della pagina mirror. [Ulteriori informazioni](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Migliora il recapito e la reputazione delle e-mail raggruppando gli indirizzi IP forniti con la tua istanza. [Ulteriori informazioni](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Crea configurazioni dei canali e seleziona il canale **[!UICONTROL e-mail]**. [Ulteriori informazioni](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. In ogni configurazione dei canali e-mail, configura tutti i parametri tecnici necessari per inviare e-mail. [Ulteriori informazioni](email-settings.md)

   * In questo punto è possibile selezionare il sottodominio da utilizzare per inviare le e-mail e i pool IP da associare alla configurazione. [Ulteriori informazioni](email-settings.md#subdomains-and-ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * Gli indirizzi **[!UICONTROL e-mail mittente]** e **[!UICONTROL e-mail di errore]** devono utilizzare il corrente sottodominio delegato selezionato. [Ulteriori informazioni](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Determina l’indirizzo e-mail da utilizzare in priorità per i destinatari quando sono disponibili più indirizzi in Adobe Experience Platform. [Ulteriori informazioni](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Gestisci il numero di giorni durante i quali vengono eseguiti nuovi tentativi prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
