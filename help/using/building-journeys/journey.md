---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai percorsi
description: 'Guida introduttiva ai percorsi: scopri tipi di percorso, flusso di lavoro, funzionalità e best practice per creare esperienze cliente personalizzate in Adobe Journey Optimizer'
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: percorsi, discovery, get-start, unitario, pubblico di lettura, qualificazione del pubblico, evento di business, in tempo reale, pianificato, batch, attivato da eventi, flusso di lavoro, orchestrazione, personalizzazione, multicanale
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 522dba0516268a17e72f56c0f28205ba60709d78
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 3%

---


# Introduzione ai percorsi{#jo-general-principle}

Adobe Journey Optimizer ti consente di creare percorsi di clienti personalizzati e a più passaggi che si adattano in tempo reale al comportamento e alle esigenze del pubblico. Utilizzando un’area di lavoro intuitiva basata su trascinamento, puoi orchestrare messaggi e azioni tra più canali, sfruttando i dati contestuali e il targeting del pubblico per il massimo impatto.

Questa guida fornisce una roadmap chiara per aiutarti a comprendere le nozioni di base del percorso, scegliere il tipo di percorso adatto al tuo caso d’uso e progettare con sicurezza percorsi che forniscano esperienze cliente significative e tempestive.

## Cosa sono i percorsi?

**Percorsi** sono esperienze cliente automatizzate e a più passaggi che orchestrano interazioni personalizzate tra canali in risposta al comportamento del cliente, a eventi di business o a campagne pianificate.

Utilizza [!DNL Journey Optimizer] per:

* Crea **orchestrazione in tempo reale** casi d&#39;uso utilizzando dati contestuali archiviati in eventi o origini dati
* Progetta **scenari avanzati a più passaggi** che rispondono in modo dinamico al comportamento del cliente e agli eventi di business
* Distribuisci **1:1 esperienze personalizzate** su larga scala tramite e-mail, push, SMS, in-app, web e altro ancora

![Interfaccia di Progettazione Percorsi con riquadro palette, area di lavoro e proprietà](assets/journey38.png)

➡️ **Inizio generazione?** [Crea il tuo primo percorso](journey-gs.md) in 5 minuti.

### Percorsi e campagne: quando utilizzarle {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer offre tre approcci per raggiungere i clienti: **Percorsi** (1:1 orchestrazione in tempo reale), **Campagne** (consegna semplice in batch o attivata da API) e **Campagne orchestrate** (flussi di lavoro in batch con dati di più entità).

**Decisione rapida:**

* Utilizza **Percorsi** per esperienze con più passaggi basate sul comportamento, in cui ogni cliente procede al proprio ritmo
* Utilizza **Campagne Azione/API** per la consegna di messaggi semplice, pianificata o attivata ai tipi di pubblico
* Utilizza **Campagne orchestrate** per flussi di lavoro batch complessi che richiedono segmentazione di più entità e conteggi pre-invio esatti

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## Scegli il tipo di percorso {#journey-types}

Adobe Journey Optimizer supporta quattro tipi di percorsi, ciascuno progettato per diversi meccanismi di ingresso e scenari aziendali:

