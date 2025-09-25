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
source-git-commit: 2a5db6950ac82fd18deb2e4009c9a43247444d6a
workflow-type: tm+mt
source-wordcount: '1996'
ht-degree: 7%

---

# Ruoli incorporati {#ootb-product-profiles}

I ruoli incorporati sono un insieme di diritti unitari che consentono agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia. Per un elenco delle autorizzazioni disponibili per la creazione del ruolo, consulta [questa pagina](ootb-permissions.md).


## [!DNL Campaign Administrator] {#campaign-administrator}

Il ruolo **[!DNL Campaign Administrator]** consente ai menu di amministrazione di gestire e pubblicare campagne e gestione delle decisioni.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li> <li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li> <li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li> <li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li> <li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi delle identità.</li> <li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li> <li>**[!DNL Sandbox]**: concedere l&#39;accesso alle sandbox.</li> </ul> |
| Campagne | <ul><li> **[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare campagne.</li><li>**[!DNL Publish campaigns]**: pubblicare campagne.</li><li>**[!DNL View campaigns report]**: leggere e modificare il report delle campagne.</li></ul> |
| Configurazione del canale | <ul> <li>**[!DNL Export suppression list]**: accesso per esportare l&#39;elenco di soppressione come file CSV.</li> <li>**[!DNL Manage alerts]**: abilita/disabilita gli avvisi per campagne, messaggi e adesioni.</li> <li>**[!DNL Manage IP pools]**: lettura, creazione, modifica ed eliminazione del pool ip.</li> <li>**[!DNL Manage landing page settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni della pagina di destinazione.</li> <li>**[!DNL Manage messages general settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni generali del messaggio.</li> <li>**[!DNL Manage messages presets]**: lettura, creazione, modifica ed eliminazione del branding dei contenuti.</li> <li>**[!DNL Manage PTR records]**: lettura e modifica dei record PTR.</li> <li>**[!DNL Manage SMS settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni SMS.</li> <li>**[!DNL Manage subdomains delegation]**: delega del sottodominio di lettura, creazione, modifica ed eliminazione.</li> <li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione in lettura, creazione, modifica ed eliminazione.</li> <li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li> <li>**[!DNL View suppression list]**: lettura ed esportazione dell&#39;elenco di soppressione locale.</li> </ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le decisioni.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina strategie di classificazione.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Il ruolo **[!DNL Campaign Approver]** consente agli utenti di approvare le consegne e pubblicarle. Potranno in seguito verificare il successo delle loro consegne con i report **[!DNL Campaigns]**.

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li></ul> |
| Campagne | <ul><li>**[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare campagne.</li><li>**[!DNL Publish campaigns]**: pubblicare campagne.</li><li>**[!DNL View campaigns report]**: lettura, modifica report campagne.</li></ul> |
| Configurazione del canale | <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i report di messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul> |


## [!DNL Campaign Manager] {#campaign-manager}

Il ruolo **[!DNL Campaign Manager]** consente agli utenti di creare e modificare **[!UICONTROL Campagne]** e tutte le funzionalità collegate a **[!UICONTROL Campagne]**, ma non sarà possibile pubblicarle.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li></ul> |
| Campagne | <ul><li>**[!DNL Manage campaigns]**: leggere, creare, modificare ed eliminare campagne.</li><li>**[!DNL View campaigns report]**: lettura, modifica report percorso.</li></ul> |
| Configurazione del canale | <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i report di messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Il ruolo **[!DNL Campaign Viewer]** consente l&#39;accesso in sola lettura alle funzionalità **[!UICONTROL Campagne]** e **[!UICONTROL Gestione delle decisioni]**.

Gli utenti assegnati a questo ruolo non potranno modificare o pubblicare.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Campagne | <ul><li>**[!DNL View campaigns]**: accesso in sola lettura alle campagne.</li><li>**[!DNL View campaigns report]**: accesso in sola lettura ai report delle campagne.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

Il ruolo **[!DNL Content Library Manager]** consente l&#39;accesso solo al menu **[!UICONTROL Modelli di contenuto]**. Gli utenti assegnati a questo ruolo potranno accedere alla libreria di modelli solo per creare contenuti senza accedere ai percorsi o alle campagne.

Questa autorizzazione include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: lettura, creazione, modifica ed eliminazione di report personalizzati e utilizzo delle funzionalità di azione.</li></ul> |
| Libreria Journey Optimizer | <ul><li>**[!DNL Manage library items]**: lettura, creazione, modifica ed eliminazione di elementi della libreria Journey Optimizer, inclusi modelli di contenuto e frammenti.</li><li>**[!DNL Manage simulate content]**: accesso all&#39;opzione **[!UICONTROL Simula contenuto]** per anteprima e bozza.</li><li>**[!DNL Publish Fragment]**: pubblicare frammenti di contenuto.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Il ruolo **[!DNL Decisioning manager]** consente solo l&#39;accesso al menu **[!UICONTROL Gestione delle decisioni]**. Gli utenti assegnati a questo ruolo potranno solo gestire, visualizzare e pubblicare decisioni.

Questa autorizzazione include le seguenti autorizzazioni:

| Funzionalità | Autorizzazioni |
|-|-|
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: lettura, creazione, modifica ed eliminazione di report personalizzati e utilizzo delle funzionalità di azione.</li><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisioning.</li><li>**[!DNL Publish decisions]**: attiva o disattiva le attività decisioning.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Il ruolo **[!DNL Journey Administrator]** consente ai menu di amministrazione di gestire e pubblicare Percorsi e Gestione delle decisioni.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li> <li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li> <li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li> <li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li> <li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi delle identità.</li> <li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li> <li>**[!DNL Sandbox]**: concedere l&#39;accesso alle sandbox.</li> </ul> |
| Configurazione del canale | <ul> <li>**[!DNL Manage alerts]**: abilita/disabilita avvisi per percorsi e diritti.</li> <li>**[!DNL Manage IP pools]**: lettura, creazione, modifica ed eliminazione del pool ip.</li> <li>**[!DNL Manage Landing page settings]**: crea, modifica ed elimina i sottodomini della pagina di destinazione e i predefiniti della pagina di destinazione.</li> <li>**[!DNL Manage messages general settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni generali del messaggio.</li> <li>**[!DNL Manage messages presets]**: lettura, creazione, modifica ed eliminazione del branding dei contenuti.</li> <li>**[!DNL Manage PTR records]**: lettura e modifica dei record PTR.</li> <li>**[!DNL Manage SMS settings]**: creare, modificare ed eliminare le credenziali API e le configurazioni del canale SMS necessarie per abilitare il canale SMS.</li> <li>**[!DNL Manage subdomains delegation]**: delega del sottodominio di lettura, creazione, modifica ed eliminazione.</li> <li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione in lettura, creazione, modifica ed eliminazione.</li> <li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li> <li>**[!DNL View suppression list]**: lettura ed esportazione dell&#39;elenco di soppressione locale.</li> </ul> |
| Governance dei dati | <ul> <li>**[!DNL Manage data usage policies]**: lettura, creazione, modifica ed eliminazione dei criteri di utilizzo dei dati.</li> <li>**[!DNL Manage usage label]**: leggere, creare ed eliminare le etichette di utilizzo.</li> <li>**[!DNL View data usage policies]**: accesso in sola lettura ai criteri di utilizzo dei dati.</li> <li>**[!DNL View user activity log]**: accesso in sola lettura per visualizzare i registri di controllo registrati delle attività di Experience Platform.</li> </ul> |
| Gestione delle decisioni | <ul> <li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le decisioni.</li> <li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina strategie di classificazione.</li> </ul> |
| Percorsi | <ul> <li>**[!DNL Manage journeys]**: lettura, creazione, modifica, pausa, interruzione ed eliminazione di percorsi.</li> <li>**[!DNL Manage journeys events, data sources and actions]**: lettura, creazione, modifica ed eliminazione di eventi, origini o azioni.</li> <li>**[!DNL Publish journeys]**: pubblica percorsi.</li> <li>**[!DNL View journeys report]**: leggere e modificare il rapporto percorsi.</li> </ul> |
| Libreria Journey Optimizer | <ul> <li>**[!DNL Manage Library Items]**: aggiungere ed eliminare le espressioni salvate nella libreria [!DNL Journey Optimizer].</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

Il ruolo **[!DNL Journey Approver]** consente agli utenti di approvare le consegne e pubblicarle. Potranno in seguito verificare il successo delle loro consegne con i report **[!DNL Journey]**.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li></ul> |
| Configurazione del canale | <ul><li>**[!DNL View channel configurations]**: accesso in sola lettura alle configurazioni dei canali.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: lettura, creazione, modifica ed eliminazione di report personalizzati e utilizzo delle funzionalità di azione.</li></ul> |
| Percorsi | <ul><li>**[!DNL Manage journeys]**: lettura, creazione, modifica, pausa, interruzione ed eliminazione di percorsi.</li><li>**[!DNL Publish journey]**: pubblica percorsi.</li><li>**[!DNL View journeys events, data sources and actions]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati del percorso.</li><li>**[!DNL View journeys report]**: lettura, modifica report percorso.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Il ruolo **[!DNL Journey Manager]** consente agli utenti di creare e modificare **[!UICONTROL Percorsi]** e tutte le funzionalità collegate a **[!UICONTROL Percorsi]**, ma non sarà in grado di pubblicarli.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li><li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li></ul> |
| Configurazione del canale | <ul><li>**[!DNL View channel configurations]**: accesso in sola lettura alle configurazioni dei canali.</li></ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: lettura, creazione, modifica ed eliminazione di report personalizzati e utilizzo delle funzionalità di azione.</li></ul> |
| Percorsi | <ul><li>**[!DNL Manage journeys]**: lettura, creazione, modifica ed eliminazione di percorsi.</li><li>**[!DNL View journeys events]**: accesso in sola lettura agli eventi di percorso, alle azioni personalizzate del percorso e alle origini dati del percorso.</li><li>**[!DNL View journeys report]**: lettura, modifica report percorso.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Il ruolo **[!DNL Journey viewer]** consente l&#39;accesso in sola lettura alle funzionalità **[!UICONTROL Percorsi]** e **[!UICONTROL Gestione delle decisioni]**.

Gli utenti assegnati a questo ruolo non potranno modificare o pubblicare.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Gestione delle decisioni | <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul> |
| Percorsi | <ul><li>**[!DNL View journeys]**: accesso in sola lettura ai percorsi.</li><li>**[!DNL View journeys event, data sources, actions]**: accesso in sola lettura agli eventi di percorso e alle origini dati.</li><li>**[!DNL View journeys report]**: accesso in sola lettura ai report percorsi.</li></ul> |

## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

Il ruolo **[!DNL Orchestrated Campaign Administrator]** consente ai menu di amministrazione di gestire e pubblicare campagne orchestrate.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Enable AI Assistant]**: abilita o accedi alle funzionalità relative a campagne e pubblico basate sull’intelligenza artificiale.</li> <li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li> <li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li> <li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li> <li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li> <li>**[!DNL Read Identity namespace]**: accesso in sola lettura allo spazio dei nomi delle identità.</li> <li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li> <li>**[!DNL Sandbox]**: concedere l&#39;accesso alle sandbox.</li> <li>**[!DNL View operational insights]**: accesso in sola lettura a dashboard di monitoraggio e insights a livello di sistema.</li></ul> |
| Configurazione del canale | <ul><li>**[!DNL Export suppression list]**: accesso per esportare l&#39;elenco di soppressione come file CSV.</li> <li>**[!DNL Manage alerts]**: abilita/disabilita gli avvisi per campagne, messaggi e adesioni.</li> <li>**[!DNL Manage custom dashboards]**: leggere, creare, modificare ed eliminare dashboard personalizzati.</li><li>**[!DNL Manage IP pools]**: lettura, creazione, modifica ed eliminazione del pool ip.</li> <li>**[!DNL Manage landing page settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni della pagina di destinazione.</li> <li>**[!DNL Manage messages general settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni generali del messaggio.</li> <li>**[!DNL Manage messages presets]**: lettura, creazione, modifica ed eliminazione del branding dei contenuti.</li><li>**[!DNL Manage PTR records]**: lettura e modifica dei record PTR.</li> <li>**[!DNL Manage SMS settings]**: lettura, creazione, modifica ed eliminazione delle impostazioni SMS.</li> <li>**[!DNL Manage subdomains delegation]**: delega del sottodominio di lettura, creazione, modifica ed eliminazione.</li> <li>**[!DNL Manage suppression rules]**: accedere alle regole di soppressione in lettura, creazione, modifica ed eliminazione.</li> <li>**[!DNL View PTR records]**: accesso in sola lettura ai record PTR.</li> <li>**[!DNL View suppression list]**: lettura ed esportazione dell&#39;elenco di soppressione locale.</li> </ul> |
| Dashboard di | <ul> <li>**[!DNL Manage standard dashboard]**: leggere, creare, modificare ed eliminare i widget personalizzati e lo schema di widget tramite la libreria Widget.</li> </ul> |
| Governance dei dati | <ul> <li>**[!DNL View user activity log]**: accesso in sola lettura per visualizzare i registri di controllo registrati delle attività di Experience Platform. </li> </ul> |
| Acquisizione dati | <ul> <li>**[!DNL Manage sources]**: lettura, creazione, modifica e disabilitazione delle origini.</li> </ul> |
| Gestione dati | <ul> <li>**[!DNL Manage datasets]**: leggere, creare, modificare ed eliminare i set di dati.</li> </ul> |
| Modellazione dati | <ul> <li>**[!DNL Manage schemas]**: lettura, creazione, modifica ed eliminazione di schemi e risorse correlate.</li> </ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: leggere, creare, modificare ed eliminare le decisioni.</li><li>**[!DNL Manage ranking strategies]**: leggi, crea, modifica ed elimina strategie di classificazione.</li></ul> |
| Regole Journey Optimizer | <ul> <li>**[!DNL View frequency rules]**: accesso in sola lettura alle regole di frequenza.</li><li>**[!DNL Manage frequency rules]**: leggere, creare, modificare o eliminare le regole di frequenza.</li> </ul> |
| Messaggi | <ul><li> **[!DNL Manage Messages]**: lettura, creazione, modifica ed eliminazione di messaggi. </li> **[!DNL Manage Messages Preview and Test]**: approva e pubblica i messaggi quando viene applicato un criterio.</li><li>**[!DNL Publish Messages]**: pubblicare i messaggi. </li><li>**[!DNL View Messages Report]**: legge e modifica i rapporti sui messaggi. <li></ul> |
| Campagne orchestrate | <ul><li> **[!DNL Manage orchestrated campaigns]**: lettura, creazione, modifica ed eliminazione di campagne orchestrate.</li> <li>**[!DNL Manage orchestrated campaigns admin]**: lettura, creazione, modifica ed eliminazione di collegamenti e riconciliazioni tra i profili di Adobe Experience Platform e le entità dell&#39;archivio relazionale.</li><li>**[!DNL Publish orchestrated campaigns]**: pubblica campagne orchestrate.</li><li>**[!DNL View orchestrated campaigns report]**: lettura e modifica del report Campagne orchestrate.</li></ul> |

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

Il ruolo **[!DNL Orchestrated Campaign Approver]** consente agli utenti di pubblicare campagne orchestrate.

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li> <li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li> <li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li> <li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li> <li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li> <li>**[!DNL Enable AI Assistant]**: abilita o accedi alle funzionalità relative a campagne e pubblico basate sull’intelligenza artificiale.</li>  <li>**[!DNL View operational insights]**: accesso in sola lettura a dashboard di monitoraggio e insights a livello di sistema.</li></ul> |
| Configurazione del canale | <ul><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li> <li>**[!DNL Manage custom dashboards]**: crea, modifica ed elimina dashboard personalizzati.</li></ul> |
| Dashboard di | <ul> <li>**[!DNL Manage standard dashboard]**: leggere, creare, modificare ed eliminare i widget personalizzati e lo schema di widget tramite la libreria Widget.</li> </ul> |
| Governance dei dati | <ul> <li>**[!DNL View user activity log]**: accesso in sola lettura per visualizzare i registri di controllo registrati delle attività di Experience Platform.</li> </ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i report di messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul> |
| Regole Journey Optimizer | <ul> <li>**[!DNL View frequency rules]**: accesso in sola lettura alle regole di frequenza.</li></ul> |
| Messaggi | <ul><li> **[!DNL Manage Messages]**: lettura, creazione, modifica ed eliminazione di messaggi. </li> **[!DNL Manage Messages Preview and Test]**: approva e pubblica i messaggi quando viene applicato un criterio.</li><li>**[!DNL Publish Messages]**: pubblicare i messaggi. </li><li>**[!DNL View Messages Report]**: legge e modifica i rapporti sui messaggi. <li></ul> |
| Campagne orchestrate | <ul><li>**[!DNL Manage orchestrated campaigns]**: lettura, creazione, modifica ed eliminazione di campagne orchestrate.</li><li>**[!DNL Publish orchestrated campaigns]**: pubblica campagne orchestrate.</li><li>**[!DNL View orchestrated campaigns admin]**: accesso in sola lettura ai collegamenti e alle riconciliazioni tra i profili di Adobe Experience Platform e le entità dell&#39;archivio relazionale.</li><li>**[!DNL View orchestrated campaigns report]**: lettura, modifica dei report delle campagne orchestrate.</li></ul> |

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

Il ruolo **[!DNL Orchestrated Campaign Manager]** consente agli utenti di creare e modificare **[!UICONTROL Campagne orchestrate]** e ogni funzionalità collegata a **[!UICONTROL Campagne orchestrate]**, ma non sarà in grado di pubblicarle.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: abilita o accedi alle funzionalità relative a campagne e pubblico basate sull’intelligenza artificiale.</li> <li>**[!DNL Manage merge policies]**: lettura, creazione, modifica ed eliminazione dei criteri di unione.</li><li>**[!DNL Manage profiles]**: lettura, creazione, modifica ed eliminazione di profili.</li><li> **[!DNL Manage segments]**: leggere, creare, modificare ed eliminare le definizioni dei segmenti.</li><li>**[!DNL View datasets]**: accesso in sola lettura ai set di dati.</li>  <li>**[!DNL View operational insights]**: accesso in sola lettura a dashboard di monitoraggio e insights a livello di sistema.</li><li>**[!DNL View schemas]**: accesso in sola lettura agli schemi.</li></ul> |
| Configurazione del canale | <ul><li>**[!DNL Manage custom dashboards]**: crea, modifica ed elimina dashboard personalizzati.</li><li>**[!DNL View messages presets]**: accesso in sola lettura ai predefiniti per messaggi.</li></ul> |
| Dashboard di | <ul> <li>**[!DNL Manage standard dashboard]**: leggere, creare, modificare ed eliminare i widget personalizzati e lo schema di widget tramite la libreria Widget.</li> </ul> |
| Governance dei dati | <ul> <li>**[!DNL View user activity log]**: accesso in sola lettura per visualizzare i registri di controllo registrati delle attività di Experience Platform.</li> </ul> |
| Gestione delle decisioni | <ul><li>**[!DNL Manage decisions]**: lettura, creazione, modifica ed eliminazione di entità decisioning.</li><li>**[!DNL Manage ranking strategies]**: leggere, creare, modificare ed eliminare i report di messaggi personalizzati e utilizzare le funzionalità di azione.</li></ul> |
| Regole Journey Optimizer | <ul> <li>**[!DNL View frequency rules]**: accesso in sola lettura alle regole di frequenza. </li></ul> |
| Messaggi | <ul><li> **[!DNL Manage Messages]**: lettura, creazione, modifica ed eliminazione di messaggi. </li> **[!DNL Manage Messages Preview and Test]**: approva e pubblica i messaggi quando viene applicato un criterio.</li><li>**[!DNL View Messages Report]**: legge e modifica i rapporti sui messaggi. </li></ul> |
| Campagne orchestrate | <ul><li>**[!DNL Manage orchestrated campaigns]**: lettura, creazione, modifica ed eliminazione di campagne orchestrate.</li><li>**[!DNL View orchestrated campaigns report]**: lettura, modifica campagne orchestrate.</li><li>**[!DNL View orchestrated campaigns admin]**: accesso in sola lettura ai collegamenti e alle riconciliazioni tra i profili di Adobe Experience Platform e le entità dell&#39;archivio relazionale.</li></ul> |

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

Il ruolo **[!DNL Campaign Viewer]** consente l&#39;accesso in sola lettura alle funzionalità **[!UICONTROL Campagne orchestrate]**.

Gli utenti assegnati a questo ruolo non potranno modificare o pubblicare.

Questo ruolo include le seguenti autorizzazioni:

| Risorse | Autorizzazioni |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: abilita o accedi alle funzionalità relative a campagne e pubblico basate sull’intelligenza artificiale.</li> <li>**[!DNL View operational insights]**: accesso in sola lettura a dashboard di monitoraggio e insights a livello di sistema.</li></ul> |
| Configurazione del canale | <ul><li>**[!DNL Manage custom dashboards]**: crea, modifica ed elimina dashboard personalizzati.</li></ul> |
| Dashboard di | <ul> <li>**[!DNL Manage standard dashboard]**: leggere, creare, modificare ed eliminare i widget personalizzati e lo schema di widget tramite la libreria Widget.</li> </ul> |
| Governance dei dati | <ul> <li>**[!DNL View user activity log]**: accesso in sola lettura per visualizzare i registri di controllo registrati delle attività di Experience Platform.</li> </ul> |
| Gestione delle decisioni | <ul><li>**[!DNL View decisions]**: accesso in sola lettura alle entità decisionali.</li></ul> |
| Regole Journey Optimizer | <ul> <li>**[!DNL View frequency rules]**: accesso in sola lettura alle regole di frequenza.</li></ul> |
| Campagne orchestrate | <ul><li>**[!DNL View orchestrated campaigns]**: accesso in sola lettura alle campagne orchestrate.</li><li>**[!DNL View orchestrated campaigns report]**: accesso in sola lettura ai report delle campagne orchestrate.</li></ul> |




