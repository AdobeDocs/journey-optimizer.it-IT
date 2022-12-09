---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione con Adobe Campaign Standard
description: Scopri come integrare con Adobe Campaign Standard
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Integrazione con Adobe Campaign Standard {#using_adobe_campaign_standard}

Puoi inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign Standard.

Se disponi di Adobe Campaign Standard, è disponibile un’azione incorporata per consentire la connessione ad Adobe Campaign Standard.

Per poter essere utilizzato in Journey Optimizer, il messaggio transazionale di Campaign Standard e il relativo evento associato devono essere pubblicati. Se l’evento è pubblicato ma il messaggio non lo è, non sarà visibile nell’interfaccia di Journey Optimizer. Se il messaggio viene pubblicato ma l’evento associato non lo è, sarà visibile nell’interfaccia di Journey Optimizer ma non sarà utilizzabile.

## Note importanti {#important-notes}

* Per le azioni di Adobe Campaign Standard viene automaticamente definita una regola di limitazione di 4000 chiamate per 5 minuti. Questo corrisponde alla scala ufficiale dei messaggi transazionali di Adobe Campaign Standard. Ulteriori informazioni sugli SLA di messaggistica transazionale in [Descrizione del prodotto Adobe Campaign Standard](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html).

* L’integrazione di Adobe Campaign Standard viene configurata tramite un’azione incorporata dedicata nell’elenco delle azioni. Questo deve essere configurato per ogni sandbox.

* Non puoi utilizzare un’azione Campaign Standard con qualifica Segment o attività Read segment .

* Un percorso non può utilizzare sia le azioni Messaggi che Campaign Standard.

## Configurazione dell’azione {#configure-action}

Di seguito sono riportati i passaggi per configurarlo:

1. Seleziona **[!UICONTROL Configurations]** nella sezione menu AMMINISTRAZIONE . In  **[!UICONTROL Actions]** sezione, fai clic su **[!UICONTROL Manage]**. Viene visualizzato l’elenco delle azioni disponibili.

1. Seleziona il predefinito **[!UICONTROL AdobeCampaignStandard]** azione. Il riquadro di configurazione delle azioni si apre sul lato destro dello schermo.

   ![](assets/actioncampaign.png)

1. Copia l’URL dell’istanza di Adobe Campaign Standard e incollalo nel **[!UICONTROL URL]** campo .

1. Fai clic sul pulsante **[!UICONTROL Test the instance URL]** per verificare la validità dell’istanza.

   >[!NOTE]
   >
   >Questo test verifica che:
   >
   >L’host è &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot;&quot; o &quot;.adls.adobe.com&quot;.
   >
   >L’URL inizia con https,
   >
   >L’ORG associato all’istanza di Adobe Campaign Standard è uguale all’ORG di Journey Optimizer.

Durante la progettazione del percorso, saranno disponibili tre azioni nel **[!UICONTROL Action]** categoria: **[!UICONTROL Email]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]** (vedi [Utilizzo delle azioni di Adobe Campaign](../building-journeys/using-adobe-campaign-standard.md)).

![](assets/journey58.png)

Puoi utilizzare un **Reazioni** per reagire ai dati di tracciamento relativi a un messaggio Campaign Standard inviato all’interno dello stesso percorso. Per le notifiche push, puoi reagire ai messaggi con clic, inviati o non riusciti. Per i messaggi SMS, puoi reagire ai messaggi inviati o non riusciti. Per le e-mail puoi reagire a messaggi con un clic, con un clic, un invio, un messaggio aperto o con errore. Vedi [Eventi di reazione](../building-journeys/reaction-events.md).

Se utilizzi un sistema di terze parti per l’invio dei messaggi, devi aggiungere e configurare un’azione personalizzata. Vedi [Informazioni sulla configurazione delle azioni personalizzata](../action/about-custom-action-configuration.md).
