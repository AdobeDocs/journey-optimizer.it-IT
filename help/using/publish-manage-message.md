---
title: Pubblicare e modificare un messaggio
description: Scopri come pubblicare e aggiornare i messaggi
snippet: y
feature: Percorsi
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: fa025278c2e2cf02df22d31532b0d33786996915
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 4%

---

# Pubblicare i messaggi {#publish-manage-messages}

## Pubblicare un messaggio {#publish-message}

Una volta creato il messaggio, puoi pubblicarlo per renderlo disponibile per l’esecuzione.

>[!CAUTION]
>
>Prima della pubblicazione, controlla e risolvi gli avvisi. [Ulteriori informazioni](alerts.md)

![](assets/publish-message.png)

Dopo la pubblicazione, il messaggio viene aggiunto all’elenco dei messaggi con lo stato **[!UICONTROL Published]** .

È ora pronto per essere attivato da uno o più [percorsi](building-journeys/journey.md).

## Aggiornare un messaggio di sola lettura {#modify-message}

Dopo la pubblicazione, un messaggio è in modalità di sola lettura. È comunque possibile aggiornarlo creando una nuova bozza del messaggio.

Questo consente ad esempio di aggiornare il contenuto o risolvere un problema, senza pubblicare nuovamente l’intero percorso in cui viene utilizzato il messaggio.

>[!NOTE]
>
>La bozza può essere modificata mentre la versione pubblicata è ancora pubblicata e attiva.

Per aggiornare un messaggio pubblicato:

1. Seleziona il messaggio da aprire dall’elenco dei messaggi.

1. Fai clic su **[!UICONTROL Modify]**.

   ![](assets/message-modify.png)

1. Conferma la tua scelta. Viene creata una versione bozza del messaggio.

   ![](assets/message-modify-v2.png)

1. Modifica il contenuto o modifica le impostazioni desiderate.
1. Fai clic su **[!UICONTROL Publish]**. Questa azione pubblica la nuova versione del messaggio che verrà utilizzata per le esecuzioni successive.

Non appena viene pubblicata la nuova versione, alla successiva chiamata API verrà generata una nuova esecuzione del messaggio. La nuova versione verrà ricevuta dal profilo successivo in arrivo.

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version. -->
