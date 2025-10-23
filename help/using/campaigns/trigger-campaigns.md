---
solution: Journey Optimizer
product: journey optimizer
title: Rivedere e attivare una campagna
description: Scopri come rivedere e attivare le campagne in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campagna, revisione, convalida, attivazione, attivazione, ottimizzatore
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---


# Eseguire una campagna attivata da API {#execute}

Una volta attivata la campagna, devi recuperare la richiesta cURL di esempio generata e utilizzarla nell’API per generare il payload e attivare la campagna.

## Da leggere {#must-read}

* **Date di inizio/fine campagna** - Se hai configurato una data di inizio e/o fine specifica durante la creazione della campagna, questa non verrà eseguita oltre queste date e le chiamate API avranno esito negativo.

* **Timeout chiamata** - Il timeout della chiamata all&#39;API REST di esecuzione messaggi interattiva è di 60 secondi. Tuttavia, in caso di timeout imprevisti per garantire la consegna, sono presenti nuovi tentativi interni.

## Attivare la campagna {#trigger}

1. Apri la campagna, quindi copia e incolla la richiesta di payload dalla sezione **[!UICONTROL richiesta cURL]**. Questo payload include tutte le variabili di personalizzazione (profilo e contesto) utilizzate nel messaggio. È disponibile una volta che la campagna è in diretta.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >Gli endpoint nella sezione cURL differiscono tra le campagne standard e le [campagne con throughput elevato](../campaigns/api-triggered-high-throughput.md).

1. Utilizza questa richiesta cURL nelle API per generare il payload e attivare la campagna. Per ulteriori informazioni, consulta la [documentazione dell&#39;API di esecuzione interattiva dei messaggi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution), in cui sono elencati tutti gli endpoint per le campagne Standard e High Throughput.

   Gli esempi di chiamate API sono disponibili anche in [questa pagina](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).
