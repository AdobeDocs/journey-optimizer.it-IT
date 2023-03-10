---
title: Raccolta dati
description: Ulteriori informazioni sulla raccolta di dati di feedback di Gestione delle decisioni
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 2%

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

1. Da un lato, alcuni canali **automaticamente** tenere traccia di impression e clic. Essi sono i seguenti:

   * E-mail create da [!DNL Journey Optimizer]
   * Notifiche push per dispositivi mobili create da [!DNL Journey Optimizer]
   * App mobili che utilizzano [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o Mobile SDK<!--TBC--> per eseguire il rendering delle offerte <!--need more info + link-->

   >[!NOTE]
   >
   >Se Adobe esegue il rendering dell’offerta visivamente all’utente finale sul canale, puoi presumere che Adobe invierà automaticamente il feedback.

1. D’altra parte, alcuni canali richiedono l’invio di impression e dati di clic in Adobe Experience Platform come **evento esperienza**.

   Eccetto le app mobili che utilizzano [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o Mobile SDK<!--TBC-->, tutti i canali che utilizzano una richiesta API di decisioning per ricevere le offerte necessitano di un feedback inviato come evento esperienza. Ciò include:

   * Pagine web
   * Chioschi
   * Messaggi inviati tramite applicazioni di terze parti

   >[!NOTE]
   >
   >Se l’offerta necessita di istruzioni su come eseguire il rendering, puoi presumere che dovresti inviare un feedback come eventi di esperienza.

### Eventi personalizzati

Il feedback sugli eventi personalizzati associati a un’offerta può essere inviato a Adobe Experience Platform in base alle tue preferenze. Ad esempio, se un’offerta ha più pulsanti, come *Interessato*, *Non interessato*, ecc., potrebbe essere utile inviare tali eventi separatamente, ma possono anche essere inviati come eventi di esperienza. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Invio di dati di feedback

Per inviare i dati di feedback, devi creare un set di dati per raccogliere gli eventi e, per ogni tipo di evento, definire un evento esperienza da inviare a Adobe Experience Platform.

* Scopri come creare un set di dati in cui raccogliere gli eventi di esperienza in [questa sezione](create-dataset.md).

* Scopri come definire gli eventi di esperienza da inviare ai dati di feedback in [questa sezione](schema-requirement.md).

