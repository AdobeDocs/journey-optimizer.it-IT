---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un’attività di canale in una campagna con più passaggi
description: Scopri come aggiungere un’attività di canale in una campagna con più passaggi
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 2201cc8b9c0c7813c13156937e1cf319660c1039
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 82%

---

# Attività di canale {#channel}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Attività e-mail"
>abstract="L’attività E-mail ti consente di inviare e-mail all’interno della campagna orchestrata, sia per i messaggi singoli che ricorrenti. Consente di automatizzare il processo di invio di e-mail a una destinazione calcolata all’interno della stessa campagna orchestrata. È possibile combinare le attività del canale nell’area di lavoro di una campagna multifase per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Attività SMS"
>abstract="L’attività SMS consente l’invio di SMS all’interno della campagna orchestrata, sia per i messaggi singoli che ricorrenti. Consente di automatizzare il processo di invio di SMS a una destinazione calcolata all’interno della stessa campagna orchestrata. È possibile combinare le attività del canale nell’area di lavoro della campagna multifase per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Attività push"
>abstract="L’attività push ti consente di inviare notifiche push come parte della campagna orchestrata. Consente la consegna di campagne orchestrate, sia singole che ricorrenti, automatizzando l’invio di notifiche push a una destinazione predefinita all’interno della stessa campagna orchestrata. È possibile combinare le attività del canale nell’area di lavoro della campagna per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."

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
>abstract="L’attività direct mail facilita l’invio con direct mail all’interno della campagna orchestrata, sia per messaggi singoli che ricorrenti. Consente di automatizzare il processo di generazione del file di estrazione richiesto dai provider di direct mail. È possibile combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela."


