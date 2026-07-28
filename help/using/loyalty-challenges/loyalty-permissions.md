---
solution: Journey Optimizer
product: journey optimizer
title: Autorizzazioni per le sfide di fedeltà
description: Scopri quali autorizzazioni sono necessarie per accedere, configurare e utilizzare le sfide di fidelizzazione in Adobe Journey Optimizer.
feature: Journeys
topic: Administration
role: Admin
level: Intermediate
exl-id: 7d6d4f18-8c5d-4c9c-9f7d-2d6c5f9a8b31
feature_v2: []
subfeature_v2: []
source-git-commit: b45a83f480603ecd38cfcbdf31ccc639f617f592
workflow-type: tm+mt
source-wordcount: 967
ht-degree: 6%

---

# Autorizzazioni per le sfide di fedeltà {#loyalty-permissions}

## Panoramica {#overview}

La fedeltà di [!DNL Adobe Journey Optimizer] utilizza il controllo degli accessi basato sul ruolo di Adobe Admin Console per gestire l&#39;accesso degli utenti.

L&#39;assegnazione del ruolo è necessaria prima che gli utenti possano eseguire operazioni di fidelizzazione. Agli utenti senza un ruolo assegnato viene negato l’accesso agli endpoint del servizio fedeltà. Prima di effettuare l’onboarding degli utenti in Fedeltà, assegna un ruolo appropriato a ciascun utente che utilizzerà il servizio.

