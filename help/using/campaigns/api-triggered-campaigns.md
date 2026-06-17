---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 17%

---
Autorizzazioni dello strumento wiki non concesse. Continuerò utilizzando le informazioni dettagliate del ticket stesso, che contiene le specifiche chiave (500 TPS predefiniti, 1000/1500 TPS livelli tramite Performance Add-on, solo push, supporta aumenti burst/limitati nel tempo).

&#x200B;---

soluzione: Journey Optimizer
product: percorsi optimizer
title: Utilizzare campagne attivate da API
description: Scopri come attivare campagne utilizzando le API di Journey Optimizer.
funzione: Campagne, API
topic: Gestione dei contenuti
ruolo: Sviluppatore
livello: esperienza
parole chiave: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
- id: cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label: Journey Optimizer
feature_v2:
- id: a653cc2e-bc85-4353-a306-399e5b247978
internal-label: campagne Journey Optimizer
subfeature_v2:
- id: f7479fa1-474b-479d-8c98-f6cee5865a38
internal-label: campagne attivate dall’API
- id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label: Gestione delle campagne
role_v2:
- id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label: Developer
topic_v2:
- id: e0eb8757-182f-49f3-94a4-1587d16f5094
internal-label: Personalization

Ecco il file markdown aggiornato completo:

&#x200B;---

```
solution: Journey Optimizer
product: journey optimizer
title: Work with API triggered campaigns
description: Learn how to trigger campaigns using Journey Optimizer APIs.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campaigns, API-triggered, REST, optimizer, messages
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
    internal-label: Journey Optimizer campaigns
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
    internal-label: API triggered campaigns
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
    internal-label: Campaign management
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
```

# Utilizzare le campagne attivate da API {#trigger-campaigns}

>[!BEGINSHADEBOX]

**In questa pagina:** crea e avvia campagne attivate dall&#39;API tramite una chiamata API REST per poter inviare messaggi di marketing e transazionali in tempo reale utilizzando dati di profilo e contestuali.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campagne attivate da API"
>abstract="**Campagne attivate da API transazionale**<br/> Attivare messaggi in tempo reale tramite chiamate API <br/><br/>**Messaggi di marketing**<br/> Contenuto promozionale (richiede consenso, soggetto a regole business)<br/><br/>**Messaggi transazionali**<br/> Contenuto relativo ai servizi (conferma, avvisi, non soggetto al consenso marketing)<br/><br/>**Canali disponibili**<br/> E-mail, SMS, notifiche push"

## Informazioni sulle campagne attivate da API {#about}

Le campagne attivate da API consentono alle comunicazioni di marketing di raggiungere un pubblico al momento giusto oppure messaggi transazionali/operativi a un individuo come la reimpostazione della password, in cui la necessità può comportare la personalizzazione non solo utilizzando gli attributi del profilo, ma anche dati contestuali in tempo reale nel trigger, che è un payload API REST.

A questo scopo, devi innanzitutto creare una campagna attivata da API in Journey Optimizer, quindi avviarne l&#39;esecuzione tramite una chiamata API utilizzando l&#39;[API REST di esecuzione interattiva dei messaggi](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution).

➡️ [Scopri questa funzione nel video](#video)

>[!NOTE]
>
>Per ulteriori informazioni sui canali supportati, consulta la tabella in questa sezione: [Canali nei percorsi e nelle campagne](../channels/gs-channels.md#channels).
>
>I canali disponibili variano in base al modello di licenza e ai componenti aggiuntivi.

## Velocità effettiva notifiche push {#push-throughput}

Per impostazione predefinita, le campagne attivate da API supportano fino a **500 transazioni al secondo (TPS)** per la consegna di notifiche push. Le organizzazioni con requisiti di messaggistica operativa per volumi elevati possono aumentare questo limite tramite il componente aggiuntivo **Prestazioni**.

Il componente aggiuntivo Performance fornisce due livelli di velocità effettiva più elevati per le notifiche push:

| Livello | Velocità effettiva |
|------|-----------|
| Standard | 500 TPS (incluso per tutti i clienti) |
| Componente aggiuntivo prestazioni - Livello 1 | 1.000 TPS |
| Componente aggiuntivo Prestazioni - Livello 2 | 1.500 TPS |

Un throughput più elevato è disponibile sia come incremento contrattuale permanente che per una **durata limitata** per supportare scenari temporanei di volumi elevati come il lancio di prodotti o campagne su larga scala.

>[!NOTE]
>
>I livelli di velocità effettiva aumentati si applicano solo al **canale di notifica push** per le campagne attivate dall&#39;API. I canali e-mail e SMS non rientrano nell’ambito di questo componente aggiuntivo.
>
>Contatta il team del tuo account Adobe per abilitare un livello di velocità effettiva più elevato per la tua organizzazione.

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

>[!VIDEO](https://video.tv.adobe.com/v/3452733?captions=ita&quality=12)

&#x200B;---

L&#39;aggiunta chiave è la nuova sezione **Throughput notifiche push** (`## Push notification throughput {#push-throughput}`) situata tra &quot;Informazioni su&quot; e &quot;Passaggi chiave&quot;, che documenta:
- Il 500 TPS predefinito incluso per tutti i clienti
- I due livelli del componente aggiuntivo Prestazioni (1.000 e 1.500 TPS)
- Sostegno ad aumenti permanenti e limitati
- Ambito limitato solo al canale push
- Una nota che indirizza i clienti al loro account team Adobe