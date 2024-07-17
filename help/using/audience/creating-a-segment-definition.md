---
solution: Journey Optimizer
product: journey optimizer
title: Generare definizioni di segmento
description: Scopri come creare tipi di pubblico tramite le definizioni dei segmenti
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: b9d70bf2b3e16638a03b59fd4036771ad959a631
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 16%

---

# Generare definizioni di segmento {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Creare una regola"
>abstract="Il metodo di creazione delle regole consente di creare una nuova definizione di pubblico, utilizzando il servizio di segmentazione di Adobe Experience Platform."

In questo esempio, creeremo un pubblico per rivolgerci a tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980. Tutti questi clienti avrebbero dovuto aprire l’applicazione Luma negli ultimi 7 giorni, quindi hanno effettuato un acquisto entro 2 ore dall’apertura dell’applicazione.

➡️ [Scopri come creare tipi di pubblico in questo video](#video-segment)

1. Dal menu **[!UICONTROL Tipi di pubblico]**, fai clic sul pulsante **[!UICONTROL Crea pubblico]** e seleziona **[!UICONTROL Genera regola]**.

   ![](assets/create-segment.png)

   La schermata di definizione del segmento ti consente di configurare tutti i campi obbligatori per definire il pubblico. Scopri come configurare i tipi di pubblico nella [documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it){target="_blank"}.

   ![](assets/segment-builder.png)

1. Nel riquadro **[!UICONTROL Proprietà pubblico]**, fornisci un nome e una descrizione (facoltativa) per il pubblico.

   ![](assets/segment-properties.png)

1. Trascina e rilascia i campi desiderati dal riquadro di sinistra all’area di lavoro centrale, quindi configurali in base alle tue esigenze.

   >[!NOTE]
   >
   >I campi disponibili nel riquadro a sinistra variano a seconda della configurazione degli schemi **XDM Individual Profile** e **XDM ExperienceEvent** per la tua organizzazione.  Ulteriori informazioni sono disponibili nella [documentazione di Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

   ![](assets/drag-fields.png)

   In questo esempio, per creare il pubblico, è necessario basarsi sui campi **Attributi** e **Eventi**:

   * **Attributi**: profili che vivono ad Atlanta, San Francisco o Seattle nati dopo il 1980

     ![](assets/add-attributes.png)

   * **Eventi**: profili che hanno aperto l’applicazione Luma negli ultimi 7 giorni e che hanno effettuato un acquisto entro 2 ore dall’apertura dell’applicazione.

     ![](assets/add-events.png)

     >[!NOTE]
     >
     >L’Adobe consiglia di non utilizzare eventi di apertura e invio con segmentazione in streaming. Utilizza invece segnali reali di attività dell’utente come clic, acquisti o dati beacon. Per la logica di frequenza o eliminazione, utilizza le regole di business anziché inviare eventi. [Ulteriori informazioni](about-audiences.md#open-and-send-event-guardrails)

1. Durante l&#39;aggiunta e la configurazione di nuovi campi nell&#39;area di lavoro, il riquadro **[!UICONTROL Proprietà pubblico]** viene aggiornato automaticamente con informazioni sui profili stimati appartenenti al pubblico.

   ![](assets/segment-estimate.png)

1. Quando il pubblico è pronto, fai clic su **[!UICONTROL Salva]**. Viene visualizzato nell’elenco del pubblico di Adobe Experience Platform. È disponibile una barra di ricerca che consente di eseguire ricerche in un pubblico specifico dell’elenco.

Ora puoi utilizzare il pubblico nei tuoi percorsi. Per ulteriori informazioni al riguardo, consulta [questa sezione](../audience/about-audiences.md).

## Video introduttivo{#video-segment}

Scopri in che modo Journey Optimizer utilizza le regole per generare il pubblico e come utilizzare gli attributi, gli eventi e i tipi di pubblico esistenti per creare un pubblico.

>[!VIDEO](https://video.tv.adobe.com/v/3425020?quality=12)
