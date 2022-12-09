---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione precedente (2021)
description: Note sulla versione di Journey Optimizer 2021
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '2077'
ht-degree: 0%

---

# Note sulla versione 2021 {#release-notes-2021}

In questa pagina sono elencate tutte le funzioni e i miglioramenti per [!DNL Journey Optimizer] rilasciato nel 2021.


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
<p>Adobe Journey Optimizer ora supporta i CNAME. Un record CNAME, o Canonical Name, è un record che punta a un altro indirizzo di dominio anziché a un indirizzo IP. La delega dei sottodomini CNAME consente di creare un sottodominio e di utilizzare i CNAME per puntare a record specifici di Adobe. Utilizzando questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS per configurare l’ambiente per l’invio, il rendering e il tracciamento delle e-mail.</p>
<p>Questo metodo è consigliato se i criteri dell'organizzazione limitano il metodo di delega del sottodominio completo.</p>
<p>Ulteriori informazioni sulla delega del sottodominio CNAME nel <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">documentazione dettagliata</a>.</p>
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
<p>Ora puoi simulare quali offerte verranno consegnate a un profilo di test per un determinato posizionamento nell’interfaccia utente di Journey Optimizer. Questo ti consente di convalidare facilmente la logica decisionale, compresi i vincoli di idoneità e gli algoritmi di classificazione, prima di inserirli in produzione. Questa funzionalità consente agli utenti non tecnici e tecnici di testare rapidamente la gestione delle decisioni e di risolvere eventuali problemi.</p>
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
<p>Ora puoi personalizzare il contenuto delle offerte utilizzando gli attributi e i segmenti di profilo di Adobe Experience Platform, utilizzando lo stesso componente editor di espressioni presente in tutta l’interfaccia utente di Journey Optimizer. </p>
<p>Per ulteriori informazioni, consulta la <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


Vedi anche [Note sulla versione di ottobre di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html){target=&quot;_blank&quot;} per ulteriori modifiche.

### Miglioramenti

**Percorsi**

* **Editor espressioni** - In qualità di utente avanzato, è ora possibile utilizzare le funzioni per lavorare con le mappe. Questa funzionalità può essere utilizzata con gli elenchi di sottoscrizione. Ad esempio, da un segmento puoi ora ottenere un indirizzo e-mail da un elenco di abbonamenti. [Ulteriori informazioni in questo esempio](../building-journeys/message-to-subscribers-uc.md)

