---
product: adobe campaign
title: toString
description: Scopri la funzione toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 5ae67db97ef7a2562e5c9179658400a4dceff72d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# toString {#toString}

Converte un valore di argomento in un valore di stringa, a seconda del tipo. Per ulteriori informazioni sui tipi di dati, consulta [questa pagina](../expression/data-types.md).

## Categoria

Conversione

## Sintassi della funzione

`toString(<parameter>)`

## Parametri

| Parametro | Descrizione |
|--- |--- |
| dateTime | converte la data in formato data UTC |
| dateTimeOnly | converte la data in formato data UTC |
| durata | convertire nel numero corrispondente di millisecondi come stringa |
| integer | converte in rappresentazione stringa del valore (1 diventa &quot;1&quot;) |
| decimale | converte in rappresentazione stringa del valore (1.5 diventa &quot;1.5&quot;) |
| booleano | converte il valore booleano come &#39;true&#39; se true, &#39;false&#39; se false |

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
