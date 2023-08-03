---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: ht
source-wordcount: '638'
ht-degree: 100%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di luglio 2023 {#july-rn-2023}

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
<p>Per ulteriori informazioni, consulta la <a href="../audience/get-started-audience-orchestration.md">documentazione dettagliata</a>.</p>
<p>La composizione del pubblico è completamente integrata con il nuovo menu "Tipi di pubblico" di Adobe Experience Platform, che funge da portale centralizzato per i tipi di pubblico. Ora puoi utilizzare una pagina Sfoglia che include una nuova dashboard con tendenze di segmenti e sovrapposizioni, per trovare nuove informazioni ed esplorare gli strumenti organizzativi per cartelle e tag. In questa esperienza sono incorporati controlli di governance per l’etichettatura standardizzata del pubblico e funzionalità di gestione del ciclo di vita del pubblico, al fine di gestire i flussi di lavoro di attivazione. Con questa nuova esperienza di gestione, ora puoi gestire in modo semplice e sicuro i tipi di pubblico da un’unica posizione. Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it" target="_blank">documentazione di Adobe Experience Platform</a>.</p></p>
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
<img src="assets/do-not-localize/gif-dm.gif"/>
<p>For more information, refer to the <a href="../direct-mail/create-direct-mail.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Convertire il contenuto HTML per E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi importare e convertire qualsiasi contenuto HTML nell’editor e-mail di Journey Optimizer. I blocchi di contenuto vengono identificati automaticamente e sono disponibili in E-mail designer: utilizza le sue potenti funzionalità di progettazione per aggiornarli e personalizzarli.</p>
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
<p>Oltre a campagne e percorsi, ora puoi assegnare i tag unificati di Adobe Experience Platform a pagine di destinazione, modelli di contenuto, frammenti ed elenchi di iscrizione. Questo ne agevola la classificazione e migliora la ricerca e la navigazione in tutti gli elenchi. </p>
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
<p>Ora puoi creare e gestire modelli di contenuto Adobe Journey Optimizer utilizzando API dedicate, fornendo un’integrazione diretta con il sistema di contenuti esistente.</p>
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#july-2023-improvements}

Questa versione include i miglioramenti elencati di seguito.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* È stato introdotto un nuovo tipo di avviso di sistema. Ora puoi ricevere una notifica quando un’azione personalizzata non viene completata.
-->

**Campagne**

* Gli eventi contestuali relativi alle campagne sono ora disponibili all’uso nel menu “Attributi contestuali” dell’editor di personalizzazione.


**Tipi di pubblico**

Sono stati apportati miglioramenti al selettore del pubblico in percorsi o campagne, con l’aggiunta di nuove colonne che mostrano l’origine e la frequenza di aggiornamento dei tipi di pubblico.

Con il rilascio del portale di composizione del pubblico, nel sistema e nella documentazione di Adobe Experience Platform e Adobe Journey Optimizer è stato aggiornato l’utilizzo di “pubblico” e “segmenti”.

* Pubblico: un set di persone, account, famiglie o altre entità che hanno in comune caratteristiche e/o comportamenti specifici.
* Definizione di segmento: in Adobe Experience Platform, le regole utilizzate per descrivere le caratteristiche o il comportamento chiave di un pubblico di destinazione. Questo termine era precedentemente noto semplicemente come “segmento”.

Di conseguenza, in Adobe Journey Optimizer e nell’interfaccia utente di Adobe Experience Platform, vedrai che “Segmenti” è stato sostituito da “Tipi di pubblico” per riflettere questo nuovo percorso di creazione e gestione del pubblico.

**API**

Autenticazione nelle API di Adobe Journey Optimizer: il metodo JWT per generare token di accesso è stato dichiarato obsoleto. Tutte le nuove integrazioni devono essere create utilizzando il metodo di autenticazione server-to-server OAuth. Adobe consiglia inoltre di migrare le integrazioni esistenti al metodo OAuth. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)


**Altre modifiche**

L’esportazione di set di dati Journey Optimizer in destinazioni di archiviazione cloud è ora disponibile per tutti i clienti come Beta pubblica. Ora, per esportare il contenuto dei set di dati, è possibile stabilire una connessione in tempo reale con posizioni di archiviazione cloud. [Ulteriori informazioni](../data/export-datasets.md)




