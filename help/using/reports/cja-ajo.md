---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare Customer Journey Analytics
description: Introduzione a Customer Journey Analytics
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 2%

---

# Configura manualmente [!DNL Customer Journey Analytics] {#cja-ajo}

L&#39;integrazione di [!DNL Journey Optimizer] con [!DNL Customer Journey Analytics] offre una visualizzazione olistica di tutti i tuoi percorsi con la distribuzione automatizzata dei rapporti e visualizzazioni personalizzate dei dati.

La sezione seguente illustra come sfruttare manualmente i dati generati da Journey Optimizer per un’analisi approfondita all’interno di Customer Journey Analytics. Tieni presente che questa integrazione può essere impostata automaticamente. [Ulteriori informazioni](report-gs-cja.md)

![](assets/cja.png)

Dopo aver creato il percorso in [!DNL Journey Optimizer], puoi importare i dati del cliente in [!DNL Customer Journey Analytics] per avviare i rapporti e comprendere l&#39;impatto di ogni interazione di un cliente con i tuoi percorsi.

➡️ [Individua Customer Journey Analytics](https://experienceleague.adobe.com/it/docs/analytics-platform/using/integrations/ajo#manually-configure-a-data-view-to-be-used-with-journey-optimizer){target="_blank"}

>[!NOTE]
>
>Oltre a questa integrazione, puoi anche esportare il contenuto dei set di dati di Adobe Journey Optimizer in posizioni di archiviazione cloud e utilizzare queste informazioni a scopo di reporting o analisi. [Scopri come esportare i set di dati nei percorsi di archiviazione cloud](../data/export-datasets.md)
>

Prima di utilizzare [!DNL Customer Journey Analytics] per i percorsi, è necessario configurare questa integrazione:

1. [Crea una connessione](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=it) in [!DNL Customer Journey Analytics] con il **[!UICONTROL Set di dati]** che desideri inviare a Adobe Experience Platform.

   È possibile configurare [!DNL Journey Optimizer]:
   * [Evento passaggio Percorso](../data/datasets-query-examples.md#journey-step-event): consente di visualizzare chi entra nei percorsi e fino a che punto arrivano.
   * [Set di dati di feedback/tracciamento dei messaggi](../data/datasets-query-examples.md#message-feedback-event-dataset): ti consente di visualizzare le informazioni di recapito dei messaggi inviati tramite [!DNL Journey Optimizer].
   * [Set di dati di entità e Percorso](../data/datasets-query-examples.md#entity-dataset): consente di eseguire ricerche in nomi descrittivi e di utilizzarli nei rapporti.

1. [Crea una visualizzazione dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=it) per configurare le dimensioni e le metriche da utilizzare per il report.

   Puoi creare metriche specifiche per Journey Optimizer per riflettere meglio i dati dei tuoi percorsi. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html?lang=it#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

L&#39;utilizzo di [!DNL Journey Optimizer] con [!DNL Customer Journey Analytics] potrebbe causare discrepanze nei dati di reporting causate da:

* **Sia [!DNL Journey Optimizer] che [!DNL Customer Journey Analytics] sincronizzano i dati da Azure Data Lake Storage (ADLS) per il reporting.**

  Il tempo di elaborazione dei dati in arrivo può variare leggermente da un prodotto all’altro. Per questo motivo, i dati potrebbero non corrispondere quando si visualizzano rapporti da una data specificata al giorno corrente. Per ridurre le discrepanze, utilizza intervalli di date che escludono il giorno corrente.

* **Nei report [!DNL Journey Optimizer], la metrica Inviata include anche la metrica Riprova.**

  **[!UICONTROL Nuovi tentativi]** non saranno inclusi nella metrica **[!UICONTROL Inviato]** in [!DNL Customer Journey Analytics]. In questo modo [!DNL Customer Journey Analytics] **[!UICONTROL Inviato]** le metriche mostreranno valori inferiori a [!DNL Journey Optimizer]. Tuttavia, i dati dei tentativi vengono convertiti nella metrica **[!UICONTROL Messaggi inviati correttamente]** o **[!UICONTROL Mancati recapiti]**.
Per ridurre le discrepanze, utilizza intervalli di date da una settimana fa o anche più tardi.

* **I report vengono gestiti da un&#39;origine dati diversa.**

  Ciò potrebbe causare discrepanze di dati tra l’1% e il 2% tra i prodotti.
