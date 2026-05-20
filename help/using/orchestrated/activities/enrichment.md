---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Arricchimento
description: Scopri come utilizzare l’attività Arricchimento
exl-id: 8a0aeae8-f4f2-4f1d-9b89-28ce573fadfd
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/Q7lT1NR61ALn475i9akX7z80pybh93kbx06Gc8TcCuI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126
source-git-commit: 71bcca11ff671594c6883b5675bea20cadc2fa53
workflow-type: tm+mt
source-wordcount: 844
ht-degree: 64%

---

# Arricchimento {#enrichment}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment"
>title="Attività Arricchimento"
>abstract="L’attività di **Arricchimento** consente di migliorare i dati mirati con informazioni aggiuntive provenienti dal database. Viene comunemente utilizzata in una campagna dopo le attività di segmentazione."

L’attività **[!UICONTROL Arricchimento]** è un’attività **[!UICONTROL targeting]** che consente di migliorare i dati del pubblico con attributi aggiuntivi.

Puoi sfruttare queste informazioni per segmentare il pubblico in modo più preciso, in base a comportamenti, preferenze o esigenze, e per creare messaggi personalizzati che si colleghino meglio con ciascun profilo.

## Aggiungere un’attività Arricchimento {#enrichment-configuration}

>[!CONTEXTUALHELP]
>id="ajo_targetdata_personalization_enrichmentdata"
>title="Dati di arricchimento"
>abstract="Seleziona i dati da utilizzare per arricchire la campagna orchestrata. Puoi selezionare due tipi di dati di arricchimento: un attributo di arricchimento singolo dalla dimensione di destinazione oppure un collegamento di raccolta, ossia un collegamento con cardinalità 1-N tra più tabelle."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_data"
>title="Attività Arricchimento"
>abstract="Una volta aggiunti alla campagna orchestrata, i dati di arricchimento possono essere utilizzati nelle attività aggiunte dopo l’attività di Arricchimento per segmentare la clientela in gruppi distinti in base a comportamenti, preferenze ed esigenze, o per creare messaggi e campagne di marketing personalizzati che hanno più probabilità di suscitare l’interesse del pubblico target."

Per configurare l’attività **Arricchimento** segui questi passaggi:

1. Aggiungi un’attività **Arricchimento**.

