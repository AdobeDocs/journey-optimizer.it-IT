---
solution: Journey Optimizer
product: Journey Optimizer
title: Test, convalida e approvazione
description: Scopri tutte le funzionalità di test e approvazione in Journey Optimizer. Contenuto in anteprima, simula percorsi, convalida e-mail, esegui esperimenti, rileva i conflitti e imposta i flussi di lavoro di approvazione prima del lancio.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: test, convalida, approvazione, approvazione, controllo qualità, controllo qualità, profili di test, personalizzazione, rendering, spam-check, content-experiment, a/b-test, rilevamento conflitti, elenco seed, bozze, dati di esempio, approvazione-flusso di lavoro, test e-mail, convalida-flusso di lavoro
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: 5b1a68bb64fc55de894cb97a5239f4e1cd77fb40
workflow-type: tm+mt
source-wordcount: '2308'
ht-degree: 5%

---

# Test, convalida e approvazione{#section-overview}

Questa sezione descrive tutte le funzionalità di test e approvazione in Journey Optimizer. Troverai strumenti per visualizzare in anteprima i contenuti con profili di test, convalidare la logica di percorso, controllare il rendering di e-mail e i punteggi di spam, eseguire esperimenti A/B, rilevare i conflitti e impostare flussi di lavoro di approvazione.

