---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare i dati di Adobe Experience Platform per prendere decisioni (Beta)
description: Scopri come utilizzare i dati di Adobe Experience Platform per prendere decisioni.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor
exl-id: 46d868b3-01d2-49fa-852b-8c2e2f54292f
source-git-commit: cf700f4097883c875c74196317f6494f74f9bc7c
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 25%

---

# Utilizzare i dati di Adobe Experience Platform per la funzione Decisioni {#aep-data}

>[!CONTEXTUALHELP]
>id="ajo_exd_rules_dataset_lookup"
>title="Ricerca nei set di dati"
>abstract="L’utilizzo dei dati di Adobe Experience Platform nelle regole di decisione consente di definire criteri di idoneità in base ad attributi esterni dinamici, in modo che vengano mostrati solo gli elementi decisionali pertinenti. Crea una mappatura per definire come unire il set di dati di Adobe Experience Platform ai dati in [!DNL Journey Optimizer]. Seleziona il set di dati con gli attributi necessari e scegli una chiave di unione presente sia negli attributi dell’elemento decisionale che nel set di dati."

>[!CONTEXTUALHELP]
>id="ajo_exd_formula_dataset_lookup"
>title="Ricerca nei set di dati"
>abstract="Le formule di classificazione definiscono la priorità degli elementi decisionali. Utilizzando gli attributi del set di dati [!DNL Adobe Experience Platform], puoi regolare dinamicamente la logica di classificazione per riflettere le condizioni reali. Crea una mappatura per definire il modo in cui unire il set di dati di Adobe Experience Platform ai dati in [!DNL Journey Optimizer]. Seleziona il set di dati con gli attributi necessari e scegli una chiave di unione presente sia negli attributi dell’elemento decisionale che nel set di dati"

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile per tutta la clientela come versione Beta pubblica. Se desideri accedervi, contatta il rappresentante del tuo account.

[!DNL Journey Optimizer] consente di sfruttare i dati di [!DNL Adobe Experience Platform] per Decisioning. Questo consente di estendere la definizione degli attributi di decisione ai dati aggiuntivi nei set di dati per aggiornamenti in blocco che vengono modificati periodicamente senza dover aggiornare manualmente gli attributi uno alla volta. Ad esempio disponibilità, tempi di attesa e così via.

## Guardrail e limitazioni {#guidelines}

Prima di iniziare, prendi nota delle seguenti restrizioni e linee guida:

* Una policy decisionale può fare riferimento a un massimo di 3 set di dati totali, in tutte le sue regole decisionali e formule di classificazione combinate. Ad esempio, se le regole utilizzano 2 set di dati, le formule possono utilizzare solo 1 set di dati aggiuntivo.
* Una regola di decisione può utilizzare 3 set di dati.
* Una formula di classificazione può utilizzare 3 set di dati.
* Quando viene valutato un criterio decisionale, il sistema eseguirà fino a 1000 query di set di dati (ricerche) in totale. Ogni mappatura di set di dati utilizzata da un elemento decisionale conta come una query. Esempio: se un elemento di decisione utilizza 2 set di dati, la valutazione di tale offerta conta come 2 query per il limite di 1000 query.

## Abilitare un set di dati per la ricerca di dati {#enable}

Per utilizzare i dati di un set di dati [!DNL Adobe Experience Platform] per le decisioni, è necessario innanzitutto abilitarli per la ricerca tramite una chiamata API. Per istruzioni dettagliate, consulta questa sezione: [Sfruttare i set di dati di Adobe Experience Platform in Journey Optimizer](../data/lookup-aep-data.md).

## Sfruttare i dati Adobe Experience Platform {#leverage-aep-data}

Una volta abilitato un set di dati per la ricerca, puoi utilizzarne gli attributi per arricchire la logica decisionale con dati esterni. Questa funzione è particolarmente utile per gli attributi che cambiano frequentemente, ad esempio la disponibilità del prodotto o il prezzo in tempo reale.

Gli attributi dei set di dati di Adobe Experience Platform possono essere utilizzati in due parti della logica decisionale:

