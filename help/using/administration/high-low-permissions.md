---
title: Livelli di autorizzazione
description: Informazioni sulle autorizzazioni di livello elevato e basso
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
source-git-commit: b32306f9561946a6c289e5e9c7cc3243349141bc
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# Livelli di autorizzazione {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Ogni profilo di prodotto è composto da autorizzazioni che consentono agli utenti di accedere alle diverse funzioni.
Possono essere suddivisi in due tipi:

* **Autorizzazione** di alto livello: rappresenta le diverse autorizzazioni che possono essere assegnate a  **[!UICONTROL Product profile]** in  [!DNL Admin console], ad esempio  **[!UICONTROL Publish journeys]** e  **[!UICONTROL Manage subdomains delegation]**. Le autorizzazioni di alto livello includono le autorizzazioni di basso livello.

* **Autorizzazione** di basso livello: rappresenta le diverse autorizzazioni provenienti dall&#39;autorizzazione di alto livello.

Ad esempio, al profilo di prodotto **[!UICONTROL Journey administrator]** viene assegnata l&#39;autorizzazione **[!UICONTROL Manage journeys]**. Da questa autorizzazione risultano le autorizzazioni di basso livello che consentiranno all&#39;amministratore di Percorso di scrivere, leggere ed eliminare percorsi.

## Capacità percorso {#journey-capability}

### Autorizzazione per la gestione dei percorsi {#manage-journeys}

L’ **[!UICONTROL Manage journeys]** autorizzazione di alto livello consente agli utenti di creare nuovi Percorsi e di modificarli o eliminarli, nonché di accedere agli oggetti utilizzati nell’area di lavoro del percorso per creare il flusso di percorso.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Adobe Experience Platform specifico:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### Autorizzazione per la pubblicazione di percorsi {#publish-journeys}

L’ autorizzazione di alto livello **[!UICONTROL Publish journeys]** consente agli utenti di pubblicare percorsi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * journeys.publish
   * journeys.read

### Visualizza autorizzazione percorsi {#view-journeys}

L’ autorizzazione di alto livello **[!UICONTROL View journeys]** consente agli utenti di sfogliare e visualizzare percorsi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * journeys.read

* Adobe Experience Platform specifico:
   * segments.read
   * profiles.read

### Gestisci autorizzazioni eventi, origini dati e azioni percorsi {#manage-journeys-events}

L’ autorizzazione di alto livello **[!UICONTROL Manage journeys events, data sources and actions]** consente agli utenti di configurare configurazioni di eventi e dati.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * percorsi_events.read
   * percorsi_events.write
   * percorsi_events.delete
   * percorsi_data_Sources.read
   * percorsi_data_Sources.write
   * percorsi_data_Sources.delete
   * percorsi_actions.read
   * percorsi_actions.write
   * percorsi_actions.delete
