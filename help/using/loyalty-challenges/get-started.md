---
solution: Journey Optimizer
product: journey optimizer
title: Comprendere le sfide della fedeltà
description: Scopri le funzionalità, il flusso di lavoro e le funzionalità delle sfide di fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 2%

---


# Comprendere le sfide della fedeltà {#understand-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Informazioni sulle sfide di fedeltà"
>abstract="Sfide di fidelizzazione consente di creare offerte di coinvolgimento personalizzate che motivano i clienti a completare azioni specifiche e a ricevere premi."

Sfide di fidelizzazione consente di progettare e distribuire offerte di coinvolgimento personalizzate che motivano i clienti a completare azioni specifiche e a ricevere premi.

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](gs-loyalty-challenges.md) - Panoramica rapida e passaggi successivi
* **Comprendere le sfide relative alla fedeltà** ◀︎ **Sei qui** - Funzionalità, flusso di lavoro, prerequisiti
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

## Panoramica {#overview}

Sfide relative alla fedeltà offre una soluzione completa per la creazione di programmi fedeltà su larga scala, dalla definizione di attività e milestone alla distribuzione di contenuti e al tracciamento delle prestazioni su tutti i canali. Puoi creare tre tipi di esperienze di sfida, configurare premi, inviare notifiche multicanale nelle fasi principali del ciclo di vita e monitorare le prestazioni tramite percorsi generati automaticamente, mantenendo al contempo l’integrazione con il sistema di gestione della fedeltà esterno.

## Come funziona {#how-it-works}

La creazione e il lancio di una sfida di fidelizzazione segue questo flusso di lavoro:

1. **Configura l&#39;acquisizione dei dati**. Configura i connettori di origine di Experience Platform (come Capillary) per acquisire i dati dell&#39;evento fedeltà che tengono traccia delle azioni dei clienti e dell&#39;avanzamento.

2. **Crea una sfida** - Definisci le proprietà della sfida di base, tra cui nome, tipo (Standard, Streak o Sequenziale), pubblico e intervallo di date.

3. **Aggiungi attività** - Definisci le azioni specifiche che i clienti devono completare, inclusi i tipi di attività (acquisto, spesa, visita, ecc.), le quantità, i filtri dei prodotti e i premi.

4. **Progetta schede di contenuto** - Crea la rappresentazione visiva della tua sfida utilizzando le schede di contenuto Journey Optimizer visualizzate sui dispositivi dei clienti.

5. **Configurazione della messaggistica** (facoltativo): configurazione di messaggi multicanale (in-app, e-mail, push) per le fasi chiave: avvio, in corso e completamento.

6. **Rivedi e pubblica** - Verifica la tua sfida con i profili di test, quindi pubblicala per renderla disponibile al pubblico di destinazione.

7. **percorso generato automaticamente** - Quando si pubblica, Journey Optimizer crea automaticamente un percorso che orchestra la consegna e la messaggistica delle schede di contenuto.

8. **Attiva percorso** - Il percorso generato automaticamente si attiva alla data di inizio della sfida e gestisce tutte le interazioni dei clienti.

9. **Monitora le prestazioni** - Tieni traccia della partecipazione, dei tassi di completamento, della distribuzione dei premi e del coinvolgimento nei messaggi tramite rapporti incorporati e l&#39;area di lavoro del percorso.

>[!NOTE]
>
>Il percorso generato automaticamente viene visualizzato nell&#39;inventario del percorso e, se necessario, può essere personalizzato. Tuttavia, le modifiche apportate direttamente al percorso non vengono sincronizzate con la configurazione di verifica.

## Funzionalità principali {#key-capabilities}

Utilizzare le sfide di fidelizzazione per:

* **Creare tre tipi di problemi**:
   * **Standard**: i clienti completano un numero qualsiasi di attività per ottenere premi.
   * **Streak**: i clienti completano la stessa attività più volte.
   * **Sequenziale**: i clienti completano le attività in un ordine specifico.

* **Progetta contenuto sfida**: utilizza le schede di contenuto Journey Optimizer per creare la rappresentazione visiva della sfida sui dispositivi dei clienti. Le schede dei contenuti mostrano le informazioni sulla sfida, l’avanzamento e i premi sul dispositivo del cliente.

