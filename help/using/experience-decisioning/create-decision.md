---
title: Creare criteri di decisioni
description: Scopri come creare criteri di decisioni
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: ed0c1b9f219b3b855aaac1a27b5ceb704d6f6d5e
workflow-type: tm+mt
source-wordcount: '2931'
ht-degree: 11%

---

# Creare criteri di decisione {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Che cos’è una decisione?"
>abstract="I criteri di decisione contengono tutta la logica di selezione affinché il motore decisionale possa scegliere il contenuto migliore. I criteri di decisione sono specifici della campagna. Il loro obiettivo è selezionare le migliori offerte per ciascun profilo mentre la creazione della campagna consente di indicare come devono essere presentati gli elementi decisionali selezionati, inclusi gli attributi degli elementi da includere nel messaggio."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Informazioni sulla funzione Decisioni"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="Definire un criterio di decisione"
>abstract="Un criterio di decisione consente di scegliere gli elementi migliori dal motore decisionale e di consegnarli al pubblico giusto."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Informazioni sulla funzione Decisioni"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="Criterio di decisione"
>abstract="Un criterio di decisione consente di scegliere gli elementi migliori dal motore decisionale e di consegnarli a ciascun pubblico."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="Posizionamento"
>abstract="Un posizionamento determina dove vengono visualizzati in un messaggio gli elementi restituiti dal motore decisionale. Puoi tenere traccia delle relative prestazioni in diversi posizionamenti nel reporting."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="Selezionare gli attributi di decisione dal catalogo"
>abstract="Gli attributi di decisione sono memorizzati nello schema del catalogo. Seleziona un attributo da utilizzare qui dal catalogo selezionato."

I criteri di decisione sono contenitori per le offerte che sfruttano il motore di decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico. Il loro obiettivo è quello di selezionare le offerte migliori per ciascun profilo, mentre l’authoring della campagna/del percorso ti consente di indicare in che modo devono essere presentati gli elementi decisionali selezionati, compresi gli attributi degli elementi da includere nel messaggio.

## Passaggi chiave {#key}

I passaggi principali per sfruttare i criteri decisionali nei messaggi sono i seguenti:

