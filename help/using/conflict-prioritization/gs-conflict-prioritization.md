---
title: Gestione dei conflitti e assegnazione delle priorità
description: Scopri come sfruttare gli strumenti per i conflitti e l’assegnazione delle priorità di Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: a0eda2e1d021af37eb54f3ffa5bac0ac6e8ef6ce
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 30%

---

# Gestione dei conflitti e assegnazione delle priorità {#conflict-prioritization}

In Journey Optimizer, è essenziale gestire il volume e la tempistica delle campagne e dei percorsi per evitare di sopraffare la clientela con troppe interazioni. Gli strumenti per la gestione dei conflitti e la definizione delle priorità consentono di comunicare in modo tempestivo e accurato, evitando l&#39;affaticamento dei clienti e garantendo che i messaggi corretti raggiungano il pubblico. Utilizzando il rilevamento dei conflitti, i punteggi di priorità e i set di regole, puoi semplificare le campagne e i percorsi per evitare sovrapposizioni e bilanciare la frequenza tra i canali.

Questi strumenti sono disponibili per le campagne e per i percorsi di pubblico unitari, di qualificazione del pubblico e di lettura. Che tu stia impostando limiti sulla frequenza con cui vengono inviati i messaggi o decidendo quali campagne hanno la precedenza, queste funzioni collaborano per semplificare il processo decisionale e ottimizzare la strategia di marketing.

## Da dove iniziare {#where-to-start}

| Il tuo obiettivo | Strumento | Azione |
|-----------|------|--------|
| Verificare se i percorsi o le campagne si sovrappongono (timeline, pubblico, canale) | **Rilevamento conflitti** | [Identificare conflitti potenziali](conflicts.md) |
| Decidere quale messaggio vince quando un profilo si qualifica per diversi | **Punteggi di priorità** | [Assegna punteggi di priorità](priority-scores.md) |
| Limitare la frequenza o il numero di messaggi ricevuti da un profilo | **Set di regole** (limite di frequenza, limite di percorso, ore non interattive) | [Imposta le regole di limitazione messaggi e percorso](../../rp_landing_pages/capping-rules-landing-page.md) |

**Flusso tipico:** utilizza il rilevamento dei conflitti per individuare le sovrapposizioni, quindi applica punteggi di priorità e set di regole per controllare quali messaggi vengono inviati e con quale frequenza.

## Strumenti di gestione dei conflitti e definizione delle priorità {#tools}

### Strumento di rilevamento dei conflitti

Con lo **strumento di rilevamento dei conflitti**, è possibile identificare potenziali sovrapposizioni in percorsi e campagne. Questo è fondamentale, in quanto troppe comunicazioni simultanee possono causare un affaticamento della clientela. Journey Optimizer consente di monitorare elementi quali timeline, sovrapposizione del pubblico e configurazioni del canale. Identificando i conflitti per tempo, puoi perfezionare le campagne per evitare di inviare ai clienti troppi messaggi allo stesso tempo.

[Scopri come rilevare potenziali conflitti in percorsi e campagne](conflicts.md)

### Punteggi di priorità

I **punteggi di priorità** ti aiutano a controllare quali campagne o percorsi hanno la precedenza nei casi cui una persona risulti idonea a più comunicazioni. Questa funzione è particolarmente utile per i canali in entrata, come web e mobile, dove è possibile presentare una sola campagna in un dato momento. Assegnando un punteggio di priorità a ogni percorso o campagna, puoi garantire che venga consegnato per primo il messaggio più importante.

[Scopri come assegnare punteggi di priorità a percorsi e campagne](priority-scores.md)

### Set di regole

I set di regole ti consentono di **raggruppare più regole** e applicarle ai percorsi e alle campagne che preferisci. Ciò offre una maggiore granularità per limitare la frequenza e il numero di percorsi che un cliente può inserire entro un determinato intervallo di tempo, oppure per controllare la frequenza con cui gli utenti ricevono i messaggi a seconda del tipo di comunicazione.

