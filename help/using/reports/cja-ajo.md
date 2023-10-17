---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare Customer Journey Analytics
description: Introduzione al Customer Journey Analytics
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 11%

---

# Utilizzare [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] integrazione con [!DNL Customer Journey Analytics] offre una visualizzazione olistica di tutti i percorsi con distribuzione automatizzata dei rapporti e visualizzazioni personalizzate dei dati.

![](assets/cja.png)

Dopo aver creato il percorso in [!DNL Journey Optimizer], puoi importare i dati dei clienti in [!DNL Customer Journey Analytics] per avviare rapporti e capire l’impatto di ogni interazione di un cliente con i tuoi percorsi.

➡️ [Individua Customer Journey Analytics](https://docs.adobe.com/content/help/it-IT/experience-cloud/user-guides/home.translate.html){target="_blank"}

>[!NOTE]
>
>Oltre a questa integrazione, puoi anche esportare il contenuto dei set di dati di Adobe Journey Optimizer in posizioni di archiviazione cloud e utilizzare queste informazioni a scopo di reporting o analisi. [Scopri come esportare i set di dati nelle posizioni di archiviazione cloud](../data/export-datasets.md)
>
>La funzione di esportazione dei set di dati è attualmente in versione beta e disponibile per tutti gli utenti di Adobe Journey Optimizer. Collabora con il tuo rappresentante Adobe per accedere alle destinazioni se non hai già accesso.

Prima di utilizzare [!DNL Customer Journey Analytics] per i percorsi, devi prima configurare questa integrazione:

1. [Creare una connessione](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=it) in [!DNL Customer Journey Analytics] con **[!UICONTROL Set di dati]** desideri inviarli a Adobe Experience Platform.

   I seguenti elementi [!DNL Journey Optimizer] può essere configurato:
   * [Evento passaggio percorso](../data/datasets-query-examples.md#journey-step-event): consente di visualizzare chi entra nei percorsi e fino a che punto arrivano.
   * [Set di dati di feedback/tracciamento messaggi](../data/datasets-query-examples.md#message-feedback-event-dataset): ti consente di visualizzare le informazioni sulla consegna dei messaggi inviati tramite [!DNL Journey Optimizer].
   * [Set di dati di entità e Percorso](../data/datasets-query-examples.md#entity-dataset): consente di cercare nomi descrittivi e utilizzarli nei rapporti.

1. [Creare una visualizzazione dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=it) per configurare le dimensioni e le metriche da utilizzare per il rapporto.

   Puoi creare metriche specifiche per Journey Optimizer per riflettere meglio i dati dei tuoi percorsi. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

Utilizzo di [!DNL Journey Optimizer] con [!DNL Customer Journey Analytics] potrebbe causare discrepanze nei dati di reporting causate da:

* **Entrambi [!DNL Journey Optimizer] e [!DNL Customer Journey Analytics] sincronizza i dati da Azure Data Lake Storage (ADLS) per i rapporti.**

  Il tempo di elaborazione dei dati in arrivo può variare leggermente da un prodotto all’altro. Per questo motivo, i dati potrebbero non corrispondere quando si visualizzano rapporti da una data specificata al giorno corrente. Per ridurre le discrepanze, utilizza intervalli di date che escludono il giorno corrente.

* **In entrata [!DNL Journey Optimizer] rapporti, la metrica Inviata include anche la metrica Nuovi tentativi.**

  **[!UICONTROL Nuovi tentativi]** non sarà incluso in **[!UICONTROL Inviato]** metrica in [!DNL Customer Journey Analytics]. Questo causerà [!DNL Customer Journey Analytics] **[!UICONTROL Inviato]** metriche per mostrare valori inferiori a [!DNL Journey Optimizer]. Tuttavia, i dati dei nuovi tentativi vengono convertiti in **[!UICONTROL Messaggi inviati correttamente]** o **[!UICONTROL Mancati recapiti]** metrica.
Per ridurre le discrepanze, utilizza intervalli di date da una settimana fa o anche più tardi.

* **I rapporti vengono gestiti da un’origine dati diversa.**

  Ciò potrebbe causare discrepanze di dati tra l’1% e il 2% tra i prodotti.
