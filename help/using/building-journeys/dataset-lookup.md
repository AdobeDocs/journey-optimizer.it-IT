---
solution: Journey Optimizer
product: journey optimizer
title: Usa  [!DNL Adobe Experience Platform]  dati in percorsi
description: Scopri come utilizzare l’attività di ricerca del set di dati in [!DNL Adobe Journey Optimizer] per arricchire i percorsi di clienti con dati esterni da [!DNL Adobe Experience Platform].
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilità limitata" type="Informative"
exl-id: b6f54a79-b9e7-4b3a-9a6f-72d5282c01d3
source-git-commit: 6836d30ca7864a82a75a73b8944e43691338558e
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 7%

---

# Utilizzare i dati [!DNL Adobe Experience Platform] nei percorsi {#datalookup}

>[!CONTEXTUALHELP]
>id="ajo_journey_dataset_lookup"
>title="Attività di ricerca del set di dati"
>abstract="L&#39;attività **[!UICONTROL Ricerca set di dati]** consente di recuperare dinamicamente i dati dai set di dati del record [!DNL Adobe Experience Platform] durante il runtime. Sfruttando questa funzionalità, puoi accedere ai dati che potrebbero non trovarsi nel profilo o nel payload dell’evento, garantendo che le interazioni della clientela siano pertinenti e tempestive."

L&#39;attività **[!UICONTROL Ricerca set di dati]** consente di recuperare dinamicamente i dati dai set di dati del record [!DNL Adobe Experience Platform] durante il runtime. Sfruttando questa funzionalità, puoi accedere ai dati che potrebbero non trovarsi nel profilo o nel payload dell’evento, garantendo che le interazioni della clientela siano pertinenti e tempestive.

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile per tutti i clienti come versione a disponibilità limitata.

Vantaggi principali:

* **Real-Time personalization**: Tailor customer experiences using enriched data.
* **Dynamic decision-making**: Use external data to drive journey logic and actions.
* **Accesso ai dati migliorato**: recupera i metadati di prodotto, le tabelle dei prezzi o i dati relazionali associati a chiavi specifiche.

## Da leggere {#must-read}

Esamina questi requisiti prima di configurare le ricerche dei set di dati.

### Abilitazione set di dati

Il set di dati deve essere abilitato per la ricerca in [!DNL Adobe Experience Platform]. Informazioni dettagliate sono disponibili in questa sezione: [Usa [!DNL Adobe Experience Platform] dati](../data/lookup-aep-data.md).

### Limits &amp; restrictions

* Maximum of 10 Dataset Lookup activities per journey.
* Maximum of 20 selected fields.
* Maximum of 50 keys in the lookup keys array.
* La dimensione dei dati arricchiti è limitata a 10 KB.

### Considerazioni aggiuntive sulle prestazioni

Le seguenti raccomandazioni sono un orientamento per evitare ritardi nella consegna dei messaggi:

| Considerazione | Limite consigliato | Descrizione |
| ------- | ------- | ------- |
| Attributi per ricerca | Fino a 20 | Numero di campi dati recuperati per record in una singola attività di ricerca. |
| Attività di ricerca | Fino a 5 al percorso | Each journey can contain up to 5 separate lookup activities. Each lookup can target a different dataset. |

## Configurare l’attività di ricerca del set di dati {#configure}

Per configurare l&#39;attività **[!UICONTROL Ricerca set di dati]**, eseguire la procedura seguente:

1. Espandi la categoria **[!UICONTROL Orchestrazione]** e rilascia un&#39;attività **[!UICONTROL Ricerca set di dati]** nell&#39;area di lavoro.

   ![[!DNL Adobe Experience Platform] attività di ricerca set di dati nel percorso](assets/aep-data-activity.png)

1. Aggiungi un’etichetta e una descrizione.

