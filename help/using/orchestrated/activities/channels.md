---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un’attività di canale in una campagna a più passaggi
description: Scopri come aggiungere un’attività di canale in una campagna a più passaggi
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 46%

---

# Attività di canale {#channel}

+++ Sommario

| Benvenuto in campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md) | [Creare una campagna orchestrata](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con le campagne orchestrate](send-messages.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare Query Modeler](orchestrated-query-modeler.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

Adobe Journey Optimizer consente di automatizzare ed eseguire campagne di marketing su canali in entrata e in uscita. Puoi combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne orchestrate cross-channel che possono attivare azioni in base al comportamento dei clienti e ai dati. I canali supportati sono elencati in [questa pagina](../../channels/gs-channels.md).

Ad esempio, puoi creare una campagna e-mail di benvenuto che includa una serie di messaggi su diversi canali, come e-mail, SMS, push e direct mail. Puoi anche inviare un’e-mail di follow-up dopo che un cliente ha completato un acquisto o inviare un messaggio di auguri di compleanno personalizzato a un cliente tramite SMS.

Utilizzando le attività dei canali, puoi creare campagne complete e personalizzate che coinvolgono la clientela su più punti di contatto e danno impulso alle conversioni.

## Prerequisiti {#channel-activity-prereq}

Inizia a creare la tua campagna orchestrata con le attività pertinenti:

* Prima di inserire un’attività di canale, è necessario definire il pubblico. Il pubblico è il target principale della consegna: i profili che ricevono i messaggi.

* Per inviare una consegna ricorrente, avvia la campagna orchestrata con un&#39;attività **Scheduler**. Puoi anche utilizzare un&#39;attività **Scheduler** per singole consegne una tantum per impostare la data di contatto per quella consegna. Tale data di contatto può essere impostata anche nelle impostazioni di consegna.

## Configurare un’attività di canale {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Attività e-mail"
>abstract="L’attività E-mail ti consente di inviare e-mail all’interno della campagna multifase, sia per i messaggi singoli che ricorrenti. Consente di automatizzare il processo di invio di e-mail a una destinazione calcolata all’interno della stessa campagna multifase. È possibile combinare le attività del canale nell’area di lavoro di una campagna multifase per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Attività SMS"
>abstract="L’attività SMS consente l’invio di SMS all’interno della campagna multifase, sia per i messaggi singoli che ricorrenti. Consente di automatizzare il processo di invio di SMS a una destinazione calcolata all’interno della stessa campagna multifase. È possibile combinare le attività del canale nell’area di lavoro della campagna multifase per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Attività push iOS"
>abstract="L’attività push iOS ti consente di inviare notifiche push di iOS come parte della campagna multifase. Consente la consegna di campagne multifase, sia singole che ricorrenti, automatizzando l’invio di notifiche push iOS a una destinazione predefinita all’interno dello stesso flusso di lavoro. Puoi combinare le attività dei canali nell’area del flusso di lavoro per creare flussi di lavoro cross-channel che possono attivare azioni in base al comportamento e ai dati della clientela."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Attività push Android"
>abstract="L’attività push Android ti consente di inviare notifiche push di Android come parte della campagna multifase. Consente la consegna di messaggi sia singoli che ricorrenti, automatizzando l’invio di notifiche push Android a una destinazione predefinita all’interno della stessa campagna multifase. È possibile combinare le attività del canale nell’area di lavoro della campagna multifase per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Attività direct mail"
>abstract="L’attività direct mail facilita l’invio con direct mail all’interno della campagna multifase, sia per messaggi singoli che ricorrenti. Consente di automatizzare il processo di generazione del file di estrazione richiesto dai provider di direct mail. È possibile combinare le attività del canale nell’area di lavoro della campagna multifase per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

Per impostare una consegna nel contesto di una campagna orchestrata, segui i passaggi seguenti:

1. Aggiungi un&#39;attività del canale: **[!UICONTROL E-mail]**, **[!UICONTROL SMS]**, **[!UICONTROL Notifica push (Android)]**, **[!UICONTROL Notifica push (iOS)]** o **[!UICONTROL Direct mail]**.

1. Seleziona il **Tipo di consegna**: singola o ricorrente.

   * Una **consegna singola** è una consegna one-shot, inviata una sola volta, ad esempio un&#39;e-mail del Black Friday.
   * Una **consegna ricorrente** viene inviata più volte in base alla frequenza di esecuzione. Ogni volta che viene eseguita la campagna orchestrata, il pubblico viene ricalcolato e la consegna al pubblico aggiornato viene inviata con il contenuto aggiornato. Ad esempio, una newsletter settimanale o un’e-mail di compleanno ricorrente.

1. Seleziona un **Modello** di consegna. I modelli sono impostazioni di consegna preconfigurate, specifiche per un canale. Per ogni canale è disponibile un modello incorporato, precompilato per impostazione predefinita.

   ![](../assets/delivery-activity-in-wf.png)

   Puoi selezionare il modello dal riquadro a sinistra della configurazione dell’attività del canale. Se il pubblico selezionato in precedenza non è compatibile con il canale, non puoi selezionare un modello. Per risolvere questo problema, aggiorna l&#39;attività **Genera pubblico** per selezionare un pubblico con la mappatura di destinazione corretta.

1. Fai clic su **Crea consegna**. Puoi quindi definire le impostazioni dei messaggi e il contenuto nello stesso modo in cui crei una consegna autonoma. Puoi anche testare e simulare il contenuto.

1. Torna al flusso di lavoro. Se desideri continuare il flusso di lavoro, attiva l&#39;opzione **Genera una transizione in uscita** per aggiungere una transizione dopo l&#39;attività del canale.

1. Fai clic su **Avvia** per avviare la tua campagna orchestrata.

   Per impostazione predefinita, l’avvio di una campagna orchestrata attiva la fase di preparazione dei messaggi, senza inviare immediatamente il messaggio.

1. Apri l&#39;attività del canale per confermare l&#39;invio dal pulsante **Rivedi e invia**.

1. Nella dashboard della consegna, fai clic su **Invia**.

## Esempi {#cross-channel-workflow-sample}

Di seguito è riportato un esempio di campagna orchestrata cross-channel con una segmentazione e due consegne. La campagna orchestrata prende di mira tutti i clienti che vivono a Parigi e che sono interessati alle macchine da caffè. Tra questa popolazione, viene inviata un’e-mail ai clienti regolari e un SMS ai clienti VIP.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

Puoi anche creare una campagna orchestrata ricorrente per inviare un SMS personalizzato ogni primo giorno del mese alle 20 a tutti i clienti che vivono a Parigi.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
