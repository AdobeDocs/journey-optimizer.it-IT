---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle origini dati
description: Scopri come iniziare a utilizzare le origini dati
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: dati, origine, percorso, piattaforma
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
TQID: https://experienceleague.adobe.com/eG1QcfpHtxpabUt5e7RZiMIpSAJD6Z6bjO-4wtZEUOg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e366af78935405cd5acb15269194875098b20914
workflow-type: tm+mt
source-wordcount: 948
ht-degree: 29%

---

# Introduzione alle origini dati {#about-data-sources}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri le origini dati e come scegliere la strategia di accesso ai dati più adatta per inserire dati aggiuntivi nei tuoi percorsi in termini di condizioni, personalizzazione e tempistica.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informazioni sulle origini dati"
>abstract="La configurazione dell’origine dati viene sempre eseguita da un utente tecnico. La configurazione dell’origine dati consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive, le quali verranno utilizzate nei percorsi. Tali informazioni saranno destinate a: definizione della condizione, dati relativi a parametri e personalizzazione nelle azioni, definizione di attesa personalizzata, impostazione del fuso orario."

>[!TIP]
>La gestione dati in Journey Optimizer è per te una novità? Inizia con la panoramica di [Introduzione alla gestione dei dati](../data/gs-data.md) per comprendere schemi, set di dati, identità e come scorrono i dati prima di configurare le origini dati.

La configurazione dell’origine dati consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive, le quali verranno utilizzate nei percorsi e consentiranno di ottenere:

