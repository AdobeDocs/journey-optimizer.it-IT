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
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1403
ht-degree: 11%

---

# Introduzione alla personalizzazione{#add-personalization}

>[!BEGINSHADEBOX]

**In questa pagina:** Inizia a usare la personalizzazione in Adobe Journey Optimizer, incluso il funzionamento dell&#39;editor di personalizzazione, i dati del profilo che puoi utilizzare, la playground di apprendimento e la modifica in linea.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalizzare le esperienze"
>abstract="Utilizza **Adobe Journey Optimizer** per adattare i messaggi a ogni destinatario sfruttando i dati e le informazioni di cui disponi. Ad esempio, il nome del destinatario, i suoi interessi, dove vive, cosa ha comprato e altro ancora."

Le funzionalità di personalizzazione di [!DNL Adobe Journey Optimizer] consentono di adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni disponibili su di essi. Ad esempio, il nome del destinatario, i suoi interessi, dove vive, cosa ha comprato e altro ancora.

## Come funziona la personalizzazione

Utilizzando l&#39;**editor personalizzazione**, puoi selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione personalizzata per il contenuto e utilizzare vari strumenti, come funzioni di assistenza o espressioni predefinite, per personalizzare i messaggi in modo efficace.

Journey Optimizer utilizza una sintassi di personalizzazione in linea basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe **`{{}}`**.

Durante l’elaborazione del messaggio, Journey Optimizer sostituisce l’espressione con i dati contenuti nel set di dati di Experience Platform. `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`, ad esempio, diventa `Hello John Doe` in modo dinamico. Utilizzando questa sintassi, puoi personalizzare i messaggi in più campi, tra cui righe dell’oggetto e-mail, corpo del messaggio, notifiche push o URL.

## Dati utilizzati per la personalizzazione

Personalization si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Lo schema **Profilo individuale XDM** è l&#39;unico schema utilizzabile per personalizzare il contenuto in [!DNL Journey Optimizer]. Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

Puoi anche sfruttare **attributi calcolati** per personalizzare il contenuto. Gli attributi calcolati consentono di riepilogare i singoli eventi comportamentali in attributi di profilo calcolati disponibili in Adobe Experience Platform. [Scopri come utilizzare gli attributi calcolati](../audience/computed-attributes.md)

Inoltre, [!DNL Journey Optimizer] ti consente di sfruttare i dati provenienti da Adobe Experience Platform nell&#39;editor di personalizzazione per personalizzare il contenuto. A questo scopo, i set di dati necessari per la personalizzazione della ricerca devono prima essere abilitati tramite una chiamata API. Al termine, puoi utilizzare i loro dati per personalizzare il contenuto in Journey Optimizer. Questa funzione è attualmente disponibile in versione beta. [Ulteriori informazioni](../personalization/aep-data-perso.md)

## Scopri e sperimenta la personalizzazione {#playground}

**[!DNL Adobe Journey Optimizer]** include uno strumento interattivo progettato per aiutarti a imparare e sperimentare le funzionalità di personalizzazione.

Questo ambiente playground fornisce un ambiente simulato per scrivere e testare il codice di personalizzazione utilizzando dati di esempio senza richiedere set di dati live. Puoi sfruttare esempi di codice predefiniti, modificare payload di profilo fittizi e visualizzare in anteprima l’output del codice di personalizzazione in tempo reale.

![area di gioco personalizzazione](assets/playground.png)

