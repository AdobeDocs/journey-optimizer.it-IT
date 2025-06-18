---
solution: Journey Optimizer
product: journey optimizer
title: Risoluzione dei problemi del percorso
description: Scopri come risolvere gli errori nei percorsi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: risoluzione dei problemi, risoluzione dei problemi, percorso, controllo, errori
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 44%

---

# Risolvere i problemi di un percorso {#troubleshooting}

In questa sezione, scopri come risolvere i problemi dei percorsi prima di eseguire test o pubblicare. Tutti i controlli elencati di seguito possono essere effettuati quando il percorso è in modalità di test o quando è live. Ti consigliamo di eseguire tutti i controlli riportati di seguito in modalità di test, quindi di procedere alla pubblicazione. Ulteriori informazioni sulla modalità di test in [questa pagina](../building-journeys/testing-the-journey.md).

In qualità di amministratore, puoi anche testare le configurazioni delle azioni personalizzate effettuando chiamate API reali direttamente dall’interfaccia utente. Ulteriori informazioni sono disponibili in [questa pagina](../action/troubleshoot-custom-action.md).

## Verifica la presenza di errori prima del test {#checking-for-errors-before-testing}

Prima di testare e pubblicare il percorso, controlla che tutte le attività siano state configurate correttamente. Non è possibile eseguire test o pubblicazioni se il sistema rileva ancora degli errori.


### Errori nelle attività {#activity-errors}

Gli errori vengono visualizzati con un simbolo di avviso visualizzato sulle attività stesse all’interno dell’area di lavoro. Per visualizzare il messaggio di errore, posiziona il cursore sul punto esclamativo. Se fai clic sull’attività, la riga dovrebbe essere visualizzata in errore con un avviso. Ad esempio:

* se un campo obbligatorio è vuoto, viene visualizzato un errore

  ![](assets/journey63.png)

* quando due attività vengono disconnesse, nell’area di lavoro viene visualizzato un avviso

  ![](assets/canvas-disconnected.png)

### Errori nel percorso {#canvas-errors}

Gli errori sono visibili anche dal pulsante **[!UICONTROL Avvisi]**, sopra l&#39;area di lavoro. Questo pulsante consente di visualizzare gli errori rilevati dal percorso che impediscono l&#39;attivazione della modalità di test o la pubblicazione.

Il sistema rileva due tipi di problemi: **errori** e **avvisi**. Gli errori bloccano la pubblicazione e l’attivazione di test. Gli avvisi indicano i potenziali problemi che non impediscono l’attivazione del test o la pubblicazione. Vedrai una descrizione del problema e un ID di registro del problema del tipo ERR_XXX_XXX. Questo può aiutare a identificare il problema.

