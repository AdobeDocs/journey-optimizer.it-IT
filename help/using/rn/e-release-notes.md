---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1a5f6be689c9e91ee0dc0b5f024dbe8020424337
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 29%

---

# Note pre-release {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).


## Note pre-release del 25 ottobre {#25-10-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 21-22 ottobre 2025

### Nuove funzionalità {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Canale direct mailing in percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente limitato alle campagne, il canale Direct Mail è ora disponibile nell’area di lavoro del percorso e consente di incorporare Direct Mail nei percorsi. La direct mailing può ora essere utilizzata sia in scenari batch che in scenari di percorso 1:1, con il supporto per la configurazione dell'estrazione dei file e le impostazioni di frequenza basate sul tempo.</p>
<p> Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuova API per recuperare le campagne Azione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile una nuova API di Journey Optimizer che consente di recuperare e ispezionare a livello di programmazione i dati relativi alla campagna, come dettagli, versioni e configurazioni.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio e reporting per le azioni personalizzate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa funzionalità fornisce una migliore visibilità sullo stato e sull’esecuzione del percorso, inclusi gli avvisi sullo stato del ciclo di vita e sulle prestazioni. Ora puoi capire rapidamente quando, dove e perché si verifica una situazione anomala in un’azione personalizzata.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Messaggistica di base RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con la nuova offerta del componente aggiuntivo RCS Basic, è ora possibile distribuire messaggi RCS (Rich Communication Services) di base in Journey Optimizer, abilitando le seguenti funzionalità di messaggistica avanzata, soggette al supporto del provider e geografico:</p>
<ul>
<li><strong>Supporto mittente con marchio e verificato:</strong> Inviare messaggi utilizzando profili aziendali verificati con elementi di branding (logo, nome mittente, ecc.).</li>
<li><strong>Informazioni sulla consegna dei messaggi:</strong> Ricevi rapporti dettagliati sulla consegna, inclusi gli aggiornamenti sullo stato dei messaggi (ad esempio, inviato, consegnato, letto).</li>
<li><strong>Tracciamento collegamenti:</strong> incorpora e traccia gli URL nei messaggi RCS per l'analisi del coinvolgimento.</li>
<li><strong>Fallback a SMS:</strong> Fallback automatico a SMS quando il dispositivo del destinatario non supporta RCS o è temporaneamente non raggiungibile tramite RCS.</li>
<li><strong>Composizione di base del messaggio:</strong> Inviare messaggi RCS di base basati su testo.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale direct mail nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il canale direct mailing è ora disponibile nelle campagne orchestrate. L’attività direct mail facilita l’invio con direct mail all’interno della campagna orchestrata, sia per messaggi singoli che ricorrenti. Consente di automatizzare il processo di generazione del file di estrazione richiesto dai provider di direct mail. È possibile combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuovi connettori di origine per le app fedeltà</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Adobe Experience Platform sono ora disponibili nuovi connettori sorgente per le app fedeltà Talon.One, Capillary e Kobie. Questi connettori consentono di trasferire in streaming i dati relativi alla fedeltà in Adobe Experience Platform e di sfruttarli in Journey Optimizer.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere i criteri di decisione in percorsi e campagne e-mail. I criteri di decisione sono contenitori per le offerte che sfruttano il motore di Decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico.</p>
<p> Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modalità a throughput elevato per campagne e-mail attivate da API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nelle campagne attivate da API è ora disponibile una nuova modalità di velocità effettiva elevata. Questa modalità è progettata per la messaggistica in tempo reale su larga scala (fino a 5000 transazioni al secondo) e fornisce maggiore disponibilità con minore latenza.</p>
<p>Questa funzionalità è disponibile solo per il canale e-mail, per le organizzazioni che hanno acquistato il componente aggiuntivo di velocità effettiva elevata di Adobe per la messaggistica transazionale. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ore/Esclusioni basate sul tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le ore di pausa consentono di definire esclusioni basate sul tempo per i canali E-mail, SMS, Push e WhatsApp. Assicura che non vengano inviati messaggi in specifici periodi di tempo, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità.</p>
<p>Puoi applicare ore non interattive tramite set di regole, che possono essere assegnate a singole azioni in campagne o percorsi per un controllo preciso. Semplificando questi processi.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuova funzione helper per metadati di esecuzione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nell’editor di personalizzazione è disponibile una nuova funzione helper executionMetadata. Consente di aggiungere informazioni contestuali a qualsiasi azione nativa e di acquisirle in un set di dati per l’esportazione in sistemi esterni.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Data di disponibilità: 13 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Agente esperimento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’agente di sperimentazione è uno strumento basato sull’intelligenza artificiale che modernizza le modalità di esecuzione e gestione degli esperimenti digitali su siti web, e-mail, messaggi push e applicazioni. Basato sulla piattaforma di intelligenza artificiale Adobe Experience Platform e su strumenti di sperimentazione, l’agente di sperimentazione consente di eseguire gli esperimenti in modo più efficiente, organizzare gli obiettivi di business e generare informazioni fruibili, evidenziando cosa ha funzionato, cosa non ha funzionato e dove sperimentare successivamente.</p>
<p>Come parte della nuova funzione di Experimentation Accelerator, l’agente offre:</p>
<ul>
<li><strong>Prestazioni:</strong> una chiara visualizzazione di ciò che è successo nell'esperimento</li>
<li><strong>Informazioni:</strong> spiegazione del motivo per cui si sono verificati i risultati</li>
<li><strong>Opportunità:</strong> indicazioni sulle prossime azioni da intraprendere</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Data di disponibilità: 9 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API pubblica per recuperare i percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile una nuova API Journey Optimizer per recuperare i percorsi e i relativi oggetti associati, come campagne e superfici.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Data di disponibilità: 25 settembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

