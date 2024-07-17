---
solution: Journey Optimizer
product: journey optimizer
title: Casi di utilizzo dei percorsi
description: Casi di utilizzo dei percorsi
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: caso d’uso, multicanale, messaggi, percorso, canale, eventi, push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# Caso di utilizzo: invio di messaggi multicanale{#send-multi-channel-messages}

Questa sezione presenta un caso d’uso che combina un Read Audience, un evento, eventi di reazione e messaggi e-mail/push.

![](assets/jo-uc1.png)

## Descrizione del caso d’uso

In questo caso d’uso, vogliamo inviare un primo messaggio e-mail a tutti i clienti appartenenti a un pubblico specifico.

In base alla loro reazione al primo messaggio, vogliamo inviare messaggi specifici.

Se il cliente apre l’e-mail, attendiamo un acquisto e inviamo un messaggio push per ringraziare il cliente.

In assenza di reazioni, inviamo loro un’e-mail di follow-up.

## Prerequisiti

Affinché questo caso d’uso funzioni, devi configurare quanto segue:

* un pubblico per tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980.
* un evento di acquisto

### Creare il pubblico

Nel nostro percorso, vogliamo sfruttare un pubblico specifico di clienti. Tutti gli individui appartenenti al pubblico entrano nel percorso e seguono i diversi passaggi. Nel nostro esempio, abbiamo bisogno di un pubblico che indirizzi tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980.

Per ulteriori informazioni sui tipi di pubblico, consulta questa [pagina](../audience/about-audiences.md).

1. Dalla sezione del menu CUSTOMER, seleziona **[!UICONTROL Tipi di pubblico]**.

1. Fai clic sul pulsante **[!UICONTROL Crea pubblico]** in alto a destra nell&#39;elenco del pubblico.

1. Nel riquadro **[!UICONTROL Proprietà pubblico]** immettere un nome per il pubblico.

1. Trascina e rilascia i campi desiderati dal riquadro di sinistra all’area di lavoro centrale, quindi configurali in base alle tue esigenze. In questo esempio utilizziamo i campi degli attributi **Città** e **Anno di nascita**.

1. Fai clic su **[!UICONTROL Salva]**.

   ![](assets/add-attributes.png)

Il pubblico ora è stato creato ed è pronto per essere utilizzato nel percorso. Utilizzando un&#39;attività **Read Audience**, puoi fare in modo che tutti i singoli utenti appartenenti al pubblico entrino nel percorso.

### Configurare l’evento

Devi configurare un evento che viene inviato al tuo percorso quando un cliente effettua un acquisto. Quando il percorso riceve l&#39;evento, attiva il messaggio di ringraziamento.

Per questo, utilizziamo un evento basato su regole. Per ulteriori informazioni sugli eventi, consulta questa [pagina](../event/about-events.md).

1. Nella sezione del menu AMMINISTRAZIONE, seleziona **[!UICONTROL Configurazioni]**, quindi fai clic su **[!UICONTROL Eventi]**. Fai clic su **[!UICONTROL Crea evento]** per creare un nuovo evento.

1. Inserisci il nome dell’evento.

1. Nel campo **[!UICONTROL Tipo ID evento]**, seleziona **[!UICONTROL Basato su regole]**.

1. Definisci lo **[!UICONTROL Schema]** e il payload **[!UICONTROL Campi]**. Puoi utilizzare diversi campi, ad esempio il prodotto acquistato, la data di acquisto e l’ID acquisto.

1. Nel campo **[!UICONTROL Condizione ID evento]**, definire la condizione utilizzata dal sistema per identificare gli eventi che attivano il percorso. Ad esempio, puoi aggiungere un campo `purchaseMessage` e definire la seguente regola: `purchaseMessage="thank you"`

1. Definisci **[!UICONTROL Spazio dei nomi]** e **[!UICONTROL Identificatore profilo]**.

1. Fai clic su **[!UICONTROL Salva]**.

   ![](assets/jo-uc2.png)

L’evento è ora configurato e pronto per essere utilizzato nel percorso. Utilizzando l’attività evento corrispondente, puoi attivare un’azione ogni volta che un cliente effettua un acquisto.

## Progettare il percorso

1. Avvia il percorso con un&#39;attività **Read Audience**. Seleziona il pubblico creato in precedenza. Tutti gli individui appartenenti al pubblico entrano nel percorso.

   ![](assets/jo-uc4.png)

1. Rilascia un&#39;attività di azione **Email** e definisci il contenuto del &quot;primo messaggio&quot;. Questo messaggio viene inviato a tutti i singoli utenti del percorso. Consulta questa [sezione](../email/create-email.md) per scoprire come configurare e progettare un messaggio e-mail.

   ![](assets/jo-uc5.png)

1. Aggiungi un evento **Reaction** e seleziona **Email open**. L’evento viene attivato quando una persona appartenente al pubblico apre l’e-mail.

1. Seleziona la casella **Definisci il timeout dell&#39;evento**, definisci una durata (1 giorno nel nostro esempio) e seleziona **Imposta un percorso di timeout**. In questo modo viene creato un altro percorso per i singoli utenti che non aprono il primo messaggio push o e-mail.

1. Nel percorso di timeout, rilascia un&#39;attività di azione **E-mail** e definisci il contenuto del messaggio di completamento. Questo messaggio viene inviato alle persone che non aprono l’e-mail o non inviano il primo messaggio push nel giorno successivo. Consulta questa [sezione](../email/create-email.md) per scoprire come configurare e progettare un messaggio e-mail.

1. Nel primo percorso, aggiungi l’evento di acquisto creato in precedenza. L’evento viene attivato quando un individuo effettua un acquisto.

1. Dopo l&#39;evento, rilascia un&#39;attività di azione **Push** e definisci il contenuto del messaggio di ringraziamento. Consulta questa [sezione](../push/create-push.md) per scoprire come configurare e progettare un push.

## Test e pubblicazione del percorso

1. Prima di eseguire il test del percorso, verificare che sia valido e che non vi siano errori.

1. Per attivare la modalità di test, fai clic sull&#39;interruttore **Test**, situato nell&#39;angolo in alto a destra. Consulta questa [sezione](testing-the-journey.md) per scoprire come utilizzare la modalità di test.

1. Quando il percorso è pronto, pubblicalo utilizzando il pulsante **Publish**, in alto a destra.
