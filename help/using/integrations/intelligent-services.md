---
solution: Journey Optimizer
product: journey optimizer
title: Integrare con Intelligent Services
description: Scopri come sfruttare le previsioni di Adobe Intelligent Services e Customer AI in Journey Optimizer
feature: Journeys, Integrations
topic: Artificial Intelligence
role: User
level: Intermediate
keywords: artificiale, AI, intelligente, percorso, servizio
exl-id: 20da09e1-0611-4d27-a589-30552011e06c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/rTKcWHwfwleQtD68fcdeqYK2AMQHVaknKtsNDFsOldI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# Integrare con i servizi intelligenti {#ai-overview}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come integrare Adobe Intelligent Services e le previsioni di IA per l&#39;analisi dei clienti con Journey Optimizer per utilizzare i punteggi di abbandono e conversione come attributi di profilo per il decisioning, le azioni e la creazione di segmenti.

>[!ENDSHADEBOX]

L&#39;integrazione con **[!DNL Adobe Intelligent Services]** consente di sfruttare l&#39;intelligenza artificiale e l&#39;apprendimento automatico per i casi di utilizzo dell&#39;esperienza del cliente. Questo consente agli analisti di marketing di impostare previsioni personalizzate in base alle esigenze di un’azienda utilizzando configurazioni a livello aziendale senza richiedere competenze in materia di data science.

[!DNL Intelligent Services], basato su [!DNL Adobe Experience Platform], fornisce AI-as-a-service per i team di customer experience. Consente di prevedere il comportamento dei clienti, misurare l’impatto delle campagne e migliorare il ritorno sull’investimento. Per ulteriori dettagli, consulta la [[!DNL Adobe Experience Platform] documentazione](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/home.html?lang=it){target="_blank"}.

L&#39;integrazione tra [!DNL Journey Optimizer] e [!DNL Intelligent Services] consente di sfruttare le previsioni dei clienti.

IA per l&#39;analisi dei clienti, un componente di [!DNL Adobe Intelligent Services], prevede azioni probabili dei clienti. Consulta la [[!DNL Adobe Experience Platform] documentazione](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/overview.html?lang=it){target="_blank"}.

IA per l’analisi dei clienti consente ai brand di creare punteggi basati sull’apprendimento automatico di abbandono o conversione. Questi punteggi sono disponibili come attributi di profilo nei profili [!DNL Adobe Experience Platform] (Profilo cliente in tempo reale).

Di conseguenza, questi attributi possono essere utilizzati come qualsiasi altro attributo di profilo in Journey Optimizer. Utilizzali in condizioni per il decisioning, le azioni o la creazione di segmenti.

![Integrazione di IA per l&#39;analisi dei clienti con punteggi e previsioni di propensione](assets/customer-ai.png)

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

- **TL;DR:** Questa pagina spiega come Journey Optimizer si integra con Adobe Intelligent Services, in particolare IA per l&#39;analisi dei clienti, per sfruttare i punteggi di propensione basati sull&#39;apprendimento automatico come attributi di profilo nei percorsi.

**Intenti:**
- Comprendere come Adobe Intelligent Services si integra con Journey Optimizer
- Utilizzare i punteggi di propensione di Customer AI come attributi di profilo in condizioni o azioni di percorso
- Previsioni basate sull’intelligenza artificiale per abbandono o conversione senza richiedere competenze in materia di data science
- Applicare i punteggi di apprendimento automatico alla creazione di segmenti in Journey Optimizer

**Glossario:**
- **Adobe Intelligent Services**: una suite di servizi di IA/ML basati su Adobe Experience Platform che consente di prevedere l&#39;esperienza del cliente senza richiedere competenze di data science *(specifico per prodotto)*
- **Customer AI**: componente di Adobe Intelligent Services che genera punteggi di propensione di abbandono o conversione basati sull&#39;apprendimento automatico per i profili cliente *(specifici per prodotto)*
- **Punteggio tendenza**: un punteggio basato sull&#39;apprendimento automatico che rappresenta la probabilità che un cliente esegua un&#39;azione specifica (ad esempio abbandono o conversione), memorizzata come attributo di profilo *(specifico per prodotto)*

**Guardrail:**
- Non è richiesta alcuna competenza in materia di data science, ma la configurazione a livello aziendale deve essere completata da analisti di marketing
- I punteggi di Customer AI devono essere configurati in Adobe Experience Platform prima di poter essere disponibili come attributi di profilo in Journey Optimizer

**Terminologia:**
- Nome canonico: Adobe Intelligent Services — Acronimo: none — varianti: Intelligent Services, servizi di intelligenza artificiale
- Nome canonico: IA per l’analisi dei clienti — Acronimo: none — varianti: punteggi di analisi dei clienti, punteggi di tendenza
- Sinonimi: &quot;churn score&quot; = &quot;churn proppensity&quot; ; &quot;conversion score&quot; = &quot;conversion propensity&quot;
- Non confondere: &quot;Adobe Intelligent Services&quot; ≠ &quot;AI Assistant&quot; (Intelligent Services è una piattaforma ML predittiva; AI Assistant è un’interfaccia di conversazione)

**Domande frequenti:**
- **D: Cos&#39;è IA per l&#39;analisi dei clienti nel contesto di Journey Optimizer?** — IA per l&#39;analisi dei clienti è un componente di Adobe Intelligent Services che crea punteggi di abbandono o conversione basati sull&#39;apprendimento automatico, disponibili come attributi di profilo utilizzabili nelle condizioni, nelle azioni e nella creazione di segmenti di Journey Optimizer.
- **D: sono necessarie competenze di data science per utilizzare Adobe Intelligent Services?** — No, gli analisti di marketing possono configurare le previsioni utilizzando impostazioni a livello aziendale senza richiedere competenze in materia di data science.
- **Q: dove sono memorizzati i punteggi di IA per l&#39;analisi dei clienti?** — Vengono memorizzati come attributi di profilo nel profilo cliente in tempo reale di Adobe Experience Platform, rendendoli accessibili come qualsiasi altro attributo di profilo in Journey Optimizer.
- **Q: come posso utilizzare i punteggi di Customer AI in un percorso?** — una volta disponibili come attributi di profilo, i punteggi possono essere utilizzati in condizioni per il processo decisionale, in configurazioni di azione o per la creazione di segmenti di pubblico.

+++
