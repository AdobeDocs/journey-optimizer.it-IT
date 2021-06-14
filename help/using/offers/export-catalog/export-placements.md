---
title: Set di dati sui posizionamenti
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per i posizionamenti.
feature: Offerte
topic: Integrazioni
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 2%

---

# Set di dati sui posizionamenti {#placements-dataset}

Ogni volta che un’offerta viene modificata, il set di dati generato automaticamente per i posizionamenti viene aggiornato.

![](../../assets/dataset-placements.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nel set di dati **[!UICONTROL Decision Object Repository - Placements]** .

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## Identificatore

**Campo:** _id 
**Titolo:** Identificatore 
**Descrizione:** un identificatore univoco per il record.
**Tipo:** stringa

## _esperienza

**Campo:** _experience 
**Type:** object

### _esperienza > decisionale

**Campo:** 
**tipo di decisione:** oggetto

#### _esperienza > decisionale > Identificatore del canale del posizionamento

**Campo:** canaleID 
**Titolo:** Identificativo canale del posizionamento 
**Descrizione:** il canale in cui è stata fatta la proposta. Il valore è un URI canale valido. Vedi https://ns.adobe.com/xdm/channels/channel.
**Tipo:** stringa

#### _esperienza > decisionale > Tipo componente di contenuto

**Campo:** tipo di componente 
**Titolo:** tipo di componente di contenuto 
**Descrizione:** un set enumerato di URI in cui ogni valore corrisponde a un tipo dato al componente di contenuto. Alcuni consumatori delle rappresentazioni di contenuto si aspettano che il valore @type sia un riferimento allo schema che descrive proprietà aggiuntive del componente di contenuto.
**Tipo:** stringa

#### _esperienza > decisionale > contentTypes

**Campo:** contentTypes 
**Tipo:** array

**_esperienza > decisionale > contentTypes > MIME Media Type**

**Titolo:** Tipo di elemento multimediale MIME 
**Descrizione:** un vincolo per il tipo di supporto dei componenti che si prevede in tale posizionamento. Per un componente, ad esempio un formato immagine diverso, potrebbe essere possibile utilizzare più di un tipo di supporto.
**Tipo:** stringa

#### _esperienza > decisionale > Posizionamento descrizione

**Campo:** descrizione 
**Titolo:** Posizionamento Descrizione 
**Descrizione:** viene utilizzato per comunicare all’utente le intenzioni leggibili riguardo al modo in cui il contenuto dinamico viene utilizzato nella consegna complessiva dei messaggi. Che un determinato spazio sia un \&quot;Banner\&quot; in una pagina web viene spesso veicolato tramite la descrizione e non con un metodo formale.
**Tipo:** stringa

#### _esperienza > decisionale > Nome posizionamento

**Campo:** nome 
**Titolo:** Nome posizionamento 
**Descrizione:** un nome assegnato per il posizionamento per farvi riferimento nelle interazioni umane.
**Tipo:** stringa

## _repo

**Campo:** _repo 
**Type:** object

### _repo > Posizionamento ETag

**Campo:** 
**Titolo tag:** Posizionamento ETag 
**Descrizione:** La revisione in cui si trovava l&#39;oggetto opzione di decisione al momento dello snapshot.
**Tipo:** stringa
