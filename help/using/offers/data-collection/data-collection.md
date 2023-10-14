---
title: Raccolta dati
description: Ulteriori informazioni sulla raccolta di dati di feedback di Gestione delle decisioni
feature: Offers, Datasets
topic: Integrations
role: User
level: Intermediate
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# Raccolta dati di gestione delle decisioni {#data-collection}

## Informazioni sulla raccolta dati

In Adobe Experience Platform puoi raccogliere feedback di offer decisioning, ad esempio quali offerte vengono visualizzate e come gli utenti interagiscono con esse. Questi dati possono essere utilizzati per:
* Composizione [Rapporti di gestione delle decisioni](../reports/get-started-events.md);
* Utilizzo di [quota limite](../offer-library/add-constraints.md#capping) norme;
* Generazione [Modelli IA](../ranking/create-ranking-strategies.md) che possono essere utilizzati come metodo di classificazione.

## Tipi di eventi

La modalità di raccolta dei dati varia a seconda del tipo di evento che si desidera acquisire.

### Eventi decisionali

Ogni volta che la gestione delle decisioni prende una decisione, le informazioni relative a tale evento decisionale sono **automaticamente** inviato a Adobe Experience Platform per tutti i canali. [Ulteriori informazioni](../reports/get-started-events.md)

### Eventi di impression e clic

Le impression e i clic di gestione delle decisioni sono definiti come segue:

* Un **impression** L&#39;evento si verifica quando un&#39;offerta viene visualizzata a un utente.

* A **click** si verifica quando un utente fa clic o interagisce con un’offerta.

Il feedback sulle impression e sui clic viene acquisito a seconda della [!DNL Journey Optimizer] canale utilizzato.

**E-mail** creato da [!DNL Journey Optimizer] **automaticamente** tenere traccia di impression e clic.

Tuttavia, **maggior parte dei canali** richiedere l’invio di impression e dati di clic in Adobe Experience Platform come **evento esperienza**. Ciò include:

* Pagine web che utilizzano [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target="_blank"} per eseguire il rendering delle offerte

* App mobili che utilizzano [SDK di Adobe Experience Platform Mobile](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Chioschi
* Messaggi inviati tramite applicazioni di terze parti
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>I canali che utilizzano una richiesta API di decisioning per ricevere le offerte devono ricevere un feedback inviato come evento esperienza. In altre parole, se l’offerta necessita di istruzioni su come eseguire il rendering, puoi presumere che dovresti inviare un feedback come eventi di esperienza.

### Eventi personalizzati

Il feedback sugli eventi personalizzati associati a un’offerta può essere inviato a Adobe Experience Platform in base alle tue preferenze. Ad esempio, se un’offerta ha più pulsanti, come *Interessato*, *Non interessato*, ecc., potrebbe essere utile inviare tali eventi separatamente, ma possono anche essere inviati come eventi di esperienza.

## Invio di dati di feedback

Per inviare i dati di feedback, devi creare un set di dati per raccogliere gli eventi e, per ogni tipo di evento, definire un evento esperienza da inviare a Adobe Experience Platform.

* Scopri come creare un set di dati in cui raccogliere gli eventi di esperienza in [questa sezione](create-dataset.md).

* Scopri come definire gli eventi di esperienza da inviare ai dati di feedback in [questa sezione](schema-requirement.md).
