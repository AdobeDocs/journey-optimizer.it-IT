---
solution: Journey Optimizer
product: journey optimizer
title: Riferimenti campo
description: Scopri i riferimenti ai campi nelle espressioni avanzate
feature: Journeys
role: Developer
level: Experienced
keywords: percorso, campo, espressione, evento
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/G8ooc1R2PwL06V89EBs-jH8Lf43F6q5xj3I4Wl6hDHk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 1%

---

# Riferimenti campo {#field-references}

Un riferimento di campo può essere allegato a un evento o a un gruppo di campi. L’unica informazione significativa è il nome del campo e il relativo percorso.

Se in un campo si utilizzano caratteri speciali, è necessario utilizzare virgolette doppie o semplici. Di seguito sono riportati i casi in cui sono necessarie virgolette:

* il campo inizia con caratteri numerici
* il campo inizia con il carattere &quot;-&quot;
* il campo contiene elementi diversi da: _a_-_z_, _A_-_Z_, _0_-_9_, _,_-_

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

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come fare riferimento ai campi evento e ai gruppi di campi dell&#39;origine dati nelle espressioni di percorso, inclusi la sintassi dei valori predefiniti, le funzioni di accesso alle mappe (`entry`, `firstEntryKey`, `keys`) e il parametro dell&#39;origine dati in linea che passa con la parola chiave `params`.

**Intenti:**

* Fare riferimento a un campo evento in un&#39;espressione utilizzando la sintassi `@event{eventName.fieldPath}`
* Fare riferimento a un gruppo di campi di origine dati utilizzando la sintassi `#{dataSourceName.fieldGroupName.fieldPath}`
* Assegnare un valore predefinito di fallback a un riferimento di campo in modo che le espressioni non restituiscano null
* Recuperare una voce specifica da una mappa di identità o di abbonamento utilizzando la funzione `entry()`
* Recuperare tutte le chiavi da un campo mappa utilizzando la funzione `keys()`
* Trasmettere i valori dei parametri a un&#39;origine dati esterna in linea utilizzando la parola chiave `params`

**Glossario:**

* **Riferimento campo**: sintassi di espressione che punta a un campo denominato all&#39;interno di un payload evento o di un gruppo di campi origine dati *(specifico per prodotto)*
* **defaultValue**: espressione di fallback facoltativa aggiunta a un riferimento a un campo restituito quando il campo è assente o nullo *(specifico per prodotto)*
* **entry(key)**: funzione di mapping che recupera la voce di raccolta associata alla chiave specificata *(specifica del prodotto)*
* **firstEntryKey()**: funzione mappa che restituisce la prima chiave di un campo mappa *(specifico per prodotto)*
* **keys()**: funzione di mapping che restituisce tutte le chiavi di un campo di mapping *(specifico per prodotto)*
* **parola chiave params**: sintassi in linea per specificare i valori dei parametri per i campi dell&#39;origine dati esterna all&#39;interno dell&#39;espressione principale *(specifico per prodotto)*

**Guardrail:**

* I nomi dei campi contenenti caratteri speciali (a partire da una cifra, contenente `-` o caratteri esterni a `a-z A-Z 0-9 _`) devono essere racchiusi tra virgolette singole o doppie
* L’espressione del valore predefinito deve restituire lo stesso tipo di dati del campo; i tipi non corrispondenti non sono validi
* Quando si utilizza la parola chiave `params` per definire i valori dei parametri in linea, la scheda separata dei parametri a destra dell&#39;editor scompare
* Le funzioni utilizzate come valori predefiniti devono essere racchiuse tra parentesi

**Terminologia:**

* Nome canonico: riferimenti campo — Acronimo: none — varianti: percorso campo, espressione campo
* Sinonimi: `@event{...}` = &quot;riferimento campo evento&quot;; `#{...}` = &quot;riferimento campo origine dati&quot;
* Non confondere: campi evento (prefisso `@`) ≠ campi origine dati (prefisso `#`)

**Domande frequenti:**

* **D: come si fa riferimento a un campo il cui nome inizia con un numero?** — Racchiudere il nome del campo tra virgolette singole o doppie, ad esempio `#{OpenWeather.weatherData.rain.'3h'}`.
* **D: cosa succede quando manca un campo a cui si fa riferimento nel payload dell&#39;evento e non viene impostato alcun valore predefinito?** — L&#39;espressione restituisce `null`.
* **D: come si imposta un valore predefinito dinamico utilizzando una funzione?** — Racchiudi la chiamata della funzione tra parentesi, ad esempio `defaultValue: (now())`.
* **D: come è possibile recuperare l&#39;indirizzo di posta elettronica memorizzato come prima chiave in una mappa del sottoscrittore?** — Utilizzare la funzione `firstEntryKey()` nel campo mappa sottoscrittori.
* **D: come posso passare un parametro a un&#39;origine dati esterna senza utilizzare la scheda a destra?** — Utilizza la parola chiave `params` in linea: `#{DataSource.group.field, params: {paramName: value}}`.

+++
