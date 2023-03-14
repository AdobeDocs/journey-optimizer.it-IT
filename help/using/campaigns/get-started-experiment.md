---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione all’esperimento sui contenuti
description: Ulteriori informazioni sull’esperimento sui contenuti in Journey Optimizer
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: introduzione, avvio, contenuto, esperimento
hide: true
hidefromtoc: true
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '2013'
ht-degree: 2%

---

# Introduzione agli esperimenti sui contenuti {#get-started-experiment}

>[!BEGINSHADEBOX]

Informazioni disponibili in questa documentazione:

* **[Introduzione all’esperimento sui contenuti](get-started-experiment.md)**
* [Creare un esperimento sui contenuti](content-experiment.md)
* [Comprendere i calcoli statistici](experiment-calculations.md)
* [Configurare i rapporti sulla sperimentazione](reporting-configuration.md)
* [Calcoli statistici nel rapporto di sperimentazione](experiment-report-calculations.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La funzione Esperimento contenuti è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

## Che cos’è un esperimento sui contenuti?

Gli esperimenti sui contenuti ti consentono di ottimizzare i contenuti per le azioni nelle campagne.

Gli esperimenti sono un insieme di studi randomizzati, che nel contesto dei test online, significa che alcuni utenti selezionati in modo casuale sono esposti a una determinata variante di un messaggio e un altro gruppo selezionato in modo casuale di utenti a un altro trattamento. Dopo aver inviato il messaggio, puoi quindi misurare le metriche di risultato a cui sei interessato, ad esempio aperture di e-mail o clic.

## Perché eseguire gli esperimenti?

![](assets/content_experiment_schema.png)

Gli esperimenti consentono di isolare le modifiche che portano a miglioramenti nelle metriche. Come illustrato nell’immagine precedente: alcuni utenti selezionati in modo casuale sono esposti a ciascun gruppo di trattamento, il che significa che in media i gruppi condivideranno le stesse caratteristiche. Pertanto, qualsiasi differenza nei risultati può essere interpretata come dovuta alle differenze nei trattamenti ricevuti, ovvero, si è in grado di stabilire un nesso causale tra le modifiche apportate e i risultati che si sono interessati.

Questo consente di prendere decisioni basate sui dati per ottimizzare gli obiettivi aziendali.

Per gli esperimenti di contenuto in Adobe Journey Optimizer, puoi testare idee come:

* **Oggetto**: quale potrebbe essere l’impatto di un cambiamento nel tono o nel grado di personalizzazione di un oggetto?
* **Contenuto del messaggio**: la modifica del layout visivo di un’e-mail comporterà un maggior numero di clic sul messaggio?

## Come funziona l’esperimento sui contenuti? {#content-experiment-work}

### Assegnazione casuale

La sperimentazione dei contenuti in Adobe Journey Optimizer utilizza un hash pseudo-casuale dell’identità del visitatore per eseguire l’assegnazione casuale degli utenti nel pubblico di destinazione a uno dei trattamenti definiti. Il meccanismo di hashing assicura che negli scenari in cui il visitatore accede a una campagna più volte, riceva deterministicamente lo stesso trattamento.

In dettaglio, l’algoritmo MumurHash3 a 32 bit viene utilizzato per eseguire l’hashing della stringa di identità dell’utente in uno dei 10.000 bucket. In un esperimento sui contenuti con il 50% del traffico assegnato a ciascun trattamento, gli utenti che rientrano nei contenitori 1-5.000 riceveranno il primo trattamento, mentre gli utenti nei contenitori 5.001-10.000 riceveranno il secondo trattamento. Poiché viene utilizzato l’hashing pseudo-casuale, le suddivisioni del visitatore osservate potrebbero non essere esattamente 50-50; tuttavia, la suddivisione sarà statisticamente equivalente alla percentuale di suddivisione target.

Tieni presente che, come parte della configurazione di ogni campagna con un esperimento sui contenuti, devi scegliere uno spazio dei nomi di identità da cui l’ID utente verrà selezionato per l’algoritmo di randomizzazione. Questo è indipendente dal [indirizzi di esecuzione](../configuration/primary-email-addresses.md).

### Raccolta e analisi dei dati

Al momento dell’assegnazione, ovvero quando il messaggio viene inviato in canali in uscita, o quando l’utente accede alla campagna in canali in entrata, viene registrato un &quot;record di assegnazione&quot; nel set di dati di sistema appropriato. Registra il trattamento a cui è stato assegnato l’utente, insieme agli identificatori dell’esperimento e della campagna.

Le metriche oggettive possono essere raggruppate in due classi principali:

* Metriche dirette, in cui l’utente reagisce direttamente al trattamento, ad esempio aprendo un’e-mail o facendo clic su un collegamento.
* Metriche indirette o &quot;bottom of funnel&quot;, che si verificano dopo che l’utente è stato esposto al trattamento.

Per le metriche di obiettivo diretto in cui Adobe Journey Optimizer tiene traccia dei messaggi, gli eventi di risposta degli utenti finali vengono automaticamente taggati con gli identificatori della campagna e del trattamento, consentendo l’associazione diretta della metrica di risposta a un trattamento. [Ulteriori informazioni sul tracciamento](../email/message-tracking.md).

![](assets/technote_2.png)

Per gli obiettivi indiretti o &quot;bottom of funnel&quot; come gli acquisti, gli eventi di risposta degli utenti finali non sono taggati con gli identificatori della campagna e del trattamento, ovvero un evento di acquisto si verifica dopo l’esposizione a un trattamento, non esiste alcuna associazione diretta di tale acquisto con un’assegnazione di trattamento precedente. Per queste metriche, Adobe assocerà il trattamento alla parte inferiore dell’evento di conversione funnel se:

* L&#39;identità utente è la stessa al momento dell&#39;assegnazione e dell&#39;evento di conversione.
* La conversione avviene entro sette giorni dall’assegnazione del trattamento.

![](assets/technote_3.png)

Adobe Journey Optimizer utilizza quindi metodi statistici avanzati &quot;in qualsiasi momento validi&quot; per interpretare questi dati di reporting non elaborati, che consentono di interpretare i rapporti di sperimentazione. Per ulteriori informazioni, consulta [questa pagina](../campaigns/experiment-calculations.md).

## Suggerimenti per l’esecuzione di esperimenti

Durante l’esecuzione di Esperimenti, è importante seguire determinate best practice. Di seguito sono riportati alcuni suggerimenti per l’esecuzione di questi esperimenti:

+++Isolare le variabili da testare

Formulare alcune ipotesi da testare e limitare questa ipotesi al minor numero possibile di modifiche per determinare quale ha avuto un impatto sulla consegna.

Ad esempio, una buona ipotesi è se la personalizzazione nelle righe dell’oggetto dell’e-mail determini tassi di apertura migliori. Tuttavia, anche l’aggiunta di una modifica nel contenuto del messaggio o nelle immagini può causare una conclusione confusa.
+++

+++Assicurarsi di utilizzare la metrica corretta

Determina la metrica di destinazione e se le modifiche che stai apportando possono avere un impatto diretto su questa metrica.

Ad esempio, è improbabile che la modifica del contenuto del corpo del messaggio influisca sui tassi di apertura delle e-mail.
+++

+++Esegui il test sulla giusta dimensione di pubblico o per un periodo di tempo sufficiente

Se esegui i test più a lungo, potrai rilevare differenze più piccole nella metrica dell’obiettivo tra i trattamenti. Tuttavia, se il valore linea di base della metrica obiettivo è basso, sono necessarie dimensioni di campione più grandi.
Il numero di utenti che devono essere inclusi nell’esperimento dipende dalla dimensione dell’effetto che desideri rilevare, dalla varianza o dalla diffusione della metrica dell’obiettivo, nonché dalla tolleranza per i falsi positivi e falsi negativi. Negli esperimenti classici, puoi utilizzare un [calcolatore dimensione campione](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=it){_blank} per determinare per quanto tempo si deve eseguire il test.
+++

+++Comprendere l’incertezza statistica

Se esegui un esperimento in cui 1000 utenti hanno visualizzato un trattamento e il tasso di conversione è impostato su 5%. Questo sarebbe il tasso di conversione reale se tutti gli utenti fossero inclusi? Quale sarebbe il vero tasso di conversione?
I metodi statistici ci permettono di formalizzare questa incertezza. Uno dei concetti più importanti da capire durante l’esecuzione di esperimenti online è che i tassi di conversione osservati sono coerenti con un intervallo di tassi di conversione effettivi sottostanti, il che significa che è necessario attendere che tali stime siano sufficientemente precise, prima di tentare di trarre una conclusione. Intervalli di affidabilità e affidabilità ci aiutano a quantificare questa incertezza.
+++

+++Creare nuove ipotesi e testare in modo continuo

Per ottenere informazioni di business effettive, devi attenerti a un solo esperimento. Piuttosto, segui gli esperimenti formulando nuove ipotesi ed eseguendo nuovi test con modifiche diverse, su segmenti diversi ed esaminando l’impatto sulle diverse metriche.
+++

## Interpretare i risultati degli esperimenti {#interpret-results}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_summary"
>title="Widget riepilogo"
>abstract="Il widget Riepilogo fornisce una panoramica dei risultati dell’esperimento, specificando se sono conclusivi o meno. Offre un modo rapido e semplice per comprendere il risultato del tuo esperimento."

![](assets/experimentation_report_3.png)

Questa sezione descrive i rapporti degli esperimenti e come comprendere le varie quantità statistiche presentate.

Di seguito sono riportate alcune linee guida per l’interpretazione dei risultati dell’esperimento sui contenuti.

Si noti che una descrizione completa dei risultati dovrebbe prendere in considerazione tutte le prove disponibili (ad esempio le dimensioni del campione, i tassi di conversione, gli intervalli di affidabilità, ecc.) e non solo la dichiarazione conclusiva o meno. Anche quando un risultato non è ancora conclusivo, ci possono essere prove convincenti che un trattamento sia diverso da un altro.

Per informazioni sui calcoli statistici, consulta questa [pagina](../campaigns/experiment-calculations.md).

### 1. Confrontare le metriche normalizzate {#normalized-metrics}

Quando confronti le prestazioni di due trattamenti, devi sempre confrontare le metriche normalizzate per tenere conto di eventuali differenze nel numero di profili esposti a ciascun trattamento.

Ad esempio, se l’obiettivo dell’esperimento è impostato su **[!UICONTROL Aperture univoche]** e un dato trattamento è stato mostrato a 10.000 Profili con 200 Aperture univoche registrate, quindi questo rappresenta un **[!UICONTROL Tasso di conversione]** del 2%. Per le metriche non univoche, ad esempio la metrica Opens, la metrica normalizzata viene visualizzata come **[!UICONTROL Conteggio per profilo]**, mentre per le metriche continue come il totale dei prezzi, la metrica normalizzata viene visualizzata come **[!UICONTROL Totale per profilo]**.

### 2. Concentrarsi sugli intervalli di affidabilità {#confidence-intervals}

Quando esegui esperimenti su campioni dei profili, il tasso di conversione osservato per un dato trattamento rappresenta una stima del reale tasso di conversione sottostante.

Ad esempio, se il trattamento A ha **[!UICONTROL Tasso di conversione]** del 3%, mentre il trattamento B ha un’incidenza **[!UICONTROL Tasso di conversione]** del 2%, il trattamento A è più efficace del trattamento B? Per rispondere a questa domanda, dobbiamo innanzitutto quantificare l’incertezza di questi tassi di conversione osservati.

Gli intervalli di confidenza contribuiscono a quantificare l’entità dell’incertezza nei tassi di conversione stimati, ma intervalli di confidenza più ampi implicano maggiore incertezza. Man mano che più profili vengono aggiunti all’esperimento, gli intervalli diventano più piccoli e rappresentano una stima più precisa. L’intervallo di affidabilità rappresenta un intervallo di tassi di conversione compatibili con i dati osservati.

Se gli intervalli di confidenza per due trattamenti si sovrappongono appena, ciò significa che i due trattamenti hanno tassi di conversione diversi. Ma, se c’è molta sovrapposizione tra gli intervalli di affidabilità per due trattamenti, allora è più probabile che i due trattamenti abbiano lo stesso tasso di conversione.

Adobe utilizza intervalli di affidabilità validi al 95% in qualsiasi momento, o sequenze di affidabilità, il che significa che i risultati possono essere visualizzati in modo sicuro in qualsiasi momento durante l’esperimento.

### 3. Comprendere l’incremento {#understand-lift}

Il riepilogo del rapporto Esperimento mostra **[!UICONTROL Incremento rispetto alla linea di base]**, che è una misura del miglioramento percentuale del tasso di conversione di un dato trattamento rispetto al basale. Definita con precisione, rappresenta la differenza di prestazioni tra un dato trattamento e il basale, divisa per le prestazioni del basale, espressa in percentuale.

### 3. Comprendere l’affidabilità {#understand-confidence}

Mentre è necessario concentrarsi principalmente sul **[!UICONTROL Intervallo di affidabilità]** per la performance di ciascun trattamento, Adobe mostra anche Confidence (Affidabilità), che è una misura probabilistica della quantità di prove che dimostrano che un dato trattamento è uguale al trattamento basale. Una maggiore affidabilità indica meno prove dell’ipotesi che i trattamenti al basale e non al basale abbiano prestazioni uguali. Più precisamente, l’affidabilità visualizzata rappresenta la probabilità (espressa in percentuale) di osservare una differenza minore nei tassi di conversione tra un dato trattamento e la linea di base, se in realtà non vi è alcuna differenza nei veri tassi di conversione sottostanti. In termini di valori p, l’affidabilità visualizzata è 1 - valore p.

Adobe utilizza i valori di affidabilità &quot;Anytime Valid&quot; e &quot;Anytime Valid&quot; che sono coerenti con le sequenze di affidabilità descritte in precedenza.

### 4. Rilevanza statistica

Durante l’esecuzione degli Esperimenti, un risultato è considerato statisticamente significativo se era molto improbabile che fosse stato osservato, data un’ipotesi nulla che un dato trattamento e la linea di base abbiano tassi/prestazioni reali di conversione sottostanti identici.

Adobe dichiara un esperimento conclusivo quando l’affidabilità è superiore al 95%.

## Cosa fare dopo l’esecuzione di un esperimento

Dopo aver eseguito l’esperimento, è possibile eseguire diverse azioni di follow-up:

* **Implementare idee vincenti**

   Con un risultato inequivocabile, puoi implementare questa idea vincente, sia spingendo il trattamento con le prestazioni migliori a tutti i tuoi clienti, sia creando nuove campagne in cui la struttura del trattamento con le prestazioni migliori viene replicata.
   </br>Tieni presente che in un ambiente dinamico ciò che funziona bene in un’unica operazione potrebbe non funzionare bene in un secondo momento.

* **Eseguire test di follow-up**

   A volte i risultati degli esperimenti possono essere inconcludenti, sia perché non sono stati inclusi sufficienti profili per rilevare eventuali differenze nei trattamenti, sia perché i trattamenti definiti non erano sufficientemente diversi.

   Se l’ipotesi che stavi testando è ancora rilevante, l’esecuzione di un test di follow-up su un pubblico più ampio o diverso o la modifica dei tuoi trattamenti in modo da individuare differenze più evidenti potrebbe essere l’azione di follow-up migliore.

* **Eseguire analisi più approfondite**

   Il trattamento che funziona bene per un pubblico a volte può non essere il trattamento migliore per un altro pubblico. Analizzando in modo più approfondito il comportamento dei trattamenti per diversi segmenti è possibile generare idee per nuovi test.

   Allo stesso modo, lo studio delle prestazioni di ciascun trattamento con metriche diverse può anche fornire una visione più completa dei tuoi esperimenti.

   >[!CAUTION]
   >
   >Più analisi significano una maggiore probabilità di rilevare un effetto spurio o un falso positivo.
