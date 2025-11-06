---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare GenStudio for Performance Marketing in Journey Optimizer
description: Scopri come utilizzare GenStudio for Performance Marketing in Journey Optimizer
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
badge: label="Disponibilità limitata" type="Informative"
role: User
level: Beginner, Intermediate
exl-id: c22a44a8-e4e2-453a-9ca2-b80f7c0edc19
source-git-commit: 11c6dd43d6b20864f9823130c5aed790a3091938
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 16%

---

# Utilizzare GenStudio for Performance Marketing {#ajo-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="Utilizzare un modello creato con GenStudio"
>abstract="Grazie all’integrazione diretta con Adobe GenStudio for Performance Marketing, puoi importare facilmente un modello GenStudio ottimizzato con la tecnologia dell’intelligenza artificiale di Adobe."

## Introduzione a GenStudio {#gs-genstudio}

[Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"} è un&#39;applicazione IA-first generativa che consente ai team di marketing di creare annunci ed e-mail personalizzati per promuovere campagne di marketing personalizzate e di forte impatto, conformi agli standard del brand e conformi ai criteri aziendali. Sfruttando la tecnologia di intelligenza artificiale Adobe, fornisce una suite completa di strumenti che semplificano le complessità della creazione e della gestione dei contenuti in modo che i creativi possano concentrarsi sull’innovazione.

>[!AVAILABILITY]
>
>* L’integrazione di GenStudio in [!DNL Adobe Journey Optimizer] attualmente non può essere utilizzata con le offerte che includono il componente aggiuntivo **Healthcare Shield** o **Privacy and Security Shield**.
>
>* Questa funzionalità è disponibile solo per il canale e-mail.

Per migliorare l&#39;efficienza del marketing e mantenere la coerenza del brand, puoi integrare perfettamente [!DNL **esperienze GenStudio for Performance Marketing**] con [!DNL **Adobe Journey Optimizer**]. Questo consente di sfruttare la creazione di contenuti basata sull&#39;intelligenza artificiale di [!DNL GenStudio] insieme alle funzionalità di orchestrazione avanzate di [!DNL Journey Optimizer].

![Importare un contenuto GenStudio in Adobe Journey Optimizer](../rn/assets/do-not-localize/genstudio.gif)

>[!INFO]
>
>Per andare oltre, vedi questa [panoramica](https://business.adobe.com/it/products/genstudio-for-performance-marketing.html#watch-overview){target="_blank"} e una [demo](https://business.adobe.com/it/products/genstudio-for-performance-marketing.html#demo){target="_blank"} di [!DNL Adobe GenStudio for Performance Marketing].

➡️ [Scopri questa funzione nel video](#video)


<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->



<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](gs-generative.md#generative-guardrails) for AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## Utilizzare le funzionalità di GenStudio in Journey Optimizer {#use-genstudio}

L&#39;integrazione di [!DNL GenStudio for Performance Marketing] e [!DNL Journey Optimizer] consente agli addetti al marketing della tua azienda di collaborare meglio per semplificare i processi.

Ad esempio, un esperto di marketing tecnico, che utilizza [!DNL Journey Optimizer] per sviluppare e automatizzare campagne e-mail, può collaborare con un esperto di marketing delle prestazioni che crea contenuti utilizzando [!DNL GenStudio].

Con questa integrazione, entrambi possono collaborare per integrare facilmente i contenuti del brand da [!DNL GenStudio] a [!DNL Journey Optimizer], distribuendo e-mail coinvolgenti che mirano a segmenti di clienti specifici e stimolano le vendite.

### Esportare un modello di HTML da Journey Optimizer a GenStudio {#export-from-ajo-to-genstudio}

È innanzitutto possibile esportare un modello di HTML [!DNL Journey Optimizer] contenente le linee guida del brand in [!DNL GenStudio for Performance Marketing]. Segui i passaggi seguenti.

1. In [!DNL Journey Optimizer], accedi al contenuto dell&#39;e-mail in un percorso o in una campagna. [Scopri come](../email/get-started-email-design.md#key-steps)

1. In E-mail Designer, seleziona **[!UICONTROL Esporta HTML]** dal pulsante **[!UICONTROL Altro]**.

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. Carica questo modello esportato da HTML in [!DNL GenStudio for Performance Marketing]. <!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >Scopri come caricare un modello di HTML in [!DNL GenStudio] nella sezione dedicata della [Guida utente di Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo){target="_blank"}.

1. In GenStudio, utilizza questo modello per creare diverse varianti di e-mail con prompt di IA e salvarle.

   >[!NOTE]
   >
   >Scopri come creare esperienze e-mail nella [sezione](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience){target="_blank"} dedicata a GenStudio.

### Sfruttare le esperienze GenStudio in Journey Optimizer {#leverage-genstudio-experiences}

Per sfruttare le varianti di e-mail [!DNL GenStudio] create importandole in [!DNL Journey Optimizer], attieniti alla procedura seguente.

1. In [!DNL Journey Optimizer], [aggiungi un&#39;e-mail](../email/create-email.md) a una campagna.

1. Dalla schermata di configurazione della campagna, passa alla [schermata Modifica contenuto](../email/create-email.md#define-email-content) e fai clic su **[!UICONTROL Modifica corpo dell&#39;e-mail]** per aprire E-mail Designer. [Scopri come](../email/get-started-email-design.md#key-steps)

1. Nella home page di E-mail Designer, seleziona **[!UICONTROL Importa HTML]** e fai clic sul pulsante **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![](assets/genstudio-pem-import-email.png){zoomable="yes"}

1. Sfoglia le esperienze GenStudio per iniziare a creare i contenuti. Puoi filtrare le esperienze in base a diversi criteri, ad esempio prodotti, utenti tipo, marchi o persino colori.

   <!--![](assets/genstudio-filter-experiences.png){zoomable="yes"}-->

1. Seleziona un&#39;esperienza e fai clic su **[!UICONTROL Usa]**.

   ![](assets/genstudio-use-experience.png){zoomable="yes"}

1. Seleziona la cartella in cui desideri importare l’esperienza GenStudio.

   ![](assets/genstudio-choose-destination.png){zoomable="yes"}

1. Il contenuto selezionato viene visualizzato in E-mail Designer.

   ![](assets/genstudio-email-content.png){zoomable="yes"}

   >[!NOTE]
   >
   >Le esperienze GenStudio [create da un [!DNL Journey Optimizer] modello](#export-from-ajo-to-genstudio) vengono importate direttamente nel Designer di posta elettronica. Le esperienze GenStudio create senza un modello [!DNL Journey Optimizer] vengono importate in [modalità di compatibilità](../email/existing-content.md).

   Utilizza gli [strumenti di modifica del contenuto e-mail](../email/content-from-scratch.md) e i [campi di personalizzazione](../personalization/personalize.md) per modificare l&#39;e-mail come desiderato. Salva il contenuto.

1. Torna alla pagina di riepilogo della campagna e fai clic su **[!UICONTROL Crea esperimento]** per utilizzare la sperimentazione. [Scopri come creare un esperimento sui contenuti](../content-management/content-experiment.md)

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. Crea diversi trattamenti e ripeti i passaggi precedenti per importare e sfruttare rapidamente le altre varianti di esperienza e-mail create in [!DNL GenStudio].

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. Salva le modifiche e [attiva](../campaigns/review-activate-campaign.md) la campagna.

Dopo aver eseguito l&#39;esperimento, tieni traccia delle prestazioni dei trattamenti della campagna con il [rapporto sulla campagna di sperimentazione](../reports/campaign-global-report-cja-experimentation.md). Puoi quindi interpretare i risultati dell’esperimento. [Scopri come](../content-management/get-started-experiment.md#interpret-results)

## Video dimostrativo {#video}

Scopri come esportare un modello e-mail da Journey Optimizer a GenStudio for Performance Marketing, creare e-mail conformi al brand utilizzando il modello in GenStudio e importarle nuovamente in Journey Optimizer con facilità.

>[!VIDEO](https://video.tv.adobe.com/v/3456057/?captions=ita&quality=12)