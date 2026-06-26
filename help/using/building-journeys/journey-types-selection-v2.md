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
source-git-commit: d4ed86ea2833c1753d89186a460ba24ae57773fd
workflow-type: tm+mt
source-wordcount: '2109'
ht-degree: 0%

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

| Il tuo obiettivo | Tipo di percorso consigliato | Perché |
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

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina è disponibile un confronto completo dei quattro tipi di percorso di AJO: Evento unitario, Read Audience, Qualificazione del pubblico ed Evento di business, oltre a una guida alle decisioni e a una matrice di compatibilità delle funzionalità per consentire agli utenti di scegliere il tipo corretto per il proprio caso d&#39;uso.

**Intenti:**

* Scegliere il tipo di percorso corretto per un determinato caso d’uso aziendale utilizzando la tabella delle decisioni
* Confrontare i tipi di percorso affiancati utilizzando la matrice di compatibilità dettagliata delle funzioni
* Scopri quando utilizzare percorsi Read Audience per le comunicazioni batch pianificate
* Scopri quando utilizzare i percorsi di eventi unitari per esperienze in tempo reale attivate da eventi
* Scopri quando utilizzare i percorsi di qualificazione del pubblico per rispondere in tempo reale alla modifica dello stato
* Comprendere quando utilizzare i percorsi di eventi business per le comunicazioni basate su condizioni di business
* Comprendere i limiti di velocità effettiva per tipo di percorso durante la pianificazione delle distribuzioni di volumi elevati

**Glossario:**

* **percorso di eventi unitario**: percorso attivato da una specifica azione del cliente (ad esempio, acquisto, accesso) in cui i profili ne immettono uno alla volta in tempo reale. *(specifico per prodotto)*
* **percorso di tipi di pubblico lettura**: percorso che inizia con un pubblico di Adobe Experience Platform e invia messaggi in batch a tutti i profili contemporaneamente in base a una pianificazione. *(specifico per prodotto)*
* **percorso di qualificazione del pubblico**: percorso che viene attivato quando i profili si qualificano per un segmento di pubblico specifico o ne escono. Richiede un pubblico valutato in streaming per il comportamento di immissione in tempo reale. *(specifico per prodotto)*
* **percorso di eventi aziendali**: percorso attivato da un evento a livello aziendale (ad esempio, aggiornamento delle scorte, modifica del prezzo) che interessa più profili contemporaneamente; è sempre associato a un passaggio Read Audience interno per l&#39;acquisizione del profilo. *(specifico per prodotto)*
* **Lettura incrementale**: funzionalità Read Audience che elabora solo i profili che sono entrati a far parte del pubblico dall&#39;ultima esecuzione, non ogni volta il pubblico completo. Disponibile solo per percorsi Read Audience. *(specifico per prodotto)*
* **Pubblico in streaming**: un pubblico Adobe Experience Platform valutato continuamente in tempo reale, anziché un pubblico batch valutato su una pianificazione (ad esempio, ogni giorno). Necessario affinché i percorsi di qualificazione del pubblico possano ottenere un comportamento di immissione in tempo reale. *(specifico per prodotto)*

**Guardrail:**

* La lettura incrementale è disponibile solo per percorsi Read Audience e non per percorsi evento Unitario, Qualificazione del pubblico o Evento di business
* Gli esperimenti di percorso (test A/B) non sono supportati per i percorsi di eventi di business
* Per impostazione predefinita, il rientro del profilo nei percorsi Read Audience è limitato a una volta per esecuzione; usa Forza rientro in caso di ricorrenza nelle esecuzioni pianificate per consentire ai profili di rientrare nell’esecuzione successiva
* L’attività Read Audience è disponibile solo come voce percorso nei percorsi evento Read Audience e Business, non nei percorsi di voce Unitario o Qualificazione del pubblico
* I percorsi di qualificazione e lettura del pubblico non possono contenere un’attività Salta e non possono essere il target di un’attività Salta da un altro percorso
* I percorsi di qualificazione del pubblico richiedono un pubblico valutato in streaming. A partire da agosto 2026, i tipi di pubblico valutati in batch non possono essere utilizzati in un nodo di qualificazione del pubblico. Consulta la [guida alla migrazione](aq-batch-audiences-migration.md)
* I percorsi unitari di qualificazione di eventi e pubblico condividono un limite di velocità effettiva di 5.000 TPS a livello di organizzazione; Read Audience percorsi supportano fino a 20.000 TPS per sandbox
* Un profilo già presente in un percorso non può rientrare nella stessa versione di quel percorso, indipendentemente dalla configurazione di rientro