* **Limitazione Percorsi e arbitrato** - Limita la frequenza e il numero di percorsi che un cliente può immettere entro un determinato intervallo di tempo. Puoi limitare il numero di voci di percorso per un profilo o limitare il numero di percorsi in cui un cliente può essere iscritto contemporaneamente. Utilizzare le impostazioni di arbitrato per decidere il percorso che un cliente deve inserire se si qualifica per più percorsi, utilizzando i punteggi di priorità per determinare il miglior abbinamento. [Scopri come utilizzare la limitazione e l’arbitrato dei percorsi](journey-capping.md)

* **Limitazione di frequenza per canale e tipo di comunicazione** - Impostare la limitazione di frequenza per tipo di comunicazione (ad esempio Vendite, Promozionali) per evitare di sovraccaricare i clienti con messaggi simili. Controlla la frequenza su più canali, escludendo automaticamente i profili sollecitati eccessivamente. [Scopri come impostare il limite di frequenza per canale e tipo di comunicazione](channel-capping.md)

* **Ore tranquille** - Definisci le esclusioni basate sul tempo in modo che non vengano inviati messaggi durante periodi specifici (e-mail, SMS, push, WhatsApp). [Scopri come impostare le ore non interattive](quiet-hours.md)

[Scopri come utilizzare i set di regole](rule-sets.md)

## Guardrail e limitazioni {#guardrails}

* **Campagne e punteggi di priorità** - Nelle campagne, il punteggio di priorità è disponibile solo per i canali in entrata **web**, **in-app** e **basati su codice**.

* **Latenza aggiornamento contatore profili** - Possono essere necessari fino a 10 minuti dopo che un cliente ha inserito un percorso per aggiornare il valore del contatore profili. Se un profilo effettua l’ingresso in due percorsi in un breve intervallo di tempo, il secondo percorso potrebbe non riconoscere correttamente che il limite di frequenza è già stato raggiunto, ed è quindi possibile che il profilo entri in entrambi i percorsi.

* **Priorità dello spazio dei nomi per il limite delle voci di percorso** - Il limite delle voci è supportato solo se lo spazio dei nomi selezionato nel percorso è lo spazio dei nomi con la priorità più elevata definito nella sandbox. Se la priorità dello spazio dei nomi non è stata configurata in modo esplicito, la priorità più elevata predefinita è quella e-mail.

* **Attivazioni simultanee nei percorsi di qualificazione del pubblico** - Quando più percorsi di qualificazione del pubblico vengono attivati dallo stesso evento di qualificazione del pubblico, i conteggi per il limite di ingresso non saranno accurati. Se i conteggi sono al di sotto del limite massimo, il percorso continuerà ad arbitrare, ma non sarà in grado di ottenere i conteggi più aggiornati con attivazioni simultanee.

## Risorse aggiuntive

* **[Identificare potenziali conflitti](conflicts.md)** - Scopri come rilevare e risolvere i conflitti tra campagne e percorsi sovrapposti.
* **[Assegna punteggi di priorità](priority-scores.md)** - Scopri come assegnare e utilizzare i punteggi di priorità per controllare la precedenza di consegna dei messaggi.
* **[Utilizzare i set di regole](rule-sets.md)** - Scopri come generare e applicare i set di regole per la gestione dei conflitti e la governance dei messaggi.
* **[Limitazione Percorsi e arbitrato](journey-capping.md)** - Imposta le regole di limitazione a livello di percorso e l&#39;arbitrato.
* **[Limitazione della frequenza per canale](channel-capping.md)** - Imposta i limiti di frequenza a livello di canale per evitare messaggi eccessivi.
* **[Imposta le ore non interattive](quiet-hours.md)** - Definisci le esclusioni basate sul tempo per la consegna dei messaggi.
* **[Esercitazioni sulla gestione dei conflitti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}** - Esercitazioni video dettagliate.
