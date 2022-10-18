---
solution: Journey Optimizer
product: journey optimizer
title: Progettazione del percorso
description: Scopri come progettare il percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1998f6fc-60fd-4038-8669-39cd55bc02d1
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '1490'
ht-degree: 3%

---

# Progettazione del percorso {#design-your-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_canvas"
>title="Progettazione del percorso"
>abstract="L’interfaccia di percorso ti consente di trascinare facilmente le attività dalla palette nell’area di lavoro. Puoi anche fare doppio clic su un’attività per aggiungerla nell’area di lavoro al passaggio successivo disponibile."

L’interfaccia di percorso ti consente di trascinare facilmente le attività dalla palette nell’area di lavoro. Puoi anche fare doppio clic su un’attività per aggiungerla nell’area di lavoro al passaggio successivo disponibile. Ciascuna attività ha un ruolo specifico e un ruolo specifico nel processo. Le attività vengono sequenziate. Al termine di un’attività, il flusso continua ed elabora l’attività successiva e così via.

## Guida introduttiva alla progettazione di percorsi {#gs-journey-design}

La **palette** si trova sul lato sinistro dello schermo. Tutte le attività disponibili sono suddivise in diverse categorie: **[!UICONTROL Eventi]**, **[!UICONTROL Orchestrazione]** e **[!UICONTROL Azioni]**. È possibile espandere o comprimere le diverse categorie facendo clic sul loro nome. Per utilizzare un’attività nel percorso, trascinala dalla palette nell’area di lavoro.

Quando si avvia un nuovo percorso, gli elementi che non possono essere eliminati nell’area di lavoro come primo passaggio vengono nascosti. Questo riguarda tutte le azioni, l’attività della condizione, l’attesa e la reazione.

![](assets/journey38.png)

La **[!UICONTROL Filtrare gli elementi]** nell’angolo in alto a sinistra consente di visualizzare i seguenti filtri:

* **Mostra solo gli elementi disponibili**: nascondere o visualizzare gli elementi non disponibili nella palette, ad esempio gli eventi che utilizzano uno spazio dei nomi diverso da quelli utilizzati nel percorso. Per impostazione predefinita, gli elementi non disponibili sono nascosti. Se scegli di visualizzarli, verranno visualizzati in grigio.

* **Mostra solo elementi recenti**: questo filtro consente di visualizzare solo gli ultimi cinque eventi e azioni utilizzati, oltre a quelli predefiniti. Questo è specifico per ogni utente. Per impostazione predefinita, vengono visualizzati tutti gli elementi.

È inoltre possibile utilizzare **[!UICONTROL Ricerca]** campo . Solo gli eventi e le azioni vengono filtrati.

La **tela** è la zona centrale del designer del percorso. È in questa zona che puoi rilasciare le attività e configurarle. Fai clic su un’attività nell’area di lavoro per configurarla. Viene aperto il riquadro di configurazione dell’attività sul lato destro.

![](assets/journey39.png)

La **riquadro di configurazione delle attività** viene visualizzato quando si fa clic su un’attività nella palette. Compila i campi richiesti. Fai clic sul pulsante **[!UICONTROL Elimina]** per eliminare l’attività. Fai clic su **[!UICONTROL Annulla]** annullare le modifiche o **[!UICONTROL Ok]** per confermare. Per eliminare le attività, puoi anche selezionare una (o più) attività e premere il tasto backspace. Premendo il tasto Esc si chiude il riquadro di configurazione dell’attività.

Per impostazione predefinita, i campi di sola lettura sono nascosti. Per visualizzare campi di sola lettura, fai clic sul pulsante **Mostra campi di sola lettura** in alto a sinistra nel riquadro di configurazione dell’attività. Questa impostazione si applica a tutte le attività in tutti i percorsi.

![](assets/journey59bis.png)

