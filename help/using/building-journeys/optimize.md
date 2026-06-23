---
solution: Journey Optimizer
product: journey optimizer
title: Attività Ottimizza
description: Scopri l’attività Ottimizza
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attività, condizione, area di lavoro, percorso, ottimizzazione
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/hbDoGEHdCBcOe-e9h06kGY2Rvb129cIzto6jJAuGkX4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1094
ht-degree: 7%

---

# Introduzione all’attività Ottimizza {#journey-path-optimization}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare l&#39;attività Ottimizza per creare più percorsi di percorso in base a sperimentazione, targeting e condizioni, sostituendo l&#39;attività Condizione precedente.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Attività Ottimizza"
>abstract="L’attività **Ottimizza** consente di definire il modo in cui i singoli utenti avanzano nel percorso creando più percorsi in base a criteri specifici, inclusi sperimentazione, targeting e condizioni specifiche. Tieni presente che l’attività **Ottimizza** è il nuovo strumento per la creazione di percorsi condizionali nei percorsi. Sostituisce la precedente attività **Condizione**."

>[!IMPORTANT]
>
>L&#39;attività **Ottimizza** è il nuovo veicolo per la creazione di percorsi condizionali in percorsi. Sostituisce l’attività **Condizione** precedente, che è stata rimossa dall’interfaccia utente. Tutta la logica condizionale viene mantenuta e ora viene gestita tramite le [condizioni](conditions.md) dell&#39;attività **Ottimizza**.
>
>Se esistono percorsi che hanno utilizzato **[!UICONTROL Attività condizionali]**, puoi continuare a utilizzarli come prima. Vengono ora visualizzate con una nuova icona come attività **[!UICONTROL Ottimizza]** utilizzando il metodo **[!UICONTROL Condizione]**, ma il comportamento rimane invariato. Tutte le etichette personalizzate impostate sul nodo vengono mantenute.

L&#39;attività **Ottimizza** consente di definire il modo in cui i singoli utenti avanzano nel percorso creando più **percorsi** in base a criteri specifici, tra cui sperimentazione, targeting e condizioni specifiche, garantendo il massimo coinvolgimento e successo nella creazione di percorsi altamente personalizzati ed efficaci.

![Pulsante Ottimizza nella tavolozza attività percorso](assets/journey-optimize.png)

## Che cos&#39;è un percorso di percorso? {#journey-path}

Un percorso **percorso** può essere costituito da uno dei seguenti elementi: sequenza di comunicazioni, tempo che intercorre tra di esse, numero di comunicazioni o una combinazione di queste tre variabili.

Ad esempio, un percorso potrebbe contenere un messaggio e-mail, un altro potrebbe contenere due messaggi SMS e un terzo potrebbe contenere un messaggio e-mail, un nodo Attendi di due ore e quindi un messaggio SMS.

## Tre modi per ottimizzare i percorsi {#optimization-methods}

Tramite l&#39;attività **Ottimizza** è possibile eseguire le azioni seguenti nei percorsi di percorso:

* [Esegui esperimenti sui percorsi](path-experimentation.md): esegui test di percorsi diversi in base a suddivisioni casuali per determinare quali prestazioni migliori in base alle metriche di successo predefinite (ad esempio, tasso di conversione, ricavi, coinvolgimento).

* [Sfrutta le regole di targeting](path-targeting.md): definisci le regole specifiche che devono essere soddisfatte affinché un cliente possa immettere uno dei percorsi di percorso, in base a segmenti di pubblico, attributi di profilo o dati contestuali. In questo modo il pubblico adatto entra nel percorso specificato.

  >[!AVAILABILITY]
  >
  >Questa funzionalità è attualmente disponibile in modo limitato. Per richiedere l’accesso, contatta il tuo rappresentante Adobe.

* [Applica condizioni](conditions.md) - Crea percorsi condizionali in base a criteri specifici quali origini dati, ora, data, divisioni percentuali o limiti di profilo. Equivale all’attività Condizione precedente.

## Come funziona {#how-it-works}

Una volta che il percorso è attivo, i profili vengono valutati in base ai criteri definiti e, in base ai criteri di corrispondenza, vengono inviati lungo il percorso appropriato dal percorso.

## Passaggi successivi {#next-steps}

Seleziona il metodo di ottimizzazione più adatto al tuo caso d’uso:

* Vuoi testare e scoprire quale percorso funziona meglio? → Vai a [Sperimentazione percorso](path-experimentation.md)
* Vuoi inviare diversi tipi di pubblico in percorsi specifici? → Vai a [Destinazione percorso](path-targeting.md)
* Creare una logica condizionale (scenari if/then)? → Vai a [Condizioni](conditions.md)

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene introdotta l&#39;attività Ottimizza, che sostituisce l&#39;attività Condizione precedente, che consente agli utenti di creare più percorsi di percorso utilizzando la sperimentazione, le regole di targeting o la logica condizionale.

