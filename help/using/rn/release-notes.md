---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 8766f64c4ea7985c6c9d6e4ba022ef6b1fc0dbed
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 86%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Scopri di più su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti alla [newsletter trimestrale di Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Versione di luglio 2022 {#july-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Nuovo flusso di messaggistica in linea</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fornisce un nuovo flusso per la creazione dei messaggi nei Percorsi. La messaggistica in linea consente agli utenti di risparmiare tempo e semplifica il processo del flusso di lavoro per creare e inviare un’e-mail, una notifica push o un SMS in Journey Optimizer. Rimuovendo i messaggi come passaggio separato e rendendoli modificabili in linea nell’ambito di un’azione nell’area di lavoro del Percorso, si riducono i clic e le schermate necessari per progettare e modificare i contenuti.</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../messages/get-started-content.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Controllo degli accessi basato su attributi (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile identificare i campi dello schema con etichette che definiscono gli ambiti di utilizzo organizzativi o dei dati. Gli amministratori possono utilizzare l’interfaccia Autorizzazioni per definire i criteri di accesso che coprono i campi dello schema XDM per controllare l’accesso consentito a utenti o gruppi di utenti (utenti interni, esterni o di terze parti) e gestire l’accesso a tipi specifici di dati (ad esempio Dati personali sensibili/SPD).</p>
<p>Il controllo degli accessi basato su attributi è attualmente limitato ad alcuni utenti e verrà esteso a tutti gli ambienti con una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../administration/attribute-based-access.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Processi decisionali in batch</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile eseguire processi decisionali in batch direttamente dall’interfaccia utente; non è quindi più necessario ricorrere a uno sviluppatore per eseguire processi API in batch, riducendo il tempo necessario per il marketing. Questa nuova interfaccia consente di creare nuovi processi e gestire quelli correnti o passati.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/batch-delivery.md">documentazione dettagliata.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizza automaticamente l’offerta più performante nelle decisioni (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nella gestione delle decisioni, ora puoi utilizzare sistemi di modelli di ottimizzazione personalizzati. Questo nuovo tipo di modello consente di ottimizzare e personalizzare le offerte in base a segmenti e prestazioni.</p>
<p>L’utilizzo di modelli di ottimizzazione personalizzati basati su IA è attualmente limitato ad alcuni utenti e verrà esteso a tutti gli ambienti con una versione futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/ranking/personalized-optimization-model.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* **Terminazione di un percorso** - Nell&#39;area di lavoro del percorso, il **Fine** l’attività è stata rimossa dalla palette. I tag finali vengono ora aggiunti per impostazione predefinita alla fine di ciascun percorso e non possono essere rimossi. Questo miglioramento consente una migliore generazione di rapporti su dove un cliente ha abbandonato il percorso, senza che sia necessaria alcuna azione da parte del professionista del percorso. Fai riferimento a [documentazione](../building-journeys/journey-end.md) e [video sulle funzioni](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.

**Messaggi**

* I predefiniti per messaggi sono ora **superfici di canale**. [Ulteriori informazioni](../configuration/channel-surfaces.md)

**Amministrazione**

* **Modifica record PTR**: ora, quando si aggiorna un record PTR, il tempo di elaborazione richiederà solo un massimo di 3 ore. [Ulteriori informazioni](../configuration/ptr-records.md#processing)

* **Interfaccia utente per l’elenco Consentiti**: è ora possibile utilizzare l’interfaccia utente di Journey Optimizer per aggiungere nuovi indirizzi e-mail o domini all’elenco Consentiti. [Ulteriori informazioni](../configuration/allow-list.md)

* **Aggiornamento della logica per l’elenco Consentiti**: ora la logica dell’elenco Consentiti si applica non appena la funzione è abilitata, anche se l’elenco è vuoto. [Ulteriori informazioni](../configuration/allow-list.md#logic)

* **Parametri di tracciamento URL** - È ora possibile utilizzare l’editor espressioni per configurare i parametri di tracciamento URL nelle superfici dell’e-mail (ad es. predefiniti). [Ulteriori informazioni](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **Dimensione del pubblico**: ora durante la creazione di una regola decisionale, durante la selezione di un segmento o di una regola per impostare un’idoneità per l’offerta o quando aggiungi un segmento o una regola a un ambito decisionale, nell’interfaccia utente viene visualizzato un nuovo componente per la stima delle dimensioni del pubblico.