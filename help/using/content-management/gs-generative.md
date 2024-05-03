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
source-git-commit: 98ce21578d30ac50665561438715d19d1723f4a7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 65%

---

# Introduzione all’assistente IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_content_generation"
>title="Creare il contenuto dell’e-mail"
>abstract="L’assistente IA di Adobe Journey Optimizer offre suggerimenti proattivi per varianti di contenuto per testo e immagini. È disponibile per i canali e-mail, push, SMS e web. Questa nuova funzionalità fornisce una generazione di testo e immagini basata su prompt."

>[!BEGINSHADEBOX]

**Sommario**

* **[Introduzione all’Assistente IA](gs-generative.md)**
* [Generazione di e-mail con l’Assistente IA](generative-email.md)
* [Generazione di SMS con l’Assistente IA](generative-sms.md)
* [Generazione push con l’Assistente AI](generative-push.md)
* [Esperimento sui contenuti con l’Assistente AI](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>L’assistente IA di Adobe Journey Optimizer è attualmente disponibile come versione beta solo per alcuni utenti. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.

L’assistente IA di Adobe Journey Optimizer offre suggerimenti proattivi per varianti di contenuto per testo e immagini. È disponibile per i canali e-mail, push e SMS. Questa nuova funzionalità fornisce una generazione di testo e immagini basata su prompt. La generazione di immagini è gestita con Adobe Firefly.

Utilizza l’assistente IA di Journey Optimizer per ottimizzare l’impatto del messaggio sperimentando con diversi titoli principali e immagini. Genera più varianti e crea un esperimento per confrontarle. Sfruttando l’esperimento con contenuti di Journey Optimizer, puoi definire più trattamenti per i messaggi al fine di misurare quale funziona meglio per il tuo pubblico di destinazione. Puoi scegliere di variare il contenuto della consegna o l’oggetto. Il pubblico del messaggio viene allocato in modo casuale a ciascun trattamento per determinare quale funziona meglio nei termini della metrica specificata. Per ulteriori informazioni sull’esperimento contenuti, consulta [questa sezione](../campaigns/content-experiment.md).

## Guardrail e limitazioni {#generative-guardrails}

Di seguito sono elencate le linee guida generali per l’utilizzo dell’Assistente IA in Journey Optimizer per la generazione di e-mail:

* La qualità del contenuto generato è fortemente influenzata dalla finalità dell’iniziativa di marketing e dal prompt che inserisci nelle impostazioni. Inserisci un prompt chiaro e preciso nelle impostazioni, per consentire al modello GenAI di interpretarle con precisione. 
* Per ottenere contenuti accurati e in linea con i requisiti del marchio, carica una risorsa del marchio. In caso contrario, il contenuto verrà generato sulla base di informazioni di pubblico dominio. Puoi caricare contenuti nei seguenti formati: file PDF, immagini JPEG o PNG, o file ZIP (contenenti formati di file supportati).
* La dimensione massima per la risorsa del brand caricata è di 50 MB.È possibile utilizzare anche file di dimensioni maggiori o numerose immagini, ma questo comporterà tempi di elaborazione più lunghi.
* Utilizza un modello e-mail creato da Adobe Campaign, preferibilmente [modelli e-mail incorporati](../email/use-email-templates.md), modello specifico per il brand o modello personalizzato per creare il contenuto delle e-mail. Si consiglia di utilizzare un modello e-mail con un massimo di 8-10 immagini.
* Assicurati di segnalare eventuali output problematici utilizzando le icone thumb up, thumb down o flag durante la selezione delle varianti.
* L’utilizzo dell’assistente IA è soggetto alle linee guida per l’utente di Adobe Experience Cloud Generative AI. [Ulteriori informazioni](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Le seguenti limitazioni si applicano all’Assistente IA in Journey Optimizer:

* La lingua supportata è solo inglese.
* Disponibile solo per i canali e-mail, push e SMS.
* Il contenuto GenAI potrebbe non essere sempre accurato: condividi il tuo feedback in modo che i nostri ingegneri possano perfezionare i modelli.
* Puoi caricare più risorse per il brand, ma puoi sfruttarne una sola per una generazione specifica.

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
<img alt="Generazione push" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Generazione di notifiche push</strong></a>
</div>
<p></td>
</tr></table>
