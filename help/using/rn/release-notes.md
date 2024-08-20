---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d971d857a480868f5ef502f3a3f2c209afc93cca
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 70%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Note preliminari sulla versione di agosto 2024 {#e-2024}

**Data di rilascio**: 20-21 agosto 2024

>[!CAUTION]
>
>**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di rilascio**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati alla data di rilascio.
>

### Nuove funzionalità {#e-features}

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
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Content Cards</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content card is a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved Channel Configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels, including Web, In-app messaging, or Code-based experience.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>You can attach one or multiple marketing actions to enforce consent and data governance policies</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
</td>
</tr>
</tbody>
</table-->

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


### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Percorsi**

<!--* In the **Condition** activity, by default, the Time condition is now set by hour, from 00:00 to 12:00. [Read more](../building-journeys/condition-activity.md#time_condition)-->
* Durante la creazione dei percorsi, gli avvisi vengono ora visualizzati in un elenco a discesa, per allinearsi agli avvisi delle campagne e fornire un’esperienza utente coerente. [Ulteriori informazioni](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Sono state migliorate le opzioni di zoom nella barra degli strumenti del percorso: la percentuale di zoom è ora visibile ed è possibile reimpostare facilmente il valore di zoom al 100%.

**Tipi di pubblico**

* L’utilizzo dei tipi di pubblico da caricamento personalizzato (file CSV) è ora disponibile con il componente aggiuntivo Privacy and Security Shield.
* Quando esegui il targeting di un pubblico di caricamento personalizzato (file CSV), ora puoi utilizzare gli attributi del file nelle campagne e nei percorsi. Questi attributi sono disponibili nell’editor di personalizzazione, per personalizzare i messaggi, e nell’editor di espressioni avanzate di percorso.

## Note sulla versione di luglio 2024 {#24-7-2024}

**Data di rilascio**: 30-31 luglio 2024

### Nuove funzionalità {#27-4-features}

Questa versione include le nuove funzionalità elencate di seguito.

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
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../sms/sms-configuration-custom.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Composizione di pubblico federato (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Composizione di pubblico federato è ora disponibile in Adobe Journey Optimizer. Consente alle aziende di comporre dati per un migliore utilizzo in vari casi d’uso. Con questo nuovo approccio, in qualità di utente di Adobe Real-Time Customer Data Platform e/o di Adobe Journey Optimizer, puoi federare i set di dati direttamente dal data warehouse esistente per arricchire i tipi di pubblico e gli attributi di Adobe Experience Platform in un unico sistema.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/it/docs/federated-audience-composition/using/home"  target="_blank">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#27-4-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Percorsi**

* (Data di disponibilità: 8 luglio) **Editor di espressioni avanzate nella configurazione degli eventi percorso**: ora puoi sfruttare l’editor di espressioni avanzate durante la configurazione di un evento, in modo da definire espressioni più complesse o utilizzare funzioni nella condizione ID evento. [Ulteriori informazioni](../event/about-creating.md#adv-exp-editor)

