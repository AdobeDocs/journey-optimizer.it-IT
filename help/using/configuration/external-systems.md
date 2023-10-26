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
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 32%

---

# Integrare con sistemi esterni {#external-systems}

Questa pagina presenta i diversi guardrail forniti da Journey Optimizer durante l’integrazione di un sistema esterno, nonché le best practice: come ottimizzare la protezione del sistema esterno utilizzando l’API di limitazione di utilizzo, come configurare il timeout del percorso e come funzionano i nuovi tentativi.

Journey Optimizer consente di configurare connessioni a sistemi esterni tramite origini dati e azioni personalizzate. Ciò ti consente, ad esempio, di arricchire i tuoi percorsi con dati provenienti da un sistema di prenotazione esterno o di inviare messaggi utilizzando un sistema di terze parti come Epsilon o Facebook.

Quando si integra un sistema esterno, è possibile riscontrare diversi problemi, il sistema può essere lento, può smettere di rispondere o potrebbe non essere in grado di gestire un volume di grandi dimensioni. Journey Optimizer offre diversi guardrail per proteggere il sistema dal sovraccarico.

Tutti i sistemi esterni sono diversi in termini di prestazioni. Devi adattare la configurazione ai tuoi casi d’uso.

Quando Journey Optimizer esegue una chiamata a un’API esterna, i guardrail tecnici vengono eseguiti come segue:

1. Vengono applicate le regole di limitazione o limitazione: se viene raggiunta la velocità massima, le chiamate rimanenti vengono scartate o messe in coda.

2. Timeout e nuovo tentativo: se la regola di limitazione o limite viene soddisfatta, Journey Optimizer tenta di eseguire la chiamata fino al raggiungimento della fine della durata del timeout.

## Limitazione e limitazione delle API {#capping}

### Informazioni sulle API di limitazione e limitazione

Durante la configurazione di un’origine dati o di un’azione, viene stabilita una connessione a un sistema per recuperare informazioni aggiuntive da utilizzare nei percorsi oppure per inviare messaggi o chiamate API.

Le API dei percorsi supportano fino a 5000 eventi al secondo, ma alcuni sistemi o API esterni potrebbero non avere una velocità effettiva equivalente. Per evitare il sovraccarico di questi sistemi, è possibile utilizzare **Limitazione** e **Limitazione** API per limitare il numero di eventi inviati al secondo.

Ogni volta che una chiamata API viene eseguita dai percorsi, passa attraverso il motore API. Se viene raggiunto il limite impostato nell’API, la chiamata viene rifiutata se utilizzi l’API di limitazione di utilizzo, oppure viene messa in coda per un massimo di 6 ore ed elaborata il prima possibile nell’ordine in cui è stata ricevuta se utilizzi l’API di limitazione.

Ad esempio, supponiamo che sia stata definita una regola di limitazione di utilizzo o di limitazione di 200 chiamate al secondo per il sistema esterno. Il sistema viene chiamato da un’azione personalizzata in 10 percorsi diversi. Se un percorso riceve 300 chiamate al secondo, utilizza i 200 slot disponibili ed elimina o mette in coda i 100 slot rimanenti. Poiché il limite massimo è stato superato, gli altri 9 percorsi non avranno più alcuno slot. Questa granularità aiuta a proteggere il sistema esterno da sovraccarichi e arresti anomali.

>[!IMPORTANT]
>
>Le **regole di limitazione di utilizzo** sono configurate a livello di sandbox, per un endpoint specifico (l’URL chiamato) ma sono globali per tutti i percorsi di tale sandbox. Il limite è disponibile sia sulle origini dati che sulle azioni personalizzate.
>
>Le **regole di limitazione** sono configurate solo sulle sandbox di produzione, per un endpoint specifico ma globale per tutti i percorsi in tutte le sandbox. Si può disporre di una sola configurazione di limitazione per organizzazione. La limitazione è disponibile solo per le azioni personalizzate.
>
>Il **maxCallsCount** deve essere maggiore di 1.

Per ulteriori informazioni su come utilizzare le API, consulta le sezioni seguenti:

* [API di limitazione di utilizzo](capping.md)
* [API di limitazione](throttling.md)

