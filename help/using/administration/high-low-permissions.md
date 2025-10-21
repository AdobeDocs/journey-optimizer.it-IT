---
solution: Journey Optimizer
product: journey optimizer
title: Livelli di autorizzazione
description: Scopri le autorizzazioni di alto e basso livello che consentono agli utenti di accedere alle diverse funzioni.
topic: Administration
feature: Access Management
role: Admin, Developer
level: Experienced
keywords: autorizzazione, alto livello, basso livello, profilo, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Livelli di autorizzazione {#high-low-permissions}


Ogni ruolo è composto da autorizzazioni che consentono agli utenti di accedere alle diverse funzioni.

Possono essere divisi in due tipi:

* **Autorizzazione di alto livello**: rappresenta le diverse autorizzazioni che possono essere assegnate a **[!UICONTROL Ruolo]**, ad esempio **[!DNL Publish journeys]** e **[!DNL Manage subdomains delegation]**. Le autorizzazioni di alto livello comprendono le autorizzazioni di basso livello. Le autorizzazioni di alto livello sono dettagliate in [questa pagina](ootb-permissions.md).

* **Autorizzazione di basso livello**: rappresenta le diverse autorizzazioni provenienti dall&#39;autorizzazione di alto livello.

Ad esempio, al ruolo **[!DNL Journey administrator]** viene assegnata l&#39;autorizzazione **[!DNL Manage journeys]**. Da questa autorizzazione derivano le autorizzazioni di basso livello che consentiranno all&#39;amministratore di Percorso di scrivere, leggere ed eliminare percorsi.

![](assets/do-not-localize/permissions.png){width="70%"}


## risorsa percorso {#journey-capability}

* L&#39;autorizzazione di alto livello **[!DNL Manage journeys]** consente agli utenti di creare nuovi Percorsi e di modificare, eliminare, arrestare e mettere in pausa quelli esistenti, nonché di accedere agli oggetti utilizzati nell&#39;area di lavoro del percorso per generare il flusso del percorso.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

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

  +++

* **[!DNL Publish journeys]** autorizzazione di alto livello consente agli utenti di pubblicare percorsi.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  
   * Specifico di Journey Optimizer:
      * journeys.publish
      * journeys.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL View journeys]** consente agli utenti di visualizzare e sfogliare i percorsi.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * journeys.read

   * Specifico di Adobe Experience Platform:
      * segments.read
      * profiles.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage journeys events, data sources and actions]** consente agli utenti di configurare le configurazioni di eventi e dati.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

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

  +++

* L&#39;autorizzazione di alto livello **[!DNL View journeys events, data sources and actions]** consente agli utenti di utilizzare eventi e dati nel flusso di percorso.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * percorsi_events.read
      * percorsi_data_sources.read
      * percorsi_actions.read

   * Specifico di Adobe Experience Platform:
      * schemas.read
      * datasets.read
      * identity_namespace.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL View journeys report]** consente agli utenti di visualizzare un report del percorso di sola lettura.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * percorsi_report.read
      * messages_report.read

   * Specifico di Adobe Experience Platform:
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

  +++

## risorsa regole Journey Optimizer {#journey-rules-capability}

* L&#39;autorizzazione di alto livello **[!DNL Manage frequency rules]** consente agli utenti di leggere, creare, modificare, eliminare e attivare/disattivare le regole di frequenza.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

  +++

* **[!DNL View frequency rules]** autorizzazione di alto livello consente agli utenti di visualizzare le regole di frequenza.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * frequency_rules.read

  +++

## Risorsa della campagna {#campaign-capability}

* L&#39;autorizzazione di alto livello **[!DNL Export suppression list]** consente agli utenti di scaricare l&#39;elenco di soppressione come file CSV.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 

   * Specifico di Journey Optimizer:
      * suppression_list.export

   * Specifico di Adobe Experience Platform:
      * profiles.read
      * datasets.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage campaigns]** consente agli utenti di creare nuove campagne e di modificarle o eliminarle

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

  +++