![](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

Gli errori e gli avvisi globali relativi al percorso vengono visualizzati per primi nell’elenco. Gli errori e gli avvisi relativi ad attività specifiche sono elencati successivamente per ordine di attività o per visualizzazione nel percorso da sinistra a destra. Nella parte inferiore dell&#39;elenco degli avvisi, il pulsante **[!UICONTROL Copia dettagli]** consente di copiare le informazioni tecniche sul percorso utili per la risoluzione dei problemi.

### Aggiungi un percorso alternativo {#canvas-add-path}

È possibile definire un&#39;azione di fallback in caso di errore per le seguenti attività di percorso: **[!UICONTROL Condizione]** e **[!UICONTROL Azione]**.

Quando si verifica un errore in un’azione o in una condizione, il percorso di un singolo utente si arresta. L&#39;unico modo per farlo continuare è risolvere il problema. Per evitare di interrompere il percorso, puoi anche selezionare l&#39;opzione **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o errore]** nelle proprietà dell&#39;attività. Ulteriori informazioni in [questa sezione](../building-journeys/using-the-journey-designer.md#paths).


## Verifica che gli eventi siano inviati correttamente {#checking-that-events-are-properly-sent}

Il punto di partenza di un percorso è sempre un evento. Puoi eseguire i test utilizzando strumenti come Postman.

Puoi verificare se la chiamata API inviata tramite questi strumenti viene inviata correttamente o meno. Se ricevi nuovamente un errore, significa che la chiamata presenta un problema. Controlla di nuovo il payload, l’intestazione (e in particolare l’ID organizzazione) e l’URL di destinazione. Puoi chiedere all’amministratore qual è l’URL corretto da utilizzare.

Gli eventi non vengono inviati direttamente dall’origine ai percorsi. In effetti, i percorsi si basano sulle API Streaming Ingestion di Adobe Experience Platform. Di conseguenza, in caso di problemi relativi agli eventi, puoi fare riferimento alla [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} per la risoluzione dei problemi relativi alle API Streaming Ingestion.

Se il percorso non è in grado di abilitare la modalità di test con l&#39;errore `ERR_MODEL_RULES_16`, verificare che l&#39;evento utilizzato includa uno spazio dei nomi [identità](../audience/get-started-identity.md) quando si utilizza un&#39;azione del canale.

Lo spazio dei nomi dell’identità viene utilizzato per identificare in modo univoco i profili di test. Ad esempio, se per identificare i profili di test si utilizza l&#39;e-mail, deve essere selezionato lo spazio dei nomi dell&#39;identità **E-mail**. Se l&#39;identificatore univoco è il numero di telefono, deve essere selezionato lo spazio dei nomi dell&#39;identità **Telefono**.

## Controlla se le persone entrano nel percorso {#checking-if-people-enter-the-journey}

Il reporting percorso misura le entrate delle persone in un percorso in tempo reale.

Se l’invio dell’evento è stato completato con successo ma non viene visualizzata alcuna entrata nel percorso, significa che si sono verificati errori tra l’invio dell’evento e la ricezione dell’evento nel percorso.

Per iniziare la risoluzione dei problemi, consulta le domande seguenti:

* Hai la certezza che il percorso in cui prevedevi che arrivasse l’evento fosse in modalità di test o live?
* Hai salvato l’evento prima di copiare il payload dall’anteprima del payload?
* Il payload dell’evento contiene un ID evento?
* Hai raggiunto l’URL giusto?
* Hai seguito la struttura del payload delle API per l’acquisizione in streaming utilizzando l’anteprima della struttura del payload nel riquadro di configurazione dell’evento? Consulta [questa pagina](../event/about-creating.md#preview-the-payload).
* Hai utilizzato le coppie chiave-valore corrette nell’intestazione dell’evento?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## Controllare il modo in cui le persone si spostano nel percorso {#checking-how-people-navigate-through-the-journey}

Il reporting di percorso misura il progresso delle persone all&#39;interno di un percorso. È facile identificare in che punto una persona si è fermata e per quale motivo.

Di seguito sono riportati alcuni elementi da verificare:

* È dovuto a una condizione che esclude la persona? Ad esempio, la condizione è “genere = uomo” e la persona in oggetto è una donna. Questo controllo può essere eseguito da un utente aziendale, se la condizione non è troppo complessa.
* È dovuto a una chiamata a un’origine dati che non risponde? Quando il percorso è in modalità di test, queste informazioni possono essere visualizzate nei registri in modalità di test. Quando il percorso è live, un amministratore può testare le chiamate dirette all’origine dati e verificare la risposta ricevuta. Un amministratore può anche duplicare il percorso e testarlo.

## Verifica che i messaggi siano inviati correttamente {#checking-that-messages-are-sent-successfully}

Se gli individui si spostano nel modo giusto all’interno del percorso ma non ricevono i messaggi che dovrebbero ricevere, puoi verificare se:

* [!DNL Journey Optimizer] ha preso correttamente in considerazione la richiesta di invio del messaggio. Gli utenti aziendali possono accedere al messaggio che doveva essere stato inviato e verificare se l’ora dell’esecuzione più recente corrisponde all’orario di esecuzione del percorso. Può anche controllare le ultime chiamate/eventi API ricevuti.
* [!DNL Journey Optimizer] ha inviato correttamente il messaggio. Controlla la segnalazione del percorso per assicurarti che non ci siano errori.

Nel caso di un messaggio inviato tramite un’azione personalizzata, l’unica cosa che è possibile controllare durante il test di percorso è il fatto che la chiamata del sistema dell’azione personalizzata conduca o meno a un errore. Se la chiamata al sistema esterno associata all’azione personalizzata non genera un errore ma non causa l’invio di un messaggio, è necessario eseguire alcune indagini sul lato del sistema esterno.
