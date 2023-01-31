---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 19%

---

# Note sulla versione {#release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Tutte le modifiche sono consolidate l’ultima settimana di ogni mese nelle presenti note sulla versione.

Le note sulle versioni precedenti sono disponibili in [questa pagina](release-notes-2022.md). Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Scopri di più su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti a [Newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} ricevi oggi stesso gli ultimi aggiornamenti dei prodotti, storie entusiasmanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


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
<p>Adobe Experience Platform offre una suite di funzionalità di igiene dei dati che ti consentono di gestire i dati archiviati tramite l’eliminazione programmatica di record e set di dati di consumo. Questa funzionalità è ora disponibile per Adobe Journey Optimizer. </p>
<p>Puoi gestire gli archivi dati per garantire che le informazioni vengano utilizzate come previsto, che vengano aggiornate quando è necessario correggere i dati in modo errato e che vengano eliminate quando i criteri organizzativi lo ritengono necessario.</p>
<p><strong>Attenzione</strong> - Le funzionalità di igiene dati sono attualmente disponibili solo per le organizzazioni che hanno acquistato il <strong>Scudo sanitario</strong> e <strong>Privacy e sicurezza</strong> offerte aggiuntive.</p><p>Per ulteriori informazioni, consulta la <a href="../privacy/data-hygiene.md">documentazione dettagliata</a>.

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
<!--img src="assets/do-not-localize/"/-->
<p>Scopri come creare, modificare e utilizzare modelli di contenuto in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">questo video</a>.
<p>Per ulteriori informazioni, consulta la <a href="../email/content-templates.md">documentazione dettagliata</a>.
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

* Quando si aggiunge una **Qualificazione di un segmento** o **Leggi segmento** in un percorso, lo spazio dei nomi viene ora precompilato, per impostazione predefinita, con l’ultimo spazio dei nomi utilizzato. Fai riferimento a [Qualificazione di un segmento](../building-journeys/segment-qualification-events.md#about-segment-qualification) e [Leggi segmento](../building-journeys/read-segment.md#configuring-segment-trigger-activity) sezioni.

* Nell’area di lavoro del percorso, è disponibile un nuovo pulsante nella barra degli strumenti che consente di scaricare uno screenshot del percorso.

**E-mail Designer**

* Ora puoi esportare il contenuto delle e-mail dalla **Esporta HTML** menu. I file esportati sono disponibili in un file di archivio (.ZIP).

**Amministrazione**

* Una nuova sottosezione fornisce raccomandazioni sulla creazione di **Rispondi a (e-mail)** e garantire una corretta gestione delle risposte. [Ulteriori informazioni](../email/email-settings.md#reply-to-email)

* Durante la creazione o la modifica **Pool IP**, i record PTR associati vengono ora visualizzati nell’elenco IP e al passaggio del mouse sugli indirizzi IP selezionati. [Ulteriori informazioni](../configuration/ip-pools.md#create-ip-pool)

* Dopo aver selezionato un pool IP in una superficie del canale, le informazioni del record PTR sono ora visibili quando si passa il mouse sugli indirizzi IP. [Ulteriori informazioni](../email/email-settings.md#subdomains-and-ip-pools)

* Interfaccia utente per la modifica [Record PTR](../configuration/ptr-records.md#edit-ptr-record) e [campi di esecuzione](../configuration/primary-email-addresses.md) è stato aggiornato.

* È stata migliorata l’interfaccia utente per la creazione e la modifica dei sottodomini. [Ulteriori informazioni](../configuration/delegate-subdomain.md)

* Elenco di soppressione **Caricamenti recenti** la schermata è stata aggiornata. [Ulteriori informazioni](../configuration/manage-suppression-list.md#recent-uploads)

**Campagne**

* Una richiesta cURL di esempio che consente l’esecuzione di campagne con attivazione API viene ora generata automaticamente e resa disponibile nella schermata della campagna. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personalizzazione**

* Sono disponibili nuove funzioni helper: formatCurrency, charCodeAt, stringToDate, toString, formatNumber e toHexString. Inoltre, la funzione toDateTimeOnly ora accetta tipi di campi stringa, data, long e int. [Ulteriori informazioni](../personalization/functions/functions.md)