**Terminologia:**

* Nome canonico: percorso unitario di eventi — varianti: percorso attivato da eventi, percorso unitario
* Nome canonico: percorso Read Audience — varianti: percorso batch
* Nome canonico: Audience Qualification percorso — varianti: percorso di eventi di qualificazione del pubblico
* Nome canonico: percorso di eventi aziendali — varianti: percorso attivato da eventi aziendali
* Non confondere: &quot;Leggi percorso di pubblico&quot; ≠ &quot;percorso di qualificazione del pubblico&quot;: Read Audience elabora tutti i membri del pubblico in batch secondo la pianificazione; Audience Qualification risponde ai cambiamenti di iscrizione individuale in tempo reale (pubblico in streaming solo per l’ingresso immediato)
* Non confondere: &quot;percorso di eventi unitario&quot; ≠ &quot;percorso di eventi di business&quot;: l’evento unitario viene attivato da un’azione del cliente che interessa un profilo; l’evento di business viene attivato da una condizione di business e acquisisce più profili tramite un passaggio Read Audience interno

**Domande frequenti:**

* **Q: quale tipo di percorso utilizzare per una newsletter mensile?** : utilizza un percorso Read Audience; è progettato per la comunicazione batch pianificata per tutti i profili in un segmento di pubblico simultaneamente.
* **Q: quale tipo di percorso utilizzare per ripristinare un carrello abbandonato?** — Utilizza un percorso di eventi Unitario; si attiva immediatamente quando si verifica l’evento di abbandono e risponde al comportamento dell’individuo in tempo reale.
* **Q: posso eseguire esperimenti di percorso A/B in un percorso di eventi aziendali?** — No; gli esperimenti di percorso non sono supportati per i percorsi di eventi Business.
* **D: Qual è la differenza tra un percorso di eventi unitario e un percorso di qualificazione del pubblico?** — Un percorso di eventi unitario viene attivato da un’azione specifica del cliente (ad esempio, l’acquisto); un percorso di qualificazione del pubblico viene attivato quando un profilo entra o esce da un segmento di pubblico in base alla valutazione dei criteri di streaming.
* **Q: quali tipi di percorso supportano la lettura incrementale?** — Solo i percorsi Read Audience supportano la lettura incrementale; gli altri tre tipi di percorso non la supportano.
* **Q: posso aggiungere un&#39;attività Read Audience a un percorso di eventi unitario?** — No; l&#39;attività Read Audience è disponibile solo come voce percorso nei percorsi di eventi Read Audience e Business.
* **Q: posso utilizzare un&#39;attività Salta in un percorso Read Audience?** — No; i percorsi che iniziano con un&#39;attività Read Audience o Audience Qualification non possono contenere un&#39;attività Jump e non possono essere il target di un Jump da un altro percorso.
* **D: posso dare il benvenuto ai nuovi utenti dell&#39;app con un percorso di qualificazione del pubblico?** — Sì, se l’ingresso è guidato da un pubblico in streaming (ad esempio, quando un profilo si unisce a un segmento di nuovi utenti); un percorso di eventi unitari di iscrizione è anche un pattern comune.
* **D: il mio percorso di qualificazione del pubblico non si attiva in tempo reale. Perché?** — I percorsi di qualificazione del pubblico richiedono un pubblico valutato in streaming. L’utilizzo di un pubblico valutato in batch è diventato obsoleto e verrà bloccato a partire da agosto 2026. [Consulta la guida alla migrazione](aq-batch-audiences-migration.md)
* **D: qual è la differenza di velocità effettiva tra l&#39;evento Unitario e il percorso Read Audience?** — I percorsi di eventi unitari condividono un limite di 5.000 TPS con i percorsi di qualificazione del pubblico a livello di organizzazione. I percorsi Read Audience supportano fino a 20.000 TPS per sandbox, rendendoli più adatti per campagne batch su larga scala.

+++
