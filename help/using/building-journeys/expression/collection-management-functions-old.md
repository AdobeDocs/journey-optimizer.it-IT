---
solution: Journey Optimizer
product: journey optimizer
title: Funzioni di gestione delle raccolte
description: Informazioni sui tipi di dati nelle funzioni di gestione delle raccolte
feature: Journeys
hide: true
role: Developer
level: Experienced
keywords: query, raccolte, funzioni, payload, percorso
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1222
ht-degree: 1%

---

# Funzioni di gestione delle raccolte

Il linguaggio delle espressioni introduce anche un set di funzioni per le raccolte di query.

Queste funzioni sono descritte di seguito. Nell’esempio seguente, utilizziamo il payload dell’evento contenente una raccolta:

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

**Funzione &quot;all(`<condition>`)&quot;**

La funzione **[!UICONTROL all]** abilita la definizione di un filtro per una determinata raccolta utilizzando un&#39;espressione booleana.

```json
<listExpression>.all(<condition>)
```

Ad esempio, tra tutti gli utenti dell’app, puoi ottenere quelli che utilizzano IOS 13 (espressione booleana &quot;app utilizzata == IOS 13&quot;). Il risultato di questa funzione è l’elenco filtrato contenente gli elementi che corrispondono all’espressione booleana (ad esempio: utente app 1, utente app 34, utente app 432).

In un&#39;attività Condizione Data Source è possibile verificare se il risultato della funzione **[!UICONTROL all]** è nullo o meno. È inoltre possibile combinare questa funzione **[!UICONTROL all]** con altre funzioni quali **[!UICONTROL count]**. Per ulteriori informazioni, vedere [Attività condizione Data Source](../conditions.md#data_source_condition).


## Esempi

>[!CAUTION]
>
>L’utilizzo di eventi di esperienza nelle espressioni/condizioni di percorso è supportato, ma non consigliato. Se il caso d&#39;uso richiede l&#39;utilizzo di eventi esperienza, prendere in considerazione metodi alternativi come [attributi calcolati](../../audience/computed-attributes.md) o creare un segmento utilizzando gli eventi e incorporando tale segmento in [`inAudience` espressioni](../../building-journeys/functions/functioninaudience.md).

**Esempio 1:**

Vogliamo verificare se un utente ha installato una versione specifica di un’applicazione. Per questo otteniamo tutti i token di notifica push associati alle applicazioni mobili per le quali la versione è 1.0. Quindi eseguiamo una condizione con la funzione **[!UICONTROL count]** per verificare che l&#39;elenco di token restituito contenga almeno un elemento.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

Il risultato è vero.

**Esempio 2:**

In questo caso, usiamo la funzione **[!UICONTROL count]** per verificare se la raccolta contiene token di notifica push.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```

Il risultato sarà vero.

<!--
Alternatively, you can check if there is no token in the collection:

   ```json
   count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) == 0
   ```

The result will be false.

Here we use the count function in a condition to count the number of push notification tokens in the event.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token})`

The result is true.

Note that when the condition in the **all()** function is empty, the filter will return all the elements in the list. Hence, the expression above is equivalent to:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.application.name})`

In both cases, the result of the expression is **3**.

A query of experience events recorded on the Adobe Experience Platform may or may not include the current event that triggered the current Journey. This will depend on the relative processing time with which [!DNL Journey Orchestration] sees an event and started evaluating conditions, versus the time it takes for that event to be ingested into the Adobe Experience Platform. For example, when using the .all() syntax to query experience events from the Adobe Experience Platform, we recommend enforcing the exclusion of the current event (by requiring an
earlier timestamp) in order to only consider prior events.
-->

>[!NOTE]
>
>Quando la condizione di filtro nella funzione **all()** è vuota, il filtro restituirà tutti gli elementi dell&#39;elenco. **Tuttavia, per contare il numero di elementi di una raccolta, la funzione all non è obbligatoria.**


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

Il risultato dell&#39;espressione è **3**.

**Esempio 3:**

Qui controlliamo se un individuo non ha ricevuto alcuna comunicazione nelle ultime 24 ore. La raccolta di eventi di esperienza recuperata dall’origine dati di Experience Platform viene filtrata utilizzando due espressioni basate su due elementi della raccolta. In particolare, la marca temporale dell&#39;evento viene confrontata con la data/ora restituita dalla funzione **[!UICONTROL nowWithDelta]**.

```json
count(#{ExperiencePlatform.MarltonExperience.experienceevent.all(
   currentDataPackField.directMarketing.sends.value > 0 and
   currentDataPackField.timestamp > nowWithDelta(-1, "days")).timestamp}) == 0
