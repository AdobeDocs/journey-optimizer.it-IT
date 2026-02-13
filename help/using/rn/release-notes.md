---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7263e5ace72823ce7a3a184d2842f9bba495c068
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 31%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzioni, miglioramenti e correzioni su base continuativa. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti.

A causa di questo modello, le note sulla versione vengono aggiornate prima del successivo rilascio mensile. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Note pre-release di febbraio 2026 {#feb-26-01-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 17-18 febbraio 2026

### Nuove funzionalità {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Invio ondata di messaggi in uscita</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Puoi pianificare i messaggi in uscita da <strong>campagne</strong> o <strong>percorsi</strong> per essere recapitati in <strong>batch</strong> controllati nel tempo.</p>
<p>L’invio ondata offre i seguenti vantaggi:</p>
<ul>
<li>Migliore <strong>recapito messaggi</strong> - Il servizio Spread invia nel tempo per contribuire a mantenere una solida reputazione del <strong>mittente</strong> e ridurre il rischio di essere segnalati come spam.</li>
<li><strong>Controllo del carico</strong> - Evita di sovraccaricare i sistemi a valle (ad esempio call center, pagine di destinazione) limitando il numero di messaggi inviati contemporaneamente.</li>
<li>Casi d’uso complessi e sensibili al tempo: adatti a tipi di pubblico di grandi dimensioni o quando è necessario controllare la tempistica (ad esempio capacità del call center, offerte incrementali o con limiti di tempo).</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>arbitrato di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>formule</strong> e <strong>modelli di IA</strong> per aumentare automaticamente i <strong>punteggi di priorità dei percorsi</strong> in base agli attributi del profilo cliente e ai fattori contestuali, in modo che i clienti immettano i percorsi più rilevanti.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (<strong>Disponibilità limitata</strong>). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
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
<p>Con tecnologia <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> è disponibile in Journey Optimizer e consente di analizzare i percorsi tramite un'interfaccia <strong>in linguaggio naturale</strong>. È inoltre possibile generare e gestire contenuti specifici per il canale direttamente in Journey Agent, creando contenuti per canali quali e-mail e push, applicando e visualizzando in anteprima modelli, perfezionando tono e stile tramite prompt e aprendo contenuti in <strong>Content Designer</strong> per la modifica nel contesto.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività mobili live</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Le attività live</strong> forniscono <strong>aggiornamenti in tempo reale</strong> ed esperienze interattive nelle app mobili, consentendo agli utenti di rimanere informati sugli eventi in corso o sulle attività direttamente sullo schermo del proprio dispositivo. Questa funzione migliora il coinvolgimento fornendo informazioni in tempo reale, come tracciamento dell’avanzamento, aggiornamenti degli eventi o contenuti interattivi, senza richiedere agli utenti di aprire l’app.</p>
<p>Precedentemente rilasciata in versione beta, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività di azione nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supporta una nuova attività <strong>Action</strong> generica che consente di configurare sia le azioni singole che i gruppi di azioni in entrata <strong>con più azioni</strong>, semplificando la configurazione delle azioni nell'area di lavoro <strong>percorsi</strong>. In particolare, questa nuova funzione consente:</p>
<ul>
<li>una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso;</li>
<li>la capacità di creare gruppi di azioni in entrata con più azioni;</li>
<li>Possibilità di aggiungere <strong>ottimizzazione</strong> a qualsiasi azione del canale incorporata.</li>
<li>Possibilità di aggiungere entrambe le opzioni <strong>sperimentazione</strong> e <strong>multilingue</strong> a qualsiasi azione.</li>
</ul>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale di notifiche web push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta le <strong>notifiche web push</strong>, estendendo il canale push oltre i dispositivi mobili. Puoi inviare facilmente le notifiche ai browser di dispositivi mobili e desktop, per raggiungere ogni cliente direttamente sul dispositivi che utilizza, senza ricorrere a un’app. Questo miglioramento consente di coinvolgere gli utenti con messaggi tempestivi e personalizzati in tempo reale, sfruttando gli stessi <strong>flussi di lavoro per l'authoring</strong> e le stesse <strong>funzionalità di targeting</strong> già disponibili per il push mobile.</p>
<p>Precedentemente rilasciata in versione beta, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
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
<p>Una nuova <strong>attività Content Decision</strong> è ora disponibile nell'<strong>area di lavoro percorsi</strong> per l'integrazione di <strong>offerte personalizzate</strong> direttamente nei percorsi di clienti. Questa attività ti consente di fornire contenuti basati su decisioni e di fare riferimento a tali offerte in tutto il percorso, in condizioni per la creazione di diramazioni basate sull’idoneità, in azioni personalizzate per il passaggio dei dati delle offerte a sistemi esterni e in altre attività per la creazione di esperienze cliente completamente personalizzate.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/content-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: giovedì 11 febbraio 2026</p>
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
<p><strong>Le API per gli strumenti di migrazione</strong> sono ora disponibili per migrare a livello di programmazione <strong>Entità di gestione delle decisioni</strong> in <strong>Decisioning</strong>, con:</p>
<ul>
<li>Ambiti di migrazione flessibili (<strong>sandbox</strong>, <strong>offer</strong> o <strong>decision</strong> livello)</li>
<li><strong>analisi delle dipendenze</strong> e convalida automatizzate</li>
<li><strong>Supporto rollback</strong> per le migrazioni completate</li>
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
<p>Approfondisci insight sullo stato e sulle prestazioni dei <strong>endpoint di azioni personalizzati</strong> con un nuovo <strong>dashboard di monitoraggio</strong> e dati di <strong>evento del passaggio di percorso</strong> arricchiti. Tieni traccia correttamente di chiamate, errori, velocità effettiva, tempi di risposta e tempi di attesa delle code per comprendere rapidamente quando, dove e perché si verificano anomalie.</p>
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
<p>Ora puoi personalizzare e ottimizzare il contenuto dei <strong>messaggi SMS</strong> con <strong>Decisioning</strong>. Utilizza <strong>Punteggi di priorità</strong>, <strong>Formule</strong> o <strong>Modelli AI</strong> per mostrare ai tuoi clienti il contenuto migliore.</p>
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


* **Cambio del metodo di delega del sottodominio** - È ora possibile passare da un metodo di <strong>delega del sottodominio</strong> a un altro. Questo consente di migrare i domini utilizzando la modalità di delega <strong>CNAME</strong> al metodo di delega <strong>personalizzata</strong> per rispettare i criteri di sicurezza della tua azienda.

  **Nota**: questa funzionalità è disponibile solo per un set di organizzazioni (<strong>Disponibilità limitata</strong>). Per potervi accedere, contatta il tuo rappresentante Adobe.


#### E-mail designer

* **Utilizza un tema del brand per convertire un&#39;immagine in un modello e-mail**. Quando converti un&#39;immagine in un modello e-mail in Journey Optimizer, ora puoi utilizzare un <strong>tema</strong> come input in modo che il HTML generato segua i tuoi <strong>parametri del brand</strong>. Lo stile, ad esempio il colore di sfondo, il colore dei pulsanti, i tipi di carattere, l&#39;interlinea, i margini e la spaziatura interna, viene applicato automaticamente, riducendo il lavoro di progettazione manuale e distribuendo un modello pronto per l&#39;uso con modifiche minime.


* **Aggiorna i marchi con la nuova scheda colore** - <strong>Linee guida per i marchi</strong> per garantire che il tuo marchio venga presentato in modo coerente in tutti i punti di contatto. Nella nuova <strong>sezione Colori</strong> puoi definire gli standard del sistema di colori del brand, delineando il modo in cui i colori vengono selezionati, organizzati e applicati in tutte le esperienze. Questa seione promuove un utilizzo coerente dei colori primari, secondari, di accento e neutri per supportare un’identità del brand coesa, accessibile e riconoscibile.


#### IA

* **Integrazione di modelli Firefly personalizzati e di modelli di generazione di immagini di terze parti** - Integrazione perfetta di <strong>modelli Firefly</strong> standard e personalizzati, insieme a <strong>modelli di immagini di terze parti</strong> approvati (ad esempio, NanoBanana), per fornire maggiore flessibilità, controllo e allineamento del brand durante la generazione di immagini. Questo consente di selezionare il modello migliore per ogni caso d’uso: Firefly standard per esigenze generali, Firefly personalizzato per la generazione on-brand o modelli di terze parti approvati per scenari specializzati o sperimentali.


#### Decisioni per le esperienze

* **Supporto Edge in entrata per l&#39;utilizzo dei dati Adobe Experience Platform in Decisioning**. Il supporto Decisioning di <strong>Ricerca dati Experience Platform</strong> ora include <strong>casi d&#39;uso Edge in entrata</strong>. La funzionalità rimane a disponibilità limitata; la disponibilità generale della funzione di ricerca dei dati sottostante non è ancora stata annunciata (AEP/dipendenza del prodotto).

  **Nota**: questa funzionalità è disponibile solo per un set di organizzazioni (<strong>Disponibilità limitata</strong>). Per potervi accedere, contatta il tuo rappresentante Adobe.


* **Anteprima Experience Decisioning nel canale esperienza basato su codice** - È ora possibile visualizzare in anteprima <strong>elementi decisionali</strong> durante la configurazione di <strong>Experience Decisioning</strong> con il canale <strong>Esperienza basata su codice</strong>. L’anteprima è disponibile direttamente nell’interfaccia di authoring prima della pubblicazione.


* **Osservabilità del modello di IA per la classificazione delle offerte** - Journey Optimizer ora consente di monitorare <strong>integrità</strong>, <strong>stato di apprendimento</strong> e <strong>prestazioni</strong> dei <strong>modelli di IA</strong> in Decisioning, in modo da verificare il successo della formazione, risolvere gli errori e comprendere l&#39;impatto sui risultati. Questa funzionalità è disponibile solo per i modelli di ottimizzazione personalizzati (non per l’ottimizzazione automatica).


* **Allega frammenti agli elementi decisionali** - Journey Optimizer ora consente di allegare <strong>frammenti</strong> a <strong>elementi decisionali</strong> che possono essere utilizzati nelle campagne di esperienza basate su codice tramite <strong>criteri decisionali</strong>.

  **Nota**: rilasciata in precedenza in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale).

  Data di disponibilità: 12 febbraio 2026.


#### Percorsi

* **Più azioni in entrata nei percorsi**. Per semplificare l&#39;orchestrazione del percorso, è ora possibile definire più <strong>azioni in entrata</strong> in un singolo percorso. Precedentemente disponibile nelle campagne, questa funzionalità consente di distribuire più <strong>esperienze basate su codice</strong>, <strong>messaggi in-app</strong>, <strong>schede di contenuto</strong> o <strong>azioni Web</strong> in posizioni diverse contemporaneamente, ogni azione contenente contenuti specifici.

  **Nota**: rilasciata in precedenza in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale).


* **Webhook SMS**: i <strong>webhook</strong> sono ora supportati per tutti i provider SMS. Puoi configurare ogni webhook in base allo scopo previsto: <strong>Webhook in entrata</strong> per acquisire i messaggi in arrivo e <strong>Webhook di feedback</strong> per ricevere conferme di recapito, aggiornamenti dello stato e altri eventi relativi ai messaggi. [Ulteriori informazioni](../sms/sms-webhook.md)

  Data di disponibilità: 2 febbraio 2026.