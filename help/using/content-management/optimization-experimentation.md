---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare la sperimentazione nell’ottimizzazione dei messaggi
description: Scopri come utilizzare gli esperimenti sui contenuti per testare più versioni dei contenuti e determinare quale offre le prestazioni migliori.
role: User
level: Intermediate
keywords: sperimentazione, ottimizzazione, test A/B, esperimento sui contenuti, trattamenti
source-git-commit: f4eb982ba0840acfe336e759fcbf9cfd47b3b98c
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 2%

---

# Utilizzare la sperimentazione {#experimentation}

>[!NOTE]
>
>Questa pagina fornisce una panoramica sull’utilizzo della sperimentazione nell’ottimizzazione dei contenuti. Per informazioni dettagliate sugli esperimenti di contenuto, incluse le opzioni di configurazione, le metriche e l&#39;analisi, consulta la [documentazione sull&#39;esperimento di contenuto](../content-management/get-started-experiment.md).

La sperimentazione consente di testare più versioni di contenuto per determinare quale offre le migliori prestazioni in base a metriche di successo predefinite.

Per impostare la sperimentazione, segui i passaggi riportati di seguito.

Supponiamo che tu voglia testare i seguenti messaggi promozionali in una campagna:

* **Trattamento A**: &quot;20% di sconto sul prossimo acquisto&quot;
* **Trattamento B**: &quot;Spedizione gratuita per ordini superiori a $50&quot;
* **Trattamento C**: &quot;Ottieni la tua gift card da $ 10&quot;

Per impostare la sperimentazione e determinare quale messaggio determina il maggior numero di acquisti, segui i passaggi seguenti.

1. Crea un [percorso](../building-journeys/journey-gs.md#jo-build) o una [campagna](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Se fai parte di un percorso, aggiungi un&#39;attività **[!UICONTROL Azione]**, scegli un&#39;attività canale e seleziona **[!UICONTROL Configura azione]**. [Ulteriori informazioni](../building-journeys/journey-action.md#add-action)

1. Dalla scheda **[!UICONTROL Azioni]**, seleziona due azioni in entrata, ad esempio [esperienza basata su codice](../code-based/get-started-code-based.md) e [In-app](../../rp_landing_pages/in-app-landing-page.md).

1. Nella sezione **[!UICONTROL Ottimizzazione]**, seleziona **[!UICONTROL Crea esperimento]**.

   ![](../campaigns/assets/msg-optimization-select-experiment.png){width=85%}

1. Progetta e configura l’esperimento sui contenuti come desideri. [Scopri come](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}

   Una volta definito, l&#39;esperimento viene applicato a tutte le azioni inserite in quella campagna o tramite l&#39;attività di percorso **[!UICONTROL Azione]**, il che significa che gli stessi clienti visualizzano le stesse offerte su tutte le superfici.

   >[!NOTE]
   >
   >Puoi selezionare altre azioni: la sperimentazione si applica a tutte le azioni aggiunte alla campagna o all&#39;[attività Azione](../building-journeys/journey-action.md) del percorso.

1. [Attiva](../campaigns/review-activate-campaign.md) il percorso o la campagna.

Una volta che il percorso/la campagna è attivo, agli utenti vengono assegnate in modo casuale le diverse varianti di contenuto. [!DNL Journey Optimizer] tiene traccia della variante che determina più acquisti e fornisce informazioni fruibili.

Segui il successo della tua campagna con i report [percorso](../reports/journey-global-report-cja.md) e [campagna](../reports/campaign-global-report-cja-experimentation.md). <!--Link to Experimentation journey reportis missing-->

