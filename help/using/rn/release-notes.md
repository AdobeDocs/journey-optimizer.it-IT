---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d2e53b85638a7ca5defcbe67aff6e19bc029f9a0
workflow-type: tm+mt
source-wordcount: '1321'
ht-degree: 62%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Note preliminari sulla versione di giugno 2024 {#24-6-2024}

**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità del rilascio**.

**Data di rilascio**: 18-19 giugno 2024

### Nuove funzionalità {#june-24-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Flusso di lavoro di riscaldamento IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se invii un’e-mail con un nuovo indirizzo IP, ora puoi eseguire facilmente i flussi di lavoro di riscaldamento IP direttamente dall’interfaccia utente. Adobe Journey Optimizer offre un modo standardizzato ed efficiente di riscaldare gli indirizzi IP seguendo le best practice per una consegna ottimale.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


<table>
<thead>
<tr>
<th><strong>Assistente AI in Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’Assistente AI è una funzione dell’interfaccia utente che consente di navigare tra i concetti Adobi e comprenderli e ottenere informazioni operative per l’ambiente specifico. È disponibile in diversi prodotti Adobe Experience Cloud, tra cui Adobe Journey Optimizer.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ai-assistant.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Reporting with Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer reporting is now fully integrated with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. This seamless integration between Journey Optimizer and Customer Journey Analytics provides a clearer view of performance metrics, enabling users to make more informed decisions.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns  (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
<p>Multilingual content is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
<p>Experimentation in journeys is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->



<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Miglioramenti {#june24-improvements}

Questa versione include i miglioramenti elencati di seguito.


**Gestione delle decisioni**

* **Supporto di più regole nella gestione delle decisioni** - È ora possibile aggiungere fino a 10 regole di limite per una determinata offerta in Gestione delle decisioni. Ciò offre un maggiore controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**Frammenti di contenuto**

>[!AVAILABILITY]
>
>Tieni presente che questi miglioramenti verranno implementati gradualmente nel corso di alcuni giorni dopo la versione iniziale. Alcuni utenti avranno accesso immediato, altri potrebbero notare un ritardo prima che questo diventi disponibile nei loro ambienti.

* È ora possibile modificare i frammenti e propagare le modifiche in tutti i percorsi live e le campagne in cui vengono utilizzati.
* Sono stati introdotti nuovi stati per i frammenti di contenuto: **Bozza**, **Live**, **Pubblicazione**, e **Archiviato**.
* Per utilizzare un frammento in un percorso o in una campagna, ora è necessario che sia nel **Live** stato. È stato aggiunto un nuovo passaggio al processo di creazione del frammento, che consente di pubblicarlo e renderlo disponibile per l’utilizzo in percorsi e campagne. La pubblicazione del frammento richiede una nuova autorizzazione.

  **ATTENZIONE** - Da **Bozza** e **Live** sono stati introdotti gli stati con la versione di giugno di Journey Optimizer; tutti i frammenti creati prima di questa versione presentano **Bozza** anche se vengono utilizzati in un percorso o in una campagna. Scopri come aggiornare i frammenti esistenti in questa sezione.

**Percorsi**

* Il timeout globale del percorso è stato aumentato da 30 a 90 giorni.
* Adobe Journey Optimizer ora supporta le richieste di accesso/cancellazione della privacy e le richieste di gestione del ciclo di vita dei dati.
* È ora possibile ridimensionare le colonne nell’inventario del percorso.
* **Editor di espressioni avanzate nella configurazione dell’evento** è ora GA - È ora possibile sfruttare l’editor di espressioni avanzate durante la configurazione di un evento, consentendoti di definire espressioni più complesse o utilizzare funzioni nella condizione dell’ID evento. Questa funzionalità viene rilasciata in Disponibilità limitata per alcuni clienti. <!--[Read more](../event/about-creating.md)-->
* **Criteri di unione** sono ora GA: i criteri di unione utilizzati da un Percorso sono ora visibili e coerenti in tutto il percorso. Questa funzionalità viene rilasciata in Disponibilità limitata per alcuni clienti. <!--[Read more](../building-journeys/journey-gs.md#merge-policies)-->



**Campagne**

* Durante la creazione di una campagna in Adobe Journey Optimizer, ora puoi scegliere il tipo di campagna (pianificata o attivata) in una nuova finestra modale.

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**Canale SMS**

* Ora puoi aggiungere codici brevi univoci per ogni sandbox con una singola configurazione API, per rendere il processo più efficiente e semplificato.
  <!--* You can now modify existing SMS configurations.-->

**Canale in-app**

* **Frammento di espressione** - I frammenti di espressione sono ora disponibili per **Canale in-app**. <!--[Read more](../personalization/use-expression-fragments.md)-->


* Ora puoi utilizzare il plug-in Edge Delivery per ottenere le informazioni necessarie per comprendere e risolvere i problemi relativi alle implementazioni in entrata.

<!--
**Direct mail channel**

* Direct mail channel is now available for organizations that have purchased the Adobe **Healthcare Shield** and **Privacy and Security Shield** add-on offerings.
-->

## Note sulla versione di maggio 2024 {#may-2024}

**Data di rilascio**: 21-22 maggio 2024

### Nuove funzionalità {#e-features}

Questa versione include le nuove funzionalità elencate di seguito.

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
<p>Questi elementi decisionali sono integrati direttamente in un’ampia gamma di superfici in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne di Journey Optimizer. I criteri decisionali relativi alla funzione Decisioni per le esperienze sono disponibili per l’utilizzo solo in campagne di esperienza basate su codice.</p>
<p>La funzione Decisioni per le esperienze è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/gs-experience-decisioning.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalizzazione della superficie e-mail: disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire sottodomini dinamici e parametri di intestazione personalizzati durante la creazione di superfici di canale e-mail, per maggiore flessibilità e controllo sulle impostazioni e-mail.</p>
<p>La personalizzazione della superficie e-mail è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../email/surface-personalization.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Decisioni per le esperienze**: disponibilità limitata

Dalla versione beta a quella con Disponibilità limitata, sono stati aggiunti i seguenti miglioramenti:

* **Decisioni per le esperienze + Esperienze basate su codice**: ora puoi sfruttare la funzione Decisioni per le esperienze per utilizzare gli elementi decisionali nelle campagne basate su codice. Nota: il canale di esperienza basato su codice e la funzione Decisioni per le esperienze non sono disponibili per le organizzazioni che hanno acquistato le offerte aggiuntive Healthcare Shield e Privacy and Security Shield di Adobe. [Ulteriori informazioni](../code-based/get-started-code-based.md)
* **Dati contestuali**: ora puoi sfruttare i dati contestuali provenienti da Adobe Experience Platform nelle regole di decisione e nelle formule di classificazione. [Ulteriori informazioni](../experience-decisioning/context-data.md)
* **Nuova autorizzazione**: è ora disponibile la nuova autorizzazione “Gestisci decisioni per le esperienze” per la risorsa Gestione delle decisioni. Questa consente di gestire i diritti relativi alla funzione Decisioni per le esperienze. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md)
* **Regole di limitazione**: ora, in Decisione per le esperienze, è possibile aggiungere più regole di limitazione per un determinato elemento in Decisioni per le esperienze. Ciò offre un maggiore controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../experience-decisioning/items.md#capping)
* **Reporting**: ora puoi creare dashboard di reporting personalizzate delle campagne di Decisioni per le esperienze tramite [!DNL Customer Journey Analytics]. [Ulteriori informazioni](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canale e-mail**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Punteggio contenuto indesiderato** (beta): ora puoi controllare il punteggio del contenuto indesiderato in un rapporto relativo dedicato. Utilizzando SpamAssassin, Adobe Journey Optimizer può ora testare il contenuto delle e-mail e assegnargli un punteggio per indicare se gli ISP o i provider di caselle postali lo considereranno come contenuto indesiderato o meno. [Ulteriori informazioni](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Questa funzionalità è disponibile nella versione beta e solo per clienti beta. Per partecipare al programma Beta, contatta il tuo rappresentante Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Percorsi**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Supporto mTLS**: l’autenticazione mTLS è ora supportata nelle azioni personalizzate. Non è necessaria alcuna configurazione aggiuntiva nell’azione o nel percorso personalizzato per attivare mTLS; l’attivazione viene eseguita automaticamente quando viene rilevato un endpoint abilitato per mTLS. [Ulteriori informazioni](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tabelle di ricerca negli eventi**: è ora possibile sfruttare i dati di un set di dati di ricerca quando una relazione è stata definita utilizzando un attributo all’interno di un array di oggetti. I valori di ricerca saranno disponibili nei percorsi (condizioni, azioni personalizzate, ecc.) e nella personalizzazione dei messaggi. [Ulteriori informazioni](../event/experience-event-schema.md#relationships_limitations)
* **Editor di espressioni avanzate nella configurazione dell’evento** (Disponibilità limitata): è ora possibile sfruttare l’editor di espressioni avanzate durante la configurazione di un evento, consentendoti di definire espressioni più complesse o utilizzare funzioni nella condizione per l’ID evento. Questa funzionalità viene rilasciata in Disponibilità limitata per clienti selezionati. [Ulteriori informazioni](../event/about-creating.md)
* **Criteri di unione** (Disponibilità limitata): i criteri di unione utilizzati da un percorso sono ora visibili e coerenti in tutto il percorso. Questa funzionalità viene rilasciata in Disponibilità limitata per clienti selezionati. [Ulteriori informazioni](../building-journeys/journey-gs.md#merge-policies)

**Globalizzazione**

Come parte del nostro impegno continuo per offrire un’esperienza utente unificata, armonizziamo la terminologia utilizzata nei prodotti e nelle app di Adobe Experience Cloud. Questo influisce sul termine tedesco “Titel” che viene modificato in “Label” quando si riferisce al nome di un oggetto. Le modifiche verranno implementate progressivamente nell’interfaccia utente e nella documentazione.



