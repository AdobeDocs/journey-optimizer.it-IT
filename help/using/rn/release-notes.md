---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9845e8ca89943b7c2bb7d236cac5e30aa2b01e23
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 62%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.



## Note preliminari sulla versione del 25 giugno {#25-6-rn}


**Le note preliminari sulla versione riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata sono pubblicati alla data di rilascio.

**Data di rilascio**: 17-18 giugno 2025


### Nuove funzionalità {#25-06-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.


<table>
<thead>
<tr>
<th><strong>Messaggistica RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La messaggistica RCS (Rich Communication Services) è ora supportata in Journey Optimizer, consentendo le seguenti funzionalità di messaggistica avanzate soggette al supporto di provider e gestori:</p>
<ul>
<li>Supporto per mittenti con marchio e verificati: invia messaggi utilizzando profili aziendali verificati con elementi di branding (logo, nome del mittente, ecc.).</li>
<li>Informazioni sulla consegna dei messaggi: puoi ricevere rapporti di consegna dettagliati, inclusi gli aggiornamenti sullo stato del messaggio (ad esempio inviato, consegnato, letto).</li>
<li>Tracciamento dei collegamenti: incorpora e tieni traccia degli URL nei messaggi RCS per l’analisi del coinvolgimento.</li>
<li>Fallback a SMS: fallback automatico a SMS quando il dispositivo del profilo non supporta RCS o è temporaneamente non raggiungibile tramite RCS.</li>
<li>Composizione di base dei messaggi: invia messaggi RCS basati su testo con file multimediali facoltativi ed elementi avanzati, a seconda del supporto del provider.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campi modulo nel contenuto dell’esperienza basata su codice</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire campi modificabili specifici nei modelli di contenuto JSON o HTML, che consentono agli utenti non tecnici di modificare facilmente il contenuto in una visualizzazione modulo nell’authoring del canale di esperienza basato sul codice, senza dover manipolare alcun codice. Inoltre, quando definisci i modelli di contenuto dell’esperienza basati su codice ora puoi inserire criteri di decisione nel modello, aumentando la riutilizzabilità e la facilità d’uso.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Metodo di delega personalizzato per sottodomini</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oltre alla delega completa e al metodo CNAME, ora è disponibile un nuovo metodo di configurazione del sottodominio: il metodo di delega personalizzata, che consente di gestire e controllare tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento dei messaggi.</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Attività Content Decisioning nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi includere offerte personalizzate nei tuoi percorsi tramite un’attività Content Decisioning dedicata nell’area di lavoro del percorso e utilizzarle nelle attività del percorso, incluse condizioni e azioni personalizzate.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esecuzione di prova del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Percorsi Dry run è una speciale modalità di pubblicazione del percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di testare un percorso utilizzando dati di produzione reali senza contattare clienti reali o aggiornare le informazioni del profilo. Questa funzione aiuta i professionisti del percorso ad acquisire fiducia nella progettazione del percorso e nel targeting del pubblico prima di pubblicarlo in diretta.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sospendi e riprendi percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile sospendere e riprendere i percorsi. Questa funzionalità offre ai professionisti del percorso maggiore controllo e flessibilità, consentendo la sospensione temporanea dei percorsi live senza interrompere la customer experience. Quando è in pausa, non vengono inviate comunicazioni e i profili rimangono in stato di sospensione fino alla ripresa del percorso.</p>
<p>È possibile sospendere e riprendere un solo percorso oppure eseguire le operazioni di pausa collettiva e ripresa di un gruppo di percorsi.</p>
<p>Inoltre, puoi applicare filtri globali ai percorsi in pausa per escludere i profili in base ai loro attributi.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Scalare il vincitore della sperimentazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Scalabilità del vincitore della sperimentazione consente di distribuire automaticamente o manualmente la variante vincente di un esperimento al pubblico completo. Questa funzione assicura che, una volta identificata la variante dalle prestazioni migliori, sia possibile massimizzarne la portata e l’efficacia senza una costante supervisione manuale.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-experiment.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 giugno 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflitti e assegnazione delle priorità</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, è essenziale gestire il volume e la tempistica delle campagne e dei percorsi per evitare di sopraffare la clientela con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e l’assegnazione delle priorità. In precedenza disponibili solo per le organizzazioni con accesso alle funzionalità rilasciate con disponibilità limitata (LA), questi sono ora disponibili per tutti (GA, disponibilità generale).</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti. Con questa versione con disponibilità generale sono stati introdotti i seguenti miglioramenti:</p>
<ul>
<li>Supporto esteso: gli strumenti per la gestione dei conflitti ora supportano sia i percorsi unitari che i percorsi di qualificazione di un pubblico, oltre ai percorsi Leggi pubblico.</li>
<li>Risoluzione dei problemi migliorata: nel servizio query sono ora disponibili due nuovi campi evento del passaggio che consentono di analizzare il motivo per cui un profilo è stato rifiutato da un percorso o da una campagna.</li>
<li>Rapporti migliorati: i rapporti ora indicano la regola specifica che ha determinato l’esclusione di un profilo da un percorso o da una campagna, fornendo maggiore trasparenza e informazioni actionable.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 giugno 2025</p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#25-06-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

