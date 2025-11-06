---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla composizione del pubblico
description: Ulteriori informazioni sulla composizione del pubblico
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: af71d24d-77eb-44df-8216-b0aeaf4c4fa4
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 50%

---

# Introduzione alla composizione del pubblico {#get-start-audience-composition}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_composition"
>title="Creare una composizione"
>abstract="Crea un flusso di lavoro di composizione per combinare i tipi di pubblico di Adobe Experience Platform esistenti in un’area di lavoro visiva e sfruttare le varie attività (divisione, esclusione...) per creare nuovi tipi di pubblico."

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Pubblicare il pubblico"
>abstract="Pubblica la composizione per salvare i segmenti di pubblico risultanti in Adobe Experience Platform."

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Attività Pubblico"
>abstract="L’attività Pubblico consente di includere nella composizione profili aggiuntivi appartenenti a un pubblico esistente."

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Tipi di unione"
>abstract="Specifica come devono essere uniti i profili dei tipi di pubblico selezionati."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Tipo di esclusione"
>abstract="Utilizza il tipo Escludi pubblico per escludere i profili appartenenti a un pubblico esistente. Il tipo Escludi con attributo consente di escludere i profili in base a un attributo specifico."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Attività di esclusione"
>abstract="L’attività di esclusione consente di escludere i profili dalla composizione selezionando un pubblico esistente o utilizzando una regola."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="Attività Arricchisci"
>abstract="Utilizza l’attività Enrich per arricchire il pubblico con attributi aggiuntivi provenienti dai set di dati di Adobe Experience Platform. Ad esempio, puoi aggiungere informazioni relative al prodotto acquistato come nome, prezzo o ID produttore e sfruttarle per personalizzare le consegne inviate al pubblico."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="Set di dati di arricchimento"
>abstract="Seleziona il set di dati di arricchimento contenente i dati che desideri associare al pubblico."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="Criteri di arricchimento"
>abstract="Seleziona i campi da utilizzare come chiave di riconciliazione tra il set di dati di origine, ovvero il pubblico, e il set di dati di arricchimento."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="Attributi di arricchimento"
>abstract="Seleziona uno o più attributi dal set di dati di arricchimento da associare al pubblico. Una volta pubblicata la composizione, questi attributi sono associati al pubblico e possono essere utilizzati nelle campagne Journey Optimizer per personalizzare le consegne."

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Attività Classificazione"
>abstract="L’attività Classificazione consente di classificare i profili in base a un attributo specifico e di includerli nella composizione. Ad esempio, puoi includere i 50 profili con la maggiore quantità di punti fedeltà."

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="Aggiungere un limite al profilo"
>abstract="Attiva questa opzione per specificare un numero massimo di profili da includere nella composizione."

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="Attività Dividi"
>abstract="L’attività Dividi consente di dividere la composizione in più percorsi. Quando pubblichi la composizione, viene salvato un pubblico per ogni percorso in Adobe Experience Platform."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="Tipo di divisione"
>abstract="Utilizza il tipo di divisione percentuale per dividere in modo casuale i profili in più percorsi. Il tipo di divisione per attributo consente invece di dividere i profili in base a un attributo specifico."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="Altri profili"
>abstract="Attiva questa opzione per creare un percorso aggiuntivo con i profili rimanenti che non corrispondono a nessuna delle condizioni specificate negli altri percorsi."

>[!BEGINSHADEBOX]

Questa documentazione fornisce informazioni dettagliate su come lavorare con la composizione del pubblico in Adobe Journey Optimizer. Se sei cliente solo del servizio Profilo cliente in tempo reale e non utilizzi Adobe Journey Optimizer, [fai clic qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=it){target="_blank"}.

>[!ENDSHADEBOX]

La composizione del pubblico consente di creare **flussi di lavoro di composizione**, in cui è possibile combinare il pubblico di Adobe Experience Platform esistente in un&#39;area di lavoro visiva e sfruttare varie attività (suddivisione, esclusione...) per creare nuovi tipi di pubblico.

Al termine, i **tipi di pubblico risultanti** vengono salvati nuovamente in Adobe Experience Platform insieme ai tipi di pubblico esistenti e possono essere utilizzati nelle campagne e nei percorsi Journey Optimizer per eseguire il targeting dei clienti. Scopri come eseguire il targeting dei tipi di pubblico in Journey Optimizer
![](assets/audiences-process.png)

>[!IMPORTANT]
>
>* L’utilizzo dei tipi di pubblico e degli attributi della composizione del pubblico non è attualmente disponibile con Healthcare Shield o Privacy and Security Shield.
>
>* Gli attributi di arricchimento non sono ancora integrati con il servizio di applicazione dei criteri. Pertanto, eventuali etichette di utilizzo dei dati applicate agli attributi di arricchimento non verranno applicate nelle campagne o nei percorsi Journey Optimizer.

