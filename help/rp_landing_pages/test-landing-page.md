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
source-git-commit: fb13aee243757de7fe47bdd9d9ebad47069e24ba
workflow-type: tm+mt
source-wordcount: '3103'
ht-degree: 4%

---

# Test, convalida e approvazione{#section-overview}

Questa sezione descrive tutte le funzionalità di test e approvazione in Journey Optimizer. Troverai strumenti per visualizzare in anteprima i contenuti con profili di test, convalidare la logica di percorso, controllare il rendering di e-mail e i punteggi di spam, eseguire esperimenti A/B, rilevare i conflitti e impostare flussi di lavoro di approvazione.

Questa pagina di destinazione consente di scegliere l’approccio di test corretto in base a ciò che stai creando (campagne anziché percorsi), illustra i flussi di lavoro di test consigliati e fornisce un accesso rapido a tutte le risorse di test e approvazione. Inizia con [Scegli il tuo approccio di test](#choose-your-testing-approach) di seguito per identificare gli strumenti applicabili al tuo caso d&#39;uso.

## Panoramica delle funzionalità di test

**Tipi di test disponibili:**

* Test del contenuto: visualizza l&#39;anteprima e convalida del contenuto del messaggio prima di inviare → [Campagne di test](#testing-campaigns), [Verifica della personalizzazione](#testing-personalization)
* Test della logica di percorso: simulare la progressione del cliente attraverso i percorsi di percorso → [percorsi di test](#testing-journeys)
* Test tecnici: Convalida rendering, recapito messaggi e autenticazione → [Convalida tecnica](#2-technical-validation)
* Test delle prestazioni: confrontare le varianti di contenuto utilizzando esperimenti A/B → [Esperimenti di contenuto](#content-experiments--ab-testing)
* Test dei conflitti: rilevamento sovrapposizioni campagna e percorso → [Rilevamento conflitti](#conflict-detection)
* Test di approvazione: flussi di lavoro di revisione strutturati prima dell&#39;attivazione → [Flussi di lavoro di approvazione](#approval-workflows-for-journeys-and-campaigns)

**Funzionalità chiave per contesto:**

| Funzionalità | Applicabile a | Limitazioni per il canale | Prerequisiti | Scopo principale | Documentazione |
|------------|-----------|---------------------|--------------|-----------------|---------------|
| [Profili di test](../using/content-management/test-profiles.md) | Campagne, Percorsi | Tutti i canali | Profili di test creati | Anteprima di contenuti personalizzati | [Guida](#testing-campaigns) |
| [Dati di input di esempio](../test-approve/simulate-sample-input.md) | Campagne, Percorsi | E-mail, SMS, push, web, basato su codice, in-app, schede di contenuto | File CSV/JSON | Test di più varianti di personalizzazione | [Guida](#simulate-content-variations) |
| [Modalità di prova](../using/building-journeys/testing-the-journey.md) | Solo percorsi | N/D | Bozza di percorso, spazio dei nomi configurato | Simula progressione profilo | [Scheda](#test-your-journey) |
| [Esecuzione a secco](../using/building-journeys/journey-dry-run.md) | Solo percorsi | N/D | Percorso creato | Analizzare i percorsi di esecuzione | [Scheda](#journey-dry-run) |
| [Rendering e-mail](../using/content-management/rendering.md) | Campagne, Percorsi | Solo e-mail | Integrazione con Litmus | Verifica della visualizzazione tra client | [Flusso di lavoro](#2-technical-validation) |
| [Punteggio posta indesiderata](../using/content-management/spam-report.md) | Campagne, Percorsi | Solo e-mail | Nessuna | Convalida del recapito | [Flusso di lavoro](#2-technical-validation) |
| [Elenchi seed](../using/configuration/seed-lists.md) | Campagne, Percorsi | Solo e-mail | Elenco seed configurato | Monitoraggio delle parti interessate | [Scheda](#seed-lists-for-stakeholder-monitoring) |
| [Esperimenti sui contenuti](../using/content-management/get-started-experiment.md) | Solo campagne | Tutti i canali | Nessuna | Test A/B e slot machine | [Scheda](#content-experiments--ab-testing) |
| [Rilevamento conflitti](../using/conflict-prioritization/conflicts.md) | Campagne, Percorsi (limitati) | Tutti i canali | Nessuna | Impedisci messaggi eccessivi del cliente | [Scheda](#conflict-detection) |
| [Flussi di lavoro di approvazione](../using/test-approve/gs-approval.md) | Campagne, Percorsi | Tutti i canali | Criterio di approvazione creato | Processo di revisione strutturato | [Scheda](#approval-workflows-for-journeys-and-campaigns) |
| [Area di riproduzione Personalization](../using/personalization/personalize.md#playground) | Tutto | Tutti i canali | Nessuna | Scopri e verifica la sintassi di personalizzazione | [Scheda](#personalization-playground) |

**Flussi di lavoro di test comuni:**

1. Pre-sviluppo: utilizza [area di riproduzione per la personalizzazione](#testing-personalization) per apprendere la sintassi
2. Durante lo sviluppo: anteprima con [profili di test](#testing-campaigns), convalida con [dati di input di esempio](#simulate-content-variations)
3. Pre-avvio: esegui [test tecnici](#2-technical-validation) (rendering, spam), seleziona [conflitti](#conflict-detection), invia per [approvazione](#approval-workflows-for-journeys-and-campaigns)
4. Post-avvio: monitoraggio con rapporti live (vedi [Monitoraggio e risoluzione dei problemi](#monitoring--troubleshooting)), iterazione in base ai risultati


## Perché le prove e le approvazioni sono importanti

I processi di test e approvazione fungono da gate di qualità essenziali che proteggono la reputazione del tuo marchio e garantiscono il successo della campagna. Ecco perché sono importanti:

* **Rileva gli errori prima che raggiungano i clienti** - Identifica collegamenti interrotti, personalizzazione non corretta, problemi di rendering e errori di logica in un ambiente controllato in cui le correzioni sono rapide e prive di rischi.

* **Migliora il recapito messaggi** - Verifica i punteggi di posta indesiderata, convalida l&#39;autenticazione e-mail e verifica il rendering tra client e-mail per massimizzare il posizionamento della casella in entrata e le percentuali di coinvolgimento.

* **Assicurati della coerenza del brand** - Anteprima di contenuti con profili di test diversi per verificare che la personalizzazione venga visualizzata correttamente per vari segmenti di clienti e mantenga gli standard del brand.

* **Convalida percorsi complessi** - Simula flussi di percorso con più passaggi per verificare che i trigger vengano attivati correttamente, che le condizioni vengano valutate correttamente e che i clienti ricevano i messaggi corretti al momento giusto.

* **Stabilisci la responsabilità** - Implementa flussi di lavoro di approvazione formali che richiedono l&#39;approvazione delle parti interessate, creando una chiara proprietà e riducendo i lanci non autorizzati o prematuri di campagne.

* **Risparmia tempo e risorse** - Rileva i problemi all&#39;inizio del ciclo di sviluppo quando le correzioni sono più economiche e veloci, evitando costose correzioni post-avvio o escalation del servizio clienti.

## Terminologia chiave

**[Profili di test](../using/content-management/test-profiles.md)** = Profili cliente sintetici (non clienti reali) utilizzati per visualizzare in anteprima i contenuti personalizzati. Contrassegnato nel servizio Profilo cliente in tempo reale. Obbligatorio per la modalità di test e l’anteprima del contenuto. [Scopri come creare profili di test](../using/audience/creating-test-profiles.md)

**[Modalità di test](../using/building-journeys/testing-the-journey.md)** = funzionalità di simulazione del Percorso che invia i profili di test attraverso i percorsi del percorso. Limitazioni: solo percorsi in stato di bozza, richiede spazio dei nomi e solo profili di test. [Consulta la documentazione sulla modalità di test](../using/building-journeys/testing-the-journey.md)

**[Esecuzione in prova](../using/building-journeys/journey-dry-run.md)** = strumento di analisi dell&#39;esecuzione del Percorso che traccia i percorsi senza inviare messaggi o effettuare chiamate API. Caso di utilizzo: convalida della logica senza utilizzare risorse. [Informazioni sull&#39;esecuzione in prova](../using/building-journeys/journey-dry-run.md)

**[Dati di input di esempio](../test-approve/simulate-sample-input.md)** = file CSV o JSON contenenti i valori degli attributi di profilo per testare la personalizzazione. Supporta fino a 30 varianti. Alternativa alla creazione di profili di test. [Simulare varianti di contenuto](../test-approve/simulate-sample-input.md)

**[Elenchi seed](../using/configuration/seed-lists.md)** = Indirizzi e-mail delle parti interessate interne inclusi automaticamente nelle consegne effettive (non negli invii di test). Solo canale e-mail. Caso d’uso: monitoraggio della qualità e conformità. [Configura elenchi seed](../using/configuration/seed-lists.md)

**[Esperimenti di contenuto](../using/content-management/get-started-experiment.md)** = test A/B o esperimenti con slot machine che mettono a confronto varianti di contenuto. Solo campagne, non disponibile in percorsi. [Introduzione agli esperimenti](../using/content-management/get-started-experiment.md) | [Crea esperimenti](../using/content-management/content-experiment.md)

**[Bozze](../using/content-management/proofs.md)** = Verifica delle consegne e-mail inviate a indirizzi e-mail specifici utilizzando i dati del profilo di test. Diverso dagli elenchi seed (le bozze sono invii di test manuali, gli elenchi seed sono copie automatiche delle parti interessate). [Invia bozze](../using/content-management/proofs.md)

**[Rilevamento dei conflitti](../using/conflict-prioritization/conflicts.md)** = Strumento che identifica le campagne e i percorsi sovrapposti che si rivolgono agli stessi tipi di pubblico. Supporto limitato per il percorso: unitari, qualificazione del pubblico e solo tipi di pubblico lettura. [Informazioni sulla gestione dei conflitti](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Flussi di lavoro di approvazione](../using/test-approve/gs-approval.md)** = Processo di revisione in più passaggi che richiede l&#39;approvazione delle parti interessate prima dell&#39;attivazione. Richiede la configurazione dei criteri di approvazione. [Configura approvazioni](../using/test-approve/gs-approval.md) | [Crea criteri](../using/test-approve/approval-policies.md)

**[Test di rendering](../using/content-management/rendering.md)** = convalida della visualizzazione delle e-mail tra client e-mail (Gmail, Outlook, Apple Mail) e dispositivi. Richiede l&#39;integrazione con Litmus. [Test rendering e-mail](../using/content-management/rendering.md)

**[Ambiente playground di Personalization](../using/personalization/personalize.md#playground)** = ambiente di apprendimento interattivo per sperimentare la sintassi di personalizzazione e testare le espressioni con dati di esempio. Non è richiesto alcun set di dati live. [Accedi al parco giochi](../using/personalization/personalize.md#playground)

## Albero decisionale per la selezione del metodo di prova

Utilizza questa struttura decisionale per identificare rapidamente gli strumenti di test corretti per lo scenario specifico. Rispondi a ogni domanda in base al contesto (cosa stai creando, cosa devi convalidare e quale canale stai utilizzando) per passare direttamente alle funzionalità e alla documentazione pertinenti.

+++ **Domanda 1: Cosa stai testando?**

* Campaign → [Test delle campagne](#testing-campaigns)
* Percorso → [percorsi di prova](#testing-journeys)
* Espressioni Personalization → [Ambiente playground Personalization](#testing-personalization)
+++

+++**Domanda 2: quale aspetto deve essere convalidato?**

* Contenuto e personalizzazione → [Profili di test](#testing-campaigns) o [Dati di input di esempio](#simulate-content-variations)
* Visualizzazione e-mail → [Test di rendering e-mail](#2-technical-validation)
* Recapito messaggi → [Controlli punteggio posta indesiderata](#2-technical-validation)
* Logica di percorso e flusso → [Modalità di test](#testing-journeys) o [esecuzione in prova](#journey-dry-run)
* Confronto delle prestazioni → [Esperimento sui contenuti](#content-experiments--ab-testing) (solo campagne)
* Conflitti di tempistica → [Rilevamento conflitti](#conflict-detection)
* Revisione delle parti interessate → [Flusso di lavoro di approvazione](#approval-workflows-for-journeys-and-campaigns)
+++

+++**Domanda 3: quale canale?**

* E-mail → Tutti i metodi di test disponibili (consulta [Campagne di test](#testing-campaigns))
* SMS, → push [Test del contenuto](#testing-campaigns), [dati di input di esempio](#simulate-content-variations), [flussi di lavoro di approvazione](#approval-workflows-for-journeys-and-campaigns)
* Web, in-app, basato su codice → [Test dei contenuti](#testing-campaigns), [dati di input di esempio](#simulate-content-variations), [flussi di lavoro di approvazione](#approval-workflows-for-journeys-and-campaigns)
* Più canali → Testare ogni canale separatamente
+++

+++**Domanda 4: quando nel flusso di lavoro?**

* Prima di creare → [parco giochi Personalization](#personalization-playground) per l&#39;apprendimento
* → Durante la generazione di [profili di test](#testing-campaigns) e [dati di input di esempio](#simulate-content-variations) per la convalida
* Prima dell&#39;avvio → [test di rendering](#2-technical-validation), [controlli di posta indesiderata](#email-spam-report), [rilevamento conflitti](#conflict-detection), [approvazioni](#approval-workflows-for-journeys-and-campaigns)
* Dopo l&#39;avvio → [rapporti live](../using/building-journeys/report-journey.md) e [monitoraggio](#monitoring--troubleshooting)
+++


## Scegli il tuo approccio di test

L’approccio corretto per i test dipende da cosa stai creando e da cosa devi convalidare. Usa questa guida per identificare gli strumenti di test più rilevanti per lo scenario.

### Test delle campagne

**Per tutte le campagne:**

* Anteprima e test del contenuto tramite [profili di test](../using/content-management/test-profiles.md) o [dati di input di esempio](../test-approve/simulate-sample-input.md)
* Controlla [il rendering di e-mail](../using/content-management/rendering.md) tra dispositivi e client (solo canale e-mail)
* Esegui [controlli punteggio posta indesiderata](../using/content-management/spam-report.md) (solo canale e-mail)
* Rivedi [conflitti](../conflict-prioritization/conflicts.md) con altre campagne e altri percorsi
* Configura [elenchi seed](../configuration/seed-lists.md) per il monitoraggio delle parti interessate (solo canale e-mail)
* Invia per [approvazione](../using/test-approve/gs-approval.md) prima dell&#39;attivazione

**Per test A/B e ottimizzazione:**

* Crea [esperimenti di contenuto](../using/content-management/get-started-experiment.md) per testare più trattamenti e misurare le prestazioni

**Per campagne attivate da API:**

* Utilizza l&#39;[API di simulazione campagna](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} per attivare i processi di bozza a livello di programmazione

### Percorsi di prova

**Per tutti i percorsi:**

* Utilizza la [modalità di test](../using/building-journeys/testing-the-journey.md) per simulare la progressione del profilo (solo per percorsi bozza, richiede spazio dei nomi) oppure [esecuzione inattiva](../using/building-journeys/journey-dry-run.md) per analizzare i percorsi di esecuzione senza inviare messaggi
* Verifica singoli messaggi tramite [anteprima e bozze](../using/content-management/preview-test.md)
* Controlla [conflitti](../conflict-prioritization/conflicts.md) con altri percorsi e campagne
* Invia per [approvazione](../using/test-approve/gs-approval.md) prima di pubblicare

**Per percorsi complessi:**

* Utilizza la modalità di test ed esegui a secco insieme per convalidare completamente la logica di diramazione e i percorsi di esecuzione
* Verificare sistematicamente condizioni di ingresso e attributi di profilo diversi

**Nota:** il rilevamento dei conflitti e la limitazione dei percorsi sono disponibili solo per percorsi di pubblico unitari, di qualificazione del pubblico e di lettura.

### Verifica della personalizzazione

**Prima di creare il contenuto:**

* Esperimento nel [parco giochi di personalizzazione](../using/personalization/personalize.md#playground) per apprendere la sintassi e testare le espressioni con dati di esempio

**Durante la creazione del contenuto:**

* Anteprima con [profili di test](../using/content-management/test-profiles.md) per convalidare correttamente i rendering di personalizzazione
* Verifica più scenari utilizzando [dati di input di esempio](../test-approve/simulate-sample-input.md) da file CSV/JSON (supporta fino a 30 varianti)

## Best practice di test

Per massimizzare l’efficacia delle attività di test, segui queste pratiche consigliate:

1. **Esegui il test in anticipo e spesso** - Non aspettare che una campagna sia completamente generata. Puoi testare contenuti, personalizzazione e logica in modo incrementale durante lo sviluppo.

1. **Utilizza profili di test realistici** - [Crea profili di test](../using/audience/creating-test-profiles.md) che rappresentino con precisione i segmenti di pubblico target, inclusi casi limite e diversi scenari di personalizzazione.

1. **Verifica tra dispositivi e client** - Verifica il [rendering di e-mail](../using/content-management/rendering.md) nei client e-mail più diffusi (Gmail, Outlook, Apple Mail) e nei dispositivi (desktop, dispositivi mobili, tablet) per garantire una visualizzazione coerente (solo canale e-mail).

1. **Convalida della personalizzazione in modo completo** - Verifica con più [profili di test](../using/content-management/test-profiles.md) che hanno valori di attributo diversi per confermare che i token di personalizzazione vengano visualizzati correttamente e che i valori di fallback funzionino. Utilizza il [parco giochi di personalizzazione](../using/personalization/personalize.md#playground) per sperimentare espressioni di personalizzazione e testare il codice con dati di esempio prima di applicarli alle campagne.

1. **Verifica varianti di contenuto con dati di esempio**. Utilizza [dati di input di esempio](../test-approve/simulate-sample-input.md) da file CSV o JSON per testare fino a 30 scenari di personalizzazione senza creare numerosi profili di test, risparmiando tempo e garantendo al contempo una copertura completa. Supporta i canali di e-mail, SMS, push, web, esperienza basata su codice, in-app e schede di contenuto.

1. **Utilizza elenchi seed per il monitoraggio delle parti interessate**. Configura [elenchi seed](../configuration/seed-lists.md) per includere automaticamente le parti interessate interne che riceveranno copie di tutte le consegne al momento dell&#39;esecuzione per il monitoraggio della qualità e la verifica della conformità (solo canale e-mail).

1. **Simula percorsi di percorso**. Per percorsi complessi con più rami, utilizza la [modalità di test](../using/building-journeys/testing-the-journey.md) per testare condizioni di ingresso e attributi di profilo diversi e convalidare tutti i percorsi possibili. Disponibile per i percorsi 2D che utilizzano uno spazio dei nomi.

1. **Verifica gli indicatori di recapito messaggi** - Rivedi [i punteggi di posta indesiderata](../using/content-management/spam-report.md), lo stato di autenticazione e le metriche di integrità delle e-mail prima degli invii di grandi dimensioni (solo canale e-mail).

1. **Documenta i risultati dei test** - Conserva i record dei risultati dei test, dei problemi rilevati e delle risoluzioni per migliorare i processi di test futuri e condividi gli insegnamenti con il tuo team.

1. **Coinvolgi le parti interessate in anticipo** - Condividi anteprime e risultati dei test con le parti interessate prima dell&#39;[approvazione formale](../using/test-approve/gs-approval.md) per raccogliere feedback e allineare le aspettative.

## Flusso di lavoro di test consigliato

Segui questo approccio sistematico per garantire test approfonditi e approvazioni senza problemi:

### &#x200B;1. Sviluppo e anteprima dei contenuti

Inizia creando i contenuti e utilizzando le funzionalità di anteprima per verificare la progettazione e la personalizzazione iniziali:

* Progetta [e-mail](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [notifica push](../using/push/create-push.md) o altro contenuto del canale

* Utilizza la funzionalità **[Simula contenuto](../using/content-management/preview-test.md)** per visualizzare in anteprima con i profili di test

* Controlla [token di personalizzazione](../using/personalization/personalization-syntax.md), contenuto dinamico e valori di fallback

* Prova le espressioni di personalizzazione nel **[parco giochi di personalizzazione](../using/personalization/personalize.md#playground)** per testare e perfezionare il codice con dati di esempio prima di applicarlo al contenuto live

* Test di più varianti utilizzando **[dati di input di esempio](../test-approve/simulate-sample-input.md)** da file CSV/JSON per convalidare la personalizzazione in diversi scenari di profilo

* Verifica il rendering di [1} in diverse dimensioni dello schermo e client di posta elettronica](../using/content-management/rendering.md)

### &#x200B;2. Convalida tecnica

Convalidare gli aspetti tecnici che influiscono sulla consegna dei messaggi e sulle funzionalità:

* Esegui [controlli punteggio posta indesiderata](../using/content-management/spam-report.md) per identificare potenziali problemi di recapito messaggi

* Verifica i collegamenti per assicurarti che non siano interrotti e che siano tracciati correttamente

* Convalida configurazione [autenticazione e-mail](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC)

* Esamina il rendering HTML e verifica la presenza di problemi di compatibilità CSS

* Test della [progettazione reattiva](../using/email/content-from-scratch.md) su dispositivi mobili e desktop

* Verifica la presenza di [potenziali conflitti](../conflict-prioritization/conflicts.md) con altre campagne e altri percorsi per evitare problemi di affaticamento dei messaggi del cliente e di tempistica

### &#x200B;3. Prove di Percorso (solo percorsi)

Se stai testando un percorso, convalida la logica di orchestrazione:

* Attiva **[Modalità test](../using/building-journeys/testing-the-journey.md)** per simulare la progressione del profilo nel percorso

* Test di [condizioni di ingresso](../using/building-journeys/entry-management.md) e qualifiche del pubblico diverse

* Verifica che le [attività attendi](../using/building-journeys/wait-activity.md), [condizioni](../using/building-journeys/condition-activity.md) e la logica di diramazione funzionino correttamente

* Utilizza **[Esegui a secco](../using/building-journeys/journey-dry-run.md)** per percorsi complessi per analizzare i percorsi di esecuzione senza inviare messaggi

* Verifica che [eventi](../using/event/about-events.md) vengano attivati correttamente e che [azioni personalizzate](../using/action/about-custom-action-configuration.md) vengano eseguite come previsto

### &#x200B;4. Presentazione dell’approvazione

Una volta completato il test e risolti i problemi:

* Invia la campagna o il percorso per l&#39;approvazione in base ai [criteri di approvazione](../using/test-approve/approval-policies.md) della tua organizzazione

* Includi i risultati dei test e la documentazione con la [richiesta di approvazione](../using/test-approve/request-approval.md)

* Risolvi eventuali feedback o richieste di modifica da [approvatori](../using/test-approve/review-approve-request.md)

* Effettuare le revisioni necessarie e ripetere il test se le modifiche sono significative

### &#x200B;5. Verifica pre-lancio

Prima di attivare la campagna o il percorso:

* Esegui una revisione finale di tutte le impostazioni, tipi di pubblico e [pianificazioni](../using/building-journeys/journey-properties.md)

* Verifica che tutte le approvazioni siano attive e documentate

* Conferma che gli orari di invio e i [fusi orari](../using/building-journeys/timezone-management.md) siano corretti

* Abilita [monitoraggio e avvisi](../using/reports/alerts.md) per monitorare le prestazioni dopo l&#39;avvio

### &#x200B;6. Monitorare e ripetere

Dopo il lancio, continua il monitoraggio per rilevare eventuali problemi in anticipo:

* Configura [avvisi di sistema](../using/reports/alerts.md) per errori di percorso, tassi di mancato recapito elevati o coinvolgimento ridotto

* Rivedi [rapporti live](../using/building-journeys/report-journey.md) per tenere traccia delle prestazioni rispetto alle aspettative

* Preparati a [sospendere o modificare](../using/building-journeys/journey-pause.md) percorsi in caso di problemi critici

* Documentare le lezioni apprese per migliorare i processi di testing futuri

## Test in azione: casi d’uso

Scopri come i concetti di test si applicano agli scenari reali:

| Caso d’uso | Cosa imparerai | Obiettivo principali dei test |
|----------|-------------------|-------------------|
| **[Inviare messaggi multicanale](../using/building-journeys/journeys-uc.md)** | Test di un percorso che combina Read Audience, eventi di reazione e messaggi e-mail/push. Convalida l’intero flusso dal targeting del pubblico alla consegna dei messaggi. | Coordinazione multicanale, eventi di reazione, convalida del flusso end-to-end, passaggi di test e pubblicazione |
| **[Invia un messaggio ai sottoscrittori](../using/building-journeys/message-to-subscribers-uc.md)** | Percorsi di test che eseguono il targeting degli elenchi di abbonamenti con indirizzi e-mail dinamici. Convalida le espressioni di personalizzazione per il targeting corretto del sottoscrittore. | Espressioni Personalization, indirizzamento dinamico, targeting degli elenchi di iscrizioni |
| **[Invio di messaggi con limiti di tempo](../using/building-journeys/weekday-email-uc.md)** | Verifica i percorsi con condizioni basate sul tempo per garantire che i messaggi vengano inviati in giorni specifici. Convalida le attività di attesa e la logica di pianificazione. | Condizioni basate sul tempo, attività di attesa, convalida della pianificazione |
| **[Esplora altri casi d&#39;uso del percorso](../using/building-journeys/jo-use-cases.md)** | Accedi a una raccolta completa di esempi pratici che riguardano eventi di esperienza, messaggistica multicanale e integrazioni di sistemi esterne. | Vari scenari, modelli avanzati, test dell’integrazione |

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

## Risorse aggiuntive

### Guide alla verifica e alla convalida essenziali

* [Simula varianti di contenuto](../test-approve/simulate-sample-input.md) - Puoi testare fino a 30 scenari di personalizzazione utilizzando file CSV o JSON. Ideale per il test dei contenuti multilingue senza creare più profili di test. Supporta e-mail, SMS, push, web, schede basate su codice, in-app e di contenuto.

* [Creazione di profili di test](../using/audience/creating-test-profiles.md) - Creazione e gestione di profili di test per simulare scenari cliente. Scopri come contrassegnare i profili per il test, impostare gli attributi e organizzare i segmenti di test.

* [Rapporto posta indesiderata](../using/content-management/spam-report.md) - Controlla i punteggi di posta indesiderata prima dell&#39;invio per migliorare il recapito messaggi e il posizionamento della casella in entrata. Consigli fruibili per l’ottimizzazione dei contenuti.

* [Domande frequenti sul Percorso](../using/building-journeys/journey-faq.md) - Riferimento rapido per le domande comuni su test, esecuzione e risoluzione dei problemi del percorso.

### Dipendenze e relazioni

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

* Flussi di lavoro di test e approvazione = processo di controllo qualità
* Test + Rilevamento dei conflitti = Impedire ai clienti di inviare messaggi eccessivi
* Test + esperimenti di contenuto = ottimizzazione delle prestazioni
* Test + Reporting = Ciclo di miglioramento continuo
* Profili di test + Personalization = convalida del contenuto
* Esecuzione a secco + modalità test = convalida completa del percorso

+++

+++**Combinazioni di funzionalità comuni**

* Test dei contenuti: profili di test + dati di input di esempio + area di riproduzione Personalization
* Convalida e-mail: test di rendering + punteggi spam + profili di test + bozze
* Convalida del percorso: modalità di test + esecuzione a secco + profili di test
* Lista di controllo per il pre-lancio: tutti i test tecnici + rilevamento dei conflitti + flussi di lavoro di approvazione

+++

### Domande comuni

+++**D: quali test sono necessari prima di avviare una campagna?**

**Minimo:** anteprima contenuto con profili di test + controllo punteggio posta indesiderata (e-mail)
**Consigliato:** + Rendering di e-mail + Rilevamento conflitti + Flusso di lavoro di approvazione
**Best practice:** + Test dei dati di input di esempio + Elenchi seed + Esperimento A/B (in caso di ottimizzazione)

+++

+++**D: come posso testare la personalizzazione senza creare molti profili di test?**

**Soluzione primaria:** utilizza [dati di input di esempio](../test-approve/simulate-sample-input.md) con file CSV/JSON (supporta fino a 30 varianti)
**Alternativa:** creare da 3 a 5 [profili di test](../using/audience/creating-test-profiles.md) rappresentativi che coprono segmenti chiave
**Strumento di apprendimento:** Esperimento iniziale in [area giochi di personalizzazione](../using/personalization/personalize.md#playground)

+++

+++**D: qual è la differenza tra la modalità di test e l&#39;esecuzione in prova per i percorsi?**

**Modalità di test:** invia i profili di test tramite il percorso, attiva le azioni effettive e genera i messaggi di test. Richiede bozza di percorso e spazio dei nomi.
**Esecuzione in prova:** traccia i percorsi di esecuzione senza inviare nulla. Funziona su qualsiasi stato del percorso. Nessun messaggio inviato, nessuna azione eseguita.
**Usare insieme:** Modalità di test per il test dei messaggi + Esecuzione a secco per la convalida logica = copertura completa.

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

**Opzione 1:** Utilizza [API di simulazione campagna](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} per test programmatici
**Opzione 2:** Anteprima del contenuto con i profili di test nell&#39;interfaccia utente
**Opzione 3:** Inviare bozze agli indirizzi e-mail di prova
**Best practice:** combina tutti e tre per una convalida completa

+++


### Argomenti correlati

* [Gestione dei contenuti](content-management-landing-page.md) - Scopri come progettare, visualizzare in anteprima e gestire i contenuti utilizzando modelli, frammenti e il Designer e-mail. Best practice per la creazione di contenuti principali per un branding coerente.

* [Reporting e analisi](reporting-landing-page.md) - Analizza le prestazioni di campagne e percorsi con report, dashboard e metriche complete. Prendi decisioni basate sui dati per ottimizzare le esperienze dei clienti.

* [Configurazione Percorso](configure-journeys-landing-page.md) - Configura origini dati, eventi e azioni personalizzate per abilitare una sofisticata orchestrazione del percorso. Imposta le basi tecniche per la creazione del percorso.

* [Gestione campagne](../using/campaigns/get-started-with-campaigns.md) - Esplora diversi tipi di campagne e scopri come creare, pianificare e ottimizzare campagne batch e in tempo reale per il massimo impatto.
