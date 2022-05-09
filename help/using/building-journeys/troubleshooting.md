---
title: Risoluzione dei problemi del percorso
description: Scopri come risolvere gli errori nei percorsi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 81%

---

# Risolvere i problemi del percorso{#troubleshooting}

In questa sezione viene descritto come risolvere i problemi dei percorsi prima di eseguire i test o di pubblicare. Tutti i controlli elencati di seguito possono essere effettuati quando il percorso è in modalità di test o quando è live. Ti consigliamo di eseguire tutti i controlli riportati di seguito in modalità di test, quindi di procedere alla pubblicazione. Consulta [questa pagina](../building-journeys/testing-the-journey.md).

## Verifica gli errori prima del test{#checking-for-errors-before-testing}

Prima di testare e pubblicare il percorso, controlla che tutte le attività siano state configurate correttamente. Non è possibile eseguire test o pubblicazioni se il sistema rileva ancora degli errori.

Gli errori vengono visualizzati con un simbolo di avviso visualizzato sulle attività stesse all’interno dell’area di lavoro. Per visualizzare il messaggio di errore, posiziona il cursore sul punto esclamativo. Se fai clic sull’attività, la riga dovrebbe essere visualizzata in errore con un avviso. Ad esempio, se un campo obbligatorio è vuoto, viene visualizzato un errore.

![](assets/journey63.png)

Ad esempio, nell’area di lavoro, quando due attività sono disconnesse, viene visualizzato un avviso.

![](assets/canvas-disconnected.png)

Accanto all’interruttore **[!UICONTROL Test]** e al pulsante **[!UICONTROL Publish]**, è possibile visualizzare un segnale di avviso. Questo segnale di avviso riporta gli errori rilevati dal sistema e impedisce l’attivazione della modalità di test o la pubblicazione del percorso. Nella maggior parte dei casi, gli errori rilevati dal sistema sono collegati a errori visibili sulle attività, ma a volte sono collegati ad altri problemi. In questo caso, puoi visualizzare gli errori e cercare di identificare il problema utilizzando la relativa descrizione. Se non riesci a identificare il problema, puoi copiare i dettagli e inviarli all’amministratore o al supporto tecnico. Gli errori che bloccano il test e quelli che impediscono la pubblicazione sono simili.

Il sistema rileva due tipi di problemi: errori e avvisi. Gli errori bloccano la pubblicazione e l’attivazione di test. Gli avvisi indicano i potenziali problemi che non impediscono l’attivazione del test o la pubblicazione. Vedrai una descrizione del problema e un ID di registro del problema del tipo ERR_XXX_XXX. Questo aiuterà il supporto tecnico a identificare il problema.

Sul segno accanto all’interruttore **[!UICONTROL Test]** e al pulsante **[!UICONTROL Publish]** possono essere visualizzati due colori diversi. In caso di errori, il segno viene visualizzato in rosso. In caso di avvisi, viene visualizzato in arancione.

![](assets/journey75.png)

Gli errori e gli avvisi globali relativi al percorso vengono visualizzati per primi nell’elenco. Gli errori e gli avvisi relativi ad attività specifiche sono elencati successivamente per ordine di attività o per visualizzazione nel percorso da sinistra a destra. Il pulsante **[!UICONTROL Copy details]** consente di copiare le informazioni tecniche sul percorso che il team di supporto può utilizzare per la risoluzione dei problemi.

