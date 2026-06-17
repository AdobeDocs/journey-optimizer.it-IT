---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere la personalizzazione nelle campagne orchestrate
description: Scopri come personalizzare i messaggi della campagna orchestrata utilizzando gli attributi di profilo, gli attributi di destinazione dalla tabella di lavoro e gli array di raccolta di arricchimento.
exl-id: c4a91e2b-6f08-4d1a-9e3b-2f8f5a0d1c62
version: Campaign Orchestration
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: e0a12bd7971c778378f9905cf93653792f38509d
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 0%

---

# Aggiungere la personalizzazione nelle campagne orchestrate {#add-personalization}

Dopo aver [orchestrato le attività](orchestrate-activities.md) nell&#39;area di lavoro e aggiunto un&#39;attività di canale, puoi personalizzare il contenuto del messaggio nell&#39;e-mail, SMS o in un altro editor di canale.

Personalization nelle campagne orchestrate funziona in modo simile ad altre campagne o percorsi [!DNL Journey Optimizer], con differenze associate alla **tabella di lavoro**: attributi calcolati dalle attività di targeting e arricchimento nell&#39;area di lavoro, non solo i dati dell&#39;archivio profili.

## Accedere all’editor di personalizzazione {#access}

1. Apri la campagna orchestrata e aggiungi un’attività di canale. [Scopri come aggiungere un&#39;attività canale](activities/channels.md#add)

1. Configura l&#39;attività del canale, quindi apri la scheda **[!UICONTROL Contenuto]** e modifica il messaggio.

1. Nell’editor dei messaggi, utilizza l’editor di personalizzazione per inserire attributi nel contenuto.

Per visualizzare l&#39;anteprima e verificare i contenuti personalizzati dall&#39;attività del canale, consulta [Verifica e verifica i contenuti](activities/channels.md#simulate-content-test-profiles).

## Attributi di profilo e di destinazione {#attributes}

Quando apri l’editor di personalizzazione, due cartelle principali contengono gli attributi disponibili per la personalizzazione:

* **[!UICONTROL Attributi del profilo]**

  Dati relativi al profilo da [!DNL Adobe Experience Platform]: nome, indirizzo e-mail, posizione e altre caratteristiche acquisite nel profilo utente.

* **[!UICONTROL Attributi di destinazione]** (solo campagne orchestrate)

  Attributi calcolati nell’area di lavoro della campagna dalla tabella di lavoro. Questa cartella contiene due sottocartelle:

   * **`<Targeting dimension>`** (ad esempio, Destinatari o Acquisti) — Attributi relativi alla dimensione di destinazione nella campagna.

   * **`Enrichment`** — Dati aggiunti tramite **[!UICONTROL attività di arricchimento]** (collegamenti relazionali, righe raccolte, aggregati). Dopo un arricchimento di 1:N **[!UICONTROL Raccolta dati]**, si ottengono sia righe numerate che un array di raccolta. [Scopri come utilizzare i dati della raccolta di arricchimento](#enrichment-collections)

Per una panoramica dettagliata dell&#39;editor di personalizzazione in [!DNL Journey Optimizer], vedi [Introduzione alla personalizzazione](../personalization/personalize.md).

## Utilizzare i dati della raccolta di arricchimento {#enrichment-collections}

Quando configuri un&#39;attività **[!UICONTROL Enrichment]** con un collegamento 1:N e **[!UICONTROL Collect data]**, gli attributi di arricchimento sono disponibili in **[!UICONTROL Attributi di destinazione] > [!UICONTROL Enrichment]** in due forme:

* **Righe appiattite** — Un campo per riga recuperata (ad esempio, **Acquisto 1**, **Acquisto 2**, **Acquisto 3**), ciascuno con gli attributi selezionati sul collegamento (ad esempio prezzo o prodotto). Utilizzare queste opzioni quando sono necessari slot separati e fissi, ad esempio `target.enrichment.purchase1.price`.

* **Matrice di raccolta**: una matrice per tutte le righe raccolte, denominata dall&#39;etichetta del collegamento (ad esempio, **acquisti**). Utilizzalo quando devi lavorare sull&#39;intero set di record, con [funzioni array](#array-functions).

![](assets/enrichment-target-attributes-picker.png)

Per identificare le righe di flattend dall&#39;array di raccolta, inserire l&#39;attributo nell&#39;editor di espressioni e leggere il percorso generato. L&#39;array di raccolta è la voce il cui percorso è **plural** (ad esempio `purchases`) e non ha **alcun numero di riga** (`purchase1`, `purchase2` e così via).

| Cosa ti serve | Percorso nell’editor espressioni |
| --- | --- |
| **Una riga raccolta** | **Numerato**, ad esempio `target.enrichment.purchase1.price` |
| **Raccolta completa** | **Plurale e senza numero**, ad esempio `target.enrichment.purchases.price` |

È possibile applicare le stesse [funzioni array ed elenco](../personalization/functions/arrays-list.md) utilizzate altrove in [!DNL Journey Optimizer] a una raccolta di arricchimento, facendo riferimento a `target.enrichment.<label>`.

Ad esempio, in una riga dell&#39;oggetto puoi visualizzare il numero di acquisti raccolti esistenti e il prezzo del primo articolo:

```sql
Hello number of Items: {%= count(target.enrichment.purchases.price) %} , Name of first item: {%= head(target.enrichment.purchases.product) %}
```

➡️ [Scopri come configurare l&#39;arricchimento della raccolta nell&#39;area di lavoro](activities/enrichment.md#collection-personalization)
