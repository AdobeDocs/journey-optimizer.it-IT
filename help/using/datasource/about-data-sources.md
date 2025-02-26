---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sulle origini dati
description: Informazioni su come configurare un’origine dati
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: dati, origine, percorso, piattaforma
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 7adee85117a3aad1a347f9f0808b0f32531dc548
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 57%

---

# Informazioni sulle origini dati {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informazioni sulle origini dati"
>abstract="La configurazione dell’origine dati viene sempre eseguita da un utente tecnico. La configurazione dell’origine dati consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive che verranno utilizzate nei percorsi per i seguenti scopi: definizione delle condizioni, dati relativi a parametri e personalizzazione nelle azioni, definizione di attesa personalizzata, impostazione del fuso orario."

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

Per ulteriori informazioni su come configurare un Adobe Experience Platform Data Source e un&#39;origine dati esterna, nonché su come trovare e utilizzare i dati in un percorso, guarda questo [video di esercitazione](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## Video introduttivo {#video}

Scopri cos’è un’origine dati e come configurare le origini dati esterne e di Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

