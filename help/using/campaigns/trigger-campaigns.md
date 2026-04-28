---
solution: Journey Optimizer
product: journey optimizer
title: Rivedere e attivare una campagna
description: Learn how to review and activate campaigns in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campaign, review, validation, activation, activating, optimizer
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 1%

---


# Execute an API triggered campaign {#execute}

Once your campaign has been activated, you need to retrieve the generated sample cURL request and use it into the API to build your payload and trigger the campaign.

## Da leggere {#must-read}

* **Campaign start/end dates** - If you have configured a specific start and/or end date when creating the campaign, it will not be executed outside these dates, and API calls will fail.

* **Call timeout** - The call to the Interactive Message Execution REST API has a timeout of 60 sec. However internal retries are in place in case of unexpected timeouts to guarantee the delivery.

## Trigger the campaign {#trigger}

1. Open the campaign, then copy-paste the payload request from the **[!UICONTROL cURL request]** section. This payload includes all personalization (profile and context) variables used in the message. It is available once the campaign is live.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >The endpoints in the cURL section differ between standard and [High throughput campigns](../campaigns/api-triggered-high-throughput.md).

1. Use this cURL request into the APIs to build your payload and trigger the campaign. For more information, refer to the [Interactive Message Execution API documentation](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution), where all endpoints for standard and High throughput campaigns are listed.

   API call examples are also available on [this page](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples).

## Risoluzione dei problemi {#troubleshooting}

### Email delivery delays {#delivery-delays}

If email delivery times exceed expectations, investigate potential outages or performance issues with external services, such as cloud infrastructure providers or email service providers. Journey Optimizer logs record message departure timestamps, which can help determine whether delays occurred downstream in the delivery pipeline.

### Azure cosmos DB authentication errors (500 internal server error) {#cosmosdb-auth-errors}

If you encounter **500 Internal Server Errors** when triggering API-triggered campaigns, and the system logs show a **403 Forbidden** error from Azure Cosmos DB with a message such as:

_&quot;Access to your account is currently revoked because the Azure Cosmos DB service is unable to obtain the AAD authentication token for the account&#39;s default identity&quot;_

This error typically occurs when the Azure service principal required for Cosmos DB authentication has been disabled, deleted, or misconfigured.

+++Come risolvere questo problema

1. **Verificare l&#39;entità servizio Azure**. Verificare che l&#39;entità servizio Azure o l&#39;identità gestita siano abilitate e non siano state disabilitate o eliminate in Azure Active Directory.

1. **Verifica autorizzazioni** - Verifica che l&#39;entità servizio disponga delle autorizzazioni necessarie per accedere alle risorse Azure Key Vault e Cosmos DB. L’entità servizio deve disporre delle assegnazioni di ruolo appropriate per l’autenticazione con Azure Cosmos DB.

1. **Controlla la configurazione della CMK di Azure Cosmos DB**. Se utilizzi le chiavi gestite dal cliente (CMK), consulta la [guida alla risoluzione dei problemi della CMK di Azure Cosmos DB](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"} per i passaggi dettagliati per ripristinare l&#39;acquisizione del token AAD.

1. **Riattiva e verifica** - Dopo aver corretto la configurazione, riattiva l&#39;entità servizio, se è stata disabilitata, e verifica nuovamente le chiamate API della campagna transazionale per verificare che l&#39;autenticazione abbia esito positivo e che i messaggi vengano recapitati.

>[!NOTE]
>
>Questo problema è in genere causato da una configurazione errata o da una disabilitazione accidentale dell’entità principale del servizio Azure richiesta per l’autenticazione Cosmos DB. Se l&#39;entità servizio viene mantenuta abilitata e configurata correttamente, l&#39;errore non si verificherà più.

+++
