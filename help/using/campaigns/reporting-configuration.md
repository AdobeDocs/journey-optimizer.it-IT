---
title: Configurazione del reporting
description: Scopri come impostare l’origine dati per la generazione di rapporti
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---

# Configurazione del reporting {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Imposta set di dati per il reporting"
>abstract="La configurazione di reporting ti consente di definire una connessione a un sistema per recuperare informazioni personalizzate aggiuntive da utilizzare nei rapporti. Deve essere eseguito da un utente tecnico."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Selezionare un set di dati"
>abstract="Puoi selezionare solo un set di dati di tipo evento che deve contenere almeno uno dei gruppi di campi supportati: experienceevent-web, experienceevent-application, experienceevent-commerce."

La configurazione dell’origine dati consente di definire una connessione a un sistema per recuperare informazioni aggiuntive, le quali verranno utilizzate nei rapporti.

>[!NOTE]
>
>La configurazione dell’origine dati viene sempre eseguita da un utente tecnico. <!--Rights?-->

Per questa configurazione, devi aggiungere uno o più set di dati contenenti gli attributi che desideri utilizzare per i rapporti. Per farlo, segui la procedura indicata di seguito.

>[!CAUTION]
>
>Prima di poter aggiungere un set di dati alla configurazione di reporting, devi crearlo. Scopri come fare nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=it#create){target=&quot;_blank&quot;}.
>
>È possibile aggiungere solo set di dati di tipo evento, che devono contenere almeno uno dei [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group)supportati {target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Ad esempio, se desideri conoscere l’impatto di una campagna e-mail sui dati di commerce, ad esempio acquisti o ordini, devi creare un set di dati evento esperienza con il gruppo di campi **experienceevent-commerce**. Allo stesso modo, se desideri creare rapporti sulle interazioni mobili, devi creare un set di dati evento esperienza con gruppo di campi **experienceevent-application**. <!--If you want to report on web interactions then you need to include the web field group.--> Puoi aggiungere questi gruppi di campi a uno o più schemi che verranno utilizzati in un set di dati o in set di dati diversi.

>[!NOTE]
>
>Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella [Documentazione di panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}.

1. Dal menu **[!UICONTROL ADMINISTRATION]**, seleziona **[!UICONTROL Configurations]**. Dalla sezione **[!UICONTROL Reporting]**, fai clic su **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   Viene visualizzato l’elenco dei set di dati già aggiunti.

1. Dalla scheda **[!UICONTROL Dataset]**, fai clic su **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Se selezioni la scheda **[!UICONTROL System dataset]**, vengono visualizzati solo i set di dati creati dal sistema. Non potrai aggiungere altri set di dati.

1. Dall’elenco a discesa **[!UICONTROL Dataset]**, seleziona il set di dati da utilizzare per i rapporti.

   >[!CAUTION]
   >
   >Puoi selezionare solo un set di dati di tipo evento, che deve contenere almeno uno dei [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group) supportato{target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**. Se selezioni un set di dati che non corrisponde a tali criteri, non potrai salvare le modifiche.

   ![](assets/reporting-config-datasets.png)

   Per ulteriori informazioni sui set di dati, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=it){target=&quot;_blank&quot;}.

1. Dall’elenco a discesa **[!UICONTROL Profile ID]**, seleziona l’attributo del campo set di dati che verrà utilizzato per identificare ogni profilo nei rapporti.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Vengono visualizzati solo gli ID disponibili per i rapporti.

1. L’opzione **[!UICONTROL Use Primary ID namespace]** è attivata per impostazione predefinita. Se il **[!UICONTROL Profile ID]** selezionato è **[!UICONTROL Identity Map]**, puoi disattivare questa opzione e scegliere un altro spazio dei nomi dall’elenco a discesa visualizzato.

   ![](assets/reporting-config-namespace.png)

   Per ulteriori informazioni sugli spazi dei nomi, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=it){target=&quot;_blank&quot;}.

1. Salva le modifiche per aggiungere il set di dati selezionato all’elenco di configurazione del reporting.

   >[!CAUTION]
   >
   >Se hai selezionato un set di dati che non è di tipo evento, non potrai procedere.

Durante la creazione dei rapporti delle consegne, ora puoi utilizzare i dati di questo set di dati per recuperare informazioni personalizzate aggiuntive e perfezionare meglio i rapporti. [Ulteriori informazioni](content-experiment.md#objectives-global)

>[!NOTE]
>
>Se aggiungi più set di dati, tutti i dati provenienti da tutti i set di dati saranno disponibili per il reporting.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
