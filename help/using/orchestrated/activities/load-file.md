---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Load file
description: Scopri come utilizzare l’attività Load file per indirizzare un pubblico di una campagna orchestrata da un file CSV o TXT senza acquisire il file in Adobe Experience Platform
exl-id: a7c3e891-4f2d-4b8e-9c1a-6e8f0d3b2a41
version: Campaign Orchestration
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 9c2ed338c676a02055802ce8ea956b5b698f3d7c
workflow-type: tm+mt
source-wordcount: 1258
ht-degree: 2%

---

# Caricare file {#load-file}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_load_file"
>title="Attività di caricamento file"
>abstract="L&#39;attività **Load file** è un&#39;attività **Data Management**. Utilizzalo per lavorare con profili e dati memorizzati in un file esterno nell’area di lavoro della campagna orchestrata e definire il pubblico della campagna. I dati del file vengono utilizzati al momento dell’esecuzione e non vengono mantenuti come set di dati di Adobe Experience Platform."

L&#39;attività **[!UICONTROL Load file]** è un&#39;attività **[!UICONTROL Data Management]**. Utilizzala per lavorare con profili e dati memorizzati in un file esterno. Supporta il targeting **basato su file** nelle campagne orchestrate quando l&#39;elenco dei destinatari proviene da un sistema esterno (ad esempio, un&#39;esportazione CRM o un file partner) e desideri eseguire una campagna senza prima creare una pipeline di acquisizione Adobe Experience Platform completa.

>[!AVAILABILITY]
>
>L&#39;attività **Load file** è disponibile in **Disponibilità limitata** per un set di organizzazioni. Per richiedere l’accesso, contatta il tuo rappresentante Adobe. Per le fasi di disponibilità, vedere [Ciclo di rilascio di Journey Optimizer](../../rn/releases.md).
>
>L&#39;attività non è attualmente disponibile per l&#39;utilizzo con **Healthcare Shield**.

## Guardrail e limitazioni {#limitations}

All’attività Load file si applicano le seguenti limitazioni:

* Puoi caricare fino a 50 MB per file.
* Sono supportati solo i file CSV e TXT a struttura piatta.
* I dati caricati vengono utilizzati durante l’esecuzione della campagna e non vengono memorizzati come set di dati di Adobe Experience Platform.
* Ogni riga deve corrispondere a un destinatario esistente per la dimensione di targeting selezionata. L’attività Load file non crea nuovi profili dal file.

