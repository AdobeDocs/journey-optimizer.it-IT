---
solution: Journey Optimizer
product: journey optimizer
title: Note sulle versioni precedenti (2021)
description: Note sulle versioni 2021 di Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
hide: true
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 0331f8fe2439d41c08ad88a6d0bd95dd150bab90
workflow-type: tm+mt
source-wordcount: '2035'
ht-degree: 100%

---

# Note sulle versioni 2021 {#release-notes-2021}

In questa pagina sono elencate tutte le funzioni e i miglioramenti rilasciati nel 2021 per [!DNL Journey Optimizer].

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
<p>Ulteriori informazioni sulla delega del sottodominio CNAME sono disponibili nella <a href="../configuration/delegate-subdomain.md#cname-subdomain-setup">documentazione dettagliata</a>.</p>
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
<p>Ora puoi simulare quali offerte verranno consegnate a un profilo di test per un determinato posizionamento nell’interfaccia utente di Journey Optimizer. Questo ti consente di convalidare facilmente la logica decisionale, compresi i vincoli di idoneità e gli algoritmi di classificazione, prima di inserirli in produzione. Questa funzionalità consente agli utenti tecnici e non di testare rapidamente la gestione delle decisioni e risolvere potenziali problemi.</p>
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
<p>Ora puoi personalizzare il contenuto delle offerte utilizzando gli attributi e i tipi di pubblico del profilo Adobe Experience Platform, tramite lo stesso componente editor di espressioni presente nell’interfaccia utente di Journey Optimizer. </p>
<p>Per ulteriori informazioni, consulta la <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


Consulta anche le [Note sulla versione di ottobre di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=it){target="_blank"} per ulteriori modifiche.

### Miglioramenti

**Percorsi**

* **Editor espressioni** - In qualità di utente avanzato, ora puoi utilizzare le funzioni per lavorare con le mappe. Questa funzionalità può essere utilizzata con gli elenchi degli abbonamenti. Ad esempio, da un pubblico, ora puoi ottenere un indirizzo e-mail da un elenco di iscrizioni. [Per ulteriori informazioni, consulta questa pagina](../building-journeys/message-to-subscribers-uc.md)

