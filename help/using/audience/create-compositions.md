---
solution: Journey Optimizer
product: journey optimizer
title: Creare il primo flusso di lavoro per la composizione
description: Scopri come creare flussi di lavoro di composizione per combinare e disporre i tipi di pubblico esistenti.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 01c14590fe55d8f11c1ff2b18141933b0b3dd5ca
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 15%

---

# Creare il primo flusso di lavoro per la composizione {#create-compositions}

>[!BEGINSHADEBOX]

Questa documentazione fornisce informazioni dettagliate su come lavorare con la composizione del pubblico in Adobe Journey Optimizer. Se non utilizzi Adobe Journey Optimizer, [fai clic qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=it){target="_blank"}.

>[!ENDSHADEBOX]

## Creare un flusso di lavoro di composizione {#create}

Per creare un flusso di lavoro di composizione, effettuate le seguenti operazioni:

1. Accedi al menu **[!UICONTROL Tipi di pubblico]** e seleziona **[!UICONTROL Crea pubblico]**.

1. Seleziona **[!UICONTROL Componi pubblico]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >Il metodo di creazione della **[!UICONTROL regola di compilazione]** ti consente di creare una nuova definizione di segmento utilizzando il [servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it).

1. L’area di lavoro della composizione viene visualizzata con due attività predefinite:

   * **[!UICONTROL Pubblico]**: il punto iniziale della composizione. Questa attività ti consente di selezionare uno o più tipi di pubblico come base per il flusso di lavoro,

   * **[!UICONTROL Salva]**: ultimo passaggio della composizione. Questa attività ti consente di salvare il risultato del flusso di lavoro in un nuovo pubblico.

   Per ulteriori informazioni su come configurare le attività nell&#39;area di lavoro del flusso di lavoro composizione, fare riferimento a [Operazioni con l&#39;area di lavoro composizione](composition-canvas.md).

1. Aprite le proprietà di composizione per specificare un titolo e una descrizione.

   Se nelle proprietà non è definito alcun titolo, l&#39;etichetta della composizione viene impostata su &quot;Composizione&quot; seguita dalla data e dall&#39;ora di creazione.

   ![](assets/audiences-properties.png)

1. Configura la composizione aggiungendo tutte le attività necessarie tra le attività **[!UICONTROL Pubblico]** e **[!UICONTROL Salva]**. [Scopri come utilizzare l&#39;area di lavoro della composizione](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Quando la composizione è pronta, fai clic sul pulsante **[!UICONTROL Publish]** per pubblicare la composizione e salvare i tipi di pubblico risultanti in Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Puoi pubblicare fino a 10 composizioni in una determinata sandbox. Se hai raggiunto questa soglia, elimina una composizione per liberare spazio e pubblicarne una nuova.

   Se si verifica un errore durante la pubblicazione, vengono visualizzati avvisi con informazioni su come risolvere il problema.

   ![](assets/audiences-alerts.png)

1. La composizione viene pubblicata. I tipi di pubblico risultanti vengono salvati in Adobe Experience Platform e sono pronti per essere indirizzati in Journey Optimizer. [Scopri come indirizzare i tipi di pubblico in Journey Optimizer](../audience/about-audiences.md#segments-in-journey-optimizer)

## Accedere alle composizioni {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Pubblicare il pubblico"
>abstract="Pubblica la composizione per salvare i segmenti di pubblico risultanti in Adobe Experience Platform."

Tutte le composizioni create sono accessibili dalla scheda **[!UICONTROL Composizioni]**. Potete duplicare o eliminare una composizione esistente in qualsiasi momento utilizzando il pulsante con i puntini di sospensione nell&#39;elenco.

Le composizioni possono avere più stati:

* **[!UICONTROL Bozza]**: la composizione è in corso e non è stata pubblicata.
* **[!UICONTROL Pubblicato]**: la composizione è stata pubblicata, i tipi di pubblico risultanti sono stati salvati e sono disponibili per l&#39;utilizzo.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>La composizione del pubblico non è attualmente integrata con la funzionalità di ripristino della sandbox. Prima di avviare il ripristino di una sandbox, è necessario eliminare manualmente le composizioni per garantire che i dati del pubblico associato vengano eliminati correttamente. Informazioni dettagliate sono disponibili nella [Documentazione sulle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions) di Adobe Experience Platform
