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
source-git-commit: bc779f732b865d5c178141f0b660d5c75f95a237
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 10%

---

# Pianificare la campagna Azione {#action-campaign-schedule}

Utilizza la scheda **[!UICONTROL Pianificazione]** per definire la pianificazione della campagna.

## Impostare una data di inizio campagna

Per impostazione predefinita, le campagne di azione iniziano una volta attivate manualmente e terminano non appena il messaggio viene inviato una volta.

Se non desideri eseguire la campagna subito dopo l&#39;attivazione, puoi specificare la data e l&#39;ora dell&#39;invio del messaggio nella sezione **[!UICONTROL Inizio campagna]**.

![](assets/campaign-start.png)

>[!NOTE]
>
>Quando pianifichi campagne in [!DNL Adobe Journey Optimizer], assicurati che la data/ora di inizio sia allineata alla prima consegna desiderata. Per le campagne ricorrenti, se l’ora pianificata iniziale è già passata, le campagne passeranno al successivo intervallo di tempo disponibile in base alle relative regole di ricorrenza.

## Impostare una frequenza di esecuzione

Per le azioni **E-mail**, **SMS** e **Notifica push**, puoi definire una frequenza con cui inviare il messaggio della campagna. A questo scopo, utilizza le opzioni **[!UICONTROL Action triggers]** nella schermata di creazione della campagna per specificare se la campagna deve essere eseguita ogni giorno, ogni settimana o ogni mese.

![](assets/campaign-frequency.png)

>[!NOTE]
>
>Per le azioni **email**, puoi creare campagne di attivazione del piano di riscaldamento IP specifiche. La pianificazione della campagna sarà guidata dal piano di riscaldamento IP a cui sarà associata, il che significa che la pianificazione non è più definita nella campagna stessa. [Scopri come creare campagne di riscaldamento IP](../configuration/ip-warmup-campaign.md).

## Impostare una data di fine

La sezione **[!UICONTROL Fine campagna]** ti consente di specificare quando interrompere l&#39;esecuzione di una campagna. Al di fuori delle date specificate, la campagna non verrà eseguita.

![](assets/campaign-end.png)

## Imposta il controllo della frequenza

[!DNL Journey Optimizer] consente di abilitare il controllo della frequenza per le azioni in uscita (e-mail, SMS, notifiche push).

Questa funzione è particolarmente utile per prevenire il sovraccarico sui sistemi a valle, come le pagine di destinazione o le piattaforme di assistenza clienti. Ad esempio, puoi impostare un limite di velocità di 165 messaggi al secondo per garantire una consegna costante senza sovraccaricare i sistemi a valle.

Per impostare il controllo della velocità, abilita l&#39;opzione **[!UICONTROL Limita consegna]** nella sezione **[!UICONTROL Impostazioni consegna]** e specifica la **[!UICONTROL Velocità di consegna]** al secondo desiderata.

* Velocità minima di consegna supportata: 1 al secondo.
* Velocità massima di consegna supportata: 2000 al secondo quando l’opzione &quot;Limita consegna&quot; è abilitata.

![](assets/throttling-rate-control.png)

>[!IMPORTANT]
>
>Quando si imposta una frequenza di consegna, l’intervallo di tempo massimo per il quale il pubblico della campagna può essere eseguito è di 12 ore. Se la velocità di consegna è impostata su un valore che non consente a tutto il pubblico di ricevere il messaggio nell’arco di 12 ore, i profili rimanenti vengono esclusi dalla campagna. Puoi visualizzare il conteggio di questi profili esclusi nel rapporto della campagna.

## Passaggi successivi {#next}

Una volta che la pianificazione della campagna è pronta, puoi rivederla e attivarla. [Ulteriori informazioni](review-activate-campaign.md)
