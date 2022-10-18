---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare Customer Journey Analytics
description: Guida introduttiva a Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 8%

---

# Utilizzare [!DNL Customer Journey Analytics] {#cja-ajo}

![](assets/cja.png)
[!DNL Journey Optimizer] integrazione con [!DNL Customer Journey Analytics] fornisce una visualizzazione olistica di tutti i tuoi percorsi con distribuzione automatizzata dei rapporti e visualizzazioni personalizzate dei dati.

Dopo aver creato il percorso in [!DNL Journey Optimizer], puoi importare i dati dei clienti in [!DNL Customer Journey Analytics] per avviare i rapporti e comprendere l&#39;impatto di ogni interazione che un cliente ha con i tuoi percorsi.

➡️ [Scopri Customer Journey Analytics](https://docs.adobe.com/content/help/it-IT/experience-cloud/user-guides/home.translate.html){target=&quot;_blank&quot;}

Prima di utilizzare [!DNL Customer Journey Analytics] per i percorsi, devi prima configurare questa integrazione:

1. [Creare una connessione](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=it) in [!DNL Customer Journey Analytics] con **[!UICONTROL Set di dati]** desideri inviare a Platform.

   I seguenti [!DNL Journey Optimizer] può essere configurato:
   * [Evento passaggio percorso](../start/datasets-query-examples.md#journey-step-event): ti consente di vedere chi entra nei tuoi percorsi e quanto lontano arrivano.
   * [Feed di dati di feedback/tracciamento dei messaggi](../start/datasets-query-examples.md#message-feedback-event-dataset): consente di visualizzare le informazioni sulla consegna dei messaggi inviati tramite [!DNL Journey Optimizer].
   * [Set di dati di entità e Percorso](../start/datasets-query-examples.md#entity-dataset): consente di cercare i nomi descrittivi e di utilizzarli nei rapporti.

1. [Creare una visualizzazione dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=it) per configurare le dimensioni e le metriche che desideri utilizzare per il rapporto.

   Puoi creare metriche specifiche per Journey Optimizer per riflettere meglio i dati dei tuoi percorsi. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


Utilizzo [!DNL Journey Optimizer] con [!DNL Customer Journey Analytics] potrebbe causare alcune discrepanze nei dati di reporting causati da:

* **Entrambi [!DNL Journey Optimizer] e [!DNL Customer Journey Analytics] sincronizza i dati da Azure Data Lake Storage (ADLS) per i rapporti.**

   Il tempo di elaborazione dei dati in arrivo può essere leggermente diverso tra i prodotti. Per questo motivo, i dati potrebbero non corrispondere quando si visualizzano i rapporti da una data specifica al giorno corrente. Per ridurre la discrepanza, utilizza intervalli di date esclusi il giorno corrente.

* **In [!DNL Journey Optimizer] nei rapporti, la metrica Sent include anche la metrica Retry (Nuovo tentativo).**

   **[!UICONTROL Nuovi tentativi]** non sarà incluso in **[!UICONTROL Inviato]** metrica in [!DNL Customer Journey Analytics]. Questo causerà [!DNL Customer Journey Analytics] **[!UICONTROL Inviato]** metriche per mostrare valori inferiori a [!DNL Journey Optimizer]. Tuttavia, i dati dei nuovi tentativi vengono convertiti in **[!UICONTROL Messaggi inviati]** o **[!UICONTROL Rimbalzi]** metrica.
Per ridurre la discrepanza, utilizza intervalli di date di una settimana fa o anche più tardi.

* **I rapporti vengono serviti da un’origine dati diversa.**

   Questo potrebbe causare discrepanze di dati tra l’1-2% tra i prodotti.
