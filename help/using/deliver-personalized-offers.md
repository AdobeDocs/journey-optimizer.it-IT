---
title: Aggiungere offerte personalizzate
description: Scopri come aggiungere offerte personalizzate ai messaggi
feature: Journeys
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# Aggiungere offerte personalizzate {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## Informazioni su Gestione delle decisioni {#about-offer-decisioning}

Con [!DNL Journey Optimizer], puoi inserire nei messaggi e-mail decisioni (precedentemente note come attività di offerta) che sfruttano il modulo di gestione delle decisioni per l’offerta al fine di scegliere l’offerta migliore da consegnare ai tuoi clienti.

Ad esempio, puoi aggiungere una decisione che visualizzerà nell’e-mail un’offerta di sconto speciale che varia a seconda del livello di fedeltà del destinatario.

Per ulteriori informazioni su come creare e gestire le offerte, consulta [questa sezione](offers/get-started/starting-offer-decisioning.md).

## Inserire una decisione in un messaggio e-mail {#insert-offers}

Per inserire una decisione in un messaggio e-mail, segui la procedura seguente:

1. Crea l’e-mail, quindi apri E-mail Designer per configurarne il contenuto.

1. Aggiungi un componente di contenuto **[!UICONTROL Offer decision]** (consulta [Utilizzare i componenti di contenuto](content-components.md)).

   ![](assets/deliver-offer-component.png)

1. Al componente viene aggiunta una scheda **[!UICONTROL Offer decision]** . Fai clic su **[!UICONTROL Add personalization - Offer decision]** per aggiungere un’attività di offerta.

   ![](assets/deliver-offer-tab.png)

1. Seleziona il posizionamento corrispondente alle offerte da visualizzare.

   I posizionamenti sono contenitori utilizzati per mostrare le offerte. In questo esempio, utilizzeremo il posizionamento &quot;immagine principale dell’e-mail&quot;. Questo posizionamento è stato creato nella Libreria offerte per visualizzare le offerte di tipo immagine situate nella parte superiore dei messaggi.

1. Seleziona l’attività di offerta da utilizzare nel componente contenuto, quindi fai clic su **[!UICONTROL Add]**.

   >[!NOTE]
   >
   >Nell’elenco vengono visualizzate solo le decisioni compatibili con il posizionamento selezionato. In questo esempio, una sola attività di offerta corrisponde al posizionamento &quot;immagine superiore dell’e-mail&quot;.

   ![](assets/deliver-offer-placement.png)

1. L’attività di offerta viene ora aggiunta al componente . Puoi visualizzare in anteprima le diverse offerte che fanno parte della decisione utilizzando la sezione **[!UICONTROL Offers]** o le frecce dei componenti di contenuto.

   ![](assets/deliver-offer-preview.png)
