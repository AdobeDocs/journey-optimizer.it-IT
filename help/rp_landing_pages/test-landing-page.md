---
solution: Journey Optimizer
product: Journey Optimizer
title: Test, convalida e approvazione
description: Scopri tutte le funzionalità di test e approvazione in Journey Optimizer. Visualizza in anteprima il contenuto, simula i percorsi, convalida le e-mail, esegui esperimenti, rileva eventuali conflitti e configura i flussi di lavoro di approvazione prima del lancio.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: test, convalida, approva, approvazione, garanzia qualità, controllo qualità, profili di test, personalizzazione, rendering, controllo spam, esperimenti sui contenuti, test a/b, rilevamento conflitti, elenco seed, bozze, dati di esempio, flusso di lavoro di approvazione, test e-mail, flusso di lavoro di convalida
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: c3535f39b351d671054031b9cc391bf6d9d83a09
workflow-type: ht
source-wordcount: '2328'
ht-degree: 100%

---

# Test, convalida e approvazione{#section-overview}

Questa sezione descrive tutte le funzionalità di test e approvazione in Journey Optimizer. Troverai strumenti per visualizzare in anteprima i contenuti con profili di test, convalidare la logica dei percorsi, controllare il rendering delle e-mail e i punteggi di spam, eseguire esperimenti A/B, rilevare eventuali conflitti e configurare i flussi di lavoro per l’approvazione.

