---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare azioni personalizzate per scrivere eventi di Percorso in AEP
description: Utilizzare azioni personalizzate per scrivere eventi di Percorso in AEP
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer
level: Experienced
exl-id: 890a194f-f54d-4230-863a-fb2b924d716a
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 4%

---

# Utilizzare azioni personalizzate per scrivere eventi del percorso in Experience Platform {#custom-action-aep}

Questo caso d’uso spiega come scrivere eventi personalizzati in Adobe Experience Platform da Percorsi utilizzando Azioni personalizzate e chiamate autenticate.

## Configurare un progetto per sviluppatori {#custom-action-aep-IO}

1. Da Adobe Developer Console, fai clic su **Progetto** e apri il progetto di I/O.

1. Nella sezione **Credenziali**, fai clic su **OAuth Server-to-Server**.

   ![](assets/custom-action-aep-1.png)

1. Fare clic su **Visualizza comando cURL**.

   ![](assets/custom-action-aep-2.png)

1. Copiare il comando cURL e archiviare client_id, client_secret, grant_type e scope.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

>[!CAUTION]
>
>Dopo aver creato il progetto su Adobe Developer Console, assicurati di concedere agli sviluppatori e al controllo dell’accesso API le autorizzazioni appropriate. Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/landing/platform-apis/api-authentication#grant-developer-and-api-access-control){target="_blank"}

## Configurare l’origine utilizzando l’ingresso API HTTP

1. Crea un endpoint in Adobe Experience Platform per scrivere i dati dai percorsi.

1. In Adobe Experience Platform, fai clic su **Origini**, in **Connessioni** nel menu a sinistra. In **API HTTP**, fare clic su **Aggiungi dati**.

   ![](assets/custom-action-aep-3.png)

1. Seleziona **Nuovo account** e abilita l&#39;autenticazione. Selezionare **Connetti a Source**.

   ![](assets/custom-action-aep-4.png)

1. Seleziona **Avanti** e il set di dati in cui desideri scrivere i dati. Fai clic su **Avanti** e **Fine**.

   ![](assets/custom-action-aep-5.png)

1. Apri il flusso di dati appena creato. Copia il payload dello schema e salvalo nel blocco note.

```
{
"header": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
},
"imsOrgId": "<org_id>",
"datasetId": "<dataset_id>",
"source": {
"name": "Custom Journey Events"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
}
},
"xdmEntity": {
"_id": "test1",
"<your_org>": {
"journeyVersionId": "",
"nodeId": "", "customer_Id":""
},
"eventMergeId": "",
"eventType": "",
"producedBy": "self",
"timestamp": "2018-11-12T20:20:39+00:00"
}
}
}
```

## Configurare l’azione personalizzata {#custom-action-config}

La configurazione dell&#39;azione personalizzata è dettagliata in [questa pagina](../action/about-custom-action-configuration.md).

Per questo esempio, segui questi passaggi:

1. Apri Adobe Journey Optimizer e fai clic su **Configurazioni**, in **Amministrazione** nel menu a sinistra. In **Azioni**, fai clic su **Gestisci** e poi su **Crea azione**.

1. Imposta l’URL e seleziona il metodo Post.

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. Assicurati che le intestazioni (Content-Type, Charset, sandbox-name) siano configurate.

   ![](assets/custom-action-aep-7bis.png)

### Configurare l’autenticazione {#custom-action-aep-authentication}

1. Seleziona **Tipo** come **Personalizzato** con il seguente payload.

1. Incollare client_secret, client_id, scope e grant_type dal payload del progetto IO utilizzato in precedenza.

   ```
   {
   "type": "customAuthorization",
   "authorizationType": "Bearer",
   "endpoint": "https://ims-na1.adobelogin.com/ims/token/v3",
   "method": "POST",
   "headers": {},
   "body": {
   "bodyType": "form",
   "bodyParams": {
   "grant_type": "client_credentials",
   "client_secret": "********",
   "client_id": "<client_id>",
   "scope": "openid,AdobeID,read_organizations,additional_info.projectedProductContext,session"
   }
   },
   "tokenInResponse": "json://access_token",
   "cacheDuration": {
   "duration": 28000,
   "timeUnit": "seconds"
   }
   }
   ```

1. Utilizza **Fare clic per verificare l&#39;autenticazione** per verificare la connessione.

   ![](assets/custom-action-aep-8.png)

### Impostare il payload {#custom-action-aep-payload}

1. Nei campi **Richiesta** e **Risposta**, incolla il payload dalla connessione di origine utilizzata in precedenza.

   ```
   {
   "xdmMeta": {
   "schemaRef": {
   "id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
   "contentType": "application/vnd.adobe.xed-full+json;version=1.0"
   }
   },
   "xdmEntity": {
   "_id": "/uri-reference",
   "<your_org>": {
   "journeyVersionId": "Sample value",
   "nodeId": "Sample value",
   "customer_Id":""
   },
   "eventMergeId": "Sample value",
   "eventType": "advertising.completes,
   "producedBy": "self",
   "timestamp": "2018-11-12T20:20:39+00:00"
   }
   }
   ```

1. Modifica la configurazione del campo da **Costante** a **Variabile** per i campi che verranno compilati in modo dinamico.

1. Salva l&#39;azione personalizzata.

## Percorso

1. Infine, utilizza questa azione personalizzata in un percorso per scrivere gli eventi di percorso personalizzati.

1. Popola l’ID versione del Percorso, l’ID nodo, il nome del nodo e altri attributi in base al tuo caso d’uso.

   ![](assets/custom-action-aep-9.png)
