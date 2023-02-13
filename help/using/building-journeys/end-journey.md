---
solution: Journey Optimizer
product: journey optimizer
title: Percorso finale
description: Scopri come termina il percorso in Journey Optimizer
feature: Journeys
role: User
level: Beginner
keywords: reinserire, percorso, fine, live, stop
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 3%

---

# Termina un percorso{#journey-ending}

Un percorso può terminare per un individuo in due contesti specifici:

* La persona arriva all&#39;ultima attività di un percorso.
* La persona arriva ad un **Condizione** (o **Wait** attività con una condizione) e non corrisponde a nessuna delle condizioni.

La persona può quindi rientrare nel percorso se è consentito il rientro. Consulta [questa pagina](../building-journeys/journey-gs.md#change-properties)

Per terminare un percorso live, ti consigliamo di chiuderlo. L&#39;arrivo di nuovi clienti nel percorso sarà poi bloccato. I clienti che sono già entrati nel percorso possono sperimentarlo fino alla fine. Vedi [questa sezione](../building-journeys/journey.md#close-journey)

È possibile interrompere un percorso solo se si è verificata un&#39;emergenza e tutte le operazioni di elaborazione devono essere terminate immediatamente su un percorso. Le persone che sono già entrate in un percorso vengono tutte fermate nel loro progresso. Vedi [questa sezione](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Non è possibile riprendere un percorso chiuso o interrotto.

## Tag di fine percorso{#end-tag}

Durante la creazione di un percorso, alla fine di ogni percorso viene visualizzato un &quot;tag finale&quot;. Impossibile aggiungere questo nodo da un utente, non può essere rimosso e può essere modificata solo la relativa etichetta. Segna la fine di ogni percorso del percorso. Se il percorso dispone di diversi percorsi, ti consigliamo di aggiungere un’etichetta a ogni estremità per facilitare la lettura dei rapporti. Consulta [questa pagina](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Chiudi un percorso{#close-journey}

Un percorso può chiudersi per i motivi seguenti:

* Il percorso viene chiuso manualmente tramite il **[!UICONTROL Vicino alle nuove entrate]** pulsante .
* Un percorso basato su segmenti una tantum che ha completato l’esecuzione.
* Dopo l’ultima occorrenza di un percorso basato su segmenti ricorrente.

La chiusura manuale di un percorso garantisce che i clienti che sono già entrati nel percorso possano completare il loro percorso ma che i nuovi utenti non siano in grado di accedere al percorso. Quando un percorso viene chiuso (per uno qualsiasi dei motivi di cui sopra), avrà lo stato **[!UICONTROL Chiuso]**. Il percorso smette di lasciare entrare nuovi individui nel percorso. Le persone già nel percorso possono finire il percorso normalmente. Dopo il timeout globale predefinito di 30 giorni, il percorso passerà al **Completato** stato. Consulta questa [sezione](../building-journeys/journey-gs.md#global_timeout).

Impossibile riavviare o eliminare una versione di un percorso chiuso. Puoi crearne una nuova versione o duplicarla. È possibile eliminare solo i percorsi finiti.

Per chiudere un percorso dall’elenco dei percorsi, fai clic sul pulsante **[!UICONTROL Ellissi]** a destra del nome del percorso e seleziona **[!UICONTROL Vicino alle nuove entrate]**.

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. In **[!UICONTROL Percorsi]** fare clic sul percorso che si desidera chiudere.
1. In alto a destra, fai clic sulla freccia giù.

   ![](assets/finish_drop_down_list.png)

1. Fai clic su **[!UICONTROL Vicino alle nuove entrate]** e conferma nella finestra di dialogo.

## Interrompi un percorso{#stop-journey}

Nel caso tu debba interrompere il progresso di tutti gli individui nel percorso, puoi fermarlo. Arrestare il percorso causerà il timeout di tutti gli individui nel percorso. Tuttavia, fermare un percorso implica che le persone che sono già entrate in un percorso vengono tutte fermate nel loro progresso. Il percorso è fondamentalmente spento. Se vuoi mettere fine a un percorso ti consigliamo di chiuderlo.

Impossibile riavviare una versione di percorso interrotta.

Quando viene arrestato, lo stato del percorso viene impostato su **[!UICONTROL Arrestato]**.

È possibile interrompere un percorso, ad esempio, se un addetto al marketing si rende conto che il percorso esegue il targeting del pubblico errato o che un&#39;azione personalizzata che dovrebbe inviare i messaggi non funziona correttamente. Per interrompere un percorso dall’elenco dei percorsi, fai clic sul pulsante **[!UICONTROL Ellissi]** a destra del nome del percorso e seleziona **[!UICONTROL Interrompi]**.

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. In **[!UICONTROL Percorsi]** fare clic sul percorso che si desidera interrompere.
1. In alto a destra, fai clic sulla freccia giù.
   ![](assets/finish_drop_down_list.png)
1. Fai clic su **[!UICONTROL Interrompi]** e conferma nella finestra di dialogo.
