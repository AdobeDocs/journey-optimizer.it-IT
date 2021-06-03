---
title: Record PTR
description: Scopri come xxxx
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
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# Record PTR

## Informazioni sui record PTR

Un record puntatore (PTR) è un tipo di record DNS (Domain Name System) che fornisce il nome di dominio collegato a un indirizzo IP.

Con i record PTR, i server di posta riceventi possono controllare l&#39;autenticità dei server di posta inviati identificando se i loro indirizzi IP corrispondono ai nomi con cui i server si connettono.

## Accedere ai record PTR dei tuoi sottodomini

Una volta delegato un sottodominio in Customer Journey Management, viene creato e associato automaticamente un record PTR a questo sottodominio. Puoi accedervi dal menu **[!UICONTROL Channels]** / **[!UICONTROL PTR records]** .

![](../assets/ptr-records.png)

L’elenco mostra i record PTR generati per ciascun sottodominio delegato, utilizzando la sintassi seguente:

* &quot;r&quot; per la registrazione,
* &quot;xx&quot; per le ultime due cifre dell’indirizzo IP,
* nome del sottodominio.

Puoi aprire un record PTR dall’elenco per visualizzare il nome del sottodominio e l’indirizzo IP associati.

>[!NOTE]
>
>I record PTR sono di sola lettura e non è possibile modificare il sottodominio associato a un indirizzo IP.