+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Introduzione alle attività](about-activities.md)<br/><br/>Attività:<br/>[AND-join](and-join.md) - [Crea pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - <b>[Attività canale](channels.md)</b> - [Combina](combine.md) - [Deduplica](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] ti consente di automatizzare ed eseguire campagne di marketing su più canali: e-mail, SMS e notifiche push. Puoi combinare le attività del canale nell’area di lavoro della campagna per creare campagne orchestrate cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela.

Ad esempio:
* Invia una serie di messaggi di benvenuto tramite e-mail, SMS e push.
* Consegna un’e-mail di follow-up dopo l’acquisto.
* Invia messaggi di auguri di compleanno personalizzati tramite SMS.

Utilizzando le attività dei canali, puoi creare campagne complete e personalizzate che coinvolgono la clientela su più punti di contatto e danno impulso alle conversioni.

>[!PREREQUISITES]
>
>Prima di aggiungere un’attività di canale, definisci il pubblico target utilizzando un’[Attività Crea pubblico](build-audience.md).

## Aggiungere un’attività di canale e definirne le proprietà {#add}

1. Aggiungi un’attività di canale nell’area di lavoro. Le attività del canale disponibili sono **[!UICONTROL E-mail]**, **[!UICONTROL SMS]** e **[!UICONTROL Push]**.

   ![immagine che mostra l’area di lavoro con le attività disponibili](../assets/channel-add.png)

1. Seleziona l’attività e fai clic su **[!UICONTROL Modifica e-mail]**, **[!UICONTROL Modifica SMS]** o **[!UICONTROL Modifica push]** a seconda del canale scelto.

   ![immagine che mostra l’area di lavoro con un’attività e-mail](../assets/channel-edit.png)

1. Nella scheda **[!UICONTROL Proprietà]**, immetti una descrizione, quindi passa alla scheda **[!UICONTROL Azioni]** per configurare l’attività.

## Configurazione e impostazioni del canale {#configuration}

Utilizza la scheda **[!UICONTROL Azioni]** per selezionare una configurazione dei canali per il messaggio e configurare impostazioni aggiuntive, ad esempio il tracciamento, l’esperimento sul contenuto o il contenuto multilingue.

1. Selezionare una configurazione dei canali

   Una configurazione viene definita da un [amministratore di sistema](../../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Scopri come impostare la configurazione di canale](../../configuration/channel-surfaces.md).

   ![immagine che mostra la sezione Azioni](../assets/channel-actions.png)

1. Traccia il coinvolgimento (per e-mail e SMS).

   Utilizza la sezione **[!UICONTROL Tracciamento delle azioni]** per tenere traccia di come i destinatari reagiscono alle consegne e-mail o SMS. I risultati del tracciamento sono accessibili dal rapporto della campagna una volta che è stata eseguita. [Ulteriori informazioni sui rapporti della campagna](../../reports/campaign-global-report-cja.md).

1. Abilitare la modalità Consegna rapida (per messaggio push).

   La modalità Consegna rapida è un componente aggiuntivo [!DNL Journey Optimizer] che consente l’invio molto rapido di messaggi push in volumi elevati tramite campagne. La consegna rapida viene utilizzata quando il ritardo nella consegna dei messaggi è business-critical, quando desideri inviare un avviso push urgente sui telefoni cellulari, ad esempio una notizia straordinaria agli utenti che hanno installato la tua app per il canale notizie. Per ulteriori informazioni sulle prestazioni durante l’utilizzo della modalità Consegna rapida, consulta la [descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html).

1. Creare un esperimento sui contenuti

   Utilizza la sezione **[!UICONTROL Esperimento contenuti]** per definire più trattamenti di consegna al fine di capire quale funzioni meglio per il tuo pubblico target. Fai clic sul pulsante **[!UICONTROL Crea esperimento]**, quindi segui i passaggi descritti in questa sezione: [Creare un esperimento sui contenuti](../../content-management/content-experiment.md).

1. Aggiungere contenuto multilingue.

   Utilizza la sezione **[!UICONTROL Lingue]** per creare contenuti in più lingue all’interno della campagna. A tale scopo, fai clic sul pulsante **[!UICONTROL Aggiungi lingue]** e seleziona le **[!UICONTROL impostazioni lingua]** desiderate. Informazioni dettagliate su come impostare e utilizzare le funzionalità multilingue sono disponibili in questa sezione: [Introduzione ai contenuti multilingue](../../content-management/multilingual-gs.md)

   ![immagine che mostra la sezione Esperimento contenuti](../assets/channel-experiment.png)

Una volta configurata l’attività del canale, seleziona la scheda **[!UICONTROL Contenuto]** per definirne il contenuto.

## Definire il contenuto {#content}

Passa alla scheda **[!UICONTROL Contenuto]** per creare il messaggio. La procedura dei passaggi varia in base al canale selezionato. Scopri i passaggi dettagliati per creare il contenuto del messaggio nella pagina seguente:

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="e-mail" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>Creare un messaggio e-mail</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>Creare un SMS</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="push" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>Creare una notifica push</strong></a></td>
</tr></table>

## Aggiungere personalizzazione

Personalization nelle campagne orchestrate funziona in modo simile ad altre campagne o percorsi **[!UICONTROL Journey Optimizer]**, ma con alcune differenze chiave specifiche all&#39;area di lavoro orchestrata.

Quando accedi all’editor di personalizzazione da una campagna orchestrata, due cartelle principali contengono gli attributi disponibili per la personalizzazione, descritti di seguito.

* **[!UICONTROL Attributi del profilo]**

  Questa cartella include tutti i dati relativi al profilo di [!DNL Adobe Experience Platform]. Si tratta di attributi standard come nome, indirizzo e-mail, posizione o qualsiasi altra caratteristica acquisita nel profilo utente.

* **[!UICONTROL Attributi di destinazione]** (specifici delle campagne orchestrate)

  Questa cartella è univoca per le campagne orchestrate. Contiene attributi calcolati direttamente nell’area di lavoro della campagna. Contiene due sottocartelle:

   * **`<Targeting dimension>`** (ad esempio, &quot;Destinatari&quot;, &quot;Acquisti&quot;): contiene tutti gli attributi relativi alla dimensione di destinazione della campagna.

   * **`Enrichment`**: include i dati aggiunti tramite **[!UICONTROL attività di arricchimento]** nell&#39;area di lavoro. Questo consente di personalizzare i messaggi in base a set di dati esterni o a logica aggiuntiva incorporata durante l’orchestrazione. [Scopri come utilizzare un&#39;attività di arricchimento](../activities/enrichment.md)

Per una panoramica dettagliata su come utilizzare l&#39;editor di personalizzazione, consulta [Introduzione alla personalizzazione](../../personalization/personalize.md)

## Verifica e verifica il contenuto

Una volta creato il contenuto, utilizza il pulsante **[!UICONTROL Simula contenuto]** per visualizzare in anteprima e verificare il contenuto con profili di test o dati di input di esempio caricati da un file CSV/JSON, oppure aggiunti manualmente. [Ulteriori informazioni](../../content-management/preview-test.md)

![immagine che mostra il pulsante Simula contenuto](../assets/channel-simulate.png)

## Passaggi successivi {#next}

Quando il contenuto del messaggio è pronto, torna alla campagna orchestrata utilizzando la freccia **[!UICONTROL Indietro]**. Puoi quindi completare l’orchestrazione delle attività nell’area di lavoro e pubblicare la campagna per iniziare a inviare i messaggi. [Scopri come avviare e monitorare le campagne orchestrate](../start-monitor-campaigns.md)

![immagine che mostra il pulsante Indietro](../assets/channel-back.png)

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
