---
solution: Journey Optimizer
product: journey optimizer
title: Migra tipi di pubblico in batch da percorsi di qualificazione del pubblico
description: Scopri come eseguire la migrazione di percorsi che utilizzano tipi di pubblico in batch in un nodo di qualificazione del pubblico prima della data di applicazione di agosto 2026.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: qualificazione del pubblico, pubblico in batch, deprecazione, migrazione, pubblico di lettura, pubblico in streaming
exl-id: f3c2a7d1-b58e-4a92-c3d5-0e871f2a9b4c
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: cea41add5b86adb3b447ce606e73248adce0f731
workflow-type: tm+mt
source-wordcount: 869
ht-degree: 0%

---


# Migra tipi di pubblico in batch da percorsi di qualificazione del pubblico {#aq-batch-migration}

A partire da agosto 2026, Journey Optimizer bloccherà la pubblicazione per i percorsi che utilizzano un pubblico batch in un nodo di qualificazione del pubblico. Identifica il tuo caso d’uso e segui il percorso di migrazione consigliato.

>[!CAUTION]
>
>**Data di applicazione: agosto 2026.** I percorsi nuovi, in bozza e duplicati che utilizzano un pubblico batch in un nodo di qualificazione del pubblico non possono essere pubblicati dopo questa data. Un avviso di convalida è già stato visualizzato nell’area di lavoro del percorso a partire dalla versione di giugno 2026.

## Perché questo cambiamento {#why}

Il nodo **[Qualificazione del pubblico](audience-qualification-events.md)** è progettato per reagire quasi in tempo reale quando i singoli profili entrano o escono da un pubblico; gli eventi di qualificazione arrivano continuamente, uno per uno. È destinato a **[tipi di pubblico in streaming](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)**.

Quando invece si utilizza un pubblico batch con un nodo di qualificazione del pubblico, tutti gli eventi di qualificazione arrivano simultaneamente durante la finestra di acquisizione. Questo può attivare decine di migliaia o milioni di ingressi di percorsi nello stesso momento, causando gravi sollecitazioni e comportamenti imprevedibili nei sistemi a valle. Questa non è la progettazione prevista del nodo Audience Qualification.

L&#39;attività **[Read Audience](read-audience.md)** è lo strumento giusto per i casi d&#39;uso basati su batch: è stata creata per gestire l&#39;elaborazione pianificata in blocco in modo controllato e prevedibile.

## Effetti sui percorsi {#impact}

Un percorso live che utilizza un pubblico batch in un nodo di qualificazione del pubblico continua a essere eseguito dopo agosto 2026. Tuttavia, se interrompi, duplichi o ripubblichi il percorso, questo verrà bloccato fino a quando la configurazione non viene aggiornata.


| Stato del percorso | Impatto dopo agosto 2026 |
| --- | --- |
| **percorsi attivi** | Nessun impatto. I percorsi live esistenti continuano a essere eseguiti. Nessun arresto automatico. |
| **Nuovi percorsi** | Bloccato dalla pubblicazione fino alla sostituzione del pubblico batch. |
| **percorsi bozza** | Bloccato dalla pubblicazione fino alla sostituzione del pubblico batch. |
| **percorsi duplicati** | Bloccato dalla pubblicazione fino alla sostituzione del pubblico batch. |


## Guida alla migrazione {#migration-paths}

Se utilizzi un pubblico batch in un nodo di qualificazione del pubblico, identifica il caso di utilizzo riportato di seguito e segui il percorso di migrazione consigliato.

### Caso d’uso 1: pubblico basato sugli eventi di tracciamento dei messaggi di AJO {#use-case-1}

**Aspetto:** il pubblico di qualificazione del pubblico utilizza condizioni basate su invii di e-mail, aperture o clic dai set di dati di tracciamento interni di Journey Optimizer, ad esempio *&quot;il profilo ha ricevuto un&#39;e-mail&quot;* o *&quot;il profilo ha aperto un&#39;e-mail.&quot;*

>[!NOTE]
>
>Da novembre 2024, la segmentazione in streaming non supporta più eventi di invio e apertura dai set di dati di tracciamento di Journey Optimizer. I tipi di pubblico basati su questi eventi ora vengono valutati in modalità batch. [Ulteriori informazioni sui metodi di valutazione del pubblico](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)

**Alternative consigliate:**

