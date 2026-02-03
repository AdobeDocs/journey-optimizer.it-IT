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
source-git-commit: 7b075996eebd03f0aa812da3ece9cfebef8c65fc
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 3%

---


# Introduzione alle sfide di fedeltà {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

Sfide di fidelizzazione consente di creare offerte di coinvolgimento personalizzate per i clienti, aiutandoti a orchestrare programmi fedeltà su larga scala. Puoi progettare le sfide con attività e obiettivi specifici, premiare i clienti per averli completati e fornire l’esperienza tramite i canali Adobe Journey Optimizer.

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* **Introduzione alle sfide di fidelizzazione** ◀︎ **Sei qui** - Panoramica rapida e passaggi successivi
* [Informazioni sulle sfide relative alla fedeltà](get-started.md) - Caratteristiche, flusso di lavoro, prerequisiti
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

## Panoramica rapida {#quick-overview}

Utilizzare le sfide di fidelizzazione per:

* **Creazione di tre tipi di problemi**: standard (tutte le attività), Streak (attività ripetute) o sequenziale (attività ordinate)
* **Progetta contenuto sfida**: utilizza le schede dei contenuti per visualizzare le sfide sui dispositivi dei clienti
* **Imposta requisiti attività**: definisci azioni quali acquisti, visite o eventi personalizzati con premi
* **Invio di notifiche multicanale**: consegna di messaggi tramite in-app, e-mail e push in fasi chiave
* **Monitoraggio delle prestazioni**: monitora tramite percorsi generati automaticamente e rapporti incorporati

## Come funziona {#how-it-works-overview}

La creazione di una sfida di fidelizzazione segue questo flusso di lavoro:

1. **Configura l&#39;acquisizione dei dati** - Configura i connettori di origine per tenere traccia delle azioni dei clienti
2. **Crea una sfida** - Definisci tipo, pubblico e date
3. **Aggiungi attività** - Configura azioni e premi
4. **Progetta contenuto** - Crea schede di contenuto e messaggi facoltativi
5. **Pubblica** - Journey Optimizer genera e attiva automaticamente un percorso
6. **Monitoraggio** - Tracciamento partecipazione e prestazioni

>[!NOTE]
>
>Il percorso generato automaticamente viene visualizzato nell&#39;inventario del percorso e, se necessario, può essere personalizzato. Tuttavia, le modifiche apportate direttamente al percorso non vengono sincronizzate con la configurazione di verifica.

## Prerequisiti {#prerequisites-overview}

Prima di utilizzare le sfide di fedeltà:

* Configura i connettori di origine di Experience Platform (ad esempio, Capillary) per acquisire i dati dell’evento fedeltà
* Assicurati di disporre delle autorizzazioni appropriate in Journey Optimizer
* Creare tipi di pubblico target in Experience Platform

Per i prerequisiti dettagliati, vedi [Comprendere le sfide relative alla fedeltà](get-started.md#prerequisites).

## Limitazioni importanti {#limitations-overview}

* **Nessun sistema di contabilità generale**: le sfide di fidelizzazione non tengono traccia dei valori monetari o dei saldi dei punti. Journey Optimizer chiama il sistema di gestione della fedeltà esterno per gestire l’allocazione di punti.
* **Solo selezione del pubblico**: puoi selezionare tipi di pubblico esistenti ma non puoi crearne di nuovi dall&#39;interfaccia utente Sfide fedeltà.

## Passaggi successivi {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="get-started.md">
    <img alt="Comprendere" src="../assets/do-not-localize/learn-more-button.svg">
    </a>
    <div>
    <a href="get-started.md"><strong>Comprendere le sfide della fedeltà</strong></a>
    </div>
    <p>
    <em>Informazioni su funzionalità, flusso di lavoro e funzionalità</em>
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