**Intenti:**

* Scopri cosa fa l’attività Optimize e come sostituisce l’attività Condition precedente
* Creare più percorsi di percorso utilizzando la sperimentazione dei percorsi (test A/B)
* Definisci le regole di targeting per indirizzare specifici segmenti di pubblico o attributi di profilo verso percorsi separati
* Applicare la logica condizionale (if/then) utilizzando il metodo Conditions (Condizioni) all’interno dell’attività Optimize
* Migrare i percorsi esistenti che hanno utilizzato l’attività Condizione alla nuova attività Ottimizza

**Glossario:**

* **Ottimizza attività**: l&#39;attività dell&#39;area di lavoro del percorso che sostituisce l&#39;attività Condizione precedente e consente la creazione di più percorsi tramite sperimentazione, targeting o condizioni. *(specifico per prodotto)*
* **Percorso Percorso**: una sequenza all&#39;interno di un percorso che può essere costituita da comunicazioni, tempi di attesa, numero di messaggi o qualsiasi combinazione; i profili vengono instradati a un percorso basato sui criteri definiti nell&#39;attività Ottimizza. *(specifico per prodotto)*
* **Sperimentazione del percorso**: metodo Optimize che suddivide in modo casuale i profili tra i percorsi per determinare quali prestazioni sono migliori rispetto a metriche di successo predefinite, come il tasso di conversione o i ricavi. *(specifico per prodotto)*
* **Destinazione percorso**: metodo Optimize (attualmente in disponibilità limitata) che indirizza i profili ai percorsi basati su segmenti di pubblico, attributi di profilo o dati contestuali. *(specifico per prodotto)*
* **Condizioni**: metodo Optimize equivalente all&#39;attività Condizione precedente, che crea percorsi condizionali in base a origini dati, ora, data, frazionamenti percentuali o limiti di profilo. *(specifico per prodotto)*

**Guardrail:**

* Il targeting dei percorsi è attualmente a disponibilità limitata; contatta il rappresentante Adobe per richiedere l’accesso
* L’attività Condizione precedente è stata rimossa dall’interfaccia utente; i percorsi esistenti che la utilizzano continuano a funzionare e ora vengono visualizzati con una nuova icona come Attività di ottimizzazione che utilizzano il metodo Condizioni
* Le etichette personalizzate impostate sui nodi Condizione precedenti vengono mantenute dopo la migrazione a Ottimizza

**Terminologia:**

* Nome canonico: Ottimizza attività — Acronimo: none — varianti: ottimizzazione percorso percorso, ottimizza nodo
* Sinonimi: &quot;Ottimizza attività (metodo Condizioni)&quot; = &quot;attività Condizione precedente&quot;
* Da non confondere: &quot;Sperimentazione del percorso&quot; ≠ &quot;Targeting del percorso&quot;: la sperimentazione del percorso utilizza suddivisioni casuali per verificare quale percorso funziona meglio; il targeting del percorso utilizza regole definite per indirizzare pubblici specifici a percorsi specifici

**Domande frequenti:**

* **Q: Cos&#39;è successo all&#39;attività Condizione?** — È stato sostituito dall’attività Ottimizza e rimosso dall’interfaccia utente. I percorsi esistenti che utilizzavano le attività Condizione continuano a funzionare invariati; ora vengono visualizzati con una nuova icona come Ottimizza attività utilizzando il metodo Condizioni.
* **D: quali sono i tre metodi disponibili nell&#39;attività Ottimizza?** — sperimentazione del percorso (suddivisioni A/B casuali per trovare il percorso con le prestazioni migliori), targeting del percorso (routing basato su regole per attributi di pubblico o profilo, attualmente in Disponibilità limitata) e condizioni (logica condizionale if/then equivalente all&#39;attività Condizione precedente).
* **D: quali sono le differenze tra la sperimentazione sui percorsi e il targeting dei percorsi?** — La sperimentazione dei percorsi suddivide in modo casuale i profili per testare e confrontare le prestazioni dei percorsi rispetto alle metriche di successo; il targeting dei percorsi indirizza tipi di pubblico o di profilo specifici lungo percorsi designati in base a criteri definiti.
* **Q: il targeting del percorso è generalmente disponibile?** — No; è attualmente disponibile in modo limitato. Contatta il tuo rappresentante Adobe per richiedere l’accesso.
* **Q: cos&#39;è un percorso di percorso?** — Un percorso è una sequenza all&#39;interno di un percorso che può includere una combinazione di comunicazioni, periodi di attesa e conteggi dei messaggi; i profili vengono valutati e instradati al percorso appropriato in base ai criteri dell&#39;attività Ottimizza.

+++
