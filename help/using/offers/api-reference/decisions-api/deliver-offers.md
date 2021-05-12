---
title: Consegnare offerte
description: Gestione delle decisioni è una raccolta di servizi e programmi dell’interfaccia utente che consente agli esperti di marketing di creare e fornire esperienze di offerta personalizzate dagli utenti finali su canali e applicazioni utilizzando regole decisionali e logiche di business.
translation-type: tm+mt
source-git-commit: b527186d0722492f5f509f1ae0a5315b9a9f771e
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 2%

---

# Consegnare offerte tramite l’API Decisioni

Con Gestione delle decisioni, puoi creare e fornire esperienze di offerta personalizzate per gli utenti finali, su più canali e applicazioni utilizzando la logica di business e le regole decisionali. Un’offerta è un messaggio di marketing a cui possono essere associate regole che specificano gli utenti idonei per visualizzare l’offerta.

Puoi creare e distribuire le offerte effettuando una richiesta POST all’ API [!DNL Decisions] .

Questa esercitazione richiede una comprensione funzionante delle API, in particolare per quanto riguarda la gestione delle decisioni. Per ulteriori informazioni, consulta la [Guida per gli sviluppatori dell&#39;API di gestione delle decisioni](../getting-started.md). Questa esercitazione richiede anche che sia disponibile un ID di posizionamento e un valore dell&#39;ID decisione univoci. Se non hai acquisito questi valori, consulta le esercitazioni per [creare un posizionamento](../offers-api/placements/create.md) e [creare una decisione](../activities-api/activities/create.md).

![](../../../assets/do-not-localize/how-to-video.png) [Scopri questa funzione nel video](#video)

## Intestazioni Accept e Content-Type

La tabella seguente mostra i valori validi che comprendono i campi *Content-Type* e *Accept* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**Formato API**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le decisioni. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Richiesta**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
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
| `xdm:propositionRequests` | Questo oggetto contiene gli identificatori di posizionamento e decisione. |
| `xdm:propositionRequests.xdm:placementId` | Identificatore di posizionamento univoco. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | Identificatore decisionale univoco. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | Il numero di offerte da restituire. Il numero massimo è 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Questo oggetto contiene informazioni sul profilo per il quale viene richiesta la decisione. Per una richiesta API, questo conterrà un profilo. |
| `xdm:profiles.xdm:identityMap` | Questo oggetto contiene un set di identità utente finale basate sul codice di integrazione dello spazio dei nomi dell&#39;identità. La mappa di identità può contenere più di un’identità per ogni namespace. Per ulteriori informazioni sugli spazi dei nomi, consulta la [Panoramica sullo spazio dei nomi identità](https://docs.adobe.com/content/help/en/experience-platform/identity/namespaces.html). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | ID generato dal cliente che può essere utilizzato per identificare in modo univoco una richiesta di decisione del profilo. Questo ID viene riportato nella risposta e non influenza il risultato della decisione. | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | Questo oggetto rappresenta la struttura di controllo delle regole di deduplicazione. È costituita da una serie di flag che indicano se la stessa opzione può essere proposta in una determinata dimensione. Un flag impostato su true indica che i duplicati sono consentiti e non devono essere rimossi tra le categorie indicate dal flag . Un flag impostato su false indica che il motore di decisione non deve effettuare la stessa proposta in tutta la dimensione e sceglie invece l’opzione migliore successiva per una delle decisioni secondarie. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Se è impostato su true, a più decisioni può essere assegnata la stessa opzione. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Se è impostato su true, a più posizionamenti può essere assegnata la stessa opzione. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Identifica il criterio di unione in base al quale governare i dati restituiti dal servizio di accesso al profilo. Se non ne viene specificato uno nella richiesta, la gestione delle decisioni non passerà nessun servizio di accesso al profilo, altrimenti passerà l&#39;id fornito dal chiamante. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Un set di flag che formatta il contenuto della risposta. |
| `xdm:responseFormat.xdm:includeContent` | Valore booleano che, se impostato su `true`, include il contenuto della risposta. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Oggetto utilizzato per specificare i metadati aggiuntivi restituiti. Se questa proprietà non è inclusa, vengono restituiti `xdm:id` e `repo:etag` per impostazione predefinita. | `name` |
| `xdm:responseFormat.xdm:activity` | Questo flag identifica le informazioni di metadati specifiche restituite per `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Questo flag identifica le informazioni di metadati specifiche restituite per `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Questo flag identifica le informazioni di metadati specifiche restituite per `xdm:placement`. | `name`, `channel`, `componentType` |

**Risposta**

Una risposta corretta restituisce informazioni sulla proposta, incluso il relativo `xdm:propositionId` univoco.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
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
| `xdm:propositionId` | Identificatore univoco per l&#39;entità proposta associata a un elemento DecisionEvent XDM. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Questo oggetto contiene una singola proposta di decisione. È possibile restituire più opzioni per la decisione. Se non viene trovata alcuna opzione, viene restituita l’offerta di fallback della decisione. Le singole proposte di decisione includono sempre una proprietà `options` o una proprietà `fallback`. Se presente, la proprietà `options` non può essere vuota. |
| `xdm:propositions.xdm:activity` | Questo oggetto contiene l&#39;identificatore univoco di una decisione. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Questo oggetto contiene l’identificatore univoco di un posizionamento di offerta. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Questo oggetto contiene una singola opzione, incluso il relativo identificatore univoco. Se presente, l&#39;oggetto non può essere vuoto. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Definisce il tipo di componente. `@type` agisce come contratto di elaborazione per il cliente. Quando l&#39;esperienza viene assemblata, il compositore cercherà i componenti che hanno un tipo specifico. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | Il formato del contenuto della risposta. | Il contenuto della risposta può essere: `text`, `html block` o `image link` |
| `xdm:score` | Punteggio per un&#39;opzione calcolata come risultato di una funzione di classificazione associata all&#39;opzione o alla decisione. Questo campo viene restituito dall’API se una funzione di classificazione è coinvolta nella determinazione del punteggio di un’offerta durante la classificazione. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Questo oggetto contiene una singola offerta di fallback, incluso il relativo identificatore univoco. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | La manifestazione fisica o digitale della risorsa. In genere, il formato deve includere il tipo di supporto della risorsa. Il formato può essere utilizzato per determinare il software, l&#39;hardware o altre apparecchiature necessarie per visualizzare o utilizzare la risorsa. Si consiglia di selezionare un valore da un vocabolario controllato, ad esempio l&#39;elenco di [Tipi di file multimediali Internet](http://www.iana.org/assignments/media-types/) che definisce i formati dei file multimediali del computer. | `"dc:format": "image/png"` oppure `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Un URL facoltativo per leggere la risorsa da una rete di distribuzione di contenuti o da un endpoint di servizio. Questo URL viene utilizzato per accedere pubblicamente alla risorsa da un agente utente. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | Data e ora di creazione del messaggio di risposta della decisione. Questo è rappresentato come tempo epoca. | `"ode:createDate": 1566497582038` |

## Video tutorial {#video}

Il seguente video è pensato per aiutarti a comprendere i componenti di Gestione delle decisioni.

>[!NOTE]
>
>Questo video si applica al servizio di applicazione Offer Decisioning integrato in Adobe Experience Platform. Tuttavia, fornisce indicazioni generiche per utilizzare Offerta nel contesto di Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Passaggi successivi

Seguendo questa guida API, hai creato e consegnato le offerte utilizzando l’ [!DNL Decisions] API . Per ulteriori informazioni, consulta la [panoramica su Gestione delle decisioni](../../../offers/get-started/starting-offer-decisioning.md).