* **Set di regole canale**

   * **Intervallo di durata personalizzato** per il limite - Nella schermata di configurazione dei set di regole di canale è ora disponibile un nuovo campo **Conteggio ripetizioni** che consente di applicare le regole del limite di frequenza su più giorni, settimane o mesi, a seconda della durata specificata.

   * **Durata oraria** - È ora possibile applicare il limite su base oraria per i set di regole del canale.

* **Esperienze basate su codice**

  I criteri di decisione sono ora disponibili nei modelli di contenuto di esperienza basati su codice e nella barra a destra dell’editor di codice.

* **E-mail Designer**

   * **Supporto CSS personalizzato** - Journey Optimizer ora consente di aggiungere CSS personalizzato al contenuto delle e-mail direttamente all&#39;interno di E-mail Designer.
   * **Supporto modalità scura** - La finestra di progettazione e-mail di Journey Optimizer offre ora la possibilità di passare alla modalità scura in cui è possibile definire impostazioni specifiche.


* **Decisioning** - Data di disponibilità: 3 giugno 2025

  Ora è possibile copiare gli oggetti decisionali in sandbox diverse, semplificando i test e i flussi di lavoro di implementazione. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Supporto degli attributi degli elementi di decisione per le regole di decisione** - Data di disponibilità: 4 giugno 2025

  Ora puoi sfruttare gli attributi degli elementi di decisione per creare regole di decisione. [Ulteriori informazioni](../experience-decisioning/rules.md#create)

* **Aggiornamento API di esecuzione messaggi interattivi** - Data di disponibilità: 6 giugno 2025

  L’API di esecuzione interattiva dei messaggi ora consente di eliminare la pianificazione della prossima esecuzione delle campagne. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}

