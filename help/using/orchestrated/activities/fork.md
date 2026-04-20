---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Fork
description: Scopri come utilizzare l’attività Fork in una campagna orchestrata
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 4ba956e83c4e28a6d578ffa093d8b8e5fbd2c50b
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 47%

---


# Fork {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Attività Fork"
>abstract="L’attività **Fork** consente di creare transizioni in uscita per avviare più attività contemporaneamente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Transizioni delle attività Fork"
>abstract="Per impostazione predefinita, vengono create due transizioni con attività **Fork**. Fai clic sul pulsante **Aggiungi transizione** per definire una transizione in uscita aggiuntiva e immetterne l’etichetta."

L’attività **[!UICONTROL Fork]** è un componente del **[!UICONTROL Controllo flusso]** che consente di creare più transizioni in uscita, abilitando l’esecuzione in parallelo di più attività.

## Configurare l’attività Fork{#fork-configuration}

Per configurare l’attività **[!UICONTROL Fork]** segui questi passaggi:

![](../assets/workflow-fork.png)

1. Aggiungi un&#39;attività **[!UICONTROL Fork]** alla campagna orchestrata.

1. Definisci un’**[!UICONTROL etichetta]**.

1. Assegna un’etichetta a ogni transizione in uscita. Per impostazione predefinita, vengono fornite due transizioni.

1. Per rimuovere una transizione, fai clic sull’icona ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Se necessario, fai clic su **[!UICONTROL Aggiungi transizione]** per aggiungere un’altra transizione in uscita.

## Esempi {#fork-examples}

Di seguito è riportato un utilizzo tipico dell&#39;attività **[!UICONTROL Fork]**: il targeting dello stesso pubblico con due canali e-mail diversi, uno Marketing e uno Transazionale, per confrontare il comportamento di consegna.

Dopo che un&#39;attività **[!UICONTROL Genera pubblico]** seleziona la popolazione target, un **[!UICONTROL Fork]** crea due rami paralleli:

* **Il ramo 1** si connette a un&#39;attività del canale e-mail di marketing. I messaggi seguono le regole aziendali standard e vengono inviati solo ai profili con consenso.
* **Il ramo 2** si connette a un&#39;attività del canale e-mail transazionale. I messaggi ignorano le regole aziendali e vengono consegnati a tutti i profili indipendentemente dallo stato di consenso.

![](../assets/workflow-fork.png)

Questo modello è utile per comprendere in che modo le impostazioni delle categorie di canale influiscono sul comportamento di consegna e per inviare diversi tipi di messaggi allo stesso pubblico in una singola esecuzione della campagna.
