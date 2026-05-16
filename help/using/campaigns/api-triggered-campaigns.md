---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare le campagne attivate da API
description: Scopri come attivare le campagne utilizzando le API di Journey Optimizer.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 41%

---

# Utilizzare le campagne attivate da API {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campagne attivate da API"
>abstract="**Campagne attivate da API transazionale**<br/> Attivare messaggi in tempo reale tramite chiamate API <br/><br/>**Messaggi di marketing**<br/> Contenuto promozionale (richiede consenso, soggetto a regole business)<br/><br/>**Messaggi transazionali**<br/> Contenuto relativo ai servizi (conferma, avvisi, non soggetto al consenso marketing)<br/><br/>**Canali disponibili**<br/> E-mail, SMS, notifiche push"

## Informazioni sulle campagne attivate da API {#about}

Le campagne attivate da API consentono alle comunicazioni di marketing di raggiungere un pubblico al momento giusto oppure messaggi transazionali/operativi a un individuo come la reimpostazione della password, in cui la necessità può comportare la personalizzazione non solo utilizzando gli attributi del profilo, ma anche dati contestuali in tempo reale nel trigger, che è un payload API REST.

A questo scopo, devi innanzitutto creare una campagna attivata da API in Journey Optimizer, quindi avviarne l&#39;esecuzione tramite una chiamata API utilizzando l&#39;[API REST di esecuzione interattiva dei messaggi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

➡️ [Guarda un video su questa funzione](#video)

>[!NOTE]
>
>Per ulteriori informazioni sui canali supportati, consulta la tabella in questa sezione: [Canali nei percorsi e nelle campagne](../channels/gs-channels.md#channels).
>
>I canali disponibili variano in base al modello di licenza e ai componenti aggiuntivi.

## Passaggi chiave per la creazione di campagne attivate da API {#steps}

Prima di iniziare con le campagne, controlla i seguenti prerequisiti elencati [in questa sezione](get-started-with-campaigns.md#prerequisites). Una volta soddisfatti questi prerequisiti, puoi iniziare a creare la campagna:

1. [Definire le proprietà della campagna](api-triggered-campaign-properties.md)
1. [Configurare l’azione della campagna](api-triggered-campaign-action.md)
1. [Modificare il contenuto della campagna](api-triggered-campaign-content.md)
1. [Definire il pubblico della campagna](api-triggered-campaign-audience.md)
1. [Pianificare la campagna](api-triggered-campaign-schedule.md)
1. [Rivedere e attivare una campagna](review-activate-api-triggered-campaign.md)
1. [Attivare l’esecuzione della campagna](trigger-campaigns.md)

Ulteriori informazioni sul [flusso di lavoro completo per la creazione di campagne con guide specifiche per tipo →](get-started-with-campaigns.md#workflow)

## Video dimostrativi {#video}

Scopri come creare una campagna e attivarla da un sistema esterno basato sulle interazioni dell’utente, utilizzando l’API REST di Esecuzione interattiva dei messaggi.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
