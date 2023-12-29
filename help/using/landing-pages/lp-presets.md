---
solution: Journey Optimizer
product: journey optimizer
title: Definire i predefiniti per la pagina di destinazione
description: Scopri come configurare l’ambiente per creare e utilizzare le pagine di destinazione con Journey Optimizer
feature: Landing Pages, Channel Configuration
role: Admin
level: Experienced
keywords: destinazione, pagina di destinazione, configurazione, ambiente, sottodominio, predefiniti
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 17%

---

# Definire i predefiniti per la pagina di destinazione {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="Creare un predefinito per la pagina di destinazione"
>abstract="Per creare una pagina di destinazione e utilizzarla tramite Journey Optimizer, devi creare un predefinito per pagina di destinazione che includa il sottodominio da utilizzare."

Quando [creazione di una pagina di destinazione](../landing-pages/create-lp.md#create-a-lp), è necessario selezionare un predefinito per pagina di destinazione per poterla creare e sfruttarlo tramite **[!DNL Journey Optimizer]**.

## Accedere ai predefiniti della pagina di destinazione {#access-lp-presets}

Per accedere ai predefiniti per pagine di destinazione, effettua le seguenti operazioni.

1. Accedere a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** menu.

1. Seleziona **[!UICONTROL Marchio]** > **[!UICONTROL Predefiniti per pagine di destinazione]**.

   ![](assets/lp_presets-access.png)

1. Fai clic su un’etichetta del predefinito per accedere ai dettagli del predefinito per pagina di destinazione.

   ![](assets/lp_preset-details.png)

## Creare un predefinito per la pagina di destinazione {#lp-create-preset}

Per creare un predefinito per pagina di destinazione, effettua le seguenti operazioni.

>[!NOTE]
>
>Per poter creare un predefinito, accertati di aver configurato in precedenza almeno un sottodominio della pagina di destinazione. [Scopri come](lp-subdomains.md)

1. Accedere a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** , quindi seleziona **[!UICONTROL Marchio]** > **[!UICONTROL Predefiniti per pagine di destinazione]**.

1. Seleziona **[!UICONTROL Crea predefinito per pagina di destinazione]**.

   ![](assets/lp_create-preset-temp.png)

1. Immettete un nome e una descrizione per il predefinito.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, punto`.` e trattino `-` caratteri.

1. Seleziona un sottodominio della pagina di destinazione dall’elenco a discesa.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Per poter selezionare un sottodominio, accertati di aver configurato in precedenza almeno un sottodominio della pagina di destinazione. [Scopri come](#lp-subdomains)

   Vengono visualizzate le impostazioni corrispondenti al sottodominio selezionato.

1. Se desideri selezionare il sottodominio della pagina di destinazione per l’URL di tracciamento, controlla **[!UICONTROL Come sottodominio della pagina di destinazione]** opzione. [Ulteriori informazioni sul tracciamento](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Ad esempio, se l’URL della pagina di destinazione è &quot;pages.mail.luma.com&quot; e l’URL di tracciamento è &quot;data.mail.luma.com&quot;, puoi scegliere &quot;pages.mail.luma.com&quot; da utilizzare come sottodominio di tracciamento.

1. Clic **[!UICONTROL Invia]** per confermare la creazione del predefinito per pagina di destinazione. <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. Una volta creato il predefinito per pagina di destinazione, questo viene visualizzato nell’elenco con **[!UICONTROL Attivo]** stato. È pronto per essere utilizzato nelle pagine di destinazione.

   ![](assets/lp-preset-active-temp.png)

Ora sei pronto per [creare pagine di destinazione](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**Argomenti correlati**:

* [Introduzione alle pagine di destinazione](../landing-pages/get-started-lp.md)
* [Creare una pagina di destinazione](../landing-pages/create-lp.md#create-a-lp)