- **Campagne, Experience Decisioning, Percorsi**
   - **Seleziona regole riutilizzabili nel targeting**. Ora puoi sfruttare il generatore di regole quando utilizzi le regole di targeting con la funzione Ottimizzazione messaggi in percorsi e campagne. <!-- [Read more](../FILE.md) -->

- **Canale - WhatsApp**
   - **Campo di esecuzione per canale WhatsApp** - Oltre a E-mail e SMS, ora è possibile aggiornare il campo di esecuzione predefinito di WhatsApp. È inoltre possibile sovrascrivere il campo di esecuzione impostato globalmente nei parametri avanzati dell’attività di percorso WhatsApp o nella configurazione del canale WhatsApp. <!-- [Read more](../FILE.md) -->

- **Autorizzazioni**
   - **L&#39;utente che ha creato il Percorso o la campagna non deve essere in grado di approvare**. È stata aggiunta un&#39;opzione durante la creazione o l&#39;impostazione dei criteri di approvazione per impedire ai creatori del Percorso o della campagna di approvare i propri oggetti. <!-- [Read more](../FILE.md) -->

- **Canale - Push**
   - **Mobile Live Activities - Private beta** - Live Activities forniscono aggiornamenti in tempo reale ed esperienze interattive all&#39;interno delle app mobili, consentendo agli utenti di rimanere informati sugli eventi in corso o sulle attività direttamente sullo schermo del proprio dispositivo. Questa funzione migliora il coinvolgimento distribuendo informazioni live, come tracciamento dell’avanzamento, aggiornamenti degli eventi o contenuti interattivi, senza richiedere agli utenti di aprire l’app. <!-- [Read more](../FILE.md) -->

- **Percorsi**
   - **Avvisi nuovo Percorso** - Data di disponibilità: 14 ottobre 2025
Sono disponibili nuovi avvisi preconfigurati per i percorsi: Frequenza di eliminazione profilo superata (rapporto scarti profilo rispetto ai profili immessi negli ultimi 5 minuti ha superato la soglia), Frequenza di errori azione personalizzata superata (rapporto errori azione personalizzata rispetto alle chiamate HTTP riuscite negli ultimi 5 minuti ha superato la soglia), Frequenza di errori profilo superata (rapporto profili in errore rispetto ai profili immessi negli ultimi 5 minuti ha superato la soglia). <!-- [Read more](../FILE.md) -->

- **Configurazione**
   - **Supporto attributi personalizzati con URL per l&#39;annullamento dell&#39;iscrizione con un solo clic** - Data di disponibilità: 6 ottobre 2025
Con Journey Optimizer, se gestisci il consenso al di fuori di Adobe, puoi impostare un endpoint esterno personalizzato definendo un collegamento con un solo clic per annullare l’abbonamento nella configurazione dell’e-mail. Quando i destinatari fanno clic sul collegamento di annullamento dell’abbonamento, Journey Optimizer aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso. Per personalizzare ulteriormente l’indirizzo e-mail di annullamento dell’iscrizione con un solo clic, puoi definire gli attributi personalizzati che verranno aggiunti all’evento del consenso. Questa funzionalità è già disponibile per l’URL personalizzato per l’annullamento dell’abbonamento con un clic da agosto del 25 agosto ed è ora disponibile per l’opzione Invia a (annulla abbonamento) in Disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe. <!-- [Read more](../FILE.md) -->

- **Canale - E-mail**
   - **Allegati PDF alle e-mail** - Data di disponibilità: 30 settembre 2025
È ora possibile allegare un file PDF statico a un messaggio e-mail inviato con Journey Optimizer. Puoi inviare fino a 6 messaggi all’anno con un allegato PDF per profilo. La dimensione massima consentita per ciascun allegato è di 5 MB. Per ulteriori dimensioni o volumi, è possibile acquistare il componente aggiuntivo per allegati PDF. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

  >[!AVAILABILITY]
  >
  >Precedentemente rilasciato in Disponibilità limitata, questo miglioramento è ora disponibile per tutti gli ambienti (Disponibilità generale).

  <!-- [Read more](../FILE.md) -->

