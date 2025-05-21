---
solution: Journey Optimizer
product: journey optimizer
title: Note sulle versioni 2025
description: Note sulle versioni 2025 di Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 92%

---

# Note sulle versioni 2025 {#release-notes-2025}

In questa pagina sono elencate tutte le funzioni e i miglioramenti di [!DNL Journey Optimizer] rilasciati nel 2025.


## Note sulla versione di aprile 2025 {#25-4-rn}

**Data di rilascio**: 29-30 aprile 2025

### Nuove funzionalità {#25-04-features}

Di seguito sono elencate le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Editor di personalizzazione - Impara con la pratica</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile un playground di personalizzazione, in cui puoi sperimentare le espressioni di personalizzazione. Consente di esplorare modelli e payload di esempio per aiutarti a iniziare e provare le espressioni di personalizzazione.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/personalize.md#playground">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 aprile 2025</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Canale LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ha ampliato le sue funzionalità cross-channel per includere il supporto per il canale LINE. Questo miglioramento consente di creare, modificare e visualizzare in anteprima le esperienze LINE, permettendo interazioni più personalizzate e coinvolgenti. Con LINE, puoi connetterti con più clientela, inviare contenuti rilevanti e migliorare il coinvolgimento.</p>
<p>Il canale LINE è abilitato per i clienti Adobe Journey Optimizer su richiesta. Contatta l’Assistenza clienti di Adobe o il tuo rappresentante Adobe per attivare la funzione per la tua organizzazione.</p>
<p>Per ulteriori informazioni, consulta la <a href="../line/get-started-line.md">documentazione dettagliata</a>.</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Metriche di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le metriche di percorso sono ora disponibili e consentono di misurare l’impatto delle attività sulle metriche più importanti per l’azienda e di fornire informazioni più chiare sulle prestazioni.</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/success-metrics.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 aprile 2025</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Integrazione di Adobe Express (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora è integrato con Adobe Express, consentendo di collegare facilmente le risorse creative con l’orchestrazione del percorso. Questa integrazione semplifica il processo di progettazione e distribuzione di contenuti personalizzati nelle campagne. </p>
<p>Questa integrazione non è attualmente disponibile per l’utilizzo con Healthcare Shield o Privacy and Security Shield.</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>Per ulteriori informazioni, consulta la <a href="../integrations/express.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>L’attivazione giornaliera del percorso viene eseguita dopo il completamento della segmentazione batch (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Per i percorsi pianificati quotidianamente, una nuova opzione consente di definire un intervallo di tempo massimo di 6 ore per l’attesa dei dati del pubblico dai processi di segmentazione batch, in modo che i percorsi vengano eseguiti con i dati più aggiornati o vengano ignorati se non sono pronti. L’opzione Attiva dopo la valutazione del pubblico batch è disponibile solo per alcune organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/read-audience.md#schedule">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Punteggio di allineamento al brand (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione di punteggio di allineamento del brand offre un feedback chiaro direttamente nell’E-mail designer, consentendoti di visualizzare se il contenuto è allineato al tono, allo stile e alle linee guida del brand. Questa funzione è disponibile in versione Beta.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/brands-score.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### Miglioramenti {#25-04-improv}

**API anteprima campagne**

Sono disponibili nuove API per l’anteprima delle campagne, oltre alle funzionalità di invio di bozze esistenti. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}.

**Strumenti sandbox**

* **Strumenti sandbox per azioni personalizzate**

  Le azioni personalizzate sono ora incluse nell’elenco degli oggetti Adobe Journey Optimizer che possono essere copiati utilizzando la funzione strumenti sandbox, semplificando il test e la distribuzione. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md)

* **Strumenti sandbox per le campagne** - Data di disponibilità: 3 aprile 2025

  Ora puoi copiare campagne in più sandbox utilizzando le funzionalità di esportazione e importazione dei pacchetti. Le campagne vengono copiate insieme a tutti gli elementi relativi al profilo, al pubblico, allo schema, ai messaggi in linea e agli oggetti dipendenti. Alcuni elementi non vengono copiati, ad esempio elementi decisionali, etichette di utilizzo dei dati e impostazioni della lingua. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#custom-actions)

**Personalizzazione**

