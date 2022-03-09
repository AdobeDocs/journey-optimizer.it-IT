---
title: Livelli di autorizzazione
description: Informazioni sulle autorizzazioni di livello elevato e basso
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 2a27c19766c84d8c65e8b21ba381754758d60cae
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Livelli di autorizzazione {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Ogni profilo di prodotto è composto da autorizzazioni che consentono agli utenti di accedere alle diverse funzioni.
Possono essere suddivisi in due tipi:

* **Autorizzazione di alto livello**: rappresenta le diverse autorizzazioni a cui è possibile assegnare **[!UICONTROL Product profile]** in [!DNL Admin console], quali **[!DNL Publish journeys]** e **[!DNL Manage subdomains delegation]**. Le autorizzazioni di alto livello includono le autorizzazioni di basso livello.

* **Autorizzazione di basso livello**: rappresenta le diverse autorizzazioni provenienti dall&#39;autorizzazione di alto livello.

Ad esempio, il **[!DNL Journey administrator]** al profilo di prodotto viene assegnato il **[!DNL Manage journeys]** autorizzazione. Da questa autorizzazione risultano le autorizzazioni di basso livello che consentiranno all&#39;amministratore di Percorso di scrivere, leggere ed eliminare percorsi.

## Capacità percorso {#journey-capability}

### [!DNL Manage journeys] autorizzazione {#manage-journeys}

La **[!DNL Manage journeys]** le autorizzazioni di alto livello consentono agli utenti di creare nuovi Percorsi e di modificarli o eliminarli, nonché di accedere agli oggetti utilizzati nell’area di lavoro del percorso per generare il flusso di percorso.

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

### [!DNL Publish journeys] autorizzazione {#publish-journeys}

La **[!DNL Publish journeys]** le autorizzazioni di alto livello consentono agli utenti di pubblicare percorsi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * journeys.publish
   * journeys.read

### [!DNL View journeys] autorizzazione {#view-journeys}

La **[!DNL View journeys]** le autorizzazioni di alto livello consentono agli utenti di sfogliare e visualizzare percorsi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * journeys.read

* Adobe Experience Platform specifico:
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] autorizzazione {#manage-journeys-events}

La **[!DNL Manage journeys events, data sources and actions]** le autorizzazioni di alto livello consentono agli utenti di configurare configurazioni di eventi e dati.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * percorsi_events.read
   * percorsi_events.write
   * percorsi_events.delete
   * percorsi_data_Sources.read
   * percorsi_data_Sources.write
   * journeys_data_sources.delete
   * percorsi_actions.read
   * journeys_actions.write
   * journeys_actions.delete

* Adobe Experience Platform specifico:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys events, data sources and actions] autorizzazione {#view-journeys-event}

La **[!DNL View journeys events, data sources and actions]** le autorizzazioni di alto livello consentono agli utenti di utilizzare eventi e dati nel flusso di percorso.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * percorsi_events.read
   * percorsi_data_Sources.read
   * percorsi_actions.read

* Adobe Experience Platform specifico:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] autorizzazione {#view-journeys-report}

La **[!DNL View journeys report]** le autorizzazioni di alto livello consentono agli utenti di visualizzare rapporti di percorso di sola lettura.

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

### [!DNL Manage messages] autorizzazione {#manage-messages}

La **[!DNL Manage messages]** le autorizzazioni di alto livello consentono agli utenti di creare e modificare/eliminare messaggi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform specifico:
   * segments.read
   * schemas.read

### [!DNL Manage messages preview and test] autorizzazione {#mange-messages-preview}

La **[!DNL Manage messages preview and test]** le autorizzazioni di alto livello consentono agli utenti di visualizzare in anteprima i messaggi personalizzati.

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

### [!DNL Publish messages] autorizzazione {#publish-messages}

La **[!DNL Publish messages]** le autorizzazioni di alto livello consentono agli utenti di pubblicare messaggi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages.publish

* Adobe Experience Platform specific:
   * profiles.read
   * schemas.read
   * datasets.read

### [!DNL View messages] permission {#view-messages}

La **[!DNL View messages]** le autorizzazioni di alto livello consentono agli utenti di leggere solo i messaggi.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages.read
   * messages_presets.read

* Adobe Experience Platform specific:
   * schemas.read
   * segments.read

### [!DNL View messages report] autorizzazione {#view-message-reports}

La **[!DNL View messages report]** le autorizzazioni di alto livello consentono agli utenti di inviare e-mail e rapporti push di sola lettura.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Capacità di gestione delle decisioni {#decisions-permissions}

### [!DNL Manage decisions] autorizzazione {#manage-decisioning}

La **[!DNL Manage decisions]** le autorizzazioni di alto livello consentono agli utenti di creare nuovi e modificare/eliminare quelli esistenti **[!DNL Activity entities]**, nonché gestire gli oggetti utilizzati in tali attività per prendere le decisioni.

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

### [!DNL View decisions] autorizzazione {#view-decisions}

La **[!DNL View decisions]** le autorizzazioni di alto livello consentono agli utenti di utilizzare un&#39;attività esistente e gli oggetti aziendali correlati per prendere le decisioni necessarie.

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

### [!DNL Publish offers decisioning] autorizzazione {#publish-decisions}

The **[!DNL Publish offers decisioning]** high-level permission allows users to access to approve/un-approve Offer activities.

Include le seguenti autorizzazioni di basso livello:

* Decision management specific:
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

### [!DNL Manage ranking strategies] autorizzazione {#manage-decisions}

La **[!DNL Manage ranking strategies]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare, modificare ed eliminare i rapporti sui messaggi personalizzati e di utilizzare le funzioni di azione.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Capacità di amministrazione {#administration-permissions}

### [!DNL Manage subdomains delegation] autorizzazione {#manage-subdomain}

La **[!DNL Manage subdomains delegation]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare deleghe di sottodominio (incluso il pool IP).

Include le seguenti autorizzazioni di basso livello:

* subdomains_delegation.read
* sottodomini_delegate.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] autorizzazione {#manage-ptr}

La **[!DNL Manage PTR records]** le autorizzazioni di alto livello consentono agli utenti di leggere e modificare i record PTR configurati in base al sottodominio.

Include le seguenti autorizzazioni di basso livello:

* PTR_records.read
* PTR_records.write
* sottodomini_delegate.read

### [!DNL View PTR records] permission {#view-ptr}

La **[!DNL View PTR records]** le autorizzazioni di alto livello consentono agli utenti di visualizzare i record PTR configurati in base al sottodominio.

Include le seguenti autorizzazioni di basso livello:

* PTR_records.read
* sottodomini_delegate.read

### [!DNL Manage IP pools] autorizzazione {#manage-ip-pools}

La **[!DNL Manage IP pools]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare la definizione di affinità.

Include le seguenti autorizzazioni di basso livello:

* IP_pool.read
* IP_pool.write
* IP_pool.delete

### [!DNL Manage messages general settings] autorizzazione {#manage-message-settings}

La **[!DNL Manage messages general settings]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare le impostazioni globali a livello di sandbox.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Adobe Experience Platform specifico:
   * schemas.read

### [!DNL View messages general settings] autorizzazione {#view-message-settings}

La **[!DNL View messages general settings]** le autorizzazioni di alto livello consentono agli utenti di visualizzare le impostazioni generali dei messaggi, ad esempio l’indirizzo di esecuzione.

It includes the following low-level permissions:

* Journey Optimizer specifico:
   * messages_general_settings.read
* Adobe Experience Platform specific:
   * schemas.read

### [!DNL Manage messages presets] autorizzazione {#manage-message-presets}

La **[!DNL Manage messages presets]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare i predefiniti per messaggi tra i diversi canali a livello di sandbox.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * sottodomini_delegate.read
   * IP_pool.read
   * mobile_setting.read (da Adobe Experience Platform Launch)

### [!DNL View messages presets] autorizzazione {#view-message-presets}

La **[!DNL View messages presets]** le autorizzazioni di alto livello consentono agli utenti di visualizzare i predefiniti per messaggi al fine di sapere quali predefiniti per messaggi utilizzare durante la creazione di un messaggio.

Include le seguenti autorizzazioni di basso livello:

* messages_presets.read
* sottodomini_delegate.read
* IP_pool.read
* mobile_setting.read (da raccolta dati Adobe Experience Platform)

### [!DNL Manage suppression] autorizzazione {#manage-suppression}

La **[!DNL Manage suppression]** l’autorizzazione di alto livello consente agli utenti di definire il numero di mancati recapiti prima che un indirizzo e-mail venga aggiunto all’elenco di soppressione, nonché di aggiungere ed eliminare voci da/verso l’elenco di soppressione.

Include le seguenti autorizzazioni di basso livello:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] autorizzazione {#view-suppression-list}

The **[!DNL View suppression list]** high-level permission allows users to view the suppression list content and settings.

It includes the following low-level permissions:

* Journey Optimizer specifico:
   * suppression_list.view

* Adobe Experience Platform specific:
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] permission {#export-suppression-list}

La **[!DNL Export suppression list]** le autorizzazioni di alto livello consentono agli utenti di scaricare l’elenco di soppressione come file CSV.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * suppression_list.export

* Adobe Experience Platform specifico:
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] autorizzazione {#manage-landing-page-settings}

La **[!DNL Manage landing page settings]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare e modificare i sottodomini della pagina di destinazione e le impostazioni predefinite.

Include le seguenti autorizzazioni di basso livello:

* Journey Optimizer specifico:
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete
