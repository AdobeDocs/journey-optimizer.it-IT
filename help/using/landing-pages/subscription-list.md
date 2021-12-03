---
title: Creare un elenco di iscrizioni
description: Scopri come impostare un elenco di abbonamenti in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Creare un elenco di iscrizioni {#create-subscription-list}

## Che cos’è un elenco di abbonamenti?

Un servizio di abbonamento si riferisce a beni e servizi di marketing forniti ai clienti che hanno acconsentito a ricevere comunicazioni su un soggetto/evento/interesse/ecc specifico. su base continuativa. In [!DNL Journey Optimizer], questi clienti con consenso vengono raccolti in un elenco di sottoscrizioni.

Un servizio di abbonamento può essere:

* una newsletter, ad esempio &quot;Serie in esecuzione&quot;
* un evento, ad esempio &quot;Summit 2021&quot;
* un webinar, ad esempio &quot;Ulteriori informazioni su crypto&quot;
* un interesse su un particolare prodotto/sport/servizio/ecc., per esempio &quot;Interessato ad acquistare una casa nei prossimi 12 mesi&quot;
* una preferenza su come ricevere le notifiche, ad esempio &quot;Ricevere nuove notifiche sulle e-mail&quot;

I profili possono essere aggiunti a un elenco di abbonamenti tramite un [pagina di destinazione](create-lp.md). Un esempio è presentato in [questa sezione](get-started-lp.md#subscription-to-a-service).

## Definire un elenco di sottoscrizione {#define-subscription-list}

Per creare un elenco di iscrizioni, segui i passaggi riportati di seguito.

1. Per accedere agli elenchi di sottoscrizione, selezionare **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. Dall’elenco delle sottoscrizioni, fai clic su **[!UICONTROL Create subscription]** elenco.

   ![](../assets/lp_create-subscription-list.png)

1. Aggiungi un nome e una descrizione. Questi campi sono obbligatori.

1. Puoi definire una data di inizio e una data di fine.

   ![](../assets/lp_subscription-list-dates.png)

1. Fai clic su **[!UICONTROL Save]**.

Nell’elenco vengono visualizzati tutti gli elenchi di sottoscrizioni creati. Puoi filtrarli in base alla data di creazione o di modifica.

![](../assets/lp_subscription-filters.png)

Gli stati possibili sono i seguenti:

* **[!UICONTROL Not started]**: Hai definito una data di inizio successiva al giorno corrente. I profili abbonati a questo elenco non riceveranno ancora comunicazioni relative a questo elenco di abbonamenti.
* **[!UICONTROL Live]**: Il giorno corrente è compreso tra la data di inizio e la data di fine dell’elenco degli abbonamenti oppure non hai definito le date di fine/inizio, il che significa che l’elenco degli abbonamenti è sempre attivo.
* **[!UICONTROL Expired]**: La data di fine viene passata. L&#39;elenco di sottoscrizione non è più valido. Qualsiasi profilo iscritto a questo elenco non riceverà altre comunicazioni relative a questo elenco di abbonamenti.

Una volta creato l’elenco di sottoscrizioni, puoi utilizzarlo in una pagina di destinazione in modo che i profili possano effettuare il consenso tramite un modulo e aggiungerlo all’elenco. [Ulteriori informazioni](design-lp.md)

Puoi anche utilizzare gli elenchi di abbonamenti come segmenti durante la creazione di percorsi e personalizzazioni.

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* How do you handle the different statuses? Live, Not started, Expired? Is it only through start/end dates?

* What does it mean when a subscription list is expired or not started? You can't use it in a LP? And if a user is subscribed to this service, then he won't receive communications any more?

* What else can you currently do with subscription lists apart from attach them to a landing page?

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->