---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai percorsi
description: 'Introduzione ai percorsi: informazioni sui tipi di percorso, flusso di lavoro, funzionalità e best practice per creare esperienze cliente personalizzate in Adobe Journey Optimizer'
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: percorso, informazioni, guida introduttiva, unitario, leggi pubblico, qualificazione del pubblico, evento di business, in tempo reale, pianificato, batch, attivato da eventi, flusso di lavoro, orchestrazione, personalizzazione, multicanale
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 522dba0516268a17e72f56c0f28205ba60709d78
workflow-type: ht
source-wordcount: '1448'
ht-degree: 100%

---


# Introduzione ai percorsi{#jo-general-principle}

Adobe Journey Optimizer consente di creare percorsi cliente personalizzati e a più passaggi che si adattano in tempo reale al comportamento e alle esigenze del pubblico. Utilizzando un’area di lavoro intuitiva basata su trascinamento, puoi orchestrare messaggi e azioni tra più canali, sfruttando i dati contestuali e il targeting del pubblico per il massimo impatto.

Questa guida fornisce una roadmap chiara per aiutarti a comprendere le nozioni di base del percorso, scegliere il tipo di percorso adatto al tuo caso d’uso e progettare con sicurezza percorsi che forniscano esperienze cliente significative e tempestive.

## Che cosa sono i percorsi?

I **percorsi** sono esperienze cliente automatizzate e a più passaggi che orchestrano interazioni personalizzate in canali diversi in risposta al comportamento del cliente, a eventi di business o a campagne pianificate.

Utilizza [!DNL Journey Optimizer] per:

* Creare casi d’uso di **orchestrazione in tempo reale** utilizzando dati contestuali memorizzati negli eventi o nelle origini dati
* Progettare **scenari avanzati a più passaggi** che rispondono in modo dinamico al comportamento del cliente e agli eventi di business
* Consegnare **1:1 esperienze personalizzate** su larga scala tramite e-mail, push, SMS, in-app, web e altro ancora

![Interfaccia di designer percorsi con riquadro palette, area di lavoro e proprietà](assets/journey38.png)

➡️ **Vuoi iniziare subito?** [Crea il tuo primo percorso](journey-gs.md) in 5 minuti.

### Percorsi o campagne: quando utilizzare l’uno o l’altra {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer offre tre approcci per raggiungere la clientela: **Percorsi** (1:1 orchestrazione in tempo reale), **Campagne** (consegna semplice in batch o attivata da API) e **Campagne orchestrate** (flussi di lavoro con aree di lavoro in batch con dati di più entità).

**Decisione rapida:**

* Utilizza **Percorsi** per esperienze con più passaggi basate sul comportamento, in cui ogni cliente procede al proprio ritmo
* Utilizza **Campagne Azione/API** per la consegna di messaggi semplice, pianificata o attivata ai tipi di pubblico
* Utilizza **Campagne orchestrate** per flussi di lavoro in batch complessi che richiedono segmentazione di più entità e conteggi pre-invio esatti

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## Scegliere il tipo di percorso {#journey-types}

Adobe Journey Optimizer supporta quattro tipi di percorsi, ciascuno progettato per diversi meccanismi di ingresso e scenari aziendali:

* **Percorsi unitari**: esperienze in tempo reale attivate da eventi (conferme d’ordine, e-mail di benvenuto)
* **Percorsi Leggi pubblico**: comunicazioni in batch pianificate ai segmenti di pubblico (newsletter, campagne promozionali)
* **Percorsi di qualificazione del pubblico**: risposte in tempo reale alle modifiche di appartenenza al pubblico (aggiornamenti di VIP, ricoinvolgimento)
* **Percorsi di eventi di business**: condizioni aziendali che interessano più clienti (avvisi di inventario, vendite flash)

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## Creare con designer percorsi {#journey-designer}

Il **[designer percorsi](using-the-journey-designer.md)** è l’area di lavoro visiva per la creazione di esperienze cliente. Grazie all’intuitiva interfaccia di trascinamento, è possibile orchestrare ogni passaggio del percorso senza scrivere codice.

