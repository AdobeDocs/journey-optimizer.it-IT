---
solution: Journey Optimizer
product: journey optimizer
title: Integrare Journey Optimizer con sistemi esterni
description: Scopri le best practice per l’integrazione di Journey Optimizer con sistemi esterni
role: User
level: Beginner
keywords: esterno, API, ottimizzatore, limiti
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 65da82fd67442cfa2b5d45ec753fb3c5a86d4cc7
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 3%

---

# Integrare con sistemi esterni {#external-systems}

Questa pagina presenta le diverse protezioni fornite da Journey Optimizer durante l’integrazione di un sistema esterno, nonché le best practice: come ottimizzare la protezione del sistema esterno utilizzando l’API di limitazione dei tag, come configurare il timeout del percorso e come funzionano i nuovi tentativi.

Journey Optimizer consente di configurare connessioni a sistemi esterni tramite origini dati e azioni personalizzate. Questo ti consente, ad esempio, di arricchire i tuoi percorsi con i dati provenienti da un sistema di prenotazione esterno, o di inviare messaggi utilizzando un sistema di terze parti come Epsilon o Facebook.

Quando si integra un sistema esterno, è possibile che si verifichino diversi problemi, il sistema può essere lento, può interrompere la risposta, o potrebbe non essere in grado di gestire un grande volume. Journey Optimizer offre diverse protezioni per proteggere il sistema dal sovraccarico.

Tutti i sistemi esterni sono diversi in termini di prestazioni. Devi adattare la configurazione ai tuoi casi d’uso.

Quando Journey Optimizer esegue una chiamata a un’API esterna, le protezioni tecniche vengono eseguite come segue:

1. Le regole di limitazione o limitazione vengono applicate: se viene raggiunto il tasso massimo, le chiamate rimanenti vengono scartate o messe in coda.

2. Timeout e nuovo tentativo: se la regola di limite viene soddisfatta, Journey Optimizer tenta di eseguire la chiamata fino al raggiungimento della fine della durata di timeout.

## API di limitazione e limitazione {#capping}

### Informazioni sulle API di limitazione e limitazione

Durante la configurazione di un’origine dati o di un’azione, stabilisci una connessione a un sistema per recuperare informazioni aggiuntive da utilizzare nei percorsi oppure per inviare messaggi o chiamate API.

Le API dei percorsi supportano fino a 5000 eventi al secondo, ma alcuni sistemi o API esterni potrebbero non avere una velocità effettiva equivalente. Per evitare il sovraccarico di questi sistemi, puoi utilizzare il **Limitazione** e **Limitazione** API per limitare il numero di eventi inviati al secondo.

Ogni volta che una chiamata API viene eseguita dai percorsi, passa attraverso il motore API. Se viene raggiunto il limite impostato nell’API, la chiamata viene rifiutata se utilizzi l’API di limitazione delle funzioni o viene messa in coda ed elaborata il prima possibile nell’ordine in cui sono state ricevute se utilizzi l’API di limitazione delle prestazioni.

Ad esempio, supponiamo che tu abbia definito una regola di limitazione o limitazione di 100 chiamate al secondo per il sistema esterno. Il sistema viene chiamato da un&#39;azione personalizzata in 10 percorsi diversi. Se un percorso riceve 200 chiamate al secondo, utilizza i 100 slot disponibili ed elimina o mette in coda i 100 slot rimanenti. Poiché la tariffa massima è stata superata, gli altri 9 percorsi non avranno più alcuna slot. Questa granularità aiuta a proteggere il sistema esterno da sovraccarichi e crash.

>[!IMPORTANT]
>
>**Regole di limitazione** sono configurati a livello di sandbox, per un endpoint specifico (l’URL chiamato) ma sono globali per tutti i percorsi di tale sandbox.
>
>**Regole di limitazione** sono configurati solo sulle sandbox di produzione, per un endpoint specifico ma globale per tutti i percorsi in tutte le sandbox. Puoi disporre di una sola configurazione di limitazione per organizzazione.

Per ulteriori informazioni su come utilizzare le API, consulta queste sezioni:

* [API di limitazione](capping.md)
* [API di limitazione](throttling.md)

