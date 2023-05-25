---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il reporting di Journey Optimizer per la sperimentazione
description: Scopri come impostare l’origine dati per la generazione di rapporti
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: configurazione, sperimentazione, reporting, ottimizzatore
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 066bceb078f619e75e5776764f534619d5a0bd5a
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 33%

---

# Configurare la generazione di rapporti per la sperimentazione {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Imposta set di dati per il reporting"
>abstract="La configurazione di reporting consente di recuperare metriche aggiuntive che verranno utilizzate nella scheda Finalità dei rapporti della campagna. Deve essere eseguito da un utente tecnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selezionare un set di dati"
>abstract="Puoi selezionare solo un set di dati di tipo evento, che deve contenere almeno uno dei gruppi di campi supportati: dettagli applicazione, dettagli e-commerce, dettagli web."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

La configurazione dell’origine dati per la generazione di rapporti ti consente di recuperare metriche aggiuntive che verranno utilizzate nel **[!UICONTROL Obiettivi]** dei rapporti della campagna. [Ulteriori informazioni](content-experiment.md#objectives-global)

>[!NOTE]
>
>La configurazione del reporting deve essere eseguita da un utente tecnico. <!--Rights?-->

Per questa configurazione, devi aggiungere uno o più set di dati contenenti gli elementi aggiuntivi che desideri utilizzare per i rapporti. A questo scopo, segui la procedura [sotto](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Prerequisiti


Prima di poter aggiungere un set di dati alla configurazione di reporting, devi crearlo. Scopri come fare nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#create){target="_blank"}.

* Puoi aggiungere solo set di dati di tipo evento.

* Questi set di dati devono contenere almeno uno dei seguenti elementi [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"}: **Dettagli applicazione**, **Dettagli Commerce**, **Dettagli web**.

   >[!NOTE]
   >
   >Al momento sono supportati solo questi gruppi di campi.

   Ad esempio, se desideri conoscere l’impatto di una campagna e-mail sui dati di commerce, ad esempio acquisti o ordini, devi creare un set di dati evento esperienza con **Dettagli Commerce** gruppo di campi.

   Allo stesso modo, se desideri creare rapporti sulle interazioni mobili, devi creare un set di dati evento esperienza con **Dettagli applicazione** gruppo di campi.

   Vengono elencate le metriche corrispondenti a ciascun gruppo di campi [qui](#objective-list).

* Puoi aggiungere questi gruppi di campi a uno o più schemi che verranno utilizzati in uno o più set di dati.

>[!NOTE]
>
>Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella [Documentazione di panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

## Obiettivi corrispondenti a ciascun gruppo di campi {#objective-list}

La tabella seguente mostra quali metriche verranno aggiunte al **[!UICONTROL Obiettivi]** dei rapporti della campagna per ciascun gruppo di campi.

| Gruppo di campi | Obiettivi |
|--- |--- |
| Dettagli Commerce | Totale prezzo<br>Importo pagamento<br>(Univoco) Pagamenti<br>Aggiunte a elenco prodotti (univoche)<br>(Univoco) Aperture dell’elenco dei prodotti<br>Rimozione elenco prodotti (univoca)<br>(Univoco) Visualizzazioni elenco prodotti<br>(Univoco) Visualizzazioni prodotto<br>(Univoco) Acquisti<br>(Univoco) Salva Per Dopo<br>Totale prezzo prodotto<br>Quantità prodotto |
| Dettagli applicazione | (Univoco) Avvii di app<br>Primi avvii app<br>(Univoco) Installazioni app<br>Aggiornamenti app (univoci) |
| Dettagli web | (Univoco) Visualizzazioni pagina |

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

   Per ulteriori informazioni sui set di dati, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=it){target="_blank"}.

1. Dalla sezione **[!UICONTROL ID profilo]** dall’elenco a discesa, seleziona l’attributo del campo set di dati che verrà utilizzato per identificare ogni profilo nei rapporti.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Vengono visualizzati solo gli ID disponibili per i rapporti.

1. Il **[!UICONTROL Usa spazio dei nomi ID primario]** è attivata per impostazione predefinita. Se il valore selezionato **[!UICONTROL ID profilo]** è **[!UICONTROL Mappa identità]**, è possibile disattivare questa opzione e scegliere un altro spazio dei nomi dall’elenco a discesa visualizzato.

   ![](assets/reporting-config-namespace.png)

   Per ulteriori informazioni sugli spazi dei nomi, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=it){target="_blank"}.

1. Salva le modifiche per aggiungere il set di dati selezionato all’elenco di configurazione del reporting.

   >[!CAUTION]
   >
   >Se hai selezionato un set di dati che non è di tipo evento, non potrai procedere.

Durante la creazione dei rapporti della campagna, ora puoi vedere le metriche corrispondenti ai gruppi di campi utilizzati nei set di dati aggiunti. Vai a **[!UICONTROL Obiettivi]** e seleziona le metriche desiderate per ottimizzare i rapporti. [Ulteriori informazioni](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>Se aggiungi più set di dati, tutti i dati provenienti da tutti i set di dati saranno disponibili per il reporting.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
