---
solution: Journey Optimizer
product: journey optimizer
title: Creare un segmento
description: Scopri come creare segmenti
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Creare segmenti {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Creare una regola"
>abstract="Il metodo di creazione delle regole di compilazione consente di creare una nuova definizione di segmento utilizzando il servizio di segmentazione di Adobe Experience Platform."

In questo esempio, creeremo un segmento per tutti i clienti che vivono ad Atlanta, San Francisco, o Seattle e sono nati dopo il 1980. Tutti questi clienti avrebbero dovuto aprire l’applicazione Luma entro gli ultimi 7 giorni, quindi effettuare un acquisto entro 2 ore dall’apertura dell’applicazione.

➡️ [Scopri come creare segmenti in questo video](#video-segment)

1. Accedere al **[!UICONTROL Segments]** quindi fai clic sul **[!UICONTROL Create segment]** pulsante .

   ![](assets/create-segment.png)

   La schermata di definizione del segmento ti consente di configurare tutti i campi richiesti per definire il segmento. Scopri come configurare i segmenti nel [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target=&quot;_blank&quot;}.

   ![](assets/segment-builder.png)

1. In **[!UICONTROL Segment properties]** Specifica un nome e una descrizione (facoltativi) per il segmento.

   ![](assets/segment-properties.png)

1. Trascina e rilascia i campi desiderati dal riquadro di sinistra all’area di lavoro centrale, quindi configurali in base alle tue esigenze.

   >[!NOTE]
   >
   >I campi disponibili nel riquadro a sinistra variano a seconda del modo in cui **Profilo individuale XDM** e **ExperienceEvent XDM** Gli schemi sono stati configurati per la tua organizzazione.  Ulteriori informazioni nel [Documentazione di Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

   ![](assets/drag-fields.png)

   In questo esempio dobbiamo fare affidamento su **Attributi** e **Eventi** campi per creare il segmento:

   * **Attributi**: profili che vivono ad Atlanta, San Francisco o Seattle nati dopo il 1980

      ![](assets/add-attributes.png)

   * **Eventi**: i profili che hanno aperto l’applicazione Luma negli ultimi 7 giorni, quindi hanno effettuato un acquisto entro 2 ore dall’apertura dell’applicazione.

      ![](assets/add-events.png)

1. Durante l’aggiunta e la configurazione di nuovi campi nell’area di lavoro, la **[!UICONTROL Segment Properties]** viene aggiornato automaticamente con le informazioni sui profili stimati appartenenti al segmento.

   ![](assets/segment-estimate.png)

1. Una volta pronto il segmento, fai clic su **[!UICONTROL Save]**. Viene visualizzato nell’elenco dei segmenti di Adobe Experience Platform. È disponibile una barra di ricerca per facilitare la ricerca di un segmento specifico nell’elenco.

Il segmento può ora essere utilizzato nei percorsi. Per ulteriori informazioni, consulta [questa sezione](../segment/about-segments.md).

## Video introduttivo{#video-segment}

Scopri come creare segmenti.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
