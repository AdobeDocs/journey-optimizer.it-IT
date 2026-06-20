---
solution: Journey Optimizer
product: journey optimizer
title: Inizia dall’obiettivo | ADOBE JOURNEY OPTIMIZER
description: Scopri i casi d’uso principali per i quali Adobe Journey Optimizer è progettato, con indicazioni sulle funzionalità di AJO più adatte a ogni scenario.
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: ottimizzatore di percorso, caso d’uso, guida alle decisioni, quali funzionalità, guida introduttiva, obiettivi per gli utenti, tutorial
source-git-commit: 49146a29a474a240ca1fdb10b2a6ef175f44f595
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 31%

---

# Inizia dall’obiettivo {#ajo-use-case-guide}

>[!BEGINSHADEBOX]

**In questa pagina:** Inizia da ciò che desideri eseguire, quindi passa alla funzionalità Adobe Journey Optimizer che la risolve, senza dover conoscere prima il nome della funzionalità.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] offre molte funzionalità e quella giusta dipende da ciò che si sta tentando di ottenere. Questa guida è organizzata in base agli obiettivi aziendali piuttosto che alle caratteristiche del prodotto: trova l’obiettivo che corrisponde alle tue esigenze, quindi segui il collegamento per iniziare con la funzionalità consigliata.

Usa questa pagina come router rapido: cerca l’obiettivo e passa direttamente alla funzionalità giusta. Se hai appena iniziato, inizia con [Inizia a usare Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) per trovare il punto di ingresso corretto per il tuo ruolo.

