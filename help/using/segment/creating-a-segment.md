---
title: Creare un segmento
description: Scopri come creare segmenti
feature: Percorsi
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: 9e93a97ff793fec9fdf4aecd645f1df95b65b31a
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 6%

---

# Generare segmenti {#build-segments}

In questo esempio, creeremo un segmento per tutti i clienti che vivono ad Atlanta, San Francisco, o Seattle e sono nati dopo il 1980. Tutti questi clienti avrebbero dovuto aprire l’applicazione Luma entro gli ultimi 7 giorni, quindi effettuare un acquisto entro 2 ore dall’apertura dell’applicazione.

1. Accedi al menu **[!UICONTROL Segments]**, quindi fai clic sul pulsante **[!UICONTROL Create segment]** .

   ![](../assets/create-segment.png)

   La schermata di definizione del segmento ti consente di configurare tutti i campi richiesti per definire il segmento. Scopri come configurare i segmenti nella [documentazione Servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](../assets/segment-builder.png)

1. Nel riquadro **[!UICONTROL Segment properties]**, fornisci un nome e una descrizione (facoltativi) per il segmento.

   ![](../assets/segment-properties.png)

1. Trascina e rilascia i campi desiderati dal riquadro di sinistra all’area di lavoro centrale, quindi configurali in base alle tue esigenze.

   >[!NOTE]
   >
   >I campi disponibili nel riquadro a sinistra variano a seconda della configurazione degli schemi **XDM Singolo profilo** e **XDM ExperienceEvent** per la tua organizzazione.  Ulteriori informazioni sono disponibili nella documentazione [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).

   ![](../assets/drag-fields.png)

   In questo esempio, per creare il segmento è necessario basarsi sui campi **Attributi** e **Eventi** :

   * **Attributi**: profili che vivono ad Atlanta, San Francisco o Seattle nati dopo il 1980

      ![](../assets/add-attributes.png)

   * **Eventi**: i profili che hanno aperto l’applicazione Luma negli ultimi 7 giorni, quindi hanno effettuato un acquisto entro 2 ore dall’apertura dell’applicazione.

      ![](../assets/add-events.png)

1. Durante l’aggiunta e la configurazione di nuovi campi nell’area di lavoro, il riquadro **[!UICONTROL Segment Properties]** viene aggiornato automaticamente con le informazioni sui profili stimati appartenenti al segmento.

   ![](../assets/segment-estimate.png)

1. Quando il segmento è pronto, fai clic su **[!UICONTROL Save]**. Viene visualizzato nell’elenco dei segmenti di Adobe Experience Platform. È disponibile una barra di ricerca per facilitare la ricerca di un segmento specifico nell’elenco.

Il segmento può ora essere utilizzato nei percorsi. Per ulteriori informazioni al riguardo, consulta [questa sezione](../segment/about-segments.md).

## Video tutorial{#create-segment-video}

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
