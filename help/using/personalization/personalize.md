---
solution: Journey Optimizer
product: journey optimizer
title: Personalizzare i contenuti in Journey Optimizer
description: Introduzione alla personalizzazione.
feature: Personalization
topic: Personalization
role: Developer
level: Beginner
keywords: espressione, editor, start, personalization
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 25%

---

# Introduzione alla personalizzazione{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalizzare le esperienze"
>abstract="Utilizza **Adobe Journey Optimizer** per adattare i messaggi a ogni destinatario sfruttando i dati e le informazioni di cui disponi. Ad esempio, il nome del destinatario, i suoi interessi, dove vive, cosa ha comprato e altro ancora."

Le funzionalità di personalizzazione di [!DNL Adobe Journey Optimizer] consentono di adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni disponibili su di essi. Ad esempio, il nome del destinatario, i suoi interessi, dove vive, cosa ha comprato e altro ancora.

## Come funziona la personalizzazione

Utilizzando l&#39;**editor personalizzazione**, puoi selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione personalizzata per il contenuto e utilizzare vari strumenti, come funzioni di assistenza o espressioni predefinite, per personalizzare i messaggi in modo efficace.

Journey Optimizer utilizza una sintassi di personalizzazione in linea basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe **`{{}}`**.

Durante l’elaborazione del messaggio, Journey Optimizer sostituisce l’espressione con i dati contenuti nel set di dati di Experience Platform. `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`, ad esempio, diventa `Hello John Doe` in modo dinamico.

Utilizzando questa sintassi, puoi personalizzare i messaggi in più campi, tra cui righe dell’oggetto e-mail, corpo del messaggio, notifiche push o URL.

## Dati utilizzati per la personalizzazione

Personalization si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Lo schema **Profilo individuale XDM** è l&#39;unico schema utilizzabile per personalizzare il contenuto in [!DNL Journey Optimizer]. Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

Puoi anche sfruttare **attributi calcolati** per personalizzare il contenuto. Gli attributi calcolati consentono di riepilogare i singoli eventi comportamentali in attributi di profilo calcolati disponibili in Adobe Experience Platform. [Scopri come utilizzare gli attributi calcolati](../audience/computed-attributes.md)

Inoltre, [!DNL Journey Optimizer] ti consente di sfruttare i dati provenienti da Adobe Experience Platform nell&#39;editor di personalizzazione per personalizzare il contenuto. A questo scopo, i set di dati necessari per la personalizzazione della ricerca devono prima essere abilitati tramite una chiamata API. Al termine, puoi utilizzare i loro dati per personalizzare il contenuto in Journey Optimizer. Questa funzione è attualmente disponibile in versione beta. [Ulteriori informazioni](../personalization/aep-data-perso.md)

## Scopri e sperimenta la personalizzazione {#playground}

**[!DNL Adobe Journey Optimizer]** include uno strumento interattivo progettato per aiutarti a imparare e sperimentare le funzionalità di personalizzazione.

Questo ambiente playground fornisce un ambiente simulato per scrivere e testare il codice di personalizzazione utilizzando dati di esempio senza richiedere set di dati live. Puoi sfruttare esempi di codice predefiniti, modificare payload di profilo fittizi e visualizzare in anteprima l’output del codice di personalizzazione in tempo reale.

![area di gioco personalizzazione](assets/playground.png)

➡️ [Accedi al playground di personalizzazione](https://experienceleague.adobe.com/it/apps/journey-optimizer/ajo-personalization){target="_blank"}

## Approfondiamo

Ora che conosci la personalizzazione in **[!DNL Journey Optimizer]**, è il momento di approfondire queste sezioni della documentazione per iniziare a lavorare con questa funzione.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="personalization-build-expressions.md">
<img alt="aggiungi personalizzazione" src="assets/do-not-localize/add.png">
</a>
<div>
<a href="personalization-build-expressions.md"><strong>Aggiungere la personalizzazione</strong></a>
</div>
<p>
</td>
<td>
<a href="../personalization/personalization-syntax.md">
<img alt="Lead" src="assets/do-not-localize/syntax.png">
</a>
<div><a href="../personalization/personalization-syntax.md"><strong>Sintassi Personalization</strong>
</div>
<p>
</td>
<td>
<a href="../personalization/functions/functions.md">
<img alt="Non frequente" src="assets/do-not-localize/functions.png">
</a>
<div>
<a href="../personalization/functions/functions.md"><strong>Elenco funzioni helper</strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-use-case.md">
<img alt="Non frequente" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-use-case.md"><strong>Casi di utilizzo di Personalization</strong></a>
</div>
<p></td>
</tr></table>

## Video sulle procedure{#video-perso}

Scopri come utilizzare le informazioni sugli eventi contestuali provenienti da un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Scopri come aggiungere a un messaggio la personalizzazione basata sul profilo e come utilizzare l’appartenenza a un pubblico come condizione preliminare di blocco della personalizzazione.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Scopri come sfruttare l’area di gioco dell’editor di personalizzazione per scrivere e testare il codice di personalizzazione utilizzando dati di esempio.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12)
