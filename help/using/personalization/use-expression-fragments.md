---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare frammenti di espressione
description: Scopri come utilizzare i frammenti di espressione nell'editor di personalizzazione  [!DNL Journey Optimizer] .
feature: Personalization, Fragments
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, libreria, personalizzazione
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
TQID: https://experienceleague.adobe.com/0N5waBGElHBnlsk1pHhKT8roaly-A6srIjb3UPIDNqY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 2174
ht-degree: 0%

---

# Sfruttare i frammenti di espressione {#use-expression-fragments}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come inserire e riutilizzare frammenti di espressione nell&#39;editor di personalizzazione, lavorare con variabili implicite, utilizzare frammenti all&#39;interno di loop, personalizzare campi modificabili e interrompere l&#39;ereditarietà in Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Quando utilizzi l&#39;**editor di personalizzazione**, puoi sfruttare tutti i frammenti di espressione creati o salvati nella sandbox corrente.

Un frammento è un componente riutilizzabile a cui è possibile fare riferimento in [!DNL Journey Optimizer] campagne e percorsi. Questa funzionalità consente di precreare più blocchi di contenuto personalizzati che possono essere utilizzati dagli utenti di marketing per assemblare rapidamente i contenuti in un processo di progettazione migliorato. [Ulteriori informazioni sui frammenti](../content-management/fragments.md)