## Note sulla versione di maggio 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Nuove funzionalità {#25-05-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Vista calendario per l’inventario delle campagne e dei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Negli elenchi dei percorsi e delle campagne è ora disponibile una vista calendario. Consente di visualizzare tutte le attivazioni dei percorsi e delle campagne nei rispettivi elenchi.</p>
<p>Questa modifica è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per richiedere l'accesso, usa <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">questo modulo</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Per ulteriori informazioni, consulta le seguenti sezioni: <a href="../building-journeys/journey-ui.md">Sfoglia e filtra i tuoi percorsi</a>, <a href="../campaigns/modify-stop-campaign.md">Accedi alle campagne</a>.</p>
<p>Data di disponibilità: giovedì 28 maggio 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazione dei frammenti di contenuto di Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con l’integrazione di Adobe Experience Manager e Adobe Journey Optimizer, ora puoi utilizzare i frammenti di contenuto di Adobe Experience Manager all’interno dei contenuti Journey Optimizer. Questa connessione semplifica l’accesso e l’utilizzo dei contenuti AEM direttamente in Journey Optimizer.</p>
<p>Precedentemente disponibile per un set limitato di organizzazioni (LA), questa funzionalità è ora disponibile in versione GA con i seguenti miglioramenti: ora puoi definire segnaposto e mappare valori di personalizzazione all’interno della firma del frammento utilizzando la modalità Editor.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Per ulteriori informazioni, consulta la <a href="../integrations/aem-fragments.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 23 maggio 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazione di Adobe Experience Manager Dynamic Media</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le risorse Dynamic Media sono ora direttamente disponibili e accessibili in Journey Optimizer. Questa integrazione consente di:</p>
<ul>
<li>Gestire in maniera centralizzata le risorse con aggiornamenti in tempo reale</li>
<li>Modificare all’istante le impostazioni delle risorse, ad esempio larghezza e altezza</li>
<li>Personalizzare i modelli Dynamic Media aggiornando i contenuti e aggiungendo campi di personalizzazione</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/aem-dynamic.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 23 maggio 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>ID supplementare per percorsi attivati da eventi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi attivare i percorsi utilizzando un ID profilo insieme a un altro identificatore, ad esempio un ID ordine, un ID abbonamento o un ID prescrizione, affinché un profilo possa nello stesso percorso più volte allo stesso tempo. Questo consente scenari come la gestione di più ordini o abbonamenti in parallelo, con ogni istanza che segue il proprio iter lungo il percorso.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/supplemental-identifier.md">documentazione dettagliata</a>.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Data di disponibilità: 23 maggio 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulare varianti di contenuto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti. Con la versione in disponibilità generale, la funzione ora include il supporto per contenuti multilingue ed esperimenti sui contenuti, consentendo di testare le varianti per diverse lingue e trattamenti. Inoltre, ora supporta gli attributi contestuali (oltre agli attributi di profilo), consentendo test di contenuto ancora più dinamici e situazionali.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/simulate-sample-input.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 23 maggio 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sincronizzare la pianificazione Leggi pubblico con il processo di segmentazione in batch</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi attivare esecuzioni giornaliere di un percorso dopo il completamento della segmentazione in batch. Questa opzione è ora disponibile nei percorsi con pianificazione giornaliera per tutta la clientela. L’opzione consente di definire un intervallo di tempo massimo di 6 ore per l’attesa dei dati del pubblico dai processi di segmentazione in batch, in modo che i percorsi vengano eseguiti con i dati più aggiornati o che vengano ignorati se non sono pronti.</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/read-audience.md#schedule">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: mercoledì 20 maggio 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Provider SMS personalizzato</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di configurare altri provider SMS oltre alle opzioni predefinite: Sinch, Infobip e Twilio. Con la configurazione del provider SMS personalizzato, puoi integrare direttamente provider di terze parti, sfruttare la personalizzazione avanzata del payload per la messaggistica dinamica e gestire le preferenze di consenso (consenso/rinuncia) per garantire la conformità.</p>
<p>Per ulteriori informazioni, consulta la <a href="../sms/sms-configuration-custom.md">documentazione dettagliata</a>.</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Data di disponibilità: mercoledì 20 maggio 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temi in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi applicare rapidamente temi preapprovati per garantire la coerenza del brand in tutte le e-mail, velocizzare il processo di creazione delle campagne e creare e-mail di alta qualità in modo indipendente, riducendo al contempo la dipendenza dai team di design.</p>
<p>Questa funzionalità è disponibile attualmente in versione beta e solo per la clientela beta. Per partecipare al programma Beta, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Per ulteriori informazioni, consulta la <a href="../email/apply-email-themes.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 14 maggio 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning: nuovo generatore di formule basato sull’IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare formule di classificazione di decisioning specifiche definendo e combinando i criteri da una nuova interfaccia migliorata. Invece di usare soltanto una priorità di offerta statica, tramite un’interfaccia guidata puoi definire formule di classificazione personalizzate combinando punteggi di modelli IA, priorità di offerta, attributi di profilo, attributi di offerta e segnali contestuali.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/exd-ranking-formulas.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 14 maggio 2025</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#25-05-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.


