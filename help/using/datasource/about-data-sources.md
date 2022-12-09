---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sulle origini dati
description: Scopri come configurare un’origine dati
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Informazioni sulle origini dati {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informazioni sulle origini dati"
>abstract="La configurazione dell’origine dati viene sempre eseguita da un utente tecnico. La configurazione dell’origine dati ti consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive, che verranno utilizzate nei percorsi, al fine di: definizione della condizione, dati di parametro e personalizzazione nelle azioni, definizione di attesa personalizzata, definizione del fuso orario."

La configurazione dell’origine dati ti consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive, che verranno utilizzate nei percorsi, al fine di:

* [definizione della condizione](../building-journeys/condition-activity.md)
* dati dei parametri e della personalizzazione in [azioni](../action/action.md)
* [Impostazione di attesa personalizzata](../building-journeys/wait-activity.md#custom)
* [definizione del fuso orario](../building-journeys/timezone-management.md)

➡️ [Scopri questa funzione nel video](#video)

Questa configurazione non è necessaria se i percorsi sfruttano solo i dati locali provenienti da un payload di eventi. Ad esempio, se il percorso è composto da un evento seguito da un’attività azione canale che utilizza solo i dati dell’evento, non è necessario configurare un’origine dati.

Esistono due tipi di origini dati:

* L’origine dati preconfigurata di Adobe Experience Platform che definisce la connessione al servizio Profilo del cliente in tempo reale. È un’origine dati incorporata. Vedi [questa pagina](../datasource/adobe-experience-platform-data-source.md).
* Le origini dati esterne che consentono di definire una connessione a sistemi esterni. Questi sono quelli che puoi creare. Vedi [questa pagina](../datasource/external-data-sources.md).

Per ogni origine dati è possibile definire le informazioni da recuperare utilizzando i gruppi di campi. I gruppi di campi sono insiemi di campi che possono essere recuperati da un’origine dati. Vedi [questa pagina](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Le relazioni di schema non sono supportate per le origini dati.

Per ulteriori informazioni su come configurare un’origine dati Adobe Experience Platform e un’origine dati esterna, nonché su come individuare e utilizzare i dati in un percorso, consulta questo articolo [video tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target=&quot;_blank&quot;}.

## Video introduttivo {#video}

Scopri cos’è un’origine dati e come configurare Experience Platform e origini dati esterne.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

