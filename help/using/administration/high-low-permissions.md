---
solution: Journey Optimizer
product: journey optimizer
title: Livelli di autorizzazione
description: Learn about high and low level permissions allowing users to access the different features.
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: permission, high level, low level, profile, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 0%

---

# Livelli di autorizzazione {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Each role is composed of permissions allowing users to access the different features.
They can be divided into two types:

* **********[!DNL Publish journeys]****[!DNL Manage subdomains delegation]** High level permissions encompass low level permissions. [](ootb-permissions.md)

* ****

**[!DNL Journey administrator]****[!DNL Manage journeys]** From this permission results the low-level permissions which will allow the Journey administrator to write, read and delete journeys.

## risorsa percorso {#journey-capability}

* L&#39;autorizzazione di alto livello **[!DNL Manage journeys]** consente agli utenti di creare nuovi Percorsi e modificare/eliminare quelli esistenti, nonché di accedere agli oggetti utilizzati nell&#39;area di lavoro del percorso per generare il flusso di percorso.

+++ Include le seguenti autorizzazioni di basso livello:

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

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:
      * journeys.publish
      * journeys.read

+++

* L&#39;autorizzazione di alto livello **[!DNL View journeys]** consente agli utenti di visualizzare e sfogliare i percorsi.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * journeys.read

   * Adobe Experience Platform specific:
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]**

+++ It includes the following low-level permissions:

   * Journey Optimizer specific:
      * percorsi_events.read
      * percorsi_events.write
      * percorsi_events.delete
      * journeys_data_sources.read
      * journeys_data_sources.write
      * percorsi_data_sources.delete
      * journeys_actions.read
      * journeys_actions.write
      * journeys_actions.delete

   * Adobe Experience Platform specific:
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* L&#39;autorizzazione di alto livello **[!DNL View journeys events, data sources and actions]** consente agli utenti di utilizzare eventi e dati nel flusso di percorso.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * percorsi_events.read
      * percorsi_data_sources.read
      * percorsi_actions.read

   * Specifico di Adobe Experience Platform:
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]**

+++ It includes the following low-level permissions:

   * Journey Optimizer specific:
      * percorsi_report.read
      * messages_report.read

   * Adobe Experience Platform specific:
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

+++

## risorsa regole Journey Optimizer {#journey-rules-capability}

* L&#39;autorizzazione di alto livello **[!DNL Manage frequency rules]** consente agli utenti di leggere, creare, modificare, eliminare e attivare/disattivare le regole di frequenza.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifiche per Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** autorizzazione di alto livello consente agli utenti di visualizzare le regole di frequenza.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * frequency_rules.read

+++

## Risorsa della campagna {#campaign-capability}

* L&#39;autorizzazione di alto livello **[!DNL Export suppression list]** consente agli utenti di scaricare l&#39;elenco di soppressione come file CSV.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * suppression_list.export

   * Specifico di Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* L&#39;autorizzazione di alto livello **[!DNL Manage campaigns]** consente agli utenti di creare nuove campagne e di modificarle o eliminarle

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* **[!DNL Publish campaigns]**

+++ It includes the following low-level permissions:

   * Specifico di Journey Optimizer:

      * lettura campagna
      * campagna-pubblicare
        <!--* experiments.activate-->

+++

* L&#39;autorizzazione di alto livello **[!DNL View campaigns report]** consente agli utenti di leggere e modificare il report delle campagne.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## Risorse per la gestione delle decisioni {#decisions-permissions}

* **[!DNL Manage decisions]** La autorizzazione di alto livello consente agli utenti di crearne di nuovi e di modificare/eliminare quelli esistenti **[!DNL Activity entities]**, nonché di gestire gli oggetti utilizzati in tali attività per prendere decisioni.

+++ Include le seguenti autorizzazioni di basso livello:

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

   * Adobe Experience Platform specific:
      * datasets.read
      * datasets.write
      * datasets.delete
      * schemas.read
      * profile.read
      * segments.read

+++

* **[!DNL View decisions]**

+++ It includes the following low-level permissions:

   * Decision management specific:
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

