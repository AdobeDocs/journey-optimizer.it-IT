---
solution: Journey Optimizer
product: journey optimizer
title: Funzioni di gestione delle raccolte
description: Informazioni sui tipi di dati nelle funzioni di gestione delle raccolte
feature: Journeys
role: Developer
level: Experienced
keywords: query, raccolte, funzioni, payload, percorso
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 3%

---

# Funzioni di gestione delle raccolte {#collection-management-functions}


## Informazioni sulle funzioni di raccolta query

Il linguaggio delle espressioni introduce anche un set di funzioni per le raccolte di query. Queste funzioni sono descritte di seguito.

Nell’esempio seguente, utilizziamo il payload dell’evento contenente una raccolta:

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

## La funzione all(`<condition>`)

La funzione **[!UICONTROL all]** abilita la definizione di un filtro per una determinata raccolta utilizzando un&#39;espressione booleana.

```json
<listExpression>.all(<condition>)
```

Ad esempio, tra tutti gli utenti dell’app, puoi ottenere quelli che utilizzano IOS 13 (espressione booleana &quot;app utilizzata == IOS 13&quot;). Il risultato di questa funzione è l’elenco filtrato contenente gli elementi che corrispondono all’espressione booleana (ad esempio: utente app 1, utente app 34, utente app 432).

In un&#39;attività Condizione Data Source è possibile verificare se il risultato della funzione **[!UICONTROL all]** è nullo o meno. È inoltre possibile combinare questa funzione **[!UICONTROL all]** con altre funzioni quali **[!UICONTROL count]**. Per ulteriori informazioni, vedere [Attività condizione Data Source](../condition-activity.md#data_source_condition).


>[!CAUTION]
>
>L’utilizzo di eventi di esperienza nelle espressioni/condizioni di percorso non è supportato. Se il caso d’uso richiede l’utilizzo di eventi esperienza, considera metodi alternativi. [Ulteriori informazioni](../exp-event-lookup.md)

### Esempio 1

Vogliamo verificare se un utente ha installato una versione specifica di un’applicazione. Per questo otteniamo tutti i token di notifica push associati alle applicazioni mobili per le quali la versione è 1.0. Quindi eseguiamo una condizione con la funzione **[!UICONTROL count]** per verificare che l&#39;elenco di token restituito contenga almeno un elemento.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

Il risultato è vero.

### Esempio 2

In questo caso, usiamo la funzione **[!UICONTROL count]** per verificare se la raccolta contiene token di notifica push.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


Il risultato è vero.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

Il risultato dell&#39;espressione è **3**.


>[!NOTE]
>
>* Quando la condizione di filtro nella funzione **all()** è vuota, il filtro restituirà tutti gli elementi dell&#39;elenco. **Tuttavia, per contare il numero di elementi di una raccolta, la funzione all non è obbligatoria.**
>
>* `currentEventField` è disponibile solo quando si manipolano le raccolte eventi, `currentDataPackField` quando si manipolano le raccolte origini dati e `currentActionField` quando si manipolano le raccolte di risposte di azioni personalizzate.
>
>  Durante l&#39;elaborazione delle raccolte con `all`, `first` e `last`, viene eseguito un ciclo su ogni elemento della raccolta uno alla volta. `currentEventField`, `currentDataPackField` e `currentActionField` corrispondono all&#39;elemento di cui viene eseguito il ciclo.


## La prima(`<condition>`) e l&#39;ultima(`<condition>`) funzioni

Le funzioni **[!UICONTROL first]** e **[!UICONTROL last]** abilitano inoltre la definizione di un filtro nella raccolta restituendo il primo/ultimo elemento dell&#39;elenco che soddisfa il filtro.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### Esempio 1

Questa espressione restituisce il primo token di notifica push associato alle applicazioni mobili la cui versione è 1.0.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

Risultato: `token_1`.

### Esempio 2

Questa espressione restituisce l’ultimo token di notifica push associato alle applicazioni mobili la cui versione è 1.0.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

Risultato: `token_2`.

## Funzione at(`<index>`)

La funzione **[!UICONTROL at]** consente di fare riferimento a un elemento specifico di una raccolta in base a un indice.
L&#39;indice 0 è il primo indice della raccolta.

_`<listExpression>`.at(`<index>`)_

### Esempio

Questa espressione restituisce il secondo token di notifica push dell’elenco.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Risultato: `token_2`.