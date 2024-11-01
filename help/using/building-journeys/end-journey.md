---
solution: Journey Optimizer
product: journey optimizer
title: Fine percorso
description: Scopri come termina un percorso in Journey Optimizer
feature: Journeys
role: User
level: Intermediate
keywords: reenter, percorsi, end, live, stop
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 20d99c082ef8d1f2442900dc6a6e6db6b0aaa46f
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 2%

---

# Termina un percorso{#journey-ending}

Un percorso può terminare per un individuo in due contesti specifici:

* La persona arriva all’ultima attività di un percorso.
* La persona arriva a un&#39;attività **Condition** (o a un&#39;attività **Wait** con una condizione) e non corrisponde a nessuna delle condizioni.

La persona può quindi rientrare nel percorso se il rientro è consentito. Vedi [questa pagina](../building-journeys/journey-properties.md#entrance)

Per terminare un percorso live, è consigliabile chiuderlo. L&#39;arrivo di nuovi clienti nel percorso sarà quindi bloccato. I clienti che sono già entrati nel percorso possono provarlo fino alla fine. Vedi [questa sezione](../building-journeys/journey.md#close-journey)

È possibile arrestare un percorso solo in caso di emergenza ed è necessario terminare immediatamente l&#39;elaborazione in un percorso. Le persone che sono già entrate in un percorso sono tutte fermate nel loro avanzamento. Vedi [questa sezione](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Non è possibile riprendere un percorso chiuso o interrotto.

## Tag di fine percorso{#end-tag}

Durante la creazione di un percorso, alla fine di ciascun percorso viene visualizzato un &quot;tag di fine&quot;. Questo nodo non può essere aggiunto da un utente, non può essere rimosso e solo la relativa etichetta può essere modificata. Segna la fine di ogni percorso del percorso. Se il percorso dispone di diversi percorsi, si consiglia di aggiungere un’etichetta a ogni estremità per facilitare la lettura dei rapporti. Consulta [questa pagina](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Chiudi un percorso{#close-journey}

Un percorso può essere chiuso per i motivi seguenti:

* Il percorso viene chiuso manualmente tramite il pulsante **[!UICONTROL Chiudi ai nuovi ingressi]**.
* Un percorso basato su un segmento che ha completato l’esecuzione e ha raggiunto il timeout globale di 91 giorni.
* Dopo l’ultima occorrenza di un percorso ricorrente basato su pubblico.

La chiusura manuale di un percorso consente ai clienti che sono già entrati nel percorso di completare il percorso, ma ai nuovi utenti di non accedere al percorso. Quando un percorso viene chiuso (per uno dei motivi di cui sopra), avrà lo stato **[!UICONTROL Chiuso]**. Il percorso non consente più l&#39;ingresso di nuovi individui nel percorso. Le persone già nel percorso possono finire il percorso normalmente. Dopo il timeout globale predefinito di 91 giorni, il percorso passa allo stato Finito. Consulta [questa sezione](journey-properties.md#timeout).

Dopo il [timeout globale](journey-properties.md#timeout) di 91 giorni, un percorso Read audience passa allo stato **Finished**. Questo comportamento è impostato solo per 91 percorsi (ovvero [valore di timeout globale del percorso](journey-properties.md#global_timeout)) poiché tutte le informazioni sui profili che sono entrati nel gruppo vengono rimosse 91 giorni dopo l&#39;immissione. Le persone ancora nel percorso sono automaticamente interessate. Uscono dal percorso dopo il timeout di 91 giorni.

Consulta questa [sezione](../building-journeys/journey-properties.md#global_timeout).

Impossibile riavviare o eliminare una versione di percorso chiusa. Puoi crearne una nuova versione o duplicarla. È possibile eliminare solo i percorsi finiti.

Per chiudere un percorso dall&#39;elenco dei percorsi, fare clic sul pulsante **[!UICONTROL Puntini di sospensione]** a destra del nome del percorso e selezionare **[!UICONTROL Chiudi ai nuovi ingressi]**.

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. Nell&#39;elenco **[!UICONTROL Percorsi]** fare clic sul percorso che si desidera chiudere.
1. In alto a destra, fare clic sulla freccia giù.

   ![](assets/finish_drop_down_list.png)

1. Fai clic su **[!UICONTROL Chiudi ai nuovi ingressi]** e conferma nella finestra di dialogo.

## Interrompi un percorso{#stop-journey}

Nel caso in cui si debba fermare il progresso di tutti i singoli individui nel percorso, è possibile fermarlo. L’arresto del percorso causerà il timeout di tutti gli utenti del percorso. Tuttavia, l&#39;arresto di un percorso implica che le persone che sono già entrate in un percorso sono tutte ferme nel loro progresso. Il percorso è spento. Se si desidera interrompere un percorso, è consigliabile chiuderlo.

Impossibile riavviare una versione del percorso interrotta.

Quando viene interrotto, lo stato del percorso è impostato su **[!UICONTROL Arrestato]**.

Puoi interrompere un percorso, ad esempio, se un addetto marketing si rende conto che il percorso esegue il targeting del pubblico sbagliato o che un’azione personalizzata destinata a consegnare i messaggi non funziona correttamente. Per interrompere un percorso dall&#39;elenco dei percorsi, fare clic sul pulsante **[!UICONTROL Puntini di sospensione]** a destra del nome del percorso e selezionare **[!UICONTROL Interrompi]**.

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. Nell&#39;elenco **[!UICONTROL Percorsi]** fare clic sul percorso che si desidera interrompere.
1. In alto a destra, fai clic sulla freccia giù.

   ![](assets/finish_drop_down_list2.png)

1. Fai clic su **[!UICONTROL Interrompi]** e conferma nella finestra di dialogo.
