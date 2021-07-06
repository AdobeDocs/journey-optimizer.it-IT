---
title: Case&amp per uso personalizzazione;due punti; e-mail di abbandono carrello
description: Scopri come personalizzare un messaggio utilizzando le funzioni di supporto
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '1016'
ht-degree: 3%

---


# Caso di utilizzo della personalizzazione: e-mail di abbandono carrello {#personalization-use-case-helper-functions}

In questo esempio, personalizzerai il corpo di un messaggio e-mail. Questo messaggio è destinato ai clienti che hanno lasciato gli articoli nel carrello ma non hanno completato l’acquisto.

Verranno utilizzati i seguenti tipi di funzioni di supporto:

* La funzione stringa `upperCase`, per inserire il nome del cliente in lettere maiuscole. [Ulteriori informazioni](functions/string.md#upper).
* L’ `each` helper, per elencare gli elementi presenti nel carrello. [Ulteriori informazioni](functions/helpers.md#each).
* L’ `if` helper, per inserire una nota specifica per il prodotto se il prodotto correlato è nel carrello. [Ulteriori informazioni](functions/helpers.md#if-function).

<!-- **Context**: personalization based on contextual data from the journey -->

Prima di iniziare, assicurati di sapere come configurare questi elementi:
* Un messaggio e-mail. [Ulteriori informazioni](../create-message.md)
* Il corpo di un’e-mail. [Ulteriori informazioni](../create-email-content.md).
* Un evento unitario. [Ulteriori informazioni](../event/about-events.md).
* Percorso che inizia con un evento. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md).

Segui questi passaggi:
1. [Crea un messaggio e-mail](#configure-email).
2. [Inserire il nome del cliente in lettere](#uppercase-function) maiuscole.
3. [Crea l’evento iniziale e il percorso](#create-context).
4. [Aggiungi il contenuto del carrello all’e-mail](#each-helper).
5. [Inserisci una nota](#if-helper) specifica per il prodotto.
6. [Test e pubblicazione del percorso](#test-and-publish).

## Passaggio 1: Creare l’e-mail{#configure-email}

1. Crea o modifica un messaggio e-mail, quindi fai clic su **[!UICONTROL Email Designer]**.
   ![](../assets/personalization-uc-helpers-1.png)

2. Dalla palette a sinistra della home page di E-mail Designer, trascina e rilascia tre componenti struttura nel corpo del messaggio.

3. Trascina un componente di contenuto HTML in ogni nuovo componente struttura.

   ![](../assets/personalization-uc-helpers-2.png)

## Passaggio 2: Inserire il nome del cliente in lettere maiuscole {#uppercase-function}

1. Nella home page di E-mail Designer, fai clic sul componente HTML in cui desideri aggiungere il nome del cliente.
2. Sulla barra degli strumenti contestuale, fai clic su **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

3. Nella finestra **[!UICONTROL Edit HTML]**, aggiungi la funzione stringa `upperCase` :
   1. Nell’elenco, seleziona **[!UICONTROL Helper functions]**.
   2. Usa il campo di ricerca per trovare &quot;maiuscolo&quot;.
   3. Dai risultati della ricerca, aggiungi la funzione `upperCase` . A questo scopo, fai clic sul segno più (+) accanto a `{%= upperCase(string) %}: string`.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![](../assets/personalization-uc-helpers-4.png)

4. Rimuovere il segnaposto &quot;string&quot; dall&#39;espressione.
5. Aggiungi il token del nome:
   1. Nell’elenco, seleziona **[!UICONTROL Profile]**.
   2. Seleziona **[!UICONTROL Profile]** > **[!UICONTROL Person]** > **[!UICONTROL Full name]**.
   3. Aggiungi il token **[!UICONTROL First name]** all’espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![](../assets/personalization-uc-helpers-5.png)

      Ulteriori informazioni sul tipo di dati del nome della persona nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target=&quot;_blank&quot;}.

6. Fai clic su **[!UICONTROL Validate]**, quindi su **[!UICONTROL Save]**.

   ![](../assets/personalization-uc-helpers-6.png)
7. Salva il messaggio.

## Passaggio 3: Creare l’evento iniziale e il percorso correlato {#create-context}

Il contenuto del carrello è un’informazione contestuale proveniente dal percorso. Pertanto, devi aggiungere un evento iniziale e l’e-mail a un percorso prima di poter aggiungere informazioni specifiche sul carrello all’e-mail.

1. Crea un evento il cui schema include la matrice `productListItems`.
2. Definisci tutti i campi di questa matrice come campi di payload per questo evento.

   Ulteriori informazioni sul tipo di dati dell&#39;elemento dell&#39;elenco prodotti [Documentazione Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target=&quot;_blank&quot;}.

3. Crea un percorso che inizia con questo evento.
4. Aggiungi il messaggio al percorso.
5. Termina il percorso con un’attività finale.

   Poiché il messaggio non è ancora stato pubblicato, non puoi né testare né pubblicare il percorso.

   ![](../assets/personalization-uc-helpers-7.png)

6. Fai clic su **[!UICONTROL OK]**.

   Un messaggio ti informa che il contesto del percorso è stato trasmesso al messaggio.

   ![](../assets/personalization-uc-helpers-8.png)

## Passaggio 4: Inserisci l&#39;elenco degli elementi dal carrello {#each-helper}

1. Riapri il messaggio.

   ![](../assets/personalization-uc-helpers-18.png)

2. Nella home page di E-mail Designer, fai clic sul componente HTML in cui desideri elencare il contenuto del carrello.
3. Sulla barra degli strumenti contestuale, fai clic su **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

4. Nella finestra **[!UICONTROL Edit HTML]**, aggiungi l’ `each` helper:
   1. Nell’elenco, seleziona **[!UICONTROL Helper functions]**.
   2. Usa il campo di ricerca per trovare &quot;ogni&quot;.
   3. Dai risultati della ricerca, aggiungi l’ `each` helper .

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![](../assets/personalization-uc-helpers-9.png)

5. Aggiungi la matrice `productListItems` all&#39;espressione:

   1. Rimuovere il segnaposto &quot;someArray&quot; dall’espressione.
   2. Nell’elenco, seleziona **[!UICONTROL Context]**.

      L’opzione **[!UICONTROL Context]** è disponibile solo dopo che il contesto del percorso è stato trasmesso al messaggio.

   3. Seleziona **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > **[!UICONTROL event_name]**, quindi espandi il nodo **[!UICONTROL productListItems]**.

      In questo esempio, *nome_evento* rappresenta il nome dell&#39;evento.

   4. Aggiungi il token **[!UICONTROL Product]** all’espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```
      In questo esempio, *event_ID* rappresenta l&#39;ID dell&#39;evento.

      ![](../assets/personalization-uc-helpers-10.png)

   5. Modificare l’espressione:
      1. Rimuovi la stringa &quot;.product&quot;.
      2. Sostituisci il segnaposto &quot;variabile&quot; con &quot;prodotto&quot;.

      Questo esempio mostra l&#39;espressione modificata:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```
6. Incolla questo codice tra il tag di apertura `{{#each}}` e il tag di chiusura `{/each}}` :

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

7. Aggiungi i token di personalizzazione per il nome dell’articolo, la quantità e il prezzo:

   1. Rimuovere il segnaposto &quot;#name&quot; dalla tabella HTML.
   2. Dai risultati della ricerca precedenti, aggiungi il token **[!UICONTROL Name]** all’espressione.

   Ripeti due volte questi passaggi:
   * Sostituisci il segnaposto &quot;#Quantity&quot; con il token **[!UICONTROL Quantity]**.
   * Sostituisci il segnaposto &quot;#priceTotal&quot; con il token **[!UICONTROL Total price]**.

   Questo esempio mostra l&#39;espressione modificata:

   ```handlebars
   {{#each context.journey.events.event_ID.productListItems as |product|}}
      <table>
         <tbody>
            <tr>
               <td><b>{{context.journey.events.event_ID.productListItems.name}}</b></td>
               <td><b>{{context.journey.events.event_ID.productListItems.quantity}}</b></td>
               <td><b>${{context.journey.events.event_ID.productListItems.priceTotal}}</b></td>
            </tr>
         </tbody>
      </table>
   {{/each}}
   ```
8. Fai clic su **[!UICONTROL Validate]**, quindi su **[!UICONTROL Save]**.
   ![](../assets/personalization-uc-helpers-11.png)

## Passaggio 5: Inserire una nota specifica per il prodotto {#if-helper}

1. Nella home page di E-mail Designer, fai clic sul componente HTML in cui desideri inserire la nota.
2. Sulla barra degli strumenti contestuale, fai clic su **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

3. Nella finestra **[!UICONTROL Edit HTML]**, aggiungi l’ `if` helper:
   1. Nell’elenco, seleziona **[!UICONTROL Helper functions]**.
   2. Usa il campo di ricerca per trovare &quot;if&quot;.
   3. Dai risultati della ricerca, aggiungi l’ `if` helper .

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-12.png)

4. Rimuovi questa condizione dall&#39;espressione:

   ```handlebars
   {%else if condition2%} render_2
   ```

   Questo esempio mostra l&#39;espressione modificata:

   ```handlebars
   {%#if condition1%} render_1
      {%else%} default_render
   {%/if%}
   ```

5. Aggiungi il token del nome del prodotto alla condizione:
   1. Rimuovere il segnaposto &quot;condizione1&quot; dall&#39;espressione.
   2. Nell’elenco, seleziona **[!UICONTROL Context]**.
   3. Seleziona **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > **[!UICONTROL event_name]**, quindi espandi il nodo **[!UICONTROL productListItems]**.

      In questo esempio, *nome_evento* rappresenta il nome dell&#39;evento.

   4. Aggiungi il token **[!UICONTROL Name]** all’espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-13.png)

6. Modificare l’espressione:
   1. Nell’editor espressioni, specifica il nome del prodotto dopo il token `name` .

      Utilizza questa sintassi, in cui *product_name* rappresenta il nome del tuo prodotto:

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

   2. Sostituire il segnaposto &quot;render_1&quot; con il testo della nota.

      Esempio:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```
   3. Rimuovere il segnaposto &quot;default_render&quot; dall&#39;espressione.
7. Fai clic su **[!UICONTROL Validate]**, quindi su **[!UICONTROL Save]**.

   ![](../assets/personalization-uc-helpers-14.png)

8. Salva e pubblica il messaggio.

## Passaggio 6: Test e pubblicazione del percorso {#test-and-publish}

1. Apri il percorso. Se il percorso è già aperto, aggiorna la pagina.
2. Attiva l&#39;interruttore **[!UICONTROL Test]**, quindi fai clic su **[!UICONTROL Trigger an event]**.

   Puoi attivare la modalità di test solo dopo aver pubblicato il messaggio.

   ![](../assets/personalization-uc-helpers-15.png)

3. Nella finestra **[!UICONTROL Event configuration]**, immetti i valori immessi, quindi fai clic su **[!UICONTROL Send]**.

   La modalità di test funziona solo con i profili di test.

   ![](../assets/personalization-uc-helpers-16.png)

   L’e-mail viene inviata all’indirizzo del profilo di test.

   In questo esempio, l’e-mail contiene la nota sulla giacca Juno perché questo prodotto è nel carrello:

   ![](../assets/personalization-uc-helpers-17.png)

4. Verifica che non ci sia alcun errore, quindi pubblica il percorso.


## Argomenti correlati

### Funzioni del manubrio

* [Assistenza](functions/helpers.md)

* [Funzioni stringa](functions/string.md)

### Casi di utilizzo

* [Personalizzazione con informazioni sul profilo, contesto e offerta](personalization-use-case.md)

* [Personalizzazione con offerta basata su decisione](../offers/offers-e2e.md)

## Video tutorial{#helper-functions-video}

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)