---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
source-git-commit: 4d3352184aac7fe19096c21650982e29506f2bff
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 24%

---


# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in Journey Optimizer.
Puoi anche consultare gli [Aggiornamenti alla documentazione](documentation-updates.md) più recenti.

## Versione di luglio 2021 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>Utilizzo delle relazioni tra schemi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform ti consente di definire relazioni tra schemi per utilizzare un set di dati come tabella di ricerca per un altro. Journey Optimizer ora può sfruttare i dati provenienti da uno schema collegato.</p>
<p>Questi campi sono disponibili nella configurazione unitaria degli eventi, nelle condizioni di percorso, nella personalizzazione dei messaggi e nella personalizzazione delle azioni personalizzate.</p>
<p>Per ulteriori informazioni, consulta la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Elenco Consentiti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile definire un elenco specifico di invio sicuro a livello di sandbox per evitare, ad esempio, di inviare e-mail indesiderate ai destinatari in un ambiente di test.
</p>
<p>Per ulteriori informazioni, consulta la <a href="allow-list.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

* Il tasso di limitazione complessivo di tutti i segmenti letti eseguiti contemporaneamente nella stessa sandbox è limitato a 17.000 messaggi al secondo. [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Il campo **Durata cache** è stato rimosso dal riquadro di configurazione dell&#39;origine dati. [Ulteriori informazioni](datasource/about-data-sources.md)
* Per le origini dati esterne, ora viene definita automaticamente una regola di limitazione di 15 chiamate al secondo. [Ulteriori informazioni](configuration/external-systems.md#capping)
* Per i percorsi live, nella schermata delle proprietà del percorso vengono ora visualizzate la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso. [Ulteriori informazioni](building-journeys/journey-gs.md#change-properties)
* Nella schermata dell’elenco dei percorsi, è stato aggiunto il filtro del tipo di percorso . [Ulteriori informazioni](user-interface.md#section_lgm_hpz_pgb)
* Il parametro [!UICONTROL Throttling rate] è stato aggiunto nell’attività Leggi segmento . [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)
