---
solution: Journey Optimizer
product: journey optimizer
title: Ruoli incorporati di Journey Optimizer
description: Scopri i ruoli incorporati
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: autorizzazioni, authoring, messaggi
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: fd8835b1f9bffd887758e4015171074c5dfc16c0
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 6%

---

# Ruoli incorporati {#ootb-product-profiles}

I ruoli incorporati sono un insieme di diritti unitari che consentono agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia. Fai riferimento a [questa pagina](ootb-permissions.md) per l’elenco delle autorizzazioni disponibili per generare il ruolo.

## [!DNL Campaign Administrator] {#campaign-administrator}

Il **[!DNL Campaign Administrator]** consente ai menu di amministrazione di gestire e pubblicare campagne e gestire le decisioni.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li> **[!DNL Manage campaigns]**: leggi, crea, modifica ed elimina campagne.</li><li>**[!DNL Publish campaigns]**: campagne di pubblicazione.</li><li>**[!DNL View campaigns report]**: leggi e modifica il rapporto campagne.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL Manage subdomains delegation]**: consente di leggere, creare, modificare ed eliminare la delega dei sottodomini.</li><li>**[!DNL Manage IP pools]**: lettura, creazione, modifica ed eliminazione del pool ip.</li><li>**[!DNL Manage PTR records]**: legge e modifica i record PTR.</li><li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li><li> **[!DNL Manage messages general settings]**: leggi, crea, modifica ed elimina le impostazioni generali del messaggio.</li><li>**[!DNL Manage messages presets]**: legge, crea, modifica ed elimina il branding dei contenuti.</li><li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione di lettura, creazione, modifica ed eliminazione.</li><li>**[!DNL Export suppression list]**: accesso per esportare l’elenco di soppressione come file CSV.</li><li>**[!DNL View suppression list]**: legge ed esporta l’elenco di soppressione locale.</li><li>**[!DNL Manage alerts]**: abilita/disabilita gli avvisi per campagne, messaggi e adesioni.</li><li>**[!DNL Manage landing page settings]**: leggi, crea, modifica ed elimina le impostazioni della pagina di destinazione.</li><li>**[!DNL Manage SMS settings]**: leggi, crea, modifica ed elimina le impostazioni SMS.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: legge, crea, modifica ed elimina decisioni.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina strategie di classificazione.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: concedi l’accesso alle sandbox.</li><li>**[!DNL Manage segments]**: leggi, crea, modifica ed elimina le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: legge, crea, modifica ed elimina profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi delle identità.</li><li>**[!DNL Manage merge policies]**: leggi, crea, modifica ed elimina i criteri di unione.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Il **[!DNL Campaign Approver]** Il ruolo consente agli utenti di approvare le consegne e pubblicarle. In un secondo momento potranno verificare il successo delle consegne con **[!DNL Campaigns]** rapporti.

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li>**[!DNL Manage campaigns]**: leggi, crea, modifica ed elimina campagne.</li><li>**[!DNL Publish campaigns]**: campagne di pubblicazione.</li><li>**[!DNL View Campaigns report]**: leggi, modifica i rapporti sul percorso.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: leggi, crea, modifica ed elimina entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti sui messaggi personalizzati e utilizza le funzioni di azione.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: leggi, crea, modifica ed elimina le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: legge, crea, modifica ed elimina profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggi, crea, modifica ed elimina i criteri di unione.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

Il **[!DNL Campaign Manager]** consente agli utenti di creare e modificare **[!UICONTROL Campagne]** e ogni funzionalità collegata a **[!UICONTROL Campagne]** ma non sarà in grado di pubblicarli.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li>**[!DNL Manage campaigns]**: leggi, crea, modifica ed elimina campagne.</li><li>**[!DNL View campaigns report]**: leggi, modifica rapporto percorso.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: leggi, crea, modifica ed elimina entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti sui messaggi personalizzati e utilizza le funzioni di azione.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leggi, crea, modifica ed elimina le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: legge, crea, modifica ed elimina profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggi, crea, modifica ed elimina i criteri di unione.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Il **[!DNL Campaign Viewer]** consente l&#39;accesso in sola lettura al **[!UICONTROL Campagne]** e **[!UICONTROL Gestione delle decisioni]** funzionalità.