I ruoli possono essere assegnati direttamente a singoli utenti o tramite gruppi di utenti. [Scopri come assegnare ruoli agli utenti](#assign-roles).

## Ruoli consigliati {#recommended-roles}

La fidelizzazione fornisce tre ruoli predefiniti preconfigurati per la sandbox **Prod**. I nuovi clienti possono utilizzare questi ruoli così come sono.

### Amministratore fedeltà {#loyalty-administrator}

Il ruolo di **Amministratore fedeltà** fornisce accesso amministrativo completo a tutte le funzionalità di fedeltà: problemi, configurazione, catalogo prodotti e approfondimenti.

| Autorizzazione | Descrizione |
| - | - |
| Gestire le sfide di fedeltà | Problemi di creazione, modifica, eliminazione, pubblicazione, annullamento della pubblicazione e archiviazione; attivare la generazione di percorsi |
| Gestisci configurazione principale fedeltà | Creare, modificare ed eliminare la configurazione dell’organizzazione principale |
| Gestisci configurazione avanzata fedeltà | Gestisce gli endpoint di ricompensa e le impostazioni di trasformazione degli eventi, incluso l&#39;accesso in lettura/scrittura ai valori delle credenziali sensibili |
| Gestione catalogo prodotti fedeltà | Visualizzare, importare e modificare le voci del catalogo prodotti |
| Gestisci informazioni sulla fedeltà | Visualizzare approfondimenti, aggiornare la configurazione dei KPI e attivare la pipeline di approfondimenti |

### Professionista fedeltà {#loyalty-practitioner}

Il ruolo **Professionista fedeltà** è progettato per i proprietari aziendali che gestiscono l&#39;intero ciclo di vita della sfida e modificano la configurazione principale. La configurazione dei premi, la configurazione degli eventi e l’accesso al catalogo dei prodotti sono di sola lettura. L’eliminazione e le scritture di configurazione avanzate non sono consentite.

| Autorizzazione | Descrizione |
| - | - |
| Gestire le sfide di fedeltà | Problemi di creazione, modifica, eliminazione, pubblicazione, annullamento della pubblicazione e archiviazione; attivare la generazione di percorsi |
| Configurare la configurazione principale del programma fedeltà | Crea e modifica la configurazione dell’organizzazione principale. Eliminazione non consentita |
| Visualizza configurazione premio fedeltà | Visualizza la configurazione del premio, inclusi provider, definizioni e proxy. I valori sensibili sono esclusi |
| Visualizza configurazione evento fedeltà | Visualizzare le definizioni degli eventi e le mappature della trasformazione degli eventi |
| Visualizza catalogo prodotti fedeltà | Visualizzare le voci del catalogo dei prodotti e lo stato del processo di importazione |
| Sviluppa Approfondimenti Fedeltà | Visualizza i dati di insights e aggiorna le schede di insight |

### Analista fedeltà {#loyalty-analyst}

Il ruolo **Analista fedeltà** fornisce accesso in sola lettura a sfide, catalogo dei prodotti e approfondimenti. Utilizza questo ruolo a scopo di reporting e controllo.

| Autorizzazione | Descrizione |
| - | - |
| Visualizza le sfide di fedeltà | Visualizza le sfide |
| Visualizza catalogo prodotti fedeltà | Visualizzare le voci del catalogo dei prodotti e lo stato del processo di importazione |
| Visualizza informazioni sulla fedeltà | Visualizzare schede insight generate dall’intelligenza artificiale, dati vitali sulla salute e dati sulle prestazioni della sfida |

## Funzionalità ruolo {#role-capabilities}

| Operazione | Amministratore | Professionista | Analista |
| - | - | - | - |
| Sfide - vista | Sì | Sì | Sì |
| Sfide: creare o modificare | Sì | Sì | No |
| Sfide - Elimina | Sì | Sì | No |
| Problematiche: pubblicare, annullare la pubblicazione o archiviare | Sì | Sì | No |
| Problemi - generazione di percorsi | Sì | Sì | No |
| Configurazione organizzazione principale - vista | Sì | Sì | No |
| Configurazione organizzazione principale: creazione o modifica | Sì | Sì | No |
| Configurazione organizzazione principale - Elimina | Sì | No | No |
| Configurazione premio: visualizzazione, esclusi i valori sensibili | Sì | Sì | No |
| Configurazione premio: scrittura o accesso ai valori sensibili | Sì | No | No |
| Configurazione evento - vista | Sì | Sì | No |
| Configurazione evento - scrittura | Sì | No | No |
| Catalogo prodotti - visualizza | Sì | Sì | Sì |
| Catalogo prodotti: importare o modificare | Sì | No | No |
| Approfondimenti - visualizza | Sì | Sì | Sì |
| Approfondimenti: scrittura o aggiornamento della configurazione KPI | Sì | No | No |

## Ambito ruolo predefinito {#default-role-scope}

>[!IMPORTANT]
>
>I ruoli fedeltà predefiniti hanno ambito solo per la sandbox **Prod**.

Per concedere agli utenti l’accesso a una sandbox non di produzione, ad esempio una sandbox di staging o di sviluppo, crea un ruolo personalizzato per tale sandbox e assegna le stesse autorizzazioni del ruolo predefinito corrispondente.

## Autorizzazioni disponibili per i ruoli personalizzati {#custom-role-permissions}

Quando crei un ruolo personalizzato per una sandbox non di produzione, seleziona una delle autorizzazioni seguenti. Per replicare un ruolo predefinito, consulta le autorizzazioni elencate nella sezione relativa al ruolo precedente.

| Autorizzazione | Descrizione |
| - | - |
| Gestire le sfide di fedeltà | Operazioni di verifica complete: creazione, modifica, eliminazione, pubblicazione, annullamento della pubblicazione, archiviazione e attivazione della generazione di percorsi |
| Sviluppare problemi di fedeltà | Crea e modifica le sfide tramite API. Le azioni di eliminazione e del ciclo di vita non sono consentite |
| Visualizza le sfide di fedeltà | Visualizza solo le sfide |
| Gestisci configurazione principale fedeltà | Creare, modificare ed eliminare la configurazione dell’organizzazione principale |
| Configurare la configurazione principale del programma fedeltà | Crea e modifica la configurazione dell’organizzazione principale. Eliminazione non consentita |
| Gestisci configurazione avanzata fedeltà | Gestisce gli endpoint di ricompensa e le impostazioni di trasformazione degli eventi, incluso l&#39;accesso in lettura/scrittura ai valori delle credenziali sensibili |
| Visualizza configurazione premio fedeltà | Visualizzare i provider di premi, le definizioni di premi e i proxy di premio. I valori sensibili sono esclusi |
| Visualizza configurazione evento fedeltà | Visualizzare le definizioni degli eventi e le mappature della trasformazione degli eventi |
| Gestione catalogo prodotti fedeltà | Visualizza, importa da CSV e modifica le voci del catalogo dei prodotti, incluse inclusioni ed esclusioni; monitora lo stato del processo di importazione |
| Visualizza catalogo prodotti fedeltà | Visualizzare le voci del catalogo dei prodotti e lo stato del processo di importazione. Le azioni di caricamento e modifica non sono consentite |
| Gestisci informazioni sulla fedeltà | Visualizzare approfondimenti, aggiornare la configurazione dei KPI e attivare la pipeline di approfondimenti |
| Sviluppa Approfondimenti Fedeltà | Visualizza i dati di insights e aggiorna le schede di insight |
| Visualizza informazioni sulla fedeltà | Visualizza solo schede insight generate dall’intelligenza artificiale, dati vitali sullo stato di salute e dati sulle prestazioni della sfida |

## Assegna ruoli agli utenti {#assign-roles}

>[!IMPORTANT]
>
>Solo gli amministratori di prodotto e di sistema possono gestire utenti, gruppi e ruoli.

Adobe Admin Console supporta due approcci per l’associazione di ruoli agli utenti.

### Assegnare gli utenti direttamente a un ruolo {#assign-users-directly}

Aggiungere singoli utenti direttamente a un ruolo. Questo approccio è ideale per piccoli team o assegnazioni una tantum.

### Utilizzare i gruppi di utenti {#use-user-groups}

Crea un gruppo di utenti, quindi assegna al gruppo sia utenti che un ruolo. Questo approccio è ideale per gestire l’accesso per reparto o funzione su larga scala.

Per istruzioni dettagliate sulla gestione di ruoli, gruppi e utenti, consulta la documentazione sul controllo degli accessi a Adobe Journey Optimizer:

* [Gestire utenti e ruoli](../administration/permissions.md)
* [Autorizzazioni incorporate](../administration/ootb-permissions.md)

## Risoluzione dei problemi di accesso {#troubleshooting}

Se un utente non può accedere a Sfide fedeltà o a una funzione correlata, verifica quanto segue:

* L’utente viene assegnato a un ruolo Fedeltà.
* Il ruolo include la sandbox in cui è abilitata l’opzione Sfide di fedeltà.
* Il ruolo include l&#39;autorizzazione necessaria per l&#39;azione che l&#39;utente sta tentando di eseguire.
* Per le sandbox non di produzione, è stato creato un ruolo personalizzato per tale sandbox.
* L’organizzazione e la sandbox sono abilitate per le sfide di fedeltà.

Se i problemi di accesso persistono dopo l’aggiornamento delle autorizzazioni, contatta il rappresentante Adobe.
