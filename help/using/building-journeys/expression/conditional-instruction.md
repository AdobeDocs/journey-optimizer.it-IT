---
solution: Journey Optimizer
product: journey optimizer
title: Istruzione condizionale (if, then, else)
description: Informazioni sull’istruzione condizionale
feature: Journeys
role: Developer
level: Experienced
keywords: avanzato, condizione, azione, percorso
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cce82f05-fc3c-4af7-85ff-8bba603861a7
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 0%

---

# Istruzione condizionale (if, then, else) {#conditional-instruction}

L’istruzione condizionale (if, then, else) è supportata nell’editor avanzato. Consente di definire espressioni più complesse. È composto dai seguenti elementi:

* **[!UICONTROL if]**: la condizione da valutare per prima.
* **[!UICONTROL then]**: l&#39;espressione da valutare nel caso in cui il risultato della valutazione della condizione sia vero.
* **[!UICONTROL else]**: l&#39;espressione da valutare se il risultato della valutazione della condizione è falso.

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

`<expression1>` deve restituire un valore **booleano**.

`<expression2>` e `<expression3>` devono avere tipi uguali o compatibili. Le firme supportate e i tipi restituiti sono:

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

L’istruzione condizionale ti consente di ottimizzare il flusso di lavoro del percorso riducendo il numero di attività relative alle condizioni. Ad esempio, all’interno della stessa attività di azione, puoi specificare due alternative per la definizione di un campo utilizzando una sola espressione di condizione.

Esempio per un’attività di azione (per un campo che prevede una stringa come risultato dell’istruzione condizionale):

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
