---
product: journey optimizer
title: toString
description: Scopri la funzione toString
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toString, funzione, espressione, percorso
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# toString {#toString}

Converte un valore di argomento in un valore stringa, a seconda del tipo. Per ulteriori informazioni sui tipi di dati, consultare [questa pagina](../expression/data-types.md).

## Categoria

Conversione

## Sintassi della funzione

`toString(<parameter>)`

## Elemento “parameters”

| Parametro | Descrizione |
|--- |--- |
| dateTime | converte la data nel formato data UTC |
| dateTimeOnly | converte la data nel formato data UTC |
| durata | convertire nel numero di millisecondi corrispondente come stringa |
| intero | converte in rappresentazione stringa del valore (1 diventa &quot;1&quot;) |
| decimale | converte in rappresentazione stringa del valore (1,5 diventa &quot;1,5&quot;) |
| booleano | converti il valore booleano come &#39;true&#39; se true, &#39;false&#39; se false |

## Firme e tipo restituito

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Restituisce una stringa.

## Esempio

`toString(4)`

Restituisce &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Restituisce la rappresentazione in forma di stringa del campo dataOnly specificato (campo Data XDM), ad esempio &quot;2023-08-18&quot;.

`toString(toDuration(1520))`

Restituisce &quot;PT1.52S&quot;.
