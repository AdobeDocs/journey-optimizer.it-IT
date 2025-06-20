---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 8f3d619adfb7b2f3dd876da7a3a6eba1fda6dd6b
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 44%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.


## Note sulla versione di giugno 2025 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Data di rilascio**: giovedì 18 giugno 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

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
<p>Per ulteriori informazioni, consulta la <a href="../sms/sms-configuration.md">documentazione dettagliata</a>.</p>
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
<p>Ora puoi definire campi modificabili specifici nei modelli di contenuto JSON o HTML, che consentono agli utenti non tecnici di modificare facilmente il contenuto in una visualizzazione modulo nell’authoring del canale di esperienza basato sul codice, senza dover manipolare alcun codice.<br />Inoltre, quando definisci i modelli di contenuto dell'esperienza basati su codice ora puoi inserire criteri di decisione nel modello, aumentando la riutilizzabilità e la facilità d'uso.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>Per ulteriori informazioni, consulta la <a href="../code-based/code-based-form-fields.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Attività Content Decision nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi includere offerte personalizzate nei tuoi percorsi tramite un’attività Content Decision dedicata nell’area di lavoro del percorso e utilizzarle nelle attività del percorso, incluse condizioni e azioni personalizzate.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/content-decision.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prova del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Percorsi Dry run è una speciale modalità di pubblicazione del percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di testare un percorso utilizzando dati di produzione reali senza contattare clienti reali o aggiornare le informazioni del profilo. Questa funzione aiuta i professionisti del percorso ad acquisire fiducia nella progettazione del percorso e nel targeting del pubblico prima di pubblicarlo in diretta.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-dry-run.md">documentazione dettagliata</a>.</p>

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
<img src="assets/do-not-localize/PauseResume.gif">
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-pause.md">documentazione dettagliata</a>.</p>
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
<p>Per “scalare il vincitore della sperimentazione” si intende presentare automaticamente o manualmente la variante vincente di un esperimento a tutto il pubblico. Questa funzione assicura che, una volta identificata la variante dalle prestazioni migliori, sia possibile massimizzarne la portata e l’efficacia senza una costante supervisione manuale.</p>
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

   * **Intervallo di durata personalizzato** per la limitazione - Nella schermata di configurazione dei set di regole di canale è ora disponibile un nuovo campo **Ogni**, che consente di applicare le regole della limitazione della frequenza su più giorni, settimane o mesi, a seconda della durata specificata.

   * **Frequenza limite di reimpostazione oraria** - È ora possibile applicare il limite su base oraria per i set di regole del canale. Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Contatta l’assistenza clienti per l’attivazione.

   * **Durata giornaliera** - Precedentemente disponibile in Disponibilità limitata, il limite di frequenza &quot;Giornaliero&quot; nei set di regole del canale è ora disponibile per tutti i clienti.

  Per ulteriori informazioni, consulta la [documentazione dettagliata](../conflict-prioritization/channel-capping.md).

* **Esperienze basate su codice**

   * L’aggiunta di un criterio decisionale è ora disponibile nei modelli di contenuto di esperienza basati su codice, dove può essere utilizzato per sfruttare le offerte nei campi di modulo modificabili. [Ulteriori informazioni](../code-based/code-based-form-fields.md)

   * Dalla schermata del percorso di esperienze basato sul codice o dell’edizione di una campagna, ora puoi aggiungere direttamente un criterio di decisione senza aprire l’editor di personalizzazione. [Ulteriori informazioni](../code-based/create-code-based.md#edit-code)

* **Supporto CSS personalizzato in E-mail Designer**

  Journey Optimizer ora consente di aggiungere CSS personalizzati al contenuto delle e-mail direttamente all’interno di E-mail Designer. [Ulteriori informazioni](../email/custom-css.md)

* **Nuova navigazione a schede per le campagne**

  Un nuovo modello di navigazione consente un accesso più rapido all’authoring dei contenuti e supporta un’ulteriore espansione delle impostazioni tra le campagne. [Ulteriori informazioni](../campaigns/create-campaign.md)

* **Decisioning** - Data di disponibilità: 3 giugno 2025

  Ora è possibile copiare gli oggetti decisionali in sandbox diverse, semplificando i test e i flussi di lavoro di implementazione. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Supporto degli attributi di elementi decisionali per le regole decisionali** - Data di disponibilità: 4 giugno 2025

  Ora puoi sfruttare gli attributi degli elementi decisionali per creare regole decisionali. [Ulteriori informazioni](../experience-decisioning/rules.md#create)

* **Aggiornamento API per l’esecuzione messaggi interattivi** - Data di disponibilità: 6 giugno 2025

  L’API per l’esecuzione dei messaggi interattivi ora consente di eliminare la pianificazione per l’esecuzione delle campagne successive. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
