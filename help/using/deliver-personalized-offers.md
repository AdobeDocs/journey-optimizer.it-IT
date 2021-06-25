---
title: Aggiungere offerte personalizzate
description: Scopri come aggiungere offerte personalizzate ai messaggi
feature: Percorsi
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: 6fc882827c2ba98af539abf90347483301d48edc
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 2%

---

# Aggiungere offerte personalizzate {#deliver-personalized-offers}

Nei messaggi e-mail [!DNL Journey Optimizer] puoi inserire le decisioni (precedentemente note come &quot;attività di offerta&quot;) che sfruttano il motore decisionale per l’offerta al fine di scegliere l’offerta migliore da consegnare ai tuoi clienti.

Ad esempio, puoi aggiungere una decisione che visualizzerà nell’e-mail un’offerta di sconto speciale che varia a seconda del livello di fedeltà del destinatario.

Per ulteriori informazioni su come creare e gestire le offerte, consulta [questa sezione](offers/get-started/starting-offer-decisioning.md).

Per un **esempio completo** che mostra come configurare le offerte, utilizzale in una decisione e sfrutta questa decisione in un&#39;e-mail, controlla [questa sezione](offers/offers-e2e.md#insert-decision-in-email).

[!DNL :arrow_forward:] [Scopri come aggiungere le offerte come personalizzazione in questo video](#video-offers)


## Inserire una decisione in un messaggio e-mail {#insert-offers}

>[!CAUTION]
>
>Prima di iniziare, devi [definire una decisione di offerta](offers/offer-activities/create-offer-activities.md).

Per inserire una decisione in un messaggio e-mail, segui la procedura seguente:

1. Crea l’e-mail, quindi apri E-mail Designer per configurarne il contenuto.

1. Aggiungi un componente di contenuto **[!UICONTROL Offer decision]** .

   ![](assets/deliver-offer-component.png)

   Scopri come utilizzare i componenti contenuto in [questa sezione](content-components.md).

1. La scheda **[!UICONTROL Offer decision]** viene visualizzata nella palette a destra. Fai clic su **[!UICONTROL Select Offer decision]**.

   ![](assets/deliver-offer-tab.png)

1. Nella finestra visualizzata, seleziona il posizionamento corrispondente alle offerte da visualizzare.

   [](offers/offer-library/creating-placements.md) I posizionamenti sono contenitori utilizzati per mostrare le offerte. In questo esempio, utilizzeremo il posizionamento &quot;immagine principale dell’e-mail&quot;. Questo posizionamento è stato creato nella Libreria offerte per visualizzare le offerte di tipo immagine situate nella parte superiore dei messaggi.

1. Seleziona l’attività di offerta da utilizzare nel componente contenuto, quindi fai clic su **[!UICONTROL Add]**.

   >[!NOTE]
   >
   >Nell’elenco vengono visualizzate solo le decisioni compatibili con il posizionamento selezionato. In questo esempio, una sola attività di offerta corrisponde al posizionamento &quot;immagine superiore dell’e-mail&quot;.

   ![](assets/deliver-offer-placement.png)

L’attività di offerta viene ora aggiunta al componente .


## Anteprima delle offerte in un messaggio e-mail {#preview-offers-in-email}

Puoi visualizzare in anteprima le diverse offerte che fanno parte della decisione aggiunta all’e-mail utilizzando la sezione **[!UICONTROL Offers]** o le frecce dei componenti di contenuto.

![](assets/deliver-offer-preview.png)

Per visualizzare le diverse offerte che fanno parte della decisione con un profilo cliente, segui la procedura seguente.

1. Fai clic su **[!UICONTROL Preview]**.

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >Per visualizzare l’anteprima dei messaggi, devi disporre dei profili di test. Scopri come [creare profili di test](building-journeys/creating-test-profiles.md).

1. Per scegliere lo spazio dei nomi da utilizzare per identificare i profili di test, seleziona **[!UICONTROL Email]** dal campo **[!UICONTROL Identity namespace]** .

   >[!NOTE]
   >
   >In questo esempio, utilizzeremo lo spazio dei nomi **Email** . Ulteriori informazioni sui namespace di identità Adobe Experience Platform [in questa sezione](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=en#getting-started).

1. Nell’elenco dei namespace di identità, selezionare **[!UICONTROL Email]** e fare clic su **[!UICONTROL Select]**.

1. Nel campo **[!UICONTROL Identity value]** , immetti il valore per identificare il profilo di test. In questo esempio, immetti l’indirizzo e-mail di un profilo di test.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. Aggiungi altri profili in modo da poter testare diverse varianti del messaggio a seconda dei dati del profilo.

   ![](assets/deliver-offer-test-profiles.png)

1. Fai clic sulla scheda **[!UICONTROL Preview]** per verificare il messaggio.

1. Seleziona un profilo di test. Viene visualizzata l’offerta corrispondente al profilo selezionato (una donna).

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. Seleziona altri profili di test per visualizzare in anteprima il contenuto dell’e-mail per ogni variante del messaggio. Nel contenuto del messaggio, ora viene visualizzata l’offerta corrispondente al profilo di test selezionato (ora un uomo).

   ![](assets/deliver-offer-test-profile-male-preview.png)

Ulteriori informazioni sui passaggi dettagliati per controllare l&#39;anteprima del messaggio in [questa sezione](#preview-your-messages).

## Video introduttivo{#video-offers}

Scopri come aggiungere un componente offer decisioning ai messaggi in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
