---
solution: Journey Optimizer
product: journey optimizer
title: Rivedi e attiva la campagna attivata dall’API
description: Scopri come rivedere e attivare le campagne attivate dall’API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: 561f1215-d13d-4ffc-b6f1-396ae67774c8
source-git-commit: 81e54a3e3428d58818805b5dcb397ede4039436a
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 4%

---

# Rivedi e attiva la campagna attivata dall’API {#api-review}

Una volta configurata la campagna attivata dall’API, devi esaminarne il parametro e il contenuto prima di attivarla. Per farlo, segui questi passaggi:

>[!IMPORTANT]
>
> Se la campagna è soggetta a un criterio di approvazione, per poter inviare la campagna dovrai richiedere l’approvazione. [Ulteriori informazioni](../test-approve/gs-approval.md)

1. Nella schermata di configurazione della campagna, fai clic su **[!UICONTROL Verifica per attivare]** per visualizzare un riepilogo della campagna.

   ![](assets/campaign-review.png)

1. Viene visualizzato un riepilogo della configurazione della campagna, che ti consente di verificare se un parametro è errato o mancante e di modificare la campagna se necessario.

   In caso di errori, non puoi attivare la campagna. Risolvi gli errori prima di procedere.

   ![](assets/create-campaign-alerts.png)

1. Verifica che la tua campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Attiva]**.

1. La campagna è attivata. Il suo stato è **[!UICONTROL Live]** o **[!UICONTROL Pianificato]** se hai immesso una data di inizio.

   Lo stato **[!UICONTROL Completato]** viene assegnato automaticamente alla campagna 3 giorni dopo la sua attivazione o alla data di fine se ha un&#39;esecuzione ricorrente. [Ulteriori informazioni sugli stati delle campagne](manage-campaigns.md#statuses).

   Se non è stata specificata alcuna data di fine, la campagna mantiene lo stato **[!UICONTROL Live]**. Per modificarlo, devi interrompere la campagna manualmente. [Scopri come interrompere una campagna](manage-campaigns.md)

1. Dopo l’attivazione di una campagna, puoi controllarne le informazioni in qualsiasi momento aprendola. Il riepilogo consente di ottenere statistiche sul numero di profili target e di azioni consegnate e non riuscite.

   Puoi anche ottenere ulteriori statistiche nei report dedicati facendo clic sul pulsante **[!UICONTROL Report]**. [Ulteriori informazioni](../reports/campaign-global-report-cja.md)

   ![](assets/create-campaign-summary.png)

## Passaggi successivi {#next}

Una volta che la campagna attivata dall’API è pronta, puoi attivarne l’esecuzione utilizzando le API. [Ulteriori informazioni](trigger-campaigns.md)
