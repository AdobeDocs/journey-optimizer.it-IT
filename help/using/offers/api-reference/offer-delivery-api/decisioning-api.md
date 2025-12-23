---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Consegnare offerte
description: Gestione delle decisioni è una raccolta di servizi e programmi di interfaccia utente che consente agli addetti marketing di creare e fornire esperienze di offerta personalizzate per l’utente finale tramite diversi canali e applicazioni utilizzando la logica di business e le regole decisionali.
badge: label="Legacy" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
version: Journey Orchestration
source-git-commit: d34dfa121f005d28c6ab8895de2bbbd0cdf71dc1
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 4%

---

# Distribuire le offerte tramite l’API Decisioning {#decisioning-api}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../../experience-decisioning/gs-experience-decisioning.md)

Con la funzione di gestione delle decisioni, puoi creare e fornire esperienze di offerta personalizzate per l’utente finale, per diversi canali e applicazioni utilizzando la logica di business e le regole decisionali. Un’offerta è un messaggio di marketing a cui possono essere associate delle regole che determinano gli utenti idonei per visualizzare l’offerta.

È possibile creare e distribuire offerte effettuando una richiesta POST all&#39;API [!DNL Decisioning].

Questo tutorial richiede una buona conoscenza delle API, in particolare per quanto riguarda la gestione delle decisioni. Per ulteriori informazioni, consulta la [Guida per gli sviluppatori API per la gestione delle decisioni](../getting-started.md). Questo tutorial richiede anche di avere a disposizione un ID posizionamento e un valore ID decisione univoci. Se non hai acquisito questi valori, consulta i tutorial per [creare un posizionamento](../offers-api/placements/create.md) e [creare una decisione](../activities-api/activities/create.md).

>[!NOTE]
>
>**Trasmissione dei dati contestuali nelle richieste Decisioning**
>
>Puoi trasmettere dati contestuali (come tipo di dispositivo, posizione o preferenze utente) nelle richieste di Decisioning per creare regole di idoneità dinamiche e distribuire offerte personalizzate in base a condizioni in tempo reale. [Ulteriori informazioni sui dati contestuali e sulle richieste Decisioning](../../context-data-decisioning.md)

## Intestazioni richieste {#required-headers}

La tabella seguente mostra i valori validi che comprendono i campi *Content-Type* e *Accept* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accetta | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |
| Authorization | `Bearer {ACCESS_TOKEN}` |
| x-gw-ims-org-id | `{IMS_ORG}` |
| x-sandbox-name | `{SANDBOX_NAME}` |
| x-api-key | `{API_KEY}` |

* Tutte le richieste che contengono un payload (POST,PUT,PATCH) richiedono l’intestazione del tipo di contenuto


>[!NOTE]
>
>Il controllo delle autorizzazioni non viene applicato per singole sandbox. Se il chiamante ha presentato un token valido, l’API di consegna passerà attraverso.

## richiesta API {#request}

### Formato API

```https
POST /{ENDPOINT_PATH}/decisions
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/ods` |

### Richiesta

```shell
curl -X POST 'https://platform.adobe.io/data/core/ods/decisions' \
-H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
-H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}....' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'x-request-id: e9ac8d7e-3e77-4b38-8726-555ef1737b32-example' \
-d '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:15ded04b1786ea27",
            "xdm:placementId": "dps:offer-placement:15d9bc01d35e1238"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "example@adobe.com",
                        "primary": true
                    }
                ]
            }
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}' 
```

