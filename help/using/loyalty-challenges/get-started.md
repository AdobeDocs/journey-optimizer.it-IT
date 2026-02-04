---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle sfide di fedeltà
description: Scopri come creare e gestire le sfide di fidelizzazione in Adobe Journey Optimizer per creare programmi di fidelizzazione coinvolgenti.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%

---


# Introduzione alle sfide di fedeltà {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* **Introduzione alle sfide di fidelizzazione** ◀︎ **Sei qui** - Panoramica, flusso di lavoro, prerequisiti
* [Accedere alle sfide di fidelizzazione](access-loyalty-challenges.md) - Inventario e filtro
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Informazioni sulle sfide di fedeltà"
>abstract="Sfide di fidelizzazione consente di creare offerte di coinvolgimento personalizzate che motivano i clienti a completare azioni specifiche e a ricevere premi."

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

## Panoramica {#overview}

Sfide relative alla fedeltà offre una soluzione completa per la creazione di programmi fedeltà su larga scala, dalla definizione di attività e milestone alla distribuzione di contenuti e al tracciamento delle prestazioni su tutti i canali. Puoi creare tre tipi di esperienze di sfida, configurare premi, inviare notifiche multicanale nelle fasi principali del ciclo di vita e monitorare le prestazioni tramite percorsi generati automaticamente, mantenendo al contempo l’integrazione con il sistema di gestione della fedeltà esterno.

## Funzionalità principali {#key-capabilities}

Utilizzare le sfide di fidelizzazione per:

* **Creare tre tipi di problemi**:
   * **Standard**: i clienti completano un numero qualsiasi di attività per ottenere premi
   * **Streak**: i clienti completano la stessa attività più volte consecutivamente
   * **Sequenziale**: i clienti completano le attività in un ordine specifico

* **Progetta contenuto sfida**: utilizza le schede di contenuto Journey Optimizer per creare la rappresentazione visiva della sfida sui dispositivi dei clienti. Le schede dei contenuti mostrano le informazioni sulla sfida, l’avanzamento e i premi.

* **Imposta requisiti attività**: definisci cosa devono fare i clienti per ottenere premi, tra cui:
   * Tipi di attività (acquisto, importo spesa, visita, coinvolgimento, eventi personalizzati)
   * Quantità richiesta
   * Inclusioni/esclusioni di prodotti tramite SKU, categorie o attributi
   * Attributi e condizioni personalizzati

* **Configura premi**: definisci i premi ottenuti dai clienti al completamento dell&#39;attività (premi progressivi) o dopo aver completato l&#39;intera sfida (premi finali).

* **Inviare notifiche multicanale**: consegna di messaggi su più canali (in-app, e-mail, push) in fasi chiave:
   * **Lancio**: quando inizia la richiesta di verifica
   * **In corso**: quando i clienti sono tra di loro
   * **Completo**: quando i clienti finiscono la sfida

* **Monitoraggio delle prestazioni**: monitora i percorsi generati automaticamente e rivedi le prestazioni della verifica tramite rapporti incorporati.

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

## Prerequisiti {#prerequisites}

Prima di utilizzare le sfide di fedeltà, assicurati di disporre di:

### Configurazione dell’acquisizione dati {#data-ingestion}

Le sfide relative alla fedeltà si basano sui dati acquisiti tramite i connettori di origine di Experience Platform per monitorare l’avanzamento dei clienti e il completamento delle attività.

1. **Configurare un connettore di origine supportato**: attualmente il connettore Capillary è generalmente disponibile. Sono pianificati connettori aggiuntivi.

2. **Convalida acquisizione dati**: assicurati che gli eventi fedeltà e i dati dei clienti vengano trasmessi ad Experience Platform e siano disponibili in Journey Optimizer.

Per istruzioni dettagliate, consulta:

* [Documentazione origini Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/sources/home)
* [Configurare i connettori di origine in Journey Optimizer](../start/get-started-sources.md)

### Autorizzazioni richieste {#required-permissions}

Per utilizzare le sfide di fidelizzazione, è necessario disporre delle autorizzazioni appropriate in Journey Optimizer. Se non riesci ad accedere alla funzione, contatta l’amministratore.

### Tipi di pubblico di destinazione {#target-audiences}

Crea dei tipi di pubblico target in Experience Platform prima di creare delle sfide. Puoi selezionare i tipi di pubblico esistenti, ma non puoi crearne di nuovi dall’interfaccia utente Sfide fedeltà.

## Limitazioni importanti {#limitations}

* **Nessun sistema di contabilità generale**: le sfide di fidelizzazione non tengono traccia dei valori monetari o dei saldi dei punti. Quando i clienti completano una sfida e ottengono un premio, Journey Optimizer chiama il sistema di gestione della fedeltà esterno per gestire l’allocazione di punti.

* **Solo selezione del pubblico**: puoi selezionare tipi di pubblico esistenti ma non puoi crearne di nuovi dall&#39;interfaccia utente Sfide fedeltà.

## Passaggi successivi {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Accedere Alle Sfide Di Fedeltà</strong></a>
    </div>
    <p>
    <em>Scopri come accedere alle sfide di inventario e filtro</em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>Crea problemi</strong></a>
    </div>
    <p>
    <em>Crea e configura la prima sfida fedeltà</em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>Gestire le sfide</strong></a>
    </div>
    <p>
    <em>Modificare, monitorare e ottimizzare le sfide</em>
    <p>
  </td>
</tr>
</table>
