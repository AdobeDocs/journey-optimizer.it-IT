---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: f24f4526d4b324df8da56013f0e41c11e1268ca8
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 77%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di luglio 2024 {#e-2024}

**Data di rilascio**: 30-31 luglio 2024

### Nuove funzionalità {#e-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Flusso di lavoro di preparazione IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se invii un’e-mail con un nuovo indirizzo IP, ora puoi eseguire facilmente i flussi di lavoro di preparazione IP direttamente dall’interfaccia utente. Adobe Journey Optimizer offre un modo standardizzato ed efficiente di preparare gli indirizzi IP seguendo le best practice per una recapitabilità ottimale.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Canale SMS con qualsiasi provider (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora, in Journey Optimizer, puoi configurare altri provider SMS oltre a quelli predefiniti Sinch, Infobip e Twilio.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Federated Audience Composition (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Federated Audience Composition è ora disponibile in Adobe Journey Optimizer. Consente alle aziende di comporre i dati per un migliore utilizzo in vari casi d’uso. Con questo nuovo approccio, in qualità di utente di Adobe Real-time Customer Data Platform e/o Adobe Journey Optimizer, puoi federare i set di dati direttamente dal data warehouse esistente per creare e arricchire il pubblico e gli attributi di Adobe Experience Platform in un unico sistema.</p>
<!--p>For more information, refer to the <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Marketo Engage custom action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now integrate Adobe Journey Optimizer with Adobe Marketo Engage to build your B2B use cases. From a journey, a new custom action allows you to ingest data into Marketo.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved channel configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>From the Channel configurations inventory you can now create reusable channel configurations for all channels, including now Web, In-app messaging, or Code-based experience</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


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

* (Disponibilità: 8 luglio) È ora possibile sfruttare l’editor di espressioni avanzato durante la configurazione di un evento, che consente di definire espressioni più complesse o utilizzare funzioni nella condizione per l’ID evento. [Ulteriori informazioni](../event/about-creating.md#adv-exp-editor)

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

**Canale in-app**

* I frammenti di espressione sono ora disponibili per il canale in-app.

**Tipi di pubblico**

* L’utilizzo dei tipi di pubblico provenienti da caricamento personalizzato (file CSV) è ora disponibile con Privacy and Security Shield.
<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->
