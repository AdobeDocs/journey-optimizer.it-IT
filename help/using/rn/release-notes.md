---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2dfcbd1631c7fefccaf02782a3218c9a1c1dc7aa
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 96%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

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
* **Interfaccia utente**: la barra superiore, nelle schermate del percorso, è stata riorganizzata per offrire un’esperienza migliorata. Tra i diversi aggiornamenti, l’icona a forma di “matita” che consente di accedere alle proprietà del percorso è ora visualizzata a sinistra della barra superiore, accanto al nome del percorso. [Ulteriori informazioni](../building-journeys/journey-gs.md#change-properties)

**Canale SMS**

* **Parole chiave di consenso/rinuncia**: durante la configurazione del canale SMS, ora puoi personalizzare le **parole chiave di consenso e rinuncia** in base alle tue preferenze. Journey Optimizer attiva la risposta in base a queste parole chiave specificate. [Ulteriori informazioni](../sms/sms-configuration.md#create-api)

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

* **Doppio consenso**: il flusso di lavoro do doppio consenso per SMS garantisce che gli utenti acconsentano esplicitamente alla ricezione di messaggi quando la richiesta viene avviata dal proprio dispositivo. Gli utenti avviano il processo di consenso inviando un messaggio SMS in entrata. Una volta confermato il consenso, viene inviato un messaggio di follow-up con la richiesta di verifica finale. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. [Ulteriori informazioni](../sms/sms-configuration.md#create-api)

  Questa funzionalità è disponibile con i provider per SMS Sinch e Infobip.

**Percorsi**

* **Durata eventi di reazione** - La durata massima che puoi definire negli **eventi di reazione** è ora di 29 giorni anziché di 30. [Ulteriori informazioni](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Leggi pubblico**: l’attività **Leggi pubblico** ora si basa sul set di dati dello snapshot del profilo per i segmenti batch, che viene generato solo una volta al giorno dopo l’esecuzione del processo batch giornaliero pianificato, pertanto i dati verranno aggiornati fino all’ultimo processo batch giornaliero. [Ulteriori informazioni](../building-journeys/read-audience.md)

* **Gruppi di campi**: questa versione risolve un problema che in alcuni casi impediva il salvataggio dei gruppi di campi.

* Il supporto a `<listObject>` è stato modificato in più funzioni.

**Regole di frequenza**

* **Limite di frequenza settimanale** - Ora puoi specificare il numero massimo di messaggi inviati a un profilo cliente alla settimana, oltre al mese. Il limite di frequenza si basa sul periodo di calendario selezionato e viene reimpostato all’inizio dell’intervallo di tempo corrispondente. [Ulteriori informazioni](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >Il limite di frequenza giornaliero è disponibile anche su richiesta. Contatta il rappresentante del tuo Adobe.

**Gestione delle decisioni**

* **Quota limite su Edge**: il contatore della quota limite ora è aggiornato e disponibile in una decisione API Edge Decisioning in meno di 3 secondi. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
