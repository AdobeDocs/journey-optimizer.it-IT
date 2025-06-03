---
title: Gestione dei conflitti e assegnazione delle priorità
description: Scopri come sfruttare gli strumenti per i conflitti e l’assegnazione delle priorità di Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 28%

---

# Gestione dei conflitti e assegnazione delle priorità {#conflict-prioritization}

## Strumenti di gestione dei conflitti e assegnazione delle priorità {#tools}

In Journey Optimizer, è essenziale gestire il volume e la tempistica delle campagne e dei percorsi per evitare di sopraffare la clientela con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e l’assegnazione delle priorità.

Questi strumenti sono disponibili per le campagne e per i percorsi unitari, di qualificazione del pubblico e di tipo “Leggi pubblico”.

Sfruttando questi strumenti, puoi garantire attività di marketing più fluide e mirate, consegnando il messaggio giusto al momento giusto ed evitando conflitti e sovraccarichi.

### Strumento di rilevamento dei conflitti

Con lo **strumento di rilevamento dei conflitti**, è possibile identificare potenziali sovrapposizioni in percorsi e campagne. Questo è fondamentale, in quanto troppe comunicazioni simultanee possono causare un affaticamento della clientela. Journey Optimizer consente di monitorare elementi quali timeline, sovrapposizione del pubblico e configurazioni del canale. Identificando i conflitti in anticipo, puoi perfezionare le campagne per evitare di bombardare i clienti con più messaggi contemporaneamente.

➡️ [Scopri come rilevare potenziali conflitti in percorsi e campagne](conflicts.md)

### Punteggi di priorità

**I punteggi di priorità** consentono di controllare quali campagne o percorsi hanno la precedenza quando un cliente è idoneo a più comunicazioni. Questa funzione è particolarmente utile per i canali in entrata, come web e mobile, dove è possibile visualizzare una sola campagna in un dato momento. Assegnando un punteggio di priorità a ogni percorso o campagna, puoi garantire che venga consegnato per primo il messaggio più importante.

➡️ [Scopri come assegnare punteggi di priorità a percorsi e campagne](priority-scores.md)

### Set di regole

I set di regole ti consentono di **raggruppare più regole in set di regole** e di applicarle ai percorsi e alle campagne di tua scelta. Questo fornisce una maggiore granularità per limitare la frequenza e il numero di percorsi che un cliente può inserire entro un determinato intervallo di tempo o controllare la frequenza con cui gli utenti riceveranno un messaggio a seconda del tipo di comunicazione.

* **Limitazione Percorsi e arbitrato**

  I set di regole consentono di limitare la frequenza e il numero di percorsi che un cliente può inserire in un determinato intervallo di tempo. Puoi anche impostare regole per limitare il numero di voci di percorso per un profilo o limitare il numero di percorsi in cui un cliente può essere iscritto contemporaneamente.

  Inoltre, è possibile utilizzare le impostazioni di arbitrato per decidere quale percorso deve essere immesso da un cliente se si qualifica per più percorsi, utilizzando i punteggi di priorità per determinare il miglior adattamento.

  ➡️ [Scopri come utilizzare la limitazione dei percorsi e l&#39;arbitrato](journey-capping.md)

* **Limitazione della frequenza per canale e tipo di comunicazione**

  Puoi anche utilizzare i set di regole per impostare il limite di frequenza per tipo di comunicazione (ad esempio, Vendite, Promozionali) per evitare di sovraccaricare i clienti con messaggi simili. Puoi controllare la frequenza su più canali, escludendo automaticamente i profili sollecitati eccessivamente per garantire una migliore esperienza cliente.

  ➡️ [Scopri come impostare il limite di frequenza per canale e tipo di comunicazione](../conflict-prioritization/channel-capping.md)

## Guardrail e limitazioni

* **Campagne e punteggi di priorità** - Nelle campagne, il punteggio di priorità è disponibile solo per i canali in entrata **web**, **in-app** e **basati su codice**.

* **Latenza aggiornamento contatore profili**

  Possono essere necessari fino a 20 minuti dopo che un cliente ha inserito un percorso per aggiornare il valore del contatore dei profili.

  Se un profilo entra in due percorsi in una breve finestra, il secondo percorso potrebbe non riconoscere correttamente che il limite di frequenza è già stato raggiunto, consentendo potenzialmente al profilo di entrare in entrambi i percorsi.

* **Priorità dello spazio dei nomi per il limite delle voci di percorso**

  Il limite di ingresso è supportato solo se lo spazio dei nomi selezionato nel percorso corrisponde allo spazio dei nomi con priorità più elevata definito nella sandbox. Se la priorità dello spazio dei nomi non è stata configurata in modo esplicito, la priorità massima predefinita è e-mail.

* **Attivazioni simultanee nei percorsi di qualificazione del pubblico**

  Quando più percorsi di qualificazione del pubblico vengono attivati dallo stesso evento di qualificazione del pubblico, i conteggi per il limite di ingresso non saranno precisi. Se i conteggi sono al di sotto del limite massimo, il percorso continuerà ad arbitrare, ma non sarà in grado di ottenere i conteggi più aggiornati con attivazioni simultanee.
