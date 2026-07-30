---
title: Creare le regole
description: Scopri come utilizzare le regole
feature: Decisioning, Campaigns, Journeys, Activities
topic: Integrations, Content Management
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/yfeFpaNi0rYVeyXdzaZ7SfoZnu-BkyivCMDzED7dpsM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: de2272c6d570047cd386941cd2e38cf82942c029
workflow-type: tm+mt
source-wordcount: 1619
ht-degree: 9%

---

# Creare le regole {#rules}

>[!BEGINSHADEBOX]

**In questa pagina:** crea regole di decisione riutilizzabili e di targeting, in modo da poter controllare quali elementi di decisione e contenuti personalizzati vengono visualizzati a quali tipi di pubblico nelle campagne e nei percorsi.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Creare le regole"
>abstract="Puoi creare due tipi di regole: **regole di decisione** che possono essere utilizzate in elementi decisionali o strategie di selezione, per controllare quali elementi devono essere presentati a quale pubblico; oppure **regole di targeting** per determinare segmenti di pubblico specifici qualificati per ricevere contenuti personalizzati o per entrare in un percorso specifico.<br/><br/>Durante la creazione di una regola di decisione, puoi selezionare **[!UICONTROL Abilita ricerca nel set di dati]** per utilizzare i dati di Adobe Experience Platform. Questo ti consente di definire criteri di idoneità in base ad attributi esterni dinamici, in modo che vengano mostrati solo gli elementi decisionali pertinenti."

## Informazioni sulle regole {#about}

In [!DNL Journey Optimizer] è possibile creare due tipi di regole riutilizzabili:

* [Regole di decisione](#decision-rules)
* [Regole di targeting](#targeting-rules)

### Regole di decisione {#decision-rules}

Le regole di decisione ti consentono di definire il pubblico per gli elementi di decisione applicando vincoli, direttamente a livello di elemento di decisione o all’interno di una strategia di selezione specifica. Ciò consente di controllare con precisione quali elementi devono essere presentati a chi.

Ad esempio, consideriamo uno scenario in cui si hanno elementi decisionali con prodotti relativi allo yoga progettati per le donne. Con le regole di decisione, puoi specificare che questi elementi devono essere visualizzati solo ai profili il cui genere è &quot;Femmina&quot; e che hanno indicato un &quot;Punto di interesse&quot; in &quot;Yoga&quot;.

>[!NOTE]
>
>Oltre alle regole di decisione a livello di articolo e di strategia di selezione, puoi anche definire il pubblico a cui rivolgerti a livello di campagna. [Ulteriori informazioni](../campaigns/create-campaign.md#audience)

### Regole di targeting {#targeting-rules}

>[!AVAILABILITY]
>
>Le regole di targeting sono attualmente in disponibilità limitata. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.
>
>Questa funzionalità è disponibile solo per le organizzazioni che hanno acquistato il componente aggiuntivo **Decisioning**. Verrà introdotto progressivamente per tutti i clienti.

Le regole di targeting consentono di determinare le qualifiche specifiche che devono essere soddisfatte affinché un cliente sia idoneo a ricevere contenuti personalizzati o a immettere un percorso di percorso specifico, in base a segmenti di pubblico specifici, che consente di eseguire il targeting di pubblici secondari nei percorsi e nelle campagne.

Spesso si tratta di una combinazione di più attributi, oltre a eventi di comportamento del cliente e dati contestuali. Per risparmiare tempo e fatica, puoi creare regole di targeting una volta e riutilizzarle in tutti i tuoi percorsi e campagne, con la possibilità di modificarle rapidamente in linea al momento dell’authoring.

Puoi utilizzare queste regole:

* Durante la creazione di [targeting di ottimizzazione del contenuto](../building-journeys/path-targeting.md) in percorsi o campagne;
* Durante la creazione di [ottimizzazione del percorso di percorso](../building-journeys/path-targeting.md).

➡️ [Scopri questa funzione nel video](#video)

## Regole di accesso {#access}

L&#39;elenco delle regole è accessibile nel menu **[!UICONTROL Decisioning]** > **[!UICONTROL Imposta strategia]**.

Sono disponibili le seguenti azioni:

* Puoi filtrare in base all&#39;entità regola (**[!UICONTROL Elemento decisione]** o **[!UICONTROL Impostazione destinazione]** - [Ulteriori informazioni](#about)).

* Seleziona una regola facendo clic sul nome e modificala utilizzando il generatore di regole. [Scopri come](#create)

* Dal pulsante **[!UICONTROL Altre azioni]** accanto a ogni elemento, puoi effettuare le seguenti operazioni:

  * Se hai selezionato l&#39;entità **[!UICONTROL Elemento decisione]**, aggiungi la regola a un pacchetto per esportarla in un&#39;altra sandbox. Scopri come [esportare gli oggetti in un&#39;altra sandbox](../configuration/copy-objects-to-sandbox.md).
  * Duplica una regola.
  * Eliminare una regola.

![](assets/rules-list.png){width=100%}

* Fai clic sull&#39;icona **[!UICONTROL Ulteriori informazioni]** per visualizzare la formula che costituisce la regola.

![](assets/rule-formula.png){width=60%}

## Creare una regola {#create}

Per creare una regola, effettua le seguenti operazioni:

1. Passa a **[!UICONTROL Decisioning]** > **[!UICONTROL Configurazione strategia]** > **[!UICONTROL Regole]**, quindi fai clic sul pulsante **[!UICONTROL Crea regola]**.

1. Nella finestra di dialogo **[!UICONTROL Crea regola]**, scegli una delle seguenti schede:

   * **[!UICONTROL Crea da zero]** per continuare nel flusso di creazione della regola.
   * **[!UICONTROL Crea con IA]** per utilizzare l&#39;authoring basato su IA. Descrivi la regola da creare, quindi conferma. L’utente viene reindirizzato al generatore di regole e l’Assistente AI genera un suggerimento di regole nel riquadro a destra. Per ulteriori informazioni su come generare una regola utilizzando l&#39;intelligenza artificiale, consulta [Creare una regola con intelligenza artificiale](#build-rule-with-ai) sezione.

     >[!NOTE]
     >
     >Questa funzionalità è disponibile per le organizzazioni con accesso alle funzionalità di Adobe AI.

1. Se si sceglie **[!UICONTROL Crea da zero]**, selezionare l&#39;entità regola per specificare il tipo di oggetto per cui viene creata la regola.

   ![](assets/rules-select-entity.png){width=90%}

   * **[!UICONTROL Elemento decisione]** - La regola può essere applicata a un [elemento decisione](#decision-rules) nel contesto di Decisioning;
   * **[!UICONTROL Targeting]** - La regola può essere utilizzata durante la creazione di [regole di targeting](#targeting-rules), come parte della [ottimizzazione del contenuto](../building-journeys/path-targeting.md) in una campagna o in un percorso, nell&#39;attività [Ottimizza percorso](../building-journeys/path-targeting.md).

   Se crei una regola di tipo **[!UICONTROL Elemento decisione]**, puoi selezionare **[!UICONTROL Abilita ricerca set di dati]** per utilizzare i dati di Adobe Experience Platform per arricchire la logica decisionale con dati esterni. Questa funzione è particolarmente utile per gli attributi che cambiano frequentemente, ad esempio la disponibilità del prodotto o il prezzo in tempo reale. [Scopri come utilizzare i dati di Adobe Experience Platform per prendere decisioni](../experience-decisioning/aep-data-exd.md)

1. Viene visualizzata la schermata di creazione della regola. Denomina la regola e fornisci una descrizione.

1. Crea la regola in base alle tue esigenze utilizzando il Generatore di segmenti di Adobe Experience Platform. A questo scopo, puoi sfruttare diverse origini dati, ad esempio:
   * Attributi del profilo;
   * Attributi degli elementi di decisione - disponibili solo durante la creazione di una regola **[!UICONTROL Elemento di decisione]**;
   * Pubblico;
   * Dati contestuali provenienti da Adobe Experience Platform. [Scopri come sfruttare i dati contestuali](context-data.md)

   ![](assets/decision-rules-build.png){width=85%}

   >[!NOTE]
   >
   >Il Generatore di segmenti fornito per la creazione di regole presenta alcune specificità rispetto a quello utilizzato con il servizio di segmentazione di Adobe Experience Platform. Tuttavia, il processo globale descritto nella documentazione è valido per la generazione di regole in [!DNL Journey Optimizer]. [Scopri come creare le definizioni dei segmenti](../audience/creating-a-segment-definition.md)

1. Durante l&#39;aggiunta e la configurazione di nuovi campi nell&#39;area di lavoro, nel riquadro **[!UICONTROL Proprietà pubblico]** vengono visualizzate informazioni sui profili stimati appartenenti al pubblico. Fai clic su **[!UICONTROL Aggiorna stima]** per aggiornare i dati.

   ![](assets/decision-rule-audience-properties.png){width=85%}

   >[!NOTE]
   >
   >Le stime del profilo non sono disponibili quando i parametri della regola includono dati non memorizzati nel profilo, come i dati contestuali.

1. Quando la regola è pronta, fai clic su **[!UICONTROL Crea]**. La regola creata viene visualizzata nell&#39;elenco e, a seconda dell&#39;entità creata, è disponibile per l&#39;uso:

   * In **elementi decisionali** e **strategie di selezione** per gestire la presentazione degli elementi decisionali ai profili;
   * Oppure durante la creazione di **targeting** nell&#39;ottimizzazione del contenuto o del percorso.

>[!NOTE]
>
>La profondità di nidificazione in una regola è limitata a 30 livelli. Questo viene misurato contando le parentesi di chiusura `)` nella stringa PQL.
>
>Una stringa di regola può avere dimensioni fino a 15 KB per caratteri con codifica UTF-8. Equivale a 15.000 caratteri ASCII (1 byte ciascuno) o 3.750-7.500 caratteri non ASCII (2-4 byte ciascuno).
>
>[Ulteriori informazioni sulle regole di idoneità Guardrail e limitazioni](decisioning-guardrails.md#eligibility-rules)

## Creare una regola con IA {#build-rule-with-ai}

>[!NOTE]
>
>Questa funzionalità è disponibile per le organizzazioni con accesso alle funzionalità di Adobe AI. È disponibile solo per un insieme di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.
>
>Al momento, la generazione di regole assistite da IA non supporta la generazione di espressioni basate su dati di contesto di Percorso.

Puoi avviare l’authoring di regole assistite da IA da due posizioni:

* Dalla finestra di dialogo Crea regola, nella scheda **[!UICONTROL Crea con IA]**:

  ![](assets/rule-ai-create.png){width=85%}

* Dal generatore di regole, utilizzando il pulsante **[!UICONTROL Assistente AI]**.

  ![](assets/rule-ai-generate.png){width=85%}

Nel riquadro Assistente AI, descrivi la regola da generare in linguaggio semplice. L’Assistente AI genera un suggerimento di regole che puoi applicare al generatore o eliminare.

![](assets/rule-ai-generate-prompt.png)

>[!CAUTION]
>
>Quando fai clic su **[!UICONTROL Applica al generatore]**, la regola generata dall&#39;intelligenza artificiale sostituisce qualsiasi logica di regola esistente attualmente generata nell&#39;area di lavoro del generatore.

## Simulare la regola {#simulate-rules}

Prima di utilizzare una regola nella strategia decisionale o nella campagna, puoi testarla con dati di esempio o generati per convalidare la logica della regola e assicurarti che si comporti come previsto.

1. Apri una regola esistente o [creane una nuova](#create), quindi fai clic sul pulsante **[!UICONTROL Simula regola]**.

   ![](assets/rule-simulate-button.png)


1. Viene visualizzata la schermata di simulazione con diverse sezioni:

   ![](assets/rule-simulate-new.png)

   * **Varianti test**: dove si generano o si creano varianti test manuali
   * **Espressione regola**: visualizza la definizione della regola per il riferimento
   * **Risultato simulazione**: indica se il profilo sarà idoneo o meno da questa regola

1. Aggiungi varianti di test con gli attributi richiesti dalla regola utilizzando uno dei due metodi seguenti:
   * Per creare un campione manuale, selezionare il pulsante **[!UICONTROL Crea campione]**.
   * Per generare varianti di test utilizzando l&#39;intelligenza artificiale, fare clic sul pulsante **[!UICONTROL Genera]**.

>[!NOTE]
>
>La generazione di varianti di test basate sull’intelligenza artificiale è disponibile per le organizzazioni con accesso alle funzionalità di Adobe AI.

La sezione Varianti di test viene compilata automaticamente con i campioni creati o generati. Ogni variante include gli attributi utilizzati nella regola. Puoi modificare direttamente i valori dei campi per simulare scenari diversi.

Per visualizzare i risultati della valutazione della regola, seleziona una variante di test dall’elenco. L’area dei risultati della simulazione mostra se il profilo sarà idoneo o meno in base a questa regola.

Nell&#39;esempio seguente, la prima variante di test mostra un risultato della simulazione **[!UICONTROL Pass]**, mentre la seconda variante di test mostra un risultato **[!UICONTROL Failed]**.

| Passa esempio | Esempio non riuscito |
| --- | --- |
| ![](assets/rule-simulate-pass.png) | ![](assets/rule-simulate-fail.png) |
| I dati della variante soddisfano tutte le condizioni della regola, pertanto il profilo è idoneo per la regola. | Una o più condizioni non sono soddisfatte, pertanto il profilo non è idoneo per la regola. |

## Ottimizzazione delle regole basate su AI {#optimize}

[!DNL Journey Optimizer] può analizzare automaticamente le regole e suggerire semplificazioni che mantengono la logica originale. Sono idonee solo le regole con espressione PQL di dimensioni superiori a **2 KB** (codifica UTF-8). Le espressioni più piccole non vengono analizzate. Quando viene trovata una semplificazione, accanto alla regola nell&#39;inventario viene visualizzato un indicatore rosso **[!UICONTROL Ottimizza]**.

>[!NOTE]
>
>L&#39;ottimizzazione delle regole basate sull&#39;intelligenza artificiale si basa sulle stesse funzionalità di intelligenza artificiale generative di **Generate Content** e utilizza gli stessi controlli di accesso. Agli utenti deve essere concessa l&#39;autorizzazione **[!UICONTROL Generate Content]** per la risorsa **[!UICONTROL AI Assistant]**. Per ulteriori informazioni, vedere [Generazione contenuto di Access](../content-management/gs-generative.md#generative-access).

![](assets/decision-rules-ai.png)

Per ottimizzare una regola:

1. Nell’inventario delle regole, fai clic sull’icona dell’indicatore rosso accanto al nome della regola.

1. Viene visualizzata la finestra **[!UICONTROL Ottimizza]**, con l&#39;espressione PQL originale e la versione suggerita dall&#39;intelligenza artificiale.

   ![](assets/decision-rules-ai-details.png)

1. Per verificare che entrambe le espressioni si comportino in modo identico, fare clic su **[!UICONTROL Scarica analisi di ottimizzazione (TSV)]** per scaricare un file che mostra il modo in cui i profili simulati vengono valutati rispetto a ogni versione.

1. Al termine, fare clic su **[!UICONTROL Applica]** per sostituire l&#39;espressione originale con quella ottimizzata.

## Video introduttivo {#video}

Scopri come creare, duplicare e applicare **regole di targeting** riutilizzabili in Adobe Journey Optimizer per personalizzare in modo efficiente le campagne in base agli attributi del cliente come area geografica, lingua e comportamento, risparmiando tempo e migliorando la precisione del pubblico.

>[!VIDEO](https://video.tv.adobe.com/v/3476127/?quality=12)
