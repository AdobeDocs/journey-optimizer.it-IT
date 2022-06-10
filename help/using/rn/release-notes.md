---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 32%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Scopri di più su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti alla [newsletter trimestrale di Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Versione di maggio 2022 {#may-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Regole di frequenza dei messaggi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare regole di business cross-channel che escluderanno automaticamente i profili sollecitati eccessivamente da messaggi e azioni.</p>
<img src="assets/frequency-rn.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/frequency-rules.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Email BCC</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Availability date: <strong>May, 31</strong></p>
<p>You can now use the Email BCC (blind carbon copy) capability to store emails sent by Adobe Journey Optimizer. Enable this option in your email presets so that every email sent is blind-copied to your BCC address.</p>
<img src="assets/bcc-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/email-settings.md#bcc-email">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Gestione delle decisioni - Modello di ottimizzazione automatica di AI Ranking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare sistemi basati su modelli in Gestione delle decisioni. Questa nuova funzionalità classifica le offerte da visualizzare per un determinato profilo.</p>
<img src="assets/optimization.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Registri di controllo Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile monitorare le azioni eseguite dagli utenti sulle risorse di Adobe Journey Optimizer.</p>
<img src="assets/audit-rn.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../reports/audit-logs.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Personalizzazione**

* **Nuova funzione helper per per nascondere i caratteri** - `mask` la funzione helper ti consente di sostituire una parte di una stringa con caratteri &quot;X&quot;. [Ulteriori informazioni](../personalization/functions/string.md#mask)

**Pagine di destinazione**

* **Pagine di destinazione senza modulo** - È ora possibile creare e pubblicare una pagina di destinazione che non contiene un modulo e che non richiede alcuna azione da parte dei visitatori.
* **Modelli di pagina di destinazione** - È ora possibile salvare una pagina di destinazione come modello e riutilizzarla durante la creazione di altre pagine di destinazione. [Ulteriori informazioni](../landing-pages/lp-templates.md)
* **Torna alla pagina principale** - È ora possibile aggiungere un collegamento alla pagina principale da qualsiasi pagina secondaria all’interno della stessa pagina di destinazione.
* **Supporto JavaScript personalizzato** - È ora possibile aggiungere JavaScript personalizzati al contenuto della pagina di destinazione per eseguire uno stile avanzato o aggiungere comportamenti personalizzati alle pagine di destinazione.	[Ulteriori informazioni](../landing-pages/lp-custom-js.md)

**Percorsi**

* **Leggi segmento** - I percorsi di segmenti di sola lettura ora passano allo stato Finished 30 giorni dopo l’esecuzione del percorso. Per i segmenti di lettura pianificati, trascorrono 30 giorni dall’esecuzione dell’ultima occorrenza. [Ulteriori informazioni](../building-journeys/read-segment.md)
* **Editor espressioni** - [limite](../building-journeys/functions/functionlimit.md) è stata aggiunta la funzione per consentire di limitare il numero di elementi di un elenco. La [sort](../building-journeys/functions/functionsort.md) consente ora di ordinare un oggetto elenco. È stato aggiunto anche il supporto di listObject al [disctinct](../building-journeys/functions/functiondistinct.md) e [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) funzioni.

**Amministrazione**

* **Aggiornamento del dashboard di utilizzo della licenza** - Il dashboard di utilizzo della licenza disponibile in [!DNL Adobe Journey Optimizer] l&#39;interfaccia utente ora riflette il valore esatto per **Concesso in licenza** Ricchezza media del profilo. Vedrai un calo di questa rappresentazione metrica, il che significa che il limite di licenza è ora correttamente segnalato. [Ulteriori informazioni](../start/licence-usage.md)
