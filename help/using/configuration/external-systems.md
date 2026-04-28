---
solution: Journey Optimizer
product: journey optimizer
title: Integrare Journey Optimizer con sistemi esterni
description: Scopri le best practice per l’integrazione di Journey Optimizer con sistemi esterni
feature: Integrations
role: User
level: Beginner
keywords: esterno, API, ottimizzatore, limitazione
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '1834'
ht-degree: 23%

---

# Integrare con sistemi esterni {#external-systems}

Questa pagina presenta i diversi guardrail forniti da Journey Optimizer durante l’integrazione di un sistema esterno, nonché le best practice: come ottimizzare la protezione del sistema esterno utilizzando l’API di limitazione di utilizzo, come configurare il timeout del percorso e come funzionano i nuovi tentativi.

Journey Optimizer consente di configurare connessioni a sistemi esterni tramite [origini dati personalizzate](../datasource/about-data-sources.md) e [azioni personalizzate](../action/action.md). Ciò ti consente, ad esempio, di arricchire i tuoi percorsi con dati provenienti da un sistema di prenotazione esterno o di inviare messaggi utilizzando un sistema di terze parti come Epsilon o Facebook.

Quando si integra un sistema esterno, è possibile riscontrare diversi problemi, il sistema può essere lento, può smettere di rispondere o potrebbe non essere in grado di gestire un volume di grandi dimensioni. Journey Optimizer offre diversi guardrail per proteggere il sistema dal sovraccarico.

Tutti i sistemi esterni sono diversi in termini di prestazioni. Devi adattare la configurazione ai tuoi casi d’uso.

Quando Journey Optimizer esegue una chiamata a un’API esterna, i guardrail tecnici vengono eseguiti come segue:

1. Vengono applicate le regole di limitazione o limitazione: se viene raggiunta la velocità massima, le chiamate rimanenti vengono scartate o messe in coda.

1. Timeout e nuovo tentativo: se la regola di limitazione o limite viene soddisfatta, Journey Optimizer tenta di eseguire la chiamata fino al raggiungimento della fine della durata del timeout.

>[!TIP]
>
>È consigliabile lasciare un buffer di almeno un minuto tra il periodo di scadenza del token dell&#39;API esterna e l&#39;impostazione [`cacheDuration` di Journey Optimizer ](../datasource/external-data-sources.md#custom-authentication-access-token), soprattutto in caso di carichi di lavoro pesanti, per evitare incongruenze di scadenza ed errori 401.

## Limitazione e limitazione delle API {#capping}

### Informazioni sulle api di limitazione e limitazione

Durante la configurazione di un’origine dati o di un’azione, viene stabilita una connessione a un sistema per recuperare informazioni aggiuntive da utilizzare nei percorsi oppure per inviare messaggi o chiamate API.

Le API dei percorsi supportano fino a 5.000 eventi al secondo, ma alcuni sistemi o API esterni potrebbero non avere una velocità effettiva equivalente. Per evitare di sovraccaricare questi sistemi, puoi utilizzare le API **Capping** e **Throttling** per limitare il numero di eventi inviati al secondo.

Ogni volta che una chiamata API viene eseguita dai percorsi, passa attraverso il motore API. Se viene raggiunto il limite impostato nell’API, la chiamata viene rifiutata se utilizzi l’API di limitazione di utilizzo, oppure viene messa in coda per un massimo di 6 ore ed elaborata il prima possibile nell’ordine in cui è stata ricevuta se utilizzi l’API di limitazione.

Ad esempio, supponiamo che tu abbia definito una regola di limitazione o limitazione di 200 chiamate al secondo per il sistema esterno. Il sistema viene chiamato da un’azione personalizzata in 10 percorsi diversi. Se un percorso riceve 300 chiamate al secondo, utilizza i 200 slot disponibili ed elimina o mette in coda i 100 slot rimanenti. Poiché il limite massimo è stato superato, gli altri 9 percorsi non avranno più alcuno slot. Questa granularità aiuta a proteggere il sistema esterno da sovraccarichi e arresti anomali.

