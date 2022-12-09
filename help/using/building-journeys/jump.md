---
solution: Journey Optimizer
product: journey optimizer
title: Salto da un viaggio all'altro
description: Salto da un viaggio all'altro
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 46d8950b-8b02-4160-89b4-1c492533c0e2
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Passa da un viaggio all’altro {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Attività Jump"
>abstract="L’attività di azione Jump (Passa a) consente di spingere singoli utenti da un percorso all’altro. Questa funzione ti consente di semplificare la progettazione di percorsi molto complessi e di generare percorsi basati su pattern di percorso comuni e riutilizzabili."

La **[!UICONTROL Jump]** l’attività di azione ti consente di spingere singoli utenti da un percorso all’altro. Questa funzione consente di:

* semplificare la progettazione di percorsi molto complessi suddividendoli in più percorsi
* creare percorsi basati su pattern di percorso comuni e riutilizzabili

Nel percorso di origine, aggiungi semplicemente un **[!UICONTROL Jump]** e seleziona un percorso target. Quando l’utente accede alla **[!UICONTROL Jump]** un evento interno viene inviato al primo evento del percorso di destinazione. Se la **[!UICONTROL Jump]** l&#39;azione ha successo, l&#39;individuo continua a progredire nel percorso. Il comportamento è simile ad altre azioni.

Nel percorso di destinazione, il primo evento attivato internamente dal **[!UICONTROL Jump]** l’attività farà sì che il singolo flusso del percorso sia generato.

## Ciclo di vita

Supponiamo che tu abbia aggiunto un **[!UICONTROL Jump]** attività in un percorso A a un percorso B. Il percorso A è il **percorso di origine** e il percorso B, **percorso target**.
Di seguito sono riportati i diversi passaggi del processo di esecuzione:

**Percorso A** viene attivato da un evento esterno:

1. Journey A riceve un evento esterno relativo a una persona.
1. L&#39;individuo raggiunge il **[!UICONTROL Jump]** passo.
1. L’utente viene inviato al percorso B e passa ai passaggi successivi nel percorso A, dopo il **[!UICONTROL Jump]** passo.

Nel percorso B, il primo evento viene attivato internamente, tramite il **[!UICONTROL Jump]** attività dal percorso A:

1. Il percorso B ha ricevuto un evento interno dal percorso A.
1. L’utente inizia a scorrere nel percorso B.

>[!NOTE]
>
>Il percorso B può essere attivato anche tramite un evento esterno.

## Best practice e limitazioni

### Authoring

* La **[!UICONTROL Jump]** l’attività è disponibile solo nei percorsi che utilizzano uno spazio dei nomi.
* Puoi passare a un percorso che utilizza lo stesso namespace del percorso di origine.
* Non puoi saltare a un percorso che inizia con un **Qualificazione del segmento** evento o **Leggi segmento**.
* Non puoi avere un **[!UICONTROL Jump]** attività e **Qualificazione del segmento** evento o **Leggi segmento** nello stesso percorso.
* Puoi includere più **[!UICONTROL Jump]** attività necessarie in un percorso. Dopo un **[!UICONTROL Jump]**, puoi aggiungere qualsiasi attività necessaria.
* Puoi avere tutti i livelli di salto necessari. Ad esempio, il percorso A salta al percorso B, che passa al percorso C e così via.
* Il percorso di destinazione può includere anche altrettanti **[!UICONTROL Jump]** le attività necessarie.
* I pattern di loop non sono supportati. Non esiste modo di collegare due o più percorsi tra loro, il che creerebbe un ciclo infinito. La **[!UICONTROL Jump]** la schermata di configurazione dell’attività non consente di eseguire questa operazione.

### Esecuzione

* Quando il **[!UICONTROL Jump]** l’attività viene eseguita e viene attivata la versione più recente del percorso di destinazione.
* Come al solito, un individuo unico può essere presente solo una volta nello stesso percorso. Di conseguenza, se l’individuo inviato dal percorso di origine è già nel percorso di destinazione, l’utente non accederà al percorso di destinazione. Non verrà segnalato alcun errore nel **[!UICONTROL Jump]** perché si tratta di un comportamento normale.

## Configurazione dell’attività Jump

1. Progettazione di **percorso di origine**.

   ![](assets/jump1.png)

1. In qualsiasi fase del percorso, aggiungi un **[!UICONTROL Jump]** dall&#39;attività **[!UICONTROL ACTIONS]** categoria. Aggiungi un’etichetta e una descrizione.

   ![](assets/jump2.png)

1. Fai clic all’interno del **Percorso di Target** campo .
Nell’elenco sono visualizzate tutte le versioni del percorso che sono in bozza, in tempo reale o in modalità di test. Percorsi che utilizzano uno spazio dei nomi diverso o che iniziano con un **Qualificazione del segmento** l&#39;evento non è disponibile. Vengono inoltre esclusi i percorsi di destinazione che creerebbero un pattern di ciclo.

   ![](assets/jump3.png)

   >[!NOTE]
   >
   >Puoi fare clic su **Apri percorso target** a destra per aprire il percorso di destinazione in una nuova scheda.

1. Seleziona il percorso di destinazione a cui desideri passare.
La **Primo evento** viene precompilato con il nome del primo evento del percorso di destinazione. Se il percorso di destinazione include più eventi, la **[!UICONTROL Jump]** è consentito solo nel primo evento.

   ![](assets/jump4.png)

1. La **Parametri azione** visualizza tutti i campi dell&#39;evento target. Allo stesso modo degli altri tipi di azioni, mappa ogni campo con campi dell’evento di origine o dell’origine dati. Queste informazioni verranno trasmesse al percorso di destinazione in fase di runtime.
1. Aggiungi le attività successive per completare il percorso di origine.

   ![](assets/jump5.png)


   >[!NOTE]
   >
   >L&#39;identità dell&#39;individuo viene mappata automaticamente. Queste informazioni non sono visibili nell’interfaccia.

Le **[!UICONTROL Jump]** l’attività è configurata. Non appena il tuo percorso è live o in modalità di test, gli individui che raggiungono **[!UICONTROL Jump]** il passaggio verrà inviato dal al percorso di destinazione.

Quando un **[!UICONTROL Jump]** l’attività viene configurata in un percorso, come **[!UICONTROL Jump]** l’icona di ingresso viene aggiunta automaticamente all’inizio del percorso di destinazione. Questo ti aiuta a identificare che il percorso può essere attivato esternamente ma anche internamente da un **[!UICONTROL Jump]** attività.

![](assets/jump7.png)

## Risoluzione dei problemi

Quando il percorso viene pubblicato o in modalità di test, si verificano degli errori se:
* il percorso target non esiste più
* il percorso di destinazione è bozza, chiuso o interrotto
* se il primo evento del percorso di destinazione è cambiato e la mappatura è interrotta

![](assets/jump6.png)
