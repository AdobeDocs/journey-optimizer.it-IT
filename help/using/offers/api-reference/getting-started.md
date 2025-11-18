---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introduzione
description: Scopri come iniziare a utilizzare l’API della Libreria di offerte per eseguire operazioni chiave utilizzando il motore decisionale.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: ht
source-wordcount: '382'
ht-degree: 100%

---

# API per la gestione delle decisioni - Guida per sviluppatori  {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="Nuove API di gestione delle decisioni"
>abstract="Sono ora disponibili nuove API per la creazione e la gestione di oggetti di gestione delle decisioni. Le API legacy saranno supportate fino al 27/03/2024."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="Nuove API di gestione delle decisioni"
>abstract="Sono ora disponibili nuove API per la creazione e la gestione di oggetti di gestione delle decisioni. Le API legacy saranno supportate fino al 27/03/2024."

Questa guida per sviluppatori descrive i passaggi per iniziare a utilizzare l’API di [!DNL Offer Library]. La guida fornisce quindi esempi di chiamate API per eseguire operazioni chiave utilizzando il motore decisionale.

➡️ [Ulteriori informazioni sui componenti della Gestione delle decisioni sono disponibili questo video](#video)

## Prerequisiti {#prerequisites}

Questa guida richiede una buona conoscenza dei seguenti componenti di Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}: il framework standardizzato tramite cui [!DNL Experience Platform] organizza i dati sull’esperienza cliente.
   * [Nozioni di base sulla composizione degli schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it){target="_blank"}: scopri i blocchi predefiniti di base degli schemi XDM.
* [Gestione delle decisioni](../../../using/offers/get-started/starting-offer-decisioning.md): illustra i concetti e i componenti utilizzati per la funzione Decisioni in generale e per la gestione delle decisioni in particolare. Illustra le strategie utilizzate per scegliere l’opzione migliore da presentare durante l’esperienza cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=it){target="_blank"}: PQL è un potente linguaggio per la scrittura delle espressioni sulle istanze XDM. PQL viene utilizzato per definire le regole di decisione.

## Lettura delle chiamate API di esempio {#reading-sample-api-calls}

Questa guida fornisce esempi di chiamate API per illustrare come formattare le richieste. Questi includono percorsi, intestazioni richieste e payload di richieste formattati correttamente. Viene inoltre fornito un codice JSON di esempio restituito nelle risposte API. Per informazioni sulle convenzioni utilizzate nella documentazione per le chiamate API di esempio, consulta la sezione su [come leggere gli esempi di chiamate API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=it#how-do-i-format-an-api-request){target="_blank"} nella guida alla risoluzione dei problemi di [!DNL Experience Platform].

## Raccogliere i valori per le intestazioni richieste {#gather-values-for-required-headers}

Per effettuare chiamate alle API di [!DNL Adobe Experience Platform], prima è necessario completare il [tutorial sull’autenticazione](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=it){target="_blank"}. Completando il tutorial sull’autenticazione si ottengono i valori per ciascuna delle intestazioni richieste in tutte le chiamate API di [!DNL Experience Platform], come mostrato di seguito:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Tutte le richieste che contengono un payload (POST, PUT, PATCH) richiedono un’intestazione aggiuntiva:

* `Content-Type: application/json`

>[!NOTE]
>
>I controlli delle autorizzazioni vengono applicati in base ai profili di prodotto assegnati. Solo le autorizzazioni concesse nel profilo di prodotto associato determinano le risorse accessibili o gestibili tramite l’API.

## Passaggi successivi {#next-steps}

Questo documento tratta le conoscenze preliminari necessarie per effettuare chiamate alle API di [!DNL Offer Library]. Ora puoi passare alle chiamate di esempio fornite in questa guida per sviluppatori e seguire le relative istruzioni.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

<!-- ## How-to video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12) -->