```

Il risultato sarà vero se non c’è un evento esperienza che corrisponde alle due condizioni.

**Esempio 4:**

Qui vogliamo verificare se un singolo utente ha avviato un’applicazione almeno una volta negli ultimi 7 giorni, ad esempio per attivare una notifica push che invita l’utente ad avviare un’esercitazione.

```json
count(
 #{ExperiencePlatform.AnalyticsData.experienceevent.all(
 nowWithDelta(-7,"days") <= currentDataPackField.timestamp
 and currentDataPackField.application.firstLaunches.value > 0
)._id}) > 0
```

<!--
**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`
-->

>[!NOTE]
>
>**[!UICONTROL currentEventField]** è disponibile solo quando si manipolano le raccolte eventi, **[!UICONTROL currentDataPackField]** quando si manipolano le raccolte origini dati e **[!UICONTROL currentActionField]** quando si manipolano le raccolte di risposte alle azioni personalizzate.
>
>Durante l&#39;elaborazione delle raccolte con **[!UICONTROL all]**, **[!UICONTROL first]** e **[!UICONTROL last]**, viene eseguito un ciclo su ogni elemento della raccolta uno alla volta. **[!UICONTROL currentEventField]**, **currentDataPackField** e **[!UICONTROL currentActionField]** corrispondono all&#39;elemento di cui viene eseguito il ciclo.

**Funzioni &quot;first(`<condition>`)&quot; e &quot;last(`<condition>`)&quot;**

Le funzioni **[!UICONTROL first]** e **[!UICONTROL last]** abilitano inoltre la definizione di un filtro nella raccolta restituendo il primo/ultimo elemento dell&#39;elenco che soddisfa il filtro.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

**Esempio 1:**

Questa espressione restituisce il primo token di notifica push associato alle applicazioni mobili la cui versione è 1.0.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token
```

Il risultato è &quot;token_1&quot;.

**Esempio 2:**

Questa espressione restituisce l’ultimo token di notifica push associato alle applicazioni mobili la cui versione è 1.0.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

Il risultato è &quot;token_2&quot;.

>[!NOTE]
>
>Gli eventi esperienza vengono recuperati da Adobe Experience Platform come raccolta in ordine cronologico inverso, quindi:
>
>* La funzione **[!UICONTROL first]** restituirà l&#39;evento più recente
>* La funzione **[!UICONTROL last]** restituirà quella meno recente.

**Esempio 3:**

Verifichiamo se il primo evento Adobe Analytics (più recente) con un valore diverso da zero per l’ID DMA ha un valore uguale a 602.

```json
#{ExperiencePlatform.AnalyticsProd_EvarsProps.experienceevent.first(
currentDataPackField.placeContext.geo.dmaID > 0).placeContext.geo.dmaID} == 602
```

**Funzione &quot;at(`<index>`)&quot;**

La funzione **[!UICONTROL at]** consente di fare riferimento a un elemento specifico di una raccolta in base a un indice.
L&#39;indice 0 è il primo indice della raccolta.

_`<listExpression>`.at(`<index>`)_

**Esempio:**

Questa espressione restituisce il secondo token di notifica push dell’elenco.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Il risultato è &quot;token_2&quot;.

**Altri esempi**

Questa espressione restituisce i nomi dei prodotti in base al valore SKU. L’elenco di questi prodotti è incluso nell’elenco degli eventi, con la condizione che è l’ID evento.

```json
#{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.all(currentDataPackField._aepgdcdevenablement2.purchase_event.receipt_nbr == "10-337-4016"). 
_aepgdcdevenablement2.purchase_event.productListItems.all(currentDataPackField.SKU == "AB17 1234 1775 19DT B4DR 8HDK 762").name}
```

Questa espressione recupera il nome dell’ultimo prodotto nell’elenco dei prodotti di un evento commerciale in cui il tipo di evento è &quot;productListAdds&quot; e il prezzo totale è maggiore o uguale a 150.

```json
 #{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.last(
