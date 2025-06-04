---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Genera pubblico
description: Scopri come utilizzare l’attività Genera pubblico in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 7f535b87e415ae9191199b34476adb5c977b66e9
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 52%

---

# Crea pubblico {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Attività Crea pubblico"
>abstract="L’attività **Crea pubblico** ti consente di definire il pubblico che entrerà nella campagna orchestrata. Quando si inviano messaggi nel contesto di una campagna orchestrata, il pubblico del messaggio non è definito nell’attività del canale, ma nell’attività **Crea del pubblico**."

In qualità di addetto al marketing, puoi creare facilmente query complesse utilizzando un’interfaccia intuitiva, per segmentare il pubblico in base a un’ampia gamma di criteri e comportamenti e adattare le campagne in modo più efficace.

Per eseguire questa operazione, utilizza l&#39;attività di targeting **Genera pubblico**. Questa attività ti consente di definire il pubblico che entrerà nella campagna orchestrata. Quando si inviano messaggi nel contesto di una campagna orchestrata, il pubblico del messaggio non è definito nell’attività del canale, ma nell’attività **Crea del pubblico**.

Per definire la popolazione del pubblico, puoi eseguire le seguenti operazioni:

* Seleziona un pubblico esistente.
* Seleziona un filtro predefinito.
* Crea un nuovo pubblico con Query Modeler definendo e combinando criteri di filtro.

>[!NOTE]
>
>I tipi di pubblico caricati da un file non possono essere targetizzati utilizzando un’attività Genera pubblico. A tale scopo, è necessario utilizzare un&#39;attività **Load file** seguita da un&#39;attività **Reconciliation**.


## Configurare l’attività Crea pubblico {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Pubblico"
>abstract="Seleziona il pubblico nello stesso modo in cui utilizzi un pubblico durante la progettazione di una nuova consegna."

Per configurare l’attività **Crea pubblico**, segui questi passaggi:

![](../assets/build-audience.png)

1. Aggiungi un’attività **Crea pubblico**.
1. Definisci un’etichetta.
1. Definisci il tipo di pubblico: **Crea una query personalizzata** o **Leggi pubblico**.
1. Configura il pubblico seguendo i passaggi descritti nelle schede seguenti.


Per creare una query personalizzata, effettua le seguenti operazioni:

1. Seleziona **Crea una query personalizzata**.
1. Scegli la **Dimensione targeting**. La dimensione targeting consente di definire la popolazione target dell’operazione: destinatari, beneficiari del contratto, operatore, iscritti, ecc. Per impostazione predefinita, il target viene selezionato dai destinatari.
1. Fai clic su **Continua**.
1. Utilizza il modellatore di query per definire la query. [Ulteriori informazioni su Query Modeler in questa sezione](../orchestrated-query-modeler.md)

## Esempi{#build-audience-examples}

Ecco un esempio di campagna orchestrata con due attività **Genera pubblico**. Il primo esegue il targeting di un pubblico di giocatori di poker, seguito da una consegna e-mail. Il secondo quello di un pubblico di clienti VIP, seguito da una consegna SMS.

![](../assets/workflow-audience-example.png)
