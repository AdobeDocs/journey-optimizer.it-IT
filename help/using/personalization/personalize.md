---
title: Personalizzare i contenuti in Journey Optimizer
description: Introduzione alla personalizzazione
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 49%

---

# Guida introduttiva alla personalizzazione{#add-personalization}

![](../assets/do-not-localize/badge.png)

Scopri le funzionalità di personalizzazione di Percorsi Optimier per adattare i tuoi messaggi a ogni destinatario specifico sfruttando i dati e le informazioni che hai su di lui/lei. Può essere il suo nome, i suoi interessi, dove vive, quello che ha comprato, e altro ancora.

Journey Optimizer utilizza una sintassi di personalizzazione **inline** semplice basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. Ulteriori informazioni sono disponibili in [Sintassi di personalizzazione](personalization-syntax.md).

La personalizzazione si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Per ulteriori informazioni, consulta la documentazione di [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).

>[!CAUTION]
>Lo schema **XDM Singolo profilo** è l’unico schema utilizzabile per personalizzare il contenuto in Journey Optimizer.

**Esempi:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Durante l’elaborazione del messaggio (e-mail e push), Journey Optimizer sostituisce l’espressione con i dati contenuti nel database di Experience Cloud Platform.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
