---
solution: Journey Optimizer
product: journey optimizer
title: Creazione di flussi di lavoro di composizione
description: Scopri come creare flussi di lavoro per la composizione per combinare e disporre tipi di pubblico esistenti.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Creazione di flussi di lavoro di composizione {#create-compositions}

I flussi di lavoro di composizione consentono di combinare e disporre i tipi di pubblico esistenti per creare nuovi tipi di pubblico.

## Creare un flusso di lavoro di composizione {#create}

1. Accedere al **[!UICONTROL Segments]** menu e seleziona **[!UICONTROL Create Audience]**.

1. Seleziona **[!UICONTROL Compose Audience]**.

   >[!NOTE]
   >
   >La **[!UICONTROL Build rule]** il metodo di creazione consente di creare una nuova definizione del segmento utilizzando [Servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-create.png)

1. L’area di lavoro della composizione viene visualizzata con due attività predefinite:

   * **[!UICONTROL Audience]**: il punto di partenza della composizione. Questa attività ti consente di selezionare uno o più tipi di pubblico come base per il flusso di lavoro,

   * **[!UICONTROL Save]**: l&#39;ultimo passo della composizione. Questa attività ti consente di salvare il risultato del flusso di lavoro in un nuovo pubblico.
   Per ulteriori informazioni su come configurare le attività nell’area di lavoro della composizione, consulta [Lavorare con il quadro di composizione](composition-canvas.md).

1. Apri le proprietà di composizione per specificare un titolo e una descrizione.

   Se nelle proprietà non è definito alcun titolo, l’etichetta della composizione sarà quella di partenza **[!UICONTROL Audience]** attività.

   ![](assets/audiences-properties.png)

1. Configura la composizione aggiungendo tutte le attività necessarie tra le **[!UICONTROL Audience]** e **[!UICONTROL Save]** attività. [Scopri come lavorare con l’area di lavoro della composizione](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Una volta che la composizione è pronta, fai clic sul pulsante **[!UICONTROL Publish]** per pubblicare la composizione e salvare i tipi di pubblico risultanti in Adobe Experience Platform.

   Se si verifica un errore durante la pubblicazione, gli avvisi contengono informazioni su come risolvere il problema.

   ![](assets/audiences-alerts.png)

1. La composizione viene pubblicata. I tipi di pubblico risultanti vengono salvati in Adobe Experience Platform e sono pronti per il targeting nelle campagne di Journey Optimizer. [Scopri come utilizzare le campagne](../campaigns/get-started-with-campaigns.md)

## Accedere a composizioni {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Pubblicare il pubblico"
>abstract="Pubblica la tua composizione per salvare i tipi di pubblico risultanti in Adobe Experience Platform."

Tutte le composizioni create sono accessibili dal **[!UICONTROL Compositions]** scheda . Possono avere più stati:

* **[!UICONTROL Draft]**: la composizione è in corso e non è stata pubblicata.
* **[!UICONTROL Published]**: la composizione è stata pubblicata, i tipi di pubblico risultanti sono stati salvati e sono disponibili per l’uso.
* **[!UICONTROL Archived]**: la composizione è stata archiviata.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Puoi duplicare o eliminare una composizione esistente in qualsiasi momento utilizzando il pulsante di ellisse nell’elenco.

Ulteriori informazioni:

* [Introduzione alla composizione dell’audience](get-started-audience-orchestration.md)
* [Lavorare con il quadro di composizione](composition-canvas.md)
* [Accesso e gestione dei tipi di pubblico](access-audiences.md)
