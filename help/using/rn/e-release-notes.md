---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1cbc5512fe23db22eca4fe1a2cb512a154b01844
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 32%

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
<th><strong>Flusso di lavoro di riscaldamento IP (GA)</strong><br/></th>
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
<p>Ora puoi configurare altri provider SMS in Journey Optimizer, oltre ai provider predefiniti Sinch, Infobip e Twilio.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<p>Ora puoi integrare Adobe Journey Optimizer con Adobe Marketo Engage per creare i tuoi casi d’uso B2B. Da un percorso, una nuova azione personalizzata consente di acquisire dati in Marketo.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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

* (Disponibilità: 8 luglio) Ora puoi sfruttare l’editor di espressioni avanzate durante la configurazione di un evento, consentendoti di definire espressioni più complesse o utilizzare funzioni nella condizione ID evento. [Ulteriori informazioni](../event/about-creating.md#adv-exp-editor)

<!--* The `event-id` condition is now automatically filled during test mode. -->

**Canale SMS**

* Ora puoi modificare le configurazioni SMS esistenti.

**Canale in-app**

* I frammenti di espressione sono ora disponibili per il canale in-app.

**Canale push**

* Ora puoi aggiungere le credenziali push dell’app mobile nelle impostazioni di configurazione del canale Adobe Journey Optimizer. Non è più necessario creare una superficie app nella raccolta dati di Adobe Experience Platform.

**Tipi di pubblico**

* L’utilizzo di tipi di pubblico e attributi dalla composizione del pubblico e dal caricamento personalizzato (file CSV) è ora disponibile con Healthcare Shield o Privacy and Security Shield.