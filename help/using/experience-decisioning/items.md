---
title: Elementi decisionali
description: Scopri come utilizzare gli elementi decisionali
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 26%

---

# Elementi decisionali {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="Gestire gli elementi decisionali"
>abstract="Journey Optimizer consente di creare offerte di marketing, note come elementi decisionali, da creare e organizzare in un catalogo e in raccolte centralizzati. Attualmente, tutti gli elementi decisionali creati sono consolidati all’interno di un singolo catalogo “Offerte”. Da questa schermata, puoi anche accedere allo schema del catalogo utilizzando il pulsante **Modifica schema** e creare attributi personalizzati per gli elementi decisionali."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html?lang=it" text="Configurare il catalogo degli elementi"

>[!BEGINSHADEBOX &quot;Cosa troverai in questa guida alla documentazione&quot;]

* [Introduzione a Offer Decisioning](gs-experience-decisioning.md)
* Gestire gli elementi decisionali: [Configurare il catalogo articoli](catalogs.md) - **[Creare elementi decisionali](items.md)** - [Gestire le raccolte elementi](collections.md)
* Configura la selezione degli elementi: [Creare regole di decisione](rules.md) - [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* [Creare criteri di decisione](create-decision.md)

>[!ENDSHADEBOX]

Journey Optimizer consente di creare offerte di marketing, note come elementi decisionali, da creare e organizzare in un catalogo e in raccolte centralizzati. Sono costituiti da attributi standard e personalizzati progettati per allinearsi con precisione alle tue esigenze. Inoltre, incorporano vincoli di profilo che ti consentono di definire a chi può essere visualizzato un elemento decisionale.

Prima di creare un elemento di decisione, assicurati di aver creato un **regola di decisione** se desideri impostare le condizioni per determinare a chi può essere visualizzato l’elemento decisionale. [Scopri come creare regole di decisione](rules.md).

## Creare il primo elemento decisionale

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="Definire la priorità dell’elemento decisionale"
>abstract="Se un profilo è idoneo per più elementi, la priorità consente di confrontare questo elemento decisionale con altri. Una priorità più alta concede la precedenza di un elemento rispetto agli altri."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="Definire gli attributi personalizzati"
>abstract="Gli attributi personalizzati sono attributi specifici personalizzati in base alle proprie esigenze, che si possono assegnare a un elemento decisionale. Vengono creati nello schema del catalogo degli elementi decisionali. Questa sezione viene visualizzata solo se hai aggiunto almeno un attributo personalizzato allo schema del catalogo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html?lang=it" text="Configurare il catalogo degli elementi"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="Aggiungere tipi di pubblico o regole di decisione"
>abstract="Per impostazione predefinita, tutti i profili sono idonei a ricevere l’elemento decisionale, ma puoi utilizzare tipi di pubblico o regole per limitare l’elemento solo a profili specifici."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html?lang=it" text="Utilizzare i tipi di pubblico"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html?lang=it" text="Utilizzare le regole di decisione"

Per creare un elemento di decisione, effettua le seguenti operazioni:

1. Accedi a **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Elementi]**.

1. Definire gli attributi standard dell&#39;elemento di decisione:

   1. Immetti un nome e una descrizione.
   1. Specifica le date di inizio e fine. L’elemento verrà preso in considerazione solo dal motore decisionale entro queste date.
   1. Imposta il **[!UICONTROL Priorità]** dell’elemento decisionale rispetto ad altri, se un profilo è idoneo per più elementi. Una priorità più alta concede la precedenza di un elemento rispetto agli altri.

   ![](assets/item-attributes.png)

   >[!NOTE]
   >
   >La priorità è un tipo di dati intero. Tutti gli attributi che sono tipi di dati integer devono contenere valori interi (senza decimali).

1. Gli attributi personalizzati sono attributi specifici personalizzati in base alle proprie esigenze, che si possono assegnare a un elemento decisionale. Sono definite nello schema di catalogo degli elementi decisionali. [Scopri come utilizzare i cataloghi](catalogs.md)

