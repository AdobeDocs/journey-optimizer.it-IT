---
title: Introduzione a Decisioning
description: Ulteriori informazioni su Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 6b0735f619379e01e87012ba4300c0ec41334fd4
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 15%

---

# Introduzione a Decisioning {#get-started-experience-decisioning}

## Che cos’è Decisioning {#about}

La funzione Decisioni semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti.

Questi elementi decisionali vengono integrati direttamente in un&#39;ampia gamma di superfici in entrata tramite il [nuovo canale di esperienza basato su codice](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based), ora accessibile nelle campagne Journey Optimizer. I criteri decisionali sono disponibili per l’utilizzo solo nelle campagne di esperienza basate su codice.

## Guardrail e limitazioni {#guardrails}

Per garantire un utilizzo ottimale di Decisioning, tieni presenti le seguenti protezioni e limitazioni:

### Guardrail generali {#general}

* **Elementi offerta**: ogni raccolta di elementi può contenere fino a 500 elementi offerta.
* **Attributi personalizzati**: un elemento decisione può includere un massimo di 100 attributi personalizzati.
* **Strategie di selezione ed elementi decisionali per criterio**: un criterio di decisione supporta fino a 10 strategie di selezione e elementi decisionali combinati.

### Eligibility rules (Regole di idoneità) {#eligibility}

* **Livelli di nidificazione**: la profondità di nidificazione è limitata a 30 livelli. Questo viene misurato contando le `)` parentesi di chiusura nella stringa PQL.
* **Dimensione stringa regola**: una stringa regola può avere una dimensione massima di 15 KB per i caratteri con codifica UTF-8. Equivale a 15.000 caratteri ASCII (1 byte ciascuno) o 3.750-7.500 caratteri non ASCII (2-4 byte ciascuno).

### Formule di classificazione {#ranking}

* **Livelli di nidificazione**: la profondità di nidificazione è limitata a 30 livelli. Questo viene misurato contando le `)` parentesi di chiusura nella stringa PQL.
* **Dimensione stringa di formula**: una stringa di regola può avere una dimensione massima di 8 KB per i caratteri con codifica UTF-8. Equivale a 8.000 caratteri ASCII (1 byte ciascuno) o 2.000-4.000 caratteri non ASCII (2-4 byte ciascuno).

## Decisioning dei passaggi chiave {#steps}

I passaggi principali per lavorare con Decisioning sono i seguenti:

1. **Assegna le autorizzazioni appropriate**. Decisioning è disponibile solo per gli utenti con accesso a un **[!UICONTROL ruolo]** correlato a Decisioning, ad esempio i responsabili delle decisioni. Se non riesci ad accedere a Decisioning, devi estendere le autorizzazioni.

   +++Scopri come assegnare il ruolo Responsabili delle decisioni

   1. Per assegnare un ruolo a un utente nel prodotto [!DNL Permissions], passare alla scheda **[!UICONTROL Ruoli]** e selezionare Responsabili delle decisioni.

      ![](assets/decision_permission_1.png)

   1. Dalla sezione **[!UICONTROL Utenti]**, fai clic su **[!UICONTROL Aggiungi utente]**.

      ![](assets/decision_permission_2.png)

   1. Digita il nome o l’indirizzo e-mail dell’utente o selezionalo dall’elenco e fai clic su **[!UICONTROL Salva]**.

      Se l’utente non è stato creato in precedenza, consulta la [documentazione Aggiungere utenti](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

+++

1. **Configurare gli attributi personalizzati**: personalizzare il catalogo degli elementi in base alle proprie esigenze impostando gli attributi personalizzati nello schema del catalogo.

   ➡️ [Scopri come configurare il catalogo elementi](catalogs.md)

1. **Crea elementi decisionali** da mostrare al pubblico di destinazione.

   ➡️ [Scopri come creare elementi decisionali](items.md) ([documentazione API](api-reference/decisions-items/create.md))

1. **Organizza con le raccolte**: utilizza le raccolte per categorizzare gli elementi decisionali in base a regole basate su attributi. Incorpora le raccolte nelle strategie di selezione per determinare quale raccolta di elementi decisionali deve essere considerata.

   ➡️ [Scopri come gestire le raccolte di elementi](collections.md) ([documentazione API](api-reference/items-collections/create.md))

1. **Crea regole di decisione**: le regole di decisione vengono utilizzate negli elementi di decisione e/o nelle strategie di selezione per determinare a chi può essere visualizzato un elemento di decisione.

   ➡️ [Scopri come creare regole di decisione](rules.md)

1. **Implementare metodi di classificazione**: creare metodi di classificazione e applicarli nelle strategie di decisione per determinare l&#39;ordine di priorità per la selezione degli elementi di decisione.

   ➡️ [Scopri come creare metodi di classificazione](ranking.md)

1. **Creare strategie di selezione**: creare strategie di selezione che sfruttano raccolte, regole di decisione e metodi di classificazione per identificare gli elementi di decisione adatti alla visualizzazione nei profili.

   ➡️ [Scopri come creare strategie di selezione](selection-strategies.md) ([documentazione API](api-reference/selection-strategies/create.md))

1. **Crea un criterio di decisione e incorporalo nella campagna basata su codice**: i criteri di decisione combinano più strategie di selezione per determinare gli elementi di decisione idonei da visualizzare al pubblico previsto.

   ➡️ [Scopri come utilizzare i criteri di decisione](create-decision.md)
