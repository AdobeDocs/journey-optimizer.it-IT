---
solution: Journey Optimizer
product: journey optimizer
title: 'Tipi di percorso: scegli quello giusto'
description: Confronta i tipi di percorso e scegli quello giusto per il tuo caso d’uso con le guide alla decisione e la matrice di compatibilità delle funzioni
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: Tipi di percorso, unitari, pubblico di lettura, qualificazione del pubblico, evento di business, confronto, guida alle decisioni, scelta, selezione, in tempo reale, pianificato, batch, attivato da evento
version: Journey Orchestration
exl-id: 0c894dc1-76b6-4b33-baf8-eaf6686f7d38
TQID: https://experienceleague.adobe.com/rEANha6Lppyd5vog-0kZ3aL9VvZHc9kziW-d-jiWqeA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: 1264
ht-degree: 5%

---

# Tipi di percorso: scegli quello giusto {#journey-types-selection}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come confrontare i quattro tipi di percorso: evento unitario, lettura di tipi di pubblico, qualificazione del pubblico ed evento di business e utilizza la guida alle decisioni e la matrice di compatibilità delle funzionalità per scegliere quella giusta per il tuo caso d&#39;uso.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] supporta quattro tipi di percorso, ognuno progettato per diversi meccanismi di ingresso e scenari aziendali. Questa guida ti aiuta a comprendere le differenze e a scegliere il tipo giusto per il tuo caso d’uso.

>[!NOTE]
>
>Quale tipo scegliere? Inizia con **percorsi di eventi unitari** per le esperienze basate su eventi o **percorsi di pubblico di lettura** per le campagne pianificate; questi coprono i casi d&#39;uso più comuni.

## Panoramica sui tipi di percorso {#journey-types}

>[!BEGINTABS]

>[!TAB percorsi di eventi unitari]

**Quando utilizzare:** esperienze in tempo reale attivate da eventi

**I percorsi di eventi unitari** vengono attivati singolarmente quando si verifica un&#39;azione specifica (acquisto, accesso all&#39;app, invio di moduli). I profili vengono inseriti uno alla volta in tempo reale, rendendolo ideale per risposte immediate e basate sul comportamento.

**Ideale per:** ripristino abbandono carrello, onboarding nuovi membri, e-mail di benvenuto quando qualcuno si abbona e personalizzazione post-accesso.

➡️ [Informazioni sugli eventi](../event/about-events.md) | [Caso di utilizzo: messaggio agli abbonati](message-to-subscribers-uc.md) | [Crea il primo percorso](journey-gs.md)

>[!TAB Leggi percorsi di pubblico]

**Quando utilizzare:** campagne pianificate per i segmenti di pubblico

**Leggi percorsi di pubblico** inizia con un pubblico [!DNL Adobe Experience Platform] e invia messaggi in batch a tutti i profili contemporaneamente. Questo percorso è ideale per comunicazioni pianificate su larga scala. Utilizza l&#39;opzione **lettura incrementale** nei percorsi ricorrenti per elaborare solo i profili che sono entrati a far parte del pubblico dall&#39;ultima esecuzione, anziché rielaborare ogni volta il pubblico completo.

**Ideale per:** newsletter mensili, campagne promozionali per segmenti target, annunci di prodotti, serie ricorrenti di ricoinvolgimento e campagne di marketing stagionali.

➡️ [Scopri il pubblico in lettura](read-audience.md) | [Introduzione ai tipi di pubblico](../audience/about-audiences.md) | [Crea il primo percorso](journey-gs.md)

>[!TAB percorsi di qualificazione del pubblico]

**Quando utilizzare:** le risposte in tempo reale alle modifiche di iscrizione al pubblico

**I percorsi di qualificazione del pubblico** si attivano quando i profili si qualificano per un pubblico specifico (o ne escono). I profili vengono inseriti singolarmente in base ai criteri, consentendo un coinvolgimento immediato quando il comportamento del cliente cambia. Utilizza i tipi di pubblico **valutati in streaming**: sono l&#39;unico tipo di pubblico supportato per questa attività.

>[!CAUTION]
>
>A partire dal **agosto 2026**, i percorsi che utilizzano un pubblico batch in un nodo di qualificazione del pubblico non possono essere pubblicati. [Scopri come eseguire la migrazione dei percorsi](aq-batch-audiences-migration.md)

**Ideale per:** notifiche di aggiornamento a livello di VIP, messaggi di festeggiamento per il primo acquisto, avvisi sui rischi di abbandono e transizioni tra le fasi del ciclo di vita della fedeltà.

➡️ [Scopri le qualificazioni per il pubblico](audience-qualification-events.md) | [Creazione di tipi di pubblico](../audience/creating-a-segment-definition.md) | [Crea il primo percorso](journey-gs.md)

>[!TAB percorsi di eventi di business]

**Quando utilizzare:** condizioni aziendali che interessano più clienti

