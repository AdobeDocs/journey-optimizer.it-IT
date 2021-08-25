---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
source-git-commit: cd077b6f1fd5c81955aec2475dfd8b52aeb23422
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 11%

---


# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Puoi anche consultare gli [Aggiornamenti alla documentazione](documentation-updates.md) più recenti.


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
<p>Invia automaticamente il tuo messaggio push o e-mail al momento migliore per ogni cliente con cui hai a che fare con Adobe Journey Optimizer. L’ottimizzazione del tempo di invio, basata sui servizi AI di Adobe, prevede il momento migliore per inviare un’e-mail o un messaggio push per massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche preconfigurate.</p>
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
<!--
<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

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
<p>Per ulteriori informazioni, consulta la <a href="configuration/retries.md#retry-duration">documentazione dettagliata</a>.</p>
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

* **Intestazioni dinamiche** : è ora possibile trasmettere dati dinamici nei parametri di intestazione HTTP. Questi parametri possono essere utilizzati dai sistemi di integrazione che ricevono le chiamate HTTP dell’azione percorso, ad esempio la marca temporale o l’ID di tracciamento. [Ulteriori informazioni](action/about-custom-action-configuration.md#url-configuration)
* **Percorsi URL dinamici** : ora puoi impostare percorsi URL dinamici per le azioni personalizzate. [Ulteriori informazioni](action/about-custom-action-configuration.md#url-configuration)
* Il tasso di limitazione complessivo per i segmenti letti è stato modificato da 17.000 a 20.000 messaggi al secondo. [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interfaccia utente**

* **Ricerca** : in ogni pagina è ora possibile cercare oggetti aziendali e aiutare gli articoli direttamente dal campo di ricerca Unified Experience Cloud. [Ulteriori informazioni](user-interface.md#unified-search)
* **Recenti**  - La visualizzazione degli elementi recenti dalla home page di Adobe Journey Optimizer è ora estesa ad altri oggetti aziendali. Con questo aggiornamento, le scelte rapide per l&#39;accesso recente includono Messaggi, Percorsi, Segmenti, Schemi, Set di dati, Origini dati, Eventi, Azioni, Origini e Destinazioni. [Ulteriori informazioni](action/about-custom-action-configuration.md#passing-collection)

**Progettazione dei contenuti**

* **Sfondo** : le immagini di sfondo sono ora supportate nell’anteprima live. [Ulteriori informazioni](preview.md)
* **Collegamento**  di rinuncia con un clic: puoi inserire un nuovo tipo di collegamento nel contenuto dell’e-mail: il collegamento  **Opt-** outlink consente agli utenti di annullare l&#39;iscrizione alla ricezione delle tue comunicazioni con un solo clic, senza essere reindirizzati a una pagina di destinazione per confermare la rinuncia. [Ulteriori informazioni](message-tracking.md#one-click-opt-out-link)

<!--**Personalization**

* **Expression Editor** - You can now easily add a fall-back value when defining personalization: when personalization field is empty for a profile, the fall-back value will display. [Learn more](documentation-updates.md)-->

**Configurazione e-mail**

* **Elenco Consentiti** : l’elenco Consentiti ora può essere abilitato e disabilitato su una sandbox non di produzione tramite una chiamata API. [Ulteriori informazioni](allow-list.md#enable-allow-list)

<!--* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](configuration/manage-suppression-list.md#add-addresses-and-domains)-->
<!--* **Navigation** - The suppression list, which was accessible under the **Channels > Email configuration > General** menu, has been moved to the **Channels > Email configuration > Suppression list** menu for easier access. [Learn more](configuration/manage-suppression-list.md#access-suppression-list)-->


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
* Il campo **Durata cache** è stato rimosso dal riquadro di configurazione dell&#39;origine dati. [Ulteriori informazioni](datasource/about-data-sources.md)
* Per le origini dati esterne, ora viene definita automaticamente una regola di limitazione di 15 chiamate al secondo. [Ulteriori informazioni](configuration/external-systems.md#capping)
* Per i percorsi live, nella schermata delle proprietà del percorso vengono ora visualizzate la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso. [Ulteriori informazioni](building-journeys/journey-gs.md#change-properties)
* Nella schermata dell’elenco dei percorsi, è stato aggiunto il filtro del tipo di percorso . [Ulteriori informazioni](user-interface.md#section_lgm_hpz_pgb)
* Il parametro **[!UICONTROL Throttling rate]** è stato aggiunto nell’attività Leggi segmento . [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Anteprima e verifica dei messaggi**

* Identità e spazio dei nomi ora sono visibili nella schermata **[!UICONTROL Preview]** . [Ulteriori informazioni](preview.md#preview-your-messages)
* Il numero di e-mail di test per le bozze è ora limitato a 10.
* I caratteri consentiti per il **prefisso della riga oggetto** nelle bozze sono ora limitati. [Ulteriori informazioni](preview.md#send-proofs)

**Editor di espressioni di personalizzazione**

* L’elenco a discesa helper è stato rinominato e riordinato.

### Correzioni

* È stato risolto un problema che causava la consegna di messaggi duplicati per la consegna di e-mail batch.
* Gli eventi vengono ora generati di conseguenza quando l’invio e-mail non viene eseguito una volta terminato il periodo di esecuzione dei nuovi tentativi.
* È stato risolto un problema a causa del quale le informazioni IP mancavano nella schermata Record PTR.
* È ora implementata la localizzazione nella barra delle offerte nell’editor espressioni.
* È stata corretta la spaziatura errata nei popup delle informazioni.
* È stato risolto un problema in E-mail designer durante il caricamento di un file HTML in cui il foglio di stile interno con proprietà `background-image` non era supportato.

