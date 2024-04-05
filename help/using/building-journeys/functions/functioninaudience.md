---
product: journey optimizer
title: inAudience
description: Scopri la funzione in Audience
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, funzione, espressione, percorso
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---

# inAudience {#inAudience}

Controlla se un singolo appartiene a un determinato pubblico.

>[!NOTE]
>
>Puoi recuperare fino a 100 tipi di pubblico.

Il nome del pubblico deve essere una costante stringa. Non può essere un riferimento di campo né un&#39;espressione.

I tipi di pubblico sono definiti in [Adobe Experience Platform](https://platform.adobe.com/audience/overview). L’editor espressioni fornisce un elenco di tipi di pubblico compilato automaticamente.

I tipi di pubblico possono avere tre stati:

* esistente: l’entità continua a essere nel pubblico.
* realizzato: l’entità sta entrando nel pubblico.
* uscita: l’entità sta uscendo dal pubblico.

Solo i singoli utenti con **Realizzato** e **Esistente** gli stati di partecipazione del pubblico verranno considerati membri del pubblico. Per ulteriori informazioni su come valutare un pubblico, consulta [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inAudience('audienceName') == true` significa che disponi di un segmentMembership con lo stato inserito/esistente.

`inAudience('audienceName') == false` significa che disponi di segmentMembership dello stato di uscita.

## Categoria

Adobe Experience Platform

## Sintassi della funzione

`inAudience(<parameter>)`

## Parametri

| Parametro | Descrizione | Tipo |
|--- |--- |--- |
| Pubblico | Il nome del pubblico | `<string>` |

## Firma e tipo restituito

`inAudience(<string>)`

Restituisce un valore booleano.

## Esempio

`inAudience("men over 50")`

Spiegazione:

La funzione restituirà **[!UICONTROL true]** se l’individuo all’interno dell’istanza del percorso fa parte del pubblico Adobe Experience Platform denominato &quot;uomini sopra i 50 anni&quot;, **[!UICONTROL false]** altrimenti.
