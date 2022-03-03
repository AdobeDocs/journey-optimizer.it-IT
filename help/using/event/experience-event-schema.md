---
title: About ExperienceEvent Schemas for journey events
description: Learn about ExperienceEvent Schemas for journey events
feature: Schemas
topic: Administration
role: Admin
level: Intermediate
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: 587ac4a17db71790ed4d9ee07214293a2882180c
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 1%

---

# [!DNL Journey Optimizer] {#about-experienceevent-schemas}

[!DNL Journey Optimizer]

[!DNL Journey Optimizer]

## [!DNL Journey Optimizer]  {#schema-requirements}

[!DNL Journey Optimizer] Having a dataset for your events is not strictly necessary, but sending the events to a specific dataset will allow you to maintain users’ event history for future reference and analysis, so it is always a good idea. If you do not already have a suitable schema and dataset for your event, both of those tasks can be done in Adobe Experience Platform web interface.

![](assets/schema1.png)

[!DNL Journey Optimizer]

* The schema must be of the XDM ExperienceEvent class.

   ![](assets/schema2.png)

* For system-generated events, the schema must include the Orchestration eventID field group. [!DNL Journey Optimizer]

   ![](assets/schema3.png)

* Declare an identity field for identifying the subject of the event. If no identity is specified, an identity map can be used. Queste operazioni non sono consigliate.

   ![](assets/schema4.png)

* If you would like this data to be available for lookup later in a Journey, mark the schema and dataset for profile.

   ![](assets/schema5.png)

   ![](assets/schema6.png)

* Feel free to include data fields to capture any other context data you want to include with the event, such as information about the user, the device from which the event was generated, location, or any other meaningful circumstances related to the event.

   ![](assets/schema7.png)

   ![](assets/schema8.png)

## Sfruttamento delle relazioni tra schemi{#leverage_schema_relationships}

Adobe Experience Platform allows you to define relationships between schemas in order to use one dataset as a lookup table for another.

Let&#39;s say your brand data model has a schema capturing purchases. You also have a schema for the product catalog. You can capture the product ID in the purchase schema and use a relationship to look up more complete product details from the product catalog. This allows you to create a segment for all customers who bought a laptop, for example, without having to explicitly list out all laptop IDs or capture every single product details in transactional systems.

To define a relationship, you need to have a dedicated field in the source schema, in this case the product ID field in the purchase schema. This field needs to reference the product ID field in the destination schema. The source and destination tables must be enabled for profiles and the destination schema must have that common field defined as its primary identity.

Here is the product catalog schema enabled for profile with the product ID defined as the primary identity.

![](assets/schema9.png)

Here is the purchase schema with the relationship defined on the product ID field.

![](assets/schema10.png)

>[!NOTE]
>
>[](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html?lang=en)

In Journey Optimizer, you can then leverage all the fields from the linked tables:

* [](../event/experience-event-schema.md#unitary_event_configuration)
* [](../event/experience-event-schema.md#journey_conditions_using_event_context)
* [](../event/experience-event-schema.md#message_personalization)
* [](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### Configurazione evento{#unitary_event_configuration}

The linked schema fields are available in unitary and business event configuration:

* when browsing through the event schema fields in the event configuration screen.
* when defining a condition for system-generated events.

![](assets/schema11.png)

The linked fields are not available:

* in the event key formula
* in event id condition (rule-based events)

[](../event/about-creating.md)

### Journey conditions using event context{#journey_conditions_using_event_context}

You can use data from a lookup table linked to an event used in a journey for condition building (expression editor).

Add a condition in a journey, edit the expression and unfold the event node in the expression editor.

![](assets/schema12.png)

[](../building-journeys/condition-activity.md)

### Message personalization{#message_personalization}

The linked fields are available when personalizing a message. The related fields are displayed in the context passed from the journey to the message.

![](assets/schema14.png)

[](../personalization/personalization-use-case.md)

### Custom action personalization with journey event context{#custom_action_personalization_with_journey_event_context}

The linked fields are available when configuring the action parameters of a journey custom action activity.

![](assets/schema13.png)

[](../building-journeys/using-custom-actions.md)
