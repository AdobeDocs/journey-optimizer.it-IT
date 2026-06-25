---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione agli schemi
description: Scopri come utilizzare gli schemi di Adobe Experience Platform in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: schemi, piattaforma, dati, struttura
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
TQID: https://experienceleague.adobe.com/fWsW9Rvyd8L4nphczzc7GF1rbO7HuYsjqDBBpy3uoGU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 79b0c44fffb4297a9a5675200f086c5de544ec88
workflow-type: tm+mt
source-wordcount: 609
ht-degree: 78%

---

# Introduzione agli schemi {#schemas-gs}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come gli schemi standard e relazionali di Adobe Experience Platform definiscono la struttura dei tuoi dati, consentendoti di modellare profili, eventi comportamentali ed entità relazionali per la personalizzazione e le campagne orchestrate in Adobe Journey Optimizer.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] si basa sugli **schemi di Adobe Experience Platform** per descrivere la struttura dei dati in modo coerente e riutilizzabile. Uno schema fornisce una definizione astratta di un oggetto reale (ad esempio una persona) e delinea i dati da includere in ogni istanza di tale oggetto (ad esempio nome, cognome, compleanno e così via). Quando i dati vengono acquisiti in Experience Platform, sono sempre strutturati in base a uno schema **XDM**.

## Schemi relazionali e standard

In Adobe Experience Platform sono disponibili due tipi di schemi:

* Gli **schemi standard** sono schemi gerarchici che utilizzano classi e gruppi di campi per acquisire dati di record o di serie temporali.

  Uno schema standard è composto da:

   * Una **classe** (che definisce il comportamento dei dati: record o serie temporale).
   * Uno o più **gruppi di campi** (che aggiungono campi specifici allo schema).

  In Journey Optimizer, gli schemi standard vengono generalmente utilizzati per rappresentare **singole persone e i relativi attributi**, acquisire **interazioni di serie temporali**, quali clic, acquisti o accessi, e alimentare il **profilo cliente in tempo reale** per la segmentazione e la personalizzazione.

  ➡️ [Scopri come creare e configurare uno schema standard in questo video](#video-schema) (video)

* **Gli schemi relazionali** sono schemi semplici non gerarchici che non utilizzano classi o gruppi di campi. Vengono utilizzati per acquisire dati record per entità relazionali e, principalmente, nelle [!DNL Journey Optimizer] **campagne orchestrate**.

  Esempi di entità relazionali includono:
   * Prenotazioni, contratti o abbonamenti
   * Prodotti o cataloghi
   * Negozi, sedi o partner

  Con gli schemi relazionali, puoi inviare un messaggio per entità (ad esempio, per prenotazione, per iscrizione), creare segmenti basati sugli attributi di entità (ad esempio, categoria di prodotto, sede del negozio) e migliorare l’indirizzabilità raggiungendo tutti i contatti collegati a un’entità.

  Funzionamento degli schemi relazionali:

   1. **Creare gli schemi manualmente o importarli tramite DDL**
   1. **Collega gli schemi** per definire le relazioni tra entità e persone (ad esempio, transazioni di fidelizzazione collegate ai membri, premi collegati ai brand).
   1. **Acquisisci i dati** nel set di dati da origini supportate.

  ➡️ [Scopri come gestire set di dati e schemi relazionali](../orchestrated/gs-schemas.md)
➡️ [Introduzione alle campagne orchestrate](../orchestrated/gs-schemas.md)

>[!IMPORTANT]
>
>L’abilitazione di uno schema per Real-Time Customer Profile è una decisione permanente: una volta abilitato, lo schema non può essere disabilitato o eliminato. I set di dati basati su tale schema possono essere disabilitati o eliminati separatamente, ma in questo modo vengono rimossi i record di profilo associati e possono influenzare la segmentazione e i flussi di lavoro di attivazione. Prima dell’abilitazione, completa la configurazione dell’identità e la selezione del gruppo di campi. Per istruzioni dettagliate, consulta [Pianificazione dell&#39;abilitazione del profilo](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"} e [Gestione degli schemi abilitati per il profilo](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"} nella documentazione di Adobe Experience Platform.

## Video dimostrativo{#video-schema}

Scopri come creare uno schema standard, aggiungere gruppi di campi, creare e configurare gruppi di campi personalizzati.

>[!VIDEO](https://video.tv.adobe.com/v/3416871?captions=ita&quality=12)

>[!MORELIKETHIS]
>
>* [Introduzione alla gestione dei dati in Journey Optimizer](gs-data.md)
>* [Creare uno schema, un set di dati e acquisire dati per aggiungere profili di test in Journey Optimizer](../audience/creating-test-profiles.md)
>* [Panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}
>* [Best practice per la modellazione dati](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=it){target="_blank"}
>* [Pianificazione abilitazione profilo](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"}
>* [Gestione degli schemi abilitati per il profilo](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"}
>* [Creare uno schema tramite l’API del registro degli schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=it){target="_blank"}
>* [Definire una relazione tra due schemi utilizzando l’editor di schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=it){target="_blank"}