* [definizione della condizione](../building-journeys/conditions.md)
* Dati dei parametri e di personalizzazione nelle [azioni](../action/action.md).
* [definizione di attesa personalizzata](../building-journeys/wait-activity.md#custom)
* [definizione del fuso orario](../building-journeys/timezone-management.md)

➡️ [Scopri questa funzione nel video](#video)

Questa configurazione non è necessaria se i percorsi sfruttano solo i dati locali provenienti da un payload di eventi. Ad esempio, se il percorso è composto da un evento seguito da un’attività di azione del canale che utilizza solo i dati dell’evento, non è necessario configurare un’origine dati.

Esistono due tipi di origini dati:

* L&#39;origine dati di Adobe Experience Platform **preconfigurata** che definisce la connessione al servizio Profilo cliente in tempo reale. che costituisce un’origine dati incorporata. Consulta [questa pagina](../datasource/adobe-experience-platform-data-source.md).
* Le origini dati **external** che ti consentono di definire una connessione a sistemi esterni. ovvero quelle che puoi creare. Consulta [questa pagina](../datasource/external-data-sources.md).

>[!NOTE]
>
>Poiché le risposte sono ora supportate, per i casi d’uso relativi a origini dati esterne devi utilizzare azioni personalizzate anziché origini dati. Per ulteriori informazioni sulle risposte, consulta questa [sezione](../action/action-response.md)

Per ciascuna origine dati è possibile definire le informazioni da recuperare utilizzando i gruppi di campi. I gruppi di campi costituiscono insiemi di campi che possono essere recuperati da un’origine dati. Consulta [questa pagina](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Le relazioni tra schemi non sono supportate per le origini dati.

## Scegli la tua strategia di accesso ai dati {#data-access-strategy}

Prima di configurare un’origine dati, considera quale approccio si adatta meglio al tuo caso d’uso. Sono disponibili tre opzioni, ciascuna con diversi compromessi in termini di persistenza, arricchimento del profilo e riutilizzabilità. Per informazioni dettagliate su queste opzioni, vedere [Best practice per percorsi avanzati in Journey Optimizer](https://experienceleague.adobe.com/it/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

**Opzione 1: accedere ai dati esterni tramite azioni personalizzate (nessun Data Lake)**

Connettiti direttamente a un’API esterna in fase di esecuzione del percorso senza salvare i dati in modo permanente nel Data Lake di Experience Platform. Più adatto quando:

* I dati sono utili solo all’interno del contesto del percorso e non sono necessari altrove.
* Il sistema esterno è accessibile tramite un endpoint API che restituisce gli attributi necessari.

Ulteriori informazioni sulle [azioni personalizzate](../action/action.md) e sulle [risposte alle azioni personalizzate](../action/action-response.md).

>[!TIP]
>
>Questa opzione è adatta se rispondi **sì** a entrambe le domande:
>* I dati sono utili solo all’interno del contesto del percorso e non sono necessari altrove? Se i dati sono necessari anche per il pubblico o altri canali, considera le opzioni 2 o 3.
>* Il sistema esterno è accessibile tramite un endpoint API che restituisce gli attributi richiesti? In caso contrario, dovrai prima acquisire i dati nel Data Lake.

**Opzione 2: set di dati nel data lake, non abilitato per il profilo**

Acquisisci i dati in un set di dati per attivare e personalizzare i percorsi in base ai dati contestuali dell’evento, senza contribuire al Profilo cliente in tempo reale. Più adatto quando:

* I record contengono un campo di identità utilizzabile per accedere ai profili già memorizzati in Experience Platform.
* I dati non sono necessari per la creazione di tipi di pubblico o per l’unione di identità al di fuori di Journey Optimizer.

>[!TIP]
>
>Questa opzione è adatta se rispondi **sì** a entrambe le domande:
>* I record contengono un campo di identità che può essere utilizzato per accedere ai profili già memorizzati in Experience Platform? In caso contrario, i percorsi non potranno accedere ai profili e distribuirli.
>* I dati NON sono necessari per la creazione di [audience](../audience/about-audiences.md) o per l&#39;unione di identità all&#39;esterno di Journey Optimizer? In caso affermativo, utilizzare l&#39;opzione 3.

**Opzione 3: set di dati abilitato per il profilo nel Data Lake**

Acquisisci i dati in un [set di dati abilitato per il profilo](https://experienceleague.adobe.com/it/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} per creare tipi di pubblico, arricchire i grafici delle identità e sfruttare i dati in più percorsi e destinazioni RT-CDP. Più adatto quando:

* I dati sono utili per le definizioni del pubblico utilizzate nei canali oltre Journey Optimizer.
* I dati contengono più identità che contribuiscono a frammenti di profilo più ricchi e uniti.

>[!CAUTION]
>
>**Prima di abilitare un set di dati per il profilo**, valuta le seguenti aree:
>* **Sincronizzazione dati**: è necessario sincronizzare i database esterni con avvisi per identificare gli errori di acquisizione.
>* **[Guardrail del profilo](https://experienceleague.adobe.com/it/docs/experience-platform/profile/guardrails){target="_blank"}** - I guardrail specifici per il profilo si applicano in aggiunta ai [guardrail generali per l&#39;acquisizione dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/ingestion/guardrails){target="_blank"} per Experience Platform.
>* **Integrità identità**: i dati di identità nei sistemi di origine devono essere pianificati con attenzione per mantenere grafici di identità integri.
>* **Utilizzo del Data Lake**: prima dell&#39;acquisizione è necessario valutare il consumo complessivo di archiviazione, le relazioni tra tabelle e i profili indirizzabili.

| | Dati persistenti nel Data Lake | Set di dati abilitato per il profilo |
| --- | --- | --- |
| **Opzione 1** — Dati esterni tramite azioni personalizzate | No | No |
| **Opzione 2** — Set di dati non abilitato per il profilo | Sì | No |
| **Opzione 3**: set di dati abilitato per il profilo | Sì | Sì |

Per ulteriori informazioni su come configurare un’origine dati di Adobe Experience Platform e un’origine dati esterna, nonché su come individuare e utilizzare i dati all’interno di un percorso, guarda questo [video di esercitazione](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=it){target="_blank"}.

## Video introduttivo {#video}

Scopri cos’è un’origine dati e come configurare le origini dati esterne e di Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

