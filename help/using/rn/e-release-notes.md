---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: f06a9d01721ff23dfdf95db8d984143bb36fe85c
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 41%

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
<th><strong>Helper metadati esecuzione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nell’editor di personalizzazione è disponibile una nuova funzione helper "executionMetadata". Consente di aggiungere informazioni contestuali a qualsiasi azione nativa e di acquisirle in un set di dati per l’esportazione in sistemi esterni.</p>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/functions/helpers.md#execution-metadata">documentazione dettagliata</a></p>
<p>Data di disponibilità: 13 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>L'agente della sperimentazione è qui!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnologia <a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, l'agente di sperimentazione è disponibile in Journey Optimizer. </p>
<p>L’agente di sperimentazione è uno strumento basato sull’intelligenza artificiale che modernizza le modalità di esecuzione e gestione degli esperimenti digitali su siti web, e-mail, messaggi push e applicazioni. Consente di eseguire gli esperimenti in modo più efficiente, organizzare gli obiettivi di business e generare informazioni fruibili, evidenziando ciò che ha funzionato, ciò che non ha funzionato e dove sperimentare successivamente.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">documentazione dettagliata</a></p>
<p>Data di disponibilità: 10 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Allegati PDF alle e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile allegare un file PDF statico a un messaggio e-mail inviato con Journey Optimizer.</p>
<ul>
<li>Puoi inviare fino a 6 messaggi con un allegato PDF per profilo all’anno.</li>
<li>La dimensione massima del file consentita per ciascun allegato è di 5 MB.</li>
<li>Per ulteriori dimensioni o volumi, puoi acquistare il componente aggiuntivo per gli allegati PDF. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</li>
</ul>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/pdf-attachments.md">documentazione dettagliata</a></p>
<p>Data di disponibilità: 30 settembre 2025</p>
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
<p>Per ulteriori informazioni, consulta la <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">documentazione dettagliata</a></p>
<p>Data di disponibilità: 25 settembre 2025</p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti

**Seleziona regole riutilizzabili nel targeting**

Ora puoi sfruttare il generatore di regole quando utilizzi le regole di targeting con la funzione Ottimizzazione dei messaggi in percorsi e campagne. <!-- [Read more](../FILE.md) -->

**Campo di esecuzione per canale WhatsApp**

Oltre a E-mail e SMS, ora è possibile aggiornare il campo di esecuzione predefinito di WhatsApp. È inoltre possibile sovrascrivere il campo di esecuzione impostato globalmente nei parametri avanzati dell’attività di percorso WhatsApp o nella configurazione del canale WhatsApp. <!-- [Read more](../FILE.md) -->

**Autorizzazioni**

**Avvisi su nuovi percorsi**

Sono disponibili nuovi avvisi preconfigurati per i percorsi: [Frequenza eliminazioni profilo superata](../reports/alerts.md#alert-discard-rate) (rapporto tra eliminazioni profilo e profili immessi negli ultimi 5 minuti ha superato la soglia), [Frequenza errori azioni personalizzate superata](../reports/alerts.md#alert-custom-action-error-rate) (rapporto tra errori azioni personalizzate e chiamate HTTP riuscite negli ultimi 5 minuti ha superato la soglia) e [Frequenza errori profilo superata](../reports/alerts.md#alert-profile-error-rate) (rapporto tra profili in errore e profili immessi negli ultimi 5 minuti ha superato la soglia). Puoi modificare i valori di soglia e iscriverti agli avvisi a livello di singolo percorso invece che globalmente.

Data di disponibilità: 14 ottobre 2025

**Attributi personalizzati supportati per l&#39;indirizzo di posta elettronica (annullamento iscrizione)**

Con Journey Optimizer, se gestisci il consenso al di fuori di Adobe, puoi impostare endpoint esterni personalizzati definendo un collegamento con un solo clic per annullare l’abbonamento e un indirizzo e-mail personalizzato per annullare l’abbonamento nella configurazione e-mail. Quando i destinatari fanno clic sul collegamento di annullamento dell’iscrizione, Journey Optimizer aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso.

Per personalizzare ulteriormente gli endpoint personalizzati, ora puoi definire attributi personalizzati che verranno aggiunti anche all’evento di consenso. [Ulteriori informazioni](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Questa funzionalità è già disponibile per l&#39;URL personalizzato **[!UICONTROL Annulla iscrizione]** con un solo clic da agosto &#39;25 ed è ora disponibile per l&#39;opzione **[!UICONTROL Invia a (annulla iscrizione)]** in Disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

Data di disponibilità: 6 ottobre 2025