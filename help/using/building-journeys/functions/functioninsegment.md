---
product: journey optimizer
title: inSegment
description: Scopri la funzione in Segment
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, function, expression, percorsi
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 7ac246c0aa6776d3ec67223c4b07536b8ed0c881
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 6%

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

Solo i singoli utenti con lo stato di partecipazione al pubblico **Realizzato** verranno considerati membri del pubblico. Per ulteriori informazioni su come valutare un pubblico, consulta la [documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=it#interpret-segment-results).

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
