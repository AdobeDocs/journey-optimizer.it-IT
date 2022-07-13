---
title: Migrazione all’authoring in linea di percorso
description: Scopri come eseguire la migrazione dei messaggi
exl-id: accdebba-5322-401e-8a40-3e1539e65a7e
source-git-commit: 3146071854a02650c6f1632839e3dcd913a46676
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 0%

---


# Panoramica sulla migrazione dell’authoring in linea{#inline-authoring}

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_before"
>title="Ulteriori informazioni sulla nuova funzione di authoring in linea"
>abstract="A partire dal 25 luglio 2022, i messaggi vengono creati direttamente da un Percorso. I messaggi esistenti vengono automaticamente migrati al nuovo modello. Dopo la migrazione saranno necessarie ulteriori azioni, se al momento utilizzi i messaggi all’interno dei tuoi percorsi."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Passaggi di migrazione"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_during"
>title="Scopri cosa sta succedendo"
>abstract="A partire dal 25 luglio 2022, i messaggi vengono creati direttamente da un Percorso. Migrazione dell&#39;ambiente in corso. Dopo la migrazione saranno necessarie ulteriori azioni."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Passaggi di migrazione"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_after"
>title="Scopri come eseguire la migrazione dei messaggi"
>abstract="A partire dal 25 luglio 2022, i messaggi vengono creati direttamente da un Percorso. I messaggi esistenti sono stati ora migrati al nuovo modello. In qualità di professionista del percorso, ora sono necessarie ulteriori azioni."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Passaggi di migrazione"

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Scopri come eseguire la migrazione dei messaggi"
>abstract="A partire dal 25 luglio 2022, il menu Messaggi scompare e i messaggi vengono creati direttamente da un Percorso. Per riutilizzare i messaggi legacy nei percorsi, è necessario salvarli come modelli."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/design/email-templates.html#save-as-template" text="Salvare i messaggi come modelli"

Adobe Journey Optimizer sta rilasciando una nuova funzione che migliora il modo in cui crei contenuti per i canali Journey Optimizer (e-mail, push, SMS). In qualità di professionista di Journey Optimizer, ora puoi creare e creare i messaggi direttamente da un percorso.

Questa funzione richiede una migrazione dei percorsi esistenti che utilizzano i messaggi. In questa pagina trovi le informazioni necessarie su questa modifica e i passaggi che ti sono necessari.

Per ulteriori informazioni su ruoli e responsabilità in qualità di professionista di Journey Optimizer, consulta questo [page](../start/path/marketer.md).

<!--
Here are the main changes in the interface:

* Messages are created direcly from journeys.
* The **Messages** entry in the left navigation menu has been removed. 
* There is no separate library of messages, the journey now centralizes all components.


-->

