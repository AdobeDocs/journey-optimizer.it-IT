---
product: journey optimizer
title: Funzione inAudience
description: Scopri la funzione Adobe Experience Platform inAudience
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, funzione, espressione, percorso, pubblico, segmentazione
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DU8HtduB2-GmakiaHBMFU1vzBBPoVTNvrOCPWQrr5SU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1279
ht-degree: 1%

---

# Funzione inAudience {#inAudience}

La funzione `inAudience` è una funzione di Adobe Experience Platform che consente di verificare se un individuo del percorso appartiene a un pubblico specifico. Questa potente funzione ti consente di creare percorsi di percorso personalizzati in base all’iscrizione al pubblico, abilitando segmentazione e targeting sofisticati all’interno delle esperienze dei clienti.

Utilizzare la funzione `inAudience` quando è necessario:

* Percorsi del percorso di rami basati sull’iscrizione al pubblico. [Ulteriori informazioni](../conditions.md#using-a-segment)
* Applicare una logica condizionale che dipende dall’appartenenza di un profilo a un segmento specifico
* Eseguire il targeting di gruppi specifici di clienti con esperienze personalizzate
* Valutazione della partecipazione del pubblico in tempo reale in condizioni di percorso
* Combinare più controlli di pubblico per creare regole di targeting complesse

La funzione valuta l’appartenenza al pubblico in tempo reale e restituisce un valore booleano, rendendolo ideale per i nodi decisionali e le espressioni condizionali. I tipi di pubblico vengono definiti e gestiti in [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} (ulteriori informazioni su [utilizzo dei tipi di pubblico](../../audience/about-audiences.md) in Journey Optimizer) e l&#39;editor espressioni fornisce suggerimenti di completamento automatico per aiutarti a farvi riferimento in modo accurato.

**Stato pubblico:**

I tipi di pubblico possono avere due stati di partecipazione:

* **Realizzato**: l&#39;individuo è idoneo per la definizione del pubblico ed è un membro attivo
* **Uscito**: l&#39;utente ha lasciato il pubblico e non è più idoneo

Solo i singoli utenti con lo stato **Realizzato** verranno considerati membri del pubblico attivi. Quando la funzione restituisce `true`, conferma che l&#39;individuo ha realizzato lo stato; quando restituisce `false`, indica lo stato di uscita. Per ulteriori informazioni sulla valutazione del pubblico, consulta la [documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

+++Sintassi

`inAudience(<parameter>)`

+++

+++Parametri

| Parametro | Descrizione | Tipo |
|--- |--- |--- |
| Pubblico | Il nome del pubblico | `<string>` |

**Vincoli importanti:**

* Il nome del pubblico deve essere una costante stringa
* Non può essere un riferimento di campo o un&#39;espressione
* Puoi recuperare fino a 100 tipi di pubblico in un singolo percorso

+++

+++Firma e tipo restituito

`inAudience(<string>)`

Restituisce un valore booleano:
* `true`: l&#39;individuo è membro del pubblico (stato realizzato)

* `false`: l&#39;individuo non è un membro del pubblico (stato di uscita)

+++

+++Esempi

`inAudience("men over 50")`

Restituisce **true** se l&#39;individuo all&#39;interno dell&#39;istanza del percorso fa parte del pubblico Adobe Experience Platform denominato &quot;uomini sopra i 50&quot;, **false** in caso contrario.

**Casi d&#39;uso pratici:**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## Guardrail e limitazioni {#guardrails}

Quando utilizzi la funzione `inAudience` nei tuoi percorsi, tieni presente le seguenti protezioni e limitazioni:

**Limite di recupero pubblico:**
* Puoi recuperare fino a 100 tipi di pubblico in un singolo percorso
* L’editor di espressioni fornisce un elenco completato automaticamente dei tipi di pubblico disponibili, per aiutarti a farvi riferimento correttamente

**Vincoli dei parametri:**
* Il nome del pubblico deve essere una costante stringa
* I riferimenti e le espressioni di campo non sono supportati come parametri

**Modifiche nome pubblico:**
* La modifica del nome di un pubblico esistente in Adobe Experience Platform non aggiorna automaticamente i riferimenti a tale pubblico nelle espressioni di percorso
* Se il nodo della condizione utilizza `inAudience('oldAudienceName')`, è necessario modificare manualmente l&#39;espressione per utilizzare il nuovo nome
* Se non si aggiorna il nome del pubblico, la condizione di percorso si interromperà e si potrebbe verificare un comportamento di percorso errato

**Considerazioni sui criteri di unione:**
* Quando si utilizzano più tipi di pubblico con la funzione `inAudience`, le incoerenze con i criteri di unione possono causare errori o avvisi
* Per ulteriori informazioni sul comportamento dei criteri di unione, vedere [Proprietà Percorso](../journey-properties.md)

**Tempistica di propagazione:** {#propagation-timing}

Quando si utilizza `inAudience()` in un nodo condizione, i tempi di valutazione dell&#39;appartenenza ai segmenti variano a seconda della posizione in cui la condizione viene visualizzata nel percorso:

* **In un percorso Read Audience, prima di un&#39;attività Wait:** Journey Optimizer legge dalla proiezione batch del profilo. I dati in questa proiezione vengono aggiornati entro **2 ore** dopo l&#39;acquisizione. I tipi di pubblico che si basano su condizioni giornaliere o basate su un intervallo di tempo possono subire un ulteriore ritardo. Aggiungi una breve [Attività di attesa](../wait-activity.md) all&#39;inizio del percorso oppure consenti un tempo di buffer per garantire che venga riflessa l&#39;ultima appartenenza al segmento.
* **In un percorso di eventi unitario o dopo un&#39;attività Attendi:** l&#39;appartenenza al segmento viene letta dalla proiezione streaming (unitaria). I dati sono generalmente disponibili entro **15 minuti**. Per ulteriori dettagli, consulta la [documentazione sull&#39;acquisizione streaming di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/streaming/overview){target="_blank"}.

## Argomenti correlati

Scopri come utilizzare i tipi di pubblico in Adobe Journey Optimizer:

* **[Informazioni sui tipi di pubblico](../../audience/about-audiences.md)** - Comprendi come funzionano i tipi di pubblico in Adobe Experience Platform e Journey Optimizer, incluso come crearli e gestirli
* **[Attività Read Audience](../read-audience.md)** - Utilizza i tipi di pubblico per attivare l&#39;ingresso nel percorso e fare in modo che tutti i membri del pubblico entrino in un percorso
* **[Eventi di qualificazione del pubblico](../audience-qualification-events.md)** - Ascolta le entrate e le uscite del profilo dai tipi di pubblico per attivare le azioni di percorso in tempo reale
* **[Utilizzo di tipi di pubblico nelle condizioni](../conditions.md#using-a-segment)** - Creazione di percorsi di percorso condizionali in base all&#39;appartenenza al pubblico tramite l&#39;attività Ottimizza
* **[Proprietà Percorso - Criteri di unione](../journey-properties.md)** - Comprendere il funzionamento dei criteri di unione quando si utilizzano più tipi di pubblico con la funzione inAudience

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina è documentata la funzione `inAudience`, che controlla in tempo reale se un profilo di percorso appartiene a un pubblico Adobe Experience Platform denominato e restituisce un valore booleano utilizzato in condizioni di percorso.

**Intenti:**
* Dividi un percorso di percorso in base al fatto che un profilo sia membro di un pubblico specifico utilizzando `inAudience`
* Combinare più controlli `inAudience` con logica AND/OR per creare condizioni di targeting complesse
* Verificare che un profilo non sia entrato in un pubblico specifico utilizzando un controllo di negazione (`inAudience("...") == false`)
* Comprendere le differenze di tempistica della propagazione tra Leggi percorsi di pubblico e percorsi di eventi unitari
* Identificare e correggere i riferimenti di pubblico interrotti causati dalla ridenominazione del pubblico in Adobe Experience Platform

**Glossario:**
* **Realizzato**: lo stato di partecipazione del pubblico indica che l&#39;individuo è attualmente idoneo per la definizione del pubblico ed è un membro attivo *(specifico per prodotto)*
* **Uscita**: lo stato di partecipazione del pubblico indica che l&#39;utente ha lasciato il pubblico e non è più idoneo *(specifico per prodotto)*
* **Criterio di unione**: regola in Adobe Experience Platform che determina il modo in cui vengono combinati i dati del profilo da più set di dati durante la valutazione dell&#39;appartenenza al pubblico *(specifico per prodotto)*
* **Proiezione batch**: l&#39;archivio dati del profilo è stato aggiornato secondo una pianificazione (entro 2 ore dall&#39;acquisizione) utilizzata da Read Audience percorsi *(specifico per prodotto)*
* **Proiezione in streaming**: l&#39;archivio dati del profilo in tempo reale (in genere disponibile entro 15 minuti) utilizzato nei percorsi di eventi unitari e dopo le attività di attesa *(specifiche del prodotto)*

**Guardrail:**
* Un singolo percorso può recuperare fino a 100 pubblici
* Il parametro del nome del pubblico deve essere una costante stringa; i riferimenti di campo e le espressioni dinamiche non sono supportati
* La ridenominazione di un pubblico in Adobe Experience Platform non aggiorna automaticamente i riferimenti `inAudience` nelle espressioni di percorso; sono necessari aggiornamenti manuali
* I criteri di unione non coerenti tra più tipi di pubblico utilizzati nello stesso percorso possono causare errori o avvisi

**Terminologia:**
* Nome canonico: inAudience — Acronimo: none — varianti: inSegment (nome legacy)
* Sinonimi: &quot;inAudience&quot; = &quot;funzione di controllo dell’iscrizione al pubblico&quot;
* Non confondere: &quot;Realized&quot; (membro attivo) ≠ &quot;Exited&quot; (non più membro)
* Non confondere: &quot;inAudience&quot; (funzione corrente) ≠ &quot;inSegment&quot; (funzione legacy obsoleta)

**Domande frequenti:**
* **D: cosa restituisce `inAudience` quando un profilo esce dal pubblico?** — Restituisce `false`. Solo i profili con stato &quot;Realizzato&quot; sono considerati membri attivi e restituiscono `true`.
* **Q: quanti tipi di pubblico posso archiviare in un singolo percorso?** — È possibile recuperare fino a 100 tipi di pubblico in un singolo percorso.
* **D: cosa succede se rinomino un pubblico in Adobe Experience Platform dopo averlo utilizzato in un percorso?** — L&#39;espressione di percorso non viene aggiornata automaticamente. Per utilizzare il nuovo nome del pubblico, è necessario modificare manualmente la chiamata `inAudience`, altrimenti la condizione si interromperà.
* **D: quanto rapidamente è disponibile l&#39;iscrizione al pubblico dopo un aggiornamento del profilo in un percorso Read Audience?** — In un percorso Read Audience prima di un’attività Wait (Leggi pubblico prima di un’attività Attendi), i dati vengono letti dalla proiezione batch aggiornata entro 2 ore dall’acquisizione.
* **Q: posso passare un attributo di profilo come parametro del nome del pubblico?** — No, il nome del pubblico deve essere una costante stringa; i riferimenti e le espressioni di campo non sono supportati.

+++