Quando si verifica un errore in un’azione o in una condizione, il percorso di un singolo utente si arresta. L’unico modo per far sì che continui è selezionare la casella **[!UICONTROL Add an alternative path in case of a timeout or an error]** (Aggiungi percorso alternativo in caso di errore o timeout). Vedi [questa sezione](../building-journeys/using-the-journey-designer.md#paths).

## Controlla che gli eventi siano inviati correttamente{#checking-that-events-are-properly-sent}

Il punto di partenza di un percorso è sempre un evento. Puoi eseguire i test utilizzando strumenti come Postman.

Puoi verificare se la chiamata API inviata tramite questi strumenti viene inviata correttamente o meno. Se ricevi nuovamente un errore, significa che la chiamata presenta un problema. Controlla di nuovo il payload, l’intestazione (e in particolare l’ID organizzazione) e l’URL di destinazione. Puoi chiedere all’amministratore qual è l’URL corretto da utilizzare.

Gli eventi non vengono inviati direttamente dall’origine ai percorsi. In effetti, i percorsi si basano sulle API Streaming Ingestion di Adobe Experience Platform. Di conseguenza, in caso di problemi relativi agli eventi, puoi fare riferimento a [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;} per la risoluzione dei problemi relativi alle API Streaming Ingestion.

## Controlla se le persone entrano nel percorso{#checking-if-people-enter-the-journey}

Il reporting di percorso misura le entrate delle persone in un percorso in tempo reale.

Se l’invio dell’evento è stato completato con successo ma non viene visualizzato alcuna entrata nel percorso, significa che si sono verificati errori tra l’invio dell’evento e la ricezione dell’evento nel percorso.

Di seguito sono riportati alcuni elementi che l’amministratore deve controllare:

* Hai la certezza che il percorso in cui prevedevi che arrivasse l’evento fosse in modalità di test o live?
* Hai salvato l’evento prima di copiare il payload dall’anteprima del payload?
* Il payload dell’evento contiene un ID evento?
* Hai raggiunto l’URL giusto?
* Hai seguito la struttura del payload delle API di Streaming Ingestion utilizzando l’anteprima della struttura del payload nel riquadro di configurazione dell’evento? Consulta [questa pagina](../event/about-creating.md#preview-the-payload).
* Hai usato le coppie chiave-valore corrette nell&#39;intestazione dell&#39;evento?

   ```
   X-gw-ims-org-id - your organization's ID
   Content-type - application/json
   ```

## Controllare come le persone navigano nel percorso{#checking-how-people-navigate-through-the-journey}

La segnalazione dei percorsi misura i progressi delle persone all&#39;interno di un percorso. È facile identificare in che punto una persona si è fermata e per quale motivo.

Di seguito sono riportati alcuni elementi da verificare:

* È dovuto a una condizione che esclude la persona? Ad esempio, la condizione è “gender = male” e la persona in oggetto è una donna. Questo controllo può essere eseguito da un utente aziendale, se la condizione non è troppo complessa.
* È dovuto a una chiamata a un’origine dati che non risponde? Quando il percorso è in modalità di test, queste informazioni possono essere visualizzate nei registri in modalità di test. Quando il percorso è live, un amministratore può testare le chiamate dirette all’origine dati e verificare la risposta ricevuta. Un amministratore può anche duplicare il percorso e testarlo.

## Verificare che i messaggi siano stati inviati correttamente{#checking-that-messages-are-sent-successfully}

Se gli individui si spostano nel modo giusto durante il percorso ma non ricevono i messaggi che dovrebbero ricevere, puoi verificare se:

* [!DNL Journey Optimizer] ha tenuto correttamente conto della richiesta di invio del messaggio. Gli utenti aziendali possono accedere al messaggio che si suppone venga inviato e verificare se l’ora dell’esecuzione più recente corrisponde al tempo di esecuzione del percorso. Inoltre, possono controllare le chiamate/eventi API più recenti ricevuti.
* [!DNL Journey Optimizer] invio del messaggio completato. Nei registri di invio del messaggio, puoi visualizzare lo stato di ogni esecuzione. Puoi vedere se è verde, rosso e qual era il problema. Un utente aziendale può accedere a questa schermata e inviare i registri a un amministratore per ulteriori indagini.

Nel caso di un messaggio inviato tramite un’azione personalizzata, l’unica cosa che è possibile controllare durante il test del percorso è il fatto che la chiamata del sistema dell’azione personalizzata conduca o meno a un errore. Se la chiamata al sistema esterno che è associata all’azione personalizzata non genera un errore ma non provoca l’invio di un messaggio, è necessario effettuare alcune indagini sul lato del sistema esterno.
