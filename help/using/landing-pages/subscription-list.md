---
solution: Journey Optimizer
product: journey optimizer
title: Creare un elenco di iscrizione
description: Scopri come impostare un elenco di iscrizioni in Journey Optimizer
feature: Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: destinazione, pagina di destinazione, elenco, abbonamento, servizio
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: f63f9d6ffd28d276f8a3dadbf8dc6b947b8331e7
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 11%

---

# Elenchi di abbonamenti {#create-subscription-list}

## Che cos’è un elenco di abbonamenti? {#subscription-list-definition}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="Configurare un elenco di iscrizioni"
>abstract="Crea un elenco di iscrizioni per raccogliere i profili che hanno acconsentito a ricevere comunicazioni su uno specifico argomento o evento. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html?lang=it#define-subscription-list" text="Creare un elenco di iscrizione"

Un servizio di abbonamento si riferisce a beni e servizi di marketing forniti a clienti che hanno acconsentito a ricevere comunicazioni su un argomento/evento/interesse specifico/ecc. su base continuativa. In [!DNL Journey Optimizer], i clienti che hanno prestato il consenso sono raccolti in un elenco di abbonamenti.

Un servizio di abbonamento può essere:

* una newsletter, ad esempio: &quot;Serie in esecuzione&quot;
* un evento, ad esempio: &quot;Summit 2021&quot;
* un webinar, ad esempio: &quot;Ulteriori informazioni su crypto&quot;
* un interesse su un particolare prodotto/sport/servizio/ecc., ad esempio: &quot;Interessato ad acquistare una casa nei prossimi 12 mesi&quot;
* una preferenza sulla modalità di notifica, ad esempio: &quot;Ricevi notifiche di nuove canzoni tramite e-mail&quot;

I profili possono essere aggiunti a un elenco di iscrizioni tramite una [pagina di destinazione](create-lp.md). Un esempio è presentato in [questa sezione](lp-use-cases.md#subscription-to-a-service).

## Creare un elenco di iscrizione {#define-subscription-list}

Per creare un elenco di iscrizioni, segui i passaggi indicati di seguito.

1. Per accedere agli elenchi delle sottoscrizioni, selezionare **[!UICONTROL Cliente]** > **[!UICONTROL Elenco sottoscrizioni]**.

   ![](assets/lp_subscription-lists.png)

1. Selezionare il pulsante **[!UICONTROL Crea elenco iscrizioni]**.

   ![](assets/lp_create-subscription-list.png)

1. Aggiungi un titolo e una descrizione. Questi campi sono obbligatori.

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >Attualmente non è possibile utilizzare la spaziatura o immettere un nome già esistente per un altro elenco di iscrizioni nel campo **[!UICONTROL Titolo]**.

1. Puoi definire una data di inizio e una data di fine.

   ![](assets/lp_subscription-list-dates.png)

1. Seleziona o crea tag Adobe Experience Platform dal campo **[!UICONTROL Tag]** per categorizzare la pagina di destinazione ai fini di una ricerca migliorata. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Fai clic su **[!UICONTROL Salva]**.

Nell&#39;elenco vengono visualizzati tutti gli elenchi di iscrizioni creati. Puoi filtrarli in base alla data di creazione o di modifica e al loro stato.

![](assets/lp_subscription-filters.png)

I possibili stati sono i seguenti:

* **[!UICONTROL Non iniziato]**: è stata definita una data di inizio successiva al giorno corrente. I profili abbonati non riceveranno ancora comunicazioni relative a questo elenco di abbonamenti.
* **[!UICONTROL Live]**: il giorno corrente è compreso tra la data di inizio e la data di fine dell&#39;elenco di iscrizioni, oppure non sono state definite date di fine/inizio, il che significa che l&#39;elenco di iscrizioni è sempre live.
* **[!UICONTROL Scaduto]**: la data di fine è passata, pertanto l&#39;elenco iscrizioni non è più valido. I profili abbonati non riceveranno più comunicazioni relative a questo elenco di abbonamenti.

Una volta creato l’elenco di iscrizioni, puoi utilizzarlo in una pagina di destinazione. I profili che danno il consenso tramite il modulo della pagina di destinazione verranno aggiunti all’elenco. [Ulteriori informazioni](design-lp.md)

Puoi anche utilizzare gli elenchi di abbonamenti come tipi di pubblico durante la [creazione di percorsi](../building-journeys/journey-gs.md#jo-build) e l&#39;aggiunta di personalizzazioni.

>[!NOTE]
>
>Puoi monitorare l’impatto dell’elenco degli abbonamenti tramite rapporti specifici. [Ulteriori informazioni](../reports/subscription-report-live.md)
