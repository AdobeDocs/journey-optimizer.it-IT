---
solution: Journey Optimizer
product: journey optimizer
title: Personalizzare il contenuto in Journey Optimizer
description: Guida introduttiva alla personalizzazione.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Guida introduttiva alla personalizzazione{#add-personalization}

Scopri [!DNL Adobe Journey Optimizer] funzionalità di personalizzazione per adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni disponibili su di essi. Può essere il loro nome, i loro interessi, dove vivono, quello che hanno comprato, e altro ancora.

➡️ [Scopri come personalizzare un messaggio in questi video](#video-perso)
➡️ [Scopri i casi d’uso che sfruttano la personalizzazione](personalization-use-case.md)

## Creare espressioni di personalizzazione utilizzando una sintassi dedicata {#syntax}

[!DNL Journey Optimizer] utilizza un **inline** semplice sintassi di personalizzazione basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe e doppie **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. Ulteriori informazioni in [Sintassi di personalizzazione](personalization-syntax.md).

**Esempi:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Durante l’elaborazione del messaggio (e-mail e push), Journey Optimizer sostituisce l’espressione con i dati contenuti nel database Experience Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` diventa &quot;Ciao John Doe&quot;.

## Utilizza i dati del profilo per personalizzare i messaggi {#data}

La personalizzazione si basa sui dati del profilo gestiti dal **Profilo individuale XDM** schema definito in Adobe Experience Platform. Ulteriori informazioni in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

>[!CAUTION]
>La **Profilo individuale XDM** schema è l’unico schema utilizzabile per personalizzare il contenuto in [!DNL Journey Optimizer].

## Aggiungi personalizzazione in contesti diversi {#contexts}

[!DNL Journey Optimizer] ti consente di personalizzare il contenuto e la visualizzazione dei messaggi in diversi modi. Ulteriori informazioni sui contesti in cui puoi eseguire la personalizzazione in [questa sezione](personalization-contexts.md).

## Utilizzare l’editor di espressioni {#editor}

[!DNL Journey Optimizer] fornisce un editor di espressioni in cui selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione personalizzata per il contenuto.

Sono disponibili diversi strumenti per creare contenuti di personalizzazione (funzioni di supporto, libreria di espressioni predefinite, preferiti attributi).

Ulteriori informazioni [!DNL Journey Optimizer] editor di espressioni in [questa sezione](personalization-build-expressions.md)

## Video dimostrativi{#video-perso}

Scopri come utilizzare le informazioni sugli eventi contestuali di un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Scopri come aggiungere a un messaggio una personalizzazione basata su profili e come utilizzare l’appartenenza a un segmento come condizione preliminare per un blocco di personalizzazione.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
