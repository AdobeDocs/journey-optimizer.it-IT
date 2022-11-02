---
solution: Journey Optimizer
product: journey optimizer
title: Principio generale
description: Principio generale
feature: Journeys
topic: Content Management
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: ca423c25d39162838368b2242c1aff99388df768
workflow-type: tm+mt
source-wordcount: '1253'
ht-degree: 9%

---

# Principio generale{#jo-general-principle}

[!DNL Journey Optimizer] consente di creare casi di utilizzo di orchestrazione in tempo reale sfruttando i dati contestuali archiviati negli eventi o nelle origini dati.

Puoi progettare scenari avanzati a più passaggi basati sulle seguenti funzionalità:

* Invia in tempo reale una **consegna unitaria** attivata quando viene ricevuto un evento, oppure **in batch** utilizzando i segmenti di Adobe Experience Platform.

* Sfrutta **dati contestuali** da eventi, informazioni da Adobe Experience Platform o dati da servizi API di terze parti.

* Utilizza la **azioni integrate** per l’invio di messaggi progettati in [!DNL Journey Optimizer] o creare **azioni personalizzate** se utilizzi un sistema di terze parti per l’invio dei messaggi.

* Con il **designer percorsi**, genera i tuoi casi d’uso a più passaggi: trascina facilmente un evento di ingresso o un’attività di lettura segmento, aggiungi delle condizioni e invia messaggi personalizzati.

## Ciclo di vita del percorso{#journey-lifecyle}

### Profili in percorsi{#profile-journey}

In un percorso unitario:

* Se la reintroduzione è abilitata, un profilo può entrare più volte in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso.

* Se l’opzione di rientro è disabilitata, un profilo non può entrare più volte nello stesso percorso

