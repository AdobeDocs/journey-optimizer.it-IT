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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: e08599ea-8888-4294-ba74-3ba0a7762a46id: ed0d8d0e-04b9-4326-be72-a0fbca265377id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
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

* App mobili che utilizzano [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} per eseguire il rendering delle offerte - [Ulteriori informazioni](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
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
