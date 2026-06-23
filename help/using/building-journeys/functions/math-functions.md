---
product: journey optimizer
title: Funzioni matematiche
description: Scopri le funzioni matematiche
feature: Journeys
role: Developer
level: Experienced
keywords: matematica, funzioni, espressione, percorso, calcolo, numero
version: Journey Orchestration
exl-id: da710b22-3112-41fe-8b91-2b6563b79f27
TQID: https://experienceleague.adobe.com/POIbPCZrqtqGjHqn3ehGonxwv9KhKWlgg2igdN8Y4yw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 2%

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

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina sono documentate le due funzioni matematiche disponibili nelle espressioni di percorso di AJO: `random` per la generazione di un decimale casuale compreso tra 0 e 1 e `round` per l&#39;arrotondamento di un decimale o di un numero intero al numero intero più vicino.

**Intenti:**
* Genera un valore decimale casuale compreso tra 0 e 1 per la logica di campionamento o randomizzazione utilizzando `random`
* Arrotondare un numero decimale al numero intero più vicino utilizzando `round`
* Applica l&#39;arrotondamento nella logica di business quando i numeri interi sono richiesti dai calcoli decimali

**Glossario:**
* **random**: funzione che restituisce un valore decimale pseudo-casuale compreso tra 0 (inclusi) e 1 (esclusivi) *(specifici del prodotto)*
* **round**: funzione che restituisce l&#39;intero più vicino all&#39;input, con valori interi che vengono arrotondati all&#39;infinito positivo

**Guardrail:**
* `random()` non accetta parametri
* `round` accetta l&#39;input decimale o intero e restituisce sempre un numero intero
* I legami in `round` vengono risolti arrotondando all&#39;infinito positivo (ad esempio, 3,5 arrotondamenti a 4, -3,5 arrotondamenti a -3)

**Terminologia:**
* Nome canonico: funzioni matematiche — Acronimo: none — varianti: funzioni matematiche, funzioni numeriche
* Sinonimi: &quot;round&quot; = &quot;round al numero intero più vicino&quot;
* Non confondere: &quot;arrotonda&quot; (arrotonda al numero intero più vicino) ≠ funzioni di conversione come `toInteger` (tronca la parte decimale senza arrotondare)

**Domande frequenti:**
* **Q: Che cosa restituisce `random()`?** — Restituisce un numero decimale casuale compreso tra 0 e 1.
* **Q: in che modo `round` gestisce i numeri negativi?** — Viene arrotondato all&#39;infinito positivo, quindi `round(-3.14)` restituisce -3 e `round(-3.54)` restituisce anche -3 (l&#39;intero più vicino all&#39;infinito positivo).
* **Q: Qual è la differenza tra `round` e `toInteger`?** — `round` arrotonda al numero intero più vicino (3,7 diventa 4), mentre `toInteger` tronca la parte decimale senza arrotondare (3,7 diventa 3).
* **Q: `random` accetta parametri?** — No, `random()` non richiede parametri e restituisce sempre un decimale compreso tra 0 e 1.

+++
