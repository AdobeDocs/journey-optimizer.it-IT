---
solution: Journey Optimizer
product: journey optimizer
title: Personalizzare il contenuto utilizzando i dati di un endpoint esterno
description: Scopri come recuperare in modo dinamico i dati da un endpoint esterno per personalizzare il contenuto in entrata.
badge: label="Disponibilità limitata" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---


# Personalizzare il contenuto utilizzando i dati di un endpoint esterno {#data-endpoint}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata).

Journey Optimizer ti consente di sfruttare i dati di un endpoint esterno per personalizzare il contenuto nei canali in entrata, come i canali Esperienza basata su codice, Web e Messaggio in-app.

A tale scopo, nell&#39;editor di personalizzazione è disponibile una funzione di assistenza dedicata, `externalDataLookup`. Per utilizzare l&#39;helper, è innanzitutto necessario definire un&#39;[!DNL Journey Optimizer] **Azione** in cui configurare i dettagli sull&#39;endpoint esterno.

## Da leggere

### Esecuzione runtime

Quando un&#39;azione in entrata include un helper externalDataLookup, l&#39;endpoint viene chiamato in modo dinamico nel momento in cui la richiesta di personalizzazione viene ricevuta ed elaborata dall&#39;Edge Network [!DNL Adobe Experience Platform]. Ciò significa che l’endpoint esterno deve essere in grado di gestire un carico e una velocità effettiva simultanei almeno pari a quelli che il client invia per la superficie specificata all’Edge Network di AEP.

### Autenticazione

Le opzioni di autenticazione nella configurazione Action non sono attualmente supportate dall&#39;helper externalDataLookup.
Nel frattempo, per l’autenticazione basata su chiave API o altre chiavi di autorizzazione in testo normale, puoi specificarle come campi di intestazione nella configurazione Azione.
SOLO per endpoint interni ad Adobe: contatta il team ingegneristico di AJO per abilitare l’autenticazione basata su token di servizio per un endpoint.

### Guardrail e limitazioni

Consulta anche Azioni personalizzate in Campagne e Percorsi di canali in entrata AJO#GuardrailsandGuidelines

Per impostazione predefinita, AJO utilizza un timeout di 300 ms per la chiamata a un endpoint esterno. Contatta il team ingegneristico di AJO per richiedere un timeout maggiore per un endpoint.
Nell’editor di Personalization, AJO non consente di sfogliare lo schema della risposta dell’endpoint durante l’inserimento delle espressioni e non convalida i riferimenti agli attributi JSON dalla risposta utilizzata nelle espressioni.
I tipi di dati supportati per i parametri delle variabili di payload da sostituire tramite l’helper externalDataLookup sono String, Integer, Decimal, Boolean, listString, listInt, listInteger, listDecimal
Le modifiche alla configurazione di un’azione non si riflettono nelle corrispondenti chiamate externalDataLookup nelle campagne e nei percorsi live. Affinché una modifica venga rispecchiata, è necessario copiare o modificare tutte le campagne o i percorsi live che utilizzano l’azione in un helper externalDataLookup.
L’utilizzo di variabili non è ancora supportato all’interno di parametri helper per la ricerca di dati esterni.
Il percorso URL dinamico non è attualmente supportato.  - Miglioramenti azioni personalizzate in entrata#DynamicPathSegments

## Creare un’azione

Crea un’azione per configurare l’endpoint per la ricerca. Questa operazione deve essere eseguita solo una volta per ogni endpoint e deve essere eseguita da un utente tecnico. Consulta questa pagina.

La stessa azione può essere utilizzata sia in un&#39;attività **[!UICONTROL Azione personalizzata]** per recuperare contenuto in un percorso che in una funzione helper `externalDataLookup` per recuperare dati in un&#39;azione in entrata in un percorso o in una campagna.

Passare al menu **[!UICONTROL Amministrazione]** / **[!UICONTROL Configurazioni]**.

Prendi nota dell’ID azione e copialo per utilizzarlo nel passaggio 6.


## Personalizzare il contenuto utilizzando i dati recuperati

### Aggiungi la funzione di assistenza al contenuto

1. Crea una campagna in entrata o un’azione di percorso e modificane il contenuto.

1. Individua il contenuto in cui desideri utilizzare i dati memorizzati dall’endpoint esterno e accedi all’editor di personalizzazione.

1. Selezionare il menu Funzioni helper e individuare la funzione helper `externalDataLookup`.

1. Selezionare questa opzione per inserire la sintassi associata nel codice e sostituire i valori dei parametri `actionId` e `result` come segue:

   * `actionId` : Incolla l&#39;nID azione copiato durante la creazione dell&#39;azione.
   * `result`: impostare questo parametro sul nome desiderato. Utilizzerai questa variabile di risultati per accedere al contenuto recuperato.

