---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Cambia dimensione
description: Scopri come utilizzare l’attività Cambia dimensione
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/yN2RlYom4xpdiG0G8pt3U4MeY0C1JjDudDqYg-HPv1w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29c
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 50%

---

# Cambia dimensione {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **Genera complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Attività Cambia dimensione"
>abstract="Questa attività ti consente di modificare la dimensione targeting durante la creazione di un pubblico. Sposta l’asse in base al modello di dati e alla dimensione di input. Ad esempio, puoi passare dalla dimensione “contratti” alla dimensione “clienti”."

In qualità di addetto al marketing, puoi migliorare il targeting del pubblico passando da un’entità dati a una correlata all’interno di una campagna orchestrata. Questo ti consente di andare oltre i profili utente e di concentrarti su comportamenti specifici, come acquisti, prenotazioni o altre interazioni.

A tal fine, utilizza l’attività **[!UICONTROL Modifica dimensione]**. Consente di regolare la dimensione di targeting durante la campagna orchestrata.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.
-->

## Configurare l’attività Cambia dimensione {#configure}

Per configurare l’attività **[!UICONTROL Cambia dimensione]** segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Modifica dimensione]** alla campagna orchestrata.

   ![](../assets/orchestrated-change-dimension.png)

1. Definisci la **[!UICONTROL nuova dimensione target]**. Il passaggio della dimensione Modifica utilizza un join esterno: tutti i record del gruppo di input passano attraverso, inclusi quelli senza voci corrispondenti nella nuova dimensione.

   >[!IMPORTANT]
   >
   >I record privi di profilo corrispondente nella nuova dimensione di targeting sono **esclusi automaticamente al momento della consegna dei messaggi**. Al momento questa esclusione non viene riportata nei registri di esclusione. Per identificare in anticipo i record non corrispondenti, utilizza l&#39;opzione **Anteprima risultati** nella transizione dopo il passaggio Modifica dimensione e verifica che i conteggi dei record siano in linea con le aspettative prima di procedere.


## Esempio {#example}

Questo caso d’uso si incentra sull’invio di un SMS ai profili che hanno creato una wishlist nell’ultimo mese.

Inizia con un’attività **[!UICONTROL Crea pubblico]**, utilizzando la dimensione di targeting **[!UICONTROL Wishlist]** per identificare tutte quelle rilevanti.

Quindi, aggiungi un&#39;attività **[!UICONTROL Modifica dimensione]** per passare dalla dimensione di targeting **[!UICONTROL Elenco desideri]** alla **[!UICONTROL Destinatario].** Questo passaggio assicura che la campagna orchestrata esegua il targeting dei profili corretti collegati a tali elenchi di desideri, consentendo l’invio dell’SMS ai profili desiderati.

![](../assets/orchestrated-change-dimension-example.png)
