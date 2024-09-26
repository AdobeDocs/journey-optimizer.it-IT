---
solution: Journey Optimizer
product: journey optimizer
title: Accesso e gestione dei modelli di contenuto
description: Scopri come accedere e gestire i modelli di contenuto
topic: Content Management
role: User
level: Beginner
exl-id: ef6110c4-1aa6-4835-b0b0-b3c4fe0e7024
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 5%

---

# Accesso e gestione dei modelli di contenuto {#access-manage-templates}

## Accedere ai modelli di contenuto {#access}

Per accedere all&#39;elenco dei modelli di contenuto, selezionare **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli di contenuto]** dal menu a sinistra.

![](assets/content-template-list.png)

Vengono visualizzati tutti i modelli creati nella sandbox corrente, da un percorso o da una campagna tramite l&#39;opzione **[!UICONTROL Salva come modello]**, nel menu **[!UICONTROL Modelli di contenuto]**. [Scopri come creare i modelli](#create-content-templates)

Puoi ordinare i modelli di contenuto in base a:
* Tipo
* Channel
* Data di creazione o modifica
* Tag - [Ulteriori informazioni sui tag](../start/search-filter-categorize.md#tags)

Puoi anche scegliere di visualizzare solo gli elementi creati o modificati personalmente.

![](assets/content-template-list-filters.png)

## Modificare ed eliminare i modelli di contenuto {#edit}

* Per modificare il contenuto di un modello, fai clic sull’elemento desiderato dall’elenco e apporta le modifiche desiderate. È inoltre possibile modificare le proprietà del modello di contenuto facendo clic sul pulsante di modifica accanto al nome del modello.

  ![](assets/content-template-edit.png)

* Per eliminare un modello, seleziona il pulsante **[!UICONTROL Altre azioni]** accanto al modello desiderato, quindi seleziona **[!UICONTROL Elimina]**.

  ![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Quando si modifica o si elimina un modello, le campagne o i percorsi che includono il contenuto creato utilizzando questo modello non sono interessati.

## Visualizza modelli come miniature {#template-thumbnails}

Selezionare la modalità **[!UICONTROL Visualizzazione griglia]** per visualizzare ogni modello come miniatura.

>[!AVAILABILITY]
>
>Questa funzionalità viene rilasciata in Disponibilità limitata (LA) per un set limitato di clienti.

![](assets/content-template-grid-view.png)

>[!NOTE]
>
>Al momento le miniature corrette possono essere generate solo per modelli di contenuto e-mail di tipo HTML.

Quando aggiorni un contenuto, potresti dover attendere alcuni secondi prima che le modifiche vengano riportate nella miniatura.

## Esportare modelli di contenuto in un’altra sandbox {#export}

Journey Optimizer consente di copiare un modello di contenuto da una sandbox a un’altra. Ad esempio, puoi copiare un modello dall’ambiente sandbox di Stage alla sandbox di produzione.

Il processo di copia viene eseguito tramite un **pacchetto di esportazione e importazione** tra le sandbox di origine e di destinazione. Informazioni dettagliate su come esportare oggetti e importarli in una sandbox di destinazione sono disponibili in questa sezione: [Copia oggetti in un&#39;altra sandbox](../configuration/copy-objects-to-sandbox.md)
