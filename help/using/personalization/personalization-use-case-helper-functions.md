---
solution: Journey Optimizer
product: journey optimizer
title: caso d’uso Personalization&due punti; e-mail di abbandono carrello
description: Scopri come personalizzare il corpo di un messaggio e-mail tramite un caso d’uso.
feature: Personalization, Use Cases
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, helper, caso d’uso, personalizzazione
exl-id: 9c9598c0-6fb1-4e2f-b610-ccd1a80e516e
TQID: https://experienceleague.adobe.com/93bIkfyck5u-tQNGr7jGRORQiTa3gaMHn4H5RP-dpYo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: 2016539d8a34850e2730dbb2e1499739a04d88c0
workflow-type: tm+mt
source-wordcount: 1712
ht-degree: 1%

---

# Caso di utilizzo di Personalization: e-mail di abbandono del carrello {#personalization-use-case-helper-functions}

>[!BEGINSHADEBOX]

**In questa pagina:** segui un caso di utilizzo di abbandono del carrello che personalizza un corpo dell&#39;e-mail utilizzando le funzioni upperCase, each e if helper in Adobe Journey Optimizer.

>[!ENDSHADEBOX]

In questo esempio personalizzerai il corpo di un messaggio e-mail. Questo messaggio è destinato ai clienti che hanno lasciato articoli nel carrello ma non hanno completato l’acquisto.

Puoi utilizzare i seguenti tipi di funzioni di assistenza:

