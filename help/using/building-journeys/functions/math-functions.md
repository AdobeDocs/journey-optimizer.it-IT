---
product: journey optimizer
title: Funzioni matematiche
description: Scopri le funzioni matematiche
feature: Journeys
role: Developer
level: Experienced
keywords: matematica, funzioni, espressione, percorso, calcolo, numero
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 7%

---

# Funzioni matematiche {#math-functions}

Le funzioni matematiche forniscono operazioni matematiche essenziali per i calcoli numerici nelle espressioni di percorso. Queste funzioni consentono di eseguire calcoli numerici precisi e trasformazioni sui dati.

Utilizza le funzioni matematiche quando devi:

* Genera valori casuali per test, campionamento o randomizzazione ([random](#random))
* Arrotonda i numeri decimali al numero intero più vicino per una presentazione dei dati più pulita ([round](#round))
* Eseguire calcoli matematici su campi numerici
* Trasformare i valori numerici per la logica di business e il processo decisionale

Le funzioni matematiche gestiscono sia i tipi decimali che quelli interi, gestendo automaticamente le conversioni dei tipi per garantire risultati accurati nelle espressioni di percorso.

## random {#random}

Genera un numero casuale compreso tra 0 e 1.

+++Sintassi

`random()`

+++

+++Firma e tipo restituito

`random()`

Restituisce un valore decimale.

+++

## round {#round}

Restituisce il valore intero più vicino all&#39;argomento con legami arrotondati all&#39;infinito positivo.

+++Sintassi

`round(<parameters>)`

+++

+++Parametri

* decimale
* intero

+++

+++Firme e tipo restituito

`round(<decimal>)`

`round(<integer>)`

Restituisce un numero intero.

+++

+++Esempi

`round(3.14)`

Restituisce 3.

`round(3.54)`

Restituisce 4.

`round(-3.14)`

Restituisce -3.

`round(3)`

Restituisce 3.

+++

