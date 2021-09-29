---
product: experience platform
solution: Experience Platform
title: Creare strategie di classificazione
description: Scopri come creare strategie di classificazione in Adobe Experience Platform.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 7%

---

# Classificazioni AI {#ai-rankings}

## Guida introduttiva alle classificazioni AI

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can use an trained model system that ranks offers to display for a given profile.

>[!CAUTION]
>
>L’utilizzo della classificazione basata su IA è attualmente disponibile in accesso anticipato solo per determinati utenti.

Questa funzione ti consente di creare diverse **strategie di classificazione** in base ai tuoi obiettivi aziendali. Utilizzando queste diverse strategie basate su obiettivi in una decisione (precedentemente nota come attività di offerta), il sistema di modelli addestrati ti aiuterà a capire come le diverse strategie di classificazione influiscono sui tuoi obiettivi.

Ad esempio, puoi selezionare una strategia di classificazione per il canale e-mail e un’altra per il canale push. Per ogni canale, il sistema di modelli addestrati sfrutterà più punti di dati per determinare quale offerta deve essere presentata per prima per un determinato posizionamento, invece di prendere in considerazione i punteggi di priorità delle offerte o una formula di classificazione [](create-ranking-formulas.md).

<!--This feature is not enabled by default. To be able to use it, reach out to your Adobe contact.-->

Una volta creata una strategia di classificazione, assegnala a un posizionamento in una decisione. Ulteriori informazioni in [Configura la selezione delle offerte nelle decisioni](../offer-activities/configure-offer-selection.md).

## Creare una strategia di classificazione {#create-ranking-strategy}

Per creare una strategia di classificazione, segui i passaggi seguenti:

1. Accedi al menu **[!UICONTROL Components]**, quindi seleziona la scheda **[!UICONTROL AI rankings]** .

   ![](../../assets/ai-ranking-list.png)

   Vengono elencate tutte le strategie di classificazione create finora.

1. Fai clic sul pulsante **[!UICONTROL Create strategy]**.

1. Compila i campi seguenti:

   ![](../../assets/ai-ranking-fields.png)

   * **[!UICONTROL Name]**: Nome univoco da specificare.

   * **[!UICONTROL Model type]**: Attualmente l&#39;unico tipo di modello supportato è  **[!UICONTROL Auto-optimization]**.<!--More will be supported in the future so the drop-down list will be enabled.-->

   * **[!UICONTROL Optimization metric]**

      Questa opzione consente agli addetti al marketing di scegliere come generare e addestrare il modello di apprendimento automatico: in base alle offerte visualizzate, alle offerte su cui è stato fatto clic nell’e-mail e/o alle offerte su cui è stato fatto clic sul web.

      >[!NOTE]
      >
      >Se necessario, puoi selezionare tutti i tipi di metrica.

      Esistono due tipi di metriche di ottimizzazione:
      * **[!UICONTROL Impression]**: Al momento gli eventi di impression corrispondono a tutte le offerte visualizzate.
      * **[!UICONTROL Conversion]**: Gli eventi di conversione corrispondono a tutte le offerte che generano clic tramite e-mail o web.

      Tutti gli eventi di impression e/o conversione selezionati verranno acquisiti automaticamente utilizzando l’SDK per web o l’SDK mobile fornito. Per ulteriori informazioni, consulta [Panoramica dell&#39;SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en).

   * **[!UICONTROL Dataset ID]**: Per le conversioni, devi fornire un set di dati in cui vengono raccolti gli eventi selezionandolo dall’elenco a discesa. Scopri come creare tale set di dati in [questa sezione](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Nell’elenco a discesa vengono visualizzati solo i set di dati creati dagli schemi associati al gruppo di campi **[!UICONTROL Experience Event - Proposition Interactions]** (precedentemente denominato mixin).

1. Salva e attiva la strategia di classificazione.

   ![](../../assets/ai-ranking-save-activate.png)

È ora pronto per essere utilizzato in una decisione per classificare le offerte ammissibili per un posizionamento. [Ulteriori informazioni](../offer-activities/configure-offer-selection.md#use-ranking-strategy).<!--TBC?-->

## Creare un set di dati per raccogliere gli eventi {#create-dataset}

Devi creare un set di dati in cui verranno raccolti gli eventi di conversione. Inizia creando lo schema che verrà utilizzato nel set di dati:

1. Dal menu **[!UICONTROL Data Management]**, seleziona **[!UICONTROL Schema]**, vai alla scheda **[!UICONTROL Browse]** e fai clic su **[!UICONTROL Create schema]**.

   ![](../../assets/ai-ranking-create-schema.png)

1. Scegli **[!UICONTROL XDM ExperienceEvent]**.

   ![](../../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    Ulteriori informazioni sugli schemi XDM e sui gruppi di campi nella [documentazione panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).


1. Nel campo **[!UICONTROL Search]**, digita &quot;interazione di proposizione&quot; e seleziona il gruppo di campi **[!UICONTROL Experience Event - Proposition Interactions]**.

   ![](../../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    Allo schema che verrà utilizzato nel set di dati deve essere associato il gruppo di campi **[!UICONTROL Experience Event - Proposition Interactions]** . In caso contrario, non potrai utilizzarlo nella tua strategia di classificazione.

1. Fai clic su **[!UICONTROL Add field groups]**.

   ![](../../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Il gruppo di campi era precedentemente noto come mixin.


1. Digitare un nome e salvare lo schema.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    Ulteriori informazioni sulla creazione di schemi in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas).

Ora puoi creare un set di dati utilizzando questo schema. Per farlo, segui la procedura indicata di seguito:

1. Dal menu **[!UICONTROL Data Management]**, seleziona **[!UICONTROL Datasets]**, vai alla scheda **[!UICONTROL Browse]** e fai clic su **[!UICONTROL Create dataset]**.

   ![](../../assets/ai-ranking-create-dataset.png)

1. Seleziona **[!UICONTROL Create dataset from schema]**.

   ![](../../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleziona dall’elenco lo schema appena creato.

   ![](../../assets/ai-ranking-dataset-select-schema.png)

1. Fai clic su **[!UICONTROL Next]**.

1. Immetti un nome univoco per il set di dati nel campo **[!UICONTROL Name]** e fai clic su **[!UICONTROL Finish]**.

   ![](../../assets/ai-ranking-dataset-name.png)

Il set di dati è ora pronto per essere selezionato per raccogliere eventi di conversione quando [crei una strategia di classificazione](#create-ranking-strategy).

<!--## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision (previously known as offer activity). For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).-->

