---
title: Passaggi aggiuntivi per l’invio di eventi a un percorso
description: Scopri ulteriori passaggi per inviare eventi a un percorso
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 5%

---

# Passaggi aggiuntivi per l’invio di eventi {#additional-steps-to-send-events}

Per configurare gli eventi a cui inviare **[!UICONTROL Streaming Ingestion APIs]** e da utilizzare in [!DNL Journey Optimizer], segui questi passaggi:

1. Ottieni l’URL di ingresso dalle API di Adobe Experience Platform. Ulteriori informazioni in [Panoramica delle API Streaming Ingestion](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=it){target=&quot;_blank&quot;}.
1. Copia il payload dall’anteprima del payload nel **[!UICONTROL Event]** menu. Per ulteriori informazioni, consulta [questa pagina](../event/about-creating.md#define-the-payload-fields).

Devi quindi configurare il sistema di dati che invia gli eventi alle API Streaming Ingestion utilizzando il payload copiato:

1. Imposta una chiamata API di POST all’URL delle API Streaming Ingestion (chiamata ingresso).
1. Utilizzare il payload copiato da [!DNL Journey Optimizer] nel corpo (&quot;sezione dati&quot;) della chiamata API alle API Streaming Ingestion. Vedi sotto per un esempio
1. Stabilisci dove ottenere tutte le variabili presenti nel payload. Esempio: se l’evento deve trasmettere l’indirizzo , il payload incollato mostrerà &quot;indirizzo&quot;: &quot;string&quot;. La &quot;stringa&quot; deve essere sostituita dalla variabile che popolerà automaticamente il valore corretto, l’e-mail della persona a cui inviare un messaggio. Nell’anteprima del payload, nella sezione **[!UICONTROL Header]** Questa sezione contiene la compilazione automatica di molti valori per facilitare il lavoro.
1. Seleziona &quot;application/json&quot; come tipo di corpo.
1. Passa l’ID organizzazione nell’intestazione utilizzando la chiave &quot;x-gw-ims-org-id&quot;. Per il valore , utilizza l&#39;ID organizzazione (&quot;XXX@AdobeOrg&quot;).

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

Per facilitare l’identificazione del punto in cui incollare la parte &quot;dati&quot;, puoi utilizzare uno strumento di visualizzazione JSON, ad esempio [Formattatore JSON](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}.

Per risolvere i problemi relativi alle API Streaming Ingestion, fai riferimento a [Documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}.
