---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un’attività di canale in una campagna a più passaggi
description: Scopri come aggiungere un’attività di canale in una campagna a più passaggi
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 85d322e5855c6e658a3a93dc0f3d644ef79437b5
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 17%

---

# Attività di canale {#channel}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](../gs-campaign-creation.md) | [Creare una campagna orchestrata](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - **[Attività canale](channels.md)** - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer] consente di automatizzare ed eseguire campagne di marketing su più canali. Puoi combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne orchestrate cross-channel che possono attivare azioni in base al comportamento dei clienti e ai dati.

Ad esempio, puoi creare una campagna e-mail di benvenuto che include una serie di messaggi su diversi canali, come e-mail, SMS e push. Puoi anche inviare un’e-mail di follow-up dopo che un cliente ha completato un acquisto o inviare un messaggio di auguri di compleanno personalizzato a un cliente tramite SMS.

Utilizzando le attività di canale, puoi creare campagne complete e personalizzate che coinvolgono i clienti in più punti di contatto e favoriscono le conversioni. I canali supportati sono e-mail, SMS e push.

## Prerequisiti {#channel-activity-prereq}

Inizia a creare la tua campagna orchestrata con le attività pertinenti:

* Prima di inserire un’attività di canale, è necessario definire il pubblico. Il pubblico è il target principale della consegna: i profili che ricevono i messaggi. [Scopri come utilizzare l&#39;attività Genera pubblico](build-audience.md)

* Per inviare una consegna ricorrente, avvia la campagna orchestrata con un&#39;attività **[!UICONTROL Scheduler]**. Puoi anche utilizzare un&#39;attività **[!UICONTROL Scheduler]** per singole consegne una tantum per impostare la data di contatto per quella consegna. Tale data di contatto può essere impostata anche nelle impostazioni di consegna. [Scopri come pianificare una campagna orchestrata](../create-orchestrated-campaign.md#schedule)

## Configurare un’attività di canale {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Attività e-mail"
>abstract="L’attività E-mail ti consente di inviare e-mail all’interno della campagna orchestrata, sia per messaggi occasionali che ricorrenti. Serve ad automatizzare il processo di invio di e-mail a una destinazione calcolata all’interno della stessa campagna orchestrata. È possibile combinare le attività del canale nell’area di lavoro di una campagna multifase per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Attività SMS"
>abstract="L’attività SMS ti consente di inviare SMS all’interno della campagna orchestrata, sia per messaggi occasionali che ricorrenti. Serve per automatizzare il processo di invio di SMS a una destinazione calcolata all’interno della stessa campagna orchestrata. È possibile combinare le attività del canale nell’area di lavoro della campagna multifase per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Attività push"
>abstract="L’attività push ti consente di inviare notifiche push come parte della campagna orchestrata. Consente la consegna di campagne orchestrate sia una tantum che ricorrenti, automatizzando l’invio di notifiche push a un target predefinito all’interno della stessa campagna orchestrata. Puoi combinare le attività dei canali nell’area di lavoro della campagna per creare campagne cross-channel che possono attivare azioni in base al comportamento dei clienti e ai dati."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Attività direct mail"
>abstract="L’attività Direct mail facilita l’invio di direct mailing all’interno della campagna orchestrata, sia per messaggi una tantum che ricorrenti. Consente di automatizzare il processo di generazione del file di estrazione richiesto dai provider di direct mail. Puoi combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne cross-channel che possono attivare azioni in base al comportamento dei clienti e ai dati."

Per impostare una consegna nel contesto di una campagna orchestrata, segui i passaggi seguenti.

### Aggiungere un’attività di canale e definirne le proprietà {#add}

1. Aggiungi un’attività di canale nell’area di lavoro. Le attività del canale disponibili sono **[!UICONTROL E-mail]**, **[!UICONTROL SMS]** e **[!UICONTROL Push]**.

   ![immagine che mostra l&#39;area di lavoro con le attività disponibili](../assets/channel-add.png)

1. Seleziona l&#39;attività aggiunta e fai clic sul pulsante **[!UICONTROL Modifica e-mail]**, **[!UICONTROL Modifica SMS]** o **[!UICONTROL Modifica push]** a seconda del canale scelto.

   ![immagine che mostra l&#39;area di lavoro con un&#39;attività e-mail](../assets/channel-edit.png)

1. Nella scheda **[!UICONTROL Proprietà]**, immetti una descrizione per la campagna.

### Configurazione e impostazioni del canale {#configuration}

1. Seleziona la scheda **[!UICONTROL Azioni]** e scegli la configurazione del canale da utilizzare per il messaggio.

   Configurazione definita da un [amministratore di sistema](../../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Scopri come impostare le configurazioni dei canali](../../configuration/channel-surfaces.md).

1. Per e-mail e SMS, utilizza le opzioni di tracciamento per monitorare come i destinatari reagiscono alle consegne e-mail o SMS.

   I risultati del tracciamento sono accessibili dal rapporto della campagna una volta eseguita la campagna. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report-cja.md)

1. Per le notifiche push, utilizza l&#39;opzione **[!UICONTROL Modalità di consegna rapida]** per eseguire l&#39;invio di messaggi ad alta velocità sul canale push a un pubblico di dimensioni inferiori a 30 Mln.

   La modalità Consegna rapida è un componente aggiuntivo **[!DNL Journey Optimizer]** che consente l&#39;invio molto rapido di messaggi push in volumi di grandi dimensioni. [Ulteriori informazioni](../push/create-push.md#rapid-delivery)

1. La sezione **[!UICONTROL Esperimento sui contenuti]** ti consente di definire più trattamenti di consegna per misurare quale offre le migliori prestazioni per il pubblico di destinazione.

   A tale scopo, fai clic sul pulsante **[!UICONTROL Crea esperimento]**, quindi segui i passaggi descritti in questa sezione: [Crea le funzionalità di sperimentazione di un esperimento sui contenuti](../../content-management/content-experiment.md).

1. La sezione **[!UICONTROL Lingue]** consente di creare contenuti in più lingue all&#39;interno della campagna.

   A tale scopo, fare clic sul pulsante **[!UICONTROL Aggiungi lingue]** e selezionare le **[!UICONTROL impostazioni lingua]** desiderate. Informazioni dettagliate su come impostare e utilizzare le funzionalità multilingue sono disponibili in questa sezione: [Introduzione ai contenuti multilingue](../../content-management/multilingual-gs.md)

### Definire il contenuto {#content}

Selezionare la scheda **[!UICONTROL Contenuto]** per definire il contenuto del messaggio. Il processo di creazione dei contenuti dipende dal canale selezionato.

Scopri i passaggi dettagliati per creare il contenuto del messaggio nelle pagine seguenti:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../../email/create-email.md"><img alt="e-mail" src="../../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../../email/create-email.md"><strong>E-mail</strong></a></div></td>
<td><a href="../sms/../create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="push" src="../../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../../push/create-push.md"><strong>Notifica push</strong></a></div></td>
</tr></table>

Una volta definito il contenuto, utilizza il pulsante **[!UICONTROL Simula contenuto]** per visualizzare in anteprima e verificare il contenuto con profili di test o dati di input di esempio caricati da un file CSV/JSON, oppure aggiunti manualmente. [Ulteriori informazioni](../content-management/preview-test.md).

## Passaggi successivi {#next}

Torna alla campagna orchestrata utilizzando la freccia **[!UICONTROL Indietro]**.

![immagine che mostra il pulsante Indietro](../assets/channel-back.png)

Ora puoi completare l’orchestrazione delle attività nell’area di lavoro e pubblicare la campagna per avviare l’invio dei messaggi. [Scopri come avviare e monitorare le campagne orchestrate](../start-monitor-campaigns.md)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
