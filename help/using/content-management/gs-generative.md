---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione all’assistente IA
description: Scopri come accedere e lavorare con l’assistente IA di Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 267d1850cbe30b1078f3b5b5bd228364bb63edd6
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 100%

---

# Introduzione all’assistente IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Assistente IA"
>abstract="Dopo aver creato e personalizzato la consegna, puoi utilizzare l’Assistente IA per migliorare i contenuti. Questa funzione semplifica il processo di personalizzazione e miglioramento dei contenuti consentendoti di perfezionarli descrivendo cosa desideri generare."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Definire il contesto con l’Assistente IA"
>abstract="Per utilizzare il contenuto selezionato come input per la generazione di contenuto, attiva il pulsante **Usa contenuto originale**. Puoi anche caricare le risorse del brand per utilizzarle come origine. Se non utilizzi il contenuto selezionato, è obbligatorio caricare e selezionare le risorse di un brand."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Termini sull’intelligenza artificiale generativa di Adobe"
>abstract="L’accesso a questa funzione è soggetto al consenso delle linee guida per l’utente sull’intelligenza artificiale generativa di Adobe Experience Cloud. Controlla l’accuratezza degli output generati da questa funzione e assicurati che siano appropriati al tuo caso d’uso."
>additional-url="https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Linee guida per l’utente sull’intelligenza artificiale generativa di Adobe"

>[!BEGINSHADEBOX]

**Sommario**

* Introduzione all’assistente IA
* [Generazione di e-mail con l’assistente IA](generative-email.md)
* [Generazione di SMS con l’assistente IA](generative-sms.md)
* [Generazione di push con l’assistente IA](generative-push.md)
* [Esperimento contenuti con l’assistente IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>L’assistente IA in Adobe Journey Optimizer è attualmente disponibile come versione beta solo per alcuni utenti.

L’Assistente IA in Adobe Journey Optimizer, basato su tecnologia Azure OpenAI, offre suggerimenti proattivi per la variazione dei contenuti per testo e immagini. È disponibile per i canali e-mail, push e SMS. Questa nuova funzionalità fornisce una generazione di testo e immagini basata su prompt. La generazione di immagini è gestita con Adobe Firefly.

Utilizza l’assistente IA di Journey Optimizer per ottimizzare l’impatto del messaggio sperimentando con diversi titoli principali e immagini. Genera più varianti e crea un esperimento per confrontarle. Sfruttando l’esperimento con contenuti di Journey Optimizer, puoi definire più trattamenti per i messaggi al fine di misurare quale funziona meglio per il tuo pubblico di destinazione. Puoi scegliere di variare il contenuto della consegna o l’oggetto. Il pubblico del messaggio viene allocato in modo casuale a ciascun trattamento per determinare quale funziona meglio nei termini della metrica specificata. Per ulteriori informazioni sull’esperimento contenuti, consulta [questa sezione](../content-management/content-experiment.md).

## Guardrail e limitazioni {#generative-guardrails}

Di seguito sono elencate alcune linee guida generali su come utilizzare l’assistente IA in Journey Optimizer per la generazione di e-mail:

* La qualità del contenuto generato è fortemente influenzata dall’obiettivo/prompt di marketing che definisci. Utilizza un prompt ben definito per interpretare con precisione il modello GenAI. 
* Carica la risorsa del brand in modo che sia accurata per il relativo contenuto. Altrimenti, il contenuto si basa su informazioni disponibili pubblicamente. Il contenuto caricato può essere nei seguenti formati: file PDF, JPEG, PNG o ZIP (con formati di file supportati).
* La dimensione massima per risorsa del marchio caricata è 50 MB.È possibile utilizzare anche file di dimensioni maggiori o numerose immagini, ma questo comporterà tempi di elaborazione più lunghi.
* Per creare il contenuto dell’e-mail, utilizza un modello e-mail creato in Adobe Campaign, preferibilmente uno dei [modelli e-mail incorporati](../email/use-email-templates.md), un modello specifico del marchio o un modello personalizzato. Si consiglia di utilizzare un modello e-mail con un massimo di 8-10 immagini.
* Assicurati di segnalare eventuali output problematici utilizzando le icone con il pollice su, il pollice giù o un flag durante la selezione delle varianti.
* L’utilizzo dell’assistente IA è soggetto alle linee guida per l’utente sull’intelligenza artificiale generativa di Adobe Experience Cloud. [Ulteriori informazioni](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

All’assistente IA in Journey Optimizer si applicano le seguenti limitazioni:

* È supportata solo la lingua inglese.
* È disponibile solo per il canale e-mail, push e SMS.
* Il contenuto GenAI potrebbe non risultare sempre accurato: condividi il tuo feedback in modo che i nostri tecnici possano perfezionare i modelli.
* Puoi caricare più risorse del marchio, ma puoi sfruttarne una sola per una generazione specifica.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="Generazione di e-mail" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>Generazione di e-mail</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="Generazione di SMS" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>Generazione di SMS</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Generazione di push" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Generazione di notifiche push</strong></a>
</div>
<p></td>
</tr></table>
