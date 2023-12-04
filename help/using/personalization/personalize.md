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
source-git-commit: 9ac8a3ddad165f728c09baacb9d380d4611fd58a
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 33%

---

# Introduzione alla personalizzazione{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalizzare le esperienze"
>abstract="Utilizza **Adobe Journey Optimizer** per adattare i messaggi a ogni destinatario sfruttando i dati e le informazioni di cui disponi. Ad esempio, il nome del destinatario, i suoi interessi, dove vive, cosa ha comprato e altro ancora."

Scoprire [!DNL Adobe Journey Optimizer] funzionalità di personalizzazione per adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni di cui disponi su di essi. Ad esempio, il nome del destinatario, i suoi interessi, dove vive, cosa ha comprato e altro ancora.

➡️ [Scopri come personalizzare un messaggio in questi video](#video-perso)
➡️ [Scopri i casi d’uso che sfruttano la personalizzazione](personalization-use-case.md)

## Creare espressioni di personalizzazione utilizzando una sintassi dedicata {#syntax}

[!DNL Journey Optimizer] utilizza un **in linea** sintassi di personalizzazione semplice basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. Ulteriori informazioni in [Sintassi di personalizzazione](personalization-syntax.md).

**Esempi:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Durante l’elaborazione del messaggio (e-mail e push), Journey Optimizer sostituisce l’espressione con i dati contenuti nel database di Experienci Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` diventa Hello John Doe.

## Sfruttare i dati del profilo per personalizzare i messaggi {#data}

La personalizzazione si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Ulteriori informazioni in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

>[!CAUTION]
>Il **Profilo individuale XDM** schema è l’unico schema che puoi utilizzare per personalizzare il contenuto in [!DNL Journey Optimizer].

Inoltre, puoi anche sfruttare **attributi calcolati** per personalizzare il contenuto. Gli attributi calcolati si basano sui set di dati Experience Event abilitati per il profilo acquisiti in Adobe Experience Platform e fungono da punti di dati aggregati memorizzati nei profili dei clienti che riepilogano i singoli eventi comportamentali [Scopri come utilizzare gli attributi calcolati](../audience/computed-attributes.md)

## Aggiungere personalizzazione in contesti diversi {#contexts}

[!DNL Journey Optimizer] consente di personalizzare il contenuto e la visualizzazione dei messaggi in diversi modi. Ulteriori informazioni sui contesti in cui eseguire la personalizzazione in [questa sezione](personalization-contexts.md).

## Utilizzare l’editor di espressioni {#editor}

[!DNL Journey Optimizer] fornisce un editor di espressioni in cui puoi selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione personalizzata per il contenuto.

Sono disponibili diversi strumenti per creare i contenuti di personalizzazione, ad esempio: funzioni di contorno, libreria di espressioni predefinite, preferenza per gli attributi e altro ancora.

Ulteriori informazioni su [!DNL Journey Optimizer] editor di espressioni in [questa sezione](personalization-build-expressions.md)

## Video sulle procedure{#video-perso}

Scopri come utilizzare le informazioni sugli eventi contestuali provenienti da un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Scopri come personalizzare un profilo di base con un messaggio e come utilizzare l’appartenenza a un pubblico come condizione preliminare di blocco della personalizzazione.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

