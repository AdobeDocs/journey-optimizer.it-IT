---
title: Personalizzare i contenuti in Journey Optimizer
description: Guida introduttiva alla personalizzazione
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

---

# Introduzione {#add-personalization}

![](../assets/do-not-localize/badge.png)

La personalizzazione, nel contesto di Journey Optimizer, è l’azione di indirizzare un messaggio a un abbonato specifico sfruttando i dati e le informazioni che hai su di lui. Può essere il suo nome, i suoi interessi, dove vive, e molto altro.

Journey Optimizer utilizza una **sintassi di personalizzazione inline** semplice basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. Fai riferimento a [Sintassi di personalizzazione](personalization-syntax.md).

La personalizzazione si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Per ulteriori informazioni, consulta la documentazione [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).

>[!CAUTION]
>Lo schema **XDM Singolo profilo** è l’unico che puoi utilizzare per personalizzare il contenuto in Journey Optimizer.

**Esempi:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Durante l&#39; **elaborazione dei messaggi** (e-mail e push), l&#39;espressione viene sostituita con i dati contenuti nei database della piattaforma Experience Cloud.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
