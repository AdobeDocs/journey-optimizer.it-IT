---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva alla configurazione delle e-mail
description: Ulteriori informazioni sulla configurazione delle e-mail in [!DNL Journey Optimizer]
role: Admin
level: Intermediate
feature: Application Settings
topic: Administration
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Guida introduttiva alla configurazione delle e-mail {#get-starte-email-config}

Per poter inviare e-mail attraverso percorsi e campagne in [!DNL Journey Optimizer], devi seguire diversi passaggi di configurazione.

1. Per garantire un recapito messaggi ottimale e proteggere la tua reputazione, inizia delegando ad Adobe i sottodomini con cui invierai le e-mail [!DNL Journey Optimizer]. Questi sottodomini determineranno elementi quali le pagine web da tracciare e gli URL della pagina speculare. [Ulteriori informazioni](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Migliora il recapito e la reputazione delle e-mail raggruppando gli indirizzi IP forniti con la tua istanza. [Ulteriori informazioni](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Crea superfici del canale e seleziona la **[!UICONTROL Email]** canale. [Ulteriori informazioni](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. In ogni superficie del canale e-mail, configura tutti i parametri tecnici necessari per inviare e-mail. [Ulteriori informazioni](email-settings.md)

   * In questo punto è possibile selezionare il sottodominio da utilizzare per inviare le e-mail e i pool IP da associare alla superficie. [Ulteriori informazioni](email-settings.md#subdomains-and-ip-pools)

   ![](assets/preset-subdomain-ip-pool.png)

   * La **[!UICONTROL Sender email]** e **[!UICONTROL Error email]** Gli indirizzi devono utilizzare il sottodominio delegato selezionato. [Ulteriori informazioni](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Determina l’indirizzo e-mail da utilizzare in priorità per i destinatari quando diversi indirizzi sono disponibili in Adobe Experience Platform. [Ulteriori informazioni](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Gestisci il numero di giorni durante i quali vengono eseguiti nuovi tentativi prima di inviare indirizzi e-mail all’elenco di eliminazione. [Ulteriori informazioni](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
