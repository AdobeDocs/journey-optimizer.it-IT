---
solution: Journey Optimizer
product: journey optimizer
title: Definire le proprietà della campagna attivata dall’API
description: Scopri come definire le proprietà della campagna attivata da API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: bda7e337-a246-4f01-b935-4a234d4c4baa
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 20%

---

# Definire le proprietà della campagna attivata dall’API {#api-properties}

Per creare una nuova campagna attivata da API, effettua le seguenti operazioni:

1. Passa al menu **[!UICONTROL Campagne]** e seleziona la scheda **[!UICONTROL API attivata]**.

1. Fai clic sul pulsante **[!UICONTROL Crea campagna]** e seleziona il tipo di campagna:

   * **[!UICONTROL API attivata - Marketing]** - Seleziona questo tipo di campagna API attivata per inviare comunicazioni di marketing personalizzate a tipi di pubblico mirati.

   * **[!UICONTROL API attivata - Transazionale]** - Le campagne transazionali hanno lo scopo di inviare messaggi transazionali, ovvero messaggi inviati in seguito a un&#39;azione eseguita da un individuo: richiesta di reimpostazione della password, acquisto del carrello, ecc.

     +++Modalità High Throughput

     Per le campagne attivate da API transazionali, puoi abilitare la modalità **[!UICONTROL High Throughput]**. Questa modalità è progettata per la messaggistica in tempo reale su larga scala (fino a 5000 transazioni al secondo) e fornisce maggiore disponibilità con latenza inferiore. [Scopri come utilizzare la modalità Highthrouput](../campaigns/api-triggered-high-throughput.md)

     >[!AVAILABILITY]
     >
     >Attualmente, la modalità High Throughput è disponibile solo per il canale e-mail e nell’area degli Stati Uniti.
     >
     >Questa funzionalità è disponibile solo per le organizzazioni che hanno acquistato il componente aggiuntivo **Messaggistica transazionale ad alta velocità** di Adobe. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

     +++

   ![](assets/api-triggered-modal.png)

1. Nella scheda **[!UICONTROL Proprietà]**, immetti un nome e una descrizione per la campagna.

   ![](assets/create-campaign-properties.png)

1. Utilizza il campo **Tag** per assegnare alla campagna i tag unificati di Adobe Experience Platform. Questo consente di classificarle facilmente e migliorare la ricerca dall’elenco delle campagne. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags)

1. Puoi limitare l’accesso a questa campagna in base alle etichette di accesso. Per aggiungere un limite di accesso, seleziona il pulsante **[!UICONTROL Gestisci accesso]** nella parte superiore della pagina. Assicurati di selezionare solo le etichette per le quali disponi dell’autorizzazione. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

## Passaggi successivi {#next}

Una volta che la configurazione e il contenuto della campagna sono pronti, puoi configurarne l’azione. [Ulteriori informazioni](api-triggered-campaign-action.md)
