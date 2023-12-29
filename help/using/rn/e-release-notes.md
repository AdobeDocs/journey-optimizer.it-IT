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
source-git-commit: 004eb41b084f32993ec437f589e4e3d2cf7500d3
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 100%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di ottobre 2023 {#oct-rn-2023}

**Data di rilascio**: 25-26 ottobre 2023

### Nuove funzionalità{#oct-2023-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Strumenti sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gli strumenti sandbox consentono di copiare oggetti in più sandbox sfruttando le funzioni di esportazione e importazione dei pacchetti. Un pacchetto può essere costituito da uno o più oggetti. Tutti gli oggetti inclusi in un pacchetto devono appartenere alla stessa sandbox.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service) in SMS (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il canale SMS, ora è possibile migliorare le comunicazioni inviando messaggi MMS (Multimedia Message Service), che consentono la condivisione di immagini, GIF o video con la clientela. Questa funzione è attualmente disponibile in versione beta solo con Sinch.</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### Miglioramenti {#oct-2023-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Tipi di pubblico**

* Ora puoi eseguire il targeting di tipi di pubblico caricati da un file CSV in percorsi e campagne.
* Ora puoi eseguire il targeting dei tipi di pubblico creati tramite la composizione del pubblico e sfruttare gli attributi di arricchimento nei percorsi.

>[!AVAILABILITY]
>
>Queste funzionalità sono attualmente disponibili come versione beta privata.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campagne**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Quando si verifica un errore in una delle campagne, ora viene visualizzata un’icona di avviso nell’elenco delle campagne insieme allo stato della campagna.

**Percorsi**

* La durata massima che puoi definire in qualsiasi tempo di attesa è ora di 29 giorni anziché di 30. Ciò si applica:

   * al campo **Quantità di tempo** nell’[attività di attesa](../building-journeys/wait-activity.md)
   * al **Periodo di attesa prima di un reingresso** nelle [Proprietà del percorso](../building-journeys/journey-gs.md#entrance)
   * nel campo **Attendi** nella definizione di timeout di eventi [generale](../building-journeys/general-events.md#events-specific-time) e di [reazione](../building-journeys/reaction-events.md) .

**Consenso nella configurazione dei canali**

* Ora puoi selezionare un’azione di marketing al livello della superficie di canale. Se utilizzati in una superficie, tutti i criteri di consenso associati a tale azione di marketing vengono usati per rispettare le preferenze della clientela.

**Gestione delle decisioni**

* Sono state aggiornate diverse etichette relative al limite delle offerte nell’interfaccia di gestione delle decisioni.
