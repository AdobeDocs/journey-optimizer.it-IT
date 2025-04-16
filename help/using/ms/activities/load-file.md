---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Load file
description: Scopri come utilizzare l’attività Load file in una campagna orchestrata
hide: true
hidefromtoc: true
exl-id: ae0dc980-2361-4c3b-a68e-ae0bb5dc0a26
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 38%

---

# Caricare file {#load-file}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile"
>title="Attività di caricamento file"
>abstract="L’attività **Carica file** è un’attività di **gestione dati**. Usa questa attività per utilizzare i dati memorizzati in un file esterno. I profili e i dati non vengono aggiunti al database, ma tutti i campi nel file di input sono disponibili per la personalizzazione, per l’aggiornamento dei profili o di qualsiasi altra tabella. "

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_outboundtransition"
>title="Rifiuta la gestione della transizione in uscita"
>abstract="Rifiuta la gestione della transizione in uscita"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_outboundtransition_reject"
>title="Rifiuta la gestione della transizione in uscita per i valori rifiutati"
>abstract="Rifiuta la gestione della transizione in uscita per i valori rifiutati"


L’attività **Carica file** è un’attività di **gestione dati**. Utilizza questa attività per lavorare con profili e dati memorizzati in un file esterno. I profili e i dati non vengono aggiunti al database, ma tutti i campi nel file di input sono disponibili per la personalizzazione, per l’aggiornamento dei profili o di qualsiasi altra tabella.

>[!NOTE]
>Sono supportati i formati di file di testo (TXT) e i valori separati da virgole (CSV). È possibile caricare file con una dimensione massima di 50 MB.

Questa attività può essere utilizzata con un&#39;attività [Reconciliation](reconciliation.md) per collegare dati non identificati a risorse esistenti. Ad esempio, l&#39;attività **Load file** può essere inserita prima di un&#39;attività **Reconciliation** se si importano dati non standard nel database.

## Configurare l’attività Load file {#load-configuration}

La configurazione dell&#39;attività **Load file** prevede due passaggi. Innanzitutto, devi definire la struttura del file prevista effettuando il caricamento di un file di esempio. Al termine, puoi specificare l’origine del file di cui verranno importati i dati. Segui i passaggi seguenti per configurare l’attività.

![](../assets/workflow-load-file.png)

### Configurare il file di esempio {#sample}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_samplefile"
>title="File di esempio"
>abstract="Seleziona la struttura di file prevista caricando un file di esempio."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_formatting"
>title="Formattazione per l’attività di caricamento file"
>abstract="Nella sezione **Formattazione**, specifica la formattazione del file per garantire che i dati vengano importati correttamente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_valueremapping"
>title="Rimappatura del valore per l’attività di caricamento file"
>abstract="Utilizza questa opzione per mappare valori specifici dai file caricati con nuovi valori. Ad esempio, se la colonna contiene i valori “True”/“False”, puoi aggiungere una mappatura per sostituire automaticamente tali valori con i caratteri “0”/“1”."

Segui questi passaggi per configurare il file di esempio utilizzato per definire la struttura di file prevista:

1. Aggiungi un&#39;attività **Load file** nella campagna orchestrata.

1. Seleziona il file di esempio da utilizzare per definire la struttura di file prevista. A tale scopo, fare clic sul pulsante **Seleziona file** nella sezione **[!UICONTROL File di esempio]** e selezionare il file locale da utilizzare.

1. Viene visualizzata un&#39;anteprima del file di esempio, con un massimo di 30 righe.

1. Nell&#39;elenco a discesa **[!UICONTROL Tipo file]** specificare se il file utilizza colonne delimitate o colonne a larghezza fissa.

   ![](../assets/workflow-load-file-sample.png)

