---
product: journey optimizer
title: inSegment
description: Scopri la funzione in Segment
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment, function, expression, percorsi
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 2%

---

# inSegment {#inSegment}

Controlla se un singolo appartiene a un determinato pubblico.

>[!NOTE]
>
>Puoi recuperare fino a 100 tipi di pubblico.

Il nome del pubblico deve essere una costante stringa. Non può essere un riferimento di campo né un&#39;espressione.

I tipi di pubblico sono definiti in [Adobe Experience Platform](https://platform.adobe.com/audience/overview). L’editor espressioni fornisce un elenco di tipi di pubblico compilato automaticamente.

I tipi di pubblico possono avere due stati:

* realizzati: l’entità è idonea per la definizione del segmento.
* uscita: l’entità sta uscendo dalla definizione del segmento.

Solo i singoli utenti con lo stato di partecipazione al pubblico **Realizzato** verranno considerati membri del pubblico. Per ulteriori informazioni su come valutare un pubblico, consulta la [documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inSegment('segmentName') == true` significa che hai un segmentMembership con lo stato inserito/esistente.

`inSegment('segmentName') == false` significa che hai un segmentMembership con stato di uscita.

## Categoria

Adobe Experience Platform

## Sintassi della funzione

`inSegment(<parameter>)`

## Parametri

| Parametro | Descrizione | Tipo |
|--- |--- |--- |
| Segmento | Il nome del pubblico | `<string>` |

## Firma e tipo restituito

`inSegment(<string>)`

Restituisce un valore booleano.

## Esempio

`inSegment("men over 50")`

Spiegazione:

La funzione restituirà **[!UICONTROL true]** se l&#39;individuo all&#39;interno dell&#39;istanza del percorso fa parte del pubblico Adobe Experience Platform denominato &quot;uomini sopra i 50 anni&quot;, **[!UICONTROL false]** in caso contrario.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene documentata la funzione legacy `inSegment`, che controlla se un profilo di percorso appartiene a un pubblico Adobe Experience Platform denominato e restituisce un valore booleano.

**Intenti:**
* Verifica se un profilo è un membro attivo di un pubblico denominato utilizzando `inSegment`
* Utilizza `inSegment('name') == true` per confermare l&#39;iscrizione del pubblico realizzato (attivo) in una condizione di percorso
* Utilizza `inSegment('name') == false` per confermare l&#39;iscrizione al pubblico chiuso (inattivo)

**Glossario:**
* **Realizzato**: lo stato di partecipazione del pubblico indica che l&#39;entità è attualmente idonea per la definizione del segmento *(specifico per prodotto)*
* **Uscita**: stato di partecipazione del pubblico che indica che l&#39;entità sta abbandonando o ha lasciato la definizione del segmento *(specifico per prodotto)*

**Guardrail:**
* È possibile recuperare fino a 100 tipi di pubblico in un singolo percorso
* Il nome del pubblico deve essere una costante stringa; i riferimenti e le espressioni di campo non sono supportati come parametri

**Terminologia:**
* Nome canonico: inSegment — Acronimo: none — varianti: inAudience (funzione attualmente preferita)
* Sinonimi: &quot;inSegment&quot; = &quot;audience membership check&quot; (legacy)
* Non confondere: &quot;inSegment&quot; (funzione legacy/obsoleta) ≠ &quot;inAudience&quot; (funzione attualmente consigliata)
* Non confondere: &quot;realized&quot; (membro attivo) ≠ &quot;exited&quot; (non più membro)

**Domande frequenti:**
* **Q: Qual è la differenza tra `inSegment` e `inAudience`?** — `inSegment` è il nome della funzione legacy; `inAudience` è la funzione attualmente consigliata. Entrambi verificano l&#39;appartenenza al pubblico, ma `inAudience` dispone di una documentazione più completa, inclusi i guardrail e i dettagli sui tempi di propagazione.
* **Q: cosa significa `inSegment('name') == true`?** — Significa che il profilo ha uno stato &quot;realized&quot; segmentMembership (realizzato), ovvero l’individuo è un membro attivo del pubblico.
* **Q: posso passare un&#39;espressione dinamica come nome del pubblico?** — No, il nome del pubblico deve essere una costante stringa; i riferimenti e le espressioni di campo non sono supportati.
* **Q: quanti tipi di pubblico posso valutare in un percorso?** — È possibile recuperare fino a 100 tipi di pubblico in un singolo percorso.

+++