* **percorsi unitari**: esperienze in tempo reale attivate da eventi (conferme d&#39;ordine, e-mail di benvenuto)
* **Leggi percorsi di pubblico**: comunicazioni batch pianificate ai segmenti di pubblico (newsletter, campagne promozionali)
* **percorsi di qualificazione del pubblico**: risposte in tempo reale alle modifiche di iscrizione al pubblico (aggiornamenti di VIP, ricoinvolgimento)
* **percorsi di eventi aziendali**: condizioni aziendali che interessano più clienti (avvisi di inventario, vendite flash)

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## Creare con il progettista del percorso {#journey-designer}

**[Progettazione percorsi](using-the-journey-designer.md)** è l&#39;area di lavoro visiva per la creazione di esperienze cliente. Grazie all&#39;intuitiva interfaccia di trascinamento, è possibile orchestrare ogni passaggio del percorso senza scrivere codice.

![Interfaccia di Progettazione Percorsi con riquadro palette, area di lavoro e proprietà](assets/journey38.png)

### Operazioni possibili nella finestra di progettazione:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

**Definisci i punti di ingresso**

Scegli come i clienti inseriscono: attraverso un evento, un segmento di pubblico o una qualificazione del pubblico.

[Informazioni sulla gestione delle voci](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=it)

**Inviare messaggi**

Utilizza azioni di canale integrate per e-mail, push, SMS/MMS, in-app, web e altro, tutte progettate in Journey Optimizer.

[Inviare messaggi in percorsi](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=it)

**Aggiungi logica e condizioni**

Crea un ramo del percorso in base agli attributi del profilo, all’iscrizione al pubblico o a eventi in tempo reale.

[Condizioni d’uso](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=it)

**Sfruttare i dati**

Utilizza dati contestuali provenienti da eventi, Adobe Experience Platform o servizi API di terze parti.

[Utilizzare le origini dati](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

**Connetti sistemi esterni**

Crea azioni personalizzate per integrare sistemi di terze parti per l’invio di messaggi o l’attivazione di flussi di lavoro.

[Utilizzare le azioni personalizzate](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=it)

**Aggiungi attività di orchestrazione**

Utilizza tempi di attesa, salti, aggiornamenti del profilo e gestione dell&#39;audience per creare flussi sofisticati.

[Esplora tutte le attività](about-journey-activities.md)
:::

::::

➡️ **Apprendimento pratico:** [Guarda il video di Progettazione percorsi](#video) o [esplora casi d&#39;uso end-to-end](jo-use-cases.md)

## Flusso di lavoro di creazione del percorso {#workflow}

La creazione di percorsi di successo segue un processo chiaro e ripetibile. Di seguito è riportato il flusso di lavoro dettagliato:

**1. Piano** → **2. Progettazione** → **3. Test** → **4. Pubblica** → **5. Monitora** → **6. Ottimizza**

### &#x200B;1. Pianificare il percorso {#plan}

Prima di aprire la finestra di progettazione, specificare gli obiettivi:

* **Qual è l&#39;obiettivo?** (ad esempio, per integrare nuovi clienti, coinvolgere nuovamente gli utenti inattivi)
* **Chi è il pubblico?** (segmento specifico, singoli utenti guidati da eventi)
* **Quale tipo di percorso è adatto?** (vedi [Tipi di percorso](#journey-types) sopra)
* **Quali canali utilizzerai?** (e-mail, push, SMS, ecc.)

### &#x200B;2. Progettazione nel quadro {#design}

Utilizza Progettazione percorsi per generare il flusso:

* **Imposta condizioni di ingresso** - Definisci come entrano i profili (evento, pubblico, qualifica)
* **Aggiungi logica di orchestrazione** - Include tempi di attesa, condizioni e punti decisionali
* **Configura messaggi** - Progetta le comunicazioni o sfrutta i modelli esistenti
* **Imposta azioni** - Configura azioni predefinite o personalizzate da eseguire
* **Definisci i criteri di uscita** - Specifica quando e come i profili completano il percorso

[Scopri come utilizzare la → di Progettazione percorsi](using-the-journey-designer.md)

### &#x200B;3. Eseguire il test prima della pubblicazione {#test}

Esegui sempre il test del percorso per individuare eventuali problemi prima che si verifichino:

* Utilizza la **modalità di test** per simulare il percorso con profili di test
* Utilizza **prova** per visualizzare in anteprima l&#39;esecuzione del percorso senza influire sui dati reali o inviare messaggi
* Verifica che tutte le condizioni, i messaggi e le azioni funzionino come previsto
* Controllare tempistica, flussi di dati e personalizzazione

[Verifica il percorso →](testing-the-journey.md) | [Informazioni sull&#39;esecuzione →](journey-dry-run.md)

### &#x200B;4. Pubblicare il percorso {#publish}

Una volta completato il test, pubblica per rendere attivo il percorso:

* Verifica impostazioni e proprietà finali
* Pubblica per attivare per clienti reali
* Nota: i percorsi live possono essere interrotti ma non modificati (è necessario creare una nuova versione)

[Pubblicare il → di percorso](publish-journey.md)

### &#x200B;5. Monitorare le prestazioni {#monitor}

Monitora le prestazioni del percorso nel mondo reale:

* Visualizzare report e analisi di percorso
* Monitorare l&#39;immissione, il completamento e le percentuali di errore
* Impostare gli avvisi per i problemi critici

[Monitora e segnala →](report-journey.md) | [Configura avvisi →](../reports/alerts.md)

### &#x200B;6. Ottimizzare e ripetere {#optimize}

Utilizza le informazioni per migliorare:

* Analizzare le metriche di coinvolgimento e i tassi di conversione
* Ottimizzazione del tempo di invio dei test
* Creazione di nuove versioni di percorso con miglioramenti
* Utilizzare consigli basati sull’intelligenza artificiale

[Ottimizza i percorsi →](optimize.md) | [Ottimizzazione dell&#39;ora di invio →](send-time-optimization.md)

➡️ **Inizio?** [Crea il tuo primo percorso ora →](journey-gs.md)

## Casi d’uso reali {#use-cases}

Scopri dagli esempi pratici che mostrano come applicare concetti di percorso per risolvere le problematiche di marketing comuni:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=it)

**Nuovi abbonati**

Quando un cliente si abbona al servizio, attiva un percorso di benvenuto che li incoraggia a completare i passaggi di onboarding.

[Visualizza → del caso d’uso](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=it)

**Ottimizzazione dell&#39;ora di invio**

Utilizza l’intelligenza artificiale per inviare e-mail quando è più probabile che ogni cliente si interessi, massimizzando le percentuali di apertura e clic.

[Visualizza → del caso d’uso](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=it)

**Incrementa le consegne**

Aumenta gradualmente il volume dei messaggi per migliorare la reputazione del mittente ed evitare problemi di recapito dei messaggi.

[Visualizza → del caso d’uso](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=it)

**Destinazione per giorno feriale**

Inviare contenuti diversi in base al giorno della settimana in cui i clienti inseriscono il percorso, per maggiore rilevanza.

[Visualizza → del caso d’uso](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=it)

**Campagne multicanale**

Organizza esperienze senza soluzione di continuità tra canali e-mail, push, SMS e web in un unico percorso.

[Visualizza → del caso d’uso](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=it)

**Tutti i casi d&#39;uso**

Esplora la libreria completa dei casi di utilizzo del percorso con implementazioni dettagliate.

[Sfoglia tutte le →](jo-use-cases.md) | [Libreria casi d&#39;uso →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Esplora le funzionalità del percorso {#capabilities}

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

**Modalità di test ed esecuzione a secco**

Convalida i percorsi con i profili di test prima della pubblicazione e visualizza l’esecuzione dell’anteprima senza influire sui dati reali.

[Utilizzare la prova a secco](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=it)

**Copia nella sandbox**

Duplica i percorsi tra sandbox per semplificare i flussi di lavoro di test e distribuzione.

[Copia percorsi](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=it)

**Tag e organizzazione**

Utilizza i tag per categorizzare e filtrare i percorsi per una migliore gestione su larga scala.

[Organizzazione con tag](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

**Controllo velocità effettiva**

Limita la velocità effettiva dei messaggi per gestire la reputazione di invio ed evitare di sovraccaricare i sistemi.

[Velocità effettiva di controllo](limit-throughput.md)
:::

::::

[Visualizza tutte le funzionalità di percorso →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Imparare guardando {#video}

Ottieni un’introduzione visiva ai componenti di percorso e scopri le nozioni di base sulla creazione di percorsi nell’area di lavoro:

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **Desideri altri video?** [Esplora i tutorial video sul percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Domande comuni {#common-questions}

+++ Qual è la differenza tra un percorso e una campagna?

Adobe Journey Optimizer offre tre approcci:

* **Percorsi**: 1:1 orchestrazione in tempo reale in cui ogni profilo procede secondo il proprio ritmo. Consigliato per esperienze guidate dal comportamento e in più passaggi con logica condizionale (ad esempio, onboarding, abbandono del carrello).

* **Campagne (attivate da azioni e API)**: consegna semplice dei messaggi ai tipi di pubblico, in esecuzione simultanea a tutti i profili, secondo pianificazione o tramite attivatore API. Consigliato per campagne promozionali, newsletter e messaggi transazionali.

* **Campagne orchestrate**: flussi di lavoro batch con più passaggi e segmentazione complessa utilizzando dati relazionali (profili + prodotti/negozi/prenotazioni). Tutti i profili vengono elaborati con conteggi di pre-invio esatti. Consigliato per promozioni stagionali, avvii di prodotti, campagne che richiedono dati su più entità.

**Differenza chiave**: i Percorsi mantengono uno stato cliente individuale per le azioni in tempo reale; le campagne Azione/API distribuiscono messaggi semplici in batch; le campagne orchestrate forniscono l&#39;area di lavoro del flusso di lavoro batch con funzionalità di segmentazione multi-entità.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Informazioni sulle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ Posso modificare un percorso live?

Puoi modificare elementi limitati (nome, contenuto del messaggio), ma le modifiche strutturali richiedono la creazione di una nuova versione. [Informazioni sulle versioni di percorso](publish-journey.md#journey-versions)

+++

➡️ **Altre domande?** [Visualizza le domande frequenti complete sul Percorso](journey-faq.md) con più di 40 risposte dettagliate

## Hai bisogno di aiuto? {#help}

### Collegamenti rapidi per le attività comuni

* **[Crea il tuo primo percorso](journey-gs.md)** - Guida dettagliata per principianti
* **[Domande frequenti sui Percorsi](journey-faq.md)** - Risposte alle domande comuni
* **[Risoluzione dei problemi](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnosi e risoluzione dei problemi
* **[Riferimento codici errore](error-codes-reference.md)** - Comprendere i messaggi di errore
* **[Guardrail e limitazioni](../start/guardrails.md)** - Limiti tecnici e best practice

### Ricevi notifiche sui problemi

Configura **[avvisi di percorso](../reports/alerts.md)** per ricevere notifiche in tempo reale quando i percorsi rilevano errori o pattern insoliti.

### Risorse aggiuntive

* **[Hub gestione Percorsi](/help/rp_landing_pages/manage-journey-landing-page.md)** - Strumenti per filtrare, ottimizzare e gestire profili
* **[Riferimento attività Percorso](/help/rp_landing_pages/about-journey-building-landing-page.md)** - Guida completa a tutti i tipi di attività
* **[Risoluzione dei problemi di esecuzione](troubleshooting-execution.md)** - Debug dei problemi di esecuzione del percorso
* **[Risoluzione dei problemi relativi alle attività in entrata](troubleshooting-inbound.md)** - Correzione dei problemi di immissione e qualificazione

**Creare il primo percorso?** [Introduzione →](journey-gs.md)
