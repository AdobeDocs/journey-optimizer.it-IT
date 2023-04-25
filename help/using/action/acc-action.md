---
solution: Journey Optimizer
product: journey optimizer
title: Integrare con Adobe Campaign v7/v8
description: Scopri come integrare Journey Optimizer con Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campagna, acc, integrazione
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 22%

---

# Integrare con Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Azioni Adobe Campaign v7/v8"
>abstract="Questa integrazione è disponibile per Adobe Campaign Classic v7 e v8. Consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign. La connessione tra le istanze di Journey Optimizer e Campaign viene impostata da Adobe al momento del provisioning."

Questa integrazione è disponibile per Adobe Campaign Classic v7 a partire dalla versione 7.1 e Adobe Campaign v8. Consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign.

La connessione tra le istanze di Journey Optimizer e Campaign viene impostata da Adobe al momento del provisioning.

In questo viene presentato un caso d’uso end-to-end [sezione](../building-journeys/ajo-ac.md).

Per ogni azione configurata, nella palette Progettazione percorsi è disponibile un’attività di azione. Fai riferimento a questa [sezione](../building-journeys/using-adobe-campaign-classic.md).

## Note importanti {#important-notes}

* I messaggi non sono soggetti a limitazione. Il sistema limita il numero di messaggi che possono essere inviati a 4000 per 5 minuti, in base allo SLA di Campaign corrente. Per questo motivo, Journey Optimizer deve essere utilizzato solo in casi d’uso unitari (singoli eventi, non segmenti).

* È necessario configurare un’azione sull’area di lavoro per modello da utilizzare. Devi configurare un’azione in Journey Optimizer per ogni modello che desideri utilizzare da Adobe Campaign.

* È consigliabile utilizzare un’istanza del Centro messaggi dedicata ospitata per questa integrazione per evitare di influenzare altre operazioni di Campaign che potrebbero essere in corso. Il server di marketing può essere ospitato o on-premise. La build richiesta è 21.1 Release Candidate o successiva.

* Non esiste una convalida relativa alla correttezza del payload o del messaggio Campaign.

* Non puoi utilizzare un’azione Campaign con un evento di qualificazione dei segmenti.

## Prerequisiti {#prerequisites}

In Campaign, devi creare e pubblicare un messaggio transazionale e il relativo evento associato. Fai riferimento a [Documentazione di Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target="_blank"}.

Puoi creare il payload JSON corrispondente a ciascun messaggio seguendo il pattern seguente. Quindi incolla questo payload durante la configurazione dell’azione in Journey Optimizer (vedi di seguito).

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

1. Crea una nuova azione. Fai riferimento a questa [sezione](../action/action.md).
1. Immetti un nome e una descrizione.
1. In **Tipo di azione** campo , seleziona **Adobe Campaign Classic**.
1. Fai clic in **Payload** e incolla un esempio del payload JSON corrispondente al messaggio Campaign. Per ottenere questo payload, contatta l’Adobe .
1. Regola i diversi campi in modo che siano statici o variabili a seconda di se desideri mapparli sull’area di lavoro del Percorso. Alcuni campi, come i parametri del canale per l’indirizzo e-mail e i campi di personalizzazione (ctx), probabilmente dovranno essere definiti come variabili da mappare nel contesto del percorso.
1. Fai clic su **Salva**.

![](assets/accintegration1.png)
