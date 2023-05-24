---
solution: Journey Optimizer
product: journey optimizer
title: Livelli di autorizzazione
description: Scopri le autorizzazioni di alto e basso livello che consentono agli utenti di accedere alle diverse funzioni.
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: autorizzazione, alto livello, basso livello, profilo, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Livelli di autorizzazione {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Ogni profilo di prodotto è composto da autorizzazioni che consentono agli utenti di accedere alle diverse funzioni.
Possono essere divisi in due tipi:

* **Autorizzazioni di alto livello**: rappresenta le diverse autorizzazioni che possono essere assegnate a **[!UICONTROL Profilo di prodotto]** nel [!DNL Admin console], ad esempio **[!DNL Publish journeys]** e **[!DNL Manage subdomains delegation]**. Le autorizzazioni di alto livello comprendono le autorizzazioni di basso livello.

* **Autorizzazioni di basso livello**: rappresenta le diverse autorizzazioni provenienti dall’autorizzazione di livello superiore.

Ad esempio, il **[!DNL Journey administrator]** al profilo di prodotto è assegnato il **[!DNL Manage journeys]** autorizzazione. Da questa autorizzazione derivano le autorizzazioni di basso livello che consentiranno all&#39;amministratore di Percorso di scrivere, leggere ed eliminare percorsi.

## Funzionalità percorso {#journey-capability}

### [!DNL Manage journeys] autorizzazione {#manage-journeys}

Il **[!DNL Manage journeys]** le autorizzazioni di alto livello consentono agli utenti di creare nuovi Percorsi e di modificare/eliminare quelli esistenti, nonché di accedere agli oggetti utilizzati nell’area di lavoro del percorso per creare il flusso di percorso.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Specifico di Adobe Experience Platform:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### [!DNL Publish journeys] autorizzazione {#publish-journeys}

Il **[!DNL Publish journeys]** le autorizzazioni di alto livello consentono agli utenti di pubblicare percorsi.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * journeys.publish
   * journeys.read

### [!DNL View journeys] autorizzazione {#view-journeys}

Il **[!DNL View journeys]** le autorizzazioni di alto livello consentono agli utenti di sfogliare e visualizzare i percorsi.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * journeys.read

* Specifico di Adobe Experience Platform:
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] autorizzazione {#manage-journeys-events}

Il **[!DNL Manage journeys events, data sources and actions]** le autorizzazioni di alto livello consentono agli utenti di configurare le configurazioni di eventi e dati.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * percorsi_events.read
   * percorsi_events.write
   * percorsi_events.delete
   * percorsi_data_sources.read
   * percorsi_data_sources.write
   * percorsi_data_sources.delete
   * percorsi_actions.read
   * percorsi_actions.write
   * percorsi_actions.delete

* Specifico di Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys events, data sources and actions] autorizzazione {#view-journeys-event}

Il **[!DNL View journeys events, data sources and actions]** le autorizzazioni di alto livello consentono agli utenti di utilizzare eventi e dati nel flusso di percorso.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * percorsi_events.read
   * percorsi_data_sources.read
   * percorsi_actions.read

* Specifico di Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] autorizzazione {#view-journeys-report}

Il **[!DNL View journeys report]** le autorizzazioni di alto livello consentono agli utenti di visualizzare un report di sola lettura sul percorso.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * percorsi_report.read
   * messages_report.read

* Specifico di Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Capacità di gestione delle decisioni {#decisions-permissions}

### [!DNL Manage decisions] autorizzazione {#manage-decisioning}

Il **[!DNL Manage decisions]** autorizzazione di alto livello consente agli utenti di creare nuovi elementi e modificare/eliminare quelli esistenti **[!DNL Activity entities]**, nonché gestire gli oggetti utilizzati in tali attività per prendere le decisioni.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni specifica:
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

* Specifico di Adobe Experience Platform:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### [!DNL View decisions] autorizzazione {#view-decisions}

Il **[!DNL View decisions]** Le autorizzazioni di alto livello consentono agli utenti di utilizzare un’attività esistente e oggetti di business correlati per prendere le decisioni.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni specifica:
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Specifico di Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### [!DNL Publish offers decisioning] autorizzazione {#publish-decisions}

Il **[!DNL Publish offers decisioning]** Le autorizzazioni di alto livello consentono agli utenti di accedere per approvare/non approvare le attività dell’offerta.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni specifica:
   * offers_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Specifico di Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### [!DNL Manage ranking strategies] autorizzazione {#manage-ranking-strategies}

Il **[!DNL Manage ranking strategies]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare, modificare ed eliminare strategie di classificazione.

Include le seguenti autorizzazioni di basso livello:

* Gestione delle decisioni specifica:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Funzionalità di amministrazione {#administration-permissions}

### [!DNL Manage subdomains delegation] autorizzazione {#manage-subdomain}

Il **[!DNL Manage subdomains delegation]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare deleghe di sottodomini (incluso il pool IP).

Include le seguenti autorizzazioni di basso livello:

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] autorizzazione {#manage-ptr}

Il **[!DNL Manage PTR records]** le autorizzazioni di alto livello consentono agli utenti di leggere e modificare i record PTR configurati in base al sottodominio.

Include le seguenti autorizzazioni di basso livello:

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] autorizzazione {#view-ptr}

Il **[!DNL View PTR records]** le autorizzazioni di alto livello consentono agli utenti di visualizzare i record PTR configurati in base al sottodominio.

Include le seguenti autorizzazioni di basso livello:

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] autorizzazione {#manage-ip-pools}

Il **[!DNL Manage IP pools]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare la definizione di affinità.

Include le seguenti autorizzazioni di basso livello:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

<!--
### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read
-->

### [!DNL Manage channel surface] autorizzazione {#manage-channel-surface}

Il **[!DNL Manage channel surface]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare superfici di canale tra canali diversi a livello di sandbox.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * messages_preets.read
   * messages_preets.write
   * messages_preets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (da Adobe Experience Platform Launch)

### [!DNL View channel surface] autorizzazione {#view-channel-surface}

Il **[!DNL View channel surface]** le autorizzazioni di alto livello consentono agli utenti di visualizzare le superfici di canale per sapere quali superfici di canale utilizzare.

Include le seguenti autorizzazioni di basso livello:

* messages_preets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (da Raccolta dati di Adobe Experience Platform)

### [!DNL Manage suppression] autorizzazione {#manage-suppression}

Il **[!DNL Manage suppression]** le autorizzazioni di alto livello consentono agli utenti di definire il numero di mancati recapiti prima che un indirizzo e-mail venga aggiunto all’elenco di soppressione, nonché di aggiungere ed eliminare voci dall’elenco di soppressione.

Include le seguenti autorizzazioni di basso livello:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] autorizzazione {#view-suppression-list}

Il **[!DNL View suppression list]** le autorizzazioni di alto livello consentono agli utenti di visualizzare il contenuto e le impostazioni dell’elenco di soppressione.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * suppression_list.view

* Specifico di Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] autorizzazione {#export-suppression-list}

Il **[!DNL Export suppression list]** le autorizzazioni di alto livello consentono agli utenti di scaricare l’elenco di soppressione come file CSV.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * suppression_list.export

* Specifico di Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] autorizzazione {#manage-landing-page-settings}

Il **[!DNL Manage landing page settings]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare e modificare i sottodomini e le impostazioni predefinite della pagina di destinazione.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### [!DNL Manage frequency rules] autorizzazione {#manage-frequency-rules}

Il **[!DNL Manage frequency rules]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare, modificare, eliminare e attivare/disattivare le regole di frequenza.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### [!DNL View frequency rules] autorizzazione {#view-frequency-rules}

Il **[!DNL View frequency rules]** le autorizzazioni di alto livello consentono agli utenti di visualizzare le regole di frequenza.

Include le seguenti autorizzazioni di basso livello:

* Specifico di Journey Optimizer:
   * frequency_rules.read