Gli utenti assegnati a questo ruolo non potranno modificare o pubblicare.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li>**[!DNL View campaigns]**: accesso in sola lettura alle campagne.</li><li>**[!DNL View campaigns report]**: accesso in sola lettura ai rapporti delle campagne.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Il **[!DNL Journey Administrator]** consente ai menu di amministrazione di gestire e pubblicare Percorsi e gestione delle decisioni.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Percorsi | <ul><li> **[!DNL Manage journeys]**: leggi, crea, modifica ed elimina percorsi.</li><li>**[!DNL Publish journeys]**: pubblica percorsi.</li><li>**[!DNL Manage journeys events, data sources and actions]**: leggi, crea, modifica ed elimina eventi, origini o azioni.</li><li>**[!DNL View journeys report]**: leggi e modifica il rapporto percorsi.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL Manage subdomains delegation]**: consente di leggere, creare, modificare ed eliminare la delega dei sottodomini.</li><li>**[!DNL Manage IP pools]**: lettura, creazione, modifica ed eliminazione del pool ip.</li><li>**[!DNL Manage PTR records]**: legge e modifica i record PTR.</li><li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li><li>**[!DNL Manage messages presets]**: legge, crea, modifica ed elimina il branding dei contenuti.</li><li>**[!DNL Manage Landing page settings]**: crea, modifica ed elimina i sottodomini della pagina di destinazione e i predefiniti della pagina di destinazione.</li><li> **[!DNL Manage messages general settings]**: leggi, crea, modifica ed elimina le impostazioni generali del messaggio.</li><li>**[!DNL Manage SMS settings]**: crea, modifica ed elimina le credenziali API e le superfici di canale SMS necessarie per abilitare il canale SMS.</li><li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione di lettura, creazione, modifica ed eliminazione.</li><li>**[!DNL View suppression list]**: legge ed esporta l’elenco di soppressione locale.</li><li>**[!DNL Manage alerts]**: abilita/disabilita gli avvisi per percorsi e diritti.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: legge, crea, modifica ed elimina decisioni.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina strategie di classificazione.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: concedi l’accesso alle sandbox.</li><li>**[!DNL Manage segments]**: leggi, crea, modifica ed elimina le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: legge, crea, modifica ed elimina profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi delle identità.</li><li>**[!DNL Manage merge policies]**: leggi, crea, modifica ed elimina i criteri di unione.</li></ul> |
| Libreria Journey Optimizer | <ul><li>**[!DNL Manage Library Items]**: aggiungi ed elimina le espressioni salvate in [!DNL Journey Optimizer] Libreria.</li></ul> |
| Governance dei dati | <ul><li>**[!DNL Manage usage label]**: legge, crea ed elimina le etichette di utilizzo.</li><li>**[!DNL Manage data usage policies]**: leggi, crea, modifica ed elimina i criteri di utilizzo dei dati.</li><li>**[!DNL View data usage policies]**: accesso in sola lettura ai criteri di utilizzo dei dati.</li><li>**[!DNL View user activity log]**: legge ed esporta i registri di audit.</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

Il **[!DNL Journey Approver]** Il ruolo consente agli utenti di approvare le consegne e pubblicarle. In un secondo momento potranno verificare il successo delle consegne con **[!DNL Journey]** rapporti.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Percorsi | <ul><li>**[!DNL Manage journeys]**: leggi, crea, modifica ed elimina percorsi.</li><li>**[!DNL Publish journey]**: pubblica percorsi.</li><li>**[!DNL View journeys events, data sources and actions]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati del percorso.</li><li>**[!DNL View journeys report]**: leggi, modifica i rapporti sul percorso.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: leggi, crea, modifica ed elimina entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti personalizzati e utilizza le funzioni di azione.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: leggi, crea, modifica ed elimina le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: legge, crea, modifica ed elimina profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggi, crea, modifica ed elimina i criteri di unione.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL View channel surfaces]**: accesso in sola lettura alle superfici di canale.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Il **[!DNL Journey Manager]** consente agli utenti di creare e modificare **[!UICONTROL Percorsi]** e ogni funzionalità collegata a **[!UICONTROL Percorsi]** ma non sarà in grado di pubblicarli.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Percorsi | <ul><li>**[!DNL Manage journeys]**: leggi, crea, modifica ed elimina percorsi.</li><li>**[!DNL View journeys events]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati del percorso.</li><li>**[!DNL View journeys report]**: leggi, modifica rapporto percorso.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: leggi, crea, modifica ed elimina entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti personalizzati e utilizza le funzioni di azione.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leggi, crea, modifica ed elimina le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: legge, crea, modifica ed elimina profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggi, crea, modifica ed elimina i criteri di unione.</li></ul> |
| Configurazioni canale | <ul><li>**[!DNL View channel surfaces]**: accesso in sola lettura alle superfici di canale.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Il **[!DNL Journey viewer]** consente l&#39;accesso in sola lettura al **[!UICONTROL Percorsi]** e **[!UICONTROL Gestione delle decisioni]** funzionalità.

Gli utenti assegnati a questo ruolo non potranno modificare o pubblicare.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Percorsi | <ul><li>**[!DNL View journeys]**: accesso in sola lettura ai percorsi.</li><li>**[!DNL View journeys event, data sources, actions]**: accesso in sola lettura agli eventi dei percorsi e alle origini dati.</li><li>**[!DNL View journeys report]**: accesso in sola lettura ai rapporti sui percorsi.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Il **[!DNL Decisioning manager]** Il ruolo consente solo l’accesso al **[!UICONTROL Gestione delle decisioni]** menu. Gli utenti assegnati a questo ruolo potranno solo gestire, visualizzare e pubblicare decisioni.

Questo ruolo include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni |
|-|-|
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: leggi, crea, modifica ed elimina entità decisioning.</li><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti personalizzati e utilizza le funzioni di azione.</li><li>**[!DNL Publish decisions]**: attiva o disattiva le attività decisioning.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Experience decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

Il **[!DNL Content Library Manager]** Il ruolo consente solo l’accesso al **[!UICONTROL Modelli di contenuto]** menu. Gli utenti assegnati a questo ruolo potranno accedere alla libreria di modelli solo per creare contenuti senza accedere ai percorsi o alle campagne.

Questo ruolo include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni |
|-|-|
| Libreria Journey Optimizer | <ul><li>**[!DNL Manage library items]**: leggi, crea, modifica ed elimina gli elementi della libreria di Journey Optimizer, inclusi i modelli di contenuto e i frammenti.</li><li>**[!DNL Manage simulate content]**: accesso al **[!UICONTROL Simula contenuto]** opzione per anteprima e bozza.</li><li>**[!DNL Publish Fragment]**: pubblicazione di frammenti di contenuto.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: leggi, crea, modifica ed elimina entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina rapporti personalizzati e utilizza le funzioni di azione.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leggi, crea, modifica ed elimina le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: legge, crea, modifica ed elimina profili.</li><li>**[!DNL Read datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL Read schemas]**: accesso in sola lettura agli schemi.</li><li>**[!DNL Manage merge policies]**: leggi, crea, modifica ed elimina i criteri di unione.</li></ul> |