A seconda dello stato del percorso, è possibile eseguire diverse azioni sul percorso utilizzando i pulsanti disponibili nell’angolo in alto a destra: **[!UICONTROL Pubblica]**, **[!UICONTROL Duplica]**, **[!UICONTROL Elimina]**, **[!UICONTROL Proprietà percorso]**, **[!UICONTROL Test]**. Questi pulsanti vengono visualizzati quando non è selezionata alcuna attività. Alcuni pulsanti vengono visualizzati contestualmente. Il pulsante del registro della modalità di prova viene visualizzato quando viene attivata la modalità di prova.

![](assets/journey41.png)

## Avvia il percorso {#start-your-journey}

Quando si progetta un percorso, la prima domanda che si desidera porre è come i profili entreranno nel percorso. Esistono due possibilità:

**Inizia con un evento**: quando un percorso è impostato per ascoltare gli eventi, le persone entrano nel percorso **unitariamente** in tempo reale. I messaggi inclusi nel tuo percorso vengono inviati alla persona che si trova attualmente nel percorso. [Ulteriori informazioni sugli eventi](../event/about-events.md)

**Inizia con un segmento di lettura**: puoi impostare il tuo percorso per ascoltare i segmenti Adobe Experience Platform. In questo caso, tutti gli individui appartenenti al segmento specificato entrano nel percorso. I messaggi inclusi nel percorso vengono inviati agli utenti appartenenti al segmento. [Ulteriori informazioni sulla lettura dei segmenti](read-segment.md).

## Definire i passaggi successivi{#define-next-steps}

Dopo il primo evento o Leggi segmento, puoi combinare le diverse attività per creare scenari multicanale con più passaggi. Dalla palette, scegli i passaggi necessari.

**Eventi**

Quando avvii il percorso con un evento, il percorso viene attivato quando l’evento viene ricevuto. La persona seguirà, singolarmente, i passaggi successivi definiti nel tuo percorso.

