---
solution: Journey Optimizer
product: journey optimizer
title: Fine del percorso
description: Scopri come termina un percorso in Journey Optimizer
feature: Journeys
role: User
level: Beginner
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Terminare un percorso{#journey-ending}

Un percorso può terminare per un singolo utente in due contesti specifici:

* La persona arriva all&#39;ultima attività di un percorso.
* La persona arriva ad un **Condizione** (o **Wait** attività con una condizione) e non corrisponde a nessuna delle condizioni.

La persona può quindi rientrare nel percorso se è consentito un rientro. Vedi [questa pagina](../building-journeys/journey-gs.md#change-properties)

Per terminare un viaggio live, ti consigliamo di chiuderlo. L&#39;arrivo di nuovi clienti nel viaggio sarà poi bloccato. I clienti che sono già entrati nel percorso possono sperimentarlo fino alla fine. Vedi [questa sezione](../building-journeys/journey.md#close-journey)

Puoi interrompere un percorso solo se si è verificata un’emergenza e tutte le elaborazioni devono essere terminate immediatamente durante un percorso. Le persone che sono già entrate in un percorso vengono tutte fermate durante il loro progresso. Vedi [questa sezione](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Non è possibile riprendere un percorso chiuso o interrotto.

## Tag di fine percorso{#end-tag}

Durante la creazione di un percorso, alla fine di ciascun percorso viene visualizzato un &quot;tag finale&quot;. Impossibile aggiungere questo nodo da un utente, non può essere rimosso e può essere modificata solo la relativa etichetta. Segna la fine di ogni percorso del viaggio. Se il percorso include diversi percorsi, ti consigliamo di aggiungere un’etichetta a ogni estremità per facilitare la lettura dei rapporti. Vedi [questa pagina](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Chiudere un percorso{#close-journey}

Un percorso può chiudersi per i motivi seguenti:

* Il percorso viene chiuso manualmente tramite la **[!UICONTROL Close to new entrances]** pulsante .
* Un percorso basato su segmenti una tantum che ha completato l’esecuzione.
* Dopo l’ultima occorrenza di un percorso ricorrente basato su segmenti.

La chiusura manuale di un percorso garantisce che i clienti che hanno già inserito il percorso possano completare il percorso, ma che i nuovi utenti non siano in grado di accedere al percorso. Quando un percorso viene chiuso (per uno dei motivi sopra indicati), avrà lo stato **[!UICONTROL Closed]**. Il viaggio smette di permettere a nuovi individui di accedere al percorso. Le persone già in viaggio possono completare il viaggio normalmente. Dopo il timeout globale predefinito di 30 giorni, il percorso passerà al **Completato** stato. Vedi questo [sezione](../building-journeys/journey-gs.md#global_timeout).

Impossibile riavviare o eliminare una versione del percorso chiusa. Puoi crearne una nuova versione o duplicarla. È possibile eliminare solo i percorsi completati.

Per chiudere un percorso dall’elenco dei percorsi, fai clic sul pulsante **[!UICONTROL Ellipsis]** a destra del nome del percorso e seleziona **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

Puoi anche:

1. In **[!UICONTROL Journeys]** , fai clic sul percorso da chiudere.
1. In alto a destra, fai clic sulla freccia giù.

   ![](assets/finish_drop_down_list.png)

1. Fai clic su **[!UICONTROL Close to new entrances]** e conferma nella finestra di dialogo.

## Interrompere un percorso{#stop-journey}

Nel caso tu debba interrompere il progresso di tutti gli individui nel viaggio, puoi fermarlo. L’arresto del percorso causerà il timeout di tutti gli utenti presenti nel percorso. Tuttavia, interrompere un percorso implica che le persone che sono già entrate in un percorso vengono tutte fermate nel loro progresso. Il viaggio è fondamentalmente spento. Se vuoi porre fine a un percorso ti consigliamo di chiuderlo.

Impossibile riavviare una versione del percorso interrotta.

Quando viene interrotto, lo stato del percorso viene impostato su **[!UICONTROL Stopped]**.

Puoi interrompere un percorso, ad esempio, se un addetto al marketing si rende conto che il percorso esegue il targeting del pubblico errato o che un’azione personalizzata che dovrebbe inviare i messaggi non funziona correttamente. Per interrompere un percorso dall’elenco dei percorsi, fai clic sul pulsante **[!UICONTROL Ellipsis]** a destra del nome del percorso e seleziona **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

Puoi anche:

1. In **[!UICONTROL Journeys]** , fai clic sul percorso da interrompere.
1. In alto a destra, fai clic sulla freccia giù.
   ![](assets/finish_drop_down_list.png)
1. Fai clic su **[!UICONTROL Stop]** e conferma nella finestra di dialogo.
