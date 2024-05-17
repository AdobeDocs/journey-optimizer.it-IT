---
title: Elementi decisionali
description: Scopri come utilizzare gli elementi decisionali
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilità limitata"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: b6c5bb09d7a1cb7f61a532cd5ffd262436e09039
workflow-type: tm+mt
source-wordcount: '1746'
ht-degree: 14%

---

# Creare il primo elemento decisionale {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="Gestire gli elementi decisionali"
>abstract="Journey Optimizer consente di creare offerte di marketing, note come elementi decisionali, da creare e organizzare in un catalogo e in raccolte centralizzati. Attualmente, tutti gli elementi decisionali creati sono consolidati all’interno di un singolo catalogo “Offerte”. Da questa schermata, puoi anche accedere allo schema del catalogo utilizzando il pulsante **Modifica schema** e creare attributi personalizzati per gli elementi decisionali."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/decision-items/catalogs.html" text="Configurare il catalogo articoli"

Journey Optimizer consente di creare offerte di marketing, note come elementi decisionali, da creare e organizzare in un catalogo e in raccolte centralizzati. Sono costituiti da attributi standard e personalizzati progettati per allinearsi con precisione alle tue esigenze. Inoltre, incorporano vincoli di profilo che ti consentono di definire a chi può essere visualizzato un elemento decisionale.

Prima di creare un elemento di decisione, assicurati di aver creato un **regola di decisione** se desideri impostare le condizioni per determinare a chi può essere visualizzato l’elemento decisionale. [Scopri come creare regole di decisione](rules.md).

Per creare un elemento di decisione, passa a **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Cataloghi]**, quindi fai clic su **[!UICONTROL Crea elemento]** quindi segui i passaggi descritti nelle sezioni seguenti.

## Definire gli attributi dell’elemento decisionale {#attributes}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="Definire la priorità dell’elemento decisionale"
>abstract="Se un profilo è idoneo per più elementi, la priorità consente di confrontare questo elemento decisionale con altri. Una priorità più alta concede la precedenza di un elemento rispetto agli altri."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="Definire gli attributi personalizzati"
>abstract="Gli attributi personalizzati sono attributi specifici personalizzati in base alle proprie esigenze, che si possono assegnare a un elemento decisionale. Vengono creati nello schema del catalogo degli elementi decisionali. Questa sezione viene visualizzata solo se hai aggiunto almeno un attributo personalizzato allo schema del catalogo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/decision-items/catalogs.html" text="Configurare il catalogo articoli"

Per iniziare, definisci gli attributi standard e personalizzati dell’elemento decisionale:

![](assets/item-attributes.png)

1. Immetti un nome e una descrizione.
1. Specifica le date di inizio e fine. L’elemento verrà preso in considerazione solo dal motore decisionale entro queste date.
1. Imposta il **[!UICONTROL Priorità]** dell’elemento decisionale rispetto ad altri, se un profilo è idoneo per più elementi. Una priorità più alta concede la precedenza di un elemento rispetto agli altri.
1. Il **Tag** consente di assegnare tag unificati Adobe Experience Platform agli elementi decisionali. Questo consente di classificarli facilmente e di migliorare la ricerca. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags)

   >[!NOTE]
   >
   >La priorità è un tipo di dati intero. Tutti gli attributi che sono tipi di dati integer devono contenere valori interi (senza decimali).

1. Specificare gli attributi personalizzati (facoltativo). Gli attributi personalizzati sono attributi specifici personalizzati in base alle proprie esigenze, che si possono assegnare a un elemento decisionale. Sono definite nello schema di catalogo degli elementi decisionali. [Scopri come utilizzare i cataloghi](catalogs.md)

1. Una volta definiti gli attributi dell’elemento decisionale, fai clic su **[!UICONTROL Successivo]**.

## Configurare l’idoneità dell’elemento decisionale {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="Aggiungere tipi di pubblico o regole di decisione"
>abstract="Per impostazione predefinita, tutti i profili sono idonei a ricevere l’elemento decisionale, ma puoi utilizzare tipi di pubblico o regole per limitare l’elemento solo a profili specifici."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html?lang=it" text="Utilizzare i tipi di pubblico"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/selection/rules.html" text="Utilizzare le regole di decisione"

Per impostazione predefinita, tutti i profili sono idonei a ricevere l’elemento decisione, ma puoi utilizzare tipi di pubblico o regole per limitare l’elemento solo a profili specifici, entrambe le soluzioni corrispondenti a utilizzi diversi. Per ulteriori informazioni, espandi la sezione seguente:

