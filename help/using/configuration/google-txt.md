---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un record TXT di Google a un sottodominio
description: Scopri come aggiungere un record TXT di Google a un sottodominio
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 21%

---

# Aggiungere un record TXT di Google a un sottodominio {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Record TXT di Google"
>abstract="Per garantire la corretta consegna delle e-mail agli indirizzi Gmail, puoi aggiungere al sottodominio record TXT di Google per la verifica del sito per assicurarti che sia verificato."

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da origini esterne.

Al fine di garantire un recapito messaggi ottimale e la corretta consegna delle e-mail agli indirizzi Gmail, [!DNL Journey Optimizer] consente di aggiungere al sottodominio record TXT di Google per la verifica del sito per assicurarti che sia verificato.

>[!CAUTION]
>
> Questa operazione può essere eseguita solo una volta che un sottodominio ha **[!UICONTROL Completato]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).

Per aggiungere un record TXT di Google al sottodominio, effettua le seguenti operazioni:

1. Apri il sottodominio da **[!UICONTROL Canali]** / **[!UICONTROL Sottodomini]** menu.

1. In **[!UICONTROL Record TXT di Google]** immettere il codice di verifica generato da [Area di lavoro Google](https://support.google.com/a/answer/183895?hl=it){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, quindi fai clic su **[!UICONTROL Salva]**.

   ![](assets/subdomain-google-txt.png)

1. Una volta aggiunto il record TXT, è necessario che sia verificato da Google. Per eseguire questa operazione, passa a [Area di lavoro Google](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, quindi avvia il passaggio di verifica.
