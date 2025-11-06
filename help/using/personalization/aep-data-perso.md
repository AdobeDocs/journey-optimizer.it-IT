---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare i dati di Adobe Experience Platform per la personalizzazione
description: Scopri come utilizzare i dati di Adobe Experience Platform per la personalizzazione.
badge: label="Disponibilità limitata" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 3%

---

# Utilizzare i dati di Adobe Experience Platform per la personalizzazione {#aep-data}

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile per tutti i clienti come versione a disponibilità limitata.
>
>Per il momento, la funzione helper &quot;datasetLookup&quot; può essere utilizzata all’interno di frammenti di espressione per un set limitato di clienti. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

Journey Optimizer ti consente di sfruttare i dati dei set di dati dei record di Adobe Experience Platform nell&#39;editor di personalizzazione per [personalizzare il contenuto](../personalization/personalize.md). Prima di iniziare, i set di dati necessari per la personalizzazione della ricerca devono essere abilitati per la ricerca. Informazioni dettagliate sono disponibili in questa sezione: [Usa dati di Adobe Experience Platform](../data/lookup-aep-data.md).

Dopo aver abilitato un set di dati per la personalizzazione di ricerca, puoi utilizzarne i dati per personalizzare il contenuto in [!DNL Journey Optimizer].

1. Apri l’editor di personalizzazione, disponibile in ogni contesto in cui puoi definire la personalizzazione, ad esempio i messaggi. [Scopri come utilizzare l&#39;editor di personalizzazione](../personalization/personalization-build-expressions.md)

1. Passare all&#39;elenco delle funzioni di supporto e aggiungere la funzione di supporto **datasetLookup** al riquadro del codice.

   ![](assets/aep-data-helper.png)

1. Questa funzione fornisce una sintassi predefinita per consentire di chiamare campi dai set di dati di Adobe Experience Platform. La sintassi è la seguente:

   ```
   {{datasetLookup datasetId="datasetId" id="key" result="store" required=false}}
   ```

   * **datasetId** è l&#39;ID del set di dati con cui stai lavorando.
   * **id** è l&#39;ID della colonna di origine che deve essere unita all&#39;identità primaria del set di dati di ricerca.

     >[!NOTE]
     >
     >Il valore immesso per questo campo può essere un ID campo (`profile.packages.packageSKU`), un campo passato in un evento di percorso (`context.journey.events.event_ID.productSKU`) o un valore statico (`sku007653`). In ogni caso, il sistema utilizzerà il valore e la ricerca nel set di dati per verificare se corrisponde a una chiave.
     >
     >Se utilizzi un valore stringa letterale per la chiave, tieni il testo tra virgolette. Esempio: `{{datasetLookup datasetId="datasetId" id="SKU1234" result="store" required=false}}`. Se si utilizza un valore di attributo come chiave dinamica, rimuovere le virgolette. Esempio: `{{datasetLookup datasetId="datasetId" id=category.product.SKU result="SKU" required=false}}`

   * **result** è un nome arbitrario che devi fornire per fare riferimento a tutti i valori di campo che stai per recuperare dal set di dati. Questo valore verrà utilizzato nel codice per chiamare ogni campo.

   * **required=false**: se required è impostato su TRUE, il messaggio verrà recapitato solo se viene trovata una chiave corrispondente. Se è impostato su false, non è necessaria una chiave corrispondente e il messaggio può ancora essere recapitato. Se impostato su false, è consigliabile tenere conto dei valori di fallback o predefiniti nel contenuto del messaggio.

   +++Dove recuperare un ID set di dati?

   Gli ID dei set di dati possono essere recuperati nell’interfaccia utente di Adobe Experience Platform. Scopri come utilizzare i set di dati nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

   ![](assets/aep-data-dataset.png)

   +++

1. Adatta la sintassi in base alle tue esigenze. In questo esempio, vogliamo recuperare i dati relativi ai voli dei passeggeri. La sintassi è la seguente:

   ```
   {{datasetLookup datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * Stiamo lavorando nel set di dati il cui ID è &quot;1234567890abcdtId&quot;,
   * Il campo che si desidera utilizzare per effettuare un&#39;unione con il set di dati di ricerca è *profile.upcomingFlightId*,
   * Vogliamo includere tutti i valori dei campi nel riferimento &quot;volo&quot;.

1. Una volta configurata la sintassi da chiamare nel set di dati di Adobe Experience Platform, puoi specificare quali campi recuperare. La sintassi è la seguente:

   ```
   {{result.fieldId}}
   ```

   >[!NOTE]
   >
   >Quando fai riferimento a un campo di set di dati, accertati di corrispondere al percorso completo del campo definito all’interno dello schema.
   >
   >Non vi sono limiti rigidi al numero di campi che possono essere richiamati utilizzando la funzione helper. Tuttavia, per prestazioni ottimali, si consiglia di mantenere il numero di campi al di sotto di 50 per evitare di influire sulla velocità effettiva.

   * **result** è il valore assegnato al parametro **result** nella funzione helper **datasetLookup**. In questo esempio, &quot;flight&quot;.
   * **fieldID** è l&#39;ID del campo che si desidera recuperare. Questo ID è visibile nell&#39;interfaccia utente di [!DNL Adobe Experience Platform] durante la navigazione nello schema di record relativo al set di dati:

     +++Dove recuperare un ID campo?

     Gli ID dei campi possono essere recuperati durante l’anteprima di un set di dati nell’interfaccia utente di Adobe Experience Platform. Scopri come visualizzare in anteprima i set di dati nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

     +++

   In questo esempio, vogliamo utilizzare le informazioni relative all&#39;orario di imbarco e al gate dei passeggeri. Pertanto, aggiungiamo queste due righe:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Ora che il codice è pronto, puoi completare il contenuto come di consueto e testarlo utilizzando il pulsante **Simula contenuto** per controllare la personalizzazione. [Scopri come visualizzare in anteprima e testare il contenuto](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
