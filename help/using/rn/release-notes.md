---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b80d794f3782056a10310c65144a8eecbddaaf3e
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 75%

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
<th><strong>Generazione di rapporti con il Customer Journey Analytics (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione di reporting di Journey Optimizer offre una migliore interoperabilità con le funzionalità di Customer Journey Analytics, standardizzando il reporting su entrambe le piattaforme e migliorando la coerenza e l’affidabilità dei dati. Questa integrazione diretta tra Journey Optimizer e Customer Journey Analytics fornisce una visione più chiara delle metriche delle prestazioni e consente agli utenti di prendere decisioni più informate.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
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


<table>
<thead>
<tr>
<th><strong>Messaggi multilingue in percorsi e campagne (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile creare contenuti in più lingue in un’unica campagna o in un unico percorso. Con questa funzione, puoi passare da una lingua all’altra durante la modifica della campagna o del percorso, semplificando l’intero processo di modifica e migliorando la capacità di gestire in modo efficiente i contenuti multilingue.</p>
<p>Il contenuto multilingue è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Sperimentazione in percorsi (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Già disponibile nelle campagne, Adobe Journey Optimizer ora supporta gli esperimenti nei percorsi. Gli esperimenti sono test randomizzati: nel contesto dei test online significa che esponi alcuni utenti selezionati in modo casuale a una determinata variante di un messaggio e un altro gruppo di utenti selezionato in modo casuale a un’altra variante o trattamento. Dopo l’esposizione, puoi quindi misurare le metriche del risultato che ti interessano, ad esempio apertura di e-mail, iscrizioni o acquisti.</p>
<p>La sperimentazione nei percorsi è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

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

#### Gestione delle decisioni

* **Supporto di più regole nella gestione delle decisioni**: ora è possibile aggiungere fino a 10 regole di limitazione per una determinata offerta in Gestione delle decisioni. Ciò offre un maggiore controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### Frammenti di contenuto

>[!AVAILABILITY]
>
>Questi miglioramenti verranno introdotti gradualmente nel corso di alcuni giorni dopo il rilascio iniziale. Alcuni utenti potranno accedervi subtio, mentre altri li troveranno nel proprio account con un leggero ritardo.

* È ora possibile modificare i frammenti e propagare le modifiche in tutti i percorsi live e le campagne in cui vengono utilizzati.
* Sono stati introdotti nuovi stati per i frammenti di contenuto: **Bozza**, **Live**, **Pubblicazione** e **Archiviato**.
* Per utilizzare un frammento in un percorso o in una campagna, ora è necessario che sia in stato **Live**. È stato aggiunto un nuovo passaggio al processo di creazione del frammento, che consente di pubblicarlo e renderlo disponibile per l’utilizzo in percorsi e campagne. Tenere presente che la pubblicazione del frammento richiede una nuova autorizzazione.

  **ATTENZIONE**: dato che gli stati **Bozza** e **Live** sono stati introdotti con la versione di giugno di Journey Optimizer, tutti i frammenti creati prima di questa versione presentano lo stato **Bozza** anche se vengono utilizzati in un percorso o in una campagna. Scopri come aggiornare i frammenti esistenti in questa sezione.

Per ulteriori informazioni, consulta la documentazione sui [frammenti di contenuto](../content-management/fragments.md).

#### Percorsi

* Il timeout globale dei percorsi è stato esteso a 91 giorni. [Ulteriori informazioni](../building-journeys/journey-properties.md#global_timeout)

  Questo nuovo timeout verrà applicato a tutti i nuovi percorsi creati. Per ulteriori informazioni, consulta la [sezione Domande frequenti](../building-journeys/journey-properties.md#timeout-faq). Queste modifiche verranno implementate gradualmente nel corso del mese di giugno.


* Adobe Journey Optimizer ora supporta le richieste di accesso/eliminazione della privacy e le richieste di gestione del ciclo di vita dei dati. [Ulteriori informazioni](../privacy/requests.md)
* È ora possibile ridimensionare le colonne nell’inventario del percorso.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* I **Criteri di unione** ora sono disponibili: i criteri di unione utilizzati da un percorso sono quindi visibili e coerenti in tutto il percorso. [Ulteriori informazioni](../building-journeys/journey-properties.md#merge-policies)



#### Campagne

* Durante la creazione di una campagna in Adobe Journey Optimizer, ora è possibile scegliere il tipo di campagna (pianificata o attivata) in una nuova finestra modale. [Ulteriori informazioni](../campaigns/create-campaign.md)

#### Canale e-mail

* **Annullamento iscrizione mailing list** - A seguito dei recenti annunci Gmail e Yahoo per mittenti in blocco, Journey Optimizer supporta l’opzione &quot;post/1 clic&quot; List-Unsubscribe. Consulta le pagine seguenti: [Gestione della rinuncia e-mail](../email/email-opt-out.md#unsubscribe-header) e [Configurare le impostazioni e-mail](../email/email-settings.md#list-unsubscribe).

  **NOTA** - Per qualsiasi nuova superficie di canale, per impostazione predefinita viene attivata l’opzione di intestazione per annullare l’iscrizione all’elenco. Per le superfici esistenti, per default l&#39;opzione URL di annullamento sottoscrizione con un solo clic nelle impostazioni della superficie di canale non è selezionata. Se in precedenza utilizzavi un URL di rinuncia con un solo clic nel corpo dell’e-mail, questa impostazione è ancora valida. Se nelle impostazioni della superficie di canale è selezionato l’URL per l’annullamento dell’iscrizione con un clic, Adobe Journey Optimizer utilizza l’URL per l’annullamento dell’iscrizione con un clic generato di default nelle impostazioni della superficie di canale.

#### Canale SMS

* Ora è possibile aggiungere codici brevi univoci per ogni sandbox con una singola configurazione API, per rendere il processo più efficiente e lineare. [Ulteriori informazioni](../sms/sms-configuration.md)

* Dopo la creazione, il campo **Token API** sulla pagina **Dettagli delle credenziali API** ora è mascherato.

<!--* You can now modify existing SMS configurations.-->

#### Canale in-app

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Ora è possibile utilizzare il plug-in Edge Delivery per ottenere le informazioni necessarie per comprendere e risolvere i problemi relativi alle implementazioni in entrata. [Ulteriori informazioni sulla vista Edge Delivery](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


#### Canale direct mail

* Il canale direct mailing è ora disponibile per tutti i clienti. [Ulteriori informazioni](../direct-mail/get-started-direct-mail.md)
