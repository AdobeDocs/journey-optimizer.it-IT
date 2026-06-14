---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi aggiuntivi per inviare eventi a un percorso
description: Scopri ulteriori passaggi per inviare eventi a un percorso
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: passaggi, configurazione, percorso, eventi, flusso, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
TQID: https://experienceleague.adobe.com/SiUXmerz2D-TYmIEXvaYk4usjRq67Y0v7V7sGVN-4vo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 867eeef1f90c152c463397222f5ed95f3b9c264b
workflow-type: tm+mt
source-wordcount: 347
ht-degree: 5%

---

# Passaggi aggiuntivi per l’invio di eventi {#additional-steps-to-send-events}

>[!BEGINSHADEBOX]

**In questa pagina:** Configura il sistema di dati per inviare eventi alle API Streaming Ingestion in modo che gli eventi configurati raggiungano effettivamente Journey Optimizer e attivino i tuoi percorsi.

>[!ENDSHADEBOX]

Per configurare gli eventi da inviare alle **[!UICONTROL API Streaming Ingestion]** e da utilizzare in [!DNL Journey Optimizer], è necessario eseguire la procedura seguente:

1. Ottieni l’URL di ingresso dalle API di Adobe Experience Platform. Ulteriori informazioni sono disponibili in [Panoramica delle API Streaming Ingestion](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=it){target="_blank"}.
1. Copia il payload dall&#39;anteprima del payload nel menu **[!UICONTROL Evento]**. Ulteriori informazioni sono disponibili in [questa pagina](../event/about-creating.md#define-the-payload-fields).

>[!IMPORTANT]
>
>Per i requisiti e le limitazioni degli eventi (streaming, Query Service, acquisizione batch), consulta [Guardrail di Percorso - Eventi](../start/guardrails.md#events-g).

Quindi devi configurare il sistema di dati che invia gli eventi alle API Streaming Ingestion utilizzando il payload copiato:

1. Imposta una chiamata API POST all’URL delle API Streaming Ingestion (chiamata entrata).
1. Utilizza il payload copiato da [!DNL Journey Optimizer] nel corpo (&quot;sezione dati&quot;) della chiamata API alle API Streaming Ingestion. Vedi di seguito per un esempio
1. Determina dove ottenere tutte le variabili presenti nel payload. Esempio: se l’evento deve trasmettere l’indirizzo, il payload incollato mostrerà &quot;address&quot;: &quot;string&quot;. &quot;string&quot; deve essere sostituito dalla variabile che compilerà automaticamente il valore corretto, l’e-mail della persona a cui inviare un messaggio. Tieni presente che nell&#39;anteprima del payload, nella sezione **[!UICONTROL Intestazione]**, vengono compilati automaticamente molti valori che dovrebbero facilitare il tuo lavoro.
1. Seleziona &quot;application/json&quot; come tipo di corpo.
1. Passa l’ID organizzazione nell’intestazione utilizzando la chiave &quot;x-gw-ims-org-id&quot;. Per il valore, utilizza l’ID organizzazione (&quot;XXX@AdobeOrg&quot;).

Ecco un esempio di evento Streaming Ingestion APIs:

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
            "timestamp": "2023-05-29T00:00:00.000Z",
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

Per facilitare l&#39;identificazione della posizione in cui incollare la parte &quot;data&quot;, puoi utilizzare uno strumento di visualizzazione JSON come [JSON formatter](https://jsonformatter.curiousconcept.com){target="_blank"}.

Per risolvere i problemi relativi alle API Streaming Ingestion, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}.
