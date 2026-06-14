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
TQID: https://experienceleague.adobe.com/FCUB2NeETecjNGYnVhkpkYtEZqgX6y-czXinn2t3J84
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 25%

---

# Aggiungere un record TXT di Google a un sottodominio {#google-txt-record}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come aggiungere e aggiornare un record TXT di Google per la verifica del sito nel tuo sottodominio per garantire la corretta consegna delle e-mail agli indirizzi Gmail.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Record TXT di Google"
>abstract="Per garantire la corretta consegna delle e-mail agli indirizzi Gmail, puoi aggiungere al sottodominio specifici record TXT di Google per la verifica del sito per assicurarti che sia verificato."

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da origini esterne.

Per garantire il recapito ottimale delle e-mail e la corretta consegna delle e-mail agli indirizzi Gmail, [!DNL Journey Optimizer] ti consente di aggiungere al sottodominio record TXT di Google specifici per la verifica del sito per assicurarti che sia verificato.

>[!CAUTION]
>
> Questa operazione può essere eseguita solo dopo che un sottodominio ha lo stato **[!UICONTROL Operazione riuscita]**. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](delegate-subdomain.md#access-delegated-subdomains).

## Aggiungere un record TXT di Google {#add-google-txt-record}

Per aggiungere un record TXT di Google al sottodominio, effettua le seguenti operazioni:

1. Apri il sottodominio dal menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**.

1. Nella sezione **[!UICONTROL Record TXT di Google]** immettere il codice di verifica generato da [Google Workspace](https://support.google.com/a/answer/183895?hl=it){target="_blank"}<!--G Suite Admin tools-->, quindi fare clic su **[!UICONTROL Salva]**.

   ![](assets/subdomain-google-txt.png)

1. Una volta aggiunto il record TXT, è necessario che sia verificato da Google. A questo scopo, passa a [Google Workspace](https://support.google.com/a/answer/183895?hl=it){target="_blank"}<!--G Suite Admin tools-->, quindi avvia il passaggio di verifica.

## Aggiornare un record TXT di Google {#update-google-txt-record}

Per aggiornare un record TXT di Google esistente, effettua le seguenti operazioni:

1. Apri il sottodominio dal menu **[!UICONTROL Sottodomini]**.

1. Cancella il valore esistente nel campo **[!UICONTROL Record TXT di Google]** e fai clic su **[!UICONTROL Salva]**. Questo passaggio sostituisce il precedente valore del record TXT di Google con una stringa vuota.

1. Ora riapri lo stesso sottodominio e immetti il nuovo codice di verifica.

1. Fai di nuovo clic su **[!UICONTROL Salva]**.

1. Verificare il record aggiornato tramite [Google Workspace](https://support.google.com/a/answer/183895?hl=it){target="_blank"}.