* **Supporto di nuovi oggetti Campaign per la copia sandbox** - Data di disponibilità: 15 maggio 2025

  Quando si copiano le campagne in più sandbox utilizzando le funzionalità di esportazione e importazione dei pacchetti, ora vengono copiate anche le seguenti dipendenze: configurazioni dei canali, varianti e impostazioni di esperimenti, criteri ed elementi decisionali. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md)

* **Cartelle per pagine di destinazione** - Data di disponibilità: 9 maggio 2025

  Per gestire facilmente le pagine di destinazione, ora puoi utilizzare le cartelle per organizzarle in modo più efficace in una gerarchia strutturata. [Ulteriori informazioni](../landing-pages/manage-lp.md)

* **Direct mail: supporto per chiave SSH per connessioni SFTP** - Data di disponibilità: 5 maggio 2025

  Nella configurazione di indirizzamento dei file Direct Mail, oltre all’opzione SFTP esistente con tipo di autenticazione tramite password, ora puoi esportare il file direct mail in un server SFTP con autenticazione tramite chiave SSH. [Ulteriori informazioni](../direct-mail/direct-mail-configuration.md)

* **Attivazione della modalità Pillole per la personalizzazione** - Data di disponibilità: 5 maggio 2025

  All’editor di personalizzazione è stato aggiunto un nuovo pulsante “Pillole”. Quando è abilitato, gli attributi contestuali e di profilo vengono visualizzati come pillole, migliorando la leggibilità del codice. [Ulteriori informazioni](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Questa funzionalità verrà implementata gradualmente in tutti gli ambienti nei prossimi 30 giorni.

* Supporto di &quot;Reindirizzamento all&#39;URL&quot; di **nel canale Web** - Data di disponibilità: 20 maggio 2025

  Il canale web in Journey Optimizer ora consente di reindirizzare i visitatori a un altro URL esistente anziché creare una nuova variante nell’editor visivo. Questa funzionalità può essere utilizzata per eseguire esperimenti confrontando due pagine completamente diverse, anziché modificare solo alcuni elementi all’interno di una pagina. [Ulteriori informazioni](../web/create-web.md#web-redirect-to-url)

* **Cartelle per modelli e frammenti** - Data di disponibilità: 20 maggio 2025

  Le cartelle consentono di organizzare gli oggetti in modo più semplice ed efficace in una gerarchia strutturata. Precedentemente disponibili per alcune organizzazioni (disponibilità limitata), le cartelle sono ora disponibili per tutti gli utenti (disponibilità generale) per gestire i modelli di contenuto e i frammenti. Per ulteriori informazioni, consulta le sezioni [Modelli di contenuto](../content-management/access-content-templates.md#folders) e [Frammenti](../content-management/manage-fragments.md#folders).

* **Tracciamento dei clic nei modelli e-mail** - Data di disponibilità: 20 maggio 2025

  Il tracciamento dei clic sugli elementi `<area>` nelle mappe immagine nel contenuto dell’e-mail è ora supportato in modo nativo in [!DNL Journey Optimizer]. In questo modo, le aree della mappa immagine riceveranno gli stessi wrapper di tracciamento, dati di tracciamento e parametri aggiunti, al pari dei collegamenti ipertestuali standard. [Ulteriori informazioni sul tracciamento dei messaggi](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Barra a destra nell&#39;elenco delle campagne** - Data di disponibilità: 20 maggio 2025

  Nell’elenco delle campagne, quando si seleziona una campagna ora viene aperto un riquadro che ne visualizza i dettagli.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

