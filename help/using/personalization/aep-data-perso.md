---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare i dati di Adobe Experience Platform per la personalizzazione (Beta)
description: Scopri come utilizzare i dati di Adobe Experience Platform per la personalizzazione.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: 7e378cbda6ee2379a8bd795588c328cb14107aa4
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 3%

---

# Utilizzare i dati di Adobe Experience Platform per la personalizzazione{#aep-data}

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile per tutti i clienti come versione beta pubblica.
>
>Per utilizzare questa funzionalità, devi prima accettare i termini beta per la tua organizzazione che vengono visualizzati quando aggiungi le nuove funzioni helper &quot;datasetLookup&quot; nell’editor di personalizzazione.

Journey Optimizer ti consente di sfruttare i dati provenienti da Adobe Experience Platform nell&#39;editor di personalizzazione per [personalizzare il contenuto](../personalization/personalize.md). A questo scopo, i set di dati necessari per la personalizzazione della ricerca devono prima essere abilitati tramite una chiamata API come descritto di seguito. Al termine, è possibile utilizzare i relativi dati per personalizzare il contenuto in [!DNL Journey Optimizer].

## Restrizioni e linee guida di Beta {#guidelines}

Prima di iniziare, rivedi le seguenti restrizioni e linee guida:

* **Canali supportati**: per il momento questa funzionalità è disponibile solo per l&#39;utilizzo nei canali e-mail, SMS e direct mail.
* **Frammenti**: al momento non è possibile inserire la personalizzazione di ricerca del set di dati all&#39;interno di frammenti di espressione o visivi.

### Funzione Decisioni {#decisioning}

La possibilità di sfruttare [!DNL Adobe Experience Platform] set di dati nelle formule e nelle regole di classificazione di Experience Decisioning sarà presto disponibile.

Nel frattempo, si prega di rivedere le attuali protezioni descritte di seguito:

* Una politica decisionale è limitata a 3 set di dati,
* Una regola di decisione può utilizzare 3 set di dati,
* Una formula di classificazione può utilizzare 3 set di dati,
* Un criterio di decisione è limitato a 1000 query di record.

>[!NOTE]
>
>Per accedere a questa funzionalità, contatta il rappresentante del tuo account

## Abilitare un set di dati per la ricerca di dati {#enable}

Per sfruttare i dati del set di dati per la personalizzazione, devi utilizzare una chiamata API per recuperarne lo stato e abilitare il servizio di ricerca. Informazioni dettagliate sono disponibili in questa sezione: [Sfruttare i set di dati di Adobe Experience Platform in [!DNL Journey Optimizer]](../data/lookup-aep-data.md)

## Sfruttare un set di dati per la personalizzazione {#leverage}

Dopo aver abilitato un set di dati per la personalizzazione di ricerca tramite una chiamata API, puoi utilizzarne i dati per personalizzare il contenuto in [!DNL Journey Optimizer].

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
     >Il valore immesso per questo campo può essere un ID campo (*profile.packages.packageSKU*), un campo passato in un evento di percorso (*context.percorsi.events.event_ID.productSKU*) o un valore statico (*sku007653*). In ogni caso, il sistema utilizzerà il valore e la ricerca nel set di dati per verificare se corrisponde a una chiave.
     >
     >Se utilizzi un valore stringa letterale per la chiave, tieni il testo tra virgolette. Esempio: `{{datasetLookup datasetId="datasetId" id="SKU1234" result="store" required=false}}`. Se si utilizza un valore di attributo come chiave dinamica, rimuovere le virgolette. Esempio: `{{datasetLookup datasetId="datasetId" id=category.product.SKU result="SKU" required=false}}`

   * **result** è un nome arbitrario che devi fornire per fare riferimento a tutti i valori di campo che stai per recuperare dal set di dati. Questo valore verrà utilizzato nel codice per chiamare ogni campo.

   * **required=false**: se required è impostato su TRUE, il messaggio verrà recapitato solo se viene trovata una chiave corrispondente. Se è impostato su false, non è necessaria una chiave corrispondente e il messaggio può ancora essere recapitato. Se impostato su false, è consigliabile tenere conto dei valori di fallback o predefiniti nel contenuto del messaggio.

   +++Dove recuperare un ID set di dati?

   Gli ID dei set di dati possono essere recuperati nell’interfaccia utente di Adobe Experience Platform. Scopri come utilizzare i set di dati nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

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

   * **result** è il valore assegnato al parametro **result** nella funzione helper **MultiEntity**. In questo esempio &quot;flight&quot;.
   * **fieldID** è l&#39;ID del campo che si desidera recuperare. Questo ID è visibile nell&#39;interfaccia utente di [!DNL Adobe Experience Platform] durante la navigazione nello schema di record relativo al set di dati:

     +++Dove recuperare un ID campo?

     Gli ID dei campi possono essere recuperati durante l’anteprima di un set di dati nell’interfaccia utente di Adobe Experience Platform. Scopri come visualizzare in anteprima i set di dati nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

     +++

   In questo esempio, vogliamo utilizzare le informazioni relative all&#39;orario di imbarco e al gate dei passeggeri. Pertanto, aggiungiamo queste due righe:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Ora che il codice è pronto, puoi completare il contenuto come di consueto e testarlo utilizzando il pulsante **Simula contenuto** per controllare la personalizzazione. [Scopri come visualizzare in anteprima e testare il contenuto](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
