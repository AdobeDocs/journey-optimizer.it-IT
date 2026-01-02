---
solution: Journey Optimizer
product: journey optimizer
title: Tipi di percorso e guida alla selezione
description: Confronta i tipi di percorso e scegli quello giusto per il tuo caso d’uso con le guide alla decisione e la matrice di compatibilità delle funzioni
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: Tipi di percorso, unitari, pubblico di lettura, qualificazione del pubblico, evento di business, confronto, guida alle decisioni, scelta, selezione, in tempo reale, pianificato, batch, attivato da evento
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: 8ea2a0fe685678d41004d549443a1757eb30c765
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 3%

---


# Tipi di percorso e guida alla selezione {#journey-types-selection}

Adobe Journey Optimizer supporta quattro tipi di percorsi, ciascuno progettato per diversi meccanismi di ingresso e scenari aziendali. Questa guida ti aiuta a comprendere le differenze e a scegliere il tipo giusto per il tuo caso d’uso.

## Panoramica sui tipi di percorso {#journey-types}

>[!BEGINTABS]

>[!TAB percorsi unitari]

**Quando utilizzare:** esperienze in tempo reale attivate da eventi

**I percorsi unitari** vengono attivati singolarmente quando si verifica un&#39;azione specifica (acquisto, accesso all&#39;app, invio di moduli). I profili vengono inseriti uno alla volta in tempo reale, rendendolo ideale per risposte immediate e basate sul comportamento.

**Ideale per:** ordinare conferme dopo l&#39;acquisto, e-mail di benvenuto quando qualcuno si abbona, abbandono del carrello attivato dalla navigazione e notifiche di reimpostazione della password.

➡️ [Informazioni sugli eventi](../event/about-events.md) | [Caso di utilizzo: messaggio agli abbonati](message-to-subscribers-uc.md)

>[!TAB Leggi percorsi di pubblico]

**Quando utilizzare:** campagne pianificate per i segmenti di pubblico

**Leggi percorsi di pubblico** inizia con un pubblico Adobe Experience Platform e invia messaggi in batch a tutti i profili contemporaneamente. Questo percorso è ideale per comunicazioni pianificate su larga scala.

**Ideale per:** newsletter mensili, campagne promozionali per segmenti di destinazione, annunci di prodotti e campagne di marketing stagionali.

➡️ [Scopri il pubblico in lettura](read-audience.md) | [Introduzione ai tipi di pubblico](../audience/about-audiences.md)

>[!TAB percorsi di qualificazione del pubblico]

**Quando utilizzare:** le risposte in tempo reale alle modifiche di iscrizione al pubblico

**I percorsi di qualificazione del pubblico** si attivano quando i profili si qualificano per un pubblico specifico (o ne escono). I profili vengono inseriti singolarmente in quanto soddisfano i criteri in tempo reale, consentendo un coinvolgimento immediato quando il comportamento del cliente cambia.

**Ideale per:** notifiche di aggiornamento a livello VIP, nuovo coinvolgimento quando i clienti diventano inattivi, messaggi di festeggiamento del primo acquisto e targeting geografico quando i clienti si spostano.

➡️ [Scopri le qualificazioni per il pubblico](audience-qualification-events.md) | [Creazione di tipi di pubblico](../audience/creating-a-segment-definition.md)

>[!TAB percorsi di eventi di business]

**Quando utilizzare:** condizioni aziendali che interessano più clienti

**I percorsi di eventi aziendali** sono attivati da eventi a livello aziendale (aggiornamenti delle scorte, avvisi meteo, variazioni di prezzo) che interessano più profili contemporaneamente. Questi rispondono a condizioni di business più ampie piuttosto che ad azioni individuali.

**Ideale per:** avvisi di inventario ridotti per i clienti interessati, annunci di vendita flash, promozioni basate su meteo, notifiche di calo dei prezzi e avvisi di back-in-stock dei prodotti.

➡️ [Informazioni sugli eventi di business](../event/about-creating-business.md) | [Gestione delle voci](entry-management.md)

>[!ENDTABS]

## Guida alla decisione: scelta del tipo di percorso {#decision-guide}

