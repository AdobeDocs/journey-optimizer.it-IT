---
title: Set di dati sui posizionamenti
description: Questa sezione elenca tutti i campi utilizzati nel set di dati esportato per i posizionamenti
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 5%

---

# Set di dati sui posizionamenti {#placements-dataset}

Ogni volta che viene modificata un’offerta, viene aggiornato il set di dati generato automaticamente per i posizionamenti.

![](../assets/dataset-placements.png)

Il batch con esito positivo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ogni oggetto della Libreria di offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nel **[!UICONTROL Archivio oggetti decisione - Posizionamenti]** set di dati.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ Identificatore

**Campo:** _id
**Titolo:** Identificatore
**Descrizione:** Identificatore univoco del record.
**Tipo:** stringa

+++

+++ _esperienza

**Campo:** _experience
**Tipo:** oggetto

+++

+++ _experience > decisioning

**Campo:** decisioning
**Tipo:** oggetto

+++

+++ _experience > decisioning > Identificatore canale del posizionamento

**Campo:** channelID
**Titolo:** Identificatore canale del posizionamento
**Descrizione:** Il canale in cui è stata fatta la proposta. Il valore è un URI di canale valido. Vedi https://ns.adobe.com/xdm/channels/channel.
**Tipo:** stringa

+++

+++ _experience > decisioning > Tipo di componente Contenuto

**Campo:** componentType
**Titolo:** Tipo di componente contenuto
**Descrizione:** Set enumerato di URI in cui ogni valore corrisponde a un tipo assegnato al componente contenuto. Alcuni consumatori delle rappresentazioni di contenuto si aspettano che il valore @type sia un riferimento a uno schema che descrive proprietà aggiuntive del componente contenuto.
**Tipo:** stringa

+++

+++ _experience > decisioning > contentTypes

**Campo:** contentTypes
**Tipo:** array

+++

+++_esperienza > Decisioning > contentTypes > MIME Media Type

**Titolo:** Tipo di file multimediale MIME
**Descrizione:** Vincolo per il tipo di supporto dei componenti previsto in tale posizionamento. Potrebbero esistere più tipi di file multimediali possibili per un componente, ad esempio un formato immagine diverso.
**Tipo:** stringa

+++

+++ _experience > decisioning > Descrizione posizionamento

**Campo:** descrizione
**Titolo:** Descrizione posizionamento
**Descrizione:** Viene utilizzato per esprimere intenzioni leggibili sul modo in cui il contenuto dinamico viene utilizzato nella consegna complessiva dei messaggi. Il fatto che un determinato spazio sia un \&quot;Banner\&quot; in una pagina web è spesso veicolato tramite la descrizione e non tramite un metodo formale.
**Tipo:** stringa

+++

+++ _experience > decisioning > Nome posizionamento

**Campo:** nome
**Titolo:** Nome posizionamento
**Descrizione:** Un nome assegnato al posizionamento per farvi riferimento nelle interazioni umane.
**Tipo:** stringa

+++

+++ _repo

**Campo:** _repo
**Tipo:** oggetto

+++

+++ _repo > Posizionamento ETag

**Campo:** etag
**Titolo:** Posizionamento ETag
**Descrizione:** Revisione in cui si trovava l’oggetto opzione di decisione quando è stata acquisita l’istantanea.
**Tipo:** stringa

+++
