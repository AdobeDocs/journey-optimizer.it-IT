---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 61%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Aggiornamenti di maggio {#may-updates}

**Data di disponibilità**: 7 maggio 2024

<table>
<thead>
<tr>
<th><strong>Decisioni per le esperienze: disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione Decisioni per le esperienze semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti.</p>
<p>Questi elementi decisionali vengono integrati direttamente in un’ampia gamma di superfici in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne Journey Optimizer. I criteri decisionali di Experience Decisioning sono disponibili solo per l’utilizzo in campagne di esperienza basate su codice.</p>
<p>La funzione Decisioni per le esperienze è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/gs-experience-decisioning.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

Dalla versione beta a LA, sono stati aggiunti i seguenti miglioramenti:

* **Experience Decisioning + Esperienze basate su codice (LA)**: ora puoi sfruttare la funzione Experience Decisioning per utilizzare gli elementi decisionali nelle campagne basate su codice. Nota: il canale di esperienza basato sul codice e Experience Decisioning non sono disponibili per le organizzazioni che hanno acquistato le offerte aggiuntive Adobe Healthcare Shield e Privacy and Security Shield. [Ulteriori informazioni](../code-based/get-started-code-based.md)
* Ora puoi sfruttare i dati contestuali provenienti da Adobe Experience Platform nelle regole di decisione e nelle formule di classificazione. [Ulteriori informazioni](../experience-decisioning/context-data.md)
* È ora disponibile la nuova autorizzazione “Gestisci decisioni esperienza” per la risorsa Gestione delle decisioni. Consente di gestire i diritti relativi ad Experience Decisioning. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md)
* Ora in Decisione per le esperienze è possibile aggiungere più regole di limitazione per un determinato elemento decisionale. Ciò ti consente di aumentare il livello di controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../experience-decisioning/items.md#capping)
* Ora puoi creare dashboard di reporting personalizzate delle campagne Experience Decisioning tramite [!DNL Customer Journey Analytics]. [Ulteriori informazioni](../experience-decisioning/cja-reporting.md)

## Note sulla versione di aprile 2024 {#apr-2024}

**Data di rilascio**: 2 maggio 2024

### Nuove funzionalità {#apr-features}

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

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service): tutti i provider</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il canale SMS, ora è possibile migliorare le comunicazioni inviando messaggi MMS (Multimedia Message Service), che consentono di condividere immagini, GIF o video con la clientela. Inizialmente disponibile solo con Sinch, la funzione MMS è ora disponibile anche con Infobip e Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Designer del percorso e rapporti live migliorati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione include un’interfaccia utente dell’area di lavoro migliorata per i percorsi e offre un’esperienza utente più intuitiva ed efficiente. Le attività sono più chiare e nell’area di lavoro del percorso è possibile ottenere più informazioni con meno clic.</p>
<img src="assets/new-canvas3.gif"/>
<p>Oltre al design migliorato dell’area di lavoro del percorso, è stata introdotta la possibilità di visualizzare le metriche di reporting delle ultime 24 ore direttamente nell’area di lavoro del percorso. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>Nota</strong>: a partire dalla versione di aprile, queste modifiche verranno gradualmente implementate in tutti gli ambienti.</p>
<p>Per ulteriori informazioni, consulta la <a href="new-canvas.md">documentazione dettagliata</a>.</p>
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

### Miglioramenti {#apr-improvements}

Questa versione include i miglioramenti elencati di seguito.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Configurazione**

* Ora puoi selezionare un’azione di marketing al livello della superficie di canale. Se utilizzati in una superficie, tutti i criteri di consenso associati a tale azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)
* Per le superfici di canale è ora disponibile l&#39;utilizzo del controllo di accesso a livello di oggetto. [Ulteriori informazioni](../configuration/channel-surfaces.md#create-channel-surface)
* Mentre abiliti l’annullamento dell’iscrizione all’elenco in una superficie di canale, ora puoi definire il livello di consenso in base a come gestisci il consenso da tutte le altre sorgenti. [Ulteriori informazioni](../email/email-settings.md#list-unsubscribe)

**Gestione dei contenuti**

* Ora puoi simulare modelli di contenuto per tutti i canali. [Maggiori informazioni](../content-management/content-templates.md#test-templates)

**Personalizzazione**

* Il nuovo **toInt** La funzione helper è disponibile nell’editor di espressioni. Ti consente di convertire uno qualsiasi di questi tipi (number, double, int, long, float, short, byte, boolean, string) in un numero intero. [Ulteriori informazioni](../personalization/functions/math.md#to-int)
