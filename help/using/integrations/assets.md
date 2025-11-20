---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare Assets in Journey Optimizer
description: Introduzione a Experience Manager Assets
feature: Assets, Integrations
topic: Content Management, Integrations
role: User
level: Beginner
keywords: assets, experience manager, integrazione
exl-id: d4fde14b-e2da-40bf-a387-ee9f2f7ff204
source-git-commit: 5ac4220250b69289ec0f722ca54fef3b63174643
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 18%

---

# Crea e gestisci le risorse con [!DNL Experience Manager Assets]{#experience-manager-assets}

## Introduzione a [!DNL Experience Manager Assets] {#get-started-assets}

Riunisci flussi di lavoro creativi e di marketing utilizzando **[!DNL Adobe Experience Manager Assets]**. Integrazione nativa con **[!DNL Adobe Journey Optimizer]**, accesso a **[!DNL Assets Essentials]** o **[!DNL Assets as a Cloud Service]** per archiviare, gestire, individuare e distribuire risorse digitali. Fornisce un archivio di risorse unico e centralizzato da utilizzare per compilare i messaggi.

**[!DNL Adobe Experience Manager Assets]** offre due aree di lavoro per risorse collaborative e centralizzate che estendono il sistema creativo e unificano le risorse digitali per la distribuzione delle esperienze:

* **[!DNL Assets as a Cloud Service]**: Adobe Experience Manager Assets as a Cloud Service offre una soluzione cloud di facile utilizzo per la gestione efficiente delle risorse digitali e le operazioni Dynamic Media. Incorpora perfettamente funzioni avanzate, tra cui l’intelligenza artificiale e l’apprendimento automatico.

  Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/overview.html){target="_blank"}.

* **[!DNL Assets Essentials]**: Experience Manager Assets Essentials è la soluzione leggera di Assets as a Cloud Service per la gestione unificata delle risorse e la collaborazione. Grazie a un’interfaccia moderna e semplificata, i team creativi e di marketing possono archiviare, individuare e distribuire risorse digitali in modo semplice.

  Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

A seconda del contratto, è possibile accedere a **[!DNL Adobe Experience Manager Assets Essentials]** o **[!DNL Adobe Experience Manager Assets as a Cloud Service]** direttamente da **[!DNL Adobe Journey Optimizer]** tramite la sezione **[!UICONTROL Assets]** del menu a sinistra. È inoltre possibile accedere a risorse e cartelle durante la [progettazione di un contenuto di posta elettronica](../email/get-started-email-design.md).

## Prerequisiti{#assets-prerequisites}

>[!BEGINTABS]

>[!TAB Adobe Experience Manager Assets Essentials]

