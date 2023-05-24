---
solution: Journey Optimizer
product: journey optimizer
title: Integrare con Adobe Campaign Standard
description: Scopri come integrare Journey Optimizer con Adobe Campaign Standard
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campaign, standard, integrazione, limite, azione
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 5%

---

# Integrare con Adobe Campaign Standard {#using_adobe_campaign_standard}

Puoi inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign Standard.

Se disponi di Adobe Campaign Standard, è disponibile un’azione incorporata per consentire la connessione ad Adobe Campaign Standard.

Per poter essere utilizzato in Journey Optimizer, il messaggio transazionale di Campaign Standard e il relativo evento associato devono essere pubblicati. Se l’evento viene pubblicato ma il messaggio non lo è, non sarà visibile nell’interfaccia di Journey Optimizer. Se il messaggio viene pubblicato ma il relativo evento associato non lo è, sarà visibile nell’interfaccia di Journey Optimizer ma non sarà utilizzabile.

## Note importanti {#important-notes}

* Per le azioni Adobe Campaign Standard viene automaticamente definita una regola di limite di 4000 chiamate ogni 5 minuti. Ciò corrisponde alla scala ufficiale di Adobe Campaign Standard Transactional Messaging. Ulteriori informazioni sugli SLA della messaggistica transazionale in [Descrizione del prodotto Adobe Campaign Standard](https://helpx.adobe.com/it/legal/product-descriptions/campaign-standard.html).

* L’integrazione di Adobe Campaign Standard è impostata tramite un’azione incorporata dedicata nell’elenco delle azioni. Questo deve essere configurato per ogni sandbox.

* Non è possibile utilizzare un’azione Campaign Standard con una qualificazione del segmento o un’attività Leggi segmento.

* Un percorso non può utilizzare sia messaggi che azioni di Campaign Standard.

## Configurazione dell’azione {#configure-action}

Di seguito sono riportati i passaggi per configurarlo:

1. Seleziona **[!UICONTROL Configurazioni]** nella sezione del menu ADMINISTRATION. In  **[!UICONTROL Azioni]** , fare clic su **[!UICONTROL Gestisci]**. Viene visualizzato l’elenco delle azioni.

1. Seleziona il predefinito **[!UICONTROL AdobeCampaign Standard]** azione. Il riquadro di configurazione delle azioni si apre sul lato destro dello schermo.

   ![](assets/actioncampaign.png)

1. Copia l’URL dell’istanza di Adobe Campaign Standard e incollalo nella **[!UICONTROL URL]** campo.

1. Fai clic su **[!UICONTROL Verifica l’URL dell’istanza]** per verificare la validità dell’istanza.

   >[!NOTE]
   >
   >Questo test verifica che:
   >
   >L’host è &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; o &quot;.adls.adobe.com&quot;.
   >
   >L’URL inizia con https,
   >
   >L’ORGANIZZAZIONE associata a questa istanza di Adobe Campaign Standard è la stessa dell’ORGANIZZAZIONE di Journey Optimizer.

Durante la progettazione del percorso, sono disponibili tre azioni nel **[!UICONTROL Azione]** categoria: **[!UICONTROL E-mail]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]** (vedere [Utilizzo delle azioni di Adobe Campaign](../building-journeys/using-adobe-campaign-standard.md)).

![](assets/journey58.png)

È possibile utilizzare una **Reazioni** per reagire ai dati di tracciamento relativi a un messaggio Campaign Standard inviato all’interno dello stesso percorso. Per le notifiche push, puoi reagire ai messaggi con clic, inviati o non riusciti. Per i messaggi SMS, puoi reagire ai messaggi inviati o non riusciti. Per le e-mail, puoi reagire ai messaggi su cui hai fatto clic, che hai inviato, che hai aperto o non sei riuscito. Consulta [Eventi di reazione](../building-journeys/reaction-events.md).

Se utilizzi un sistema di terze parti per l’invio dei messaggi, devi aggiungere e configurare un’azione personalizzata. Consulta [Informazioni sulla configurazione delle azioni personalizzata](../action/about-custom-action-configuration.md).
