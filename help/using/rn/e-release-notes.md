---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: ht
source-wordcount: '634'
ht-degree: 100%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di settembre 2023 {#sept-rn-2023}

**Data di rilascio**: 26-27 settembre 2023

### Nuove funzionalità{#sept-2023-features}

Questa versione include le nuove funzionalità elencate di seguito.


<table>
<thead>
<tr>
<th><strong>Rapporti consolidati sui canali</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione Rapporto dei canali offre ad analisti ed esperti di marketing una panoramica completa delle metriche di traffico e coinvolgimento a livello di canale. Per accedere al menu Rapporto, è necessario disporre dell’autorizzazione Vsualizza i rapporti sui canali.</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Destinazioni di esportazione dei set di dati (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’esportazione dei set di dati di Journey Optimizer nelle destinazioni di archiviazione cloud è ora disponibile a livello generale. Ora, per esportare il contenuto dei set di dati, è possibile stabilire una connessione in tempo reale con posizioni di archiviazione cloud.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Archiviazione per sandbox delle credenziali per app mobili</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa nuova funzione consente di gestire e associare facilmente le credenziali push a una sandbox dedicata in Superfici app.</p>
<p>Per ulteriori informazioni, consulta la <a href="../in-app/inapp-configuration.md">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attributi calcolati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gli attributi calcolati consentono di riepilogare facilmente i dati evento negli attributi del profilo tramite un’interfaccia intuitiva e migliorano la segmentazione, la personalizzazione e l’attivazione basate sul comportamento. Con questa funzione, puoi creare attributi calcolati in autonomia, gestirli e utilizzarli nella segmentazione, nelle destinazioni del profilo cliente in tempo reale o in Journey Optimizer.<br/><br/>
Inoltre, gli attributi calcolati semplificano i flussi di lavoro per percorsi e segmentazione per aiutarti a fornire esperienze rilevanti in modo semplice e diretto. Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=it">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/computed-attributes.gif">
</tr>
</tbody>
</table>


### Miglioramenti {#sept-2023-improvements}

Questa versione include i miglioramenti elencati di seguito.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**Personalizzazione**

* Oltre ai frammenti visivi, ora è possibile creare, salvare e riutilizzare frammenti di espressione dall’interfaccia di Journey Optimizer tramite l’editor di espressioni. I frammenti di espressione sostituiscono le espressioni salvate in precedenza.

**Avvisi**

* È stato introdotto un nuovo tipo di avviso di sistema. Ora puoi ricevere una notifica quando un’attività Leggi pubblico non viene completata.

**Canale Web**

* Le applicazioni a pagina singola (SPA) possono ora essere create nell’editor visivo del designer web, che consente di selezionare le viste specifiche a cui applicare le modifiche alla pagina web. Una vista può essere definita come un intero sito o un gruppo di elementi visivi su un sito, ad esempio la pagina Home, l’intero sito dei prodotti o il frame delle preferenze di consegna su tutte le pagine di pagamento. Per creare ed eseguire campagne web di Adobe Journey Optimizer sulle SPA, è necessaria una singola configurazione per sviluppatori per definire le viste nell’implementazione di Adobe Experience Platform Web SDK.

* Quando modifichi una pagina utilizzando il designer web, ora puoi aggiungere nuove modifiche al contenuto direttamente dal riquadro **Modifiche**, senza dover selezionare un componente e modificarlo dall’interfaccia del designer.
* Durante la configurazione dei sottodomini web, ora puoi aggiungere un tuo sottodominio, oltre a utilizzare un sottodominio già delegato ad Adobe.

**Percorsi**

* Il supporto delle risposte alle azioni personalizzate è ora disponibile al pubblico. Ciò consente di sfruttare le risposte alle chiamate API nelle azioni personalizzate e orchestrare il percorso in base a tali risposte. Inoltre, è stato aggiunto un nuovo guardrail per limitare tutte le azioni personalizzate a 5000 chiamate per endpoint.
* Durante la duplicazione di un percorso, è ora possibile definire il nome della copia del percorso.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**Canale e-mail**

Una nuova opzione nella configurazione della superficie e-mail consente di scegliere di inviare messaggi transazionali ai profili anche se i loro indirizzi e-mail si trovano nell’elenco di soppressione di Adobe Journey Optimizer.

**Canale SMS**

Due nuovi campi, **Messaggio di consenso** e **Messaggio di aiuto**, sono stati aggiunti alla schermata di configurazione API, per consentire agli utenti di personalizzare le risposte in base alle parole chiave in entrata. Tieni presente che questo è disponibile solo per il provider SMS Sinch.

**Reporting**

Ora è possibile esportare i rapporti di Journey Optimizer come file CSV. [Ulteriori informazioni](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->
