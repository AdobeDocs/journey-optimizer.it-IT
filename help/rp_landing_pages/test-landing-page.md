---
solution: Journey Optimizer
product: Journey Optimizer
title: Testare e approvare
description: Testare e approvare
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 11%

---

# Testare e approvare{#section-overview}

Il controllo qualità è fondamentale per offrire ai clienti esperienze eccezionali. Adobe Journey Optimizer fornisce funzionalità complete di test e approvazione per aiutarti a convalidare i contenuti, verificare la logica di percorso e garantire che le campagne soddisfino gli standard di qualità prima di raggiungere il tuo pubblico. Dall’anteprima di messaggi personalizzati con profili di test alla simulazione di flussi di percorso complessi, questi strumenti ti consentono di identificare e risolvere i problemi in anticipo, ridurre i rischi e mantenere l’integrità del brand. Che tu stia testando il rendering di e-mail tra dispositivi, convalidando percorsi con più passaggi o stabilendo flussi di lavoro di approvazione formali, questa sezione ti guida attraverso procedure consigliate e processi dettagliati per creare fiducia nelle campagne e nei percorsi. Implementando test approfonditi e approvazioni strutturate, potrai ridurre al minimo gli errori, migliorare il recapito messaggi e creare esperienze fluide che risuonano con i tuoi clienti.

## Perché le prove e le approvazioni sono importanti

I processi di test e approvazione fungono da gate di qualità essenziali che proteggono la reputazione del tuo marchio e garantiscono il successo della campagna. Ecco perché sono importanti:

* **Rileva gli errori prima che raggiungano i clienti** - Identifica collegamenti interrotti, personalizzazione non corretta, problemi di rendering e errori di logica in un ambiente controllato in cui le correzioni sono rapide e prive di rischi.

* **Migliora il recapito messaggi** - Verifica i punteggi di posta indesiderata, convalida l&#39;autenticazione e-mail e verifica il rendering tra client e-mail per massimizzare il posizionamento della casella in entrata e le percentuali di coinvolgimento.

* **Assicurati della coerenza del brand** - Anteprima di contenuti con profili di test diversi per verificare che la personalizzazione venga visualizzata correttamente per vari segmenti di clienti e mantenga gli standard del brand.

* **Convalida percorsi complessi** - Simula flussi di percorso con più passaggi per verificare che i trigger vengano attivati correttamente, che le condizioni vengano valutate correttamente e che i clienti ricevano i messaggi corretti al momento giusto.

* **Stabilisci la responsabilità** - Implementa flussi di lavoro di approvazione formali che richiedono l&#39;approvazione delle parti interessate, creando una chiara proprietà e riducendo i lanci non autorizzati o prematuri di campagne.

* **Risparmia tempo e risorse** - Rileva i problemi all&#39;inizio del ciclo di sviluppo quando le correzioni sono più economiche e veloci, evitando costose correzioni post-avvio o escalation del servizio clienti.

## Best practice di test

Per massimizzare l’efficacia delle attività di test, segui queste pratiche consigliate:

1. **Esegui il test in anticipo e spesso** - Non aspettare che una campagna sia completamente generata. Puoi testare contenuti, personalizzazione e logica in modo incrementale durante lo sviluppo.

1. **Utilizza profili di test realistici** - [Crea profili di test](../using/audience/creating-test-profiles.md) che rappresentino con precisione i segmenti di pubblico target, inclusi casi limite e diversi scenari di personalizzazione.

1. **Verifica tra dispositivi e client** - Verifica il [rendering di e-mail](../using/content-management/rendering.md) nei client e-mail più diffusi (Gmail, Outlook, Apple Mail) e nei dispositivi (desktop, dispositivi mobili, tablet) per garantire una visualizzazione coerente.

1. **Convalida della personalizzazione in modo completo** - Verifica con più [profili di test](../using/content-management/test-profiles.md) che hanno valori di attributo diversi per confermare che i token di personalizzazione vengano visualizzati correttamente e che i valori di fallback funzionino.

1. **Simula percorsi di percorso**. Per percorsi complessi con più rami, utilizza la [modalità di test](../using/building-journeys/testing-the-journey.md) per testare condizioni di ingresso e attributi di profilo diversi e convalidare tutti i percorsi possibili.

1. **Verifica gli indicatori di recapito messaggi** - Rivedi [i punteggi di posta indesiderata](../using/content-management/spam-report.md), lo stato di autenticazione e le metriche di integrità delle e-mail prima di invii di grandi dimensioni.

1. **Documenta i risultati dei test** - Conserva i record dei risultati dei test, dei problemi rilevati e delle risoluzioni per migliorare i processi di test futuri e condividi gli insegnamenti con il tuo team.

1. **Coinvolgi le parti interessate in anticipo** - Condividi anteprime e risultati dei test con le parti interessate prima dell&#39;[approvazione formale](../using/test-approve/gs-approval.md) per raccogliere feedback e allineare le aspettative.

## Flusso di lavoro di test consigliato

Segui questo approccio sistematico per garantire test approfonditi e approvazioni senza problemi:

### &#x200B;1. Sviluppo e anteprima dei contenuti

