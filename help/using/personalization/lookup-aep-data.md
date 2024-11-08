---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare i dati di Adobe Experience Platform per la personalizzazione (Beta)
description: Scopri come utilizzare i dati di Adobe Experience Platform per la personalizzazione.
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: cb7842209e03c579904979480304e543a6b50f50
workflow-type: tm+mt
source-wordcount: '1015'
ht-degree: 0%

---

# Utilizzare i dati di Adobe Experience Platform per la personalizzazione (Beta) {#aep-data}

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile per tutti i clienti come versione beta pubblica.
>
>Per utilizzare questa funzionalità, devi prima accettare i termini beta per la tua organizzazione che vengono visualizzati quando aggiungi le nuove funzioni helper &quot;datasetLookup&quot; nell’editor di personalizzazione.

Journey Optimizer ti consente di sfruttare i dati provenienti da Adobe Experience Platform nell&#39;editor di personalizzazione per [personalizzare il contenuto](../personalization/personalize.md). A questo scopo, i set di dati necessari per la personalizzazione della ricerca devono prima essere abilitati tramite una chiamata API come descritto di seguito. Al termine, puoi utilizzare i loro dati per personalizzare il contenuto in [!DNL Journey Optimizer].

## Restrizioni e linee guida di Beta {#guidelines}

Prima di iniziare, rivedi le seguenti restrizioni e linee guida:

### Abilitazione dei set di dati {#enablement}

* **La dimensione del set di dati** è limitata a 5 GB per i set di dati di produzione e a 1 GB per i set di dati sandbox di sviluppo
* **È possibile abilitare un massimo di 50 set di dati** per la ricerca per organizzazione in qualsiasi momento.
* **Il numero di record** è limitato a 5 milioni nei set di dati di produzione e a 1 milione nei set di dati sandbox di sviluppo.
* **L&#39;etichettatura e l&#39;applicazione dell&#39;utilizzo dati** non sono attualmente applicate per i set di dati abilitati per la ricerca.
* **I set di dati abilitati per la ricerca e utilizzati nella personalizzazione non sono protetti dall&#39;eliminazione**. Spetta a te tenere traccia dei set di dati utilizzati per la personalizzazione per assicurarti che non vengano eliminati o rimossi.

### Personalization con dati [!DNL Adobe Experience Platform] {#perso}

* **Canali supportati**: per il momento questa funzionalità è disponibile solo per l&#39;utilizzo nei canali e-mail, SMS, push e direct mail.
* **L&#39;etichettatura e l&#39;applicazione dell&#39;utilizzo dati** non sono attualmente applicate per i set di dati abilitati per la ricerca.
* **Frammenti di espressione**: al momento non è possibile inserire la personalizzazione della ricerca del set di dati all&#39;interno dei frammenti di espressione.

## Abilitare un set di dati per la ricerca di dati {#enable}

Per sfruttare i dati del set di dati per la personalizzazione, devi utilizzare una chiamata API per recuperarne lo stato e abilitare il servizio di ricerca.

### Prerequisiti {#prerequisites-enable}

* Segui le istruzioni descritte in [questa documentazione](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) per configurare l&#39;ambiente per l&#39;invio di comandi API.
* Il progetto dello sviluppatore deve includere le API Adobe Journey Optimizer e Adobe Experience Platform aggiunte al progetto.

  ![](assets/aep-data-api.png)

* Come parte del tuo ruolo, devi disporre dell’autorizzazione Gestione set di dati.
* Lo schema su cui si basa il set di dati deve contenere una **identità primaria** che può fungere da chiave di ricerca.

### Struttura delle chiamate API {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

Dove:

* **URL** è `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **ID set di dati** è il set di dati per il quale si desidera abilitare.
* **L&#39;azione** è abilitata O disabilitata.
* **Il token di accesso** può essere recuperato dalla console per sviluppatori.
* È possibile recuperare **la chiave API** dalla console per sviluppatori.
* **ID organizzazione IMS** è la tua organizzazione Adobe IMS.
* **Nome sandbox** è il nome della sandbox in cui si trova il set di dati (ad esempio, prod, dev, ecc.).

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

   * **result** è il valore assegnato al parametro **result** nella funzione helper **MultiEntity**. In questo esempio &quot;flight&quot;.
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
