---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un record TXT di Google a un sottodominio
description: Scopri come aggiungere un record TXT di Google a un sottodominio
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, google, txt, record, gmail, recapito messaggi
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 30%

---

# Aggiungere un record TXT di Google a un sottodominio {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Record TXT di Google"
>abstract="Per garantire la corretta consegna delle e-mail agli indirizzi Gmail, puoi aggiungere al sottodominio specifici record TXT di Google per la verifica del sito per assicurarti che sia verificato."

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da origini esterne.

Per garantire il recapito ottimale delle e-mail e la corretta consegna delle e-mail agli indirizzi Gmail, [!DNL Journey Optimizer] ti consente di aggiungere al sottodominio record TXT di Google specifici per la verifica del sito per assicurarti che sia verificato.

>[!CAUTION]
>
> Questa operazione può essere eseguita solo dopo che un sottodominio ha lo stato **[!UICONTROL Operazione riuscita]**. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](about-subdomain-delegation.md#access-delegated-subdomains).

Per aggiungere un record TXT di Google al sottodominio, effettua le seguenti operazioni:

1. Apri il sottodominio dal menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**.

1. Nella sezione **[!UICONTROL Record TXT di Google]** immettere il codice di verifica generato da [Google Workspace](https://support.google.com/a/answer/183895?hl=it){target="_blank"}<!--G Suite Admin tools-->, quindi fare clic su **[!UICONTROL Salva]**.

   ![](assets/subdomain-google-txt.png)

1. Una volta aggiunto il record TXT, è necessario che sia verificato da Google. A questo scopo, passa a [Google Workspace](https://support.google.com/a/answer/183895?hl=it){target="_blank"}<!--G Suite Admin tools-->, quindi avvia il passaggio di verifica.
