---
title: Definire i predefiniti per le pagine di destinazione
description: Scopri come configurare l’ambiente per creare e utilizzare pagine di destinazione con Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: a485c58366f0690fb2515139658224d59468a24f
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 4%

---

# Definire i predefiniti per le pagine di destinazione {#lp-presets}

Quando [creazione di una pagina di destinazione](../landing-pages/create-lp.md#create-a-lp), devi selezionare un predefinito per la pagina di destinazione per creare la pagina di destinazione e sfruttarla **[!DNL Journey Optimizer]**.

## Accedere ai predefiniti della pagina di destinazione {#lp-presets}

Per accedere ai predefiniti della pagina di destinazione, effettua le seguenti operazioni.

1. Accedere al **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu.

1. Seleziona **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

   ![](assets/lp_presets-access.png)

1. Fai clic su un’etichetta preimpostata per accedere ai dettagli del predefinito della pagina di destinazione.

   ![](assets/lp_preset-details.png)

## Creare un predefinito per pagina di destinazione {#lp-create-preset}

Per creare un predefinito per una pagina di destinazione, segui i passaggi riportati di seguito.

>[!NOTE]
>
>Per creare un predefinito, accertati di aver configurato in precedenza almeno un sottodominio della pagina di destinazione. [Scopri come](lp-subdomains.md)

1. Accedere al **[!UICONTROL Administration]** > **[!UICONTROL Channels]** quindi seleziona **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

1. Seleziona **[!UICONTROL Create landing page preset]**.

   ![](assets/lp_create-preset-temp.png)

1. Immetti un nome e una descrizione per il predefinito.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, punto`.` e trattino `-` caratteri.

1. Seleziona un sottodominio della pagina di destinazione dall’elenco a discesa.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Per selezionare un sottodominio, accertati di aver configurato in precedenza almeno un sottodominio della pagina di destinazione. [Scopri come](#lp-subdomains)

   Vengono visualizzate le impostazioni corrispondenti al sottodominio selezionato.

1. Se desideri selezionare il sottodominio della pagina di destinazione come URL di tracciamento, controlla la **[!UICONTROL Same as landing page subdomain]** opzione . [Ulteriori informazioni sul tracciamento](../design/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Ad esempio, se l’URL della pagina di destinazione è &quot;pages.mail.luma.com&quot; e l’URL di tracciamento è &quot;data.mail.luma.com&quot;, puoi scegliere &quot;pages.mail.luma.com&quot; da utilizzare come sottodominio di tracciamento.

1. Fai clic su **[!UICONTROL Submit]** per confermare la creazione del predefinito della pagina di destinazione. Puoi anche salvare il predefinito come bozza e ripristinarne la configurazione in un secondo momento.

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. Una volta creato il predefinito della pagina di destinazione, questo viene visualizzato nell’elenco con **[!UICONTROL Active]** stato. È pronto per essere utilizzato per le pagine di destinazione.

   ![](assets/lp-preset-active-temp.png)

Ora è pronto per [creare pagine di destinazione](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].

>[!NOTE]
>
>Scopri come creare i predefiniti per i messaggi per le notifiche push e le e-mail in [questa sezione](message-presets.md).

**Argomenti correlati**:

* [Introduzione alle pagine di destinazione](../landing-pages/get-started-lp.md)
* [Creare una pagina di destinazione](../landing-pages/create-lp.md#create-a-lp)
