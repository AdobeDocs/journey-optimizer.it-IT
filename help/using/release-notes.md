---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5e93ccee2056814c25531fc13c3cd433a19077a6
workflow-type: tm+mt
source-wordcount: '1996'
ht-degree: 16%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. È inoltre possibile consultare [ultimi aggiornamenti della documentazione](documentation-updates.md).

## Versione di ottobre 2021 {#oct-2021-release}

<!--table>
<thead>
<tr>
<th><strong>Journeys - Target users in a subscription list</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now trigger a journey targeting a subscription list. To perform this: add a Read segment activity followed by a message, and in the message email settings, define an expression that will fetch the subscriber email address from the profile, for the targeted subscription list. The expression editor has been enhanced to allow you to to select the first entry key of a map.</p>
<p>Learn more in the <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">detailed documentation</a>.</p>>
</td>
</tr>
</tbody>
</table-->



<!--table>
<thead>
<tr>
<th><strong>Journeys - Profile cap condition</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>When using a <strong>Condition</strong> activity in a journey, you can now define a <strong>Profile cap</strong> condition. This new condition type allows you set a maximum number of profiles for a journey path. When this limit is reached, the selected profiles take a second path. This allows you to optimize your IP ramp up. For example, you may want to ramp up your deliveries on a domain to 50 millions by splitting the execution: send 1000 messages on day 1, 2000 on day 2, etc.</p>
<p>For more information, refer to the <a href="building-journeys/condition-activity.md#profile_cap">detailed documentation</a> and related <a href="building-journeys/ramp-up-deliveries-uc.md">sample use case</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Gestione delle decisioni - Simulazioni delle offerte</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi simulare quali offerte verranno consegnate a un profilo di test per un determinato posizionamento nell’interfaccia utente di Journey Optimizer. Questo ti consente di convalidare facilmente la logica decisionale, compresi i vincoli di idoneità e gli algoritmi di classificazione, prima di inserirli in produzione. Questa funzionalità consente agli utenti non tecnici e tecnici di testare rapidamente gli offer decisioning e risolvere eventuali problemi.</p>
<p>Per ulteriori informazioni, consulta la <a href="offers/offer-activities/simulation.md">documentazione dettagliata</a>.</p>
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
<p>Per ulteriori informazioni, consulta la <a href="offers/offer-library/creating-personalized-offers.md#custom-text">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


Vedi anche [Note sulla versione di ottobre di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target=&quot;_blank&quot;} per ulteriori modifiche.

### Miglioramenti

**Percorsi**

* **Editor espressioni** - In qualità di utente avanzato, è ora possibile utilizzare le funzioni per lavorare con le mappe. Questa funzionalità può essere utilizzata con gli elenchi di sottoscrizione. Ad esempio, da un segmento puoi ora ottenere un indirizzo e-mail da un elenco di abbonamenti. [Ulteriori informazioni in questo esempio](building-journeys/message-to-subscribers-uc.md)

   <!-- * **Delta on segments** - When using a **Read segment** activity, you can now target the individuals who entered or exited a specific segment since the last execution.  -->
