---
title: Introduzione
description: Scopri come iniziare a utilizzare l’API della Libreria di offerte per eseguire operazioni chiave utilizzando il motore decisionale.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 4f2bbef98b2e529c2f6a663a3cf7e1ad5493c41a
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 7%

---

# Guida per gli sviluppatori API per la gestione delle decisioni {#decision-management-api-developer-guide}

Questa guida per sviluppatori descrive i passaggi per iniziare a utilizzare [!DNL Offer Library] API. La guida fornisce quindi esempi di chiamate API per eseguire operazioni chiave utilizzando il motore decisionale.

➡️ [Ulteriori informazioni sui componenti di Gestione delle decisioni sono disponibili in questo video](#video)

## Prerequisiti {#prerequisites}

Questa guida richiede una buona conoscenza dei seguenti componenti di Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}: il quadro standardizzato mediante il quale [!DNL Experience Platform] organizza i dati sull’esperienza del cliente.
   * [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it){target="_blank"}: scopri gli elementi di base degli schemi XDM.
* [Gestione delle decisioni](../../../using/offers/get-started/starting-offer-decisioning.md): illustra i concetti e i componenti utilizzati per Experience Decisioning in generale e per la gestione delle decisioni in particolare. Illustra le strategie utilizzate per scegliere l’opzione migliore da presentare durante l’esperienza di un cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: PQL è un linguaggio potente per scrivere espressioni sulle istanze XDM. PQL viene utilizzato per definire le regole di decisione.

## Lettura delle chiamate API di esempio {#reading-sample-api-calls}

Questa guida fornisce esempi di chiamate API per dimostrare come formattare le richieste. Questi includono percorsi, intestazioni richieste e payload di richieste formattati correttamente. Viene inoltre fornito il codice JSON di esempio restituito nelle risposte API. Per informazioni sulle convenzioni utilizzate nella documentazione per le chiamate API di esempio, consulta la sezione su [come leggere esempi di chiamate API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} nel [!DNL Experience Platform] guida alla risoluzione dei problemi.

## Raccogli i valori per le intestazioni richieste {#gather-values-for-required-headers}

Per effettuare chiamate a [!DNL Adobe Experience Platform] , devi prima completare le [tutorial sull’autenticazione](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=it){target="_blank"}. Il completamento del tutorial sull’autenticazione fornisce i valori per ciascuna delle intestazioni richieste in tutte [!DNL Experience Platform] Chiamate API, come mostrato di seguito:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Tutte le richieste che contengono un payload (POST, PUT, PATCH) richiedono un’intestazione aggiuntiva:

* `Content-Type: application/json`

## Passaggi successivi {#next-steps}

In questo documento sono state trattate le conoscenze preliminari necessarie per effettuare chiamate [!DNL Offer Library] API. Ora puoi passare alle chiamate di esempio fornite in questa guida per sviluppatori e seguire le loro istruzioni.

## Video introduttivo {#video}

Il video seguente ha lo scopo di aiutarti a comprendere i componenti di Gestione delle decisioni.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