+++ Include le seguenti autorizzazioni di basso livello:

   * Gestione delle decisioni specifica:
      * offers_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read

   * Adobe Experience Platform specific:
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* **[!DNL Manage ranking strategies]**

+++ It includes the following low-level permissions:

   * Decision management specific:
      * ranking_strategy.read
      * ranking_strategy.write
      * classificazione_strategia.delete
      * activities.read
      * offers.read
      * placements.read

+++

## Risorsa configurazioni canale {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

  +++ It includes the following low-level permissions:  

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

* **[!DNL Manage file routing]** L&#39;autorizzazione di alto livello consente agli utenti di creare, modificare ed eliminare le configurazioni di routing dei file.

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifiche per Journey Optimizer:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

+++

* L&#39;autorizzazione di alto livello **[!DNL Manage IP pools]** consente agli utenti di creare, modificare ed eliminare la definizione di affinità.

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* L&#39;autorizzazione di alto livello **[!DNL Manage landing page settings]** consente agli utenti di leggere, creare e modificare i sottodomini della pagina di destinazione e le impostazioni predefinite.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* L&#39;autorizzazione di alto livello **[!DNL Manage messages general settings]** consente agli utenti di creare, modificare ed eliminare le impostazioni globali a livello di sandbox.

+++ It includes the following low-level permissions:

   * Journey Optimizer specific:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Adobe Experience Platform specific:
      * schemas.read

+++

* L&#39;autorizzazione di alto livello **[!DNL Manage messages presets]** consente agli utenti di leggere, creare, modificare ed eliminare configurazioni di canale tra canali a livello di sandbox.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifiche per Journey Optimizer:
      * messages_presets.read
      * messages_preets.write
      * messages_preets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Data Collection specific:
      * <!--(from Adobe Experience Platform Launch)-->

+++

* **[!DNL Manage PTR records]**

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL Manage Seedlist]**

+++ It includes the following low-level permissions:

   * Journey Optimizer specific:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* **[!DNL Manage SMS subdomains]**

+++ It includes the following low-level permissions:

   * Journey Optimizer specific:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++

* **[!DNL Manage subdomains delegations]** autorizzazione di alto livello consente agli utenti di creare, modificare ed eliminare delegazioni di sottodomini (incluso il pool IP).

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage suppression]** L&#39;autorizzazione di alto livello consente agli utenti di definire il numero di messaggi non recapitati prima che un indirizzo e-mail venga aggiunto all&#39;elenco di eliminazione, nonché di aggiungere ed eliminare voci all&#39;elenco di eliminazione.

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifiche per Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View file routing]** autorizzazione di alto livello consente agli utenti di visualizzare le configurazioni di indirizzamento dei file.

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:

      * file_routing.read

+++

* L&#39;autorizzazione di alto livello **[!DNL View messages general settings]** consente agli utenti di visualizzare le impostazioni generali dei messaggi, ad esempio l&#39;indirizzo di esecuzione.

+++ Include le seguenti autorizzazioni di basso livello:

   * Journey Optimizer specific:
      * messages_general_settings.read

   * Adobe Experience Platform specific:
      * schemas.read

+++

* **[!DNL View messages presets]**

+++ It includes the following low-level permissions:

   * Journey Optimizer specific:
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Data Collection specific:
      * Mobile_setting.read

+++

* **[!DNL View PTR records]**

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

+++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* L&#39;autorizzazione di alto livello **[!DNL View suppression list]** consente agli utenti di visualizzare il contenuto e le impostazioni dell&#39;elenco di soppressione.

+++ Include le seguenti autorizzazioni di basso livello:

   * Journey Optimizer specific:
      * suppression_list.view

   * Adobe Experience Platform specific:
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

## Risorsa di assistenza IA {#ai-permissions}

* L&#39;autorizzazione di alto livello **[!DNL Generate content]** consente agli utenti di accedere all&#39;Assistente per l&#39;intelligenza artificiale Content Accelerator in Journey Optimizer.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * ai-assistant-generated-content.generate

+++
