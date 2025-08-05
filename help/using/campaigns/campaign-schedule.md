---
solution: Journey Optimizer
product: journey optimizer
title: Pianificare la campagna Azione
description: Scopri come pianificare la campagna Azione.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: crea, ottimizzatore, campagna, superficie, messaggi
exl-id: b183eeb8-606f-444d-9302-274f159c3847
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 16%

---

# Pianificare la campagna Azione {#action-campaign-schedule}

Utilizza la scheda **[!UICONTROL Pianificazione]** per definire la pianificazione della campagna.

Per impostazione predefinita, le campagne di azione iniziano una volta attivate manualmente e terminano non appena il messaggio viene inviato una volta. Se non desideri eseguire la campagna subito dopo l&#39;attivazione, puoi specificare la data e l&#39;ora dell&#39;invio del messaggio utilizzando l&#39;opzione **[!UICONTROL Inizio campagna]**.

L&#39;opzione **[!UICONTROL Fine campagna]** consente di specificare quando interrompere l&#39;esecuzione di una campagna. Al di fuori delle date specificate, la campagna non verrà eseguita.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Quando pianifichi campagne in [!DNL Adobe Journey Optimizer], assicurati che la data/ora di inizio sia allineata alla prima consegna desiderata. Per le campagne ricorrenti, se l’ora pianificata iniziale è già passata, le campagne passeranno al successivo intervallo di tempo disponibile in base alle relative regole di ricorrenza.

Sono disponibili opzioni di pianificazione aggiuntive in base al canale della campagna:

* **Frequenza** (e-mail, SMS, azione push)

  Puoi definire una frequenza con cui inviare il messaggio della campagna. A questo scopo, utilizza le opzioni **[!UICONTROL Action triggers]** nella schermata di creazione della campagna per specificare se la campagna deve essere eseguita ogni giorno, ogni settimana o ogni mese.

* **Attivazione del piano di riscaldamento IP** (e-mail)

  Per le campagne e-mail, puoi creare campagne di attivazione del piano di riscaldamento IP specifiche. La pianificazione della campagna sarà guidata dal piano di riscaldamento IP a cui sarà associata, il che significa che la pianificazione non è più definita nella campagna stessa. [Scopri come creare campagne di riscaldamento IP](../configuration/ip-warmup-campaign.md).

## Passaggi successivi {#next}

Una volta che la pianificazione della campagna è pronta, puoi rivederla e attivarla. [Ulteriori informazioni](review-activate-campaign.md)
