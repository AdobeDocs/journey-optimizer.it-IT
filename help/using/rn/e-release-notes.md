---
solution: Journey Optimizer
product: journey optimizer
title: Note preliminari sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: f371f2181b5a4b302e3cb1f47c85d470a58b9f90
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 26%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione del 25 febbraio {#25-02-rn}

### Nuove funzionalità {#25-02-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Regole aziendali</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare regole business utilizzando i set di regole. I set di regole sono gruppi di regole che ti aiutano a limitare i messaggi inviati all’interno di campagne e azioni di percorso tra canali diversi e a controllare le voci di profilo in percorsi.<p>
<p><ul><li>Crea set di regole di canale per limitare il numero di messaggi inviati su uno o più canali. Applicale alle campagne o alle azioni di percorso per applicare le regole definite nel set di regole. Il set di regole del canale consente di applicare regole di limitazione in base ai tipi di comunicazione. Ad esempio, imposta un set di regole per limitare "messaggi promozionali" e un altro per "newsletter". Applica il set di regole appropriato nella campagna o nell’azione di percorso in base al tipo di comunicazione che stai inviando.</li>
<li> Creazione di set di regole di percorso per controllare le voci di profilo nei percorsi. Limita la frequenza con cui un profilo può entrare in un percorso in un determinato periodo o il numero di percorsi in cui un profilo può essere iscritto contemporaneamente. Applicarli a livello di percorso per garantire una corretta gestione degli ingressi.</li></p>
<p>Precedentemente disponibile per un set di organizzazioni (LA), le regole aziendali sono ora disponibili per tutti gli utenti (GA).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto multi-regionale per SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi gestire la consegna di messaggi SMS da endpoint multiregionali sovrascrivendo gli URL di consegna, feedback, in entrata e callback. Per supportare questa funzione, è stato aggiunto un nuovo URL di sostituzione campo alla configurazione delle credenziali API. Questa modifica è disponibile solo con il provider Sinch.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modelli di Customer Journey Analytics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi migliorare i rapporti di Journey Optimizer sfruttando i modelli di Customer Journey Analytics. Questa nuova funzione consente di semplificare il processo di reporting con modelli pre-progettati personalizzati per le tue esigenze di analisi.
</p>
<img src="assets/do-not-localize/cja-templates.gif">
<p>Per ulteriori informazioni, consulta la <a href="../reports/report-cja-manage.md#cja-template">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: a partire dal 15 gennaio 2025</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Valutazione flessibile del pubblico (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La valutazione flessibile del pubblico consente di eseguire un processo di segmentazione su richiesta per i tipi di pubblico selezionati, garantendo di disporre sempre dei dati del pubblico più aggiornati prima di eseguirne il targeting in percorsi e campagne Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Per ulteriori informazioni, consulta la <a href="../audience/about-audiences.md#flexible">documentazione dettagliata</a>.</p>
<p> La valutazione flessibile del pubblico è disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Data di disponibilità: 28 gennaio 2025</p>
</tr>
</tbody>
</table>


### Miglioramenti {#25-02-improvements}

I miglioramenti riportati di seguito sono inclusi nell&#39;aggiornamento di febbraio.

* **Percorsi** - È ora possibile testare le azioni personalizzate del percorso inviando chiamate API dall&#39;interfaccia utente di amministrazione. Questa nuova funzionalità consente di risolvere i problemi relativi alle azioni personalizzate.

* **Durata (TTL) del set di dati** - A partire da questo mese, verrà introdotto un guardrail time-to-live (TTL) nei set di dati generati dal sistema Journey Optimizer in nuove sandbox e nuove organizzazioni come segue:

   * 90 giorni per i dati nell’archivio dei profili
   * 13 mesi per i dati nel data lake

  In una fase successiva, questa modifica verrà implementata nelle sandbox dei clienti esistenti.

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Direct mail** - DLZ (DAta Landing Zone) è ora supportato come tipo di server per il routing dei file nella configurazione Direct mail.

**Personalizzazione**

<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->

* Data di disponibilità: 29 gennaio 2025 - Nell’editor di personalizzazione sono disponibili nuove funzioni di assistenza per data e ora. [Ulteriori informazioni](../personalization/functions/dates.md)

**Configurazione e-mail** - Data di disponibilità: 12 febbraio 2025

* Se gestisci il consenso al di fuori di Adobe, ora puoi impostare un indirizzo e-mail personalizzato per l’annullamento dell’abbonamento e un URL personalizzato per l’annullamento dell’abbonamento con un solo clic, come parte delle impostazioni di configurazione del canale e-mail. [Ulteriori informazioni](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

  >[!AVAILABILITY]
  >
  >Questa funzionalità viene rilasciata in Disponibilità limitata (LA) per un set limitato di clienti.

**Decisioning** - Data di disponibilità: 28 gennaio 2025

* Decisioning ora supporta i tipi di dati Oggetto quando si modifica lo schema del catalogo elementi. [Ulteriori informazioni](../experience-decisioning/catalogs.md)