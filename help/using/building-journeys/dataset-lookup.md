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
TQID: https://experienceleague.adobe.com/4sQ3A15j47fQ6hI1G9oS6T6ne9nbxIaeqc-95zSUIq4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: []
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 908
ht-degree: 11%

---

# Utilizzare i dati [!DNL Adobe Experience Platform] nei percorsi {#datalookup}

>[!CONTEXTUALHELP]
>id="ajo_journey_dataset_lookup"
>title="Attività di ricerca del set di dati"
>abstract="L’attività **[!UICONTROL Ricerca nei set di dati]** consente di recuperare dinamicamente i dati dai set di dati dei record di [!DNL Adobe Experience Platform] durante il runtime. Sfruttando questa funzionalità, puoi accedere ai dati che potrebbero non trovarsi nel profilo o nel payload dell’evento, garantendo che le interazioni della clientela siano pertinenti e tempestive."

L’attività **[!UICONTROL Ricerca nei set di dati]** consente di recuperare dinamicamente i dati dai set di dati dei record di [!DNL Adobe Experience Platform] durante il runtime. Sfruttando questa funzionalità, puoi accedere ai dati che potrebbero non trovarsi nel profilo o nel payload dell’evento, garantendo che le interazioni della clientela siano pertinenti e tempestive.

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile per tutti i clienti come versione a disponibilità limitata.

Vantaggi principali:

* **Personalizzazione in tempo reale**: personalizza le esperienze dei clienti utilizzando dati arricchiti.
* **Processo decisionale dinamico**: utilizza dati esterni per indirizzare la logica e le azioni del percorso.
* **Accesso ai dati migliorato**: recupera i metadati di prodotto, le tabelle dei prezzi o i dati relazionali associati a chiavi specifiche.

## Da leggere {#must-read}

Esamina questi requisiti prima di configurare le ricerche dei set di dati.

### Abilitazione set di dati

Il set di dati deve essere abilitato per la ricerca in [!DNL Adobe Experience Platform]. Informazioni dettagliate sono disponibili in questa sezione: [Usa [!DNL Adobe Experience Platform] dati](../data/lookup-aep-data.md).

### Limiti e restrizioni

* Massimo 10 attività di ricerca set di dati al percorso.
* Massimo 20 campi selezionati.
* Massimo 50 chiavi nell’array delle chiavi di ricerca.
* La dimensione dei dati arricchiti è limitata a 10 KB.

### Considerazioni aggiuntive sulle prestazioni

Le seguenti raccomandazioni sono un orientamento per evitare ritardi nella consegna dei messaggi:

| Considerazione | Limite consigliato | Descrizione |
| ------- | ------- | ------- |
| Attributi per ricerca | Fino a 20 | Numero di campi dati recuperati per record in una singola attività di ricerca. |
| Attività di ricerca | Fino a 5 al percorso | Ogni percorso può contenere fino a 5 attività di ricerca separate. Ogni ricerca può eseguire il targeting di un set di dati diverso. |

## Configurare l’attività di ricerca del set di dati {#configure}

Per configurare l&#39;attività **[!UICONTROL Ricerca set di dati]**, eseguire la procedura seguente:

1. Espandi la categoria **[!UICONTROL Orchestrazione]** e rilascia un&#39;attività **[!UICONTROL Ricerca set di dati]** nell&#39;area di lavoro.

   ![[!DNL Adobe Experience Platform] attività di ricerca set di dati nel percorso](assets/aep-data-activity.png)

1. Aggiungi un’etichetta e una descrizione.

1. Nel campo **[!UICONTROL Set di dati]**, seleziona il set di dati con gli attributi necessari.

   >[!NOTE]
   >
   >Se il set di dati che stai cercando non viene visualizzato nell’elenco, assicurati di averlo abilitato per la ricerca. Per ulteriori dettagli, consulta la sezione [Da leggere](#must-read).

1. Seleziona i campi specifici che desideri recuperare dal set di dati.

   * Puoi selezionare solo nodi foglia (campi al livello più basso dello schema). Il campo deve essere un valore primitivo (stringa, numero, booleano, data e così via).

   * Non è possibile selezionare elenchi (array) e mappe (oggetti chiave-valore).

   +++Esempio

   ![Selezione del campo del set di dati con tipi di dati e struttura di base](assets/aep-data-leaf-primitive.png)

   +++

1. Nel campo **[!UICONTROL Chiavi di ricerca]**, scegli una chiave di unione esistente sia negli attributi dell&#39;elemento di decisione che nel set di dati. Questa chiave viene utilizzata dal sistema per eseguire ricerche nel set di dati selezionato.

   * Le chiavi possono essere espressioni derivate dal contesto del percorso, ad esempio SKU, ID e-mail o altri identificatori. Esempio: `@profile.email` o `list(@event{purchase_event.products.sku})`.

   * Sono supportati solo **stringhe** o **elenchi di stringhe**.

   >[!IMPORTANT]
   >
   >È necessario definire la chiave di ricerca utilizzando **modalità avanzata**. Se si utilizza la modalità semplice per impostare la chiave, l&#39;output dell&#39;attività di ricerca del set di dati non sarà disponibile come attributo di contesto nelle attività a valle e la sintassi `@datasetLookup{}` avrà esito negativo con un errore &quot;Ricerca set di dati non trovata&quot; nelle attività condizione.

   +++Esempio

   ![Editor espressioni con funzioni di ricerca campi set di dati e stringhe](assets/aep-data-strings.png)

   +++

## Utilizzare dati arricchiti nel percorso

I dati recuperati dall&#39;attività **[!UICONTROL Ricerca set di dati]** vengono memorizzati nel contesto del Percorso come array di oggetti. È disponibile nell’editor di espressioni di percorso e nell’editor di personalizzazione, abilitando la logica condizionale e la messaggistica personalizzata in base a dati arricchiti.

* **Editor espressioni Percorso**:

  Accedere all&#39;editor **[!UICONTROL Modalità avanzata]** e utilizzare la sintassi: `@datasetLookup{MyDatasetLookUpActivity1.entities}`. [Scopri come utilizzare l&#39;editor di espressioni avanzate](../building-journeys/expression/expressionadvanced.md)

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

**Scenario**: identifica l&#39;account e-mail per un profilo con stato di fedeltà Platinum. In questo scenario, l’account fedeltà è associato a un ID e-mail e i dati fedeltà non sono disponibili nell’archivio di ricerca profilo standard.

**Flusso Percorso**:

1. **Attivatore evento profilo**: acquisisce gli ID e-mail dal profilo o dal contesto dell&#39;evento.

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

**Causa:** La chiave di ricerca nell&#39;attività di ricerca del set di dati è stata impostata in modalità semplice. Quando la chiave non è definita in modalità avanzata, l’output dell’attività non viene esposto come attributo di contesto nelle attività a valle.

**Correzione:** Apri l&#39;attività di ricerca del set di dati, individua il campo **[!UICONTROL Chiavi di ricerca]** e passa alla **modalità avanzata** per ridefinire l&#39;espressione chiave. Salva l’attività e ripubblica il percorso.