Una descrizione dettagliata delle API è disponibile in [Documentazione API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Origini dati e capacità di azioni personalizzate {#capacity}

Per **origini dati esterne**, il numero massimo di chiamate al secondo è limitato a 15. Se questo limite viene superato, tutte le chiamate aggiuntive vengono scartate o messe in coda a seconda dell’API in uso. È possibile aumentare questo limite per le origini dati esterne private contattando Adobe per includere l’endpoint nell’inserire nell&#39;elenco Consentiti, ma questa non è un’opzione per le origini dati esterne pubbliche. * [Scopri come configurare le origini dati](../datasource/about-data-sources.md).

>[!NOTE]
>
>Se un’origine dati utilizza un’autenticazione personalizzata con un endpoint diverso da quello utilizzato per l’origine dati, è necessario contattare Adobe per includere tale endpoint nell’inserire nell&#39;elenco Consentiti.

Per **azioni personalizzate**, devi valutare la capacità dell’API esterna. Ad esempio, se Journey Optimizer invia 1000 chiamate al secondo e il sistema supporta solo 100 chiamate al secondo, è necessario definire una configurazione di limitazione o limitazione in modo che il sistema non saturi. [Scopri come configurare le azioni](../action/action.md)

## Timeout e nuovi tentativi{#timeout}

Se la regola di limitazione o di limitazione è soddisfatta, viene applicata la regola di timeout.

In ogni percorso, puoi definire una durata di timeout. Questo consente di impostare una durata massima quando si chiama un sistema esterno. La durata del timeout è configurata nelle proprietà di un percorso. Consulta [questa pagina](../building-journeys/journey-gs.md#timeout_and_error).

Questo timeout è globale per tutte le chiamate esterne (chiamate API esterne in azioni personalizzate e origini dati personalizzate). Per impostazione predefinita, è impostato su 30 secondi.

Durante la durata di timeout definita, Journey Optimizer cerca di chiamare il sistema esterno. Dopo la prima chiamata, è possibile eseguire un massimo di tre tentativi fino al raggiungimento della fine della durata di timeout. Impossibile modificare il numero di tentativi.

Ogni nuovo tentativo utilizza uno slot. Se hai un limite di 100 chiamate al secondo e ciascuna di esse richiede due tentativi, la frequenza scende a 30 chiamate al secondo (ogni chiamata utilizza 3 slot: la prima chiamata e due tentativi).

Il valore della durata del timeout dipende dal caso d’uso. Se desideri inviare il messaggio rapidamente, ad esempio quando il cliente entra nello store, non vuoi impostare un timeout lungo. Inoltre, più il timeout è lungo, più elementi saranno messi in coda. Questo può avere un notevole impatto sulle prestazioni. Se Journey Optimizer esegue 1000 chiamate al secondo, mantenere 5 o 15 secondi di dati può rapidamente superare il sistema.

Prendiamo ad esempio un timeout di 5 secondi.

* La prima chiamata dura meno di 5 secondi: la chiamata ha esito positivo, non viene eseguito alcun nuovo tentativo.
* La prima chiamata dura più di 5 secondi: la chiamata è annullata e non vi sono tentativi. Viene conteggiato come errore di timeout nel reporting.
* La prima chiamata non riesce dopo 2 secondi (il sistema esterno restituisce un errore): Se sono disponibili degli slot di tappatura, rimangono 3 secondi per i nuovi tentativi.
   * Se uno dei tre tentativi ha esito positivo prima della fine dei 5 secondi, la chiamata viene eseguita e non si verifica alcun errore.
   * Se durante i nuovi tentativi viene raggiunta la fine della durata del timeout, la chiamata viene annullata e conteggiata come errore di timeout nel reporting.

## Domande frequenti{#faq}

**Come posso configurare una regola di limitazione o limitazione? Esiste una regola predefinita?**

Per impostazione predefinita, non è presente alcuna regola di limitazione o limitazione. Le regole sono definite a livello di sandbox per un endpoint specifico (l’URL chiamato), utilizzando l’API di limitazione o limitazione di limitazione di limitazione o limitazione di limitazione di utilizzo. Fai riferimento a [questa sezione](../configuration/external-systems.md#capping).

**Quanti tentativi vengono eseguiti? Posso cambiare il numero di tentativi o definire un periodo di attesa minimo tra i tentativi?**

Per una determinata chiamata, è possibile eseguire un massimo di tre tentativi dopo la prima chiamata, fino a quando la durata di timeout non viene raggiunta. Impossibile modificare il numero di tentativi e l&#39;intervallo di tempo tra ogni nuovo tentativo. Fai riferimento a [questa sezione](../configuration/external-systems.md#timeout).

**Dove posso configurare il timeout? Esiste un valore massimo?**

In ogni percorso, puoi definire una durata di timeout. La durata del timeout è configurata nelle proprietà di un percorso. La durata del timeout deve essere compresa tra 1 secondo e 30 secondi. Fai riferimento a [questa sezione](../configuration/external-systems.md#timeout) e [questa pagina](../building-journeys/journey-gs.md#timeout_and_error).