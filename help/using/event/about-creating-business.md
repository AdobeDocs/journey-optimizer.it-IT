---
title: Configurare un evento aziendale
description: Scopri come creare un evento aziendale
source-git-commit: 4464ea7169424c1ec6212394b8bda79a9bec1913
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 14%

---

# Configurare un evento aziendale {#configure-a-business-event}

![](../assets/do-not-localize/badge.png)

A differenza degli eventi unitari, gli eventi aziendali non sono collegati a un profilo specifico. Il tipo di ID evento è sempre basato su regole. Per ulteriori informazioni sugli eventi aziendali, consulta [questa sezione](../event/about-events.md).

I percorsi basati su segmenti di lettura possono essere attivati in una sola volta, da un programmatore regolarmente o da un evento aziendale, quando si verifica l’evento.

Gli eventi di business possono essere &quot;un prodotto è di nuovo in magazzino&quot;, &quot;il prezzo delle azioni di un&#39;azienda raggiunge un certo valore&quot;, ecc.

## Note importanti

* Lo schema dell&#39;evento deve contenere un&#39;identità primaria.
* Gli eventi aziendali possono essere eliminati solo come primo passo di un percorso.
* Quando si rilascia un evento business come primo passaggio di un percorso, il tipo di pianificazione del percorso sarà &quot;evento business&quot;.
* Solo un’attività di segmento di lettura può essere rilasciata dopo un evento aziendale. Viene aggiunto automaticamente come passaggio successivo.
* Gli eventi aziendali non possono essere attivati più di un&#39;ora.
* Dopo l’attivazione di un evento aziendale, si verifica un ritardo nell’esportazione del segmento da 15 minuti a un’ora.
* Quando si esegue il test di un evento aziendale, è necessario trasmettere i parametri dell&#39;evento e l&#39;identificatore del profilo di test che immetterà il percorso nel test. Inoltre, quando esegui il test di un percorso basato su eventi aziendali, puoi attivare solo l’ingresso a un singolo profilo. Vedi [questa sezione](../building-journeys/testing-the-journey.md#test-business). In modalità di test non è disponibile la modalità &quot;Vista codice&quot;.
* Cosa succede agli individui che si trovano attualmente nel percorso se arriva un nuovo evento di business? Si comporta come quando gli individui si trovano ancora in un percorso ricorrente quando si verifica una nuova ricorrenza. Il loro percorso è finito. Di conseguenza, gli esperti di marketing devono prestare attenzione a evitare di generare percorsi troppo lunghi se si aspettano eventi di business frequenti.

## Guida introduttiva agli eventi aziendali

Di seguito sono riportati i primi passaggi per configurare un evento aziendale:

1. Nella sezione AMMINISTRAZIONE, seleziona **[!UICONTROL Configurations]**, quindi fai clic su **[!UICONTROL Events]**. Viene visualizzato l’elenco degli eventi.

   ![](../assets/jo-event1.png)

1. Per creare un nuovo evento, fai clic su **[!UICONTROL Add]**. Il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

   ![](../assets/jo-event2.png)

1. Inserisci il nome dell’evento. Puoi anche aggiungere una descrizione.

   ![](../assets/jo-event3-business.png)

   >[!NOTE]
   >
   >Non utilizzare spazi o caratteri speciali. Non usare più di 30 caratteri.

1. Nel campo **[!UICONTROL Type]**, scegli **Business**.

   ![](../assets/jo-event3bis-business.png)

1. Il numero di percorsi che utilizzano questo evento viene visualizzato nel campo **[!UICONTROL Used in]**. Puoi fare clic sull’icona **[!UICONTROL View journeys]** per visualizzare l’elenco dei percorsi che utilizzano questo evento.

1. Definisci i campi dello schema e del payload: in questo punto è possibile selezionare le informazioni sull’evento (solitamente denominato payload) che i percorsi prevedono di ricevere. Potrai quindi utilizzare queste informazioni nel tuo percorso. Vedi [questa sezione](../event/about-creating-business.md#define-the-payload-fields).

   ![](../assets/jo-event5-business.png)

   Sono disponibili solo gli schemi di serie temporali. Gli schemi Eventi esperienza, Eventi decisionali e Eventi di Percorso non sono disponibili. Lo schema dell&#39;evento deve contenere un&#39;identità primaria.

   ![](../assets/test-profiles-4.png)

1. Fai clic all’interno del campo **[!UICONTROL Event ID condition]** . Utilizzando l’editor di espressioni semplici, definisci la condizione che verrà utilizzata dal sistema per identificare gli eventi che attiveranno il percorso.
   ![](../assets/jo-event6-business.png)

   Nel nostro esempio, abbiamo scritto una condizione basata sull’ID del prodotto. Ciò significa che ogni volta che il sistema riceve un evento che corrisponde a questa condizione, lo trasmette ai percorsi.

1. Fai clic su **[!UICONTROL Save]**.

   ![](../assets/journey7-business.png)

   L’evento è ora configurato e pronto per essere rilasciato in un percorso. Per poter ricevere gli eventi sono necessari ulteriori passaggi di configurazione. Consulta [questa pagina](../event/additional-steps-to-send-events-to-journey-orchestration.md).

## Definire i campi payload {#define-the-payload-fields}

La definizione del payload ti consente di scegliere le informazioni che il sistema prevede di ricevere dall’evento nel tuo percorso e la chiave per identificare quale persona è associata all’evento. Il payload si basa sulla definizione del campo XDM di Experience Cloud. Per ulteriori informazioni su XDM, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).

1. Seleziona uno schema XDM dall’elenco e fai clic sul campo **[!UICONTROL Payload]** o sull’icona **[!UICONTROL Edit]**.

   ![](../assets/journey8-business.png)

   Vengono visualizzati tutti i campi definiti nello schema. L’elenco dei campi varia da uno schema all’altro. È possibile cercare un campo specifico o utilizzare i filtri per visualizzare tutti i nodi e i campi o solo i campi selezionati. In base alla definizione dello schema, alcuni campi possono essere obbligatori e preselezionati. Non è possibile deselezionarli. Per impostazione predefinita, tutti i campi obbligatori affinché l’evento possa essere ricevuto correttamente dai percorsi sono selezionati.

   ![](../assets/journey9-business.png)

1. Seleziona i campi che si prevede di ricevere dall’evento. Questi sono i campi che l&#39;utente aziendale sfrutterà nel percorso.

   ![](../assets/journey10-business.png)

1. Dopo aver selezionato i campi necessari, fai clic su **[!UICONTROL Save]** o premi **[!UICONTROL Enter]**.

   Il numero di campi selezionati viene visualizzato nel campo **[!UICONTROL Payload]** .

   ![](../assets/journey12-business.png)

## Anteprima del payload {#preview-the-payload}

L’anteprima del payload ti consente di convalidare la definizione del payload.

1. Fai clic sull&#39;icona **[!UICONTROL View Payload]** per visualizzare in anteprima il payload previsto dal sistema.

   ![](../assets/journey13-business.png)

   I campi selezionati vengono visualizzati.

   ![](../assets/journey14-business.png)

1. Seleziona l’anteprima per convalidare la definizione del payload.

1. Quindi, puoi condividere l’anteprima del payload con la persona responsabile dell’invio dell’evento. Questo payload può aiutarlo a progettare la configurazione di un evento che preme su [!DNL Journey Optimizer]. Consulta [questa pagina](../event/additional-steps-to-send-events-to-journey-orchestration.md).