* **Regole di decisione**: definire se un elemento di decisione è idoneo per la visualizzazione.
* **Classificazione delle formule**: assegnazione di priorità agli elementi decisionali in base a dati esterni.

Nelle sezioni successive viene illustrato come utilizzare i dati di Adobe Experience Platform in entrambi i contesti.

### Regole di decisione {#rules}

L’utilizzo dei dati di Adobe Experience Platform nelle regole di decisione consente di definire criteri di idoneità in base ad attributi esterni dinamici, garantendo che gli elementi decisionali vengano visualizzati solo se pertinenti.

Supponiamo ad esempio che un retailer online desideri promuovere i prodotti consigliati in base all’inventario del negozio locale. Un prodotto può essere consigliato solo se è in stock nel luogo più vicino. In Adobe Experience Platform viene caricato un set di dati contenente gli aggiornamenti giornalieri dell’inventario. La logica della regola controlla se `inventory_count` per un determinato prodotto è maggiore di 0 per l&#39;archivio preferito del cliente. In tal caso, l’elemento decisionale è idoneo.

Per utilizzare i dati di Adobe Experience Platform nelle regole di decisione, effettua le seguenti operazioni:

1. Vai al menu **[!UICONTROL Imposta strategia]** / **[!UICONTROL Regole di decisione]** e seleziona **[!UICONTROL Crea regola con set di dati]**.

   ![](assets/exd-lookup-rule.png)

1. Fai clic su **[!UICONTROL Crea mappatura]** per definire il modo in cui il set di dati di Adobe Experience Platform si unisce ai dati in [!DNL Journey Optimizer].

   * Seleziona il set di dati con gli attributi necessari.
   * Scegli una chiave di unione (ad esempio, ID prodotto o ID store) presente sia negli attributi dell’elemento decisione che nel set di dati.

   ![](assets/exd-lookup-mapping.png)

   >[!NOTE]
   >
   >Puoi creare fino a 3 mappature per regola.

1. Fai clic su **[!UICONTROL Continua]**. È ora possibile accedere agli attributi del set di dati nel menu **[!UICONTROL Ricerca set di dati]** e utilizzarli nelle condizioni della regola. [Scopri come creare una regola di decisione](../experience-decisioning/rules.md#create)

   ![](assets/exd-lookup-menu.png)

### Formule di classificazione {#ranking-formulas}

Le formule di classificazione definiscono la priorità degli elementi decisionali. Utilizzando gli attributi del set di dati [!DNL Adobe Experience Platform], puoi regolare dinamicamente la logica di classificazione per riflettere le condizioni del mondo reale.

Ad esempio, supponiamo che una compagnia aerea utilizzi una formula di classificazione per dare priorità alle offerte di aggiornamento. Se un cliente ha un livello di fedeltà elevato e la disponibilità corrente dei posti è bassa (in base a un set di dati aggiornato ogni ora), gli viene assegnata una priorità maggiore. Il set di dati include campi come `flight_number`, `available_seats` e `loyalty_score`.

Per utilizzare i dati di Adobe Experience Platform nelle formule di classificazione, effettua le seguenti operazioni:

1. Crea o modifica una formula di classificazione. Nella sezione **[!UICONTROL Ricerca set di dati]** fare clic su **[!UICONTROL Crea mapping]**.

1. Definisci la mappatura del set di dati:

   * Seleziona il set di dati appropriato (ad esempio, disponibilità di posti in aereo).
   * Scegli una chiave di unione (ad esempio, numero di volo o ID cliente) presente sia negli attributi dell’elemento decisione che nel set di dati.

   ![](assets/exd-lookup-formula-mapping.png)

   >[!NOTE]
   >
   >Puoi creare fino a 3 mappature per formula di classificazione.

1. Utilizza i campi del set di dati per creare la formula di classificazione come di consueto. [Scopri come creare una formula di classificazione](ranking/ranking-formulas.md#create-ranking-formula)

   ![](assets/exd-lookup-formula-criteria.png)