Inizia creando i contenuti e utilizzando le funzionalità di anteprima per verificare la progettazione e la personalizzazione iniziali:

* Progetta [e-mail](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [notifica push](../using/push/create-push.md) o altro contenuto del canale
* Utilizza la funzionalità **[Simula contenuto](../using/content-management/preview-test.md)** per visualizzare in anteprima con i profili di test
* Controlla [token di personalizzazione](../using/personalization/personalization-syntax.md), contenuto dinamico e valori di fallback
* Verifica il rendering di [1} in diverse dimensioni dello schermo e client di posta elettronica](../using/content-management/rendering.md)

### &#x200B;2. Convalida tecnica

Convalidare gli aspetti tecnici che influiscono sulla consegna dei messaggi e sulle funzionalità:

* Esegui [controlli punteggio posta indesiderata](../using/content-management/spam-report.md) per identificare potenziali problemi di recapito messaggi
* Verifica i collegamenti per assicurarti che non siano interrotti e che siano tracciati correttamente
* Convalida configurazione [autenticazione e-mail](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC)
* Esamina il rendering HTML e verifica la presenza di problemi di compatibilità CSS
* Test della [progettazione reattiva](../using/email/content-from-scratch.md) su dispositivi mobili e desktop

### &#x200B;3. Test Percorso

Per i percorsi, convalida la logica di orchestrazione:

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

* **[Invio di messaggi multicanale](../using/building-journeys/journeys-uc.md)** - Questo caso d&#39;uso illustra come eseguire il test di un percorso che combina attività Read audience, eventi di reazione e messaggi e-mail/push. Scopri come convalidare l’intero flusso dal targeting del pubblico alla consegna dei messaggi e come verificare i passaggi di test e pubblicazione in azione.

* **[Invia un messaggio agli abbonati](../using/building-journeys/message-to-subscribers-uc.md)** - Scopri come testare i percorsi che eseguono il targeting degli elenchi di abbonamenti con indirizzi e-mail dinamici. Questo esempio mostra come convalidare le espressioni di personalizzazione e garantire che i messaggi raggiungano gli abbonati corretti.

* **[Invio di messaggi con limiti di tempo](../using/building-journeys/weekday-email-uc.md)**: scopri come verificare i percorsi con condizioni basate sul tempo per assicurarsi che i messaggi vengano inviati in giorni specifici. Scopri come convalidare le attività di attesa e la logica di pianificazione.

* **[Esplora altri casi di utilizzo del percorso](../using/building-journeys/jo-use-cases.md)**: accedi a una raccolta completa di esempi pratici che includono eventi di esperienza, messaggistica multicanale e integrazioni di sistemi esterne.

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

Convalida il percorso prima di pubblicarlo testandolo con profili specifici per garantire che eventi, condizioni e azioni funzionino come previsto.

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

::::

## Risorse aggiuntive

### Guide alla verifica e alla convalida essenziali

* [Rapporto live nel tuo Percorso](../using/building-journeys/report-journey.md) - Monitora le metriche del percorso in tempo reale per monitorare le prestazioni e identificare i problemi durante l&#39;esecuzione. Accedi a raggruppamenti dettagliati della progressione del profilo, dei trigger di evento e dei tassi di completamento delle azioni.

* [Creazione di profili di test](../using/audience/creating-test-profiles.md) - Creazione e gestione di profili di test per simulare scenari di clienti reali e convalidare la personalizzazione. Scopri come contrassegnare i profili per il test, impostare i valori degli attributi e organizzare i segmenti dei profili di test.

* [Rapporto posta indesiderata](../using/content-management/spam-report.md) - Controlla il punteggio di posta indesiderata prima dell&#39;invio per migliorare il recapito messaggi e il posizionamento della casella in entrata. Scopri in che modo i filtri anti-spam valutano i contenuti e ottengono consigli su come migliorarli.

* [Domande frequenti sui Percorsi](../using/building-journeys/journey-faq.md) - Trova le risposte alle domande più frequenti sulla creazione, il test, l&#39;esecuzione e la risoluzione dei problemi dei percorsi. Guida di riferimento rapido per la risoluzione di problemi frequenti e la comprensione del comportamento del percorso.

### Argomenti correlati

* [Gestione dei contenuti](content-management-landing-page.md) - Scopri come progettare, visualizzare in anteprima e gestire i contenuti utilizzando modelli, frammenti e il Designer e-mail. Best practice per la creazione di contenuti principali per un branding coerente.

* [Reporting e analisi](reporting-landing-page.md) - Analizza le prestazioni di campagne e percorsi con report, dashboard e metriche complete. Prendi decisioni basate sui dati per ottimizzare le esperienze dei clienti.

* [Configurazione Percorso](configure-journeys-landing-page.md) - Configura origini dati, eventi e azioni personalizzate per abilitare una sofisticata orchestrazione del percorso. Imposta le basi tecniche per la creazione del percorso.

* [Gestione campagne](../using/campaigns/get-started-with-campaigns.md) - Esplora diversi tipi di campagne e scopri come creare, pianificare e ottimizzare campagne batch e in tempo reale per il massimo impatto.
