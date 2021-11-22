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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 26%

---

# Aggiungere un record TXT di Google a un sottodominio

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da sorgenti esterne.

Al fine di garantire il buon recapito dei messaggi e la corretta consegna delle e-mail agli indirizzi Gmail, la Gestione dei Percorsi dei clienti ti consente di aggiungere ai sottodomini record TXT di Google specifici per la verifica del sito, in modo da verificarli.

>[!NOTE]
>
> Questa operazione può essere eseguita solo una volta che un sottodominio ha **[!UICONTROL Success]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).

Per aggiungere un record TXT di Google al sottodominio, effettua le seguenti operazioni:

1. Apri il sottodominio da **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** menu.

1. Nella sezione TXT record di Google, immetti il codice di verifica generato in [Strumenti di amministrazione di G Suite](https://support.google.com/a/answer/183895?hl=it), quindi fai clic su **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Una volta aggiunto il record TXT, è necessario che sia verificato da Google. A questo scopo, accedi agli strumenti di amministrazione di G Suite e avvia il passaggio di verifica.
