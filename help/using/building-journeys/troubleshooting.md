---
solution: Journey Optimizer
product: journey optimizer
title: Risoluzione dei problemi del percorso
description: Scopri come risolvere gli errori nei percorsi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---

# Risolvere i problemi del percorso{#troubleshooting}

In questa sezione viene descritto come risolvere i problemi dei percorsi prima di eseguire test o pubblicare. Tutti i controlli elencati di seguito possono essere eseguiti quando il percorso è in modalità di test o quando il percorso è live. Si consiglia di eseguire tutti i controlli riportati di seguito in modalità di test e quindi procedere alla pubblicazione. Vedi [questa pagina](../building-journeys/testing-the-journey.md).

## Verifica gli errori prima del test{#checking-for-errors-before-testing}

Prima di testare e pubblicare il percorso, verifica che tutte le attività siano configurate correttamente. Non è possibile eseguire test o pubblicazioni se il sistema rileva ancora errori.

Gli errori vengono visualizzati con un simbolo di avviso visualizzato sulle attività stesse nell’area di lavoro. Posiziona il cursore sul punto esclamativo per visualizzare il messaggio di errore. Se fai clic sull’attività, dovresti visualizzare la riga in errore con un avviso. Ad esempio, se un campo obbligatorio è vuoto, viene visualizzato un errore.

![](assets/journey63.png)

Ad esempio, nell’area di lavoro, quando due attività sono disconnesse, viene visualizzato un avviso.

![](assets/canvas-disconnected.png)

Accanto al **[!UICONTROL Test]** e **[!UICONTROL Publish]** è possibile visualizzare un segnale di avviso. Questo segnale di avviso visualizza gli errori rilevati dal sistema e impedisce l’attivazione della modalità di test o la pubblicazione del percorso. Nella maggior parte dei casi, gli errori rilevati dal sistema sono collegati a errori visibili sulle attività, ma a volte sono collegati ad altri problemi. In questo caso, puoi visualizzarli, cercare di identificare il problema utilizzando la descrizione dell’errore. Se non riesci a identificare il problema, puoi copiare i dettagli e inviarli all’amministratore o al supporto. Gli errori che bloccano il test e quelli che impediscono la pubblicazione sono simili.

Il sistema rileva due tipi di problemi: errori e avvisi. Gli errori bloccano la pubblicazione e l’attivazione di test. Gli avvisi indicano potenziali problemi che non impediscono l’attivazione o la pubblicazione dei test. Vedrai una descrizione del problema e un ID di registro del problema del tipo ERR_XXX_XXX. Questo aiuterà il supporto tecnico a identificare il problema.

Sul segno accanto al **[!UICONTROL Test]** e **[!UICONTROL Publish]** pulsante . Il segno viene visualizzato in rosso in caso di errori. In caso di avvisi, viene visualizzato in arancione.

![](assets/journey75.png)

Gli errori e gli avvisi globali relativi al percorso vengono visualizzati per primi nell’elenco. Gli errori e gli avvisi relativi ad attività specifiche sono elencati dopo, per ordine di attività o per aspetto nel percorso da sinistra a destra. La **[!UICONTROL Copy details]** consente di copiare le informazioni tecniche sul percorso che il team di supporto può utilizzare per la risoluzione dei problemi.

Quando si verifica un errore in un’azione o in una condizione, il percorso di un singolo utente si arresta. L’unico modo per far sì che continui è selezionare la casella . **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Vedi [questa sezione](../building-journeys/using-the-journey-designer.md#paths).

## Controlla che gli eventi siano inviati correttamente{#checking-that-events-are-properly-sent}

Il punto di partenza di un percorso è sempre un evento. Puoi eseguire i test utilizzando strumenti come Postman.

Puoi verificare se la chiamata API inviata tramite questi strumenti viene inviata correttamente o meno. Se ricevi nuovamente un errore, significa che la chiamata presenta un problema. Controlla di nuovo il payload, l’intestazione (e in particolare l’ID organizzazione) e l’URL di destinazione. Puoi chiedere all’amministratore qual è l’URL corretto da utilizzare.

Gli eventi non vengono inviati direttamente dall’origine ai percorsi. In effetti, i percorsi si basano sulle API Streaming Ingestion di Adobe Experience Platform. Di conseguenza, in caso di problemi relativi agli eventi, puoi fare riferimento a [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;} per la risoluzione dei problemi relativi alle API Streaming Ingestion.

## Controlla se le persone accedono al percorso{#checking-if-people-enter-the-journey}

Il rapporto sul percorso misura le entrate delle persone in un percorso in tempo reale.

Se l’invio dell’evento è riuscito ma non viene visualizzato alcun ingresso nel percorso, significa che si è verificato un errore tra l’invio dell’evento e la ricezione dell’evento nel percorso.

Di seguito sono riportati alcuni elementi che l’amministratore deve controllare:

* Sei sicuro che il percorso in cui prevedevi che l’evento in arrivo sia in modalità di test o live?
* Hai salvato l’evento prima di copiare il payload dall’anteprima del payload?
* Il payload dell’evento contiene un ID evento?
* Hai raggiunto l&#39;URL giusto?
* Hai seguito la struttura del payload delle API di Streaming Ingestion utilizzando l’anteprima della struttura del payload nel riquadro di configurazione dell’evento? Vedi [questa pagina](../event/about-creating.md#preview-the-payload).
* Hai usato le coppie chiave-valore corrette nell&#39;intestazione dell&#39;evento?

   ```
   X-gw-ims-org-id - your organization's ID
   Content-type - application/json
   ```

## Controllare come le persone navigano nel percorso{#checking-how-people-navigate-through-the-journey}

Il rapporto sul percorso misura il progresso delle persone all’interno di un percorso. È facile identificare dove e perché una persona si è fermata.

Di seguito sono riportati alcuni elementi da controllare:

* È dovuto a una condizione che esclude la persona? Ad esempio, la condizione è &quot;gender = male&quot; e la persona è una donna. Questo controllo può essere eseguito da un utente aziendale se la condizione non è troppo complessa.
* È dovuto a una chiamata a un’origine dati che non risponde? Quando il percorso è in fase di test, queste informazioni possono essere visualizzate nei registri in modalità di test. Quando il percorso è attivo, un amministratore può testare le chiamate dirette all’origine dati e controllare la risposta ricevuta. Un amministratore può anche duplicare il percorso e testarlo.

## Verificare che i messaggi siano stati inviati correttamente{#checking-that-messages-are-sent-successfully}

Se gli individui scorrono nel modo giusto nel percorso ma non ricevono i messaggi che dovrebbero ricevere, puoi verificare se:

* [!DNL Journey Optimizer] ha tenuto correttamente conto della richiesta di invio del messaggio. Gli utenti aziendali possono accedere al messaggio che si presume venga inviato e verificare se l’ora dell’esecuzione più recente corrisponde al tempo di esecuzione del percorso. Inoltre, possono controllare le chiamate/eventi API più recenti ricevuti.
* [!DNL Journey Optimizer] invio del messaggio completato. Controlla il reporting del percorso per assicurarti che non ci siano errori.

Nel caso di un messaggio inviato tramite un’azione personalizzata, l’unica cosa che è possibile controllare durante il test del percorso è il fatto che la chiamata del sistema dell’azione personalizzata conduca o meno a un errore. Se la chiamata al sistema esterno associata all’azione personalizzata non genera un errore ma non provoca l’invio di un messaggio, è necessario effettuare alcune indagini sul lato del sistema esterno.
