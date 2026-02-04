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
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---


# Introduzione alle sfide di fedeltà {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* **Introduzione alle sfide di fidelizzazione** ◀︎ **Sei qui** - Panoramica, flusso di lavoro, prerequisiti
* [Accedere alle sfide di fidelizzazione](access-loyalty-challenges.md) - Inventario e filtro
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* [Crea attività](create-tasks.md) - Definisci le attività di verifica
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Panoramica {#overview}

Le sfide relative alla fedeltà offrono una soluzione completa per la creazione di programmi fedeltà su larga scala, dalla definizione di attività e obiettivi intermedi alla distribuzione di contenuti e al tracciamento delle prestazioni su tutti i canali.

Puoi creare tre tipi di esperienze di sfida:

* **Sfide standard**: i clienti completano un numero specificato di attività in qualsiasi ordine
* **Sfide**: i clienti completano la stessa attività più volte di seguito
* **Sfide sequenziali**: i clienti completano le attività in un ordine definito

Con le sfide della fidelizzazione, è possibile configurare i premi, inviare notifiche multicanale nelle fasi principali del ciclo di vita e monitorare le prestazioni tramite percorsi generati automaticamente, mantenendo al contempo l&#39;integrazione con il sistema di gestione della fidelizzazione esterno.

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## Come funziona {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

La creazione e il lancio di una sfida di fidelizzazione segue questo flusso di lavoro:

1. **Configura l&#39;acquisizione dei dati**. Configura i connettori di origine di Experience Platform (ad esempio il connettore Capillary) per acquisire i dati dell&#39;evento fedeltà che tengono traccia delle azioni dei clienti e dell&#39;avanzamento. Questi dati consentono il rilevamento delle sfide e il completamento delle attività.

1. **Crea una sfida** - Definisci le proprietà della sfida di base, tra cui nome, tipo (Standard, Streak o Sequenziale), pubblico e intervallo di date. Consulta [Creare le sfide](create-challenges.md) per i passaggi dettagliati.

1. **Aggiungi attività** - Definisci le azioni specifiche che i clienti devono completare, inclusi i tipi di attività (acquisto, spesa, visita, coinvolgimento, eventi personalizzati), le quantità, i filtri dei prodotti e i premi. Per istruzioni dettagliate, consulta [Creare attività](create-tasks.md).

1. **Progetta schede di contenuto** - Crea la rappresentazione visiva della tua sfida utilizzando le [schede di contenuto](../content-card/get-started-content-card.md) di Journey Optimizer visualizzate sui dispositivi del cliente. Le schede dei contenuti mostrano informazioni sulla sfida, l’avanzamento e i premi.

1. **Configura messaggi** (facoltativo) - Configura messaggi multicanale ([in-app](../in-app/get-started-in-app.md), [e-mail](../email/get-started-email.md), [push](../push/get-started-push.md)) per le fasi chiave del ciclo di vita: avvio, in corso e completamento.

1. **Rivedi e pubblica** - Verifica la tua sfida con [profili di test](../test-approve/test-profiles.md), quindi pubblicala per renderla disponibile al pubblico di destinazione.

1. **Attiva percorso** - Quando si pubblica una sfida, Journey Optimizer crea automaticamente un [percorso](../building-journeys/journey-gs.md) in stato Bozza che orchestra la consegna e la messaggistica delle schede di contenuto. Passa all&#39;inventario dei Percorsi, individua il percorso generato automaticamente (denominato &quot;Sfida: [Nome sfida]&quot;) e [attivalo](../building-journeys/publishing-the-journey.md) per rendere la sfida disponibile ai tuoi clienti.

1. **Monitora le prestazioni** - Tieni traccia della partecipazione, dei tassi di completamento, della distribuzione dei premi e del coinvolgimento nei messaggi tramite rapporti incorporati e l&#39;area di lavoro del percorso. Consulta [Gestire le sfide](manage-challenges.md) per informazioni sul monitoraggio.

## Prerequisiti {#prerequisites}

Prima di utilizzare le sfide di fedeltà, assicurati di disporre di:

+++Configurazione dell’acquisizione dati

Le sfide relative alla fedeltà si basano sui dati acquisiti tramite i connettori di origine di Experience Platform per monitorare l’avanzamento dei clienti e il completamento delle attività.

1. **Configurare un connettore di origine supportato**: attualmente il connettore Capillary è generalmente disponibile. Connettori aggiuntivi sono pianificati per le versioni future.

1. **Convalida acquisizione dati**: assicurati che gli eventi fedeltà e i dati dei clienti vengano trasmessi ad Experience Platform e siano disponibili in Journey Optimizer. Verifica che lo schema dati includa i campi necessari per monitorare le azioni e l’avanzamento del cliente.

Per istruzioni dettagliate, consulta:

* [Documentazione origini Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/sources/home)
* [Configurare i connettori di origine in Journey Optimizer](../start/get-started-sources.md)

+++

+++Autorizzazioni richieste

Per utilizzare le sfide di fidelizzazione, è necessario disporre delle autorizzazioni appropriate in Journey Optimizer. Le autorizzazioni necessarie includono:

* Accesso alla funzionalità **[!UICONTROL Sfide fedeltà]**
* Autorizzazioni per la creazione e la gestione di percorsi
* Autorizzazioni per creare e gestire schede di contenuto
* Autorizzazioni per creare e gestire i tipi di pubblico

Se non riesci ad accedere alla funzione o se hai bisogno di autorizzazioni aggiuntive, contatta l’amministratore.

+++

+++Tipi di pubblico di destinazione

Crea dei tipi di pubblico target in Experience Platform prima di creare delle sfide. Questi tipi di pubblico definiscono quali clienti sono idonei a partecipare alle sfide di fidelizzazione. Per ulteriori informazioni su come creare tipi di pubblico, consulta [Introduzione ai tipi di pubblico](../audience/about-audiences.md).

+++

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
    </p>
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
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>Crea attività</strong></a>
    </div>
    <p>
    <em>Definire azioni e premi per le sfide</em>
    </p>
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
    </p>
  </td>
</tr>
</table>
