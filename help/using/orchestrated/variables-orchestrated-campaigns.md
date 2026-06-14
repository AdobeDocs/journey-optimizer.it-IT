---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare le variabili nelle campagne orchestrate
description: Scopri come utilizzare le variabili evento nelle campagne orchestrate per creare condizioni e regole di targeting.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
version: Campaign Orchestration
exl-id: 3f2a1c0d-8e9b-4a7c-b5d1-0f2e3a4b5c6d
feature_v2: 
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: cda41058be1eb26538f4b0ef8c7b6c3f1c01eccd
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---


# Utilizzare le variabili nelle campagne orchestrate {#variables-oc}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come impostare le variabili da un segnale o da definizioni globali e utilizzarle per indirizzare il targeting, le condizioni e la logica dell&#39;attività di test nelle campagne orchestrate.

>[!ENDSHADEBOX]

## Impostare le variabili {#set}

In una campagna orchestrata è possibile lavorare con variabili, ovvero valori che determinano il targeting, **[!UICONTROL Condizioni di test]** e altra logica dell&#39;area di lavoro. Questi valori possono provenire da due posizioni:

* **Un segnale** - Se la pianificazione della campagna è **[!UICONTROL Attivata da un segnale]**, è possibile trasmettere parametri quando si attiva la campagna. Tali parametri diventano disponibili come variabili nella campagna orchestrata attivata per tale esecuzione. [Scopri come attivare una campagna orchestrata utilizzando un segnale](trigger-orchestrated-campaign.md)

* **Variabili globali** - È possibile definire coppie nome-valore direttamente nella campagna utilizzando il menu **[!UICONTROL Modifica variabili]**, senza che sia richiesto alcun segnale o API. [Scopri come definire le variabili globali nelle campagne orchestrate](global-variables.md)

>[!NOTE]
>
>Per il momento, le variabili supportano solo i valori **text**.
>
>Le variabili eseguono la **logica canvas** (regole, condizioni) e non possono essere utilizzate per la personalizzazione dei messaggi.

## Utilizzare le variabili nell’area di lavoro {#use}

Le variabili sono disponibili nelle seguenti posizioni nell’area di lavoro:

* **Generatore di regole** - Aprire l&#39;editor di espressioni per una regola e utilizzare il selettore **variabili evento** per selezionare una variabile e inserirne il riferimento nell&#39;espressione. [Scopri come modificare le espressioni](edit-expressions.md)

  Nell&#39;esempio seguente è stata passata una variabile denominata `brand` che la regola utilizza come condizione di filtro.

  ![Condizione del generatore di regole che utilizza una variabile del brand da variabili evento](assets/variables-rule.png){zoomable="yes"}

* **[!UICONTROL Attività Test]** - Quando si definisce una condizione, nell&#39;elenco a discesa **[!UICONTROL Tipo di condizione]** sono elencate tutte le variabili nell&#39;ambito insieme a **[!UICONTROL Conteggio popolazione]**. Seleziona una variabile da utilizzare come base per un ramo di test. [Scopri come configurare l&#39;attività **[!UICONTROL Test]**](activities/test.md)

  Nell&#39;esempio seguente, la variabile `channel` viene utilizzata per instradare il flusso a transizioni diverse a seconda del relativo valore.

  ![Elenco a discesa del tipo di condizione dell&#39;attività di test della variabile di canale](assets/variables-test.png){zoomable="yes"}