Per ulteriori informazioni sul rientro del profilo, consulta questo [sezione](../building-journeys/journey-gs.md#change-properties).

In un percorso di segmenti letto:

* Per percorsi non ricorrenti: il profilo entra una volta e una sola volta il percorso.
* per percorsi ricorrenti: il profilo entra nel percorso per ogni ricorrenza, se si trova nello stato del segmento o previsto. Se era ancora nel percorso da una precedente ricorrenza, lo riavvierà dall&#39;inizio.

In percorsi di eventi aziendali che iniziano con un segmento di lettura :

Sapendo che questo percorso è basato sulla ricezione di un evento aziendale, se il profilo è qualificato nel segmento previsto, entrerà nel percorso per ogni evento aziendale ricevuto, il che significa che questo profilo può essere più volte nello stesso percorso, allo stesso tempo, ma nel contesto di eventi commerciali diversi.

I percorsi unitari (a partire da un evento o da una qualifica di segmento) includono una guardrail che impedisce l’attivazione errata dei percorsi più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.


### Percorso finale{#journey-ending}

Un percorso può terminare per un individuo in due contesti specifici:

* La persona arriva all&#39;ultima attività di un percorso.
* La persona arriva ad un **Condizione** (o **Wait** attività con una condizione) e non corrisponde a nessuna delle condizioni.

La persona può quindi rientrare nel percorso se è consentito il rientro. Consulta [questa pagina](../building-journeys/journey-gs.md#change-properties)

Per terminare un percorso live, ti consigliamo di chiuderlo. L&#39;arrivo di nuovi clienti nel percorso sarà poi bloccato. I clienti che sono già entrati nel percorso possono sperimentarlo fino alla fine. Vedi [questa sezione](../building-journeys/.md#close-journey)

È possibile interrompere un percorso solo se si è verificata un&#39;emergenza e tutte le operazioni di elaborazione devono essere terminate immediatamente su un percorso. Le persone che sono già entrate in un percorso vengono tutte fermate nel loro progresso. Vedi [questa sezione](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Non è possibile riprendere un percorso chiuso o interrotto.

#### Tag di fine percorso{#end-tag}

Durante la creazione di un percorso, alla fine di ogni percorso viene visualizzato un &quot;tag finale&quot;. Impossibile aggiungere questo nodo da un utente, non può essere rimosso e può essere modificata solo la relativa etichetta. Segna la fine di ogni percorso del percorso. Se il percorso dispone di diversi percorsi, ti consigliamo di aggiungere un’etichetta a ogni estremità per facilitare la lettura dei rapporti. Consulta [questa pagina](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

#### Chiudi un percorso{#close-journey}

Un percorso può chiudersi per i motivi seguenti:

* Il percorso viene chiuso manualmente tramite il **[!UICONTROL Vicino alle nuove entrate]** pulsante .
* Un percorso basato su segmenti una tantum che ha completato l’esecuzione.
* Dopo l’ultima occorrenza di un percorso basato su segmenti ricorrente.

La chiusura manuale di un percorso garantisce che i clienti che sono già entrati nel percorso possano completare il loro percorso ma che i nuovi utenti non siano in grado di accedere al percorso. Quando un percorso viene chiuso (per uno qualsiasi dei motivi di cui sopra), avrà lo stato **[!UICONTROL Chiuso]**. Il percorso smette di lasciare entrare nuovi individui nel percorso. Le persone già nel percorso possono finire il percorso normalmente. Dopo il timeout globale predefinito di 30 giorni, il percorso passerà al **Completato** stato. Vedi questo [sezione](../building-journeys/journey-gs.md#global_timeout).

Impossibile riavviare o eliminare una versione di un percorso chiuso. Puoi crearne una nuova versione o duplicarla. È possibile eliminare solo i percorsi finiti.

Per chiudere un percorso dall’elenco dei percorsi, fai clic sul pulsante **[!UICONTROL Ellissi]** a destra del nome del percorso e seleziona **[!UICONTROL Vicino alle nuove entrate]**.

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. In **[!UICONTROL Percorsi]** fare clic sul percorso che si desidera chiudere.
1. In alto a destra, fai clic sulla freccia giù.

   ![](assets/finish_drop_down_list.png)

1. Fai clic su **[!UICONTROL Vicino alle nuove entrate]** e conferma nella finestra di dialogo.

#### Interrompi un percorso{#stop-journey}

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



## Versioni del percorso{#journey-versions}

Nell’elenco percorso vengono visualizzate tutte le versioni del percorso con il numero di versione. Consulta [questa pagina](../building-journeys/using-the-journey-designer.md).

Quando cerchi un percorso, le versioni più recenti vengono visualizzate nella parte superiore dell’elenco al primo avvio dell’applicazione. Quindi, puoi definire l’ordinamento desiderato e l’applicazione lo manterrà come preferenza utente. La versione del percorso viene visualizzata anche nella parte superiore dell&#39;interfaccia dell&#39;edizione del percorso, sopra l&#39;area di lavoro.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Nella maggior parte dei casi, un profilo non può essere presente più volte nello stesso percorso e allo stesso tempo. Se la reintroduzione è abilitata, un profilo può rientrare in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso. [Ulteriori informazioni](#journey-ending)

Per modificare un percorso live, crea una nuova versione del percorso.

1. Apri la versione più recente del percorso live e fai clic su **[!UICONTROL Creare una nuova versione]** e confermare.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Puoi creare una nuova versione solo dall’ultima versione di un percorso.

1. Apporta le modifiche desiderate, fai clic su **[!UICONTROL Pubblica]** e confermare.

   ![](assets/journeyversions3.png)

Dal momento in cui il percorso verrà pubblicato, i singoli inizieranno a scorrere nell&#39;ultima versione del percorso. Le persone che hanno già inserito una versione precedente vi rimangono fino a quando non finiscono il percorso. Se in seguito vengono reinseriti nello stesso percorso, passeranno alla versione più recente.

Le versioni di percorso possono essere arrestate singolarmente. Tutte le versioni dei percorsi hanno lo stesso nome.

Quando pubblichi una nuova versione di un percorso, la versione precedente termina automaticamente e passa alla **Chiuso** stato. Non può accadere alcuna entrata nel percorso. Anche se si interrompe l&#39;ultima versione, la versione precedente rimane chiusa.

>[!NOTE]
>
>Ulteriori informazioni sulle versioni di percorso protezioni e limitazioni, in [questa pagina](../start/guardrails.md#journey-versions-limitations)