* **Monitoraggio** - Sono stati migliorati gli eventi di passaggio per i percorsi live e la modalità di test. [Nuovi campi](reports/sharing-field-list.md#serviceevents) sono stati aggiunti relativi ai processi di esportazione del profilo. Per una migliore esperienza utente, i campi evento del passaggio sono ora organizzati in diverse categorie. Tutti i campi degli eventi dei passaggi precedenti sono ancora disponibili nel [stepEvents](reports/sharing-legacy-fields.md) categoria.
* **Accessibilità** - I miglioramenti all’accessibilità sono stati implementati nei percorsi.
* **Raccolte** - Sono ora supportati gli array di oggetti contenenti oggetti secondari. [Ulteriori informazioni](building-journeys/collections.md)
* **Elenchi** - Sono state migliorate le schermate degli elenchi per percorsi, eventi, azioni, origini dati.

**Generazione rapporti**

* **Formato dati nella visualizzazione globale** - È ora possibile alternare tra numeri e percentuali nella **Vista globale** del **Esecuzione** scheda . [Ulteriori informazioni](message-monitoring.md)

<!--* **New metrics** - New metrics and widgets are now available in **Live** and **Global** reports to measure your offers' impact on recipients. [Learn more](reports/journey-global-report.md)-->

**Amministrazione**

* **Modificare i predefiniti per i messaggi** - È ora possibile modificare i predefiniti per i messaggi e monitorarne lo stato di aggiornamento. [Ulteriori informazioni](configuration/message-presets.md#edit-message-preset)
* **Modifica record PTR** - È ora possibile modificare i record PTR e monitorarne lo stato di aggiornamento. [Ulteriori informazioni](configuration/ptr-records.md#edit-ptr-record)

**Personalizzazione**

* **Nuova funzione helper per per la formattazione della data** - È ora possibile specificare la modalità di rappresentazione di una stringa di data. [Ulteriori informazioni](personalization/functions/dates.md#format-date)

**Gestione delle decisioni**

* **Sequenza delle valutazioni** - Il flusso di creazione delle decisioni nuovo e migliorato consente non solo di navigare tra gli oggetti decisionali in modo più semplice, ma offre anche un controllo completo sul modo in cui le raccolte di offerte vengono valutate dal motore decisionale. Ciò include quali raccolte vengono valutate insieme e separatamente, e in quale ordine le raccolte devono essere valutate. [Ulteriori informazioni](offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Correzioni

* È stato risolto un problema che impediva la visualizzazione dell’elenco dei Percorsi, dell’elenco dei messaggi e della finestra di progettazione e-mail quando la lingua del browser non era inglese.
* È stato corretto un errore di sintassi che si verificava quando si aggiungeva la personalizzazione utilizzando un’espressione nella finestra di progettazione e-mail: i personaggi erano scampati erroneamente.
* È stato risolto un problema che causava un errore 404 durante la navigazione in **Amministrazione** menu.
* È stato risolto un problema che attivava altri percorsi in tempo reale durante il test di un percorso utilizzando un evento aziendale.

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
<p>Sono disponibili nuove metriche nel reporting: Le opzioni Destinate ed Escluse per e-mail e messaggi push sono visibili sia nei rapporti live che globali. </br> Per poter accedere alle metriche più recenti, è necessario reimpostare le diverse dashboard di reporting per ogni canale e tipo di reporting. Per ulteriori informazioni sulla personalizzazione del dashboard, consulta <a href="reports/live-report.md">documentazione dettagliata.</a></p>
<p>Una nuova colonna nell’elenco di esecuzione dei messaggi visualizza il numero di profili target per ogni esecuzione dei messaggi. </p>
<p>Per ulteriori informazioni, consulta la <a href="message-monitoring.md">documentazione dettagliata</a>.</p>
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
<p>Per ulteriori informazioni sulle raccolte, consulta la <a href="building-journeys/collections.md">documentazione dettagliata</a>. </p>
<p>Le funzioni filtro e intersezione sono state aggiunte all’elenco delle funzioni disponibili nell’editor di espressioni avanzate. Questo offre più possibilità per il filtraggio della raccolta e il confronto.</p>
<p>Consulta la documentazione sul <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">filter</a> e <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionintersect.html">intersecare</a> funzioni.</p>
</td>
</tr>
</tbody>
</table>



### Miglioramenti

**Percorsi**

* Gli schemi e i set di dati generati dal sistema che sono stati creati durante il provisioning per gli eventi delle fasi ora sono in modalità di sola lettura, evitando eventuali modifiche involontarie agli schemi critici. [Ulteriori informazioni](reports/sharing-overview.md)
* Etichettare in modo chiaro il **Wait** attività con un’etichetta che verrà visualizzata nell’area di lavoro. L’etichetta viene utilizzata anche nei registri della modalità di reporting e test per identificare chiaramente ciò che si sta facendo. [Ulteriori informazioni](building-journeys/about-journey-activities.md#best-practices)
* Trova più rapidamente i tuoi eventi e le tue azioni filtrando gli elementi nel **Eventi** e **Azione** categorie che utilizzano la ricerca. Le attività di orchestrazione non vengono più filtrate. [Ulteriori informazioni](building-journeys/using-the-journey-designer.md)
* Quando definisci una condizione ID evento in un evento aziendale o basato su regole, l&#39;operatore &quot;contiene&quot; è ora disponibile per i tipi di campi stringa. [Ulteriori informazioni](event/about-creating.md)

**Configurazione e-mail**

* Quando un pool IP è stato associato a un predefinito per messaggi, ora puoi modificarlo in modo asincrono. Puoi anche controllare lo stato di aggiornamento di ogni pool IP. [Ulteriori informazioni](configuration/ip-pools.md#edit-ip-pool)

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
<p>Invia automaticamente il messaggio push o e-mail al momento migliore per ogni cliente con cui hai a che fare con Adobe Journey Optimizer. L’ottimizzazione del tempo di invio, basata sui servizi AI di Adobe, prevede il momento migliore per inviare un’e-mail o un messaggio push per massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche preconfigurate.</p>
<p>Al momento questa funzione è disponibile nella versione beta e solo per i clienti beta. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="building-journeys/journeys-message.md#send-time-optimization">documentazione dettagliata</a>.</p>
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
<p>Per ulteriori informazioni, consulta la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentazione dettagliata</a>.</p>
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
<p>Gli URL personalizzati indirizzano i destinatari a pagine specifiche di un sito web o a un microsito personalizzato, a seconda degli attributi del profilo. In Adobe Journey Optimizer, ora puoi aggiungere la personalizzazione agli URL nel contenuto del messaggio. La personalizzazione URL può essere applicata a testo e immagini e utilizzare dati di profilo o dati contestuali.</p>
<p>Per ulteriori informazioni, consulta la <a href="personalization/personalization-syntax.md#perso-urls">documentazione dettagliata</a>.</p>
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
<p>È ora possibile definire il periodo di tempo di un nuovo tentativo su base predefinita, in modo da evitare che i nuovi tentativi vengano eseguiti quando non è più necessario. Ad esempio, puoi impostare il periodo di esecuzione dei nuovi tentativi su 24 ore per un messaggio transazionale di reimpostazione della password contenente un collegamento valido solo per un giorno. Le impostazioni dei nuovi tentativi si applicano solo al canale e-mail.</p>
<p>Per ulteriori informazioni, consulta la <a href="configuration/retries.md#retry-duration">documentazione dettagliata</a>.</p>
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
<p>L’aggiunta di indirizzi e-mail e domini all’elenco di eliminazione è ora disponibile dall’interfaccia utente, uno alla volta o in modalità collettiva tramite un caricamento di file CSV.</p>
<p>Per ulteriori informazioni, consulta la <a href="configuration/manage-suppression-list.md#add-addresses-and-domains">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Miglioramenti

**Percorsi**

* **Intestazioni dinamiche** - È ora possibile trasmettere dati dinamici nei parametri di intestazione HTTP. Questi parametri possono essere utilizzati dai sistemi di integrazione che ricevono le chiamate di azione HTTP del percorso, ad esempio la marca temporale o l’ID di tracciamento. [Ulteriori informazioni](action/about-custom-action-configuration.md#url-configuration)
* **Percorsi URL dinamici** - È ora possibile impostare percorsi URL dinamici per le azioni personalizzate. [Ulteriori informazioni](action/about-custom-action-configuration.md#url-configuration)
* Il tasso di limitazione complessivo per i segmenti letti è stato modificato da 17.000 a 20.000 messaggi al secondo. [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interfaccia utente**

* **Ricerca** - In ogni pagina, è ora possibile cercare oggetti aziendali e aiutare gli articoli direttamente dal campo di ricerca Unified Experience Cloud. [Ulteriori informazioni](user-interface.md#unified-search)
* **Recenti** - La visualizzazione degli elementi recenti della home page di Adobe Journey Optimizer è ora estesa ad altri oggetti aziendali. Con questo aggiornamento, le scelte rapide per l&#39;accesso recente includono Messaggi, Percorsi, Segmenti, Schemi, Set di dati, Origini dati, Eventi, Azioni, Origini e Destinazioni. [Ulteriori informazioni](action/about-custom-action-configuration.md#passing-collection)

**Progettazione dei contenuti**

* **Sfondo** - Le immagini di sfondo sono ora supportate nell’anteprima live. [Ulteriori informazioni](preview.md)
* **Collegamento di rinuncia con un clic** - Puoi inserire un nuovo tipo di collegamento nel contenuto dell’e-mail: la **Rinuncia** Il collegamento consente agli utenti di annullare l’iscrizione alla ricezione delle comunicazioni con un solo clic, senza essere reindirizzati a una pagina di destinazione per confermare la rinuncia. [Ulteriori informazioni](message-tracking.md#one-click-opt-out-link)

**Personalizzazione**

* **Editor espressioni** - È ora possibile aggiungere facilmente un valore di fallback durante la definizione della personalizzazione: quando il campo di personalizzazione è vuoto per un profilo, viene visualizzato il valore di fallback. [Ulteriori informazioni](personalization/functions/helpers.md)

**Configurazione e-mail**

* **Elenco Consentiti** - L’elenco Consentiti può ora essere abilitato e disabilitato in una sandbox non di produzione tramite una chiamata API. [Ulteriori informazioni](allow-list.md#enable-allow-list)
* **Navigazione** - Elenco di soppressione, accessibile sotto **Amministrazione > Canali > Configurazione e-mail > Generale** è stato spostato nel nuovo menu **Elenco di eliminazione** sottomenu, che raccoglie tutte le funzionalità correlate per un accesso più semplice. [Ulteriori informazioni](configuration/manage-suppression-list.md#access-suppression-list)

**Gestione delle decisioni**

* La modalità di aggiunta e configurazione delle rappresentazioni durante la creazione di un’offerta è stata aggiornata per migliorare l’esperienza di utilizzo. In particolare, la libreria Risorse ora viene visualizzata solo quando, per una rappresentazione, si definiscono contenuti di tipo immagine. [Ulteriori informazioni](offers/offer-library/creating-personalized-offers.md#representations)

### Correzioni

* È stato risolto un problema di accessibilità nella navigazione nella scheda dei messaggi.
* È stato risolto un problema di localizzazione nelle etichette di e-mail designer.
* È stato risolto un problema che si verificava selezionando più nodi in un percorso e facendo clic su &#39;Elimina&#39; nel pannello delle proprietà.
* È stato risolto un problema che impediva l&#39;aggiunta di una nuova intestazione a un&#39;azione utilizzata in un percorso.
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
<p>Per ulteriori informazioni, consulta la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentazione dettagliata</a>.</p>
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
<p>Per ulteriori informazioni, consulta la <a href="allow-list.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Il tasso di limitazione complessivo di tutti i segmenti letti eseguiti contemporaneamente nella stessa sandbox è limitato a 17.000 messaggi al secondo. [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* La **Durata della cache** campo rimosso dal riquadro di configurazione dell’origine dati. [Ulteriori informazioni](datasource/about-data-sources.md)
* Per le origini dati esterne, ora viene definita automaticamente una regola di limitazione di 15 chiamate al secondo. [Ulteriori informazioni](configuration/external-systems.md#capping)
* Per i percorsi live, nella schermata delle proprietà del percorso vengono ora visualizzate la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso. [Ulteriori informazioni](building-journeys/journey-gs.md#change-properties)
* Nella schermata dell’elenco dei percorsi, è stato aggiunto il filtro del tipo di percorso . [Ulteriori informazioni](user-interface.md#section_lgm_hpz_pgb)
* La **[!UICONTROL Throttling rate]** È stato aggiunto il parametro nell’attività Leggi segmento . [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Anteprima e verifica dei messaggi**

* L’identità e lo spazio dei nomi sono ora visibili nella **[!UICONTROL Preview]** schermo. [Ulteriori informazioni](preview.md#preview-your-messages)
* Il numero di e-mail di test per le bozze è ora limitato a 10.
* Caratteri consentiti per **Prefisso riga oggetto** le bozze ora sono limitate. [Ulteriori informazioni](preview.md#send-proofs)

**Editor di espressioni di personalizzazione**

* L’elenco a discesa helper è stato rinominato e riordinato.

### Correzioni

* È stato risolto un problema che causava la consegna di messaggi duplicati per la consegna di e-mail batch.
* Gli eventi vengono ora generati di conseguenza quando l’invio e-mail non viene eseguito una volta terminato il periodo di esecuzione dei nuovi tentativi.
* È stato risolto un problema a causa del quale le informazioni IP mancavano nella schermata Record PTR.
* È ora implementata la localizzazione nella barra delle offerte nell’editor espressioni.
* È stata corretta la spaziatura errata nei popup delle informazioni.
* È stato risolto un problema in E-mail designer durante il caricamento di un file HTML in cui foglio di stile interno con `background-image` proprietà non supportata.
