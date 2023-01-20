---
solution: Journey Optimizer
product: journey optimizer
title: Profili di prodotto incorporati
description: Informazioni sui profili di prodotto incorporati
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: autorizzazioni, authoring, messaggi
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 9%

---

# Profili di prodotto incorporati {#ootb-product-profiles}


## Informazioni sulle autorizzazioni relative ai messaggi{#message-permissions}

Adobe Journey Optimizer ha rilasciato nuove funzionalità di authoring in linea che consentono di creare e creare messaggi direttamente da un percorso o da una campagna.

Questa funzione influisce sulle autorizzazioni come segue:

| Nome dell&#39;autorizzazione | Sarà incluso in |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**Dopo il 25 luglio**, autorizzazioni relative a **Messaggi** sono ancora disponibili, in quanto è ancora possibile accedere ai messaggi per abilitare la transizione e puoi comunque salvarli come modello.

**A partire dal 6 settembre**, autorizzazioni relative a **Messaggi** verranno rimossi e i messaggi non saranno più accessibili.

>[!WARNING]
>
>Se hai degli utenti assegnati al **[!DNL Message Manager]** solo profilo di prodotto, senza **[!DNL Journey manager]** profilo di prodotto, devi assegnare un nuovo profilo di prodotto per consentire loro di continuare a modificare il contenuto.


## [!DNL Campaign Administrator] {#campaign-administrator}

