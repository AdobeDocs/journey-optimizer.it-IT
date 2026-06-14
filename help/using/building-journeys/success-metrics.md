---
solution: Journey Optimizer
product: journey optimizer
title: Pubblicare il percorso
description: Scopri come creare rapporti sulle metriche del percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: pubblicazione, percorso, live, validità, verifica
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/iHr0CFVSDz-4tOxNKyCyPZdwva3nfDyuU0Y5XHZEdjk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 623
ht-degree: 6%

---

# Configurare e tenere traccia della metriche del percorso {#success-metrics}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come configurare e assegnare le metriche di percorso per monitorare le prestazioni rispetto ai KPI e misurare l&#39;efficacia dei percorsi di clienti in tempo reale.

>[!ENDSHADEBOX]

Ottieni una chiara visibilità dell’efficacia dei percorsi dei clienti con le metriche di percorso. Questa funzione consente di monitorare le prestazioni rispetto a KPI definiti, scoprire informazioni approfondite sul funzionamento e identificare le aree da ottimizzare. Misurando l’impatto in tempo reale, puoi promuovere il miglioramento continuo e prendere decisioni basate sui dati che aumentano il coinvolgimento dei clienti.

## Prerequisiti {#prerequisites}

Prima di utilizzare le metriche di percorso, è necessario aggiungere un set di dati che includa `Commerce Details`, `Web` e `Mobile` [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"} in Configurazione > Generazione rapporti in [!DNL Adobe Experience Platform].

Questi gruppi di campi devono essere selezionati dalle opzioni incorporate, non dai gruppi personalizzati. Consulta la sezione [Aggiungere set di dati](../reports/reporting-configuration.md#add-datasets).

## Metriche disponibili {#metrics}

L&#39;elenco delle metriche varia a seconda dei [gruppi di campi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it#field-group){target="_blank"} inclusi nel set di dati.

Se il set di dati non è configurato, saranno disponibili solo le metriche seguenti: **[!UICONTROL Clic]**, **[!UICONTROL Clic univoco]**, **[!UICONTROL Frequenza clickthrough]** e **[!UICONTROL Frequenza aperture]**.

Tieni presente che con una licenza Customer Journey Analytics puoi creare metriche di successo personalizzate. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| Metriche | Gruppo di campi correlato |
|-|-|
| Clic | Nessun gruppo di campi richiesto |
| Clic univoci | Nessun gruppo di campi richiesto |
| Percentuale di clickthrough (CTR) | Nessun gruppo di campi richiesto |
| Percentuale di apertura click-through (CTOR) | Nessun gruppo di campi richiesto |
| Page Views | Gruppo di campi Web |
| Avvii app | Gruppo di campi mobile |
| Primi avvii app | Gruppo di campi mobile |
| Installazioni app | Gruppo di campi mobile |
| Aggiornamenti delle app | Gruppo di campi mobile |
| Acquisti | Gruppo di campi Dettagli Commerce |
| Pagamenti | Gruppo di campi Dettagli Commerce |
| Aggiunte al carrello | Gruppo di campi Dettagli Commerce |
| Aperture carrello | Gruppo di campi Dettagli Commerce |
| Visualizzazioni carrello | Gruppo di campi Dettagli Commerce |
| Rimozioni dal carrello | Gruppo di campi Dettagli Commerce |
| Visualizzazioni prodotto | Gruppo di campi Dettagli Commerce |
| Salva per dopo | Gruppo di campi Dettagli Commerce |

## Attribuzione {#attribution}

Ogni metrica viene fornita con una determinata attribuzione che determina quali punti di contatto o interazioni hanno contribuito a un risultato specifico.

* **Attribuzione delle metriche con licenza Journey Optimizer**:

  Solo con la licenza Journey Optimizer, l’intervallo di lookback massimo disponibile per qualsiasi metrica selezionata è impostato su 7 giorni. Per queste metriche, il modello di attribuzione è impostato per impostazione predefinita su **Ultimo contatto**, ovvero l&#39;interazione più recente prima della conversione.

  Ad esempio, puoi tenere traccia di un acquisto effettuato dopo che un cliente ha interagito con il tuo percorso negli ultimi 7 giorni.

* **Attribuzione delle metriche con licenza Customer Journey Analytics**:

  Con entrambe le licenze Journey Optimizer e Customer Journey Analytics, puoi creare metriche personalizzate con impostazioni di attribuzione specifiche o modificare le attribuzioni delle metriche integrate.

  Ulteriori informazioni su [Modelli di attribuzione](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Assegnare le metriche del percorso {#assign}

>[!IMPORTANT]
>
>È consentita una sola metrica di percorso per percorso.

Per iniziare a tracciare le metriche del percorso, segui i passaggi descritti di seguito:

1. Dal menu **[!UICONTROL Percorsi]**, fai clic su **[!UICONTROL Crea Percorso]**.

1. Modificate il riquadro di configurazione del percorso per definire il nome del percorso e impostarne le proprietà. Scopri come impostare le proprietà del percorso in [questa pagina](../building-journeys/journey-properties.md).

1. Scegli le **[!UICONTROL metriche di Percorso]** che verranno utilizzate per misurare l&#39;efficacia del percorso.

   Le metriche si applicano al percorso stesso e sono applicabili a tutti gli elementi del percorso.

   ![Pannello di configurazione delle metriche di successo nelle proprietà del percorso](assets/success_metric.png)

1. Fai clic su **[!UICONTROL Salva]**.

1. Progetta il tuo percorso con le **[!UICONTROL Attività]** necessarie.

1. Verifica e pubblica il percorso.

1. Apri il rapporto sul percorso per tenere traccia delle prestazioni delle metriche di successo assegnate.

   Le metriche scelte vengono visualizzate nella tabella KPI e statistiche Percorso del rapporto.

   ![Elenco a discesa delle metriche di successo che mostra gli eventi disponibili per il tracciamento degli obiettivi](assets/success_metric_2.png)

