---
product: journey optimizer
title: funzione inAudience
description: Scopri la funzione Adobe Experience Platform inAudience
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, funzione, espressione, percorso, pubblico, segmentazione
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 4f653c0bd3f6998dd54deeae996b7b0427a1744e
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 2%

---

# funzione inAudience {#inAudience}

La funzione `inAudience` è una funzione di Adobe Experience Platform che consente di verificare se un individuo del percorso appartiene a un pubblico specifico. Questa potente funzione ti consente di creare percorsi di percorso personalizzati in base all’iscrizione al pubblico, abilitando segmentazione e targeting sofisticati all’interno delle esperienze dei clienti.

Utilizzare la funzione `inAudience` quando è necessario:

* Percorsi del percorso di rami basati sull’iscrizione al pubblico. [Ulteriori informazioni](../condition-activity.md#using-a-segment)
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

## Argomenti correlati

Scopri come utilizzare i tipi di pubblico in Adobe Journey Optimizer:

* **[Informazioni sui tipi di pubblico](../../audience/about-audiences.md)** - Comprendi come funzionano i tipi di pubblico in Adobe Experience Platform e Journey Optimizer, incluso come crearli e gestirli
* **[Attività Read Audience](../read-audience.md)** - Utilizza i tipi di pubblico per attivare l&#39;ingresso nel percorso e fare in modo che tutti i membri del pubblico entrino in un percorso
* **[Eventi di qualificazione del pubblico](../audience-qualification-events.md)** - Ascolta le entrate e le uscite del profilo dai tipi di pubblico per attivare le azioni di percorso in tempo reale
* **[Utilizzo di tipi di pubblico nelle condizioni](../condition-activity.md#using-a-segment)** - Creazione di percorsi di percorso condizionali in base all&#39;appartenenza al pubblico tramite l&#39;attività Condizione
* **[Proprietà Percorso - Criteri di unione](../journey-properties.md)** - Comprendere il funzionamento dei criteri di unione quando si utilizzano più tipi di pubblico con la funzione inAudience

