---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 97967e8043df9b75d3120e4a7bfccff700f5d57f
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 16%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione. I collegamenti, le schermate e la documentazione aggiornata sono pubblicati nella [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di gennaio 2024 {#e-2024}

**Data di rilascio**: 20-31 gennaio 2024

### Nuove funzionalità{#e-features}

Questa versione include le nuove funzionalità elencate di seguito.


<table>
<thead>
<tr>
<th><strong>Aggiornamenti del recapito messaggi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora supporta la tecnologia di autenticazione DMARC.</p>
<p>A partire dal 1° febbraio 2024, Google e Yahoo! ti verrà richiesto di disporre di un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail. Assicurati di aver impostato il record DMARC per tutti i sottodomini che hai delegato o a cui stai delegando l’Adobe in Journey Optimizer.</p>
<!--img src="assets/channel-reports.png"/-->
<p>Per ulteriori informazioni, consulta la <a href="../configuration/dmarc-record.md">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Playbook di casi d’uso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sfrutta un catalogo di playbook di casi d’uso specifici per il settore in Real-Time CDP e Journey Optimizer per risolvere casi d’uso comuni che è possibile eseguire utilizzando Adobe Experience Platform e Adobe Percorsi Optimizer.</p><p>Dopo aver scelto il playbook più adatto alle tue esigenze, puoi abilitarlo per generare le risorse necessarie per supportare il caso d’uso, ad esempio percorsi, messaggi, schemi o segmenti, e personalizzarli nel tuo schema per velocizzare il time-to-value.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
<!--<p>For more information, refer to the <a href="../start/playbooks.md">detailed documentation</a>.</p>-->
</tr>
</tbody>
</table>

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Reporting**

* **Nuovi widget di suddivisione basati su dominio** - Sono stati aggiunti nuovi widget per migliorare i rapporti Campagna e Percorso. Il **Motivi di mancato recapito per dominio**, **Inviato e consegnato da domini**, **Aperture e clic per dominio** e **Mancato recapito ed errori per dominio** i widget forniscono una suddivisione dettagliata a livello di dominio per le metriche chiave di consegna e tracciamento delle e-mail. [Ulteriori informazioni](../reports/channel-report.md)

**Canale SMS**

* **Doppio consenso** - Il flusso di lavoro Double Opt-In per SMS garantisce che gli utenti acconsentano esplicitamente alla ricezione di messaggi quando la richiesta viene avviata dal proprio dispositivo. Gli utenti avviano il processo di consenso inviando un messaggio SMS in entrata. Una volta confermato il loro consenso, viene inviato un messaggio di follow-up con la richiesta di verifica finale. Se un profilo utente non esiste, viene creato dopo la conferma. [Ulteriori informazioni](../sms/sms-configuration.md#create-api)

  Tieni presente che questo si applica solo ai provider SMS Sinch e Infobip.

**Percorsi**

* **Durata eventi di reazione** : la durata massima che puoi definire nel **Eventi di reazione** è ora di 29 giorni invece di 30. [Ulteriori informazioni](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Read audience**  - L’attività Read Audience ora si basa sul set di dati snapshot del profilo per i segmenti batch, che viene generato solo una volta al giorno dopo l’esecuzione del processo batch giornaliero pianificato, pertanto i dati verranno aggiornati all’ultimo processo batch giornaliero.

* **Gruppi di campi** - Correzione di un problema che in alcuni casi impediva il salvataggio dei gruppi di campi.

* **Editor espressioni** - Il tipo di dati listObject è ora supportato in tutte le espressioni e nelle funzioni aggiuntive. [Ulteriori informazioni](../building-journeys/expression/functions.md)

**Regole di frequenza**

* **Limite di frequenza settimanale e giornaliero** - È ora possibile specificare il numero massimo di messaggi inviati a un profilo cliente in una settimana o in un giorno, oltre al mese. Il limite di frequenza si basa sul periodo di calendario selezionato e viene reimpostato all’inizio dell’intervallo di tempo corrispondente. [Ulteriori informazioni](../configuration/frequency-rules.md#create-new-rule)

**Gestione delle decisioni**

* **Limitazione di frequenza su Edge** - Il contatore dei limiti di frequenza ora è aggiornato e disponibile in una decisione API Edge Decisioning in meno di 3 secondi.