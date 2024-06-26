---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione 2024
description: Note sulle versioni 2024 di Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '2229'
ht-degree: 100%

---

# Note sulla versione 2024 {#release-notes-2024}

In questa pagina sono elencate tutte le funzioni e i miglioramenti di [!DNL Journey Optimizer] rilasciati nel 2024.



## Note sulla versione di maggio 2024 {#may-2024}

**Data di rilascio**: 21-22 maggio 2024

### Nuove funzionalità {#e-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Decisioni per le esperienze: disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione Decisioni per le esperienze semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti.</p>
<p>Questi elementi decisionali sono integrati direttamente in un’ampia gamma di superfici in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne di Journey Optimizer. I criteri decisionali relativi alla funzione Decisioni per le esperienze sono disponibili per l’utilizzo solo in campagne di esperienza basate su codice.</p>
<p>La funzione Decisioni per le esperienze è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/gs-experience-decisioning.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalizzazione della superficie e-mail: disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire sottodomini dinamici e parametri di intestazione personalizzati durante la creazione di superfici di canale e-mail, per maggiore flessibilità e controllo sulle impostazioni e-mail.</p>
<p>La personalizzazione della superficie e-mail è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../email/surface-personalization.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Decisioni per le esperienze**: disponibilità limitata

Dalla versione beta a quella con Disponibilità limitata, sono stati aggiunti i seguenti miglioramenti:

