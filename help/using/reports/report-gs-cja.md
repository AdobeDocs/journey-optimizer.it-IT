---
solution: Journey Optimizer
product: journey optimizer
title: Esperienza di reporting aggiornata
description: Introduzione al rapporto tutte le ore
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bfd88d2a-e7b8-4e3b-85a1-4a14b0ba56dc
source-git-commit: a9349cedc4da2a8e76e53f9e2b5185270cda2558
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 32%

---

# Introduzione al rapporto tutte le ore {#channel-report-gs-cja}

>[!CONTEXTUALHELP]
>id="cja_connections_enable_cja"
>title="Abilitare Customer Journey Analytics"
>abstract="Per analizzare questo rapporto in Customer Journey Analytics, contatta l’amministratore per assicurarti che la tua organizzazione abbia acquistato Customer Journey Analytics e che l’integrazione sia configurata correttamente."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Customer Journey Analytics"

La funzione di reporting di Journey Optimizer include una migliorata interoperabilità con le funzionalità di Customer Journey Analytics, per standardizzare il reporting su entrambe le piattaforme e migliorare la coerenza e l’affidabilità dei dati. Questa integrazione ottimizzata tra Journey Optimizer e Customer Journey Analytics consente una visione più chiara delle metriche delle prestazioni, in modo che gli utenti possano prendere decisioni più informate.

L’accesso a queste funzionalità di reporting dipende dal contesto e dalle aree di prodotto:

* **Percorsi** - Se desideri eseguire il targeting di uno o più percorsi nel contesto di un percorso, dal menu **[!UICONTROL Percorsi]**, accedi al tuo percorso e fai clic sul pulsante **[!UICONTROL Visualizza report]**.

  Dall&#39;elenco del percorso esistente, puoi anche selezionare **[!UICONTROL Report]** dal menu avanzato del percorso selezionato. [Ulteriori informazioni sul report Percorso](journey-global-report-cja.md)

  ![](assets/gs-cja-report-3.png)

* **Campagne** - Se desideri eseguire il targeting di una campagna, dal menu **[!UICONTROL Campagne]**, accedi alla campagna e fai clic sul pulsante **[!UICONTROL Rapporti]**, quindi **[!UICONTROL Visualizza tutti i rapporti temporali]**.

  Dall&#39;elenco delle campagne esistenti, puoi anche selezionare **[!UICONTROL Report]** dal menu avanzato della campagna selezionata. [Ulteriori informazioni sul report della campagna](campaign-global-report-cja.md)

  ![](assets/gs-cja-report-2.png)

* **Globale** - Se desideri eseguire il targeting delle metriche per tutte le campagne e i percorsi all&#39;interno del tuo ambiente, accedi al report **Panoramica** accedendo al menu **[!UICONTROL Report]** nella sezione **[!UICONTROL Gestione Percorsi]**. [Ulteriori informazioni sul rapporto Panoramica](channel-report-cja.md)

  ![](assets/gs-cja-report-1.png)

>[!IMPORTANT]
>
>La generazione di rapporti in Adobe Journey Optimizer è attualmente standardizzata in UTC. La possibilità di personalizzare il fuso orario per la generazione di rapporti verrà introdotta in una versione futura.

## Prerequisiti {#prerequisites}

* Se **non** possiedi Customer Journey Analytics o se ne sei il proprietario ma **non** hai accesso ad alcun profilo di prodotto Customer Journey Analytics, le autorizzazioni vengono gestite in Journey Optimizer. In questo caso, è necessario disporre dell&#39;autorizzazione **[!UICONTROL Visualizza report canale]** o dei ruoli correlati. [Ulteriori informazioni](../administration/permissions.md)

* Se **possiedi** Customer Journey Analytics e hai accesso a un profilo di prodotto Customer Journey Analytics, devi:

   * **[!UICONTROL Autorizzazioni per la creazione di tipi di pubblico]** e **[!UICONTROL Autorizzazioni per la visualizzazione del pubblico]** per Customer Journey Analytics. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/access-control){target="_blank"}

   * **[!UICONTROL Gestione dei profili]** - Autorizzazione per Adobe Journey Optimizer. [Ulteriori informazioni](../administration/permissions.md)

* Le visualizzazioni dati di Customer Journey Analytics devono essere configurate con l&#39;impostazione seguente: **Imposta come visualizzazione dati predefinita in Adobe Journey Optimizer**. [Ulteriori informazioni sulle visualizzazioni dati](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}


## Tutti i rapporti temporali per canale

Tutti i rapporti globali temporali sono disponibili per tutti i tuoi canali. Seleziona il rapporto per il canale di cui hai bisogno per ottenere ulteriori dettagli.

### Canali in uscita

Seleziona un canale in uscita per individuare i **report globali all-time associati**.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="e-mail" src="../channels/assets/do-not-localize/email.png">
<div align="center"><p><strong>Canale e-mail</strong></p><p><a href="campaign-global-report-cja-email.md"><strong>Rapporto campagna</strong></a></p><p><a href="journey-global-report-cja-email.md"><strong>Rapporto percorso</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><p><strong>Canale SMS</strong></p><p><a href="campaign-global-report-cja-sms.md"><strong>Rapporto campagna</strong></a></p><p><a href="journey-global-report-cja-sms.md"><strong>Rapporto percorso</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-push.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><p><strong>Canale push</strong></p><p><a href="campaign-global-report-cja-push.md"><strong>Rapporto campagna</strong></a></p><p><a href="journey-global-report-cja-push.md"><strong>Rapporto percorso</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-direct.md"><img alt="direct mail" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><p><strong>Canale direct mail</strong></p><p><a href="campaign-global-report-cja-direct.md"><strong>Rapporto campagna</strong></a></p><p><a href="journey-global-report-cja-direct.md"><strong>Rapporto percorso</strong></a></p></div></td>
</tr></table>

### Esperienze in entrata

Seleziona un&#39;esperienza in entrata per individuare i **report globali all-time associati**.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="in-app" src="../channels/assets/do-not-localize/inapp.jpg">
<div align="center"><p><strong>Canale in-app</strong></p><p><a href="campaign-global-report-cja-inapp.md"><strong>Rapporto campagna</strong></a></p><p><a href="journey-global-report-cja-inapp.md"><strong>Rapporto percorso</strong></a></p></div></td>
<td><p><img alt="web" src="../channels/assets/do-not-localize/web.jpg"></p>
<div align="center"><p><strong>Canale web</strong></p><p><a href="campaign-global-report-cja-web.md"><strong>Rapporto campagna</strong></a></p><p><a href="journey-global-report-cja-web.md"><strong>Rapporto percorso</strong></a></p></div></td>
<td><img alt="esperienza basata su codice" src="../channels/assets/do-not-localize/code.png">
<div align="center"><p><strong>Esperienze basate su codice</strong></p><p><a href="campaign-global-report-cja-code.md"><strong>Rapporto campagna</strong></a></p><p><a href="campaign-global-report-cja-code.md"><strong>Rapporto percorso</strong></a></p></div></td>
<td><img alt="schede contenuto" src="../channels/assets/do-not-localize/cards.png">
<div align="center"><p><strong>Schede contenuto</strong></p><p><a href="campaign-global-report-cja-content.md"><strong>Rapporto campagna</strong></a></p><p><a href="journey-global-report-cja-content.md"><strong>Rapporto percorso</strong></a></p></div></td>
</tr></table>

## Video dimostrativo{#video}

Il video seguente mostra come utilizzare la funzionalità avanzata di reporting di Journey Optimizer con Customer Journey Analytics.

>[!VIDEO](https://video.tv.adobe.com/v/3430413)