1. [Creare un criterio di decisione in un’esperienza basata su codice o in un’e-mail](#add-decision)

   Imposta un criterio di decisione nell’e-mail o nell’esperienza basata sul codice scegliendo il numero di elementi da restituire, configurando strategie di selezione, opzioni di fallback e ordine di valutazione.

1. [Utilizzare il criterio di decisione nel contenuto](#use-decision-policy)

   Personalizza il contenuto con l’output del criterio di decisione e gli attributi degli elementi di decisione che desideri visualizzare nel messaggio.

1. [Creare dashboard di reporting](cja-reporting.md)

   Crea dashboard di Customer Journey Analytics personalizzati per misurare le prestazioni e ottenere informazioni approfondite su come vengono distribuite e utilizzate le politiche e le offerte decisionali.

## Guardrail e limitazioni

* **Disponibilità limitata - Criteri di decisione nelle e-mail** - Per il momento, la creazione di criteri di decisione nelle e-mail è disponibile in Disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.
* **Pagine mirror** - Per il momento, gli elementi decisionali non vengono riprodotti nelle pagine mirror delle e-mail.
* **Tipo di tracciamento e collegamenti** - Per tenere traccia dei collegamenti generati dal decisioning, definiscili nello schema come &quot;Decisioning Assets&quot;. I collegamenti basati su attributi non sono tracciabili.
* **Nidificazione dei criteri di decisione nelle e-mail** - Non è possibile nidificare più criteri di decisione all&#39;interno di un componente e-mail principale a cui è già associato un criterio di decisione.
* **percorsi/campagne duplicati con decisioning** - Se duplichi un percorso o una campagna che include un criterio di decisione, la versione duplicata fa riferimento all&#39;e-mail o all&#39;esperienza basata su codice originale, causando errori. Riconfigura sempre il criterio di decisione dopo la duplicazione.
* **Criteri di consenso** - Gli aggiornamenti ai criteri di consenso richiedono fino a 48 ore per essere effettivi. Se un criterio di decisione fa riferimento a un attributo associato a un criterio di consenso aggiornato di recente, le modifiche non verranno applicate immediatamente.

  Analogamente, se a un criterio di decisione vengono aggiunti nuovi attributi di profilo soggetti a un criterio di consenso, questi saranno utilizzabili, ma il criterio di consenso associato a essi non verrà applicato fino a quando il ritardo non sarà passato.

  I criteri di consenso sono disponibili solo per le organizzazioni con il componente aggiuntivo Adobe Healthcare Shield o Privacy and Security Shield.

* **Classifica IA** - Per il momento, la classificazione IA non è supportata per il canale e-mail nei percorsi con decisioning.

## Creare un criterio di decisione in un’esperienza basata su codice o in un’e-mail {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Definire il numero di elementi da restituire"
>abstract="Seleziona il numero di elementi decisionali che desideri restituire. Ad esempio, se selezioni 2, verranno presentate le 2 offerte idonee migliori per la configurazione corrente."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Selezionare un fallback"
>abstract="L’utente visualizza un elemento di fallback quando nessuna delle strategie di selezione definite per tale criterio decisionale è qualificata."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="Che cos’è una strategia?"
>abstract="La sequenza della strategia di selezione determina quale strategia verrà valutata per prima. È necessaria almeno una strategia. Gli elementi decisionali nelle strategie combinate saranno valutati insieme."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Creare strategie"

Per presentare l’offerta e l’esperienza migliore e dinamica ai destinatari e ai visitatori delle e-mail sul sito web o sull’app mobile, aggiungi un criterio decisionale a un’e-mail o a una campagna o a un percorso basato su codice. A questo scopo, segui i passaggi riportati qui sotto.

### Creare un criterio di decisione {#add}

1. In un percorso o in una campagna, aggiungi un&#39;azione **[!UICONTROL E-mail]** o **[!UICONTROL Esperienza basata su codice]**.

1. Per le e-mail, attiva **[!UICONTROL Abilita decisioning]** nella schermata di configurazione.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >L’abilitazione del decisioning cancella il contenuto delle e-mail esistenti. Se hai già progettato l’e-mail, assicurati di salvare preventivamente il contenuto come modello.
   >
   >Eventuali criteri di decisione configurati all’interno dell’e-mail non verranno salvati nel modello. Se applichi il modello a un’altra e-mail, devi riconfigurare il criterio.

1. I criteri possono essere creati tramite e-mail ed esperienze basate su codice utilizzando l’editor di personalizzazione. Possono essere creati anche nelle e-mail da un menu dedicato nel Designer e-mail. Per ulteriori informazioni, espandi le sezioni seguenti.

   +++Editor Personalization

   1. Apri l&#39;editor di personalizzazione e seleziona **[!UICONTROL Criteri di decisione]**.
   1. Fare clic sul pulsante **[!UICONTROL Aggiungi criterio di decisione]** per creare un nuovo criterio.

      ![](assets/decision-code-based-create.png)

   +++

   +++Invia menu **[!UICONTROL Decisioning]** a Designer tramite e-mail

   1. Seleziona un componente, fai clic sull&#39;icona **[!UICONTROL Decisioning]** nella barra degli strumenti o nel riquadro delle proprietà, quindi seleziona **[!UICONTROL Aggiungi nuovo criterio]**.

   1. Selezionare **[!UICONTROL Riutilizza output decisione]** per riutilizzare un criterio di decisione già creato in questa e-mail.

      ![](assets/decision-policy-email-designer.png)

   +++

1. Specifica un nome e seleziona un catalogo (attualmente limitato al catalogo predefinito **[!UICONTROL Offerte]**).

1. Seleziona il numero di elementi da restituire. Ad esempio, se selezioni 2, verranno presentate le 2 offerte idonee migliori per la configurazione corrente.

   ![](assets/decision-code-based-details.png)

   Per le e-mail, è possibile restituire più elementi solo in un componente di contenuto **[!UICONTROL Ripeti griglia]**. Per ulteriori informazioni, espandi la sezione seguente:

   +++ Restituire più elementi decisionali nelle e-mail

   1. Trascina un componente **[!UICONTROL Ripeti griglia]** nell&#39;area di lavoro e configuralo come desiderato utilizzando il riquadro **[!UICONTROL Impostazioni]**.

      ![](assets/decision-policy-repeat.png)

   1. Fai clic sull&#39;icona **[!UICONTROL Decisioning]** nella barra degli strumenti dell&#39;area di lavoro oppure apri il riquadro **[!UICONTROL Decisioning]** e seleziona **[!UICONTROL Aggiungi criterio di decisione]**.

   1. Specifica il numero di elementi da restituire nel campo **[!UICONTROL Numero di elementi]**, quindi configura il criterio di decisione come documentato di seguito. Il numero massimo di elementi selezionabili è limitato dal numero di riquadri definito nel componente **[!UICONTROL Ripeti griglia]**.

   ![](assets/decision-policy-repeat-number.png)

   +++

1. Fai clic su **[!UICONTROL Avanti]**.

### Selezione di elementi e strategie di selezione {#select}

La sezione **[!UICONTROL Sequenza strategica]** consente di selezionare gli elementi decisionali e le strategie di selezione da presentare con il criterio decisionale.

1. Fare clic su **[!UICONTROL Aggiungi]** e scegliere il tipo di oggetto da includere nel criterio:

   * **[!UICONTROL Strategia di selezione]**: aggiungere una o più strategie di selezione. Le strategie decisionali sfruttano le raccolte associate ai vincoli di idoneità e ai metodi di classificazione per determinare gli elementi da mostrare. Puoi selezionare una strategia di selezione esistente o crearne una nuova utilizzando il pulsante **[!UICONTROL Crea strategia di selezione]**. [Scopri come creare strategie di selezione](selection-strategies.md)

   * **[!UICONTROL Elemento decisione]**: aggiungere singoli elementi decisione da presentare senza dover eseguire una strategia di selezione. È possibile selezionare un solo elemento di decisione alla volta. Eventuali vincoli di idoneità impostati per l’articolo verranno applicati.

   ![](assets/decision-code-based-strategy-sequence.png)

   >[!NOTE]
   >
   >Una politica decisionale supporta fino a 10 strategie di selezione e elementi decisionali combinati. [Ulteriori informazioni su guardrail e limitazioni di Decisioning](gs-experience-decisioning.md#guardrails)

1. Quando si aggiungono più elementi e/o strategie di decisione, queste vengono valutate in un ordine specifico. Il primo oggetto aggiunto alla sequenza verrà valutato per primo e così via. Per modificare la sequenza predefinita, trascinare e rilasciare gli oggetti e/o i gruppi per riordinarli in base alle esigenze. Per ulteriori informazioni, espandi la sezione seguente.

   +++Gestire l’ordine di valutazione in un criterio decisionale

   Dopo aver aggiunto al criterio elementi decisionali e strategie di selezione, è possibile disporne l&#39;ordine per determinarne l&#39;ordine di valutazione e combinare le strategie di selezione per valutarli insieme.

   L&#39;**ordine sequenziale** in cui verranno valutati gli elementi e le strategie è indicato con numeri alla sinistra di ogni oggetto o gruppo di oggetti. Per spostare la posizione di una strategia di selezione (o di un gruppo di strategie) all&#39;interno della sequenza, trascinarla e rilasciarla in un&#39;altra posizione.

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >Solo le strategie di selezione possono essere trascinate e rilasciate all&#39;interno di una sequenza. Per modificare la posizione di un elemento di decisione, è necessario rimuoverlo e aggiungerlo nuovamente utilizzando il pulsante **[!UICONTROL Aggiungi]** dopo aver aggiunto gli altri elementi che si desidera valutare in precedenza.

   È inoltre possibile **combinare** più strategie di selezione in gruppi in modo che vengano valutate insieme e non separatamente. A tale scopo, fare clic sul pulsante **`+`** in una strategia di selezione per combinarla con un&#39;altra. Puoi anche trascinare e rilasciare una strategia di selezione su un’altra per raggruppare le due strategie in un gruppo.

   >[!NOTE]
   >
   >Gli elementi decisionali non possono essere raggruppati con altri elementi o strategie di selezione.

   Le strategie multiple e il loro raggruppamento determinano la priorità delle strategie e la classificazione delle offerte idonee. La prima strategia ha la massima priorità e le strategie combinate all&#39;interno dello stesso gruppo hanno la stessa priorità.

   Ad esempio, sono disponibili due raccolte, una nella strategia A e una nella strategia B. La richiesta prevede il rinvio di due elementi decisionali. Supponiamo che vi siano due offerte ammissibili dalla strategia A e tre offerte ammissibili dalla strategia B.

   * Se le due strategie sono **non combinate** o in ordine sequenziale (1 e 2), le prime due offerte idonee della prima strategia verranno restituite nella prima riga. Se non ci sono due offerte idonee per la prima strategia, il motore decisionale passerà alla strategia successiva in sequenza per trovare quante offerte sono ancora necessarie e alla fine restituirà un fallback, se necessario.

     ![](assets/decision-code-based-consecutive-strategies.png)

   * Se le due raccolte sono **valutate contemporaneamente**, poiché esistono due offerte idonee dalla strategia A e tre offerte idonee dalla strategia B, le cinque offerte saranno tutte raggruppate in base al valore determinato dai rispettivi metodi di classificazione. Sono richieste due offerte, pertanto verranno restituite le prime due offerte idonee di queste cinque.

     ![](assets/decision-code-based-combined-strategies.png)

   **Esempio con più strategie**

   Prendiamo ora in considerazione un esempio in cui si dispone di più strategie suddivise in gruppi diversi. Hai definito tre strategie. La strategia 1 e la strategia 2 sono combinate nel gruppo 1 e la strategia 3 è indipendente (gruppo 2). Le offerte ammissibili per ciascuna strategia e la loro priorità (utilizzata nella valutazione della funzione di classificazione) sono le seguenti:

   * Gruppo 1:
      * Strategia 1 - (offerta 1, offerta 2, offerta 3) - Priorità 1
      * Strategia 2 - (offerta 3, offerta 4, offerta 5) - Priorità 1

   * Gruppo 2:
      * Strategia 3 - (Offerta 5, Offerta 6) - Priorità 0

   Le offerte di strategia con priorità più alta vengono valutate per prime e aggiunte all’elenco delle offerte classificate.

   * **Iterazione 1:**

     Le offerte di Strategia 1 e Strategia 2 vengono valutate insieme (Offerta 1, Offerta 2, Offerta 3, Offerta 4, Offerta 5). Supponiamo che il risultato sia:

     Offerta 1 - 10
Offerta 2 - 20
Offerta 3-30 dalla Strategia 1, 45 dalla Strategia 2. Il più alto di entrambi sarà considerato, quindi 45 è preso in considerazione.
Offerta 4 - 40
Offerta 5 - 50

     Le offerte classificate sono ora le seguenti: Offerta 5, Offerta 3, Offerta 4, Offerta 2, Offerta 1.

   * **Iterazione 2:**

     Vengono valutate le offerte della Strategia 3 (Offerta 5, Offerta 6). Supponiamo che il risultato sia:

      * Offerta 5: non verrà valutata perché esiste già nel risultato precedente.
      * Offerta 6 - 60

     Le offerte classificate sono ora le seguenti: Offerta 5 , Offerta 3, Offerta 4, Offerta 2, Offerta 1, Offerta 6.

   +++

1. Fai clic su **[!UICONTROL Avanti]**

### Aggiungere offerte di fallback {#fallback}

Dopo aver selezionato gli elementi decisionali e/o le strategie di selezione, puoi aggiungere offerte di fallback da visualizzare se nessuno degli elementi o delle strategie di selezione di cui sopra è qualificato.

È possibile selezionare qualsiasi elemento dall’elenco, in cui vengono visualizzati tutti gli elementi decisionali creati nella sandbox corrente. Se non viene definita alcuna strategia di selezione, il fallback viene visualizzato all&#39;utente indipendentemente dalle date e dal vincolo di idoneità applicato all&#39;elemento selezionato<!--nor frequency capping when available - TO CLARIFY-->.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> I fallback sono facoltativi. È possibile selezionare fino al numero di elementi richiesti. Se nessuna è idonea e non è impostato alcun fallback, non viene visualizzato nulla.

### Salvare e gestire i criteri di decisione {#save}

Quando il criterio decisionale è pronto, salvarlo e fare clic su **[!UICONTROL Crea]**.

Per le e-mail, devi definire un posizionamento per il componente associato al criterio decisionale. A tale scopo, fare clic sul pulsante **[!UICONTROL Decisioning]** nel riquadro delle proprietà del componente e selezionare **[!UICONTROL Assegna posizionamento]**. [Scopri come utilizzare i posizionamenti](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

Puoi modificare o eliminare un criterio di decisione in qualsiasi momento utilizzando il pulsante con i puntini di sospensione nell&#39;editor di personalizzazione o nel menu **[!UICONTROL Decisioning]** all&#39;interno del riquadro delle proprietà del componente.

>[!BEGINTABS]

>[!TAB Modifica o elimina un criterio dall&#39;editor di personalizzazione]

![](assets/decision-policy-edit.png)

>[!TAB Modifica o elimina un criterio dalle proprietà del componente]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## Utilizzare un criterio di decisione nel contenuto {#use-decision-policy}

Una volta creato, il criterio di decisione e gli attributi collegati agli elementi di decisione restituiti possono essere utilizzati nel contenuto per personalizzare il contenuto. Per farlo, segui la procedura riportata di seguito.

### Inserire il codice del criterio di decisione {#insert-code}

1. Apri l&#39;editor di personalizzazione e accedi al menu **[!UICONTROL Criteri di decisione]**.

1. Per le e-mail, fai clic su **[!UICONTROL Inserisci sintassi]** per aggiungere il codice corrispondente al criterio di decisione. Per le esperienze basate su codice, fare clic su **[!UICONTROL Inserisci criterio]**.

   +++Inserire il codice del criterio di decisione nelle e-mail

   ![](assets/decision-policy-add.png)

   Per le e-mail, se non è stato precedentemente associato alcun posizionamento al componente, selezionane uno dall&#39;elenco e fai clic su **[!UICONTROL Assegna]**.

   ![](assets/decision-policy-placement.png)

   +++

   +++Inserire il codice del criterio di decisione nell’esperienza basata su codice

   ![](assets/decision-code-based-add-decision.png)

   +++

   >[!NOTE]
   >
   >Se il pulsante di inserimento del codice non viene visualizzato, è possibile che per il componente principale sia già stato configurato un criterio di decisione.

1. Viene aggiunto il codice per il criterio di decisione. Questa sequenza verrà ripetuta il numero di volte che si desidera che venga restituito il criterio di decisione. Ad esempio, se si sceglie di restituire 2 elementi durante la [creazione della decisione](#add-decision), la stessa sequenza verrà ripetuta due volte.

### Sfruttare gli attributi degli elementi di decisione {#attributes}

Ora puoi aggiungere tutti gli attributi di decisione desiderati all’interno di tale codice. Gli attributi disponibili sono archiviati nello schema del catalogo **[!UICONTROL Offerte]**. Gli attributi personalizzati sono archiviati nella cartella **`_<imsOrg`>** e gli attributi standard nella cartella **`_experience`**. [Ulteriori informazioni sullo schema del catalogo delle offerte](catalogs.md)

![](assets/decision-code-based-decision-attributes.png)

>[!NOTE]
>
>Per il tracciamento degli elementi dei criteri di decisione, è necessario aggiungere l&#39;attributo `trackingToken` come segue per il contenuto dei criteri di decisione:
>&#x200B;>`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. Fai clic su ciascuna cartella per espanderla. Posizionare il cursore del mouse nella posizione desiderata e fare clic sull&#39;icona + accanto all&#39;attributo che si desidera aggiungere. Puoi aggiungere al codice tutti gli attributi che desideri.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Assicurarsi di racchiudere il loop `#each` in una coppia di parentesi quadre `[ ]` e aggiungere una virgola immediatamente prima del `/each` di chiusura.

   ![](assets/decision-code-based-wrap-code.png)

1. Puoi anche aggiungere qualsiasi altro attributo disponibile nell’editor di personalizzazione, ad esempio gli attributi del profilo.

   ![](assets/decision-code-based-decision-profile-attribute.png)

### Sfruttare i frammenti {#fragments}

Se il criterio di decisione contiene elementi di decisione, inclusi frammenti, puoi sfruttarli nel codice del criterio di decisione. [Ulteriori informazioni sui frammenti](../content-management/fragments.md)

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

Ad esempio, supponiamo che tu voglia visualizzare contenuti diversi per diversi modelli di dispositivi mobili. Accertati di aver aggiunto frammenti corrispondenti a tali dispositivi all’elemento decisionale utilizzato nel criterio di decisione. [Scopri come](items.md#attributes).

![](assets/item-fragments.png){width=70%}

Al termine, puoi utilizzare uno dei seguenti metodi:

>[!BEGINTABS]

>[!TAB Inserisci direttamente il codice]

È sufficiente copiare e incollare il blocco di codice riportato di seguito nel codice del criterio di decisione. Sostituisci `variable` con l&#39;ID frammento e `placement` con la chiave di riferimento frammento:

```
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
```

>[!TAB Segui i passaggi dettagliati]

1. Passare alle **[!UICONTROL Funzioni helper]** e aggiungere la funzione **Let** `{% let variable = expression %} {{variable}}` al riquadro del codice, in cui è possibile dichiarare la variabile per il frammento.

   ![](assets/decision-let-function.png)

1. Utilizza la **Mappa** > **Ottieni** funzione `{%= get(map, string) %}` per generare la tua espressione. La mappa è il frammento a cui si fa riferimento nell&#39;elemento di decisione e la stringa può essere il modello di dispositivo immesso nell&#39;elemento di decisione come **[!UICONTROL chiave di riferimento frammento]**.

   ![](assets/decision-map-function.png)

1. Puoi anche utilizzare un attributo contestuale che contenga questo ID modello dispositivo.

   ![](assets/decision-contextual-attribute.png)

1. Aggiungi la variabile scelta per il frammento come ID frammento.

   ![](assets/decision-fragment-id.png)

>[!ENDTABS]

L&#39;ID frammento e la chiave di riferimento verranno selezionati dalla sezione **[!UICONTROL Frammenti]** dell&#39;elemento di decisione.

>[!WARNING]
>
>Se la chiave del frammento non è corretta o se il contenuto del frammento non è valido, il rendering non riuscirà e verrà generato un errore nella chiamata di Edge.

#### Guardrail quando si utilizzano frammenti {#fragments-guardrails}

**Attributi di contesto ed elemento della decisione**

Gli attributi degli elementi decisionali e gli attributi contestuali non sono supportati per impostazione predefinita nei frammenti [!DNL Journey Optimizer]. Tuttavia, puoi utilizzare in alternativa le variabili globali, come descritto di seguito.

Supponiamo che desideri utilizzare la variabile *sport* nel frammento.

1. Fai riferimento a questa variabile nel frammento, ad esempio:

   ```
   Elevate your practice with new {{sport}} gear!
   ```

1. Definisci la variabile con la funzione **Let** all&#39;interno del blocco dei criteri di decisione. Nell&#39;esempio seguente, *sport* è definito con l&#39;attributo elemento decisione:

   ```
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

**Convalida del contenuto del frammento di elemento decisione**

* A causa della natura dinamica di questi frammenti, quando vengono utilizzati in una campagna, la convalida del messaggio durante la creazione del contenuto della campagna viene ignorata per i frammenti a cui si fa riferimento negli elementi decisionali.

* La convalida del contenuto del frammento viene eseguita solo durante la creazione e la pubblicazione del frammento.

* In caso di frammenti JSON, la validità dell’oggetto JSON non è garantita. Assicurati che il contenuto del frammento di espressione sia un JSON valido in modo che possa essere utilizzato negli elementi decisionali.

In fase di esecuzione, viene convalidato il contenuto della campagna (incluso il contenuto del frammento dagli elementi decisionali). In caso di errore di convalida, la campagna non verrà rappresentata.

## Passaggi finali {#final-steps}

Una volta che il contenuto è pronto, rivedi e pubblica la campagna o il percorso:

* [Pubblicare un percorso](../building-journeys/publishing-the-journey.md)
* [Rivedere attivare una campagna](../campaigns/review-activate-campaign.md)
* [Pubblicare e attivare un’esperienza basata su codice](../code-based/publish-code-based.md)

Per le esperienze basate su codice, non appena lo sviluppatore effettua una chiamata API o SDK per recuperare il contenuto per la superficie definita nella configurazione del canale, le modifiche verranno applicate alla pagina web o all’app.

>[!NOTE]
>
>Attualmente non è possibile simulare contenuti dall&#39;interfaccia utente in una campagna o in un percorso [esperienza basata su codice](../code-based/create-code-based.md) utilizzando le decisioni. Una soluzione alternativa è disponibile in [questa sezione](../code-based/code-based-decisioning-implementations.md).

Per visualizzare le prestazioni delle decisioni, puoi creare [dashboard di reporting di Customer Journey Analytics](cja-reporting.md) personalizzati.