La composizione del pubblico è accessibile dal menu **[!UICONTROL Tipi di pubblico]** di Adobe Journey Optimizer:

![](assets/audiences-browse.png)

* La scheda **[!UICONTROL Panoramica]** fornisce una dashboard dedicata con una metrica chiave relativa ai dati di pubblico dell’organizzazione. Per ulteriori informazioni, consulta la [Guida alle dashboard di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/segments.html?lang=it).

* La scheda **[!UICONTROL Sfoglia]** elenca tutti i tipi di pubblico esistenti memorizzati in Adobe Experience Platform.

* La scheda **[!UICONTROL Composizioni]** consente di creare flussi di lavoro di composizione in cui è possibile combinare e organizzare i tipi di pubblico per crearne di nuovi.

## Creare un flusso di lavoro di composizione {#create}

Per creare un flusso di lavoro di composizione, effettuate le seguenti operazioni:

1. Accedi al menu **[!UICONTROL Tipi di pubblico]** e seleziona **[!UICONTROL Crea pubblico]**.

1. Seleziona **[!UICONTROL Componi pubblico]**.

   ![](assets/audiences-create.png)

1. L’area di lavoro della composizione viene visualizzata con due attività predefinite:

   * **[!UICONTROL Pubblico]**: il punto iniziale della composizione. Questa attività ti consente di selezionare uno o più tipi di pubblico come base per il flusso di lavoro,

   * **[!UICONTROL Salva]**: ultimo passaggio della composizione. Questa attività ti consente di salvare il risultato del flusso di lavoro in un nuovo pubblico.

1. Aprite le proprietà di composizione per specificare un titolo e una descrizione.

   Se nelle proprietà non è definito alcun titolo, l&#39;etichetta della composizione viene impostata su &quot;Composizione&quot; seguita dalla data e dall&#39;ora di creazione.

   ![](assets/audiences-properties.png)

1. Configura la composizione aggiungendo tutte le attività necessarie tra le attività **[!UICONTROL Pubblico]** e **[!UICONTROL Salva]**. Per ulteriori informazioni su come creare una composizione, consulta la [documentazione sulla composizione del pubblico](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/ui/audience-composition).

   ![](assets/audiences-publish.png)

1. Quando la composizione è pronta, fai clic sul pulsante **[!UICONTROL Pubblica]** per pubblicare la composizione e salvare i tipi di pubblico risultanti in Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Puoi pubblicare fino a 10 composizioni in una determinata sandbox. Se hai raggiunto questa soglia, elimina una composizione per liberare spazio e pubblicarne una nuova.

   Se si verifica un errore durante la pubblicazione, vengono visualizzati avvisi con informazioni su come risolvere il problema.

   ![](assets/audiences-alerts.png)

1. La composizione viene pubblicata. I tipi di pubblico risultanti vengono salvati in Adobe Experience Platform e sono pronti per essere indirizzati in Journey Optimizer. [Scopri come indirizzare i tipi di pubblico in Journey Optimizer](../audience/about-audiences.md#segments-in-journey-optimizer)

>[!NOTE]
>
>I tipi di pubblico da **composizione del pubblico** vengono eseguiti ogni giorno, quindi potrebbe essere necessario attendere fino a 24 ore prima di utilizzarli in Journey Optimizer. Gli attributi arricchiti nei tipi di pubblico di composizione del pubblico sono aggiornati quanto l’ultima esecuzione della composizione, che può durare fino a 24 ore nel passato.

## Accedere alle composizioni {#access}

Tutte le composizioni create sono accessibili dalla scheda **[!UICONTROL Composizioni]**. Potete duplicare o eliminare una composizione esistente in qualsiasi momento utilizzando il pulsante con i puntini di sospensione nell&#39;elenco.

Le composizioni possono avere più stati:

* **[!UICONTROL Bozza]**: la composizione è in corso e non è stata pubblicata.
* **[!UICONTROL Pubblicato]**: la composizione è stata pubblicata, i tipi di pubblico risultanti sono stati salvati e sono disponibili per l&#39;utilizzo.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>La composizione del pubblico non è attualmente integrata con la funzionalità di ripristino della sandbox. Prima di avviare il ripristino di una sandbox, è necessario eliminare manualmente le composizioni per garantire che i dati del pubblico associato vengano eliminati correttamente. Informazioni dettagliate sono disponibili nella [Documentazione sulle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it#delete-audience-compositions) di Adobe Experience Platform