Per i limiti sulle attività dei canali e delle aree di lavoro, vedere [Guardrail e limitazioni](../guardrails.md#activities-limitations).

## Configurare l’attività Load file {#load-file-configuration}

Configura l’attività in due parti: definisci la struttura del file prevista con un file di esempio, quindi specifica il file da caricare durante l’esecuzione della campagna.

1. Aggiungi un&#39;attività **[!UICONTROL Load file]** all&#39;area di lavoro della campagna orchestrata.

   ![](../assets/load-file.png)

1. Immetti un **[!UICONTROL Etichetta]** per l&#39;attività.

### Definire il file di esempio {#sample-file}

Utilizzare un file di esempio per configurare **[!UICONTROL Colonne]** e **[!UICONTROL Formattazione]**. I dati di esempio non vengono importati come pubblico della campagna.

1. Nella sezione **[!UICONTROL File di esempio]** selezionare il file locale che definisce la struttura prevista.

   >[!NOTE]
   >
   > Il file di esempio viene utilizzato solo per configurare colonne e formattazione; i relativi dati non vengono importati come pubblico della campagna. Il formato deve corrispondere ai file che verranno caricati durante l’esecuzione della campagna.

1. Nell&#39;elenco a discesa **[!UICONTROL Tipo file]**, specificare se il file utilizza **colonne delimitate** o **colonne a larghezza fissa**.

   ![](../assets/load-file-sample.png)

1. Nella sezione **[!UICONTROL Colonne]**, espandi ogni colonna e configurane le proprietà.

   ![](../assets/load-file-sample-columns.png)

   Dopo aver selezionato un tipo di dati **[!UICONTROL Tipo di dati]**, vengono visualizzate ulteriori opzioni per tale tipo. Espandi le sezioni seguenti per i parametri comuni a tutte le colonne e per le opzioni specifiche del tipo.

   +++Parametri comuni per le colonne

   * **[!UICONTROL Ignora colonna]** - Escludi la colonna dall&#39;importazione se selezionata.
   * **[!UICONTROL Etichetta]** — Nome visualizzato per la colonna (ad esempio, `email`).
   * **[!UICONTROL Nome interno]** — Nome di sistema per la colonna, derivato dall&#39;intestazione del file (sola lettura).
   * **[!UICONTROL Tipo di dati]** — Tipo di dati nella colonna.
   * **[!UICONTROL Consenti valori NULL]** - Specifica come gestire i valori vuoti nella colonna:

      * **[!UICONTROL Impostazione predefinita di Adobe Campaign]** - Genera un errore solo per i campi numerici. In caso contrario, inserisce un valore NULL.
      * **[!UICONTROL È consentito un valore vuoto]** — autorizza valori vuoti. Pertanto, viene inserito il valore NULL.
      * **[!UICONTROL Sempre popolato]** — Genera un errore se un valore è vuoto.

   * **[!UICONTROL Errore durante l&#39;elaborazione]** — definisce il comportamento in caso di errore nella colonna:

      * **[!UICONTROL Ignora il valore]**. Il valore viene ignorato.
      * **[!UICONTROL Rifiuta la riga]** — L&#39;intera riga non viene elaborata.
      * **[!UICONTROL Utilizzare un valore predefinito in caso di errore]** — Sostituisce il valore che causa l&#39;errore con un valore predefinito, definito nel campo **[!UICONTROL Valore predefinito]**.
      * **[!UICONTROL Utilizzare un valore predefinito se il valore non viene rimappato]** — Sostituisce il valore che causa l&#39;errore con un valore predefinito, definito nel campo **[!UICONTROL Valore predefinito]**, a meno che non sia stata definita una mappatura per il valore errato.
      * **[!UICONTROL Rifiuta la riga quando non è presente alcun valore di mapping]**. L&#39;intera riga non viene elaborata a meno che non sia stata definita una mappatura per il valore errato.

   * **[!UICONTROL Valore predefinito]** — Valore predefinito da utilizzare quando **[!UICONTROL Errore di elaborazione]** è impostato per l&#39;utilizzo di un valore predefinito.
   * **[!UICONTROL Nuova mappatura valori]** - Mappa valori specifici a nuovi valori. Fai clic su **[!UICONTROL Aggiungi mapping]** per definire ogni mapping (ad esempio, sostituisci `True`/`False` con `1`/`0`).

   +++

   +++Parametri delle colonne stringa

   * **[!UICONTROL Larghezza]** — Numero massimo di caratteri.
   * **[!UICONTROL Trasformazione dati]** - Trasformazione di maiuscole e minuscole applicata ai valori stringa (ad esempio, nessuna o maiuscole/minuscole).
   * **[!UICONTROL Gestione degli spazi vuoti]**: come gestire gli spazi iniziali o finali nei valori stringa.

   +++

   +++Parametri per colonne a numero intero e a numero mobile

   * **[!UICONTROL Formato]** — definisce la modalità di lettura dei valori numerici nel file:

      * **[!UICONTROL Altro]** — Definisci il **[!UICONTROL Separatore delle migliaia]** e il **[!UICONTROL Separatore decimale]** nella sezione **[!UICONTROL Separatori]**.
      * **[!UICONTROL 1.000.00]** — Virgola come separatore delle migliaia e punto come separatore decimale.
      * **[!UICONTROL 1 000,00]** — Spazio come separatore delle migliaia e virgola come separatore decimale.

   * **[!UICONTROL Separatori]** (quando **[!UICONTROL Formato]** è **[!UICONTROL Altro]**):

      * **[!UICONTROL Separatore delle migliaia]** - Carattere che raggruppa le migliaia in valori numerici (lasciare vuoto se non utilizzato).
      * **[!UICONTROL Separatore decimale]** - Carattere utilizzato per la parte decimale dei valori numerici (ad esempio, `,` o `.`).

   +++

   +++Parametri delle colonne data e ora

   Le opzioni dipendono dal tipo di dati **[!UICONTROL Tipo di dati]**: **Data**, **Ora** o **Data e ora**.

   **Data**

   * **[!UICONTROL Formato data]** — Pattern che corrisponde alla modalità di visualizzazione delle date nel file (ad esempio, `yyyy/mm/dd`).
   * **[!UICONTROL Separatori]**:

      * **[!UICONTROL Anno, mese, giorno]** - Carattere tra i componenti anno, mese e giorno (ad esempio, `/`).

   **Ora**

   * **[!UICONTROL Formato ora]** — Schema che corrisponde al modo in cui le ore vengono visualizzate nel file (ad esempio, `13:30` per ore e minuti di 24 ore).
   * **[!UICONTROL Separatori]**:

      * **[!UICONTROL Ora, minuto, secondo]** — Carattere tra i componenti ora, minuto e secondo (ad esempio, `:`).

   **Data e ora**

   * **[!UICONTROL Formato data]** — Pattern che corrisponde alla modalità di visualizzazione della porzione di data nel file.
   * **[!UICONTROL Formato ora]** — Schema che corrisponde al modo in cui la porzione di tempo viene visualizzata nel file.
   * **[!UICONTROL Separatori]** — Caratteri tra i componenti data e ora.

   +++

1. Nella sezione **[!UICONTROL Formattazione]**, specifica la struttura del file in modo che le righe e le colonne vengano lette correttamente durante l&#39;esecuzione della campagna. Il file di destinazione deve utilizzare la stessa formattazione del file di esempio.

   ![](../assets/load-file-sample-formatting.png)

   * **[!UICONTROL Utilizza la prima riga come intestazione di colonna]**. Se selezionata, la prima riga del file viene considerata come nomi di colonna. Questa opzione è in genere abilitata quando configuri l’esempio da un file che include una riga di intestazione.
   * **[!UICONTROL Utilizzare un numero di riga come identificatore]**: se selezionata, ogni riga viene identificata dal relativo numero di riga nel file.
   * **[!UICONTROL I record si estendono su più righe]**. Se selezionata, un singolo record può estendersi su più righe nel file, ad esempio quando i campi contengono interruzioni di riga.
   * **[!UICONTROL Righe da ignorare]** — Numero di righe da ignorare all&#39;inizio del file prima che i dati vengano letti (ad esempio, righe di commento o metadati).
   * **[!UICONTROL Fuso orario]** — Fuso orario applicato quando vengono importati i valori di data e ora.
   * **[!UICONTROL Codifica]** - Codifica caratteri del file. Seleziona la codifica corrispondente al file di origine.
   * **[!UICONTROL Delimitatore stringa]** — Carattere utilizzato per racchiudere i valori stringa nel file.
   * **[!UICONTROL Separatore colonne]** - Carattere che separa le colonne in un file delimitato.

1. Fai clic su **[!UICONTROL Conferma]** per convalidare la configurazione del file di esempio.

### Definire il file di destinazione {#target-file}

Specifica il file da caricare all’esecuzione della campagna e come ogni riga corrisponde ai destinatari esistenti.

1. Nella sezione **[!UICONTROL File di destinazione]**, seleziona il file CSV o TXT contenente di destinazione.

   ![](../assets/load-file-target.png)

   >[!CAUTION]
   >
   > Assicurati che il file di destinazione segua lo stesso formato, la stessa struttura delle colonne e lo stesso numero di colonne del file di esempio.

1. Nella sezione **[!UICONTROL Rifiuta gestione]**, definisci il comportamento dell&#39;attività quando si verificano errori durante l&#39;elaborazione del file:

   * **[!UICONTROL Numero di errori consentito]** — Numero massimo di errori consentiti prima che l&#39;attività non riesca.
   * **[!UICONTROL Mantieni i rifiuti in un file]** — Se abilitata, le righe che non possono essere caricate vengono scritte in un file rifiutato sul server per la revisione dopo l&#39;esecuzione.

1. Facoltativamente, abilitare **[!UICONTROL Elimina file dopo l&#39;importazione]** per rimuovere il file caricato dal server dopo l&#39;esecuzione della campagna.

Dopo che **[!UICONTROL il file di caricamento]** ha risolto il pubblico,n connette la transizione in uscita alle attività a valle. [Scopri come orchestrare le attività della campagna](../orchestrate-activities.md)
