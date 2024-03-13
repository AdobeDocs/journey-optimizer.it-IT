---
title: Introduzione alla recapitabilità delle offerte tramite API
description: Ulteriori informazioni sulle API disponibili per distribuire le offerte personalizzate.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 4%

---

# Introduzione alla recapitabilità delle offerte tramite API {#about-decisioning-apis}

Puoi distribuire le offerte utilizzando **Decisioning** o **Edge Decisioning** API. Inoltre, il **Batch Decisioning** API ti consente di distribuire offerte a tutti i profili in un determinato pubblico in una chiamata. Il contenuto dell’offerta per ogni profilo del pubblico viene inserito in un set di dati Adobe Experience Platform dove è disponibile per flussi di lavoro batch personalizzati.

In questa pagina trovi informazioni su funzionalità specifiche disponibili con **Decisioning** e **Edge Decisioning** API. Sebbene entrambi consentano di offrire offerte ai clienti, si consiglia di utilizzare **Edge Decisioning** Se possibile, API per casi di utilizzo in entrata e per garantire una migliore latenza e velocità effettiva sulla piattaforma.

Per ulteriori informazioni su come utilizzare le API, consulta le sezioni seguenti:
* [API Decisioning](decisioning-api.md)
* [API Edge Decisioning](edge-decisioning-api.md)
* [API Batch Decisioning](batch-decisioning-api.md)

## Gestire l’accesso a un contenitore {#manage-access-to-container}

Un contenitore è un meccanismo di isolamento per tenere separate le diverse preoccupazioni. L’ID contenitore è il primo elemento percorso per tutte le API dell’archivio. Tutti gli oggetti decisioning si trovano all’interno di un contenitore.

Un amministratore può raggruppare entità principali e risorse simili e accedere alle autorizzazioni nei profili. Ciò riduce il carico di gestione ed è supportato da [Adobe Admin Console](https://adminconsole.adobe.com/). Per creare profili e assegnare utenti a Adobe Experience Platform nella tua organizzazione, devi essere amministratore di prodotto. È sufficiente creare profili di prodotto che soddisfino determinate autorizzazioni in un unico passaggio e quindi aggiungere semplicemente gli utenti a tali profili. I profili fungono da gruppi ai quali sono state concesse autorizzazioni e ogni utente reale o tecnico di quel gruppo eredita tali autorizzazioni.

Dati i privilegi di amministratore, puoi concedere o revocare le autorizzazioni agli utenti tramite [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=it){target="_blank"}.

### Elencare i contenitori accessibili agli utenti e alle integrazioni {#list-containers-accessible-to-users-and-integrations}

**Formato API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtra l’elenco dei contenitori in base alla loro associazione ai contesti di prodotto. | `acp` |
| `{PROPERTY}` | Filtra il tipo di contenitore restituito. | `_instance.containerType==decisioning` |

**Richiesta**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce le informazioni relative ai contenitori di gestione delle decisioni. Ciò include un `instanceId` , il cui valore corrisponde all&#39;ID del contenitore.

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2023-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2023-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## Funzionalità API di Edge Decisioning {#edge}

**Richiesta univoca per eventi di esperienza e richieste di decisioni**

Con l’API Edge Decisioning, puoi inviare in un’unica richiesta l’evento esperienza stesso insieme alla richiesta decisioning, anziché avere due richieste diverse.

Ad esempio, se un cliente visita il tuo sito web, la richiesta includerà l’evento esperienza (la visita del cliente alla pagina) e otterrà nuovamente un’offerta per popolare la pagina visitata.

**Archiviazione dei dati contestuali in Adobe Experience Platform**

I dati contestuali si riferiscono a dati che si conoscono solo al momento in cui si desidera che venga restituita un’offerta. Ad esempio, il colore dell’articolo acquistato, il tempo al momento dell’acquisto, ecc.

Quando si trasmettono dati contestuali con una richiesta API Edge Decisioning, i dati vengono memorizzati nel profilo di Adobe Experience Platform, consentendo un riutilizzo futuro.

>[!NOTE]
>
>Per memorizzare i dati contestuali, è necessario configurare uno schema XDM dedicato.

**Aggiornamento del contatore dei limiti di frequenza**

Se per alcune offerte è stato abilitato il limite di frequenza per definire la frequenza con cui viene reimpostato il conteggio dei limiti, il contatore viene aggiornato e disponibile in una decisione API Edge Decisioning in meno di 3 secondi. [Scopri come aggiungere vincoli a un’offerta](../../offer-library/add-constraints.md)

## Funzionalità API di decisioning {#decisioning}

Le funzionalità elencate di seguito sono disponibili solo con l’API Decisioning. Se devi sfruttarne una per soddisfare le tue esigenze, utilizza l’API Decisioning. In caso contrario, consigliamo di utilizzare le API Edge Decisioning.

* **Contenuto e caratteristiche dell’offerta**: puoi scegliere di non restituire il contenuto e le caratteristiche di un’offerta utilizzando un’opzione dedicata.
* **Metadati offerta**: abilita un’opzione per restituire i metadati di un’offerta.
* **Criterio di unione**: utilizza nella richiesta un criterio di unione diverso da quello associato alla sandbox.
* **Eventi decisionali e quota limite**: gli eventi di blocco delle decisioni non vengono conteggiati da alcun limite di frequenza che si verifica.
* **Proposte duplicate**: abilita un’opzione per non deduplicare le proposte.
