---
solution: Journey Optimizer
product: journey optimizer
title: Configurare le impostazioni delle campagne in più passaggi
description: Scopri come configurare le impostazioni delle campagne con più passaggi con Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 13%

---


# Configurare le impostazioni delle campagne in più passaggi {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Proprietà di una campagna in più passaggi"
>abstract="In questa schermata, scegli il modello da utilizzare per creare la campagna con più passaggi e specifica un’etichetta. Espandi la sezione **Opzioni aggiuntive** per configurare altre impostazioni, ad esempio il nome interno della campagna in più passaggi, la cartella, il fuso orario e il gruppo di supervisori. Si consiglia vivamente di selezionare un gruppo di supervisori in modo che gli operatori vengano avvisati in caso di errore."

Quando crei una campagna in più passaggi o orchestri attività di campagna in più passaggi nell’area di lavoro, puoi accedere alle impostazioni avanzate relative alla campagna in più passaggi. Ad esempio, puoi impostare un fuso orario specifico per la campagna in più passaggi, gestire il comportamento della campagna in più passaggi in caso di errore o gestire il ritardo dopo il quale la cronologia della campagna in più passaggi deve essere eliminata.

Queste impostazioni sono preconfigurate nel modello selezionato durante la creazione della campagna in più passaggi, ma possono essere modificate in base alle esigenze per questa specifica campagna in più passaggi.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Proprietà di una campagna in più passaggi {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Proprietà di una campagna in più passaggi"
>abstract="Questa sezione fornisce proprietà generiche per campagne con più passaggi, accessibili anche durante la creazione di campagne con più passaggi. Puoi scegliere il modello da utilizzare per creare la campagna con più passaggi e specificare un’etichetta. Espandi la sezione Opzioni aggiuntive per configurare impostazioni specifiche, ad esempio la cartella di archiviazione della campagna in più passaggi o il fuso orario."

La sezione **[!UICONTROL Proprietà]** fornisce impostazioni generiche che possono essere configurate durante la creazione di una campagna in più passaggi. Per accedere alle proprietà di una campagna con più passaggi esistente, fai clic sul pulsante **[!UICONTROL Impostazioni]** disponibile nella barra delle azioni sopra l&#39;area di lavoro della campagna con più passaggi.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Queste proprietà sono:

* **[!UICONTROL Label]** della campagna con più passaggi visualizzata nell&#39;elenco.
* **[!UICONTROL Nome interno]** della campagna con più passaggi.
* La **[!UICONTROL cartella]** in cui deve essere salvata la campagna con più passaggi.
* Il **[!UICONTROL Fuso orario]** predefinito da utilizzare in tutte le attività della campagna in più passaggi. Per impostazione predefinita, il fuso orario della campagna in più passaggi è quello definito per l’operatore corrente di Campaign.
I valori possibili sono:
   * **Fuso orario del server** per utilizzare il fuso orario dell&#39;organizzazione Adobe Experience Platform
   * **Fuso orario operatore** per utilizzare il fuso orario dell&#39;operatore che esegue la campagna in più passaggi
   * **Fuso orario del database** per utilizzare il fuso orario del server del database
   * Un fuso orario specifico
* Quando una campagna in più passaggi non riesce, gli operatori appartenenti al gruppo di operatori selezionato nel campo **[!UICONTROL Supervisori]** ricevono una notifica via e-mail.
* Puoi anche immettere una **[!UICONTROL Descrizione]** della tua campagna in più passaggi.

## Impostazioni di segmentazione  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Impostazioni di segmentazione"
>abstract="In questa sezione, puoi selezionare la dimensione di targeting per eseguire il targeting dei profili nella campagna in più passaggi e scegliere di mantenere i risultati del flusso di lavoro tra due esecuzioni. Questa opzione deve essere utilizzata solo a scopo di test e non deve mai essere abilitata in una campagna con più passaggi di produzione."

* **[!UICONTROL Dimensione targeting]**: seleziona la dimensione di targeting da utilizzare per eseguire il targeting dei profili, tra cui destinatari, beneficiari del contratto, operatore, abbonati, ecc.

* **[!UICONTROL Mantieni il risultato delle popolazioni provvisorie tra due esecuzioni]**: per impostazione predefinita, vengono mantenute solo le tabelle di lavoro dell&#39;ultima esecuzione della campagna con più passaggi. Le tabelle di lavoro delle esecuzioni precedenti vengono eliminate da una campagna tecnica in più passaggi, che viene eseguita su base giornaliera.

  Se questa opzione è abilitata, le tabelle di lavoro verranno mantenute anche dopo l’esecuzione della campagna con più passaggi. Puoi utilizzarlo a scopo di test e quindi deve essere utilizzato **solo** in ambienti di sviluppo o di staging. Non deve mai essere controllato in una campagna con più passaggi di produzione.

## Impostazioni di esecuzione  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Impostazioni di esecuzione"
>abstract="In questa sezione puoi configurare le impostazioni relative all’esecuzione del flusso di lavoro, ad esempio il numero di giorni in cui viene mantenuta la cronologia delle campagne in più passaggi."

* **[!UICONTROL Cronologia in giorni]**: specifica il numero di giorni dopo i quali la cronologia deve essere eliminata. La cronologia contiene elementi relativi alla campagna in più passaggi: registri, attività, eventi (oggetti tecnici collegati all’operazione della campagna in più passaggi). Il valore predefinito è 30 giorni per i modelli di campagna in più passaggi predefiniti. La rimozione della cronologia viene eseguita dalla campagna tecnica in più passaggi di pulizia del database, eseguita per impostazione predefinita ogni giorno

  >[!IMPORTANT]
  >
  >Se il campo della **[!UICONTROL Cronologia in giorni]** è lasciato vuoto, il suo valore sarà considerato come “1”, il che significa che la cronologia verrà eliminata dopo 1 giorno.

* **[!UICONTROL Affinità predefinita]**: se l&#39;installazione include più server di campagne con più passaggi, utilizzare questo campo per specificare il server su cui verrà eseguita la campagna con più passaggi. Questo forza l’esecuzione di quella campagna in più passaggi su un determinato server. Puoi scegliere un nome di affinità esistente, ma assicurati di non utilizzare spazi o segni di punteggiatura. Se si utilizzano server diversi, specificare nomi diversi, separati da virgole.

  >[!IMPORTANT]
  >
  >Se il valore definito in questo campo non esiste su alcun server, la campagna con più passaggi rimarrà in sospeso.


* **[!UICONTROL Salva query SQL nel registro]**: selezionare questa opzione per salvare le query SQL dalla campagna workflmulti-step nei registri. Questa funzionalità è riservata agli utenti avanzati. Si applica alle campagne con più passaggi che contengono attività di targeting come **[!UICONTROL Genera pubblico]**. Quando questa opzione è abilitata, le query SQL inviate al database durante l’esecuzione di una campagna con più passaggi vengono visualizzate nei registri della campagna con più passaggi, consentendo di analizzarle per ottimizzare le query o diagnosticare i problemi.

## Errore di impostazioni di gestione  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Errore di impostazioni di gestione"
>abstract="In questa sezione puoi definire come la campagna con più passaggi deve gestire gli errori durante la sua esecuzione. Puoi scegliere di sospendere il processo, ignorare un certo numero di errori o interrompere l’esecuzione della campagna in più passaggi."

* **[!UICONTROL Gestione degli errori]**: questo campo consente di definire le azioni da eseguire in caso di errori in un&#39;attività della campagna in più passaggi. Sono disponibili tre opzioni:

   * **[!UICONTROL Sospendi il processo]**: la campagna con più passaggi viene automaticamente sospesa e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riprendere la campagna con più passaggi utilizzando i pulsanti **[!UICONTROL Riprendi]**.
   * **[!UICONTROL Ignora]**: lo stato dell&#39;attività che ha attivato l&#39;errore diventa **[!UICONTROL Non riuscito]**, ma la campagna in più passaggi mantiene lo stato **[!UICONTROL Avviato]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Interrompi il processo]**: la campagna con più passaggi viene automaticamente interrotta e il suo stato cambia in **[!UICONTROL Non riuscito]**. Una volta risolto il problema, riavvia la campagna in più passaggi utilizzando i pulsanti **[!UICONTROL Avvia]**.

* **[!UICONTROL Errori consecutivi]**: questo campo diventa disponibile quando il valore **[!UICONTROL Ignora]** è selezionato nel campo **[!UICONTROL In caso di errori]**. È possibile specificare il numero di errori che possono essere ignorati prima dell’interruzione del processo. Una volta raggiunto questo numero, lo stato della campagna in più passaggi diventa **[!UICONTROL Non riuscito]**. Se il valore di questo campo è 0, la campagna in più passaggi non verrà mai interrotta indipendentemente dal numero di errori.

## Script di inizializzazione {#initialization-script}

Lo script di inizializzazione **** consente di inizializzare le variabili o modificare le proprietà dell&#39;attività. Fare clic sul pulsante **Modifica codice** e digitare il frammento di codice da eseguire. Lo script viene chiamato quando viene eseguita la campagna in più passaggi. Consulta la sezione relativa a [variabili evento](event-variables.md).