Questa pagina di destinazione consente di scegliere l’approccio di test corretto in base a ciò che stai creando (campagne anziché percorsi), illustra i flussi di lavoro di test consigliati e fornisce un accesso rapido a tutte le risorse di test e approvazione. Inizia con [Scegli l’approccio di test](#choose-your-testing-approach) di seguito per identificare gli strumenti applicabili al tuo caso d’uso. Per le definizioni dei termini di test chiave, consulta [Terminologia chiave](#key-terminology).

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

Convalida il percorso prima di pubblicarlo testandolo con profili specifici per garantire che eventi, condizioni e azioni funzionino come previsto. Disponibile per percorsi di bozza che utilizzano uno spazio dei nomi.

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

Playground di personalizzazione

Sperimenta con le espressioni di personalizzazione in un ambiente sicuro. Prima di applicare il codice a campagne e percorsi, testalo con i dati di esempio e i risultati di anteprima.

[Informazioni sul playground di personalizzazione](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Esperimenti sui contenuti e test A/B

Ottimizza le campagne testando più varianti di contenuto e misurando le prestazioni per identificare i trattamenti con le prestazioni migliori. Disponibile solo per le campagne (supporta esperimenti multi-armed bandit e A/B).

[Informazioni sugli esperimenti sui contenuti](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Elenchi di seed per il monitoraggio delle parti interessate

Includi automaticamente nelle consegne gli indirizzi interni degli stakeholder per monitorare i messaggi effettivi inviati alla clientela per il controllo qualità e la conformità. Disponibile solo per il canale e-mail.

[Configurare elenchi di seed](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

Rilevamento di conflitti

Identifica potenziali sovrapposizioni tra campagne e percorsi per evitare di esporre la clientela a un eccesso di comunicazioni simultanee. Disponibili per campagne e percorsi unitari, qualificazione del pubblico e percorsi Leggi pubblico.

[Rilevare conflitti](../using/conflict-prioritization/conflicts.md)
:::

::::

## Perché test e approvazione sono importanti

I processi di test e approvazione fungono da controlli qualità essenziali che proteggono la reputazione del brand e garantiscono il successo della campagna. Ecco perché sono importanti:

* **Per rilevare per tempo eventuali errori**: puoi individuare errori quali collegamenti interrotti, personalizzazione non corretta, problemi di rendering e di logica in un ambiente controllato in cui puoi apportare correzioni in modo rapido e privo di rischi.

* **Per migliorare la recapitabilità**: convalidare l’autenticazione delle e-mail e verificarne il rendering per client e-mail diversi, per massimizzarne la consegna nella casella in entrata e i tassi di coinvolgimento.

* **Per assicurare la coerenza del brand**: puoi visualizzare in anteprima i contenuti con profili di test diversi per verificare che la personalizzazione si presenti correttamente per diversi segmenti di clientela e rispetti gli standard del brand.

* **Per convalidare percorsi complessi**: puoi simulare flussi di percorso con più passaggi per verificare che l’attivazione dei trigger e la valutazione delle condizioni avvengano correttamente e per assicurarti che la clientela riceva i messaggi giusti al momento giusto.

* **Per sostenere trasparenza e responsabilità**: puoi implementare flussi di lavoro formali che richiedono l’approvazione degli stakeholder, definendo chiaramente chi è responsabile e riducendo il rischio di lanci non autorizzati o prematuri delle campagne.

* **Per risparmiare tempo e risorse**: rilevando eventuali problemi nelle prime fasi del ciclo di sviluppo, quando è possibile correggerli in modo più economico e veloce, puoi evitare costose correzioni post-avvio o escalation del servizio clienti.

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

## Scegliere l’approccio al test

L’approccio al test corretto dipende da cosa stai creando e da cosa devi convalidare. Utilizza questa guida per identificare gli strumenti di test più rilevanti per lo scenario.

>[!BEGINTABS]

>[!TAB Test delle campagne]

**Per tutte le campagne:**

* Anteprima e test del contenuto tramite [profili di test](../using/content-management/test-profiles.md) o [dati di input di esempio](../using/test-approve/simulate-sample-input.md)
* Controlla [il rendering di e-mail](../using/content-management/rendering.md) per dispositivi e client diversi (solo canale e-mail)
* Esegui [controlli del punteggio di spam](../using/content-management/spam-report.md) (solo canale e-mail)
* Rivedi i [conflitti](../using/conflict-prioritization/conflicts.md) con altre campagne e percorsi
* Configura [elenchi di seed](../using/configuration/seed-lists.md) per il monitoraggio degli stakeholder (solo canale e-mail)
* Invia per l’[approvazione](../using/test-approve/gs-approval.md) prima dell’attivazione

**Per test A/B e ottimizzazione:**

* Crea [esperimenti di contenuto](../using/content-management/get-started-experiment.md) per testare più trattamenti e misurare le prestazioni

**Per campagne attivate da API:**

* Utilizza l’[API di simulazione campagna](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} per attivare in modo programmatico i processi di bozza

>[!TAB Test dei percorsi]

**Per tutti i percorsi:**

* Utilizza la [modalità test](../using/building-journeys/testing-the-journey.md) per simulare la progressione del profilo (solo per percorsi di bozza, richiede lo spazio dei nomi) oppure l’[esecuzione di prova](../using/building-journeys/journey-dry-run.md) per analizzare i percorsi di esecuzione senza inviare messaggi
* Testare singoli messaggi tramite [anteprima e bozze](../using/content-management/preview-test.md)
* Controlla i [conflitti](../using/conflict-prioritization/conflicts.md) con altri percorsi e campagne
* Invia per l’[approvazione](../using/test-approve/gs-approval.md) prima della pubblicazione

**Per percorsi complessi:**

* Utilizza la modalità test e l’esecuzione di prova insieme per convalidare completamente la logica di diramazione e i percorsi di esecuzione
* Testare sistematicamente condizioni di ingresso e attributi di profilo diversi

**Nota:** il rilevamento dei conflitti e la limitazione dei percorsi sono disponibili solo per percorsi di qualificazione del pubblico, unitari e di Leggi pubblico.

>[!TAB Testare la personalizzazione]

**Prima di creare il contenuto:**

* Sperimenta nel [playground di personalizzazione](../using/personalization/personalize.md#playground) per apprendere la sintassi e testare le espressioni con dati di esempio

**Durante la creazione di contenuti:**

* Visualizza l’anteprima con [profili di test](../using/content-management/test-profiles.md) per convalidare correttamente i rendering di personalizzazione
* Testa più scenari utilizzando [dati di input di esempio](../using/test-approve/simulate-sample-input.md) da file CSV/JSON (supporta fino a 30 varianti)

>[!ENDTABS]

## Testare le best practice

Per ottimizzare l’efficacia dell’analisi delle attività di test, segui queste procedure consigliate:

1. **Testa in anticipo e spesso**: non aspettare che una campagna sia completamente generata. Testa contenuti, personalizzazione e logica in modo incrementale durante lo sviluppo.

1. **Utilizza profili di test realistici**: [crea profili di test](../using/audience/creating-test-profiles.md) che rappresentino con precisione i segmenti di pubblico target, inclusi casi Edge e diversi scenari di personalizzazione.

1. **Testa per dispositivi e client diversi**: verifica il [rendering delle e-mail](../using/content-management/rendering.md) nei più diffusi client e-mail (Gmail, Outlook, Mail di Apple) e dispositivi (desktop, dispositivi mobili, tablet) per assicurarti che vengano visualizzate correttamente (solo canale e-mail).

1. **Convalida la personalizzazione attentamente**: testa con più [profili di test](../using/content-management/test-profiles.md) che hanno valori di attributo diversi per confermare che nei token di personalizzazione venga eseguito il rendering correttamente e che i valori di fallback funzionino. Utilizza il [playground di personalizzazione](../using/personalization/personalize.md#playground) per sperimentare espressioni di personalizzazione e testare il codice con dati di esempio prima di applicarli alle campagne.

1. **Testa varianti di contenuto con dati di esempio**. Utilizza [dati di input di esempio](../using/test-approve/simulate-sample-input.md) da file CSV o JSON per testare fino a 30 scenari di personalizzazione senza creare numerosi profili di test, risparmiando tempo e garantendo al contempo una copertura completa. Supporta i canali di e-mail, SMS, push, web, esperienza basata su codice, in-app e schede contenuto.

1. **Utilizza elenchi di seed per il monitoraggio degli stakeholder**: configura [elenchi di seed](../using/configuration/seed-lists.md) per includere automaticamente stakeholder interni che riceveranno copie di tutte le consegne al momento dell’esecuzione per il monitoraggio della qualità e la verifica della conformità (solo canale e-mail).

1. **Simula percorsi di percorso**: per percorsi complessi con più rami, utilizza la [modalità test](../using/building-journeys/testing-the-journey.md) per testare condizioni di ingresso e attributi di profilo diversi per convalidare tutti i percorsi possibili. Disponibile per percorsi di bozza che utilizzano uno spazio dei nomi.

1. **Controlla gli indicatori di recapitabilità**: rivedi i [punteggi di spam](../using/content-management/spam-report.md), lo stato di autenticazione e le metriche di integrità delle e-mail prima degli invii di grandi dimensioni (solo canale e-mail).

1. **Documenta i risultati dei test**: tieni traccia dei risultati dei test, dei problemi rilevati e delle risoluzioni per migliorare i processi di test futuri e condividi con il tuo team le informazioni raccolte.

1. **Coinvolgi gli stakeholder fin dalle fasi iniziali**: condividi anteprime e risultati dei test con gli stakeholder prima dell’[approvazione formale](../using/test-approve/gs-approval.md) per raccogliere feedback e allineare le aspettative.

## Flusso di lavoro di test consigliato

Segui questo approccio in 4 fasi per convalidare le campagne e i percorsi prima del lancio:

| Fase | Che cosa testare | Azioni chiave |
|-------|-------------|-------------|
| **1. Convalida dei contenuti** | Personalizzazione, progettazione, rendering | [Visualizza anteprima con profili di test](../using/content-management/preview-test.md), testa [più varianti](../using/test-approve/simulate-sample-input.md) con CSV/JSON, verifica [rendering](../using/content-management/rendering.md) tra dispositivi |
| **2. Controlli tecnici** | Recapitabilità, collegamenti, conflitti | Esegui i [controlli del punteggio di spam](../using/content-management/spam-report.md), convalida i collegamenti, controlla la presenza di [conflitti](../using/conflict-prioritization/conflicts.md) con altre campagne |
| **3. Logica del percorso** (solo percorsi) | Condizioni di ingresso, flusso, diramazione | Utilizza la [modalità test](../using/building-journeys/testing-the-journey.md) per simulare la progressione, esegui l’[esecuzione di prova](../using/building-journeys/journey-dry-run.md) per percorsi complessi |
| **4. Pre-avvio** | Impostazioni, approvazioni, monitoraggio | Invia per l’[approvazione](../using/test-approve/gs-approval.md), verifica pianificazioni e pubblico, abilita gli [avvisi](../using/reports/alerts.md) |

**Suggerimento:** inizia con il [playground per la personalizzazione](../using/personalization/personalize.md#playground) per testare le espressioni prima di creare il contenuto; e controlla sempre il [rilevamento di conflitti](../using/conflict-prioritization/conflicts.md) prima del lancio per evitare un invio eccessivo di messaggi.

## Test in azione: casi d’uso

Scopri come i concetti di test si applicano agli scenari reali:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/journeys-uc.md">
<img alt="Inviare messaggi multicanale" src="../using/assets/do-not-localize/start-journey.jpeg">
</a>
<div>
<a href="../using/building-journeys/journeys-uc.md"><strong>Inviare messaggi multicanale</strong></a>
</div>
<p>
Testa un percorso che combina Leggi pubblico, eventi di reazione e messaggi push/e-mail. Convalida l’intero flusso dal targeting del pubblico alla consegna dei messaggi. Concentrati sul coordinamento multicanale, sugli eventi di reazione, sulla convalida del flusso end-to-end e sui passaggi di test/pubblicazione.
</p>
</td>
<td>
<a href="../using/building-journeys/message-to-subscribers-uc.md">
<img alt="Inviare un messaggio agli iscritti" src="../using/assets/do-not-localize/start-quick.png">
</a>
<div>
<a href="../using/building-journeys/message-to-subscribers-uc.md"><strong>Inviare un messaggio agli iscritti</strong></a>
</div>
<p>
Testa i percorsi che hanno come target elenchi di iscrizioni con indirizzamento e-mail dinamico. Convalida le espressioni di personalizzazione per il targeting di iscritti corretto. Concentrati sulle espressioni di personalizzazione, l’indirizzamento dinamico e il targeting di elenchi di iscrizioni.
</p>
</td>
<td>
<a href="../using/building-journeys/weekday-email-uc.md">
<img alt="Inviare messaggi con limite di tempo" src="../using/assets/do-not-localize/calendar.jpeg">
</a>
<div>
<a href="../using/building-journeys/weekday-email-uc.md"><strong>Inviare messaggi con limite di tempo</strong></a>
</div>
<p>
Testa i percorsi con condizioni basate sul tempo per garantire che i messaggi vengano inviati in giorni specifici. Convalida le attività di attesa e la logica di pianificazione. Concentrati sulle condizioni basate sul tempo, sulle attività di attesa e sulla convalida della pianificazione.
</p>
</td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/jo-use-cases.md">
<img alt="Esplorare più casi d’uso del percorso" src="../using/assets/do-not-localize/icon-quick-start.svg">
</a>
<div>
<a href="../using/building-journeys/jo-use-cases.md"><strong>Esplorare più casi d’uso del percorso</strong></a>
</div>
<p>
Accedi a una raccolta completa di esempi pratici che riguardano eventi di esperienza, messaggistica multicanale e integrazioni di sistemi esterni. Esplora vari scenari, pattern avanzati e approcci di test dell’integrazione.
</p>
</td>
</tr></table>

## Terminologia chiave

Acquisisci familiarità con questi concetti di test essenziali per comprendere meglio le funzionalità di test e approvazione di Journey Optimizer. Ogni termine si collega alla documentazione dettagliata.

**[Profili di test](../using/content-management/test-profiles.md)**: profili cliente sintetici (non di clienti reali) utilizzati per visualizzare in anteprima i contenuti personalizzati. Contrassegnato nel servizio profilo cliente in tempo reale. Richiesto per la modalità test e l’anteprima del contenuto. [Scopri come creare i profili di test](../using/audience/creating-test-profiles.md)

**[Modalità test](../using/building-journeys/testing-the-journey.md)**: funzione di simulazione del percorso che invia i profili di test attraverso i percorsi del percorso. Limitazioni: solo percorsi di bozza, richiede spazio dei nomi e solo profili di test. [Consulta la documentazione sulla modalità test](../using/building-journeys/testing-the-journey.md)

**[Esecuzione di prova](../using/building-journeys/journey-dry-run.md)**: strumento di analisi dell’esecuzione del percorso che traccia i percorsi senza inviare messaggi o effettuare chiamate API. Caso d’uso: convalida della logica senza l’utilizzo di risorse. [Informazioni sull’esecuzione di prova](../using/building-journeys/journey-dry-run.md)

**[Dati di input di esempio](../using/test-approve/simulate-sample-input.md)**: file CSV o JSON contenenti i valori dell’attributo di profilo per testare la personalizzazione. Supporta fino a 30 varianti. Alternativa alla creazione di profili di test. [Come simulare varianti di contenuto](../using/test-approve/simulate-sample-input.md)

**[Elenchi di seed](../using/configuration/seed-lists.md)**: indirizzi e-mail di stakeholder interni inclusi automaticamente nelle consegne effettive (non invii di test). Solo canale e-mail. Caso d’uso: monitoraggio della qualità e conformità. [Configurare gli elenchi di seed](../using/configuration/seed-lists.md)

**[Esperimenti sui contenuti](../using/content-management/get-started-experiment.md)**: test A/B o esperimenti multi-armed bandit che mettono a confronto varianti di contenuto. Solo campagne, non disponibile in percorsi. [Introduzione agli esperimenti](../using/content-management/get-started-experiment.md) | [Creare esperimenti](../using/content-management/content-experiment.md)

**[Bozze](../using/content-management/proofs.md)**: testa le consegne e-mail inviate a indirizzi e-mail specifici utilizzando i dati del profilo di test. Diverso dagli elenchi di seed (le bozze sono invii di test manuali, gli elenchi di seed sono copie automatiche degli stakeholder). [Invia bozze](../using/content-management/proofs.md)

**[Rilevamento dei conflitti](../using/conflict-prioritization/conflicts.md)**: strumento che identifica campagne e percorsi sovrapposti il cui targeting sono gli stessi tipi di pubblico. Supporto limitato per il percorso: unitario, qualificazione del pubblico e solo tipi di Leggi pubblico. [Scopri la gestione dei conflitti](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Flussi di lavoro di approvazione](../using/test-approve/gs-approval.md)**: processo di revisione in più passaggi che richiede l’approvazione degli stakeholder prima dell’attivazione. Richiede la configurazione dei criteri di approvazione. [Configurare le approvazioni](../using/test-approve/gs-approval.md) | [Creare i criteri](../using/test-approve/approval-policies.md)

**[Test di rendering](../using/content-management/rendering.md)**: convalida della visualizzazione delle e-mail tra client e-mail (Gmail, Outlook, Apple Mail) e dispositivi. Richiede l’integrazione Litmus. [Testare il rendering delle e-mail](../using/content-management/rendering.md)

**[Playground di personalizzazione](../using/personalization/personalize.md#playground)**: ambiente di apprendimento interattivo per sperimentare la sintassi di personalizzazione e testare le espressioni con dati di esempio. Non è richiesto alcun set di dati live. [Accedere al playground](../using/personalization/personalize.md#playground)

## Risorse aggiuntive

>[!BEGINTABS]

>[!TAB Guide essenziali]

* [Simulare varianti di contenuto](../using/test-approve/simulate-sample-input.md): testa fino a 30 scenari di personalizzazione utilizzando file CSV o JSON. Ideale per il test dei contenuti multilingue senza creare più profili di test. Supporta e-mail, SMS, push, web, schede basate su codice, in-app e schede di contenuto.

* [Creazione di profili di test](../using/audience/creating-test-profiles.md): crea e gestisci i profili di test per simulare scenari reali della clientela. Scopri come contrassegnare i profili per il test, impostare gli attributi e organizzare i segmenti di test.

* [Rapporto spam sulle e-mail](../using/content-management/spam-report.md): controlla il punteggio di spam prima dell’invio per migliorare la recapitabilità e la consegna nella casella in entrata. Consigli fruibili per l’ottimizzazione dei contenuti.

* [Domande frequenti sui percorsi](../using/building-journeys/journey-faq.md): riferimenti rapidi per domande comuni sul test, l’esecuzione e la risoluzione dei problemi relativi ai percorsi.

>[!TAB Dipendenze e relazioni]

Scopri come le funzionalità di test si connettono tra loro e ai flussi di lavoro Journey Optimizer più ampi. In questa sezione vengono mappati i prerequisiti, le dipendenze a monte/a valle e le combinazioni di funzionalità comuni.

+++**Prerequisiti (richiesti prima del test)**

* I profili di test devono essere creati prima di utilizzare la modalità test o l’anteprima del contenuto
* I criteri di approvazione devono essere configurati prima dell’invio per l’approvazione
* È necessario creare elenchi di seed prima di aggiungerli a campagne/percorsi
* Integrazione Litmus richiesta per i test di rendering di e-mail
* Per utilizzare la modalità test, il percorso deve essere in stato bozza
* Il percorso deve avere uno spazio dei nomi configurato per utilizzare la modalità test

+++

+++**Da che cosa dipende il test (a monte)**

* Creazione di contenuti: campagne o percorsi da testare
* Profili di test: richiesti per la modalità test e l’anteprima del contenuto
* Criteri di approvazione: richiesti per i flussi di lavoro di approvazione
* Configurazione: configurazioni del canale, autenticazione e-mail, impostazioni del dominio

+++

+++**Che cosa dipende dai test (a valle)**

* Attivazione campagna/percorso: impossibile attivare senza risolvere gli errori
* Pubblicazione: potrebbe essere richiesta l’approvazione prima della pubblicazione
* Monitoraggio live: monitoraggio e rapporti dopo l’avvio
* Ottimizzazione: utilizza i risultati dei test per perfezionare le campagne future

+++

+++**Funzionalità correlate**

* Test + Flussi di lavoro di approvazione: processo di controllo qualità
* Test + Rilevamento dei conflitti: prevenzione dell’invio eccessivo di messaggi della clientela
* Test + Esperimenti di contenuto: ottimizzazione delle prestazioni
* Test + Rapporti: ciclo di miglioramento continuo
* Profili di test + Personalizzazione: convalida dei contenuti
* Esecuzione di prova + Modalità test: convalida del percorso completa

+++

+++**Combinazioni di funzionalità comuni**

* Test dei contenuti: profili di test + dati di input di esempio + playground di personalizzazione
* Convalida e-mail: test di rendering + punteggi di spam + profili di test + bozze
* Convalida del percorso: modalità test + esecuzione di prova + profili di test
* Lista di controllo per il pre-avvio: tutti i test tecnici + rilevamento dei conflitti + flussi di lavoro di approvazione

+++

>[!TAB Domande comuni]

+++**D: Quali test sono richiesti prima di avviare una campagna?**

**Minimo:** anteprima contenuto con profili di test + controllo punteggio di spam (e-mail)
**Consigliato:** + Rendering di e-mail + Rilevamento dei conflitti + Flusso di lavoro di approvazione
**Best practice:** + Test dati di input di esempio + Elenchi di seed + Esperimento A/B (in caso di ottimizzazione)

+++

+++**D: Come posso testare la personalizzazione senza creare molti profili di test?**

**Soluzione primaria:** utilizza [dati di input di esempio](../using/test-approve/simulate-sample-input.md) con file CSV/JSON (supporta fino a 30 varianti)
**Alternativa:** crea da 3 a 5 [profili di test](../using/audience/creating-test-profiles.md) rappresentativi che coprono segmenti chiave
**Strumento di apprendimento:** Primo esperimento in [playground di personalizzazione](../using/personalization/personalize.md#playground)

+++

+++**D: Qual è la differenza tra la modalità test e l’esecuzione di prova per i percorsi?**

**Modalità test:** invia profili di test tramite percorso, attiva azioni effettive e genera messaggi di test. Richiede percorso della bozza + spazio dei nomi.
**Esecuzione di prova:** traccia i percorsi di esecuzione senza inviare nulla. Funziona su qualsiasi stato del percorso. Nessun messaggio inviato, nessuna azione eseguita.
**Utilizzare insieme:** modalità test per test dei messaggi + Esecuzione di prova per convalida della logica - copertura completa.

+++

+++**D: Come posso testare i percorsi nello stato produzione/live?**

**Modalità test:** No. Solo in percorsi in bozza
**Esecuzione di prova:** Sì. Funziona su qualsiasi stato del percorso
**Anteprima contenuto:** Sì. Puoi visualizzare l’anteprima di singoli messaggi in qualsiasi momento
**Soluzione:** duplica il percorso live per ottenerne uno con lo stato “bozza” su cui puoi eseguire la convalida completa in modalità test

+++

+++**D: Quali funzionalità di test richiedono integrazioni esterne?**

**Rendering di e-mail:** richiede l’integrazione Litmus (licenza separata)
**Tutti gli altri:** incorporati in Journey Optimizer, nessuna integrazione aggiuntiva richiesta
**Nota:** i profili di test richiedono il servizio profilo cliente in tempo reale (incluso)

+++

+++**D: Come posso testare le campagne attivate da API?**

**Opzione 1:** utilizza [API di simulazione campagna](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} per test programmatici
**Opzione 2:** visualizza anteprima del contenuto con i profili di test nell’interfaccia utente
**Opzione 3:** invia bozze per testare gli indirizzi e-mail
**Best practice:** combina queste tre opzioni per una convalida completa

+++

>[!ENDTABS]
