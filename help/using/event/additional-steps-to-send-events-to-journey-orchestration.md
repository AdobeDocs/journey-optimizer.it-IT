---
title: Passaggi aggiuntivi per l’invio di eventi a un percorso
description: Scopri ulteriori passaggi per inviare eventi a un percorso
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# Passaggi aggiuntivi per l&#39;invio di eventi {#concept_xrz_n1q_y2b}

![](../assets/do-not-localize/badge.png)

Per configurare gli eventi da inviare a **[!UICONTROL Streaming Ingestion APIs]** e da utilizzare in [!DNL Journey Optimizer], segui questi passaggi:

1. Ottieni l’URL di ingresso dalle API di Adobe Experience Platform. Ulteriori informazioni sono disponibili in [Panoramica delle API Streaming Ingestion](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html).
1. Copia il payload dall’anteprima del payload nel menu **[!UICONTROL Event]** . Ulteriori informazioni in [questa pagina](../event/about-creating.md#define-the-payload-fields).

Devi quindi configurare il sistema di dati che invia gli eventi alle API Streaming Ingestion utilizzando il payload copiato:

1. Imposta una chiamata API di POST all’URL delle API Streaming Ingestion (chiamata ingresso).
1. Utilizza il payload copiato da [!DNL Journey Optimizer] nel corpo (&quot;sezione dati&quot;) della chiamata API alle API Streaming Ingestion. Vedi sotto per un esempio
1. Stabilisci dove ottenere tutte le variabili presenti nel payload. Esempio: se l’evento deve trasmettere l’indirizzo , il payload incollato mostrerà &quot;indirizzo&quot;: &quot;string&quot;. La &quot;stringa&quot; deve essere sostituita dalla variabile che popolerà automaticamente il valore corretto, l’e-mail della persona a cui inviare un messaggio. Nell’anteprima del payload, nella sezione **[!UICONTROL Header]** verranno compilati automaticamente molti valori che dovrebbero facilitare il lavoro dell’utente.
1. Seleziona &quot;application/json&quot; come tipo di corpo.
1. Passa il tuo ID organizzazione IMS nell’intestazione utilizzando la chiave &quot;x-gw-ims-org-id&quot;. Per il valore , utilizza il tuo ID organizzazione IMS (&quot;XXX@AdobeOrg&quot;).

Ecco un esempio di evento API Streaming Ingestion:

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2018-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

Per facilitare l’identificazione del punto in cui incollare la parte &quot;dati&quot;, puoi utilizzare uno strumento di visualizzazione JSON, ad esempio [https://jsonformatter.curiousconcept.com](https://jsonformatter.curiousconcept.com)

Per risolvere i problemi relativi alle API Streaming Ingestion, fai riferimento a questa [pagina](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html).
