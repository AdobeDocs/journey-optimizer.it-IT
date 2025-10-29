---
solution: Journey Optimizer
product: journey optimizer
title: Importa il contenuto delle e-mail
description: Scopri come importare il contenuto dell’e-mail
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: e-mail, importazione, contenuto, html, zip, css
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
source-git-commit: ddbab603e4ac612a49a3853fcac428950def1d98
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 66%

---

# Importa il contenuto delle e-mail {#existing-content}

[!DNL Journey Optimizer] consente di importare contenuto HTML esistente per progettare le e-mail. Tali contenuti possono essere:

* Un **file HTML** con un foglio di stile incorporato;
* Una cartella **.zip** che include un file HTML, il foglio di stile (.css) e le immagini.

  >[!NOTE]
  >
  >La struttura del file .zip non è soggetta a specifici vincoli. Tuttavia, i riferimenti devono essere relativi e adattarsi alla struttura ad albero della cartella .zip.

<!--DOCAC-13676
>[!TIP]
>
>If you have image designs (JPEG or PNG) instead of HTML files, you can use the [Template Accelerator](image-to-html.md) to automatically convert them into editable HTML email templates using AI.-->

Per importare un file con contenuto HTML, effettua le seguenti operazioni:

1. Dalla home page di E-mail Designer, seleziona **[!UICONTROL Importa HTML]**.

   ![](assets/import-html_2.png)

1. Trascina il file HTML o .zip con il contenuto HTML e fai clic su **[!UICONTROL Importa]**.

   ![](assets/html-imported_2.png)

1. Una volta caricato il contenuto HTML, questo sarà in **[!UICONTROL Modalità di compatibilità]**.

   In questa modalità, puoi solo personalizzare il testo, aggiungere collegamenti o includere risorse nel contenuto.

1. Per poter sfruttare i componenti di contenuto di E-mail designer, accedi alla scheda **[!UICONTROL Convertitore HTML]** e fai clic su **[!UICONTROL Converti]**.

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > L’utilizzo di un tag `<table>` come primo livello in un file HTML può causare la perdita di stile, incluse le impostazioni di sfondo e larghezza nel tag del livello superiore.

1. Ora puoi personalizzare il file importato in base alle esigenze con le funzionalità di E-mail Designer. [Ulteriori informazioni](content-from-scratch.md)

## Video introduttivo {#video}

Scopri come importare contenuti HTML esistenti, modificarne la progettazione, aggiungere una pagina mirror e collegamenti per annullare l’iscrizione, e come creare i contenuti tramite codice di programmazione.

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
