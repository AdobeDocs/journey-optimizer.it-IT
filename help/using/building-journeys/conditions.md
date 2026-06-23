---
solution: Journey Optimizer
product: journey optimizer
title: Condizioni
description: Configurare le condizioni nell’attività Ottimizzare per i percorsi dei percorsi
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attività, condizione, area di lavoro, percorso
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/8gtrjnNNob-iRXdjSytSYOMyDswVxsrd8knipi4i1gI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 2629
ht-degree: 11%

---

# Condizioni {#conditions}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare le condizioni nell&#39;attività Ottimizza per creare più percorsi di percorso in base a origini dati, ora, date, percentuali di suddivisione, limiti di profilo o appartenenza a un pubblico.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_conditions"
>title="Condizioni"
>abstract="Le condizioni consentono di definire il modo in cui i singoli utenti avanzano nel percorso, mediante la creazione di più percorsi in base a criteri specifici. Puoi anche configurare un percorso alternativo per gestire timeout o errori, per un’esperienza sempre fluida. Tieni presente che ora le condizioni sono configurate nell’attività Ottimizza, che sostituisce la precedente attività Condizione."

Con **condizioni** puoi definire il modo in cui i singoli utenti avanzano nel tuo percorso creando più percorsi in base a criteri specifici. Puoi anche configurare un percorso alternativo per gestire timeout o errori, per un’esperienza sempre fluida.

>[!NOTE]
>
>Il nuovo veicolo per la creazione di percorsi condizionali nei percorsi è l&#39;attività [Ottimizza](optimize.md). Sostituisce l’attività **Condizione** precedente, che è stata rimossa dall’interfaccia utente. Tutta la logica condizionale viene ora gestita tramite le condizioni dell’attività Ottimizza presentate in questa pagina.
>
>Se esistono percorsi che hanno utilizzato **[!UICONTROL Attività condizionali]**, puoi continuare a utilizzarli come prima. Vengono ora visualizzate con una nuova icona come attività **[!UICONTROL Ottimizza]** utilizzando il metodo **[!UICONTROL Condizione]**, ma il comportamento rimane invariato. Tutte le etichette personalizzate impostate sul nodo vengono mantenute.

## Aggiungere una condizione {#add-condition-activity}

Per aggiungere una condizione al percorso, attieniti alla procedura seguente.

1. Rilascia l&#39;attività **[!UICONTROL Ottimizza]** nell&#39;area di lavoro del percorso. [Ulteriori informazioni](optimize.md)

1. Aggiungi un’etichetta opzionale per identificare l’attività nei rapporti e nei registri in modalità di test.

