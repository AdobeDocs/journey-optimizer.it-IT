---
solution: Journey Optimizer
product: Journey Optimizer
title: Funzionalità di intelligenza artificiale in Adobe Journey Optimizer
description: Funzionalità di intelligenza artificiale in Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 9d0460d303a3701ad7ff5b7f2487ac6ccdd6facd
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 3%

---

# Funzionalità di intelligenza artificiale in Adobe Journey Optimizer{#section-overview}

Adobe Journey Optimizer sfrutta la potenza dell’intelligenza artificiale e dell’apprendimento automatico per trasformare il modo in cui crei, ottimizza e distribuisci le esperienze dei clienti. Dalla generazione di contenuti personalizzati su più canali alla previsione del tempo ottimale per coinvolgere i clienti, le funzionalità di intelligenza artificiale semplificano il flusso di lavoro e massimizzano l’impatto. Questa sezione illustra come le funzioni basate sull’intelligenza artificiale collaborano per aiutarti a prendere decisioni più intelligenti, automatizzare attività complesse e creare esperienze che risuonino davvero con il tuo pubblico. Che tu stia sfruttando l’intelligenza artificiale generativa per la creazione di contenuti, utilizzando modelli predittivi per il processo decisionale o ottimizzando i tempi di invio per un coinvolgimento migliore, scoprirai strumenti e strategie pratici per sfruttare appieno il potenziale dell’intelligenza artificiale nell’orchestrazione del percorso del cliente.

## Funzioni basate sull’intelligenza artificiale

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/sparkles.svg)

Assistente IA per la generazione di contenuti

Sfrutta l’intelligenza artificiale generativa per creare e personalizzare contenuti per e-mail, SMS, notifiche push, pagine web e pagine di destinazione.

[Esplora Assistente IA](ai-assistant-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=it)

Ottimizzazione dei tempi di invio

Utilizza l’intelligenza artificiale per prevedere il tempo ottimale per l’invio dei messaggi e massimizzare il coinvolgimento dei clienti in base al comportamento storico.

