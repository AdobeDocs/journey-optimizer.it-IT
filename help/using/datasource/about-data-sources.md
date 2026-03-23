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
source-git-commit: 36f8224b33411f23f23985c55bdb6cebbcdf5712
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 37%

---

# Introduzione alle origini dati {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informazioni sulle origini dati"
>abstract="La configurazione dell’origine dati viene sempre eseguita da un utente tecnico. La configurazione dell’origine dati consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive, le quali verranno utilizzate nei percorsi. Tali informazioni saranno destinate a: definizione della condizione, dati relativi a parametri e personalizzazione nelle azioni, definizione di attesa personalizzata, impostazione del fuso orario."

La configurazione dell’origine dati consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive, le quali verranno utilizzate nei percorsi e consentiranno di ottenere:

* [definizione della condizione](../building-journeys/condition-activity.md)
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

Prima di configurare un’origine dati, considera quale approccio si adatta meglio al tuo caso d’uso. Sono disponibili tre opzioni, ciascuna con diversi compromessi in termini di persistenza, arricchimento del profilo e riutilizzabilità. Per informazioni dettagliate su queste opzioni, vedere [Best practice per percorsi avanzati in Journey Optimizer](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

**Opzione 1: accedere ai dati esterni tramite azioni personalizzate (nessun Data Lake)**

Connettiti direttamente a un’API esterna in fase di esecuzione del percorso senza salvare i dati in modo permanente nel Data Lake di Experience Platform. Più adatto quando:

* I dati sono utili solo all’interno del contesto del percorso e non sono necessari altrove.
* Il sistema esterno è accessibile tramite un endpoint API che restituisce gli attributi necessari.

Ulteriori informazioni sulle [azioni personalizzate](../action/action.md) e sulle [risposte alle azioni personalizzate](../action/action-response.md).

**Opzione 2: set di dati nel data lake, non abilitato per il profilo**

Acquisisci i dati in un set di dati per attivare e personalizzare i percorsi in base ai dati contestuali dell’evento, senza contribuire al Profilo cliente in tempo reale. Più adatto quando:

* I record contengono un campo di identità utilizzabile per accedere ai profili già memorizzati in Experience Platform.
* I dati non sono necessari per la creazione di tipi di pubblico o per l’unione di identità al di fuori di Journey Optimizer.

**Opzione 3: set di dati abilitato per il profilo nel Data Lake**

Acquisisci i dati in un [set di dati abilitato per il profilo](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} per creare tipi di pubblico, arricchire i grafici delle identità e sfruttare i dati in più percorsi e destinazioni RT-CDP. Più adatto quando:

* I dati sono utili per le definizioni del pubblico utilizzate nei canali oltre Journey Optimizer.
* I dati contengono più identità che contribuiscono a frammenti di profilo più ricchi e uniti.

| | Dati persistenti nel Data Lake | Set di dati abilitato per il profilo |
| --- | --- | --- |
| **Opzione 1** — Dati esterni tramite azioni personalizzate | No | No |
| **Opzione 2** — Set di dati non abilitato per il profilo | Sì | No |
| **Opzione 3**: set di dati abilitato per il profilo | Sì | Sì |

Per ulteriori informazioni su come configurare un’origine dati di Adobe Experience Platform e un’origine dati esterna, nonché su come individuare e utilizzare i dati all’interno di un percorso, guarda questo [video di esercitazione](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## Video introduttivo {#video}

Scopri cos’è un’origine dati e come configurare le origini dati esterne e di Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

