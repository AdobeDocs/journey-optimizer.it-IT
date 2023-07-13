---
solution: Journey Optimizer
product: journey optimizer
title: Eventi di qualificazione del pubblico
description: Scopri gli eventi di qualificazione del pubblico
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: qualificazione, eventi, pubblico, percorso, piattaforma
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Eventi di qualificazione del pubblico {#segment-qualification}

## Informazioni sugli eventi di qualificazione del pubblico{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Eventi di qualificazione del pubblico"
>abstract="Questa attività consente al percorso di ascoltare le entrate e le uscite dei profili nei tipi di pubblico di Adobe Experience Platform per consentire a singoli utenti di entrare o proseguire in un percorso."

Questa attività consente al percorso di ascoltare le entrate e le uscite dei profili nei tipi di pubblico di Adobe Experience Platform per consentire a singoli utenti di entrare o proseguire in un percorso. Per ulteriori informazioni sulla creazione di tipi di pubblico, consulta questa [sezione](../audience/about-audiences.md).

Supponiamo che tu abbia un pubblico di tipo &quot;cliente silver&quot;. Con questa attività, puoi fare in modo che tutti i nuovi clienti silver entrino in un percorso e inviino loro una serie di messaggi personalizzati.

Questo tipo di evento può essere posizionato come primo passaggio o successivamente nel percorso.

>[!IMPORTANT]
>
>Tieni presente che i tipi di pubblico di Adobe Experience Platform vengono calcolati una volta al giorno (**batch** pubblico) o in tempo reale (**streaming** pubblico, utilizzando l&#39;opzione Tipi di pubblico ad alta frequenza di Adobe Experience Platform).
>
>Se il pubblico selezionato viene inviato in streaming, gli utenti appartenenti a questo pubblico potrebbero entrare nel percorso in tempo reale. Se il pubblico è batch, le persone appena qualificate per questo pubblico entreranno potenzialmente nel percorso quando il calcolo del pubblico viene eseguito su Adobe Experience Platform.
>
>I gruppi di campo di evento esperienza non possono essere utilizzati in percorsi che iniziano con un’attività Read audience, Audience Qualification o Business Event.


1. Espandi la **[!UICONTROL Eventi]** categoria e rilascia una **[!UICONTROL Qualificazione del pubblico]** attività nell’area di lavoro.

   ![](assets/segment5.png)

1. Aggiungi un **[!UICONTROL Etichetta]** all’attività. Questo passaggio è facoltativo.

1. Fai clic su nella **[!UICONTROL Pubblico]** e selezionare i tipi di pubblico da sfruttare.

   >[!NOTE]
   >
   >Si noti che è possibile personalizzare le colonne visualizzate nell&#39;elenco e ordinarle.

   ![](assets/segment6.png)

   Una volta aggiunto il pubblico, il **[!UICONTROL Copia]** consente di copiarne nome e ID:

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. In **[!UICONTROL Comportamento]** , scegli se desideri ascoltare le entrate, le uscite o entrambi i tipi di pubblico.

   >[!NOTE]
   >
   >Tieni presente che **[!UICONTROL Invio]** e **[!UICONTROL Esci]** corrisponde al **Realizzato** e **Uscita** stati di partecipazione del pubblico da Adobe Experience Platform. Per ulteriori informazioni su come valutare un pubblico, consulta [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. Seleziona uno spazio dei nomi. Questa opzione è necessaria solo se l’evento è posizionato come primo passaggio del percorso. Per impostazione predefinita, il campo è precompilato con l’ultimo spazio dei nomi utilizzato.

   >[!NOTE]
   >
   >È possibile selezionare solo uno spazio dei nomi delle identità basato su persone. Se hai definito uno spazio dei nomi per una tabella di ricerca (ad esempio: Spazio dei nomi ProductID per una ricerca di prodotto), questo non sarà disponibile nella **Namespace** elenco a discesa.

   ![](assets/segment7.png)

Il payload contiene le seguenti informazioni contestuali, che è possibile utilizzare in condizioni e azioni:

* il comportamento (entrata, uscita)
* il timestamp della qualifica
* l’id del pubblico

Quando si utilizza l’editor di espressioni in una condizione o azione che segue un **[!UICONTROL Qualificazione del pubblico]** attività, puoi accedere al **[!UICONTROL AudienceQualification]** nodo. È possibile scegliere tra **[!UICONTROL Ora ultima qualifica]** e **[!UICONTROL stato]** (entrata o uscita).

Consulta [Attività condizione](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Un nuovo percorso che include un evento di qualificazione del pubblico è operativo dieci minuti dopo la pubblicazione. Questo intervallo di tempo corrisponde all&#39;intervallo di aggiornamento della cache del servizio dedicato. Pertanto, è necessario attendere dieci minuti prima di utilizzare questo percorso.

## Best practice {#best-practices-segments}

Il **[!UICONTROL Qualificazione del pubblico]** L’attività consente l’ingresso immediato in percorsi di persone che si qualificano o squalificano da un pubblico Adobe Experience Platform.

La velocità di ricezione di queste informazioni è elevata. Le misurazioni effettuate mostrano una velocità di 10.000 eventi ricevuti al secondo. Di conseguenza, è necessario assicurarsi di capire come possono verificarsi picchi di ingresso, come evitarli e come rendere il percorso pronto per loro.

### Pubblico in batch{#batch-speed-segment-qualification}

Quando utilizzi la qualificazione del pubblico per un pubblico batch, tieni presente che un picco di ingresso si verificherà al momento del calcolo giornaliero. La dimensione del picco dipenderà dal numero di individui che entrano (o escono) dal pubblico ogni giorno.

Inoltre, se il pubblico batch è stato appena creato e immediatamente utilizzato in un percorso, il primo batch di calcolo potrebbe fare entrare nel percorso un numero molto elevato di individui.

### Tipi di pubblico in streaming{#streamed-speed-segment-qualification}

Quando si utilizza la qualificazione del pubblico per i tipi di pubblico in streaming, vi è meno rischio di ottenere picchi di entrate/uscite a causa della valutazione continua del pubblico. Tuttavia, se la definizione del pubblico porta a rendere un grande volume di clienti idonei allo stesso tempo, potrebbe esserci anche un picco.

Per ulteriori informazioni sulla segmentazione in streaming, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### Come evitare gli overload{#overloads-speed-segment-qualification}

Di seguito sono riportate alcune best practice che aiuteranno a evitare il sovraccarico dei sistemi utilizzati nei percorsi (origini dati, azioni personalizzate, attività di azione del canale).

Non utilizzare, in un **[!UICONTROL Qualificazione del pubblico]** attività, un pubblico batch immediatamente dopo la sua creazione. Eviterà il picco del primo calcolo. Se stai per utilizzare un pubblico che non è mai stato calcolato, nell’area di lavoro di percorso verrà visualizzato un avviso giallo.

![](assets/segment-error.png)

Inserisci una regola di limite per le origini dati e le azioni utilizzate nei percorsi per evitare di sovraccaricarle. Ulteriori informazioni in [Documentazione del Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. La regola di limite non ha alcun nuovo tentativo. Se devi riprovare, seleziona la casella e usa un percorso alternativo nel percorso **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o errore]** in condizioni o azioni.

Prima di utilizzare il pubblico in un percorso di produzione, valuta sempre per primo il volume di persone qualificate per questo pubblico ogni giorno. A questo scopo, puoi controllare il **[!UICONTROL Pubblico]** , apri il pubblico e osserva il **[!UICONTROL Profili nel tempo]** grafico.

![](assets/segment-overload.png)
