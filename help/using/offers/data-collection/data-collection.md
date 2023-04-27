---
title: Raccolta dati
description: Ulteriori informazioni sulla raccolta dati di feedback di Gestione delle decisioni
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# Raccolta dati di gestione delle decisioni {#data-collection}

## Informazioni sulla raccolta dati

Puoi raccogliere un feedback di offer decisioning in Adobe Experience Platform, tra cui quali offerte vengono visualizzate e come gli utenti interagiscono con esse. Questi dati possono essere utilizzati per:
* Composizione [Relazioni sulla gestione delle decisioni](../reports/get-started-events.md);
* Utilizzo [limite di frequenza](../offer-library/add-constraints.md#capping) norme;
* Costruzione [Modelli AI](../ranking/create-ranking-strategies.md) che può essere utilizzato come metodo di classificazione.

## Tipi di eventi

La modalità di raccolta dei dati varia a seconda del tipo di evento che si desidera acquisire.

### Eventi decisionali

Ogni volta che la direzione decisionale prende una decisione, le informazioni relative a tale evento decisionale sono **automaticamente** inviati a Adobe Experience Platform per tutti i canali. [Ulteriori informazioni](../reports/get-started-events.md)

### Eventi di impression e clic

Le impression e i clic della gestione delle decisioni sono definiti come segue:

* Un **impression** si verifica quando un&#39;offerta viene visualizzata a un utente.

* A **click** si verifica quando un utente fa clic o interagisce con un&#39;offerta.

Il feedback sulle impression e sui clic viene acquisito a seconda del [!DNL Journey Optimizer] canale utilizzato.

**E-mail** creato da [!DNL Journey Optimizer] **automaticamente** tenere traccia di impression e clic.

Tuttavia, **maggior parte dei canali** richiedere l’invio di dati relativi a impression e clic in Adobe Experience Platform as a **evento esperienza**. Ciò include:

* Pagine web che utilizzano [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target="_blank"} rendering delle offerte

* App per dispositivi mobili che utilizzano [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Chioschi
* Messaggi inviati tramite applicazioni di terze parti
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>I canali che utilizzano una richiesta API decisionale per ricevere le offerte devono ricevere un feedback inviato come evento di esperienza. In altre parole, se l’offerta richiede istruzioni su come eseguire il rendering, puoi presumere di dover inviare un feedback come eventi di esperienza.

### Eventi personalizzati

Puoi inviare un feedback sugli eventi personalizzati legati a un’offerta in Adobe Experience Platform in base alle tue preferenze. Ad esempio, se un’offerta include più pulsanti, come *Interessato*, *Non interessato*, ecc., potresti voler inviare separatamente tali eventi, ma questi possono anche essere inviati come eventi di esperienza.

## Invio di dati di feedback

Per inviare i dati di feedback, devi creare un set di dati per raccogliere gli eventi e, per ciascun tipo di evento, definire un evento di esperienza che verrà inviato in Adobe Experience Platform.

* Scopri come creare un set di dati in cui verranno raccolti gli eventi di esperienza in [questa sezione](create-dataset.md).

* Scopri come definire gli eventi di esperienza in cui inviare i dati di feedback in [questa sezione](schema-requirement.md).
