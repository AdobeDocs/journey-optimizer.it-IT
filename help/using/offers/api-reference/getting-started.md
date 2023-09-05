---
title: Introduzione
description: Scopri come iniziare a utilizzare l’API della Libreria di offerte per eseguire operazioni chiave utilizzando il motore decisionale.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 7%

---

# Guida per gli sviluppatori API per la gestione delle decisioni {#decision-management-api-developer-guide}

Questa guida per sviluppatori descrive i passaggi per iniziare a utilizzare [!DNL Offer Library] API. La guida fornisce quindi esempi di chiamate API per eseguire operazioni chiave utilizzando il motore decisionale.

➡️ [Ulteriori informazioni sui componenti di Gestione delle decisioni sono disponibili in questo video](#video)

## Prerequisiti {#prerequisites}

Questa guida richiede una buona conoscenza dei seguenti componenti di Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}: il quadro standardizzato mediante il quale [!DNL Experience Platform] organizza i dati sull’esperienza del cliente.
   * [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it){target="_blank"}: scopri gli elementi di base degli schemi XDM.
* [Gestione delle decisioni](../../../using/offers/get-started/starting-offer-decisioning.md): illustra i concetti e i componenti utilizzati per Experience Decisioning in generale e per la gestione delle decisioni in particolare. Illustra le strategie utilizzate per scegliere l’opzione migliore da presentare durante l’esperienza di un cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: PQL è un linguaggio potente per scrivere espressioni sulle istanze XDM. PQL viene utilizzato per definire le regole di decisione.

## Lettura delle chiamate API di esempio {#reading-sample-api-calls}

Questa guida fornisce esempi di chiamate API per dimostrare come formattare le richieste. Questi includono percorsi, intestazioni richieste e payload di richieste formattati correttamente. Viene inoltre fornito il codice JSON di esempio restituito nelle risposte API. Per informazioni sulle convenzioni utilizzate nella documentazione per le chiamate API di esempio, consulta la sezione su [come leggere esempi di chiamate API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} nel [!DNL Experience Platform] guida alla risoluzione dei problemi.

## Raccogli i valori per le intestazioni richieste {#gather-values-for-required-headers}

Per effettuare chiamate a [!DNL Adobe Experience Platform] , devi prima completare le [tutorial sull’autenticazione](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=it){target="_blank"}. Il completamento del tutorial sull’autenticazione fornisce i valori per ciascuna delle intestazioni richieste in tutte [!DNL Experience Platform] Chiamate API, come mostrato di seguito:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Tutte le richieste che contengono un payload (POST, PUT, PATCH) richiedono un’intestazione aggiuntiva:

* `Content-Type: application/json`

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
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
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

## Passaggi successivi {#next-steps}

In questo documento sono state trattate le conoscenze preliminari necessarie per effettuare chiamate [!DNL Offer Library] API, inclusa l’acquisizione dell’ID contenitore. Ora puoi passare alle chiamate di esempio fornite in questa guida per sviluppatori e seguire le loro istruzioni.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Video introduttivo {#video}

Il video seguente ha lo scopo di aiutarti a comprendere i componenti di Gestione delle decisioni.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

