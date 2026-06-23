---
solution: Journey Optimizer
product: journey optimizer
title: Ricerca eventi esperienza in percorsi
description: Scopri come utilizzare la ricerca di eventi esperienza in percorsi
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/kVO36LmCfr9cYVq3EHRy8OpqPCZDq20mXTEA49TIRTI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: fa683eda-48de-4558-af32-2673edcd44fe
topic_v2:
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1717
ht-degree: 4%

---

# Ricerca eventi esperienza in percorsi {#ee-journeys}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri i pattern scalabili e le best practice per l&#39;utilizzo degli eventi di esperienza nei percorsi per eliminare, qualificare o personalizzare i profili in base al loro comportamento e agli attributi degli eventi.

>[!ENDSHADEBOX]

>[!CAUTION]
>
>A partire dall’8 luglio 2025, nelle nuove organizzazioni dei clienti, la creazione di espressioni utilizzando gli eventi di esperienza non è più supportata nell’editor di espressioni utilizzato nelle condizioni di percorso. Di conseguenza, gli eventi esperienza nell’[origine dati di Experience Platform](../datasource/adobe-experience-platform-data-source.md) non possono essere utilizzati per la creazione di espressioni.
>
>A partire dal 1° aprile 2026, l’utilizzo degli attributi dell’evento esperienza nelle espressioni di percorso non sarà più supportato per le organizzazioni che non hanno utilizzato questa funzionalità negli ultimi 90 giorni. Di seguito sono riportati approcci alternativi e best practice per la creazione di espressioni/logiche con eventi di esperienza.
>
>Hai bisogno di altri dettagli? [Consulta le domande frequenti](#faq-ee).

Questa pagina illustra i pattern comuni e gli approcci scalabili che consentono di sfruttare al meglio gli eventi esperienza in [!DNL Adobe Journey Optimizer]. Questi casi d’uso sono progettati per aiutarti a risolvere problemi frequenti come la gestione delle rinunce, il controllo della frequenza dei messaggi, la personalizzazione dei contenuti in base al comportamento degli utenti e la reazione ai segnali in tempo reale.

Sfruttando queste strategie, puoi trasformare i dati comportamentali in azioni significative, ossia eliminare, qualificare o escludere i profili in base agli eventi che attivano o agli attributi trasportati. Che tu stia creando una logica per le soglie di acquisto, i trigger di abbandono o la gestione dei mancati recapiti, questi esempi offrono indicazioni pratiche che puoi adattare alle tue esigenze.

Quando valuti quale approccio si adatta meglio, prendi in considerazione i requisiti di latenza del caso d’uso per garantire che i percorsi rimangano reattivi ed efficaci.

## Soppressione della rinuncia

Per eliminare i profili che hanno rinunciato alle comunicazioni di marketing, utilizza la gestione del consenso integrata. Le preferenze di rinuncia vengono acquisite automaticamente nei campi di consenso del profilo; è possibile farvi riferimento direttamente nelle condizioni di percorso e vengono applicate automaticamente da Journey Optimizer durante la consegna dei messaggi.

Ulteriori informazioni:

* [Gestire il consenso](../privacy/opt-out.md)
* [Gestione della rinuncia alle e-mail](../email/email-opt-out.md)
* [Gestione delle rinunce per i messaggi mobili](../mobile/mobile-opt-out.md)


## Soppressione basata su mancato recapito

Per escludere i profili che hanno riscontrato mancati recapiti e-mail, sfrutta l&#39;elenco di soppressione automatica di [!DNL Adobe Journey Optimizer] per gli indirizzi non recapitati. Questo meccanismo integrato garantisce che le e-mail non valide o non raggiungibili siano escluse da invii futuri senza richiedere una logica personalizzata.

Ulteriori informazioni:

* [Gestire l’elenco di soppressione](../configuration/manage-suppression-list.md)


## Soppressione generica

Per eliminare i profili che hanno dimostrato determinati comportamenti, utilizza tipi di pubblico in batch con logica basata su eventi per acquisire profili che soddisfano i criteri di eliminazione. Fai riferimento a questo pubblico in condizioni di percorso.

Ulteriori informazioni:

* [!DNL Adobe Experience Platform] [Generatore di segmenti - Eventi](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Generatore di segmenti - Vincoli di tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utilizzo dei tipi di pubblico nelle condizioni](../building-journeys/conditions.md#using-a-segment)

* [funzione inAudience()](../building-journeys/functions/functioninaudience.md)


## Esclusione di comunicazioni ricevute

Per evitare l’invio di messaggi a profili che hanno ricevuto comunicazioni in un intervallo di tempo recente:

* Utilizza i tipi di pubblico in batch con criteri basati sul tempo e farvi riferimento in condizioni di percorso.
* Applica le regole aziendali relative ai limiti di frequenza per applicare limiti giornalieri o settimanali ai messaggi.


Ulteriori informazioni sull’utilizzo dei tipi di pubblico:

* [!DNL Adobe Experience Platform] [Generatore di segmenti - Eventi](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Generatore di segmenti - Vincoli di tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utilizzo dei tipi di pubblico nelle condizioni](../building-journeys/conditions.md#using-a-segment)

* [funzione inAudience()](../building-journeys/functions/functioninaudience.md)


Vedi anche:

* [Quota limite per tipo di comunicazione e canale](../conflict-prioritization/channel-capping.md)



## Inclusione/esclusione specifica per il messaggio

Per includere o escludere i profili in base al fatto che abbiano ricevuto un messaggio specifico, crea tipi di pubblico in batch che incapsulano questa logica e vi fanno riferimento nelle condizioni di percorso.


Ulteriori informazioni:

* [!DNL Adobe Experience Platform] [Generatore di segmenti - Eventi](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Generatore di segmenti - Vincoli di tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utilizzo dei tipi di pubblico nelle condizioni](../building-journeys/conditions.md#using-a-segment)

* [funzione inAudience()](../building-journeys/functions/functioninaudience.md)

## Personalizzazione dell’abbandono del carrello o della navigazione

Per personalizzare le comunicazioni in base agli ultimi eventi del carrello o per sfogliare più tipi di carrello o visualizzazioni prodotto:

* Se hai accesso a [[!DNL Adobe Experience Platform] Data Distiller](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configura le query automatizzate per estrarre i dati richiesti dall&#39;evento, modificarli per adattarli al caso d&#39;uso e riscriverli in un [set di dati abilitato per il profilo](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} per l&#39;attivazione.
* Se i dati di abbandono possono essere modellati sul profilo con attributi scalari, considera l’utilizzo di Attributi calcolati per acquisire le informazioni più recenti e quindi fai riferimento a tali attributi nel percorso per costruire la comunicazione. [Ulteriori informazioni nella [!DNL Adobe Experience Platform] documentazione](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## Uscita dal percorso basata sul comportamento

Per rimuovere i profili dal percorso quando mostrano un comportamento particolare, utilizza i criteri di uscita per uscire dal profilo dal percorso quando viene ricevuto un evento particolare o il profilo si qualifica per un pubblico specifico.

Ulteriori informazioni:

* [Impostare le proprietà del percorso - Criteri di uscita](journey-properties.md#exit-criteria)

## Qualificazione basata sull&#39;acquisto con soglie di valore

Per attivare i percorsi basati sugli acquisti ed eliminare se il valore è superiore/inferiore a una soglia, definisci gli attributi calcolati per sommare gli acquisti in un periodo di tempo specifico. Crea un pubblico che includa profili il cui importo di spesa soddisfa determinati criteri.

Ulteriori informazioni:

* [!DNL Adobe Experience Platform] [Panoramica attributi calcolati](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Domande frequenti {#faq-ee}

Queste domande frequenti si concentrano sulla timeline per il ritiro dell’utilizzo degli eventi esperienza nelle espressioni di percorso e su chi è interessato. Per informazioni su approcci alternativi, consulta i casi d’uso e le best practice di cui sopra.

Hai bisogno di altri dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [[!DNL Adobe Journey Optimizer] community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=it){target="_blank"}.

+++Quali funzionalità specifiche sono interessate? 

È interessata solo la ricerca di eventi di esperienza nell’editor espressioni. Le seguenti funzionalità sono **non** interessate e rimangono le stesse:

* Osservare gli eventi esperienza associati a un profilo specifico nell’interfaccia utente del profilo

* Utilizzo degli eventi di esperienza nelle regole di attributi calcolati e accesso agli attributi calcolati in un percorso

* Attivazione di un percorso con un evento unitario o di business

* Utilizzo dei dati contestuali del percorso dagli eventi che attivano il percorso negli editor di espressioni e personalizzazione

* Ascolto di un evento all’interno di un percorso

* Configurazione degli eventi per attivare un percorso

* Rilevamento di eventi di reazione dell’utente finale alle comunicazioni di marketing (ad esempio, e-mail aperta)

+++

+++Questo aggiornamento influisce sulla mia organizzazione Adobe esistente?

A partire dall’8 luglio 2025, le nuove organizzazioni dei clienti non possono creare espressioni utilizzando gli attributi dell’evento esperienza. A partire dal 1° aprile 2026, le organizzazioni che non hanno effettuato l’accesso a eventi di esperienza tramite espressioni di percorso negli ultimi 90 giorni non avranno più accesso a questa funzionalità.

+++

+++Ho una nuova organizzazione Adobe. Come posso risolvere il mio caso d’uso che richiede dati sull’evento esperienza? 

Sono disponibili qui sopra approcci alternativi e best practice che coinvolgono eventi di esperienza per ottenere i casi d’uso desiderati.

+++

+++ Cosa succede se gli approcci alternativi non funzionano per il mio caso d’uso?

Se il tuo caso d’uso non può essere risolto utilizzando uno degli approcci alternativi elencati sopra, contatta il tuo rappresentante Adobe.

+++

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina sono illustrati modelli alternativi e best practice per l&#39;utilizzo dei dati di Experience Event nei percorsi Adobe Journey Optimizer, nel contesto della deprecazione della ricerca diretta degli eventi di esperienza nell&#39;editor di espressioni di percorso.

**Intenti:**

* Eliminare i profili con rinuncia utilizzando la gestione del consenso integrata invece delle espressioni dell’evento esperienza
* Escludere gli indirizzi e-mail non recapitati utilizzando l’elenco di soppressione automatica di AJO
* Creare una logica di soppressione generica utilizzando tipi di pubblico in batch con criteri basati su eventi
* Previeni le comunicazioni eccessive applicando regole di quota limite o condizioni di pubblico basate sul tempo
* Personalizzare le comunicazioni abbandonate nel carrello o sfogliare utilizzando gli attributi AEP Data Distiller o Computed

**Glossario:**

* **Evento esperienza**: record immutabile con marca temporale di un&#39;azione o di un comportamento del cliente archiviato in Adobe Experience Platform *(specifico per prodotto)*
* **Attributo calcolato**: attributo a livello di profilo derivato dall&#39;aggregazione o dal riepilogo dei dati dell&#39;evento esperienza nel tempo, disponibile per l&#39;utilizzo nelle espressioni di percorso *(specifiche per prodotto)*
* **Elenco di soppressione**: l&#39;elenco predefinito di indirizzi e-mail di AJO è stato automaticamente escluso da invii futuri a causa di mancati recapiti permanenti o reclami di spam *(specifico per prodotto)*
* **Limite di frequenza**: una regola business che limita il numero di messaggi che un profilo può ricevere entro un intervallo di tempo definito *(specifico per prodotto)*
* **Data Distiller**: funzionalità di AEP che consente alle query batch basate su SQL di estrarre e trasformare i dati evento in set di dati abilitati per il profilo *(specifici per prodotto)*

**Guardrail:**

* A partire dall’8 luglio 2025, le nuove organizzazioni dei clienti non possono creare espressioni utilizzando gli attributi dell’evento esperienza nell’editor di espressioni di percorso.
* A partire dal 1° aprile 2026, le organizzazioni che non hanno utilizzato gli attributi dell’evento esperienza nelle espressioni di percorso negli ultimi 90 giorni non potranno più accedere a questa funzionalità.
* La ricerca diretta degli eventi esperienza nelle condizioni di percorso viene ritirata; le alternative includono tipi di pubblico in batch, attributi calcolati e AEP Data Distiller.
* Le funzionalità NON influenzate dal ritiro includono: attivazione di percorsi con eventi, ascolto di eventi all&#39;interno di un percorso, utilizzo di dati contestuali di percorso da eventi trigger, configurazione di eventi e rilevamento di eventi di reazione.

**Terminologia:**

* Nome canonico: Ricerca evento esperienza — Acronimo: Ricerca EE — varianti: Espressioni evento esperienza, Ricerca attributo evento
* Sinonimi: &quot;pubblico batch con logica basata su eventi&quot; = &quot;segmento basato su eventi&quot; come meccanismo di soppressione/inclusione
* Non confondere: &quot;experience event lookup in expression editor&quot; ≠ &quot;triggering a percorsi with an event&quot; — attivazione di percorsi con eventi NON ritirata

**Domande frequenti:**

* **Q: posso ancora attivare un percorso utilizzando un evento esperienza?** — Sì, il cambiamento non influisce sull&#39;attivazione di percorsi con eventi unitari o di business.
* **D: qual è la sostituzione consigliata per la ricerca degli eventi esperienza nelle condizioni di percorso?** utilizzo di tipi di pubblico in batch generati con logica basata su eventi di AEP Segment Builder, attributi calcolati o AEP Data Distiller per trasformazioni complesse.
* **Q: interessa la mia organizzazione esistente al momento?** — Nuove organizzazioni interessate dall’8 luglio 2025. A partire dal 1° aprile 2026, le organizzazioni esistenti verranno interessate solo se non hanno utilizzato la funzionalità negli ultimi 90 giorni.
* **D: come posso gestire la personalizzazione dell&#39;abbandono del carrello senza una ricerca diretta degli eventi?** utilizzo di AEP Data Distiller per estrarre e scrivere dati evento in un set di dati abilitato per il profilo oppure utilizzo di attributi calcolati per acquisire lo stato di abbandono più recente nel profilo.
* **D: quali funzionalità NON sono interessate da questa deprecazione?** non influisce sui percorsi che attivano eventi, che ascoltano eventi all&#39;interno di percorsi, utilizzano i dati contestuali degli eventi trigger nelle espressioni, configurano eventi e rilevano eventi di reazione (ad esempio, aperture di e-mail).

+++
