---
title: Profili di prodotto incorporati
description: Informazioni sui profili di prodotto incorporati
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: b1c4fb836d34cc6263f804c7a0f700571281b31a
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 10%

---

# Profili di prodotto incorporati {#ootb-product-profiles}

## [!DNL Journey Administrator] {#journey-administrator}

La **[!DNL Journey Administrator]** il profilo di prodotto consente ai menu di amministrazione di gestire e pubblicare Percorsi, messaggi e gestione delle decisioni.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li> **[!DNL Manage journeys]**: leggere, creare, modificare ed eliminare percorsi.</li><li>**[!DNL Publish journeys]**: pubblica percorsi.</li><li>**[!DNL Manage journeys events, data sources and actions]**: leggere, creare, modificare ed eliminare eventi, origini o azioni.</li><li>**[!DNL View journeys report]**: leggere e modificare il rapporto percorsi.</li></ul>|
|Messaggi|<ul><li> **[!DNL Manage messages]**: leggi, crea, modifica anteprima messaggio e invia test/bozza.</li><li>**[!DNL Manage messages preview and test]**: pubblicare messaggi.</li><li>**[!DNL Publish messages]**: leggi, crea e modifica l’anteprima dei messaggi e invia test/bozza.</li><li>**[!DNL View messages report]**: leggere e modificare il rapporto sui messaggi.</li></ul>|
|Amministrazione|<ul><li>**[!DNL Manage subdomains delegation]**: leggere, creare, modificare ed eliminare la delega dei sottodomini.</li><li>**[!DNL Manage IP pools]**: leggi, crea, modifica ed elimina il pool ip.</li><li>**[!DNL Manage PTR records]**: leggere e modificare i record PTR.</li><li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li><li> **[!DNL Manage messages general settings]**: leggere, creare, modificare ed eliminare le impostazioni generali del messaggio.</li><li>**[!DNL Manage messages presets]**: leggere, creare, modificare ed eliminare il branding dei contenuti.</li><li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione lette, create, modificate ed eliminate.</li><li>**[!DNL View suppression list]**: leggere ed esportare l&#39;elenco di soppressione locale.</li><li>**[!DNL Manage alerts]**: abilitare/disabilitare gli avvisi per percorsi, messaggi e adesioni.</li></ul>|
|Gestione delle decisioni|<ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le decisioni.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: concedere l’accesso alle sandbox.</li><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi identità.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>| |Libreria Journey Optimizer|<ul><li>**[!DNL Manage Library Items]**: aggiungere ed eliminare espressioni salvate nel [!DNL Journey Optimizer] Libreria.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

La **[!DNL Journey Approver]** il profilo di prodotto consente agli utenti di approvare le consegne e pubblicarle. In un secondo momento possono verificare il successo delle consegne con **[!DNL Message]** e **[!DNL Journey]** rapporti.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li>**[!DNL Manage journeys]**: leggere, creare, modificare ed eliminare percorsi.</li><li>**[!DNL Publish journey]**: pubblica percorsi.</li><li>**[!DNL View journeys events, data sources and actions]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati di percorso.</li><li>**[!DNL View journeys report]**: leggere, modificare i rapporti sui percorsi.</li></ul>|
|Messaggi| <ul><li>**[!DNL Manage messages]**: leggere, creare, modificare ed eliminare i messaggi.</li><li>**[!DNL Publish messages]** pubblicare messaggi.</li><li>**[!DNL Manage messages preview and test]**: leggi, crea e modifica l’anteprima dei messaggi e invia test/bozza.</li><li>**[!DNL View messages report]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>|
|Amministrazione| <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

La **[!DNL Journey Manager]** il profilo di prodotto consente agli utenti di creare e modificare **[!UICONTROL Journeys]** e ogni funzionalità collegata **[!UICONTROL Journeys]** ma non sarà in grado di pubblicarli.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li>**[!DNL Manage journeys]**: leggere, creare, modificare ed eliminare percorsi.</li><li>**[!DNL View journeys events]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati di percorso.</li><li>**[!DNL View journeys report]**: leggere, modificare il rapporto percorso.</li></ul>|
|Messaggi| <ul><li>**[!DNL Manage messages]**: leggere, creare, modificare ed eliminare i messaggi.</li><li> **[!DNL Manage messages preview and test]**: leggi, crea e modifica l’anteprima dei messaggi e invia test/bozza.</li><li>**[!DNL View messages report]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>|
|Amministrazione| <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul>|

## [!DNL Journey viewer] {#journey-viewer}

La **[!DNL Journey viewer]** il profilo di prodotto consente l’accesso in sola lettura al **[!UICONTROL Journeys]**, **[!UICONTROL Goals]**, **[!UICONTROL Messages]** e **[!UICONTROL Decision management]** funzionalità.

Gli utenti assegnati a questo profilo di prodotto non potranno modificare o pubblicare.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li>**[!DNL View journeys]**: accesso in sola lettura ai percorsi.</li><li>**[!DNL View journeys event, data sources, actions]**: accesso in sola lettura agli eventi di percorso e alle origini dati.</li><li>**[!DNL View journeys report]**: accesso in sola lettura ai rapporti sui percorsi.</li></ul>|
|Messaggi| <ul><li>**[!DNL View messages]**: accesso in sola lettura ai messaggi.</li><li>**[!DNL View messages report]**: accesso in sola lettura ai rapporti sui messaggi.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul>|

## [!DNL Message Manager] {#message-manager}

La **[!DNL Message Manager]** il profilo di prodotto consente agli utenti di creare e modificare **[!UICONTROL Messages]** e **[!UICONTROL Decision management]** ma non sarà in grado di pubblicarli.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li>**[!DNL View journeys]**: accesso in sola lettura ai percorsi.</li><li>**[!DNL View Journeys events, data sources and actions]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati di percorso.</li></ul>|
|Messaggi| <ul><li>**[!DNL Manage messages]**: leggere, creare, modificare ed eliminare i messaggi.</li><li>**[!DNL Manage messages preview and test]**: leggi, crea e modifica l’anteprima dei messaggi e invia test/bozza.</li><li> **[!DNL View messages report]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Read profiles]**: accesso in sola lettura al profilo per l’anteprima e il test.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>|
|Amministrazione| <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

La **[!DNL Decisioning manager]** il profilo di prodotto consente solo **[!UICONTROL Decision management]** menu. Gli utenti assegnati a questo profilo di prodotto potranno solo gestire, visualizzare e pubblicare le decisioni.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi personalizzati e utilizzare le funzionalità di azione.</li><li>**[!DNL Publish decisions]**: attiva o disattiva le attività decisionali.</li></ul>|
