---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzo di integrazioni esterne
description: Integra integrazioni esterne nel processo di authoring dei canali per arricchire i contenuti con informazioni personalizzate e dinamiche, incluse le risposte API di distribuzione di Adobe Target
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: integrazione
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: d16f7424-4847-4b90-a37c-4b52cbdabee5
source-git-commit: bfb28a935dffca7c381fe72339abc840d2ab297b
workflow-type: tm+mt
source-wordcount: 842
ht-degree: 1%

---


# Utilizzo di integrazioni esterne per la personalizzazione {#integrations-personalization}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come gli addetti al marketing applicano integrazioni configurate per personalizzare contenuti e-mail, SMS e push e concatenano una chiamata API a un&#39;altra per una messaggistica più ricca e dinamica.

>[!ENDSHADEBOX]

Prima di utilizzare le integrazioni esterne nel contenuto, verificare che un amministratore abbia **configurato e attivato** ogni integrazione (endpoint, autenticazione, criteri, payload di risposta e attivazione) come descritto in [Operazioni con le integrazioni](integrations.md).

Puoi aggiungere fino a **3** integrazioni per **[!UICONTROL Frammento]** e fino a **5** nel messaggio. Le integrazioni provenienti solo da frammenti non vengono conteggiate per **5**.

## Applicare la personalizzazione dell’integrazione al contenuto {#apply-integration-personalization}

In qualità di addetto marketing, puoi utilizzare integrazioni configurate per personalizzare il contenuto. Segui questi passaggi:

1. Accedi al contenuto della tua campagna e fai clic su **[!UICONTROL Aggiungi personalizzazione]** dal tuo **[!UICONTROL Componenti]** di testo o HTML.

   [Ulteriori informazioni sui componenti](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Passa alla sezione **[!UICONTROL Integrazioni]** e fai clic su **[!UICONTROL Apri integrazioni]** per visualizzare tutte le integrazioni attive.

   I **frammenti di Journey Optimizer** sono disponibili con le integrazioni ma supportano solo i canali in uscita. Dopo la pubblicazione di un frammento, l’aggiunta e il salvataggio di nuove integrazioni viene disattivato per evitare un impatto sui percorsi e sulle campagne esistenti.

   ![](assets/external-integration-content-2.png)

1. Seleziona un&#39;integrazione e fai clic su **[!UICONTROL Salva]**.

   ![](assets/external-integration-content-3.png)

1. Attiva la modalità **[!UICONTROL Pillole]** per sbloccare il menu di integrazione avanzato.

   ![](assets/external-integration-content-4.png)

1. Quando si crea la personalizzazione dell&#39;integrazione, l&#39;helper integrazioni include un campo **`required`** che definisce il modo in cui gli errori o i dati mancanti interagiscono con il contenuto predefinito:

   * **`required=true`** (impostazione predefinita): il rendering viene interrotto per il messaggio. L&#39;invio è escluso con **`ExternalDataLookupExclusion`** e tale esclusione è registrata nel **set di dati di feedback del messaggio**.
   * **`required=false`**: la variabile dei risultati è impostata su **`null`** e il rendering continua. Utilizza testo predefinito, fallback o logica condizionale nel modello, in modo che i profili non ricevano contenuto vuoto quando l’integrazione non restituisce dati.

     ![](assets/external-integration-content-8.png)

1. Per completare la configurazione dell&#39;integrazione, definire gli attributi di integrazione specificati in precedenza durante la [configurazione](integrations.md#configure).

   Puoi assegnare valori a questi attributi utilizzando valori statici, che rimangono costanti, o attributi di profilo, che estraggono informazioni in modo dinamico dai profili utente.

   ![](assets/external-integration-content-5.png)

1. Una volta definiti gli attributi di integrazione, puoi utilizzare i campi di integrazione nel contenuto per la messaggistica personalizzata facendo clic sull&#39;icona ![aggiungi](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >I token nel modello devono utilizzare solo i campi esposti dall&#39;amministratore nella configurazione dell&#39;integrazione. Ad esempio, `{{weatherResponse.temperature}}` è valido quando `temperature` è esposto; `{{weatherResponse.humidity}}` è rifiutato nell&#39;editor se `humidity` non è stato esposto.

1. Fai clic su **[!UICONTROL Salva]**.

La personalizzazione dell’integrazione ora viene applicata correttamente al contenuto, garantendo a ogni destinatario un’esperienza personalizzata e rilevante in base agli attributi configurati.

![](assets/external-integration-content-7.png)

## Mappare una chiamata API su un’altra {#map-integration-chain}

Puoi concatenare le integrazioni in modo che i risultati di una chiamata vengano inseriti nel successivo, ad esempio segmenti di percorso, intestazioni o parametri di query. Le chiamate vengono eseguite in ordine nello stesso messaggio, che supporta una personalizzazione più ricca senza codice personalizzato.

Prima di iniziare, assicurati che:

* Un amministratore ha configurato e attivato ogni integrazione necessaria. Consulta [Configurare l&#39;integrazione](integrations.md).
* I segnaposto per percorsi variabili, le intestazioni e i parametri di query sono impostati nella configurazione dell’integrazione con etichette per gli addetti al marketing.
* L&#39;amministratore ha esposto i campi di risposta necessari nel payload **[!UICONTROL Risposta]** di ogni integrazione, in modo che vengano visualizzati durante l&#39;authoring.

L’esempio seguente utilizza un’integrazione di prenotazione che restituisce un numero di volo dalla prenotazione del profilo, quindi un’integrazione di informazioni di volo che utilizza tale numero per lo stato live (ritardi, destinazione). Mappa gli input della seconda integrazione alla risposta della prima chiamata.

1. Apri il messaggio o il frammento e apri l’editor di personalizzazione.

   ![](assets/uc-integrations-1.png)

1. In **[!UICONTROL Integrazioni]**, fai clic su **[!UICONTROL Apri integrazioni]**.

   ![](assets/uc-integrations-2.png)

1. Aggiungi l’integrazione la cui risposta alimenta la chiamata successiva, ad esempio i dati di prenotazione o prenotazione che includono l’identificatore del volo.

   ![](assets/uc-integrations-3.png)

1. (Facoltativo) Aprire il menu della funzione **[!UICONTROL Helper]** e aggiungere un helper, ad esempio la funzione `Let`, se si desidera associare una variabile denominata alla risposta della prenotazione.

   >[!NOTE]
   >
   > Sono disponibili solo i campi esposti nel payload **[!UICONTROL Risposta]** definito dall&#39;amministratore. Non è possibile fare riferimento a proprietà non esposte nella configurazione.

1. Se utilizzi una variabile helper, mappa tale variabile sul campo restituito dall’integrazione della prenotazione per l’uso a valle, ad esempio il numero del volo nel payload del passeggero o della prenotazione.

   ![](assets/uc-integrations-4.png)

1. Dal menu **[!UICONTROL Apri integrazioni]**, aggiungi la seconda integrazione, ad esempio lo stato del volo.

   ![](assets/uc-integrations-5.png)

1. Nella seconda integrazione, apri **[!UICONTROL Attributi di integrazione]**. Per ogni input che deve riutilizzare i dati della prima chiamata, ad esempio una variabile di percorso, un’intestazione o un parametro di query, seleziona un’origine di mappatura dalla prima risposta di integrazione.

   Nell&#39;esperienza **[!UICONTROL Pills]**, puoi mappare l&#39;output della prima chiamata direttamente all&#39;input della seconda chiamata senza un&#39;istruzione `Let`. Se hai utilizzato `Let`, puoi eseguire il mapping attraverso tale variabile.

   ![](assets/uc-integrations-6.png)

1. Inserisci i token della seconda integrazione nel contenuto con il controllo ![add](assets/do-not-localize/Smock_Add_18_N.svg), ad esempio la destinazione dalla risposta di informazioni sul volo.

   ![](assets/uc-integrations-8.png)

1. Salva il contenuto.

In **[!UICONTROL Simulazione]** o invio, Journey Optimizer esegue le integrazioni in ordine: la prima chiamata utilizza il contesto del profilo configurato e il risultato genera la seconda richiesta. Se una determinata integrazione viene eseguita al momento della simulazione o dell’invio dipende dalla configurazione e dal canale.

![](assets/uc-integrations-7.png)

<!--
## Use Adobe Target data in templates {#use-adobe-target-in-templates}

This section explains how to use **Integrations** in Adobe Journey Optimizer to fetch personalization data from **[!DNL Adobe Target]** at send time and use it in message templates. It assumes the Target Delivery API has already been configured as an integration.

For configuration steps, see [Work with Integrations](integrations.md) and the [Adobe Target Recommendations](vendor-integration.md#adobe-target-recommendations) sample.

The Target Delivery API returns a `prefetch.mboxes` array. Each mbox includes an `options` object with `content` and `type` fields. The `type` value determines how you use `content` in your template. Open the tab that matches your mbox response, then follow the steps to use that data in your message.

>[!BEGINTABS]

>[!TAB JSON content]

When `type` is `json`, the `content` field is a **JSON string**. Parse it before you access nested fields. The example below shows a typical Delivery API response for a JSON mbox.

```json
{
  "status": 200,
  "prefetch": {
    "mboxes": [
      {
        "index": 0,
        "name": "SummerOffer",
        "options": {
          "content": "{\"recommendations\":[{\"productId\":\"p101\",\"name\":\"Noise Smartwatch\",\"price\":2999},{\"productId\":\"p205\",\"name\":\"Boat Earbuds\",\"price\":1499}],\"strategy\":\"collaborative-filtering\"}",
          "type": "json"
        }
      }
    ]
  }
}
```

Use three helpers in sequence to fetch, extract, and parse the Target response.

1. **Fetch the Target response.** Call your configured Target integration with `externalDataLookup`. Set `integrationName` to the **[!UICONTROL Name]** of that integration (replace the example placeholder `target_recommendations`). Use the `result` parameter to name the template variable that holds the full Delivery API payload—for example, `targetResponse`.

    ```handlebars
    {{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
    ```

1. **Extract a specific mbox using valueAtPath.** `valueAtPath` extracts an element from an array by its 0-based index and assigns it to a template variable. Use the `idx` parameter to specify which element to access.

    ```handlebars
    {{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
    ```

    | Parameter | Description |
    | --- | --- |
    | `path` | Path to the array (positional, no keyword) |
    | `idx` | 0-based index for array access (optional) |
    | `result` | Variable name to store the extracted value |

    >[!NOTE]
    >
    > If `idx` is out of bounds, rendering throws an exception. Guard invalid indexes with `{%#if idx >= 0 and idx < count(targetResponse.prefetch.mboxes)%}` when the index may be invalid. PQL expressions cannot be used as the path. **Available since release 2025.9.0.**

1. **Parse the JSON string using parseJson.** The mbox `options.content` field is a raw JSON string. `parseJson` converts it into a structured object whose fields can then be accessed directly in the template.

    ```handlebars
    {{parseJson jsonStr=summerOffer.options.content result="summerOfferContent"}}
    ```

    | Parameter | Description |
    | --- | --- |
    | `jsonStr` | Path to the string field containing valid JSON |
    | `result` | Variable name to store the parsed object |

    >[!NOTE]
    >
    > If the JSON string is invalid or the reference is null, `result` is set to `null` — no rendering error is thrown. Test with your actual Target response to confirm the content is valid JSON. **Available since: 2026.6.0**

1. **Access the data.** Once parsed, use dot notation to access fields from `summerOfferContent`. To render a list of recommendations:

    ```handlebars
    {{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
    {{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
    {{parseJson jsonStr=summerOffer.options.content result="summerOfferContent"}}

    Strategy: {{summerOfferContent.strategy}}
    {{#each summerOfferContent.recommendations as |rec|}}
      {{rec.name}} — {{rec.price}}
    {{/each}}
    ```

>[!TAB HTML content]

When `type` is `html`, the `content` field is a ready-to-render HTML string. You do not need to parse it. The example below shows a typical Delivery API response for an HTML mbox.

```json
{
  "status": 200,
  "prefetch": {
    "mboxes": [
      {
        "index": 0,
        "name": "SummerOffer",
        "options": {
          "content": "<div class=\"offer\"><h2>Summer Sale</h2><p>50% off Smartwatch</p></div>",
          "type": "html"
        }
      }
    ]
  }
}
```

Fetch and extract the mbox, then render `content` directly. Skip `parseJson`.

```handlebars
{{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
{{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
{{{summerOffer.options.content}}}
```

>[!NOTE]
>
> Use **triple braces** `{{{...}}}` to render HTML content as-is. Double braces `{{...}}` will escape HTML entities and render raw tag strings instead of the HTML.

>[!ENDTABS]

-->

## Video introduttivo {#video}

Questo video mostra come le **Integrazioni** collegano Adobe Journey Optimizer alle API esterne in modo da poter richiamare dati e contenuti live in **canali in uscita**, e-mail, SMS e push, per una personalizzazione più rilevante.

>[!VIDEO](https://video.tv.adobe.com/v/3484118/?learn=on)
