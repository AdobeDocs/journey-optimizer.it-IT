---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
hide: true
hidefromtoc: true
source-git-commit: 281387d650dc3a6c67ba365cd804f2b875dcd60b
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 34%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di aprile 2024 {#e-2024}

**Data di rilascio**: 30 aprile 2024

### Nuova funzionalità {#e-features}

Questa versione include le nuove funzionalità descritte di seguito.

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Experience Decisioning - Disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning semplifica la personalizzazione offrendo un catalogo centralizzato di offerte di marketing note come "elementi decisionali" e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni individuo gli elementi decisionali più rilevanti.</p>
<p>Questi elementi decisionali vengono integrati direttamente in un’ampia gamma di superfici in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne Journey Optimizer. I criteri decisionali di Experience Decisioning sono disponibili solo per l’utilizzo in campagne di esperienza basate su codice.</p>
<p>Experience Decisioning è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il rappresentante del tuo Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service) con Infobip</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il canale SMS, ora è possibile migliorare le comunicazioni inviando messaggi MMS (Multimedia Message Service), che consentono la condivisione di immagini, GIF o video con la clientela. Questa funzione in precedenza disponibile solo con Sinch, è ora disponibile anche con Infobip.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

<!--
* **Experience Decisioning + Code-based experiences (LA)**: You can now leverage the Experience decisioning feature to use decision items in your code-based campaigns. Note: The Code-based experience channel and Experience decisioning are not available for organizations that have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.
-->
<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Gestione delle decisioni**

* Il **Registro modifiche** Questa scheda ti consente di visualizzare tutte le modifiche apportate a un’offerta o a una decisione che sono state rimosse. Le modifiche relative alle offerte e alle decisioni ora sono visibili in **Audit** menu.

**Experience Decisioning**

Dalla versione beta a LA, ecco i miglioramenti apportati:

* Ora puoi sfruttare i dati contestuali provenienti da Adobe Experience Platform nelle regole di decisione utilizzando **Dati contestuali** scheda.
* È ora disponibile una nuova autorizzazione &quot;Gestisci decisioni esperienza&quot; per la risorsa Gestione delle decisioni. Consente di gestire i diritti relativi ad Experience Decisioning.
* Ora puoi aggiungere più regole di limite per un’offerta. Ciò consente di aumentare il livello di controllo sulla modalità di invio delle offerte.
* Ora in Experience Decisioning è possibile aggiungere più regole di limitazione per un determinato elemento decisionale. Ciò consente di aumentare il livello di controllo sulla modalità di invio delle offerte.
* Ora puoi creare dashboard di reporting personalizzate delle campagne Experience Decisioning tramite [!DNL Customer Journey Analytics].

**Percorsi**

* **Progettazione Percorsi migliorata**:

   * L’interfaccia utente dell’area di lavoro migliorata offre un’esperienza utente più intuitiva ed efficiente.
   * Le attività sono più chiare e presentano più informazioni sull’area di lavoro del percorso con meno clic.

* **Nuovo reporting live**: il reporting per percorsi è ora accessibile tramite l’applicazione Live Reports. Questa è un’applicazione che fornisce molte informazioni approfondite sull’esecuzione del percorso.

**Configurazione**

* Ora puoi selezionare un’azione di marketing al livello della superficie di canale. Se utilizzati in una superficie, tutti i criteri di consenso associati a tale azione di marketing vengono usati per rispettare le preferenze della clientela.
* Per le superfici di canale è ora disponibile l&#39;utilizzo del controllo di accesso a livello di oggetto.