>[!NOTE]
>
>Per esempi di implementazione dettagliati, consulta la [libreria dei casi d&#39;uso Percorsi](../building-journeys/jo-use-cases.md).

Se un tutorial end-to-end non è disponibile per uno scenario specifico, il collegamento ti porta al miglior punto di partenza attuale per scoprire la funzionalità e iniziare.

L&#39;intelligenza artificiale è integrata in molte di queste funzionalità. Cercare il tag **(AI)** nelle tabelle seguenti. L&#39;[Assistente AI](ai-features.md#ai-assistant) conversazionale può anche rispondere a domande sul prodotto e acquisire informazioni operative sui percorsi in qualsiasi momento. Per l&#39;insieme completo delle funzionalità intelligenti, vedere [Funzionalità intelligenti e di intelligenza artificiale](ai-features.md).

>[!TIP]
>
>Ti avvicini ora a Journey Optimizer? Inizia con [Inizia a usare Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) per scegliere il percorso corretto per il tuo ruolo, quindi leggi [Cos&#39;è Journey Optimizer](get-started.md) per le funzionalità di base. Per rafforzare l&#39;affidabilità pratica, sfoglia le [esercitazioni Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}, segui una [playlist video](https://experienceleague.adobe.com/en/playlists?solution=Journey+Optimizer){target="_blank"} curata da esperti ed esercitati in una [sandbox di formazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} o con le [sfide pratiche](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"}.

## Configurare Journey Optimizer per il team {#setup-admin}

Per amministratori e utenti tecnici che devono configurare l’ambiente prima di creare percorsi o campagne.

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Configurare i canali e-mail, SMS o push prima dell’invio | Configurazione dei canali | [Introduzione alla configurazione del canale](../configuration/get-started-configuration.md) |
| Riscaldamento di un nuovo indirizzo IP per l’invio di e-mail | Piano di riscaldamento IP | [Introduzione al riscaldamento IP](../configuration/ip-warmup-gs.md) |
| Configurare ruoli, autorizzazioni e controllo degli accessi | Controllo degli accessi | [Introduzione al controllo degli accessi](../administration/permissions-overview.md) |
| Utilizzo in più ambienti o aree geografiche | Sandbox | [Utilizzare le sandbox](../administration/sandboxes.md) |

## Coinvolgi i clienti man mano che si verificano gli eventi {#engage-real-time}

Per scenari in cui si reagisce a un&#39;azione o a un evento del cliente mentre si verifica.

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Benvenuto automaticamente un nuovo cliente o abbonato | Percorso attivato da eventi | [Introduzione ai percorsi](../building-journeys/journey-gs.md) · [Introduzione alla creazione di un percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} |

>[!BEGINSHADEBOX]

**Prima della compilazione:** assicurati di (1) aver configurato un evento di [partecipazione al percorso](../event/about-events.md) per acquisire il trigger di iscrizione, (2) avere configurato una [superficie di canale e-mail o push](../configuration/channel-surfaces.md) per la sandbox e (3) almeno un [profilo di test](../audience/creating-test-profiles.md) disponibile per convalidare il percorso prima della pubblicazione.

>[!ENDSHADEBOX]

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Recuperare un carrello abbandonato o sfogliare una sessione | Percorso attivato da eventi | [Introduzione ai percorsi](../building-journeys/journey-gs.md) · [Esercitazione sull&#39;esplorazione abbandonata](https://experienceleague.adobe.com/it/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma){target="_blank"} |

>[!BEGINSHADEBOX]

**Prima di generare:** è necessario (1) un [evento comportamentale](../event/about-events.md) che acquisisca l&#39;azione del carrello o di esplorazione dal SDK Web o mobile, (2) una strategia di [attività di attesa](../building-journeys/wait-activity.md) decisa (in genere 1-4 ore prima del primo spunto) e (3) una superficie di canale pronta per il messaggio di follow-up. Nota: il percorso deve includere una condizione per uscire dai profili che completano l’acquisto prima della fine del periodo di attesa.

>[!ENDSHADEBOX]

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Attivare un percorso dall’invio di un modulo a un sito web | Percorso attivato da eventi | [Introduzione ai percorsi](../building-journeys/journey-gs.md) · [Esercitazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/trigger-journey-on-form-submission/introduction){target="_blank"} |
| Reagire al comportamento in-app (apertura app, visualizzazione schermo) | Percorsi + In-app | [Guida introduttiva in-app](../in-app/get-started-in-app.md) |
| Invia conferme ordine, spedizione o appuntamento | Campagna attivata da API | [Utilizzare campagne attivate da API](../campaigns/api-triggered-campaigns.md) |
| Coinvolgi di nuovo i clienti inattivi o inattivi | Percorsi + pubblico | [Introduzione a profili e tipi di pubblico](../audience/get-started-profiles.md) · [Creare tipi di pubblico con il generatore di regole](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/profiles-audiences-subscriptions/create-audiences-using-the-rule-builder){target="_blank"} |

>[!BEGINSHADEBOX]

**Prima di compilare:** è necessario (1) un pubblico [definito in Adobe Experience Platform](../audience/about-audiences.md) che identifichi i profili inattivi (ad esempio, nessun acquisto o accesso entro 60 giorni), (2) una decisione sul canale di ricoinvolgimento (e-mail, push o SMS) e (3) una regola di soppressione o un [limite di frequenza](../conflict-prioritization/channel-capping.md) per evitare di contattare i profili inviati di recente. Utilizza una voce di percorso **Read Audience**, non un evento, per questo scenario.

>[!ENDSHADEBOX]

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Eseguire il test di un percorso con dati reali prima di attivarlo | Percorso di prova | [Verifica il percorso con esecuzione a secco](../building-journeys/journey-dry-run.md) |
| Sospendere un percorso live per apportare modifiche senza interrompere i profili in-flight | Pausa percorso e ripresa | [Sospendi e riprendi un percorso](../building-journeys/journey-pause.md) |
| Creare o ottimizzare un percorso da un prompt in linguaggio naturale | Journey Agent **(AI)** | [Agenti AI](ai-features.md#ai-agents) · [Esercitazione Journey Agent](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} |

## Raggiungere il pubblico su larga scala {#reach-at-scale}

Per un’attività pianificata &quot;uno-a-molti&quot; indirizzata a un pubblico definito.

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Inviare una newsletter o una promozione a un segmento | Campagna pianificata | [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md) |

>[!BEGINSHADEBOX]

**Prima di compilare:** è necessario (1) un [segmento di pubblico pubblicato](../audience/about-audiences.md) in Adobe Experience Platform, (2) una [superficie di canale e-mail](../configuration/channel-surfaces.md) con un dominio di invio verificato e (3) eventuali [frammenti di contenuto o modelli](../content-management/fragments.md) che si intende riutilizzare già pubblicati. Le campagne pianificate sono la scelta giusta qui, non percorsi, se si tratta di un invio una tantum o ricorrente senza logica di ramificazione.

>[!ENDSHADEBOX]

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Avviare un prodotto con un test A/B | Sperimentazione sui contenuti **(AI)** | [Introduzione alla sperimentazione sui contenuti](../content-management/experiment-accelerator-gs.md) · [Creazione di esperimenti sui contenuti per le campagne e-mail](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} |
| Notifica ai clienti un’interruzione o un aggiornamento del servizio | Campagna programmata + tipi di pubblico | [Informazioni sui tipi di pubblico](../audience/about-audiences.md) |
| Progettare una campagna in più passaggi con logica di diramazione | Campagne orchestrate | [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md) |
| Esegui il targeting solo dei profili che sono cambiati dall’ultima esecuzione della campagna | Campagne orchestrate — query incrementale | [Creare query in campagne orchestrate](../orchestrated/build-query.md) <!-- TODO: verify target — no dedicated "incremental query" page found; build-query.md ("Build your first rule") is the closest existing page --> |
| Controlla quanti profili corrispondono al mio pubblico prima di avviare | Anteprima pubblico | [Informazioni sui tipi di pubblico](../audience/about-audiences.md) <!-- TODO: verify target — no "create-compositions.md#preview" page/anchor exists; about-audiences.md used as placeholder --> |
| Coordinare la messaggistica su molti canali su larga scala | Orchestrazione | [Introduzione alle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md) · [Ridimensionamento dell&#39;orchestrazione in un impegno omni-channel](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/scaling-orchestration-to-omnichannel-engagement/introduction){target="_blank"} |
| Invia ogni messaggio al momento migliore per ogni cliente | Ottimizzazione dell&#39;ora di invio **(AI)** | [Ottimizzazione del tempo di invio](../building-journeys/send-time-optimization.md) |

## Personalizzare ciò che vede ogni cliente {#personalize}

Per personalizzare offerte e contenuti per ogni utente.

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Mostra l&#39;offerta migliore per ogni cliente | Funzione Decisioni | [Introduzione a offer decisioning](../offers/get-started/starting-offer-decisioning.md) · [Esercitazione sulle offerte Web](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} |

>[!BEGINSHADEBOX]

**Prima della compilazione:** il decisioning richiede una sequenza di installazione specifica. È necessario (1) [creare elementi decisionali (offerte)](../experience-decisioning/items.md) con regole di idoneità e attributi, (2) una [strategia di selezione](../experience-decisioning/selection-strategies.md) o formula di classificazione configurata e (3) un [criterio decisionale](../experience-decisioning/create-decision.md) allegato alla superficie in cui verranno visualizzate le offerte. Ignorare questa sequenza è il motivo più comune per cui le prime impostazioni di decisioning non restituiscono risultati.

>[!ENDSHADEBOX]

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Classificare le offerte utilizzando una formula (codice postale, reddito, tempo) | Decisioning — formula di classificazione | [Formule di classificazione](../experience-decisioning/ranking/ranking-formulas.md) · [Esercitazione formula di classificazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/personalizing-offers-with-ranking-formulas-based-on-user-zip-code-and-income/introduction){target="_blank"} · [Esercitazione dati meteo](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction){target="_blank"} |
| Utilizzare dati di prodotto o CRM esterni per personalizzare le offerte | Decisioning: ricerca di set di dati di AEP | [Utilizzare la ricerca nel set di dati nel processo decisionale](../experience-decisioning/context-data.md) |
| Personalizzare il contenuto dei messaggi con i dati del profilo | Personalizzazione | [Personalizza il contenuto](../personalization/personalize.md) |
| Genera copie, immagini e varianti di messaggi | Generazione di contenuti IA **(AI)** | [Generazione di contenuti AI](../content-management/gs-generative.md) · [Esercitazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} |
| Convertire un’immagine di progettazione in un modello e-mail modificabile | Convertitore immagine-HTML **(AI)** | [Convertire un&#39;immagine in un modello e-mail](../content-management/image-to-html.md) |
| Classificazione e personalizzazione automatiche delle offerte | Modelli di classificazione IA **(AI)** | [Modelli di IA per il decisioning](../experience-decisioning/ranking/ai-models.md) |
| Distribuire contenuti contestuali sempre disponibili (nessuna campagna) | Schede contenuto | [Introduzione alle schede dei contenuti](../content-card/get-started-content-card.md) · [Creazione delle schede dei contenuti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/channels/content-cards/create-content-cards){target="_blank"} |
| Distribuisci contenuti personalizzati tramite API a qualsiasi app o superficie | Esperienza basata su codice | [Introduzione all&#39;esperienza basata su codice](../code-based/get-started-code-based.md) |
| Controlla le parti di un modello e-mail che il team può modificare | Blocco dei contenuti | [Blocca il contenuto nei modelli e-mail](../content-management/content-locking.md) |

## Coordinare e gestire la consegna {#coordinate-govern}

Per controllare come, quando e con quale frequenza i clienti vengono contattati tra i canali.

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Impedisci l’eccesso di messaggi tra i canali | Quota limite | [Imposta il limite di frequenza per canale](../conflict-prioritization/channel-capping.md) |
| Risolvere i messaggi in conflitto o in competizione | Priorità conflitti | [Identificare potenziali conflitti](../conflict-prioritization/conflicts.md) · [Esercitazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"} |
| Decidere quale percorso ha la priorità | Arbitrato del percorso | [Utilizzare le formule per classificare i percorsi](../conflict-prioritization/journey-ranking-formulas.md) |
| Rispetta le ore di silenzio e il consenso | Ore tranquille / Privacy | [Ore non interattive](../conflict-prioritization/quiet-hours.md) |
| Imporre criteri di consenso ed etichette di utilizzo dei dati tra i canali | Consenso e governance dei dati | [Introduzione alla privacy](../privacy/get-started-privacy.md) |
| Ricevi avvisi quando un percorso presenta tassi elevati di errore o di eliminazione | Avvisi percorso | [Imposta avvisi di percorso](../reports/alerts.md) |

## Scegli un canale per la consegna {#choose-channel}

| Voglio inviare... | Canale | Inizia qui |
| --- | --- | --- |
| Newsletter e promozioni via e-mail o messaggi transazionali | E-mail | [Introduzione all&#39;e-mail](../email/get-started-email.md) |
| Notifiche push per dispositivi mobili (iOS e Android) | Push | [Introduzione alle notifiche push](../push/get-started-push.md) |
| SMS, MMS o SMS RCS | SMS/MMS/RCS | [Guida introduttiva a SMS/MMS/RCS](../mobile/get-started-mobile.md) · [Mobile Learning Hub](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/mobile-learning-hub/overview){target="_blank"} |
| Messaggi WhatsApp tramite API Meta Cloud | WhatsApp | [Introduzione a WhatsApp](../whatsapp/get-started-whatsapp.md) |
| Sovrapposizioni e banner nel browser o in-app | In-app | [Guida introduttiva in-app](../in-app/get-started-in-app.md) |
| Contenuto di pagine web personalizzate | Web | [Introduzione al canale Web](../web/get-started-web.md) |
| Qualsiasi superficie tramite API (chiosco, dispositivo connesso, app headless) | Esperienza basata su codice | [Introduzione all&#39;esperienza basata su codice](../code-based/get-started-code-based.md) |
| Messaggi fisici attivati da un percorso | Direct mail | [Introduzione alla direct mailing](../direct-mail/get-started-direct-mail.md) |

## Misurazione e ottimizzazione {#measure-optimize}

Per il tracciamento delle prestazioni, la diagnosi dei problemi e il miglioramento dei risultati nel tempo.

| Voglio... | Funzionalità consigliata | Inizia qui |
| --- | --- | --- |
| Vedi le metriche delle prestazioni per un percorso o una campagna live | Rapporti live | [Rapporti live](../reports/live-report.md) · [Monitora e analizza il tuo percorso con rapporti live](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} |
| Report sulle prestazioni complete della campagna o del percorso al termine | Rapporti globali | [Introduzione al reporting](../reports/gs-reports.md) |
| Analizzare un esperimento e ottenere consigli per il passaggio successivo | Agente di sperimentazione **(AI)** | [Agente di sperimentazione](ai-features.md#experimentation-agent) · [Esercitazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/experimentation/experimentation-agent-overview){target="_blank"} |
| Monitora lo stato e la latenza delle azioni personalizzate nei miei percorsi | Monitoraggio delle azioni personalizzate | [Usa azioni personalizzate](../building-journeys/using-custom-actions.md) <!-- TODO: verify target — no dedicated "custom-action-monitoring.md" page found; using-custom-actions.md is the closest existing page --> |
| Ricevi avvisi quando i tassi di errore o di eliminazione del percorso superano le soglie | Avvisi percorso | [Imposta avvisi di percorso](../reports/alerts.md) |

## Flussi iniziali {#starter-flows}

Ogni flusso iniziale di seguito è un breve set di passaggi orientati ai risultati: cosa costruirai, per chi è e come raggiungerlo. Scegli l’obiettivo che corrisponde al primo progetto e segui i collegamenti alla documentazione dettagliata.

### Benvenuto per i nuovi clienti {#flow-welcome}

**Genererai:** una serie di benvenuto automatizzata che accoglie ogni nuovo abbonato e svuota quelli inattivi.
**Consigliato per:** addetti al marketing · **Funzionalità:** percorso attivato da eventi

1. Conferma che [i profili unificati e i tipi di pubblico](../audience/get-started-profiles.md) ricevano l&#39;evento di iscrizione.
1. [Crea il tuo primo percorso](../building-journeys/journey-gs.md) e utilizza l&#39;evento di abbonamento come voce.
1. Aggiungi una [e-mail di benvenuto](../email/get-started-email.md), quindi un passaggio di attesa e una [notifica push](../push/get-started-push.md) di follow-up per i profili non coinvolti.
1. [Personalizza il contenuto](../personalization/personalize.md) con attributi di profilo quali nome e interessi dichiarati.

➡️ [Inizia con percorsi](../building-journeys/journey-gs.md)

### Recupera carrelli abbandonati {#flow-cart}

**Verrà creato:** un flusso di ripristino automatico che ricorda ai clienti gli elementi rimasti indietro.
**Consigliato per:** addetti al marketing · **Funzionalità:** percorso attivato da eventi

1. Assicurati che l&#39;evento di abbandono del carrello raggiunga Journey Optimizer (se necessario, collabora con il tuo [team di dati](../data/gs-data.md)).
1. [Crea un percorso](../building-journeys/journey-gs.md) attivato dall&#39;evento di abbandono.
1. Invia un promemoria e-mail personalizzato. Se non si fa clic entro 24 ore, passa a un follow-up [push](../push/get-started-push.md).
1. [Personalizza](../personalization/personalize.md) con gli elementi abbandonati e lo stato di fedeltà.

➡️ [Inizia con percorsi](../building-journeys/journey-gs.md)

### Inviare messaggi transazionali {#flow-transactional}

**Genererai:** conferme di ordini, spedizioni o appuntamenti su richiesta attivate da un sistema esterno.
**Ideale per:** addetti al marketing e sviluppatori · **Funzionalità:** Campagna attivata da un sistema esterno

1. Controlla il funzionamento di [campagne attivate da un sistema esterno](../campaigns/api-triggered-campaigns.md) e il payload previsto.
1. Progetta il modello di messaggio e [personalizzalo](../personalization/personalize.md) con i dettagli della transazione.
1. Chiedi allo sviluppatore di chiamare l&#39;endpoint della campagna dal tuo ordine o sistema di evasione.

➡️ [Utilizzare le campagne attivate da un sistema esterno](../campaigns/api-triggered-campaigns.md)

### Avviare una campagna con test dei contenuti {#flow-campaign}

**Genererai:** una promozione pianificata che seleziona automaticamente i contenuti con le prestazioni migliori.
**Ideale per:** addetti al marketing · **Funzionalità:** Campagna pianificata + sperimentazione sui contenuti

1. [Inizia a usare le campagne](../campaigns/get-started-with-campaigns.md) e definisci il pubblico.
1. Utilizza la [generazione di contenuti](../content-management/gs-generative.md) per creare bozze dell&#39;oggetto e copiare le varianti.
1. Configura un [esperimento sui contenuti](../content-management/experiment-accelerator-gs.md) per testare le varianti su un campione, quindi invia il vincitore al resto.

➡️ [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)

### Personalizzare le offerte per cliente {#flow-offers}

**Genererai:** una decisione che mostra l&#39;unica offerta migliore per ogni cliente.
**Ideale per:** addetti al marketing · **Funzionalità:** Decisioning

1. [Inizia a usare offer decisioning](../offers/get-started/starting-offer-decisioning.md) e crea le offerte e le regole di idoneità.
1. Aggiungi la decisione a un [percorso](../building-journeys/journey-gs.md) o messaggio della campagna.
1. Crea livelli di [funzioni intelligenti](ai-features.md) per classificare e ottimizzare automaticamente le offerte.

➡️ [Introduzione a offer decisioning](../offers/get-started/starting-offer-decisioning.md)

## Scenari di esempio {#example-scenarios}

Questi esempi illustrano il modo in cui le funzionalità di Journey Optimizer collaborano tra ruoli, settori e canali diversi.

### Recupero spedizione ritardata {#scenario-delayed-shipment}

**Ruolo:** Marketer | **Funzionalità di base:** [Profilo unificato + esclusione pubblico](../audience/get-started-profiles.md)

Un negozio di abbigliamento invia in genere dei sondaggi post-vendita a tutta la clientela che ha acquistato prodotti nell’ultima settimana. A causa delle condizioni climatiche avverse, alcune spedizioni hanno avuto ritardi. Potendo sapere chi non ha ancora ricevuto le proprie spedizioni, il negozio di abbigliamento può escludere queste persone dall’invio del questionario pianificato sulla soddisfazione, inviando invece un’e-mail personalizzata di scuse per il ritardo e offrendo un codice sconto con prodotti consigliati in base agli acquisti precedenti.

[Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)

### Coinvolgimento in-store in tempo reale {#scenario-instore}

**Ruolo:** Marketer | **Funzionalità di base:** [Attivazione geofence + push](../push/get-started-push.md)

Lo stesso retailer può coinvolgere un cliente fedele che entra nel parcheggio del negozio inviando una notifica push su un maglione che è di nuovo in magazzino nella dimensione del cliente.

[Introduzione alle notifiche push](../push/get-started-push.md)

### Recupero abbandono carrello {#scenario-cart}

**Ruolo:** Marketer | **Funzionalità di base:** [percorso con più passaggi attivato da evento](../building-journeys/journey-gs.md)

Quando un cliente aggiunge articoli a un carrello online ma lascia senza completare l’acquisto, Journey Optimizer rileva l’evento e avvia automaticamente un percorso di ripristino. Il cliente riceve un’e-mail personalizzata per ricordare gli articoli lasciati indietro. Se il cliente non riceve il click-through entro 24 ore, viene inviata una notifica push di follow-up, personalizzata in base alla cronologia di navigazione e allo stato di fidelizzazione.

[Creare il primo percorso](../building-journeys/journey-gs.md)

### Serie di messaggi di benvenuto del servizio di streaming {#scenario-welcome}

**Ruolo:** marketer | **Funzionalità di base:** [percorso di benvenuto attivato da eventi](../building-journeys/journey-gs.md)

Quando un cliente si abbona a un servizio di streaming, Journey Optimizer rileva l’evento di abbonamento e avvia immediatamente un percorso di benvenuto in più passaggi. Il cliente riceve un’e-mail di benvenuto che lo invita ad aprire l’app per la prima volta. Se non viene rilevata alcuna attività di accesso entro 48 ore, viene inviata una notifica push di follow-up con contenuti personalizzati consigliati in base agli interessi dichiarati durante l’iscrizione, convertendo un abbonato passivo in un utente attivo e coinvolto dal primo giorno.

[Creare il primo percorso](../building-journeys/journey-gs.md)

### Promemoria della prenotazione con indicazioni {#scenario-reservation}

**Ruolo:** marketer | **Funzionalità di base:** [Pianificato + Messaggistica in base alla posizione](../campaigns/get-started-with-campaigns.md)

Un brand di ospitalità invia a ogni ospite un promemoria puntuale un’ora prima della prenotazione. La notifica include il nome dell’ospite, l’ora della prenotazione e le indicazioni della sede basate sulla posizione, assemblate automaticamente dal profilo cliente e dai dati di prenotazione, senza alcuno sforzo manuale da parte del team di marketing.

[Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)

### Notifica proattiva di interruzione del servizio {#scenario-outage}

**Ruolo:** operazioni | **Funzionalità di base:** [selezione automatizzata del pubblico su larga scala](../audience/about-audiences.md)

Quando si verifica un’interruzione del servizio, Journey Optimizer identifica automaticamente la clientela interessata in base ai dati dell’account e ai pattern di utilizzo. La clientela riceve una notifica proattiva che riconosce il problema e delinea i passaggi successivi, trasformando un’esperienza potenzialmente negativa in un momento di trasparenza e fiducia, consegnato su larga scala.

[Creare il primo percorso](../building-journeys/journey-gs.md)

### Campagna promozionale intelligente {#scenario-ai-campaign}

**Ruolo:** Addetto marketing | **Funzionalità di base:** [Generazione di contenuti + sperimentazione](ai-features.md)

Un brand di vendita al dettaglio che pianifica il lancio di un prodotto utilizza l’Assistente IA di Journey Optimizer per generare, in pochi minuti, più varianti dell’oggetto e del corpo del messaggio, guidato da un prompt in linguaggio naturale e dalle linee guida del brand caricate. La sperimentazione di contenuti incorporata identifica automaticamente la variante con le prestazioni migliori tra un campione di pubblico iniziale. Il messaggio vincente viene quindi distribuito ai destinatari rimanenti, ottimizzando il coinvolgimento senza ulteriore sforzo di scrittura.

[Esplora le funzionalità intelligenti](ai-features.md) | [Scopri di più sulla sperimentazione dei contenuti](../content-management/experiment-accelerator-gs.md)

### Avvisi di manutenzione tramite app mobile {#scenario-maintenance}

**Ruolo:** operazioni | **Funzionalità di base:** [orchestrazione del percorso non di marketing](../building-journeys/journey-gs.md)

I non marketer, come i team operativi e l’assistenza clienti, possono utilizzare [!DNL Adobe Journey Optimizer] per gestire le notifiche operative o monitorare i processi di onboarding. Ad esempio, un parco divertimenti in cui i visitatori scaricano un’app mobile come parte della loro esperienza: il personale di manutenzione può utilizzare Journey Optimizer per informare i visitatori dei percorsi attualmente chiusi a causa di manutenzione.

[Creare il primo percorso](../building-journeys/journey-gs.md)

## Raccolta video {#videos}

Sfoglia i contenuti video curati per argomento. Ogni scheda contiene i collegamenti ai tutorial e alle playlist pertinenti su Experience League.

>[!BEGINTABS]

>[!TAB Introduzione]

* [Introduzione a Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"}: concetti di base e presentazione del prodotto.
* [Panoramica dei tutorial su Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}: l&#39;intero catalogo di video guidati.

>[!TAB Percorsi e campagne]

* [Introduzione alla creazione di un percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — Genera il tuo primo percorso attivato da eventi.
* [Crea percorsi con Journey Agent](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"}: consente di creare percorsi da un prompt in linguaggio naturale.

>[!TAB Personalization e intelligence]

* [Assistente AI per la generazione di contenuti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"}: genera copie, immagini e varianti.
* [Utilizza il decisioning per personalizzare le offerte web](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — Personalizzare le offerte per cliente.

>[!TAB Reporting e ottimizzazione]

* [Monitora e analizza il tuo percorso con rapporti live](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"}: tieni traccia delle prestazioni durante l&#39;esecuzione dei percorsi.
* [Creare esperimenti di contenuto per campagne e-mail](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} — Testare e ottimizzare il contenuto.

>[!ENDTABS]

## Scelta tra percorsi, campagne e campagne orchestrate {#choosing}

| Scenario | Utilizzo di |
| -------- | --- |
| Basato sul comportamento e in più fasi, ciascun cliente si muove al proprio ritmo | Percorso |
| Semplice messaggio pianificato o attivato da API per un pubblico | Campaign |
| Flusso di lavoro batch complesso con segmentazione di più entità | Campagna orchestrata |

## Non sei sicuro? {#not-sure}

Se l&#39;obiettivo è associato a un termine che non conosci o se non sai a quale funzionalità punta la tabella, inizia con la pagina della terminologia chiave [Journey Optimizer](terminology.md) per chiarire i concetti alla base di ciascuna funzionalità.

Puoi anche creare un&#39;affidabilità pratica con gli esercizi end-to-end nelle [esercitazioni di Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}.
