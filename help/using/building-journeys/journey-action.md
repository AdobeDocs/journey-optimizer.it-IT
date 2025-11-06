---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività percorso di azioni
description: Scopri come aggiungere un’attività Azione generica per configurare azioni singole e gruppi di azioni in entrata con più azioni all’interno dell’area di lavoro del percorso.
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: percorso, messaggio, push, sms, e-mail, in-app, web, scheda di contenuti, esperienza basata su codice
exl-id: 0ed97ffa-8efc-45a2-99ae-7bcb872148d5
version: Journey Orchestration
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 16%

---

# Utilizzare l’attività Azione {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_action_activity"
>title="Attività azione"
>abstract="L’attività **Azione** generica consente di configurare un’unica azione per il canale nativo e più attività in entrata con la possibilità di aggiungere l’ottimizzazione a qualsiasi azione del canale incorporata."

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

[!DNL Journey Optimizer] include una nuova attività **Action** generica che consente di configurare una singola azione di canale incorporata e più attività in entrata.

Consente di:

* Una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso.
* La capacità di creare gruppi di azioni in entrata con più azioni.
* La possibilità di aggiungere l’ottimizzazione a qualsiasi azione del canale incorporata.

>[!NOTE]
>
>Puoi anche impostare azioni personalizzate per inviare i messaggi in [!DNL Journey Optimizer]. [Ulteriori informazioni](#recommendation)

## Aggiungere un&#39;azione a un percorso  {#add-action}

Per aggiungere un’azione di canale incorporata a un percorso, segui la procedura riportata di seguito.

1. Avvia il percorso con un&#39;attività [Event](general-events.md) o [Read Audience](read-audience.md).

1. Dalla sezione **[!UICONTROL Azioni]** della palette, trascina e rilascia un&#39;attività **[!UICONTROL Azione]** nell&#39;area di lavoro.

1. Seleziona l’attività di canale incorporata che desideri sfruttare nel percorso.

   ![](assets/journey-action-type-cbe.png)

1. Aggiungi un&#39;etichetta all&#39;azione e seleziona **[!UICONTROL Configura azione]**.

   ![](assets/journey-action-configure.png){width="80%"}

1. Sei stato indirizzato alla scheda **[!UICONTROL Azioni]** della schermata di configurazione delle azioni di percorso.

   Seleziona la configurazione da utilizzare per il canale selezionato.

   ![](assets/journey-action-actions-tab.png)

1. Se hai selezionato un canale in entrata, puoi aggiungere più azioni. [Ulteriori informazioni](#multi-action)

1. Configura l’attività in base al canale selezionato. Scopri come configurare le azioni di canale integrate in [questa sezione](journeys-message.md).

1. Utilizza la sezione **[!UICONTROL Ottimizzazione]** per eseguire esperimenti di contenuto, sfruttare le regole di targeting o utilizzare combinazioni avanzate di sperimentazione e targeting.

   Queste diverse opzioni e i passaggi da seguire sono descritti in [questa sezione](../campaigns/campaigns-message-optimization.md).

1. Utilizza la sezione **[!UICONTROL Lingue]** per creare contenuti in più lingue all&#39;interno dell&#39;azione di percorso. A tale scopo, fare clic sul pulsante **[!UICONTROL Aggiungi lingue]** e selezionare le **[!UICONTROL impostazioni lingua]** desiderate.

   Informazioni dettagliate su come impostare e utilizzare le funzionalità multilingue sono disponibili in [questa sezione](../content-management/multilingual-gs.md).

Sono disponibili impostazioni aggiuntive a seconda del canale di comunicazione selezionato. Per ulteriori informazioni, espandi le sezioni seguenti.

+++**Applica regole limite** (e-mail, direct mailing, push, SMS)

Nell&#39;elenco a discesa **[!UICONTROL Regole aziendali]**, selezionare un set di regole per applicare le regole di limitazione di utilizzo all&#39;azione di percorso.

L’utilizzo dei set di regole di canale consente di impostare i limiti di frequenza per tipo di comunicazione per evitare di sovraccaricare i clienti con messaggi simili.

[Scopri come utilizzare i set di regole](../conflict-prioritization/rule-sets.md)

+++

+++**Rileva coinvolgimento** (e-mail, SMS).

Utilizza la sezione **[!UICONTROL Tracciamento delle azioni]** per tenere traccia di come i destinatari reagiscono alle consegne e-mail o SMS.

I risultati del tracciamento sono accessibili dal rapporto sul percorso una volta che il percorso è stato eseguito.

[Ulteriori informazioni sui report di percorso](../reports/journey-global-report-cja.md)

+++

+++**Attiva modalità Consegna rapida** (Push).

La modalità Consegna rapida è un componente aggiuntivo [!DNL Journey Optimizer] che consente l&#39;invio molto rapido di messaggi push in volumi elevati tramite campagne.

La consegna rapida viene utilizzata quando il ritardo nella consegna dei messaggi è di importanza critica per l’azienda, quando si desidera inviare un avviso push urgente sui telefoni cellulari, ad esempio una notizia straordinaria agli utenti che hanno installato la tua app per il canale news.

Scopri come abilitare la modalità Consegna rapida per le notifiche push [&#x200B; in questa pagina](../push/create-push.md#rapid-delivery).

Per ulteriori informazioni sulle prestazioni durante l’utilizzo della modalità Consegna rapida, consulta la [descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++**Assegna punteggi di priorità** (Web, In-app, basati su codice)

Nella sezione **[!UICONTROL Gestione dei conflitti]**, è possibile assegnare un punteggio di priorità all&#39;azione di percorso, consentendo di assegnare un&#39;azione in entrata quando sono presenti più azioni di percorso o campagne che utilizzano la stessa configurazione di canale.

Per impostazione predefinita, il punteggio di priorità per l’azione viene ereditato da quello complessivo relativo al percorso.

[Scopri come assegnare punteggi di priorità alle azioni del canale](../conflict-prioritization/priority-scores.md#priority-action)

+++

+++**Imposta regole di consegna aggiuntive** (schede contenuto)

Per i percorsi di schede di contenuto, puoi abilitare regole di consegna aggiuntive per scegliere gli eventi e i criteri che attivano il messaggio.

[Scopri come creare schede di contenuto](../content-card/create-content-card.md)

+++

+++**Definisci trigger** (in-app)

Per i messaggi in-app, puoi utilizzare il pulsante **[!UICONTROL Modifica trigger]** per scegliere gli eventi e i criteri che attivano il messaggio.

[Scopri come creare un messaggio in-app](../in-app/create-in-app.md)

+++

## Aggiungere più azioni in entrata {#multi-action}

>[!CONTEXTUALHELP]
>id="ajo_multi_action_journey"
>title="Aggiungere più azioni in entrata"
>abstract="Puoi selezionare diverse azioni in entrata all’interno di un singolo percorso. Questa funzionalità consente di consegnare più esperienze basate su codice, messaggi in-app, schede di contenuto o azioni web in diverse posizioni contemporaneamente, ciascuna con contenuti specifici."

Per semplificare l’orchestrazione del percorso, puoi definire diverse azioni in entrata all’interno di una singola azione del percorso.

>[!NOTE]
>
>Questa capacità è disponibile solo per i canali in entrata. Attualmente i canali in uscita come e-mail non sono supportati.

Questa capacità ti consente di fornire varie esperienze basate su codice, messaggi in-app, schede di contenuto o azioni web a posizioni diverse contemporaneamente, senza la necessità di creare più azioni di percorso. Semplifica l’implementazione del percorso e consente rapporti più fluidi, con tutti i dati consolidati in un unico percorso.

Ad esempio, puoi inviare un’esperienza basata su codice a più endpoint con contenuti leggermente diversi. A questo scopo, crea più azioni basate su codice all’interno della stessa azione di percorso, ciascuna con una configurazione di endpoint diversa.

Per definire più azioni in entrata in un singolo nodo di azione di percorso, segui i passaggi indicati di seguito.

1. Avvia il percorso con un&#39;attività [Event](general-events.md) o [Read Audience](read-audience.md).

1. Dalla sezione **[!UICONTROL Azioni]** della palette, trascina e rilascia un&#39;attività **[!UICONTROL Azione]** nell&#39;area di lavoro.

1. Seleziona **[!UICONTROL Azione multipla]** come tipo di azione.

   ![](assets/journey-multi-action.png)

1. Aggiungi un&#39;etichetta se necessario e seleziona **[!UICONTROL Configura azione]**.

   ![](assets/journey-multi-action-configure.png){width="60%"}

1. Sei stato indirizzato alla scheda **[!UICONTROL Azioni]** della schermata di configurazione delle azioni di percorso.

   ![](assets/journey-multi-action-configuration.png){width="70%"}

1. Seleziona un&#39;azione in entrata (**Esperienza basata su codice**, **Messaggio in-app**, **Scheda contenuto** o **Web**) dalla sezione **[!UICONTROL Azioni]**.

1. Seleziona la configurazione del canale e definisci un contenuto specifico per tale azione.

1. Utilizza il pulsante **[!UICONTROL Aggiungi azione]** per selezionare un&#39;altra azione in entrata dall&#39;elenco a discesa.

   ![](assets/journey-multi-action-add.png){width="80%"}

1. Procedi in modo simile per aggiungere altre azioni. Puoi aggiungere fino a 10 azioni in entrata in un percorso di azioni di gruppo.

Una volta che il percorso è [live](publish-journey.md), tutte le azioni vengono attivate contemporaneamente.
<!--
## Next steps {#next}

Once your action is configured, you can design its content. [Learn more]-->