+++Utilizzo dei tipi di pubblico e regole di decisione

In sostanza, l’output di un pubblico è un elenco di profili, mentre una regola di decisione è una funzione eseguita su richiesta su un singolo profilo durante il processo decisionale.

* **Tipi di pubblico**: da un lato, i tipi di pubblico sono un gruppo di profili Adobe Experience Platform che corrispondono a una determinata logica basata sugli attributi del profilo e sugli eventi di esperienza. Tuttavia, Gestione delle offerte non ricalcola il pubblico, che potrebbe non essere aggiornato al momento della presentazione dell’offerta.

* **Regole di decisione**: d’altra parte, una regola di decisione si basa sui dati disponibili in Adobe Experience Platform e determina a chi può essere visualizzata un’offerta. Una volta selezionata in un’offerta o in una decisione per un determinato posizionamento, la regola viene eseguita ogni volta che viene presa una decisione, in modo che ogni profilo ottenga l’offerta più recente e migliore.

+++

* Per limitare la presentazione dell’elemento decisionale ai membri di uno o più tipi di pubblico di Adobe Experience Platform, seleziona la **[!UICONTROL Visitatori che rientrano in uno o più tipi di pubblico]** , quindi aggiungi uno o più tipi di pubblico dal riquadro a sinistra e combinali utilizzando **[!UICONTROL E]** / **[!UICONTROL Oppure]** operatori logici. [Ulteriori informazioni sui tipi di pubblico](../audience/about-audiences.md).

* Per associare una regola di decisione specifica all&#39;elemento di decisione, selezionare **[!UICONTROL Per regola]**, quindi trascinare la regola desiderata dal riquadro di sinistra nell&#39;area centrale. [Ulteriori informazioni sulle regole di decisione](rules.md).

![](assets/item-constraints.png)

Quando selezioni tipi di pubblico o regole di decisione, puoi visualizzare informazioni sui profili qualificati stimati. Clic **[!UICONTROL Aggiorna]** per aggiornare i dati.

>[!NOTE]
>
>Le stime del profilo non sono disponibili quando i parametri della regola includono dati non presenti nel profilo, come i dati contestuali. Ad esempio, una regola di idoneità che richiede che il tempo corrente sia di ≥80 gradi.

## Impostare le regole di limitazione {#capping}

Il limite viene utilizzato come vincolo per definire il numero massimo di volte in cui è possibile presentare un’offerta. Limitare il numero di volte in cui gli utenti ricevono offerte specifiche consente di evitare di sollecitare eccessivamente i clienti e quindi di ottimizzare ogni punto di contatto con l’offerta migliore. Puoi creare fino a 10 maiuscole per un determinato elemento decisionale.

![](assets/item-capping.png)

>[!NOTE]
>
>
>L&#39;aggiornamento del valore del contatore di limite può richiedere fino a 3 secondi. Ad esempio, supponiamo che tu stia visualizzando un banner web che mostra un’offerta sul tuo sito web. Se un determinato utente passa alla pagina successiva del sito Web in meno di 3 secondi, il valore del contatore non verrà incrementato per tale utente.

Per impostare le regole di limite per l’elemento decisionale, fai clic su **[!UICONTROL Crea limite]** quindi seguire questi passaggi:

