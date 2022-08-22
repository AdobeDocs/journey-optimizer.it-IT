---
title: Configurazione del reporting
description: Scopri come impostare l’origine dati per la generazione di rapporti
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 11f7ce37dc1a99de4ed29fa7793f126e259f518d
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 5%

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

La configurazione dell’origine dati per la generazione di rapporti ti consente di definire una connessione a un sistema per recuperare informazioni aggiuntive che verranno utilizzate nei rapporti.

>[!NOTE]
>
>La configurazione dell’origine dati deve essere eseguita da un utente tecnico. <!--Rights?-->

Per questa configurazione, devi aggiungere uno o più set di dati contenenti gli attributi che desideri utilizzare per i rapporti. Per farlo, segui la procedura indicata di seguito.

>[!CAUTION]
>
>Prima di poter aggiungere un set di dati alla configurazione di reporting, devi crearlo. Scopri come in [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.
>
>È possibile aggiungere solo set di dati di tipo evento, che devono contenere almeno uno dei set di dati supportati [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Ad esempio, se desideri conoscere l’impatto di una campagna e-mail sui dati di e-mail, ad esempio acquisti o ordini, devi creare un set di dati evento esperienza con **experienceevent-commerce** gruppo di campi. Allo stesso modo, se desideri creare rapporti sulle interazioni mobili, devi creare un set di dati evento esperienza con **experienceevent-application** gruppo di campi. <!--If you want to report on web interactions then you need to include the web field group.--> Puoi aggiungere questi gruppi di campi a uno o più schemi che verranno utilizzati in un set di dati o in set di dati diversi.

>[!NOTE]
>
>Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella sezione [Panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}.

1. Dal menu **[!UICONTROL ADMINISTRATION]**, seleziona **[!UICONTROL Configurations]**. In  **[!UICONTROL Reporting]** sezione, fai clic su **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   Viene visualizzato l’elenco dei set di dati già aggiunti.

1. Dalla scheda **[!UICONTROL Dataset]**, fai clic su **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Se selezioni la **[!UICONTROL System dataset]** vengono visualizzati solo i set di dati creati dal sistema. Non potrai aggiungere altri set di dati.

1. Da **[!UICONTROL Dataset]** dall’elenco a discesa, seleziona il set di dati da utilizzare per i rapporti.

   >[!CAUTION]
   >
   >Puoi selezionare solo un set di dati di tipo evento, che deve contenere almeno uno dei [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**. Se selezioni un set di dati che non corrisponde a tali criteri, non potrai salvare le modifiche.

   ![](assets/reporting-config-datasets.png)

   Ulteriori informazioni sui set di dati in [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

1. Da **[!UICONTROL Profile ID]** elenco a discesa, seleziona l’attributo del campo set di dati che verrà utilizzato per identificare ogni profilo nei rapporti.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Vengono visualizzati solo gli ID disponibili per i rapporti.

1. La **[!UICONTROL Use Primary ID namespace]** è attivata per impostazione predefinita. Se selezionato **[!UICONTROL Profile ID]** è **[!UICONTROL Identity Map]**, puoi disattivare questa opzione e scegliere un altro namespace dall’elenco a discesa visualizzato.

   ![](assets/reporting-config-namespace.png)

   Ulteriori informazioni sugli spazi dei nomi in [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=it){target=&quot;_blank&quot;}.

1. Salva le modifiche per aggiungere il set di dati selezionato all’elenco di configurazione del reporting.

   >[!CAUTION]
   >
   >Se hai selezionato un set di dati che non è di tipo evento, non potrai procedere.

Durante la creazione dei rapporti delle consegne, ora puoi utilizzare i dati di questo set di dati per recuperare informazioni personalizzate aggiuntive e perfezionare meglio i rapporti. [Ulteriori informazioni](campaign-global-report.md#objectives-global)

>[!NOTE]
>
>Se aggiungi più set di dati, tutti i dati provenienti da tutti i set di dati saranno disponibili per la generazione di rapporti.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
