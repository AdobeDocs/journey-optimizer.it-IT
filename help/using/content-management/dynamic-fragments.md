---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare frammenti dinamici
description: Scopri come utilizzare la risoluzione dei frammenti dinamici in Adobe Journey Optimizer per selezionare e inserire frammenti in fase di esecuzione in base ad attributi di profilo, ricerche di set di dati o dati contestuali.
feature: Fragments
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: dinamico, frammento, espressione, personalizzazione, runtime
source-git-commit: b4affc5b905236419928a65cd173173b49058827
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 2%

---

# Utilizzare frammenti dinamici {#dynamic-fragments}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare la risoluzione dei frammenti dinamici in Adobe Journey Optimizer per selezionare il frammento pubblicato da inserire in un messaggio in fase di esecuzione, in base agli attributi di profilo, alle ricerche di set di dati o ai dati contestuali passati al momento dell&#39;invio.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] supporta **la risoluzione frammento dinamico** in fase di esecuzione, consentendo di selezionare il frammento pubblicato inserito in un messaggio in base agli attributi di profilo, alle ricerche di set di dati o ai dati contestuali passati al momento dell&#39;invio. Ciò consente di ottenere contenuti altamente personalizzati senza duplicare la logica di campagna o di percorso.

## Panoramica {#overview}

**Frammenti statici** sono incorporati in un messaggio in fase di progettazione. Lo stesso frammento viene utilizzato per ogni destinatario. **I frammenti dinamici** risolvono l&#39;ID frammento in fase di esecuzione per destinatario, il che significa che profili diversi possono ricevere blocchi di contenuto completamente diversi all&#39;interno della stessa campagna o dello stesso percorso.

Gli ID frammento dinamico possono provenire da tre origini:

* Una **ricerca set di dati**, ad esempio un set di dati di consigli basato su stile o prodotto
* Attributo **profile** archiviato in Adobe Experience Platform
* **Dati contestuali** passati direttamente nella richiesta API al momento dell&#39;invio

>[!NOTE]
>
>L&#39;utilizzo della funzione helper `datasetLookup` all&#39;interno dei frammenti di espressione è attualmente disponibile per un gruppo limitato di clienti. Per potervi accedere, contatta il tuo rappresentante Adobe.

## Prerequisiti {#prerequisites}

Prima di utilizzare i frammenti dinamici, verifica che siano presenti gli elementi seguenti:

* Si dispone delle autorizzazioni necessarie per creare e pubblicare frammenti in [!DNL Journey Optimizer]. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)
* Il frammento a cui intendi fare riferimento è **pubblicato** (stato: **Live**). I frammenti bozza non possono essere risolti in fase di runtime.
* Se l&#39;ID frammento viene risolto da un set di dati, lo schema del set di dati include un campo che memorizza l&#39;ID frammento e il set di dati è [abilitato per la ricerca](../data/lookup-aep-data.md).
* Tutti gli attributi di profilo a cui fa riferimento il frammento dinamico stesso sono inclusi nel percorso di esportazione del messaggio o sono disponibili nel profilo al momento dell’invio.

>[!CAUTION]
>
>Le convalide relative ai frammenti vengono ignorate nel flusso del frammento dinamico. Gli ID frammento non validi vengono rilevati come errori di consegna in fase di runtime anziché come errori di convalida iniziali. Prima di attivare una campagna, verifica sempre che gli ID dei frammenti di riferimento siano validi e pubblicati.

## Passaggio 1: creare e pubblicare il frammento {#create-fragment}

Prima di fare riferimento a un frammento in modo dinamico, è necessario pubblicarlo in [!DNL Journey Optimizer].

1. In [!DNL Journey Optimizer], passare a **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Frammenti]**.

1. Seleziona **[!UICONTROL Crea frammento]** e crea il contenuto. [Scopri come creare frammenti](create-fragments.md)

1. Quando il contenuto è pronto, fare clic su **[!UICONTROL Pubblica]**. La pubblicazione è asincrona e potrebbe richiedere alcuni secondi. Prima di procedere, verifica che lo stato del frammento sia **Live**.

1. Nota l&#39;**ID frammento** dalla vista dei dettagli del frammento o dalla risposta API Frammenti. Farai riferimento a questo ID nel messaggio.