* **Monitoraggio** - Sono stati migliorati gli eventi di passaggio per i percorsi live e la modalità di test. [Nuovi campi](../reports/sharing-field-list.md#serviceevents) sono stati aggiunti in relazione ai processi di esportazione del profilo. Per una migliore esperienza utente, i campi evento del passaggio sono ora organizzati in diverse categorie. Tutti i campi degli eventi dei passaggi precedenti sono ancora disponibili nella categoria [stepEvents](../reports/sharing-legacy-fields.md).
* **Accessibilità** - I miglioramenti all’accessibilità sono stati implementati nei percorsi.
* **Raccolte** - Sono ora supportati gli array di oggetti contenenti oggetti secondari. [Ulteriori informazioni](../building-journeys/collections.md)
* **Elenchi** - Sono state migliorate le schermate degli elenchi per percorsi, eventi, azioni, origini dati.

**Generazione rapporti**

* **Formato dati nella vista Globale** - Ora è possibile passare da numeri a percentuali nella **vista Globale** della scheda **Esecuzione**.


**Amministrazione**

* **Modificare i predefiniti per i messaggi** - È ora possibile modificare i predefiniti per i messaggi e monitorarne lo stato di aggiornamento. [Ulteriori informazioni](../configuration/channel-surfaces.md#edit-channel-surface)
* **Modifica record PTR** - È ora possibile modificare i record PTR e monitorarne lo stato di aggiornamento. [Ulteriori informazioni](../configuration/ptr-records.md#edit-ptr-record)

**Personalizzazione**

* **Nuova funzione di assistenza per la formattazione della data** - È ora possibile specificare la modalità di rappresentazione di una stringa di data. [Ulteriori informazioni](../personalization/functions/dates.md#format-date)


**Gestione delle decisioni**

* **Sequenza delle valutazioni** - Il flusso di creazione delle decisioni nuovo e migliorato consente non solo di navigare tra gli oggetti decisionali in modo più semplice, ma offre anche un controllo completo sul modo in cui le raccolte di offerte vengono valutate dal motore decisionale. Ciò include quali raccolte vengono valutate insieme e separatamente, e in quale ordine le raccolte devono essere valutate. [Ulteriori informazioni](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Correzioni

* È stato risolto un problema che impediva la visualizzazione dell’elenco dei percorsi, dell’elenco dei messaggi e di E-mail designer quando la lingua del browser non era inglese.
* È stato risolto un errore di sintassi che si verificava durante l’aggiunta di personalizzazione con un’espressione in E-mail designer: i caratteri venivano preceduti erroneamente dall’escape.
* È stato risolto un problema che causava un errore 404 durante la navigazione nel menu **Amministrazione**.
* È stato risolto un problema che attivava altri percorsi live durante il test di un percorso utilizzando un evento di business.


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
<p>Per ulteriori informazioni, consulta la <a href="../reports/report-gs-cja.md">documentazione dettagliata</a>.</p>
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
<p>Consulta la documentazione sulle funzioni <a href="../building-journeys/functions/list-functions.md#filter">filtro</a> e <a href="../building-journeys/functions/list-functions.md#intersect">intersezione</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Gli schemi e i set di dati generati dal sistema che sono stati creati durante il provisioning per gli eventi delle fasi ora sono in modalità di sola lettura, in modo da evitare eventuali modifiche involontarie agli schemi critici. [Ulteriori informazioni](../reports/sharing-overview.md)
* Etichetta in modo chiaro l’attività **Attesa** con un’etichetta che verrà visualizzata nell’area di lavoro. L’etichetta viene utilizzata anche nei registri della modalità di reporting e test per identificare chiaramente ciò che si sta facendo. [Ulteriori informazioni](../building-journeys/about-journey-activities.md#best-practices)
* Trova più rapidamente i tuoi eventi e le tue azioni filtrando gli elementi nelle categorie **Eventi** e **Azione** utilizzando la ricerca. Le attività di orchestrazione non vengono più filtrate. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md)
* Quando definisci una condizione per un ID evento in un evento di business o basato su regole, l’operatore “contiene” è ora disponibile per i tipi di campi stringa. [Ulteriori informazioni](../event/about-creating.md)

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
<p>Invia automaticamente il messaggio push o e-mail nel momento migliore per ogni cliente con cui hai a che fare, grazie ad Adobe Journey Optimizer. L’ottimizzazione dell’ora di invio, gestita dai servizi Adobe basati su IA, prevede il momento migliore per inviare un’e-mail o un messaggio push per massimizzare il coinvolgimento in base alle percentuali storiche di apertura e clic preconfigurate.</p>
<p>Al momento questa funzione è disponibile nella versione beta e solo per i clienti beta. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/send-time-optimization.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Sfruttamento delle relazioni di schema negli eventi di business: gestione delle tabelle di ricerca</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile riutilizzare le relazioni tra schemi durante la configurazione di un evento di business. Questo si aggiunge alla possibilità di sfruttare i campi delle tabelle collegate durante la configurazione di un evento unitario, durante l’utilizzo delle condizioni in un percorso, nella personalizzazione dei messaggi e nella personalizzazione delle azioni personalizzate.</p>
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
* La frequenza di limitazione complessiva per i tipi di pubblico letti è stata modificata da 17.000 a 20.000 messaggi al secondo. [Ulteriori informazioni](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Interfaccia utente**

* **Ricerca** - In ogni pagina, ora puoi eseguire ricerche negli oggetti di business e negli articoli della documentazione direttamente dal campo di ricerca unificata di Experience Cloud. [Ulteriori informazioni](../start/user-interface.md#unified-search)
* **Recenti** - La visualizzazione degli elementi recenti della pagina home di Adobe Journey Optimizer è ora estesa ad altri oggetti di business. Con questo aggiornamento, le scelte rapide per l’accesso recente includono Messaggi, Percorsi, Tipi di pubblico, Schemi, Set di dati, Origini dati, Eventi, Azioni, Origini e Destinazioni. [Ulteriori informazioni](../action/about-custom-action-configuration.md#passing-collection)

**Progettazione dei contenuti**

* **Sfondo** - Le immagini di sfondo sono ora supportate nell’anteprima live. [Ulteriori informazioni](../content-management/preview-test.md)
  <!--* **One-click opt-out link** - You can insert a new type of link into your email content: the **Opt-out** link allows users to unsubscribe from receiving your communications in just one click, without being redirected to a landing page to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)-->

**Personalizzazione**

* **Editor di espressioni** - Ora è possibile aggiungere facilmente un valore di fallback durante la definizione di personalizzazione; quando il campo di personalizzazione è vuoto per un profilo, viene visualizzato il valore di fallback. [Ulteriori informazioni](../personalization/functions/helpers.md)

**Configurazione e-mail**

* **Elenco Consentiti** - L’elenco Consentiti può ora essere abilitato e disabilitato in una sandbox non di produzione tramite una chiamata API. [Ulteriori informazioni](../configuration/allow-list.md#enable-allow-list)
* **Navigazione**: l’elenco di soppressione, accessibile dal menu **Amministrazione > Canali > Configurazione e-mail > Generale**, è stato spostato nel nuovo sottomenu **Elenco di soppressione**, che raccoglie tutte le funzionalità correlate per un accesso più semplice. [Ulteriori informazioni](../configuration/manage-suppression-list.md#access-suppression-list)

**Gestione delle decisioni**

* La modalità di aggiunta e configurazione delle rappresentazioni durante la creazione di un’offerta è stata aggiornata per migliorare l’esperienza di utilizzo. In particolare, la libreria Risorse ora viene visualizzata solo quando, per una rappresentazione, si definiscono contenuti di tipo immagine. [Ulteriori informazioni](../offers/offer-library/creating-personalized-offers.md#representations)

### Correzioni

* È stato risolto un problema di accessibilità nella navigazione della scheda dei messaggi.
* È stato risolto un problema di localizzazione nelle etichette in E-mail designer.
* È stato risolto un problema che si verificava quando si selezionavano più nodi in un percorso e quindi si faceva clic su “Elimina” nel riquadro delle proprietà.
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
<p>Arricchisci le esperienze con i dati di riferimento caricati in Journey Optimizer. Ad esempio, è possibile cercare metadati su un ID di prenotazione in un evento esperienza o trovare informazioni sui prodotti da uno SKU in un evento esperienza da utilizzare nell’area di lavoro. </p>
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
<p>Per ulteriori informazioni, consulta la <a href="../configuration/allow-list.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* La frequenza di limitazione complessiva di tutti i tipi di pubblico letti eseguiti contemporaneamente nella stessa sandbox è limitata a 17.000 messaggi al secondo. [Ulteriori informazioni](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Il campo **Durata della cache** è stato rimosso dal riquadro di configurazione dell’origine dati. [Ulteriori informazioni](../datasource/about-data-sources.md)
* Per le origini dati esterne, ora viene definita automaticamente una regola di limitazione di 15 chiamate al secondo. [Ulteriori informazioni](../configuration/external-systems.md#capping)
* Per i percorsi live, nella schermata delle proprietà del percorso vengono ora visualizzate la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso. [Ulteriori informazioni](../building-journeys/journey-gs.md#change-properties)
* Nella schermata dell’elenco dei percorsi, è stato aggiunto il filtro del tipo di percorso. [Ulteriori informazioni](../start/user-interface.md#filter-lists)
* Il parametro **[!UICONTROL Frequenza di limitazione]** è stato aggiunto nell’attività Leggi pubblico. [Ulteriori informazioni](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Anteprima e test**

* L’identità e lo spazio dei nomi ora sono visibili nella schermata **[!UICONTROL Anteprima]**. [Ulteriori informazioni](../content-management/preview-test.md#preview-your-messages)
* Il numero di e-mail di prova per le bozze è ora limitato a 10.
* I caratteri consentiti per **Prefisso riga oggetto** nelle bozze ora sono limitati. [Ulteriori informazioni](../content-management/preview-test.md#send-proofs)

**Editor di espressioni di personalizzazione**

* L’elenco a discesa helper è stato rinominato e riordinato.

### Correzioni

* È stato risolto un problema che causava la consegna di messaggi duplicati per la consegna di e-mail in batch.
* Gli eventi vengono ora generati di conseguenza quando l’invio e-mail non viene eseguito una volta terminato il periodo di esecuzione dei nuovi tentativi.
* È stato risolto un problema a causa del quale le informazioni IP mancavano nella schermata Record PTR.
* È stata implementata la localizzazione nella barra delle offerte nell’editor di espressioni.
* È stata corretta la spaziatura errata nei popup delle informazioni.
* È stato risolto un problema in E-mail designer durante il caricamento di un file HTML, in cui il foglio di stile interno con proprietà `background-image` non veniva supportato.
