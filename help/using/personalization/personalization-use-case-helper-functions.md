---
solution: Journey Optimizer
product: journey optimizer
title: Caso di utilizzo personalizzazione&due punti; e-mail di abbandono carrello
description: Scopri come personalizzare il corpo di un messaggio e-mail tramite un caso d’uso.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, helper, caso d’uso, personalizzazione
exl-id: 9c9598c0-6fb1-4e2f-b610-ccd1a80e516e
source-git-commit: 02fc8825f61bd365b02788bbcd3e0647f5842bfa
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 3%

---

# Caso di utilizzo della personalizzazione: e-mail di abbandono del carrello {#personalization-use-case-helper-functions}

In questo esempio personalizzerai il corpo di un messaggio e-mail. Questo messaggio è destinato ai clienti che hanno lasciato articoli nel carrello ma non hanno completato l’acquisto.

Puoi utilizzare i seguenti tipi di funzioni di assistenza:

* Il `upperCase` funzione stringa, per inserire il nome del cliente in lettere maiuscole. [Ulteriori informazioni](functions/string.md#upper).
* Il `each` helper, per elencare gli elementi presenti nel carrello. [Ulteriori informazioni](functions/helpers.md#each).
* Il `if` helper, per inserire una nota specifica per il prodotto se il prodotto correlato si trova nel carrello. [Ulteriori informazioni](functions/helpers.md#if-function).
<!-- **Context**: personalization based on contextual data from the journey -->

➡️ [Scopri come utilizzare le funzioni di assistenza in questo video](#video)

Prima di iniziare, assicurati di sapere come configurare questi elementi:

* Un evento unitario. [Ulteriori informazioni](../event/about-events.md).
* Un percorso che inizia con un evento. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md).
* Un messaggio e-mail nel percorso. [Ulteriori informazioni](../email/create-email.md)
* Corpo di un’e-mail. [Ulteriori informazioni](../email/content-from-scratch.md).

Segui questi passaggi:

1. [Creazione dell&#39;evento iniziale e del percorso](#create-context).
1. [Creare un messaggio e-mail](#configure-email).
1. [Inserire il nome del cliente in lettere maiuscole](#uppercase-function).
1. [Aggiungi il contenuto del carrello all’e-mail](#each-helper).
1. [Inserire una nota specifica per il prodotto](#if-helper).
1. [Test e pubblicazione del percorso](#test-and-publish).

## Passaggio 1: creare l’evento iniziale e il percorso correlato {#create-context}

Il contenuto del carrello è un’informazione contestuale proveniente dal percorso. Pertanto, è necessario aggiungere un evento iniziale e l’e-mail a un percorso prima di poter aggiungere all’e-mail informazioni specifiche per il carrello.

1. Crea un evento il cui schema include `productListItems` array.
1. Definisci tutti i campi di questo array come campi payload per questo evento.

   Ulteriori informazioni sul tipo di dati delle voci dell’elenco dei prodotti [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}.

1. Crea un percorso che inizia con questo evento.
1. Aggiungi un **E-mail** al percorso.

   ![](assets/personalization-uc-helpers-8.png)

## Passaggio 2: creare l’e-mail{#configure-email}

1. In **E-mail** attività, fai clic su **[!UICONTROL Modifica contenuto]**, quindi fai clic su **[!UICONTROL E-mail Designer]**.

   ![](assets/personalization-uc-helpers-1.png)

1. Dalla palette a sinistra della home page di E-mail Designer, trascina e rilascia tre componenti struttura sul corpo del messaggio.

1. Trascina e rilascia un componente di contenuto HTML su ciascun nuovo componente struttura.

   ![](assets/personalization-uc-helpers-2.png)

## Passaggio 3: inserire il nome del cliente in lettere maiuscole {#uppercase-function}

1. Nella pagina Home di E-mail designer, fai clic sul componente HTML in cui desideri aggiungere il nome del cliente.
1. Sulla barra degli strumenti contestuale, fai clic su **[!UICONTROL Mostra il codice sorgente]**.

   ![](assets/personalization-uc-helpers-3.png)

1. In **[!UICONTROL Modifica HTML]** , aggiungi il `upperCase` funzione stringa:
   1. Nel menu a sinistra, seleziona **[!UICONTROL Funzioni di supporto]**.
   1. Utilizza il campo di ricerca per trovare &quot;maiuscolo&quot;.
   1. Dai risultati della ricerca, aggiungi `upperCase` funzione. A tale scopo, fare clic sul segno più (+) accanto a `{%= upperCase(string) %}: string`.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![](assets/personalization-uc-helpers-4.png)

1. Rimuovi il segnaposto &quot;stringa&quot; dall’espressione.
1. Aggiungi il token di nome:
   1. Nel menu a sinistra, seleziona **[!UICONTROL Attributi del profilo]**.
   1. Seleziona **[!UICONTROL Persona]** > **[!UICONTROL Nome e cognome]**.
   1. Aggiungi il **[!UICONTROL Nome]** token per l’espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![](assets/personalization-uc-helpers-5.png)

      Ulteriori informazioni sul tipo di dati Nome persona in [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target="_blank"}.

1. Clic **[!UICONTROL Convalida]**, quindi fai clic su **[!UICONTROL Salva]**.

   ![](assets/personalization-uc-helpers-6.png)

1. Salva il messaggio.

## Passaggio 4: inserire l’elenco degli articoli dal carrello {#each-helper}

1. Riapri il contenuto del messaggio.

1. Nella pagina Home di E-mail designer, fai clic sul componente HTML in cui desideri elencare il contenuto del carrello.
1. Sulla barra degli strumenti contestuale, fai clic su **[!UICONTROL Mostra il codice sorgente]**.

   ![](assets/personalization-uc-helpers-3.png)

1. In **[!UICONTROL Modifica HTML]** , aggiungi il `each` helper:
   1. Nel menu a sinistra, seleziona **[!UICONTROL Funzioni di supporto]**.
   1. Utilizza il campo di ricerca per trovare &quot;ciascuno&quot;.
   1. Dai risultati della ricerca, aggiungi `each` aiutante.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![](assets/personalization-uc-helpers-9.png)

1. Aggiungi il `productListItems` array all’espressione:

   1. Rimuovi il segnaposto &quot;someArray&quot; dall’espressione.
   1. Nel menu a sinistra, seleziona **[!UICONTROL Attributi contestuali]**.

      **[!UICONTROL Attributi contestuali]** sono disponibili solo dopo che il contesto del percorso è stato passato al messaggio.

   1. Seleziona **[!UICONTROL Journey Optimizer]** > **[!UICONTROL Eventi]** > ***[!UICONTROL nome_evento]***, quindi espandi **[!UICONTROL productListItems]** nodo.

      In questo esempio, *nome_evento* rappresenta il nome dell’evento.

   1. Aggiungi il **[!UICONTROL Prodotto]** token per l’espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```

      In questo esempio, *event_ID* rappresenta l’ID dell’evento.

      ![](assets/personalization-uc-helpers-10.png)

   1. Modifica l’espressione:
      1. Rimuovi la stringa &quot;.product&quot;.
      1. Sostituisci il segnaposto &quot;variable&quot; con &quot;product&quot;.

      Questo esempio mostra l’espressione modificata:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```

1. Incolla questo codice tra le aperture `{{#each}}` tag e chiusura `{/each}}` tag:

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

   1. Rimuovere il segnaposto &quot;#name&quot; dalla tabella HTML.
   1. Dai risultati della ricerca precedente, aggiungi **[!UICONTROL Nome]** token per l’espressione.

   Ripeti questi passaggi due volte:

   * Sostituire il segnaposto &quot;#quantity&quot; con **[!UICONTROL Quantità]** token.
   * Sostituire il segnaposto &quot;#priceTotal&quot; con **[!UICONTROL Prezzo totale]** token.

   Questo esempio mostra l’espressione modificata:

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

1. Clic **[!UICONTROL Convalida]**, quindi fai clic su **[!UICONTROL Salva]**.

   ![](assets/personalization-uc-helpers-11.png)

## Passaggio 5: inserire una nota specifica per il prodotto {#if-helper}

1. Nella pagina Home di E-mail designer, fai clic sul componente HTML in cui desideri inserire la nota.
1. Sulla barra degli strumenti contestuale, fai clic su **[!UICONTROL Mostra il codice sorgente]**.

   ![](assets/personalization-uc-helpers-3.png)

1. In **[!UICONTROL Modifica HTML]** , aggiungi il `if` helper:
   1. Nel menu a sinistra, seleziona **[!UICONTROL Funzioni di supporto]**.
   1. Utilizza il campo di ricerca per trovare &quot;if&quot;.
   1. Dai risultati della ricerca, aggiungi `if` aiutante.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```

      ![](assets/personalization-uc-helpers-12.png)

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
   1. Seleziona **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Eventi]** > ***[!UICONTROL nome_evento]***, quindi espandi **[!UICONTROL productListItems]** nodo.

      In questo esempio, *nome_evento* rappresenta il nome dell’evento.

   1. Aggiungi il **[!UICONTROL Nome]** token per l’espressione.

      L’editor espressioni mostra questa espressione:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```

      ![](assets/personalization-uc-helpers-13.png)

1. Modifica l’espressione:
   1. Nell’editor espressioni, specifica il nome del prodotto dopo `name` token.

      Utilizza questa sintassi, dove *product_name* rappresenta il nome del prodotto:

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
1. Clic **[!UICONTROL Convalida]**, quindi fai clic su **[!UICONTROL Salva]**.

   ![](assets/personalization-uc-helpers-14.png)

1. Salva il messaggio.

## Passaggio 6: testare e pubblicare il percorso {#test-and-publish}

1. Attiva **[!UICONTROL Test]** , quindi fai clic su **[!UICONTROL Attivare un evento]**.

   ![](assets/personalization-uc-helpers-15.png)

1. In **[!UICONTROL Configurazione evento]** immettere i valori di input, quindi fare clic su **[!UICONTROL Invia]**.

   La modalità di test funziona solo con i profili di test.

   ![](assets/personalization-uc-helpers-16.png)

   L’e-mail viene inviata all’indirizzo del profilo di test.

   In questo esempio, l’e-mail contiene la nota sulla Giacca Juno, perché questo prodotto si trova nel carrello:

   ![](assets/personalization-uc-helpers-17.png)

1. Verifica che non vi sia alcun errore, quindi pubblica il percorso.


## Argomenti correlati {#related-topics}

### Funzioni Handlebars {#handlebars}

* [Helper](functions/helpers.md)

* [Funzioni stringa](functions/string.md)

### Casi d’uso {#use-case}

* [Personalizzazione con informazioni di profilo, contesto e offerta](personalization-use-case.md)

* [Personalizzazione con offerta basata sulle decisioni](../offers/offers-e2e.md)

## Video introduttivo{#video}

Scopri come utilizzare le funzioni di assistenza.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