Questa pagina di destinazione consente di scegliere l’approccio di test corretto in base a ciò che stai creando (campagne anziché percorsi), illustra i flussi di lavoro di test consigliati e fornisce un accesso rapido a tutte le risorse di test e approvazione. Inizia con [Scegli il tuo approccio di test](#choose-your-testing-approach) di seguito per identificare gli strumenti applicabili al tuo caso d&#39;uso. Per le definizioni dei termini di test chiave, vedere [Terminologia chiave](#key-terminology).

## Testare e approvare il contenuto

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Visualizzare anteprima, testare e convalidare il contenuto

Scopri come visualizzare in anteprima, testare e convalidare contenuti personalizzati utilizzando profili di test, test di rendering e-mail, valutazioni del punteggio di posta indesiderata e altro ancora.

[Esplora l’anteprima e il test del contenuto](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

Flussi di lavoro di approvazione per percorsi e campagne

Scopri come impostare, gestire ed eseguire i processi di approvazione per garantire il controllo di qualità dei percorsi e delle campagne.

[Scopri i flussi di lavoro di approvazione](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Testare il percorso

Convalida il percorso prima di pubblicarlo testandolo con profili specifici per garantire che eventi, condizioni e azioni funzionino come previsto. Disponibile per i percorsi 2D che utilizzano uno spazio dei nomi.

[Testare il percorso](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Esecuzione di prova del percorso

Esegui un’esecuzione in prova per simulare e convalidare l’esecuzione del percorso, identificando potenziali problemi prima della pubblicazione.

[Scopri l’esecuzione di prova del percorso](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Monitoraggio e risoluzione dei problemi

Accedi a risorse complete per la risoluzione dei problemi, avvisi di sistema e codici di errore per risolvere i problemi relativi all’esecuzione e alle prestazioni del percorso.

[Consulta monitoraggio e risoluzione dei problemi](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

Personalization Playground

Prova le espressioni di personalizzazione in un ambiente sicuro. Prima di applicare il codice a campagne e percorsi, prova il codice con i dati di esempio e i risultati di anteprima.

[Informazioni su Personalization Playground](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

Esperimenti sui contenuti e test A/B

Ottimizza le campagne sottoponendo a test più varianti di contenuto e misurando le prestazioni per identificare i trattamenti con le prestazioni migliori. Disponibile solo per le campagne (supporta esperimenti A/B e slot machine).

[Scopri gli esperimenti sui contenuti](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Elenchi di seed per il monitoraggio delle parti interessate

Includi automaticamente nelle consegne gli indirizzi interni delle parti interessate per monitorare i messaggi effettivi inviati ai clienti per il controllo della qualità e la conformità. Disponibile solo per il canale e-mail.

[Configura elenchi seed](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

Rilevamento dei conflitti

Identifica potenziali sovrapposizioni tra campagne e percorsi per evitare di sopraffare i clienti con troppe comunicazioni simultanee. Disponibile per campagne e percorsi unitari, Qualificazione del pubblico e Read Audience.

[Rileva conflitti](../using/conflict-prioritization/conflicts.md)
:::

::::

## Perché le prove e le approvazioni sono importanti

I processi di test e approvazione fungono da gate di qualità essenziali che proteggono la reputazione del tuo marchio e garantiscono il successo della campagna. Ecco perché sono importanti:

* **Rileva gli errori prima che raggiungano i clienti** - Identifica collegamenti interrotti, personalizzazione non corretta, problemi di rendering e errori di logica in un ambiente controllato in cui le correzioni sono rapide e prive di rischi.

* **Migliora il recapito messaggi** - Verifica i punteggi di posta indesiderata, convalida l&#39;autenticazione e-mail e verifica il rendering tra client e-mail per massimizzare il posizionamento della casella in entrata e le percentuali di coinvolgimento.

* **Assicurati della coerenza del brand** - Anteprima di contenuti con profili di test diversi per verificare che la personalizzazione venga visualizzata correttamente per vari segmenti di clienti e mantenga gli standard del brand.

* **Convalida percorsi complessi** - Simula flussi di percorso con più passaggi per verificare che i trigger vengano attivati correttamente, che le condizioni vengano valutate correttamente e che i clienti ricevano i messaggi corretti al momento giusto.

* **Stabilisci la responsabilità** - Implementa flussi di lavoro di approvazione formali che richiedono l&#39;approvazione delle parti interessate, creando una chiara proprietà e riducendo i lanci non autorizzati o prematuri di campagne.

* **Risparmia tempo e risorse** - Rileva i problemi all&#39;inizio del ciclo di sviluppo quando le correzioni sono più economiche e veloci, evitando costose correzioni post-avvio o escalation del servizio clienti.

<!--## Testing capabilities overview

**Testing types available:**

* Content testing: Preview and validate message content before sending → [Choose your testing approach](#choose-your-testing-approach)
* Journey logic testing: Simulate customer progression through journey paths → [Choose your testing approach](#choose-your-testing-approach)
* Technical testing: Validate rendering, deliverability, and authentication → [Technical validation](#2-technical-validation)
* Performance testing: Compare content variations using A/B experiments → [Content Experiments & A/B Testing](#test--approve-content)
* Conflict testing: Detect campaign and journey overlaps → [Conflict Detection](#test--approve-content)
* Approval testing: Structured review workflows before activation → [Approval Workflows](#test--approve-content)

**Key capabilities by context:**

| Capability | Applies to | Channel restrictions | Prerequisites | Primary purpose |
|------------|-----------|---------------------|--------------|-----------------|
| [Test profiles](../using/content-management/test-profiles.md) | Campaigns, Journeys | All channels | Test profiles created | Preview personalized content |
| [Sample input data](../using/test-approve/simulate-sample-input.md) | Campaigns, Journeys | Email, SMS, Push, Web, Code-based, In-app, Content cards | CSV/JSON file | Test multiple personalization variants |
| [Test mode](../using/building-journeys/testing-the-journey.md) | Journeys only | N/A | Draft journey, namespace configured | Simulate profile progression |
| [Dry run](../using/building-journeys/journey-dry-run.md) | Journeys only | N/A | Journey created | Analyze execution paths |
| [Email rendering](../using/content-management/rendering.md) | Campaigns, Journeys | Email only | Litmus integration | Verify display across clients |
| [Spam score](../using/content-management/spam-report.md) | Campaigns, Journeys | Email only | None | Deliverability validation |
| [Seed lists](../using/configuration/seed-lists.md) | Campaigns, Journeys | Email only | Seed list configured | Stakeholder monitoring |
| [Content experiments](../using/content-management/get-started-experiment.md) | Campaigns only | All channels | None | A/B and multi-armed bandit testing |
| [Conflict detection](../using/conflict-prioritization/conflicts.md) | Campaigns, Journeys (limited) | All channels | None | Prevent customer over-messaging |
| [Approval workflows](../using/test-approve/gs-approval.md) | Campaigns, Journeys | All channels | Approval policy created | Structured review process |
| [Personalization playground](../using/personalization/personalize.md#playground) | All | All channels | None | Learn and test personalization syntax |

**Common testing workflows:**

1. Pre-development: Use [personalization playground](#test--approve-content) to learn syntax
2. During development: Preview with [test profiles](#choose-your-testing-approach), validate with [sample input data](#choose-your-testing-approach)
3. Pre-launch: Run [technical tests](#2-technical-validation) (rendering, spam), check [conflicts](#test--approve-content), submit for [approval](#test--approve-content)
4. Post-launch: Monitor with live reports (see [Monitoring & Troubleshooting](#test--approve-content)), iterate based on results

-->

<!--
## Decision tree for testing method selection

Use this decision tree to quickly identify the right testing tools for your specific scenario. Answer each question based on your context (what you're building, what you need to validate, and which channel you're using) to navigate directly to the relevant capabilities and documentation.

+++ **Question 1: What are you testing?**

* Campaign → [Choose your testing approach](#choose-your-testing-approach)
* Journey → [Choose your testing approach](#choose-your-testing-approach)
* Personalization expressions → [Personalization playground](#test--approve-content)
+++

+++**Question 2: What aspect needs validation?**

* Content and personalization → [Test profiles](#choose-your-testing-approach) or [sample input data](#choose-your-testing-approach)
* Email display → [Email rendering tests](#2-technical-validation)
* Deliverability → [Spam score checks](#2-technical-validation)
* Journey logic and flow → [Test mode](#choose-your-testing-approach) or [dry run](#test--approve-content)
* Performance comparison → [Content experiment](#test--approve-content) (campaigns only)
* Timing conflicts → [Conflict detection](#test--approve-content)
* Stakeholder review → [Approval workflow](#test--approve-content)
+++

+++**Question 3: What channel?**

* Email → All testing methods available (see [Choose your testing approach](#choose-your-testing-approach))
* SMS, Push → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Web, In-app, Code-based → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Multiple channels → Test each channel separately
+++

+++**Question 4: When in the workflow?**

* Before building → [Personalization playground](#test--approve-content) for learning
* During building → [Test profiles](#choose-your-testing-approach) and [sample input data](#choose-your-testing-approach) for validation
* Before launch → [Rendering tests](#2-technical-validation), [spam checks](#2-technical-validation), [conflict detection](#test--approve-content), [approvals](#test--approve-content)
* After launch → [Live reports](../using/building-journeys/report-journey.md) and [monitoring](#test--approve-content)
+++

-->

## Scegli il tuo approccio di test

L’approccio corretto per i test dipende da cosa stai creando e da cosa devi convalidare. Usa questa guida per identificare gli strumenti di test più rilevanti per lo scenario.

>[!BEGINTABS]

>[!TAB Test delle campagne]

**Per tutte le campagne:**

* Anteprima e test del contenuto tramite [profili di test](../using/content-management/test-profiles.md) o [dati di input di esempio](../using/test-approve/simulate-sample-input.md)
* Controlla [il rendering di e-mail](../using/content-management/rendering.md) tra dispositivi e client (solo canale e-mail)
* Esegui [controlli punteggio posta indesiderata](../using/content-management/spam-report.md) (solo canale e-mail)
* Rivedi [conflitti](../using/conflict-prioritization/conflicts.md) con altre campagne e altri percorsi
* Configura [elenchi seed](../using/configuration/seed-lists.md) per il monitoraggio delle parti interessate (solo canale e-mail)
* Invia per [approvazione](../using/test-approve/gs-approval.md) prima dell&#39;attivazione

**Per test A/B e ottimizzazione:**

* Crea [esperimenti di contenuto](../using/content-management/get-started-experiment.md) per testare più trattamenti e misurare le prestazioni

**Per campagne attivate da API:**

* Utilizza l&#39;[API di simulazione campagna](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} per attivare i processi di bozza a livello di programmazione

>[!TAB percorsi di prova]

**Per tutti i percorsi:**

* Utilizza la [modalità di test](../using/building-journeys/testing-the-journey.md) per simulare la progressione del profilo (solo per percorsi bozza, richiede spazio dei nomi) oppure [esecuzione inattiva](../using/building-journeys/journey-dry-run.md) per analizzare i percorsi di esecuzione senza inviare messaggi
* Verifica singoli messaggi tramite [anteprima e bozze](../using/content-management/preview-test.md)
* Controlla [conflitti](../using/conflict-prioritization/conflicts.md) con altri percorsi e campagne
* Invia per [approvazione](../using/test-approve/gs-approval.md) prima di pubblicare

**Per percorsi complessi:**

* Utilizza la modalità di test ed esegui a secco insieme per convalidare completamente la logica di diramazione e i percorsi di esecuzione
* Verificare sistematicamente condizioni di ingresso e attributi di profilo diversi

**Nota:** il rilevamento dei conflitti e la limitazione dei percorsi sono disponibili solo per percorsi di pubblico unitari, di qualificazione del pubblico e di lettura.

>[!TAB Verifica della personalizzazione]

**Prima di creare il contenuto:**

* Esperimento nel [parco giochi di personalizzazione](../using/personalization/personalize.md#playground) per apprendere la sintassi e testare le espressioni con dati di esempio

**Durante la creazione del contenuto:**

* Anteprima con [profili di test](../using/content-management/test-profiles.md) per convalidare correttamente i rendering di personalizzazione
* Verifica più scenari utilizzando [dati di input di esempio](../using/test-approve/simulate-sample-input.md) da file CSV/JSON (supporta fino a 30 varianti)

>[!ENDTABS]

## Best practice di test

Per massimizzare l’efficacia delle attività di test, segui queste pratiche consigliate:

1. **Esegui il test in anticipo e spesso** - Non aspettare che una campagna sia completamente generata. Puoi testare contenuti, personalizzazione e logica in modo incrementale durante lo sviluppo.

1. **Utilizza profili di test realistici** - [Crea profili di test](../using/audience/creating-test-profiles.md) che rappresentino con precisione i segmenti di pubblico target, inclusi casi limite e diversi scenari di personalizzazione.

1. **Verifica tra dispositivi e client** - Verifica il [rendering di e-mail](../using/content-management/rendering.md) nei client e-mail più diffusi (Gmail, Outlook, Apple Mail) e nei dispositivi (desktop, dispositivi mobili, tablet) per garantire una visualizzazione coerente (solo canale e-mail).

1. **Convalida della personalizzazione in modo completo** - Verifica con più [profili di test](../using/content-management/test-profiles.md) che hanno valori di attributo diversi per confermare che i token di personalizzazione vengano visualizzati correttamente e che i valori di fallback funzionino. Utilizza il [parco giochi di personalizzazione](../using/personalization/personalize.md#playground) per sperimentare espressioni di personalizzazione e testare il codice con dati di esempio prima di applicarli alle campagne.

1. **Verifica varianti di contenuto con dati di esempio**. Utilizza [dati di input di esempio](../using/test-approve/simulate-sample-input.md) da file CSV o JSON per testare fino a 30 scenari di personalizzazione senza creare numerosi profili di test, risparmiando tempo e garantendo al contempo una copertura completa. Supporta i canali di e-mail, SMS, push, web, esperienza basata su codice, in-app e schede di contenuto.

1. **Utilizza elenchi seed per il monitoraggio delle parti interessate**. Configura [elenchi seed](../using/configuration/seed-lists.md) per includere automaticamente le parti interessate interne che riceveranno copie di tutte le consegne al momento dell&#39;esecuzione per il monitoraggio della qualità e la verifica della conformità (solo canale e-mail).

1. **Simula percorsi di percorso**. Per percorsi complessi con più rami, utilizza la [modalità di test](../using/building-journeys/testing-the-journey.md) per testare condizioni di ingresso e attributi di profilo diversi e convalidare tutti i percorsi possibili. Disponibile per i percorsi 2D che utilizzano uno spazio dei nomi.

1. **Verifica gli indicatori di recapito messaggi** - Rivedi [i punteggi di posta indesiderata](../using/content-management/spam-report.md), lo stato di autenticazione e le metriche di integrità delle e-mail prima degli invii di grandi dimensioni (solo canale e-mail).

1. **Documenta i risultati dei test** - Conserva i record dei risultati dei test, dei problemi rilevati e delle risoluzioni per migliorare i processi di test futuri e condividi gli insegnamenti con il tuo team.

1. **Coinvolgi le parti interessate in anticipo** - Condividi anteprime e risultati dei test con le parti interessate prima dell&#39;[approvazione formale](../using/test-approve/gs-approval.md) per raccogliere feedback e allineare le aspettative.

## Flusso di lavoro di test consigliato

Segui questo approccio in 4 fasi per convalidare le campagne e i percorsi prima del lancio:

| Fase | Cosa testare | Azioni chiave |
|-------|-------------|-------------|
| **1. Convalida del contenuto** | Personalization, progettazione, rendering | [Anteprima con profili di test](../using/content-management/preview-test.md), verifica [più varianti](../using/test-approve/simulate-sample-input.md) con CSV/JSON, verifica [rendering](../using/content-management/rendering.md) tra dispositivi |
| **2. Controlli tecnici** | Recapito messaggi, collegamenti, conflitti | Esegui [controlli punteggio posta indesiderata](../using/content-management/spam-report.md), convalida i collegamenti, verifica la presenza di [conflitti](../using/conflict-prioritization/conflicts.md) con altre campagne |
| **3. Logica percorso** (solo percorsi) | Condizioni di ingresso, flusso, diramazione | Utilizza la [modalità di test](../using/building-journeys/testing-the-journey.md) per simulare la progressione, esegui [esecuzione in prova](../using/building-journeys/journey-dry-run.md) per percorsi complessi |
| **4. Pre-avvio** | Impostazioni, approvazioni, monitoraggio | Invia per [approvazione](../using/test-approve/gs-approval.md), verifica pianificazioni e pubblico, abilita [avvisi](../using/reports/alerts.md) |

**Suggerimento pro:** inizia con [area di riproduzione per la personalizzazione](../using/personalization/personalize.md#playground) per testare le espressioni prima di creare il contenuto e controlla sempre [rilevamento conflitti](../using/conflict-prioritization/conflicts.md) prima dell&#39;avvio per evitare messaggi eccessivi.

## Test in azione: casi d’uso

Scopri come i concetti di test si applicano agli scenari reali:

| Caso d’uso | Cosa imparerai | Obiettivo principali dei test |
|----------|-------------------|-------------------|
| **[Inviare messaggi multicanale](../using/building-journeys/journeys-uc.md)** | Test di un percorso che combina Read Audience, eventi di reazione e messaggi e-mail/push. Convalida l’intero flusso dal targeting del pubblico alla consegna dei messaggi. | Coordinazione multicanale, eventi di reazione, convalida del flusso end-to-end, passaggi di test e pubblicazione |
| **[Invia un messaggio ai sottoscrittori](../using/building-journeys/message-to-subscribers-uc.md)** | Percorsi di test che eseguono il targeting degli elenchi di abbonamenti con indirizzi e-mail dinamici. Convalida le espressioni di personalizzazione per il targeting corretto del sottoscrittore. | Espressioni Personalization, indirizzamento dinamico, targeting degli elenchi di iscrizioni |
| **[Invio di messaggi con limiti di tempo](../using/building-journeys/weekday-email-uc.md)** | Verifica i percorsi con condizioni basate sul tempo per garantire che i messaggi vengano inviati in giorni specifici. Convalida le attività di attesa e la logica di pianificazione. | Condizioni basate sul tempo, attività di attesa, convalida della pianificazione |
| **[Esplora altri casi d&#39;uso del percorso](../using/building-journeys/jo-use-cases.md)** | Accedi a una raccolta completa di esempi pratici che riguardano eventi di esperienza, messaggistica multicanale e integrazioni di sistemi esterne. | Vari scenari, modelli avanzati, test dell’integrazione |

## Terminologia chiave

Acquisisci familiarità con questi concetti di test essenziali per comprendere meglio le funzionalità di test e approvazione di Journey Optimizer. Ogni termine si collega alla documentazione dettagliata.

**[Profili di test](../using/content-management/test-profiles.md)** - Profili cliente sintetici (non clienti reali) utilizzati per visualizzare in anteprima i contenuti personalizzati. Contrassegnato nel servizio Profilo cliente in tempo reale. Obbligatorio per la modalità di test e l’anteprima del contenuto. [Scopri come creare profili di test](../using/audience/creating-test-profiles.md)

**[Modalità di test](../using/building-journeys/testing-the-journey.md)** - Funzionalità di simulazione del Percorso che invia i profili di test attraverso i percorsi del percorso. Limitazioni: solo percorsi in stato di bozza, richiede spazio dei nomi e solo profili di test. [Consulta la documentazione sulla modalità di test](../using/building-journeys/testing-the-journey.md)

**[Esecuzione in prova](../using/building-journeys/journey-dry-run.md)**: strumento di analisi dell&#39;esecuzione del Percorso che traccia i percorsi senza inviare messaggi o effettuare chiamate API. Caso di utilizzo: convalida della logica senza utilizzare risorse. [Informazioni sull&#39;esecuzione in prova](../using/building-journeys/journey-dry-run.md)

**[Dati di input di esempio](../using/test-approve/simulate-sample-input.md)**: file CSV o JSON contenenti i valori degli attributi di profilo per testare la personalizzazione. Supporta fino a 30 varianti. Alternativa alla creazione di profili di test. [Simulare varianti di contenuto](../using/test-approve/simulate-sample-input.md)

**[Elenchi seed](../using/configuration/seed-lists.md)** - Indirizzi e-mail di stakeholder interni inclusi automaticamente nelle consegne effettive (non invii di test). Solo canale e-mail. Caso d’uso: monitoraggio della qualità e conformità. [Configura elenchi seed](../using/configuration/seed-lists.md)

**[Esperimenti di contenuto](../using/content-management/get-started-experiment.md)** - Test A/B o esperimenti con slot machine che mettono a confronto varianti di contenuto. Solo campagne, non disponibile in percorsi. [Introduzione agli esperimenti](../using/content-management/get-started-experiment.md) | [Crea esperimenti](../using/content-management/content-experiment.md)

**[Bozze](../using/content-management/proofs.md)** - Verifica le consegne e-mail inviate a indirizzi e-mail specifici utilizzando i dati del profilo di test. Diverso dagli elenchi seed (le bozze sono invii di test manuali, gli elenchi seed sono copie automatiche delle parti interessate). [Invia bozze](../using/content-management/proofs.md)

**[Rilevamento conflitti](../using/conflict-prioritization/conflicts.md)** - Strumento che identifica campagne e percorsi sovrapposti che si rivolgono agli stessi tipi di pubblico. Supporto limitato per il percorso: unitari, qualificazione del pubblico e solo tipi di pubblico lettura. [Informazioni sulla gestione dei conflitti](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Flussi di lavoro di approvazione](../using/test-approve/gs-approval.md)** - Processo di revisione in più passaggi che richiede l&#39;approvazione delle parti interessate prima dell&#39;attivazione. Richiede la configurazione dei criteri di approvazione. [Configura approvazioni](../using/test-approve/gs-approval.md) | [Crea criteri](../using/test-approve/approval-policies.md)

**[Test di rendering](../using/content-management/rendering.md)** - Convalida della visualizzazione delle e-mail tra client e-mail (Gmail, Outlook, Apple Mail) e dispositivi. Richiede l&#39;integrazione con Litmus. [Test rendering e-mail](../using/content-management/rendering.md)

**[Ambiente playground di Personalization](../using/personalization/personalize.md#playground)** - Ambiente di apprendimento interattivo per sperimentare la sintassi di personalizzazione e testare le espressioni con dati di esempio. Non è richiesto alcun set di dati live. [Accedi al parco giochi](../using/personalization/personalize.md#playground)

## Risorse aggiuntive

>[!BEGINTABS]

>[!TAB Guide essenziali]

* [Simula varianti di contenuto](../using/test-approve/simulate-sample-input.md) - Puoi testare fino a 30 scenari di personalizzazione utilizzando file CSV o JSON. Ideale per il test dei contenuti multilingue senza creare più profili di test. Supporta e-mail, SMS, push, web, schede basate su codice, in-app e di contenuto.

* [Creazione di profili di test](../using/audience/creating-test-profiles.md) - Creazione e gestione di profili di test per simulare scenari cliente. Scopri come contrassegnare i profili per il test, impostare gli attributi e organizzare i segmenti di test.

* [Rapporto posta indesiderata](../using/content-management/spam-report.md) - Controlla i punteggi di posta indesiderata prima dell&#39;invio per migliorare il recapito messaggi e il posizionamento della casella in entrata. Consigli fruibili per l’ottimizzazione dei contenuti.

* [Domande frequenti sul Percorso](../using/building-journeys/journey-faq.md) - Riferimento rapido per le domande comuni su test, esecuzione e risoluzione dei problemi del percorso.

>[!TAB Dipendenze e relazioni]

Scopri in che modo le funzionalità di test si connettono tra loro e ai flussi di lavoro Journey Optimizer più ampi. In questa sezione vengono mappati i prerequisiti, le dipendenze a monte/a valle e le combinazioni di funzionalità comuni.

+++**Prerequisiti (necessari prima del test)**

* I profili di test devono essere creati prima di utilizzare la modalità di test o l’anteprima del contenuto
* I criteri di approvazione devono essere configurati prima dell’invio per l’approvazione
* È necessario creare elenchi di seed prima di aggiungerli a campagne/percorsi
* Integrazione Litmus necessaria per i test di rendering di e-mail
* Per utilizzare la modalità di test, il percorso deve essere in stato bozza
* Il percorso deve avere uno spazio dei nomi configurato per utilizzare la modalità di test

+++

+++**Da cosa dipende il test (a monte)**

* Creazione di contenuti: campagne o percorsi da testare
* Profili di test: necessari per la modalità di test e l’anteprima del contenuto
* Criteri di approvazione: necessari per i flussi di lavoro di approvazione
* Configurazione: configurazioni del canale, autenticazione e-mail, impostazioni del dominio

+++

+++**Dipende dai test (downstream)**

* Attivazione campagna/percorso: impossibile attivare senza risolvere gli errori
* Pubblicazione: potrebbe essere necessaria l’approvazione prima della pubblicazione
* Monitoraggio live: monitoraggio e reporting dopo il lancio
* Ottimizzazione: utilizza i risultati dei test per perfezionare le campagne future

+++

+++**Funzionalità correlate**

* Flussi di lavoro di test e approvazione - Processo di controllo qualità
* Test e rilevamento dei conflitti: prevenzione dei messaggi eccessivi dei clienti
* Test + Esperimenti di contenuto - Ottimizzazione delle prestazioni
* Test e reporting: ciclo di miglioramento continuo
* Profili di test + Personalization - Convalida del contenuto
* Esecuzione a secco + modalità test - Convalida completa del percorso

+++

+++**Combinazioni di funzionalità comuni**

* Test dei contenuti: profili di test + dati di input di esempio + area di riproduzione Personalization
* Convalida e-mail: test di rendering + punteggi spam + profili di test + bozze
* Convalida del percorso: modalità di test + esecuzione a secco + profili di test
* Lista di controllo per il pre-lancio: tutti i test tecnici + rilevamento dei conflitti + flussi di lavoro di approvazione

+++

>[!TAB Domande comuni]

+++**D: quali test sono necessari prima di avviare una campagna?**

**Minimo:** anteprima contenuto con profili di test + controllo punteggio posta indesiderata (e-mail)
**Consigliato:** + Rendering di e-mail + Rilevamento conflitti + Flusso di lavoro di approvazione
**Best practice:** + Test dei dati di input di esempio + Elenchi seed + Esperimento A/B (in caso di ottimizzazione)

+++

+++**D: come posso testare la personalizzazione senza creare molti profili di test?**

**Soluzione primaria:** utilizza [dati di input di esempio](../using/test-approve/simulate-sample-input.md) con file CSV/JSON (supporta fino a 30 varianti)
**Alternativa:** creare da 3 a 5 [profili di test](../using/audience/creating-test-profiles.md) rappresentativi che coprono segmenti chiave
**Strumento di apprendimento:** Esperimento iniziale in [area giochi di personalizzazione](../using/personalization/personalize.md#playground)

+++

+++**D: qual è la differenza tra la modalità di test e l&#39;esecuzione in prova per i percorsi?**

**Modalità di test:** invia i profili di test tramite il percorso, attiva le azioni effettive e genera i messaggi di test. Richiede bozza di percorso e spazio dei nomi.
**Esecuzione in prova:** traccia i percorsi di esecuzione senza inviare nulla. Funziona su qualsiasi stato del percorso. Nessun messaggio inviato, nessuna azione eseguita.
**Usare insieme:** modalità di test per il test dei messaggi + Esecuzione a secco per la convalida logica - copertura completa.

+++

+++**Q: posso testare i percorsi nello stato produzione/live?**

**Modalità di test:** No - solo percorsi bozza
**Esecuzione in prova:** Sì - funziona su qualsiasi stato del percorso
**Anteprima contenuto:** Sì - visualizza l&#39;anteprima di singoli messaggi in qualsiasi momento
**Soluzione:** duplicare il percorso live nella bozza per la convalida completa della modalità di test

+++

+++**Q: quali funzionalità di test richiedono integrazioni esterne?**

**Rendering di e-mail:** richiede l&#39;integrazione con Litmus (licenza separata)
**Tutti gli altri:** integrati in Journey Optimizer, nessuna integrazione aggiuntiva richiesta
**Nota:** i profili di test richiedono il servizio Profilo cliente in tempo reale (incluso)

+++

+++**D: come posso testare le campagne attivate da API?**

**Opzione 1:** Utilizza [API di simulazione campagna](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} per test programmatici
**Opzione 2:** Anteprima del contenuto con i profili di test nell&#39;interfaccia utente
**Opzione 3:** Inviare bozze agli indirizzi e-mail di prova
**Best practice:** combina tutti e tre per una convalida completa

+++

>[!ENDTABS]
