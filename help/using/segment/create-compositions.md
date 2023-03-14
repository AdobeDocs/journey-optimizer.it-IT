---
solution: Journey Optimizer
product: journey optimizer
title: Creare il primo flusso di lavoro di composizione
description: Scopri come creare flussi di lavoro di composizione per combinare e disporre i tipi di pubblico esistenti.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informativo"
source-git-commit: 8b1bf0b0469c1efc5194dae56ddddd9f05dbf722
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 3%

---

# Creare il primo flusso di lavoro di composizione {#create-compositions}

<table style="table-layout:fixed"><tr style="border: 0;"><tr><td>Informazioni disponibili in questa documentazione:<br/><ul>
<li><a href="get-started-audience-orchestration.md">Introduzione alla composizione dei tipi di pubblico</a></li>
<li><b><a href="create-compositions.md">Creare il primo flusso di lavoro di composizione</a></b></li>
<li><a href="composition-canvas.md">Lavorare nell’area di lavoro per la composizione</a></li>
<li><a href="access-audiences.md">Accesso e gestione dei tipi di pubblico</a></li></ul></td></tr></table>

## Creare un flusso di lavoro di composizione {#create}

Per creare un flusso di lavoro di composizione, effettuate le seguenti operazioni:

1. Accedere a **[!UICONTROL Segmenti]** menu e seleziona **[!UICONTROL Crea pubblico]**.

1. Seleziona **[!UICONTROL Componi pubblico]**.

   >[!NOTE]
   >
   >Il **[!UICONTROL Genera regola]** creazione consente di creare una nuova definizione di segmento utilizzando [Servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-create.png)

1. L’area di lavoro della composizione viene visualizzata con due attività predefinite:

   * **[!UICONTROL Pubblico]**: il punto iniziale della composizione. Questa attività ti consente di selezionare uno o più tipi di pubblico come base per il flusso di lavoro,

   * **[!UICONTROL Salva]**: ultimo passaggio della composizione. Questa attività ti consente di salvare il risultato del flusso di lavoro in un nuovo pubblico.
   Per ulteriori informazioni su come configurare le attività nell’area di lavoro del flusso di lavoro di composizione, consulta [Utilizzare l’area di lavoro per la composizione](composition-canvas.md).

1. Aprite le proprietà di composizione per specificare un titolo e una descrizione.

   Se nelle proprietà non è definito alcun titolo, l&#39;etichetta della composizione viene impostata su &quot;Composizione&quot; seguita dalla data e dall&#39;ora di creazione.

   ![](assets/audiences-properties.png)

1. Configura la composizione aggiungendo tutte le attività necessarie tra **[!UICONTROL Pubblico]** e **[!UICONTROL Salva]** attività. [Scopri come utilizzare l’area di lavoro della composizione](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Una volta che la composizione è pronta, fai clic su **[!UICONTROL Pubblica]** per pubblicare la composizione e salvare i tipi di pubblico risultanti in Adobe Experience Platform.

   Se si verifica un errore durante la pubblicazione, vengono visualizzati avvisi con informazioni su come risolvere il problema.

   ![](assets/audiences-alerts.png)

1. La composizione viene pubblicata. I tipi di pubblico risultanti vengono salvati in Adobe Experience Platform e sono pronti per essere indirizzati nelle campagne Journey Optimizer. [Scopri come utilizzare le campagne](../campaigns/get-started-with-campaigns.md)

## Accedere alle composizioni {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Pubblicare il pubblico"
>abstract="Pubblica la composizione per salvare in Adobe Experience Platform i tipi di pubblico risultanti."

Tutte le composizioni create sono accessibili da **[!UICONTROL Composizioni]** scheda. Possono avere più stati:

* **[!UICONTROL Bozza]**: la composizione è in corso e non è stata pubblicata.
* **[!UICONTROL Pubblicato]**: la composizione è stata pubblicata, i tipi di pubblico risultanti sono stati salvati e sono disponibili per l’uso.
* **[!UICONTROL Archiviato]**: la composizione è stata archiviazione.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Potete duplicare o eliminare una composizione esistente in qualsiasi momento utilizzando il pulsante con i puntini di sospensione nell&#39;elenco.
