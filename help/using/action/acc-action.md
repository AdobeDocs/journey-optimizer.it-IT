---
title: Integrare con Adobe Campaign v7/v8
description: Scopri come integrare con Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 51c63b196b11905289c3c0c450c1976eb551bbc8
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 4%

---

# Integrare con Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-classic}

Questa integrazione è disponibile per Adobe Campaign Classic v7 a partire dalla versione 21.1 e Adobe Campaign v8. Ti consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign.

La connessione tra le istanze Journey Optimizer e Campaign viene impostata per Adobe al momento del provisioning.

In questo viene presentato un caso d’uso end-to-end [sezione](../building-journeys/campaign-classic-use-case.md).

For each action configured, an action activity is available in the journey designer palette. Refer to this [section](../building-journeys/using-adobe-campaign-classic.md).

## Note importanti {#important-notes}

* I messaggi non sono soggetti a limitazione. Il sistema limita il numero di messaggi che possono essere inviati a 4000 per 5 minuti, in base allo SLA di Campaign corrente. Per questo motivo, Journey Optimizer deve essere utilizzato solo in casi d’uso unitari (singoli eventi, non segmenti).

* È necessario configurare un’azione sull’area di lavoro per modello da utilizzare. You need to configure one action in Journey Optimizer for each template you wish to use from Adobe Campaign.

* È consigliabile utilizzare un’istanza del Centro messaggi dedicata ospitata per questa integrazione per evitare di influenzare altre operazioni di Campaign che potrebbero essere in corso. The marketing server can be hosted or on-premise. The build required is 21.1 Release Candidate or greater.

* There is no validation that the payload or Campaign message is correct.

* Non puoi utilizzare un’azione Campaign con un evento di qualificazione dei segmenti.

## Prerequisiti {#prerequisites}

In Campaign, devi creare e pubblicare un messaggio transazionale e il relativo evento associato. Refer to the [Adobe Campaign documentation](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target=&quot;_blank&quot;}.

Puoi creare il payload JSON corrispondente a ciascun messaggio seguendo il pattern seguente. You will then paste this payload when configuring the action in Journey Orchestration (see below)

Ecco un esempio:

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **canale**: il canale definito per il modello transazionale di Campaign
* **eventType**: il nome interno dell’evento Campaign
* **ctx**: in base alla personalizzazione contenuta nel messaggio.

## Configurazione dell’azione {#configure-action}

In Journey Optimizer, devi configurare un’azione per messaggio transazionale. Segui questi passaggi:

1. Create a new action. Fai riferimento a questo [sezione](../action/action.md).
1. Enter a name and description.
1. In **Tipo di azione** campo , seleziona **Adobe Campaign Classic**.
1. Click in the **Payload** field and paste an example of the JSON payload corresponding to the Campaign message. Per ottenere questo payload, contatta l’Adobe .
1. Regola i diversi campi in modo che siano statici o variabili a seconda di se desideri mapparli sull’area di lavoro del Percorso. Alcuni campi, come i parametri del canale per l’indirizzo e-mail e i campi di personalizzazione (ctx), probabilmente dovranno essere definiti come variabili da mappare nel contesto del percorso.
1. Fai clic su **Salva**.

![](assets/accintegration1.png)