* L&#39;autorizzazione di alto livello **[!DNL Publish campaigns]** consente agli utenti di pubblicare campagne.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

  +++

* L&#39;autorizzazione di alto livello **[!DNL View campaigns report]** consente agli utenti di leggere e modificare il report delle campagne.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

  +++

## Risorsa di gestione decisioni {#decisions-permissions}

* L&#39;autorizzazione di alto livello **[!DNL Manage decisions]** consente agli utenti di creare, modificare o eliminare **[!DNL Activity entities]** esistente e di gestire gli oggetti utilizzati in tali attività per prendere le decisioni.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

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

  +++

* L&#39;autorizzazione di alto livello **[!DNL View decisions]** consente agli utenti di utilizzare un&#39;attività esistente e oggetti business correlati per prendere le decisioni.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Gestione delle decisioni specifica:
      * activities.read
      * offers.read
      * placements.read
      * ranking_strategy.read

   * Specifico di Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage offers]** consente agli utenti di creare, modificare ed eliminare tutte le offerte, i componenti, le decisioni di lettura e le raccolte.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Gestione delle decisioni specifica:
      * offers_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read

   * Specifico di Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage ranking strategies]** consente agli utenti di leggere, creare, modificare ed eliminare strategie di classificazione.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Gestione delle decisioni specifica:
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

  +++

## Risorsa configurazioni canale {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

  +++ This permission includes the following low-level permissions:  

  * Experience decisions specific:
    * ranking_strategy.read
    * offeritem.read
    * offeritem.write
    * offeritem.delete
    * itemCollection.read
    * itemCollection.write
    * itemCollection.delete
    * SelectionStrategy.read
    * SelectionStrategy.write
    * SelectionStrategy.delete
    * Decisionpolicy.read
    * Decisionpolicy.write
    * Decisionpolicy.delete
  +++
-->

* L&#39;autorizzazione di alto livello **[!DNL Manage file routing]** consente agli utenti di creare, modificare ed eliminare configurazioni di indirizzamento dei file.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  
   * Specifico di Journey Optimizer:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage IP pools]** consente agli utenti di creare, modificare ed eliminare la definizione di affinità.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  
   * Specifico di Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage landing page settings]** consente agli utenti di leggere, creare e modificare i sottodomini della pagina di destinazione e le impostazioni predefinite.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 

   * Specifico di Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage messages general settings]** consente agli utenti di creare, modificare ed eliminare le impostazioni globali a livello di sandbox.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Specifico di Adobe Experience Platform:
      * schemas.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage messages presets]** consente agli utenti di leggere, creare, modificare ed eliminare configurazioni di canale tra canali a livello di sandbox.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 

   * Specifico di Journey Optimizer:
      * messages_preets.read
      * messages_preets.write
      * messages_preets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Specifico per raccolta dati:
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage PTR records]** consente agli utenti di leggere e modificare i record PTR configurati in base al sottodominio.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 

   * Specifico di Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage Seedlist]** consente agli utenti di leggere, creare, modificare ed eliminare Seedlist.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 

   * Specifico di Journey Optimizer:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage SMS subdomains]** consente agli utenti di leggere, creare, modificare ed eliminare i sottodomini SMS.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 

   * Specifico di Journey Optimizer:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage subdomains delegations]** consente agli utenti di creare, modificare ed eliminare deleghe di sottodomini (incluso il pool IP).

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  
   * Specifico di Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage suppression]** consente agli utenti di definire il numero di mancati recapiti prima che un indirizzo e-mail venga aggiunto all&#39;elenco di soppressione, nonché di aggiungere ed eliminare voci dall&#39;elenco di soppressione.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  
   * Specifico di Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

  +++

