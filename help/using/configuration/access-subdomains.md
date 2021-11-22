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
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 4%

---

# Accedere ai sottodomini delegati

Tutti i sottodomini delegati vengono visualizzati nella sezione **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** menu. Sono disponibili filtri per facilitare la definizione dell’elenco (data di delega, utente o stato).

![](../assets/subdomain-list.png)

La **[!UICONTROL Status]** La colonna fornisce informazioni sul processo di delega del sottodominio:

* **[!UICONTROL Draft]**: La delega del sottodominio è stata salvata come bozza. Fai clic sul nome del sottodominio per riprendere il processo di delega,
* **[!UICONTROL Processing]**: Il sottodominio sta effettuando diversi controlli di configurazione prima di poter essere utilizzato,
* **[!UICONTROL Success]**: Il sottodominio ha superato i controlli con successo e può essere utilizzato per inviare messaggi,
* **[!UICONTROL Failed]**: Uno o più controlli non sono riusciti dopo l’invio della delega del sottodominio.

Per accedere a informazioni dettagliate su un sottodominio, aprilo dall’elenco. È possibile:

* Recupera il nome del sottodominio (sola lettura) configurato durante il processo di delega, nonché gli URL generati (risorse, pagine mirror, URL di tracciamento),

* Aggiungi un record TXT di Google per la verifica del sito al tuo sottodominio per assicurarti che sia verificato (vedi [Aggiungere un record TXT di Google a un sottodominio](google-txt.md)).

![](../assets/subdomain-delegated.png)
