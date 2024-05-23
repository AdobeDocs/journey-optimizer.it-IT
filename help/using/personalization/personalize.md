---
solution: Journey Optimizer
product: journey optimizer
title: Personalizzare i contenuti in Journey Optimizer
description: Introduzione alla personalizzazione.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: espressione, editor, start, personalization
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 21%

---

# Introduzione alla personalizzazione{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalizzare le esperienze"
>abstract="Utilizzare **Adobe Journey Optimizer** adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni di cui si dispone su di essi. Può essere il nome, gli interessi, dove vivono, cosa hanno comprato e altro ancora."

Scoprire [!DNL Adobe Journey Optimizer] funzionalità di personalizzazione per adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni di cui disponi su di essi. Può essere il nome, gli interessi, dove vivono, cosa hanno comprato e altro ancora.

➡️ [Scopri come personalizzare un messaggio in questi video](#video-perso)
➡️ [Scopri i casi d’uso che sfruttano la personalizzazione](personalization-use-case.md)

## Creare espressioni di personalizzazione utilizzando una sintassi dedicata {#syntax}

[!DNL Journey Optimizer] utilizza un **in linea** sintassi di personalizzazione semplice basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. [Ulteriori informazioni sulla sintassi di personalizzazione](personalization-syntax.md).

**Esempi:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Durante l’elaborazione del messaggio (e-mail e push), Journey Optimizer sostituisce l’espressione con i dati contenuti nel database di Experienci Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` diventa Hello John Doe.

## Sfruttare i dati del profilo per personalizzare i messaggi {#data}

La personalizzazione si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Ulteriori informazioni in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

>[!CAUTION]
>Il **Profilo individuale XDM** schema è l’unico schema che puoi utilizzare per personalizzare il contenuto in [!DNL Journey Optimizer].

Inoltre, puoi anche sfruttare **attributi calcolati** per personalizzare il contenuto. Gli attributi calcolati si basano sui set di dati Experience Event abilitati per il profilo acquisiti in Adobe Experience Platform e fungono da punti di dati aggregati memorizzati nei profili dei clienti che riepilogano i singoli eventi comportamentali [Scopri come utilizzare gli attributi calcolati](../audience/computed-attributes.md)

## Utilizzare l’editor di personalizzazione {#editor}

[!DNL Journey Optimizer] fornisce un editor di personalizzazione in cui selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione personalizzata per il contenuto. Sono disponibili diversi strumenti per creare i contenuti di personalizzazione, ad esempio: funzioni di contorno, libreria di espressioni predefinite, preferenza per gli attributi e altro ancora.

* [Scopri come utilizzare l’editor di personalizzazione](personalization-build-expressions.md)
* [Scopri dove puoi eseguire la personalizzazione](personalization-contexts.md).

## Video sulle procedure{#video-perso}

Scopri come utilizzare le informazioni sugli eventi contestuali provenienti da un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Scopri come personalizzare un profilo di base con un messaggio e come utilizzare l’appartenenza a un pubblico come condizione preliminare di blocco della personalizzazione.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