| Proprietà | Descrizione | Esempio |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | Questo oggetto contiene gli identificatori di posizionamento e di decisione. |  |
| `xdm:propositionRequests.xdm:placementId` | L’identificatore di posizionamento univoco. | `"xdm:placementId": "dps:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | L’identificatore di decisione univoco. | `"xdm:activityId": "dps:offer-activity:ffed0123"` |
| `xdm:itemCount` | Il numero di offerte da restituire. Il numero massimo è 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Questo oggetto contiene informazioni sul profilo per cui è richiesta la decisione. Per una richiesta API questo conterrà un profilo. |  |
| `xdm:profiles.xdm:identityMap` | Questo oggetto contiene un set di identità dell’utente finale basate sul codice di integrazione dello spazio dei nomi dell’identità. La mappa delle identità può contenere più di un’identità di ogni spazio dei nomi. Per ulteriori informazioni sugli spazi dei nomi, vedere [questa pagina](../../../audience/get-started-identity.md). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | L’ID generato dal client che può essere utilizzato per identificare in modo univoco una richiesta di decisione di profilo. Questo ID viene ripreso nella risposta e non influenza l’esito della decisione. | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | Questo oggetto rappresenta la struttura di controllo delle regole di deduplicazione. È costituito da una serie di flag che indicano se la stessa opzione può essere proposta in una determinata dimensione. Un flag impostato su true significa che i duplicati sono consentiti e non devono essere rimossi in tutta la categoria indicata dal flag. Un flag impostato su false significa che il motore decisionale non deve fare la stessa proposta in tutta la dimensione e scegliere invece l’opzione migliore successiva per una delle sottodecisioni. |  |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Se è impostato su true, a più decisioni può essere assegnata la stessa opzione. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Se è impostato su true, a più posizionamenti può essere assegnata la stessa opzione. | `"xdm:acrossPlacements": true` |
| `xdm:enrichedAudience` | Imposta questo parametro su `true` se esegui il targeting per un pubblico di tipo Caricamento personalizzato (CSV) e desideri recuperare i dati di arricchimento nella risposta della decisione di offerta. [Ulteriori informazioni sull&#39;utilizzo dei tipi di pubblico CSV per le decisioni](../../custom-upload-decisioning.md#must-read) | `"xdm:enrichedAudience": true` |
| `xdm:mergePolicy.xdm:id` | Identifica il criterio di unione in base al quale gestire i dati restituiti dal servizio di accesso al profilo. Se non ne viene specificato uno nella richiesta, la gestione delle decisioni non trasmette alcun servizio di accesso al profilo, altrimenti trasmette l’ID fornito dal chiamante. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Un set di flag che formatta il contenuto della risposta. |  |
| `xdm:responseFormat.xdm:includeContent` | Valore booleano che, se impostato su `true`, include contenuto nella risposta. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Oggetto utilizzato per specificare i metadati aggiuntivi restituiti. Se questa proprietà non è inclusa, `xdm:id` e `repo:etag` vengono restituiti per impostazione predefinita. | `name` |
| `xdm:responseFormat.xdm:activity` | Questo flag identifica le informazioni di metadati specifiche restituite per `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Questo flag identifica le informazioni di metadati specifiche restituite per `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Questo flag identifica le informazioni di metadati specifiche restituite per `xdm:placement`. | `name`, `channel`, `componentType` |

### Risposta

In caso di esito positivo, la risposta restituisce informazioni sulla proposta, incluso l&#39;univoco `xdm:propositionId`.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "dps:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "dps:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "dps:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| Proprietà | Descrizione | Esempio |
| -------- | ----------- | ------- |
| `xdm:propositionId` | L’identificatore univoco dell’entità proposta associata a un DecisionEvent XDM. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Questo oggetto contiene una singola proposta di decisione. È possibile restituire più opzioni per la decisione. Se non viene trovata alcuna opzione, viene restituita l’offerta di fallback della decisione. Le proposte a decisione singola includono sempre una proprietà `options` o una proprietà `fallback`. Se presente, la proprietà `options` non può essere vuota. |  |
| `xdm:propositions.xdm:activity` | Questo oggetto contiene l’identificatore univoco di una decisione. | `"xdm:id": "dps:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Questo oggetto contiene l’identificatore univoco per il posizionamento di un’offerta. | `"xdm:id": "dps:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Questo oggetto contiene una singola opzione, incluso il relativo identificatore univoco. Se presente, questo oggetto non può essere vuoto. | `xdm:id": "dps:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Definisce il tipo di componente. `@type` funge da contratto di elaborazione per il client. Quando l&#39;esperienza viene assemblata, il compositore cercherà i componenti che hanno un tipo specifico. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | Il formato del contenuto della risposta. | Il contenuto della risposta può essere: `text`, `html block` o `image link` |
| `xdm:score` | Il punteggio di un’opzione calcolato come risultato di una funzione di classificazione associata all’opzione o alla decisione. Questo campo verrà restituito dall’API se una funzione di classificazione è coinvolta nella determinazione del punteggio di un’offerta durante la classificazione. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Questo oggetto contiene una singola offerta di fallback, incluso il relativo identificatore univoco. | `"xdm:id": "dps:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | La manifestazione fisica o digitale della risorsa. In genere, il formato deve includere il tipo di file multimediale della risorsa. Il formato può essere utilizzato per determinare il software, l&#39;hardware o altre apparecchiature necessarie per visualizzare o utilizzare la risorsa. È consigliabile selezionare un valore da un vocabolario controllato, ad esempio l&#39;elenco di [tipi di supporti Internet](https://www.iana.org/assignments/media-types/) che definiscono i formati dei supporti per computer. | `"dc:format": "image/png"` o `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Un URL facoltativo per leggere la risorsa da una rete di distribuzione di contenuti o da un endpoint di servizio. Questo URL viene utilizzato per accedere pubblicamente alla risorsa da un agente utente. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | L’ora in cui è stato creato il messaggio di risposta alla decisione. Questo è rappresentato come tempo dell&#39;epoca. | `"ode:createDate": 1566497582038` |

**Codici di risposta**

La tabella seguente elenca tutti i codici che possono essere restituiti nella risposta:

| Codice | Descrizione |
|  ---  |  ---  |
| 200 | Operazione completata. La decisione è stata presa per determinate attività |
| 400 | Parametro di richiesta non valido. Impossibile comprendere la richiesta dal server a causa di sintassi non valida. |
| 403 | Autorizzazioni non consentite, insufficienti. |
| 422 | Entità non elaborabile. La sintassi della richiesta è corretta, tuttavia, a causa di errori semantici non è possibile elaborarla. |
| 429 | Troppe richieste. L’utente ha inviato troppe richieste in un determinato periodo di tempo. |
| 500 | Errore interno del server. Il server ha rilevato una condizione imprevista che ha impedito il completamento della richiesta. |
| 503 | Servizio non disponibile a causa di sovraccarico del server. Il server non è attualmente in grado di gestire la richiesta a causa di un sovraccarico temporaneo. |

<!-- ## Tutorial video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12) -->

## Passaggi successivi {#next-steps}

Seguendo questa guida API, hai creato e consegnato offerte utilizzando l&#39;API [!DNL Decisions]. Per ulteriori informazioni, consulta la [panoramica sulla gestione delle decisioni](../../../offers/get-started/starting-offer-decisioning.md).
