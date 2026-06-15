---
solution: Journey Optimizer
product: journey optimizer
title: Hub di onboarding Journey Optimizer
description: Un hub dedicato per l’onboarding di Adobe Journey Optimizer che riunisce istruzioni dettagliate, casi d’uso reali e contenuti video per consentire ai nuovi utenti di crescere rapidamente e fornire la loro prima esperienza cliente.
feature: Get Started
topic: Content Management
role: User
level: Beginner
hide: true
keywords: Ottimizzatore del percorso, onboarding, onboarding hub, casi d’uso, video, tutorial, guida introduttiva, aumento graduale, primo percorso
source-git-commit: 727d99f93d3fc19848f00ab423ec320a092b357c
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 12%

---

# Hub di onboarding Journey Optimizer {#onboarding-hub}

>[!BEGINSHADEBOX]

**In questa pagina:** Approfondisci velocemente Adobe Journey Optimizer: guarda un breve orientamento, segui le istruzioni dettagliate per inviare la tua prima esperienza, sfogliare casi d&#39;uso reali e immergerti nei contenuti video curati.

>[!ENDSHADEBOX]

Sei nuovo a [!DNL Adobe Journey Optimizer]? Questo hub raccoglie le risorse che consentono di passare da zero alla prima esperienza di cliente live, con istruzioni dettagliate per obiettivi comuni, casi d’uso reali che mostrano ciò che è possibile e contenuti video curati (tutorial, procedure dettagliate e pratiche pratiche pratiche).

>[!TIP]
>
>Non sei sicuro di quale funzionalità sia adatta al tuo obiettivo? Inizia con l&#39;obiettivo [Trova la funzionalità Journey Optimizer più adatta per la tua guida all&#39;obiettivo](ajo-use-case-guide.md), quindi torna qui per istruzioni dettagliate.

## Inizia qui: guarda e scopri {#start-here}

Se hai dieci minuti, inizia con questo video di orientamento. Illustra l’interfaccia ed evidenzia le funzionalità chiave per ruolo.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

Quindi costruisci la fiducia pratica con queste risorse di apprendimento:

* [Esercitazioni Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}: video e procedure guidate dettagliate per ogni ruolo.
* [Playlist video curata da esperti](https://experienceleague.adobe.com/it/playlists?solution=Journey+Optimizer){target="_blank"}: un set sequenziale di brevi video da guardare in ordine.
* [Sandbox di formazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"}: un ambiente sicuro con dati di esempio da esercitarsi in.
* [Sfide pratiche](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"}: applica ciò che apprendi con gli esercizi guidati.

## Crea la tua prima esperienza {#build-first}

Ognuno di questi passaggi è breve e orientato ai risultati: cosa costruirete, per chi è e come raggiungerlo. Scegli l’obiettivo che corrisponde al primo progetto e segui i collegamenti alla documentazione dettagliata.

### Benvenuto per i nuovi clienti {#build-welcome}

**Genererai:** una serie di benvenuto automatizzata che accoglie ogni nuovo abbonato e svuota quelli inattivi.
**Consigliato per:** addetti al marketing · **Funzionalità:** percorso attivato da eventi

1. Conferma che [i profili unificati e i tipi di pubblico](../audience/get-started-profiles.md) ricevano l&#39;evento di iscrizione.
2. [Crea il tuo primo percorso](../building-journeys/journey-gs.md) e utilizza l&#39;evento di abbonamento come voce.
3. Aggiungi una [e-mail di benvenuto](../email/get-started-email.md), quindi un passaggio di attesa e una [notifica push](../push/get-started-push.md) di follow-up per i profili non coinvolti.
4. [Personalizza il contenuto](../personalization/personalize.md) con attributi di profilo quali nome e interessi dichiarati.

➡️ [Inizia con percorsi](../building-journeys/journey-gs.md)

### Recupera carrelli abbandonati {#build-cart}

**Verrà generato:** un flusso di ripristino in tempo reale che ricorda ai clienti gli elementi rimasti indietro.
**Consigliato per:** addetti al marketing · **Funzionalità:** percorso attivato da eventi

1. Assicurati che l&#39;evento di abbandono del carrello raggiunga Journey Optimizer (se necessario, collabora con il tuo [team di dati](../data/gs-data.md)).
2. [Crea un percorso](../building-journeys/journey-gs.md) attivato dall&#39;evento di abbandono.
3. Invia un promemoria e-mail personalizzato. Se non si fa clic entro 24 ore, passa a un follow-up [push](../push/get-started-push.md).
4. [Personalizza](../personalization/personalize.md) con gli elementi abbandonati e lo stato di fedeltà.

➡️ [Inizia con percorsi](../building-journeys/journey-gs.md)

### Inviare messaggi transazionali {#build-transactional}

**Genererai:** conferme di ordini, spedizioni o appuntamenti su richiesta attivate da un sistema esterno.
**Ideale per:** addetti al marketing e sviluppatori · **Funzionalità:** campagna attivata da API

1. Controlla il funzionamento delle [campagne attivate da API](../campaigns/api-triggered-campaigns.md) e il payload previsto.
2. Progetta il modello di messaggio e [personalizzalo](../personalization/personalize.md) con i dettagli della transazione.
3. Chiedi allo sviluppatore di chiamare l&#39;endpoint della campagna dal tuo ordine o sistema di evasione.

➡️ [Operazioni con campagne attivate da API](../campaigns/api-triggered-campaigns.md)

### Avviare una campagna con test A/B {#build-campaign}

**Genererai:** una promozione pianificata che seleziona automaticamente i contenuti con le prestazioni migliori.
**Ideale per:** addetti al marketing · **Funzionalità:** Campagna pianificata + sperimentazione sui contenuti

1. [Inizia a usare le campagne](../campaigns/get-started-with-campaigns.md) e definisci il pubblico.
2. Utilizza la [generazione di contenuti AI](../content-management/gs-generative.md) per creare bozze dell&#39;oggetto e copiare le varianti.
3. Configura un [esperimento sui contenuti](../content-management/experiment-accelerator-gs.md) per testare le varianti su un campione, quindi invia il vincitore al resto.

➡️ [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)

### Personalizzare le offerte per cliente {#build-offers}

**Genererai:** una decisione che mostra l&#39;unica offerta migliore per ogni cliente.
**Ideale per:** addetti al marketing · **Funzionalità:** Decisioning

1. [Inizia a usare offer decisioning](../offers/get-started/starting-offer-decisioning.md) e crea le offerte e le regole di idoneità.
2. Aggiungi la decisione a un [percorso](../building-journeys/journey-gs.md) o messaggio della campagna.
3. Crea livelli nelle [funzionalità AI](ai-features.md) per classificare e ottimizzare le offerte automaticamente.

➡️ [Introduzione a offer decisioning](../offers/get-started/starting-offer-decisioning.md)

## Casi d’uso per obiettivo {#use-cases}

Gli esempi riportati sopra descrivono i punti di partenza più comuni, ma Journey Optimizer supporta molti più scenari, dalle notifiche proattive di interruzione delle attività, al coinvolgimento dei clienti e alla messaggistica in tempo reale basata sulla posizione. Ogni scenario combina una o più funzionalità tra loro.

Per trovare la funzionalità esatta per l&#39;obiettivo *tuo*, utilizza l&#39;indice completo e organizzato in [Trova la funzionalità Journey Optimizer corretta per l&#39;obiettivo](ajo-use-case-guide.md). Per esempi end-to-end e funzionanti, consulta la [libreria di casi d&#39;uso Percorsi](../building-journeys/jo-use-cases.md).

## Raccolta video {#videos}

Sfoglia i contenuti video curati per argomento. Ogni scheda contiene i collegamenti ai tutorial e alle playlist pertinenti su Experience League.

>[!BEGINTABS]

>[!TAB Introduzione]

* [Introduzione a Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"}: concetti di base e presentazione del prodotto.
* [Panoramica dei tutorial su Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}: l&#39;intero catalogo di video guidati.

>[!TAB Percorsi e campagne]

* [Introduzione alla creazione di un percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — Genera il tuo primo percorso attivato da eventi.
* [Crea percorsi con Journey Agent](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"}: consente di creare percorsi da un prompt in linguaggio naturale.

>[!TAB Personalization e AI]

* [Assistente AI per la generazione di contenuti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"}: genera copie, immagini e varianti.
* [Utilizza il decisioning per personalizzare le offerte web](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — Personalizzare le offerte per cliente.

>[!TAB Reporting e ottimizzazione]

* [Monitora e analizza il tuo percorso con report live](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"}: tieni traccia delle prestazioni in tempo reale.
* [Creare esperimenti di contenuto per campagne e-mail](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} — Testare e ottimizzare il contenuto.

>[!ENDTABS]

## Elenco di controllo per l’onboarding per ruolo {#checklist}

L’onboarding si estende su diversi ruoli. Scegli il tuo ruolo per visualizzare un percorso iniziale mirato:

* **Amministratore**: configurare sandbox, autorizzazioni e canali. [Introduzione come amministratore](path/administrator.md)
* **Ingegnere dati**: modellare gli schemi e acquisire dati. [Introduzione al ruolo di ingegnere dati](path/data-engineer.md)
* **Sviluppatore**: integrazione di SDK ed eventi di attivazione. [Introduzione per sviluppatori](path/developer.md)
* **Addetto marketing**: crea percorsi, contenuti e tipi di pubblico. [Introduzione per addetti marketing](path/marketer.md)

Per una panoramica completa dell&#39;interazione di questi ruoli, vedere [Ruoli e responsabilità](quick-start.md).

## Risorse correlate {#related-resources}

* [Trova la funzionalità Journey Optimizer più adatta per il tuo obiettivo](ajo-use-case-guide.md): guida alle decisioni per il raggiungimento del primo obiettivo per ogni funzionalità.
* [Libreria casi d&#39;uso di Percorso](../building-journeys/jo-use-cases.md): esempi pratici e modelli di implementazione.
* [Terminologia chiave](terminology.md) — chiarisce i concetti alla base di ogni funzionalità.
* [Funzioni intelligenti e IA](ai-features.md): esplorazione dell&#39;Assistente IA, ottimizzazione dell&#39;ora di invio e generazione di contenuti.
* [Introduzione alla gestione dei dati](../data/gs-data.md): modalità di acquisizione, unificazione e attivazione dei dati.