* **[!DNL View file routing]** autorizzazione di alto livello consente agli utenti di visualizzare le configurazioni di indirizzamento dei file.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  
   * Specifico di Journey Optimizer:

      * file_routing.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL View messages general settings]** consente agli utenti di visualizzare le impostazioni generali dei messaggi, ad esempio l&#39;indirizzo di esecuzione.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 

   * Specifico di Journey Optimizer:
      * messages_general_settings.read

   * Specifico di Adobe Experience Platform:
      * schemas.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL View messages presets]** consente agli utenti di visualizzare i predefiniti per i messaggi.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 

   * Specifico di Journey Optimizer:
      * messages_preets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Specifico per raccolta dati:
      * Mobile_setting.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL View PTR records]** consente agli utenti di visualizzare i record PTR configurati in base al sottodominio.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello: 
   * Specifico di Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

  +++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ This permission includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* L&#39;autorizzazione di alto livello **[!DNL View suppression list]** consente agli utenti di visualizzare il contenuto e le impostazioni dell&#39;elenco di soppressione.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * suppression_list.view

   * Specifico di Adobe Experience Platform:
      * profiles.read
      * datasets.read

  +++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ This permission includes the following low-level permissions: 
-->

## Risorsa di assistenza IA {#ai-permissions}

* L&#39;autorizzazione di alto livello **[!DNL Generate content]** consente agli utenti di accedere all&#39;Assistente all&#39;intelligenza artificiale in Journey Optimizer.

  +++ Include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:
      * ai-assistant-generated-content.generate

  +++

## Risorsa della campagna orchestrata {#ai-orchestrated-campaign}

* L&#39;autorizzazione di alto livello **[!DNL Manage orchestrated campaigns]** consente agli utenti di creare nuove campagne orchestrate e di modificarle o eliminarle.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:

      * orchestrated_campaigns.read
      * orchestrated_campaigns.write
      * orchestrated_campaigns.delete
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.write
      * cjm-message.delete
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * cjm-message-preview-test.write
      * experiment.read
      * experiment.write
      * experiment.delete

   * Specifico di Adobe Experience Platform:

      * identity-graph.read
      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read
      * sandboxes.view

  +++

* L&#39;autorizzazione di alto livello **[!DNL Manage orchestrated campaigns admin]** consente agli utenti di creare nuovi collegamenti e riconciliazioni, nonché di modificarli o eliminarli, tra i profili di Adobe Experience Platform e le entità dell&#39;archivio relazionale.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:

      * cjm-orchestrated-campaign-admin.read
      * cjm-orchestrated-campaign-admin.write
      * cjm-orchestrated-campaign-admin.delete

  +++

* L&#39;autorizzazione di alto livello **[!DNL Publish orchestrated campaigns]** consente agli utenti di pubblicare campagne orchestrate.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:

      * cjm-orchestrated-campaign.read
      * cjm-orchestrated-campaign.publish
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.publish
      * cjm-library-item.read

   * Specifico di Adobe Experience Platform:

      * sandboxes.view

  +++

* L&#39;autorizzazione di alto livello **[!DNL View orchestrated campaigns]** consente agli utenti di visualizzare la campagna orchestrata e il relativo contenuto.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:

      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * experiment.read

   * Specifico di Adobe Experience Platform:

      * sandboxes.view
      * segments.read
      * profiles.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL View orchestrated campaigns admin]** consente agli utenti di visualizzare le impostazioni di amministrazione ma non di modificarle.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:

      * cjm-orchestrated-campaign-admin.read

  +++

* L&#39;autorizzazione di alto livello **[!DNL View orchestrated campaigns report]** consente agli utenti di visualizzare le prestazioni delle campagne orchestrate nei report live e aziendali.

  +++ Questa autorizzazione include le seguenti autorizzazioni di basso livello:  

   * Specifico di Journey Optimizer:

      * cjm-orchestrated-campaign-reports.read
      * cjm-message-report.read
      * cjm-channel-report.read
      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * experiment.read
      * experiment-report.read

   * Specifico di Adobe Experience Platform:

      * sandboxes.view
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

  +++
