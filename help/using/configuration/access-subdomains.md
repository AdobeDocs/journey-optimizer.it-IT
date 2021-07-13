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
source-wordcount: '163'
ht-degree: 6%

---


# Accedere ai sottodomini delegati

Tutti i sottodomini delegati vengono visualizzati nel menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** . Sono disponibili filtri per facilitare la definizione dell’elenco (data di delega, utente o stato).

![](../assets/subdomain-list.png)

La colonna **[!UICONTROL Status]** fornisce informazioni sul processo di delega del sottodominio:

* **[!UICONTROL Draft]**: La delega del sottodominio è stata salvata come bozza. Fai clic sul nome del sottodominio per riprendere il processo di delega,
* **[!UICONTROL Processing]**: Il sottodominio sta effettuando diversi controlli di configurazione prima di poter essere utilizzato,
* **[!UICONTROL Success]**: Il sottodominio ha superato i controlli con successo e può essere utilizzato per inviare messaggi,
* **[!UICONTROL Failed]**: Uno o più controlli non sono riusciti dopo l’invio della delega del sottodominio.

Per accedere a informazioni dettagliate su un sottodominio, aprilo dall’elenco. È possibile:

* Recupera il nome del sottodominio (sola lettura) configurato durante il processo di delega, nonché gli URL generati (risorse, pagine mirror, URL di tracciamento),

* Aggiungi un record TXT di Google per la verifica del sito al tuo sottodominio per assicurarti che sia verificato (consulta [Aggiungi un record TXT di Google a un sottodominio](google-txt.md)).

![](../assets/subdomain-delegated.png)
