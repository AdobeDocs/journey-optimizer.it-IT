---
title: Copia un percorso in un altro sandoto
description: Scopri come copiare un percorso in un altro sandox
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 6c9e4920f57a7f52cf52da706f309ef3a9f8f5fc
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 0%

---

# Copiare un percorso in un’altra sandbox {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copiare un percorso in un’altra sandbox"
>abstract="Journey Optimizer consente di copiare un intero percorso da una sandbox all’altra. Ad esempio, puoi copiare un percorso dall’ambiente sandbox di Stage alla sandbox di Produzione. Oltre al Percorso stesso, Journey Optimizer copia anche la maggior parte degli oggetti da cui dipende il percorso."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Dettagli della sandbox"
>abstract="Seleziona la sandbox di destinazione in cui desideri copiare il percorso. Sono disponibili solo le sandbox all’interno dell’organizzazione IMS."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Dettagli oggetto"
>abstract="Questo è il percorso che state per copiare."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Oggetti dipendenti"
>abstract="Elenco degli oggetti associati utilizzati nel percorso. Questo elenco visualizza il nome, il tipo di oggetto e l&#39;ID Journey Optimizer interno."

Journey Optimizer consente di copiare un intero percorso da una sandbox all’altra. Ad esempio, puoi copiare un percorso dall’ambiente sandbox di Stage alla sandbox di Produzione. Oltre al percorso stesso, Journey Optimizer copia anche la maggior parte degli oggetti da cui dipende il percorso: messaggi, segmenti, predefiniti, schemi, eventi e azioni. Fai riferimento a [limitazioni](../event/about-events.md)

>[!CAUTION]
>
>Non garantiamo che tutti gli elementi collegati vengano copiati nella sandbox di destinazione. Si consiglia vivamente di eseguire un controllo approfondito prima di pubblicare il percorso. Questo ti consentirà di identificare qualsiasi potenziale oggetto mancante.

Gli oggetti copiati nella sandbox di destinazione sono univoci e non sussiste il rischio di sovrascrittura degli elementi esistenti. Sia il percorso che tutti i messaggi all&#39;interno del percorso vengono portati in modalità bozza. Ciò ti consente di eseguire una convalida approfondita prima della pubblicazione sulla sandbox di destinazione. Il processo di copia copia solo sui metadati relativi al percorso e agli oggetti contenuti in quel Percorso. Nessun dato di profilo o set di dati viene copiato come parte di questo processo.

Per copiare un percorso in un’altra sandbox, effettua le seguenti operazioni:

1. Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Journeys]**. Viene visualizzato l’elenco dei percorsi.

2. Cerca il percorso da copiare, fai clic sul pulsante **Altre azioni** (i tre punti accanto al nome del percorso) e fai clic su **Copia in sandbox**.

   ![](assets/copy-sandbox1.png)

   La **Copia in sandbox** viene visualizzata la schermata .

   ![](assets/copy-sandbox2.png)

3. Seleziona la **Sandbox di Target** dal campo a discesa . Sono disponibili solo le sandbox all’interno dell’organizzazione IMS.

4. Consulta la sezione **Oggetti dipendenti** sezione . Elenco degli oggetti associati utilizzati nel percorso. Questo elenco visualizza il nome, il tipo di oggetto e l&#39;ID Journey Optimizer interno.

5. Fai clic sul pulsante **Copia** , nell’angolo in alto a destra, per iniziare a copiare il percorso nella sandbox di destinazione.

   ![](assets/copy-sandbox3.png)

   Viene avviato il processo di copia e viene visualizzato l’avanzamento di ogni singolo oggetto. Il processo di copia varia in base alla complessità del percorso e al numero di oggetti da copiare. Se si verifica un errore, viene visualizzato un messaggio per l’oggetto correlato.

   ![](assets/copy-sandbox4.png)

6. Una volta completata la copia, fai clic su **Chiudi**.

7. Accedi alla sandbox di destinazione ed esegui un controllo completo di tutti gli oggetti copiati.

## Copia del processo e delle limitazioni {#limitations}

Non garantiamo che tutti gli elementi collegati vengano copiati nella sandbox di destinazione. Ti consigliamo vivamente di eseguire un controllo approfondito. Identifica eventuali oggetti mancanti e creali manualmente prima di pubblicare il percorso.

Vengono copiati i seguenti oggetti:

* Segmento

   Un segmento può essere copiato solo una volta da una sandbox all’altra. Una volta copiato, un segmento non è modificabile nella sandbox di destinazione.

* Schema

   Gli schemi utilizzati in questo percorso vengono copiati.

* Messaggio

   I messaggi fisici utilizzati nel percorso (e-mail o messaggi push). I campi utilizzati per la personalizzazione nel messaggio non vengono controllati per verificarne la completezza. I blocchi di contenuto non vengono copiati.

* Percorso - dettagli area di lavoro

   La rappresentazione del percorso sull’area di lavoro, compresi gli oggetti nel percorso quali condizioni, azioni, eventi, segmenti di lettura, ecc. L’attività Jump è esclusa dalla copia.

* Evento

   Gli eventi e i dettagli dell&#39;evento utilizzati nel percorso vengono copiati.

* Azione

   Le azioni e i dettagli delle azioni utilizzati nel percorso vengono copiati.

I predefiniti non vengono copiati. Il sistema seleziona automaticamente la corrispondenza più vicina possibile sulla sandbox di destinazione, in base al tipo di messaggio e al nome del predefinito. Se non sono presenti predefiniti nella sandbox di destinazione, la copia preimpostata non riuscirà. Questo significa che anche la copia del messaggio avrà esito negativo, perché un messaggio richiede che sia disponibile un predefinito per la configurazione. In questo caso è necessario creare almeno un predefinito, affinché il canale giusto del messaggio funzioni correttamente.

Per gli schemi, i criteri di unione e i segmenti, la seconda volta che questi oggetti tentano di essere copiati, viene fatto riferimento solo a essi. Saranno trattati come oggetti già esistenti e verranno copiati di nuovo. Ciò significa che questi oggetti possono essere copiati una sola volta.

Si verifica un ritardo di cinque minuti prima che Adobe Journey Optimizer possa fare riferimento a Schemi, Criteri di unione e Segmenti senza che venga visualizzato un errore nell’area di lavoro. Attendi cinque minuti e questi riferimenti saranno disponibili.