1. Selezionare una condizione dall&#39;elenco a discesa **[!UICONTROL Metodo]**.

   ![Ottimizza attività con metodo condizione selezionato](assets/journey-optimize-condition.png){width=80%}

   Sono disponibili i seguenti tipi di condizioni:

   * [Condizione origine dati](#data_source_condition)
   * [Condizione temporale](#time_condition)
   * [Divisione percentuale](#percentage_split)
   * [Condizione data](#date_condition)
   * [Limite del profilo](#profile_cap)
   * È inoltre possibile utilizzare un pubblico in una condizione di percorso. [Ulteriori informazioni](#using-a-segment)

>[!NOTE]
>
>La valutazione della condizione non riuscirà per i profili che includono più di due identità multi-dispositivo nell&#39;[archivio profili](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}.

## Gestire i percorsi con condizioni {#condition_paths}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_simple2"
>title="Editor di espressioni semplici"
>abstract="La modalità editor di espressioni semplici consente di eseguire query semplici basate su una combinazione di campi. Tutti i campi disponibili sono visualizzati a sinistra. I campi vengono trascinati nella zona principale. Per combinare i diversi elementi, questi vengono interconnessi tra loro per creare gruppi e/o livelli di gruppo diversi. Un operatore logico combina quindi gli elementi sullo stesso livello."

Quando utilizzi più condizioni in un percorso, puoi definire le etichette per ciascuna di esse in modo da identificarle più facilmente.

Fare clic su **[!UICONTROL Aggiungi un percorso]** se si desidera definire più condizioni. Per ogni condizione, nell’area di lavoro viene aggiunto un nuovo percorso dopo l’attività.

![Aggiungi un pulsante percorso per creare più percorsi condizione](assets/journey-condition-add-path.png){width=80%}

Si noti che la progettazione dei percorsi ha un impatto funzionale. Quando più percorsi vengono definiti dopo una condizione, verrà eseguito solo il primo percorso idoneo. Ciò significa che puoi variare la priorità dei percorsi posizionandoli uno sopra l’altro o al di sotto di esso.

Prendiamo due condizioni di percorso: &quot;La persona è un VIP&quot; e &quot;La persona è un maschio&quot;. Se una persona soddisfa entrambe le condizioni, viene scelto il primo percorso perché è al di sopra del secondo. Per modificare questa priorità, sposta le attività in un ordine verticale diverso.

![Esempio di prioritizzazione del percorso che mostra la condizione di VIP al di sopra della condizione maschile](assets/journey48.png)

Puoi creare un altro percorso per i tipi di pubblico non idonei alle condizioni definite selezionando **[!UICONTROL Mostra percorso per casi diversi da quelli sopra]**.

>[!NOTE]
>
>Questa opzione non è disponibile in condizioni di suddivisione. [Ulteriori informazioni](#percentage_split)

La modalità semplice consente di eseguire query semplici basate su una combinazione di campi. Tutti i campi disponibili sono visualizzati a sinistra. Trascina i campi nell’area principale. Per combinare i diversi elementi, puoi unirli per creare diversi gruppi e/o livelli di gruppo. Puoi quindi selezionare un operatore logico per combinare elementi sullo stesso livello:

* **AND** - Intersezione di due criteri. Vengono presi in considerazione solo gli elementi che corrispondono a tutti i criteri.
* **OR** - Unione di due criteri. Vengono considerati gli elementi che corrispondono ad almeno uno dei due criteri.

![Editor espressioni semplici con campi trascinati e operatori logici](assets/journey64.png){width=80%}

Se utilizzi il [Servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"} per creare i tuoi tipi di pubblico, puoi sfruttarli nelle condizioni del percorso. Consulta [Utilizzare il pubblico in condizioni](#using-a-segment).

>[!NOTE]
>
>Non è possibile eseguire query sulle serie temporali (ad esempio un elenco di acquisti, clic sui messaggi passati) con l’editor semplice. A questo scopo, dovrai utilizzare l’editor avanzato. Consulta [questa pagina](expression/expressionadvanced.md).

Quando si verifica un errore in un’azione o in una condizione, il percorso di un singolo utente si interrompe. L&#39;unico modo per far sì che continui è selezionare la casella **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o errore]**. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md#paths)

Nell’editor semplice, trovi anche la categoria Proprietà Percorso, sotto le categorie evento e origine dati. Questa categoria contiene campi tecnici relativi al percorso per un determinato profilo. Si tratta delle informazioni che il sistema recupera dai percorsi in tempo reale, ad esempio l’ID percorso o specifici errori rilevati. [Ulteriori informazioni](expression/journey-properties.md)

## Condizione origine dati {#data_source_condition}

Utilizzare una **[!UICONTROL condizione origine dati]** per definire una condizione basata sui campi delle origini dati o degli eventi precedentemente posizionati nel percorso. Questo tipo di condizione viene definito con l’editor di espressioni. [Scopri come utilizzare l&#39;editor espressioni](expression/expressionadvanced.md)

Ad esempio, se esegui il targeting di un pubblico con attributi di arricchimento generati utilizzando un flusso di lavoro di composizione o un caricamento personalizzato (file CSV), puoi sfruttare questi attributi di arricchimento per creare la condizione.

>[!IMPORTANT]
>
>**Gestione di attributi mancanti o non acquisiti**
>
>Se nello schema del profilo è definito un campo schema ma non sono stati acquisiti dati per tale campo, Journey Optimizer e il profilo cliente in tempo reale sottostante interpretano il campo come `null`. Di conseguenza, le condizioni che verificano per `isEmpty()`, `isNull()` o funzioni simili restituiranno `true` anche se l&#39;attributo non è mai stato acquisito. Questo può causare un comportamento di percorso imprevisto se non si è consapevoli che il campo non contiene dati.
>
>Per evitare confusione, assicurati che gli attributi utilizzati nelle espressioni di condizione siano stati acquisiti con i dati effettivi prima che il profilo entri nel percorso. Puoi verificare i valori degli attributi nel [Profilo cliente in tempo reale](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"} per verificare se esistono dati per i campi utilizzati nelle tue condizioni.

Utilizzando l’editor di espressioni avanzate, puoi impostare condizioni più avanzate per la manipolazione delle raccolte o l’utilizzo di origini dati che richiedono il trasferimento di parametri. [Ulteriori informazioni](../datasource/external-data-sources.md)

![Condizione Data Source con editor di espressioni avanzate](assets/journey50.png){width=80%}

## Condizione data {#date_condition}

Ciò ti consente di definire un flusso diverso in base alla data. Ad esempio, se la persona entra nel passaggio durante il periodo &quot;vendite&quot;, gli invierai un messaggio specifico. Per il resto dell&#39;anno, invierai un altro messaggio.

>[!NOTE]
>
>Il fuso orario non è più specifico di una condizione ed è ora definito a livello di percorso nelle proprietà del percorso. [Ulteriori informazioni](../building-journeys/timezone-management.md)

![Configurazione condizione data con campi data di inizio e data di fine](assets/journey53.png)

## Suddivisione percentuale {#percentage_split}

Questa opzione consente di suddividere in modo casuale il pubblico per definire un’azione diversa per ciascun gruppo. Definisci il numero di divisioni e la partizione per ciascun percorso. Il calcolo della suddivisione è statistico in quanto il sistema non è in grado di prevedere quante persone scorreranno in questa attività del percorso. Di conseguenza, la suddivisione presenta un margine di errore molto basso. Questa funzione si basa su un [meccanismo casuale Java](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html){target="_blank"}.

In modalità di test, quando si raggiunge una suddivisione, viene sempre scelto il ramo superiore. Se vuoi che il test scelga un percorso diverso, puoi riorganizzare la posizione dei rami divisi. [Ulteriori informazioni](../building-journeys/testing-the-journey.md)

>[!NOTE]
>
>Non è presente alcun pulsante per aggiungere un percorso nella condizione di suddivisione percentuale. Il numero di percorsi dipende dal numero di divisioni. Nelle condizioni di [PROD143]e non è possibile aggiungere un percorso per altri casi in quanto non può verificarsi. Le persone andranno sempre in uno dei percorsi divisi.

![Configurazione con suddivisione percentuale con cursore che mostra la distribuzione del traffico](assets/journey52.png)

## Condizione temporale {#time_condition}

Utilizza una **[!UICONTROL Condizione temporale]** per eseguire azioni diverse in base all&#39;ora del giorno e/o al giorno della settimana. Ad esempio, puoi decidere di inviare notifiche push durante il giorno e e-mail di notte nei giorni feriali.

>[!NOTE]
>
>* Il fuso orario non è specifico di una condizione ed è definito a livello di percorso nelle proprietà del percorso. [Ulteriori informazioni](../building-journeys/timezone-management.md)
>
>* Per impostazione predefinita, la **[!UICONTROL condizione temporale]** è impostata per ora, da 00:00 a 12:00.

![Condizione temporale con intervallo di ore e selettori del giorno della settimana](assets/journey51.png)

Sono disponibili tre opzioni di filtro dell’ora:

* **Ora** - Consente di impostare una condizione in base all&#39;ora del giorno. Vengono quindi definiti gli orari di inizio e di fine. I singoli utenti immetteranno il percorso solo durante l&#39;intervallo di ore definito.
* **Giorno della settimana** - Consente di impostare una condizione in base al giorno della settimana. Selezionare quindi i giorni in cui si desidera che i singoli utenti immettano il percorso.
* **Giorno della settimana e ora** - Questa opzione combina le prime due opzioni.

## Limite del profilo {#profile_cap}

Utilizza questo tipo di condizione per impostare un numero massimo di profili per un percorso di percorso. Una volta raggiunto tale limite, i profili partecipanti seguono un percorso alternativo. In questo modo i percorsi non supereranno mai il limite definito.

>[!NOTE]
>
>È consigliabile definire un limite di profili di valore elevato. La precisione e la probabilità che una popolazione raggiunga il numero esatto del limite aumenta solo con l’aumento del limite. Per i numeri piccoli (ad esempio un limite di 50), i numeri non sempre corrispondono in quanto il limite potrebbe non essere raggiunto prima che i profili seguano un percorso alternativo.

<!--You can use this condition type to ramp up the volume of your deliveries. See this [use case](ramp-up-deliveries-uc.md).-->

Il limite predefinito è 1.000.

Il contatore si applica solo alla versione del percorso selezionata. Il contatore viene azzerato quando il percorso viene duplicato o viene creata una nuova versione. Dopo un ripristino, i profili in ingresso riprendono il percorso nominale fino al raggiungimento del limite del contatore.

Quando il limite del profilo è definito in un percorso ricorrente, il contatore non viene reimpostato dopo ogni ricorrenza.

Il percorso nominale ha sempre la priorità sul percorso alternativo, anche se si sposta il percorso alternativo al di sopra del percorso nominale nell&#39;area di lavoro del percorso.

Per i percorsi live, le soglie da considerare per garantire il raggiungimento del limite sono le seguenti:

* Per un tappo superiore a 10,000, il numero di profili distinti da iniettare deve essere almeno 1,3 volte il tappo.
* Per un cappuccio inferiore a 10,000, il numero di profili distinti da iniettare deve essere 1000 più il cappuccio.

Il limite del profilo non viene preso in considerazione nella modalità di test.

![Condizione limite profilo con campo di input limite profilo massimo](assets/profile-cap-condition.png)

## Utilizzare i tipi di pubblico nelle condizioni {#using-a-segment}

Questa sezione spiega come utilizzare un pubblico in una condizione di percorso. Per ulteriori informazioni sui tipi di pubblico e su come generarli, consulta [questa sezione](../audience/about-audiences.md).

Per utilizzare un pubblico in una condizione di percorso, effettua le seguenti operazioni:

1. Apri un percorso, rilascia un&#39;attività **[!UICONTROL Ottimizza]** e scegli la **[!UICONTROL condizione origine dati]**.

   ![Metodo condizione Data Source selezionato nel menu a discesa](assets/segment3.png)

1. Fai clic su **[!UICONTROL Aggiungi un percorso]** per ogni percorso aggiuntivo necessario. Per ogni percorso, fare clic sul campo **[!UICONTROL Espressione]**.

1. Sul lato sinistro, apri il nodo **[!UICONTROL Tipi di pubblico]**. Trascina e rilascia il pubblico da utilizzare per la condizione. Per impostazione predefinita, la condizione sul pubblico è true.

   ![Nodo tipi di pubblico nell&#39;editor espressioni per selezionare [!DNL Adobe Experience Platform] tipi di pubblico](assets/segment4.png){width=80%}

   >[!NOTE]
   >
   >Solo i singoli utenti con lo stato di partecipazione al pubblico **Realizzato** verranno considerati membri del pubblico. Per ulteriori informazioni su come valutare un pubblico, consulta la [documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

➡️ **Visualizza in pratica:** Scopri come utilizzare le condizioni dell&#39;ora e del giorno della settimana per [inviare e-mail solo nei giorni feriali](weekday-email-uc.md).

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come configurare le condizioni all&#39;interno dell&#39;attività Ottimizza in Journey Optimizer, che includono cinque tipi di condizioni, ovvero Data Source, Ora, Divisione percentuale, Data e Limite profilo, che indirizzano i profili a percorsi di percorso diversi in base a regole, ora o appartenenza al pubblico.

**Intenti:**
* Aggiungi una condizione a un percorso utilizzando l’attività Ottimizza e seleziona un metodo di condizione
* Creare più percorsi di diramazione e gestirne l’ordine di priorità nell’area di lavoro del percorso
* Configurare una condizione di Data Source utilizzando l’editor espressioni per valutare gli attributi di profilo o evento
* Impostare una condizione di tempo per instradare i profili in base all&#39;ora del giorno o al giorno della settimana
* Applica un limite di profili per limitare il numero di profili instradati verso un percorso specifico
* Utilizzare un controllo di appartenenza a un pubblico come condizione in un percorso di percorso

**Glossario:**
* **Ottimizza attività**: l&#39;attività di percorso corrente che sostituisce l&#39;attività Condizione precedente; tutta la logica di diramazione condizionale è ora configurata tramite il relativo elenco a discesa Metodo *(specifico per prodotto)*
* **Condizione origine dati**: metodo di condizione che valuta i campi dalle origini dati o dagli eventi di percorso utilizzando l&#39;editor espressioni *(specifico per prodotto)*
* **Divisione percentuale**: metodo di condizione che distribuisce in modo casuale i profili tra percorsi utilizzando un meccanismo casuale Java statistico *(specifico per prodotto)*
* **Limite del profilo**: metodo di condizione che indirizza i profili a un percorso alternativo una volta raggiunto il conteggio massimo definito nel percorso nominale *(specifico per prodotto)*
* **Percorso nominale**: il percorso del percorso primario associato a una condizione di limite del profilo. Ha sempre la priorità sul percorso alternativo *(specifico per prodotto)*

**Guardrail:**
* La valutazione della condizione non riesce per i profili con più di due identità multi-dispositivo nell’archivio profili
* I campi dello schema senza dati acquisiti vengono interpretati come null; isEmpty() e isNull() restituiscono true per tali campi
* Il fuso orario è definito a livello di percorso, non a livello di singola condizione
* L’opzione &quot;Mostra percorso per altri casi&quot; non è disponibile in Condizioni di suddivisione percentuale
* Il valore predefinito del limite del profilo è 1.000; il contatore viene ripristinato alla duplicazione del percorso o alla creazione di una nuova versione, ma non tra due ricorrenze
* Per tappi superiori a 10,000, iniettare almeno 1,3 volte il cappuccio; per tappi inferiori a 10,000, iniettare almeno 1,000 più il cappuccio
* Il limite del profilo non viene applicato in modalità di test; in modalità di test, il ramo superiore viene sempre scelto per la suddivisione percentuale

**Terminologia:**
* Nome canonico: Conditions — Acronimo: none — Variants: condition activity, condition method, condition branching condizionale
* Sinonimi: &quot;Ottimizza attività (metodo condizione)&quot; = &quot;attività condizione precedente&quot;
* Non confondere: &quot;Divisione percentuale&quot; ≠ &quot;Limite profilo&quot; (la suddivisione percentuale distribuisce tutti i profili in modo statistico; il limite profilo interrompe il routing al percorso nominale dopo una soglia di conteggio)

**Domande frequenti:**
* **Q: l&#39;attività Condizione non è più disponibile nell&#39;interfaccia utente. Cosa l&#39;ha sostituita?** — L&#39;attività Condizione è stata sostituita dall&#39;attività Ottimizza. Seleziona &quot;Condizione&quot; dal menu a discesa Metodo per ottenere lo stesso comportamento. I percorsi esistenti con attività Condizione continuano a funzionare e ora vengono visualizzati con l’icona Ottimizza.
* **Q: quando più percorsi sono idonei per un profilo, quale percorso viene utilizzato?** — viene eseguito solo il primo percorso idoneo (più alto nell&#39;area di lavoro); è possibile ridefinire la priorità riordinando i percorsi in verticale.
* **Q: perché la condizione isEmpty() restituisce in modo imprevisto true?** — Se il campo dello schema esiste ma non sono stati acquisiti dati per esso, Journey Optimizer lo interpreta come null e i valori isEmpty() e isNull() restituiscono true.
* **Q: il contatore del limite del profilo viene reimpostato in un percorso ricorrente?** — No, il contatore non viene reimpostato tra le ricorrenze, ma solo quando il percorso viene duplicato o viene creata una nuova versione.
* **Q: posso utilizzare un pubblico di Adobe Experience Platform come condizione?** — Sì, rilascia un’attività di ottimizzazione, seleziona &quot;Data source condition&quot;, aggiungi un percorso e trascina il pubblico dal nodo Audiences nell’editor di espressioni.

+++
