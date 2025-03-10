---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Genera pubblico
description: Scopri come utilizzare l’attività Genera pubblico in una campagna in più passaggi
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 45%

---

# Crea pubblico {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Attività Crea pubblico"
>abstract="L&#39;attività **Genera pubblico** ti consente di definire il pubblico che entrerà nella campagna in più passaggi. Quando si inviano messaggi nel contesto di una campagna in più passaggi, il pubblico del messaggio non è definito nell&#39;attività del canale, ma nell&#39;attività **Genera pubblico**."

L’attività **Crea pubblico** è un’attività di **targeting**. Questa attività ti consente di definire il pubblico che entrerà nella campagna in più passaggi. Quando si inviano messaggi nel contesto di una campagna in più passaggi, il pubblico del messaggio non è definito nell&#39;attività del canale, ma nell&#39;attività **Genera pubblico**.

Per definire la popolazione del pubblico, puoi eseguire le seguenti operazioni:

* Seleziona un pubblico di Adobe Experience Platform.
* Crea un nuovo pubblico con Query Modeler definendo e combinando criteri di filtro.

>[!NOTE]
>
>I tipi di pubblico caricati da un file non possono essere targetizzati utilizzando un’attività Genera pubblico. A tale scopo, è necessario utilizzare un&#39;attività **Load file** seguita da un&#39;attività **Reconciliation**.

<!--
The **Build audience** activity can be placed at the beginning of the workflow or after any other activity. Any activity can be placed after the **Build audience**.
-->

## Configurare l’attività Crea pubblico {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Pubblico"
>abstract="Seleziona il pubblico nello stesso modo in cui utilizzi un pubblico durante la progettazione di una nuova consegna."

Per configurare l’attività **Crea pubblico**, segui questi passaggi:

![](../assets/workflow-audience.png)

1. Aggiungi un’attività **Crea pubblico**.
1. Definisci un’etichetta.
1. Definisci il tipo di pubblico: **Crea una query personalizzata** o **Leggi pubblico**.
1. Configura il pubblico seguendo i passaggi descritti nelle schede seguenti.

>[!BEGINTABS]

>[!TAB Crea il tuo (query)]

Per creare una query personalizzata, effettua le seguenti operazioni:

1. Seleziona **Crea una query personalizzata**.
1. Scegli la **Dimensione targeting**. La dimensione targeting consente di definire la popolazione target dell’operazione: destinatari, beneficiari del contratto, operatore, iscritti, ecc. Per impostazione predefinita, il target viene selezionato dai destinatari.
1. Fai clic su **Continua**.
1. Utilizza il modellatore di query per definire la query, nello stesso modo in cui crei un pubblico durante la progettazione di una nuova e-mail.

>[!TAB Read audience]

Per selezionare un pubblico esistente, segui questi passaggi:

1. Seleziona **Leggi pubblico**.
1. Fai clic su **Continua**.
1. Seleziona il pubblico nello stesso modo in cui utilizzi un pubblico durante la progettazione di una nuova consegna.

>[!ENDTABS]

## Esempi{#build-audience-examples}

Ecco un esempio di campagna con più passaggi con due attività **Genera pubblico**. Il primo esegue il targeting di un pubblico di giocatori di poker, seguito da una consegna e-mail. Il secondo quello di un pubblico di clienti VIP, seguito da una consegna SMS.

![](../assets/workflow-audience-example.png)