>[!NOTE]
>
>È possibile recuperare tutti gli ID frammento pubblicati a livello di programmazione utilizzando l&#39;API `GET /fragments`. Per ulteriori informazioni, consulta la [documentazione delle API di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}.

## Passaggio 2: creare il messaggio con un riferimento a un frammento dinamico {#author-message}

Nell’editor di personalizzazione, inserisci il segnaposto del frammento dinamico utilizzando la sintassi seguente:

```handlebars
{{fragment id=dynamic_fragment_id}}
```

L&#39;identificatore `dynamic_fragment_id` è un nome di variabile. Il relativo valore deve essere risolto prima che venga eseguita la ricerca del frammento. Puoi risolverlo utilizzando un’espressione di ricerca del set di dati, un attributo di profilo o dati contestuali.

### Risolvere da una ricerca di set di dati {#resolve-from-dataset}

Se l&#39;ID frammento è memorizzato in un set di dati di AEP (ad esempio, una tabella di mappatura stile-frammento), utilizza la funzione helper `datasetLookup` per risolverlo:

```handlebars
{{
  {datasetLookup datasetId="<your-dataset-id>" key=profile.style attribute="fragmentId"}
}}

{{fragment id=dynamic_fragment_id}}
```

In questo esempio, il set di dati contiene righe con chiave da un valore di stile (ad esempio `style1`). Per un determinato profilo, la ricerca recupera il valore di colonna `fragmentId` corrispondente e lo assegna a `dynamic_fragment_id`, che viene quindi utilizzato per risolvere il frammento.

>[!NOTE]
>
>L&#39;utilizzo della funzione helper `datasetLookup` all&#39;interno dei frammenti di espressione è attualmente disponibile per un gruppo limitato di clienti. Per potervi accedere, contatta il tuo rappresentante Adobe. Per ulteriori informazioni sulle ricerche di set di dati nella personalizzazione, consulta [Utilizzare i dati di Adobe Experience Platform](../data/lookup-aep-data.md).

### Risolvi da dati contestuali {#resolve-from-context}

Se l’ID frammento viene fornito al momento dell’invio come parte del contesto della richiesta API, fai riferimento a esso utilizzando lo spazio dei nomi `context`:

```handlebars
{{fragment id=context.audiencePayload.fragmentId}}
```

Il percorso `context.audiencePayload` è il prefisso richiesto per tutti gli attributi originati da un file di pubblico CSV o passati tramite il contesto della richiesta API. Il nome di colonna dal file CSV (ad esempio, `fragmentId`) segue il prefisso.

### Risolvi da un attributo di profilo {#resolve-from-profile}

Se l’ID frammento è memorizzato come attributo di profilo in Adobe Experience Platform, fai riferimento direttamente a esso:

```handlebars
{{fragment id=profile.mi.fragmentId}}
```

## Passaggio 3: configurare il set di dati per l’approccio di ricerca {#configure-dataset}

Se utilizzi l’approccio di ricerca dei set di dati, aggiorna lo schema e i dati del set di dati in modo che riportino l’ID del frammento.

1. Nel set di dati per la mappatura o i consigli, aggiungi una colonna (ad esempio, `fragmentId`) in cui viene memorizzato l&#39;ID frammento di AJO pubblicato per ogni riga.

1. Per ogni stile o variante (ad esempio, `style1`, `style2`), compila la colonna `fragmentId` con l&#39;ID frammento corrispondente.

1. Assicurati che il set di dati sia acquisito in Adobe Experience Platform e [abilitato per la ricerca](../data/lookup-aep-data.md).

1. Conferma che tutti gli attributi del profilo a cui si fa riferimento all’interno del frammento dinamico vengano acquisiti nel messaggio o in un frammento statico per impedire il rendering vuoto al momento dell’esportazione.

**Struttura di esempio del set di dati:**

| Colonna | Esempio di valore |
|---|---|
| stile | style1 |
| fragmentId | &lt;fragment-id-1> |
| stile | style2 |
| fragmentId | &lt;fragment-id-2> |

## Passaggio 4: trasmettere i dati contestuali al momento dell’invio {#pass-context-data}

Se stai risolvendo l’ID frammento dai dati contestuali (ad esempio, da un file di consigli del pubblico CSV), passa l’ID frammento nella richiesta API sotto il prefisso di contesto richiesto.

Quando utilizzi l&#39;API di verifica della campagna, includi l&#39;ID frammento nell&#39;oggetto `context`:

```json
{
  "recipients": [
    {
      "userId": "<profile-email>",
      "namespace": "email"
    }
  ],
  "inChannelData": {
    "channel": "email",
    "emailAddresses": ["<delivery-address>"]
  },
  "context": {
    "audiencePayload": {
      "fragmentId": "<published-fragment-id>",
      "systemSource": "<optional-system-value>"
    }
  }
}
```

Il prefisso `context.audiencePayload` è obbligatorio. Gli attributi nidificati sotto questa chiave vengono mappati direttamente alle colonne nel file del pubblico CSV durante l’esecuzione della campagna live.

## Passaggio 5: verifica e convalida {#proof-validate}

Prima di attivare la campagna, utilizza l’API di verifica della campagna per verificare che il frammento dinamico si risolve correttamente e che l’output dell’e-mail sottoposto a rendering sia come previsto.

1. Attiva un processo di bozza utilizzando l&#39;endpoint `POST /campaigns/{id}/proofs`. Nella richiesta di bozza, passa l&#39;ID frammento che desideri verificare in `context.audiencePayload.fragmentId`.

1. Eseguire il polling dello stato del processo di bozza utilizzando l&#39;endpoint `GET /campaigns/{id}/proofs/{proofId}` fino allo stato `Submitted` o `Failed`.

1. Controlla l’e-mail consegnata per verificare che sia stato eseguito il rendering del contenuto corretto del frammento.

1. Se il contenuto del frammento è mancante o errato, verifica che l’ID frammento sia valido, che il frammento sia pubblicato e che siano presenti tutti gli attributi di profilo richiesti.

Per ulteriori informazioni sull&#39;API di Campaign, consulta la [documentazione delle API di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"}.

## Guardrail e limitazioni {#guardrails}

>[!CAUTION]
>
>OLAC (Object-Level Access Control) non viene applicato ai frammenti nel modello di frammento dinamico. Assicurati che i requisiti di controllo degli accessi siano tenuti in considerazione a livello di campagna e pubblico.

Quando si utilizzano frammenti dinamici, si applicano le seguenti limitazioni:

* **Copertura degli attributi di profilo al momento dell&#39;esportazione**: il frammento viene scelto in fase di esecuzione per profilo. Gli attributi di profilo richiesti dal frammento dinamico non sono noti in anticipo. Se il frammento dinamico si basa su un attributo di profilo che non era presente nel messaggio originale o in qualsiasi frammento statico a cui si fa riferimento nel messaggio, tale campo può risultare vuoto nel percorso di esportazione.

* **Nessuna convalida del frammento iniziale**: in questo flusso vengono ignorate le convalide relative ai frammenti. Gli ID frammento errati o non pubblicati emergono come errori di consegna in fase di esecuzione anziché come errori di convalida visualizzati nell’interfaccia utente.

* **Modifica dello schema richiesta per l&#39;approccio al set di dati**: l&#39;utilizzo del percorso lookup per ID richiede l&#39;aggiornamento dello schema del set di dati per memorizzare e trasmettere l&#39;ID del frammento, oltre al plumbing necessario per inviarlo alla pipeline dei messaggi.

* **Acquisizione degli attributi per l&#39;esportazione**: assicurarsi che tutti gli attributi utilizzati all&#39;interno del frammento dinamico vengano acquisiti nel messaggio o in frammenti statici per impedire il rendering vuoto nel percorso di esportazione.

Ulteriori guardrail applicabili ai frammenti sono disponibili in [questa sezione](../start/guardrails.md#fragments-guardrails).

## Gestione degli errori {#error-handling}

Se un frammento dinamico non viene risolto in fase di runtime, viene generato un evento di esclusione per il profilo interessato. Attualmente, tutti gli errori di rendering dei frammenti sono classificati come un singolo tipo di errore aperto.

Per eseguire il debug degli errori di risoluzione dei frammenti:

1. Controlla i rapporti di consegna della campagna per individuare eventuali eventi di esclusione.
1. Verifica che l’ID frammento passato in fase di esecuzione corrisponda a un frammento pubblicato.
1. Verifica che tutti gli attributi di profilo richiesti dal frammento siano presenti nel profilo al momento dell’invio.
1. Utilizza l&#39;[API di verifica](#proof-validate) per testare ID frammento specifici prima di attivare la campagna.
