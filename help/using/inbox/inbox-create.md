---
title: Crea casella in entrata
description: Scopri come creare e configurare una casella in entrata in Adobe Journey Optimizer per inviare messaggi persistenti e non intrusivi agli utenti.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 7d650278-4a62-4666-b8d7-f0b79ec527ea
source-git-commit: e53edd0f6f17f5b764075f61600294b91a020421
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 3%

---

# Creare una casella in entrata {#inbox-create}

Prima di creare una casella in entrata, completare i passaggi in [Configurazione casella in entrata](inbox-configuration.md). La configurazione del canale identifica l’applicazione o il sito web di destinazione, la pagina o la regola e il posizionamento in cui viene eseguito il rendering della casella in entrata.

Per creare una casella in entrata dei messaggi tramite una campagna, effettua le seguenti operazioni:

1. Creare una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Seleziona il tipo di campagna da eseguire:

   * **[!UICONTROL Pianificato - Marketing]**: esegui la campagna immediatamente o in una data specificata. Le campagne pianificate hanno lo scopo di inviare **messaggi di marketing**. Vengono configurati ed eseguiti dall’interfaccia utente di.

   * **[!UICONTROL Attivato da API - Marketing/Transazionale]**: esegui la campagna utilizzando una chiamata API. Le campagne attivate da API hanno lo scopo di inviare **messaggi di marketing** o **messaggi transazionali**, ovvero messaggi inviati in seguito a un&#39;azione eseguita da un individuo: reimpostazione password, acquisto carrello, ecc. [Scopri come attivare una campagna utilizzando le API](../campaigns/api-triggered-campaigns.md)

1. Nella scheda **[!UICONTROL Proprietà]**, specifica un nome e una descrizione per la campagna.

1. Dalla scheda **[!UICONTROL Azione]**, selezionare l&#39;azione **[!UICONTROL Posta in arrivo]**.

   ![](assets/inbox-create-1.png)

1. Selezionare o creare una nuova [configurazione Posta in arrivo](inbox-configuration.md).

   ![](assets/inbox-create-2.png)

1. Accedi alla scheda Contenuto per progettare il messaggio utilizzando Progettazione contenuti. [Ulteriori informazioni](inbox-design.md)

1. Nella scheda **[!UICONTROL Pubblico]**, fai clic sul pulsante **[!UICONTROL Seleziona pubblico]** per visualizzare l&#39;elenco dei tipi di pubblico di Adobe Experience Platform disponibili. [Ulteriori informazioni sui tipi di pubblico](../audience/about-audiences.md)

1. Nel campo **[!UICONTROL Spazio dei nomi identità]**, scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti dal segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

1. Puoi pianificare la campagna a una data specifica o impostarla per la ricorrenza a intervalli regolari. [Ulteriori informazioni](../campaigns/create-campaign.md#schedule)

1. Rivedi e attiva la campagna per inviare messaggi alla casella in entrata.

Ora puoi scegliere questa casella in entrata al momento della creazione della [campagna per schede di contenuto](../content-card/create-content-card.md).
