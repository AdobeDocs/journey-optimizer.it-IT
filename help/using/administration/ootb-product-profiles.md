---
solution: Journey Optimizer
product: journey optimizer
title: Ruoli incorporati di Journey Optimizer
description: Learn about the built-in Roles
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: permissions, authoring, messages
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 6%

---

# Ruoli incorporati {#ootb-product-profiles}

Built-in roles are a set of unitary rights which allows users access to certain functionalities or objects in the interface. Per un elenco delle autorizzazioni disponibili per la creazione del ruolo, consulta [questa pagina](ootb-permissions.md).

## [!DNL Campaign Administrator] {#campaign-administrator}

Il ruolo **[!DNL Campaign Administrator]** consente ai menu di amministrazione di gestire e pubblicare campagne e gestione delle decisioni.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li> **[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare campagne.</li><li>**[!DNL Publish campaigns]**: pubblicare campagne.</li><li>**[!DNL View campaigns report]**: leggere e modificare il report delle campagne.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL Manage subdomains delegation]**: delega del sottodominio di lettura, creazione, modifica ed eliminazione.</li><li>**[!DNL Manage IP pools]**</li><li>**[!DNL Manage PTR records]**</li><li>**[!DNL View PTR records]**</li><li> **[!DNL Manage messages general settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni generali del messaggio.</li><li>**[!DNL Manage messages presets]**: lettura, creazione, modifica ed eliminazione del branding dei contenuti.</li><li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione in lettura, creazione, modifica ed eliminazione.</li><li>**[!DNL Export suppression list]**</li><li>**[!DNL View suppression list]**</li><li>**[!DNL Manage alerts]**</li><li>**[!DNL Manage landing page settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni della pagina di destinazione.</li><li>**[!DNL Manage SMS settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni SMS.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**</li><li>**[!DNL Manage ranking strategies]**</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**</li><li>**[!DNL Manage segments]**</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi delle identità.</li><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Il ruolo **[!DNL Campaign Approver]** consente agli utenti di approvare le consegne e pubblicarle. Potranno in seguito verificare il successo delle loro consegne con i report **[!DNL Campaigns]**.

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li>**[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare campagne.</li><li>**[!DNL Publish campaigns]**: pubblicare campagne.</li><li>**[!DNL View Campaigns report]**</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**</li><li>**[!DNL Manage ranking strategies]**</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

Il ruolo **[!DNL Campaign Manager]** consente agli utenti di creare e modificare **[!UICONTROL Campagne]** e tutte le funzionalità collegate a **[!UICONTROL Campagne]**, ma non sarà possibile pubblicarle.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li>**[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare campagne.</li><li>**[!DNL View campaigns report]**: lettura, modifica report percorso.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i report di messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Il ruolo **[!DNL Campaign Viewer]** consente l&#39;accesso in sola lettura alle funzionalità **[!UICONTROL Campagne]** e **[!UICONTROL Gestione delle decisioni]**.

Gli utenti assegnati a questo ruolo non potranno modificare o pubblicare.

This role includes the following permissions:

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li>**[!DNL View campaigns]**: accesso in sola lettura alle campagne.</li><li>**[!DNL View campaigns report]**: accesso in sola lettura ai report delle campagne.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL View decisions]**</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Il ruolo **[!DNL Journey Administrator]** consente ai menu di amministrazione di gestire e pubblicare Percorsi e Gestione delle decisioni.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Percorsi | <ul><li> **[!DNL Manage journeys]**</li><li>**[!DNL Publish journeys]**</li><li>**[!DNL Manage journeys events, data sources and actions]**</li><li>**[!DNL View journeys report]**</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL Manage subdomains delegation]**: delega del sottodominio di lettura, creazione, modifica ed eliminazione.</li><li>**[!DNL Manage IP pools]**: lettura, creazione, modifica ed eliminazione del pool ip.</li><li>**[!DNL Manage PTR records]**: lettura e modifica dei record PTR.</li><li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li><li>**[!DNL Manage messages presets]**: lettura, creazione, modifica ed eliminazione del branding dei contenuti.</li><li>**[!DNL Manage Landing page settings]**</li><li> **[!DNL Manage messages general settings]**</li><li>**[!DNL Manage SMS settings]**</li><li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione in lettura, creazione, modifica ed eliminazione.</li><li>**[!DNL View suppression list]**: lettura ed esportazione dell&#39;elenco di soppressione locale.</li><li>**[!DNL Manage alerts]**</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**</li><li>**[!DNL Manage ranking strategies]**</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: concedere l&#39;accesso alle sandbox.</li><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi delle identità.</li><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li></ul> |
| Libreria Journey Optimizer | <ul><li>**[!DNL Manage Library Items]**: aggiungere ed eliminare le espressioni salvate nella libreria [!DNL Journey Optimizer].</li></ul> |
| Governance dei dati | <ul><li>**[!DNL Manage usage label]**: leggere, creare ed eliminare le etichette di utilizzo.</li><li>**[!DNL Manage data usage policies]**: lettura, creazione, modifica ed eliminazione dei criteri di utilizzo dei dati.</li><li>**[!DNL View data usage policies]**: accesso in sola lettura ai criteri di utilizzo dei dati.</li><li>**[!DNL View user activity log]**</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

**[!DNL Journey Approver]** **[!DNL Journey]**

This role includes the following permissions:

| Risorse | Autorizzazioni |
|-|-|
| Percorsi | <ul><li>**[!DNL Manage journeys]**: lettura, creazione, modifica ed eliminazione di percorsi.</li><li>**[!DNL Publish journey]**: pubblica percorsi.</li><li>**[!DNL View journeys events, data sources and actions]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati del percorso.</li><li>**[!DNL View journeys report]**: lettura, modifica report percorso.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: lettura, creazione, modifica ed eliminazione di report personalizzati e utilizzo delle funzionalità di azione.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**</li><li>**[!DNL Manage profiles]**</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL View channel configurations]**</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

**[!DNL Journey Manager]**********

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Percorsi | <ul><li>**[!DNL Manage journeys]**</li><li>**[!DNL View journeys events]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati del percorso.</li><li>**[!DNL View journeys report]**: lettura, modifica report percorso.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: lettura, creazione, modifica ed eliminazione di report personalizzati e utilizzo delle funzionalità di azione.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**</li></ul> |
| Channel configurations | <ul><li>**[!DNL View channel configurations]**: accesso in sola lettura alle configurazioni dei canali.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Il ruolo **[!DNL Journey viewer]** consente l&#39;accesso in sola lettura alle funzionalità **[!UICONTROL Percorsi]** e **[!UICONTROL Gestione delle decisioni]**.

Gli utenti assegnati a questo ruolo non potranno modificare o pubblicare.

This role includes the following permissions:

| Risorse | Autorizzazioni |
|-|-|
| Percorsi | <ul><li>**[!DNL View journeys]**</li><li>**[!DNL View journeys event, data sources, actions]**: accesso in sola lettura agli eventi di percorso e alle origini dati.</li><li>**[!DNL View journeys report]**: accesso in sola lettura ai report percorsi.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Il ruolo **[!DNL Decisioning manager]** consente solo l&#39;accesso al menu **[!UICONTROL Gestione delle decisioni]**. Gli utenti assegnati a questo ruolo potranno solo gestire, visualizzare e pubblicare decisioni.

Questo ruolo include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni |
|-|-|
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: lettura, creazione, modifica ed eliminazione di report personalizzati e utilizzo delle funzionalità di azione.</li><li>**[!DNL Publish decisions]**: attiva o disattiva le attività decisioning.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

**[!DNL Content Library Manager]****** Users assigned to this role will only be able to access the template library to create content without accessing the journeys or campaigns.

This role includes the following permissions:

| Capability | Autorizzazioni |
|-|-|
| Libreria Journey Optimizer | <ul><li>**[!DNL Manage library items]**: lettura, creazione, modifica ed eliminazione di elementi della libreria Journey Optimizer, inclusi modelli di contenuto e frammenti.</li><li>**[!DNL Manage simulate content]**: accesso all&#39;opzione **[!UICONTROL Simula contenuto]** per anteprima e bozza.</li><li>**[!DNL Publish Fragment]**: pubblicare frammenti di contenuto.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: lettura, creazione, modifica ed eliminazione di report personalizzati e utilizzo delle funzionalità di azione.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li>**[!DNL Read datasets]**</li><li>**[!DNL Read schemas]**</li><li>**[!DNL Manage merge policies]**</li></ul> |