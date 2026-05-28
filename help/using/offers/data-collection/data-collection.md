---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Raccolta dati
description: Ulteriori informazioni sulla raccolta di dati di feedback di Gestione delle decisioni
badge: label="Legacy" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Experienced
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-xLnILnYeTkebBswLoIyVxKl61aaOWqX1vp6GaAoG0A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 433
ht-degree: 7%

---

# Raccolta dati di gestione delle decisioni {#data-collection}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)

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
