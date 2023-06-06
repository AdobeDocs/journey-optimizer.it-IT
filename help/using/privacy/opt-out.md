---
solution: Journey Optimizer
product: journey optimizer
title: Gestire la rinuncia
description: Scopri come gestire l’opt-out e la privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 100%

---

# Gestire la rinuncia {#consent}

Come requisito legale, è necessario fornire ai destinatari la possibilità di annullare l’iscrizione alla ricezione di comunicazioni da parte di un marchio e garantire il rispetto di questa scelta. Ulteriori informazioni sulle normative applicabili sono disponibili nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=it#regulations){target="_blank"}.

**Perché è importante?**

* Il mancato rispetto di queste normative introduce rischi legali normativi per il tuo marchio.
* Ti aiuta a evitare l’invio di comunicazioni non richieste ai destinatari, in modo che queste non vengano contrassegnate come spam danneggiando la tua reputazione.

## Gestire gli annullamenti delle iscrizioni in percorsi e campagne {#opt-out-ajo}

Quando invii messaggi da percorsi o campagne, devi sempre assicurarti che i clienti abbiano la possibilità di annullare l’iscrizione in modo da non ricevere più comunicazioni. Una volta annullata l’iscrizione, i profili vengono rimossi automaticamente dal pubblico dei futuri messaggi di marketing.

**[!DNL Journey Optimizer]** permette di gestire la rinuncia nelle e-mail e nei messaggi SMS; tuttavia, le notifiche push non richiedono alcun intervento da parte tua, in quanto i destinatari possono annullare l’iscrizione direttamente dal proprio dispositivo. Ad esempio, al momento del download o dell’utilizzo dell’app, possono scegliere di interrompere le notifiche. Analogamente, possono modificare le impostazioni di notifica tramite il sistema operativo mobile.

Scopri come gestire la rinuncia nei messaggi e-mail e SMS di Journey Optimizer in queste sezioni:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Lead" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>Gestione della rinuncia e-mail</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Non frequente" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>Gestione della rinuncia agli SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>In [!DNL Journey Optimizer], il consenso è gestito dallo [Schema di consenso](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=it){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=it#choice-values){target="_blank"} di Experience Platform.

## Implementare il consenso alla personalizzazione {#opt-out-personalization}

I clienti possono anche rinunciare alla presentazione di contenuti personalizzati. Una volta che un profilo ha rinunciato alla personalizzazione, devi assicurarti che i suoi dati non vengano utilizzati per la personalizzazione e devi sostituire qualsiasi contenuto personalizzato con una variante di fallback.

### In Gestione decisioni

Quando utilizzi le offerte, le preferenze di personalizzazione non vengono implementate automaticamente negli [ambiti decisionali](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) utilizzati da una richiesta di [Decisioning](../offers/api-reference/offer-delivery-api/decisioning-api.md) API o [Edge Decisioning](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md) API. In questo caso, devi applicare manualmente il consenso alla personalizzazione. A questo scopo, segui i passaggi riportati qui sotto.

>[!NOTE]
>
>Gli ambiti decisionali utilizzati in canali creati in [!DNL Journey Optimizer] soddisfano questo requisito dal percorso o dalla campagna a cui appartengono.



1. Per il targeting degli utenti che hanno acconsentito alla personalizzazione, crea un [segmento Adobe Experience Platform](../segment/about-segments.md) utilizzando un attributo di profilo come ad esempio *“Acconsente alla personalizzazione = True”*.

1. Durante la creazione di una [decisione](../offers/offer-activities/create-offer-activities.md), aggiungi un ambito decisionale e definisci un vincolo di idoneità basato su questo segmento per ogni raccolta di criteri di valutazione che contiene offerte personalizzate.

1. Crea un’[offerta di fallback](../offers/offer-library/creating-fallback-offers.md) che non include contenuti personalizzati.

1. [Assegna](../offers/offer-activities/create-offer-activities.md#add-fallback) l’offerta di fallback non personalizzata alla decisione.

1. [Rivedi e salva](../offers/offer-activities/create-offer-activities.md#review) la decisione.

Se un utente:

* ha dato il consenso alla personalizzazione, l’ambito decisionale determinerà l’offerta migliore per quel profilo.

* non ha dato il consenso alla personalizzazione, il profilo corrispondente non sarà idoneo per nessuna delle offerte che rientrano nei criteri di valutazione e riceverà quindi l’offerta di fallback non personalizzata.

>[!NOTE]
>
>Il consenso all’utilizzo dei dati del profilo in [modellazione dati](../offers/ranking/ai-models.md) non è ancora supportato in [!DNL Journey Optimizer].

