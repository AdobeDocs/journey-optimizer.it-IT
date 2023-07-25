---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 380d07067a999de439ebf5a4198a203c1aa6b1d8
workflow-type: tm+mt
source-wordcount: '3125'
ht-degree: 85%

---

# Note sulla versione {#release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

Le note sulle versioni precedenti sono disponibili in [questa pagina](release-notes-2022.md). Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Note preliminari sulla versione di luglio 2023 {#july-rn-2023}

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità del rilascio. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati alla data di rilascio.


**Data di rilascio**: 26-27 luglio

### Nuove funzionalità{#july-2023-features}

Questa versione include le nuove funzionalità elencate di seguito.



<table>
<thead>
<tr>
<th><strong>Composizione del pubblico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare flussi di lavoro di composizione per combinare i tipi di pubblico di Adobe Experience Platform esistenti in un’area di lavoro visiva e sfruttare varie attività (divisione, arricchimento...) per creare nuovi tipi di pubblico. I tipi di pubblico appena creati vengono salvati nuovamente in Adobe Experience Platform insieme ai tipi di pubblico esistenti e possono essere utilizzati nelle campagne Journey Optimizer per il targeting dei clienti.</p>
<img src="../audience/assets/audiences-publish.png"/>
<p>Per ulteriori informazioni, consulta la <a href="../audience/get-started-audience-orchestration.md">documentazione dettagliata</a>.</p>
<p>La composizione del pubblico è completamente integrata con il nuovo menu "Tipi di pubblico" di Adobe Experience Platform, che funge da portale centralizzato per i tipi di pubblico. Ora puoi utilizzare una pagina Sfoglia che include una nuova dashboard con tendenze dei segmenti e sovrapposizioni per trovare nuove informazioni ed esplorare gli strumenti organizzativi per la cartella e i tag. In questa esperienza sono incorporati i controlli di governance per l’etichettatura standardizzata del pubblico e le funzionalità di gestione del ciclo di vita del pubblico per gestire i flussi di lavoro di attivazione. Con questa nuova esperienza di gestione, ora puoi gestire in modo semplice e sicuro i tipi di pubblico da un’unica posizione. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it" target="_blank">Documentazione di Adobe Experience Platform</a>.</p></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
<img src="../direct-mail/assets/direct-mail-properties.png">
<p>For more information, refer to the <a href="../direct-mail/create-direct-mail.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Convertire il contenuto HTML per e-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi importare e convertire qualsiasi contenuto HTML nell’editor e-mail di Journey Optimizer. I blocchi di contenuto vengono identificati automaticamente e sono disponibili nell’e-mail designer: utilizza le sue potenti funzionalità di progettazione per aggiornarlo e personalizzarlo.</p>
<img src="../email/assets/html-imported_2.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Utilizzare i tag in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oltre a campagne e percorsi, ora puoi assegnare Tag unificati Adobe Experience Platform alle pagine di destinazione, ai modelli di contenuto, ai frammenti e agli elenchi di abbonamento. Ciò ti consente di classificarli facilmente e di migliorare la ricerca e la navigazione in tutti gli elenchi. </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../start/search-filter-categorize.md#tags">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>API per modelli di contenuto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare e gestire modelli di contenuto Adobe Journey Optimizer utilizzando API dedicate, fornendo un’integrazione perfetta con il sistema di contenuti esistente.</p>
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#july-2023-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Percorsi**

<!--* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
È stato introdotto un nuovo tipo di avviso di sistema. Ora puoi ricevere una notifica quando un’azione personalizzata non riesce.


**Campagne**

Gli eventi contestuali relativi alle campagne sono ora disponibili per l’utilizzo nel menu &quot;Attributi contestuali&quot; dell’editor di personalizzazione.


**Tipi di pubblico**

Sono stati apportati miglioramenti al selettore del pubblico in percorsi o campagne, con l’aggiunta di nuove colonne che mostrano l’origine e la frequenza di aggiornamento dei tipi di pubblico. Con il rilascio del portale di composizione del pubblico, Adobe Experience Platform e Adobe Journey Optimizer hanno aggiornato l’utilizzo di &quot;tipi di pubblico&quot; e &quot;segmenti&quot; all’interno del sistema e della documentazione.

* Pubblico: un set di persone, account, famiglie o altre entità che hanno in comune caratteristiche e/o comportamenti specifici.
* Definizione di segmento: in Adobe Experience Platform, le regole utilizzate per descrivere le caratteristiche o il comportamento chiave di un pubblico di destinazione. Questo termine era precedentemente noto semplicemente come “segmento”.

Di conseguenza, in Adobe Journey Optimizer e nell’interfaccia utente di Adobe Experience Platform, &quot;Segmenti&quot; viene sostituito da &quot;Tipi di pubblico&quot; per riflettere questo nuovo percorso di creazione e gestione del pubblico.

**API**

Il metodo JWT per generare token di accesso per l’autenticazione API Adobe Journey Optimizer è stato dichiarato obsoleto. Tutte le nuove integrazioni devono essere create utilizzando il metodo di autenticazione server-to-server OAuth. Adobe consiglia inoltre di migrare le integrazioni esistenti al metodo OAuth. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.


**Altre modifiche**

L’esportazione dei set di dati Journey Optimizer nelle destinazioni di archiviazione cloud è ora disponibile per tutti i clienti come versione beta pubblica. Questa funzione ti consente di stabilire una connessione live con le posizioni di archiviazione cloud per esportare il contenuto dei set di dati. [Ulteriori informazioni](../data/export-datasets.md)





## Note sulla versione di giugno 2023 {#june-rn-2023}

<table>
<thead>
<tr>
<th><strong>Campagne attivate da API per casi d’uso di marketing</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi utilizzare le API per attivare campagne di marketing in Adobe Journey Optimizer da un sistema esterno.</p>
<p>Fino a questa versione, la funzionalità delle campagne attivate da API copriva varie esigenze di messaggistica operativa e transazionale, come le reimpostazioni di password o i token OTP, ma non poteva essere utilizzata per creare campagne di marketing. I canali disponibili per le campagne attivate da API sono: e-mail, SMS e messaggi push.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../campaigns/api-triggered-campaigns.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<!--
### Improvements {#june-2023-improvements}


**Audiences**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.

**Journeys**

You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

<!--
## June 2023 early release notes {#june-rn-2023}

Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Audiences**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    


**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.     

* A new type of system alert has been introduced. You can now get notified when a custom action fails.
-->

## Note sulla versione di maggio 2023 {#may-rn-2023}

### Nuove funzionalità{#may-2023-features}



<table>
<thead>
<tr>
<th><strong>Sperimentazione sui contenuti nelle campagne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta gli esperimenti nelle campagne. Gli esperimenti sono test randomizzati: nel contesto dei test online significa che esponi alcuni utenti selezionati in modo casuale a una determinata variante di un messaggio e un altro gruppo di utenti selezionato in modo casuale a un’altra variante o trattamento. Dopo l’esposizione, puoi quindi misurare le metriche del risultato che ti interessano, ad esempio apertura di e-mail, iscrizioni o acquisti.</p>
<img src="assets/do-not-localize/experiment.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../campaigns/content-experiment.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Objective reporting and performance measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the Objectives tab of your campaign reports.</p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../reports/campaign-global-report.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->


<table>
<thead>
<tr>
<th><strong>Crea e utilizza frammenti nel contenuto dell’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare, utilizzare e gestire frammenti per assemblare rapidamente e-mail e modelli di contenuto. Un frammento è un componente riutilizzabile predefinito a cui è possibile fare riferimento in più e-mail tra campagne e percorsi di Journey Optimizer per un processo di progettazione migliorato e accelerato.</p>
<img src="assets/do-not-localize/fragments.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../email/fragments.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Utilizzare i tag nelle campagne (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile assegnare tag unificati Adobe Experience Platform alle campagne. Questo consente di classificarle facilmente e migliorare la ricerca dall’elenco delle campagne. Ricorda che la funzione Tag unificati è attualmente in versione beta.</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../start/search-filter-categorize.md#tags">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Modello di classificazione IA per l’ottimizzazione personalizzata (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>I modelli di classificazione IA per l’ottimizzazione personalizzata sono ora disponibili in Gestione decisioni. Questo nuovo tipo di modello consente di ottimizzare e personalizzare le offerte in base alle loro prestazioni e ai tipi di pubblico.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/ranking/personalized-optimization-model.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>



### Miglioramenti {#may-2023-improvements}

**Tipi di pubblico**

* In preparazione alla disponibilità generale della funzione Audience Portal, Adobe Experience Platform sta aggiornando l’utilizzo di “tipi di pubblico” e “segmenti” all’interno del sistema e della documentazione.

   * Pubblico: un set di persone, account, famiglie o altre entità che hanno in comune caratteristiche e/o comportamenti specifici.
   * Definizione di segmento: in Adobe Experience Platform, le regole utilizzate per descrivere le caratteristiche o il comportamento chiave di un pubblico di destinazione. Questo termine era precedentemente noto semplicemente come “segmento”.

  Di conseguenza, in Adobe Journey Optimizer e nell’interfaccia utente di Adobe Experience Platform, vedrai che “Segmenti” è stato sostituito da “Tipi di pubblico” per riflettere questo nuovo percorso di creazione e gestione del pubblico.

  Le traduzioni del termine inglese “audience” (pubblico) quando si fa riferimento a un gruppo di profili target per la ricezione di un messaggio sono state armonizzate in tutti i prodotti Digital Experience per alcune lingue:

   * Tedesco: Zielgruppe
   * Portoghese brasiliano: público-alvo
   * Spagnolo: público destinatario

<!--* Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.-->

**Canale SMS**

* Infobip è stato aggiunto come provider disponibile per la configurazione delle superfici di canale SMS. [Maggiori informazioni](../sms/sms-configuration.md)
* Twilio: la configurazione delle credenziali API ora include la possibilità di aggiungere l’identificatore SID del servizio di messaggistica per un’integrazione perfetta con l’account Twilio. [Maggiori informazioni](../sms/sms-configuration.md)

**Canale in-app**

* Sono state aggiunte nuove regole di attivazione dei messaggi per Adobe Places Service. [Maggiori informazioni](../in-app/inapp-configuration.md)
* Sono state aggiunte nuove funzionalità di Adobe Experience Platform Assurance per acquisire eventi del dispositivo da aggiungere come regole di attivazione.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

**Campagne**

* È ora possibile duplicare una campagna dalla schermata di inventario utilizzando il menu Azioni con i tre puntini. [Maggiori informazioni](../campaigns/modify-stop-campaign.md#duplicate)
* Ora puoi eliminare le modifiche apportate alle bozze in una campagna live.
* I passaggi per attivare una campagna sono stati semplificati. [Maggiori informazioni](../campaigns/modify-stop-campaign.md)

**Gestione delle decisioni**

* Ora puoi modificare la quota limite se l’offerta è in stato **[!UICONTROL Bozza]** e non è mai stata pubblicata prima con la quota limite abilitata. [Maggiori informazioni](../offers/offer-library/add-constraints.md#frequency-capping)

**Personalizzazione**

* Ora è possibile selezionare e inserire riferimenti alle risorse direttamente dall’Editor personalizzazione quando si lavora su contenuti HTML.

### Correzioni{#may-2023-fixes}

* Messaggi in-app: è stato risolto un problema che causava un conflitto tra la pianificazione delle campagne e le impostazioni di frequenza dei messaggi.


## Note sulla versione di aprile 2023 {#apr-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: April 27, 2023-->

### Nuove funzionalità{#apr-2023-features}

<table>
<thead>
<tr>
<th><strong>Canale web (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer sta espandendo le funzionalità cross-channel aggiungendo il supporto per il canale Web. Ora puoi creare, modificare e visualizzare in anteprima le esperienze web come con qualsiasi altro canale, tramite un’interfaccia visiva intelligente e intuitiva per personalizzare l’esperienza degli utenti finali. Al momento, in Journey Optimizer puoi creare solo esperienze web nelle campagne.</p>
<img src="assets/do-not-localize/web-authoring.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../web/get-started-web.md">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Flusso di lavoro di avvio rapido per l’onboarding mobile (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile il nuovo flusso di lavoro di avvio rapido per l’onboarding mobile. Utilizza questa nuova funzione del prodotto per configurare rapidamente l’SDK Mobile e iniziare a raccogliere e convalidare i dati degli eventi mobili e a inviare notifiche push ai dispositivi mobili con Adobe Journey Optimizer. Questa funzionalità è accessibile come Beta pubblica tramite la pagina Home di raccolta dati.</p>
<img src="../push/assets/mobile-wf-home.png"/>
<p>Per ulteriori informazioni, consulta la <a href="../push/mobile-onboarding-wf.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuova dashboard Percorso (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> La dashboard Percorso è ora suddivisa in due schede:</p>
<ul><li>Utilizza la scheda <strong>Panoramica</strong> per accedere a una nuova dashboard in cui vengono visualizzate le metriche chiave relative ai percorsi.</li>
<li>Utilizza la scheda <strong>Sfoglia</strong> per accedere all’elenco di tutti i percorsi.</li></ul>
<p>Questa funzionalità è accessibile in tutti i percorsi come versione Beta pubblica.</p>
<img src="assets/do-not-localize/journey-dashboard.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-gs.md#journey-access">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#april-2023-improvements}

**Percorsi**

* L’area di lavoro del percorso ora mostra l’ID attività sulle attività di messaggistica e sui tag finali. Questo migliora la generazione di rapporti e il retargeting.
* È stato migliorato il layout del riquadro di configurazione, che ora mostra azioni, origini dati, eventi e percorsi.
* Nuovi approfondimenti sul numero di nodi nell’area di lavoro con garanzie per favorire la crescita: mantenere la facilità di lettura dei percorsi, controllo qualità e risoluzione dei problemi con un numero massimo di nodi per percorso a 50. [Ulteriori informazioni](../start/guardrails.md#journeys-guardrails-journeys)
* Quando si aggiunge un’azione [E-mail](../email/create-email.md), [SMS](../sms/create-sms.md) o [Push](../push/create-push.md) in un percorso, la superficie viene ora precompilata, per impostazione predefinita, con l’ultima superficie utilizzata per quel canale, nel percorso corrente.
* È ora possibile definire parametri di query statici o dinamici nelle azioni personalizzate. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)

**Generazione rapporti**

* È ora possibile esportare i rapporti di Journey Optimizer come PDF. [Ulteriori informazioni](../reports/global-report.md#export-reports)

**Content Designer**

* Il Content Designer di Adobe Journey Optimizer è stato aggiornato e l’accesso a stili e componenti di progettazione è ora più semplice. Questa nuova versione offre una migliore esperienza utente e include prestazioni più elevate, compatibilità parziale in modalità scura e il supporto di nuovi standard di accessibilità.



## Note sulla versione di marzo 2023 {#mar-2023}

### Nuove funzionalità{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>Canale in-app (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi inviare messaggi in-app personalizzati agli utenti dell’app all’interno di una campagna. Utilizza Journey Optimizer per progettare notifiche e personalizzare il layout, la visualizzazione, il testo e i pulsanti del messaggio per creare un’esperienza semplice.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../in-app/get-started-in-app.md">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Tracciamento dei clic SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il tracciamento dei clic SMS, puoi monitorare le prestazioni degli URL abbreviati, identificare chi vi ha fatto clic e utilizzare questi dati per effettuare il retargeting di tali clienti con le campagne successive.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../sms/create-sms.md#sms-content">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizzare i tag nei percorsi (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In qualità di utente business di Journey Optimizer, adesso puoi organizzare gli oggetti aziendali utilizzando i tag. I tag rappresentano un modo rapido e semplice di classificare gli oggetti per migliorare la ricerca. Questa funzione è attualmente in versione beta e disponibile solo nei Percorsi.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/search-filter-categorize.md#tags">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#mar-2023-improvements}

**Percorsi**

* La nuova **API di limitazione** consente di impostare un limite al numero di eventi inviati al secondo, evitando picchi di traffico eccessivi sui sistemi esterni o sulle API. Al raggiungimento del limite impostato, tutte le chiamate API successive vengono messe in coda ed elaborate il prima possibile, nell’ordine in cui sono state ricevute. Questa funzione supporta una sola configurazione di limitazione per tutte le sandbox. [Ulteriori informazioni](../configuration/external-systems.md)
* L’area di lavoro del percorso è stata ottimizzata per un’esperienza utente più semplice e migliorata. Alla fine di ogni percorso nell’area di lavoro, i segnaposto vuoti sono stati rimossi. Ora puoi semplicemente aggiungere le attività trascinandole alla fine di un percorso.
* Nell’area di lavoro del percorso, l’etichetta del tag **Fine** non viene più impostata automaticamente con il nome dell’attività precedente. Se necessario, gli utenti possono aggiungere manualmente un’etichetta personalizzata.
* Il timeout predefinito e la durata dell’errore nelle proprietà del percorso sono stati modificati da 5 a 30 secondi. [Ulteriori informazioni](../configuration/external-systems.md#timeout)
* Il tasso di limitazione predefinito nelle attività di Leggi pubblico è stato modificato da 20.000 a 5.000 messaggi al secondo. [Ulteriori informazioni](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* È stato aggiunto un guardrail alla modalità di test per ascoltare solo gli eventi inviati tramite l’interfaccia. Gli eventi inviati tramite uno strumento esterno non vengono presi in considerazione. [Ulteriori informazioni](../building-journeys/testing-the-journey.md)


<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Gestione delle decisioni**

* Per evitare potenziale confusione con il recente rilascio della funzione dei tag in Adobe Experience Platform, i tag di Gestione delle decisioni sono stati rinominati in “Qualificatori di raccolta”.

  Tieni presente che anche se il termine “tag” non viene più utilizzato nell’interfaccia utente di Gestione delle decisioni, lo è ancora nei servizi back-end come API e set di dati.

* Ora puoi reimpostare il contatore del limite di offerta su base giornaliera, settimanale o mensile. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

* Puoi anche scegliere quale evento di Adobe Experience Platform deve essere considerato come limite di offer decisioning. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

* Nella schermata di creazione dei posizionamenti sono stati aggiunti ulteriori parametri. Questi consentono di controllare se un’offerta può essere duplicata in più posizionamenti e di specificare se il contenuto e i metadati dell’offerta devono essere inclusi nella risposta API. [Ulteriori informazioni](../offers/offer-library/creating-placements.md)

**Personalizzazione**

* Ora puoi includere nell’Editor espressioni il testo di fallback predefinito per gli attributi di profilo basati su stringhe. Questi valori verranno visualizzati se gli attributi selezionati non restituiscono alcun risultato. [Ulteriori informazioni](../personalization/personalization-build-expressions.md#add)

**Generazione rapporti**

* La funzionalità dei widget di reporting è stata migliorata con la possibilità di personalizzare la visualizzazione dei dati da parte degli utenti. Con questo miglioramento, gli utenti possono ora scegliere tra più opzioni di visualizzazione, tra cui grafico, tabella e grafici ad anello.

  Per poter accedere ai widget più recenti, è necessario reimpostare le diverse dashboard di reporting. Per ulteriori informazioni sulla personalizzazione delle dashboard, consulta la [documentazione dettagliata](../reports/global-report.md#modify-dashboard).

## Note sulla versione di febbraio 2023 {#feb-2023}

### Nuove funzionalità{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Canale in-app (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi inviare messaggi in-app personalizzati agli utenti dell’app all’interno di una campagna. Utilizza Journey Optimizer per progettare notifiche e personalizzare il layout, la visualizzazione, il testo e i pulsanti del messaggio per creare un’esperienza semplice.</p>
<p><strong>Attenzione</strong>: al momento questa funzione è disponibile nella versione beta e solo per utenti beta. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../in-app/get-started-in-app.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esportare i set di dati Journey Optimizer verso destinazioni di archiviazione cloud (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile stabilire una connessione in tempo reale con le posizioni di archiviazione cloud per esportare il contenuto dei set di dati. Le destinazioni disponibili sono: archiviazione cloud Amazon S3, BLOB di Azure, Azure Data Lake Gen 2, area di destinazione dei dati, archiviazione cloud Google, SFTP.</p>
<p><strong>Attenzione</strong>: questa funzione è attualmente in versione beta ed è disponibile per tutti gli utenti di Adobe Journey Optimizer. Collabora con il tuo rappresentante Adobe per accedere alle destinazioni se non hai già accesso.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../data/export-datasets.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### Miglioramenti {#feb-2023-improvements}

**Percorsi**

* Il campo **Periodo di attesa per il rientro** è stato aggiunto alle proprietà del percorso. Questo campo ti consente di definire il tempo di attesa prima di consentire a un profilo di accedere nuovamente al percorso in percorsi unitari (a partire da un evento o da una qualificazione del pubblico). In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti. [Ulteriori informazioni](../building-journeys/journey-gs.md#entrance)

* Sono stati apportati miglioramenti per le **date di inizio e di fine percorso**. Se non hai specificato una data di inizio, ora viene aggiunta automaticamente al momento della pubblicazione. Per i percorsi **Leggi pubblico**, ora puoi aggiungere una data di fine. Questo consente ai profili di uscire automaticamente quando viene raggiunta la data. [Ulteriori informazioni](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Amministrazione**

* **Elenco Consentiti**: è ora possibile scaricare l’elenco Consentiti come file .csv. [Ulteriori informazioni](../configuration/allow-list.md#download-allowed-list)

* **Superficie e-mail**: è stato aggiunto un controllo aggiuntivo alle impostazioni dell’area e-mail. Se il record MX per il sottodominio utilizzato in **Risposta all’indirizzo (e-mail)** o **Indirizzo e-mail Ccn** non è configurato correttamente, non è più possibile creare la superficie e-mail. È necessario configurarla o utilizzarne un’altra [Ulteriori informazioni](../email/email-settings.md#reply-to-email)

* **Superficie e-mail**: nella sezione **Parametri di tracciamento URL** delle impostazioni della superficie dell’e-mail, il limite per ogni campo **Valore** è stato aggiornato da 255 caratteri a 5 KB per la compatibilità con il tracciamento di Adobe Analytics. [Ulteriori informazioni](../email/email-settings.md#url-tracking)

**Gestione delle decisioni**

* **Posizionamenti**: nella schermata di creazione dei posizionamenti sono stati aggiunti ulteriori parametri. Questi consentono di controllare se un’offerta può essere duplicata in più posizionamenti e di specificare se il contenuto e i metadati dell’offerta devono essere inclusi nella risposta API. [Ulteriori informazioni](../offers/offer-library/creating-placements.md)

* **Personalizzazione URL**: quando aggiungi URL come contenuto alle rappresentazioni delle offerte, ora puoi personalizzare tali URL utilizzando l’editor espressioni. [Ulteriori informazioni](../offers/offer-library/add-representations.md)

## Note sulla versione di gennaio 2023{#jan-2023-release}

### Nuove funzionalità{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Igiene dei dati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform offre una suite di funzionalità di igiene dei dati che ti consentono di gestire i dati archiviati tramite l’eliminazione programmatica di record e set di dati del consumatore. Questa funzionalità è ora disponibile per Adobe Journey Optimizer. </p>
<p>Puoi gestire gli archivi dati per garantire che le informazioni vengano utilizzate come previsto, che vengano aggiornate quando è necessario correggere dati non corretti e che vengano eliminate quando i criteri organizzativi lo ritengono necessario.</p>
<p><strong>Attenzione</strong>: le funzionalità di igiene dei dati sono attualmente disponibili solo per le organizzazioni che hanno acquistato le offerte aggiuntive <strong>Healthcare Shield</strong> e <strong>Privacy and Security Shield</strong>.</p><p>Per ulteriori informazioni, consulta la <a href="../privacy/data-hygiene.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modelli di contenuto e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare modelli di contenuto autonomi da sfruttare tra percorsi e campagne per riutilizzarli rapidamente.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Scopri come creare, modificare e utilizzare modelli di contenuto in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=it">questo video</a>. Per ulteriori informazioni, consulta la <a href="../email/content-templates.md">documentazione dettagliata</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#jan-2023-improvements}

**Percorsi**

* Quando si aggiunge una sezione **Qualificazione del pubblico** o **Leggi pubblico** in un percorso, lo spazio dei nomi viene ora precompilato, per impostazione predefinita, con l’ultimo spazio dei nomi utilizzato. Fai riferimento alle sezioni [Qualificazione del pubblico](../building-journeys/audience-qualification-events.md#about-segment-qualification) e [Leggi pubblico](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Nell’area di lavoro del percorso, nella barra degli strumenti è disponibile un nuovo pulsante che consente di scaricare una schermata del percorso.

**E-mail Designer**

* Ora puoi esportare il contenuto delle e-mail dal menu **Esporta HTML**. I file esportati sono disponibili in un file di archivio (.ZIP).

**Amministrazione**

* Una nuova sottosezione fornisce consigli sulla creazione dell’indirizzo **Rispondi a (e-mail)** per garantire una corretta gestione delle risposte. [Ulteriori informazioni](../email/email-settings.md#reply-to-email)

* Durante la creazione o la modifica dei **Pool IP**, i record PTR associati vengono ora visualizzati nell’elenco IP e, al passaggio del mouse, sugli indirizzi IP selezionati. [Ulteriori informazioni](../configuration/ip-pools.md#create-ip-pool)

* Dopo aver selezionato un pool IP in una superficie del canale, le informazioni del record PTR sono ora visibili quando si passa il mouse sugli indirizzi IP. [Ulteriori informazioni](../email/email-settings.md#subdomains-and-ip-pools)

* È stata aggiornata l’interfaccia utente per la modifica dei [Record PTR](../configuration/ptr-records.md#edit-ptr-record) e dei [campi esecuzione](../configuration/primary-email-addresses.md).

* È stata migliorata l’interfaccia utente per la creazione e la modifica dei sottodomini. [Ulteriori informazioni](../configuration/delegate-subdomain.md)

* La schermata Elenco di soppressione dei **Caricamenti recenti** è stata aggiornata. [Ulteriori informazioni](../configuration/manage-suppression-list.md#recent-uploads)

**Campagne**

* Una richiesta cURL di esempio che consente l’esecuzione di campagne attivate da API viene ora generata automaticamente e resa disponibile nella schermata della campagna. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md)


**Personalizzazione**

* Sono disponibili nuove funzioni assistenza: formatCurrency, charCodeAt, stringToDate, toString, formatNumber e toHexString. Inoltre, la funzione toDateTimeOnly ora accetta tipi di campi stringa, data, long e int. [Ulteriori informazioni](../personalization/functions/functions.md)
