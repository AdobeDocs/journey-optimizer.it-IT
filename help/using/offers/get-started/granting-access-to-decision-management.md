---
title: Concedere l’accesso a Offer Decisioning
description: Scopri come gestire le autorizzazioni degli utenti per il servizio Offer Decisioning tramite Adobe Admin Console
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 2a2fece9-1ad5-498e-b0ee-5bb0b73a2cd5
source-git-commit: 0545cda9f91ff18791310a4ee2463b2287ac7557
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 7%

---

# Concedere l’accesso alla gestione delle decisioni {#granting-acess-to-decision-management}

Le autorizzazioni per accedere e utilizzare le funzionalità di offer decisioning vengono gestite utilizzando [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Per concedere l&#39;accesso alla funzionalità Gestione delle decisioni, devi creare un **[!UICONTROL Product profile]** e assegna le autorizzazioni corrispondenti ai tuoi utenti. Ulteriori informazioni sulla gestione [!DNL Journey Optimizer] utenti e autorizzazioni in [questa sezione](../../administration/permissions.md).

Le autorizzazioni specifiche di Gestione delle decisioni sono elencate in [questa sezione](../../administration/high-low-permissions.md#manage-decisioning).

<!--If you are a [!DNL Journey Optimizer] user leveraging the **Decision Management** functionality, you need to have the [Decision management permissions](../../administration/high-low-permissions.md#decisions-permissions) enabled to acces all related capabilities. Learn more on managing [!DNL Journey Optimizer] users and permissions in [this section](../../administration/permissions.md).

If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service, follow the steps [below](#granting-acess-to-offer-decisioning) to grant access to [!DNL Offer Decisioning].

Grant access to Offer Decisioning

The steps below only apply to **Experience Platform users** leveraging the [!DNL Offer Decisioning] service.-->

1. Apri [Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html), quindi seleziona **[!UICONTROL Adobe Experience Platform]**.

   <!--![](../../assets/offers_admin_console.png)-->

1. Vengono visualizzati i profili di prodotto del servizio. Per creare un nuovo profilo di prodotto, fai clic sul pulsante **[!UICONTROL New Profile]** pulsante .

   ![](../../assets/offers_rights_productprofile.png)

   >[!NOTE]
   >
   >Puoi avere tutti i profili di prodotto desiderati, corrispondenti ai vari ruoli che desideri impostare per la tua organizzazione.

1. Specifica il nome e la descrizione del profilo di prodotto, quindi fai clic su **[!UICONTROL Next]**.

   ![](../../assets/create-product-profile.png)

   <!--To access the product profile’s permissions, select the **[!UICONTROL Permissions]** line.-->

1. Seleziona i servizi da abilitare per il profilo di prodotto. Per impostazione predefinita, sono selezionati tutti i servizi, il che è consigliato per garantire la disponibilità di tutte le funzionalità di Experience Platform.

   ![](../../assets/enable-services.png)

1. In **[!UICONTROL Decision Management]** fai clic sulla sezione **+** per assegnare le autorizzazioni al profilo di prodotto, quindi fai clic su **[!UICONTROL Save]**.

   ![](../../assets/configure-profile.png)

   Le autorizzazioni disponibili sono:

   **[!UICONTROL Manage Decisioning Activities]**

   * Lettura, scrittura, eliminazione offerte
   * Lettura, scrittura, eliminazione delle decisioni (precedentemente note come attività di offerta)
   * Lettura, scrittura, eliminazione posizionamenti

   **[!UICONTROL Execute Decisioning Activities]**:

   * Leggi le offerte
   * Leggi le decisioni
   * Lettura dei posizionamenti

   **[!UICONTROL Manage Decisioning Options]**:

   * Lettura, scrittura, eliminazione offerte
   * Leggi le decisioni
   * Lettura, scrittura, eliminazione posizionamenti



1. Viene visualizzato un riepilogo delle autorizzazioni del profilo di prodotto. Ora puoi assegnare gli utenti al profilo di prodotto in modo che accedano a queste autorizzazioni.

   ![](../../assets/product-profile-created.png)

>[!NOTE]
>
>Per ulteriori dettagli su come gestire le autorizzazioni degli utenti, consulta la [Documentazione di Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

