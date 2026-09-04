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
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 3%

---


# Tipi di percorso: scegli quello giusto {#journey-types-selection}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri i quattro tipi di percorso di AJO: evento unitario, lettura di tipi di pubblico, qualificazione del pubblico ed evento di business e individua quello adatto al tuo caso d&#39;uso.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] supporta quattro tipi di percorso, ognuno progettato per un tipo diverso di trigger e scenario aziendale. Comprendere la differenza ti aiuta a creare l’esperienza giusta fin dall’inizio.

## I quattro tipi di percorso {#journey-types}

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

## Quale tipo deve utilizzare? {#decision-guide}

La risposta si riduce in genere a una domanda: *cosa avvia il percorso?*

Se un **cliente fa qualcosa di specifico**, abbandona un carrello, si iscrive, fa un acquisto, utilizza un **percorso di eventi unitario**. Viene attivato immediatamente quando si verifica l’azione, un profilo alla volta.

Se desideri **raggiungere un pubblico in base a una pianificazione**, ovvero una newsletter mensile, una campagna stagionale, una serie ricorrente di ricoinvolgimento, utilizza un **percorso Read Audience**. Definisci il pubblico e la tempistica; AJO elabora tutti contemporaneamente.

Se vuoi rispondere **nel momento in cui un cliente raggiunge una milestone** — unendosi a un livello di fedeltà, raggiungendo una soglia di rischio di abbandono, completando un primo acquisto — utilizza un **percorso di qualificazione del pubblico**. Viene attivato non appena cambia l’iscrizione al pubblico in streaming, non secondo una pianificazione fissa.

Se nell&#39;azienda **cambia qualcosa che influisce su più clienti contemporaneamente, ad esempio se il livello delle azioni diminuisce, se il prezzo cambia o se inizia una vendita, utilizza un** percorso di eventi aziendali **.**

>[!TIP]
>
>**Non sei sicuro di dove iniziare?** La maggior parte dei team inizia con **Evento unitario** per le esperienze attivate dal comportamento e **Read Audience** per le campagne. Questi due casi coprono la maggior parte dei casi d’uso.

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

## Documentazione sulla disponibilità delle funzioni {#feature-compatibility}

Tutti i tipi di percorso supportano l’intero set di canali di AJO (e-mail, push, SMS, in-app, web, schede di contenuto), le attività di orchestrazione di base (attesa, condizione, azioni personalizzate), la modalità di test, l’esecuzione in prova e l’ottimizzazione dell’ora di invio. La tabella seguente mostra solo le funzionalità che differiscono tra i tipi.

>[!NOTE]
>
>Limitazioni dell’attività Salta: un percorso che inizia con un’attività Leggi pubblico o Qualificazione del pubblico non può contenere un’attività Salta e non può essere il target di un’attività Salta da un altro percorso.
>
>L&#39;attività di lettura del pubblico come voce percorso è disponibile solo in **percorsi Leggi pubblico** e **Evento business**. Impossibile aggiungerla ai percorsi di voci Evento unitario o Qualificazione pubblico.

| Funzionalità | Evento unitario | Read Audience | Qualificazione del pubblico | Evento di business |
|-----------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Voce** | | | | |
| Voce attivata da eventi | ✅ | ❌ | ❌ | ✅ (l&#39;evento business attiva il percorso; i profili entrano tramite un passaggio Read Audience interno) |
| Voce pianificata | ❌ | ✅ | ❌ | ❌ |
| Voce basata sul pubblico | ❌ | ✅ (batch) | ✅ (solo streaming) | ❌ |
| **Orchestrazione** | | | | |
| Attività Read Audience (voce percorso) | ❌ | ✅ | ❌ | ✅ (passaggio automatico dopo l&#39;evento business) |
| Attività Salta | ✅ | ❌ | ❌ | ✅ |
| **Gestione profilo** | | | | |
| Rientro profilo | ✅ configurabile | ❌ Una volta per esecuzione per impostazione predefinita ([È disponibile la funzione Force reentrance on recurrence](read-audience.md#schedule)) | ✅ Configurabile (il profilo già nel percorso non può reimmettere la stessa versione) | ✅ per evento |
| **Ottimizzazione** | | | | |
| Esperimenti di percorso (test A/B) | ✅ | ✅ | ✅ | ❌ |
| **Avanzate** | | | | |
| Lettura incrementale | ❌ | ✅ | ❌ | ❌ |
| Velocità effettiva massima | 5.000 TPS (livello organizzazione condiviso con qualificazione del pubblico) | 20.000 TPS per sandbox | 5.000 TPS (livello organizzazione condiviso con evento Unitario) | Evento di business: 5.000 TPS; passaggio Pubblico: 20.000 TPS |

**Legenda:** ✅ = Supportata | ❌ = Non supportato

## Passaggi successivi {#next-steps}

Ora che hai scelto un tipo di percorso:

* **[Crea il tuo primo percorso](journey-gs.md)**: guida dettagliata dalla voce alla pubblicazione
* **[Informazioni sulla finestra di progettazione del percorso](using-the-journey-designer.md)** — Progettare l&#39;area di lavoro del percorso
* **[Ingresso profilo nei percorsi](entry-management.md)** — Regole di ingresso, rientro e velocità effettiva per tipo
* **[Introduzione ai percorsi](journey.md)**: panoramica su nozioni di base e funzionalità
* **[Domande frequenti su Journey Orchestration](journey-faq.md)** — Risposte alle domande comuni

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-journey-types-selection-v2.md}}