* La funzione stringa `upperCase`, per inserire il nome del cliente in lettere maiuscole. [Ulteriori informazioni](functions/string.md#upper).
* Helper `each`, per elencare gli elementi presenti nel carrello. [Ulteriori informazioni](functions/helpers.md#each).
* Helper `if`, per inserire una nota specifica per il prodotto se il prodotto correlato è nel carrello. [Ulteriori informazioni](functions/helpers.md#if-function).
<!-- **Context**: personalization based on contextual data from the journey -->

➡️ [Scopri come utilizzare le funzioni di assistenza in questo video](#video)

Prima di iniziare, assicurati di sapere come configurare questi elementi:

* Un evento unitario. [Ulteriori informazioni](../event/about-events.md).
* Un percorso che inizia con un evento. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md).
* Un messaggio e-mail nel percorso. [Ulteriori informazioni](../email/create-email.md)
* Corpo di un’e-mail. [Ulteriori informazioni](../email/content-from-scratch.md).

Segui questi passaggi:

1. [Creare l&#39;evento iniziale e il percorso](#create-context).
1. [Crea un messaggio e-mail](#configure-email).
1. [Inserire il nome del cliente in lettere maiuscole](#uppercase-function).
1. [Aggiungi il contenuto del carrello all&#39;e-mail](#each-helper).
1. [Inserire una nota specifica per il prodotto](#if-helper).
1. [Verifica e pubblica il percorso](#test-and-publish).

## Passaggio 1: creare l’evento iniziale e il percorso correlato {#create-context}

Il contenuto del carrello è un’informazione contestuale proveniente dal percorso. Pertanto, è necessario aggiungere un evento iniziale e l’e-mail a un percorso prima di poter aggiungere all’e-mail informazioni specifiche per il carrello.

1. Creare un evento il cui schema include l&#39;array `productListItems`.
1. Definisci tutti i campi di questo array come campi payload per questo evento.

   Ulteriori informazioni sul tipo di dati dell&#39;elemento dell&#39;elenco prodotti nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}.

1. Crea un percorso che inizia con questo evento.
1. Aggiungi un&#39;attività **E-mail** al percorso.

   ![Area di lavoro Percorso con un evento e un&#39;attività e-mail nel flusso](assets/personalization-uc-helpers-8.png)

## Passaggio 2: creare l’e-mail {#configure-email}

1. Nell&#39;attività **E-mail**, fai clic su **[!UICONTROL Modifica contenuto]**, quindi su **[!UICONTROL E-mail Designer]**.

   ![Attività e-mail con le opzioni Modifica contenuto e Invia e-mail a Designer](assets/personalization-uc-helpers-1.png)

1. Dalla palette a sinistra della home page di E-mail Designer, trascina e rilascia tre componenti struttura sul corpo del messaggio.

1. Trascina e rilascia un componente di contenuto HTML su ciascun nuovo componente struttura.

   ![Invia un&#39;e-mail a Designer con tre componenti struttura e componenti contenuto HTML nel corpo](assets/personalization-uc-helpers-2.png)

## Passaggio 3: inserire il nome del cliente in lettere maiuscole {#uppercase-function}

1. Nella home page di E-mail Designer, fai clic sul componente HTML in cui desideri aggiungere il nome del cliente.
1. Sulla barra degli strumenti contestuale fare clic su **[!UICONTROL Mostra codice sorgente]**.

   ![Barra degli strumenti contestuale con opzione Mostra codice sorgente](assets/personalization-uc-helpers-3.png)

1. Nella finestra **[!UICONTROL Modifica HTML]**, aggiungi la funzione stringa `upperCase`:
   1. Nel menu a sinistra, seleziona **[!UICONTROL Funzioni helper]**.
   1. Utilizza il campo di ricerca per trovare &quot;maiuscolo&quot;.
   1. Aggiungere la funzione `upperCase` dai risultati della ricerca. A tale scopo, fare clic sul segno più (+) accanto a `{%= upperCase(string) %}: string`.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![Editor espressioni con funzione upperCase selezionata nelle funzioni helper](assets/personalization-uc-helpers-4.png)

1. Rimuovi il segnaposto &quot;stringa&quot; dall’espressione.
1. Aggiungi il token di nome:
   1. Nel menu a sinistra, seleziona **[!UICONTROL Attributi del profilo]**.
   1. Selezionare **[!UICONTROL Persona]** > **[!UICONTROL Nome completo]**.
   1. Aggiungi il token **[!UICONTROL First name]** all&#39;espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![L&#39;editor espressioni mostra upperCase con token nome profilo](assets/personalization-uc-helpers-5.png)

      Ulteriori informazioni sul tipo di dati del nome della persona nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target="_blank"}.

1. Fai clic su **[!UICONTROL Convalida]**, quindi su **[!UICONTROL Salva]**.

   ![Modifica finestra di HTML con i pulsanti Convalida e Salva](assets/personalization-uc-helpers-6.png)

1. Salva il messaggio.

## Passaggio 4: inserire l’elenco degli articoli dal carrello {#each-helper}

Questo passaggio illustra l’iterazione dei dati dell’evento. Per esempi completi di iterazione su diverse origini dati (eventi, risposte alle azioni personalizzate e altri dati contestuali), vedere [Iterare dati contestuali con Handlebars](iterate-contextual-data.md).

1. Riapri il contenuto del messaggio.

1. Nella pagina Home di E-mail Designer, fai clic sul componente HTML in cui desideri elencare il contenuto del carrello.
1. Sulla barra degli strumenti contestuale fare clic su **[!UICONTROL Mostra codice sorgente]**.

   ![Barra degli strumenti contestuale con opzione Mostra codice sorgente](assets/personalization-uc-helpers-3.png)

1. Nella finestra **[!UICONTROL Modifica HTML]**, aggiungi l&#39;helper `each`:
   1. Nel menu a sinistra, seleziona **[!UICONTROL Funzioni helper]**.
   1. Utilizza il campo di ricerca per trovare &quot;ciascuno&quot;.
   1. Aggiungere l&#39;helper `each` dai risultati della ricerca.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![Editor espressioni con ogni modello helper](assets/personalization-uc-helpers-9.png)

1. Aggiungere l&#39;array `productListItems` all&#39;espressione:

   1. Rimuovi il segnaposto &quot;someArray&quot; dall’espressione.
   1. Nel menu a sinistra, seleziona **[!UICONTROL Attributi contestuali]**.

      **[!UICONTROL Gli attributi contestuali]** sono disponibili solo dopo che il contesto di percorso è stato passato al messaggio.

   1. Seleziona **[!UICONTROL Journey Optimizer]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]***, quindi espandi il nodo **[!UICONTROL productListItems]**.

      In questo esempio, *nome_evento* rappresenta il nome dell&#39;evento.

   1. Aggiungi il token **[!UICONTROL Product]** all&#39;espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```

      In questo esempio, *event_ID* rappresenta l&#39;ID dell&#39;evento.

      ![Editor espressioni con productListItems negli attributi contestuali](assets/personalization-uc-helpers-10.png)

   1. Modifica l’espressione:
      1. Rimuovi la stringa &quot;.product&quot;.
      1. Sostituisci il segnaposto &quot;variable&quot; con &quot;product&quot;.

      Questo esempio mostra l’espressione modificata:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```

1. Incolla questo codice tra il tag di apertura `{{#each}}` e il tag di chiusura `{{/each}}`:

   ```html
   <table>
      <tbody>
         <tr>
            <td><b>#name</b></td>
            <td><b>#quantity</b></td>
            <td><b>$#priceTotal</b></td>
         </tr>
      </tbody>
   </table>
   ```

1. Aggiungi i token di personalizzazione per il nome dell’articolo, la quantità e il prezzo:

   1. Rimuovi il segnaposto &quot;#name&quot; dalla tabella HTML.
   1. Dai risultati della ricerca precedente, aggiungi il token **[!UICONTROL Name]** all&#39;espressione.

   Ripeti questi passaggi due volte:

   * Sostituisci il segnaposto &quot;#quantity&quot; con il token **[!UICONTROL Quantity]**.
   * Sostituisci il segnaposto &quot;#priceTotal&quot; con il token **[!UICONTROL Total price]**.

   Questo esempio mostra l’espressione modificata:

   ```handlebars
   {{#each context.journey.events.event_ID.productListItems as |product|}}
      <table>
         <tbody>
            <tr>
            <td><b>{{product.name}}</b></td>
            <td><b>{{product.quantity}}</b></td>
            <td><b>${{product.priceTotal}}</b></td>
            </tr>
         </tbody>
      </table>
   {{/each}}
   ```

1. Fai clic su **[!UICONTROL Convalida]**, quindi su **[!UICONTROL Salva]**.

   ![Editor espressioni con convalida e salvataggio dopo la configurazione di ogni blocco](assets/personalization-uc-helpers-11.png)

## Passaggio 5: inserire una nota specifica per il prodotto {#if-helper}

1. Nella home page di E-mail Designer, fai clic sul componente HTML in cui desideri inserire la nota.
1. Sulla barra degli strumenti contestuale fare clic su **[!UICONTROL Mostra codice sorgente]**.

   ![Barra degli strumenti contestuale con opzione Mostra codice sorgente](assets/personalization-uc-helpers-3.png)

1. Nella finestra **[!UICONTROL Modifica HTML]**, aggiungi l&#39;helper `if`:
   1. Nel menu a sinistra, seleziona **[!UICONTROL Funzioni helper]**.
   1. Utilizza il campo di ricerca per trovare &quot;if&quot;.
   1. Aggiungere l&#39;helper `if` dai risultati della ricerca.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```

      ![Editor espressioni con il modello helper if](assets/personalization-uc-helpers-12.png)

1. Rimuovi questa condizione dall’espressione:

   ```handlebars
   {%else if condition2%} render_2
   ```

   Questo esempio mostra l’espressione modificata:

   ```handlebars
   {%#if condition1%} render_1
      {%else%} default_render
   {%/if%}
   ```

1. Aggiungi il token del nome del prodotto alla condizione:
   1. Rimuovi il segnaposto &quot;condition1&quot; dall’espressione.
   1. Nel menu a sinistra, seleziona **[!UICONTROL Attributi contestuali]**.
   1. Seleziona **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]***, quindi espandi il nodo **[!UICONTROL productListItems]**.

      In questo esempio, *nome_evento* rappresenta il nome dell&#39;evento.

   1. Aggiungi il token **[!UICONTROL Name]** all&#39;espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```

      ![Editor espressioni con token di nome productListItems nella condizione if](assets/personalization-uc-helpers-13.png)

1. Modifica l’espressione:
   1. Nell&#39;editor espressioni specificare il nome del prodotto dopo il token `name`.

      Utilizza questa sintassi, in cui *product_name* rappresenta il nome del prodotto:

      ```javascript
      = "product_name"
      ```

      In questo esempio, il nome del prodotto è &quot;Juno Jacket&quot;:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         render_1
         {%else%} default_render
      {%/if%}
      ```

   1. Sostituite il segnaposto &quot;render_1&quot; con il testo della nota.

      Esempio:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```

   1. Rimuovi il segnaposto &quot;default_render&quot; dall’espressione.
1. Fai clic su **[!UICONTROL Convalida]**, quindi su **[!UICONTROL Salva]**.

   ![Modifica la finestra di HTML con Convalida e salva dopo la configurazione del blocco if](assets/personalization-uc-helpers-14.png)

1. Salva il messaggio.

## Passaggio 6: testare e pubblicare il percorso {#test-and-publish}

1. Attiva il **[!UICONTROL Test]**, quindi fai clic su **[!UICONTROL Attiva un evento]**.

   ![Percorso con attivazione test e attivazione pulsante evento](assets/personalization-uc-helpers-15.png)

1. Nella finestra **[!UICONTROL Configurazione evento]**, immetti i valori di input, quindi fai clic su **[!UICONTROL Invia]**.

   La modalità di test funziona solo con i profili di test.

   ![Finestra di configurazione evento con valori di input e pulsante Invia](assets/personalization-uc-helpers-16.png)

   L’e-mail viene inviata all’indirizzo del profilo di test.

   In questo esempio, l’e-mail contiene la nota sulla Giacca Juno, perché questo prodotto si trova nel carrello:

   ![E-mail di esempio che mostra la nota di spedizione della Giunone Jacket nel corpo del messaggio](assets/personalization-uc-helpers-17.png)

1. Verifica che non vi sia alcun errore, quindi pubblica il percorso.


## Argomenti correlati {#related-topics}

### Funzioni Handlebars {#handlebars}

* [Helper](functions/helpers.md)

* [Funzioni stringa](functions/string.md)

### Casi d’uso {#use-case}

* [Personalization con informazioni di profilo, contesto e offerta](personalization-use-case.md)

* [Personalization con offerta basata su decisioni](../offers/offers-e2e.md)

## Video introduttivo {#video}

Scopri come utilizzare le funzioni di assistenza.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)

## Riferimento rapido {#quick-reference}

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

>[!BEGINTABS]

>[!TAB Panoramica]

**TL;DR**

In questa pagina viene descritto un caso d&#39;uso relativo all&#39;abbandono del carrello tramite tre funzioni di supporto, `upperCase`, `each` e `if`, per visualizzare il nome di un cliente in maiuscolo, elencare gli articoli del carrello e inserire una nota di spedizione specifica per il prodotto in modo condizionale.

**Intenti**

* Crea un evento di percorso il cui schema include l&#39;array `productListItems`
* Inserire il nome di un cliente in maiuscolo utilizzando `{%= upperCase(profile.person.name.firstName) %}`
* Elencare gli elementi del carrello ripetendo l&#39;iterazione su `context.journey.events.event_ID.productListItems` con `{{#each}}`
* Visualizzare una nota specifica per il prodotto in modo condizionale utilizzando `{%#if context.journey.events.\`event_ID\`.productListItems.name = &quot;product_name&quot; %&rbrace;&grave;
* Testa il percorso in modalità di test utilizzando un profilo di test con payload dell’evento, quindi pubblica

>[!TAB Glossario]

* **`upperCase`**: funzione stringa di PQL che converte una stringa in maiuscolo; chiamata con `{%= upperCase(string) %}`. *(specifico per prodotto)*
* Helper **`each`**: Handlebars blocca helper (`{{#each array as |alias|}} ... {{/each}}`) che scorre su un array come `productListItems`. *(specifico per prodotto)*
* Helper **`if`**: helper per il blocco condizionale (`{%#if condition%} ... {%else%} ... {%/if%}`) che esegue il rendering del contenuto solo quando la condizione specificata è true.
* **`productListItems`**: array XDM standard che rappresenta il contenuto del carrello, con campi che includono `name`, `quantity` e `priceTotal`. *(specifico per prodotto)*
* **Modalità di test**: funzionalità di percorso che consente di inviare messaggi di test agli indirizzi del profilo di test per verificare il comportamento del percorso e dei messaggi prima della pubblicazione. *(specifico per prodotto)*

>[!TAB Terminologia]

* **Nome canonico:** e-mail di abbandono carrello — varianti: caso di utilizzo abbandono carrello
* **Non confondere:** `context.journey.events.event_ID.productListItems` (array originato da eventi, a cui si accede tramite attributi contestuali) ≠ `profile.*` attributi (originati da profili, sempre disponibili)

>[!TAB Guardrail e limitazioni]

* Gli attributi contestuali (inclusi i dati dell’evento di percorso) sono disponibili nell’editor di personalizzazione solo dopo che il messaggio è stato inserito all’interno di un percorso che include l’evento rilevante.
* La modalità di test funziona solo con i profili di test.

>[!TAB Domande frequenti]

**D: quali funzioni di assistenza vengono utilizzate in questo caso d&#39;uso?**

Tre: `upperCase` (esegue il rendering del nome in maiuscolo), `each` (esegue l&#39;iterazione sull&#39;array di elementi del carrello) e `if` (visualizza in modo condizionale una nota di spedizione specifica per il prodotto).

**Q: da dove provengono i dati dell&#39;elemento del carrello nell&#39;espressione di personalizzazione?**

Dall&#39;array `productListItems` dell&#39;evento di percorso, a cui si accede tramite gli attributi contestuali in `context.journey.events.event_ID.productListItems`.

**D: è possibile utilizzare attributi contestuali prima di inserire il messaggio all&#39;interno di un percorso?**

No. Gli attributi contestuali sono disponibili nell’editor di personalizzazione solo dopo che il messaggio viene inserito all’interno di un percorso che include l’evento rilevante.

**D: come posso verificare l&#39;e-mail con i dati del carrello?**

Attiva l&#39;interruttore **Test** nel percorso, fai clic su **Attiva un evento**, immetti i valori di input nella finestra Configurazione evento, quindi fai clic su **Invia**. L’e-mail viene inviata all’indirizzo del profilo di test.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 801d75d6 -->