[Informazioni Sull’Ottimizzazione Dell’Ora Di Invio](../using/building-journeys/send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

Modelli IA per decisioning

Crea modelli di ottimizzazione automatica e personalizzata per classificare e offrire le offerte migliori ai tuoi clienti.

[Scopri i modelli AI](ai-models-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/help.svg)

Conoscenza del prodotto di AI Assistant

Ottieni risposte immediate e informazioni operative su Adobe Journey Optimizer utilizzando l’intelligenza artificiale per conversazioni.

[Utilizzare l’Assistente IA](../using/start/ai-assistant.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/experiment.svg)

Sperimentazione dei contenuti con IA

Genera più varianti di contenuto ed esegui esperimenti per identificare il contenuto con le prestazioni migliori per il tuo pubblico.

[Scopri la sperimentazione sull’intelligenza artificiale](../using/content-management/generative-experimentation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/user-group.svg?lang=it)

Integrazione di Customer AI

Integra con Adobe Intelligent Services per prevedere il comportamento dei clienti e utilizzare i punteggi di abbandono e conversione nei tuoi percorsi.

[Esplora Intelligent Services](../using/building-journeys/ai-services-overview.md)
:::

::::


## Risorse aggiuntive

- **[Punteggio di allineamento del brand](../using/content-management/brands-score.md)**: valuta se i contenuti generati dall’intelligenza artificiale si allineano alle linee guida del brand utilizzando il punteggio basato sull’intelligenza artificiale.
- **[Acceleratore esperimento](../using/content-management/experiment-accelerator-gs.md)**: accelera il processo di sperimentazione dei contenuti con consigli e informazioni basate sull’intelligenza artificiale.
- **[API basate sull&#39;intelligenza artificiale](../using/configuration/ajo-apis.md)**: accedi alle funzionalità di intelligenza artificiale e machine learning di Journey Optimizer a livello di programmazione tramite API.

## Domande frequenti

+++**Quali autorizzazioni sono necessarie per utilizzare le funzionalità di intelligenza artificiale?**

Per utilizzare l&#39;Assistente AI per la generazione di contenuti, agli utenti deve essere concessa l&#39;autorizzazione **Genera contenuto**. Questa autorizzazione viene assegnata tramite la risorsa Assistente IA nel prodotto Autorizzazioni. Per utilizzare l’Assistente all’intelligenza artificiale per conoscere il prodotto e ottenere informazioni operative, gli utenti devono accettare le linee guida per gli utenti di Adobe Experience Cloud Generative AI.

[Ulteriori informazioni sulle autorizzazioni](../using/administration/ootb-permissions.md)

+++

+++**Quali canali supportano la generazione di contenuti dell&#39;Assistente IA?**

L&#39;Assistente IA per la generazione di contenuti è disponibile per i canali **E-mail**, **Push**, **SMS** e **Web**. Attualmente non è disponibile per i canali Direct Mail, Content Card, LINE o WhatsApp.

+++

+++**Quali sono le best practice per l&#39;utilizzo dell&#39;Assistente di intelligenza artificiale?**

- **Utilizza prompt ben definiti** - La qualità del contenuto generato è fortemente influenzata dalla finalità di marketing e dal prompt. Siate precisi e chiari.
- **Carica risorse marchio** - Fornisci risorse marchio in formato PDF, JPEG, PNG o ZIP (massimo 50 MB) per contenuti precisi nel marchio.
- **Utilizza modelli personalizzati**: sfrutta modelli e-mail specifici per il tuo marchio con un massimo di 8-10 immagini per ottenere risultati ottimali.
- **Fornisci feedback** - Segnala gli output problematici utilizzando icone con miniature in alto, miniature in basso o flag per perfezionare i modelli.
- **Sfrutta una sola risorsa per marchio per generazione**: anche se puoi caricare più risorse, usane una sola per ogni generazione specifica.

[Ulteriori informazioni sui guardrail dell’assistente di intelligenza artificiale](../using/content-management/gs-generative.md#generative-guardrails)

+++

+++**Quali sono le best practice per l&#39;ottimizzazione dell&#39;ora di invio?**

- **Attendi 30 giorni**. Utilizza le azioni E-mail e push per almeno 30 giorni prima di abilitare Ottimizzazione del tempo di invio per garantire una raccolta di dati sufficiente.
- **Scegliere tempi di attesa ottimali** - Impostare un tempo di attesa massimo compreso tra 6 e 24 ore per ottenere risultati ottimali. Durate più brevi limitano il potenziale di ottimizzazione; periodi più lunghi possono causare messaggi obsoleti.
- **Ottimizza per la metrica corretta** - Per le e-mail, ottimizza per i clic durante l&#39;azione oppure Apre per il contenuto informativo. I messaggi push sono sempre ottimizzati per Opens.
- **Evita l&#39;invio di messaggi sensibili al tempo** - Non utilizzare l&#39;ottimizzazione del tempo di invio per messaggi operativi urgenti quali conferme di ordini, reimpostazioni di password o notifiche di volo. Ideale per comunicazioni di marketing come promozioni e newsletter.
- **Pianifica invii mattutini per push** - Per evitare notifiche notturne, pianifica invii batch push al mattino con durate più brevi (ad esempio, 9 invio con attesa di 8 ore).

[Ulteriori informazioni sull’ottimizzazione dell’ora di invio](../using/building-journeys/send-time-optimization.md)

+++

+++**Quali sono i limiti dell&#39;ottimizzazione dell&#39;ora di invio?**

- **Canali** - Disponibile solo per i canali di notifica e-mail e push in Percorsi. Non disponibile nelle campagne o tramite azioni personalizzate.
- **Disponibilità** - Deve essere abilitata dall&#39;Assistenza clienti di Adobe o dal tuo rappresentante Adobe.
- **Periodo di formazione** - Richiede almeno 30 giorni di dati storici e-mail o push prima dell&#39;utilizzo.
- **Apprendimento del modello** - I modelli vengono inizialmente addestrati settimanalmente utilizzando le ultime 16 settimane di dati, quindi vengono riformati mensilmente.
- **Esplorazione e ottimizzazione**: il 5% dei messaggi riceve tempi di invio di esplorazione casuali; il 95% riceve tempi di invio ottimizzati.

+++

+++**Quali sono le limitazioni per i modelli AI in Decisioning?**

- **Numero massimo di modelli AI** - Fino a 5 modelli di classificazione AI per organizzazione.
- **Requisiti del set di dati** - Almeno 2 offerte devono avere più di 100 eventi di visualizzazione e più di 5 eventi di clic negli ultimi 14 giorni per i modelli di ottimizzazione automatica.
- **Eventi di feedback** - Devono essere inviati come eventi di esperienza; non raccolti automaticamente nei canali Journey Optimizer.
- **Limitazioni API** - I modelli di ottimizzazione automatica non funzionano con l&#39;API Batch Decisioning (solo per la gestione delle decisioni).

[Ulteriori informazioni sui modelli di IA](../using/experience-decisioning/ranking/ai-models.md)

+++

+++**Quali guardrail si applicano alle decisioni basate sull&#39;intelligenza artificiale?**

| Componente | Limite |
|-----------|-------|
| Modelli di classificazione IA | 5 per organizzazione |
| Richieste di decisioni (basate su codice con segmentazione Edge) | 1.500 al secondo |
| Richieste di decisioni (basate su codice senza segmentazione di Edge) | 5.000 al secondo |
| Raccolte di elementi | 10.000 in totale |
| Elementi offerta per raccolta | 500 |
| Strategie di selezione per criterio di decisione | 10 |
| Elementi offerta restituiti per criterio di decisione | 30 |
| Regole di idoneità + formule di classificazione | 10.000 combinate |
| Attributi del profilo per regola | 25 |
| Attributi dei dati contestuali per regola | 30 |

[Ulteriori informazioni sui guardrail di decisioning](../using/experience-decisioning/decisioning-guardrails.md)

+++

+++**Devo accettare qualsiasi termine per utilizzare le funzionalità di intelligenza artificiale?**

Sì, è necessario accettare le [linee guida per l&#39;utente di Adobe Experience Cloud Generative AI](https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) prima di utilizzare l&#39;Assistente all&#39;intelligenza artificiale in Journey Optimizer. Per ulteriori informazioni, contatta il rappresentante Adobe. Inoltre, Adobe applica Content Credentials alle risorse generate da Firefly come parte del suo impegno per la trasparenza nell’utilizzo dell’intelligenza artificiale generativa.

+++

+++**I contenuti generati da IA sono sempre accurati?**

No. Il contenuto di IA generativa potrebbe non essere sempre accurato. Controlla sempre l’accuratezza degli output generati dall’intelligenza artificiale e assicurati che siano appropriati al tuo caso d’uso. Condividi il feedback utilizzando gli strumenti di valutazione forniti per aiutare gli ingegneri a perfezionare i modelli.

+++