1. Per i tipi di file di colonne delimitate, utilizzare la sezione **Colonne** per configurare le proprietà di ogni colonna.

   +++Opzioni disponibili per le colonne di file

   * **[!UICONTROL Etichetta]**: etichetta da visualizzare per la colonna.
   * **[!UICONTROL Tipo di dati]**: tipo di dati contenuti nella colonna.
   * **[!UICONTROL Larghezza]** (tipo di dati stringa): numero massimo di caratteri da visualizzare nella colonna.
   * **[!UICONTROL Trasformazione dati]** (tipo di dati stringa): applica la trasformazione ai valori contenuti nella colonna.
   * **[!UICONTROL Gestione degli spazi vuoti]** (tipo di dati stringa): specificare come gestire gli spazi contenuti nella colonna.
   * **[!UICONTROL Separatori]** (tipi di dati data, ora, numero intero e numero)*: specificare i caratteri da utilizzare come separatori.
   * **[!UICONTROL Consenti valori NULL]**: specificare come gestire i valori vuoti nella colonna.
   * **[!UICONTROL Errore durante l&#39;elaborazione]** (tipo di dati stringa): specificare il comportamento in caso di errori in una delle righe.
   * **[!UICONTROL Modifica del valore]**: questa opzione consente di mappare valori specifici con valori nuovi. Ad esempio, se la colonna contiene i valori “True”/“False”, puoi aggiungere una mappatura per sostituire automaticamente tali valori con i caratteri “0”/“1”.

+++

1. Nella sezione **Formattazione**, specifica la formattazione del file per garantire che i dati vengano importati correttamente.

### Definire il file target da caricare {#target}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_targetfile"
>title="File target per l’attività di caricamento file"
>abstract="Nella sezione **[!UICONTROL File target]**, specifica come recuperare il file da caricare sul server."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_nameofthefile"
>title="Nome del file"
>abstract="Specifica il nome del campo da caricare sul server. Fai clic sull’icona **[!UICONTROL Apri finestra di dialogo per personalizzazione]** per sfruttare l’editor di espressioni, incluse le variabili evento, per calcolare il nome del file."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_targetdb"
>title="Database di destinazione"
>abstract="Se si accede a un&#39;attività **[!UICONTROL Load file]** che è già stata configurata, è disponibile un&#39;ulteriore sezione del **[!UICONTROL database di destinazione]** se l&#39;attività è stata configurata per caricare il file in un database esterno."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_command"
>title="Comando Load File"
>abstract="Consentire un comando arbitrario per la pre-elaborazione è un problema di sicurezza, disabilita l’opzione di sicurezza XtkSecurity_Disable_Preproc per forzare l’uso di un elenco predefinito di comandi."

>[!CAUTION]
>
>Prima di caricare il file di destinazione, accertati che sia conforme alla formattazione del file di esempio. Eventuali discrepanze nel formato del file, nella struttura delle colonne o nel numero di colonne possono causare errori durante l’esecuzione di una campagna orchestrata.

Per definire il file di destinazione da caricare, effettua le seguenti operazioni:

1. Nella sezione **[!UICONTROL File di destinazione]**, specifica l&#39;azione da eseguire durante il recupero del file da caricare sul server.

   * **[!UICONTROL Carica file dal computer locale]**: seleziona il file da caricare dal computer.

   * **[!UICONTROL Specificato nella transizione]**: carica il file specificato nella transizione in entrata in arrivo da un&#39;attività precedente, ad esempio **[!UICONTROL Trasferisci file]**.

   * **[!UICONTROL Pre-elabora il file]**: carica il file specificato nella transizione precedente e applica un comando di pre-elaborazione, ad esempio **[!UICONTROL Decompressione]** o **[!UICONTROL Decrittografia]**.

   * **[!UICONTROL Calcolato]**: carica il file il cui nome è specificato nel campo **[!UICONTROL Nome file]**. Fai clic sull’icona **[!UICONTROL Apri finestra di dialogo per personalizzazione]** per sfruttare l’editor di espressioni, incluse le variabili evento, per calcolare il nome del file.

   ![](../assets/workflow-load-file-config.png)

   >[!NOTE]
   >
   >Se si accede a un&#39;attività **[!UICONTROL Load file]** che è già stata configurata, viene visualizzata un&#39;ulteriore sezione **[!UICONTROL Target database]** se l&#39;attività è stata configurata per caricare il file in un database esterno. Ti consente di specificare se desideri caricare il file sul server Campaign o sul database esterno.

### Opzioni aggiuntive {#options}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_rejectmgt"
>title="Rifiuta gestione per l’attività di caricamento file"
>abstract="La sezione **Rifiuta gestione** , specifica il comportamento dell’attività in caso di errori. Puoi definire il numero massimo di errori da consentire e attivare/disattivare l’opzione **[!UICONTROL Mantieni i valori rifiutati in un file]** per scaricare sul server un file contenente gli errori che si sono verificati durante l’importazione."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_delete"
>title="Elimina file dopo l’importazione"
>abstract="Attiva/disattiva **Elimina file dopo l’importazione** per eliminare il file originale dal server dopo averlo importato."


1. Nella sezione **Rifiuta gestione**, specifica il comportamento dell&#39;attività in caso di errori:

   * Nel campo **[!UICONTROL Numero di errori consentiti]**, specifica il numero massimo di errori autorizzati durante l&#39;elaborazione del file da caricare. Ad esempio, se il valore è impostato su &quot;20&quot;, l’esecuzione della campagna orchestrata avrà esito negativo se si verificano più di 20 errori durante il caricamento del file.

   * Per mantenere gli errori che si sono verificati durante il caricamento del file, attivare l&#39;opzione **[!UICONTROL Mantieni rifiuti in un file]** e specificare il nome desiderato per il file nel campo **[!UICONTROL File di rifiuto]**.

     Dopo aver attivato questa opzione, dopo l’attività viene aggiunta una transizione di output aggiuntiva denominata &quot;Complemento&quot;. Qualsiasi errore che si verificherà durante l&#39;importazione verrà memorizzato nel file specificato sul server.

1. Per eliminare il file caricato dal server dopo l&#39;esecuzione della campagna orchestrata, attiva l&#39;opzione **[!UICONTROL Elimina file dopo l&#39;importazione]**.

   ![](../assets/workflow-load-file-options.png)

1. Fai clic su **Conferma** una volta che le impostazioni sono corrette.

## Esempio {#load-example}

Un esempio di un file esterno utilizzato con l&#39;attività **Reconciliation** è disponibile in [questa sezione](reconciliation.md#reconciliation-example).
