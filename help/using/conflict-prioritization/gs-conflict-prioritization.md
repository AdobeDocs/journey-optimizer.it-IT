---
title: Gestione dei conflitti e assegnazione delle priorità
description: Scopri come sfruttare gli strumenti per i conflitti e l’assegnazione delle priorità di Journey Optimizer.
role: User
level: Beginner
badge: label="Disponibilità limitata"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: f55f985375cf360ce55074cb227b6c424db05b5c
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 94%

---

# Gestione dei conflitti e assegnazione delle priorità {#conflict-prioritization}

>[!AVAILABILITY]
>
>Le funzionalità relative ai conflitti e all’assegnazione delle priorità sono attualmente in disponibilità limitata per un gruppo selezionato della clientela. Tenere presente che queste funzioni verranno gradualmente implementate per più utenti in futuro. Se lo desideri, puoi rivolgerti al team del tuo account per l’inserimento nella lista d’attesa per queste funzioni.

In Journey Optimizer, gestire il volume e la tempistica delle campagne e dei percorsi è essenziale per evitare di sopraffare la clientela con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e l’assegnazione delle priorità.

Questi strumenti sono disponibili per campagne e percorsi di pubblico unitari, di qualificazione del pubblico e di lettura.

Sfruttando questi strumenti, puoi garantire attività di marketing più fluide e mirate, distribuendo il messaggio giusto al momento giusto ed evitando conflitti e sovraccarichi.

## Strumenti di gestione dei conflitti e assegnazione delle priorità {#tools}

Con lo **strumento di rilevamento dei conflitti**, è possibile identificare potenziali sovrapposizioni in percorsi e campagne. Questo è fondamentale, in quanto troppe comunicazioni simultanee possono causare un affaticamento della clientela. Journey Optimizer consente di monitorare elementi quali timeline, sovrapposizione del pubblico e configurazioni del canale. Identificando i conflitti in anticipo, puoi perfezionare le campagne per evitare di bersagliare la clientela con più messaggi contemporaneamente. [Scopri come rilevare potenziali conflitti in percorsi e campagne](conflicts.md)

Inoltre, **i punteggi di priorità** ti aiutano a controllare quali campagne o percorsi hanno la precedenza quando la clientela è idonea a più comunicazioni. Questa funzione è particolarmente utile per i canali in entrata, come web e mobile, dove è possibile visualizzare una sola campagna in un dato momento. Assegnando un punteggio di priorità a ogni percorso o campagna, puoi garantire che venga consegnato per primo il messaggio più importante. [Scopri come assegnare punteggi di priorità a percorsi e campagne](priority-scores.md)

**Arbitrato e limitazione dei percorsi** consente di limitare la frequenza e il numero di percorsi a cui può accedere la clientela entro un determinato intervallo di tempo. Puoi configurare delle regole per limitare il numero di ingressi a un percorso per un profilo oppure limitare il numero di percorsi in cui la clientela può essere ammessa contemporaneamente. Inoltre, è possibile utilizzare le impostazioni di arbitrato per decidere a quale percorso debba effettuare l’ingresso la clientela nel caso sia qualificata per più percorsi, utilizzando punteggi di priorità per determinare la soluzione migliore. [Scopri come utilizzare la limitazione e l’arbitrato dei percorsi](journey-capping.md)

Infine, puoi anche utilizzare i set di regole per impostare una **quota limite per tipo di comunicazione** (ad esempio Vendite, Promozioni) per evitare di sovraccaricare la clientela con messaggi simili. Puoi controllare la frequenza su più canali, escludendo automaticamente i profili sollecitati eccessivamente per garantire una migliore esperienza cliente. [Scopri come utilizzare i set di regole](../configuration/rule-sets.md)</li></ul>

Sfruttando queste funzioni, puoi garantire attività di marketing più fluide e mirate, consegnando il messaggio giusto al momento giusto ed evitando conflitti e sovraccarichi.

## Guardrail e limitazioni

**Quota limite e tipi di pubblico in batch**

Per la quota limite, sia per il canale che per il percorso, se il pubblico utilizzato è un pubblico batch, il valore del contatore di profili a cui si fa riferimento al momento dell’ingresso nel percorso o il runtime del messaggio per una comunicazione di canale sarà quello dell’istantanea giornaliera acquisita.

Questo può essere problematico in quanto la clientela può superare la quota limite di frequenza se ha effettuato l’ingresso in un altro percorso o se ha ricevuto un’altra comunicazione tra il momento dell’istantanea giornaliera e quello di ingresso al percorso (o del messaggio che viene consegnato).

**Quota limite e tipi di pubblico in streaming**

Per i tipi di pubblico in streaming, il riconoscimento di un valore di contatore aggiornato da parte del sistema può richiedere fino a 2 ore. Pertanto, per ridurre questo rischio si consiglia di distanziare le comunicazioni e i percorsi di almeno due ore, se possibile.

**Ora di inizio dei percorsi**

Per garantire il corretto funzionamento delle funzioni di gestione dei conflitti e assegnazione delle priorità, è consigliato impostare l’ora di inizio del percorso almeno a 10 minuti, in modo da consentire al sistema di aggiornare il contatore di conseguenza.

Se la clientela ha già raggiunto il limite massimo di entrata in un percorso, non potrà comunque accedervi, ma se non lo ha raggiunto, il contatore di ingresso non verrà incrementato.

**Arbitrato dei percorsi**

Per il momento, solo i percorsi Leggi pubblico sono supportati per l’arbitrato dei percorsi. Le impostazioni di arbitrato non possono essere sfruttate per percorsi unitari o di qualificazione del pubblico.
