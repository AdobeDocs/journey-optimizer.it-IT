---
title: Terminazione di un percorso
description: Terminazione di un percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: d0d914156eaa7fe54a513ee7b4e870edbc76c846
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 2%

---

# Ciclo di vita percorso{#journey-lifecyle}

## Profili in percorsi{#profile-journey}

In un percorso unitario:

* Se la reintroduzione è abilitata, un profilo può entrare più volte in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso.

* Se l’opzione di rientro è disabilitata, un profilo non può entrare più volte nello stesso percorso

Per ulteriori informazioni sul rientro del profilo, consulta questo [sezione](../building-journeys/journey-gs.md#change-properties).

In un percorso di segmenti letto:

* Per percorsi non ricorrenti: il profilo entra una volta e una sola volta il percorso.
* per percorsi ricorrenti: il profilo entra nel percorso per ogni ricorrenza, se si trova nello stato del segmento o previsto. Se era ancora nel percorso da una precedente ricorrenza, lo riavvierà dall&#39;inizio.

In percorsi di eventi aziendali che iniziano con un segmento di lettura :

Sapendo che questo percorso è basato sulla ricezione di un evento aziendale, se il profilo è qualificato nel segmento previsto, entrerà nel percorso per ogni evento aziendale ricevuto, il che significa che questo profilo può essere più volte nello stesso percorso, allo stesso tempo, ma nel contesto di eventi commerciali diversi.

## Percorso finale{#journey-ending}

Un percorso può terminare per un individuo in due contesti specifici:

* La persona arriva all&#39;ultima attività di un percorso.
* La persona arriva ad un **Condizione** (o **Wait** attività con una condizione) e non corrisponde a nessuna delle condizioni.

La persona può quindi rientrare nel percorso se è consentito il rientro. Consulta [questa pagina](../building-journeys/journey-gs.md#change-properties)

Per terminare un percorso live, ti consigliamo di chiuderlo. L&#39;arrivo di nuovi clienti nel percorso sarà poi bloccato. I clienti che sono già entrati nel percorso possono sperimentarlo fino alla fine. Vedi [questa sezione](../building-journeys/journey-end.md#close-journey)

È possibile interrompere un percorso solo se si è verificata un&#39;emergenza e tutte le operazioni di elaborazione devono essere terminate immediatamente su un percorso. Le persone che sono già entrate in un percorso vengono tutte fermate nel loro progresso. Vedi [questa sezione](../building-journeys/journey-end.md#stop-journey)

>[!NOTE]
>
>Non è possibile riprendere un percorso chiuso o interrotto.

<!--

### Journey end tag{#end-tag}

While authoring a journey, an "end node" is displayed at the end of each path. This node cannot be added by a user, cannot be removed and only its label can be changed. It marks the end of each path of the journey. If the journey has several paths, we recommend that you add a label to each end to make reports easier to read. See [this page](../reports/live-report.md).

![](assets/journey-end.png)

-->

### Attività fine{#journey-end-activity}

La **[!UICONTROL End]** l’attività ti consente di contrassegnare la fine di ogni percorso del percorso. Non è obbligatorio ma consigliato per la chiarezza visiva. Consulta [questa pagina](../building-journeys/end-activity.md)

![](assets/journey54.png)

### Chiudi un percorso{#close-journey}

Un percorso può chiudersi per i motivi seguenti:

* Il percorso viene chiuso manualmente tramite il **[!UICONTROL Close to new entrances]** pulsante .
* Un percorso basato su segmenti una tantum che ha completato l’esecuzione.
* Dopo l’ultima occorrenza di un percorso basato su segmenti ricorrente.

La chiusura manuale di un percorso garantisce che i clienti che sono già entrati nel percorso possano completare il loro percorso ma che i nuovi utenti non siano in grado di accedere al percorso. Quando un percorso viene chiuso (per uno qualsiasi dei motivi di cui sopra), avrà lo stato **[!UICONTROL Closed]**. Il percorso smette di lasciare entrare nuovi individui nel percorso. Le persone già nel percorso possono finire il percorso normalmente. Dopo il timeout globale predefinito di 30 giorni, il percorso passerà al **Completato** stato. Vedi questo [sezione](../building-journeys/journey-gs.md#global_timeout).

Impossibile riavviare o eliminare una versione di un percorso chiuso. Puoi crearne una nuova versione o duplicarla. È possibile eliminare solo i percorsi finiti.

Per chiudere un percorso dall’elenco dei percorsi, fai clic sul pulsante **[!UICONTROL Ellipsis]** a destra del nome del percorso e seleziona **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. In **[!UICONTROL Journeys]** fare clic sul percorso che si desidera chiudere.
1. In alto a destra, fai clic sulla freccia giù.

   ![](assets/finish_drop_down_list.png)

1. Fai clic su **[!UICONTROL Close to new entrances]** e conferma nella finestra di dialogo.

### Interrompi un percorso{#stop-journey}

Nel caso tu debba interrompere il progresso di tutti gli individui nel percorso, puoi fermarlo. Arrestare il percorso causerà il timeout di tutti gli individui nel percorso. Tuttavia, fermare un percorso implica che le persone che sono già entrate in un percorso vengono tutte fermate nel loro progresso. Il percorso è fondamentalmente spento. Se vuoi mettere fine a un percorso ti consigliamo di chiuderlo.

Impossibile riavviare una versione di percorso interrotta.

Quando viene arrestato, lo stato del percorso viene impostato su **[!UICONTROL Stopped]**.

È possibile interrompere un percorso, ad esempio, se un addetto al marketing si rende conto che il percorso esegue il targeting del pubblico errato o che un&#39;azione personalizzata che dovrebbe inviare i messaggi non funziona correttamente. Per interrompere un percorso dall’elenco dei percorsi, fai clic sul pulsante **[!UICONTROL Ellipsis]** a destra del nome del percorso e seleziona **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. In **[!UICONTROL Journeys]** fare clic sul percorso che si desidera interrompere.
1. In alto a destra, fai clic sulla freccia giù.

![](assets/finish_drop_down_list.png)

1. Fai clic su **[!UICONTROL Stop]** e conferma nella finestra di dialogo.
