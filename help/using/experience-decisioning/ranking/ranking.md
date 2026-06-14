---
title: Metodi di classificazione
description: Scopri come utilizzare i metodi di classificazione
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/1qUj05fLaRqqJGfaoL-y5uwtknp7HDkWKocHMde-8lc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 14%

---

# Metodi di classificazione {#rankings}

>[!BEGINSHADEBOX]

**In questa pagina:** crea metodi di classificazione, formule o modelli di IA, e assegnali a una strategia di selezione, in modo che il motore decisionale sappia quali elementi idonei presentare per primi per ciascun profilo.

>[!ENDSHADEBOX]

I metodi di classificazione consentono di classificare gli elementi da visualizzare per un determinato profilo. Una volta creato un metodo di classificazione, puoi assegnarlo a una strategia di selezione per definire quali elementi devono essere selezionati per primi.

Sono disponibili due tipi di metodi di classificazione:

* **Le formule** consentono di definire regole che determinano quale elemento deve essere presentato per primo, anziché tenere conto dei punteggi di priorità dell&#39;elemento.

* I **modelli AI** consentono di utilizzare sistemi di modelli addestrati che sfrutteranno più punti dati per determinare quale elemento deve essere presentato per primo.

## Creare metodi di ranking {#create}

Per creare un metodo di classificazione, effettua le seguenti operazioni:

1. Passa al menu **[!UICONTROL Configurazione strategia]**, quindi seleziona il menu **[!UICONTROL Formule]** o **[!UICONTROL Modelli AI]** a seconda del tipo di classificazione che desideri utilizzare.

   ![](../assets/ranking-create.png)

1. Fai clic sul pulsante **[!UICONTROL Crea formula]** o **[!UICONTROL Crea modello di IA]** nell&#39;angolo superiore destro dello schermo.

   Informazioni dettagliate su come creare formule di classificazione e modelli di IA sono disponibili nelle sezioni seguenti:

   * [Formule di ranking](ranking-formulas.md)
   * [Modelli di IA](ai-models.md)

1. Configura la formula o il modello di IA in base alle tue esigenze, quindi salvalo.

Il tuo metodo di classificazione è ora pronto per essere utilizzato in una [strategia di selezione](../selection-strategies.md) per classificare gli elementi decisionali idonei.


