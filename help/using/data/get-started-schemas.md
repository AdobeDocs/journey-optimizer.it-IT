---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione agli schemi
description: Scopri come utilizzare gli schemi di Adobe Experience Platform in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Engineer, Admin
level: Experienced
keywords: schemi, piattaforma, dati, struttura
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 100%

---

# Introduzione agli schemi {#schemas-gs}

[!DNL Adobe Journey Optimizer] si basa sugli **schemi di Adobe Experience Platform** per descrivere la struttura dei dati in modo coerente e riutilizzabile. Uno schema fornisce una definizione astratta di un oggetto reale (ad esempio una persona) e delinea i dati da includere in ogni istanza di tale oggetto (ad esempio nome, cognome, compleanno e così via). Quando i dati vengono acquisiti in Experience Platform, sono sempre strutturati in base a uno schema **XDM**.

## Schemi basati su modelli e standard

In Adobe Experience Platform sono disponibili due tipi di schemi:

* Gli **schemi standard** sono schemi gerarchici che utilizzano classi e gruppi di campi per acquisire dati di record o di serie temporali.

  Uno schema standard è composto da:

   * Una **classe** (che definisce il comportamento dei dati: record o serie temporale).
   * Uno o più **gruppi di campi** (che aggiungono campi specifici allo schema).

  In Journey Optimizer, gli schemi standard vengono generalmente utilizzati per rappresentare **singole persone e i relativi attributi**, acquisire **interazioni di serie temporali**, quali clic, acquisti o accessi, e alimentare il **profilo cliente in tempo reale** per la segmentazione e la personalizzazione.

  ➡️ [Scopri come creare e configurare uno schema standard in questo video](#video-schema) (video)

* **Gli schemi basati su modelli** sono semplici non gerarchici che non utilizzano classi o gruppi di campi. Vengono utilizzati per acquisire dati record per entità relazionali e, principalmente, nelle [!DNL Journey Optimizer] **campagne orchestrate**.

  Esempi di entità relazionali includono:
   * Prenotazioni, contratti o abbonamenti
   * Prodotti o cataloghi
   * Negozi, sedi o partner

  Con gli schemi basati su modelli, puoi inviare un messaggio per entità (ad esempio, per prenotazioni, iscrizioni), creare segmenti basati sugli attributi di entità (ad esempio, categoria di prodotto, posizione del negozio) e migliorare l’indirizzabilità raggiungendo tutti i contatti collegati a un’entità.

  Funzionamento degli schemi basati su modelli:

   1. **Creare gli schemi manualmente o importarli tramite DDL**
   1. **Collega gli schemi** per definire le relazioni tra entità e persone (ad esempio, transazioni di fidelizzazione collegate ai membri, premi collegati ai brand).
   1. **Acquisisci i dati** nel set di dati da origini supportate.

  ➡️ [Scopri come gestire schemi e set di dati basati su modelli](../orchestrated/gs-schemas.md)
➡️ [Introduzione alle campagne orchestrate](../orchestrated/gs-schemas.md)

## Video dimostrativo{#video-schema}

Scopri come creare uno schema standard, aggiungere gruppi di campi, creare e configurare gruppi di campi personalizzati.

>[!VIDEO](https://video.tv.adobe.com/v/3416871?captions=ita&quality=12)

>[!MORELIKETHIS]
>
>* [Creare uno schema, un set di dati e acquisire dati per aggiungere profili di test in Journey Optimizer](../audience/creating-test-profiles.md)
>* [Panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}
>* [Best practice per la modellazione dati](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=it){target="_blank"}
>* [Creare uno schema tramite l’API del registro degli schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=it){target="_blank"}
>* [Definire una relazione tra due schemi utilizzando l’editor di schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=it){target="_blank"}
