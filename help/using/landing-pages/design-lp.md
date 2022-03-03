---
title: Progettare una pagina di destinazione
description: Learn how to design the content of a landing page in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: c61b8d80-17e1-4fdd-a739-efcee032dc23
source-git-commit: c988f0baa8b3c622dfb4f1ff060001a3462ed31e
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Design the landing page content {#design-lp-content}

[](create-lp.md#configure-primary-page)[](create-lp.md#configure-subpages)**[!UICONTROL Open Designer]** You can also click the corresponding button from the right palette.

![](assets/lp_open-designer.png)

From there, you can:

* ****[](../messages/assets-essentials.md) [](../messages/create-email-content.md)

* **** [](../messages/existing-content.md#import-raw-html-code)

* **** [](../messages/existing-content.md#import-html-content-from-file)

>[!NOTE]
>
>The landing page content designer is mostly similar to the email designer. [ [!DNL Journey Optimizer]](../messages/design-emails.md)

## Define landing page-specific content {#define-lp-specific-content}

To define specific content that will enable users to select and submit their choices from your landing page, follow the steps below.

1. **[!UICONTROL Form]**

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >**[!UICONTROL Form]**

1. Select it. **[!UICONTROL Form content]**

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >**[!UICONTROL Form style]** [Ulteriori informazioni](#define-lp-styles)

1. **[!UICONTROL Checkbox 1]**

1. Define if this checkbox is to opt users in or out: do they agree to receive communications or do they ask not to be contacted any more?

   ![](assets/lp_designer-form-update.png)

1. Choose what will be updated between the three following options:

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Subscription list]** [](subscription-list.md)

      ![](assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Channel (email)]** For example, if a profile that opts out has two email addresses, both addresses will be excluded from all your communications.

   * **[!UICONTROL Email identity]** For example, if a profile has two email addresses, only the one that was used to opt in will receive communications from your brand.

1. **[!UICONTROL Add field]****[!UICONTROL Checkbox]** Repeat the steps above to define its properties.

   ![](assets/lp_designer-form-checkbox-2.png)

1. **[!UICONTROL Call to action]** **[!UICONTROL Form]**

   ![](assets/lp_designer-form-call-to-action.png)

1. Define what will happen upon clicking the button:

   * **[!UICONTROL Redirect URL]**
   * **[!UICONTROL Confirmation text]**
   * **[!UICONTROL Link to a subpage]**[](create-lp.md#configure-subpages)

   ![](assets/lp_designer-form-confirmation-action.png)

1. Define what will happen upon clicking the button in case an error occurs:

   * **[!UICONTROL Redirect URL]**
   * **[!UICONTROL Error text]** [](#define-lp-styles)

   * **[!UICONTROL Link to a subpage]**[](create-lp.md#configure-subpages)

   ![](assets/lp_designer-form-error.png)

1. **[!UICONTROL Opt in]****[!UICONTROL Opt out]**

   ![](assets/lp_designer-form-additionnal-update.png)

1. [](create-lp.md#configure-primary-page)

   ![](assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## Define landing page form styles {#define-lp-styles}

1. **[!UICONTROL Form style]**

   ![](assets/lp_designer-form-style.png)

1. **[!UICONTROL Checkboxes]** For example, you can adjust the font family or size, and the checkbox border color.

   ![](assets/lp_designer-form-style-checkboxes.png)

1. **[!UICONTROL Buttons]** For example, you can add a border, edit the label color on hover, or adjust the alignement of the button.

   ![](assets/lp_designer-form-style-buttons.png)

   **[!UICONTROL Preview]** [](create-lp.md#test-landing-page)

   ![](assets/lp_designer-form-style-buttons-preview.png)

1. **[!UICONTROL Form layout]**

   ![](assets/lp_designer-form-style-layout.png)

1. **[!UICONTROL Form error]** Check the corresponing option to preview the error text on the form.

   ![](assets/lp_designer-form-error-preview.png)

