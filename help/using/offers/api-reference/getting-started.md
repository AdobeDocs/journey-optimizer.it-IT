---
title: Introduzione
description: Scopri come iniziare a utilizzare l’API della Libreria offerte per eseguire operazioni chiave utilizzando il motore di gestione delle decisioni.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 6%

---

# Guida per gli sviluppatori API per la gestione delle decisioni {#decision-management-api-developer-guide}

Questa guida per gli sviluppatori descrive i passaggi necessari per iniziare a utilizzare [!DNL Offer Library] API. La guida fornisce quindi un esempio di chiamate API per eseguire operazioni chiave utilizzando il modulo di gestione delle decisioni.

➡️ [Scopri questa funzione nel video](#video)

## Prerequisiti {#prerequisites}

Questa guida richiede una buona comprensione dei seguenti componenti di Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}: Il quadro standardizzato [!DNL Experience Platform] organizza i dati sulla customer experience.
   * [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it){target=&quot;_blank&quot;}: Scopri i blocchi di base degli schemi XDM.
* [Gestione delle decisioni](../../../using/offers/get-started/starting-offer-decisioning.md): Spiega i concetti e i componenti utilizzati per Experience Decisioning in generale e in particolare per l’Offer decisioning. Illustra le strategie utilizzate per scegliere l’opzione migliore da presentare durante l’esperienza di un cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;}: PQL è un linguaggio potente per scrivere espressioni sulle istanze XDM. PQL viene utilizzato per definire le regole decisionali.

## Lettura di chiamate API di esempio {#reading-sample-api-calls}

Questa guida fornisce esempi di chiamate API per dimostrare come formattare le richieste. Questi includono percorsi, intestazioni richieste e payload di richiesta formattati correttamente. Viene inoltre fornito un esempio di codice JSON restituito nelle risposte API. Per informazioni sulle convenzioni utilizzate nella documentazione per le chiamate API di esempio, consulta la sezione sulle [come leggere le chiamate API di esempio](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target=&quot;_blank&quot;} nel [!DNL Experience Platform] guida alla risoluzione dei problemi.

## Raccogli i valori delle intestazioni richieste {#gather-values-for-required-headers}

Per effettuare chiamate a [!DNL Platform] API, devi prima completare l’ [esercitazione sull&#39;autenticazione](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}. Il completamento dell’esercitazione sull’autenticazione fornisce i valori per ciascuna delle intestazioni richieste in tutte le [!DNL Experience Platform] Chiamate API, come mostrato di seguito:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Tutte le richieste che contengono un payload (POST, PUT, PATCH) richiedono un’intestazione aggiuntiva:

* `Content-Type: application/json`

## Gestire l’accesso a un contenitore {#manage-access-to-container}

Un contenitore è un meccanismo di isolamento per tenere separate le diverse preoccupazioni. L’ID contenitore è il primo elemento del percorso per tutte le API dell’archivio. Tutti gli oggetti decisionali risiedono all&#39;interno di un contenitore.

Un amministratore può raggruppare entità, risorse e autorizzazioni di accesso simili in profili. Ciò riduce l’onere di gestione ed è supportato da [Adobe Admin Console](https://adminconsole.adobe.com/). Devi essere un amministratore di prodotto per Adobe Experience Platform nella tua organizzazione per creare profili e assegnare loro gli utenti. È sufficiente creare profili di prodotto che corrispondano a determinate autorizzazioni in un unico passaggio e quindi aggiungere semplicemente gli utenti a tali profili. I profili fungono da gruppi a cui sono state concesse autorizzazioni e ogni utente effettivo o tecnico del gruppo eredita tali autorizzazioni.

In base ai privilegi di amministratore, è possibile concedere o revocare le autorizzazioni agli utenti tramite [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Per ulteriori informazioni, consulta la sezione [Panoramica sul controllo degli accessi](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=it){target=&quot;_blank&quot;}.

### Elencare contenitori accessibili a utenti e integrazioni {#list-containers-accessible-to-users-and-integrations}

**Formato API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
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

Una risposta corretta restituisce informazioni relative ai contenitori di gestione delle decisioni. Questo include `instanceId` , il cui valore è l&#39;ID del contenitore.

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

Il presente documento tratta le conoscenze necessarie per effettuare chiamate [!DNL Offer Library] API, inclusa l’acquisizione dell’ID contenitore. Ora puoi passare alle chiamate di esempio fornite in questa guida per gli sviluppatori e seguire le relative istruzioni.

## Video tutorial {#video}

Il seguente video è pensato per aiutarti a comprendere i componenti di Gestione delle decisioni.

>[!NOTE]
>
>Questo video si applica al servizio di applicazione Offer Decisioning integrato in Adobe Experience Platform. Tuttavia, fornisce indicazioni generiche per utilizzare Offerta nel contesto di Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
