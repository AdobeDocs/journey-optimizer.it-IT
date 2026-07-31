---
solution: Journey Optimizer
product: journey optimizer
title: API per le sfide di fedeltà
description: Scopri come utilizzare le API REST delle sfide di fedeltà per gestire in modo programmatico le sfide e interrogare lo stato di partecipazione al profilo in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Developer
level: Intermediate
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 3756e104086c83bbca88b2fe770a40a8e9f39ef3
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 8%

---


# API per le sfide di fedeltà {#loyalty-challenges-api}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare le API REST delle sfide di fedeltà per creare e gestire in modo programmatico le sfide e per eseguire query e aggiornare lo stato di partecipazione alle sfide per i singoli profili.

>[!ENDSHADEBOX]

## Accesso rapido {#quick-access}

Sono disponibili due API REST per le sfide di fedeltà:

* **[API dei metadati della sfida di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}**: crea, recupera, aggiorna, pubblica, archivia e duplica le sfide a livello di programmazione.
* **[API dello stato della richiesta di verifica della fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}** — Eseguire query e aggiornare lo stato di partecipazione alla richiesta di verifica per i singoli profili.

## API metadati per sfida fedeltà {#metadata-api}

L’API per i metadati della sfida fedeltà consente di gestire l’intero ciclo di vita delle sfide al di fuori dell’interfaccia utente di Journey Optimizer. Utilizzala per automatizzare le operazioni di verifica o integrare la gestione dei programmi fedeltà nei tuoi strumenti e flussi di lavoro. Ad esempio, puoi creare, pubblicare e archiviare le sfide, recuperare tutte le sfide con il filtraggio e l’ordinamento o duplicare una sfida esistente includendo i metadati di percorso e le campagne.

➡️ [Riferimento API metadati richiesta di verifica fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

## API per lo stato di sfida fedeltà {#state-api}

L’API per lo stato di sfida Fedeltà consente di interagire con i record di partecipazione alla sfida a livello di profilo. Utilizzarlo per eseguire una query sullo stato di partecipazione corrente di un profilo, sull&#39;avanzamento e sul completamento dell&#39;attività, ad esempio per recuperare tutti i record di partecipazione alla verifica per un profilo, controllare lo stato di un&#39;attività specifica all&#39;interno di una verifica o ritirare un profilo da una o più verifiche.

➡️ [Riferimento API per lo stato della sfida fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}

## Autenticazione {#authentication}

Tutte le chiamate API relative alle sfide di fedeltà richiedono le seguenti intestazioni:

| Intestazione | Descrizione |
|---|---|
| `Authorization` | Token Bearer dal token di accesso IMS |
| `x-gw-ims-org-id` | ID organizzazione IMS |
| `x-api-key` | ID client (chiave API) |
| `x-sandbox-name` | Nome della sandbox di destinazione |

Segui l&#39;[esercitazione sull&#39;autenticazione](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} per recuperare queste credenziali.
