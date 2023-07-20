---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: b677776becaabc15c85be0a5a46b741cebb9d87b
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 25%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Tutte le modifiche sono consolidate l&#39;ultima settimana di ogni mese nel [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità del rilascio. I collegamenti, le schermate e la documentazione aggiornata sono pubblicati nella [note sulla versione](release-notes.md), alla data di rilascio.


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
<p>Ora puoi creare flussi di lavoro di composizione per combinare i tipi di pubblico di Adobe Experience Platform esistenti in un’area di lavoro visiva e sfruttare varie attività (suddivisione, arricchimento...) per creare nuovi tipi di pubblico. I tipi di pubblico appena creati vengono salvati nuovamente in Adobe Experience Platform insieme ai tipi di pubblico esistenti e possono essere utilizzati nelle campagne Journey Optimizer per il targeting dei clienti.</p>
<img src="../audience/assets/audiences-publish.png"/>
<p>Per ulteriori informazioni, consulta la <a href="../audience/get-started-audience-orchestration.md">documentazione dettagliata</a>.</p>
<p>La composizione del pubblico è completamente integrata con il nuovo menu "Tipi di pubblico" di Adobe Experience Platform, che funge da portale centralizzato per i tipi di pubblico. Ora puoi utilizzare una pagina Sfoglia che include una nuova dashboard con tendenze dei segmenti e sovrapposizioni per trovare nuove informazioni ed esplorare gli strumenti organizzativi per la cartella e i tag. In questa esperienza sono incorporati i controlli di governance per l’etichettatura standardizzata del pubblico e le funzionalità di gestione del ciclo di vita del pubblico per gestire i flussi di lavoro di attivazione. Con questa nuova esperienza di gestione, ora puoi gestire in modo semplice e sicuro i tipi di pubblico da un’unica posizione. Per ulteriori informazioni, consulta <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html" target="_blank">Documentazione di Adobe Experience Platform</a>.</p></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Canale direct mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere messaggi di direct mailing alle campagne e ai percorsi. La direct mailing è un canale offline che ti consente di personalizzare e generare i file necessari ai provider di direct mailing per inviare e-mail ai clienti.</p>
<p>Quando prepari una consegna di direct mailing, Journey Optimizer genera un file contenente tutti i profili target e le informazioni di contatto scelte (ad esempio l’indirizzo postale). Potrai quindi inviare questo file al provider di direct mailing, che si occuperà dell’invio effettivo.</p>
<img src="../direct-mail/assets/direct-mail-properties.png">
<p>Per ulteriori informazioni, consulta la <a href="../direct-mail/create-direct-mail.md">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>

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
<p>Ora puoi assegnare Tag unificati Adobe Experience Platform alle pagine di destinazione, ai modelli, ai frammenti di contenuto e agli elenchi di abbonamenti, oltre a campagne e percorsi. Ciò ti consente di classificarli facilmente e di migliorare la ricerca e la navigazione in tutti gli elenchi. Questa funzione è attualmente in versione GA (Generale disponibile).</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../start/search-filter-categorize.md#tags">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#july-2023-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Tipi di pubblico**

Sono stati apportati miglioramenti al selettore del pubblico in percorsi o campagne, con l’aggiunta di nuove colonne che mostrano l’origine e la frequenza di aggiornamento dei tipi di pubblico.

Con il rilascio del portale di composizione del pubblico, Adobe Experience Platform e Adobe Journey Optimizer hanno aggiornato l’utilizzo di &quot;tipi di pubblico&quot; e &quot;segmenti&quot; all’interno del sistema e della documentazione.

* Pubblico: un set di persone, account, famiglie o altre entità che hanno in comune caratteristiche e/o comportamenti specifici.
* Definizione di segmento: in Adobe Experience Platform, le regole utilizzate per descrivere le caratteristiche o il comportamento chiave di un pubblico di destinazione. Questo termine era precedentemente noto semplicemente come “segmento”.

Di conseguenza, in Adobe Journey Optimizer e nell’interfaccia utente di Adobe Experience Platform, vedrai che “Segmenti” è stato sostituito da “Tipi di pubblico” per riflettere questo nuovo percorso di creazione e gestione del pubblico.


**Percorsi**

* Ora puoi sfruttare le risposte alle chiamate API nelle azioni personalizzate e orchestrare il percorso in base a tali risposte.


**Campagne**

* Gli eventi contestuali relativi alle campagne sono ora disponibili per l’utilizzo nel menu &quot;Attributi contestuali&quot; dell’editor di personalizzazione.

