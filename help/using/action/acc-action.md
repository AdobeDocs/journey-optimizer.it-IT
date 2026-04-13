---
solution: Journey Optimizer
product: journey optimizer
title: Integrare con Adobe Campaign v7/v8
description: Scopri come integrare Journey Optimizer con Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: campaign, acc, integrazione
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: ee1b6808d3247c7549e82990113d0d496c31b2a9
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 9%

---

# Integrare con Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Azioni Adobe Campaign v7/v8"
>abstract="Questa integrazione è disponibile per Adobe Campaign v7 e v8. Consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign. La connessione tra le istanze di Journey Optimizer e Campaign viene impostata da Adobe al momento del provisioning."

Se disponi di Adobe Campaign Classic v7 o Campaign v8, nei tuoi percorsi è disponibile un’azione personalizzata specifica per integrare Adobe Journey Optimizer e Adobe Campaign. Questa integrazione ti consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign. Ulteriori informazioni in questo [caso d&#39;uso end-to-end](../building-journeys/ajo-ac.md).

For each action configured, a [Campaign action activity](../building-journeys/using-adobe-campaign-v7-v8.md) is available in the journey designer palette.

## Activation {#access}

When requested, the connection between the Journey Optimizer and Adobe Campaign environments is setup by Adobe at provisioning time. If you have not requested the connection at provisioning time, contact Adobe Journey Optimizer support to request the activation. You must provide the following details:

>[!BEGINTABS]

>[!TAB Per Adobe Journey Optimizer]

* ID organizzazione (Adobe OrgID)
* Nome sandbox

>[!TAB For Adobe Campaign]

* Campaign Server URL
* Real-Time Server URL
* Your Adobe Campaign version

>[!ENDTABS]


## Guardrail e limitazioni {#important-notes}

* Non esiste alcuna limitazione dei messaggi. Il sistema limita a 4.000 il numero di messaggi che possono essere inviati in 5 minuti, in base al SLA di Campaign corrente. Per questo motivo, Journey Optimizer deve essere utilizzato solo in casi di utilizzo unitari (eventi singoli, non tipi di pubblico).

* Devi configurare un’azione nell’area di lavoro per modello da utilizzare. Devi configurare un’azione in Journey Optimizer per ogni modello da utilizzare da Adobe Campaign.

* Per questa integrazione è consigliabile utilizzare un’istanza dedicata del Centro messaggi ospitata o Managed Services, per evitare di influenzare eventuali altre operazioni di Campaign in corso. Il server di marketing può essere ospitato o on-premise.<!--The build required is 21.1 Release Candidate or greater. -->

* Non esiste alcuna convalida che dimostri che il payload o il messaggio di Campaign sono corretti.

* Non è possibile utilizzare un’azione Campaign con un evento di qualificazione del pubblico.

## Prerequisiti {#prerequisites}

In Adobe Campaign, devi creare e pubblicare un messaggio transazionale e il relativo evento associato. Consulta la [documentazione di Adobe Campaign](https://experienceleague.adobe.com/it/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}.

Puoi creare il payload JSON corrispondente a ciascun messaggio seguendo il pattern indicato di seguito. You will then paste this payload when configuring the action in Journey Optimizer (see below).

+++ Esempio

```json
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **channel**: the channel defined for your Campaign transactional template
* **eventType**: nome interno dell&#39;evento Campaign
* **ctx**: variabile basata sulla personalizzazione disponibile nel messaggio

+++

## Configurare l’azione {#configure-action}

In Journey Optimizer, devi configurare un’azione per messaggio transazionale.

To create a Campaign action, follow these steps:

1. Create a new action. [Learn how to create custom actions](../action/action.md).
1. Enter a name and description.
1. In the **[!UICONTROL Action type]** field, select **[!UICONTROL Adobe Campaign Classic]**.
   ![](assets/accintegration1.png)
1. Fai clic nel campo **[!UICONTROL Payload]** e incolla un esempio del payload JSON corrispondente al messaggio di Campaign. Contatta Adobe per ottenere questo payload.
1. Impostare ogni campo come statico o variabile a seconda che si desideri mapparlo nell&#39;area di lavoro del Percorso. Ad esempio, campi come i parametri del canale e-mail e i campi di personalizzazione (`ctx`) devono in genere essere impostati come variabili in modo che possano adattarsi dinamicamente all&#39;interno del percorso.
1. Fai clic su **[!UICONTROL Salva]**.

## Aggiorna un&#39;azione esistente {#update-action}

Se devi aggiornare un’azione personalizzata esistente per Campaign v7/v8, ad esempio quando l’endpoint in tempo reale (RT) cambia dopo la configurazione iniziale, procedi come segue:

1. From the **[!UICONTROL Administration]** menu, select **[!UICONTROL Configurations]**, then go to **[!UICONTROL Actions]**.
1. Locate and select the Campaign action you want to update from the actions list.
1. Click **[!UICONTROL Edit]** to open the action configuration.
1. Update the **[!UICONTROL URL]** field with the new RT endpoint URL. Ensure the endpoint format is correct and reachable.
1. Se necessario, aggiorna la configurazione del **[!UICONTROL Payload]** in modo che corrisponda a eventuali modifiche nella struttura dei messaggi transazionali di Campaign.
1. Click **[!UICONTROL Test]** to validate the connection to the new endpoint. Verify that the test returns a successful response before proceeding.
1. Once validated, click **[!UICONTROL Save]** to apply your changes.

>[!NOTE]
>
>Any journeys that use this action will automatically use the updated configuration. If you have live journeys using this action, monitor them closely after updating the endpoint to ensure proper message delivery.

