---
solution: Journey Optimizer
product: journey optimizer
title: Configurare un’azione personalizzata
description: Scopri come configurare un’azione personalizzata
feature: Actions
topic: Administration
role: Admin
level: Experienced
badge: label="Beta" type="Informative"
keywords: azione, terze parti, personalizzato, percorsi, API
hide: true
hidefromtoc: true
source-git-commit: 1674eceb1b9ae4cf8cd3f19deda26a9e72290106
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 9%

---

# Miglioramenti delle azioni personalizzate

Ora puoi sfruttare le risposte alle chiamate API nelle azioni personalizzate e orchestrare il percorso in base a tali risposte.

Questa funzionalità era disponibile solo quando si utilizzavano origini dati. Ora puoi utilizzarlo con azioni personalizzate.

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile come versione beta privata.

## Definizione dell’azione personalizzata

Durante la definizione dell’azione personalizzata, sono stati resi disponibili due miglioramenti: l’aggiunta del metodo GET e il nuovo campo di risposta del payload. Le altre opzioni e i parametri rimangono invariati. Consulta [questa pagina](../action/about-custom-action-configuration.md).

### Configurazione endpoint

Il **Configurazione URL** la sezione è stata rinominata **Configurazione endpoint**.

In **Metodo** a discesa, è ora possibile selezionare **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Payload

Il **Parametri azione** la sezione è stata rinominata **Payload**. Sono disponibili due campi:

* Il **Richiesta** campo: questo campo è disponibile solo per i metodi di chiamata POST e PUT.
* Il **Risposta** campo: questa è la nuova funzionalità. Questo campo è disponibile per tutti i metodi di chiamata.

>[!NOTE]
> 
>Entrambi questi campi sono facoltativi.

![](assets/action-response2.png){width="70%" align="left"}

1. Fai clic all’interno del **Risposta** campo.

   ![](assets/action-response3.png){width="70%" align="left"}

1. Incolla un esempio del payload restituito dalla chiamata. Verifica che i tipi di campo siano corretti (stringa, numero intero, ecc.).

   ![](assets/action-response4.png){width="70%" align="left"}

1. Fai clic su **Salva**.

Ogni volta che viene chiamata l’API, il sistema recupererà tutti i campi inclusi nell’esempio di payload. Puoi fare clic su **Incolla un nuovo payload** se desideri modificare il payload attualmente trasmesso.

Ecco un esempio di payload di risposta acquisito durante la chiamata a un servizio API meteo:

```
{
    "coord": {
        "lon": 2.3488,
        "lat": 48.8534
    },
    "weather": [
        {
            "id": 800,
            "main": "Clear",
            "description": "clear sky",
            "icon": "01d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 29.78,
        "feels_like": 29.78,
        "temp_min": 29.92,
        "temp_max": 30.43,
        "pressure": 1016,
        "humidity": 31
    },
    "visibility": 10000,
    "wind": {
        "speed": 5.66,
        "deg": 70
    },
    "clouds": {
        "all": 0
    },
    "dt": 1686066467,
    "sys": {
        "type": 1,
        "id": 6550,
        "country": "FR",
        "sunrise": 1686023350,
        "sunset": 1686080973
    },
    "timezone": 7200,
    "id": 2988507,
    "name": "Paris",
    "cod": 200
}
```

## Utilizzo della risposta in un percorso

È sufficiente aggiungere l’azione personalizzata a un percorso. Puoi quindi sfruttare i campi del payload di risposta in condizioni, altre azioni e personalizzazione dei messaggi.

### Condizioni e azioni

Ad esempio, puoi aggiungere una condizione per controllare la velocità del vento. Quando la persona entra nel negozio di surf puoi inviare una spinta se il tempo è troppo ventoso .

![](assets/action-response5.png){width="70%" align="left"}

Nella condizione, devi utilizzare l’editor avanzato per sfruttare i campi di risposta dell’azione, nella sezione **Contesto** nodo.

![](assets/action-response6.png){width="70%" align="left"}

Puoi anche sfruttare **jo_status** codice per creare un nuovo percorso in caso di errore.

![](assets/action-response7.png){width="70%" align="left"}

>[!WARNING]
>
>Solo le azioni personalizzate appena create includono questo campo pronto all’uso. Se desideri utilizzarla con un’azione personalizzata esistente, devi aggiornare l’azione. Ad esempio, puoi aggiornare la descrizione e salvare.

Di seguito sono riportati i possibili valori per questo campo:

* codice di stato http: ad esempio **http_200** o **http_400**
* errore di timeout: **timeout**
* errore di limite: **con limite**
* errore interno: **internalError**

### Personalizzazione dei messaggi

Puoi personalizzare i messaggi utilizzando i campi di risposta. Nel nostro esempio, nella notifica push, personalizziamo il contenuto utilizzando il valore di velocità.

![](assets/action-response8.png){width="70%" align="left"}

>[!NOTE]
>
>La chiamata viene eseguita solo una volta per profilo in un dato percorso. Messaggi multipli non attiveranno nuove chiamate.

## Sintassi delle espressioni

Di seguito è riportata la sintassi:

```json
#@action{myAction.myField} 
```

Di seguito sono riportati alcuni esempi:

```json
// action response field
@action{<action name>.<path to the field>}
@action{OpenWeatherMap.main.temp}
```

```json
// action response field
@action{<action name>.<path to the field>, defaultValue: <default value expression>}
@action{OpenWeatherMap.main.temp, defaultValue: 273.15}
@action{OpenWeatherMap.main.temp, defaultValue: @{myEvent.temperature}} 
```