1. Fai clic su **Aggiungi dati di arricchimento** e seleziona l’attributo da utilizzare per arricchire i dati.

   Puoi selezionare due tipi di dati di arricchimento: un attributo di arricchimento singolo dalla dimensione target, oppure un collegamento di raccolta. Ciascuno di questi tipi è descritto negli esempi seguenti:

   * [Attributo di arricchimento singolo](#single-attribute)
   * [Collegamento di raccolta](#collection-link)

   ![](../assets/enrichment-1.png)

1. Fare clic su **[!UICONTROL Aggiungi collegamento]** per creare un collegamento tra i dati della tabella di lavoro e Adobe Journey Optimizer. [Ulteriori informazioni](#create-links)

   Ad esempio, se carichi dati da un file contenente il livello di fedeltà del cliente e la data dell’ultimo acquisto, devi creare un collegamento alla tabella dei profili per arricchire i record dei destinatari con questi attributi e utilizzarli per la personalizzazione o il targeting.

   ![](../assets/enrichment-1.png)

## Creare collegamenti tra tabelle {#create-links}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_simplejoin"
>title="Definizione dei collegamenti"
>abstract="Crea un collegamento tra i dati della tabella di lavoro e Adobe Journey Optimizer. Ad esempio, se carichi i dati da un file che contiene il numero di account, il paese e l’e-mail dei destinatari, ora puoi creare un collegamento alla tabella dei paesi per aggiornare queste informazioni nei rispettivi profili."

Utilizzare la sezione **[!UICONTROL Definizione collegamento]** per definire una relazione tra la tabella di lavoro e un&#39;altra origine dati. Ad esempio, se importi un file contenente il livello di fedeltà del cliente e la data dell’ultimo acquisto, puoi creare un collegamento alla tabella dei profili per rendere tali attributi disponibili per la personalizzazione e il targeting.

Per creare un collegamento:

1. Nella sezione **[!UICONTROL Definizione collegamento]**, fare clic su **[!UICONTROL Aggiungi collegamento]**.

   ![](../assets/enrichment-1.png)

1. Dall&#39;elenco a discesa **[!UICONTROL Tipo di relazione]**, selezionare il tipo di relazione tra il set principale e i dati collegati:

   * Collegamento semplice con cardinalità **[!UICONTROL 1]**: ogni record nel set principale viene mappato esattamente su un record nei dati collegati.
   * Collegamento semplice **[!UICONTROL 0 o 1 cardinalità]**: ogni record nel set principale è associato a zero o a un record nei dati collegati.
   * **[!UICONTROL N collegamento raccolta di cardinalità]**: ogni record nel set principale può essere mappato su più record nei dati collegati.

   ![](../assets/enrichment-8.png)

1. Selezionare la destinazione a cui collegare il set principale:

   * **[!UICONTROL Schema del database]**: collega a una tabella esistente nel database. Selezionare la tabella dal campo **[!UICONTROL Schema di destinazione]**.
   * **[!UICONTROL Schema temporaneo]**: collegamento a dati in arrivo da una transizione di input. Seleziona la transizione pertinente dall’elenco.

1. Definisci le condizioni di unione utilizzate per far corrispondere i record tra il set principale e lo schema collegato:

   * **[!UICONTROL Unione semplice]**: corrisponde ai record di una coppia di attributi specifica. Fai clic su **[!UICONTROL Aggiungi join]**, quindi seleziona gli attributi **[!UICONTROL Source]** e **[!UICONTROL Destination]** da utilizzare come criteri di corrispondenza.
   * **[!UICONTROL Iscrizione avanzata]**: crea una logica di corrispondenza personalizzata utilizzando il generatore di regole. Fare clic su **[!UICONTROL Crea condizione]** per iniziare.

## Esempi {#example}

### Attributo di arricchimento singolo {#single-attribute}

In questo esempio, arricchisci il pubblico con un singolo attributo, ad esempio la data di nascita, dalla dimensione targeting corrente.

Per eseguire questa operazione:

1. Fai clic su **[!UICONTROL Aggiungi dati di arricchimento]**.

1. Seleziona un campo semplice, ad esempio **[!UICONTROL Data di nascita]**, dalla dimensione corrente.

   ![](../assets/enrichment-2.png)

1. Fai clic su **[!UICONTROL Conferma]**.

### Collegamento di raccolta {#collection-link}

Questo caso d’uso arricchisce il pubblico con i dati di una tabella collegata. Ad esempio, desideri recuperare i tre acquisti più recenti di valore inferiore a 100 $.

A tal fine, configura l’arricchimento come segue:

* **Attributo di arricchimento**: **[!UICONTROL Prezzo]**

* **Numero di record da recuperare**: 3

* **Filtro**: includi solo gli acquisti in cui il **[!UICONTROL prezzo]** è inferiore a 100 $

#### Aggiungere l’attributo {#add-attribute}

Innanzitutto, seleziona il collegamento della raccolta che contiene i dati che desideri arricchire.

1. Fai clic su **[!UICONTROL Aggiungi dati di arricchimento]**.

1. Dalla tabella **[!UICONTROL Acquisti]**, seleziona il campo **[!UICONTROL Prezzo]**.

   ![](../assets/enrichment-2.png)

#### Definire le impostazioni di raccolta{#collection-settings}

Quindi, configura la raccolta dei dati e quante voci includere.

1. Nel menu a discesa **[!UICONTROL Seleziona la modalità di raccolta dei dati]**, scegli **[!UICONTROL Raccolta dati]**.

   ![](../assets/enrichment-4.png)

1. Nel campo **[!UICONTROL Righe da recuperare (Colonne da creare)]**, immetti `3`.

1. Per eseguire un’aggregazione (ad esempio, importo medio di acquisto), seleziona **[!UICONTROL Dati aggregati]**, quindi scegli **[!UICONTROL Media]** dal menu a discesa **[!UICONTROL Funzione di aggregazione]**.

   ![](../assets/enrichment-5.png)

1. Utilizza i campi **[!UICONTROL Etichetta]** e **[!UICONTROL Alias]** per facilitare l’identificazione degli attributi arricchiti nelle attività successive.

#### Definire i filtri{#collection-filters}

Infine, applica i filtri per garantire che siano inclusi solo i record rilevanti:

1. Fai clic su **[!UICONTROL Crea filtri]**.

1. Aggiungi queste due condizioni:

   * Il **[!UICONTROL prezzo]** esiste (per escludere i valori NULL)

   * Il **[!UICONTROL prezzo]** è inferiore a 100

   ![](../assets/enrichment-6.png)

1. Fai clic su **[!UICONTROL Conferma]**.


<!--
#### Define the sorting{#collection-sorting}

We now need to apply sorting in order to retrieve the three **latest** purchases.

1. Activate the **Enable sorting** option.
1. Click inside the **Attribute** field.
1. Select the **Order date** field.
1. Click **Confirm**. 
1. Select **Descending** from the **Sort** drop-down.

![](../assets/workflow-enrichment7bis.png)


## Data reconciliation {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_reconciliation"
>title="Reconciliation"
>abstract="The **Enrichment** activity can be used to reconcile data from the Journey Optimizer schema with data from another schema, or with data coming from a temporary schema such as data uploaded using a Load file activity. This type of link defines a reconciliation towards a unique record. Journey Optimizer creates a link to a target table by adding a foreign key in it for storing a reference to the unique record."

The **Enrichment** activity can be used to reconcile data from the the Campaign database schema with data from another schema, or with data coming from a temporary schema such as data uploaded using a Load file activity. This type of link defines a reconciliation towards a unique record. Journey Optimizer creates a link to a target table by adding a foreign key in it for storing a reference to the unique record.

For example, you can use this option to reconcile a profile's country, specified in an uploaded file, with one of the countries available in the dedicated table of the Campaign database. 

Follow the steps to configure an **Enrichment** activity with a reconciliation link: 

1. Click the **Add link** button in the **Reconciliation** section.
1. Identify the data you want to create a reconciliation link with.

    * To create a reconciliation link with data from the Campaign database, select **Database schema** and choose the schema where the target is stored. 
    * To create a reconciliation link with data coming from the input transition, select **Temporary schema** and choose the Orchestrated campaign transition where the target data is stored. 

1. The **Label** and **Name** fields are automatically populated based on the selected target schema. You can change their values if necessary.

1. In the **Reconciliation criteria** section, specify how you want to reconcile data from the source and destination tables:

    * **Simple join**: Reconcile a specific field from the source table with another field in the destination table. To do this, click the **Add join** button and specify the **Source** and **Destination** fields to use for the reconciliation.

        >[!NOTE]
        >
        >You can use one or more **Simple join** criteria, in which case they must all be verified so that the data can be linked together.

    * **Advanced join**: Use the rule builder to configure the reconciliation criteria. To do this, click the **Create condition** button then define your reconciliation criteria by building your own rule using AND and OR operations.

The example below shows an Orchestrated campaign configured to create a link between Journey Optimizer profiles table and a temporary table generated a **Load file** activity. In this example, the **Enrichment** activity reconciliates both tables using the email address as reconciliation criteria.

![](../assets/enrichment-reconciliation.png)

### Enrichment with linked data {#link-example}

The example below shows an Orchestrated campaign configured to create a link between two transitions. The first transitions targets profile data using a **Query** activity, while the second transition includes purchase data stored into a file loaded through a Load file activity.

![](../assets/enrichment-uc-link.png)

* The first **Enrichment** activity links the primary set (data from the **Query** activity) with the schema from the **Load file** activity. This allows us to match each profile targeted by the query with the corresponding purchase data.

    ![](../assets/enrichment-uc-link-purchases.png)

* A second **Enrichment** activity is added in order to enrich data from the Orchestrated campaign table with the purchase data coming from the **Load file** activity. This allows us to use those data in further activities, for example, to personalize messages sent to the customers with information on their purchase.

    ![](../assets/enrichment-uc-link-data.png)

## Add offers {#add-offers}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_offer_proposition"
>title="Offer proposition"
>abstract="The Enrichment activity allows you to add offers for each profile."

The **[!UICONTROL Enrichment]** activity allows you to add offers for each profile.

To do so, follow the steps to configure an **[!UICONTROL Enrichment]** activity with an offer: 

1. In the **[!UICONTROL Enrichment]** activity, at the **[!UICONTROL Offer proposition]** section, click on the **[!UICONTROL Add offer]** button

    ![](../assets/enrichment-addoffer.png)

1. You have two choices for the offer selection :

    * **[!UICONTROL Search for the best offer in category]** : check this option and specify the offer engine call parameters (offer space, category or theme(s), contact date, number of offers to keep). The engine will calculate the best offer(s) to add according to these parameters. We recommend completing either the Category or the Theme field, rather than both at the same time.

        ![](../assets/enrichment-bestoffer.png)

    * **[!UICONTROL A predefined offer]** : check this option and specify an offer space, a specific offer, and a contact date to directly configure the offer that you would like to add, without calling the offer engine.

        ![](../assets/enrichment-predefinedoffer.png)

1. After selecting your offer, click on **[!UICONTROL Confirm]** button.

You can now use the offer in the delivery activity.



### Using the offers from Enrichment activity

Within an Orchestrated campaign, if you want to use the offers you get from an enrichment activity in your delivery, follow the steps below:

1. Open the delivery activity and go in the content edition. Click on **[!UICONTROL Offers settings]** button and select in the drop-down list the **[!UICONTROL Offers space]** corresponding to your offer. 
If you want to to view only offers from the enrichment activity, set the number of **[!UICONTROL Propositions]** to 0, and save the modifications.

    ![](../assets/offers-settings.png) 

1. In the Email Designer, when adding a personalization with offers, click on the **[!UICONTROL Propositions]** icon, it will display the offer(s) you get from the **[!UICONTROL Enrichment]** activity. Open the offer you want to choose by clicking on it.

    ![](../assets/offers-propositions.png) 

    Go in **[!UICONTROL Rendering functions]** and choose **[!UICONTROL HTML rendering]** or **[!UICONTROL Text rendering]** according to your needs.

    ![](../assets/offers-rendering.png) 

>[!NOTE]
>
>If you choose to have more than one offer in the **[!UICONTROL Enrichment]** activity at the **[!UICONTROL Number of offers to keep]** option, all the offers are displayed when clicking on the **[!UICONTROL Propositions]** icon.
-->