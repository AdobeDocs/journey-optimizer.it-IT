---
solution: Journey Optimizer
product: journey optimizer
title: Generare definizioni di segmento
description: Scopri come creare tipi di pubblico tramite le definizioni dei segmenti
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 14%

---

# Generare definizioni di segmento {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Creare una regola"
>abstract="La creazione di regole consente di creare una nuova definizione di segmenti di pubblico, utilizzando il servizio di creazione di pubblico di Adobe Experience Platform."

In questo esempio, creeremo un pubblico per rivolgerci a tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980. Tutti questi clienti avrebbero dovuto aprire l’applicazione Luma negli ultimi 7 giorni, quindi hanno effettuato un acquisto entro 2 ore dall’apertura dell’applicazione.

➡️ [Scopri come creare tipi di pubblico in questo video](#video-segment)

1. Accedere a **[!UICONTROL Tipi di pubblico]** , quindi fare clic sul pulsante **[!UICONTROL Creare un pubblico]** pulsante.

   ![](assets/create-segment.png)

   La schermata di definizione del segmento ti consente di configurare tutti i campi obbligatori per definire il pubblico. Scopri come configurare i tipi di pubblico in [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it){target="_blank"}.

   ![](assets/segment-builder.png)

1. In **[!UICONTROL Proprietà del pubblico]** , fornisci un nome e una descrizione (facoltativa) per il pubblico.

   ![](assets/segment-properties.png)

1. Trascina e rilascia i campi desiderati dal riquadro di sinistra all’area di lavoro centrale, quindi configurali in base alle tue esigenze.

   >[!NOTE]
   >
   >I campi disponibili nel riquadro a sinistra variano a seconda del modo in cui **Profilo individuale XDM** e **XDM ExperienceEvent** Gli schemi sono stati configurati per la tua organizzazione.  Per ulteriori informazioni, consulta [Documentazione di Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

   ![](assets/drag-fields.png)

   In questo esempio, dobbiamo affidarci a **Attributi** e **Eventi** campi per creare il pubblico:

   * **Attributi**: profili che vivono ad Atlanta, San Francisco o Seattle nati dopo il 1980

     ![](assets/add-attributes.png)

   * **Eventi**: profili che hanno aperto l’applicazione Luma negli ultimi 7 giorni e che hanno poi effettuato un acquisto entro 2 ore dall’apertura dell’applicazione.

     ![](assets/add-events.png)

1. Durante l’aggiunta e la configurazione di nuovi campi nell’area di lavoro, il **[!UICONTROL Proprietà pubblico]** viene aggiornato automaticamente con le informazioni sui profili stimati appartenenti al pubblico.

   ![](assets/segment-estimate.png)

1. Quando il pubblico è pronto, fai clic su **[!UICONTROL Salva]**. Viene visualizzato nell’elenco del pubblico di Adobe Experience Platform. È disponibile una barra di ricerca che consente di eseguire ricerche in un pubblico specifico dell’elenco.

Ora puoi utilizzare il pubblico nei tuoi percorsi. Per ulteriori informazioni al riguardo, consulta [questa sezione](../audience/about-audiences.md).

## Video introduttivo{#video-segment}

Scopri come creare tipi di pubblico.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
