---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Incremental query
description: Scopri come utilizzare l’attività Incremental query in Adobe Journey Optimizer per eseguire il targeting solo dei nuovi profili nelle campagne orchestrate.
feature: Campaigns
topic: Building campaigns
role: User
level: Intermediate
version: Campaign Orchestration
feature_v2: 
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 518
ht-degree: 22%

---


# Query incrementale {#incremental-query}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery"
>title="Query incrementale"
>abstract="La query incrementale è un’attività di targeting che esegue una query sul database ogni volta che viene eseguita la campagna orchestrata. Restituisce solo i nuovi record ed esclude chiunque sia già incluso in un’esecuzione precedente, in modo da evitare di eseguire nuovamente il targeting delle stesse persone o di esportare nuovamente le stesse righe."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery_processeddata"
>title="Dati elaborati"
>abstract="In Dati elaborati scegliere la modalità di esclusione dei record dalle esecuzioni precedenti. Con l’opzione Usa campo data, l’attività utilizza un campo data selezionato invece di tenere traccia dei singoli ID e ogni esecuzione restituisce solo righe la cui data è successiva all’ultima esecuzione."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery_history"
>title="Cronologia in giorni"
>abstract="Questa impostazione controlla per quanto tempo l’elenco viene mantenuto. Un valore pari a 0 indica la conservazione a tempo indeterminato; nessun record viene rimosso."

L&#39;attività **[!UICONTROL Incremental query]** è un&#39;attività **[!UICONTROL Targeting]** che esegue una query di database ogni volta che viene eseguita la campagna orchestrata. La parte importante è che produce solo **nuovi** record. Viene escluso chiunque sia già stato selezionato in un’esecuzione precedente, pertanto eviti di eseguire nuovamente il targeting delle stesse persone o di esportare nuovamente le stesse righe.

Utilizzalo quando la campagna può essere eseguita più volte, ad esempio quando pianifichi la campagna, ad esempio settimanalmente o quando viene attivata da un segnale o da un’API esterna. Ogni esecuzione esegue il targeting solo dei record che non sono stati restituiti in un&#39;esecuzione precedente, in modo da evitare duplicati.

Usi tipici:

* **Messaggi e pubblico**: richiama solo i nuovi abbonamenti, i nuovi acquirenti o altri segmenti &quot;nuovi dall&#39;ultima esecuzione&quot; nel passaggio successivo (ad esempio e-mail, SMS).
* **Esportazioni in corso**: invia solo righe nuove o aggiornate ai file per gli strumenti di reporting o BI, senza duplicare ciò che hai già esportato.

Quando un&#39;esecuzione non restituisce righe, la campagna orchestrata si interrompe alla **query incrementale**. Le attività dopo la query incrementale vengono eseguite solo se sono presenti dati, quando la campagna viene eseguita di nuovo.

## Configurare l’attività Incremental query {#incremental-query-configuration}

Imposta la dimensione di targeting, crea la query e scegli in che modo l’attività decide quali record escludere dalle esecuzioni future.

1. Rilascia un&#39;attività **[!UICONTROL Incremental query]** nella campagna orchestrata.

1. In **[!UICONTROL Pubblico]**, scegli la **[!UICONTROL dimensione di targeting]**, ad esempio destinatari, abbonati e fai clic su **[!UICONTROL Continua]**. Ulteriori informazioni sulle [dimensioni di targeting](../target-dimension.md).

   ![](../assets/incremental-query.png)

1. Fai clic su **[!UICONTROL Aggiungi condizione]** per definire la query. [Scopri come utilizzare il generatore di regole](../orchestrated-rule-builder.md).

   ![](../assets/incremental-query-2.png)

1. In **[!UICONTROL Dati elaborati]**, scegli il **[!UICONTROL Percorso del campo data]**. L&#39;attributo deve utilizzare il formato **Data e ora**. Ogni esecuzione restituisce solo righe la cui data è successiva all’ultima esecuzione.

   ![Configurazione attività query incrementale nell&#39;area di lavoro della campagna orchestrata](../assets/incremental-query-3.png)

<!--
   * **[!UICONTROL Exclude results of previous execution]**: The activity maintains a list of records returned in prior runs. Each run excludes those records and returns only new ones. **[!UICONTROL History in days]** controls the retention period for that list. 0 indicates indefinite retention, no records are removed.

   >[!IMPORTANT]
   >
   >This mode stores the primary key of each processed record. Personally identifiable information (PII) must not be used as the primary key.

-->

## Esempio {#incremental-query-example}

L’esempio seguente invia un’e-mail di benvenuto ai profili che sono appena diventati membri Gold. È possibile pianificare l’esecuzione della campagna settimanalmente, ogni lunedì. Ogni esecuzione esegue il targeting solo dei profili idonei per l’iscrizione Gold dall’esecuzione precedente, in modo che ogni destinatario riceva l’e-mail di benvenuto una volta.

* **[!UICONTROL Incremental query]**: seleziona i membri gold. Prima esecuzione: tutti i membri correnti dell&#39;oro. Esecuzioni successive: solo profili che sono diventati membri Gold dall’esecuzione precedente.
* **[!UICONTROL Email delivery]**: invia l&#39;e-mail di benvenuto ai profili generati dalla query.

![Configurazione attività query incrementale nell&#39;area di lavoro della campagna orchestrata](../assets/incremental-query-example.png)

