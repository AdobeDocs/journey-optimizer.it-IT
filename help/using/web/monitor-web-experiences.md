---
title: Monitorare le esperienze web
description: Scopri come monitorare le esperienze web in Journey Optimizer
feature: Web Channel, Reporting, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: d89795bb-c51d-4d1f-b7ed-2b2c5d278922
TQID: https://experienceleague.adobe.com/CEjKwnKx1ixUKA-mO7FfWGXaW9FyO-I-ZYyYm0scs88
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c618a0dc-1818-4c6d-9916-0d92e6796f24id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 288
ht-degree: 3%

---

# Monitorare le esperienze web {#monitor-web-experiences}

## Controlla i report web {#check-web-reports}

Una volta che la tua esperienza Web è attiva, puoi controllare la scheda **[!UICONTROL Web]** del [rapporto Percorso](../reports/journey-global-report-cja-web.md) e del [rapporto campagna](../reports/campaign-global-report-cja-web.md) per confrontare elementi quali il numero di impression, il tasso di clic e il numero di impegni con la pagina Web.

<!--You can check the **[!UICONTROL Web]** tab of the campaign reports. Learn more about the campaign web [live report](../reports/campaign-live-report.md#web-tab) and [global report](../reports/campaign-global-report-cja.md#web).-->

Per migliorare ulteriormente il monitoraggio dell’esperienza web, puoi anche tenere traccia dei clic su qualsiasi elemento specifico del sito web. Questo consente di visualizzare il numero di clic su tale elemento nei rapporti web. [Scopri come](#use-click-tracing)

## Utilizzare il tracciamento dei clic {#use-click-tracking}

Il web designer consente di selezionare qualsiasi elemento del sito web e di tenere traccia dei clic su di esso.

Queste informazioni possono essere utili per migliorare l’esperienza degli utenti del sito web. Ad esempio, se i [report Web](../reports/campaign-global-report-cja-web.md) mostrano che molti utenti fanno clic su un elemento che non è effettivamente cliccabile, è possibile aggiungere un collegamento a tale elemento.

1. Seleziona un elemento nella pagina e scegli **[!UICONTROL Seleziona l&#39;elemento di tracciamento]** dal menu contestuale.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >È possibile selezionare qualsiasi elemento, cliccabile o meno.

1. L&#39;azione tracciata corrispondente viene visualizzata automaticamente nel riquadro **[!UICONTROL Traccia clic]** a sinistra.

   ![](assets/web-designer-click-track-pane.png)

1. Aggiungi un’etichetta significativa per gestire tutti gli elementi tracciati e trovarli facilmente nei rapporti. Il campo **[!UICONTROL Selettore CSS]** mostra le informazioni per individuare l&#39;elemento selezionato.

1. Ripeti i passaggi precedenti per selezionare tutti gli altri elementi necessari per il tracciamento dei clic. Tutte le azioni corrispondenti sono elencate nel riquadro a sinistra.

   ![](assets/web-designer-click-tracking-actions.png)

1. Per rimuovere il tracciamento dei clic su un elemento, seleziona l’icona di eliminazione corrispondente.

Una volta che la campagna è attiva, puoi controllare il numero di clic per ogni elemento nel web della campagna [report live](../reports/campaign-live-report.md#web-tab) e [report Customer Journey Analytics](../reports/campaign-global-report-cja-web.md).
