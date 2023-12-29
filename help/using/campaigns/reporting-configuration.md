---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il reporting di Journey Optimizer per la sperimentazione
description: Scopri come impostare l’origine dati per la generazione di rapporti
feature: Experimentation, Reporting
topic: Administration
role: Admin
level: Intermediate
keywords: configurazione, sperimentazione, reporting, ottimizzatore
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 1490ac2efd39c6bf9b6ca97e682750463e9f054d
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 29%

---

# Configurare la generazione di rapporti per gli esperimenti {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Imposta set di dati per il reporting"
>abstract="La configurazione del reporting consente di recuperare metriche aggiuntive che verranno utilizzate nei rapporti della campagna. Deve essere eseguito da un utente tecnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selezionare un set di dati"
>abstract="Puoi selezionare solo un set di dati di tipo evento, che deve contenere almeno uno dei gruppi di campi supportati: dettagli applicazione, dettagli e-commerce, dettagli web."

La configurazione dell’origine dati consente di definire una connessione a un sistema per recuperare informazioni aggiuntive, le quali verranno utilizzate nei rapporti.

<!--The reporting data source configuration allows you to retrieve additional metrics that will be used in the **[!UICONTROL Objectives]** tab of your campaign reports.-->

>[!NOTE]
>
>La configurazione del reporting deve essere eseguita da un utente tecnico. <!--Rights?-->

Per questa configurazione, devi aggiungere uno o più set di dati contenenti gli elementi aggiuntivi che desideri utilizzare per i rapporti. A questo scopo, segui la procedura [sotto](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Prerequisiti


Prima di poter aggiungere un set di dati alla configurazione di reporting, devi crearlo. Scopri come nella [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#create){target="_blank"}.

* Puoi aggiungere solo set di dati di tipo evento.

* Questi set di dati devono includere `Experience Event - Proposition Interactions` [gruppo di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"}.

* Questi set di dati possono contenere anche uno dei seguenti elementi [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"}: `Application Details`, `Commerce Details`, `Web Details`.

  >[!NOTE]
  >
  >Possono essere inclusi anche altri gruppi di campi, ma solo i gruppi di campi di cui sopra sono attualmente supportati nella generazione rapporti di Journey Optimizer.

  Ad esempio, se desideri conoscere l’impatto di una campagna e-mail sui dati di commerce, ad esempio acquisti o ordini, devi creare un set di dati evento esperienza con `Commerce Details` gruppo di campi.

  Allo stesso modo, se desideri creare rapporti sulle interazioni mobili, devi creare un set di dati evento esperienza con `Application Details` gruppo di campi.

  <!--The metrics corresponding to each field group are listed [here](#objective-list).-->

* Puoi aggiungere questi gruppi di campi a uno o più schemi che verranno utilizzati in uno o più set di dati.

>[!NOTE]
>
>Ulteriori informazioni sugli schemi e sui gruppi di campi XDM in [Documentazione di panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

<!--
## Objectives corresponding to each field group {#objective-list}

The table below shows which metrics will be added to the **[!UICONTROL Objectives]** tab of your campaign reports for each field group.

| Field group | Objectives |
|--- |--- |
| Commerce Details | Price Total<br>Payment Amount<br>(Unique) Checkouts<br>(Unique) Product List Adds<br>(Unique) Product List Opens<br>(Unique) Product List Removal<br>(Unique) Product List Views<br>(Unique) Product Views<br>(Unique) Purchases<br>(Unique) Save For Laters<br>Product Price Total<br>Product Quantity |
| Application Details | (Unique) App Launches<br>First App Launches<br>(Unique) App Installs<br>(Unique) App Upgrades |
| Web Details | (Unique) Page Views |
-->

## Aggiungere set di dati {#add-datasets}

1. Dalla sezione **[!UICONTROL AMMINISTRAZIONE]** menu, seleziona **[!UICONTROL Configurazioni]**. In  **[!UICONTROL Generazione rapporti]** , fare clic su **[!UICONTROL Gestisci]**.

   ![](assets/reporting-config-menu.png)

   Viene visualizzato l’elenco dei set di dati già aggiunti.

1. Dalla sezione **[!UICONTROL Set di dati]** , fare clic su **[!UICONTROL Aggiungi set di dati]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Se si seleziona la **[!UICONTROL Set di dati di sistema]** , vengono visualizzati solo i set di dati creati dal sistema. Non potrai aggiungere altri set di dati.

1. Dalla sezione **[!UICONTROL Set di dati]** dall’elenco a discesa, seleziona il set di dati da utilizzare per i rapporti.

   >[!CAUTION]
   >
   >Puoi selezionare solo un set di dati di tipo evento, che deve contenere almeno uno dei set di dati supportati [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"}: **Dettagli applicazione**, **Dettagli Commerce**, **Dettagli web**. Se selezioni un set di dati che non corrisponde a tali criteri, non potrai salvare le modifiche.

   ![](assets/reporting-config-datasets.png)

   Per ulteriori informazioni sui set di dati, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=it){target="_blank"}.

1. Dalla sezione **[!UICONTROL ID profilo]** dall’elenco a discesa, seleziona l’attributo del campo set di dati che verrà utilizzato per identificare ogni profilo nei rapporti.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Vengono visualizzati solo gli ID disponibili per i rapporti.

1. Il **[!UICONTROL Usa spazio dei nomi ID primario]** è attivata per impostazione predefinita. Se il valore selezionato **[!UICONTROL ID profilo]** è **[!UICONTROL Mappa identità]**, è possibile disattivare questa opzione e scegliere un altro spazio dei nomi dall’elenco a discesa visualizzato.

   ![](assets/reporting-config-namespace.png)

   Per ulteriori informazioni sugli spazi dei nomi, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=it){target="_blank"}.

1. Salva le modifiche per aggiungere il set di dati selezionato all’elenco di configurazione del reporting.

   >[!CAUTION]
   >
   >Se hai selezionato un set di dati che non è di tipo evento, non potrai procedere.

Tieni presente che per i canali web e in-app, è necessario assicurarsi che [set di dati](../data/get-started-datasets.md) configurata per la raccolta dati viene aggiunta anche a questa configurazione di reporting. In caso contrario, i dati web e in-app non verranno visualizzati nei rapporti dell’esperimento sui contenuti.

* Ulteriori informazioni sui prerequisiti dell’esperimento sui contenuti per il canale web in [questa sezione](../web/web-prerequisites.md#experiment-prerequisites).

* Ulteriori informazioni sulla configurazione del canale in-app in [questa sezione](../in-app/inapp-configuration.md).

<!--
When building your campaign reports, you can now see the metrics corresponding to the field groups used in the datasets you added. Go to the **[!UICONTROL Objectives]** tab and select the metrics of your choice to better fine-tune your reports. [Learn more](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>If you add several datasets, all data from all datasets will be available for reporting.


## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
