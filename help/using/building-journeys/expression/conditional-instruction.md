---
solution: Journey Optimizer
product: journey optimizer
title: Istruzione condizionale (if, then, else)
description: Scopri le istruzioni condizionali
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Istruzione condizionale (if, then, else) {#conditional-instruction}

L’istruzione condizionale (se, then, else) è supportata nell’editor avanzato. Consente di definire espressioni più complesse. È composto dai seguenti elementi:

* **[!UICONTROL if]**: la condizione da valutare per prima.
* **[!UICONTROL then]**: l&#39;espressione da valutare nel caso in cui il risultato della valutazione della condizione sia vero.
* **[!UICONTROL else]**: l’espressione da valutare nel caso in cui il risultato della valutazione della condizione sia falso.

>[!NOTE]
>
>Sono necessarie parentesi intorno a tutte le espressioni.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` deve restituire un **booleano**.

`<expression2>` e `<expression3>` devono avere lo stesso tipo o tipi compatibili. Le firme supportate e i tipi restituiti sono:

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**Utilizzo**

L’istruzione condizionale ti consente di ottimizzare il flusso di lavoro del percorso riducendo il numero di attività di condizione. Ad esempio, all’interno della stessa attività di azione, puoi specificare due alternative per una definizione di campo utilizzando una sola espressione di condizione.

Esempio per un’attività di azione (per un campo che richiede una stringa come risultato dell’istruzione condizionale):

```json
if (startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
