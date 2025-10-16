---
solution: Journey Optimizer
product: journey optimizer
title: Pianificare una campagna attivata da API
description: Scopri come pianificare una campagna attivata da API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
source-git-commit: 93698c93f3750b4d7feff18509f8144a7c79f156
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---

# Pianificare la campagna attivata dall’API {#api-schedule}

Utilizza la scheda **[!UICONTROL Pianificazione]** per definire la pianificazione della campagna.

## Impostare le date di inizio e di fine

Per impostazione predefinita, le campagne attivate dall’API vengono avviate una volta e terminano non appena il messaggio viene inviato una volta. Se non desideri eseguire la campagna subito dopo averla attivata, puoi specificare la data e l&#39;ora dell&#39;invio del messaggio utilizzando l&#39;opzione **[!UICONTROL Inizio campagna]**.

L&#39;opzione **[!UICONTROL Fine campagna]** consente di specificare quando interrompere l&#39;esecuzione di una campagna. Al di fuori delle date specificate, la campagna non verrà eseguita.

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>Quando pianifichi campagne in [!DNL Adobe Journey Optimizer], assicurati che la data/ora di inizio sia allineata alla prima consegna desiderata.

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

Una volta che la configurazione e il contenuto della campagna sono pronti, puoi rivederli e attivarli. [Ulteriori informazioni](../campaigns/review-activate-api-triggered-campaign.md)