1. Aggiungi eventuali valori dei parametri della variabile da passare come parte della chiamata dell&#39;endpoint. Ad esempio, ecco come si può trasmettere un parametro di linguaggio e un parametro di elementi max.

### Personalizzare utilizzando i dati recuperati

Per accedere ai dati recuperati da una chiamata di ricerca dell’endpoint esterno, puoi fare riferimento ai campi definiti nel payload di risposta nella definizione dell’azione utilizzando espressioni di personalizzazione e funzioni di supporto.

Utilizza la variabile `result` per accedere ai dati recuperati e inserirla nel contenuto per l’azione in entrata. Ad esempio, ecco come restituire un array JSON di elementi recuperati dall’endpoint.

Prendiamo l’esempio seguente, in cui il payload di risposta nell’azione è stato configurato come segue:

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Personalization esempio 1: visualizza la descrizione del primo video in un’azione Experience HTML basata su codice:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Personalization esempio 2 - Restituire un array di elementi in un’azione JSON Experience basata su codice:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## Timeout e gestione degli errori

AJO utilizza un timeout rigido quando chiama l’endpoint esterno per mantenere caratteristiche di prestazioni a bassa latenza e throughput elevato per AEP Edge Network.

Se l’endpoint si interrompe o viene rilevato un errore di qualsiasi tipo che raggiunge l’endpoint, la variabile di risultato sarà vuota. Anche eventuali riferimenti agli attributi all’interno della variabile di risultato in questo caso saranno vuoti. Se visualizzi semplicemente l’attributo nel contenuto, questo verrà visualizzato come vuoto. Se si tenta di scorrere ciclicamente un attributo di array nel risultato, non verrà restituito alcun elemento.

Se desideri gestire in modo più appropriato i timeout o gli errori mostrando il contenuto di fallback, puoi verificare se il risultato della ricerca è vuoto e visualizzare in tal caso il contenuto di fallback.

Ad esempio, puoi visualizzare un valore di fallback per un singolo attributo come questo:

Prima descrizione video: {%=result.videos[0].description ?: &quot;none found&quot; %}


oppure puoi eseguire il rendering condizionale di un intero blocco di contenuto come questo:

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if risultato%}
...fare qualcosa con il risultato...
{%else%}
... restituiscono il contenuto di fallback ...
{%/if%}
Debug
Per facilitare il debug, i dettagli del timeout e dell’errore per le ricerche di dati esterni sono inclusi nella vista Edge Delivery in AEP Assurance. Se non visualizzi i risultati previsti per un helper externalDataLookup in un’azione in entrata, puoi avviare una sessione Assurance, avviare una chiamata AJO da un’implementazione web o mobile e utilizzare la visualizzazione Edge Delivery per verificare la presenza di dettagli di timeout o errore.

Ad esempio:

Nella sezione Edge Delivery di traccia dell’affidabilità come parte dei dettagli di esecuzione è stato aggiunto un nuovo blocco customActions con

dettagli di richiesta e risposta simili a quelli riportati di seguito. La sezione errori dovrebbe facilitare il debug in caso di problemi durante l’esecuzione di un’azione personalizzata

## Domande frequenti

+++Come passare un attributo contestuale dalla richiesta come parametro a una ricerca dati esterna?

Utilizza il menu Attributi contestuali > Stream di dati > Evento per sfogliare lo schema Experience Event in uso e inserire l’attributo rilevante come valore di parametro come segue:

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++AJO memorizza nella cache le risposte degli endpoint esterni?

Non al momento. Questa funzione sarà supportata in futuro.

+++









Sintassi
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



Trasmissione dei parametri
Quando viene chiamato l&#39;endpoint esterno, tutti i valori di intestazione costanti, i parametri di query e il valore di payload della richiesta definiti nell&#39;azione vengono inviati con i valori forniti nella configurazione dell&#39;azione.

Per qualsiasi valore di intestazione variabile, parametri di query/percorso o valori di payload della richiesta, è possibile trasmettere valori in modo dinamico utilizzando i parametri all’helper externalDataLookup.

Nomi parametri:

Parametri intestazione: header.<parameter-name>
Parametri query: query.<parameter-name>
Parametri di payload: payload.<parameter-name>
Path Parameters (Parametri percorso): dynamic_path.<parameter-name>
Ad esempio:

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
I valori dei parametri possono essere valori fissi o personalizzati facendo riferimento a campi di profilo o altri attributi contestuali, ad esempio:

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
I parametri di payload possono essere forniti utilizzando la notazione del punto per fare riferimento agli attributi JSON nidificati, ad esempio:

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}