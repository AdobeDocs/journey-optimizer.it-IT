---
title: Aggiungere un messaggio in un percorso
description: Aggiungere un messaggio in un percorso
feature: Percorsi
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: 7937c3b7c9247868a7a506991850537493a76cf1
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 10%

---

# Aggiungere un messaggio in un percorso

[!DNL Journey Optimizer] le funzionalità per i messaggi sono integrate e ti basta progettare il contenuto e pubblicare il messaggio. Vedi [questa sezione](../get-started-content.md). Quindi devi semplicemente aggiungere, nel tuo percorso, un messaggio push o e-mail progettato utilizzando Journey Optimizer.

Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni in questa sezione [sezione](../action/action.md).

## Aggiungere un’attività Messaggio

1. Come sempre, inizia il percorso con un evento o un&#39;attività **Leggi segmento** .

   ![](../assets/jo-message0.png)

1. Dalla sezione **Azioni** della palette, trascina e rilascia un’attività **Messaggio** nell’area di lavoro.

   ![](../assets/jo-message1.png)

1. Aggiungi un’etichetta e una descrizione.

   ![](../assets/jo-message2.png)

1. Fare clic all&#39;interno del campo **Messaggio**. Viene visualizzato l’elenco dei messaggi disponibili progettati in Journey Optimizer. È possibile filtrare l’elenco in base allo stato.

   ![](../assets/jo-message3.png)

1. Scegli un messaggio e fai clic su **Seleziona**. Puoi anche creare un nuovo messaggio direttamente da questa schermata facendo clic su **Crea messaggio**.

   ![](../assets/jo-message4-ter.png)

   Per controllare il messaggio, fai clic sull&#39;icona **Apri il messaggio** nel campo **Messaggio** . Il messaggio verrà aperto in una nuova scheda.

   ![](../assets/jo-message4-bis.png)

1. Aggiungi i passaggi successivi al percorso.

## Parametri e-mail e parametri push

Le sezioni **[!UICONTROL Email parameters]** e **[!UICONTROL Push parameters]** mostrano campi di sola lettura. Questa configurazione viene in genere eseguita al momento della creazione del messaggio. Vedi [questa sezione](../get-started-content.md).

![](../assets/jo-message4.png)

Per forzare un valore specifico, puoi utilizzare l&#39;icona **Abilita sostituzione parametro** a destra del campo. Questa opzione può essere utile a scopo di test. Ad esempio, per un’e-mail, puoi aggiungere il tuo indirizzo e-mail. Dopo aver pubblicato il percorso, l’e-mail ti viene inviata.
