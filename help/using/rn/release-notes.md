---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 16bda5dcdfdc65f236d814ec02c6222b98a5652f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
<th><strong>Nuovo flusso di messaggi in-line</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fornisce un nuovo flusso per la creazione dei messaggi nei Percorsi. La messaggistica in-line consentirà agli utenti di risparmiare tempo significativo e semplificherà il processo del flusso di lavoro per creare e inviare un’e-mail, una notifica push o un SMS in Journey Optimizer. Rimuovendo i messaggi come passaggio separato e rendendoli modificabili in linea come parte di un’azione nell’area di lavoro del Percorso, gli utenti dovranno fare clic su un numero inferiore di pulsanti e navigare in un numero inferiore di schermate per progettare e modificare il contenuto.</p>
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
<p>È ora possibile identificare i campi dello schema con le etichette che definiscono gli ambiti di utilizzo organizzativi o dei dati. Gli amministratori possono utilizzare l’interfaccia Autorizzazioni per definire i criteri di accesso che coprono i campi dello schema XDM e gestire meglio l’accesso dato a utenti o gruppi di utenti (utenti interni, esterni o di terze parti) e gestire l’accesso a tipi specifici di dati (ad esempio Dati personali sensibili/SPD).</p>
<p>L'utilizzo del controllo di accesso basato su attributi è attualmente limitato agli utenti selezionati e verrà distribuito a tutti gli ambienti in una versione futura.</p>
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
<p>È ora possibile eseguire processi di decisione batch dall'interfaccia utente, in modo che non sia necessario uno sviluppatore per eseguire processi api batch e posso ridurre il tempo necessario per il marketing. Questa nuova interfaccia ti consente di creare lavori e gestire i lavori correnti/passati.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/batch-delivery.md">documentazione dettagliata.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizza automaticamente l'offerta più performante nelle tue decisioni (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare sistemi di modelli di ottimizzazione personalizzati in Gestione delle decisioni. Questo nuovo tipo di modello ti consente di ottimizzare e personalizzare le offerte in base ai segmenti e alle prestazioni delle offerte.</p>
<p>L’utilizzo di modelli AI di ottimizzazione personalizzati è attualmente limitato agli utenti selezionati e verrà distribuito a tutti gli ambienti in una versione futura.</p>
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

* I predefiniti per messaggi sono ora **superfici del canale**. [Ulteriori informazioni](../configuration/channel-surfaces.md)

**Amministrazione**

* **Edizione record PTR** - Ora, quando si aggiorna un record PTR, il tempo di elaborazione richiederà solo 3 ore. [Ulteriori informazioni](../configuration/ptr-records.md#processing)

* **Interfaccia utente Elenco Consentiti** - È ora possibile utilizzare l’interfaccia utente di Journey Optimizer per aggiungere nuovi indirizzi e-mail o domini all’elenco Consentiti. [Ulteriori informazioni](../configuration/allow-list.md)

* **Aggiornamento della logica di Elenco Consentiti** - Ora la logica di elenco Consentiti si applica non appena la funzione è abilitata, anche se l’elenco è vuoto. [Ulteriori informazioni](../configuration/allow-list.md#logic)

* **Parametri di tracciamento URL** - Ora puoi utilizzare l’editor espressioni per configurare i parametri di tracciamento URL nelle superfici dell’e-mail (ad esempio i predefiniti per messaggi). [Ulteriori informazioni](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **Dimensione del pubblico** - Ora nell’interfaccia utente viene visualizzato un nuovo componente per la stima delle dimensioni del pubblico durante la creazione di una regola decisionale, durante la selezione di un segmento o di una regola per impostare un’idoneità per l’offerta o quando si aggiunge un segmento o una regola a un ambito decisionale.