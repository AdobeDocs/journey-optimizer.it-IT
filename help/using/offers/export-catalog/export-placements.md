---
title: Set di dati sui posizionamenti
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per i posizionamenti.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 1%

---

# Set di dati sui posizionamenti {#placements-dataset}

Ogni volta che un’offerta viene modificata, il set di dati generato automaticamente per i posizionamenti viene aggiornato.

![](../../assets/dataset-placements.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nella **[!UICONTROL Decision Object Repository - Placements]** set di dati.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## Identificatore

**Campo:** _id
**Titolo:** Identificatore
**Descrizione:** Identificatore univoco del record.
**Tipo:** string

## _esperienza

**Campo:** _esperienza
**Tipo:** oggetto

### _esperienza > decisionale

**Campo:** decisione
**Tipo:** oggetto

#### _esperienza > decisionale > Identificatore del canale del posizionamento

**Campo:** channelID
**Titolo:** Identificatore del canale del posizionamento
**Descrizione:** Il canale in cui è stata fatta la proposta. Il valore è un URI canale valido. Vedi https://ns.adobe.com/xdm/channels/channel.
**Tipo:** string

#### _esperienza > decisionale > Tipo componente di contenuto

**Campo:** componentType
**Titolo:** Tipo componente contenuto
**Descrizione:** Set enumerato di URI in cui ogni valore corrisponde a un tipo assegnato al componente contenuto. Alcuni consumatori delle rappresentazioni di contenuto si aspettano che il valore @type sia un riferimento allo schema che descrive proprietà aggiuntive del componente di contenuto.
**Tipo:** string

#### _esperienza > decisionale > contentTypes

**Campo:** contentTypes
**Tipo:** array

**_esperienza > decisionale > contentTypes > MIME Media Type**

**Titolo:** Tipo di supporto MIME
**Descrizione:** Un vincolo per il tipo di supporto dei componenti previsto in tale posizionamento. Per un componente, ad esempio un formato immagine diverso, potrebbe essere possibile utilizzare più di un tipo di supporto.
**Tipo:** string

#### _esperienza > decisionale > Posizionamento descrizione

**Campo:** descrizione
**Titolo:** Descrizione del posizionamento
**Descrizione:** Viene utilizzato per comunicare intenzioni comprensibili agli utenti in merito al modo in cui il contenuto dinamico viene utilizzato nella consegna complessiva dei messaggi. Che un determinato spazio sia un \&quot;Banner\&quot; in una pagina web viene spesso veicolato tramite la descrizione e non con un metodo formale.
**Tipo:** string

#### _esperienza > decisionale > Nome posizionamento

**Campo:** name
**Titolo:** Nome posizionamento
**Descrizione:** Un nome assegnato per il posizionamento per farvi riferimento nelle interazioni umane.
**Tipo:** string

## _repo

**Campo:** _repo
**Tipo:** oggetto

### _repo > Posizionamento ETag

**Campo:** etag
**Titolo:** Posizionamento ETag
**Descrizione:** Revisione in cui si trovava l&#39;oggetto opzione di decisione al momento dell&#39;esecuzione dello snapshot.
**Tipo:** string
