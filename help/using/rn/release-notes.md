---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 377f75a67f3a392957cefb7b2ba9347c364c11a1
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 59%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Note sulla versione di agosto 2024 {#8-2024}

**Data di rilascio**: 20-21 agosto 2024

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

### Nuove funzionalità {#8-features}

Questa versione include le nuove funzionalità elencate di seguito.

<!--table>
<thead>
<tr>
<th><strong>Guided Channel Setup</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Guided Channel Setup enables you to automate and validate channel setup in a unified experience, speeding up the process of getting started with Journey Optimizer. This new guided setup streamlines rapid channel configuration, ensuring all necessary resources are readily installed and working within Experience Platform, Journey Optimizer, and Data Collection. This enables marketing, product and data engineering teams to quickly begin with campaign and journey creation.</p>
<p>For more information, refer to the <a href="../configuration/set-mobile-config.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/guided-setup.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Configurazioni dei canali migliorate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le funzionalità della superficie di canale corrente sono state migliorate per un approccio coerente su tutti i canali. Ora puoi definire, gestire e riutilizzare queste configurazioni per qualsiasi canale, incluso Web, messaggistica in-app o esperienza basata su codice.</p>
<p><ul>
<li>Le superfici di canale ora sono state rinominate in <strong>Configurazioni di canale</strong></li>
<li>Puoi allegare una o più azioni di marketing per applicare il consenso e i criteri di governance dei dati</li>
<li>Il controllo dell’accesso a livello di oggetto (OLAC) è ora disponibile per ogni configurazione di canale, consentendo di decidere quali utenti possono creare o utilizzare configurazioni specifiche</li>
<li>Per alcuni canali, è possibile creare configurazioni di canale in grado di eseguire il targeting per più piattaforme. Ad esempio, potrebbe trattarsi di una configurazione di canale di messaggistica in-app in grado di eseguire il targeting per una pagina web, un’app iOS e un’app Android.</li>
</ul></p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/channel-surfaces.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Azione personalizzata Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi integrare Adobe Journey Optimizer con Adobe Marketo Engage per creare i tuoi casi d’uso B2B. Una nuova azione personalizzata da un percorso consente di acquisire dati in Marketo.</p>
<p>Per ulteriori informazioni, consulta la <a href="../action/marketo-engage.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variabili nei frammenti di contenuto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le variabili globali dei frammenti migliorano la funzionalità dei frammenti esistenti per migliorare l’efficienza in termini di riutilizzabilità dei contenuti e casi di utilizzo di script. I frammenti possono ora utilizzare variabili di input e creare variabili di output utilizzabili nel contenuto di campagne e percorsi. I frammenti possono utilizzare variabili di input, sia nei <a href="../personalization/use-expression-fragments.md">frammenti di espressione</a> che nei <a href="../email/use-visual-fragments.md">frammenti visivi</a>. Puoi utilizzare queste variabili per personalizzare il contenuto e i parametri dei messaggi nelle campagne e nei percorsi.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/use-expression-fragments.md">documentazione dettagliata</a>.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Flusso di lavoro di preparazione IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Data di disponibilità: 13 agosto</p>
<p>Se invii un’e-mail con un nuovo indirizzo IP, ora puoi eseguire facilmente i flussi di lavoro di preparazione IP direttamente dall’interfaccia utente. Adobe Journey Optimizer offre un modo standardizzato ed efficiente di preparare gli indirizzi IP seguendo le best practice per una recapitabilità ottimale.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/ip-warmup-gs.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#8-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Percorsi**

* Nell&#39;attività **Condizione**, per impostazione predefinita, la **[!UICONTROL Condizione temporale]** è ora impostata per ora, dalle 00:00 alle 12:00. [Ulteriori informazioni](../building-journeys/condition-activity.md#time_condition)
* Durante la creazione dei percorsi, gli avvisi vengono ora visualizzati dal pulsante **Avvisi**, per allinearli ad altri avvisi e fornire un&#39;esperienza utente coerente. [Ulteriori informazioni](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Sono state migliorate le opzioni di zoom nella barra degli strumenti del percorso: la percentuale di zoom è ora visibile ed è ora possibile reimpostare più facilmente il valore di zoom.

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)-->

**Canale push**

* Ora puoi aggiungere le credenziali push dell’app mobile nelle impostazioni di configurazione del canale Adobe Journey Optimizer. Non è più necessario creare una superficie app nella raccolta dati di Adobe Experience Platform.

### Altre modifiche {#changes}

**Reporting**

* L’esperienza di reporting corrente verrà ritirata a partire dalla versione di ottobre. Dopo questa data, la nuova esperienza di reporting diventerà lo standard. Consigliamo di acquisire familiarità con le nuove funzioni e funzionalità per garantire una transizione senza problemi.

[Introduzione alla nuova interfaccia di reporting di Journey Optimizer](../reports/report-gs-cja.md)

* Sono stati aggiunti nuovi casi d’uso alla nuova esperienza di reporting:

   * Crea metriche calcolate personalizzate direttamente all’interno dei rapporti.
   * Crea un pubblico dai dati di reporting.
   * Utilizza lo strumento di analisi esplorativa per creare facilmente tabelle e visualizzazioni dai **[!UICONTROL Dimension]** e dalle **[!UICONTROL metriche]** selezionati.

  Per ulteriori informazioni, consulta la [documentazione dettagliata](../reports/report-cja-manage.md).