Puoi aggiungere **vari eventi** nel tuo percorso, purché utilizzino lo stesso namespace. Gli eventi sono configurati in precedenza. [Ulteriori informazioni sugli eventi](about-journey-activities.md#event-activities)

Puoi anche aggiungere una **Reazione** dopo un messaggio per reagire ai dati di tracciamento relativi al messaggio. Questo consente, ad esempio, di inviare un altro messaggio se l’utente ha aperto il messaggio precedente o ha fatto clic al suo interno. Ulteriori informazioni [sezione](reaction-events.md).

La **Qualificazione del segmento** l’attività evento ti consente di far entrare o proseguire singoli utenti in un percorso in base alle entrate e alle uscite dei segmenti Adobe Experience Platform. Puoi far entrare tutti i nuovi clienti in argento in un percorso e inviare messaggi personalizzati. Ulteriori informazioni [sezione](segment-qualification-events.md).

**Orchestrazione**

Nelle attività di orchestrazione, troverai il **Leggi segmento** attività che ti consente di impostare il percorso in modo che ascolti un segmento Adobe Experience Platform. [Ulteriori informazioni sull’attività Leggi segmento](read-segment.md).

Le altre attività ti consentono di aggiungere condizioni al percorso per definire diversi percorsi, impostare un tempo di attesa prima di eseguire l’attività successiva o terminare il percorso. Ulteriori informazioni [sezione](about-journey-activities.md#orchestration-activities).

**Azioni**

Qui trovi l’attività di azione del canale che ti consente di includere un messaggio progettato in [!DNL Journey Optimizer]. [Ulteriori informazioni sulle attività di azione del canale](journeys-message.md)

Troverai anche le azioni personalizzate configurate per l’invio di messaggi con sistemi di terze parti. Ulteriori informazioni [sezione](about-journey-activities.md#action-activities).

## Aggiungi percorsi alternativi{#paths}

Puoi definire un’azione di fallback in caso di errore o timeout per le seguenti attività del percorso: **[!UICONTROL Condizione]** e **[!UICONTROL Azione]**.

Per aggiungere un’azione di fallback a un’attività, seleziona la **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o di errore]** nelle proprietà dell’attività: dopo l’attività viene aggiunto un altro percorso. La durata del timeout è definita dagli utenti amministratori nel [Proprietà percorso](../building-journeys/journey-gs.md#change-properties). Ad esempio, se l’invio di un’e-mail richiede troppo tempo o si verifica un errore, puoi decidere di inviare una notifica push.

![](assets/journey42.png)

Varie attività (evento, azione, attesa) ti consentono di aggiungere diversi percorsi dopo di essi. A questo scopo, posiziona il cursore sull’attività e fai clic sul simbolo &quot;+&quot;. Solo le attività evento e attesa possono essere impostate in parallelo. Se più eventi sono impostati in parallelo, il percorso scelto sarà quello del primo evento che si verifica.

Quando ascolti un evento, ti consigliamo di non attendere l’evento a tempo indefinito. Non è obbligatorio, è solo una buona pratica. Se desideri ascoltare uno o più eventi solo durante un certo periodo di tempo, inserirai uno o più eventi e un’attività di attesa in parallelo. Vedi [questa sezione](../building-journeys/general-events.md#events-specific-time).

Per eliminare il percorso, posiziona il cursore su di esso e fai clic sul pulsante **[!UICONTROL Elimina percorso]** icona.

![](assets/journey42ter.png)

Nell’area di lavoro, quando due attività vengono disconnesse, viene visualizzato un avviso. Posiziona il cursore sull’icona di avviso per visualizzare il messaggio di errore. Per risolvere il problema, sposta semplicemente l’attività disconnessa e collegala all’attività precedente.

![](assets/canvas-disconnected.png)

## Copiare e incollare le attività {#copy-paste}

Puoi copiare una o più attività di un percorso e incollarle nello stesso percorso o in un&#39;altra. Ciò ti consente di risparmiare tempo se desideri riutilizzare numerose attività già configurate in un percorso precedente.

**Note importanti**

* Puoi copiare/incollare diverse schede e browser. Puoi copiare/incollare solo le attività all’interno della stessa istanza.
* Non è possibile copiare/incollare un evento se il percorso di destinazione dispone di un evento che utilizza uno spazio dei nomi diverso.
* Le attività inviate possono fare riferimento a dati non esistenti nel percorso di destinazione, ad esempio se copi/incolla tra diverse sandbox. Controlla sempre gli errori e apporta le regolazioni necessarie.
* Non è possibile annullare un’azione. Per eliminare le attività incollate, dovrai selezionarle ed eliminarle. Pertanto, accertati di selezionare solo le attività necessarie prima di copiarle.
* Puoi copiare le attività da qualsiasi percorso, anche da quelli in sola lettura.
* Puoi selezionare qualsiasi attività, anche se non collegata. Le attività collegate resteranno collegate dopo essere state incollate.

Di seguito sono riportati i passaggi per copiare/incollare le attività:

1. Apri un percorso.
1. Seleziona le attività da copiare spostando il mouse mentre fai clic. È inoltre possibile fare clic su ogni attività premendo il pulsante **Ctrl/Comando** chiave. Utilizzo **Ctrl/Comando + A** se desideri selezionare tutte le attività.
   ![](assets/copy-paste1.png)
1. Press **Ctrl/Comando + C**.
Se desideri copiare una sola attività, puoi fare clic su di essa e utilizzare la **Copia** in alto a sinistra nel riquadro di configurazione dell’attività.
   ![](assets/copy-paste2.png)
1. In qualsiasi percorso, premere **Ctrl/Comando + V** per incollare le attività senza collegarle a un nodo esistente. Le attività inviate vengono collocate nello stesso ordine. Dopo essere state incollate, le attività rimangono selezionate in modo da poterle spostare facilmente. È inoltre possibile posizionare il cursore su un segnaposto vuoto e premere **Ctrl/Comando + V**. Le attività inviate saranno collegate al nodo .
   ![](assets/copy-paste3.png)
