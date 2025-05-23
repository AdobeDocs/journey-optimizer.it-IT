---
solution: Journey Optimizer
product: journey optimizer
title: Integrare con Adobe Campaign v7/v8
description: Scopri come integrare Journey Optimizer con Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign, acc, integrazione
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: cc4ea97f858a212b82ac3b77328e61f59e3bfc27
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 18%

---

# Integrare con Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Azioni Adobe Campaign v7/v8"
>abstract="Questa integrazione è disponibile per Adobe Campaign v7 e v8. Consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign. La connessione tra le istanze di Journey Optimizer e Campaign viene impostata da Adobe al momento del provisioning."

Questa integrazione è disponibile per Adobe Campaign v7/v8 a partire dalla versione 7.1 e per Adobe Campaign v8. Consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign.

Un caso d&#39;uso end-to-end è presentato in questa [sezione](../building-journeys/ajo-ac.md).

Per ogni azione configurata, nella palette di Progettazione percorsi è disponibile un’attività di azione. Consulta questa [sezione](../building-journeys/using-adobe-campaign-v7-v8.md).

## Accesso {#access}

La connessione tra le istanze Journey Optimizer e Campaign viene impostata da Adobe al momento del provisioning, se richiesto. Se non hai richiesto la connessione al momento del provisioning, contatta il supporto Adobe Journey Optimizer fornendo i seguenti dettagli per richiedere l’abilitazione:

Da Adobe Journey Optimizer:

* ID organizzazione (ID organizzazione Adobe)
* Sandbox

Da Adobe Campaign:

* URL della campagna
* URL RT
* Versione di Campaign

## Note importanti {#important-notes}

* Non esiste alcuna limitazione dei messaggi. Il sistema limita il numero di messaggi che possono essere inviati a 4000 in 5 minuti, in base allo SLA della campagna corrente. Per questo motivo, Journey Optimizer deve essere utilizzato solo in casi di utilizzo unitari (eventi singoli, non tipi di pubblico).

* Devi configurare un’azione nell’area di lavoro per modello da utilizzare. Devi configurare un’azione in Journey Optimizer per ogni modello da utilizzare da Adobe Campaign.

* È consigliabile utilizzare un’istanza dedicata del Centro messaggi ospitata per questa integrazione per evitare di influenzare eventuali altre operazioni di Campaign in corso. Il server di marketing può essere in hosting o on-premise. La build richiesta è 21.1 Release Candidate o successiva.

* Non esiste alcuna convalida che dimostri che il payload o il messaggio di Campaign sono corretti.

* Non è possibile utilizzare un’azione Campaign con un evento di qualificazione del pubblico.

## Prerequisiti {#prerequisites}

In Campaign, devi creare e pubblicare un messaggio transazionale e il relativo evento associato. Consulta la [documentazione di Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html?lang=it#transactional-messaging){target="_blank"}.

Puoi creare il payload JSON corrispondente a ciascun messaggio seguendo il pattern indicato di seguito. Incolla quindi questo payload durante la configurazione dell’azione in Journey Optimizer (vedi di seguito)

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

* **channel**: il canale definito per il modello transazionale di Campaign
* **eventType**: nome interno dell&#39;evento Campaign
* **ctx**: variabile basata sulla personalizzazione disponibile nel messaggio.

## Configurazione dell’azione {#configure-action}

In Journey Optimizer, devi configurare un’azione per ogni messaggio transazionale. Segui questi passaggi:

1. Crea una nuova azione. Consulta questa [sezione](../action/action.md).
1. Immettere un nome e una descrizione.
1. Nel campo **Tipo azione**, selezionare **Adobe Campaign Classic**.
1. Fai clic nel campo **Payload** e incolla un esempio del payload JSON corrispondente al messaggio di Campaign. Contatta l’Adobe per ottenere questo payload.
1. Imposta i diversi campi in modo che siano statici o variabili a seconda che desideri mapparli sull’area di lavoro del Percorso. Alcuni campi, come i parametri del canale per l’indirizzo e-mail e i campi di personalizzazione (ctx), probabilmente dovranno essere definiti come variabili da mappare nel contesto del percorso.
1. Fai clic su **Salva**.

![](assets/accintegration1.png)