* **Decisioni per le esperienze + Esperienze basate su codice**: ora puoi sfruttare la funzione Decisioni per le esperienze per utilizzare gli elementi decisionali nelle campagne basate su codice. Nota: il canale di esperienza basato su codice e la funzione Decisioni per le esperienze non sono disponibili per le organizzazioni che hanno acquistato le offerte aggiuntive Healthcare Shield e Privacy and Security Shield di Adobe. [Ulteriori informazioni](../code-based/get-started-code-based.md)
* **Dati contestuali**: ora puoi sfruttare i dati contestuali provenienti da Adobe Experience Platform nelle regole di decisione e nelle formule di classificazione. [Ulteriori informazioni](../experience-decisioning/context-data.md)
* **Nuova autorizzazione**: è ora disponibile la nuova autorizzazione “Gestisci decisioni per le esperienze” per la risorsa Gestione delle decisioni. Questa consente di gestire i diritti relativi alla funzione Decisioni per le esperienze. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md)
* **Regole di limitazione**: ora, in Decisione per le esperienze, è possibile aggiungere più regole di limitazione per un determinato elemento in Decisioni per le esperienze. Ciò offre un maggiore controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../experience-decisioning/items.md#capping)
* **Reporting**: ora puoi creare dashboard di reporting personalizzate delle campagne di Decisioni per le esperienze tramite [!DNL Customer Journey Analytics]. [Ulteriori informazioni](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canale e-mail**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Punteggio contenuto indesiderato** (beta): ora puoi controllare il punteggio del contenuto indesiderato in un rapporto relativo dedicato. Utilizzando SpamAssassin, Adobe Journey Optimizer può ora testare il contenuto delle e-mail e assegnargli un punteggio per indicare se gli ISP o i provider di caselle postali lo considereranno come contenuto indesiderato o meno. [Ulteriori informazioni](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Questa funzionalità è disponibile nella versione beta e solo per clienti beta. Per partecipare al programma Beta, contatta il tuo rappresentante Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Percorsi**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Supporto mTLS**: l’autenticazione mTLS è ora supportata nelle azioni personalizzate. Non è necessaria alcuna configurazione aggiuntiva nell’azione o nel percorso personalizzato per attivare mTLS; l’attivazione viene eseguita automaticamente quando viene rilevato un endpoint abilitato per mTLS. [Ulteriori informazioni](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tabelle di ricerca negli eventi**: è ora possibile sfruttare i dati di un set di dati di ricerca quando una relazione è stata definita utilizzando un attributo all’interno di un array di oggetti. I valori di ricerca saranno disponibili nei percorsi (condizioni, azioni personalizzate, ecc.) e nella personalizzazione dei messaggi. [Ulteriori informazioni](../event/experience-event-schema.md#relationships_limitations)
* **Editor di espressioni avanzate nella configurazione dell’evento** (Disponibilità limitata): è ora possibile sfruttare l’editor di espressioni avanzate durante la configurazione di un evento, consentendoti di definire espressioni più complesse o utilizzare funzioni nella condizione per l’ID evento. Questa funzionalità viene rilasciata in Disponibilità limitata per clienti selezionati. [Ulteriori informazioni](../event/about-creating.md#adv-exp-editor)
* **Criteri di unione** (Disponibilità limitata): i criteri di unione utilizzati da un percorso sono ora visibili e coerenti in tutto il percorso. Questa funzionalità viene rilasciata in Disponibilità limitata per clienti selezionati. [Ulteriori informazioni](../building-journeys/journey-properties.md#merge-policies)

**Globalizzazione**

Come parte del nostro impegno continuo per offrire un’esperienza utente unificata, armonizziamo la terminologia utilizzata nei prodotti e nelle app di Adobe Experience Cloud. Questo influisce sul termine tedesco “Titel” che viene modificato in “Label” quando si riferisce al nome di un oggetto. Le modifiche verranno implementate progressivamente nell’interfaccia utente e nella documentazione.




## Note sulla versione di aprile 2024 {#apr-2024}

**Data di rilascio**: 2 maggio 2024

### Nuove funzionalità {#apr-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service): tutti i provider</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il canale SMS, ora è possibile migliorare le comunicazioni inviando messaggi MMS (Multimedia Message Service), che consentono di condividere immagini, GIF o video con la clientela. Inizialmente disponibile solo con Sinch, la funzione MMS è ora disponibile anche con Infobip e Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Designer del percorso e rapporti live migliorati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione include un’interfaccia utente dell’area di lavoro migliorata per i percorsi e offre un’esperienza utente più intuitiva ed efficiente. Le attività sono più chiare e nell’area di lavoro del percorso è possibile ottenere più informazioni con meno clic.</p>
<img src="assets/new-canvas3.gif"/>
<p>Oltre al design migliorato dell’area di lavoro del percorso, è stata introdotta la possibilità di visualizzare le metriche di reporting delle ultime 24 ore direttamente nell’area di lavoro del percorso. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>Nota</strong>: a partire dalla versione di aprile, queste modifiche verranno gradualmente implementate in tutti gli ambienti.</p>
<p>Per ulteriori informazioni, consulta la <a href="new-canvas.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Miglioramenti {#apr-improvements}

Questa versione include i miglioramenti elencati di seguito.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Configurazione**

* Ora puoi selezionare un’azione di marketing al livello della superficie di canale. Se utilizzati in una superficie, tutti i criteri di consenso associati a tale azione di marketing vengono usati per rispettare le preferenze della clientela. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)
* Per le superfici di canale è ora possibile controllare l’accesso a livello di oggetto. [Ulteriori informazioni](../configuration/channel-surfaces.md#create-channel-surface)
* Mentre abiliti l’elenco di annullamenti dell’abbonamento in una superficie di canale, ora puoi definire il livello di consenso in base a come gestisci il consenso da tutte le altre origini. [Ulteriori informazioni](../email/email-settings.md#list-unsubscribe)

**Gestione dei contenuti**

* Ora puoi simulare modelli di contenuto per tutti i canali. [Maggiori informazioni](../content-management/content-templates.md#test-templates)

**Personalizzazione**

* La nuova funzione helper **toInt** è disponibile nell’editor di espressioni. Ti consente di convertire uno qualsiasi di questi tipi (numero, doppio, int, lungo, mobile, corto, byte, booleano, stringa) in un numero intero. [Ulteriori informazioni](../personalization/functions/math.md#to-int)



## Note sulla versione di marzo 2024 {#mar-2024}

**Data di rilascio**: 19-20 marzo 2024

### Nuova funzionalità {#mar-features}

Questa versione include la nuova funzionalità descritta di seguito.

<table>
<thead>
<tr>
<th><strong>Esperienze basate su codice</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il nuovo canale di esperienza basato su codice, Adobe Journey Optimizer consente di eseguire personalizzazioni e test avanzati per qualsiasi proprietà in entrata, facilitando la consegna diretta di esperienze personalizzate in diversi punti di contatto come app web, app mobili, app desktop, console video, dispositivi connessi per TV, smart TV, chioschi, sportelli bancomat, dispositivi IoT e altro ancora.</p>
<P>Le funzionalità principali includono:</p>
<ul><li> Personalizzazione universale: estende le esperienze personalizzate in tutti i punti di contatto, garantendo un percorso utenti coeso e personalizzato</li>
<li>Precisione granulare nella modifica: modifica contenuti specifici in singole posizioni all’interno delle app o delle pagine web</li>
<li>Implementazione versatile: supporto per metodi di implementazione lato server, basati su API o SDK per l’integrazione diretta con l’ambiente di sviluppo.</li></ul></p>
<p>Per ulteriori informazioni, consulta la <a href="../code-based/get-started-code-based.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### Miglioramenti {#mar-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Modelli di contenuto**

* **Miniature**: per i modelli di contenuto è ora disponibile la modalità **Vista a griglia**, in cui vengono visualizzate miniature dei modelli per agevolarne l’accesso visivo. Al momento sono supportati solo i modelli per e-mail HTML. [Ulteriori informazioni](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Questa funzionalità viene rilasciata in Disponibilità limitata (LA) per un set limitato di clienti.

**Percorsi**

Sono stati aggiunti nuovi stati intermedi al ciclo di vita di authoring del percorso:

* Stato **Pubblicazione** tra gli stati **Bozza** e **Live**
* Stato **Interruzione** tra gli stati **Live** e **Interrotto**
* Stati **Attivazione modalità di test** o **Disattivazione modalità di test** tra gli stati **Bozza** e **Bozza (test)**

Quando un percorso si trova in uno stato intermedio, è di sola lettura. [Ulteriori informazioni](../building-journeys/journey-gs.md#filter)

## Note sulla versione di febbraio 2024 {#feb-2024}

**Data di rilascio**: 21-22 febbraio 2024

### Nuove funzionalità{#feb-features}

Questa versione include le nuove funzionalità elencate di seguito.


<table>
<thead>
<tr>
<th><strong>Messaggistica web in-app</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi utilizzare la nuova funzionalità di messaggistica web in-app per visualizzare contenuti personalizzati direttamente sui siti web tramite messaggi di sovrapposizione modale. Questa funzione consente di interagire in modo efficace con i visitatori web, migliorando l’interazione, la conservazione e i tassi di conversione degli utenti.<br/><br/></p>
<p>Per ulteriori informazioni, consulta la <a href="../in-app/create-in-app-web.md">documentazione dettagliata</a>.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modelli di contenuto multicanale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oltre all’e-mail, ora sono disponibili modelli di contenuto per i seguenti canali: push, in-app, SMS e direct mail, ciascuno dei quali dispone di tipi di modello dedicati. Per l’e-mail, ora puoi selezionare il tipo di contenuto, che consente di salvare l’oggetto come parte del modello dell’e-mail. <br/><br/></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-templates.md">documentazione dettagliata</a>.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### Miglioramenti {#feb-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Tipi di pubblico**

* **Elenchi seed**: quando si utilizzano gli **elenchi seed**, adesso sono supportate le varianti. Gli indirizzi seed ricevono una copia di tutte le varianti dello stesso messaggio (come i diversi trattamenti di un esperimento di contenuto). [Ulteriori informazioni](../configuration/seed-lists.md)

Precedentemente disponibili in versione beta, i seguenti miglioramenti sono ora disponibili per tutti gli utenti:

* Ora puoi eseguire il targeting dei **tipi di pubblico creati tramite la composizione del pubblico** e sfruttare gli attributi di arricchimento nei percorsi. [Ulteriori informazioni](../building-journeys/read-audience.md)

* Ora puoi eseguire il targeting di **tipi di pubblico caricati da un file CSV** nei percorsi e nelle campagne. [Ulteriori informazioni](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* L’utilizzo di tipi di pubblico e attributi dalla composizione del pubblico e dal caricamento personalizzato (file CSV) non è attualmente disponibile per l’utilizzo con Healthcare Shield o Privacy and Security Shield.
  >* Il miglioramento del **caricamento del pubblico da un file CSV** verrà introdotto gradualmente nel corso di alcuni giorni successivi alla versione iniziale. Mentre alcuni utenti hanno accesso immediato, altri potrebbero notare un ritardo prima che questo diventi disponibile nel loro ambiente.

**Percorsi**

* **Filtrare i percorsi**: è ora possibile utilizzare inventari di **date personalizzate per filtrare i percorsi**, oltre ai filtri di data predefiniti esistenti. Questo consente di perfezionare l’elenco visualizzando i percorsi creati o pubblicati in una data specifica, all’interno di un mese specifico, durante un anno intero o compresi in intervalli di tempo specifici. [Ulteriori informazioni](../building-journeys/journey-gs.md#filter)
* **Azioni personalizzate**: ora puoi aggiornare l’intestazione **content-type**. Questo nuovo **content-type** dovrebbe fare riferimento al contenuto JSON. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)
* **Configurazione**: l’attributo identityMap in stepEvents ora è precompilato. L’identità primaria è definita come “primary = true”. [Ulteriori informazioni](../reports/sharing-field-list.md)
* **Interfaccia utente**: la barra superiore, nelle schermate del percorso, è stata riorganizzata per offrire un’esperienza migliorata. Tra i diversi aggiornamenti, l’icona a forma di “matita” che consente di accedere alle proprietà del percorso è ora visualizzata a sinistra della barra superiore, accanto al nome del percorso. [Ulteriori informazioni](../building-journeys/journey-properties.md)

**Canale SMS**

* **Parole chiave di consenso/rinuncia**: durante la configurazione del canale SMS, ora puoi personalizzare le **parole chiave di consenso e rinuncia** in base alle tue preferenze. Journey Optimizer attiva la risposta in base a queste parole chiave specificate. [Ulteriori informazioni](../sms/sms-configuration.md)

**Campagne**

* **Campagne attivate da API**: è stato migliorato il codice cURL generato dopo l’attivazione di una campagna attivata da API. Ora include tutte le variabili di personalizzazione (profilo e contesto) utilizzate nel messaggio. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md#execute)

**Regole di frequenza**

* Oltre a e-mail e push, ora puoi creare regole di frequenza per i canali SMS e Direct Mail. Le regole di frequenza escludono automaticamente i profili sollecitati eccessivamente dai messaggi e dalle azioni quando viene raggiunta la quota limite. [Ulteriori informazioni](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Note sulla versione di gennaio 2024 {#jan-2024}

**Data di rilascio**: 30-31 gennaio 2024

### Nuove funzionalità{#jan24-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Aggiornamenti del recapito dei messaggi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora supporta la tecnologia di autenticazione DMARC.</p>
<p>A partire dal 1 febbraio 2024, Google e Yahoo richiedono di disporre di un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail. Assicurati di aver impostato il record DMARC per tutti i sottodomini che hai delegato o stai delegando ad Adobe in Journey Optimizer.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/dmarc-record-update.md">documentazione dettagliata</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usare i playbook sui casi d’uso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sfrutta un catalogo di playbook sui casi d’uso specifici del settore in Real-Time CDP e Journey Optimizer per risolvere casi d’uso comuni che è possibile eseguire utilizzando Adobe Experience Platform e Adobe Journey Optimizer.</p><p>Dopo aver scelto il playbook più adatto alle tue esigenze, puoi abilitarlo per generare le risorse necessarie per supportare il caso d’uso, ad esempio percorsi, messaggi, schemi o segmenti, e personalizzarle nel tuo schema per velocizzare il time-to-value.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/playbooks.md">documentazione dettagliata</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Miglioramenti {#jan24-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Reporting**

* **Nuovi widget di raggruppamento basati su dominio**: sono stati aggiunti nuovi widget per migliorare i rapporti di Campaign e Journey. I widget **Motivi di mancato recapito per dominio**, **Inviato e consegnato da domini**, **Aperture e clic per dominio** e **Mancato recapito ed errori per dominio** forniscono un raggruppamento dettagliato a livello di dominio per le metriche chiave di consegna e tracciamento delle e-mail. [Ulteriori informazioni](../reports/channel-report.md)

**Canale SMS**

* **Doppio consenso**: il flusso di lavoro do doppio consenso per SMS garantisce che gli utenti acconsentano esplicitamente alla ricezione di messaggi quando la richiesta viene avviata dal proprio dispositivo. Gli utenti avviano il processo di consenso inviando un messaggio SMS in entrata. Una volta confermato il consenso, viene inviato un messaggio di follow-up con la richiesta di verifica finale. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. [Ulteriori informazioni](../sms/sms-configuration.md)

  Questa funzionalità è disponibile con i provider per SMS Sinch e Infobip.

**Percorsi**

* **Durata eventi di reazione** - La durata massima che puoi definire negli **eventi di reazione** è ora di 29 giorni anziché di 30. [Ulteriori informazioni](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Leggi pubblico**: l’attività **Leggi pubblico** ora si basa sul set di dati dello snapshot del profilo per i segmenti batch, che viene generato solo una volta al giorno dopo l’esecuzione del processo batch giornaliero pianificato, pertanto i dati verranno aggiornati fino all’ultimo processo batch giornaliero. [Ulteriori informazioni](../building-journeys/read-audience.md)

* **Gruppi di campi**: questa versione risolve un problema che in alcuni casi impediva il salvataggio dei gruppi di campi.

* Il supporto a `<listObject>` è stato modificato in più funzioni.

**Regole di frequenza**

* **Quota limite settimanale**: è ora possibile specificare il numero massimo di messaggi inviati a un profilo cliente in una settimana, oltre a quelli inviati in un mese. La quota limite si basa sul periodo di calendario selezionato e viene reimpostata all’inizio dell’intervallo di tempo corrispondente. [Ulteriori informazioni](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >Su richiesta, è disponibile anche l’opzione di durata giornaliera. Contatta il tuo rappresentante Adobe.

**Gestione delle decisioni**

* **Quota limite su Edge**: il contatore della quota limite ora è aggiornato e disponibile in una decisione API Edge Decisioning in meno di 3 secondi. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
