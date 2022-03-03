---
title: Landing page use cases
description: Discover the most common use cases with landing pages in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: c988f0baa8b3c622dfb4f1ff060001a3462ed31e
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 21%

---

# Landing page use cases {#lp-use-cases}

[!DNL Journey Optimizer]

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Subscription to a service {#subscription-to-a-service}

[](subscription-list.md) The main steps are presented on the graph below:

![](assets/lp_subscription-uc.png)

<!--to keep your customers that are interested updated on that event--> To do this, you&#39;re going to send an email including a link to a landing page that will enable your recipients to register for this event. The users who register will be added to the subscription list that you created for this purpose.

### Set up landing page {#set-up-lp}

1. Create the event registration&#39;s subscription list, which will store the registered users. [](subscription-list.md#define-subscription-list)

   ![](assets/lp_subscription-uc-list.png)

1. [](create-lp.md)

1. [](create-lp.md#configure-primary-page)

1. [](design-lp.md)

   ![](assets/lp_subscription-uc-lp-list.png)

1. Create a &#39;thank you&#39; page that will be displayed to your recipients once they submit the registration form. [](create-lp.md#configure-subpages)

   ![](assets/lp_subscription-uc-thanks.png)

1. [](create-lp.md#publish)

1. [](../messages/create-message.md)

1. [](../messages/message-tracking.md#insert-links) **[!UICONTROL Landing page]****[!UICONTROL Link type]**[](create-lp.md#configure-primary-page)

   ![](assets/lp_subscription-uc-link.png)

1. Salva il contenuto e [pubblica il messaggio](../messages/publish-manage-message.md).

1. [](../building-journeys/journey.md)

   ![](assets/lp_subscription-uc-journey.png)

   Once they receive the email, if your recipients click the link to the landing page, they will be directed to the &#39;thank you&#39; page and they will be added to the subscription list.

### Send a confirmation email {#send-confirmation-email}

Additionally, you can send a confirmation email to the recipients who registered for your event. A questo scopo, segui i passaggi riportati qui sotto.

1. [](../building-journeys/journey.md) **[!UICONTROL Create journey]** Puoi trovare ulteriori informazioni [qui](create-lp.md#configure-primary-page)

   ![](assets/lp_subscription-uc-create-journey.png)

1. **[!UICONTROL Events]****[!UICONTROL Segment Qualification]** Puoi trovare ulteriori informazioni [qui](../building-journeys/segment-qualification-events.md)

1. **[!UICONTROL Segment]**

   ![](assets/lp_subscription-uc-confirm-journey.png)

1. Select the confirmation email of your choice and send it through the journey.

   ![](assets/lp_subscription-uc-confirm-email.png)

All the users who registered for your event will receive the confirmation email.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Opting out {#opt-out}

To enable your recipients to unsubscribe from your communications, you can include a link to an opt-out landing page into your emails.

[](../messages/consent.md)

### Gestione degli opt-out {#opt-out-management}

Come requisito legale, è necessario dare ai destinatari la possibilità di annullare l’iscrizione alla ricezione di comunicazioni da parte di un marchio. Ulteriori informazioni sulle normative applicabili sono disponibili nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=it#regulations){target=&quot;_blank&quot;}.

Pertanto, devi sempre includere un **collegamento che consenta di annullare l’abbonamento** in ogni e-mail inviata ai destinatari:

* Facendo clic su questo collegamento, i destinatari verranno indirizzati a una pagina di destinazione contenente un pulsante per confermare l’opt-out.
* Upon clicking the opt-out button, the profile data will be updated with this information.

### Configure opt-out {#configure-opt-out}

To enable the recipients of an email to unsubscribe from your communications through a landing page, follow the steps below.

1. Create your landing page. [Ulteriori informazioni](create-lp.md)

1. Define the primary page. [Ulteriori informazioni](create-lp.md#configure-primary-page)

1. [](design-lp.md)**[!UICONTROL Form]****[!UICONTROL Opt-out]****[!UICONTROL Channel (email)]**

   ![](assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. [](create-lp.md#configure-subpages)

   ![](assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >**[!UICONTROL Call to action]****[!UICONTROL Form]** [Ulteriori informazioni](design-lp.md)

1. [](create-lp.md#publish)

   ![](assets/lp_opt-out-publish.png)

1. [](../messages/create-message.md)[!DNL Journey Optimizer]

1. Seleziona il testo nel contenuto e [inserisci un collegamento](../messages/message-tracking.md#insert-links) utilizzando la barra degli strumenti contestuale. You can also use a link on a button.

   ![](assets/lp_opt-out-insert-link.png)

1. **[!UICONTROL Landing page]****[!UICONTROL Link type]**[](create-lp.md#configure-primary-page)

   ![](assets/lp_opt-out-landing-page.png)

1. Salva il contenuto e [pubblica il messaggio](../messages/publish-manage-message.md).

1. Send your message through a journey. [Ulteriori informazioni](../building-journeys/journey.md).

1. Once the message is received, if a recipient clicks the unsubscribe link in the email, your landing page is displayed.

   ![](assets/lp_opt-out-submit-form.png)

   If the recipient checks the box and submits the form:

   * The opted-out recipient is redirected to the confirmation message screen.

   * The profile data is updated and will not receive communications from your brand unless subscribed again.

Per verificare che la scelta del profilo corrispondente sia stata aggiornata, passa ad Experience Platform e accedi al profilo selezionando uno spazio dei nomi di identità e un valore di identità corrispondente. Per ulteriori informazioni, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target=&quot;_blank&quot;}.

![](assets/lp_opt-out-profile-choice.png)

Nella scheda **[!UICONTROL Attributes]**, puoi vedere che il valore di **[!UICONTROL choice]** è stato modificato in **[!UICONTROL no]**.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../messages/consent.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../messages/consent.md#unsubscribe-email)
-->
