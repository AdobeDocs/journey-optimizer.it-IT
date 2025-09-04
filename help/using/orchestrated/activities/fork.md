---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Fork
description: Scopri come utilizzare l’attività Fork in una campagna orchestrata
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 86%

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
