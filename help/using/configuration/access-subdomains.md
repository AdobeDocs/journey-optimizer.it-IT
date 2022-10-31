---
solution: Journey Optimizer
product: journey optimizer
title: Accedere ai sottodomini delegati
description: Scopri come accedere ai sottodomini delegati.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 4%

---

# Accedere ai sottodomini delegati {#access-delegated-subdomains}

Tutti i sottodomini delegati vengono visualizzati nella sezione **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Sottodomini]** menu. Sono disponibili filtri per facilitare la definizione dell’elenco (data di delega, utente o stato).

![](assets/subdomain-list.png)

La **[!UICONTROL Stato]** La colonna fornisce informazioni sul processo di delega del sottodominio:

* **[!UICONTROL Bozza]**: La delega del sottodominio è stata salvata come bozza. Fai clic sul nome del sottodominio per riprendere il processo di delega,
* **[!UICONTROL Elaborazione]**: Il sottodominio sta effettuando diversi controlli di configurazione prima di poter essere utilizzato,
* **[!UICONTROL Completato]**: Il sottodominio ha superato i controlli con successo e può essere utilizzato per inviare messaggi,
* **[!UICONTROL Non riuscito]**: Uno o più controlli non sono riusciti dopo l’invio della delega del sottodominio.

Per accedere a informazioni dettagliate su un sottodominio con **[!UICONTROL Completato]** , aprilo dall&#39;elenco.

![](assets/subdomain-delegated.png)

Puoi eseguire le seguenti operazioni:

* Recupera il nome del sottodominio (sola lettura) configurato durante il processo di delega, nonché gli URL generati (risorse, pagine mirror, URL di tracciamento),

* Aggiungi un record TXT di Google per la verifica del sito al tuo sottodominio per assicurarti che sia verificato (vedi [Aggiungere un record TXT di Google a un sottodominio](google-txt.md)).


>[!CAUTION]
>
>La configurazione del sottodominio è comune a tutti gli ambienti. Pertanto, qualsiasi modifica apportata a un sottodominio influirà anche sulle sandbox di produzione.
