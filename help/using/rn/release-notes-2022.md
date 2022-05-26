---
title: Note sulla versione 2022
description: Note sulla versione di Journey Optimizer 2022
source-git-commit: 4626237ce629dcaec8d20c89db3cb8b517671502
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 97%

---

# Note sulla versione 2022 {#release-notes-2022}

In questa pagina sono elencate tutte le funzioni e i miglioramenti per [!DNL Journey Optimizer] rilasciato nel 2022.

Sono disponibili le ultime note sulla versione [in questa pagina](release-notes.md).

## Versione di aprile 2022 {#april-2022-release}

### Miglioramenti

**Pagine di destinazione**

* **Nuova opzione per le caselle di controllo di consenso/rinuncia** - È ora possibile inserire una singola casella di controllo di consenso/rinuncia nelle pagine di destinazione di iscrizione. Gli utenti devono selezionare la casella di controllo per il consenso (opt-in) e deselezionarla per la rinuncia (opt-out). [Ulteriori informazioni](../landing-pages/design-lp.md#define-lp-specific-content)

* **Campi delle pagine di destinazione precompilati** - È ora possibile consentire agli utenti di precompilare i campi della pagina di destinazione con le informazioni del profilo. [Ulteriori informazioni](../landing-pages/create-lp.md#configure-primary-page)

**Gestione delle decisioni**

* **API Decisioning in Edge** - L’API Edge Decisioning può distribuire ed eseguire il rendering di offerte personalizzate gestite in Offer Decisioning. Puoi creare le offerte e altri oggetti correlati utilizzando l’interfaccia utente (UI) o le API di Offer Decisioning. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Amministrazione**

* **Durata invio PTR** - Le modifiche PTR ora diventano effettive dopo alcune ore. [Ulteriori informazioni](../configuration/ptr-records.md#processing)

**Progettazione e-mail**

* Per progettare il contenuto delle e-mail in Journey Optimizer sono ora disponibili **20 nuovi modelli e-mail**.

**Interfaccia utente**

* **Aiuto contestuale nell’interfaccia utente di Journey Optimizer** - Sono stati aggiunti collegamenti di aiuto contestuali verso diverse pagine della documentazione di Journey Optimizer. Quando disponibile, fai clic sull’icona “i” per visualizzare una breve descrizione della funzionalità corrente e accedere ai relativi articoli.

**Integrazione con Adobe Campaign Standard**

In qualità di cliente Adobe Campaign Standard, ora puoi inviare e-mail, notifiche push e SMS utilizzando Journey Optimizer. Utilizza le nuove azioni integrate per sfruttare le funzionalità di messaggistica transazionale di Campaign Standard in Journey Optimizer.  [Ulteriori informazioni](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Versione di marzo 2022 {#march-2022-release}

### Miglioramenti

**Percorsi**

* Per evitare di includere campi non necessari nello schema di profilo unificato, lo schema Evento delle fasi del percorso non è più abilitato per i profili per impostazione predefinita. Se necessario, puoi attivarlo. [Ulteriori informazioni](../reports/sharing-overview.md)
* I nuovi eventi delle fasi relativi ai processi di esportazione vengono ora inviati da Journey Optimizer a Adobe Experience Platform. Nella documentazione sono stati aggiunti esempi di query. [Ulteriori informazioni](../reports/query-examples.md)

**Gestione delle decisioni**

* Ora puoi specificare se il limite di offerte viene applicato a tutti gli utenti o a un profilo specifico, e a tutti i posizionamenti o a singoli posizionamenti. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)
* L’API Batch Decisioning consente alle organizzazioni di utilizzare la funzionalità Offer Decisioning decisioning per tutti i profili in un dato segmento in una chiamata. Il contenuto dell’offerta per ogni profilo del segmento viene inserito in un set di dati AEP dove è disponibile per flussi di lavoro batch personalizzati. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Amministrazione**

* Ora puoi abilitare/disabilitare il collegamento di annullamento dell’iscrizione nella/dalla intestazione delle e-mail a livello di predefinito del messaggio e impostare un URL di annullamento dell’iscrizione personalizzato a livello di messaggio. [Ulteriori informazioni](../configuration/message-presets.md#list-unsubscribe)
* L’elenco Consentiti ora può essere abilitato e disabilitato tramite l’interfaccia [!DNL Journey Optimizer] sulle sandbox di produzione e di non produzione. [Ulteriori informazioni](../reports/allow-list.md#enable-allow-list)

**Personalizzazione**

* Ora puoi salvare più di 40 espressioni di personalizzazione nella libreria. [Ulteriori informazioni](../personalization/personalization-library.md)

## Versione di febbraio 2022 {#feb-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Pagine di destinazione di iscrizione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare e progettare pagine di destinazione in Journey Optimizer e indirizzare gli utenti a moduli online in cui possono acconsentire o rinunciare alla ricezione delle comunicazioni o iscriversi a un servizio specifico, ad esempio una newsletter.</p>
<p>Per ulteriori informazioni, consulta la <a href="../landing-pages/create-lp.md">documentazione dettagliata</a> e alcuni <a href="../landing-pages/lp-use-cases.md">esempi di casi d’uso</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuova libreria di espressioni di personalizzazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fornisce ora una libreria in cui è possibile accedere a espressioni di personalizzazione predefinite. Queste espressioni sono configurate dagli utenti amministratore.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/personalization-library.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Trasmettere le informazioni per tenere traccia dei messaggi con i parametri di tracciamento UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nel contenuto del messaggio di Journey Optimizer, ora puoi aggiungere parametri UTM ai collegamenti: possono fornire dati aggiuntivi su quel collegamento e aiutarti a identificare dove e perché una persona ha fatto clic sul collegamento.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/message-presets.md#configure-email-settings">documentazione dettagliata</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Per ottimizzare le prestazioni, tutti i percorsi in modalità di test che non sono stati attivati per una settimana torneranno allo stato Bozza. [Ulteriori informazioni](../building-journeys/testing-the-journey.md#important_notes)
* L’integrazione tra Journey Optimizer e Adobe Campaign Classic è stata ottimizzata per migliorarne le prestazioni. La configurazione predefinita del limite è stata modificata in 4000 chiamate/5 minuti.	[Ulteriori informazioni](../action/acc-action.md#important-notes)

**Generazione rapporti**

* È ora possibile filtrare le consegne in base al loro stato:
   * Dall’elenco Esecuzione messaggi, ora puoi escludere le bozze dall’elenco delle consegne.
   * Dai rapporti Live/Global puoi scegliere di escludere gli eventi di test.

* Ora puoi accedere ai rapporti relativi ai dati di ottimizzazione del tempo di invio: il numero di persone che hanno ricevuto messaggi immediatamente e il numero di persone a cui il messaggio è stato inviato con un&#39;ottimizzazione di 1 ora, 2 ore ecc.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestione delle decisioni**

* Le classificazioni e la classificazione IA sono ora raggruppate in un’unica scheda.

## Versione di gennaio 2022 {#january-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Percorsi: ottimizzare l’incremento graduale dell’IP con le condizioni per un limite dei profili</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durante la configurazione di un’attività <strong>Condizione</strong> in un percorso, ora puoi definire un limite di profili. Questo nuovo tipo di condizione consente di impostare un numero massimo di profili per un percorso. Una volta raggiunto tale limite, i profili partecipanti seguono un percorso alternativo. Questo consente di incrementare gradualmente il volume delle consegne (incremento graduale dell’IP). Ad esempio, puoi incrementare gradualmente le consegne per un dominio suddividendo l’esecuzione su più giorni: invia 1000 messaggi il primo giorno, 2000 il secondo giorno e così via.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/condition-activity.md#profile_cap">documentazione dettagliata</a> e alcuni <a href="../building-journeys/ramp-up-deliveries-uc.md">esempi di casi d’uso</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Percorsi: miglioramento delle attività Leggi segmento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Alle attività <strong>Leggi segmento</strong> ricorrenti è stata aggiunta l’opzione <strong>Lettura incrementale</strong>. Questa opzione consente di indirizzare solo i singoli utenti che sono entrati a far parte del segmento dopo l’ultima esecuzione del percorso. La prima esecuzione indirizza sempre tutti i membri del segmento.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Ora è possibile collegare gli eventi dei passaggi di Journey Optimizer ad altri set di dati in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=it). Il campo **profileID** nello schema integrato Evento passaggio percorso è ora definito come campo di identità. [Ulteriori informazioni](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* Quando aggiorni un’offerta, un’offerta di fallback, una raccolta di offerte o una decisione di offerta a cui viene fatto riferimento direttamente o indirettamente in un messaggio pubblicato, gli aggiornamenti vengono ora rispecchiati automaticamente nel messaggio corrispondente, senza doverlo ripubblicare. [Ulteriori informazioni](../offers/offers-e2e.md#insert-decision-in-email)

* Quando si effettua una simulazione per capire quali offerte verranno consegnate per un determinato profilo di test, ora è possibile modificare le impostazioni predefinite della simulazione e visualizzare il codice corrispondente alle simulazioni, utile per la risoluzione dei problemi. [Ulteriori informazioni](../offers/offer-activities/simulation.md#define-simulation-settings)

**Amministrazione**

* Gli amministratori ora possono modificare i record PTR con un sottodominio configurato tramite CNAME. [Ulteriori informazioni](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalizzazione**

* **Aggiungi ai preferiti**: per rendere più efficienti le attività di personalizzazione, è stato introdotto il concetto di salvataggio dei preferiti. L’aggiunta di attributi diversi al menu dei preferiti consente di accedere rapidamente agli elementi utilizzati con maggiore frequenza. [Ulteriori informazioni](../personalization/personalize.md#fav)
