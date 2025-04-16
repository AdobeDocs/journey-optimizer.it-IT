---
solution: Journey Optimizer
product: journey optimizer
title: Configurare le impostazioni della campagna orchestrata
description: Scopri come configurare le impostazioni delle campagne orchestrate con Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 13%

---

# Configurare le impostazioni della campagna orchestrata {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Proprietà campagna orchestrata"
>abstract="In questa schermata, scegli il modello da utilizzare per creare la campagna orchestrata e specifica un’etichetta. Espandi la sezione **Opzioni aggiuntive** per configurare altre impostazioni, ad esempio il nome interno della campagna orchestrata, la cartella, il fuso orario e il gruppo di supervisori. Si consiglia vivamente di selezionare un gruppo di supervisori in modo che gli operatori vengano avvisati in caso di errore."

Durante la creazione di una campagna orchestrata o l’orchestrazione di attività di campagna orchestrate nell’area di lavoro, puoi accedere alle impostazioni avanzate relative alla campagna orchestrata. Ad esempio, puoi impostare un fuso orario specifico per la campagna orchestrata, gestire il comportamento della campagna orchestrata in caso di errore o gestire il ritardo dopo il quale la cronologia della campagna orchestrata deve essere eliminata.

Queste impostazioni sono preconfigurate nel modello selezionato durante la creazione della campagna orchestrata, ma possono essere modificate in base alle esigenze per questa specifica campagna orchestrata.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Proprietà campagna orchestrata {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Proprietà campagna orchestrata"
>abstract="Questa sezione fornisce proprietà generiche orchestrate per le campagne, accessibili anche durante la creazione della campagna orchestrata. Puoi scegliere il modello da utilizzare per creare la campagna orchestrata e specificare un’etichetta. Espandi la sezione Opzioni aggiuntive per configurare impostazioni specifiche, ad esempio la cartella di archiviazione della campagna orchestrata o il fuso orario."

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

## Impostazioni di segmentazione  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Impostazioni di segmentazione"
>abstract="In questa sezione, puoi selezionare la dimensione di targeting per eseguire il targeting dei profili nella campagna orchestrata e scegliere di mantenere i risultati del flusso di lavoro tra due esecuzioni. Questa opzione deve essere utilizzata solo a scopo di test e non deve mai essere abilitata in una campagna orchestrata di produzione."

* **[!UICONTROL Dimensione targeting]**: seleziona la dimensione di targeting da utilizzare per eseguire il targeting dei profili, tra cui destinatari, beneficiari del contratto, operatore, abbonati, ecc.

* **[!UICONTROL Mantieni il risultato delle popolazioni provvisorie tra due esecuzioni]**: per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell&#39;ultima esecuzione della campagna orchestrata. Le tabelle di lavoro delle esecuzioni precedenti vengono eliminate da una campagna tecnica orchestrata, che viene eseguita su base giornaliera.

  Se questa opzione è abilitata, le tabelle di lavoro verranno mantenute anche dopo l’esecuzione della campagna orchestrata. Puoi utilizzarlo a scopo di test e quindi deve essere utilizzato **solo** in ambienti di sviluppo o di staging. Non deve mai essere sottoposto a check-in in una campagna orchestrata di produzione.

## Impostazioni di esecuzione  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Impostazioni di esecuzione"
>abstract="In questa sezione puoi configurare le impostazioni relative all’esecuzione del flusso di lavoro, ad esempio il numero di giorni in cui viene mantenuta la cronologia orchestrata delle campagne."

* **[!UICONTROL Cronologia in giorni]**: specifica il numero di giorni dopo i quali la cronologia deve essere eliminata. La cronologia contiene elementi relativi alla campagna orchestrata: registri, attività, eventi (oggetti tecnici collegati all’operazione della campagna orchestrata). Il valore predefinito è 30 giorni per i modelli di campagna orchestrati predefiniti. La rimozione della cronologia viene eseguita dalla campagna orchestrata di pulizia tecnica del database, che viene eseguita ogni giorno per impostazione predefinita

  >[!IMPORTANT]
  >
  >Se il campo della **[!UICONTROL Cronologia in giorni]** è lasciato vuoto, il suo valore sarà considerato come “1”, il che significa che la cronologia verrà eliminata dopo 1 giorno.

* **[!UICONTROL Affinità predefinita]**: se l&#39;installazione include più server di campagne orchestrati, utilizzare questo campo per specificare il server su cui verrà eseguita la campagna orchestrata. Questo forza l’esecuzione della campagna orchestrata su un server specifico. Puoi scegliere un nome di affinità esistente, ma assicurati di non utilizzare spazi o segni di punteggiatura. Se si utilizzano server diversi, specificare nomi diversi, separati da virgole.

  >[!IMPORTANT]
  >
  >Se il valore definito in questo campo non esiste in alcun server, la campagna orchestrata rimarrà in sospeso.


* **[!UICONTROL Salva query SQL nel registro]**: selezionare questa opzione per salvare le query SQL dalla campagna workflmulti-step nei registri. Questa funzionalità è riservata agli utenti avanzati. Si applica alle campagne orchestrate che contengono attività di targeting come **[!UICONTROL Genera pubblico]**. Quando questa opzione è abilitata, le query SQL inviate al database durante l’esecuzione della campagna orchestrata vengono visualizzate nei registri della campagna orchestrata, consentendo di analizzarle per ottimizzare le query o diagnosticare i problemi.

## Errore di impostazioni di gestione  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Errore di impostazioni di gestione"
>abstract="In questa sezione puoi definire il modo in cui la campagna orchestrata deve gestire gli errori durante la sua esecuzione. Puoi scegliere di sospendere il processo, ignorare un certo numero di errori o interrompere l’esecuzione della campagna orchestrata."

* **[!UICONTROL Gestione degli errori]**: questo campo consente di definire le azioni da eseguire in caso di errori in un&#39;attività della campagna orchestrata. Sono disponibili tre opzioni:

   * **[!UICONTROL Sospendi il processo]**: la campagna orchestrata viene automaticamente sospesa e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riprendere la campagna orchestrata utilizzando i pulsanti **[!UICONTROL Riprendi]**.
   * **[!UICONTROL Ignora]**: lo stato dell&#39;attività che ha attivato l&#39;errore diventa **[!UICONTROL Non riuscito]**, ma la campagna orchestrata mantiene lo stato **[!UICONTROL Avviato]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Interrompi il processo]**: la campagna orchestrata viene automaticamente interrotta e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riavviare la campagna orchestrata utilizzando i pulsanti **[!UICONTROL Avvia]**.

* **[!UICONTROL Errori consecutivi]**: questo campo diventa disponibile quando il valore **[!UICONTROL Ignora]** è selezionato nel campo **[!UICONTROL In caso di errori]**. È possibile specificare il numero di errori che possono essere ignorati prima dell’interruzione del processo. Una volta raggiunto questo numero, lo stato della campagna orchestrata diventa **[!UICONTROL Non riuscito]**. Se il valore di questo campo è 0, la campagna orchestrata non verrà mai interrotta indipendentemente dal numero di errori.

## Script di inizializzazione {#initialization-script}

Lo script di inizializzazione **** consente di inizializzare le variabili o modificare le proprietà dell&#39;attività. Fare clic sul pulsante **Modifica codice** e digitare il frammento di codice da eseguire. Lo script viene chiamato durante l’esecuzione della campagna orchestrata. Consulta la sezione relativa a [variabili evento](event-variables.md).
