---
title: Delega sottodomini
description: Scopri come delegare i sottodomini
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Impostazioni applicazione
topic: Amministrazione
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 27%

---


# Aggiungere un record TXT di Google a un sottodominio

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da sorgenti esterne.

Al fine di garantire un buon recapito dei messaggi e la corretta consegna delle e-mail agli indirizzi Gmail, la Gestione dei Percorsi dei clienti ti consente di aggiungere ai sottodomini record TXT di Google specifici per la verifica del sito, in modo da verificarli.

>[!NOTE]
>
> Questa operazione può essere eseguita solo dopo che un sottodominio ha lo stato **[!UICONTROL Success]** . Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).

Per aggiungere un record TXT di Google al tuo sottodominio, segui questi passaggi:

1. Apri il sottodominio dal menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** .

1. Nella sezione TXT di Google, inserisci il codice di verifica generato in [G Suite Admin Tools](https://support.google.com/a/answer/183895?hl=it), quindi fai clic su **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Una volta aggiunto il record TXT, è necessario che sia verificato da Google. A questo scopo, accedi agli strumenti di amministrazione di G Suite e avvia il passaggio di verifica.
