---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 0328ffb49ca72d293c0e1a729441cde6c3a16b45
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 43%

---

# Note pre-release {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).


## Note pre-release del 25 ottobre {#oct-25-10-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: giovedì 22 ottobre 2025

### Nuove funzionalità {#oct-25-10-features}



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

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

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
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
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
<th><strong>Regole di targeting riutilizzabili</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di creare regole da un menu dedicato dell’interfaccia utente e di sfruttarle durante la creazione del targeting, come parte dell’ottimizzazione dei contenuti in una campagna o in un percorso, nell’attività Ottimizza percorso.</p>
<p>Le regole di targeting sono attualmente disponibili per le organizzazioni che hanno acquistato l’offerta aggiuntiva Decisioning e sono disponibili su richiesta per le altre organizzazioni (Disponibilità limitata).</p>
<p>Questa funzionalità verrà implementata progressivamente per tutti i clienti. Nel frattempo, contatta il tuo rappresentante Adobe per ottenere l’accesso.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
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
<p>Precedentemente rilasciata nella versione beta, questa funzionalità è ora disponibile per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Per ulteriori informazioni, consulta la <a href="../email/apply-email-themes.md">documentazione dettagliata</a>.</p>
<!--p>Availability date: October 22, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi nuovi Percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono disponibili nuovi avvisi preconfigurati per monitorare l’esecuzione del percorso:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Frequenza eliminazioni profilo superata</a>: rapporto tra eliminazioni di profili e profili immessi negli ultimi 5 minuti ha superato la soglia</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Frequenza errori azione personalizzata superata</a>: rapporto tra errori azione personalizzata e chiamate HTTP riuscite negli ultimi 5 minuti ha superato la soglia</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Frequenza errori profilo superata</a>: rapporto tra profili in errore e profili immessi negli ultimi 5 minuti ha superato la soglia.</li></ul> <p>Puoi modificare i valori di soglia e iscriverti agli avvisi a livello di singolo percorso invece che globalmente.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/alerts.md">documentazione dettagliata</a></p>
<p>Data di disponibilità: 14 ottobre 2025</p>
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
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=it" target="_blank">documentazione dettagliata</a></p>
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

**Campo di esecuzione per canale WhatsApp**

Oltre a E-mail e SMS, puoi sapere come aggiornare il campo di esecuzione predefinito per le consegne WhatsApp a livello di sandbox. È inoltre possibile ignorare il campo di esecuzione impostato a livello globale modificandolo nei parametri avanzati dell’attività di percorso WhatsApp o nella configurazione del canale WhatsApp. <!-- [Read more](../FILE.md) -->

**Attributi personalizzati supportati per l&#39;indirizzo di posta elettronica (annullamento iscrizione)**

Con Journey Optimizer, se gestisci il consenso al di fuori di Adobe, puoi impostare endpoint esterni personalizzati definendo un collegamento con un solo clic per annullare l’abbonamento e un indirizzo e-mail personalizzato per annullare l’abbonamento nella configurazione e-mail. Quando i destinatari fanno clic sul collegamento di annullamento dell’iscrizione, Journey Optimizer aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso.

Per personalizzare ulteriormente gli endpoint personalizzati, ora puoi definire attributi personalizzati che verranno aggiunti anche all’evento di consenso. [Ulteriori informazioni](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Questa funzionalità è già disponibile per l&#39;URL personalizzato **[!UICONTROL Annulla iscrizione]** con un solo clic da agosto &#39;25 ed è ora disponibile per l&#39;opzione **[!UICONTROL Invia a (annulla iscrizione)]** in Disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

Data di disponibilità: 6 ottobre 2025