* **Imposta requisiti attività**: definisci cosa devono fare i clienti per ottenere premi, tra cui:
   * Tipi di attività (acquisto, importo spesa, visita, ecc.)
   * Quantità richiesta
   * Inclusioni/esclusioni di prodotti tramite SKU
   * Attributi e condizioni personalizzati

* **Configura premi**: definisci i premi che i clienti ottengono al completamento dell&#39;attività o dopo aver completato l&#39;intera sfida

* **Invia notifiche**: consegna di messaggi su più canali (in-app, e-mail, push) in fasi chiave:
   * **Lancio**: quando inizia la richiesta di verifica
   * **In corso**: quando i clienti sono tra di loro
   * **Completo**: quando i clienti finiscono la sfida

* **Tieni traccia delle prestazioni**: monitora i percorsi generati automaticamente e rivedi le prestazioni della verifica

### Limitazioni importanti {#limitations}

* **Nessun sistema di contabilità generale**: le sfide di fidelizzazione non tengono traccia dei valori monetari o dei saldi dei punti. Quando i clienti completano una sfida e ottengono un premio, Journey Optimizer chiama il sistema di gestione della fedeltà esterno per gestire l’allocazione di punti.

* **Solo selezione del pubblico**: puoi selezionare tipi di pubblico esistenti ma non puoi crearne di nuovi dall&#39;interfaccia utente Sfide fedeltà.

## Prerequisiti {#prerequisites}

Prima di utilizzare le sfide di fedeltà, assicurati di disporre di:

### Configurazione dell’acquisizione dati {#data-ingestion}

Le sfide relative alla fedeltà si basano sui dati acquisiti tramite i connettori di origine di Experience Platform per monitorare l’avanzamento dei clienti e il completamento delle attività.

1. **Configurare un connettore di origine supportato**: attualmente il connettore Capillary è generalmente disponibile. Sono pianificati connettori aggiuntivi.

2. **Convalida acquisizione dati**: assicurati che gli eventi fedeltà e i dati dei clienti vengano trasmessi ad Experience Platform e siano disponibili in Journey Optimizer.

Per istruzioni dettagliate, consulta:

* [Documentazione origini Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Configurare i connettori di origine in Journey Optimizer](../start/get-started-sources.md)

### Autorizzazioni richieste {#required-permissions}

Per utilizzare le sfide di fidelizzazione, è necessario disporre delle autorizzazioni appropriate in Journey Optimizer. Se non riesci ad accedere alla funzione, contatta l’amministratore.

## Accedere alle sfide di fedeltà {#access}

Per accedere alle sfide di fedeltà:

1. In Adobe Journey Optimizer, seleziona **[!UICONTROL Sfide fedeltà]** nel menu di navigazione a sinistra.

2. Nell&#39;inventario Sfide fedeltà vengono visualizzate tutte le sfide esistenti con informazioni quali:
   * Nome e descrizione della sfida
   * Stato (Bozza, Live, Arrestato, ecc.)
   * Tipo di sfida (Standard, Streak, Sequenziale)
   * Date di inizio e di fine
   * Data ultima modifica

3. Seleziona **[!UICONTROL Crea sfida]** per iniziare a creare una nuova sfida.

### Problemi di ricerca e filtro {#search-filter}

Utilizza le funzionalità di ricerca e filtro per individuare rapidamente le problematiche specifiche:

* **Ricerca**: immetti il nome o le parole chiave della richiesta nel campo Ricerca
* **Filtra per stato**: Bozza, Pianificato, Live, Completato, Interrotto o Archiviato
* **Filtro per tipo**: problemi standard, in streaming o sequenziali
* **Filtra per data**: problemi entro un intervallo di date specifico
* **Filtra per tag**: problemi con tag specifici applicati

## Passaggi successivi {#next-steps}

Ora che conosci le Sfide relative alla fedeltà, scopri come creare la tua prima sfida:

* [Creare le sfide](create-challenges.md)
* [Gestire le sfide](manage-challenges.md)