Una descrizione dettagliata delle API è disponibile in [Documentazione delle API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Origini dati e capacità di azioni personalizzate {#capacity}

Per le **origini dati esterne**, il numero massimo di chiamate al secondo è limitato a 15. Se questo limite viene superato, tutte le chiamate aggiuntive vengono scartate o messe in coda a seconda dell’API in uso. È possibile aumentare questo limite per le origini dati esterne private contattando Adobe per includere l’endpoint nell&#39;elenco Consentiti, ma questa non è un’opzione per le origini dati esterne pubbliche. * [Informazioni su come configurare le origini dati esterne](../datasource/about-data-sources.md).

>[!NOTE]
>
>Se un’origine dati utilizza un’autenticazione personalizzata con un endpoint diverso da quello utilizzato per l’origine dati, è necessario contattare Adobe per includere tale endpoint nell’elenco Consentiti.

Per le **azioni personalizzate**, è necessario valutare la capacità dell’API esterna. Ad esempio, se Journey Optimizer invia 1000 chiamate al secondo e il sistema supporta solo 200 chiamate al secondo, è necessario definire una configurazione di limitazione di utilizzo o di limitazione in modo che il sistema non si saturi. [Informazioni su come configurare le azioni](../action/action.md)

## Timeout e nuovi tentativi{#timeout}

Se la regola di limitazione o limite è soddisfatta, viene applicata la regola di timeout.

In ogni percorso, puoi definire una durata di timeout. Questo consente di impostare una durata massima quando si chiama un sistema esterno. La durata del timeout è configurata nelle proprietà di un percorso. Consulta [questa pagina](../building-journeys/journey-gs.md#timeout_and_error).

Questo timeout è globale per tutte le chiamate esterne (chiamate API esterne nelle azioni personalizzate e nelle origini dati personalizzate). Per impostazione predefinita, è impostato su 30 secondi.

Durante la durata di timeout definita, Journey Optimizer tenta di chiamare il sistema esterno. Dopo la prima chiamata, è possibile eseguire un massimo di tre tentativi fino al raggiungimento della durata di timeout finale. Impossibile modificare il numero di tentativi.

Ogni nuovo tentativo utilizza uno slot. Se hai un limite massimo di 100 chiamate al secondo e ciascuna chiamata richiede due tentativi, la frequenza scende a 30 chiamate al secondo (ogni chiamata utilizza 3 slot: la prima chiamata e due tentativi).

Il valore della durata del timeout dipende dal caso d’uso. Se desideri inviare il messaggio rapidamente, ad esempio quando il client entra nell’archivio, non impostare un timeout prolungato. Inoltre, più è lungo il timeout, più elementi saranno messi in coda. Questo può avere un notevole impatto sulle prestazioni. Se Journey Optimizer esegue 1000 chiamate al secondo, la conservazione di 5 o 15 secondi di dati può sopraffare rapidamente il sistema.

Prendiamo un esempio per un timeout di 5 secondi.

* La prima chiamata dura meno di 5 secondi: la chiamata ha esito positivo e non viene eseguito un nuovo tentativo.
* La prima chiamata dura più di 5 secondi: la chiamata viene annullata e non è possibile riprovare. Viene conteggiato come errore di timeout nel reporting.
* La prima chiamata non riesce dopo 2 secondi (il sistema esterno restituisce un errore): rimangono 3 secondi per i nuovi tentativi, se sono disponibili slot di limitazione.
   * Se uno dei tre tentativi ha esito positivo prima della fine dei 5 secondi, la chiamata viene eseguita e non si verifica alcun errore.
   * Se durante i nuovi tentativi viene raggiunta la fine della durata del timeout, la chiamata viene annullata e conteggiata come un errore di timeout nel reporting.

## Domande frequenti{#faq}

**Come posso configurare una regola di limitazione o limitazione? Esiste una regola predefinita?**

Per impostazione predefinita, non esiste alcuna regola di limitazione o limite. Le regole vengono definite a livello di sandbox per un endpoint specifico (l’URL denominato), utilizzando l’API di limitazione o limitazione. Fai riferimento a [questa sezione](../configuration/external-systems.md#capping).

**Quanti tentativi vengono eseguiti? Posso cambiare il numero di tentativi o definire un periodo minimo di attesa tra un nuovo tentativo e l’altro?**

Per una determinata chiamata, è possibile eseguire un massimo di tre tentativi dopo la prima chiamata, fino al raggiungimento della durata di timeout finale. Non è possibile modificare il numero di tentativi e l’intervallo tra un tentativo e l’altro. Fai riferimento a [questa sezione](../configuration/external-systems.md#timeout).

**Dove posso configurare il timeout? Esiste un valore massimo?**

In ogni percorso, puoi definire una durata di timeout. La durata del timeout è configurata nelle proprietà di un percorso. La durata del timeout deve essere compresa tra 1 e 30 secondi. Fai riferimento a [questa sezione](../configuration/external-systems.md#timeout) e [questa pagina](../building-journeys/journey-gs.md#timeout_and_error).