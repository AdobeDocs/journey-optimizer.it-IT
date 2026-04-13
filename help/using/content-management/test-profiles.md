---
title: Selezionare i profili di test
description: Learn how to select test profiles to preview and test content.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: 95a6d032808bc735a27a98dcb61efefa93cf5047
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 18%

---

# Selezionare i profili di test {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Utilizza i profili di test per verificare il contenuto"
>abstract="Utilizza i profili di test per visualizzare in anteprima e verificare il contenuto. Se hai aggiunto campi personalizzati, puoi controllarne la visualizzazione utilizzando i dati dei profili di test."

Test profiles are additional recipients who do not match the defined targeting criteria. [Scopri come creare i profili di test](../audience/creating-test-profiles.md)

Before using test profiles to test your content, you first need to select them. Per farlo, segui questi passaggi:

1. From the edit content screen of your message or in the Email Designer, click the **[!UICONTROL Simulate content]** button and select **[!UICONTROL Simulate content]**.

1. Click the **[!UICONTROL Manage test profiles]** button then select the namespace to use to identify test profiles by clicking the **[!UICONTROL Identity namespace]** selection icon. [Learn more about Adobe Experience Platform identity namespaces](../audience/get-started-identity.md).

   In the example below, we use the **Email** namespace.

   ![](../email/assets/previewselect-namespace.png)

1. Use the search field to find the namespace, select it and click **[!UICONTROL Select]**

   ![](../email/assets/preview-email-namespace.png)

1. In the **[!UICONTROL Identity value]** field, enter the value (here the email address) to identify the test profile and click **[!UICONTROL Add profile]**.

   <!--![](assets/preview-identity-value.png)-->

1. If you added personalization to your message, add other profiles so that you can test different variants of the message depending on profile data. Once added, profiles are listed under the selected fields.

   ![](../email/assets/preview-profile-list.png)

   Based on the message personalization elements, this list displays data for each test profile in the related columns.

>[!NOTE]
>
>Oltre ai profili di test, [!DNL Journey optimizer] consente anche di testare diverse varianti del contenuto visualizzandolo in anteprima e inviando bozze utilizzando dati di input di esempio caricati da un file CSV / JSON o aggiunti manualmente. [Scopri come simulare varianti di contenuto](../test-approve/simulate-sample-input.md)
