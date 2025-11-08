---
solution: Journey Optimizer
product: journey optimizer
title: Ricerca eventi esperienza in percorsi
description: Scopri come utilizzare la ricerca di eventi esperienza in percorsi
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 6%

---

# Ricerca eventi esperienza in percorsi {#ee-journeys}

>[!CAUTION]
>
>A partire dall’8 luglio 2025, nelle nuove organizzazioni dei clienti, la creazione di espressioni utilizzando gli eventi di esperienza non è più supportata nell’editor di espressioni utilizzato nelle condizioni di percorso. Di conseguenza, gli eventi esperienza nell’[origine dati di Experience Platform](../datasource/adobe-experience-platform-data-source.md) non possono essere utilizzati per la creazione di espressioni. Di seguito sono riportati approcci alternativi e best practice per la creazione di espressioni/logiche con eventi di esperienza.
>
>Hai bisogno di ulteriori dettagli? [Consulta le domande frequenti](#faq-ee).

Questa pagina illustra modelli comuni e approcci scalabili per aiutarti a sfruttare al meglio gli eventi Experience in Adobe Journey Optimizer. Questi casi d’uso sono progettati per aiutarti a risolvere problemi frequenti come la gestione delle rinunce, il controllo della frequenza dei messaggi, la personalizzazione dei contenuti in base al comportamento degli utenti e la reazione ai segnali in tempo reale.

Sfruttando queste strategie, puoi trasformare i dati comportamentali in azioni significative, ossia eliminare, qualificare o escludere i profili in base agli eventi che attivano o agli attributi trasportati. Che tu stia creando una logica per le soglie di acquisto, i trigger di abbandono o la gestione dei mancati recapiti, questi esempi offrono indicazioni pratiche che puoi adattare alle tue esigenze.

Quando valuti quale approccio si adatta meglio, prendi in considerazione i requisiti di latenza del caso d’uso per garantire che i percorsi rimangano reattivi ed efficaci.

## Soppressione della rinuncia

Per eliminare i profili che hanno rinunciato alle comunicazioni di marketing, utilizza la gestione del consenso integrata. Le preferenze di rinuncia vengono acquisite automaticamente nei campi di consenso del profilo; è possibile farvi riferimento direttamente nelle condizioni di percorso e vengono applicate automaticamente da Journey Optimizer durante la consegna dei messaggi.

Ulteriori informazioni:

* [Gestire il consenso](../privacy/opt-out.md)
* [Gestione della rinuncia alle e-mail](../email/email-opt-out.md)
* [Gestione delle rinunce per i messaggi di testo](../sms/sms-opt-out.md)


## Soppressione basata su mancato recapito

Per escludere i profili che hanno riscontrato mancati recapiti e-mail, sfrutta l’elenco di soppressione automatica di Adobe Journey Optimizer per gli indirizzi non recapitati. Questo meccanismo integrato garantisce che le e-mail non valide o non raggiungibili siano escluse da invii futuri senza richiedere una logica personalizzata.

Ulteriori informazioni:

* [Gestire l’elenco di soppressione](../configuration/manage-suppression-list.md)


## Soppressione generica

Per eliminare i profili che hanno dimostrato determinati comportamenti, utilizza tipi di pubblico in batch con logica basata su eventi per acquisire profili che soddisfano i criteri di eliminazione. Fai riferimento a questo pubblico in condizioni di percorso.

Ulteriori informazioni:

* Generatore di segmenti [Adobe Experience Platform - Eventi](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Generatore di segmenti di Adobe Experience Platform [- Vincoli di tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utilizzo dei tipi di pubblico nelle condizioni](../building-journeys/condition-activity.md#using-a-segment)

* [funzione inAudience()](../building-journeys/functions/functioninaudience.md)


## Esclusione di comunicazioni ricevute

Per evitare l’invio di messaggi a profili che hanno ricevuto comunicazioni in un intervallo di tempo recente:

* Utilizza i tipi di pubblico in batch con criteri basati sul tempo e farvi riferimento in condizioni di percorso.
* Applica le regole aziendali relative ai limiti di frequenza per applicare limiti giornalieri o settimanali ai messaggi.


Ulteriori informazioni sull’utilizzo dei tipi di pubblico:

* Generatore di segmenti [Adobe Experience Platform - Eventi](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Generatore di segmenti di Adobe Experience Platform [- Vincoli di tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utilizzo dei tipi di pubblico nelle condizioni](../building-journeys/condition-activity.md#using-a-segment)

* [funzione inAudience()](../building-journeys/functions/functioninaudience.md)


Vedi anche:

* [Quota limite per tipo di comunicazione e canale](../conflict-prioritization/channel-capping.md)



## Inclusione/esclusione specifica per il messaggio

Per includere o escludere i profili in base al fatto che abbiano ricevuto un messaggio specifico, crea tipi di pubblico in batch che incapsulano questa logica e vi fanno riferimento nelle condizioni di percorso.


Ulteriori informazioni:

* Generatore di segmenti [Adobe Experience Platform - Eventi](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Generatore di segmenti di Adobe Experience Platform [- Vincoli di tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utilizzo dei tipi di pubblico nelle condizioni](../building-journeys/condition-activity.md#using-a-segment)

* [funzione inAudience()](../building-journeys/functions/functioninaudience.md)

## Personalizzazione dell’abbandono del carrello o della navigazione

Per personalizzare le comunicazioni in base agli ultimi eventi del carrello o per sfogliare più tipi di carrello o visualizzazioni prodotto:

* Se hai accesso a [Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configura le query automatizzate per estrarre i dati richiesti dall&#39;evento, modificarli per adattarli al caso d&#39;uso e riscriverli in un set di dati abilitato per il profilo per l&#39;attivazione.
* Se i dati di abbandono possono essere modellati sul profilo con attributi scalari, considera l’utilizzo di Attributi calcolati per acquisire le informazioni più recenti e quindi fai riferimento a tali attributi nel percorso per costruire la comunicazione. [Ulteriori informazioni sono disponibili nella documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## Uscita dal percorso basata sul comportamento

Per rimuovere i profili dal percorso quando mostrano un comportamento particolare, utilizza i criteri di uscita per uscire dal profilo dal percorso quando viene ricevuto un evento particolare o il profilo si qualifica per un pubblico specifico.

Ulteriori informazioni:

* [Impostare le proprietà del percorso - Criteri di uscita](journey-properties.md#exit-criteria)

## Qualificazione basata sull&#39;acquisto con soglie di valore

Per attivare i percorsi basati sugli acquisti ed eliminare se il valore è superiore/inferiore a una soglia, definisci gli attributi calcolati per sommare gli acquisti in un periodo di tempo specifico. Crea un pubblico che includa profili il cui importo di spesa soddisfa determinati criteri.

Ulteriori informazioni:

* Panoramica sugli attributi calcolati di Adobe Experience Platform [&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Domande frequenti {#faq-ee}

Di seguito sono riportate le domande frequenti sulla ricerca di eventi di esperienza in percorsi.

Hai bisogno di ulteriori dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

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

L’organizzazione Adobe è interessata solo se non utilizzavi già la ricerca degli eventi dell’esperienza. Se utilizzi già eventi esperienza nell&#39;[origine dati Experience Platform](../datasource/adobe-experience-platform-data-source.md), la tua organizzazione Adobe continua a supportare la ricerca di eventi esperienza.

+++

+++Ho una nuova organizzazione Adobe. Come posso risolvere il mio caso d’uso che richiede dati sull’evento esperienza? 

Sono disponibili qui sopra approcci alternativi e best practice che coinvolgono eventi di esperienza per ottenere i casi d’uso desiderati.

+++

+++ Cosa succede se gli approcci alternativi non funzionano per il mio caso d’uso?

Se il tuo caso d’uso non può essere risolto utilizzando uno degli approcci alternativi elencati sopra, contatta il tuo rappresentante Adobe.

+++
