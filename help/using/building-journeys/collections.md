---
solution: Journey Optimizer
product: journey optimizer
title: Trasmettere le raccolte in modo dinamico tramite le azioni personalizzate
description: Invio di un messaggio tramite Campaign v7/v8
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
source-git-commit: 8f25fd5110777c148246864b364d02e4c6bf00da
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 6%

---


# Trasmettere le raccolte in modo dinamico tramite le azioni personalizzate{#passing-collection}

Puoi trasmettere una raccolta nei parametri delle azioni personalizzate che verranno compilati in modo dinamico in fase di esecuzione. Sono supportati due tipi di raccolte:

* **raccolte semplici**: array di tipi di dati semplici, ad esempio con listString:

  ```json
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* o **insiemi di oggetti**: un array di oggetti JSON, ad esempio:

  ```json
  {
  "products":[
     {
        "id":"productA",
        "name":"A",
        "price":20.1
     },
     {
        "id":"productB",
        "name":"B",
        "price":10.0
     },
     {
        "id":"productC",
        "name":"C",
        "price":5.99
     }
   ]
  }
  ```


## Procedura generale {#general-procedure}

In questa sezione viene utilizzato il seguente esempio di payload JSON. Si tratta di un array di oggetti con un campo che è un insieme semplice.

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "A",
        "price": 20.1,
        "color":"blue",
        "locations": [
          "Paris",
          "London"
        ]
      },
      {
        "id": "productB",
        "name": "B",
        "price": 10.99
      }
    ]
  }
}
```

`products` è un array di due oggetti. Devi avere almeno un oggetto.

1. Crea l’azione personalizzata. Ulteriori informazioni sono disponibili in [questa pagina](../action/about-custom-action-configuration.md).

1. Nella sezione **[!UICONTROL Parametri azione]**, incolla l&#39;esempio JSON. La struttura visualizzata è statica: quando si incolla il payload, tutti i campi sono definiti come costanti.

   ![](assets/uc-collection-1.png)

1. Se necessario, regola i tipi di campo. Per gli insiemi sono supportati i tipi di campo seguenti: listString, listInteger, listDecimal, listBoolean, listDateTime, listDateTimeOnly, listDateOnly, listObject

   >[!NOTE]
   >
   >Il tipo di campo viene dedotto automaticamente in base all’esempio di payload.

1. Se si desidera passare gli oggetti in modo dinamico, è necessario impostarli come variabili. In questo esempio `products` è stato impostato come variabile. Tutti i campi oggetto inclusi nell&#39;oggetto vengono impostati automaticamente su variabili.

   >[!NOTE]
   >
   >Il primo oggetto dell’esempio di payload viene utilizzato per definire i campi.

1. Per ogni campo, definisci l’etichetta che verrà visualizzata nell’area di lavoro del percorso.

   ![](assets/uc-collection-2.png){width="70%" align="left"}

1. Crea il percorso e aggiungi l’azione personalizzata creata. Ulteriori informazioni sono disponibili in [questa pagina](../building-journeys/using-custom-actions.md).

1. Nella sezione **[!UICONTROL Parametri azione]**, definisci il parametro dell&#39;array (`products` nel nostro esempio) utilizzando l&#39;editor di espressioni avanzate.

   ![](assets/uc-collection-3.png)

1. Per ciascuno dei seguenti campi oggetto, digita il nome del campo corrispondente dallo schema XDM di origine. Se i nomi sono identici, non è necessario. Nel nostro esempio, è sufficiente definire `product id` e &quot;color&quot;.

   ![](assets/uc-collection-4.png){width="50%" align="left"}

Per il campo array, puoi anche utilizzare l’editor di espressioni avanzate per eseguire la manipolazione dei dati. Nell&#39;esempio seguente vengono utilizzate le funzioni [filter](functions/functionfilter.md) e [intersect](functions/functionintersect.md):

![](assets/uc-collection-5.png)

## Limitazioni {#limitations}

* **Supporto per array nidificati nelle azioni personalizzate**

  Adobe Journey Optimizer supporta array nidificati di oggetti nei payload di risposta **azione personalizzati**, ma questo supporto è limitato nei **payload di richiesta**.

  Nei payload delle richieste, gli array nidificati sono supportati solo se contengono un numero fisso di elementi, come definito nella configurazione dell’azione personalizzata. Ad esempio, se un array nidificato include sempre esattamente tre elementi, può essere configurato come costante. Quando il numero di elementi deve essere dinamico, solo gli array non nidificati (array al livello inferiore) possono essere definiti come variabili.

  Esempio:

   1. L&#39;esempio seguente illustra un **caso d&#39;uso non supportato**.

      In questo esempio, l&#39;array prodotti include un array nidificato (`locations`) con un numero dinamico di elementi, che non è supportato nei payload delle richieste.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "locations": [
            { "name": "Paris" },
            { "name": "London" }
            ]
         }
      ]
      }
      ```

   2. Esempio supportato, con elementi fissi definiti come costanti.

      In questo caso, le posizioni nidificate vengono sostituite da campi fissi (`location1`, `location2`), consentendo al payload di rimanere valido all&#39;interno della configurazione supportata.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "location1": { "name": "Paris" },
            "location2": { "name": "London" }
         }
      ]
      }
      ```


* Per testare le raccolte utilizzando la modalità di test, è necessario utilizzare la modalità di visualizzazione del codice. La modalità di visualizzazione codice non è al momento supportata per gli eventi di business. Puoi inviare una raccolta solo con un singolo elemento.


## Casi particolari{#examples}

Per tipi e array di array eterogenei, l’array è definito con il tipo listAny. È possibile mappare solo singoli elementi, ma non è possibile modificare la matrice in variabile.

![](assets/uc-collection-heterogeneous.png){width="70%" align="left"}

Esempio di tipo eterogeneo:

```json
{
    "data_mixed-types": [
        "test",
        "test2",
        null,
        0
    ]
}
```

Esempio di array:

```json
{
    "data_multiple-arrays": [
        [
            "test",
            "test1",
            "test2"
        ]
    ]
}
```

**Argomenti correlati**

[Utilizzare azioni personalizzate](../building-journeys/using-custom-actions.md)
