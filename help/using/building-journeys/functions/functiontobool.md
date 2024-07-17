---
product: journey optimizer
title: toBool
description: Scopri la funzione toBool
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: tobool, function, expression, percorsi
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---

# toBool {#toBool}

Converte un valore di argomento in un valore booleano, a seconda del tipo.

* Da stringa: prova a convertire il valore stringa come booleano; da &quot;true&quot; se il valore stringa è &quot;true&quot;; in caso contrario false
* Dal valore numerico: true se il valore numerico non è uguale a 0, false in caso contrario

## Categoria

Conversione

## Sintassi della funzione

`toBool(<parameter>)`

## Elemento “parameters”

* decimale
* booleano
* stringa
* intero

## Firme e tipi restituiti

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Restituisce un valore booleano.

## Esempi

`toBool("true")`

`toBool(1)`

Restituisce true.

`toBool("this is not a boolean")`

Restituisce false.
