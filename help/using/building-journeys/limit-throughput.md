---
solution: Journey Optimizer
title: Limite di trasmissione con origini dati esterne e azioni personalizzate
description: Limite di trasmissione con origini dati esterne e azioni personalizzate
feature: Journeys
topic: Content Management
role: User, Developer
level: Experienced
keywords: percorso, origini dati, limite, throughput, personalizzato, azioni
exl-id: 45d6bb82-88ea-4510-a023-a75a82cc6f7b
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 3%

---

# Caso di utilizzo: limitare il throughput con origini dati esterne e azioni personalizzate{#limit-throughput}

## Descrizione del caso d’uso

Adobe Journey Optimizer consente ai professionisti di inviare chiamate API a sistemi esterni tramite azioni personalizzate e origini dati.

Questa operazione può essere eseguita con :

* **Origini dati**: per raccogliere informazioni da sistemi esterni e utilizzarle nel contesto del percorso, ad esempio per ottenere informazioni meteo sulla città del profilo e disporre di un flusso percorso dedicato basato su questo.

* **Azioni personalizzate**: per inviare informazioni a sistemi esterni, ad esempio per inviare e-mail tramite una soluzione esterna utilizzando le funzionalità di orchestrazione di Journey Optimizer insieme alle informazioni sul profilo, ai dati sul pubblico e al contesto del percorso.

Se lavori con origini dati esterne o azioni personalizzate, puoi proteggere i sistemi esterni limitando il throughput di percorso: fino a 5000 istanze/secondo per percorsi unitari e fino a 20000 istanze/secondo per quelli attivati dai segmenti.

Per le azioni personalizzate, le funzionalità di limitazione sono disponibili a livello di prodotto. Fai riferimento a questo [page](../configuration/external-systems.md#capping).

Per le origini dati esterne, puoi definire un limite di limitazione a livello di endpoint per evitare di sovrapporre tali sistemi esterni tramite le API di Journey Optimizer Capping. Tuttavia, tutte le richieste rimanenti dopo il raggiungimento del limite verranno eliminate. In questa sezione sono disponibili soluzioni alternative che consentono di ottimizzare il throughput.

Per ulteriori informazioni su come integrare con i sistemi esterni, consulta questo [page](../configuration/external-systems.md).

## Implementazione

Per **percorsi con attivazione segmento**, puoi definire la velocità di limitazione dell’attività Leggi segmento che influirà sul throughput del percorso.  [Ulteriori informazioni](../building-journeys/read-segment.md)

![](assets/limit-throughput-1.png)

Puoi modificare questo valore da 500 a 20 000 istanze al secondo. Se devi scendere al di sotto di 500/s, puoi anche aggiungere condizioni di &quot;suddivisione percentuale&quot; con attività di attesa per dividere il percorso in più rami e farli eseguire in un momento specifico.

![](assets/limit-throughput-2.png)

Prendiamo un esempio di **percorsi con attivazione segmento** con una popolazione di **10.000 profili** e l&#39;invio di dati a un sistema esterno di supporto **100 richieste/secondo**.

1. Puoi definire il segmento di lettura per leggere i profili con un throughput di 500 profili/secondo, il che significa che la lettura di tutti i profili richiederà 20 secondi. Al secondo 1, ne leggerete 500, al secondo 2 500, ecc.

1. Puoi quindi aggiungere un’attività Condizione con suddivisione in percentuale con una suddivisione del 20% per avere a ogni secondo 100 profili in ciascun ramo.

1. In seguito, aggiungi le attività Attendi con un timer specifico in ogni ramo. Qui abbiamo impostato un&#39;attesa di 30 secondi per ognuna di esse. Al secondo, 100 profili fluiranno in ciascun ramo.

   * Al ramo 1, attenderanno 30 secondi, il che significa che:
      * al secondo 1, 100 profili attendono il secondo 31
      * al secondo 2, 100 profili attendono il secondo 32, ecc.
   * Al ramo 2, attenderanno 60 secondi, il che significa che:
      * Al secondo 1, 100 profili attendono il secondo 61 (1&#39;01&#39;&#39;)
      * Al secondo 2, 100 profili attendono il secondo 62 (1&#39;02&#39;), ecc.
   * Sapendo che ci aspettiamo un massimo di 20 secondi per leggere tutti i profili, non ci sarà sovrapposizione tra ciascun ramo, il secondo 20 è l’ultimo in cui i profili fluiranno nella condizione. Tra il secondo 31 e il secondo 51, tutti i profili nel ramo 1 saranno elaborati. Tra il secondo 61 (1&#39;01&#39;) e il secondo 81 (1&#39;21&#39;&#39;), tutti i profili nel ramo 2 saranno elaborati, ecc.

   * Come guardrail, puoi anche aggiungere un sesto ramo per avere meno di 100 profili per ramo, soprattutto se il sistema esterno supporta solo 100 richieste/secondo.



>[!IMPORTANT]
>
>Come per qualsiasi soluzione alternativa, sottoponete a test accuratamente la soluzione prima di entrare in produzione per verificare che faccia quello che volete.

Come ulteriore guardrail, è anche possibile utilizzare le funzionalità di maschiatura.

>[!NOTE]
>
>A differenza delle funzionalità di maschiatura, che proteggono un endpoint essendo globale per tutti i percorsi di una sandbox, questa soluzione funziona solo a livello di percorso. Ciò significa che se più percorsi sono in esecuzione in parallelo e hanno lo stesso endpoint, sarà necessario tenerne conto durante la progettazione del percorso. Questa soluzione non è quindi adatta per ogni caso d’uso.
