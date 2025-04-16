---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Fork
description: Scopri come utilizzare l’attività Fork in una campagna orchestrata
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '167'
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

L’attività **Fork** è un’attività di **Controllo del flusso**. Ti consente di creare transizioni in uscita per avviare più attività contemporaneamente.

## Configurare l’attività Fork{#fork-configuration}

Per configurare l’attività **Fork** segui questi passaggi:

![](../assets/workflow-fork.png)

1. Aggiungi un&#39;attività **Fork** alla campagna orchestrata.
1. Fai clic su **Aggiungi transizione** per aggiungere una nuova transizione in uscita. Per impostazione predefinita sono definite due transizioni.
1. Aggiungi un’etichetta a ciascuna delle transizioni.

## Esempio{#fork-example}

Nell’esempio seguente vengono utilizzate due attività **Fork**:

* Una prima delle due query, per eseguirle contemporaneamente.
* Una dopo l’intersezione, per inviare contemporaneamente un’e-mail e un SMS alla popolazione target.

![](../assets/workflow-fork-example.png)
