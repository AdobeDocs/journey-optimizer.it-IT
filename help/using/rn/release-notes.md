---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2cd62c97bef156d0c1e7dda8a962be789f8131de
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 42%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** viene continuamente aggiornato con nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


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
<th><strong>Personalizzazione della superficie e-mail - Disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire sottodomini dinamici e parametri di intestazione personalizzati durante la creazione di superfici di canale e-mail, per una maggiore flessibilità e un maggiore controllo sulle impostazioni e-mail.</p>
<p>La personalizzazione della superficie e-mail è attualmente disponibile solo per un set di organizzazioni (Disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
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

**Experience Decisioning** (Disponibilità limitata)

Dalla versione beta a questa versione, sono stati aggiunti i seguenti miglioramenti:

* **Experience Decisioning + Esperienze basate su codice** - Ora puoi sfruttare la funzione Experience Decisioning per utilizzare gli elementi decisionali nelle campagne basate su codice. Nota: il canale di esperienza basato su codice e la funzione Decisioni per le esperienze non sono disponibili per le organizzazioni che hanno acquistato le offerte aggiuntive Healthcare Shield e Privacy and Security Shield di Adobe. [Ulteriori informazioni](../code-based/get-started-code-based.md)
* **Dati contestuali** - Ora puoi sfruttare i dati contestuali provenienti da Adobe Experience Platform nelle regole di decisione e nelle formule di classificazione. [Ulteriori informazioni](../experience-decisioning/context-data.md)
* **Nuova autorizzazione** - È ora disponibile la nuova autorizzazione &quot;Gestisci decisioni esperienza&quot; per la risorsa Gestione delle decisioni. Questa consente di gestire i diritti relativi alla funzione Decisioni per le esperienze. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md)
* **Regole di limitazione** - Ora in Experience Decisioning è possibile aggiungere più regole di limitazione per un determinato elemento decisionale. Ciò offre un maggiore controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../experience-decisioning/items.md#capping)
* **Generazione rapporti** - Ora puoi creare dashboard di reporting personalizzati per le campagne Experience Decisioning utilizzando [!DNL Customer Journey Analytics]. [Ulteriori informazioni](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canale e-mail**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Punteggio spam** (Beta) - Ora puoi controllare il punteggio di posta indesiderata del contenuto in un rapporto spam dedicato. Utilizzando SpamAssassin, Adobe Journey Optimizer può ora testare il contenuto delle e-mail e assegnargli un punteggio per indicare se gli ISP o i provider di cassette postali lo considereranno come spam o meno. [Ulteriori informazioni](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Questa funzionalità è attualmente disponibile nella versione beta e solo per i clienti beta. Per partecipare al programma beta, contatta il rappresentante del tuo Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Percorsi**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Supporto mTLS** - L’autenticazione mTLS è ora supportata nelle azioni personalizzate. Non è necessaria alcuna configurazione aggiuntiva nell’azione o nel percorso personalizzato per attivare mTLS; l’attivazione viene eseguita automaticamente quando viene rilevato un endpoint abilitato per mTLS. [Ulteriori informazioni](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Ricercare tabelle negli eventi** - È ora possibile sfruttare i dati di un set di dati di ricerca quando una relazione è stata definita utilizzando un attributo all’interno di un array di oggetti. I valori di ricerca saranno disponibili in percorsi (condizioni, azioni personalizzate, ecc.) e la personalizzazione dei messaggi. [Ulteriori informazioni](../event/experience-event-schema.md#relationships_limitations)
* **Editor di espressioni avanzate nella configurazione dell’evento** (LA) - È ora possibile sfruttare l’editor di espressioni avanzate durante la configurazione di un evento, consentendoti di definire espressioni più complesse o utilizzare funzioni nella condizione dell’ID evento. Questa funzionalità viene rilasciata in Disponibilità limitata per alcuni clienti. [Ulteriori informazioni](../event/about-creating.md)
* **Criteri di unione** (LA) - I criteri di unione utilizzati da un Percorso sono ora visibili e coerenti in tutto il percorso. Questa funzionalità viene rilasciata in Disponibilità limitata per alcuni clienti. [Ulteriori informazioni](../building-journeys/journey-gs.md#merge-policies)

**Globalizzazione**

Come parte del nostro impegno continuo per offrire un’esperienza utente unificata, armonizziamo la terminologia utilizzata nei prodotti e nelle app Adobe Experience Cloud. Questo influisce sul termine tedesco &quot;Titel&quot; che viene modificato in &quot;Label&quot; quando si riferisce al nome di un oggetto. Le modifiche verranno implementate progressivamente nell’interfaccia utente e nella documentazione di.