* **Monitoraggio** - Sono stati migliorati gli eventi dei passaggi per i percorsi live e la modalità di test. [Nuovi campi](../reports/sharing-field-list.md#serviceevents) sono stati aggiunti relativi ai processi di esportazione del profilo. Per una migliore esperienza utente, i campi evento del passaggio sono ora organizzati in diverse categorie. Tutti i campi degli eventi dei passaggi precedenti sono ancora disponibili nel [stepEvents](../reports/sharing-legacy-fields.md) categoria.
* **Accessibilità** - I miglioramenti all’accessibilità sono stati implementati nei percorsi.
* **Raccolte** - Sono ora supportati gli array di oggetti contenenti oggetti secondari. [Leggi tutto](../building-journeys/collections.md)
* **Elenchi** - Sono state migliorate le schermate degli elenchi per percorsi, eventi, azioni, origini dati.

**Reporting**

* **Formato dati nella visualizzazione globale** - È ora possibile alternare tra numeri e percentuali nella **Vista globale** del **Esecuzione** scheda .


**Amministrazione**

* **Modificare i predefiniti per i messaggi** - È ora possibile modificare i predefiniti per i messaggi e monitorarne lo stato di aggiornamento. [Ulteriori informazioni](../configuration/channel-surfaces.md#edit-channel-surface)
* **Modifica record PTR** - È ora possibile modificare i record PTR e monitorarne lo stato di aggiornamento. [Ulteriori informazioni](../configuration/ptr-records.md#edit-ptr-record)

**Personalizzazione**

* **Nuova funzione helper per per la formattazione della data** - È ora possibile specificare la modalità di rappresentazione di una stringa di data. [Ulteriori informazioni](../personalization/functions/dates.md#format-date)


**Gestione delle decisioni**

* **Sequenza delle valutazioni** - Il flusso di creazione delle decisioni nuovo e migliorato consente non solo di navigare tra gli oggetti decisionali in modo più semplice, ma offre anche un controllo completo sul modo in cui le raccolte di offerte vengono valutate dal motore decisionale. Ciò include quali raccolte vengono valutate insieme e separatamente, e in quale ordine le raccolte devono essere valutate. [Ulteriori informazioni](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Correzioni

* È stato risolto un problema che impediva la visualizzazione dell’elenco dei percorsi, dell’elenco dei messaggi e della finestra di progettazione e-mail quando la lingua del browser non era inglese.
* È stato corretto un errore di sintassi che si verificava quando si aggiungeva la personalizzazione utilizzando un’espressione nella finestra di progettazione e-mail: i personaggi erano scampati erroneamente.
* È stato risolto un problema che causava un errore 404 durante la navigazione in **Amministrazione** menu.
* È stato risolto un problema che attivava altri percorsi live durante il test di un percorso utilizzando un evento aziendale.


## Versione di settembre 2021 {#september-2021-release}

### Nuove funzionalità

<table>
<thead>
<tr>

<th><strong>Reporting - Approfondimenti migliorati per tipi di pubblico mirati</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Sono disponibili nuove metriche nel reporting: Le opzioni Destinate ed Escluse per e-mail e messaggi push sono visibili sia nei rapporti live che globali. </br> Per poter accedere alle metriche più recenti, è necessario reimpostare le diverse dashboard di reporting per ogni canale e tipo di reporting. Per ulteriori informazioni sulla personalizzazione del dashboard, consulta <a href="../reports/live-report.md">documentazione dettagliata.</a></p>
<p>Una nuova colonna nell’elenco di esecuzione dei messaggi visualizza il numero di profili target per ogni esecuzione dei messaggi. </p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/global-report.md">documentazione dettagliata</a>.</p>
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
<p>Ora puoi passare raccolte o un elenco di dati nei parametri delle azioni personalizzate che verranno compilati in modo dinamico in fase di esecuzione. Sono supportati due tipi di raccolte: raccolte semplici e raccolte di oggetti. Le azioni personalizzate create in precedenza continueranno a funzionare. </p>
<p>Per ulteriori informazioni sulle raccolte, consulta la <a href="../building-journeys/collections.md">documentazione dettagliata</a>. </p>
<p>Le funzioni filtro e intersezione sono state aggiunte all’elenco delle funzioni disponibili nell’editor di espressioni avanzate. Questo offre più possibilità per il filtraggio della raccolta e il confronto.</p>
<p>Consulta la documentazione sul <a href="../building-journeys/functions/functionfilter.md">filter</a> e <a href="../building-journeys/functions/functionintersect.md">intersecare</a> funzioni.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Gli schemi e i set di dati generati dal sistema che sono stati creati durante il provisioning per gli eventi delle fasi ora sono in modalità di sola lettura, evitando eventuali modifiche involontarie agli schemi critici. [Ulteriori informazioni](../reports/sharing-overview.md)
* Etichettare in modo chiaro il **Wait** attività con un’etichetta che verrà visualizzata nell’area di lavoro. L’etichetta viene utilizzata anche nei registri della modalità di reporting e test per identificare chiaramente ciò che si sta facendo. [Ulteriori informazioni](../building-journeys/about-journey-activities.md#best-practices)
* Trova più rapidamente i tuoi eventi e le tue azioni filtrando gli elementi nel **Eventi** e **Azione** categorie che utilizzano la ricerca. Le attività di orchestrazione non vengono più filtrate. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md)
* Quando definisci una condizione ID evento in un evento aziendale o basato su regole, l&#39;operatore &quot;contiene&quot; è ora disponibile per i tipi di campi stringa. [Ulteriori informazioni](../event/about-creating.md)

**Configurazione e-mail**

* Quando un pool IP è stato associato a un predefinito per messaggi, ora puoi modificarlo in modo asincrono. Puoi anche controllare lo stato di aggiornamento di ogni pool IP. [Ulteriori informazioni](../configuration/ip-pools.md#edit-ip-pool)


## Versione di agosto 2021 {#august-2021-release}

### Nuove funzionalità

<table>
<thead>
<tr>

<th><strong>Invia messaggi al momento migliore - Ottimizzazione dell’ora di invio</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Invia automaticamente il tuo messaggio push o e-mail al momento migliore per ogni cliente con Adobe Journey Optimizer. L’ottimizzazione del tempo di invio, basata sui servizi AI di Adobe, prevede il momento migliore per inviare un’e-mail o un messaggio push per massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche preconfigurate.</p>
<p>Al momento questa funzione è disponibile nella versione beta e solo per i clienti beta. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journeys-message.md#send-time-optimization">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Utilizzo delle relazioni di schema negli eventi aziendali - Gestione delle tabelle di ricerca</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile sfruttare le relazioni tra gli schemi durante la configurazione di eventi aziendali. Questo si aggiunge alla possibilità di sfruttare i campi delle tabelle collegate durante la configurazione di un evento unitario, durante l’utilizzo delle condizioni in un percorso, nella personalizzazione dei messaggi e nella personalizzazione delle azioni personalizzate.</p>
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
<p>Gli URL personalizzati indirizzano i destinatari a pagine specifiche di un sito web o a un microsito personalizzato, a seconda degli attributi del profilo. In Adobe Journey Optimizer puoi ora aggiungere la personalizzazione agli URL nel contenuto del messaggio. La personalizzazione URL può essere applicata a testo e immagini e utilizzare dati di profilo o dati contestuali.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/personalization-syntax.md#perso-urls">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Assicurati che le e-mail arrivino ai tuoi utenti - Invia nuovo messaggio e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile definire il periodo di esecuzione dei nuovi tentativi in base al predefinito, in modo da evitare che i tentativi vengano più eseguiti quando non più necessario. Ad esempio, puoi impostare il periodo di esecuzione dei nuovi tentativi su 24 ore per un messaggio transazionale di reimpostazione della password contenente un collegamento valido solo per un giorno. Le impostazioni dei nuovi tentativi si applicano solo al canale e-mail.</p>
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
<p>L’aggiunta di indirizzi e-mail e domini all’elenco di soppressione è ora disponibile dall’interfaccia utente, una per una, in modalità collettiva tramite un caricamento di file CSV.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti

**Percorsi**

* **Intestazioni dinamiche** - È ora possibile trasmettere dati dinamici nei parametri di intestazione HTTP. Questi parametri possono essere utilizzati dai sistemi di integrazione che ricevono le chiamate HTTP delle azioni del percorso, ad esempio la marca temporale o l’ID di tracciamento. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)
* **Percorsi URL dinamici** - È ora possibile impostare percorsi URL dinamici per le azioni personalizzate. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)
* Il tasso di limitazione complessivo per i segmenti letti è stato modificato da 17.000 a 20.000 messaggi al secondo. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interfaccia utente**

* **Ricerca** - In ogni pagina, ora puoi cercare oggetti aziendali e aiutare gli articoli direttamente dal campo di ricerca Unified Experience Cloud . [Ulteriori informazioni](../start/user-interface.md#unified-search)
* **Recenti** - La visualizzazione degli elementi recenti dalla home page di Adobe Journey Optimizer è ora estesa ad altri oggetti aziendali. Con questo aggiornamento, le scelte rapide per l’accesso recente includono Messaggi, Percorsi, Segmenti, Schemi, Set di dati, Origini dati, Eventi, Azioni, Origini e Destinazioni. [Ulteriori informazioni](../action/about-custom-action-configuration.md#passing-collection)

**Progettazione dei contenuti**

* **Sfondo** - Le immagini di sfondo sono ora supportate nell’anteprima live. [Ulteriori informazioni](../email/preview.md)
* **Collegamento di rinuncia con un clic** - Puoi inserire un nuovo tipo di collegamento nel contenuto dell’e-mail: la **Rinuncia** Il collegamento consente agli utenti di annullare l’iscrizione alla ricezione delle comunicazioni con un solo clic, senza essere reindirizzati a una pagina di destinazione per confermare la rinuncia. [Ulteriori informazioni](../privacy/opt-out.md#one-click-opt-out-link)

**Personalizzazione**

* **Editor espressioni** - È ora possibile aggiungere facilmente un valore di fallback durante la definizione della personalizzazione: quando il campo di personalizzazione è vuoto per un profilo, viene visualizzato il valore di fallback. [Ulteriori informazioni](../personalization/functions/helpers.md)

**Configurazione e-mail**

* **Elenco consentito** - È ora possibile abilitare e disabilitare l’elenco Consentiti in una sandbox non di produzione tramite una chiamata API. [Ulteriori informazioni](../configuration/allow-list.md#enable-allow-list)
* **Navigazione** - Elenco di soppressione, accessibile sotto **Amministrazione > Canali > Configurazione e-mail > Generale** è stato spostato nel nuovo menu **Elenco di eliminazione** sottomenu, che raccoglie tutte le funzionalità correlate per un accesso più semplice. [Ulteriori informazioni](../configuration/manage-suppression-list.md#access-suppression-list)

**Gestione delle decisioni**

* La modalità di aggiunta e configurazione delle rappresentazioni durante la creazione di un’offerta è stata aggiornata per migliorare l’esperienza utente. In particolare, la libreria Risorse viene ora visualizzata solo quando si definisce il contenuto di tipo immagine per una rappresentazione. [Ulteriori informazioni](../offers/offer-library/creating-personalized-offers.md#representations)

### Correzioni

* È stato risolto un problema di accessibilità nella navigazione nella scheda dei messaggi.
* È stato risolto un problema di localizzazione nelle etichette di e-mail designer.
* È stato risolto un problema che si verificava selezionando più nodi in un percorso e facendo clic su &quot;Elimina&quot; nel riquadro delle proprietà.
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
<p>È ora possibile sfruttare le relazioni tra schemi per utilizzare un set di dati come tabella di ricerca per un altro. Puoi quindi sfruttare tutti i campi delle tabelle collegate durante la configurazione di un evento unitario, quando utilizzi le condizioni in un percorso, nella personalizzazione dei messaggi e nella personalizzazione delle azioni personalizzate.</p>
<p>Per ulteriori informazioni, consulta la <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Elenco consentito</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire un elenco di sicurezza per l’invio specifico a livello di sandbox, in modo da disporre di un ambiente sicuro a scopo di test. In un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti garantisce di non rischiare di inviare messaggi indesiderati ai clienti. Questa funzione è abilitata sfruttando le API di eliminazione.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/allow-list.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Il tasso di limitazione complessivo di tutti i segmenti letti eseguiti contemporaneamente nella stessa sandbox è limitato a 17.000 messaggi al secondo. [Leggi tutto](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* La **Durata della cache** campo rimosso dal riquadro di configurazione dell’origine dati. [Leggi tutto](../datasource/about-data-sources.md)
* Per le origini dati esterne, ora viene definita automaticamente una regola di limitazione di 15 chiamate al secondo. [Leggi tutto](../configuration/external-systems.md#capping)
* Per i percorsi live, la schermata delle proprietà del percorso visualizza ora la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso. [Leggi tutto](../building-journeys/journey-gs.md#change-properties)
* Nella schermata dell’elenco dei percorsi, è stato aggiunto il filtro del tipo di percorso. [Leggi tutto](../start/user-interface.md#filter-lists)
* La **[!UICONTROL Throttling rate]** È stato aggiunto il parametro nell’attività Leggi segmento . [Leggi tutto](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Anteprima e test**

* L’identità e lo spazio dei nomi sono ora visibili nella **[!UICONTROL Preview]** schermo. [Leggi tutto](../email/preview.md#preview-your-messages)
* Il numero di e-mail di test per le bozze è ora limitato a 10.
* Caratteri consentiti per **Prefisso riga oggetto** le bozze ora sono limitate. [Leggi tutto](../email/preview.md#send-proofs)

**Editor di espressioni di personalizzazione**

* L’elenco a discesa helper è stato rinominato e riordinato.

### Correzioni

* È stato risolto un problema che causava la consegna di messaggi duplicati per la consegna di e-mail batch.
* Gli eventi vengono ora generati di conseguenza quando l’invio e-mail non viene eseguito una volta terminato il periodo di esecuzione dei nuovi tentativi.
* È stato risolto un problema a causa del quale le informazioni IP mancavano nella schermata Record PTR.
* La localizzazione nella barra delle offerte nell’editor espressioni è ora implementata.
* È stata corretta la spaziatura errata nei popup delle informazioni.
* È stato risolto un problema in E-mail designer durante il caricamento di un file HTML in cui foglio di stile interno con `background-image` proprietà non supportata.