➡️ [Scopri come gestire, creare e utilizzare i frammenti in questo video](../content-management/fragments.md#video-fragments)

## Utilizzare un frammento di espressione {#use-expression-fragment}

Per aggiungere frammenti di espressione al contenuto, segui i passaggi seguenti.

>[!NOTE]
>
>Puoi aggiungere fino a 30 frammenti in una determinata consegna. I frammenti possono essere nidificati solo fino a un livello.

1. Apri [l&#39;editor di personalizzazione](personalization-build-expressions.md) e seleziona il pulsante **[!UICONTROL Frammenti]** nel riquadro a sinistra.

   Nell’elenco vengono visualizzati tutti i frammenti di espressione creati o salvati come frammenti nella sandbox corrente. [Scopri come creare frammenti](../content-management/create-fragments.md)
Sono ordinati per data di creazione: i frammenti di espressione aggiunti di recente vengono visualizzati per primi nell’elenco.

   ![](assets/expression-fragments-pane.png)

   Puoi anche aggiornare questo elenco.

   >[!NOTE]
   >
   >Se alcuni frammenti sono stati modificati o aggiunti durante la modifica del contenuto, l’elenco verrà aggiornato con le modifiche più recenti.

1. Fai clic sull’icona + accanto a un frammento di espressione per inserire nell’editor l’ID frammento corrispondente.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >Puoi aggiungere al contenuto qualsiasi frammento **Bozza** o **Live**. Tuttavia, non potrai attivare il percorso o la campagna se al suo interno viene utilizzato un frammento con lo stato **Bozza**. Durante la pubblicazione di un percorso o di una campagna, i frammenti bozza mostreranno un errore e dovrai approvarli per poterli pubblicare.

1. Una volta aggiunto l&#39;ID frammento, se apri il frammento di espressione corrispondente e lo [modifichi](../content-management/manage-fragments.md#edit-fragments) dall&#39;interfaccia, le modifiche vengono sincronizzate. Vengono propagati automaticamente a tutte le bozze o ai percorsi/campagne live che contengono tale ID frammento.

1. Fai clic sul pulsante **[!UICONTROL Altre azioni]** accanto a un frammento. Dal menu contestuale visualizzato, selezionare **[!UICONTROL Visualizza frammento]** per ottenere ulteriori informazioni sul frammento. Viene visualizzato anche l&#39;**[!UICONTROL ID frammento]** che può essere copiato da qui.

   ![](assets/expression-fragment-view.png)

1. Puoi aprire il frammento di espressione in un&#39;altra finestra per modificarne il contenuto e le proprietà utilizzando l&#39;opzione **[!UICONTROL Apri frammento]** nel menu contestuale o dal riquadro **[!UICONTROL Informazioni frammento]**. [Scopri come modificare un frammento](../content-management/manage-fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Potrai quindi personalizzare e convalidare i contenuti come di consueto utilizzando tutte le funzionalità di personalizzazione e authoring dell&#39;[editor di personalizzazione](personalization-build-expressions.md).

1. In alcuni casi, è necessario calcolare solo le variabili, quindi potrebbe essere utile nascondere il contenuto del frammento di espressione. A tale scopo, utilizzare l&#39;attributo `render` e impostarlo su `false`. Ad esempio:

   ```
   Hi {{profile.person.name.firstName|fragment id='ajo:fragmentId/variantId' mode ='inline' render=false}}
   ```

>[!NOTE]
>
>Se crei un frammento di espressione che contiene più interruzioni di riga e lo utilizzi nel contenuto [SMS](../mobile/create-mobile-message.md#sms-content) o [push](../push/design-push.md), le interruzioni di riga vengono mantenute. Assicurati quindi di verificare il messaggio [SMS](../mobile/send-mobile-message.md) o [push](../push/send-push.md) prima di inviarlo.

## Usa variabili implicite {#implicit-variables}

Le variabili implicite migliorano la funzionalità dei frammenti esistenti per migliorare l’efficienza in termini di riutilizzabilità dei contenuti e casi di utilizzo di script. I frammenti possono utilizzare variabili di input e creare variabili di output che possono essere utilizzate nel contenuto di campagne e percorsi.

Questa funzionalità può essere utilizzata, ad esempio, per inizializzare i parametri di tracciamento delle e-mail, in base alla campagna o al percorso corrente, e utilizzarli nei collegamenti personalizzati aggiunti al contenuto dell’e-mail.

Sono possibili i seguenti casi d’uso:

1. **Utilizzare variabili di input in un frammento.**

   Quando un frammento viene utilizzato in un contenuto di azione campagna/percorso, può sfruttare le variabili dichiarate al di fuori del frammento. Di seguito è riportato un esempio:

   ![](../personalization/assets/variable-in-a-fragment.png)

   Vediamo che sopra la variabile `utm_content` è dichiarata nel contenuto della campagna. Quando si utilizza il frammento **Blocco principale**, verrà visualizzato un collegamento a cui verrà aggiunto il valore del parametro `utm_content`. Risultato finale: `https://luma.enablementadobe.com?utm_campaign= Product_launch&utm_content= start_shopping`.

1. **Utilizzare variabili di output da un frammento.**

   Le variabili calcolate o definite all’interno di un frammento sono disponibili per l’utilizzo nel contenuto. Nell&#39;esempio seguente, un frammento **F1** dichiara un set di variabili:

   ![](../personalization/assets/personalize-with-variables.png)

   In un contenuto e-mail, puoi avere la seguente personalizzazione:

   ![](../personalization/assets/use-fragment-variable.png)

   Il frammento F1 inizializza le seguenti variabili: `utm_campaign` e `utm_content`. Al collegamento nel contenuto del messaggio verranno aggiunti questi parametri. Risultato finale: `https://luma.enablementadobe.com?utm_campaign= Product_launch&utm_content= start_shopping`.

>[!NOTE]
>
>In fase di runtime, il sistema espande il contenuto dei frammenti e quindi interpreta il codice di personalizzazione dall’alto verso il basso. Tenendo presente questo aspetto, è possibile ottenere casi d’uso più complessi. Ad esempio, puoi avere un frammento F1 che passa le variabili a un altro frammento F2 che si trova sotto. È inoltre possibile che un frammento visivo F1 passi delle variabili a un frammento di espressione nidificato F2.

## Utilizzare frammenti di espressione all’interno di cicli {#fragments-in-loops}

Quando si utilizzano frammenti di espressione nei cicli di `{{#each}}`, è importante comprendere come funziona l&#39;ambito delle variabili. I frammenti di espressione possono accedere alle variabili globali definite nel contenuto del messaggio, ma non possono ricevere variabili specifiche per il ciclo come parametri.

### Schema supportato: utilizza variabili globali {#global-variables-in-loops}

I frammenti di espressione possono fare riferimento a variabili globali definite all’esterno del frammento, anche quando il frammento viene chiamato dall’interno di un loop. Questo è l’approccio consigliato quando devi utilizzare frammenti in contesti iterativi.

**Esempio: utilizzo di un frammento con variabili globali all&#39;interno di un loop**

Nel contenuto del messaggio, definisci una variabile globale e utilizza un frammento che vi faccia riferimento:

```handlebars
{% let globalDiscount = 15 %}

{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Price: ${{product.price}}</p>
    {{fragment id='ajo:fragment123/variant456' mode='inline'}}
  </div>
{{/each}}
```

Nel frammento di espressione (fragment123), è possibile fare riferimento alla variabile `globalDiscount`:

```handlebars
<p class="discount-info">Save {{globalDiscount}}% on all items!</p>
```

Questo modello funziona perché la variabile globale è accessibile in tutto il messaggio, inclusi i frammenti, indipendentemente dal contesto del loop.

### Non supportato: passaggio delle variabili di loop come parametri di frammento {#loop-variables-limitations}

Impossibile passare l&#39;elemento di iterazione corrente (ad esempio `product` nell&#39;esempio precedente) come parametro a un frammento di espressione. Il frammento non può accedere direttamente alle variabili con ambito di loop dal blocco `{{#each}}` circostante.

**Esempio: cosa NON funziona**

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <!-- This will NOT work as expected -->
  {{fragment id='ajo:fragment123/variant456' mode='inline' currentProduct=product}}
{{/each}}
```

Il frammento non può ricevere `product` come parametro e utilizzarlo internamente perché il passaggio del parametro per variabili specifiche del ciclo non è supportato nell&#39;implementazione corrente.

### Soluzioni consigliate {#fragments-in-loops-workarounds}

Quando devi utilizzare frammenti di espressione con dati provenienti da un ciclo, considera questi approcci:

1. **Includi la logica direttamente nel messaggio**: anziché utilizzare un frammento per la logica specifica del ciclo, aggiungi il codice di personalizzazione direttamente nel blocco `{{#each}}`.

   ```handlebars
   {{#each context.journey.actions.GetProducts.items as |product|}}
     <div class="product">
       <h3>{{product.name}}</h3>
       <p>Price: ${{product.price}}</p>
       {{#if product.price > 100}}
         <span class="premium-badge">Premium Product</span>
       {{/if}}
     </div>
   {{/each}}
   ```

2. **Usa frammenti all&#39;esterno di cicli**: se il contenuto del frammento non è dipendente dal ciclo, chiamare il frammento prima o dopo il blocco dell&#39;iterazione.

   ```handlebars
   {{fragment id='ajo:fragment123/variant456' mode='inline'}}
   
   {{#each context.journey.actions.GetProducts.items as |product|}}
     <div class="product">
       <h3>{{product.name}}</h3>
       <p>Price: ${{product.price}}</p>
     </div>
   {{/each}}
   ```

3. **Imposta più variabili globali**: se devi passare valori diversi a un frammento in più iterazioni, imposta le variabili globali prima di ogni chiamata al frammento (anche se questo limita la flessibilità).

>[!NOTE]
>
>Per l&#39;iterazione dei dati contestuali e l&#39;utilizzo dei loop, vedere la guida completa sull&#39;[iterazione dei dati contestuali](iterate-contextual-data.md), che include best practice, suggerimenti per la risoluzione dei problemi e modelli avanzati.

## Personalizza campi modificabili {#customize-fields}

Se alcune parti di un frammento di espressione sono state rese modificabili utilizzando le variabili, è possibile sovrascrivere i relativi valori predefiniti utilizzando una sintassi specifica. [Scopri come rendere personalizzabili i tuoi frammenti](../content-management/customizable-fragments.md)

Per personalizzare i campi, effettua le seguenti operazioni:

1. Inserisci il frammento nel codice dal menu **[!UICONTROL Frammenti]**.

1. Utilizzare il codice `<fieldId>="<value>"` alla fine della sintassi per sostituire il valore predefinito della variabile.

   Nell’esempio seguente, sostituiamo il valore di una variabile il cui ID è &quot;sports&quot; con il valore &quot;yoga&quot;. Questo visualizzerà lo &quot;yoga&quot; nel contenuto del frammento in tutti i casi in cui si fa riferimento alla variabile &quot;sport&quot;.

   ![](../content-management/assets/fragment-expression-use.png)

Un esempio che mostra come aggiungere campi modificabili in un frammento di espressione e ignorarne i valori durante la creazione di un messaggio e-mail è disponibile in [questa sezione](../content-management/customizable-fragments.md#example).

## Usa risoluzione frammento dinamico {#dynamic-resolution}

Invece di incorporare un ID frammento in modo statico in fase di progettazione, puoi risolverlo in modo dinamico in fase di esecuzione per destinatario. Questo consente a profili diversi di ricevere blocchi di contenuto completamente diversi all’interno della stessa campagna o dello stesso percorso, in base ad attributi di profilo, ricerche di set di dati o dati contestuali.

[Scopri come utilizzare i frammenti dinamici](../content-management/dynamic-fragments.md)

## Interrompi ereditarietà {#break-inheritance}

Quando si aggiunge un ID frammento all’editor di personalizzazione, le modifiche apportate al frammento di espressione originale vengono sincronizzate.

Tuttavia, puoi anche incollare il contenuto di un frammento di espressione nell’editor. Dal menu contestuale, seleziona **[!UICONTROL Incolla frammento]** per inserire tale contenuto.

![](assets/expression-fragment-paste.png)

In tal caso, l’ereditarietà dal frammento originale è interrotta. Il contenuto del frammento viene copiato nell’editor e le modifiche non vengono più sincronizzate.

Diventa un elemento autonomo non più collegato al frammento originale; puoi modificarlo come qualsiasi altro elemento nel codice.

## Riferimento rapido {#quick-reference}

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

>[!BEGINTABS]

>[!TAB Panoramica]

**TL;DR**

Questa pagina spiega come inserire, personalizzare e gestire i frammenti di espressione nell’editor di personalizzazione, incluse le variabili implicite, utilizzando frammenti all’interno di loop, campi modificabili, risoluzione dinamica e ereditarietà di interruzioni.

**Intenti**

* Inserire un frammento di espressione dal menu Frammenti e comprendere la propagazione automatica delle modifiche
* Usa variabili implicite: variabili di input (dichiarate all’esterno del frammento, utilizzate all’interno) e variabili di output (dichiarate all’interno del frammento, utilizzate nel contenuto dei messaggi circostanti)
* Utilizzare i frammenti di espressione all’interno di loop: sfrutta le variabili globali per accedere ai frammenti; comprendi la limitazione sul passaggio di variabili con ambito di loop come parametri
* Sostituisci i campi modificabili in un frammento personalizzabile utilizzando la sintassi `<fieldId>="<value>"`
* Risolvere dinamicamente gli ID dei frammenti in fase di runtime in base ad attributi di profilo, ricerche di set di dati o dati contestuali
* Interrompi ereditarietà incollando il contenuto del frammento direttamente nell’editor

>[!TAB Glossario]

* **Frammento di espressione**: componente di espressione di personalizzazione riutilizzabile a cui fa riferimento l&#39;ID in più campagne e percorsi. Le modifiche apportate al frammento si propagano automaticamente a tutti i contenuti che vi fanno riferimento. *(specifico per prodotto)*
* **Variabili implicite**: variabili che estendono la funzionalità del frammento: variabili di input (dichiarate nel contenuto della campagna/percorso, utilizzate all&#39;interno del frammento) e variabili di output (dichiarate all&#39;interno del frammento, disponibili nel contenuto del messaggio circostante). *(specifico per prodotto)*
* **Variabile di input**: variabile dichiarata all&#39;esterno del frammento (nel contenuto della campagna o del percorso) a cui il frammento può fare riferimento e che può utilizzare internamente.
* **Variabile di output**: variabile dichiarata o calcolata all&#39;interno di un frammento che diventa disponibile per l&#39;utilizzo nel contenuto del messaggio circostante dopo la chiamata del frammento.
* **Campi modificabili**: le variabili di frammento esposte per consentire all&#39;utente di inserimento di sostituire i valori predefiniti utilizzando la sintassi `<fieldId>="<value>"`, senza modificare l&#39;origine del frammento. *(specifico per prodotto)*
* **Risoluzione frammento dinamico**: possibilità di risolvere un ID frammento in fase di esecuzione (in base agli attributi del profilo, alle ricerche di set di dati o ai dati contestuali) anziché incorporare un ID frammento statico in fase di progettazione. *(specifico per prodotto)*
* **Interrompi ereditarietà**: utilizzando &quot;Incolla frammento&quot; dal menu contestuale, il contenuto del frammento viene copiato nell&#39;editor come elemento autonomo che non è più sincronizzato con il frammento originale. *(specifico per prodotto)*

>[!TAB Terminologia]

* **Nome canonico:** frammento espressione — varianti: frammento, frammento espressione
* **Sinonimi:** &quot;ID frammento&quot; = l&#39;identificatore utilizzato per fare riferimento al frammento nelle espressioni
* **Non confondere:** inserimento di un frammento per ID (riferimento; le modifiche si propagano automaticamente a tutto il contenuto) ≠ interruzione dell&#39;ereditarietà/incolla del frammento (contenuto copiato nell&#39;editor; elemento autonomo, non più collegato all&#39;originale)
* **Non confondere:** variabili di input (dichiarate all&#39;esterno del frammento, utilizzate all&#39;interno) ≠ variabili di output (dichiarate all&#39;interno del frammento, utilizzate all&#39;esterno del contenuto del messaggio circostante)
* **Non confondere:** Frammento bozza (può essere aggiunto al contenuto ma blocca la pubblicazione di percorsi/campagne fino all&#39;approvazione) ≠ Frammento live (pubblicato completamente; sicuro per percorsi e campagne attivi)

>[!TAB Guardrail e limitazioni]

* È possibile aggiungere fino a 30 frammenti in una determinata consegna.
* I frammenti possono essere nidificati solo fino a un livello.
* Non è possibile attivare o pubblicare un percorso o una campagna se contiene un frammento con stato Bozza; i frammenti bozza devono essere approvati prima della pubblicazione.
* I frammenti di espressione non possono ricevere variabili con ambito di loop (l&#39;elemento di iterazione `{{#each}}` corrente) come parametri. Si tratta di una limitazione nota. Utilizza variabili globali o logica in linea come soluzione alternativa.
* Se nel contenuto SMS o push viene utilizzato un frammento contenente più interruzioni di riga, queste vengono mantenute; verifica il contenuto prima dell’invio.

>[!TAB Domande frequenti]

**D: quanti frammenti è possibile aggiungere in una singola consegna?**

Fino a 30 frammenti.

**Q: i frammenti possono essere nidificati all&#39;interno di altri frammenti?**

Sì, ma solo fino a 1 livello di nidificazione.

**D: cosa succede se utilizzo un frammento di bozza in un percorso o in una campagna?**

Puoi aggiungere al contenuto un frammento Bozza, ma non puoi attivare o pubblicare il percorso o la campagna finché il frammento non viene approvato e il suo stato non viene modificato in Live.

**Q: un frammento di espressione può ricevere l&#39;elemento del loop corrente (ad esempio, `product` in `{{#each}}`) come parametro?**

No. I frammenti di espressione non possono ricevere variabili con ambito di loop come parametri. Utilizza le variabili globali dichiarate all’esterno del ciclo (a cui il frammento può accedere) oppure includi la logica di personalizzazione direttamente all’interno del ciclo, anziché utilizzare un frammento.

**Q: cosa sta interrompendo l&#39;ereditarietà e quando dovrei usarla?**

Per interrompere l’ereditarietà si intende utilizzare &quot;Incolla frammento&quot; dal menu contestuale per copiare il contenuto del frammento direttamente nell’editor. Il contenuto incollato diventa un elemento indipendente che non si sincronizza più con il frammento originale. Utilizzalo quando devi personalizzare il contenuto oltre quanto consentito dai campi modificabili, sapendo che le modifiche future al frammento originale non verranno propagate a questa copia.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 64745ff0 -->

