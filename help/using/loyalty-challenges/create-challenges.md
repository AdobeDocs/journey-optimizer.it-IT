---
solution: Journey Optimizer
product: journey optimizer
title: Creare problemi di fidelizzazione
description: Scopri come creare e configurare le sfide relative alla fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: 831809b4c1dd19fdaeeb646695f606c02ec21265
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---


# Creare le sfide {#create-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* [Accedere alle sfide di fidelizzazione](access-loyalty-challenges.md) - Inventario e filtro
* **Crea problemi** ◀︎ **Sei qui** - Genera e configura problemi
* [Crea attività](create-tasks.md) - Definisci le attività di verifica
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Come funziona {#how-it-works}

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

La creazione e il lancio di una sfida di fidelizzazione segue questo flusso di lavoro:

1. **Crea una sfida** - Definisci le proprietà della sfida di base, tra cui nome, tipo (Standard, Streak o Sequenziale), pubblico e intervallo di date.

1. **Aggiungi attività** - Definisci le azioni specifiche che i clienti devono completare, inclusi i tipi di attività (acquisto, spesa, visita, ecc.), le quantità, i filtri dei prodotti e i premi.

1. **Progetta schede di contenuto** - Crea la rappresentazione visiva della tua sfida utilizzando le schede di contenuto Journey Optimizer visualizzate sui dispositivi dei clienti.

1. **Configura messaggi** (facoltativo): configura messaggi multicanale (in-app, e-mail, push, SMS) per le fasi chiave: avvio, in corso e completamento.

1. **Rivedi e pubblica** - Verifica la tua sfida con i profili di test, quindi pubblicala per renderla disponibile al pubblico di destinazione.

## Crea la sfida {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

Per creare una nuova sfida di fedeltà:

1. Passa a **[!UICONTROL Sfide fedeltà]** in Journey Optimizer.

1. Selezionare la scheda **[!UICONTROL Sfide]**.

1. Seleziona **[!UICONTROL Crea sfida]**.

1. Configura le proprietà di verifica:

   **Nome sfida**: immetti un nome descrittivo per la sfida. Questo nome viene visualizzato nell’inventario delle sfide e consente di identificare la sfida.

   **Tipo di verifica**: selezionare uno dei tipi seguenti:
   * **[!UICONTROL Standard]**: i clienti completano un numero specificato di attività in qualsiasi ordine
   * **[!UICONTROL Streak]**: i clienti completano la stessa attività più volte consecutivamente
   * **[!UICONTROL Sequenziale]**: i clienti completano le attività in un ordine definito

   **Pubblico di destinazione**: seleziona il segmento di pubblico che definisce chi può partecipare a questa sfida. Devi creare dei tipi di pubblico in Experience Platform prima di creare delle sfide. Per ulteriori informazioni, vedere [Introduzione ai tipi di pubblico](../audience/about-audiences.md).

   **Data di inizio**: imposta quando la sfida diventa disponibile per i clienti.

   **Data di fine**: imposta quando la richiesta scade e non accetta più nuovi completamenti.

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### Aggiungi attività {#add-tasks}

Le attività definiscono le azioni o i milestone specifici che i clienti devono completare per ottenere premi. Puoi configurare i tipi di attività (acquisto, spesa, visita, coinvolgimento, eventi personalizzati), le quantità, i filtri dei prodotti e i premi.

A seconda del tipo di sfida, i clienti completano le attività in modo diverso:

* **Sfide standard**: completa un numero specificato di attività in qualsiasi ordine
* **Sfide in streaming**: completa la stessa attività più volte consecutivamente
* **Sfide sequenziali**: attività completate in un ordine definito

Per aggiungere attività alla tua richiesta, seleziona **[!UICONTROL Aggiungi attività]** nella sezione Attività e configura le proprietà dell&#39;attività.

Per istruzioni dettagliate sulla creazione e la configurazione delle attività, vedi [Creare le attività](create-tasks.md).

### Configurare le schede di contenuto {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

Le schede di contenuto forniscono una rappresentazione visiva della sfida sui dispositivi dei clienti, visualizzando informazioni sulla sfida, lo stato di avanzamento e i premi. Ulteriori informazioni sulle [schede di contenuto](../content-card/create-content-card.md).

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

Per configurare le schede di contenuto per la sfida:

1. Nell&#39;editor delle sfide, passa alla sezione **[!UICONTROL Schede di contenuto]**.

1. Seleziona **[!UICONTROL Crea scheda contenuto]** o scegli un modello esistente.

1. Progettare la scheda di contenuto:
   * Aggiungere immagini, testo ed elementi di branding
   * Includi [token di personalizzazione](../personalization/personalization-syntax.md) per visualizzare informazioni specifiche per il cliente
   * Mostra gli indicatori di avanzamento delle sfide
   * Visualizza premi e incentivi

1. Configura quando viene visualizzata la scheda di contenuto:
   * **Inizio sfida**: mostra quando la sfida diventa disponibile
   * **In corso**: visualizzazione durante la partecipazione attiva dei clienti
   * **Completamento**: mostra dopo che i clienti hanno completato tutte le attività

1. Visualizza l’anteprima della scheda di contenuto su diversi dispositivi per garantire una visualizzazione corretta.

1. Salva la configurazione della scheda di contenuto.

Per ulteriori informazioni sulla progettazione e la personalizzazione delle schede di contenuto, vedere [Progettare le schede di contenuto](../content-card/design-content-card.md).

### Configurare la messaggistica {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

Configurare messaggi multicanale per coinvolgere i clienti nelle fasi chiave del ciclo di vita della sfida.

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

Per configurare la messaggistica per la sfida:

1. Nell&#39;editor delle sfide, passa alla sezione **[!UICONTROL Messaggistica]**.

1. Configurare i messaggi per ogni fase del ciclo di vita:

   **Messaggi di avvio** - Avvisa i clienti all&#39;avvio della richiesta di verifica:
   * Seleziona canali: [In-app](../in-app/get-started-in-app.md), [e-mail](../email/get-started-email.md), [notifica push](../push/get-started-push.md) o [SMS](../sms/get-started-sms.md)
   * Progetta il messaggio con i dettagli della sfida e call-to-action
   * Imposta tempistica: invia immediatamente quando la sfida diventa attiva o pianifica per un orario specifico

   **Messaggi in corso** - Mantenere i clienti coinvolti durante la verifica:
   * Definire le condizioni di attivazione (ad esempio, completamento al 50%, completamento di attività specifiche)
   * Crea messaggi di promemoria per incoraggiare la partecipazione continua
   * Includi aggiornamenti sull’avanzamento e passaggi successivi

   **Messaggi di completamento** - Celebra il successo e consegna dei premi:
   * Congratulazioni ai clienti per aver completato la sfida
   * Conferma allocazione premi
   * Fornire istruzioni per la richiesta di premi
   * Suggerisci sfide o azioni future

Per ulteriori informazioni sulla creazione di messaggi per canali specifici, consulta:

* [Documentazione dei messaggi in-app](../in-app/get-started-in-app.md)
* [Documentazione dei messaggi e-mail](../email/get-started-email.md)
* [Documentazione delle notifiche push](../push/get-started-push.md)
* [Documentazione sui messaggi SMS](../sms/get-started-sms.md)

## Rivedi e pubblica la sfida {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

Prima di pubblicare la sfida:

1. **Controlla tutti i componenti**: verifica proprietà della sfida, attività, premi, schede di contenuto e configurazioni di messaggistica.

1. **Verifica l&#39;esperienza**: utilizza [profili di test](../test-approve/test-profiles.md) per convalidare la visualizzazione della scheda dei contenuti e il comportamento dell&#39;attivazione delle attività.

1. **Pubblica**: seleziona **[!UICONTROL Pubblica]** per rendere la sfida disponibile per il pubblico di destinazione.

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

Quando si pubblica una richiesta di verifica, Journey Optimizer crea automaticamente un [percorso](../building-journeys/journey-gs.md) in stato Bozza. Il percorso generato automaticamente viene visualizzato nell&#39;inventario del percorso con il formato del nome &quot;Sfida: [Nome sfida]&quot;.

Per rendere la sfida disponibile ai clienti:

1. Passa all&#39;inventario **[!UICONTROL Percorsi]** in Journey Optimizer.

1. Individua il percorso generato automaticamente (il nome conterrà il prefisso &quot;Challenge:&quot;).

1. [Attiva il percorso](../building-journeys/publishing-the-journey.md).

Il percorso inizia automaticamente alla data di inizio richiesta di verifica specificata.

>[!NOTE]
>
>Il percorso generato automaticamente viene visualizzato nell&#39;inventario del percorso e, se necessario, può essere personalizzato. Tuttavia, le modifiche apportate direttamente al percorso non vengono sincronizzate con la configurazione di verifica.

## Passaggi successivi {#next-steps}

* [Gestire le sfide](manage-challenges.md) - Scopri come modificare, monitorare e ottimizzare le sfide
* [Comprendere le sfide relative alla fedeltà](get-started.md) - Rivedere le funzionalità

