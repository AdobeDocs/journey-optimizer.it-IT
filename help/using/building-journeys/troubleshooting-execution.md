---
solution: Journey Optimizer
product: journey optimizer
title: Risolvere i problemi relativi all’esecuzione live del percorso
description: Scopri come risolvere gli errori nell’esecuzione di un percorso live
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: risoluzione dei problemi, risoluzione dei problemi, percorso, controllo, errori
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 36%

---

# Risolvere i problemi relativi all’esecuzione live del percorso {#troubleshooting-execution}

In questa sezione, scopri come risolvere i problemi relativi agli eventi di percorso, verificare se i profili sono entrati nel percorso, come ci si sposta e se i messaggi vengono inviati.

È inoltre possibile risolvere gli errori prima di testare o pubblicare un percorso. Scopri come [in questa pagina](troubleshooting.md).

Se utilizzi azioni in entrata, scopri come risolverle [in questa pagina](troubleshooting-inbound.md).

## Verifica che gli eventi siano inviati correttamente {#checking-that-events-are-properly-sent}

Il punto di partenza di un percorso è sempre un evento. Puoi eseguire i test utilizzando strumenti come Postman.

Puoi verificare se la chiamata API inviata tramite questi strumenti viene inviata correttamente o meno. Se ricevi nuovamente un errore, significa che la chiamata presenta un problema. Controlla di nuovo il payload, l’intestazione (e in particolare l’ID organizzazione) e l’URL di destinazione. Puoi chiedere all’amministratore qual è l’URL corretto da utilizzare.

Gli eventi non vengono inviati direttamente dall’origine ai percorsi. In effetti, i percorsi si basano sulle API Streaming Ingestion di Adobe Experience Platform. Di conseguenza, in caso di problemi relativi agli eventi, puoi fare riferimento alla [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=it){target="_blank"} per la risoluzione dei problemi relativi alle API Streaming Ingestion.

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