1. Definisci quale **[!UICONTROL Evento di limite]** per aumentare il contatore.

   * **[!UICONTROL Evento decisionale]** (valore predefinito): numero massimo di volte in cui è possibile presentare un’offerta.
   * **[!UICONTROL Impression]** (solo canali in entrata): numero massimo di volte che l’offerta può essere visualizzata a un utente.
   * **[!UICONTROL Clic]**: numero massimo di volte in cui un utente può fare clic sull’elemento decisionale.
   * **[!UICONTROL Evento personalizzato]**: puoi definire un evento personalizzato che verrà utilizzato per limitare il numero di volte in cui l’elemento viene inviato. Ad esempio, puoi limitare il numero di rimborsi fino a quando non raggiungono lo stesso 10000, o fino a quando un determinato profilo non viene rimborsato 1 volta. A tale scopo, utilizza [ADOBE EXPERIENCE PLATFORM XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"} schemi per creare una regola evento personalizzata.

   >[!NOTE]
   >
   >Per tutti gli eventi di limitazione ad eccezione di quelli decisionali, il feedback di gestione delle decisioni potrebbe non essere raccolto automaticamente e il contatore di limitazione potrebbe non essere incrementato correttamente. Per garantire che ogni evento di limitazione venga tracciato e contabilizzato nel contatore delle limitazioni, accertati che lo schema utilizzato per raccogliere gli eventi di esperienza includa il gruppo di campi corretto per tale evento. Informazioni dettagliate sulla raccolta dei dati sono disponibili nella documentazione relativa alla gestione delle decisioni di Journey Optimizer:
   >* [Raccolta dati di gestione delle decisioni](../offers/data-collection/data-collection.md)
   >* [Configurare la raccolta dati](../offers/data-collection/schema-requirement.md)

1. Scegliere il tipo di limite:

   * Seleziona **[!UICONTROL In totale]** per definire quante volte l’elemento può essere proposto nel pubblico target combinato, ovvero tra tutti gli utenti. Ad esempio, se sei un rivenditore di elettronica e hai concluso un&#39;operazione &quot;TV Doorbuster&quot;, vuoi che l&#39;offerta venga restituita solo 200 volte in tutti i profili.

   * Seleziona **[!UICONTROL Per profilo]** per definire quante volte l’offerta può essere proposta allo stesso utente. Ad esempio, se sei una banca con un&#39;offerta &quot;Carta di credito Platino&quot;, non vuoi che questa offerta venga visualizzata più di 5 volte per profilo. In effetti, si ritiene che se l&#39;utente ha visto l&#39;offerta 5 volte e non ha agito di conseguenza, ha una maggiore possibilità di agire sulla migliore offerta successiva.

1. In **[!UICONTROL Limite conteggio limite]** , specifica quante volte l’offerta può essere presentata a tutti gli utenti o per profilo, a seconda del tipo di limite selezionato. Il numero deve essere un numero intero maggiore di 0.

   Ad esempio, hai definito un evento di limite personalizzato, come il numero di checkout presi in considerazione. Se si immette 10 in **[!UICONTROL Limite conteggio limite]** , non verranno inviate altre offerte dopo 10 checkout.

1. In **[!UICONTROL Reimposta la frequenza di limite]** , impostare la frequenza di ripristino del contatore di quota limite. A questo scopo, definisci il periodo di tempo per il conteggio (giornaliero, settimanale o mensile) e inserisci il numero di giorni/settimane/mesi desiderato. Ad esempio, se desideri reimpostare il conteggio dei limiti ogni 2 settimane, seleziona **[!UICONTROL Ogni settimana]** dall’elenco a discesa corrispondente e digita **2** nell&#39;altro campo.

   >[!NOTE]
   >
   >Il ripristino del contatore del limite di frequenza si verifica alle **12:00 UTC**, il giorno definito o il primo giorno della settimana/mese, se applicabile. Il giorno di inizio della settimana è **Domenica**. Qualsiasi durata scelta non può superare **2 anni** (ossia il numero corrispondente di mesi, settimane o giorni).
   >
   >Dopo aver pubblicato l’elemento decisionale, non potrai modificare il periodo di tempo (mensile, settimanale o giornaliero) selezionato per la frequenza. Puoi comunque modificare il limite di frequenza se l’elemento presenta **[!UICONTROL Bozza]** e non è mai stato pubblicato prima con il limite di frequenza abilitato.

1. Clic **[!UICONTROL Crea]** per confermare la creazione della regola di limitazione di utilizzo. Puoi creare fino a 10 regole per un singolo elemento decisionale. A tale scopo, fare clic sul pulsante **[!UICONTROL Crea limite]** e ripetere i passaggi precedenti.

   ![](assets/item-capping-rules.png)

1. Una volta definite l’idoneità dell’elemento decisionale e le regole di limitazione, fai clic su **[!UICONTROL Successivo]** per rivedere e salvare l&#39;elemento.

1. L’elemento decisionale viene ora visualizzato nell’elenco, con il comando **[!UICONTROL Bozza]** stato. Quando è pronto per essere presentato ai profili, fai clic sul pulsante con i puntini di sospensione e seleziona **[!UICONTROL Approva]**.

   ![](assets/item-approve.png)

<!--* Identifying how many times a given customer has been shown a decision item. 
If a marketer wants to determine how many times a specific customer has been shown an offer, they can do that. Go to Profiles menu, Attributes tab. You'll see all counter values. The alphanumeric string is associated to the offer. To make the map, go to an item, in the URL check the last alphanumeric strings. D stands for day, w stands for week, m for month. "Ce" custom event-->

## Gestire gli elementi decisionali {#manage}

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
