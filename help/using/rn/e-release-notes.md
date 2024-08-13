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
source-git-commit: 9fdaff7a4364bb7ecfeec27446ed8f4b4ce34488
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 52%

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
<th><strong>Configurazioni di canale migliorate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le funzionalità della superficie di canale corrente sono state migliorate per un approccio coerente su tutti i canali. Ora puoi definire, gestire e riutilizzare queste configurazioni per qualsiasi canale.</p>
<p><ul>
<li>Le superfici di canale ora sono rinominate in <strong>Configurazioni canale</strong></li>
<li>Dall’inventario delle configurazioni di canale ora puoi creare configurazioni di canale riutilizzabili per tutti i canali, inclusi ora il web, la messaggistica in-app o l’esperienza basata su codice</li>
<li>Il controllo dell'accesso a livello di oggetto (OLAC) è ora disponibile per ogni configurazione di canale, consentendo di decidere quali utenti possono creare o utilizzare configurazioni specifiche</li>
<li>Per alcuni canali, puoi creare configurazioni di canale mirate per più piattaforme. Ad esempio, potrebbe trattarsi di una configurazione del canale di messaggistica in-app in grado di eseguire il targeting per una pagina web, un’app iOS e un’app Android.</li>
</ul></p>
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

* Nell&#39;attività **Condition**, per impostazione predefinita, la condizione Ora è impostata per ora, dalle 00:00 alle 12:00. [Ulteriori informazioni](../building-journeys/condition-activity.md#time_condition)

**Tipi di pubblico**

* L’utilizzo dei tipi di pubblico provenienti da caricamento personalizzato (file CSV) è ora disponibile con Privacy and Security Shield.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
