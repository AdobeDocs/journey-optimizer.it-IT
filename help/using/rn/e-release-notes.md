---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 128a56b543f470bf967fd195fde73ff7b32b2a17
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 57%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di agosto 2024 {#e-2024}

**Data di rilascio**: 20-21 agosto 2024

### Nuove funzionalità {#e-features}

Questa versione include le nuove funzionalità elencate di seguito.


<table>
<thead>
<tr>
<th><strong>Impostazione canale guidato</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configurazione guidata del canale consente di automatizzare i passaggi per la configurazione del canale mobile in un’esperienza unificata, per iniziare più rapidamente a utilizzare Journey Optimizer. Questa configurazione facilita la configurazione rapida dei canali di marketing, garantendo che tutte le risorse richieste siano prontamente disponibili in Experience Platform, Journey Optimizer e Data Collection. Questo consente al team marketing di iniziare immediatamente con la creazione di campagne e percorsi.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Schede contenuto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La scheda di contenuto è una nuova funzione di messaggistica digitale di Adobe Journey Optimizer che offre contenuti personalizzati e coinvolgenti direttamente all’interno di app mobili e siti web. A differenza delle notifiche push tradizionali, le schede di contenuto si integrano perfettamente nell’interfaccia utente, offrendo aggiornamenti persistenti e non intrusivi che migliorano l’interazione e l’esperienza dell’utente.</p>
<p>Questa funzione consente agli addetti al marketing di presentare contenuti rich media rilevanti agli utenti, aumentando il coinvolgimento e garantendo la visualizzazione di messaggi importanti senza interrompere il percorso degli utenti.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configurazioni del canale migliorate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le funzionalità della superficie di canale corrente sono state migliorate per un approccio coerente su tutti i canali. Ora è possibile definire, gestire e riutilizzare queste configurazioni per qualsiasi canale.</p>
<p><ul>
<li>Le superfici di canale ora sono state rinominate in <strong>Configurazioni di canale</strong></li>
<li>Dall’inventario delle configurazioni di canale ora è possibile creare configurazioni di canale riutilizzabili per tutti i canali, inclusi il Web, la messaggistica in-app o l’esperienza basata su codice</li>
<li>Il controllo dell’accesso a livello di oggetto (OLAC) è ora disponibile per ogni configurazione di canale, consentendo di decidere quali utenti possono creare o utilizzare configurazioni specifiche</li>
<li>Per alcuni canali, è possibile creare configurazioni di canale in grado di eseguire il targeting per più piattaforme. Ad esempio, potrebbe trattarsi di una configurazione di canale di messaggistica in-app in grado di eseguire il targeting per una pagina web, un’app iOS e un’app Android.</li>
</ul></p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/ip-warmup-gs.md">documentazione dettagliata</a>.</p>
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
<p>I frammenti ora possono utilizzare variabili di input, sia nei <a href="../personalization/use-expression-fragments.md">frammenti di espressione</a> che nei <a href="../email/use-visual-fragments.md">frammenti visivi</a>. Puoi utilizzare queste variabili per personalizzare il contenuto e i parametri dei messaggi nelle campagne e nei percorsi.</p>
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

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Percorsi**

* Nell’attività **Condizione**, per impostazione predefinita, adesso la condizione Tempo è impostata per ora, dalle 00:00 alle 12:00. [Ulteriori informazioni](../building-journeys/condition-activity.md#time_condition)
* Durante la creazione dei percorsi, gli avvisi vengono ora visualizzati in un elenco a discesa, per allinearsi agli avvisi delle campagne e fornire un’esperienza utente coerente. [Ulteriori informazioni](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Sono state migliorate le opzioni di zoom nella barra degli strumenti del percorso: la percentuale di zoom è ora visibile ed è possibile reimpostare facilmente il valore di zoom al 100%.

**Tipi di pubblico**

* L’utilizzo dei tipi di pubblico provenienti da caricamento personalizzato (file CSV) è ora disponibile con Privacy and Security Shield.
* Quando esegui il targeting di un pubblico di caricamento personalizzato (file CSV), ora puoi utilizzare gli attributi del file nelle campagne e nei percorsi. Questi attributi sono disponibili nell’editor di personalizzazione, per personalizzare i messaggi, e nell’editor di espressioni avanzate di percorso.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
