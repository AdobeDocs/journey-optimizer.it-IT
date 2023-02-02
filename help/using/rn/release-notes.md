---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ad0ca954d2ba15293bdde2715a7aaed62b040cce
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 92%

---

# Note sulla versione {#release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

Le note sulle versioni precedenti sono disponibili in [questa pagina](release-notes-2022.md). Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Versione di gennaio 2023 {#jan-2023-release}

### Nuove funzionalità{#jan-2023-features}


<table>
<thead>
<tr>
<th><strong>Igiene dei dati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform offre una suite di funzionalità di igiene dei dati che ti consentono di gestire i dati archiviati tramite l’eliminazione programmatica di record e set di dati del consumatore. Questa funzionalità è ora disponibile per Adobe Journey Optimizer. </p>
<p>Puoi gestire gli archivi dati per garantire che le informazioni vengano utilizzate come previsto, che vengano aggiornate quando è necessario correggere dati non corretti e che vengano eliminate quando i criteri organizzativi lo ritengono necessario.</p>
<p><strong>Attenzione</strong>: le funzionalità di igiene dei dati sono attualmente disponibili solo per le organizzazioni che hanno acquistato le offerte aggiuntive <strong>Healthcare Shield</strong> e <strong>Privacy and Security Shield</strong>.</p><p>Per ulteriori informazioni, consulta la <a href="../privacy/data-hygiene.md">documentazione dettagliata</a>.

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modelli di contenuto e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare modelli di contenuto autonomi da sfruttare tra percorsi e campagne per un rapido riutilizzo.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Scopri come creare, modificare e utilizzare modelli di contenuto in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">questo video</a>. Per ulteriori informazioni, consulta la <a href="../email/content-templates.md">documentazione dettagliata</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#jan-2023-improvements}

**Percorsi**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* Quando si aggiunge una **Qualificazione del segmento** o **Leggi segmento** in un percorso, lo spazio dei nomi viene ora precompilato, per impostazione predefinita, con l’ultimo spazio dei nomi utilizzato. Fai riferimento alle sezioni [Qualificazione del segmento](../building-journeys/segment-qualification-events.md#about-segment-qualification) e [Leggi segmento](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Nell’area di lavoro del percorso, nella barra degli strumenti è disponibile un nuovo pulsante che consente di scaricare una schermata del percorso.

**E-mail Designer**

* Ora puoi esportare il contenuto delle e-mail dal menu **Esporta HTML**. I file esportati sono disponibili in un file di archivio (.ZIP).

**Amministrazione**

* Una nuova sottosezione fornisce consigli sulla creazione dell’indirizzo **Rispondi a (e-mail)** per garantire una corretta gestione delle risposte. [Ulteriori informazioni](../email/email-settings.md#reply-to-email)

* Durante la creazione o la modifica dei **Pool IP**, i record PTR associati vengono ora visualizzati nell’elenco IP e, al passaggio del mouse, sugli indirizzi IP selezionati. [Ulteriori informazioni](../configuration/ip-pools.md#create-ip-pool)

* Dopo aver selezionato un pool IP in una superficie del canale, le informazioni del record PTR sono ora visibili quando si passa il mouse sugli indirizzi IP. [Ulteriori informazioni](../email/email-settings.md#subdomains-and-ip-pools)

* È stata aggiornata l’interfaccia utente per la modifica dei [Record PTR](../configuration/ptr-records.md#edit-ptr-record) e dei [campi esecuzione](../configuration/primary-email-addresses.md).

* È stata migliorata l’interfaccia utente per la creazione e la modifica dei sottodomini. [Ulteriori informazioni](../configuration/delegate-subdomain.md)

* La schermata Elenco di soppressione dei **Caricamenti recenti** è stata aggiornata. [Ulteriori informazioni](../configuration/manage-suppression-list.md#recent-uploads)

**Campagne**

* Una richiesta cURL di esempio che consente l’esecuzione di campagne attivate da API viene ora generata automaticamente e resa disponibile nella schermata della campagna. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personalizzazione**

* Sono disponibili nuove funzioni assistenza: formatCurrency, charCodeAt, stringToDate, toString, formatNumber e toHexString. Inoltre, la funzione toDateTimeOnly ora accetta tipi di campi stringa, data, long e int. [Ulteriori informazioni](../personalization/functions/functions.md)
