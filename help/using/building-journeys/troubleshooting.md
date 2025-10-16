---
solution: Journey Optimizer
product: journey optimizer
title: Risolvere i problemi prima di testare o pubblicare il percorso
description: Scopri come risolvere gli errori prima di testare o pubblicare il percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: risoluzione dei problemi, risoluzione dei problemi, percorso, controllo, errori
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
version: Journey Orchestration
source-git-commit: 118bf89f56d26213fde71fa795fc6576ce764ef2
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 40%

---

# Risolvere i problemi prima di testare il percorso {#troubleshooting}

In questa sezione, scopri come risolvere i problemi dei percorsi prima di eseguire test o pubblicare. Tutti i controlli elencati di seguito possono essere effettuati quando il percorso è in modalità di test o quando è live. Ti consigliamo di eseguire tutti i controlli riportati di seguito in modalità di test, quindi di procedere alla pubblicazione. Ulteriori informazioni sulla modalità di test in [questa pagina](../building-journeys/testing-the-journey.md).

Scopri come risolvere i problemi relativi agli eventi di percorso, verificare se i profili sono entrati nel percorso, come si spostano e se i messaggi vengono inviati [in questa pagina](troubleshooting-execution.md).

Se utilizzi azioni in entrata, scopri come risolverle [in questa pagina](troubleshooting-inbound.md).

## Errori nelle attività {#activity-errors}

Prima di testare e pubblicare il percorso, controlla che tutte le attività siano state configurate correttamente. Non è possibile eseguire test o pubblicazioni se il sistema rileva ancora degli errori.

Gli errori vengono visualizzati con un simbolo di avviso visualizzato sulle attività stesse all’interno dell’area di lavoro. Per visualizzare il messaggio di errore, posiziona il cursore sul punto esclamativo. Se selezioni l’attività, la riga dovrebbe essere visualizzata in errore con un avviso. Ad esempio:

* se un campo obbligatorio è vuoto, viene visualizzato un errore

  ![](assets/journey63.png)

* quando due attività vengono disconnesse, nell’area di lavoro viene visualizzato un avviso

  ![](assets/canvas-disconnected.png)

## Errori nel percorso {#canvas-errors}

Gli errori sono visibili anche dal pulsante **[!UICONTROL Avvisi]**, sopra l&#39;area di lavoro. Questo pulsante consente di visualizzare gli errori rilevati dal percorso che impediscono l&#39;attivazione della modalità di test o la pubblicazione.

Il sistema rileva due tipi di problemi: **errori** e **avvisi**. Gli errori bloccano la pubblicazione e l’attivazione di test. Gli avvisi indicano i potenziali problemi che non impediscono l’attivazione del test o la pubblicazione. Vedrai una descrizione del problema e un ID di registro del problema del tipo ERR_XXX_XXX. Questo può aiutare a identificare il problema.

![](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

Gli errori e gli avvisi globali relativi al percorso vengono visualizzati per primi nell’elenco. Gli errori e gli avvisi relativi ad attività specifiche sono elencati successivamente per ordine di attività o per visualizzazione nel percorso da sinistra a destra. Nella parte inferiore dell&#39;elenco degli avvisi, il pulsante **[!UICONTROL Copia dettagli]** consente di copiare le informazioni tecniche sul percorso utili per la risoluzione dei problemi.

## Aggiungi un percorso alternativo {#canvas-add-path}

È possibile definire un&#39;azione di fallback in caso di errore per le seguenti attività di percorso: **[!UICONTROL Ottimizza]** e **[!UICONTROL Azione]**.

Quando si verifica un errore in un’azione o in una condizione, il percorso di un singolo utente si interrompe. L&#39;unico modo per farlo continuare è risolvere il problema. Per evitare di interrompere il percorso, puoi anche selezionare l&#39;opzione **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o errore]** nelle proprietà dell&#39;attività. Ulteriori informazioni in [questa sezione](../building-journeys/using-the-journey-designer.md#paths).