* **Nuovo attributo contestuale**

  È ora disponibile un nuovo attributo contestuale, **ID profilo messaggio** per la selezione dall’editor di personalizzazione. Si tratta di un attributo orientato ai messaggi che identifica in modo univoco ogni messaggio inviato a ciascun profilo target in una consegna. Questo identificatore univoco può essere utilizzato, ad esempio, come parametro di tracciamento URL per distinguere ogni collegamento aperto o cliccato dai destinatari.

* **Attributi compilati nel riquadro degli attributi** - Data di disponibilità: 2 aprile 2025

  Il riquadro degli attributi nell’editor di personalizzazione ora mostra solo gli attributi compilati per impostazione predefinita. Per visualizzare tutti gli attributi, utilizza il pulsante Impostazioni per disattivare l’opzione **[!UICONTROL Mostra solo attributi compilati]**. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

**Canale e-mail**

* **Tracciamento URL personalizzato** - Data di disponibilità: 30 aprile 2025

  Per una maggiore flessibilità e un maggiore controllo sulle impostazioni e-mail, ora puoi personalizzare tutti i parametri di tracciamento URL contemporaneamente a livello di configurazione del canale e-mail, invece di farlo nella finestra di progettazione e-mail per ogni collegamento nel contenuto. [Ulteriori informazioni](../email/surface-personalization.md#personalize-url-tracking)

* **E-mail designer** - Data di disponibilità: 1 aprile 2025

  Per migliorare l’accessibilità in Journey Optimizer, sono ora disponibili due nuovi campi nell’E-mail designer: corrispondono all’elemento `<title>` e all’attributo `lang` nell’elemento `<html>` del contenuto dell’e-mail. Puoi definire queste impostazioni oltre che nel campo **[!UICONTROL Preintestazione]**, nella sezione **[!UICONTROL Corpo]** dell’e-mail. [Ulteriori informazioni](../email/email-metadata.md)

**Playbook casi d&#39;uso**

* **Creazione e condivisione di playbook (versione beta privata)** - È ora possibile creare, gestire e condividere playbook personalizzati per casi d&#39;uso. Questa funzionalità è attualmente disponibile solo per un set di organizzazioni come versione beta privata. Per ottenere l’accesso, contatta il tuo rappresentante Adobe. [Ulteriori informazioni](../start/playbooks.md)

**Navigazione**

* **Gestione dei contenuti** - Data di disponibilità: 2 aprile 2025

  Per gestire facilmente i frammenti e i modelli di contenuto, ora puoi utilizzare le cartelle per organizzarli in modo più efficace in una gerarchia strutturata. Ulteriori informazioni sono disponibili nelle sezioni [Modelli di contenuto](../content-management/access-content-templates.md#folders) e [Frammenti](../content-management/manage-fragments.md#folders).

  >[!AVAILABILITY]
  >
  >Questo miglioramento è disponibile solo per alcune organizzazioni (disponibilità limitata).

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->



## Note sulla versione di marzo 2025 {#25-3-rn}

### Nuove funzionalità {#25-03-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Integrazione con Dynamic Media (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le risorse Dynamic Media sono ora direttamente disponibili e accessibili in Journey Optimizer. Questa integrazione consente di:
<ul>
<li>Gestire in maniera centralizzata le risorse con aggiornamenti in tempo reale</li>
<li>Modificare istantaneamente le impostazioni delle risorse, ad esempio larghezza e altezza</li>
<li>Personalizzare i modelli Dynamic Media aggiornando i contenuti e aggiungendo campi di personalizzazione</li>
</ul>
<p>
<p>Questa integrazione è disponibile solo per alcune organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/aem-dynamic.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Integrazione con Adobe GenStudio (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Per migliorare l’efficienza del marketing e mantenere la coerenza del brand, ora puoi integrare facilmente le esperienze GenStudio for Performance Marketing con Journey Optimizer. Questo consente di sfruttare la creazione del contenuto basata sull’intelligenza artificiale di GenStudio insieme alle funzionalità avanzate di orchestrazione di Journey Optimizer.<p>
<p>L’utilizzo dell’integrazione GenStudio in Journey Optimizer non è attualmente disponibile con Healthcare Shield o Privacy and Security Shield (disponibilità limitata).</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/genstudio.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Valutazione flessibile del pubblico (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente disponibile per alcune organizzazioni (disponibilità limitata, LA), la valutazione flessibile del pubblico è ora disponibile per tutti gli utenti (disponibilità generale, GA). Questa funzione consente di eseguire un processo di segmentazione su richiesta per i tipi di pubblico selezionati, per disporre sempre dei dati del pubblico più aggiornati prima di eseguirne il targeting in percorsi e campagne Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Per ulteriori informazioni, consulta la <a href="../audience/creating-a-segment-definition.md#flexible">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### Miglioramenti {#25-03-improv}

**Editor di personalizzazione** (data di disponibilità: 12 marzo)

L’editor di personalizzazione di Journey Optimizer è stato aggiornato con nuove funzionalità:
* **Progettazione dell’editor di codice aggiornata**: un’interfaccia più pulita e moderna per migliorare l’usabilità e la concentrazione.
* **Cerca e sostituisci**: una funzionalità aggiunta per trovare e sostituire rapidamente i contenuti all’interno dell’editor.
* **Supporto Annulla e Ripristina**: consente di ripristinare o riapplicare facilmente le modifiche.
* **Dimensione del font personalizzabile** : consente di regolare la dimensione del font dell’editor per una migliore leggibilità.
* **Convalida JSON in linea**: fornisce la convalida lato client in tempo reale per il contenuto JSON per accelerare il rilevamento degli errori.
* **Completamento automatico per attributi di profilo e di contesto**: offre suggerimenti avanzati per semplificare la creazione di contenuti.
* **Evidenziazione della sintassi migliorata**: migliora la leggibilità rendendo la struttura del codice visivamente più distinta.

![Video che mostra la nuova funzione nell’editor di personalizzazione](assets/do-not-localize/personalization-editor.gif)

Per ulteriori informazioni, consulta la [documentazione dettagliata](../personalization/personalization-build-expressions.md).

**Approvazioni**

Quando si definiscono le condizioni per un criterio di approvazione, ora è possibile filtrare in base a Tag e/o Categoria oggetto.

Per ulteriori informazioni, consulta la [documentazione dettagliata](../test-approve/approval-policies.md).

**Configurazione**

* Ora è possibile assegnare tag unificati Adobe Experience Platform alle configurazioni del canale. Questo ti consente di classificarli facilmente e di migliorare la ricerca e la navigazione in tutti gli elenchi. [Ulteriori informazioni](../configuration/channel-surfaces.md#channel-config-tags)

* Quando imposti o modifichi un sottodominio e-mail in Journey Optimizer, ora puoi scegliere di gestire autonomamente il record DMARC associato, se disponibile sul dominio principale. [Ulteriori informazioni](../configuration/dmarc-record.md#set-up-dmarc)

**Regole di business**

Ora è possibile utilizzare una quota limite giornaliera in percorsi e campagne con segmentazione in batch. Per garantire la precisione delle regole di quota limite giornaliera, assicurati di scegliere lo spazio dei nomi con la priorità più elevata durante la creazione di una campagna o di un percorso. Ulteriori informazioni sulla priorità dello spazio dei nomi sono disponibili nella [guida di Platform Identity Service](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

Come promemoria, la quota limite giornaliera nei set di regole è disponibile solo per alcune organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

Per ulteriori informazioni sulle regole di business, consulta la [documentazione dettagliata](../conflict-prioritization/rule-sets.md).

**Modelli di contenuto**

I modelli di contenuto di tipo HTML ora sono obsoleti. È comunque possibile utilizzare i modelli di contenuto HTML esistenti creati in precedenza in [!DNL Journey Optimizer]. [Ulteriori informazioni sui modelli di contenuto](../content-management/content-templates.md)


<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->




## Note sulla versione di febbraio 2025 {#25-02-rn}

**Data di rilascio**: 18-19 febbraio 2025


### Nuove funzionalità {#25-02-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Creare e gestire le regole di business</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare regole di business utilizzando i set di regole. I set di regole sono gruppi di regole che ti aiutano a limitare i messaggi inviati all’interno di campagne e azioni di un percorso per i diversi canali e a controllare l’ingresso dei profili nei percorsi.<p>
<p><ul><li>Crea set di regole di canale per limitare il numero di messaggi inviati su uno o più canali. Applicali alle campagne o alle azioni dei percorsi per applicare le regole definite nel set di regole. Il set di regole del canale consente di applicare regole di limitazione in base ai tipi di comunicazione. Ad esempio, puoi impostare un set di regole per limitare i “messaggi promozionali” e un altro per le “newsletter”. Applica il set di regole appropriato alla campagna o all’azione di un percorso in base al tipo di comunicazione da inviare.</li>
<li> Crea set di regole per i percorsi, per controllare l’ingresso dei profili nei percorsi. Limita la frequenza con cui un profilo può effettuare l’ingresso in un percorso in un determinato periodo o il numero di percorsi in cui può essere registrato simultaneamente. Applicali a livello di percorso per garantire una corretta gestione degli ingressi.</li></ul></p>
<p>Precedentemente disponibili per alcune organizzazioni (LA), le regole di business ora sono disponibili per tutti gli utenti (GA). Le regole di business del dominio di percorso continuano a essere disponibili solo per alcune organizzazioni limitate (LA).</p>
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/rule-sets.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generare pagine di destinazione con l’Assistente IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile creare contenuti coinvolgenti per le pagine di destinazione, compresi progettazioni di pagine intere, testo e immagini personalizzati, con l’aiuto dell’Assistente IA.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Per ulteriori informazioni, consulta la <a href="../content-management/generative-lp.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Brand con l’Assistente IA (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare i tuoi brand per definirne l’identità visiva e verbale. </p>
<p>Questa funzionalità viene rilasciata come versione beta privata a un set limitato di clienti. Sarà disponibile progressivamente per tutta la clientela nelle prossime versioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/brands.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Risolvere i problemi relativi alle azioni personalizzate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi convalidare una configurazione di azione personalizzata effettuando chiamate API reali direttamente da Adobe Journey Optimizer. Questa nuova funzionalità consente di risolvere i problemi relativi alle azioni personalizzate prima o dopo l’utilizzo in un percorso. </p>
<p>Per ulteriori informazioni, consulta la <a href="../action/troubleshoot-custom-action.md">documentazione dettagliata</a>.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Valutazione flessibile del pubblico (LA, disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La valutazione flessibile del pubblico consente di eseguire un processo di segmentazione su richiesta per i tipi di pubblico selezionati, per disporre sempre dei dati del pubblico più aggiornati prima di eseguirne il targeting in percorsi e campagne Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Per ulteriori informazioni, consulta la <a href="../audience/creating-a-segment-definition.md#flexible">documentazione dettagliata</a>.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<p>Data di disponibilità: 28 gennaio 2025</p>
</tr>
</tbody>
</table>
</table>


### Miglioramenti {#25-02-improvements}

I miglioramenti riportati di seguito sono inclusi nell’aggiornamento di febbraio.

* **Impostazione time-to-live (TTL) del set di dati**: a partire da questo mese, verrà introdotto un guardrail time-to-live (TTL) nei set di dati di Journey Optimizer generati dal sistema in nuove sandbox e nuove organizzazioni come segue:

   * 90 giorni per i dati nell’archivio dei profili
   * 13 mesi per i dati nel data lake

  In una fase successiva, questa modifica verrà implementata nelle sandbox della clientela esistente.

  Ulteriori informazioni su questo aggiornamento sono disponibili nelle [Domande frequenti dedicate](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Direct mail**: un nuovo tipo di server, Data Landing Zone, è ora supportato per il routing dei file nella configurazione del canale direct mail. [Ulteriori informazioni](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS**: è ora possibile gestire la consegna di messaggi SMS da endpoint multiregionali sovrascrivendo gli URL di consegna, feedback, in entrata e callback. Per supportare questa funzione, è stato aggiunto il nuovo campo URL di sostituzione alla configurazione delle credenziali API. Questa modifica è disponibile solo con il provider Sinch. [Ulteriori informazioni](../sms/sms-configuration-sinch.md)

* **Personalizzazione** (data di disponibilità: 29 gennaio 2025): nuove funzioni helper data/ora sono disponibili per l’utilizzo nell’editor di personalizzazione. [Ulteriori informazioni](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configurazione e-mail**: se gestisci il consenso al di fuori di Adobe, ora puoi impostare un indirizzo e-mail personalizzato per l’annullamento dell’iscrizione e un URL personalizzato per l’annullamento dell’iscrizione con un solo clic, come parte delle impostazioni di configurazione del canale e-mail.[Ulteriori informazioni](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Decisioni** (data di disponibilità: 28 gennaio 2025): la funzione Decisioni ora supporta i tipi di dati Oggetto durante la modifica dello schema del catalogo elementi. [Ulteriori informazioni](../experience-decisioning/catalogs.md)
