---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 127e7cee6c474ba1e7519985e5c768be8abc6b20
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 23%

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
<th><strong>Rapporti consolidati sul canale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione Channel Report offre ad analisti ed esperti di marketing una panoramica completa delle metriche di traffico e coinvolgimento a livello di canale. Per accedere al menu Report, devi disporre dell’autorizzazione View Channel Reports (Visualizza rapporti canale).</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Destinazioni di esportazione del set di dati (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’esportazione dei set di dati Journey Optimizer nelle destinazioni di archiviazione cloud è ora generalmente disponibile. Ora, per esportare il contenuto dei set di dati, è possibile stabilire una connessione in tempo reale con posizioni di archiviazione cloud.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Archiviazione delle credenziali per le app mobili per sandbox</strong><br/></th>
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

### Miglioramenti {#sept-2023-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Tipi di pubblico**

* Ora puoi indirizzare a percorsi e campagne i tipi di pubblico caricati da un file CSV.
<!--* You can now target audiences resulting from composition workflows into journeys. -->

**Personalizzazione**

* Oltre ai frammenti visivi, ora è possibile creare, salvare e riutilizzare frammenti di espressione dall’interfaccia di Journey Optimizer tramite l’editor di espressioni. I frammenti di espressione sostituiscono le espressioni salvate in precedenza.
* Ora puoi utilizzare gli attributi calcolati da Adobe Experience Platform per la personalizzazione in Journey Optimizer. Gli attributi calcolati sono valori aggregati che vengono calcolati in base ai set di dati Experience Event abilitati per il profilo acquisiti in Adobe Experience Platform.

**Avvisi**

* Sono stati introdotti due nuovi tipi di avvisi di sistema. Ora puoi ricevere una notifica quando un’azione personalizzata o una lettura del segmento non riesce.

**Canale Web**

* Ora puoi selezionare le visualizzazioni specifiche a cui applicare le modifiche alla pagina web. Una visualizzazione può essere definita come un intero sito o un gruppo di elementi visivi su un sito, ad esempio la pagina Home, l’intero sito dei prodotti o la cornice delle preferenze di consegna su tutte le pagine di pagamento.
* Quando modifichi una pagina utilizzando il designer Web, ora puoi aggiungere nuove modifiche al contenuto direttamente dal riquadro Modifiche, senza dover selezionare un componente e modificarlo dall’interfaccia del designer.
* Durante la configurazione dei sottodomini web, ora puoi aggiungere un tuo sottodominio, oltre a utilizzare un sottodominio già delegato ad Adobe.

**Percorsi**

* Le funzionalità di risposta dell’azione personalizzata sono ora GA. Questo consente di sfruttare le risposte alle chiamate API nelle azioni personalizzate e di orchestrare il percorso in base a tali risposte. Inoltre, è stato aggiunto un nuovo guardrail per limitare tutte le azioni doganali a 5000 chiamate/s per endpoint.
* Durante la duplicazione di un percorso, è ora possibile definire il nome della copia del percorso.
* La durata massima che puoi definire nell’attività Attesa è ora di 29 giorni invece di 30.

**Canale e-mail**

Una nuova opzione nella configurazione della superficie e-mail consente di scegliere di inviare messaggi transazionali ai profili anche se i loro indirizzi e-mail sono nell’elenco di soppressione di Adobe Journey Optimizer.

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->