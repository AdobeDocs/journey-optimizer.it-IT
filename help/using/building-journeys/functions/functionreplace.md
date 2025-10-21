---
product: journey optimizer
title: replace
description: Scopri la funzione Sostituisci
feature: Journeys
role: Developer
level: Experienced
keywords: replace, function, expression, percorsi
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 11%

---

# replace {#replace}

Sostituisce la prima occorrenza corrispondente alla stringa di destinazione con la stringa di sostituzione nella stringa di base.

La sostituzione procede dall&#39;inizio della stringa alla fine, ad esempio, sostituendo &quot;aa&quot; con &quot;b&quot; nella stringa &quot;aaa&quot; si otterrà &quot;ba&quot; invece di &quot;ab&quot;.

## Categoria

Stringa

## Sintassi della funzione

`replace(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|--------------|
| base | stringa |
| destinazione | stringa (RegExp) |
| sostituzione | stringa |

## Firma e tipo restituito

`replace(<base>,<target>,<replacement>)`

Restituisce una stringa.

## Esempio 1

`replace("Hello World", "l", "x")`

Restituisce &quot;Hexlo World&quot;.

## Esempio 2 {#example_2}

Poiché il parametro di destinazione è un RegExp, a seconda della stringa che si desidera sostituire, potrebbe essere necessario eseguire l&#39;escape di alcuni caratteri. Ecco un esempio:

* stringa da valutare: `|OFFER_A|OFFER_B`
* fornito da un attributo di profilo `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Stringa da sostituire: `|OFFER_A`
* Stringa sostituita da: `''`
* Aggiungere `\\` prima del carattere `|`.

L’espressione è:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

La stringa restituita è: `|OFFER_B`

Puoi anche creare la stringa da sostituire da un dato attributo:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
