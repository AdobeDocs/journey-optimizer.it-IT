---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d5ddf00b1a39c66b29ffb967389fb069a9648e83
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 52%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.


## Note sulla versione di aprile 2025 {#25-4-rn}


**Data di rilascio**: 29-30 aprile 2025


### Nuove funzionalità {#25-04-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Integrazione di Adobe Express (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora si integra con Adobe Express, consentendo di collegare facilmente le risorse creative con l’orchestrazione del percorso. Questa integrazione semplifica il processo di progettazione e distribuzione di contenuti personalizzati nelle campagne. </p>
<p>Questa funzione è attualmente disponibile in modo limitato.</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>Per ulteriori informazioni, consulta la <a href="../integrations/express.md">documentazione dettagliata</a>.</p>
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
<th><strong>Integrazione di Adobe Experience Manager as a Cloud Service (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponibilità generale dell’integrazione tra Adobe Journey Optimizer e Adobe Experience Manager as a Cloud Service. Questa integrazione consente l’origine e la gestione dei contenuti per percorsi di clienti personalizzati.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Editor Personalization - Come imparare facendo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile un ambiente playground di personalizzazione, in cui puoi sperimentare espressioni di personalizzazione. Consente di esplorare modelli e payload di esempio per iniziare e provare le espressioni di personalizzazione.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/personalize.md#playground">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 24 aprile 2025</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Attiva percorso giornaliero eseguito dopo il completamento della segmentazione batch (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Per i percorsi pianificati quotidianamente, una nuova opzione consente di definire un intervallo di tempo massimo di 6 ore per l’attesa dei dati del pubblico dai processi di segmentazione batch, in modo che i percorsi vengano eseguiti con i dati più aggiornati o vengano ignorati se non sono pronti. L’opzione Attiva dopo la valutazione del pubblico in batch è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/read-audience.md#schedule">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

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
<th><strong>Punteggio di allineamento del brand (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione di punteggio di allineamento del brand offre un feedback chiaro direttamente nella finestra di e-mail designer, consentendoti di vedere se il contenuto è allineato al tono, allo stile e alle linee guida del brand.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/brands-score.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Line channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->

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
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/success-metrics.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 aprile 2025</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New ranking formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.  </p>
</td>
</tr>
</tbody>
</table>
-->

### Miglioramenti {#25-04-improv}

**Canale e-mail**

<!--* **Personalized URL tracking**

  For increased flexibility and control over your email settings, you can now personalize all your URL tracking parameters at once at the email channel configuration level, instead of doing it in the Email designer for each link in your content. -->

* **E-mail designer** - Data di disponibilità: 1 aprile 2025

  Per migliorare l’accessibilità in Journey Optimizer, sono ora disponibili due nuovi campi nell’E-mail designer: corrispondono all’elemento `<title>` e all’attributo `lang` nell’elemento `<html>` del contenuto dell’e-mail. Puoi definire queste impostazioni oltre che nel campo **[!UICONTROL Preintestazione]**, nella sezione **[!UICONTROL Corpo]** dell’e-mail. [Ulteriori informazioni](../email/email-metadata.md)

<!--- **Email designer themes** (Beta) - Availability date: May 5, 2025

  You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams. -->

**Strumenti Sandbox**

<!--- **Decisioning sandbox copy**

  Decisioning objects can now be copied between sandboxes, streamlining testing and deployment workflows.-->

* **Strumenti sandbox per azioni personalizzate**

  Le azioni personalizzate sono ora incluse nell’elenco degli oggetti Adobe Journey Optimizer che possono essere copiati utilizzando la funzione strumenti sandbox, semplificando il test e la distribuzione. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md)

* **Strumenti sandbox per campagne** - Data di disponibilità: 3 aprile 2025

  Ora puoi copiare campagne in più sandbox utilizzando le funzionalità di esportazione e importazione dei pacchetti. Le campagne vengono copiate insieme a tutti gli elementi relativi al profilo, al pubblico, allo schema, ai messaggi in linea e agli oggetti dipendenti. Alcuni elementi non vengono copiati, ad esempio elementi decisionali, etichette di utilizzo dei dati e impostazioni della lingua. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#custom-actions)

**Personalizzazione**

<!--- **Pills activation**  

  A new "Pills" button has been to the personalization editor. When enabled, profile and contextual attributes display as pills, enhancing the readability of your code.-->

* **Attributi compilati nel riquadro degli attributi** - Data di disponibilità: 2 aprile 2025

  Il riquadro degli attributi nell’editor di personalizzazione ora mostra solo gli attributi compilati per impostazione predefinita. Per visualizzare tutti gli attributi, utilizza il pulsante Impostazioni per disattivare l’opzione **[!UICONTROL Mostra solo attributi compilati]**. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)


* **Nuovo attributo contestuale**

  È ora disponibile un nuovo attributo contestuale, **ID profilo messaggio**, da selezionare dall&#39;editor di personalizzazione. Si tratta di un attributo orientato ai messaggi che identifica in modo univoco ogni messaggio inviato a ciascun profilo target in una consegna. Questo identificatore univoco può essere utilizzato, ad esempio, come parametro di tracciamento URL per distinguere ogni collegamento aperto o cliccato dai destinatari.

**Navigazione**

* **Gestione dei contenuti** - Data di disponibilità: 2 aprile 2025

  Per gestire facilmente i frammenti e i modelli di contenuto, ora puoi utilizzare le cartelle per organizzarli in modo più efficace in una gerarchia strutturata. Ulteriori informazioni sono disponibili nelle sezioni [Modelli di contenuto](../content-management/access-content-templates.md#folders) e [Frammenti](../content-management/manage-fragments.md#folders).

  >[!AVAILABILITY]
  >
  >Questo miglioramento è disponibile solo per alcune organizzazioni (disponibilità limitata).

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.

- **Folders for landing pages** - Availability date: May 5, 2025

  To easily manage your landing pages, you can now also use folders to organize them more effectively into a streamlined hierarchy.  -->

<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->




