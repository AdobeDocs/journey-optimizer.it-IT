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
source-git-commit: 28a4f04ebcda27213d3bac763fb9bea8ea4a0146
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 1%

---

# Caso di utilizzo: invio di messaggi multicanale{#send-multi-channel-messages}

Questa sezione presenta un caso d’uso che combina un Read Audience, un evento, eventi di reazione e messaggi e-mail/push.

![](assets/jo-uc1.png)

## Descrizione del caso d’uso

In questo caso d’uso, vogliamo inviare un primo messaggio (e-mail e push) a tutti i clienti appartenenti a un pubblico specifico.

In base alla loro reazione al primo messaggio, vogliamo inviare messaggi specifici.

Dopo il primo messaggio, attendiamo un giorno che i clienti aprano il messaggio push o e-mail. In assenza di reazioni, inviamo loro un’e-mail di follow-up.

Poi aspettiamo un acquisto e inviamo un messaggio push per ringraziare il cliente.

## Prerequisiti

Affinché questo caso d’uso funzioni, devi configurare quanto segue:

* un pubblico per tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980.
* un evento di acquisto

### Creare il pubblico

Nel nostro percorso, vogliamo sfruttare un pubblico specifico di clienti. Tutti gli individui appartenenti al pubblico entrano nel percorso e seguono i diversi passaggi. Nel nostro esempio, abbiamo bisogno di un pubblico che indirizzi tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980.

Per ulteriori informazioni sui tipi di pubblico, consulta questa [pagina](../audience/about-audiences.md).

1. Dalla sezione del menu CUSTOMER, seleziona **[!UICONTROL Tipi di pubblico]**.

1. Fai clic su **[!UICONTROL Creare un pubblico]** che si trova in alto a destra nell’elenco del pubblico.

1. In **[!UICONTROL Proprietà del pubblico]** , immettere un nome per il pubblico.

1. Trascina e rilascia i campi desiderati dal riquadro di sinistra all’area di lavoro centrale, quindi configurali in base alle tue esigenze. In questo esempio utilizziamo **Città** e **Anno di nascita** campi degli attributi.

1. Fai clic su **[!UICONTROL Salva]**.

   ![](assets/add-attributes.png)

Il pubblico ora è stato creato ed è pronto per essere utilizzato nel percorso. Utilizzo di un **Read Audience** attività, puoi fare in modo che tutti i singoli utenti appartenenti al pubblico entrino nel percorso.

### Configurare l’evento

Devi configurare un evento che viene inviato al tuo percorso quando un cliente effettua un acquisto. Quando il percorso riceve l&#39;evento, attiva il messaggio di ringraziamento.

Per questo, utilizziamo un evento basato su regole. Per ulteriori informazioni sugli eventi, consulta questa [pagina](../event/about-events.md).

1. Nella sezione del menu ADMINISTRATION, selezionare **[!UICONTROL Configurazioni]**, quindi fai clic su **[!UICONTROL Eventi]**. Clic **[!UICONTROL Crea evento]** per creare un nuovo evento.

1. Inserisci il nome dell’evento.

1. In **[!UICONTROL Tipo ID evento]** campo, seleziona **[!UICONTROL Basato su regole]**.

1. Definisci il **[!UICONTROL Schema]** e payload **[!UICONTROL Campi]**. Puoi utilizzare diversi campi, ad esempio il prodotto acquistato, la data di acquisto e l’ID acquisto.

1. In **[!UICONTROL Condizione ID evento]** definire la condizione utilizzata dal sistema per identificare gli eventi che attivano il percorso. Ad esempio, puoi aggiungere una `purchaseMessage` e definisci la seguente regola: `purchaseMessage="thank you"`

1. Definisci il **[!UICONTROL Namespace]** e **[!UICONTROL Identificatore profilo]**.

1. Fai clic su **[!UICONTROL Salva]**.

   ![](assets/jo-uc2.png)

L’evento è ora configurato e pronto per essere utilizzato nel percorso. Utilizzando l’attività evento corrispondente, puoi attivare un’azione ogni volta che un cliente effettua un acquisto.

## Progettare il percorso

1. Avvia il percorso con un **Read Audience** attività. Seleziona il pubblico creato in precedenza. Tutti gli individui appartenenti al pubblico entrano nel percorso.

   ![](assets/jo-uc4.png)

1. Rilascia un **E-mail** attività e definire il contenuto del &quot;primo messaggio&quot;. Questo messaggio viene inviato a tutti i singoli utenti del percorso. Fai riferimento a questo [sezione](../email/create-email.md) per scoprire come configurare e progettare un’e-mail.

   ![](assets/jo-uc5.png)

1. Posiziona il cursore sull’attività e-mail e fai clic sul simbolo &quot;+&quot; per creare un nuovo percorso.

1. Nel primo percorso, aggiungi un **Reazione** evento e seleziona **Push aperto**. L’evento viene attivato quando un singolo appartenente al pubblico apre la versione push del primo messaggio.

1. Nel secondo percorso, aggiungi un **Reazione** evento e seleziona **E-mail aperta**. L’evento viene attivato quando l’utente apre l’e-mail.

1. In una delle attività di reazione, controllare **Definire il timeout dell’evento** , definisci una durata (1 giorno nel nostro esempio) e spunta **Impostare un percorso di timeout**. In questo modo viene creato un altro percorso per i singoli utenti che non aprono il primo messaggio push o e-mail.

   >[!NOTE]
   >
   >Quando configuri un timeout per più eventi (le due reazioni in questo caso), devi configurare il timeout solo per uno di questi eventi.

1. Nel percorso di timeout, rilascia una **E-mail** attività e definire il contenuto del messaggio di &quot;follow-up&quot;. Questo messaggio viene inviato alle persone che non aprono l’e-mail o non inviano il primo messaggio push nel giorno successivo. Fai riferimento a questo [sezione](../email/create-email.md) per scoprire come configurare e progettare un’e-mail.

1. Connetti i tre percorsi all’evento di acquisto creato in precedenza. L’evento viene attivato quando un individuo effettua un acquisto.

1. Dopo l’evento, rilascia una **Push** attività di azione e definisci il contenuto del messaggio di ringraziamento. Fai riferimento a questo [sezione](../push/create-push.md) per scoprire come configurare e progettare un push.

## Test e pubblicazione del percorso

1. Prima di eseguire il test del percorso, verificare che sia valido e che non vi siano errori.

1. Fai clic sul pulsante **Test** per attivare la modalità di test, posizionata nell’angolo in alto a destra. Fai riferimento a questo [sezione](testing-the-journey.md) per scoprire come utilizzare la modalità di test.

1. Quando il percorso è pronto, pubblicarlo utilizzando **Pubblica** nell&#39;angolo superiore destro.
