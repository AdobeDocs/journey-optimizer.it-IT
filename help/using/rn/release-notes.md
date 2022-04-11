---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 88b9dbd690a4dc987ee0bfe31e2d8b38a39c3f43
workflow-type: tm+mt
source-wordcount: '2938'
ht-degree: 99%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevi gli ultimi aggiornamenti dei prodotti, storie entusiasmanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Versione di marzo 2022 {#march-2022-release}

### Miglioramenti

**Percorsi**

* Per evitare di includere campi non necessari nello schema di profilo unificato, lo schema Evento delle fasi del percorso non è più abilitato per i profili per impostazione predefinita. Se necessario, puoi attivarlo. [Ulteriori informazioni](../reports/sharing-overview.md)
* I nuovi eventi delle fasi relativi ai processi di esportazione vengono ora inviati da Journey Optimizer a Adobe Experience Platform. Nella documentazione sono stati aggiunti esempi di query. [Ulteriori informazioni](../reports/query-examples.md)

**Gestione delle decisioni**

* Ora puoi specificare se il limite di offerta viene applicato a tutti gli utenti o a un profilo specifico e a tutti i posizionamenti o per posizionamento. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)
* L’API Batch Decisioning consente alle organizzazioni di utilizzare la funzionalità Offer Decisioning decisioning per tutti i profili in un dato segmento in una chiamata. Il contenuto dell’offerta per ogni profilo del segmento viene inserito in un set di dati AEP dove è disponibile per flussi di lavoro batch personalizzati. [Ulteriori informazioni](../offers/api-reference/batch-api/deliver-offers-batch.md)

**Amministrazione**

