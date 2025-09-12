---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: Utilizzo dei dati in AI con Experimentation Accelerator
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenuto, esperimento, multiplo, pubblico, trattamento
hide: true
hidefromtoc: true
source-git-commit: 50dcdd30e21fe1b12d502a2b9c478f4ceb546c49
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Utilizzo dei dati in AI con Experimentation Accelerator{#experiment-accelerator-security}

>[!BEGINSHADEBOX]

* [Introduzione a Experimentation Accelerator](experiment-accelerator.md)
* [Utilizzo dei dati in AI con Experimentation Accelerator](experiment-accelerator-security.md)
* [Best practice per Experimentation Accelerator](experiment-accelerator-best-practices.md)
* [Esperimenti di monitoraggio](experiment-accelerator-monitor.md)
* [Metriche della sperimentazione](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

**Adobe Journey Optimizer Experimentation Accelerator** ti consente di scoprire automaticamente informazioni approfondite e di consigliare opportunità per migliorare i tuoi esperimenti e il tuo programma di sperimentazione. La soluzione sfrutta l’intelligenza artificiale e l’apprendimento automatico per fornire questi consigli. Questa istruzione chiarisce come vengono utilizzati i dati dei clienti in **Experimentation Accelerator**.

## Quali dati utilizza l’acceleratore della sperimentazione?

Attualmente sono disponibili tre tipi di dati utilizzati da **Acceleratore esperimento**:

* **Metadati esperimento**: nome esperimento, definizione del pubblico utilizzato nell&#39;esperimento e i trattamenti nell&#39;esperimento, ad esempio nome, percentuali suddivise, posizione o superficie in cui viene distribuito l&#39;esperimento.

* **Prestazioni dei trattamenti**: numero di persone, media della metrica di successo e deviazione standard per ogni trattamento.

* **Contenuto del trattamento**: HTML con rendering e schermata del trattamento così come apparirebbe a un utente sul tuo sito Web.

## Cosa fa l’acceleratore della sperimentazione con questi dati?

**L&#39;acceleratore della sperimentazione** prende il contenuto di ogni trattamento e crea un&#39;incorporazione, ovvero una rappresentazione matematica del contenuto, quindi mette in correlazione tali incorporazioni con le prestazioni dei trattamenti. Questo processo consente l’estrazione degli attributi del contenuto con prestazioni migliori per utilizzi futuri. Tali attributi vengono quindi inseriti in un modello di linguaggio di grandi dimensioni ospitato da Adobe, che li converte in istruzioni leggibili dall’utente utilizzate per generare informazioni approfondite e suggerire opportunità.

## Quali restrizioni ha Experimentation Accelerator sui dati utilizzati?

Ogni cliente viene assegnato a un’organizzazione e a una sandbox specifiche. Per ogni sandbox viene addestrato un modello dedicato. Quando si elimina una sandbox, tutti i dati, i segnali e i modelli correlati vengono rimossi definitivamente.

* Utilizziamo solo i dati dei clienti per addestrare o perfezionare il modello da quel cliente.

* Non uniamo mai i clienti per addestrare o perfezionare un modello.

## I modelli Adobe o l’intelligenza artificiale cambieranno automaticamente l’esperienza utente di un brand?

No. **Experimentation Accelerator** fornisce solo consigli su cosa può essere modificato e come può essere modificato. Solo gli utenti che dispongono delle autorizzazioni per modificare l’esperienza utilizzando Journey Optimizer o Target potranno agire in base a questi consigli. Tutti i consigli possono essere rivisti e modificati prima di essere esclusi.

## Esiste un rischio per la stabilità dei dati o del sistema?

**Experimentation Accelerator** acquisisce e analizza solo i dati, producendo insight e consigli per test futuri. Non dispone dell’accesso per modificare le impostazioni di test. Tutti i suggerimenti generati all’interno dello strumento vengono inviati a Target e Journey Optimizer per l’implementazione, garantendo nessun impatto sulle attività correnti del cliente.
