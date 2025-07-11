---
solution: Journey Optimizer
product: journey optimizer
title: Avviare e monitorare campagne orchestrate con Adobe Journey Optimizer
description: Scopri come avviare e monitorare le campagne orchestrate con Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: b1bee7a5ee05e0e535a982c31bafafdc760d21ae
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 1%

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

**[!UICONTROL Campagna orchestrata]** fornisce due origini dati principali per questo:

* **[!UICONTROL Feedback messaggio]**: acquisisce eventi relativi alla consegna, ad esempio messaggi inviati, aperti, non recapitati e così via.
* **[!UICONTROL Tracciamento e-mail]**: acquisisce le azioni dell&#39;utente, ad esempio clic e aperture.

## Creare una regola di retargeting basata sul feedback {#feedback-retarget}

La regola di retargeting basata sul feedback consente di eseguire il retargeting dei destinatari in base agli eventi di consegna dei messaggi acquisiti nel set di dati **Feedback messaggio**. Questi eventi includono risultati quali messaggi inviati, aperti, non recapitati o contrassegnati come spam.

Utilizzando questi dati, puoi definire regole per identificare i destinatari che hanno ricevuto un messaggio precedente, abilitando la comunicazione di follow-up in base a stati di consegna specifici.

1. Crea una nuova **[!UICONTROL campagna orchestrata]**.

1. Aggiungi un&#39;attività **[!UICONTROL Genera pubblico]** e imposta la dimensione di targeting su **[!UICONTROL Destinatario (caas)]**.

1. Nel **[!UICONTROL Generatore regole]**, fai clic su **[!UICONTROL Aggiungi condizione]** e seleziona **[!UICONTROL Feedback messaggio]** dal **[!UICONTROL Selettore attributi]**. Fai clic su **[!UICONTROL Conferma]** per creare **Il feedback del messaggio esiste, ad esempio** condizione.

   ![](assets/retarget_1.png)

1. Scegli l&#39;attributo **[!UICONTROL Stato feedback]** per eseguire il targeting degli eventi di consegna dei messaggi.

+++ Dettagliato passo dopo passo

   1. Aggiungi un&#39;altra condizione collegata all&#39;attributo **[!UICONTROL Feedback messaggio]**.

   1. Cerca l&#39;attributo **[!UICONTROL Stato feedback]** e fai clic su **[!UICONTROL Conferma]**.

      ![](assets/retarget_3.png)

   1. Nel menu **[!UICONTROL Condizione personalizzata]**, scegli lo stato di consegna da tracciare nel menu a discesa **[!UICONTROL Valore]**.

      ![](assets/retarget_4.png)

+++

1. Scegli l&#39;attributo **[!UICONTROL Nome campagna orchestrata]** per eseguire il targeting di una campagna orchestrata specifica.

+++ Dettagliato passo dopo passo

   1. Aggiungi un&#39;altra condizione collegata all&#39;attributo **[!UICONTROL Feedback messaggio]**, cerca **[!UICONTROL entità]** e passa a:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Seleziona **[!UICONTROL Nome campagna orchestrata]**.

      ![](assets/retarget_5.png)

   1. Nel menu **[!UICONTROL Condizione personalizzata]**, specifica il nome della campagna nel campo **[!UICONTROL Valore]**.

+++

1. Scegli l&#39;attributo **[!UICONTROL Nome azione campagna orchestrata]** per eseguire il targeting di un messaggio o un&#39;attività specifica all&#39;interno di una campagna orchestrata.

+++ Dettagliato passo dopo passo

   1. Aggiungi un&#39;altra condizione collegata all&#39;attributo **[!UICONTROL Feedback messaggio]**, cerca **[!UICONTROL entità]** e passa a:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Selezionare **[!UICONTROL Nome azione campagna orchestrata]**.

      ![](assets/retarget_6.png)

   1. Nel menu **[!UICONTROL Condizione personalizzata]**, specifica il nome dell&#39;azione della campagna nel campo **[!UICONTROL Valore]**.

      Per trovare i nomi delle azioni, fai clic sull&#39;icona ![Informazioni](assets/do-not-localize/info-icon.svg) accanto a un&#39;attività nell&#39;area di lavoro.

   ++

1. In alternativa, puoi anche filtrare in base al **[!UICONTROL ID campagna]** (UUID), che si trova nelle proprietà della campagna.

## Creare una regola di retargeting basata sul tracciamento

La regola di retargeting basata sul tracciamento esegue il targeting dei destinatari in base alle loro interazioni con un messaggio, utilizzando i dati del set di dati **[!UICONTROL Tracciamento e-mail]**. Acquisisce le azioni dell’utente, ad esempio le aperture delle e-mail e i clic sui collegamenti.

Per eseguire il retargeting dei destinatari in base alle interazioni con i messaggi (ad esempio, apri o fai clic su di essi), utilizza l&#39;entità **[!UICONTROL Tracciamento e-mail]** come segue:

1. Crea una nuova **[!UICONTROL campagna orchestrata]**.

1. Aggiungi un&#39;attività **[!UICONTROL Genera pubblico]** e imposta la dimensione di targeting su **[!UICONTROL Destinatario (caas)]** per concentrarsi sui destinatari della campagna orchestrata precedente.

1. Nel **[!UICONTROL Generatore regole]**, fai clic su **[!UICONTROL Aggiungi condizione]** e seleziona **[!UICONTROL Verifica e-mail]** dal **[!UICONTROL Selettore attributi]**.

   Fai clic su **[!UICONTROL Conferma]** per creare **Verifica e-mail esistente come** condizione.

   ![](assets/retarget_2.png)

1. Per eseguire il targeting delle interazioni dei profili con un messaggio, aggiungi un&#39;altra condizione collegata all&#39;attributo **[!UICONTROL Tracciamento e-mail]** e cerca l&#39;attributo **[!UICONTROL Tipo di interazione]**.

   ![](assets/retarget_7.png)

1. Dalle opzioni di condizione personalizzate, utilizza **[!UICONTROL Incluso in]** come operatore e seleziona uno o più valori a seconda del caso d&#39;uso, ad esempio **[!UICONTROL Messaggio aperto]** o **[!UICONTROL Messaggio link fatto clic]**.

   ![](assets/retarget_8.png)

1. Per associare i dati di tracciamento a una campagna specifica, aggiungi una nuova condizione **[!UICONTROL Feedback messaggio]** e segui i passaggi descritti [in questa sezione](#feedback-retarget).
