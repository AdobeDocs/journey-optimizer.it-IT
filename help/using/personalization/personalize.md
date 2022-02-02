---
title: Personalizzare i contenuti in Journey Optimizer
description: Introduzione alla personalizzazione
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: bd4a66d4d0c280c83b37241ccba53843b9442509
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 38%

---

# Guida introduttiva alla personalizzazione{#add-personalization}

Scopri [!DNL Adobe Journey Optimizer] funzionalità di personalizzazione per adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni disponibili su di essi. Può essere il loro nome, i loro interessi, dove vivono, quello che hanno comprato, e altro ancora.

➡️ [Scopri come personalizzare un messaggio in questi video](#video-perso)

[!DNL Journey Optimizer] utilizza un **inline** semplice sintassi di personalizzazione basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe e doppie **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. Ulteriori informazioni in [Sintassi di personalizzazione](personalization-syntax.md).

La personalizzazione si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Ulteriori informazioni in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}.

>[!CAUTION]
>La **Profilo individuale XDM** schema è l’unico schema utilizzabile per personalizzare il contenuto in [!DNL Journey Optimizer].

**Esempi:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Durante l’elaborazione del messaggio (e-mail e push), Journey Optimizer sostituisce l’espressione con i dati contenuti nel database di Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` diventa &quot;Ciao John Doe&quot;.

## Video sulle procedure{#video-perso}

Scopri come utilizzare le informazioni sugli eventi contestuali provenienti da un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Scopri come utilizzare le informazioni sugli eventi contestuali provenienti da un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
