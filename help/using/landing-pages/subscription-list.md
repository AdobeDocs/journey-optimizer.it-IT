---
title: Creare un elenco di abbonamenti
description: Learn how to set up a subscription list in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: c988f0baa8b3c622dfb4f1ff060001a3462ed31e
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 3%

---

# Subscription lists {#create-subscription-list}

## What is a subscription list? {#subscription-list-definition}

A subscription service refers to marketing goods and services provided to customers who have opted in to receive communications on a specific subject/event/interest/etc. on an ongoing basis. [!DNL Journey Optimizer]

A subscription service can be:

* a newsletter, for example: &quot;Running series&quot;
* an event, for example: &quot;Summit 2021&quot;
* a webinar, for example: &quot;Learn more about crypto&quot;
* an interest on a particular product/sport/service/etc., for example: &quot;Interested to buy a house in the next 12 months&quot;
* a preference on how to be notified, for example: &quot;Receive new song notifications on email&quot;

[](create-lp.md) [](lp-use-cases.md#subscription-to-a-service)

## Define a subscription list {#define-subscription-list}

To create a subscription list, follow the steps below.

1. **[!UICONTROL Customer]****[!UICONTROL Subscription list]**

   ![](assets/lp_subscription-lists.png)

1. Fai clic sul pulsante **[!UICONTROL Create subscription list]**.

   ![](assets/lp_create-subscription-list.png)

1. Add a name and a description. These fields are mandatory.

1. You can define a start date and end date.

   ![](assets/lp_subscription-list-dates.png)

1. Fai clic su **[!UICONTROL Save]**.

The list displays all the subscription lists created. You can filter them based on the creation date or modification date, and their status.

![](assets/lp_subscription-filters.png)

The possible statuses are as follows:

* **[!UICONTROL Not started]** The susbscribed profiles will not receive yet communications relating to this subscription list.
* **[!UICONTROL Live]**
* **[!UICONTROL Expired]** Any subscribed profile will not receive any more communications relating to this subscription list.

Once the subscription list is created, you can use it in a landing page. The profiles who opt in through the landing page form will be added to the list. [Ulteriori informazioni](design-lp.md)

[](../building-journeys/journey-gs.md#jo-build)

>[!NOTE]
>
>You can monitor your subscription list impacts through specific reports. [Ulteriori informazioni](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