currentDataPackField.eventType == "commerce.productListAdds").productListItems.last(currentDataPackField.priceTotal >= 150).name}
```

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina sono illustrate le funzioni di gestione della raccolta `all()`, `first()`, `last()` e `at()` disponibili nel linguaggio delle espressioni di Percorso, con esempi di utilizzo dei payload dei token di notifica push e dei dati dell&#39;evento esperienza.

**Intenti:**

* Filtrare una raccolta utilizzando una condizione booleana con `all(<condition>)` per recuperare gli elementi corrispondenti
* Contare gli elementi in una raccolta utilizzando la funzione `count()` combinata con `all()`
* Recuperare il primo o l&#39;ultimo elemento di una raccolta filtrata utilizzando `first()` o `last()`
* Accedere a un elemento specifico di una raccolta mediante l&#39;indice utilizzando `at(<index>)`
* Combinare le query di raccolta nidificate per cercare i nomi dei prodotti in base allo SKU o al tipo di evento e alla soglia di prezzo

**Glossario:**

* **all(condition)**: funzione di raccolta che filtra un elenco e restituisce elementi che corrispondono all&#39;espressione booleana specificata *(specifica per prodotto)*
* **first(condition)**: funzione di raccolta che restituisce il primo elemento (più recente, per eventi di esperienza) che corrisponde alla condizione *(specifico per prodotto)*
* **last(condition)**: funzione di raccolta che restituisce l&#39;ultimo elemento (meno recente, per eventi di esperienza) che corrisponde alla condizione *(specifico per prodotto)*
* **at(index)**: Funzione di raccolta che restituisce l&#39;elemento in corrispondenza di uno specifico indice a base zero *(specifico per prodotto)*
* **currentEventField**: variabile di loop disponibile per l&#39;iterazione delle raccolte eventi in `all()`, `first()` o `last()` *(specifico per prodotto)*
* **currentDataPackField**: variabile di loop disponibile quando si esegue l&#39;iterazione sulle raccolte di origini dati *(specifico per prodotto)*
* **currentActionField**: variabile di loop disponibile quando si esegue l&#39;iterazione sulle raccolte di risposte di azioni personalizzate *(specifico per prodotto)*

**Guardrail:**

* L’utilizzo di eventi di esperienza nelle espressioni/condizioni di percorso è supportato ma non consigliato; considera gli attributi calcolati o i segmenti di pubblico come alternative
* `currentEventField` è disponibile solo per le raccolte eventi; `currentDataPackField` per le raccolte di origini dati; `currentActionField` per le raccolte di risposte di azioni personalizzate
* La funzione `all` non è necessaria per contare gli elementi di una raccolta. `count()` può essere applicato direttamente al campo della raccolta
* Gli eventi esperienza vengono recuperati in ordine cronologico inverso: `first()` restituisce l&#39;evento più recente, `last()` restituisce il più vecchio

**Terminologia:**

* Nome canonico: Funzioni di gestione delle raccolte — Acronimo: none — varianti: funzioni di raccolta, funzioni di raccolta query
* Sinonimi: &quot;all()&quot; = &quot;funzione filtro&quot;; &quot;first()&quot; = &quot;funzione elemento più recente&quot; (per eventi esperienza)
* Non confondere: `first()` (evento esperienza più recente) ≠ primo elemento in base all&#39;ordine di inserimento

**Domande frequenti:**

* **D: cosa restituisce `all()` quando la condizione è vuota?** — Restituisce tutti gli elementi dell’elenco, equivalenti a nessun filtro.
* **D: come si conta il numero di token di notifica push in una raccolta?** — Utilizza `count()` direttamente nel percorso del campo token senza richiedere `all()`, ad esempio `count(@event{...pushNotificationTokens.token})`.
* **D: come è possibile ottenere il secondo elemento di una raccolta?** — Utilizzare `at(1)` poiché l&#39;indice 0 è il primo elemento.
* **Q: perché `first()` restituisce l&#39;evento esperienza più recente?** — Gli eventi di esperienza vengono recuperati da Adobe Experience Platform in ordine cronologico inverso, quindi `first()` seleziona l&#39;elemento principale (più recente).
* **D: come posso verificare se un utente non ha ricevuto alcuna comunicazione nelle ultime 24 ore?** — Filtra la raccolta eventi esperienza con `nowWithDelta(-1, "days")` come limite inferiore di marca temporale e utilizza `count(...) == 0`.

+++
