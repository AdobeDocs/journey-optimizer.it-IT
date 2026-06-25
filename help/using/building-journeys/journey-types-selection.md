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
hide: true
exl-id: 0c894dc1-76b6-4b33-baf8-eaf6686f7d38
TQID: https://experienceleague.adobe.com/rEANha6Lppyd5vog-0kZ3aL9VvZHc9kziW-d-jiWqeA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cce82f05-fc3c-4af7-85ff-8bba603861a7
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 6f35d9b951850220382e3662502b9e1d7ad6b990
workflow-type: tm+mt
source-wordcount: 2295
ht-degree: 1%

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

**I percorsi di qualificazione del pubblico** si attivano quando i profili si qualificano per un pubblico specifico (o ne escono). I profili vengono inseriti singolarmente in base ai criteri, consentendo un coinvolgimento immediato quando il comportamento del cliente cambia. Per il comportamento di immissione in tempo reale, il pubblico deve essere **valutato in streaming**; i tipi di pubblico valutati in batch attivano la voce solo alla finestra di valutazione successiva (fino a 24 ore).

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
| **Requisiti dei dati** | Schema evento con dati trigger | Pubblico [!DNL Adobe Experience Platform] | Pubblico in streaming (richiesto per l’immissione in tempo reale); il pubblico batch è supportato ma l’immissione subisce ritardi | Schema evento di business |

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
* I percorsi di qualificazione del pubblico richiedono un pubblico valutato in streaming per l’immissione in tempo reale; i pubblici valutati in batch causano ritardi di immissione fino a 24 ore
* I percorsi unitari di qualificazione di eventi e pubblico condividono un limite di velocità effettiva di 5.000 TPS a livello di organizzazione; Read Audience percorsi supportano fino a 20.000 TPS per sandbox
* La simulazione è supportata per la maggior parte dei tipi di percorso ma non per l&#39;immissione di eventi aziendali. Vedere Limitazioni della simulazione per le restrizioni a livello di nodo
* Un profilo già presente in un percorso non può rientrare nella stessa versione di quel percorso, indipendentemente dalla configurazione di rientro

**Terminologia:**

* Nome canonico: percorso unitario di eventi — varianti: percorso attivato da eventi, percorso unitario
* Nome canonico: percorso Read Audience — varianti: percorso batch, percorso trigger segmento, percorso Leggi segmento
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
* **D: il mio percorso di qualificazione del pubblico non si attiva in tempo reale. Perché?** — I percorsi di qualificazione del pubblico richiedono un pubblico valutato in streaming. Se il pubblico viene valutato in batch (ad esempio, uno snapshot giornaliero), l’immissione viene posticipata alla finestra di valutazione successiva, che può durare fino a 24 ore.
* **D: qual è la differenza di velocità effettiva tra l&#39;evento Unitario e il percorso Read Audience?** — I percorsi di eventi unitari condividono un limite di 5.000 TPS con i percorsi di qualificazione del pubblico a livello di organizzazione. I percorsi Read Audience supportano fino a 20.000 TPS per sandbox, rendendoli più adatti per campagne batch su larga scala.

+++
