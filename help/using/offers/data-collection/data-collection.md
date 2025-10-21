---
title: Raccolta dati
description: Ulteriori informazioni sulla raccolta di dati di feedback di Gestione delle decisioni
badge: label="Legacy" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Experienced
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%

---

# Raccolta dati di gestione delle decisioni {#data-collection}

## Informazioni sulla raccolta dati

Puoi raccogliere in Adobe Experience Platform i feedback su Offer Decisioning, tra cui le offerte visualizzate e il modo in cui gli utenti interagiscono con esse. Questi dati possono essere utilizzati per:

* Composizione di [report di gestione delle decisioni](../reports/get-started-events.md);
* Utilizzo di [regole di quota limite](../offer-library/add-constraints.md#capping);
* Creazione di [modelli AI](../ranking/create-ranking-strategies.md) che possono essere utilizzati come metodo di classificazione.

## Tipi di eventi

La modalità di raccolta dei dati varia a seconda del tipo di evento che si desidera acquisire.

### Eventi decisionali

Ogni volta che la gestione delle decisioni prende una decisione, le informazioni relative a tale evento decisionale vengono **inviate automaticamente** a Adobe Experience Platform per tutti i canali. [Ulteriori informazioni](../reports/get-started-events.md)

### Eventi di impression e clic

Le impression e i clic di gestione delle decisioni sono definiti come segue:

* Un evento **impression** si verifica quando un&#39;offerta viene visualizzata a un utente.

* Un evento **click** si verifica quando un utente fa clic o interagisce con un&#39;offerta.

Il feedback sulle impression e sui clic viene acquisito a seconda del canale [!DNL Journey Optimizer] utilizzato.

**E-mail** create da [!DNL Journey Optimizer] **automaticamente** tieni traccia di impression e clic.

Tuttavia, **la maggior parte dei canali** richiede l&#39;invio di impression e dati di clic in Adobe Experience Platform come **evento esperienza**. Ciò include:

* Pagine Web che utilizzano [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target="_blank"} per eseguire il rendering delle offerte

* App mobili che utilizzano [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=it){target="_blank"} per eseguire il rendering delle offerte - [Ulteriori informazioni](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Chioschi
* Messaggi inviati tramite applicazioni di terze parti
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>I canali che utilizzano una richiesta API di decisioning per ricevere le offerte devono ricevere un feedback inviato come evento esperienza. In altre parole, se l’offerta necessita di istruzioni su come eseguire il rendering, puoi presumere che dovresti inviare un feedback come eventi di esperienza.

### Eventi personalizzati

Il feedback sugli eventi personalizzati associati a un’offerta può essere inviato a Adobe Experience Platform in base alle tue preferenze. Ad esempio, se un&#39;offerta ha più pulsanti come *Interessato*, *Non interessato*, ecc., è possibile inviare tali eventi separatamente, ma è anche possibile inviarli come eventi di esperienza.

## Invio di dati di feedback

Per inviare i dati di feedback, devi creare un set di dati per raccogliere gli eventi e, per ogni tipo di evento, definire un evento esperienza da inviare a Adobe Experience Platform.

* Scopri come creare un set di dati in cui gli eventi esperienza verranno raccolti in [questa sezione](create-dataset.md).

* Scopri come definire gli eventi esperienza da inviare ai dati di feedback in [questa sezione](schema-requirement.md).
