---
title: Metodi di classificazione
description: Scopri come utilizzare i metodi di classificazione
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilità limitata"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 27%

---

# Metodi di classificazione {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Creare formule di classificazione"
>abstract="Le formule consentono di definire regole che determinano quale elemento deve essere presentato per primo, anziché tenere conto dei punteggi di priorità dell’elemento. Una volta creato un metodo di classificazione, puoi assegnarlo a una strategia di selezione per definire quali elementi devono essere selezionati per primi."

I metodi di classificazione consentono di classificare gli elementi da visualizzare per un determinato profilo. Una volta creato un metodo di classificazione, puoi assegnarlo a una strategia di selezione per definire quali elementi devono essere selezionati per primi.

Sono disponibili due tipi di metodi di classificazione:

* **Le formule** consentono di definire regole che determinano quale elemento deve essere presentato per primo, anziché tenere conto dei punteggi di priorità dell&#39;elemento.

* I **modelli AI** consentono di utilizzare sistemi di modelli addestrati che sfrutteranno più punti dati per determinare quale elemento deve essere presentato per primo.

## Creare metodi di classificazione {#create}

Per creare un metodo di classificazione, effettua le seguenti operazioni:

1. Passa al menu **[!UICONTROL Configurazione strategia]**, quindi seleziona il menu **[!UICONTROL Formule]** o **[!UICONTROL Modelli AI]** in base al tipo di classificazione che desideri utilizzare.

1. Fai clic sul pulsante **[!UICONTROL Crea formula]** o **[!UICONTROL Crea modello di IA]** nell&#39;angolo superiore destro dello schermo.

   ![](assets/ranking-create.png)

1. Configura la formula o il modello di IA in base alle tue esigenze, quindi salvalo.

   Informazioni dettagliate su come creare formule di classificazione e modelli di IA sono disponibili nella documentazione di gestione delle decisioni:

   * [Formule di classificazione](../offers/ranking/create-ranking-formulas.md)
   * [Modelli di intelligenza artificiale](../offers/ranking/ai-models.md)


## Sfruttare gli attributi degli elementi decisionali nelle formule {#items}

Le formule di classificazione sono espresse in **sintassi PQL** e possono sfruttare vari attributi come gli attributi del profilo, [dati contestuali](context-data.md) e attributi correlati agli elementi decisionali.

Per sfruttare gli attributi relativi agli elementi decisionali nelle formule, assicurati di seguire la sintassi riportata di seguito nel codice della formula di classificazione. Espandi ogni sezione per ulteriori informazioni:

+++Sfruttare gli attributi standard degli elementi decisionali

![](assets/formula-attribute.png)

+++

+++Sfruttare gli attributi personalizzati degli elementi decisionali

![](assets/formula-attribute-custom.png)

+++
