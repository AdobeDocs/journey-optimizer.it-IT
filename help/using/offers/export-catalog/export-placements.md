---
title: Set di dati sui posizionamenti
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per i posizionamenti.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Set di dati dei posizionamenti {#placements-dataset}

Ogni volta che un’offerta viene modificata, il set di dati generato automaticamente per i posizionamenti viene aggiornato.

![](../assets/dataset-placements.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Un posizionamento descrive una posizione o un luogo in un messaggio personalizzato. Viene utilizzato per impostare i vincoli tecnici per i contenuti forniti dalla decisione di personalizzazione. Il posizionamento rappresenta anche una richiesta per produrre determinati tipi di metriche quando viene prodotto un evento di esperienza in cui è coinvolto questo posizionamento. Ad esempio, il posizionamento facilita un’immagine personalizzata cliccabile all’interno di un’e-mail mostrata a un utente finale. Il posizionamento può, ad esempio, richiedere all&#39;esperienza assemblata che il clic sulla sua immagine venga riportato in un evento di esperienza con una metrica https://ns.adobe.com/xdm/data/metrics/web/linkclicks e un riferimento a questo posizionamento.

Elenco di tutti i campi che possono essere utilizzati nel set di dati **[!UICONTROL Decision Object Repository - Placements]** .

## Identificatore

Identificatore univoco del record.

Tipo: string

## _esperienza

### decisione

#### Identificatore del canale del posizionamento

Il canale in cui è stata fatta la proposta. Il valore è un URI canale valido. Vedi https://ns.adobe.com/xdm/channels/channel.

Tipo: string

#### Tipo componente contenuto

Set enumerato di URI in cui ogni valore corrisponde a un tipo assegnato al componente contenuto. Alcuni consumatori delle rappresentazioni di contenuto si aspettano che il valore @type sia un riferimento allo schema che descrive proprietà aggiuntive del componente di contenuto.

Tipo: string

#### Tipo di supporto MIME

Un vincolo per il tipo di supporto dei componenti previsto in tale posizionamento. Per un componente, ad esempio un formato immagine diverso, potrebbe essere possibile utilizzare più di un tipo di supporto.

Tipo: string

#### Descrizione del posizionamento

Viene utilizzato per comunicare intenzioni comprensibili agli utenti in merito al modo in cui il contenuto dinamico viene utilizzato nella consegna complessiva dei messaggi. Che un determinato spazio sia un \&quot;Banner\&quot; in una pagina web viene spesso veicolato tramite la descrizione e non con un metodo formale.

Tipo: string

#### Nome posizionamento

Un nome assegnato per il posizionamento per farvi riferimento nelle interazioni umane.

Tipo: string

## _repo

### Posizionamento ETag

Revisione in cui si trovava l&#39;oggetto opzione di decisione al momento dell&#39;esecuzione dello snapshot.

Tipo: string