Per selezionare il tipo di percorso appropriato per il caso d’uso, segui questa struttura decisionale:

### Passaggio 1: cosa attiva il percorso?

* **Il cliente esegue un&#39;azione specifica** (acquisto, clic, accesso) → Passare al passaggio 2
* **Ora/Pianificazione** (invio a un&#39;ora specifica o ricorrente) → **Usa percorso Read Audience**
* **Modifiche allo stato del cliente** (si unisce/lascia un segmento) → Passare al passaggio 3
* **Condizione aziendale** (livello azionario, variazione di prezzo, meteo) → **Utilizza percorso eventi aziendali**

### Passaggio 2: trigger di azione del cliente individuale

* **È necessaria una risposta immediata e in tempo reale?**
   * Sì → **Usa percorso unitario**
   * Nessun → Considerare la lettura del percorso di pubblico con l’esecuzione pianificata

### Passaggio 3: modifiche allo stato del cliente

* **È necessario rispondere quando i clienti entrano o escono da un segmento?**
   * Sì → **Utilizza percorso di qualificazione del pubblico**
   * No, solo quando si immette → Considera percorso unitario con evento o Leggi pubblico con filtro pubblico

### Selezione rapida per caso d’uso

| Il tuo obiettivo | Tipo di percorso consigliato | Perché |
|-----------|------------------------|-----|
| Invia conferma ordine dopo l’acquisto | Unitario | Risposta immediata alle azioni individuali |
| Invia newsletter mensile agli abbonati | Read Audience | Comunicazione batch programmata |
| Avvisa i clienti quando raggiungono lo stato VIP | Qualificazione del pubblico | Risposta in tempo reale al cambiamento di stato |
| Avvisa i clienti in caso di scorte ridotte sugli articoli osservati | Evento di business | La condizione di business interessa più clienti |
| Benvenuto per i nuovi utenti dell&#39;app | Unitario | Attivato da un evento di registrazione |
| Coinvolgere di nuovo i clienti inattivi | Qualificazione del pubblico | Risponde alla voce segmento inattività |
| Promozione stagionale nel segmento di destinazione | Read Audience | Campagna pianificata al pubblico |
| Annuncio vendita flash | Evento di business | Le decisioni aziendali influiscono su più clienti |

>[!NOTE]
>
>Non sei sicuro del tipo da scegliere? Inizia con **percorsi unitari** per le esperienze basate su eventi o **Leggi percorsi di pubblico** per le campagne pianificate; questi riguardano i casi d&#39;uso più comuni.

## Confronto dettagliato dei tipi di percorso {#journey-types-comparison}

Utilizzare questa tabella per confrontare rapidamente i tipi di percorso e scegliere quello corretto per il caso d&#39;uso:

| Formato | Percorsi unitari | Leggi percorsi di pubblico | Percorsi di qualificazione del pubblico | Percorsi di eventi aziendali |
|--------|------------------|------------------------|--------------------------------|------------------------|
| **Meccanismo di ingresso** | Attivazione evento individuale | Batch programmato | Modifica dell’iscrizione al pubblico in tempo reale | Evento a livello aziendale |
| **Tempistica di ingresso** | In tempo reale, quando si verificano gli eventi | Pianificato (una tantum o ricorrente) | In tempo reale, quando si verifica la qualifica | In tempo reale, quando viene attivato un evento di business |
| **Voce profilo** | Uno alla volta | Tutto in una volta (batch) | Uno alla volta | Più profili simultaneamente |
| **Origine trigger** | Azione del cliente (acquisto, clic, accesso) | Pianificazione basata su tempo | Iscrizione al pubblico (entrata/uscita) | Condizioni dell’attività (scorte, tempo, prezzo) |
| **Ottimo per** | Messaggi transazionali, risposte comportamentali | Campagne di marketing, newsletter | Programmi fedeltà, fasi del ciclo di vita | Avvisi di inventario, promozioni, condizioni aziendali |
| **Usa quando** | Necessità di una risposta immediata alle singole azioni | Raggiungere grandi segmenti di pubblico secondo la pianificazione | Risposta alle modifiche dello stato del cliente | Gli eventi di business interessano più clienti |
| **Esempi** | Conferma dell’ordine, reimpostazione della password | Newsletter mensile, campagna stagionale | Aggiornamento VIP, avviso di inattività | Allarme scorte basse, vendita flash, calo prezzi |
| **Rientro** | Configurabile (consente più voci per profilo) | Ogni profilo viene immesso una volta per esecuzione | Configurabile per evento di qualifica | Più profili possono essere interessati dallo stesso evento |
| **Requisiti dei dati** | Schema evento con dati trigger | Pubblico Adobe Experience Platform | Pubblico in streaming o in batch | Schema evento di business |

## Compatibilità delle funzioni per tipo di percorso {#feature-compatibility}

Non tutte le funzionalità sono disponibili per tutti i tipi di percorso. Utilizza questa matrice per capire quali funzionalità funzionano con quali tipi di percorso:

| Funzionalità | Unitario | Read Audience | Qualificazione del pubblico | Evento di business |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Meccanismi di ingresso** |
| Voce attivata da eventi | ✅ | ❌ | ❌ | ✅ |
| Voce pianificata | ❌ | ✅ | ❌ | ❌ |
| Voce basata sul pubblico | ❌ | ✅ | ✅ | ❌ |
| **Funzioni di orchestrazione** |
| Attività di attesa | ✅ | ✅ | ✅ | ✅ |
| Attività condizione | ✅ | ✅ | ✅ | ✅ |
| Azioni personalizzate | ✅ | ✅ | ✅ | ✅ |
| Attività Read audience (nel percorso) | ✅ | ✅ | ✅ | ✅ |
| Attività di qualificazione del pubblico | ✅ | ✅ | ✅ | ✅ |
| Attività Salta | ✅ | ✅ | ✅ | ✅ |
| **Gestione profilo** |
| Rientro profilo | ✅ configurabile | ❌ una volta per esecuzione | ✅ configurabile | ✅ per evento |
| Configurazione dello spazio dei nomi | ✅ richiesto | ✅ facoltativo | ✅ richiesto | ✅ richiesto |
| Limite del profilo | ✅ | ✅ | ✅ | ✅ |
| **Test e ottimizzazione** |
| Modalità di test | ✅ | ✅ | ✅ | ✅ |
| Esecuzione a secco | ✅ | ✅ | ✅ | ✅ |
| Esperimenti di percorso (test A/B) | ✅ | ✅ | ✅ | ❌ |
| Ottimizzazione del tempo di invio | ✅ | ✅ | ✅ | ✅ |
| **Canali** |
| E-mail | ✅ | ✅ | ✅ | ✅ |
| Notifiche push | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| Messaggi in-app | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Schede di contenuto | ✅ | ✅ | ✅ | ✅ |
| **Funzionalità avanzate** |
| Lettura incrementale | ❌ | ✅ | ❌ | ❌ |
| Esporta pubblico | ✅ | ✅ | ✅ | ✅ |
| Gestione del fuso orario | ✅ | ✅ | ✅ | ✅ |
| Eventi di reazione | ✅ | ✅ | ✅ | ✅ |
| Origini dati esterne | ✅ | ✅ | ✅ | ✅ |
| Limitazione/Limitazione | ✅ | ✅ | ✅ | ✅ |

**Legenda:** ✅ = Supportata | ❌ = Non supportato

## Passaggi successivi {#next-steps}

Ora che conosci i tipi di percorso, puoi effettuare le seguenti operazioni:

* **[Crea il tuo primo percorso](journey-gs.md)** - Guida dettagliata
* **[Scopri la finestra di progettazione del percorso](using-the-journey-designer.md)** - Progetta l&#39;area di lavoro del percorso
* **[Esplora le funzionalità di percorso](journey.md#capabilities)** - Scopri le funzionalità avanzate
* **[Visualizza domande frequenti sul percorso](journey-faq.md)** - Risposte alle domande comuni

**È necessario eseguire un confronto con le campagne?**
&#x200B;- [Guida al confronto tra Percorsi e campagne](../start/journeys-vs-campaigns.md) - Scegli tra percorsi, campagne Action/API e campagne orchestrate

