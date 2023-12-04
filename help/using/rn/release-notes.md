---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# Note sulla versione {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

Le note sulle versioni precedenti sono disponibili in [questa pagina](release-notes-2023.md). Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Note sulla versione di ottobre 2023 {#oct-rn-2023}

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
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/copy-to-sandbox.md">documentazione dettagliata</a>.</p>
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
<th><strong>MMS (Multimedia Message Service) negli SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il canale SMS, ora è possibile migliorare le comunicazioni inviando messaggi MMS (Multimedia Message Service), che consentono la condivisione di immagini, GIF o video con la clientela. Questa funzione è attualmente disponibile solo con Sinch.</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../sms/create-sms.md#mms-content">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>

### Miglioramenti {#oct-2023-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Tipi di pubblico**

* Ora puoi eseguire il targeting di tipi di pubblico caricati da un file CSV in percorsi e campagne. [Ulteriori informazioni](../audience/about-audiences.md#segments-in-journey-optimizer)
* Ora puoi eseguire il targeting dei tipi di pubblico creati tramite la composizione del pubblico e sfruttare gli attributi di arricchimento nei percorsi. [Ulteriori informazioni](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>Queste funzionalità sono attualmente disponibili come versione beta privata.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campagne**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Quando si verifica un errore in una delle campagne, ora viene visualizzata un’icona di avviso nell’elenco delle campagne insieme allo stato della campagna. [Ulteriori informazioni](../campaigns/modify-stop-campaign.md#statuses)

**Percorsi**

* La durata massima che puoi definire in qualsiasi tempo di attesa è ora di 29 giorni anziché di 30. Questo miglioramento è stato introdotto per evitare che le durate di attesa superino la durata del percorso di 30 giorni. Ciò si applica:

   * al campo **Quantità di tempo** nell’[attività di attesa](../building-journeys/wait-activity.md)
   * al **Periodo di attesa per rientro** nelle [Proprietà del percorso](../building-journeys/journey-gs.md#entrance)
   * il campo **Attendi** nella definizione di timeout delle [attività evento](../building-journeys/general-events.md#events-specific-time).

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**Gestione delle decisioni**

* Sono state aggiornate diverse etichette relative al limite delle offerte nell’interfaccia di gestione delle decisioni. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

