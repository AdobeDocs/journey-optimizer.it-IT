---
solution: Journey Optimizer
product: journey optimizer
title: Rivedere e attivare una campagna
description: Scopri come rivedere e attivare le campagne in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campagna, revisione, convalida, attivazione, attivazione, ottimizzatore
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
TQID: https://experienceleague.adobe.com/Q9UQEnAqQNFD869w4lQOQxcbH82SwDZyT8Q-9RvRD5k
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 551
ht-degree: 1%

---

# Eseguire una campagna attivata da API {#execute}

Una volta attivata la campagna, devi recuperare la richiesta cURL di esempio generata e utilizzarla nell’API per generare il payload e attivare la campagna.

## Da leggere {#must-read}

* **Date di inizio/fine campagna** - Se hai configurato una data di inizio e/o fine specifica durante la creazione della campagna, questa non verrà eseguita oltre queste date e le chiamate API avranno esito negativo.

* **Timeout chiamata** - Il timeout della chiamata all&#39;API REST di esecuzione messaggi interattiva è di 60 secondi. Tuttavia, in caso di timeout imprevisti per garantire la consegna, sono presenti nuovi tentativi interni.

## Attivare la campagna {#trigger}

1. Apri la campagna, quindi copia e incolla la richiesta di payload dalla sezione **[!UICONTROL richiesta cURL]**. Questo payload include tutte le variabili di personalizzazione (profilo e contesto) utilizzate nel messaggio. È disponibile una volta che la campagna è in diretta.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >Gli endpoint nella sezione cURL differiscono tra le campagne standard e le [campagne con throughput elevato](../campaigns/api-triggered-high-throughput.md).

1. Utilizza questa richiesta cURL nelle API per generare il payload e attivare la campagna. Per ulteriori informazioni, consulta la [documentazione dell&#39;API di esecuzione interattiva dei messaggi](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution), in cui sono elencati tutti gli endpoint per le campagne Standard e High Throughput.

   Gli esempi di chiamate API sono disponibili anche in [questa pagina](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples).

## Risoluzione dei problemi {#troubleshooting}

### Ritardi nella consegna delle e-mail {#delivery-delays}

Se i tempi di consegna delle e-mail superano le aspettative, esamina potenziali interruzioni o problemi di prestazioni con i servizi esterni, come i provider di infrastrutture cloud o di servizi e-mail. I registri di Journey Optimizer registrano i timestamp di partenza del messaggio, che possono aiutare a determinare se si sono verificati ritardi a valle nella pipeline di consegna.

### Errori di autenticazione di Azure cosmos DB (errore 500 interno del server) {#cosmosdb-auth-errors}

Se rilevi **500 errori interni del server** durante l&#39;attivazione di campagne attivate da API e i registri di sistema mostrano un errore **403 Forbidden** da Azure Cosmos DB con un messaggio di tipo:

_&quot;L&#39;accesso al tuo account è attualmente revocato perché il servizio Azure Cosmos DB non è in grado di ottenere il token di autenticazione AAD per l&#39;identità predefinita dell&#39;account&quot;_

Questo errore si verifica in genere quando l’entità principale del servizio Azure richiesta per l’autenticazione Cosmos DB è stata disabilitata, eliminata o non configurata correttamente.

+++Come risolvere questo problema

1. **Verificare l&#39;entità servizio Azure**. Verificare che l&#39;entità servizio Azure o l&#39;identità gestita siano abilitate e non siano state disabilitate o eliminate in Azure Active Directory.

1. **Verifica autorizzazioni** - Verifica che l&#39;entità servizio disponga delle autorizzazioni necessarie per accedere alle risorse Azure Key Vault e Cosmos DB. L’entità servizio deve disporre delle assegnazioni di ruolo appropriate per l’autenticazione con Azure Cosmos DB.

1. **Controlla la configurazione della CMK di Azure Cosmos DB**. Se utilizzi le chiavi gestite dal cliente (CMK), consulta la [guida alla risoluzione dei problemi della CMK di Azure Cosmos DB](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"} per i passaggi dettagliati per ripristinare l&#39;acquisizione del token AAD.

1. **Riattiva e verifica** - Dopo aver corretto la configurazione, riattiva l&#39;entità servizio, se è stata disabilitata, e verifica nuovamente le chiamate API della campagna transazionale per verificare che l&#39;autenticazione abbia esito positivo e che i messaggi vengano recapitati.

>[!NOTE]
>
>Questo problema è in genere causato da una configurazione errata o da una disabilitazione accidentale dell’entità principale del servizio Azure richiesta per l’autenticazione Cosmos DB. Se l&#39;entità servizio viene mantenuta abilitata e configurata correttamente, l&#39;errore non si verificherà più.

+++