Prima di utilizzare [!DNL Adobe Experience Manager Assets Essentials], devi aggiungere gli utenti ai **Utenti consumer di Assets Essentials** o/e **Utenti di Assets Essentials** profili di prodotto. Ulteriori informazioni sono disponibili nella [documentazione di Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html#add-user-groups){target="_blank"}.

>[!NOTE]
>Per i prodotti di Journey Optimizer ottenuti prima del 6 gennaio 2022, devi implementare **[!DNL Adobe Experience Manager Assets Essentials]** per la tua organizzazione. Per ulteriori informazioni, consulta la sezione [Distribuire Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=it){target="_blank"}.

>[!TAB Adobe Experience Manager Assets as a Cloud Service]

Prima di utilizzare **[!DNL Adobe Experience Manager Assets as a Cloud Service]**, è necessario aggiungere utenti ad Assets Cloud Services. Ulteriori informazioni in [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/security/ims-support.html).

>[!ENDTABS]

## Caricare e inserire le risorse{#add-asset}

Per importare i file in **[!DNL Assets Essentials]** o **[!DNL Assets as a Cloud Service]**, è innanzitutto necessario sfogliare o creare la cartella in cui verranno archiviati. Potrai quindi inserirli nel contenuto dell’e-mail.

1. Dalla home page di [!DNL Adobe Journey Optimizer], selezionare la scheda **[!UICONTROL Assets]** nel menu **[!UICONTROL Gestione contenuto]** per accedere a **[!DNL Assets Essentials]** o **[!DNL Assets as a Cloud Service]**.

   ![](assets/media_library_1.png)

1. Scegli l’archivio per il tuo Assets in Journey Optimizer. È possibile optare per un repository **[!DNL Assets Essentials]** o **[!DNL Assets as a Cloud Service]**, a condizione che si sia proprietari di questa soluzione.

   ![](assets/media_library_4.png)

   +++ Scopri come cambiare archivio Assets.

   Per modificare il repository di Assets, selezionare l&#39;icona Account in alto a destra e fare clic su **[!UICONTROL Seleziona repository]**.

   ![](assets/media_library_3.png)

   +++

1. Fare doppio clic su una cartella dalla sezione centrale o dalla vista ad albero per aprirla.

   Puoi anche fare clic su **[!UICONTROL Crea cartella]** per crearne una nuova.

   ![](assets/media_library_8.png)

1. Una volta nella cartella selezionata o creata, fai clic su **[!UICONTROL Aggiungi risorse]** per caricare una nuova risorsa nella cartella.

   ![](assets/media_library_2.png)

1. Da **[!UICONTROL Carica file]**, fai clic su **[!UICONTROL Sfoglia]** e scegli **[!UICONTROL Sfoglia file]** o **[!UICONTROL Sfoglia cartelle]** a seconda delle esigenze.

1. Seleziona il file da caricare. Al termine, fai clic su **[!UICONTROL Carica]**. Per ulteriori informazioni su come gestire le risorse, consulta questa [pagina](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/manage-organize.html).

1. Per modificare ulteriormente le risorse con Adobe Photoshop Express, fai doppio clic sulle risorse. Quindi, dal menu a destra, seleziona l’icona corrispondente alla **[!UICONTROL Modalità di modifica]**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/edit-images.html){target="_blank"}.

   ![](assets/media_library_12.png)

1. Da [!DNL Adobe Journey Optimizer], seleziona il menu **[!UICONTROL Selettore risorse]** dal riquadro a sinistra di E-mail Designer.

   ![](assets/media_library_5.png)

1. Seleziona la cartella **[!UICONTROL Risorse]** creata in precedenza. Puoi anche cercare la risorsa o la cartella nella barra di ricerca.

1. Trascina la risorsa nel contenuto dell’e-mail.

   ![](assets/media_library_6.png)

1. Puoi personalizzare ulteriormente le risorse, ad esempio aggiungendo un collegamento esterno o un testo, utilizzando le schede **[!UICONTROL Impostazioni]** e **[!UICONTROL Stili]**. [Ulteriori informazioni sulle impostazioni dei componenti](../email/content-components.md)

   ![](assets/media_library_13.png)

   <!--
    After adding your asset to your email, use the **[!UICONTROL Find similar Stock photos]** option to locate Stock photos that match the content, color, and composition of your image. [Learn more about Adobe Stock](stock.md).

    Note that this option is available for licensed/unlicensed Stock images and images from your Assets folder. 

    ![](assets/media_library_14.png)
    -->


## Domande frequenti {#faq-assets}

Di seguito sono riportate le domande frequenti su Adobe Experience Manager Assets.

Hai bisogno di ulteriori dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

+++ Posso continuare a utilizzare l’archivio in bundle Assets Essentials in Journey Optimizer?

Se si esegue il provisioning in **[!DNL Adobe Experience Manager Assets as a Cloud Service]**, si dispone dell&#39;accesso sia all&#39;archivio **[!DNL Adobe Experience Manager Assets Essentials]** che all&#39;archivio **[!DNL Adobe Experience Manager Assets as a Cloud Service]** se l&#39;utente dispone delle autorizzazioni appropriate. Questi archivi sono separati e non sincronizzati. Un utente in Journey Optimizer sarà in grado di visualizzare entrambi gli archivi, inclusi altri ambienti a cui ha diritto come Stage, Dev, ecc., e dovrebbe essere in grado di passare facilmente da un archivio all’altro con il selettore dell’archivio.

