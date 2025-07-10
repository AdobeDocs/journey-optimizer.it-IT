---
solution: Journey Optimizer
product: journey optimizer
title: Avviare e monitorare campagne orchestrate con Adobe Journey Optimizer
description: Scopri come avviare e monitorare le campagne orchestrate con Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 2%

---

# Creazione di query di retargeting {#retarget}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Accesso e gestione delle campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Crea e pianifica la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrazione attività](orchestrate-activities.md)<br/><br/>[Avvia e monitora la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/><b>[Retargeting](retarget.md)</b> | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

Documentazione in corso

>[!ENDSHADEBOX]

Il retargeting ti consente di monitorare i destinatari in base al modo in cui hanno risposto a una campagna orchestrata precedente. Ad esempio, puoi inviare una seconda e-mail ai profili che hanno ricevuto ma non hanno fatto clic sul primo.

A tal fine, la campagna orchestrata fornisce due origini dati principali:

- **Feedback messaggio**: acquisisce eventi relativi alla consegna, ad esempio messaggi inviati, aperti, non recapitati e così via.

- **Tracciamento e-mail**: acquisisce le azioni utente, ad esempio clic e aperture.

## Creare una regola di retargeting basata sul feedback

La regola di retargeting basata sul feedback consente di eseguire il retargeting dei destinatari in base agli eventi di consegna dei messaggi acquisiti nel set di dati **Feedback messaggio**. Questi eventi includono risultati quali messaggi inviati, aperti, non recapitati o contrassegnati come spam.

Utilizzando questi dati, puoi definire regole per identificare i destinatari che hanno ricevuto un messaggio precedente ma non vi si sono interessati, abilitando una comunicazione di follow-up basata su stati di consegna specifici.

1. Crea una nuova **campagna orchestrata**.

2. Aggiungi un&#39;attività **Genera pubblico** e imposta la dimensione di targeting su **Destinatario (caas)**.

3. Nel **Generatore regole**, fai clic su **Aggiungi condizione** e seleziona **Feedback messaggio** dal selettore attributi. Fai clic su **Conferma**.

4. Aggiungi una condizione per **Stato feedback** e imposta il valore su **Messaggio inviato**.

5. Per eseguire il targeting di una campagna orchestrata specifica:

   - Aggiungi un&#39;altra condizione, cerca `entity` e passa a:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Selezionare **Nome campagna orchestrata** e specificare il nome della campagna.

6. Per eseguire il targeting di un messaggio o un’attività specifica all’interno della campagna orchestrata:

   - Aggiungi un&#39;altra condizione, cerca `entity` e passa a:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Selezionare **Nome azione campagna orchestrata** e specificare il nome dell&#39;azione della campagna.

     Per trovare i nomi delle azioni, fai clic sull&#39;icona ![Informazioni](assets/do-not-localize/info-icon.svg) accanto a un&#39;attività nell&#39;area di lavoro.

   >[!TIP]
   >
   >Invece di utilizzare i nomi, puoi anche filtrare in base all&#39;**ID campagna** (UUID), che si trova nelle proprietà della campagna.

## Creare una regola di retargeting basata sul tracciamento

La regola di retargeting basata sul tracciamento esegue il targeting dei destinatari in base alle loro interazioni con un messaggio, utilizzando i dati del set di dati **Tracciamento e-mail**. Acquisisce le azioni dell’utente, ad esempio le aperture delle e-mail e i clic sui collegamenti.

Per eseguire il retargeting dei destinatari in base alle interazioni con i messaggi (ad esempio, apri o fai clic su di essi), utilizza l&#39;entità **Tracciamento e-mail** come segue:

1. Crea una nuova **campagna orchestrata**, quindi aggiungi un&#39;attività **Crea pubblico** con **Destinatario (caas)** come dimensione di targeting per concentrarsi sui destinatari della campagna orchestrata precedente.

1. Aggiungi una nuova condizione per **Tracciamento e-mail**. Fai clic su **Conferma** per creare una condizione &quot;Tracciamento e-mail esistente, ad esempio&quot;.

1. All&#39;interno di tale condizione, aggiungere una condizione e cercare l&#39;attributo **Interaction Type**.

1. Dalle opzioni di condizione personalizzata, utilizza **Incluso in** come operatore e seleziona uno o più valori a seconda del caso d&#39;uso. Ad esempio:
   - **Messaggio aperto**
   - **Collegamento messaggio selezionato**

1. Per associare i dati di tracciamento a una campagna specifica:

   - Aggiungi una condizione nel blocco di tracciamento e-mail.

   - Passa a `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Aggiungi condizioni sia per **Nome campagna orchestrata** che, se necessario, per **Nome azione campagna orchestrata**.

     Per trovare i nomi delle azioni, fai clic sull&#39;icona ![Informazioni](assets/do-not-localize/info-icon.svg) accanto a un&#39;attività nell&#39;area di lavoro.

   >[!TIP]
   >
   >Invece di utilizzare i nomi, puoi anche filtrare in base all&#39;**ID campagna** (UUID), che si trova nelle proprietà della campagna.
