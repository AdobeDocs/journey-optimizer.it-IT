---
solution: Journey Optimizer
product: journey optimizer
title: Origine dati Adobe Experience Platform
description: Learn how to configure Adobe Experience Platform data source
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: built-in, source, data, platform, integration
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: 43a4b85adb74e24c7c57fa74177795d014b88774
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 26%

---

# Origine dati Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Origine dati Adobe Experience Platform"
>abstract="L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è incorporata e preconfigurata e non può essere eliminata. È progettata per recuperare e utilizzare i dati dal servizio Profilo cliente in tempo reale (ad esempio, controlla se la persona che ha effettuato l’accesso in un percorso è una donna)."

L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è incorporata e preconfigurata e non può essere eliminata. This data source is designed to retrieve and use data from the Real-time Customer Profile Service (for example, check if the person who entered a journey is a female). For more information about Adobe Real-time Customer Profile, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}.

To allow the connection to the Real-time Customer Profile Service, we must use a key to identify a person, and a namespace that contextualizes the key. As a result, you can only use this data source if your journeys start with an event containing a key and a namespace. [Ulteriori informazioni](../building-journeys/journey.md).

You can edit the pre-configured field group named &quot;ProfileFieldGroup&quot;, add new ones and remove the ones that are not used in any draft or live journeys. [Ulteriori informazioni](../datasource/configure-data-sources.md#define-field-groups).

>[!CAUTION]
>
>L’utilizzo di eventi di esperienza nelle espressioni/condizioni di percorso non è supportato. Se il caso d’uso richiede l’utilizzo di eventi esperienza, considera metodi alternativi. [Ulteriori informazioni](../building-journeys/exp-event-lookup.md)

Main steps to add field groups to the built-in data source are detailed below:

1. From the list of data sources, select the built-in **Adobe Experience Platform** data source.

   Sul lato destro dello schermo si apre il riquadro di configurazione dell’origine dati .

   ![](assets/journey23.png)

1. Select **[!UICONTROL Add a New Field Group]** to define a [new series of fields to retrieve](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Select a schema from the **[!UICONTROL Schema]** drop-down. Schema creation is performed in Adobe Experience Platform, not performed in Adobe Journey Optimizer.

   >[!NOTE]
   >
   >Only XDM Individual Profile-based schemas are supported in the [!DNL Journey Optimizer] Data Source configuration. For more information, see [XDM Individual Profile class](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/classes/individual-profile){target="_blank"}.

1. Select the fields to use, and save your changes.

>[!TIP]
>
>Hover over the name of a field group to reveal two icons on the right. Use these to **Duplicate** or **Delete** the field group. Note that the **[!UICONTROL Delete]** icon is only available if the field group is not used in any **Live**, **Draft** or **Finished** journey. Refer to the **[!UICONTROL Used in]** field to check if this is the case.