La **[!DNL Campaign Administrator]** il profilo di prodotto consente ai menu di amministrazione di gestire e pubblicare le campagne e la gestione delle decisioni.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Campagne| <ul><li> **[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare le campagne.</li><li>**[!DNL Publish campaigns]**: pubblicare campagne.</li><li>**[!DNL View campaigns report]**: leggere e modificare il rapporto sulle campagne.</li></ul>|
|Amministrazione|<ul><li>**[!DNL Manage subdomains delegation]**: leggere, creare, modificare ed eliminare la delega dei sottodomini.</li><li>**[!DNL Manage IP pools]**: leggi, crea, modifica ed elimina il pool ip.</li><li>**[!DNL Manage PTR records]**: leggere e modificare i record PTR.</li><li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li><li> **[!DNL Manage messages general settings]**: leggere, creare, modificare ed eliminare le impostazioni generali del messaggio.</li><li>**[!DNL Manage messages presets]**: leggere, creare, modificare ed eliminare il branding dei contenuti.</li><li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione lette, create, modificate ed eliminate.</li><li>**[!DNL Export suppression list]**: accesso all’esportazione dell’elenco di soppressione come file CSV.</li><li>**[!DNL View suppression list]**: leggere ed esportare l&#39;elenco di soppressione locale.</li><li>**[!DNL Manage alerts]**: abilitare/disabilitare gli avvisi per campagne, messaggi e adesioni.</li><li>**[!DNL Manage landing page settings]**: leggere, creare, modificare ed eliminare le impostazioni della pagina di destinazione.</li><li>**[!DNL Manage SMS settings]**: leggere, creare, modificare ed eliminare le impostazioni SMS.</li></ul>|
|Gestione delle decisioni|<ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le decisioni.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare le strategie di classificazione.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: concedere l’accesso alle sandbox.</li><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi identità.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

La **[!DNL Campaign Approver]** il profilo di prodotto consente agli utenti di approvare le consegne e pubblicarle. In un secondo momento possono verificare il successo delle consegne con **[!DNL Campaigns]** rapporti.

| Funzionalità | Autorizzazioni| |-|-| |Campagne| <ul><li>**[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare le campagne.</li><li>**[!DNL Publish campaigns]**: pubblicare campagne.</li><li>**[!DNL View Campaigns report]**: leggere, modificare i rapporti sui percorsi.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>|
|Amministrazione| <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

La **[!DNL Campaign Manager]** il profilo di prodotto consente agli utenti di creare e modificare **[!UICONTROL Campagne]** e ogni funzionalità collegata **[!UICONTROL Campagne]** ma non sarà in grado di pubblicarli.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Campagne| <ul><li>**[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare le campagne.</li><li>**[!DNL View campaigns report]**: leggere, modificare il rapporto percorso.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i rapporti sui messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>|
|Amministrazione| <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

La **[!DNL Campaign Viewer]** il profilo di prodotto consente l’accesso in sola lettura al **[!UICONTROL Campagne]** e **[!UICONTROL Gestione delle decisioni]** funzionalità.

Gli utenti assegnati a questo profilo di prodotto non potranno modificare o pubblicare.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Campagne| <ul><li>**[!DNL View campaigns]**: accesso in sola lettura alle campagne.</li><li>**[!DNL View campaigns report]**: accesso in sola lettura ai report delle campagne.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

La **[!DNL Journey Administrator]** il profilo di prodotto consente ai menu di amministrazione la possibilità di gestire e pubblicare Percorsi e gestione delle decisioni.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li> **[!DNL Manage journeys]**: leggere, creare, modificare ed eliminare percorsi.</li><li>**[!DNL Publish journeys]**: pubblica percorsi.</li><li>**[!DNL Manage journeys events, data sources and actions]**: leggere, creare, modificare ed eliminare eventi, origini o azioni.</li><li>**[!DNL View journeys report]**: leggere e modificare il rapporto percorsi.</li></ul>|
|Amministrazione|<ul><li>**[!DNL Manage subdomains delegation]**: leggere, creare, modificare ed eliminare la delega dei sottodomini.</li><li>**[!DNL Manage IP pools]**: leggi, crea, modifica ed elimina il pool ip.</li><li>**[!DNL Manage PTR records]**: leggere e modificare i record PTR.</li><li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li><li>**[!DNL Manage channel surfaces]**: leggere, creare, modificare ed eliminare il branding dei contenuti.</li><li>**[!DNL Manage Landing page settings]**: creare, modificare ed eliminare sottodomini della pagina di destinazione e predefiniti della pagina di destinazione.</li><li> **[!DNL Manage messages general settings]**: leggere, creare, modificare ed eliminare le impostazioni generali del messaggio.</li><li>**[!DNL Manage SMS settings]**: crea, modifica ed elimina le credenziali API e le superfici del canale SMS necessarie per abilitare il canale SMS.</li><li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione lette, create, modificate ed eliminate.</li><li>**[!DNL View suppression list]**: leggere ed esportare l&#39;elenco di soppressione locale.</li><li>**[!DNL Manage alerts]**: abilitare/disabilitare gli avvisi per percorsi e adesioni.</li></ul>|
|Gestione delle decisioni|<ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le decisioni.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare le strategie di classificazione.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: concedere l’accesso alle sandbox.</li><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi identità.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>| |Libreria Journey Optimizer|<ul><li>**[!DNL Manage Library Items]**: aggiungere ed eliminare espressioni salvate nel [!DNL Journey Optimizer] Libreria.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

La **[!DNL Journey Approver]** il profilo di prodotto consente agli utenti di approvare le consegne e pubblicarle. In un secondo momento possono verificare il successo delle consegne con **[!DNL Journey]** rapporti.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li>**[!DNL Manage journeys]**: leggere, creare, modificare ed eliminare percorsi.</li><li>**[!DNL Publish journey]**: pubblica percorsi.</li><li>**[!DNL View journeys events, data sources and actions]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati di percorso.</li><li>**[!DNL View journeys report]**: leggere, modificare i rapporti sui percorsi.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti personalizzati e utilizza le funzionalità di azione.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>|
|Amministrazione| <ul><li>**[!DNL View channel surfaces]**: accesso in sola lettura alle superfici del canale.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

La **[!DNL Journey Manager]** il profilo di prodotto consente agli utenti di creare e modificare **[!UICONTROL Percorsi]** e ogni funzionalità collegata **[!UICONTROL Percorsi]** ma non sarà in grado di pubblicarli.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li>**[!DNL Manage journeys]**: leggere, creare, modificare ed eliminare percorsi.</li><li>**[!DNL View journeys events]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati di percorso.</li><li>**[!DNL View journeys report]**: leggere, modificare il rapporto percorso.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti personalizzati e utilizza le funzionalità di azione.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare i segmenti.</li><li>**[!DNL Manage profiles]**: leggere, creare, modificare ed eliminare i profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggere, creare, modificare ed eliminare i criteri di unione.</li></ul>|
|Amministrazione| <ul><li>**[!DNL View channel surfaces]**: accesso in sola lettura alle superfici del canale.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

La **[!DNL Journey viewer]** il profilo di prodotto consente l’accesso in sola lettura al **[!UICONTROL Percorsi]** e **[!UICONTROL Gestione delle decisioni]** funzionalità.

Gli utenti assegnati a questo profilo di prodotto non potranno modificare o pubblicare.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Percorsi| <ul><li>**[!DNL View journeys]**: accesso in sola lettura ai percorsi.</li><li>**[!DNL View journeys event, data sources, actions]**: accesso in sola lettura agli eventi di percorso e alle origini dati.</li><li>**[!DNL View journeys report]**: accesso in sola lettura ai rapporti sui percorsi.</li></ul>|
|Gestione delle decisioni| <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

La **[!DNL Decisioning manager]** il profilo di prodotto consente solo **[!UICONTROL Gestione delle decisioni]** menu. Gli utenti assegnati a questo profilo di prodotto potranno solo gestire, visualizzare e pubblicare le decisioni.

Questo profilo di prodotto include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni| |-|-| |Gestione delle decisioni| <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le entità decisionali.</li><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti personalizzati e utilizza le funzionalità di azione.</li><li>**[!DNL Publish decisions]**: attiva o disattiva le attività decisionali.</li></ul>|
