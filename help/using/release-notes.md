---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
source-git-commit: a1800c333bfbee178682d773c729aad7e23d86d0
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 15%

---


# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Puoi anche consultare gli [Aggiornamenti alla documentazione](documentation-updates.md) più recenti.

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
<p>Adobe Experience Platform ti consente di definire relazioni tra schemi per utilizzare un set di dati come tabella di ricerca per un altro. Ora è possibile sfruttare i dati provenienti da uno schema collegato.</p>
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
<p>Ora puoi definire un elenco di sicurezza per l’invio specifico a livello di sandbox, in modo da disporre di un ambiente sicuro a scopo di test. In un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti ti assicura di non correre il rischio di inviare messaggi indesiderati ai clienti. Questa funzione è abilitata sfruttando le API di eliminazione.</p>
<p>Per ulteriori informazioni, consulta la <a href="allow-list.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Il tasso di limitazione complessivo di tutti i segmenti letti eseguiti contemporaneamente nella stessa sandbox è limitato a 17.000 messaggi al secondo. [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Il campo **Durata cache** è stato rimosso dal riquadro di configurazione dell&#39;origine dati. [Ulteriori informazioni](datasource/about-data-sources.md)
* Per le origini dati esterne, ora viene definita automaticamente una regola di limitazione di 15 chiamate al secondo. [Ulteriori informazioni](configuration/external-systems.md#capping)
* Per i percorsi live, nella schermata delle proprietà del percorso vengono ora visualizzate la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso. [Ulteriori informazioni](building-journeys/journey-gs.md#change-properties)
* Nella schermata dell’elenco dei percorsi, è stato aggiunto il filtro del tipo di percorso . [Ulteriori informazioni](user-interface.md#section_lgm_hpz_pgb)
* Il parametro **[!UICONTROL Throttling rate]** è stato aggiunto nell’attività Leggi segmento . [Ulteriori informazioni](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Anteprima e verifica dei messaggi**

* Identità e spazio dei nomi ora sono visibili nella schermata **[!UICONTROL Preview]** . [Ulteriori informazioni](preview.md#preview-your-messages)
* Il numero di e-mail di test per le bozze è ora limitato a 10.
* I caratteri consentiti per il **prefisso della riga oggetto** nelle bozze sono ora limitati. [Ulteriori informazioni](preview.md#send-proofs)

**Editor di espressioni di personalizzazione**

* L’elenco a discesa helper è stato rinominato e riordinato.

### Correzioni

* È stato risolto un problema che causava la consegna di messaggi duplicati per la consegna di e-mail batch.
* Gli eventi vengono ora generati di conseguenza quando l’invio e-mail non viene eseguito una volta terminato il periodo di esecuzione dei nuovi tentativi.
* È stato risolto un problema a causa del quale le informazioni IP mancavano nella schermata Record PTR.
* È ora implementata la localizzazione nella barra delle offerte nell’editor espressioni.
* È stata corretta la spaziatura errata nei popup delle informazioni.
* È stato risolto un problema in E-mail designer durante il caricamento di un file HTML in cui il foglio di stile interno con proprietà `background-image` non era supportato.