* Adobe Experience Platform specifico:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Visualizza autorizzazione eventi, origini dati e azioni percorsi {#view-journeys-event}

L’ autorizzazione di alto livello **[!UICONTROL View journeys events, data sources and actions]** consente agli utenti di utilizzare eventi e dati nel flusso di percorso.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * percorsi_events.read
   * percorsi_data_Sources.read
   * percorsi_actions.read

* Adobe Experience Platform specifico:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Visualizza autorizzazione rapporto percorsi {#view-journeys-report}

L’ autorizzazione di alto livello **[!UICONTROL View journeys report]** consente agli utenti di visualizzare rapporti di percorso di sola lettura.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * percorsi_report.read
   * messages_report.read

* Adobe Experience Platform specifico:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Capacità del messaggio {#message-capability}

### Autorizzazione per la gestione dei messaggi {#manage-messages}

L’ **[!UICONTROL Manage messages]** autorizzazione di alto livello consente agli utenti di creare e modificare/eliminare messaggi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform specifico:
   * segments.read
   * schemas.read

### Gestione dell’anteprima e del test dei messaggi {#mange-messages-preview}

L’ **[!UICONTROL Manage messages preview and test]** autorizzazione di alto livello consente agli utenti di visualizzare in anteprima i messaggi personalizzati.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Adobe Experience Platform specifico:
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_Policies.read

### Autorizzazione per la pubblicazione dei messaggi {#publish-messages}

L’ **[!UICONTROL Publish messages]** autorizzazione di alto livello consente agli utenti di pubblicare messaggi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages.publish

* Adobe Experience Platform specifico:
   * profiles.read
   * schemas.read
   * datasets.read

### Visualizza autorizzazione messaggi {#view-messages}

L’ autorizzazione di alto livello **[!UICONTROL View messages]** consente agli utenti di leggere solo i messaggi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages.read
   * messages_presets.read

* Adobe Experience Platform specifico:
   * schemas.read
   * segments.read

### Visualizza autorizzazione rapporti messaggi {#view-message-reports}

L’ **[!UICONTROL View messages report]** autorizzazione di alto livello consente agli utenti di inviare e-mail e rapporti push di sola lettura.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Capacità di gestione delle decisioni {#decisions-permissions}

### Autorizzazione per la gestione delle decisioni {#manage-decisioning}

L’ **[!UICONTROL Manage decisions]** autorizzazione di alto livello consente agli utenti di creare nuovi e modificare/eliminare **[!UICONTROL Activity entities]** esistenti, nonché di gestire gli oggetti utilizzati in tali attività per prendere le decisioni necessarie.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni:
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform specifico:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### Visualizza autorizzazione decisioni {#view-decisions}

L’ autorizzazione di alto livello **[!UICONTROL View decisions]** consente agli utenti di utilizzare un’attività esistente e gli oggetti aziendali correlati per prendere le decisioni necessarie.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni:
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Adobe Experience Platform specifico:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### Autorizzazione per pubblicare offerte decisionali {#publish-decisions}

L’ **[!UICONTROL Publish offers decisioning]** autorizzazione di alto livello consente agli utenti di accedere alle attività di approvazione/annullamento dell’approvazione dell’offerta.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni:
   * offers_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform specifico:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### Autorizzazione per gestire le strategie di classificazione {#manage-decisions}

L’ **[!UICONTROL Manage ranking strategies]** autorizzazione di alto livello consente agli utenti di leggere, creare, modificare ed eliminare i rapporti sui messaggi personalizzati e di utilizzare le funzioni di azione.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Capacità di amministrazione {#administration-permissions}

### Gestisci autorizzazioni di delega dei sottodomini {#manage-subdomain}

L’ **[!UICONTROL Manage subdomains delegation]** autorizzazione di alto livello consente agli utenti di creare, modificare ed eliminare delegazioni di sottodominio (incluso il pool IP).

Include le seguenti autorizzazioni di basso livello:

* sottodomini_delegate.read
* sottodomini_delegate.write
* sottodomini_delegate.delete

### Visualizza autorizzazione record PTR {#view-ptr}

L’ autorizzazione di alto livello **[!UICONTROL View PTR records]** consente agli utenti di visualizzare i record PTR configurati in base al sottodominio.

Include le seguenti autorizzazioni di basso livello:

* PTR_records.read
* sottodomini_delegate.read

### Gestisci autorizzazioni pool IP {#manage-ip-pools}

L’ autorizzazione **[!UICONTROL Manage IP pools]** di alto livello consente agli utenti di creare, modificare ed eliminare la definizione di affinità.

Include le seguenti autorizzazioni di basso livello:

* IP_pool.read
* IP_pool.write
* IP_pool.delete

### Gestisci autorizzazioni impostazioni generali dei messaggi {#manage-message-settings}

L’ **[!UICONTROL Manage messages general settings]** autorizzazione di alto livello consente agli utenti di creare, modificare ed eliminare le impostazioni globali a livello di sandbox.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Adobe Experience Platform specifico:
   * schemas.read

### Visualizza messaggi autorizzazione impostazioni generali {#view-message-settings}

L’ **[!UICONTROL View messages general settings]** autorizzazione di alto livello consente agli utenti di visualizzare i messaggi e le impostazioni generali, ad esempio l’indirizzo di esecuzione.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages_general_settings.read
* Adobe Experience Platform specifico:
   * schemas.read

### Autorizzazioni per la gestione dei predefiniti per i messaggi {#manage-message-presets}

L’ **[!UICONTROL Manage messages presets]** autorizzazione di alto livello consente agli utenti di creare, modificare ed eliminare i predefiniti per messaggi tra i diversi canali a livello di sandbox.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * sottodomini_delegate.read
   * IP_pool.read
   * mobile_setting.read (da Adobe Experience Platform Launch)

### Visualizza autorizzazione predefiniti per messaggi {#view-message-presets}

L’ **[!UICONTROL View messages presets]** autorizzazione di alto livello consente agli utenti di visualizzare i predefiniti per i messaggi, al fine di sapere quali predefiniti per i messaggi devono essere utilizzati durante la creazione di un messaggio.

Include le seguenti autorizzazioni di basso livello:

* messages_presets.read
* sottodomini_delegate.read
* IP_pool.read
* mobile_setting.read (da Adobe Experience Platform Launch)

### Gestisci autorizzazione di soppressione {#manage-suppression}

L’ **[!UICONTROL Manage suppression]** autorizzazione di alto livello consente agli utenti di definire il numero di messaggi non recapitati prima che un indirizzo e-mail venga aggiunto all’elenco di eliminazione, nonché di aggiungere ed eliminare voci da/verso l’elenco di eliminazione.

Include le seguenti autorizzazioni di basso livello:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### Visualizza autorizzazione elenco di soppressione {#view-suppresion-list}

L’ autorizzazione di alto livello **[!UICONTROL View suppression list]** consente agli utenti di visualizzare il contenuto e le impostazioni dell’elenco di soppressione.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * suppression_list.view
* Adobe Experience Platform specifico:
   * profiles.read
   * datasets.read

### Autorizzazione per l&#39;esportazione dell&#39;elenco di soppressione {#export-suppression-list}

L’ autorizzazione di alto livello **[!UICONTROL Export suppression list]** consente agli utenti di scaricare l’elenco di soppressione come file CSV.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * suppression_list.export
* Adobe Experience Platform specifico:
   * profiles.read
   * datasets.read