* Ora puoi abilitare/disabilitare il collegamento di annullamento dell’iscrizione nella/dalla intestazione delle e-mail a livello di predefinito del messaggio e impostare un URL di annullamento dell’iscrizione personalizzato a livello di messaggio. [Ulteriori informazioni](../configuration/message-presets.md#list-unsubscribe)
* L’elenco Consentiti ora può essere abilitato e disabilitato tramite l’interfaccia [!DNL Journey Optimizer] sulle sandbox di produzione e di non produzione. [Ulteriori informazioni](../reports/allow-list.md#enable-allow-list)

**Personalizzazione**

* Ora puoi salvare più di 40 espressioni di personalizzazione nella libreria. [Ulteriori informazioni](../personalization/personalization-library.md)

## Versione di febbraio 2022 {#feb-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Pagine di destinazione di iscrizione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare e progettare pagine di destinazione in Journey Optimizer e indirizzare gli utenti a moduli online in cui possono acconsentire o rinunciare alla ricezione delle comunicazioni o iscriversi a un servizio specifico, ad esempio una newsletter.</p>
<p>Per ulteriori informazioni, consulta la <a href="../landing-pages/create-lp.md">documentazione dettagliata</a> e alcuni <a href="../landing-pages/lp-use-cases.md">esempi di casi d’uso</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuova libreria di espressioni di personalizzazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fornisce ora una libreria in cui è possibile accedere a espressioni di personalizzazione predefinite. Queste espressioni sono configurate dagli utenti amministratore.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/personalization-library.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Trasmettere le informazioni per tenere traccia dei messaggi con i parametri di tracciamento UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nel contenuto del messaggio di Journey Optimizer, ora puoi aggiungere parametri UTM ai collegamenti: possono fornire dati aggiuntivi su quel collegamento e aiutarti a identificare dove e perché una persona ha fatto clic sul collegamento.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/message-presets.md#configure-email-settings">documentazione dettagliata</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Per ottimizzare le prestazioni, tutti i percorsi in modalità di test che non sono stati attivati per una settimana torneranno allo stato Bozza. [Ulteriori informazioni](../building-journeys/testing-the-journey.md#important_notes)
* L’integrazione tra Journey Optimizer e Adobe Campaign Classic è stata ottimizzata per migliorarne le prestazioni. La configurazione predefinita del limite è stata modificata in 4000 chiamate/5 minuti.	[Ulteriori informazioni](../action/acc-action.md#important-notes)

**Generazione rapporti**

* È ora possibile filtrare le consegne in base al loro stato:
   * Dall’elenco Esecuzione messaggi, ora puoi escludere le bozze dall’elenco delle consegne.
   * Dai rapporti Live/Global puoi scegliere di escludere gli eventi di test.

* Ora puoi accedere ai rapporti relativi ai dati di ottimizzazione del tempo di invio: il numero di persone che hanno ricevuto messaggi immediatamente e il numero di persone a cui il messaggio è stato inviato con un&#39;ottimizzazione di 1 ora, 2 ore ecc.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestione delle decisioni**

* Le classificazioni e la classificazione IA sono ora raggruppate in un’unica scheda.

## Versione di gennaio 2022 {#january-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Percorsi: ottimizzare l’incremento graduale dell’IP con le condizioni per un limite dei profili</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durante la configurazione di un’attività <strong>Condizione</strong> in un percorso, ora puoi definire un limite di profili. Questo nuovo tipo di condizione consente di impostare un numero massimo di profili per un percorso. Una volta raggiunto tale limite, i profili partecipanti seguono un percorso alternativo. Questo consente di incrementare gradualmente il volume delle consegne (incremento graduale dell’IP). Ad esempio, puoi incrementare gradualmente le consegne per un dominio suddividendo l’esecuzione su più giorni: invia 1000 messaggi il primo giorno, 2000 il secondo giorno e così via.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/condition-activity.md#profile_cap">documentazione dettagliata</a> e alcuni <a href="../building-journeys/ramp-up-deliveries-uc.md">esempi di casi d’uso</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Percorsi: miglioramento delle attività Leggi segmento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Alle attività <strong>Leggi segmento</strong> ricorrenti è stata aggiunta l’opzione <strong>Lettura incrementale</strong>. Questa opzione consente di indirizzare solo i singoli utenti che sono entrati a far parte del segmento dopo l’ultima esecuzione del percorso. La prima esecuzione indirizza sempre tutti i membri del segmento.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Ora è possibile collegare gli eventi dei passaggi di Journey Optimizer ad altri set di dati in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=it). Il campo **profileID** nello schema integrato Evento passaggio percorso è ora definito come campo di identità. [Ulteriori informazioni](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* Quando aggiorni un’offerta, un’offerta di fallback, una raccolta di offerte o una decisione di offerta a cui viene fatto riferimento direttamente o indirettamente in un messaggio pubblicato, gli aggiornamenti vengono ora rispecchiati automaticamente nel messaggio corrispondente, senza doverlo ripubblicare. [Ulteriori informazioni](../offers/offers-e2e.md#insert-decision-in-email)

* Quando si effettua una simulazione per capire quali offerte verranno consegnate per un determinato profilo di test, ora è possibile modificare le impostazioni predefinite della simulazione e visualizzare il codice corrispondente alle simulazioni, utile per la risoluzione dei problemi. [Ulteriori informazioni](../offers/offer-activities/simulation.md#define-simulation-settings)

**Amministrazione**

* Gli amministratori ora possono modificare i record PTR con un sottodominio configurato tramite CNAME. [Ulteriori informazioni](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalizzazione**

* **Aggiungi ai preferiti**: per rendere più efficienti le attività di personalizzazione, è stato introdotto il concetto di salvataggio dei preferiti. L’aggiunta di attributi diversi al menu dei preferiti consente di accedere rapidamente agli elementi utilizzati con maggiore frequenza. [Ulteriori informazioni](../personalization/personalize.md#fav)

## Versione di novembre 2021 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>Delega dei sottodomini CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta i CNAME. Un record CNAME, o Canonical Name, è un record che punta a un altro indirizzo di dominio anziché a un indirizzo IP. La delega dei sottodomini CNAME ti consente di creare un sottodominio e di utilizzare i CNAME per puntare a record specifici per Adobe. Utilizzando questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS per configurare l’ambiente per l’invio, il rendering e il tracciamento delle e-mail.</p>
<p>Questo metodo è consigliato se i criteri dell'organizzazione limitano il metodo di delega del sottodominio completo.</p>
<p>Ulteriori informazioni sulla delega del sottodominio CNAME nella <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


## Versione di ottobre 2021 {#oct-2021-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Gestione delle decisioni - Simulazioni delle offerte</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi simulare quali offerte verranno consegnate a un profilo di test per un determinato posizionamento nell’interfaccia utente di Journey Optimizer. Questo ti consente di convalidare facilmente la logica decisionale, compresi i vincoli di idoneità e gli algoritmi di classificazione, prima di inserirli in produzione. Questa funzionalità consente agli utenti tecnici e non di testare rapidamente gli offer decisioning e risolvere eventuali problemi.</p>
<p>Per ulteriori informazioni, consulta la <a href="../offers/offer-activities/simulation.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestione delle decisioni - Personalizzare le offerte</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi personalizzare il contenuto delle offerte utilizzando gli attributi e i segmenti del profilo Adobe Experience Platform, utilizzando lo stesso componente editor di espressioni presente nell’interfaccia utente di Journey Optimizer. </p>
<p>Per ulteriori informazioni, consulta la <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


Consulta anche [Note sulla versione di ottobre di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=it){target=&quot;_blank&quot;} per ulteriori modifiche.

### Miglioramenti

**Percorsi**

* **Editor espressioni** - In qualità di utente avanzato, ora puoi utilizzare le funzioni per lavorare con le mappe. Questa funzionalità può essere utilizzata con gli elenchi degli abbonamenti. Ad esempio, da un segmento, puoi ottenere un indirizzo e-mail da un elenco di abbonamenti. [Per ulteriori informazioni, consulta questa pagina](../building-journeys/message-to-subscribers-uc.md)

* **Monitoraggio** - Sono stati migliorati gli eventi di passaggio per i percorsi live e la modalità di test. [Nuovi campi](../reports/sharing-field-list.md#serviceevents) sono stati aggiunti in relazione ai processi di esportazione del profilo. Per una migliore esperienza utente, i campi evento del passaggio sono ora organizzati in diverse categorie. Tutti i campi degli eventi dei passaggi precedenti sono ancora disponibili nella categoria [stepEvents](../reports/sharing-legacy-fields.md).
* **Accessibilità** - I miglioramenti all’accessibilità sono stati implementati nei percorsi.
* **Raccolte** - Sono ora supportati gli array di oggetti contenenti oggetti secondari. [Ulteriori informazioni](../building-journeys/collections.md)
* **Elenchi** - Sono state migliorate le schermate degli elenchi per percorsi, eventi, azioni, origini dati.

**Generazione rapporti**

* **Formato dati nella visualizzazione globale** - È ora possibile alternare tra numeri e percentuali nella **Visualizzazione globale** della scheda **Esecuzione**. [Ulteriori informazioni](../reports/message-monitoring.md)


**Amministrazione**

* **Modificare i predefiniti per i messaggi** - È ora possibile modificare i predefiniti per i messaggi e monitorarne lo stato di aggiornamento. [Ulteriori informazioni](../configuration/message-presets.md#edit-message-preset)
* **Modifica record PTR** - È ora possibile modificare i record PTR e monitorarne lo stato di aggiornamento. [Ulteriori informazioni](../configuration/ptr-records.md#edit-ptr-record)

**Personalizzazione**

* **Nuova funzione di assistenza per la formattazione della data** - È ora possibile specificare la modalità di rappresentazione di una stringa di data. [Ulteriori informazioni](../personalization/functions/dates.md#format-date)


**Gestione delle decisioni**

* **Sequenza delle valutazioni** - Il flusso di creazione delle decisioni nuovo e migliorato consente non solo di navigare tra gli oggetti decisionali in modo più semplice, ma offre anche un controllo completo sul modo in cui le raccolte di offerte vengono valutate dal motore decisionale. Ciò include quali raccolte vengono valutate insieme e separatamente, e in quale ordine le raccolte devono essere valutate. [Ulteriori informazioni](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Correzioni

* È stato risolto un problema che impediva la visualizzazione dell’elenco dei percorsi, dell’elenco dei messaggi e della finestra di progettazione e-mail quando la lingua del browser non era inglese.
* È stato corretto un errore di sintassi che si verificava quando si aggiungeva la personalizzazione utilizzando un’espressione nella finestra di progettazione e-mail: i caratteri venivano preceduti erroneamente.
* È stato risolto un problema che causava un errore 404 durante la navigazione nel menu **Amministrazione**.
* È stato risolto un problema che attivava altri percorsi in tempo reale durante il test di un percorso utilizzando un evento aziendale.


## Versione di settembre 2021 {#september-2021-release}

### Nuove funzionalità

<table>
<thead>
<tr>

<th><strong>Reporting: approfondimenti migliorati per tipi di pubblico mirati</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Sono disponibili nuove metriche nel reporting: le opzioni Destinati ed Esclusi per e-mail e messaggi push sono visibili sia nei rapporti live che globali. </br> Per poter accedere alle metriche più recenti, è necessario reimpostare le diverse dashboard di generazione rapporti per ogni canale e tipo di reporting. Per ulteriori informazioni sulla personalizzazione della dashboard, consulta la <a href="../reports/live-report.md">documentazione dettagliata.</a></p>
<p>Una nuova colonna nell’elenco di esecuzione dei messaggi mostra il numero di profili target per ogni esecuzione di messaggio. </p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/message-monitoring.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Trasmettere dinamicamente elenchi di dati utilizzando azioni personalizzate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi trasferire raccolte o un elenco di dati nei parametri delle azioni personalizzate che verranno compilati in modo dinamico in fase di esecuzione. Sono supportati due tipi di raccolte: raccolte semplici e raccolte di oggetti. Le azioni personalizzate create in precedenza continueranno a funzionare. </p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/collections.md">documentazione dettagliata</a>. </p>
<p>Le funzioni filtro e intersezione sono state aggiunte all’elenco delle funzioni disponibili nell’editor di espressioni avanzate. Questo offre più possibilità per il filtraggio della raccolta e il confronto.</p>
<p>Consulta la documentazione sulle funzioni <a href="../building-journeys/functions/functionfilter.md">filtro</a> e <a href="../building-journeys/functions/functionintersect.md">intersezione</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Gli schemi e i set di dati generati dal sistema che sono stati creati durante il provisioning per gli eventi delle fasi ora sono in modalità di sola lettura, in modo da evitare eventuali modifiche involontarie agli schemi critici. [Ulteriori informazioni](../reports/sharing-overview.md)
* Etichetta in modo chiaro l’attività **Attesa** con un’etichetta che verrà visualizzata nell’area di lavoro. L’etichetta viene utilizzata anche nei registri della modalità di reporting e test per identificare chiaramente ciò che si sta facendo. [Ulteriori informazioni](../building-journeys/about-journey-activities.md#best-practices)
* Trova più rapidamente i tuoi eventi e le tue azioni filtrando gli elementi nelle categorie **Eventi** e **Azione** utilizzando la ricerca. Le attività di orchestrazione non vengono più filtrate. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md)
* Quando definisci una condizione ID evento in un evento aziendale o basato su regole, l’operatore “contiene” è ora disponibile per i tipi di campi stringa. [Ulteriori informazioni](../event/about-creating.md)

**Configurazione e-mail**

* Ora puoi modificare un pool IP associato a un predefinito per messaggi, perché l’aggiornamento è asincrono. Puoi anche controllare lo stato di aggiornamento di ogni pool IP. [Ulteriori informazioni](../configuration/ip-pools.md#edit-ip-pool)


## Versione di agosto 2021 {#august-2021-release}

### Nuove funzionalità

<table>
<thead>
<tr>

<th><strong>Invia messaggi al momento migliore: ottimizzazione dell’ora di invio</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Invia automaticamente il messaggio push o e-mail nel momento migliore per ogni cliente con cui hai a che fare, grazie ad Adobe Journey Optimizer. L’ottimizzazione dell’ora di invio, basata sui servizi AI di Adobe, prevede il momento migliore per inviare un’e-mail o un messaggio push per massimizzare il coinvolgimento in base alle percentuali storiche di apertura e clic preconfigurate.</p>
<p>Al momento questa funzione è disponibile nella versione beta e solo per i clienti beta. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journeys-message.md#send-time-optimization">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Sfruttamento delle relazioni di schema negli eventi aziendali: gestione delle tabelle di ricerca</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile riutilizzare le relazioni tra schemi durante la configurazione di un evento aziendale. Questo si aggiunge alla possibilità di sfruttare i campi delle tabelle collegate durante la configurazione di un evento unitario, durante l’utilizzo delle condizioni in un percorso, nella personalizzazione dei messaggi e nella personalizzazione delle azioni personalizzate.</p>
<p>Per ulteriori informazioni, consulta la <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>URL personalizzati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gli URL personalizzati indirizzano i destinatari verso pagine specifiche di un sito web o verso un microsito personalizzato, a seconda degli attributi del profilo. In Adobe Journey Optimizer, ora puoi aggiungere la personalizzazione agli URL nel contenuto del messaggio. La personalizzazione URL può essere applicata a testo e immagini e utilizzare dati di profilo o dati contestuali.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/personalization-syntax.md#perso-urls">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Assicurati che le e-mail arrivino ai tuoi utenti - Tentativo di invio e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare il periodo di tempo di un nuovo tentativo su base predefinita, in modo da evitare che i nuovi tentativi vengano eseguiti quando non è più necessario. Ad esempio, puoi impostare il periodo di esecuzione dei nuovi tentativi su 24 ore per un messaggio transazionale di reimpostazione della password contenente un collegamento valido solo per un giorno. Le impostazioni dei nuovi tentativi si applicano solo al canale e-mail.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/retries.md#retry-duration">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Definire gli indirizzi da escludere dall’invio - Elenco di eliminazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adesso è possibile aggiungere indirizzi e-mail e domini all’elenco di eliminazione dall’interfaccia utente, uno alla volta o in modalità collettiva tramite un caricamento di file CSV.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti

**Percorsi**

* **Intestazioni dinamiche** - Ora puoi trasmettere dati dinamici nei parametri di intestazione HTTP. Questi parametri possono essere utilizzati dai sistemi di integrazione che ricevono le chiamate di azione HTTP del percorso, ad esempio la marca temporale o l’ID di tracciamento. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)
* **Percorsi URL dinamici** - Ora puoi impostare percorsi URL dinamici per azioni personalizzate. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)
* Il tasso di limitazione complessivo per i segmenti letti è stato modificato da 17.000 a 20.000 messaggi al secondo. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interfaccia utente**

* **Ricerca** - In ogni pagina, ora puoi e cercare oggetti aziendali e gli articoli direttamente dal campo di ricerca Unified Experience Cloud. [Ulteriori informazioni](../start/user-interface.md#unified-search)
* **Recenti** - La visualizzazione degli elementi recenti della home page di Adobe Journey Optimizer è ora estesa ad altri oggetti aziendali. Con questo aggiornamento, le scelte rapide per l’accesso recente includono Messaggi, Percorsi, Segmenti, Schemi, Set di dati, Origini dati, Eventi, Azioni, Origini e Destinazioni. [Ulteriori informazioni](../action/about-custom-action-configuration.md#passing-collection)

**Progettazione dei contenuti**

* **Sfondo** - Le immagini di sfondo sono ora supportate nell’anteprima live. [Ulteriori informazioni](../design/preview.md)
* **Collegamento rinuncia con un clic** - Puoi inserire un nuovo tipo di collegamento nel contenuto dell’e-mail: il collegamento **Rinuncia** consente agli utenti di annullare l’iscrizione alla ricezione delle comunicazioni con un solo clic, senza essere reindirizzati a una pagina di destinazione per confermare la rinuncia. [Ulteriori informazioni](../messages/consent.md#one-click-opt-out-link)

**Personalizzazione**

* **Editor espressioni** - È ora possibile aggiungere facilmente un valore di fallback durante la definizione della personalizzazione: quando il campo di personalizzazione è vuoto per un profilo, viene visualizzato il valore di fallback. [Ulteriori informazioni](../personalization/functions/helpers.md)

**Configurazione e-mail**

* **Elenco Consentiti** - L’elenco Consentiti può ora essere abilitato e disabilitato in una sandbox non di produzione tramite una chiamata API. [Ulteriori informazioni](../reports/allow-list.md#enable-allow-list)
* **Navigazione** - Elenco di soppressione, accessibile dal menu **Amministrazione > Canali > Configurazione e-mail > Generale** è stato spostato nel nuovo sottomenu **Elenco di eliminazione**, che raccoglie tutte le funzionalità correlate per un accesso più semplice. [Ulteriori informazioni](../configuration/manage-suppression-list.md#access-suppression-list)

**Gestione delle decisioni**

* La modalità di aggiunta e configurazione delle rappresentazioni durante la creazione di un’offerta è stata aggiornata per migliorare l’esperienza di utilizzo. In particolare, la libreria Risorse ora viene visualizzata solo quando, per una rappresentazione, si definiscono contenuti di tipo immagine. [Ulteriori informazioni](../offers/offer-library/creating-personalized-offers.md#representations)

### Correzioni

* È stato risolto un problema di accessibilità nella navigazione della scheda dei messaggi.
* È stato risolto un problema di localizzazione nelle etichette di e-mail designer.
* È stato risolto un problema che si verificava selezionando più nodi in un percorso e facendo clic su “Elimina” nel pannello delle proprietà.
* È stato risolto un problema che impediva l’aggiunta di una nuova intestazione a un’azione utilizzata in un percorso.
* Ora puoi scoprire il motivo per cui una creazione di un predefinito di messaggio non è riuscita tramite un avviso più esplicito nell’interfaccia utente.


## Versione di luglio 2021 {#july-2021-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Utilizzare i metadati nei messaggi - Gestione tabella di ricerca</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Arricchisci le esperienze con i dati di riferimento caricati in Journey Optimizer. Ad esempio, è possibile cercare i metadati su un ID di prenotazione in un evento di esperienza o trovare le informazioni sui prodotti da uno SKU in un evento di esperienza da utilizzare nell’area di lavoro. </p>
<p>È ora possibile sfruttare le relazioni tra schemi per utilizzare un set di dati come tabella di ricerca per un altro. Puoi quindi sfruttare tutti i campi delle tabelle collegate durante la configurazione di un evento unitario, quando utilizzi le condizioni in un percorso, nella personalizzazione dei messaggi e nella personalizzazione delle azioni personalizzata.</p>
<p>Per ulteriori informazioni, consulta la <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Elenco Consentiti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire un elenco di sicurezza per l’invio specifico a livello di sandbox, in modo da disporre di un ambiente sicuro a scopo di test. In un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti ti assicura di non correre il rischio di inviare messaggi indesiderati ai clienti. Questa funzione è abilitata sfruttando le API di eliminazione.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/allow-list.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Il tasso di limitazione complessivo di tutti i segmenti letti eseguiti contemporaneamente nella stessa sandbox è limitato a 17.000 messaggi al secondo. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Il campo **Durata della cache** è stato rimosso dal riquadro di configurazione dell’origine dati. [Ulteriori informazioni](../datasource/about-data-sources.md)
* Per le origini dati esterne, ora viene definita automaticamente una regola di limitazione di 15 chiamate al secondo. [Ulteriori informazioni](../configuration/external-systems.md#capping)
* Per i percorsi live, nella schermata delle proprietà del percorso vengono ora visualizzate la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso. [Ulteriori informazioni](../building-journeys/journey-gs.md#change-properties)
* Nella schermata dell’elenco dei percorsi, è stato aggiunto il filtro del tipo di percorso. [Ulteriori informazioni](../start/user-interface.md#filter-lists)
* Il parametro **[!UICONTROL Throttling rate]** è stato aggiunto il parametro nell’attività Leggi segmento. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Anteprima e verifica dei messaggi**

* L’identità e lo spazio dei nomi sono ora visibili nella **[!UICONTROL Preview]** schermata. [Ulteriori informazioni](../design/preview.md#preview-your-messages)
* Il numero di e-mail di prova per le bozze è ora limitato a 10.
* I caratteri consentiti per **Prefisso riga oggetto** nelle bozze ora sono limitati. [Ulteriori informazioni](../design/preview.md#send-proofs)

**Editor di espressioni di personalizzazione**

* L’elenco a discesa helper è stato rinominato e riordinato.

### Correzioni

* È stato risolto un problema che causava la consegna di messaggi duplicati per la consegna di e-mail in batch.
* Gli eventi vengono ora generati di conseguenza quando l’invio e-mail non viene eseguito una volta terminato il periodo di esecuzione dei nuovi tentativi.
* È stato risolto un problema a causa del quale le informazioni IP mancavano nella schermata Record PTR.
* È ora implementata la localizzazione nella barra delle offerte nell’editor espressioni.
* È stata corretta la spaziatura errata nei popup delle informazioni.
* È stato risolto un problema in E-mail designer durante il caricamento di un file HTML in cui il foglio di stile interno con proprietà `background-image` non era supportato.
