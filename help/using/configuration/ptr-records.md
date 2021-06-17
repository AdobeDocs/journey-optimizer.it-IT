---
title: Record PTR
description: '"Scopri come gestire i record ptr"'
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
role: Administrator
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 1%

---


# Record PTR

## Informazioni sui record PTR

Un record puntatore (PTR) è un tipo di record DNS (Domain Name System) che fornisce il nome di dominio collegato a un indirizzo IP.

Con i record PTR, i server di posta riceventi possono controllare l&#39;autenticità dei server di posta inviati identificando se i loro indirizzi IP corrispondono ai nomi con cui i server si connettono.

## Accedere ai record PTR dei tuoi sottodomini

Una volta delegato un sottodominio in Customer Journey Management, viene creato e associato automaticamente un record PTR a questo sottodominio. Puoi accedervi dal menu **[!UICONTROL Channels]** `>` **[!UICONTROL PTR records]** .

![](../assets/ptr-records.png)

L’elenco mostra i record PTR generati per ciascun sottodominio delegato, utilizzando la sintassi seguente:

* &quot;r&quot; per la registrazione,
* &quot;xx&quot; per le ultime due cifre dell’indirizzo IP,
* nome del sottodominio.

Puoi aprire un record PTR dall’elenco per visualizzare il nome del sottodominio e l’indirizzo IP associati.

>[!NOTE]
>
>I record PTR sono di sola lettura e non è possibile modificare il sottodominio associato a un indirizzo IP.
