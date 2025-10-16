---
solution: Journey Optimizer
product: journey optimizer
title: Riferimenti campo
description: Scopri i riferimenti ai campi nelle espressioni avanzate
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: percorso, campo, espressione, evento
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
version: Journey Orchestration
source-git-commit: 7ac246c0aa6776d3ec67223c4b07536b8ed0c881
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 2%

---

# Riferimenti campo {#field-references}

Un riferimento di campo può essere allegato a un evento o a un gruppo di campi. L’unica informazione significativa è il nome del campo e il relativo percorso.

Se in un campo si utilizzano caratteri speciali, è necessario utilizzare virgolette doppie o semplici. Di seguito sono riportati i casi in cui sono necessarie virgolette:

* il campo inizia con caratteri numerici
* il campo inizia con il carattere &quot;-&quot;
* il campo contiene elementi diversi da: _a_-_z_, _A_-_Z_, _0_-_9_, _ , _-_

Ad esempio, se il campo è _3h_: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

```json
// event field
@event{<event name>.<XDM path to the field>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id}

// field group
#{<data source name>.<field group name>.<path to the field>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address}
```

Nell’espressione, ai campi evento viene fatto riferimento con &quot;@&quot; e ai campi dell’origine dati viene fatto riferimento con &quot;#&quot;.

Un colore di sintassi viene utilizzato per distinguere visivamente i campi degli eventi (verde) dai gruppi di campi (blu).

## Valori predefiniti per riferimenti campo {#default-value}

Un valore predefinito può essere associato a un nome di campo. La sintassi è la seguente:

```json
// event field
@event{<event name>.<XDM path to the field>, defaultValue: <default value expression>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue: "example@adobe.com"}
// field group
#{<data source name>.<field group name>.<path to the field>, defaultValue: <default value expression>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address, defaultValue: "example@adobe.com"}
```

>[!NOTE]
>
>Il tipo del campo e il valore predefinito devono essere uguali. `@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue : 2}`, ad esempio, non è valido perché il valore predefinito è un numero intero, mentre il valore previsto deve essere una stringa.

Esempi:

```json
// for an event 'OrderEvent' having the following payload:
{
    "orderId": "12345"
}
 
expression example:
- @event{OrderEvent.orderId}                                    -> "12345"
- @event{OrderEvent.productId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
- @event{OrderEvent.productId}                                  -> null
 
 
// for an entity 'Profile' on datasource 'ACP' having fields person/lastName, with fetched data such as:
{
    "person": {
        "lastName":"Snow"
    },
    "emails": [
        { "email":"john.snow@winterfell.westeros" },
        { "email":"snow@thewall.westeros" }
    ]
}
 
expression examples:
- #{ACP.Profile.person.lastName}                 -> "Snow"
- #{ACP.Profile.emails.at(1).email}              -> "snow@thewall.westeros"
- #{ACP.Profile.person.age, defaultValue : -1}   -> -1 // default value, age is not a field present in the payload
- #{ACP.Profile.person.age}                      -> null
```

È possibile aggiungere qualsiasi tipo di espressione come valore predefinito. L’unico vincolo è che l’espressione deve restituire il tipo di dati previsto. Quando si utilizza una funzione, è necessario incapsularla con ().

```
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.any.time, defaultValue : (now())} 
== date("2022-02-10T00:00:00Z")
```

## Riferimento a un campo all’interno di raccolte

Si fa riferimento agli elementi definiti nelle raccolte utilizzando le funzioni specifiche `all`, `first` e `last`. Per ulteriori informazioni, consulta [questa pagina](../expression/collection-management-functions.md).

Esempio:

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all()
```

## Riferimento a un campo definito in una mappa

### Funzione `entry`

Per recuperare un elemento in una mappa, utilizziamo la funzione di immissione con una determinata chiave. Ad esempio, viene utilizzato quando si definisce la chiave di un evento, in base allo spazio dei nomi selezionato. Per ulteriori informazioni, vedere [questa pagina](../../event/about-creating.md#select-the-namespace).

```json
@event{MyEvent.identityMap.entry('Email').first().id}
```

In questa espressione, si ottiene la voce per la chiave &quot;E-mail&quot; del campo &quot;IdentityMap&quot; di un evento. La voce &quot;E-mail&quot; è una raccolta, dalla quale prendiamo il &quot;id&quot; nel primo elemento utilizzando &quot;first()&quot;. Per ulteriori informazioni, vedere [questa pagina](../expression/collection-management-functions.md).

### Funzione `firstEntryKey`

Per recuperare la prima chiave di ingresso di una mappa, utilizzare la funzione `firstEntryKey`.

Questo esempio mostra come recuperare il primo indirizzo e-mail degli abbonati di un elenco specifico:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

In questo esempio, l&#39;elenco iscrizioni è denominato `daily-email`. Gli indirizzi di posta elettronica sono definiti come chiavi nella mappa `subscribers`, collegata alla mappa dell&#39;elenco iscrizioni.

### Funzione `keys`

Per recuperare in tutte le chiavi di una mappa, utilizzare la funzione `keys`.

Questo esempio mostra come recuperare, per un profilo specifico, tutti gli indirizzi e-mail associati agli abbonati di un elenco specifico:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## Valori dei parametri di un’origine dati (valori dinamici dell’origine dati)

Se selezioni un campo da un’origine dati esterna che richiede la chiamata di un parametro, a destra viene visualizzata una nuova scheda che consente di specificare questo parametro. Consulta [questa pagina](../expression/expressionadvanced.md).

Per casi d&#39;uso più complessi, se desideri includere i parametri dell&#39;origine dati nell&#39;espressione principale, puoi definirne i valori utilizzando la parola chiave _params_. Un parametro può essere qualsiasi espressione valida anche da un&#39;altra origine dati che include anche un altro parametro.

>[!NOTE]
>
>Quando definite i valori dei parametri nell&#39;espressione, la linguetta a destra scompare.

Utilizza la seguente sintassi:

```json
#{<datasource>.<field group>.fieldName, params: {<params-1-name>: <params-1-value>, <params-2-name>: <params-2-value>}}
```

* **`<params-1-name>`**: nome esatto del primo parametro dell&#39;origine dati.
* **`<params-1-value>`**: valore del primo parametro. Può essere qualsiasi espressione valida.

Esempio:

```json
#{Weather.main.temperature, params: {localisation: @event{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @event{Profile.address.city}}}}}
```
