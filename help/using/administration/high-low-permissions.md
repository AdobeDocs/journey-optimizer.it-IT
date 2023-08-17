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
source-git-commit: 7ac2ae714f2d11d2559b6195af37e2dece35b17c
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---

# Livelli di autorizzazione {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Ogni ruolo è composto da autorizzazioni che consentono agli utenti di accedere alle diverse funzioni.
Possono essere divisi in due tipi:

* **Autorizzazioni di alto livello**: rappresenta le diverse autorizzazioni che possono essere assegnate a **[!UICONTROL Ruolo]** nel [!DNL Admin console], ad esempio **[!DNL Publish journeys]** e **[!DNL Manage subdomains delegation]**. Le autorizzazioni di alto livello comprendono le autorizzazioni di basso livello.

* **Autorizzazioni di basso livello**: rappresenta le diverse autorizzazioni provenienti dall’autorizzazione di livello superiore.

Ad esempio, il **[!DNL Journey administrator]** al ruolo è assegnato il **[!DNL Manage journeys]** autorizzazione. Da questa autorizzazione derivano le autorizzazioni di basso livello che consentiranno all&#39;amministratore di Percorso di scrivere, leggere ed eliminare percorsi.

## risorsa percorso {#journey-capability}

* **[!DNL Manage journeys]** le autorizzazioni di alto livello consentono agli utenti di creare nuovi Percorsi e di modificare/eliminare quelli esistenti, nonché di accedere agli oggetti utilizzati nell’area di lavoro del percorso per creare il flusso di percorso.

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

* **[!DNL Publish journeys]** le autorizzazioni di alto livello consentono agli utenti di pubblicare percorsi.

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** le autorizzazioni di alto livello consentono agli utenti di sfogliare e visualizzare i percorsi.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * journeys.read

   * Specifico di Adobe Experience Platform:
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** le autorizzazioni di alto livello consentono agli utenti di configurare le configurazioni di eventi e dati.

+++ Include le seguenti autorizzazioni di basso livello:

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

* **[!DNL View journeys events, data sources and actions]** le autorizzazioni di alto livello consentono agli utenti di utilizzare eventi e dati nel flusso di percorso.

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

* **[!DNL View journeys report]** le autorizzazioni di alto livello consentono agli utenti di visualizzare un report di sola lettura sul percorso.

+++ Include le seguenti autorizzazioni di basso livello:

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

* **[!DNL Manage frequency rules]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare, modificare, eliminare e attivare/disattivare le regole di frequenza.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** le autorizzazioni di alto livello consentono agli utenti di visualizzare le regole di frequenza.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * frequency_rules.read

+++

## Risorsa della campagna {#campaign-capability}

* **[!DNL Manage campaigns]** Le autorizzazioni di alto livello consentono agli utenti di creare nuove campagne e di modificarle/eliminarle

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* **[!DNL Publish campaigns]** le autorizzazioni di alto livello consentono agli utenti di pubblicare campagne.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** le autorizzazioni di alto livello consentono agli utenti di leggere e modificare i rapporti sulle campagne.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## Risorsa di gestione decisioni {#decisions-permissions}

* **[!DNL Manage decisions]** autorizzazione di alto livello consente agli utenti di creare nuovi elementi e modificare/eliminare quelli esistenti **[!DNL Activity entities]**, nonché gestire gli oggetti utilizzati in tali attività per prendere le decisioni.

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

   * Specifico di Adobe Experience Platform:
      * datasets.read
      * datasets.write
      * datasets.delete
      * schemas.read
      * profile.read
      * segments.read

+++

* **[!DNL View decisions]** Le autorizzazioni di alto livello consentono agli utenti di utilizzare un’attività esistente e oggetti di business correlati per prendere le decisioni.

+++ Include le seguenti autorizzazioni di basso livello:

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

+++

* **[!DNL Manage offers]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare tutte le offerte, i componenti, le decisioni di lettura e le raccolte.

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

   * Specifico di Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* **[!DNL Manage ranking strategies]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare, modificare ed eliminare strategie di classificazione.

+++ Include le seguenti autorizzazioni di basso livello:

   * Gestione delle decisioni specifica:
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

+++

## Risorsa configurazioni canale {#administration-permissions}

* **[!DNL Manage subdomains delegation]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare deleghe di sottodomini (incluso il pool IP).

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage PTR records]** le autorizzazioni di alto livello consentono agli utenti di leggere e modificare i record PTR configurati in base al sottodominio.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL View PTR records]** le autorizzazioni di alto livello consentono agli utenti di visualizzare i record PTR configurati in base al sottodominio.

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

+++

* **[!DNL Manage IP pools]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare la definizione di affinità.

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage messages general settings]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare le impostazioni globali a livello di sandbox.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Specifico di Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL View messages general settings]** le autorizzazioni di alto livello consentono agli utenti di visualizzare le impostazioni generali dei messaggi, ad esempio l’indirizzo di esecuzione.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * messages_general_settings.read

   * Specifico di Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL Manage channel surface]** le autorizzazioni di alto livello consentono agli utenti di creare, modificare ed eliminare superfici di canale tra canali diversi a livello di sandbox.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * messages_preets.read
      * messages_preets.write
      * messages_preets.delete
      * subdomains_delegation.read
      * IP_pools.read
      * mobile_setting.read (da Adobe Experience Platform Launch)

+++

<!--
### [!DNL View channel surface] permission {#view-channel-surface}

The **[!DNL View channel surface]** high-level permission allows users to view channel surfaces in order to know which channel surfaces to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->

* **[!DNL Manage suppression]** le autorizzazioni di alto livello consentono agli utenti di definire il numero di mancati recapiti prima che un indirizzo e-mail venga aggiunto all’elenco di soppressione, nonché di aggiungere ed eliminare voci dall’elenco di soppressione.

+++ Include le seguenti autorizzazioni di basso livello:
   * Specifico di Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View suppression list]** le autorizzazioni di alto livello consentono agli utenti di visualizzare il contenuto e le impostazioni dell’elenco di soppressione.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * suppression_list.view

   * Specifico di Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* **[!DNL Export suppression list]** le autorizzazioni di alto livello consentono agli utenti di scaricare l’elenco di soppressione come file CSV.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * suppression_list.export

   * Specifico di Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage landing page settings]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare e modificare i sottodomini e le impostazioni predefinite della pagina di destinazione.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

* **[!DNL Manage messages presets]** le autorizzazioni di alto livello consentono agli utenti di leggere, creare, modificare ed eliminare il branding dei contenuti.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * messages_preets.read
      * messages_preets.write
      * messages_preets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Specifico per raccolta dati:
      * Mobile_setting.read

+++

* **[!DNL View messages presets]** le autorizzazioni di alto livello consentono agli utenti di visualizzare i predefiniti per i messaggi.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * messages_preets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Specifico per raccolta dati:
      * Mobile_setting.read

+++

* **[!DNL Manage SMS subdomains]** Le autorizzazioni di alto livello consentono agli utenti di leggere, creare, modificare ed eliminare i sottodomini SMS.

+++ Include le seguenti autorizzazioni di basso livello:

   * Specifico di Journey Optimizer:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++
