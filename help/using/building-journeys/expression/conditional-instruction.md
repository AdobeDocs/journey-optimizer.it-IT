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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 576
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

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrata l&#39;istruzione condizionale `if / then / else` disponibile nell&#39;editor di espressioni avanzate di Percorso, incluse le regole di sintassi, le combinazioni di tipi supportate e un esempio pratico di utilizzo.

**Intenti:**

* Scrivere un&#39;espressione condizionale utilizzando `if`, `then` e `else` per restituire valori diversi in base a una condizione booleana
* Riduci il numero di attività condizione in un percorso incorporando una logica condizionale in linea in una singola attività azione
* Determinare quali combinazioni di tipi di dati sono valide per i rami `then` e `else`
* Applicare l’istruzione condizionale per indirizzare i token di notifica push ad APNS o FCM in base al modello del dispositivo

**Glossario:**

* **Istruzione condizionale**: costrutto di espressione `if / then / else` nell&#39;editor avanzato che valuta un valore booleano e restituisce una delle due espressioni *(specifiche per prodotto)*
* **Editor espressioni avanzate**: interfaccia di Journey Optimizer per la scrittura di espressioni complesse utilizzate nelle condizioni, nelle attività di attesa e nella mappatura dei parametri delle azioni *(specifico per prodotto)*

**Guardrail:**

* Sono necessarie parentesi per tutte le espressioni nelle clausole `if`, `then` e `else`
* La clausola `if` (`<expression1>`) deve restituire un tipo booleano
* Le espressioni `then` e `else` (`<expression2>` e `<expression3>`) devono avere lo stesso tipo o tipi compatibili (ad esempio `decimal` e `integer` sono compatibili, `string` e `integer` non lo sono)
* Non tutte le combinazioni di tipi sono supportate. Solo le coppie elencate nella tabella delle firme supportate sono valide

**Terminologia:**

* Nome canonico: Istruzione condizionale — Acronimo: none — varianti: if/then/else, condizione ternaria
* Sinonimi: &quot;istruzione condizionale&quot; = &quot;condizione in linea&quot; = &quot;espressione if-then-else&quot;
* Da non confondere: istruzione condizionale (espressione in linea) ≠ attività Condizione (un nodo di area di lavoro del percorso)

**Domande frequenti:**

* **Q: la clausola `if` deve essere racchiusa tra parentesi?** — Sì, sono necessarie parentesi per tutte le espressioni, inclusa la condizione nella clausola `if`.
* **Q: posso utilizzare `if / then / else` per restituire un numero da un ramo e una stringa da un altro?** — No; `<expression2>` e `<expression3>` devono avere tipi uguali o compatibili.
* **D: in che modo l&#39;istruzione condizionale riduce la complessità del percorso?** — Consente di specificare due valori di campo alternativi all’interno di una singola attività di azione utilizzando una sola espressione, evitando un nodo separato dell’attività Condizione sull’area di lavoro.
* **D: che tipo restituisce l&#39;istruzione condizionale se entrambi i rami sono stringhe?** — Restituisce un `string`.
* **Q: è possibile utilizzare `if / then / else` per selezionare un canale di notifica push?** — Sì; ad esempio, la valutazione del modello di dispositivo per restituire `'apns'` per dispositivi Apple o `'fcm'` per altri.

+++
