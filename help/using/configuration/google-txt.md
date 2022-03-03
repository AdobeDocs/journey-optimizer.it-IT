---
title: Aggiungere un record TXT di Google a un sottodominio
description: Scopri come aggiungere un record TXT di Google a un sottodominio
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 7c9f04b8d3faa171444bfa0adc537b5faabde37e
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 26%

---

# Aggiungere un record TXT di Google a un sottodominio {#google-txt-record}

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da sorgenti esterne.

Al fine di garantire il buon recapito dei messaggi e la corretta consegna delle e-mail agli indirizzi Gmail, [!DNL Journey Optimizer] consente di aggiungere ai sottodomini record TXT di Google per la verifica del sito, in modo da verificarne la validità.

>[!CAUTION]
>
> Questa operazione può essere eseguita solo una volta che un sottodominio ha **[!UICONTROL Success]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).

Per aggiungere un record TXT di Google al sottodominio, effettua le seguenti operazioni:

1. Apri il sottodominio da **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** menu.

1. In **[!UICONTROL Google txt record]** immettere il codice di verifica generato da [Area di lavoro Google](https://support.google.com/a/answer/183895?hl=it){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, quindi fai clic su **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. Una volta aggiunto il record TXT, è necessario che sia verificato da Google. Per eseguire questa operazione, passa a [Area di lavoro Google](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, quindi avvia il passaggio di verifica.
