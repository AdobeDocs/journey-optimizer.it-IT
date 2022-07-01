---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 108a7aab025aa92fab59c26d0bf5bf5339b81bb3
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 84%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Scopri di più su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti alla [newsletter trimestrale di Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Versione di giugno 2022 {#june-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Inviare SMS agli utenti (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare, personalizzare e inviare SMS in Journey Optimizer tramite un’integrazione con <b>Sinch</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Il canale SMS è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p>Per informazioni su come creare e inviare un SMS, consulta la <a href="../messages/create-sms.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>L’integrazione con Adobe Stock consente di trovare più rapidamente immagini di forte impatto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il plug-in per l’integrazione di Adobe Stock e Adobe Journey Optimizer Email Designer offre ai clienti un modo semplice di cercare le immagini da utilizzare nella creazione dei messaggi, acquistarne la licenza e salvarle. </br> La nuova opzione <b>Trova foto Stock simili</b> consente inoltre di individuare foto Stock simili alle tue immagini per contenuto, colore e composizione. </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../design/stock.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizza E-mail Ccn in tutte le e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile utilizzare la funzionalità E-mail Ccn (copia carbone nascosta) per memorizzare le e-mail inviate da Adobe Journey Optimizer. Se abiliti questa opzione nei tuoi predefiniti e-mail, ogni e-mail verrà inviata anche come copiata nascosta all’indirizzo in Ccn.</p>
<img src="assets/do-not-localize/bcc-rn.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/bcc-email.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Copiare oggetti tra le sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi ricreare le esperienze da una sandbox Journey Optimizer a un’altra, ad esempio da una sandbox non di produzione a una sandbox di produzione. Questa nuova funzionalità consente di copiare un intero Percorso, compresi tutti gli oggetti da cui dipende l’esecuzione corretta del Percorso, da un ambiente all’altro. Oltre ai Percorsi, puoi anche copiare altri componenti quali Offerte, Messaggi, Schemi, Set di dati, Origini dati, Eventi e Azioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/copy-to-sandbox.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Miglioramenti

**Gestione delle decisioni**

* **Supporto di file HTML e JSON**: ora è possibile trascinare file HTML e JSON esterni dalla libreria di risorse Adobe Experience Cloud nel contenuto della rappresentazione dell’offerta. [Ulteriori informazioni](../offers/offer-library/add-representations.md#html-json)


**E-mail**

* **Salva come modello**: ora è possibile salvare un contenuto e-mail come modello e riutilizzarlo per creare altri messaggi. [Ulteriori informazioni](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**Amministrazione**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **Parametri URL di tracciamento anteprima**: quando configuri un predefinito di messaggio, se definisci i parametri di tracciamento URL ora viene visualizzata un’anteprima dinamica dell’URL di tracciamento risultante. [Ulteriori informazioni](../configuration/email-settings.md#url-tracking)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
