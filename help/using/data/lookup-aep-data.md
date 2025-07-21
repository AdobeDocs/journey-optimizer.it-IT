---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare i dati di Adobe Experience Platform (Beta)
description: Scopri come utilizzare i set di dati di Adobe Experience Platform nelle funzionalità di  [!DNL Journey Optimizer] decisioning e personalizzazione.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: bd1274a5547f4ea835fc258f280c1efc667b6780
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 6%

---

# Utilizzare i dati di Adobe Experience Platform {#aep-data}

>[!CONTEXTUALHELP]
>id="lookup-aep-data"
>title="Abilita per ricerca"
>abstract="Abilita per ricerca"

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile per tutti i clienti come versione beta pubblica.
>
>Per utilizzare questa funzionalità, devi prima accettare i termini beta per la tua organizzazione.

Journey Optimizer consente di sfruttare i dati di Adobe Experience Platform in [!DNL Journey Optimizer]. A questo scopo, i set di dati necessari per la personalizzazione della ricerca devono prima essere abilitati tramite una chiamata API come descritto di seguito. Al termine, puoi utilizzare i loro dati con le funzionalità di personalizzazione e decisioning di [!DNL Journey Optimizer].

## Restrizioni e linee guida di Beta {#guidelines}

Prima di iniziare, rivedi le seguenti restrizioni e linee guida:

* **La dimensione del set di dati** è limitata a 5 GB per i set di dati di produzione e a 1 GB per i set di dati sandbox di sviluppo
* **È possibile abilitare un massimo di 50 set di dati** per la ricerca per organizzazione in qualsiasi momento.
* **Il numero di record** è limitato a 5 milioni nei set di dati di produzione e a 1 milione nei set di dati sandbox di sviluppo.
* **L&#39;etichettatura e l&#39;applicazione dell&#39;utilizzo dati** non sono attualmente applicate per i set di dati abilitati per la ricerca.
* **I set di dati abilitati per la ricerca e utilizzati nella personalizzazione non sono protetti dall&#39;eliminazione**. Spetta a te tenere traccia dei set di dati utilizzati per la personalizzazione per assicurarti che non vengano eliminati o rimossi.

## Abilitare un set di dati per la ricerca di dati {#enable}

Per sfruttare i dati del set di dati per la personalizzazione, devi utilizzare una chiamata API per recuperarne lo stato e abilitare il servizio di ricerca.

### Prerequisiti {#prerequisites-enable}

* Segui le istruzioni descritte in [questa documentazione](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) per configurare l&#39;ambiente per l&#39;invio di comandi API.
* Il progetto dello sviluppatore deve includere le API Adobe Journey Optimizer e Adobe Experience Platform aggiunte al progetto.

  ![](assets/aep-data-api.png)

* Come parte del tuo ruolo, devi disporre dell’autorizzazione Gestione set di dati.
* Lo schema su cui si basa il set di dati deve contenere una **identità primaria** che può fungere da chiave di ricerca.

### Struttura delle chiamate API {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

Dove:

* **URL** è `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **ID set di dati** è il set di dati per il quale si desidera abilitare.
* **L&#39;azione** è abilitata O disabilitata.
* **Il token di accesso** può essere recuperato dalla console per sviluppatori.
* È possibile recuperare **la chiave API** dalla console per sviluppatori.
* **ID organizzazione IMS** è la tua organizzazione Adobe.
* **Nome sandbox** è il nome della sandbox in cui si trova il set di dati (ad esempio, prod, dev, ecc.).

>[!NOTE]
>
>Se riscontri l’errore seguente quando tenti una chiamata API per abilitare i set di dati, prova a rimuovere le API Adobe Journey Optimizer dal progetto della console per sviluppatori e quindi a aggiungerle nuovamente.
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

Dopo aver abilitato un set di dati per la ricerca tramite una chiamata API, puoi utilizzarne i dati con le funzionalità di personalizzazione e decisioning di [!DNL Journey Optimizer].

* [Utilizzare i dati di Adobe Experience Platform per la personalizzazione](../personalization/aep-data-perso.md)
* [Utilizzare i dati di Adobe Experience Platform per la funzione Decisioni](../experience-decisioning/aep-data-exd.md)
