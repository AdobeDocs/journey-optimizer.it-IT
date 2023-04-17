---
solution: Journey Optimizer
product: journey optimizer
title: Crea il primo flusso di lavoro per la composizione
description: Scopri come creare flussi di lavoro per la composizione per combinare e disporre tipi di pubblico esistenti.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informativo"
source-git-commit: 818c3ff2d159ec3a668c55224996b4736f950e5d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 3%

---

# Crea il primo flusso di lavoro per la composizione {#create-compositions}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* [Introduzione alla composizione dei tipi di pubblico](get-started-audience-orchestration.md)
* **[Crea il primo flusso di lavoro per la composizione](create-compositions.md)**
* [Lavorare nell’area di lavoro per la composizione](composition-canvas.md)
* [Accesso e gestione dei tipi di pubblico](access-audiences.md)

>[!ENDSHADEBOX]

## Creare un flusso di lavoro di composizione {#create}

Per creare un flusso di lavoro di composizione, effettua le seguenti operazioni:

1. Accedere al **[!UICONTROL Segmenti]** menu e seleziona **[!UICONTROL Crea pubblico]**.

1. Seleziona **[!UICONTROL Componi pubblico]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >La **[!UICONTROL Crea regola]** il metodo di creazione consente di creare una nuova definizione del segmento utilizzando [Servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

1. L’area di lavoro della composizione viene visualizzata con due attività predefinite:

   * **[!UICONTROL Pubblico]**: il punto di partenza della composizione. Questa attività ti consente di selezionare uno o più tipi di pubblico come base per il flusso di lavoro,

   * **[!UICONTROL Salva]**: l&#39;ultimo passo della composizione. Questa attività ti consente di salvare il risultato del flusso di lavoro in un nuovo pubblico.
   Per ulteriori informazioni su come configurare le attività nell’area di lavoro della composizione, consulta [Lavorare con il quadro di composizione](composition-canvas.md).

1. Apri le proprietà di composizione per specificare un titolo e una descrizione.

   Se nelle proprietà non è definito alcun titolo, l’etichetta della composizione è impostata su &quot;Composizione&quot; seguita dalla data e dall’ora di creazione.

   ![](assets/audiences-properties.png)

1. Configura la composizione aggiungendo tutte le attività necessarie tra le **[!UICONTROL Pubblico]** e **[!UICONTROL Salva]** attività. [Scopri come lavorare con l’area di lavoro della composizione](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Una volta che la composizione è pronta, fai clic sul pulsante **[!UICONTROL Pubblica]** per pubblicare la composizione e salvare i tipi di pubblico risultanti in Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Puoi pubblicare fino a 75 composizioni in una data sandbox. Se hai raggiunto questa soglia, devi eliminare una composizione per liberare spazio e pubblicarne una nuova.

   Se si verifica un errore durante la pubblicazione, gli avvisi contengono informazioni su come risolvere il problema.

   ![](assets/audiences-alerts.png)

1. La composizione viene pubblicata. I tipi di pubblico risultanti vengono salvati in Adobe Experience Platform e sono pronti per il targeting nelle campagne Journey Optimizer. [Scopri come utilizzare le campagne](../campaigns/get-started-with-campaigns.md)

## Accedere a composizioni {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Pubblicare il pubblico"
>abstract="Pubblica la tua composizione per salvare i tipi di pubblico risultanti in Adobe Experience Platform."

Tutte le composizioni create sono accessibili dal **[!UICONTROL Composizioni]** scheda . Possono avere più stati:

* **[!UICONTROL Bozza]**: la composizione è in corso e non è stata pubblicata.
* **[!UICONTROL Pubblicato]**: la composizione è stata pubblicata, i tipi di pubblico risultanti sono stati salvati e sono disponibili per l’uso.
* **[!UICONTROL Archiviato]**: la composizione è stata archiviata.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Puoi duplicare o eliminare una composizione esistente in qualsiasi momento utilizzando il pulsante con i puntini di sospensione nell’elenco.
