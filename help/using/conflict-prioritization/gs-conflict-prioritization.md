---
title: Gestione dei conflitti e assegnazione delle priorità
description: Scopri come sfruttare gli strumenti per i conflitti e l’assegnazione delle priorità di Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: ht
source-wordcount: '716'
ht-degree: 100%

---

# Gestione dei conflitti e assegnazione delle priorità {#conflict-prioritization}

## Strumenti di gestione dei conflitti e assegnazione delle priorità {#tools}

In Journey Optimizer, è essenziale gestire il volume e la tempistica delle campagne e dei percorsi per evitare di sopraffare la clientela con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e l’assegnazione delle priorità.

Questi strumenti sono disponibili per le campagne e per i percorsi unitari, di qualificazione del pubblico e di tipo “Leggi pubblico”.

Sfruttando questi strumenti, puoi garantire attività di marketing più fluide e mirate, consegnando il messaggio giusto al momento giusto ed evitando conflitti e sovraccarichi.

### Strumento di rilevamento dei conflitti

Con lo **strumento di rilevamento dei conflitti**, è possibile identificare potenziali sovrapposizioni in percorsi e campagne. Questo è fondamentale, in quanto troppe comunicazioni simultanee possono causare un affaticamento della clientela. Journey Optimizer consente di monitorare elementi quali timeline, sovrapposizione del pubblico e configurazioni del canale. Identificando i conflitti per tempo, puoi perfezionare le campagne per evitare di inviare ai clienti troppi messaggi allo stesso tempo.

➡️ [Scopri come rilevare potenziali conflitti in percorsi e campagne](conflicts.md)

### Punteggi di priorità

I **punteggi di priorità** ti aiutano a controllare quali campagne o percorsi hanno la precedenza nei casi cui una persona risulti idonea a più comunicazioni. Questa funzione è particolarmente utile per i canali in entrata, come web e mobile, dove è possibile presentare una sola campagna in un dato momento. Assegnando un punteggio di priorità a ogni percorso o campagna, puoi garantire che venga consegnato per primo il messaggio più importante.

➡️ [Scopri come assegnare punteggi di priorità a percorsi e campagne](priority-scores.md)

### Set di regole

I set di regole consentono di **raggruppare più regole in set di regole** e di applicarle ai percorsi e alle campagne desiderate. Questo fornisce una maggiore granularità per limitare la frequenza e il numero di percorsi a cui una persona può accedere entro un determinato arco temporale o per controllare la frequenza con cui gli utenti ricevono un messaggio a seconda del tipo di comunicazione. [Scopri come utilizzare i set di regole](../conflict-prioritization/rule-sets.md)

* **Limitazione del percorso e arbitrato**

  I set di regole consentono di limitare la frequenza e il numero di percorsi a cui una persona può accedere entro un determinato arco temporale. Puoi anche configurare delle regole per limitare il numero di ingressi a un percorso per un profilo oppure limitare il numero di percorsi ai quali una persona più registrata allo stesso tempo.

  Inoltre, puoi usare le impostazioni di arbitrato per decidere il percorso al quale una persona può entrare qualora sia qualificata per più percorsi, utilizzando i punteggi di priorità per determinare il percorso più adatto.

  ➡️ [Scopri come utilizzare l’arbitrato e la limitazione dei percorsi](journey-capping.md)

* **Quota limite per canale e tipo di comunicazione**

  Puoi utilizzare i set di regole anche per impostare una quota limite per tipo di comunicazione (ad esempio Vendite, Promozioni) per evitare di sovraccaricare la clientela con messaggi simili. Puoi controllare la frequenza su più canali, escludendo automaticamente i profili sollecitati eccessivamente per garantire una migliore esperienza cliente.

  ➡️ [Scopri come impostare la quota limite per canale e tipo di comunicazione](../conflict-prioritization/channel-capping.md)

## Guardrail e limitazioni

* **Campagne e punteggi di priorità** - Nelle campagne, il punteggio di priorità è disponibile solo per i canali in entrata **web**, **in-app** e **basati su codice**.

* **Latenza nell’aggiornamento del contatore profili**

  Dopo l’ingresso di una persona in un percorso, l’aggiornamento del valore del contatore di profili può richiedere fino a 10 minuti .

  Se un profilo effettua l’ingresso in due percorsi in un breve intervallo di tempo, il secondo percorso potrebbe non riconoscere correttamente che il limite di frequenza è già stato raggiunto, ed è quindi possibile che il profilo entri in entrambi i percorsi.

* **Priorità dello spazio dei nomi per la limitazione degli ingressi al percorso**

  La limitazione degli ingressi è supportata solo se lo spazio dei nomi selezionato nel percorso corrisponde allo spazio dei nomi con priorità più elevata definita nella sandbox. Se la priorità dello spazio dei nomi non è stata configurata in modo esplicito, la priorità più elevata predefinita è quella e-mail.

* **Attivazioni simultanee nei percorsi di qualificazione del pubblico**

  Quando più percorsi di qualificazione del pubblico vengono attivati dallo stesso evento di qualificazione del pubblico, i conteggi per la limitazione degli ingressi non sarà precisa. Se i conteggi sono al di sotto del limite, il percorso continuerà ad arbitrare, ma in caso di attivazioni simultanee non sarà in grado di ottenere i conteggi più aggiornati.

## Risorse aggiuntive

* **[Gestire i conflitti](conflicts.md)**: scopri come identificare e risolvere i conflitti tra le campagne e i percorsi sovrapposti.
* **[Impostare punteggi di priorità](priority-scores.md)**: informazioni su come assegnare e utilizzare i punteggi di priorità per controllare la precedenza della consegna dei messaggi.
* **[Configurare la quota limite](channel-capping.md)**: scopri come impostare le quote limite a livello di canale per evitare l’invio eccessivo di messaggi.
* **[Creare set di regole](rule-sets.md)**: scopri come creare regole di business per la gestione avanzata dei conflitti e la governance dei messaggi.
* **[Limitazione specifica del percorso](journey-capping.md)**: imposta le regole di limitazione a livello di percorso per controllare la frequenza dei messaggi all’interno dei percorsi.
* **[Tutorial sulla gestione dei conflitti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}**: esplora i tutorial video dettagliati sulla gestione dei conflitti e l’assegnazione delle priorità.
