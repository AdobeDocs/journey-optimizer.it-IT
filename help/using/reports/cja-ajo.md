---
title: Utilizzare il Customer Journey Analytics
description: Guida introduttiva a Customer Journey Analytics
feature: Overview
topic: Reporting
role: User
level: Beginner
source-git-commit: b7bda87c3e2d6e1841ca231aa4acc3a406655244
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Utilizzare [!DNL Customer Journey Analytics] {#cja-ajo}

![](assets/cja.png)

Dopo aver creato il percorso in [!DNL Journey Optimizer], puoi importare i dati dei clienti in [!DNL Customer Journey Analytics] per avviare i rapporti e comprendere l&#39;impatto di ogni interazione che un cliente ha con i tuoi percorsi.

➡️ [Scopri Customer Journey Analytics](https://docs.adobe.com/content/help/it-IT/experience-cloud/user-guides/home.translate.html){target=&quot;_blank&quot;}

Prima di utilizzare [!DNL Customer Journey Analytics] per i percorsi, devi prima configurare questa integrazione:

1. [Creare una connessione](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=it) in [!DNL Customer Journey Analytics] con **[!UICONTROL Set di dati]** desideri inviare a Platform.

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
