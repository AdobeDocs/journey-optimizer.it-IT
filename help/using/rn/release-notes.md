---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 30d197f3eab05e2e38025189a6948a6c0fbd6d54
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Scopri di più su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti alla [newsletter trimestrale di Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Versione di agosto 2022 {#aug-2022-release}

### Nuove funzionalità

<!--table>
<thead>
<tr>
<th><strong>Create and manage campaigns in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use Journey Optimizer campaigns to deliver one-time content to a specific segment using various channels. When using journeys, actions are designed to be executed in sequence. With campaigns actions are performed simultaneously, either immediately, or based on a specified schedule. </p>
<p>For more information, refer to the <a href="../campaigns/get-started-with-campaigns.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Inviare SMS agli utenti (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare, personalizzare e inviare SMS in Journey Optimizer tramite un’integrazione con <b>Sinch</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Per informazioni su come creare e inviare un SMS, consulta la <a href="../messages/create-sms.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->



### Miglioramenti

**Generazione rapporti**

* La tabella e il grafico dei criteri di consenso sono ora disponibili nei rapporti globali del Percorso. Questi widget ti consentono di tenere traccia dei profili esclusi dai criteri nelle azioni personalizzate. [Ulteriori informazioni](../reports/journey-global-report.md#journey-global)

   Per poter accedere ai widget più recenti, è necessario reimpostare le diverse dashboard di reporting. Per ulteriori informazioni sulla personalizzazione del dashboard, consulta [la documentazione dettagliata](../reports/global-report.md).

**Amministrazione**

* È ora possibile aggiornare il numero di telefono principale da utilizzare per il canale SMS. [Ulteriori informazioni](../configuration/primary-email-addresses.md)