+++

+++ Gestione delle risorse Le modifiche in Assets as a Cloud Service si riflettono in Journey Optimizer?

**[!DNL Adobe Experience Manager Assets as a Cloud Service]** si integra con Journey Optimizer in modo simile a **[!DNL Adobe Experience Manager Assets Essentials]**. Quando vengono apportate modifiche alle risorse, viene generata una copia binaria. Si noti che gli aggiornamenti in **[!DNL Assets as a Cloud Service]** non si propagano automaticamente alle campagne e-mail live. Eventuali modifiche devono essere riselezionate manualmente in E-mail Designer per garantire la sincronizzazione tra le risorse e le campagne e-mail in corso.

+++

+++ È possibile utilizzare gli URL di Dynamic Media durante la creazione di e-mail in Journey Optimizer?

Sì, puoi utilizzare gli URL di Dynamic Media nell’authoring delle e-mail di Journey Optimizer. È sufficiente incollare gli URL invece di selezionare dal selettore delle risorse.

+++

+++ L’utente di Journey Optimizer può apportare modifiche all’archivio Adobe Experience Manager Assets as a Cloud Service dall’interfaccia di Journey Optimizer?

Se l&#39;utente di Journey Optimizer è un utente standard con diritto **[!DNL Adobe Experience Manager Assets as a Cloud Service]** e dispone dell&#39;autorizzazione di modifica per l&#39;archivio, può apportare modifiche all&#39;archivio **[!DNL Adobe Experience Manager Assets as a Cloud Service]**.

+++

+++ Perché talvolta le immagini non vengono caricate nelle e-mail inviate da Journey Optimizer?

Se le risorse (come le immagini) vengono gestite tramite Adobe Experience Manager e utilizzate in Journey Optimizer, sono soggette a criteri del ciclo di vita delle risorse con un valore TTL (Time-To-Live). Una volta scaduto il periodo TTL, le risorse potrebbero essere rimosse dall’archiviazione (CDN) e ciò potrebbe causare il danneggiamento delle immagini nelle e-mail che fanno riferimento a tali risorse.

>[!NOTE]
>
>Il TTL della risorsa è gestito dai servizi back-end di Adobe Journey Optimizer e non è attualmente configurabile dai clienti. Il periodo TTL corrente è impostato su 730 giorni per tutte le organizzazioni Journey Optimizer.

+++

+++ Come posso risolvere le immagini danneggiate a causa della scadenza delle risorse?

Per ripristinare la disponibilità dell&#39;immagine quando le risorse sono scadute:

1. **Ripubblica le risorse interessate**: accedi alla risorsa in Adobe Experience Manager e ripubblicala. In questo modo la risorsa sarà nuovamente disponibile nella rete CDN.

2. **Aggiorna riferimenti contenuto**: se si utilizzano frammenti di contenuto o modelli che fanno riferimento a risorse scadute:
   * Creare una bozza o un clone del frammento di contenuto
   * Aggiungi nuovamente o riseleziona la risorsa
   * Pubblicare il contenuto aggiornato

3. **Gestione proattiva**: per evitare interruzioni future, è consigliabile rivedere e ripubblicare periodicamente le risorse utilizzate nelle campagne e-mail attive, in particolare quelle prossime al periodo di scadenza TTL.

>[!CAUTION]
>
>I requisiti di ripubblicazione si applicano a tutti gli ambienti (produzione, stage, sviluppo). Assicurati che le risorse rimangano disponibili gestendone adeguatamente il ciclo di vita.

+++

+++ La logica di scadenza della risorsa verrà migliorata in futuro?

Sì, Adobe sta lavorando attivamente ai miglioramenti per perfezionare la logica di scadenza delle risorse e di gestione del ciclo di vita. Questi miglioramenti mirano a fornire una migliore visibilità sullo stato del ciclo di vita delle risorse e a ridurre il rischio di immagini danneggiate nelle campagne live.

Per gli ultimi aggiornamenti, consulta il team del tuo account Adobe o monitora le note sulla versione di Adobe Journey Optimizer.

+++
