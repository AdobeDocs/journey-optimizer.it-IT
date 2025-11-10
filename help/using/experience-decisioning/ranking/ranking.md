---
title: Metodi di classificazione
description: Scopri come utilizzare i metodi di classificazione
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 16%

---

# Metodi di classificazione {#rankings}

I metodi di classificazione consentono di classificare gli elementi da visualizzare per un determinato profilo. Una volta creato un metodo di classificazione, puoi assegnarlo a una strategia di selezione per definire quali elementi devono essere selezionati per primi.

Sono disponibili due tipi di metodi di classificazione:

* **Le formule** consentono di definire regole che determinano quale elemento deve essere presentato per primo, anziché tenere conto dei punteggi di priorità dell&#39;elemento.

* I **modelli AI** consentono di utilizzare sistemi di modelli addestrati che sfrutteranno più punti dati per determinare quale elemento deve essere presentato per primo.

## Creare metodi di classificazione {#create}

Per creare un metodo di classificazione, effettua le seguenti operazioni:

1. Passa al menu **[!UICONTROL Configurazione strategia]**, quindi seleziona il menu **[!UICONTROL Formule]** o **[!UICONTROL Modelli AI]** a seconda del tipo di classificazione che desideri utilizzare.

   ![](../assets/ranking-create.png)

1. Fai clic sul pulsante **[!UICONTROL Crea formula]** o **[!UICONTROL Crea modello di IA]** nell&#39;angolo superiore destro dello schermo.

   Informazioni dettagliate su come creare formule di classificazione e modelli di IA sono disponibili nelle sezioni seguenti:

   * [Formule di classificazione](ranking-formulas.md)
   * [Modelli di IA](ai-models.md)

1. Configura la formula o il modello di IA in base alle tue esigenze, quindi salvalo.

Il tuo metodo di classificazione è ora pronto per essere utilizzato in una [strategia di selezione](../selection-strategies.md) per classificare gli elementi decisionali idonei.