➡️ [Accedi al playground di personalizzazione](https://experienceleague.adobe.com/it/apps/journey-optimizer/ajo-personalization){target="_blank"}

## Assistente IA per le espressioni di personalizzazione {#ai-personalization-expressions}

In **[!UICONTROL Personalization Editor]** o nella barra degli strumenti di E-mail Designer (**[!UICONTROL Aggiungi espressione]**), **[!UICONTROL AI Assistant]** ti consente di generare nuove espressioni dal linguaggio naturale, spiegare cosa fa il codice esistente e risolvere i problemi in una selezione, quindi applicare l&#39;output quando corrisponde alle tue intenzioni.

![](../content-management/assets/ai-perso-generate.png)

➡️ [Scopri come utilizzare l&#39;Assistente all&#39;intelligenza artificiale per le espressioni di Personalization](../content-management/generative-personalization-expressions.md)

## Modifica in linea degli attributi del profilo {#inline-personalization}

È possibile inserire espressioni di attributi di profilo direttamente durante la modifica del contenuto nell&#39;editor **E-mail Designer** o nell&#39;editor **Canale push**, senza aprire l&#39;editor di personalizzazione completo.

Per farlo, segui questi passaggi:

1. Digitare `{{` in qualsiasi campo di testo. Viene visualizzato un menu a discesa di completamento automatico in linea in corrispondenza della posizione del cursore.
1. Inizia a digitare per filtrare gli attributi di profilo disponibili.
1. Seleziona l’attributo necessario: viene inserito come token di personalizzazione in corrispondenza della posizione del cursore.

![](assets/inline-profile-attributes.png)

## Argomenti di approfondimento

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
<a href="../personalization/personalization-recipes.md">
<img alt="Non frequente" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-recipes.md"><strong>Ricette Personalization</strong></a>
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

## Video dimostrativi{#video-perso}

Scopri come utilizzare le informazioni sugli eventi contestuali provenienti da un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Scopri come aggiungere a un messaggio la personalizzazione basata sul profilo e come utilizzare l’appartenenza a un pubblico come condizione preliminare di blocco della personalizzazione.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Scopri come sfruttare l’area di gioco dell’editor di personalizzazione per scrivere e testare il codice di personalizzazione utilizzando dati di esempio.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12)

Esplora altri tutorial video sulle funzioni di personalizzazione e sulle best practice in [esercitazioni di Personalization](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/personalize-content/personalization-editor-overview){target="_blank"}

## Riferimento rapido {#quick-reference}

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

>[!BEGINTABS]

>[!TAB Panoramica]

**TL;DR**

Questa pagina introduce la personalizzazione in Journey Optimizer: il funzionamento dell’editor di personalizzazione basato su Handlebars, quali dati utilizza, l’area di riproduzione interattiva, l’Assistente AI per le espressioni e la modifica degli attributi in linea nell’editor Designer e-mail e push.

**Intenti**

* Comprendere come funziona la personalizzazione Journey Optimizer (sintassi Handlebars con doppie parentesi graffe)
* Identifica le origini dati disponibili per la personalizzazione (schema Profilo individuale XDM, attributi calcolati, ricerca di set di dati AEP in versione beta)
* Sperimenta la personalizzazione utilizzando il parco giochi interattivo senza una sandbox live
* Utilizza l’Assistente AI per generare, spiegare o correggere espressioni di personalizzazione dal linguaggio naturale
* Inserire gli attributi del profilo in linea nel Designer e-mail o nell&#39;editor push digitando `{{`

>[!TAB Glossario]

* **Editor Personalization**: strumento completo per la creazione, la personalizzazione e la convalida delle espressioni di personalizzazione, disponibile in qualsiasi campo di Journey Optimizer che supporta la personalizzazione. *(specifico per prodotto)*
* **Schema profilo individuale XDM**: unico schema che può essere utilizzato per personalizzare il contenuto in Journey Optimizer; definisce tutti gli attributi di profilo disponibili per la personalizzazione. *(specifico per prodotto)*
* **Attributi calcolati**: attributi di profilo precalcolati che riepilogano singoli eventi comportamentali in valori a livello di profilo; disponibili come dati di personalizzazione insieme ai campi di profilo XDM standard. *(specifico per prodotto)*
* **Ambiente playground di Personalization**: un ambiente interattivo simulato su Experience League per la scrittura e il test del codice di personalizzazione con dati di esempio, senza set di dati o sandbox live. *(specifico per prodotto)*
* **Modifica in linea**: possibilità di digitare `{{` in qualsiasi campo di testo nel Designer e-mail o nell&#39;editor di canali push per attivare un menu a discesa di completamento automatico e inserire attributi di profilo senza aprire l&#39;editor di personalizzazione completo. *(specifico per prodotto)*
* **Assistente IA (espressioni di personalizzazione)**: strumento di IA nell&#39;editor di personalizzazione e in E-mail Designer che genera espressioni di personalizzazione dal linguaggio naturale, spiega il codice esistente e risolve i problemi in una selezione. *(specifico per prodotto)*

>[!TAB Terminologia]

* **Nome canonico:** personalizzazione — varianti: personalizzazione contenuto, personalizzazione messaggio, personalizzazione espressione
* **Nome canonico:** editor di personalizzazione — varianti: funzionalità di personalizzazione
* **Non confondere:** l&#39;editor di Personalization (utilizzato per creare espressioni di contenuto nei messaggi e nelle offerte, supporta sia Handlebars che PQL) ≠ l&#39;editor di espressioni avanzate (utilizzato nel percorso per condizioni su origini dati e informazioni sugli eventi, attività di attesa personalizzate e mappatura dei parametri delle azioni) fornisce funzioni e operatori incorporati diversi da quelli dell&#39;editor di personalizzazione
* **Non confondere:** modifica in linea (tipo `{{` in E-mail Designer o Push per l&#39;inserimento rapido degli attributi senza aprire l&#39;editor completo) ≠ editor di personalizzazione (strumento completo per espressioni complesse, funzioni di supporto, regole condizionali e frammenti)
* **Non confondere:** schema Profilo individuale XDM (l&#39;unico schema utilizzabile per la personalizzazione in Journey Optimizer) ≠ altri schemi AEP (non utilizzabile per la personalizzazione a meno che non sia esposto tramite la ricerca del set di dati)

>[!TAB Guardrail e limitazioni]

* Lo schema Profilo individuale XDM è l’unico schema che può essere utilizzato per personalizzare il contenuto in Journey Optimizer.
* La ricerca di set di dati di AEP per la personalizzazione richiede che i set di dati siano abilitati tramite una chiamata API prima dell’uso; questa funzione è attualmente in versione beta.
* La modifica in linea (digitando `{{` in E-mail Designer o nell&#39;editor push) supporta solo gli attributi del profilo.

>[!TAB Domande frequenti]

**D: quali dati possono essere utilizzati per la personalizzazione in Journey Optimizer?**

Dati profilo dallo schema Profilo individuale XDM, attributi calcolati (eventi comportamentali riepilogati a livello di profilo) e ricerca di set di dati di record AEP (attualmente beta, richiede che i set di dati siano abilitati tramite API).

**D: Cos&#39;è il parco giochi di personalizzazione?**

Ambiente interattivo e simulato su Experience League in cui puoi scrivere e testare il codice di personalizzazione utilizzando dati di esempio, senza richiedere una sandbox live di Journey Optimizer o set di dati reali.

**D: come funziona la modifica degli attributi in linea?**

Digitare `{{` in qualsiasi campo di testo nel Designer e-mail o nell&#39;editor di canali push per aprire un menu a discesa di completamento automatico nella posizione del cursore. Inizia a digitare per filtrare gli attributi del profilo, quindi selezionane uno per inserirlo come token di personalizzazione. Solo gli attributi del profilo sono disponibili in linea.

**D: cosa può fare l&#39;Assistente AI nell&#39;editor di personalizzazione?**

Può generare nuove espressioni di personalizzazione dalle descrizioni del linguaggio naturale, spiegare cosa fa il codice esistente e risolvere i problemi in un’espressione selezionata, quindi applicare l’output quando corrisponde all’intento.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 248b894f -->
