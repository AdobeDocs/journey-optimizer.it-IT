---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 522f1815ae6de33f9e0a7ea598d52c8e88d2ff0d
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 64%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Note sulla versione di giugno 2024 {#24-6-2024}

**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità del rilascio**.

**Data di rilascio**: 18-19 giugno 2024

### Nuove funzionalità {#june-24-features}

Questa versione include le nuove funzionalità elencate di seguito.

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


<table>
<thead>
<tr>
<th><strong>Personalizzazione Frammenti di contenuto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile definire in un frammento campi specifici che possono essere modificati quando il frammento viene aggiunto a una campagna o a un percorso. Questo consente di regolare le parti di contenuto al momento dell’utilizzo, fornendo flessibilità per sovrascrivere i valori predefiniti con dettagli specifici del contesto.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/customizable-fragments.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>




<table>
<thead>
<tr>
<th><strong>Generazione di rapporti con il Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il reporting di Journey Optimizer è ora completamente integrato con le funzionalità di Customer Journey Analytics, standardizzando il reporting su entrambe le piattaforme e migliorando la coerenza e l’affidabilità dei dati. Questa integrazione diretta tra Journey Optimizer e il Customer Journey Analytics fornisce una visione più chiara delle metriche delle prestazioni, consentendo agli utenti di prendere decisioni più informate.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/report-gs-cja.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente IA in Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Assistente IA è una funzione dell’interfaccia utente che consente di accedere ai concetti Adobe, comprenderli e ottenere informazioni operative per l’ambiente specifico. È disponibile in diversi prodotti Adobe Experience Cloud, tra cui Adobe Journey Optimizer.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ai-assistant.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns (Limited Availability)</strong><br/></th>
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

* **Supporto di più regole nella gestione delle decisioni**: ora è possibile aggiungere fino a 10 regole di limitazione per una determinata offerta in Gestione delle decisioni. Ciò offre un maggiore controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**Frammenti di contenuto**

>[!AVAILABILITY]
>
>Tieni presente che questi miglioramenti verranno implementati gradualmente nel corso di alcuni giorni dopo la versione iniziale. Alcuni utenti avranno accesso immediato, altri potrebbero notare un ritardo prima che questo diventi disponibile nei loro ambienti.

* È ora possibile modificare i frammenti e propagare le modifiche in tutti i percorsi live e le campagne in cui vengono utilizzati.
* Sono stati introdotti nuovi stati per i frammenti di contenuto: **Bozza**, **Live**, **Pubblicazione** e **Archiviato**.
* Per utilizzare un frammento in un percorso o in una campagna, ora è necessario che sia in stato **Live**. È stato aggiunto un nuovo passaggio al processo di creazione del frammento, che consente di pubblicarlo e renderlo disponibile per l’utilizzo in percorsi e campagne. Tenere presente che la pubblicazione del frammento richiede una nuova autorizzazione.

  **ATTENZIONE**: dato che gli stati **Bozza** e **Live** sono stati introdotti con la versione di giugno di Journey Optimizer, tutti i frammenti creati prima di questa versione presentano lo stato **Bozza** anche se vengono utilizzati in un percorso o in una campagna. Scopri come aggiornare i frammenti esistenti in questa sezione.

Per ulteriori informazioni, consulta [frammento di contenuto](../content-management/fragments.md) documentazione.

**Percorsi**

* Il timeout globale dei Percorsi è stato esteso a 91 giorni. [Ulteriori informazioni](../building-journeys/journey-properties.md#global_timeout)

  Questo nuovo timeout verrà applicato a tutti i nuovi percorsi creati. Fai riferimento a questo [Sezione Domande frequenti](../building-journeys/journey-properties.md#timeout-faq) per ulteriori informazioni. Tieni presente che queste modifiche verranno implementate gradualmente nel corso del mese di giugno.


* Adobe Journey Optimizer ora supporta le richieste di accesso/cancellazione della privacy e le richieste di gestione del ciclo di vita dei dati. [Ulteriori informazioni](../privacy/requests.md)
* È ora possibile ridimensionare le colonne nell’inventario del percorso.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* I **Criteri di unione** ora sono disponibili: i criteri di unione utilizzati da un percorso sono quindi visibili e coerenti in tutto il percorso [Ulteriori informazioni](../building-journeys/journey-properties.md#merge-policies)



**Campagne**

* Durante la creazione di una campagna in Adobe Journey Optimizer, ora puoi scegliere il tipo di campagna (pianificata o attivata) in una nuova finestra modale. [Ulteriori informazioni](../campaigns/create-campaign.md)

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**Canale SMS**

* Ora puoi aggiungere codici brevi univoci per ogni sandbox con una singola configurazione API, per rendere il processo più efficiente e semplificato. [Ulteriori informazioni](../sms/sms-configuration.md)

* Dopo la creazione, il **Token API** campo sul **Dettagli delle credenziali API** La pagina è ora nascosta.

<!--* You can now modify existing SMS configurations.-->

**Canale in-app**

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Ora puoi utilizzare il plug-in Edge Delivery per ottenere le informazioni necessarie per comprendere e risolvere i problemi relativi alle implementazioni in entrata. [Ulteriori informazioni sulla vista Consegna Edge](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


**Canale direct mail**

* Il canale direct mailing è ora disponibile per tutti i clienti. [Ulteriori informazioni](../direct-mail/get-started-direct-mail.md)