**I percorsi di eventi aziendali** sono attivati da un evento a livello aziendale (aggiornamenti delle scorte, modifiche dei prezzi) che interessa più profili contemporaneamente. Internamente, il trigger dell’evento business è sempre seguito da un passaggio Read Audience che acquisisce i profili rilevanti, pertanto l’immissione del profilo segue le regole di throughput Read Audience, non la velocità effettiva unitaria degli eventi.

**Ideale per:** avvisi di inventario ridotti per i clienti interessati, annunci di vendita flash, notifiche di calo dei prezzi e avvisi di back-in-stock dei prodotti.

➡️ [Informazioni sugli eventi di business](../event/about-creating-business.md) | [Gestione voci](entry-management.md) | [Crea il primo percorso](journey-gs.md)

>[!ENDTABS]

## Guida alla decisione: scelta del tipo di percorso {#decision-guide}

Utilizza la tabella seguente per far corrispondere l’obiettivo al tipo di percorso corretto. Per la maggior parte dei nuovi utenti, **Evento unitario** o **Pubblico di lettura** percorsi coprono la maggior parte dei casi d&#39;uso.

| Il tuo obiettivo | Tipo di percorso consigliato | Il motivo |
|-----------|--------------------------|-----|
| Recuperare un carrello abbandonato | Evento unitario | Risposta immediata al comportamento individuale |
| Invia newsletter mensile agli abbonati | Read Audience | Comunicazione batch programmata |
| Avvisa i clienti quando raggiungono lo stato VIP | Qualificazione del pubblico | Risposta in tempo reale all’ingresso di pubblico in streaming |
| Avvisa i clienti in caso di scorte ridotte sugli articoli osservati | Evento di business | La condizione di business interessa più clienti |
| Benvenuto per i nuovi utenti dell&#39;app | Evento unitario o qualificazione del pubblico | Evento di iscrizione (evento unitario) o ingresso in un pubblico in streaming per nuovi utenti (qualificazione del pubblico) |
| Rivolgersi nuovamente ai clienti inattivi (ricorrenti, pianificati) | Read Audience | Esecuzione batch ricorrente per pubblico inattivo |
| Promozione stagionale nel segmento di destinazione | Read Audience | Campagna pianificata al pubblico |
| Annuncio vendita flash | Evento di business | Le decisioni aziendali influiscono su più clienti |
| Reagire non appena un cliente raggiunge il livello di fedeltà Gold | Qualificazione del pubblico | Pubblico in streaming, ingresso individuale in tempo reale |

## Confronto dettagliato dei tipi di percorso {#journey-types-comparison}