1. In the **[!UICONTROL Dataset]** field, select the dataset with the attributes you need.

   >[!NOTE]
   >
   >If the dataset you are looking for does not display in the list, make sure you have enabled it for lookup. For more details, refer to the [Must read](#must-read) section.

1. Select the specific fields you want to fetch from the dataset.

   * You can only select leaf nodes (fields at the lowest level of the schema). Il campo deve essere un valore primitivo (stringa, numero, booleano, data e così via).

   * Non è possibile selezionare elenchi (array) e mappe (oggetti chiave-valore).

   +++Esempio

   ![Selezione del campo del set di dati con tipi di dati e struttura di base](assets/aep-data-leaf-primitive.png)

   +++

1. Nel campo **[!UICONTROL Chiavi di ricerca]**, scegli una chiave di unione esistente sia negli attributi dell&#39;elemento di decisione che nel set di dati. Questa chiave viene utilizzata dal sistema per eseguire ricerche nel set di dati selezionato.

   * Le chiavi possono essere espressioni derivate dal contesto del percorso, ad esempio SKU, ID e-mail o altri identificatori. Example: `@profile.email` or `list(@event{purchase_event.products.sku})`.

   * Only **strings** or **lists of strings** are supported.

   >[!IMPORTANT]
   >
   >È necessario definire la chiave di ricerca utilizzando **modalità avanzata**. Se si utilizza la modalità semplice per impostare la chiave, l&#39;output dell&#39;attività di ricerca del set di dati non sarà disponibile come attributo di contesto nelle attività a valle e la sintassi `@datasetLookup{}` avrà esito negativo con un errore &quot;Ricerca set di dati non trovata&quot; nelle attività condizione.

   +++Esempio

   ![Editor espressioni con funzioni di ricerca campi set di dati e stringhe](assets/aep-data-strings.png)

   +++

## Utilizzare dati arricchiti nel percorso

I dati recuperati dall&#39;attività **[!UICONTROL Ricerca set di dati]** vengono memorizzati nel contesto del Percorso come array di oggetti. It is available in the journey expression editor and personalization editor, enabling conditional logic and personalized messaging based on enriched data.

* **Journey Expression Editor**:

  Access the **[!UICONTROL Advanced mode]** editor and use the syntax: `@datasetLookup{MyDatasetLookUpActivity1.entities}`. [Learn how to work with the advanced expression editor](../building-journeys/expression/expressionadvanced.md)

* **Editor Personalization**:

  Utilizzare la sintassi: `{{context.journey.datasetLookup.1482319411.entities}}`.

>[!NOTE]
>
>I dati arricchiti sono transitori e disponibili solo durante il runtime del percorso e nella personalizzazione delle attività in uscita (e-mail, push, SMS, ecc.)

## Esempi di casi d’uso

+++Filtro basato su categorie di prodotti

**Scenario**:Send un coupon per gli utenti che spendono più di $ 40 per i prodotti per la casa.

**Flusso Percorso**:

1. **Evento di acquisto**: acquisisci SKU dal carrello dell&#39;utente.

1. **Attività di ricerca set di dati**:

   * Set di dati: `products-dataset` (SKU come chiave primaria).
   * Chiavi di ricerca: `list(@event{purchase_event.products.sku})`.
   * Campi da restituire: `["SKU", "category", "price"]`.

1. **Attività condizione**:

   * Filtra gli SKU in cui la categoria è &quot;famiglia&quot;.

     ```
     @event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookupActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )} 
     ```

   O

   * Aggrega la spesa totale per i prodotti per la casa e confrontala con la soglia di 40 $.

     ```
     sum(@event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookUpActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )}.price}, ',', true ) > 40
     ```

1. **Editor Personalization**:

   Utilizza i dati arricchiti per personalizzare il contenuto dell’e-mail:

   ```
   {% let householdTotal = 0 %}
   {{#each journey.datasetlookup.3709000.entities as |product|}}
   {%#if get(product, "category") = "household"%}
   {% let householdTotal = householdTotal + product.price %}{%/if%}
   {{/each}}
   "Hi, thanks for spending " + {%= householdTotal %} + " on household products. Here is your reward!"
   ```

+++

+++Personalization che utilizza dati fedeltà esterni

**Scenario**: Identify which email account for a profile has a Loyalty Status of Platinum. In this scenario, loyalty account is associated to an email ID and loyalty data is not available in the standard profile lookup store.

**Flusso Percorso**:

1. **Profile Event Trigger**: Capture email IDs from the profile or event context.

1. **Attività di ricerca set di dati**:
   * Set di dati: `loyalty-member-dataset` (e-mail come chiave primaria).
   * Chiavi di ricerca: `@profile.email`.
   * Campi da restituire: `["email", "loyaltyTier"]`.

1. **Attività condizione**:

   Dividi il percorso in base al livello di fedeltà:

   ```
   @datasetLookup{MyDatasetLookUpActivity1.entity.loyaltyMember.loyaltyTier} == 'Platinum'
   ```

1. **Editor Personalization**:

   Utilizza i dati del livello fedeltà arricchito per personalizzare la comunicazione in uscita:

   ```
   {{context.journey.datasetLookup.1482319411.entity.loyaltyMember.loyaltyTier}}
   ```

+++

## Risoluzione dei problemi {#troubleshooting}

### Errore &quot;Ricerca set di dati non trovata&quot; nell’attività della condizione {#troubleshooting-not-found}

**Sintomo:** La sintassi `@datasetLookup{}` nell&#39;editor di espressioni avanzate di un&#39;attività condizione restituisce un errore &quot;Ricerca set di dati non trovata&quot;, anche se l&#39;attività di ricerca set di dati è configurata correttamente nel percorso.

**Cause:** The lookup key in the dataset lookup activity was set using simple mode. Quando la chiave non è definita in modalità avanzata, l’output dell’attività non viene esposto come attributo di contesto nelle attività a valle.

**Correzione:** Apri l&#39;attività di ricerca del set di dati, individua il campo **[!UICONTROL Chiavi di ricerca]** e passa alla **modalità avanzata** per ridefinire l&#39;espressione chiave. Salva l’attività e ripubblica il percorso.
