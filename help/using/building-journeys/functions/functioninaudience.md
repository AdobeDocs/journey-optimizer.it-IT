---
product: journey optimizer
title: inAudience
description: Scopri la funzione in Audience
feature: Journeys
role: Engineer
level: Experienced
keywords: inAudience, funzione, espressione, percorso
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---

# inAudience {#inAudience}

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

`inAudience('audienceName') == true` significa che hai un segmentMembership con lo stato immesso.

`inAudience('audienceName') == false` significa che hai un segmentMembership con stato di uscita.


>[!IMPORTANT]
>
>La modifica del nome di un pubblico esistente non aggiorna automaticamente alcun riferimento a tale pubblico nelle espressioni di percorso. Se il nodo della condizione utilizza `inAudience('oldAudienceName')`, è necessario modificare manualmente l&#39;espressione per utilizzare il nuovo nome. In caso contrario, la condizione del percorso si interromperà.

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

La funzione restituirà **[!UICONTROL true]** se l&#39;individuo all&#39;interno dell&#39;istanza del percorso fa parte del pubblico Adobe Experience Platform denominato &quot;uomini sopra i 50 anni&quot;, **[!UICONTROL false]** in caso contrario.

