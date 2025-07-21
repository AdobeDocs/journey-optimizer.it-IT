---
solution: Journey Optimizer
product: journey optimizer
title: Pianificare la campagna di azione
description: Scopri come pianificare la campagna di azione.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: crea, ottimizzatore, campagna, superficie, messaggi
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# Pianificare la campagna di azione {#action-campaign-schedule}

Utilizza la scheda **[!UICONTROL Pianificazione]** per definire la pianificazione della campagna.

Per impostazione predefinita, le campagne di azione iniziano una volta attivate manualmente e terminano non appena il messaggio viene inviato. Se non desideri eseguire la campagna subito dopo l&#39;attivazione, puoi specificare la data e l&#39;ora dell&#39;invio del messaggio utilizzando l&#39;opzione **[!UICONTROL Inizio campagna]**.

L&#39;opzione **[!UICONTROL Fine campagna]** consente di specificare quando interrompere l&#39;esecuzione di una campagna. Al di fuori delle date specificate, la campagna non verrà eseguita.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Quando pianifichi campagne in [!DNL Adobe Journey Optimizer], assicurati che la data/ora di inizio sia allineata alla prima consegna desiderata. Per le campagne ricorrenti, se l’ora pianificata iniziale è già passata, le campagne passeranno alla successiva fascia oraria disponibile in base alle relative regole di ricorrenza.

Sono disponibili opzioni di pianificazione aggiuntive in base al canale della campagna:

* **Frequenza** (e-mail, SMS, azione push)

  Puoi definire una frequenza con cui inviare il messaggio della campagna. A questo scopo, utilizza le opzioni **[!UICONTROL Action triggers]** nella schermata di creazione della campagna per specificare se la campagna deve essere eseguita ogni giorno, ogni settimana o ogni mese.

* **Attivazione del piano di riscaldamento IP** (e-mail)

  Per le campagne e-mail, puoi creare campagne di attivazione del piano di riscaldamento IP specifiche. La pianificazione della campagna sarà guidata dal piano di riscaldamento IP a cui sarà associata, il che significa che la pianificazione non è più definita nella campagna stessa. [Scopri come creare campagne di riscaldamento IP](../configuration/ip-warmup-campaign.md).

## Passaggi successivi {#next}

Una volta che la pianificazione della campagna è pronta, puoi rivederla e attivarla. [Ulteriori informazioni](review-activate-campaign.md)
