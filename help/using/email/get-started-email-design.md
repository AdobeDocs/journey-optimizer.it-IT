---
solution: Journey Optimizer
product: journey optimizer
title: Progettare le e-mail
description: Scopri come progettare le e-mail
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: e-mail, progettazione, stock, risorse
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
source-git-commit: 7176f5a1fa4c1b6c564fdb5d65f4e9208a1dce30
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 89%

---

# Introduzione alla progettazione delle e-mail {#get-started-content-design}

Puoi importare un contenuto esistente in [!DNL Journey Optimizer] oppure sfruttare le funzionalità di progettazione dei contenuti:

* Utilizza le **funzionalità di progettazione delle e-mail** di [!DNL Journey Optimizer] per creare o importare e-mail dinamiche. [Ulteriori informazioni](content-from-scratch.md)

* Sfrutta **Adobe Experience Manager Assets Essentials** per arricchire le e-mail e creare e gestire un tuo database di risorse. [Ulteriori informazioni](../integrations/assets.md)

* Trova **foto Adobe Stock** per creare i contenuti e migliorare la progettazione delle e-mail. [Ulteriori informazioni](../integrations/stock.md)

* Migliora l’esperienza dei clienti creando messaggi personalizzati e dinamici in base ai loro attributi di profilo. Ulteriori informazioni su [personalizzazione](../personalization/personalize.md) e [contenuti dinamici](../personalization/get-started-dynamic-content.md).

➡️ [Scopri questa funzione nel video](#video)

## Best practice per la progettazione e-mail {#best-practices}

Quando si inviano le e-mail, è importante tenere presente che i destinatari possono inoltrarle e, a volte, questo può causare problemi con il rendering dell’e-mail. Ciò è particolarmente vero quando si utilizzano classi CSS che potrebbero non essere supportate dal provider di posta elettronica utilizzato per l’inoltro, ad esempio, se si utilizza la classe CSS “is-desktop-hidden” per nascondere un’immagine su dispositivi mobili.

Per ridurre al minimo questi problemi di rendering, ti consigliamo di mantenere la struttura della progettazione e-mail il più semplice possibile. Prova a utilizzare una singola progettazione che funzioni bene sia per il desktop che per i dispositivi mobili ed evita di utilizzare classi CSS complesse o altri elementi di progettazione che potrebbero non essere completamente supportati da tutti i client e-mail. Seguendo queste best practice, puoi assicurarti che il rendering delle e-mail sia sempre corretto, indipendentemente da come vengono visualizzate o inoltrate dai destinatari.

Per le best practice per la progettazione di e-mail, fai riferimento alla tabella seguente:

| Consigliato | Da usare con cautela | Non consigliato |
|-|-|-|
| <ul><li><b>Layout statici basati su tabella</b> per la struttura</li> <li><b>Tabelle HTML e tabelle nidificate</b> per layout coerenti</li> <li><b>Larghezze del modello</b> tra 600 px e 800 px </li> <li><b>CSS semplice e in linea</b> per gli stili </li> <li><b>Font sicuri per il web</b> per compatibilità universale</li> | <ul><li>Le <b>immagini di sfondo</b> potrebbero non essere visualizzate in alcune piattaforme e-mail.</li><li>I <b>font web personalizzati</b> non sono universalmente supportati.</li><li>I <b>layout larghi</b> possono essere difficili da visualizzare sugli schermi più piccoli.</li><li>Le <b>mappe immagine</b> offrono funzionalità limitate.</li><li>Gli stili <b>CSS incorporati</b> vengono talvolta rimossi durante la consegna delle e-mail.</li> | <ul><li><b>JavaScript</b> non è solitamente supportato negli ambienti e-mail.</li> <li> I tag <b>`<iframe>`</b> vengono bloccati nella maggior parte delle piattaforme. </li> <li><b>Flash</b> è obsoleto e non è più supportato.</li> <li>L’<b>audio incorporato</b> spesso non viene riprodotto correttamente.</li> <li>I <b>video incorporati</b> non sono compatibili con molte piattaforme e-mail.</li> <li> I <b>moduli</b> non funzionano nelle e-mail.</li> <li> L’utilizzo di più livelli `<div>` può causare problemi di rendering.</li> |

>[!NOTE]
>
>Il [European Accessibility Act](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"} stabilisce che tutte le comunicazioni digitali devono essere accessibili. Oltre alle best practice per la progettazione delle e-mail elencate in questa sezione, assicurati di seguire anche le linee guida elencate in [questa pagina](accessible-content.md) specifiche per la creazione di contenuti accessibili con E-mail Designer.

## Passaggi chiave per la creazione di contenuti e-mail {#key-steps}

Una volta che [è stata aggiunta un’e-mail](create-email.md) a un percorso o a una campagna, puoi iniziare a creare il contenuto dell’e-mail.

1. Dalla schermata di configurazione del percorso o della campagna, passa alla schermata **[!UICONTROL Modifica contenuto]** per accedere a E-mail Designer. [Ulteriori informazioni](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. Nella pagina home di E-mail Designer, scegli come desideri progettare l’e-mail tra le seguenti opzioni:

   * **Progetta l’e-mail da zero** tramite l’interfaccia di E-mail designer e sfrutta le immagini da [Adobe Experience Manager Assets](../integrations/assets.md). Scopri come progettare il contenuto delle e-mail in [questa sezione](content-from-scratch.md).

   * **Codifica o incolla HTML non elaborato** direttamente in E-mail designer. Scopri come codificare il tuo contenuto in [questa sezione](code-content.md).

     >[!NOTE]
     >
     >In una campagna, puoi anche selezionare il pulsante **[!UICONTROL Editor di codice]** dalla schermata **[!UICONTROL Modifica contenuto]**. [Ulteriori informazioni](create-email.md#define-email-content)

   * **Importa contenuto HTML esistente** da un file o da una cartella .zip. Scopri come importare un contenuto e-mail in [questa sezione](existing-content.md).

   * **Convertire le progettazioni di immagini in modelli HTML** utilizzando l&#39;immagine basata sull&#39;intelligenza artificiale in un convertitore HTML. Scopri come trasformare le immagini statiche in modelli e-mail modificabili in [questa sezione](image-to-html.md).

   * **Seleziona un contenuto esistente** da un elenco di modelli incorporati o personalizzati. Scopri come utilizzare i modelli e-mail in [questa sezione](../email/use-email-templates.md).

   ![](assets/email_designer_create_options.png)

1. Una volta definito e personalizzato il contenuto dell’e-mail, puoi esportarlo per la convalida o per un utilizzo successivo. Fai clic su **[!UICONTROL Esporta HTML]** per salvare sul computer un file zip che includerà il tuo HTML e le tue risorse.

   ![](assets/email_designer_export.png)

## Video sulle procedure {#video}

Scopri come creare contenuti e-mail con l’editor dei messaggi.

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)

Scopri come configurare gli esperimenti sui contenuti per test A/B ed esplora al meglio i contenuti e-mail per raggiungere gli obiettivi aziendali.

>[!VIDEO](https://video.tv.adobe.com/v/3419893)
