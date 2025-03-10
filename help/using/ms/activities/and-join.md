---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività AND-join
description: Scopri come utilizzare l’attività AND-join in una campagna in più passaggi
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 65%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Attività AND-join"
>abstract="L&#39;attività **And-join** consente di sincronizzare più rami di esecuzione di una campagna con più passaggi. Viene attivata al termie di tutte le attività precedenti. Questo ti consente di assicurarti che alcune attività siano terminate prima di continuare a eseguire la campagna in più passaggi."

L’attività **Unione AND** è un’attività di **Controllo del flusso**. Consente di sincronizzare più rami di esecuzione di una campagna con più passaggi.

Questa attività attiva la relativa transizione in uscita solo dopo che tutte le transizioni in entrata sono state attivate, in altre parole, dopo che tutte le attività precedenti sono state completate. Questo ti consente di verificare che alcune attività siano state completate prima di continuare a eseguire la campagna in più passaggi.

## Configurare l’attività And-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Opzioni di unione"
>abstract="Seleziona le attività che vuoi unire. Nel menu a discesa **Set primario**, scegli la popolazione di transizione in entrata da mantenere."

Per configurare l’attività **Unione AND**, segui questi passaggi:

![](../assets/workflow-andjoin.png)

1. Aggiungi più attività, come le attività del canale, per creare almeno due rami di esecuzione diversi.
1. Aggiungi un’attività **Unione AND** a uno dei rami.
1. Nella sezione **Opzioni di unione**, seleziona tutte le attività precedenti che desideri unire.
1. Nel menu a discesa **Set primario**, scegli la popolazione di transizione in entrata da mantenere. La transizione in uscita può contenere solo una delle popolazioni di transizione in entrata.

## Esempio{#and-join-example}

L’esempio seguente mostra due rami di campagna con più passaggi e una consegna e-mail e SMS. L’Unione AND verrà attivata quando sono abilitate entrambe le transizioni in entrata. Le notifiche push verranno quindi inviate solo al termine di entrambe le consegne.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
