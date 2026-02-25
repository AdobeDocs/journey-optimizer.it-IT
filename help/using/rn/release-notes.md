---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9922f8cfeed40e826142d8201e0a1071a1099d75
workflow-type: tm+mt
source-wordcount: '1598'
ht-degree: 36%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzioni, miglioramenti e correzioni su base continuativa. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti.

A causa di questo modello, le note sulla versione vengono aggiornate prima del successivo rilascio mensile. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Note sulla versione di febbraio 2026 {#feb-26-01-rn}

Le sezioni [Nuove funzionalità](#feb-26-01-features) e [Miglioramenti](#feb-26-01-improv) riguardano le funzionalità già disponibili. Nella sezione [In arrivo](#coming-soon) sono elencate le funzionalità e i miglioramenti pianificati per la versione di febbraio.

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### Nuove funzionalità {#feb-26-01-features}


<!--
<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide real-time updates and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>
-->


<table>
<thead>
<tr>
<th><strong>Attività di azione nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supporta una nuova <strong>attività Azione</strong> generica che consente di configurare sia le azioni singole che i gruppi di azioni in entrata con più azioni, semplificando la configurazione delle azioni nell'area di lavoro del percorso. In particolare, questa nuova funzione consente:</p>
<ul>
<li>una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso;</li>
<li>la capacità di creare gruppi di azioni in entrata con più azioni;</li>
<li>la possibilità di aggiungere l’ottimizzazione a qualsiasi azione del canale incorporata;</li>
<li>Possibilità di aggiungere sia opzioni di sperimentazione che opzioni multilingue a qualsiasi azione.</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-action.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: sabato 20 febbraio 2026</p>
<p><strong>Nota:</strong> tutti i canali nativi sono ora accessibili tramite l'attività del percorso di azioni. Le attività dei canali nativi legacy diventeranno obsolete con la versione di marzo. I percorsi esistenti che includono azioni legacy continueranno a funzionare così come sono, non è richiesta alcuna migrazione.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Invio ondata di messaggi in uscita</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi pianificare i messaggi provenienti da campagne o percorsi Journey Optimizer da consegnare in batch controllati nel tempo.</p>
<p>L’invio ondata offre i seguenti vantaggi:</p>
<ul>
<li>Migliore recapito messaggi: Spread invia nel tempo per contribuire a mantenere una solida reputazione del mittente e ridurre il rischio di essere segnalati come spam.</li>
<li>Controllo del carico: evita di sopraffare i sistemi a valle (ad esempio call center e pagine di destinazione) limitando il numero di messaggi che vengono inviati contemporaneamente.</li>
<li>Casi d’uso complessi e sensibili al tempo: adatti a tipi di pubblico di grandi dimensioni o quando è necessario controllare la tempistica (ad esempio capacità del call center, offerte incrementali o con limiti di tempo).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>In <strong>campagne</strong>, questa funzionalità è disponibile per tutti gli ambienti (disponibilità generale). Per ulteriori informazioni, consulta la <a href="../campaigns/send-using-waves.md">documentazione dettagliata</a>.</p>

<p>In <strong>percorsi</strong>, questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l'accesso, contatta il tuo rappresentante Adobe. Per ulteriori informazioni, consulta la <a href="../building-journeys/send-using-waves.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 19 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Migrare i sottodomini alla delega personalizzata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi migrare i sottodomini utilizzando la modalità di delega CNAME alla delega personalizzata direttamente dall’interfaccia, in modo da soddisfare criteri di sicurezza più severi in linea con le linee guida della tua azienda senza ricreare le configurazioni del canale.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/custom-subdomain-migration.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 19 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale per notifiche push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta <strong>notifiche push web</strong>, espandendo il canale push oltre i dispositivi mobili. Puoi inviare facilmente le notifiche ai <strong>browser di dispositivi mobili e desktop</strong>, per raggiungere la clientela direttamente sui dispositivi senza richiedere un’app. Questo miglioramento consente di coinvolgere gli utenti con messaggi tempestivi e personalizzati in tempo reale, sfruttando gli stessi flussi di lavoro di authoring e le stesse funzionalità di targeting già disponibili per le notifiche push per dispositivi mobili.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Precedentemente rilasciata in Beta, questa funzionalità sarà disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../push/push-configuration-web.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: sabato 13 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività di decisione sui contenuti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova <strong>attività Content Decision</strong> è ora disponibile nell'area di lavoro del percorso per l'integrazione di offerte personalizzate direttamente nei percorsi di clienti. Questa attività ti consente di fornire contenuti basati su decisioni e di fare riferimento a tali offerte in tutto il percorso, in condizioni per la creazione di diramazioni basate sull’idoneità, in azioni personalizzate per il passaggio dei dati delle offerte a sistemi esterni e in altre attività per la creazione di esperienze cliente completamente personalizzate.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/content-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: mercoledì 10 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API per strumenti di migrazione self-service</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le API per gli strumenti di migrazione sono ora disponibili per migrare a livello di programmazione le entità <strong>Gestione decisioni</strong> in <strong>Decisioning</strong>, con:</p>
<ul>
<li>Ambiti di migrazione flessibili (a livello di sandbox, offerta o decisione)</li>
<li>Automazione di analisi e convalida delle dipendenze</li>
<li>Supporto del rollback per le migrazioni completate</li>
<li>Rapporti dettagliati sulla migrazione con mappature degli oggetti</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/decisioning-migration-api.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio delle azioni personalizzate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Approfondisci insight sullo stato e sulle prestazioni degli endpoint di azione personalizzati con un nuovo dashboard di monitoraggio e dati arricchiti sugli eventi dei passaggi del percorso. Tieni traccia correttamente di chiamate, errori, velocità effettiva, tempi di risposta e tempi di attesa delle code per comprendere rapidamente quando, dove e perché si verificano anomalie.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../action/reporting.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi personalizzare e ottimizzare il contenuto dei messaggi SMS con Decisioning. Utilizzando punteggi di priorità, formule o modelli di IA, puoi così presentare a ogni cliente i contenuti più adatti.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#feb-26-01-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

#### Configurazione

* **Utilizzo degli eventi di esperienza nelle espressioni di percorso** - A partire dal 1° aprile 2026, l&#39;utilizzo degli attributi degli eventi di esperienza nelle espressioni di percorso non sarà più supportato per le organizzazioni che non hanno utilizzato questa funzionalità negli ultimi 90 giorni. Questa funzionalità non è più disponibile per le nuove organizzazioni di clienti dall’8 luglio 2025. Per alternative, consulta [Ricerca eventi esperienza in percorsi](../building-journeys/exp-event-lookup.md).

#### Gestione dei contenuti

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **Utilizza i temi per convertire le immagini in modelli e-mail**. Quando converti un&#39;immagine in un modello e-mail in Journey Optimizer, ora puoi utilizzare un tema come input in modo che il HTML generato segua i parametri del tuo marchio. Lo stile, ad esempio il colore di sfondo, il colore dei pulsanti, i tipi di carattere, l&#39;interlinea, i margini e la spaziatura interna, viene applicato automaticamente, riducendo il lavoro di progettazione manuale e distribuendo un modello pronto per l&#39;uso con modifiche minime. [Ulteriori informazioni](../content-management/image-to-html.md)

  Data di disponibilità: 17 febbraio 2026.

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### E-mail designer

* **Rientro testo** - È ora possibile applicare un rientro a sinistra personalizzabile alla prima riga di paragrafi nei componenti di testo direttamente dal pannello delle proprietà. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->Ciò migliora la leggibilità dei contenuti lunghi, ad esempio editoriali e articoli. [Ulteriori informazioni](../email/get-started-email-style.md)

  Data di disponibilità: 18 febbraio 2026.

#### Decisioni per le esperienze

* **Supporto in entrata di Edge per l&#39;utilizzo dei dati di Adobe Experience Platform in Decisioning**. L&#39;utilizzo dei dati di Adobe Experience Platform in Decisioning ora supporta casi d&#39;uso in entrata Edge, oltre alle azioni e-mail e personalizzate nei percorsi. [Ulteriori informazioni](../experience-decisioning/aep-data-exd.md)

  Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.


* **Allega frammenti agli elementi decisionali**: Journey Optimizer ora consente di allegare agli elementi decisionali frammenti che possono essere utilizzati nelle campagne di esperienza basata su codice tramite i criteri di decisione. [Ulteriori informazioni](../experience-decisioning/fragments-decision-policies.md)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

  Data di disponibilità: 12 febbraio 2026.

#### Personalizzazione

* **Helper metadati esecuzione** - La funzione helper `executionMetadata` è ora disponibile per tutti i clienti Journey Optimizer. Utilizzala per aggiungere dinamicamente informazioni contestuali a qualsiasi azione nativa e acquisirle in un set di dati per l’esportazione in sistemi esterni. [Ulteriori informazioni](../personalization/functions/helpers.md#execution-metadata)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

  Data di disponibilità: 20 febbraio 2026.

#### SMS

* **Webhook SMS** - I webhook sono ora supportati in tutti i provider SMS. Puoi configurare ogni webhook in base allo scopo previsto: i webhook in entrata per acquisire i messaggi in arrivo e i webhook di feedback per ricevere le conferme di consegna, gli aggiornamenti di stato e altri eventi relativi ai messaggi. [Ulteriori informazioni](../sms/sms-webhook.md)

  Data di disponibilità: 2 febbraio 2026.

## Disponibile a breve {#coming-soon}

Le funzioni e i miglioramenti riportati di seguito sono previsti per la versione di febbraio. Le date di rilascio e l’ambito di applicazione possono cambiare senza preavviso.

<table>
<thead>
<tr>
<th><strong>arbitrato di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>formule di classificazione</strong> per aumentare automaticamente i punteggi di priorità del percorso in base agli attributi del profilo cliente e ai fattori contestuali, in modo che i clienti immettano i percorsi più rilevanti.</p>
<!--p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p-->
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Data di disponibilità: giovedì 25 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: creazione di contenuti per il canale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnologia <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> è disponibile in Journey Optimizer e consente di analizzare i percorsi tramite un'interfaccia in linguaggio naturale. È inoltre possibile generare e gestire contenuti specifici per il canale direttamente in Journey Agent, creando contenuti per canali quali e-mail e push, applicando e visualizzando in anteprima modelli, perfezionando tono e stile tramite prompt e aprendo contenuti in <strong>Content Designer</strong> per la modifica nel contesto.</p>
<p>Data di disponibilità: inizio marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio del modello di IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di monitorare lo stato, lo stato di formazione e le prestazioni dei modelli di IA per il decisioning. Questo consente di verificare il successo della formazione, risolvere eventuali problemi e comprendere l’impatto sui risultati, al fine di selezionare le offerte migliori per ogni cliente che utilizza l’intelligenza artificiale. Questa funzionalità è disponibile solo per <strong>Decisioning</strong> (non per i modelli di gestione delle decisioni legacy).</p>
<p>Questa funzionalità è attualmente disponibile solo per i modelli di <strong>ottimizzazione personalizzata</strong> (non ottimizzazione automatica).</p>
<p>Data di disponibilità: inizio marzo 2026</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#coming-soon-improv}

* **Anteprima Experience Decisioning nel canale di esperienza basato su codice** - È ora possibile visualizzare in anteprima gli elementi decisionali durante la configurazione di Experience Decisioning con il canale di esperienza basato su codice. L’anteprima è disponibile direttamente nell’interfaccia di authoring prima della pubblicazione.

  Data di disponibilità: giovedì 18 febbraio 2026

* **Integrazione di modelli Firefly personalizzati e di modelli di generazione di immagini di terze parti** - Integrazione perfetta di modelli Firefly standard e personalizzati, insieme a modelli di immagini di terze parti approvati (ad esempio, NanoBanana), per fornire maggiore flessibilità, controllo e allineamento del brand durante la generazione di immagini. Questo consente di selezionare il modello migliore per ogni caso d’uso: Firefly standard per esigenze generali, Firefly personalizzato per la generazione on-brand o modelli di terze parti approvati per scenari specializzati o sperimentali.

  Data di disponibilità: inizio di marzo 2026.