>[!IMPORTANT]
>
>Le **regole di limitazione di utilizzo** sono configurate a livello di sandbox, per un endpoint specifico (l’URL chiamato) ma sono globali per tutti i percorsi di tale sandbox. Il limite è disponibile sia sulle origini dati che sulle azioni personalizzate.
>
>Le **regole di limitazione** sono configurate solo sulle sandbox di produzione, per un endpoint specifico ma globale per tutti i percorsi in tutte le sandbox. Si può disporre di una sola configurazione di limitazione per organizzazione. La limitazione è disponibile solo per le azioni personalizzate.
>
>Il valore **maxCallsCount** deve essere maggiore di 1.

Per ulteriori informazioni su come utilizzare le API, consulta le sezioni seguenti:

* [API di limitazione di utilizzo](capping.md)
* [API di limitazione](throttling.md)

Una descrizione dettagliata delle API è disponibile nella [documentazione delle API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling)

### Origini dati e capacità di azioni personalizzate {#capacity}

Per le **origini dati esterne**, il numero massimo di chiamate al secondo è limitato a 15. Se questo limite viene superato, tutte le chiamate aggiuntive vengono scartate o messe in coda a seconda dell’API in uso. È possibile aumentare questo limite per le origini dati esterne private contattando Adobe per includere l’endpoint nell&#39;elenco Consentiti, ma questa non è un’opzione per le origini dati esterne pubbliche. * [Informazioni su come configurare le origini dati esterne](../datasource/about-data-sources.md).

>[!NOTE]
>
>Se un’origine dati utilizza un’autenticazione personalizzata con un endpoint diverso da quello utilizzato per l’origine dati, è necessario contattare Adobe per includere tale endpoint nell’elenco Consentiti.

Per le **azioni personalizzate**, è necessario valutare la capacità dell’API esterna. For example, if Journey Optimizer sends 1000 calls per second and your system can only support 200 calls per second, you need to define a capping or throttling configuration so that your system does not saturate. [Informazioni su come configurare le azioni](../action/action.md)

>[!NOTE]
>
>Poiché le risposte sono ora supportate, per i casi d’uso relativi a origini dati esterne devi utilizzare azioni personalizzate anziché origini dati. For more information on responses, see this [section](../action/action-response.md)

## Endpoints with slow response time {#response-time}

When an endpoint has a response time greater than 0.75 seconds, its custom action calls are routed through a dedicated **slow custom action service** instead of the default service.

This slow custom action service applies a capping limit of 150,000 calls every 30 seconds. The limit is enforced using a sliding window, which can begin at any millisecond within that 30-second period. Once the window is full, additional calls are rejected with capping errors. The system does not wait for the next fixed interval but begins capping immediately after the 30-second threshold is reached.

Because slow endpoints can cause delays across all queued actions in the pipeline, it is recommended not to configure custom actions with endpoints that have slow response times. Routing such actions to the slow service helps protect overall system performance and prevents added latency for other custom actions.

## Timeout and retries {#timeout}

If the capping or throttling rule is fulfilled, then the timeout rule is applied.

In each journey, you can define a timeout duration. This allows you to set a maximum duration when calling an external system. Timeout duration is configured in the properties of a journey. Consulta [questa pagina](../building-journeys/journey-properties.md#timeout_and_error).

This timeout is global to all external calls (external API calls in custom actions and custom data sources). By default, it is set to 30 seconds.

During the defined timeout duration, Journey Optimizer tries to call the external system. After the first call, a maximum of three retries can be performed until the end of timeout duration is reached. The number of retries cannot be changed.

Each retry uses one slot. If you have a capping of 100 calls per second and each of your calls require two retries, the rate drops to 30 calls per second (each call uses 3 slots: the first call and two retries).

The timeout duration value depends on the use case. If you want to send your message quickly, for example when the client enters the store, then you do not want to set up a long timeout. Also, the longer the timeout is, the more items will be placed in queue. Questo può avere un notevole impatto sulle prestazioni. Se Journey Optimizer esegue 1000 chiamate al secondo, la conservazione di 5 o 15 secondi di dati può sopraffare rapidamente il sistema.

Prendiamo un esempio per un timeout di 5 secondi.

* La prima chiamata dura meno di 5 secondi: la chiamata ha esito positivo e non viene eseguito un nuovo tentativo.
* La prima chiamata dura più di 5 secondi: la chiamata viene annullata e non è possibile riprovare. Viene conteggiato come errore di timeout nel reporting.
* La prima chiamata non riesce dopo 2 secondi (il sistema esterno restituisce un errore): rimangono 3 secondi per i nuovi tentativi, se sono disponibili slot di limitazione.
   * Se uno dei tre tentativi ha esito positivo prima della fine dei 5 secondi, la chiamata viene eseguita e non si verifica alcun errore.
   * Se durante i nuovi tentativi viene raggiunta la fine della durata del timeout, la chiamata viene annullata e conteggiata come un errore di timeout nel reporting.

## Domande frequenti {#faq}

Di seguito sono riportate le domande frequenti sull&#39;integrazione di Journey Optimizer con sistemi esterni.

Hai bisogno di altri dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=it){target="_blank"}.

