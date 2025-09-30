---
solution: Journey Optimizer
product: journey optimizer
title: Definire il pubblico della campagna attivata dall’API
description: Scopri come definire il pubblico della campagna attivata da API.
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: 6dda5687-3742-4e88-be7c-c4969b183161
source-git-commit: be07b0dfec31d23f741bfc2a9f89fe1a7891ef0b
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 2%

---

# Definire il pubblico della campagna attivata dall’API {#api-audience}

Utilizza la scheda **[!UICONTROL Pubblico]** per definire il pubblico della campagna.

![](assets/campaign-audience.png)

## Selezionare il pubblico

**Per le campagne attivate dall&#39;API di marketing**, fai clic sul pulsante **[!UICONTROL Seleziona pubblico]** per visualizzare l&#39;elenco dei tipi di pubblico di Adobe Experience Platform disponibili. [Ulteriori informazioni sui tipi di pubblico](../audience/about-audiences.md).

>[!IMPORTANT]
>
>L&#39;utilizzo dei tipi di pubblico e degli attributi di [composizione del pubblico](../audience/get-started-audience-orchestration.md) non è attualmente disponibile per l&#39;utilizzo con Healthcare Shield o Privacy and Security Shield.

**Per le campagne attivate dall&#39;API transazionale**, i profili target devono essere definiti nella chiamata API. Una singola chiamata API supporta fino a 20 destinatari univoci. Ogni destinatario deve avere un ID utente univoco; gli ID utente duplicati non sono consentiti. Ulteriori informazioni sono disponibili nella [documentazione dell&#39;API di esecuzione interattiva dei messaggi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}

## Seleziona il tipo di identità

Nel campo **[!UICONTROL Tipo di identità]**, scegli il tipo di chiave da utilizzare per identificare i singoli utenti del pubblico selezionato. Puoi utilizzare un tipo di identità esistente o crearne uno nuovo utilizzando il servizio Adobe Experience Platform Identity. Gli spazi dei nomi di identità standard sono elencati in [questa pagina](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

È consentito un solo tipo di identità per campagna. Gli individui appartenenti a un segmento che non ha il tipo di identità selezionato tra le loro diverse identità non possono essere targetizzati dalla campagna. Ulteriori informazioni sui tipi di identità e sugli spazi dei nomi sono disponibili nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=it){target="_blank"}.

## Attivare la creazione del profilo all’esecuzione della campagna

In alcuni casi, potrebbe essere necessario inviare messaggi transazionali a profili che non esistono nel sistema. Ad esempio, se un utente sconosciuto tenta di reimpostare la password sul sito web. Se nel database non esiste un profilo, Journey Optimizer ti consente di crearlo automaticamente durante l’esecuzione della campagna per consentire l’invio del messaggio a questo profilo.

Per attivare la creazione del profilo durante l&#39;esecuzione della campagna, attiva l&#39;opzione **[!UICONTROL Crea nuovi profili]**. Se questa opzione è disabilitata, i profili sconosciuti verranno rifiutati per qualsiasi invio e la chiamata API avrà esito negativo.

![](assets/api-triggered-create-profile.png)

>[!IMPORTANT]
>
>Questa opzione viene fornita per **la creazione di profili di volumi molto piccoli** in un caso di utilizzo di invio transazionale di volumi elevati, con la maggior parte dei profili già esistenti in Platform.
>
>I profili sconosciuti vengono creati nel set di dati del profilo di messaggistica interattiva **AJO**, in tre spazi dei nomi predefiniti (e-mail, telefono e ECID) rispettivamente per ogni canale in uscita (e-mail, SMS e push). Tuttavia, se utilizzi uno spazio dei nomi personalizzato, l’identità viene creata con lo stesso spazio dei nomi personalizzato.

## Webhook SMS {#webhook}

Per le campagne attivate dall’API transazionale, puoi abilitare i webhook per ricevere feedback in tempo reale sullo stato di esecuzione dei messaggi. A tale scopo, attiva l&#39;opzione **[!UICONTROL Abilita webhook]** per inviare eventi di stato di consegna a un webhook configurato.

![](assets/api-triggered-webhook.png)

Le configurazioni del webhook vengono gestite centralmente nel menu **[!UICONTROL Amministrazione]** / **[!UICONTROL Canali]** / **[!UICONTROL Feedback del webhook]**. Da qui, gli amministratori possono creare e modificare gli endpoint del webhook. [Scopri come creare webhook di feedback](../configuration/feedback-webhooks.md)

## Passaggi successivi {#next}

Una volta che la configurazione e il contenuto della campagna sono pronti, puoi pianificarne l’esecuzione. [Ulteriori informazioni](api-triggered-campaign-schedule.md)
