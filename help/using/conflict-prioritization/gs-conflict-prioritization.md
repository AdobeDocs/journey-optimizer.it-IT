---
title: Gestione dei conflitti e assegnazione delle priorità
description: Scopri come sfruttare gli strumenti di gestione dei conflitti e definizione delle priorità di Journey Optimizer.
role: User
level: Beginner
badge: label="Disponibilità limitata"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: dbe312f332031391c49a973f323994f860e354e3
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 10%

---

# Gestione dei conflitti e assegnazione delle priorità {#conflict-prioritization}

>[!AVAILABILITY]
>
>Le funzionalità per conflitti e definizione delle priorità sono attualmente disponibili in Disponibilità limitata per un gruppo selezionato di clienti. Tenere presente che queste funzioni verranno gradualmente implementate per più utenti in futuro. Se lo desideri, puoi rivolgerti al team del tuo account per l’inserimento nella lista d’attesa per queste funzioni.

In Journey Optimizer, gestire il volume e la tempistica delle campagne e dei percorsi è essenziale per evitare di sopraffare i clienti con troppe interazioni. Journey Optimizer offre diversi strumenti per la gestione dei conflitti e la definizione delle priorità.

## Strumenti di gestione dei conflitti e definizione delle priorità {#tools}

Con lo strumento di rilevamento dei conflitti **&#x200B;**, è possibile identificare potenziali sovrapposizioni in percorsi e campagne. Questo è fondamentale, perché troppe comunicazioni simultanee possono causare la &quot;customer fatigue&quot;. Journey Optimizer consente di monitorare elementi quali timeline, sovrapposizione del pubblico e configurazioni dei canali. Identificando i conflitti in anticipo, puoi perfezionare le campagne per evitare di bombardare i clienti con più messaggi contemporaneamente. [Scopri come rilevare potenziali conflitti in percorsi e campagne](conflicts.md)

Inoltre, **i punteggi di priorità** ti aiutano a controllare quali campagne o percorsi hanno la precedenza quando un cliente è idoneo a più comunicazioni. Questa funzione è particolarmente utile per i canali in entrata, come web e mobile, dove è possibile visualizzare una sola campagna alla volta. Assegnando un punteggio di priorità a ogni percorso o campagna, puoi garantire che venga consegnato per primo il messaggio più importante. [Scopri come assegnare punteggi di priorità a percorsi e campagne](priority-scores.md)

**Limitazione Percorsi e arbitrato** consente di limitare la frequenza e il numero di percorsi che un cliente può inserire entro un determinato intervallo di tempo. Puoi impostare regole per limitare il numero di voci di percorso per un profilo o per limitare il numero di percorsi in cui un cliente può essere iscritto contemporaneamente. Inoltre, è possibile utilizzare le impostazioni di arbitrato per decidere quale percorso deve essere immesso da un cliente se si qualifica per più percorsi, utilizzando i punteggi di priorità per determinare il miglior adattamento. [Scopri come utilizzare la limitazione e l&#39;arbitrato del percorso](journey-capping.md)

Infine, puoi anche utilizzare i set di regole per impostare **il limite di frequenza per tipo di comunicazione** (ad esempio Vendite, Promozionali) per evitare di sovraccaricare i clienti con messaggi simili. Puoi controllare la frequenza su più canali, escludendo automaticamente i profili sollecitati eccessivamente per garantire una migliore esperienza del cliente. [Scopri come utilizzare i set di regole](../configuration/rule-sets.md)</li></ul>

Sfruttando queste funzioni, puoi garantire attività di marketing più fluide e mirate, distribuendo il messaggio giusto al momento giusto ed evitando conflitti e sovraccarichi.

## Guardrail e limitazioni

**Limitazione di frequenza e tipi di pubblico in batch**

Per il limite di frequenza, sia per il canale che per il percorso, se il pubblico utilizzato è un pubblico batch, il valore del contatore di profili a cui si fa riferimento al momento dell’ingresso nel percorso o il runtime del messaggio per una comunicazione di canale sarà quello dell’istantanea giornaliera acquisita.

Questo può essere problematico in quanto i clienti possono superare il limite di quota limite se hanno effettuato un’operazione in un altro percorso o se hanno ricevuto un’altra comunicazione tra l’ora dello snapshot giornaliero e l’ora del percorso in fase di immissione (o del messaggio in fase di consegna).

**Limitazione della frequenza e pubblico in streaming**

Per i tipi di pubblico in streaming, il riconoscimento di un valore di contatore aggiornato può richiedere fino a 2 ore. Per ridurre i rischi, si consiglia di distanziare le comunicazioni e i percorsi di almeno due ore.

**Percorsi di inizio**

Per garantire il corretto funzionamento delle funzionalità di gestione dei conflitti e definizione delle priorità, si consiglia di impostare l&#39;ora di inizio del percorso su almeno 10 minuti, in modo da consentire al sistema di aggiornare il contatore di conseguenza.

Se i clienti hanno già raggiunto il limite massimo quando entrano in un percorso, non potranno comunque entrare, ma se non hanno raggiunto il limite massimo, il contatore di ingresso non verrà incrementato.

**arbitrato di Percorso**

Per il momento, per l’arbitrato di percorso sono supportati solo i percorsi di pubblico di lettura. Le impostazioni di arbitrato non possono essere utilizzate per percorsi di qualificazione unitari o di pubblico.