![Interfaccia di designer percorsi con riquadro palette, area di lavoro e proprietà](assets/journey38.png)

### Cosa puoi fare nel designer:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

**Definire i punti di ingresso**

Scegli come si verificherà l’ingresso nel percorso: attraverso un evento, un segmento di pubblico o la qualificazione del pubblico.

[Informazioni sulla gestione degli ingressi](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=it)

**Inviare messaggi**

Utilizza azioni di canale incorporate per e-mail, push, SMS/MMS, in-app, web e altro, tutte progettate in Journey Optimizer.

[Aggiungere messaggi nei percorsi](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=it)

**Aggiungere logica e condizioni**

Crea un ramo del percorso in base agli attributi profilo, all’appartenenza al pubblico o a eventi in tempo reale.

[Condizioni d’uso](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=it)

**Sfruttare i dati**

Utilizza dati contestuali provenienti da eventi, Adobe Experience Platform o servizi API di terze parti.

[Utilizzare origini dati](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

**Connettere sistemi esterni**

Crea azioni personalizzate per integrare sistemi di terze parti per l’invio di messaggi o l’attivazione di flussi di lavoro.

[Utilizzare le azioni personalizzate](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=it)

**Aggiungere attività di orchestrazione**

Utilizza tempi di attesa, salti, aggiornamenti del profilo e gestione del pubblico per creare flussi sofisticati.

[Esplorare tutte le attività](about-journey-activities.md)
:::

::::

➡️ **Apprendimento pratico:** [guarda il video del designer percorsi](#video) o [esplora casi d’uso end-to-end](jo-use-cases.md)

## Flusso di lavoro di creazione del percorso {#workflow}

La creazione di percorsi di successo segue un processo chiaro e ripetibile. Di seguito è riportato il flusso di lavoro dettagliato:

**1. Pianifica** → **2. Progetta** → **3. Testa** → **4. Pubblica** → **5. Monitora** → **6. Ottimizza**

### &#x200B;1. Pianificare il percorso {#plan}

Prima di aprire il designer, chiarisci gli obiettivi:

* **Qual è l’obiettivo?** (ad esempio, per dare il benvenuto alla nuova clientela, coinvolgi gli utenti inattivi)
* **Chi è il pubblico?** (segmento specifico, singoli utenti guidati da eventi)
* **Quale tipo di percorso è adatto?** (consulta [Tipi di percorso](#journey-types) sopra)
* **Quali canali utilizzerai?** (e-mail, push, SMS, ecc.)

### &#x200B;2. Progettare nell’area di lavoro {#design}

Utilizza il designer percorsi per generare il flusso:

* **Imposta le condizioni di ingresso**: definisci come verrà determinato l’ingresso dei profili (evento, pubblico, qualificazione)
* **Aggiungi la logica di orchestrazione**: include tempi di attesa, condizioni e punti decisionali
* **Configura i messaggi**: progetta le comunicazioni o sfrutta i modelli esistenti
* **Configura le azioni**: configura le azioni incorporate o personalizzate da eseguire
* **Definisci i criteri di uscita**: specifica quando e come i profili completano il percorso

[Scopri come utilizzare il designer percorsi →](using-the-journey-designer.md)

### &#x200B;3. Testare prima della pubblicazione {#test}

Testa sempre il percorso per individuare problemi prima che li riceva la clientela:

* Utilizza la **modalità test** per simulare il percorso con profili di test
* Utilizza l’**esecuzione di prova** per visualizzare in anteprima l’esecuzione del percorso senza influire sui dati reali o inviare messaggi
* Verifica che tutte le condizioni, i messaggi e le azioni funzionino come previsto
* Controlla tempistica, flussi di dati e personalizzazione

[Testa il percorso →](testing-the-journey.md) | [Informazioni sull’esecuzione di prova →](journey-dry-run.md)

### &#x200B;4. Pubblicare il percorso {#publish}

Una volta completato il test, pubblica per rendere live il percorso:

* Rivedi le impostazioni e le proprietà finali
* Pubblica per attivare per clientela reale
* Nota: i percorsi live possono essere interrotti ma non modificati (è necessario creare una nuova versione)

[Pubblica il percorso →](publish-journey.md)

### &#x200B;5. Monitorare le prestazioni {#monitor}

Tieni traccia delle prestazioni del percorso nel mondo reale:

* Visualizza rapporti e analisi del percorso
* Monitora l’ingresso, il completamento e i tassi di errore
* Configura gli avvisi per i problemi critici

[Monitora e segnala →](report-journey.md) | [Configura gli avvisi →](../reports/alerts.md)

### &#x200B;6. Ottimizzare ed eseguire l’iterazione {#optimize}

Utilizza le informazioni per migliorare:

* Analizza le metriche di coinvolgimento e i tassi di conversione
* Testa l’ottimizzazione del tempo di invio
* Crea nuove versioni di percorso con miglioramenti
* Utilizza consigli basati sull’intelligenza artificiale

[Ottimizza i percorsi →](optimize.md) | [Ottimizzazione del tempo di invio →](send-time-optimization.md)

➡️ **Vuoi iniziare?** [Crea il primo percorso ora →](journey-gs.md)

## Casi d’uso del mondo reale {#use-cases}

Scopri dagli esempi pratici che dimostrano come applicare concetti di percorso per risolvere le sfide di marketing comuni:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=it)

**Dare il benvenuto a chi si iscrive**

Quando un cliente si iscrive al servizio, attiva un percorso di benvenuto che lo incoraggi a completare i passaggi di onboarding.

[Visualizza caso d’uso →](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=it)

**Ottimizzazione del tempo di invio**

Utilizza l’intelligenza artificiale per inviare e-mail quando il coinvolgimento del cliente è più probabile, massimizzando i tassi di apertura e clic.

[Visualizza caso d’uso →](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=it)

**Incrementare gradualmente le consegne**

Aumenta gradualmente il volume dei messaggi per migliorare la reputazione dell’invio ed evitare problemi di recapitabilità.

[Visualizza caso d’uso →](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=it)

**Target per giorno feriale**

Invia contenuti diversi in base al giorno della settimana in cui si verifica l’ingresso nel percorso, per migliorarne la rilevanza.

[Visualizza caso d’uso →](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=it)

**Campagne multicanale**

Orchestra esperienze semplici tra canali e-mail, push, SMS e web in un unico percorso.

[Visualizza caso d’uso →](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=it)

**Tutti i casi d’uso**

Esplora la libreria completa dei casi d’uso del percorso con implementazioni dettagliate.

[Sfoglia tutti →](jo-use-cases.md) | [Libreria casi d’uso →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Esplorare le funzionalità del percorso {#capabilities}

Man mano che acquisisci dimestichezza con la creazione del percorso, esplora queste potenti funzionalità per creare esperienze cliente sofisticate:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=it)

**Espressioni avanzate**

Crea condizioni dinamiche e personalizzazione utilizzando l’editor di espressioni per la manipolazione dei dati e la logica complessa.

[Informazioni sulle espressioni](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=it)

**Gestione del fuso orario**

Gestisci i tipi di pubblico globali con regolazioni automatiche del fuso orario e tempi di invio ottimali.

[Gestire i fusi orari](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=it)

**Modalità test ed esecuzione di prova**

Convalida i percorsi con i profili di test prima della pubblicazione e visualizza in anteprima l’esecuzione senza influire sui dati reali.

[Utilizzare l’esecuzione di prova](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=it)

**Copiare nella sandbox**

Duplica i percorsi tra sandbox per semplificare i flussi di lavoro di test e implementazione.

[Copiare i percorsi](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=it)

**Tag e organizzazione**

Utilizza i tag per categorizzare e filtrare i percorsi per una migliore gestione su larga scala.

[Organizzare con i tag](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

**Controllo velocità effettiva**

Limita la velocità effettiva dei messaggi per gestire la reputazione di invio ed evitare di sovraccaricare i sistemi.

[Velocità effettiva di controllo](limit-throughput.md)
:::

::::

[Visualizza tutte le funzionalità del percorso →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Apprendere guardando {#video}

Ottieni un’introduzione visiva ai componenti del percorso e scopri le nozioni di base sulla creazione di percorsi nell’area di lavoro:

>[!VIDEO](https://video.tv.adobe.com/v/3430348?captions=ita&quality=12)

➡️ **Desideri più video?** [Esplora i tutorial video sul percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Domande comuni {#common-questions}

+++ Qual è la differenza tra un percorso e una campagna?

Adobe Journey Optimizer offre tre approcci:

* **Percorsi**: 1:1 orchestrazione in tempo reale in cui ogni profilo percorre i diversi passaggi al proprio ritmo. Consigliato per esperienze guidate dal comportamento e in più passaggi con logica condizionale (ad esempio, onboarding, abbandono del carrello).

* **Campagne (attivate da azioni e API)**: consegna semplice dei messaggi al pubblico, con esecuzione simultanea per tutti i profili, secondo pianificazione o tramite attivatore API. Consigliato per campagne promozionali, newsletter e messaggi transazionali.

* **Campagne orchestrate**: flussi di lavoro in batch con più passaggi e segmentazione complessa utilizzando dati relazionali (profili + prodotti/negozi/prenotazioni). Tutti i profili vengono elaborati con conteggi di pre-invio esatti. Consigliato per promozioni stagionali, lanci di prodotti, campagne che richiedono dati su più entità.

**Differenze chiave**: i percorsi mantengono lo stato dei singoli clienti per le azioni in tempo reale; le campagne con azioni o attivate da API consegnano messaggi semplici in batch; le campagne orchestrate forniscono un’area di lavoro con flusso di lavoro in batch con funzionalità di segmentazione per più entità.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Informazioni sulle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ Posso modificare un percorso live?

Puoi modificare elementi limitati (nome, contenuto del messaggio), ma le modifiche strutturali richiedono la creazione di una nuova versione. [Informazioni sulle versioni del percorso](publish-journey.md#journey-versions)

+++

➡️ **Altre domande?** [Visualizza le domande frequenti complete sul percorso](journey-faq.md) con più di 40 risposte dettagliate

## Hai bisogno di aiuto? {#help}

### Collegamenti rapidi per le attività comuni

* **[Crea il tuo primo percorso](journey-gs.md)**: guida dettagliata per principianti
* **[Domande frequenti sul percorso](journey-faq.md)**: risposte alle domande comuni
* **[Risoluzione dei problemi](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)**: diagnosi e correzione dei problemi
* **[Riferimento codici errore](error-codes-reference.md)**: comprendere i messaggi di errore
* **[Guardrail e limitazioni](../start/guardrails.md)**: limiti tecnici e best practice

### Ricevere notifiche sui problemi

Configura gli **[avvisi di percorso](../reports/alerts.md)** per ricevere notifiche in tempo reale quando i percorsi rilevano errori o pattern insoliti.

### Risorse aggiuntive

* **[Hub per la gestione del percorso](/help/rp_landing_pages/manage-journey-landing-page.md)**: strumenti per filtrare, ottimizzare e gestire profili
* **[Riferimento alle attività di percorso](/help/rp_landing_pages/about-journey-building-landing-page.md)**: guida completa a tutti i tipi di attività
* **[Risoluzione dei problemi di esecuzione](troubleshooting-execution.md)**: eseguire il debug dei problemi di esecuzione del percorso
* **[Risoluzione dei problemi relativi alle attività in entrata](troubleshooting-inbound.md)**: correzione dei problemi di immissione e qualificazione

**Vuoi creare il tuo primo percorso?** [Inizia ora →](journey-gs.md)
