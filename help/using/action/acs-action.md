---
solution: Journey Optimizer
product: journey optimizer
title: Integrare con Adobe Campaign Standard
description: Scopri come integrare Journey Optimizer con Adobe Campaign Standard
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: campaign, standard, integrazione, limite, azione
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
TQID: https://experienceleague.adobe.com/1JQFfviWGc3OXYN0YdAh0Koaboro2wJU8HpEf75PoKQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 450
ht-degree: 5%

---

# Integrare con Adobe Campaign Standard {#using_adobe_campaign_standard}

Se disponi di Adobe Campaign Standard, è disponibile un’azione incorporata per consentire la connessione ad Adobe Campaign Standard. Puoi inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign Standard.

Per poter essere utilizzato in Journey Optimizer, il messaggio transazionale di Campaign Standard e il relativo evento associato devono essere pubblicati. Se l’evento viene pubblicato ma il messaggio non lo è, non sarà visibile nell’interfaccia di Journey Optimizer. Se il messaggio viene pubblicato ma il relativo evento associato non lo è, sarà visibile nell’interfaccia di Journey Optimizer ma non sarà utilizzabile.

## Guardrail e limitazioni {#important-notes}

* Per le azioni Adobe Campaign Standard viene definita automaticamente una regola di limite di 4.000 chiamate ogni 5 minuti. Ulteriori informazioni sugli SLA per la messaggistica transazionale in [Descrizione del prodotto Adobe Campaign Standard](https://helpx.adobe.com/it/legal/product-descriptions/campaign-standard.html){target="_blank"}.

* L’integrazione di Adobe Campaign Standard è impostata tramite un’azione incorporata dedicata nell’elenco delle azioni. Questo deve essere configurato per ogni sandbox.

* Non è possibile utilizzare un’azione Campaign Standard con un’attività Qualificazione del pubblico o Lettura pubblico.

* Un percorso non può utilizzare sia [azioni canale incorporate](../building-journeys/journey-action.md) che [azioni Campaign Standard](../building-journeys/using-adobe-campaign-standard.md).

## Configurare l’azione {#configure-action}

In Journey Optimizer, devi configurare un’azione per messaggio transazionale.

Per configurare un’azione Campaign Standard, effettua le seguenti operazioni:

1. Selezionare **[!UICONTROL Configurazioni]** nella sezione del menu AMMINISTRAZIONE.

1. Nella sezione **[!UICONTROL Azioni]**, fai clic su **[!UICONTROL Gestisci]**. Viene visualizzato l’elenco delle azioni.

1. Seleziona l&#39;azione incorporata **[!UICONTROL AdobeCampaignStandard]**. Il riquadro di configurazione delle azioni si apre sul lato destro dello schermo.

   ![](assets/actioncampaign.png)

1. Copia l&#39;URL dell&#39;istanza di Adobe Campaign Standard e incollalo nel campo **[!UICONTROL URL]**.

1. Fai clic su **[!UICONTROL Verifica l&#39;URL dell&#39;istanza]** per verificare la validità dell&#39;istanza.

   >[!NOTE]
   >
   >Questo test verifica che:
   >
   >* L’host è &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; o &quot;.adls.adobe.com&quot;
   >
   >* L’URL inizia con https
   >
   >* L’organizzazione associata a questa istanza di Adobe Campaign Standard è la stessa dell’organizzazione Journey Optimizer

Al termine della configurazione, sono disponibili tre azioni nella categoria **[!UICONTROL Azione]** durante la progettazione di un percorso: **[!UICONTROL E-mail]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]**. [Scopri come utilizzarli](../building-journeys/using-adobe-campaign-standard.md).

![](assets/journey58.png)

Utilizza un evento **Reactions** per reagire al tracciamento dei dati relativi a un messaggio di Campaign Standard inviato nello stesso percorso:

* Per le notifiche push, i percorsi possono reagire ai messaggi selezionati, inviati o non riusciti.

* Per i messaggi SMS, i percorsi possono reagire ai messaggi inviati o non riusciti.

* Per le e-mail, i percorsi possono reagire ai messaggi selezionati, inviati, aperti o non riusciti. [Ulteriori informazioni sugli eventi di reazione](../building-journeys/reaction-events.md).

Quando utilizzi un sistema di terze parti per l’invio dei messaggi, devi aggiungere e configurare un’azione personalizzata. [Ulteriori informazioni sulla configurazione delle azioni personalizzate](../action/about-custom-action-configuration.md).