* **Reazione ad aperture o clic nello stesso percorso**. Utilizzare il nodo **[Evento reazione](reaction-events.md)**. È stato progettato per rispondere alle aperture e ai clic da un messaggio inviato nello stesso percorso, senza richiedere un pubblico separato. [Vedi un esempio end-to-end utilizzando gli eventi di reazione](journeys-uc.md#send-multi-channel-messages)

* **Targeting per clic su più percorsi** — Crea un [pubblico in streaming](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) dagli eventi di clic e utilizza il nodo Qualificazione pubblico con tale pubblico in streaming.

* **Eliminazione basata su mancato recapito**: utilizza l&#39;elenco di soppressione [&#x200B; nativo di Journey Optimizer](../configuration/manage-suppression-list.md) anziché modellare il comportamento di mancato recapito come condizione di pubblico.

* **Qualsiasi logica di invio/apertura rimanente** — Passa a un percorso di **[Read Audience](read-audience.md)** in un&#39;esecuzione pianificata per elaborare il pubblico batch in modo sicuro.


### Caso d’uso 2: Percorso in attesa di nuovi dati di segmentazione batch {#use-case-2}

**Aspetto:** Pianifica l&#39;esecuzione di un percorso dopo un processo di segmentazione giornaliero e utilizza un nodo di qualificazione del pubblico per garantire che il percorso venga attivato solo quando sono disponibili i dati più recenti del pubblico.

**Alternativa consigliata:**

Utilizza un percorso **[Read Audience](read-audience.md)** con l&#39;opzione **[!UICONTROL Trigger dopo valutazione del pubblico in batch]** abilitata. Questa funzione incorporata mantiene l’esecuzione del percorso fino al completamento del processo di segmentazione, quindi inizia immediatamente quando sono disponibili nuovi dati, senza richiedere un nodo di qualificazione del pubblico. [Scopri come configurare questa opzione](read-audience.md#schedule)


### Caso d’uso 3: attivazione di un pubblico batch periodico di grandi dimensioni {#use-case-3}

**Aspetto:** attivi o aggiorni periodicamente un pubblico di grandi dimensioni (potenzialmente milioni di profili) e il percorso di qualificazione del pubblico viene attivato per tutti i profili appena qualificati contemporaneamente.

**Alternativa consigliata:**

Utilizza un percorso **[Read Audience](read-audience.md)**. È stato progettato appositamente per elaborare pubblici di grandi dimensioni in blocco, gestire profili in batch controllati e fornire un’esecuzione del percorso più prevedibile e affidabile su larga scala. [Vedi un esempio end-to-end](message-to-subscribers-uc.md)

## Cosa succede se nessuna delle alternative funziona per il tuo caso d’uso? {#exceptions}

Se il caso d’uso non può essere risolto utilizzando uno dei percorsi di migrazione indicati sopra, contatta il rappresentante Adobe. I casi che non possono essere risolti con alternative esistenti saranno esaminati singolarmente.

## Risorse correlate {#related}

* [Eventi di qualificazione del pubblico](audience-qualification-events.md) — guida alla configurazione completa e guardrail
* [Attività Read Audience](read-audience.md): come configurare una voce di pubblico batch pianificata
* [Eventi di reazione](reaction-events.md): come reagire ad aperture e clic all&#39;interno dello stesso percorso
* [Metodi di valutazione del pubblico](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) — spiegazione di batch, streaming e segmentazione Edge
* [Informazioni sui tipi di pubblico](../audience/about-audiences.md): tipi di pubblico e modalità di creazione in Journey Optimizer
* [Gestire l&#39;elenco di soppressione](../configuration/manage-suppression-list.md): come accedere e configurare l&#39;eliminazione dei messaggi non recapitati
* [Guardrail e limitazioni del percorso](limitations.md)
* [Criteri di entrata e di uscita dal Percorso](entry-exit-criteria-guide.md): confronto tra modelli di ingresso in tempo reale e batch con esempi reali
* [Invio di messaggi multicanale](journeys-uc.md#send-multi-channel-messages): caso d&#39;uso end-to-end che combina attività Read Audience, eventi di reazione, e-mail e push
* [Invia un messaggio ai sottoscrittori](message-to-subscribers-uc.md) — caso d&#39;uso end-to-end per l&#39;attivazione in blocco del pubblico con Read Audience
