---
title: Casi d’uso dei percorsi
description: Casi d’uso dei percorsi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 2%

---

# Caso di utilizzo: inviare messaggi multicanale{#send-multi-channel-messages}

Questa sezione presenta un caso d’uso che combina un segmento di lettura, un evento, eventi di reazione e messaggi e-mail/push.

![](assets/jo-uc1.png)

## Descrizione del caso d’uso

In questo caso d’uso, desideri inviare un primo messaggio (e-mail e push) a tutti i clienti appartenenti a un segmento specifico.

In base alla loro reazione al primo messaggio, vogliamo inviare messaggi specifici.

Dopo il primo messaggio, attendiamo un giorno che i clienti aprano il messaggio push o e-mail. Se non ci sono reazioni, gli inviamo un&#39;e-mail di follow-up.

Quindi attendiamo un acquisto e inviamo un messaggio push per ringraziare il cliente.

## Prerequisiti

Affinché questo caso d’uso funzioni, devi configurare quanto segue:

* un segmento per tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980.
* un evento di acquisto
* tre messaggi

### Creare il segmento

Nel nostro percorso, vogliamo sfruttare un segmento specifico di clienti. Tutti gli individui appartenenti al segmento entrano nel percorso e seguono i diversi passaggi. Nel nostro esempio, abbiamo bisogno di un segmento che si rivolga a tutti i clienti che vivono ad Atlanta, San Francisco, o Seattle e che sono nati dopo il 1980.

Per ulteriori informazioni sui segmenti, consulta questo [page](../segment/about-segments.md).

1. Nella sezione del menu CLIENTE, selezionare **[!UICONTROL Segments]**.

1. Fai clic sul pulsante **[!UICONTROL Create segment]** in alto a destra nell’elenco dei segmenti.

1. In **[!UICONTROL Segment properties]** immettere un nome per il segmento.

1. Trascina e rilascia i campi desiderati dal riquadro di sinistra all’area di lavoro centrale, quindi configurali in base alle tue esigenze. In questo esempio, utilizziamo il **Città** e **Anno di nascita** campi degli attributi.

1. Fai clic su **[!UICONTROL Save]**.

   ![](assets/add-attributes.png)

Il segmento viene ora creato e pronto per essere utilizzato nel percorso. Utilizzo di un **Leggi segmento** attività , puoi fare in modo che tutti gli individui appartenenti al segmento entrino nel percorso .

### Configurare l’evento

Devi configurare un evento inviato al tuo percorso quando un cliente effettua un acquisto. Quando il percorso riceve l&#39;evento, attiva il messaggio di &quot;grazie&quot;.

A questo scopo, utilizziamo un evento basato su regole. Per ulteriori informazioni sugli eventi, consulta questo [page](../event/about-events.md).

1. Nella sezione del menu AMMINISTRAZIONE, seleziona **[!UICONTROL Configurations]**, quindi fai clic su **[!UICONTROL Events]**. Per creare un nuovo evento, fai clic su **[!UICONTROL Create event]**. 

1. Inserisci il nome dell’evento.

1. Nel campo **[!UICONTROL Event ID type]** seleziona **[!UICONTROL Rule Based]**.

1. Definisci la **[!UICONTROL Schema]** e payload **[!UICONTROL Fields]**. Puoi utilizzare diversi campi, ad esempio il prodotto acquistato, la data di acquisto e l’ID acquisto.

1. In **[!UICONTROL Event ID condition]** definire la condizione utilizzata dal sistema per identificare gli eventi che attivano il percorso. Ad esempio, puoi aggiungere una `purchaseMessage` e definisci la seguente regola: `purchaseMessage="thank you"`

1. Definisci la **[!UICONTROL Namespace]** e **[!UICONTROL Profile Identifier]**.

1. Fai clic su **[!UICONTROL Save]**.

   ![](assets/jo-uc2.png)

L’evento è ora configurato e pronto per essere utilizzato nel percorso. Utilizzando l’attività evento corrispondente, puoi attivare un’azione ogni volta che un cliente effettua un acquisto.

### Creare i messaggi

Per questo caso d’uso, è necessario creare tre messaggi:

* un primo messaggio push ed e-mail
* un messaggio push di ringraziamento
* un messaggio di follow-up e-mail

![](assets/jo-uc3.png)

Fai riferimento a questo [sezione](../segment/about-segments.md) per scoprire come progettare e pubblicare questi messaggi.

## Progettare il percorso

1. Avvia il percorso con un **Leggi segmento** attività. Seleziona il segmento creato in precedenza. Tutti i singoli utenti appartenenti al segmento entrano nel percorso.

   ![](assets/jo-uc4.png)

1. Rilascia un **Messaggio** e seleziona il primo messaggio push ed e-mail. Questo messaggio viene inviato a tutti gli individui del percorso.

   ![](assets/jo-uc5.png)

1. Posiziona il cursore sull’attività del messaggio e fai clic sul simbolo &quot;+&quot; per creare un nuovo percorso.

1. Nel primo percorso, aggiungi un **Reazione** evento e seleziona **Push aperto**. L’evento viene attivato quando una persona appartenente al segmento apre la versione push del primo messaggio.

1. Nel secondo percorso, aggiungi un **Reazione** evento e seleziona **E-mail aperta**. L’evento viene attivato quando l’utente apre l’e-mail.

1. In una delle attività di reazione, controlla il **Definire il timeout dell’evento** , definisci una durata (1 giorno nel nostro esempio) e seleziona **Imposta un percorso di timeout**. Questo crea un altro percorso per gli utenti che non aprono il primo messaggio push o e-mail.

   >[!NOTE]
   >
   >Quando configuri un timeout su più eventi (le due reazioni in questo caso), devi configurare il timeout solo su uno di questi eventi.

1. Nel percorso di timeout, rilascia una **Messaggio** e seleziona il messaggio di follow-up e-mail. Questo messaggio viene inviato agli utenti che non aprono l’e-mail o non inviano il primo messaggio push il giorno successivo.

1. Collega i tre percorsi all’evento di acquisto creato in precedenza. L’evento viene attivato quando un singolo utente effettua un acquisto.

1. Dopo l’evento, rilascia una **Messaggio** e seleziona il messaggio di e-mail &quot;grazie&quot;.

1. Aggiungi un **Fine** attività.

## Test e pubblicazione del percorso

1. Prima di testare il percorso, verifica che sia valido e che non vi sia alcun errore.

1. Fai clic sul pulsante **Test** per attivare la modalità di prova, nell’angolo in alto a destra. Definisci come desideri che i profili di test entrino nel test: un singolo profilo, o fino a 100 alla volta. Fai riferimento a questo [sezione](testing-the-journey.md) per scoprire come utilizzare la modalità di test.

1. Quando il percorso è pronto, pubblicalo utilizzando la variabile **Pubblica** nell&#39;angolo in alto a destra.