>[!VIDEO](https://video.tv.adobe.com/v/344698)


## Scelta chiave{#keys}

* **Sono interessato?**: sei interessato se crei messaggi dal **Messaggi** nel menu di navigazione a sinistra e utilizzali nei tuoi percorsi. Se utilizzi un sistema di terze parti (come Adobe Campaign), questa migrazione non ti interessa.

* **Modifiche al prodotto**: in GA (25 luglio), il contenuto del canale viene creato e gestito all’interno di ogni percorso. La **Messaggi** nel menu di navigazione a sinistra non è più disponibile ([ulteriori informazioni](../rn/inline-messages.md#change)). Verrà eseguita la migrazione per i percorsi esistenti.

* **Timeline**: la migrazione avviene per ogni regione di notte, attraverso [iterazioni](../rn/inline-messages.md#iterations).

   ![](assets/inline-migration-timeline.png)

* **Azioni necessarie**: viene eseguita una conversione automatica dei percorsi. Detto questo, abbiamo bisogno del vostro aiuto con alcuni passi. Ulteriori informazioni sui passaggi richiesti in questo [page](../rn/inline-messages-steps.md).

* **Obsolescenza**: dopo il 6 settembre, tutti i percorsi che utilizzano ancora messaggi legacy vengono interrotti e verranno eliminati in seguito.

## Vantaggi e modifiche ai prodotti{#change}

La visione di Adobe è quella di semplificare continuamente il prodotto per fornire flussi di utenti efficienti e ottimizzati. Questo nuovo modo di creare i messaggi semplifica il processo degli utenti.

Abbiamo progettato questo nuovo flusso di lavoro per centralizzare i contenuti in un’unica posizione, direttamente dove vengono utilizzati.

La creazione di contenuti viene ora eseguita direttamente all’interno del percorso. L&#39;immediato **vantaggi** ottieni:

* Creazione di percorsi più rapida utilizzando i canali Journey Optimizer in un unico flusso.
* Visualizzazione rapida dei contenuti passando ininterrottamente tra tutti i contenuti e-mail, push e SMS in un percorso.
* Flusso migliorato per le e-mail e il push utilizzando la personalizzazione contestuale dall’area di lavoro.
* Il reporting per percorso centralizza le informazioni dettagliate sul reporting per canale.

Qui sono **modifiche al prodotto** grazie a questa nuova funzione:

<table>
<tr>
<th>Prima della migrazione</th>
<th>Dopo la migrazione</th>
</tr>
<tr>
<td><img src="assets/inline-migration-before.png"><p>Prima, hai creato il messaggio da <strong>Messaggi</strong> menu. </p></td>
<td><img src="assets/inline-migration-after.png"><p>Ora, la <strong>Messaggi</strong> nel menu di navigazione a sinistra non è più disponibile. </p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before2.png"><p>Hai quindi creato un percorso, aggiunto un <strong>Messaggio</strong> e ha selezionato il messaggio creato in precedenza.</p></td>
<td><img src="assets/inline-migration-after2.png"><p>Ora puoi semplicemente aggiungere al tuo percorso l’attività di azione del canale desiderata (e-mail, SMS, push). Nell’attività , puoi configurare direttamente i parametri dei messaggi e accedere all’editor dei contenuti.</p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before3.png"><p>In precedenza, il reporting era accessibile sia a livello di messaggio che di percorso. È stato necessario spostarsi tra la scheda di esecuzione del messaggio e il rapporto del percorso.</p></td>
<td><img src="assets/inline-migration-after3.png"><p>Tutti i rapporti sono ora centralizzati a livello di percorso. Questo migliora la navigazione e l’esperienza utente. Se hai più e-mail in un percorso, puoi utilizzare la funzione <strong>Azione</strong> menu a discesa per visualizzare il rapporto correlato.
</p></td>
</tr>
</table>

In GA (25 luglio), questo nuovo flusso utente si applica a tutti i nuovi percorsi. La **Messaggi** nel menu di navigazione a sinistra non è più disponibile.

## Timeline di migrazione{#iterations}

È necessaria una migrazione per trasformare i percorsi esistenti utilizzando **Messaggi** in percorsi con azioni di authoring in linea. Viene eseguita una conversione automatica dei percorsi. Detto questo, abbiamo bisogno del vostro aiuto con alcuni passi.

La migrazione si verifica per ogni regione di notte, attraverso diverse iterazioni. Ecco la timeline della migrazione:

* 25 luglio 2022: GA - 1a iterazione
* 1 agosto 2022: 2a iterazione
* 5 settembre 2022: 3a iterazione
* 6 settembre 2022: deprecazione

Perché abbiamo bisogno di più iterazioni?

Durante un&#39;iterazione, passiamo attraverso ogni percorso e li migriamo quando possibile. Ci sono casi in cui non vogliamo eseguire la migrazione automatica: quando il percorso è live o chiuso (ovvero può ancora essere presente un profilo). In questi casi, ti chiediamo di eseguire un’azione e quindi l’iterazione successiva eseguirà la migrazione di questi percorsi che non è stato possibile migrare nell’iterazione precedente.

## Domande frequenti {#faq}

### Come sarò informato del cambiamento?{#inform}

Adobe comunica con te prima della prima iterazione.

Il cambiamento viene distribuito durante la notte, attraverso diverse iterazioni. Ulteriori informazioni su [iterazioni](../rn/inline-messages.md#inline-authoring).

Inoltre, le notifiche interne al prodotto vengono visualizzate sugli schermi dei Percorsi:

* Prima di modificare la distribuzione

   ![](assets/inline-migration-banner1.png)

* Durante un&#39;iterazione

   ![](assets/inline-migration-banner2.png)

* Dopo un’iterazione

   ![](assets/inline-migration-banner3.png)

   Dopo un&#39;iterazione, la **Stato del controllo** viene visualizzato il pulsante . Questo ti consente di visualizzare tutti i tuoi percorsi in formato JSON e il rispettivo stato di migrazione. Vedi questo [sezione](../rn/inline-messages.md#status).

* Quando il banner scompare, sei bravo ad andare. Non è richiesta alcuna altra azione da parte tua.

### Qual è il processo di migrazione?{#process}

La migrazione è completamente automatica per i percorsi che non sono live o chiusi. Non vogliamo avere un impatto sui percorsi live o chiusi per evitare qualsiasi impatto sulla produzione. Ti chiediamo di pubblicare la nuova versione creata per te.

Tutte le sandbox di un ORG cliente vengono elaborate simultaneamente. Durante la distribuzione delle modifiche, vengono eseguite le azioni seguenti:

**QUALSIASI percorso che non utilizza i messaggi**

Questi non sono influenzati dal cambiamento. La migrazione ha come target solo i percorsi che utilizzano i messaggi. Tuttavia, potrai comunque accedere ai messaggi non utilizzati in un percorso tramite il seguente URL: https://experience.adobe.com/#/@[ORO]/sname:[SANDBOX]/percorsi-optimizer/messages/

**BOZZA percorsi utilizzando almeno un messaggio**

Le versioni bozze dei messaggi vengono modificate durante la migrazione. Non fanno più riferimento a un messaggio. La **Messaggio** le attività vengono sostituite con le attività di azione del canale appropriate. Ognuno di essi include i parametri e il contenuto del canale.

Come al solito, testa il percorso di bozza prima di pubblicarlo.

**PERCORSI LIVE che utilizzano almeno un messaggio**

La versione live di un percorso continua a funzionare per evitare qualsiasi impatto sulla produzione.

Durante la migrazione viene creata una nuova versione bozza di questo percorso. Questa nuova versione bozza è una copia della tua versione live ma i messaggi vengono sostituiti con azioni del canale in linea create. Ciascuna attività di azione del canale include i parametri e il contenuto del canale. Il contenuto non viene perso. Il reporting non viene perso.

Prevediamo che rivedi questa versione bozza, la sottoponga a test e la pubblichi in modo che diventi la versione live.

**PERCORSI completati o ARRESTATI che utilizzano almeno un messaggio**

Anche questi percorsi vengono migrati.

Nel rapporto sul percorso, i rapporti sono ora più ricchi e includono il livello di informazioni precedentemente disponibili nel rapporto sui messaggi.

**Percorsi chiusi che utilizzano almeno un messaggio**

La versione chiusa di un percorso continua a funzionare per qualsiasi profilo interno, per evitare qualsiasi impatto sulla produzione.

Dopo 30 giorni, i percorsi chiusi vengono automaticamente spostati allo stato &quot;Completato&quot;. Saranno presi in considerazione nella prossima iterazione, quando avranno finito.

**Percorsi multicanale**

Queste non vengono migrate. Devi ricrearli.

### Quali sono gli elementi delle mie azioni come cliente?{#actions}

Viene eseguita una conversione automatica dei percorsi, ma sono necessari alcuni passaggi. Ulteriori informazioni sui passaggi richiesti in questo [page](../rn/inline-messages-steps.md).

<!--

The process timeline is indicated in a blue banner on the Journeys screen. See this [section](../rn/inline-messages.md#inform). 

**Before migration**

* Check the date indicated in the banner. 
* Stop non-critical journeys, on development, stage and production environments.
* If you have draft messages that you want to keep using, add them to a journey so they are migrated.

**During migration**

* Migration occurs at night-time
* Do not to create, edit or delete journeys.

**After migration**

* After each iteration, click the **Check status** button in the top banner. This page lists all journeys and their migration status. See this [section](../rn/inline-messages.md#status). 

* For each live journey, a new version is created. Review the new version, test it and publish it. 

* The **Messages** menu, in the left navigation is no longer available. You need to use the new in-line message feature. See this [section](../rn/inline-messages.md#change). 

* If you need to access a specific message which was not used in a journey, you can use this URL and save the content as a template: https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/journey-optimizer/messages/

## How can I check the migration status?{#status}

Click the **Check status** button in the top banner. The following page is displayed.

![](assets/inline-migration-log.png)

The status report is at sandbox level. This report includes several useful sections:

**migrationStatus**

This section displays the migration information since the first iteration. Numbers are incremented after each iteration.

* MIGRATED: number of draft journeys migrated successfully.
* NEW_VERSION_CREATED: number of live journeys migrated. For each live journey, a new draft version is created: you must test and publish this version.
* ERROR: number of draft journeys not migrated because of a failure. You need to re-create them.
* ERROR_ON_NEW_VERSION_CREATION: number of live journeys not migrated because of a failure. new draft journey versions not migrated because of a failure. You need to re-create them.

**eligibilityStatus**

This section lists the remaining items after the last iteration:

* toMigrate: number of draft journeys that need to be migrated.
* createNewVersion: number of live journeys to migrate.
* noMigration_live: number of live journeys that do not need to be migrated
* noMigration: number of draft journeys that do not need to be migrated.

The **details** section gives, for each of the above indicators, the list of related journeys.

-->

### Come posso controllare lo stato della migrazione?{#status}

Fai clic sul pulsante **Stato del controllo** nel banner superiore. Viene visualizzata la pagina seguente.

![](assets/inline-migration-log.png)

Il rapporto sullo stato si trova a livello di sandbox. Questo rapporto include diverse utili sezioni:

**migrationStatus**

In questa sezione vengono visualizzate le informazioni sulla migrazione dalla prima iterazione. I numeri vengono incrementati dopo ogni iterazione.

* MIGRAZIONE: migrazione del numero di percorsi di bozza, completati e interrotti completata.
* NEW_VERSION_CREATED: migrazione del numero di percorsi live. Per ogni percorso live viene creata una nuova versione di bozza: devi testare e pubblicare questa versione.
* ERRORE: numero di percorsi bozza, completati e interrotti non migrati a causa di un errore. Devi ricrearli.
* ERROR_ON_NEW_VERSION_CREATION: numero di percorsi live non migrati a causa di un errore. le nuove versioni di percorso bozza non sono state migrate a causa di un errore. Non sono state create nuove versioni di bozza per tali versioni. È necessario ricrearli manualmente.

**allowStatus**

In questa sezione sono elencati gli elementi rimanenti dopo l’ultima iterazione:

* toMigrate: numero di percorsi di bozza, completati e interrotti da migrare.
* createNewVersion: numero di percorsi live da migrare.
* noMigration_live: numero di percorsi live che non è necessario migrare. Qui sono elencati anche percorsi chiusi.
* noMigration: numero di percorsi per i quali non è necessario eseguire la migrazione.

La **dettagli** la sezione fornisce, per ciascuna delle sezioni di cui sopra, l&#39;elenco dei percorsi correlati.

### Questa modifica causerà un’interruzione del servizio?{#interruption}

Non ci sarà alcuna interruzione del servizio.

* Percorsi live: senza impatto, continuano a correre.
* Nei percorsi creati: durante la migrazione (di notte), consigliamo vivamente di non creare, modificare o eliminare percorsi.

### Ci sarà perdita di dati? {#data}

Non ci saranno perdite di dati e nessun impatto sui percorsi live. Potrai pubblicare versioni di percorso aggiornate.

### Si verificherà una perdita di funzionalità?{#functionality}

La modalità di creazione dei messaggi verrà modificata. Non si verificherà alcuna perdita di funzionalità.

### Sarà possibile accedere all’ambiente durante il processo di migrazione?

La migrazione avviene di notte. Potrai utilizzare il prodotto. Ma non creare, modificare o eliminare percorsi.

### I messaggi continueranno a essere inviati?

Sì, i percorsi in diretta continuano a correre.

### Come posso sapere che la migrazione è completa?

La migrazione è completa quando il banner scompare. Vedi questo [sezione](../rn/inline-messages.md#inform).

<!--
* Improved authoring flow and navigation
* Personalization: improved contextual personalization flow
* Reporting: the message execution screen will no longer exist. Reporting is centralized in journeys.
* You will still be able to update content in a live journey.
->>
