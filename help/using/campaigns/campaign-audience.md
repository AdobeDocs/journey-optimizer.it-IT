---
solution: Journey Optimizer
product: journey optimizer
title: Definire il pubblico della campagna di azione
description: Scopri come definire il pubblico della campagna di azione.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: crea, ottimizzatore, campagna, superficie, messaggi
exl-id: 5635ef04-c69d-4397-9762-7a6f1265d453
source-git-commit: 93698c93f3750b4d7feff18509f8144a7c79f156
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 6%

---

# Definire il pubblico della campagna di azione {#action-campaign-audience}

Utilizza la scheda **[!UICONTROL Pubblico]** per definire il pubblico della campagna.

![](assets/campaign-audience.png)

1. **Selezionare il pubblico**

   Per le campagne di marketing, fai clic sul pulsante **[!UICONTROL Seleziona pubblico]** per visualizzare l&#39;elenco dei tipi di pubblico di Adobe Experience Platform disponibili. [Ulteriori informazioni sui tipi di pubblico](../audience/about-audiences.md)

   >[!IMPORTANT]
   >
   >L&#39;utilizzo dei tipi di pubblico e degli attributi di [composizione del pubblico](../audience/get-started-audience-orchestration.md) non è attualmente disponibile per l&#39;utilizzo con Healthcare Shield o Privacy and Security Shield.

1. **Selezionare il tipo di identità**

   Nel campo **[!UICONTROL Tipo di identità]**, scegli il tipo di chiave da utilizzare per identificare i singoli utenti del pubblico selezionato. Puoi utilizzare un tipo di identità esistente o crearne uno nuovo utilizzando il servizio Adobe Experience Platform Identity. Gli spazi dei nomi di identità standard sono elencati in [questa pagina](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   È consentito un solo tipo di identità per campagna. Gli individui appartenenti a un segmento che non ha il tipo di identità selezionato tra le loro diverse identità non possono essere targetizzati dalla campagna. Ulteriori informazioni sui tipi di identità e sugli spazi dei nomi sono disponibili nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=it){target="_blank"}.

## Passaggi successivi {#next}

Una volta che il pubblico della campagna Azione è pronto, puoi pianificarla. [Ulteriori informazioni](campaign-schedule.md)