| Formato | Percorsi di eventi unitari | Leggi percorsi di pubblico | Percorsi di qualificazione del pubblico | Percorsi di eventi aziendali |
|--------|------------------------|------------------------|--------------------------------|------------------------|
| **Meccanismo di ingresso** | Attivazione evento individuale | Batch programmato | Modifica dell’iscrizione al pubblico in streaming in tempo reale | Evento a livello di azienda + Passaggio Read Audience |
| **Tempistica di ingresso** | In tempo reale, quando si verificano gli eventi | Pianificato (una tantum o ricorrente) | In tempo reale, quando si verifica la qualifica (pubblico in streaming); in ritardo per i tipi di pubblico valutati in batch | Trigger in tempo reale; l’acquisizione del profilo segue la velocità effettiva Read Audience |
| **Voce profilo** | Uno alla volta | Tutto in una volta (batch) | Uno alla volta | Più profili tramite il passaggio Read audience interno |
| **Origine trigger** | Azione del cliente (acquisto, clic, accesso) | Pianificazione basata su tempo | Entrata o uscita iscrizione pubblico | Condizioni dell’attività (azioni, prezzi) |
| **Ottimo per** | Messaggi transazionali, risposte comportamentali | Campagne di marketing, newsletter, programmi ricorrenti | Programmi fedeltà, transizioni delle fasi del ciclo di vita | Avvisi di inventario, promozioni, condizioni aziendali |
| **Usa quando** | Necessità di una risposta immediata alle singole azioni | Raggiungere grandi segmenti di pubblico secondo la pianificazione | Risposta in tempo reale alle modifiche dello stato del cliente | Gli eventi di business interessano più clienti contemporaneamente |
| **Esempi** | Ripristino in seguito all’abbandono del carrello, onboarding di nuovi membri | Newsletter mensile, campagna stagionale | Aggiornamento del VIP, avviso relativo ai rischi di abbandono | Allarme scorte basse, vendita flash, calo prezzi |
| **Rientro** | Configurabile | Una volta per esecuzione per impostazione predefinita; [Forza il rientro in caso di ricorrenza](read-audience.md#schedule) disponibile nelle esecuzioni pianificate | Configurabile per evento di qualifica; un profilo già nel percorso non può reinserire la stessa versione | Più profili possono essere interessati dallo stesso evento |
| **Velocità effettiva massima** | 5.000 TPS (livello organizzazione condiviso con qualificazione del pubblico) | 20.000 TPS per sandbox | 5.000 TPS (livello organizzazione condiviso con evento Unitario) | Evento di business: 5.000 TPS; passaggio Pubblico: 20.000 TPS |
| **Requisiti dei dati** | Schema evento con dati trigger | Pubblico [!DNL Adobe Experience Platform] | È necessario specificare un pubblico in streaming. I tipi di pubblico in batch sono diventati obsoleti da agosto 2026 — [esegui ora la migrazione](aq-batch-audiences-migration.md) | Schema evento di business |

## Compatibilità delle funzioni per tipo di percorso {#feature-compatibility}

Non tutte le funzionalità sono disponibili per tutti i tipi di percorso. Utilizza questa matrice per capire quali funzionalità funzionano con quali tipi di percorso:

| Funzionalità | Evento unitario | Read Audience | Qualificazione del pubblico | Evento di business |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Meccanismi di ingresso** | | | | |
| Voce attivata da eventi | ✅ | ❌ | ❌ | ✅ (l&#39;evento business attiva il percorso; i profili entrano tramite un passaggio Read Audience interno) |
| Voce pianificata | ❌ | ✅ | ❌ | ❌ |
| Voce basata sul pubblico | ❌ | ✅ (batch) | ✅ (streaming) | ❌ |
| **Funzioni di orchestrazione** | | | | |
| Attività di attesa | ✅ | ✅ | ✅ | ✅ |
| Attività condizione | ✅ | ✅ | ✅ | ✅ |
| Azioni personalizzate | ✅ | ✅ | ✅ | ✅ |
| Attività Read Audience (voce percorso) | ❌ | ✅ | ❌ | ✅ (passaggio automatico dopo l&#39;evento business) |
| Attività di qualificazione del pubblico (all’interno del percorso) | ✅ | ✅ | ✅ | ✅ |
| Attività Salta | ✅ | ❌ | ❌ | ✅ |
| **Gestione profilo** | | | | |
| Rientro profilo | ✅ configurabile | ❌ Una volta per esecuzione per impostazione predefinita ([Forza il rientro alla ricorrenza](read-audience.md#schedule) alle esecuzioni pianificate) | ✅ Configurabile (il profilo già nel percorso non può reimmettere la stessa versione) | ✅ per evento |
| Configurazione dello spazio dei nomi | ✅ richiesto | ✅ facoltativo | ✅ richiesto | ✅ richiesto |
| Limite del profilo | ✅ | ✅ | ✅ | ✅ |
| **Test e ottimizzazione** | | | | |
| Modalità di test | ✅ | ✅ | ✅ | ✅ |
| Esecuzione a secco | ✅ | ✅ | ✅ | ✅ |
| Esperimenti di percorso (test A/B) | ✅ | ✅ | ✅ | ❌ |
| Ottimizzazione del tempo di invio | ✅ | ✅ | ✅ | ✅ |
| **Canali** | | | | |
| E-mail | ✅ | ✅ | ✅ | ✅ |
| Notifiche push | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| Messaggi in-app | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Schede contenuto | ✅ | ✅ | ✅ | ✅ |
| **Funzionalità avanzate** | | | | |
| Lettura incrementale | ❌ | ✅ | ❌ | ❌ |
| Gestione del fuso orario | ✅ | ✅ | ✅ | ✅ |
| Eventi di reazione | ✅ | ✅ | ✅ | ✅ |
| Origini dati esterne | ✅ | ✅ | ✅ | ✅ |
| Limitazione/Limitazione | ✅ | ✅ | ✅ | ✅ |

**Legenda:** ✅ = Supportata | ❌ = Non supportato

>[!NOTE]
>
>Limitazioni dell’attività Salta: un percorso che inizia con un’attività Leggi pubblico o Qualificazione del pubblico non può contenere un’attività Salta e non può essere il target di un’attività Salta da un altro percorso.
>
>L&#39;attività di lettura del pubblico come voce percorso è disponibile solo in **percorsi Leggi pubblico** e **Evento business**. Impossibile aggiungerla ai percorsi di voci Evento unitario o Qualificazione pubblico.

## Passaggi successivi {#next-steps}

Ora che hai scelto un tipo di percorso:

* **[Percorsi rispetto a campagne](../start/journeys-vs-campaigns.md)**: non sei sicuro se Percorsi o campagne siano lo strumento giusto? Torna prima alla decisione di livello superiore
* **[Crea il tuo primo percorso](journey-gs.md)**: guida dettagliata dalla voce alla pubblicazione
* **[Informazioni sulla finestra di progettazione del percorso](using-the-journey-designer.md)** — Progettare l&#39;area di lavoro del percorso
* **[Ingresso profilo nei percorsi](entry-management.md)** — Regole di ingresso, rientro e velocità effettiva per tipo
* **[Introduzione ai percorsi](journey.md)**: panoramica su nozioni di base e funzionalità
* **[Domande frequenti su Journey Orchestration](journey-faq.md)** — Risposte alle domande comuni

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-journey-types-selection.md}}
