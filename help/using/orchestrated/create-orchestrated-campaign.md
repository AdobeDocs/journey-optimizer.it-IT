---
solution: Journey Optimizer
product: journey optimizer
title: Creare campagne orchestrate con Journey Optimizer
description: Scopri come creare una campagna orchestrata con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 935ab0399da88c792104b7dc14793b69713951fc
workflow-type: tm+mt
source-wordcount: '1734'
ht-degree: 29%

---


# Creare una campagna orchestrata {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Elenco delle campagne orchestrate"
>abstract="Nella scheda **multifase** sono elencate tutte le campagne orchestrate. Fai clic sul nome di una campagna orchestrata per modificarla. Fai clic sul pulsante **Crea campagna orchestrata** per aggiungerne una nuova."

+++ Sommario

| Benvenuto in campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Accesso e gestione delle campagne orchestrate](access-manage-orchestrated-campaigns.md) | [Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md)<br/><br/><b>[Creare e configurare la campagna](create-orchestrated-campaign.md)</b><br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con campagne orchestrate](send-messages.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## Crea la campagna {#create}

Per creare una campagna orchestrata, effettua le seguenti operazioni:

1. Passare al menu **Campagne**.

1. Fai clic sul pulsante **[!UICONTROL Crea campagna orchestrata]** nell&#39;angolo superiore destro della schermata.

1. Nella finestra di dialogo **Proprietà** della campagna orchestrata, seleziona il modello da utilizzare per creare la campagna orchestrata (puoi anche utilizzare il modello predefinito). [Ulteriori informazioni sui modelli di campagna orchestrati](#campaign-templates).

1. Immetti un’etichetta per la campagna orchestrata. Inoltre, ti consigliamo vivamente di aggiungere una descrizione alla campagna orchestrata, nel campo dedicato della sezione **[!UICONTROL Opzioni aggiuntive]** della schermata.

1. Espandi la sezione **[!UICONTROL Opzioni aggiuntive]** per configurare altre impostazioni per la campagna orchestrata.

1. Fai clic sul pulsante **[!UICONTROL Crea campagna orchestrata]** per confermare la creazione della campagna orchestrata.

La campagna orchestrata è ora creata ed è disponibile nell’elenco dei flussi di lavoro. Ora puoi accedere alla relativa area di lavoro visiva e iniziare ad aggiungere, configurare e orchestrare le attività che eseguirà. [Scopri come orchestrare le attività delle campagne orchestrate](orchestrate-activities.md).

## Configurare le impostazioni della campagna {#settings}

<!--Overview of new admin settings> schemas, execution fields, merge policy. [Learn more](configuration-steps.md)-->

Durante la creazione di una campagna orchestrata o l’orchestrazione di attività di campagna orchestrate nell’area di lavoro, puoi accedere alle impostazioni avanzate relative alla campagna orchestrata. Ad esempio, puoi impostare un fuso orario specifico per la campagna orchestrata, gestire il comportamento della campagna orchestrata in caso di errore o gestire il ritardo dopo il quale la cronologia della campagna orchestrata deve essere eliminata.

Queste impostazioni sono preconfigurate nel modello selezionato durante la creazione della campagna orchestrata, ma possono essere modificate in base alle esigenze per questa specifica campagna orchestrata.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

### Proprietà della campagna orchestrata {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Proprietà della campagna orchestrata"
>abstract="In questa sezione sono illustrate le proprietà generiche di una campagna orchestrata che sono accessibili anche durante la relativa creazione. Puoi scegliere il modello da utilizzare per creare una campagna orchestrata e specificare un’etichetta. Espandi la sezione Opzioni aggiuntive per configurare impostazioni specifiche, ad esempio la cartella di archiviazione della campagna orchestrata o il fuso orario."

La sezione **[!UICONTROL Proprietà]** fornisce impostazioni generiche che possono essere configurate durante la creazione di una campagna orchestrata. Per accedere alle proprietà di una campagna orchestrata esistente, fai clic sul pulsante **[!UICONTROL Impostazioni]** disponibile nella barra delle azioni sopra l&#39;area di lavoro della campagna orchestrata.

![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}

Queste proprietà sono:

* **[!UICONTROL Etichetta]** della campagna orchestrata visualizzata nell&#39;elenco.
* **[!UICONTROL Nome interno]** della campagna orchestrata.
* La **[!UICONTROL cartella]** in cui deve essere salvata la campagna orchestrata.
* Il **[!UICONTROL Fuso orario]** predefinito da utilizzare in tutte le attività della campagna orchestrata. Per impostazione predefinita, il fuso orario della campagna orchestrata è quello definito per l’operatore corrente di Campaign.
I valori possibili sono:
   * **Fuso orario del server** per utilizzare il fuso orario dell&#39;organizzazione Adobe Experience Platform
   * **Fuso orario operatore** per utilizzare il fuso orario dell&#39;operatore che esegue la campagna orchestrata
   * **Fuso orario del database** per utilizzare il fuso orario del server del database
   * Un fuso orario specifico
* Quando una campagna orchestrata non riesce, gli operatori appartenenti al gruppo di operatori selezionato nel campo **[!UICONTROL Supervisori]** ricevono una notifica via e-mail.
* Puoi anche immettere una **[!UICONTROL Descrizione]** della campagna orchestrata.

### Impostazioni di segmentazione  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Impostazioni di segmentazione"
>abstract="In questa sezione, puoi selezionare la dimensione di targeting per eseguire il targeting dei profili nella campagna orchestrata e scegliere di mantenere i risultati del flusso di lavoro tra due esecuzioni. Questa opzione deve essere utilizzata solo a scopo di test e non deve mai essere abilitata in una campagna orchestrata di produzione."

* **[!UICONTROL Dimensione targeting]**: seleziona la dimensione di targeting da utilizzare per eseguire il targeting dei profili, tra cui destinatari, beneficiari del contratto, operatore, abbonati, ecc.

* **[!UICONTROL Mantieni il risultato delle popolazioni provvisorie tra due esecuzioni]**: per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell&#39;ultima esecuzione della campagna orchestrata. Le tabelle di lavoro delle esecuzioni precedenti vengono eliminate da una campagna tecnica orchestrata, che viene eseguita su base giornaliera.

  Se questa opzione è abilitata, le tabelle di lavoro verranno mantenute anche dopo l’esecuzione della campagna orchestrata. Puoi utilizzarlo a scopo di test e quindi deve essere utilizzato **solo** in ambienti di sviluppo o di staging. Non deve mai essere sottoposto a check-in in una campagna orchestrata di produzione.

### Impostazioni di esecuzione  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Impostazioni di esecuzione"
>abstract="In questa sezione, puoi configurare le impostazioni relative all’esecuzione del flusso di lavoro, ad esempio il numero di giorni in cui viene mantenuta la cronologia della campagna orchestrata."

* **[!UICONTROL Cronologia in giorni]**: specifica il numero di giorni dopo i quali la cronologia deve essere eliminata. La cronologia contiene elementi relativi alla campagna orchestrata: registri, attività, eventi (oggetti tecnici collegati all’operazione della campagna orchestrata). Il valore predefinito è 30 giorni per i modelli di campagna orchestrati predefiniti. La rimozione della cronologia viene eseguita dalla campagna orchestrata di pulizia tecnica del database, che viene eseguita ogni giorno per impostazione predefinita

  >[!IMPORTANT]
  >
  >Se il campo della **[!UICONTROL Cronologia in giorni]** è lasciato vuoto, il suo valore sarà considerato come “1”, il che significa che la cronologia verrà eliminata dopo 1 giorno.

* **[!UICONTROL Affinità predefinita]**: se l&#39;installazione include più server di campagne orchestrati, utilizzare questo campo per specificare il server su cui verrà eseguita la campagna orchestrata. Questo forza l’esecuzione della campagna orchestrata su un server specifico. Puoi scegliere un nome di affinità esistente, ma assicurati di non utilizzare spazi o segni di punteggiatura. Se si utilizzano server diversi, specificare nomi diversi, separati da virgole.

  >[!IMPORTANT]
  >
  >Se il valore definito in questo campo non esiste in alcun server, la campagna orchestrata rimarrà in sospeso.


* **[!UICONTROL Salva query SQL nel registro]**: selezionare questa opzione per salvare le query SQL dalla campagna workflmulti-step nei registri. Questa funzionalità è riservata agli utenti avanzati. Si applica alle campagne orchestrate che contengono attività di targeting come **[!UICONTROL Genera pubblico]**. Quando questa opzione è abilitata, le query SQL inviate al database durante l’esecuzione della campagna orchestrata vengono visualizzate nei registri della campagna orchestrata, consentendo di analizzarle per ottimizzare le query o diagnosticare i problemi.

### Errore di impostazioni di gestione  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Errore di impostazioni di gestione"
>abstract="In questa sezione puoi definire il modo in cui la campagna orchestrata deve gestire gli errori durante l’esecuzione. Puoi scegliere di sospendere il processo, ignorare un certo numero di errori o interrompere l’esecuzione della campagna orchestrata."

* **[!UICONTROL Gestione degli errori]**: questo campo consente di definire le azioni da eseguire in caso di errori in un&#39;attività della campagna orchestrata. Sono disponibili tre opzioni:

   * **[!UICONTROL Sospendi il processo]**: la campagna orchestrata viene automaticamente sospesa e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riprendere la campagna orchestrata utilizzando i pulsanti **[!UICONTROL Riprendi]**.
   * **[!UICONTROL Ignora]**: lo stato dell&#39;attività che ha attivato l&#39;errore diventa **[!UICONTROL Non riuscito]**, ma la campagna orchestrata mantiene lo stato **[!UICONTROL Avviato]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Interrompi il processo]**: la campagna orchestrata viene automaticamente interrotta e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riavviare la campagna orchestrata utilizzando i pulsanti **[!UICONTROL Avvia]**.

* **[!UICONTROL Errori consecutivi]**: questo campo diventa disponibile quando il valore **[!UICONTROL Ignora]** è selezionato nel campo **[!UICONTROL In caso di errori]**. È possibile specificare il numero di errori che possono essere ignorati prima dell’interruzione del processo. Una volta raggiunto questo numero, lo stato della campagna orchestrata diventa **[!UICONTROL Non riuscito]**. Se il valore di questo campo è 0, la campagna orchestrata non verrà mai interrotta indipendentemente dal numero di errori.

## Utilizzare i modelli per campagna orchestrata {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Modelli per campagna orchestrata"
>abstract="I modelli per campagna orchestrata contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare nuove campagne orchestrate."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Proprietà della campagna orchestrata"
>abstract="I modelli per campagna orchestrata contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare nuove campagne orchestrate. In questa schermata, immetti l’etichetta del modello per campagna orchestrata e configurane le impostazioni, ad esempio il nome interno, la cartella e le cartelle di esecuzione, il fuso orario e il gruppo di supervisori."

I modelli per campagna orchestrata contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare nuove campagne orchestrate. Durante la creazione di una campagna orchestrata, puoi selezionare il modello della campagna orchestrata dalle relative proprietà. Per impostazione predefinita, viene fornito un modello vuoto.

Puoi creare un modello da una campagna orchestrata esistente o crearne uno nuovo da zero. Entrambi i metodi sono descritti di seguito.

>[!BEGINTABS]

>[!TAB Crea un modello da una campagna orchestrata esistente]

Per creare un modello di campagna orchestrata da una campagna orchestrata esistente, effettua le seguenti operazioni:

1. Apri il menu **Campaign** e passa alla campagna orchestrata da salvare come modello.
1. Fare clic sui tre punti a destra del nome della campagna orchestrata e scegliere **Copia come modello**.
1. Conferma la creazione del modello nella finestra a comparsa.
1. Nell’area di lavoro del modello della campagna orchestrata, seleziona, aggiungi e configura le attività in base alle esigenze.
1. Dal pulsante **Impostazioni**, individua le impostazioni per modificare il nome del modello della campagna orchestrata e immetti una descrizione.
1. Seleziona la **cartella** e la **cartella di esecuzione** del modello. La cartella è il percorso in cui viene salvato il modello di campagna orchestrato. La cartella di esecuzione è la cartella in cui vengono salvate le campagne orchestrate create in base a questo modello.
1. Salva le modifiche.

Il modello di campagna orchestrato è ora disponibile nell’elenco dei modelli. Puoi creare una campagna orchestrata basata su questo modello. Questa campagna orchestrata verrà preconfigurata con le impostazioni e le attività definite nel modello.


>[!TAB Creare un modello da zero]


Per creare un modello di campagna orchestrato da zero, effettua le seguenti operazioni:

1. Apri il menu **Campaign** e passa alla scheda **Modelli**. Puoi visualizzare l’elenco dei modelli di campagna orchestrati disponibili.
1. Fai clic sul pulsante **[!UICONTROL Crea modello]** nell’angolo in altro a destra della schermata.
1. Inserisci l’etichetta e apri le opzioni aggiuntive per immettere una descrizione del modello di campagna orchestrato.
1. Seleziona la cartella e la cartella di esecuzione del modello. La cartella è il percorso in cui viene salvato il modello di campagna orchestrato. La cartella di esecuzione è la cartella in cui vengono salvate le campagne orchestrate create in base a questo modello.
1. Fai clic sul pulsante **Crea** per confermare le impostazioni.
1. Nell’area di lavoro del modello della campagna orchestrata, aggiungi e configura le attività in base alle esigenze.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Salva le modifiche.

Il modello di campagna orchestrato è ora disponibile nell’elenco dei modelli. Puoi creare una campagna orchestrata basata su questo modello. Questa campagna orchestrata verrà preconfigurata con le impostazioni e le attività definite nel modello.

>[!ENDTABS]