+++ Come posso configurare una regola di limitazione o limitazione? Esiste una regola predefinita?

Per creare regole di limitazione o limitazione, consultare [questa sezione](../configuration/external-systems.md#capping). Per impostazione predefinita, non esiste una regola di limitazione ma un limite massimo di 300.000 chiamate in un minuto definito per tutte le azioni personalizzate, per host e per sandbox. Il limite “per host” si applica a livello di dominio (ad esempio, example.com). Questo limite è stato impostato in base all’utilizzo da parte della clientela, per proteggere gli endpoint esterni interessati dalle azioni personalizzate. Se necessario, puoi ignorare questa impostazione definendo un limite di limitazione di utilizzo o di limitazione maggiore tramite le rispettive API. Per ulteriori dettagli su come richiedere aumenti dei limiti, consulta [questa pagina](../action/about-custom-action-configuration.md).

+++

+++ Quanti tentativi vengono eseguiti? Posso cambiare il numero di tentativi o definire un periodo minimo di attesa tra un nuovo tentativo e l’altro?

Per una determinata chiamata, è possibile eseguire un massimo di tre tentativi dopo la prima chiamata, fino al raggiungimento della durata di timeout finale. Non è possibile modificare il numero di tentativi e l’intervallo tra un tentativo e l’altro. Fai riferimento a [questa sezione](../configuration/external-systems.md#timeout).

+++

+++ Dove posso configurare il timeout? Esiste un valore massimo?

In ogni percorso, puoi definire una durata di timeout. La durata del timeout è configurata nelle proprietà di un percorso. La durata del timeout deve essere compresa tra 1 e 30 secondi. Consulta [questa sezione](../configuration/external-systems.md#timeout) e [questa pagina](../building-journeys/journey-properties.md#timeout_and_error).

+++

+++ Qual è il proxy in uscita e quando dovrei usarlo?

Il proxy in uscita fornisce un **indirizzo IP statico** per le chiamate in uscita da **azioni personalizzate** di Journey Optimizer ai sistemi esterni. Utilizzalo quando gli endpoint di terze parti richiedono l’inserire nell&#39;elenco Consentiti dell’IP.

**Importante:** Il proxy di uscita NON controlla la velocità effettiva, i limiti di velocità o il numero di connessioni simultanee. Per gestire il volume di chiamate e i limiti di connessione, utilizzare l&#39;[API di limitazione](capping.md) o l&#39;[API di limitazione](throttling.md).

**Utilizza il proxy di uscita per:**
* Inserire nell&#39;elenco Consentiti un IP statico sul firewall o sull’endpoint di terze parti

**Usa API di limitazione/limitazione per:**
* Limitazione del numero di chiamate API al secondo
* Controllo delle connessioni simultanee all’endpoint
* Protezione del sistema esterno da sovraccarichi

Contatta Adobe per abilitare il proxy di uscita per la tua organizzazione, se hai bisogno di un IP statico a scopo di inserire nell&#39;elenco Consentiti di un’organizzazione. Per favore, contatta l’amministratore di sistema.

+++

+++ Qual è il numero massimo di connessioni aperte da Journey Optimizer quando vengono utilizzate azioni personalizzate?

Con il proxy IP abilitato e una configurazione di limitazione definita sull’endpoint di destinazione, il numero di connessioni si basa sulla frequenza (stime, numeri non garantiti):

* tra 200 e 2000 c/s: 50 collegamenti
* tra 2000 e 3000: 75 collegamenti
* tra 3000 e 4000: 100 collegamenti
* tra 4000 e 5000: 125 collegamenti

Se non è definita alcuna configurazione di limitazione su un endpoint, il motore di Journey Optimizer è progettato per aumentare la scalabilità e può raggiungere un numero elevato di connessioni (più di 2.000). Per ottenere un numero limitato di connessioni, i clienti devono utilizzare una configurazione di limitazione.

+++