1. Una volta definiti gli attributi dell’elemento decisionale, fai clic su **[!UICONTROL Successivo]** per impostare i vincoli di profilo per l&#39;elemento.

   Per impostazione predefinita, tutti i profili sono idonei a ricevere l’elemento decisione, ma puoi utilizzare tipi di pubblico o regole per limitare l’elemento solo a profili specifici, entrambe le soluzioni corrispondenti a utilizzi diversi. Per ulteriori informazioni, espandi la sezione seguente:

   +++Utilizzo dei tipi di pubblico e regole di decisione

   In sostanza, l’output di un pubblico è un elenco di profili, mentre una regola di decisione è una funzione eseguita su richiesta su un singolo profilo durante il processo decisionale.

   * **Tipi di pubblico**: da un lato, i tipi di pubblico sono un gruppo di profili Adobe Experience Platform che corrispondono a una determinata logica basata sugli attributi del profilo e sugli eventi di esperienza. Tuttavia, Gestione delle offerte non ricalcola il pubblico, che potrebbe non essere aggiornato al momento della presentazione dell’offerta.

   * **Regole di decisione**: d’altra parte, una regola di decisione si basa sui dati disponibili in Adobe Experience Platform e determina a chi può essere visualizzata un’offerta. Una volta selezionata in un’offerta o in una decisione per un determinato posizionamento, la regola viene eseguita ogni volta che viene presa una decisione, in modo che ogni profilo ottenga l’offerta più recente e migliore.

+++

   ![](assets/item-constraints.png)

   * Per limitare la presentazione dell’elemento decisionale ai membri di uno o più tipi di pubblico di Adobe Experience Platform, seleziona la **[!UICONTROL Visitatori che rientrano in uno o più tipi di pubblico]** , quindi aggiungi uno o più tipi di pubblico dal riquadro a sinistra e combinali utilizzando **[!UICONTROL E]** / **[!UICONTROL Oppure]** operatori logici. [Ulteriori informazioni sui tipi di pubblico](../audience/about-audiences.md).

   * Per associare una regola di decisione specifica all&#39;elemento di decisione, selezionare **[!UICONTROL Per regola]**, quindi trascinare la regola desiderata dal riquadro di sinistra nell&#39;area centrale. [Ulteriori informazioni sulle regole di decisione](rules.md).

   Quando selezioni tipi di pubblico o regole di decisione, puoi visualizzare informazioni sui profili qualificati stimati. Clic **[!UICONTROL Aggiorna]** per aggiornare i dati.

   >[!NOTE]
   >
   >Le stime del profilo non sono disponibili quando i parametri della regola includono dati non presenti nel profilo, come i dati contestuali. Ad esempio, una regola di idoneità che richiede che il tempo corrente sia di ≥80 gradi.

1. Una volta definiti i vincoli dell’elemento decisionale, fai clic su **[!UICONTROL Successivo]** per rivedere e salvare l&#39;elemento.

1. L’elemento decisionale viene ora visualizzato nell’elenco, con il comando **[!UICONTROL Bozza]** stato. Quando è pronto per essere presentato ai profili, fai clic sul pulsante con i puntini di sospensione e seleziona **[!UICONTROL Approva]**.

   ![](assets/item-approve.png)

## Gestire gli elementi decisionali

Dall’elenco degli elementi di decisione, puoi modificare un elemento di decisione, cambiarne lo stato (**Bozza**, **Approvato**, **Archiviato**), duplicarlo o eliminarlo.

Per modificare un elemento di decisione, aprilo, apporta le modifiche e salvalo.

Selezionando un elemento di decisione o facendo clic sul pulsante con i puntini di sospensione si abilitano le azioni descritte di seguito.

* **[!UICONTROL Approva]**: imposta lo stato dell’elemento di decisione su Approvato.
* **[!UICONTROL Annulla approvazione]**: imposta di nuovo lo stato dell’elemento decisionale su **[!UICONTROL Bozza]**.
* **[!UICONTROL Duplica]**: crea un elemento decisionale con attributi e vincoli identici. Per impostazione predefinita, il nuovo elemento presenta **[!UICONTROL Bozza]** stato.
* **[!UICONTROL Elimina]**: rimuove l’elemento decisionale dall’elenco.

  >[!IMPORTANT]
  >
  >Una volta eliminata, l’elemento decisionale e il relativo contenuto non sono più accessibili. Questa azione non può essere annullata. Se l’elemento di decisione viene utilizzato in una raccolta o in una decisione, non può essere eliminato. È necessario rimuovere prima l’elemento di decisione da qualsiasi oggetto.

* **[!UICONTROL Archivia]**: imposta lo stato dell’elemento di decisione su **[!UICONTROL Archiviato]**. L’elemento decisionale è ancora disponibile dall’elenco, ma non è possibile impostarne nuovamente lo stato su **[!UICONTROL Bozza]** o **[!UICONTROL Approvato]**. Puoi solo duplicarlo o eliminarlo.
