---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione all’esperimento sui contenuti
description: Ulteriori informazioni sull’esperimento sui contenuti in Journey Optimizer
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: iniziare, iniziare, contenuto, esperimento
hide: true
hidefromtoc: true
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '2013'
ht-degree: 2%

---

# Guida introduttiva agli esperimenti sui contenuti {#get-started-experiment}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* **[Introduzione all’esperimento sui contenuti](get-started-experiment.md)**
* [Creare un esperimento sui contenuti](content-experiment.md)
* [Comprendere i calcoli statistici](experiment-calculations.md)
* [Configurare i rapporti sulla sperimentazione](reporting-configuration.md)
* [Calcoli statistici nel rapporto di sperimentazione](experiment-report-calculations.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La funzione Esperimento di contenuto è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

## Cos&#39;è un esperimento sui contenuti?

Gli esperimenti di contenuto consentono di ottimizzare il contenuto per le azioni nelle campagne.

Gli esperimenti sono un insieme di test randomizzati, che nel contesto dei test online, significa che alcuni utenti selezionati in modo casuale sono esposti a una determinata variazione di un messaggio e un altro gruppo selezionato in modo casuale di utenti a un altro trattamento. Dopo aver inviato il messaggio, puoi quindi misurare le metriche del risultato che ti interessano, ad esempio aperture di e-mail o clic.

## Perché eseguire gli esperimenti?

![](assets/content_experiment_schema.png)

Gli esperimenti consentono di isolare le modifiche che portano a miglioramenti delle metriche. Come illustrato nell&#39;immagine precedente: alcuni utenti selezionati in modo casuale sono esposti a ciascun gruppo di trattamento, il che significa che in media i gruppi condivideranno le stesse caratteristiche. Così, qualsiasi differenza di risultati può essere interpretata come dovuto alle differenze nei trattamenti ricevuti, cioè, si è in grado di stabilire un nesso causale tra i cambiamenti che hai fatto, e i risultati a cui sei interessato.

Questo consente di prendere decisioni basate sui dati per ottimizzare gli obiettivi aziendali.

Per gli esperimenti sui contenuti in Adobe Journey Optimizer, puoi sottoporre a test idee come:

* **Linea oggetto**: Quale potrebbe essere l&#39;impatto di un cambiamento nel tono o nel grado di personalizzazione di una linea del soggetto?
* **Contenuto del messaggio**: La modifica del layout visivo di un’e-mail comporterà un maggior numero di clic sull’e-mail?

## Come funziona l&#39;esperimento sui contenuti? {#content-experiment-work}

### Assegnazione casuale

La sperimentazione dei contenuti in Adobe Journey Optimizer utilizza un hash pseudo-casuale dell’identità del visitatore per eseguire l’assegnazione casuale degli utenti nel pubblico di destinazione a uno dei trattamenti definiti. Il meccanismo di hashing assicura che, negli scenari in cui il visitatore accede a una campagna più volte, riceva in modo deterministico lo stesso trattamento.

In dettaglio, l’algoritmo a 32 bit MumurHash3 viene utilizzato per eseguire l’hash della stringa di identità dell’utente in uno dei 10.000 bucket. In un esperimento con il 50% del traffico assegnato a ogni trattamento, gli utenti che cadono in secchi 1- 5.000 riceveranno il primo trattamento, mentre gli utenti nei secchi 5.001 - 10.000 riceveranno il secondo trattamento. Poiché viene utilizzato un hashing pseudo-casuale, le suddivisioni del visitatore che si osservano potrebbero non essere esattamente 50-50; tuttavia, la suddivisione sarà statisticamente equivalente alla percentuale di suddivisione target.

Tieni presente che, come parte della configurazione di ogni campagna con un esperimento di contenuto, devi scegliere uno spazio dei nomi di identità da cui selezionare l’ID utente per l’algoritmo di randomizzazione. Questo è indipendente dal [indirizzi di esecuzione](../configuration/primary-email-addresses.md).

### Raccolta e analisi dei dati

Al momento dell’assegnazione, ovvero quando il messaggio viene inviato nei canali in uscita o quando l’utente accede alla campagna nei canali in entrata, viene registrato un &quot;record di assegnazione&quot; nel set di dati di sistema appropriato. In questo modo verrà registrato a quale trattamento l’utente è stato assegnato, insieme agli identificatori di esperimento e campagna.

Le metriche obiettivo possono essere raggruppate in due classi principali:

* Metriche dirette, in cui l’utente reagisce direttamente al trattamento, ad esempio, aprendo un’e-mail o facendo clic su un collegamento.
* Metriche indirette o &quot;bottom of funnel&quot; che si verificano dopo che l’utente è stato esposto al trattamento.

Per le metriche degli obiettivi diretti in cui Adobe Journey Optimizer tiene traccia dei messaggi, gli eventi di risposta degli utenti finali vengono automaticamente taggati con gli identificatori della campagna e del trattamento, consentendo l’associazione diretta della metrica di risposta con un trattamento. [Ulteriori informazioni sul tracciamento](../email/message-tracking.md).

![](assets/technote_2.png)

Per gli obiettivi indiretti o &quot;fondo dell&#39;imbuto&quot;, come gli acquisti, gli eventi di risposta degli utenti finali non sono contrassegnati con gli identificatori della campagna e del trattamento, ovvero, un evento di acquisto si verifica dopo l&#39;esposizione a un trattamento, non c&#39;è associazione diretta di quell&#39;acquisto con un&#39;assegnazione di trattamento precedente. Per queste metriche, l&#39;Adobe associa il trattamento con la parte inferiore dell&#39;evento di conversione funnel se:

* L&#39;identità dell&#39;utente è la stessa al momento dell&#39;assegnazione e dell&#39;evento di conversione.
* La conversione avviene entro sette giorni dall&#39;assegnazione del trattamento.

![](assets/technote_3.png)

Adobe Journey Optimizer utilizza quindi metodi statistici &quot;sempre validi&quot; avanzati per interpretare questi dati di reporting non elaborati, che consentono di interpretare i rapporti sulla sperimentazione. Per ulteriori informazioni, consulta [questa pagina](../campaigns/experiment-calculations.md).

## Suggerimenti per l’esecuzione di esperimenti

Quando esegui gli esperimenti, è importante seguire alcune best practice. Di seguito sono riportati alcuni suggerimenti per l’esecuzione di questi esperimenti:

+++Isolare le variabili che si stanno tentando di testare

Formulare alcune ipotesi che si intende testare e limitare questa ipotesi al minor numero possibile di modifiche per determinare cosa ha avuto un impatto sulla consegna.

Ad esempio, una buona ipotesi può essere se la personalizzazione nelle righe dell’oggetto dell’e-mail determina tassi di apertura migliori. Tuttavia, l’aggiunta di una modifica al contenuto del messaggio o nelle immagini può causare una conclusione confusa.
+++

+++Assicurati di utilizzare la metrica corretta

Determina la metrica di cui desideri eseguire il targeting e se le modifiche apportate possono avere un impatto diretto su questa metrica.

Ad esempio, è improbabile che la modifica del contenuto del corpo del messaggio influisca sulle percentuali di apertura delle e-mail.
+++

+++Esegui il test sulla dimensione corretta del pubblico, o per abbastanza tempo

Se esegui i test per più tempo, sarai in grado di rilevare differenze minori nella metrica di obiettivo tra i trattamenti. Tuttavia, se il valore di base della metrica obiettivo è piccolo, avrai bisogno di dimensioni di campione più grandi.
Il numero di utenti da includere nell’esperimento dipende dalle dimensioni dell’effetto che desideri rilevare, dalla varianza o dalla diffusione della metrica di obiettivo, nonché dalla tolleranza per errori falsi positivi e falsi negativi. Negli esperimenti classici, puoi utilizzare un [Calcolatore dimensione campione](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=it){_blank} per determinare per quanto tempo è necessario eseguire il test.
+++

+++Comprendere l’incertezza statistica

Se esegui un esperimento in cui 1000 utenti hanno visto un solo trattamento e il tasso di conversione è impostato sul 5%. Questo sarebbe il tasso di conversione reale se tutti i tuoi utenti fossero inclusi? Quale sarebbe il vero tasso di conversione?
I metodi statistici ci danno un modo per formalizzare questa incertezza. Uno dei concetti più importanti da comprendere durante l’esecuzione di esperimenti online, è che i tassi di conversione osservati sono coerenti con un intervallo di tassi di conversione reali sottostanti, il che significa che devi attendere che tali stime siano abbastanza precise, prima di tentare di trarre una conclusione. Intervalli di fiducia e fiducia ci aiutano a quantificare questa incertezza.
+++

+++Forma nuove ipotesi e prova continuamente

Per ottenere informazioni aziendali reali, devi attenerti a un solo esperimento. Al contrario, segui gli esperimenti formulando nuove ipotesi ed eseguendo nuovi test con modifiche diverse, su segmenti diversi ed esaminando l’impatto sulle diverse metriche.
+++

## Interpretare i risultati degli esperimenti {#interpret-results}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_summary"
>title="Widget di riepilogo"
>abstract="Il widget Riepilogo fornisce una panoramica dei risultati dell&#39;esperimento, specificando se sono conclusivi o meno. Offre un modo rapido e semplice per comprendere il risultato del vostro esperimento."

![](assets/experimentation_report_3.png)

Questa sezione descrive i rapporti degli esperimenti e come comprendere le varie quantità statistiche presentate.

Seguono alcune linee guida per interpretare i risultati dell’esperimento sui contenuti.

Si noti che una descrizione completa dei risultati dovrebbe prendere in considerazione tutte le prove disponibili (ad esempio le dimensioni del campione, i tassi di conversione, gli intervalli di affidabilità, ecc.) e non solo la dichiarazione conclusiva o meno. Anche quando un risultato non è ancora conclusivo, ci possono essere prove convincenti che un trattamento sia diverso da un altro.

Per comprendere i calcoli statistici, fare riferimento a questo [page](../campaigns/experiment-calculations.md).

### 1. Confrontare le metriche normalizzate {#normalized-metrics}

Quando confronti le prestazioni di due trattamenti, confronta sempre le metriche normalizzate per tenere conto di eventuali differenze nel numero di profili esposti a ciascun trattamento.

Ad esempio, se l’obiettivo dell’esperimento è impostato su **[!UICONTROL Aperture univoche]** e un dato trattamento è stato mostrato a 10.000 Profili con 200 Aperture Uniche registrate, quindi questo rappresenta un **[!UICONTROL Tasso di conversione]** del 2%. Per le metriche non univoche, ad esempio la metrica Apertura, la metrica normalizzata viene visualizzata come **[!UICONTROL Conteggio per profilo]**, mentre per le metriche continue come Totale prezzo, la metrica normalizzata viene visualizzata come **[!UICONTROL Totale per profilo]**.

### 2. Concentrati sugli intervalli di affidabilità {#confidence-intervals}

Quando esegui esperimenti su campioni dei profili, il tasso di conversione osservato per un dato trattamento rappresenta una stima del tasso di conversione reale sottostante.

Ad esempio, se il Trattamento A ha una **[!UICONTROL Tasso di conversione]** del 3%, mentre il trattamento B ha un **[!UICONTROL Tasso di conversione]** del 2%, il trattamento A è un più performante del trattamento B? Per rispondere a questa domanda, dobbiamo innanzitutto quantificare l&#39;incertezza dei tassi di conversione osservati.

Gli intervalli di affidabilità contribuiscono a quantificare l’ammontare di incertezza nei tassi di conversione stimati, ma intervalli di confidenza più ampi implicano maggiore incertezza. Man mano che vengono aggiunti più profili all’esperimento, gli intervalli diventeranno più piccoli, rappresentando una stima più precisa. L’intervallo di affidabilità rappresenta un intervallo di tassi di conversione compatibili con i dati osservati.

Se gli intervalli di affidabilità per due trattamenti si sovrappongono appena, ciò significa che i due trattamenti hanno tassi di conversione diversi. Ma, se c&#39;è molta sovrapposizione tra gli intervalli di affidabilità per due trattamenti, allora è più probabile che i due trattamenti abbiano lo stesso tasso di conversione.

L’Adobe utilizza il 95% in ogni momento Intervalli di affidabilità validi o Sequenze di affidabilità, il che significa che i risultati possono essere visualizzati in modo sicuro in qualsiasi momento durante l’esperimento.

### 3. Comprendere l&#39;incremento {#understand-lift}

Il riepilogo del rapporto Esperimento mostra la variabile **[!UICONTROL Incremento rispetto alla linea di base]**, che è una misura del miglioramento percentuale del tasso di conversione di un dato trattamento rispetto alla linea di base. Definito con precisione, è la differenza di prestazioni tra un dato trattamento e la linea di base, divisa per le prestazioni della linea di base, espressa in percentuale.

### 3. Comprendere la fiducia {#understand-confidence}

Mentre dovresti concentrarti principalmente sul **[!UICONTROL Intervallo di affidabilità]** per l&#39;esecuzione di ciascun trattamento, l&#39;Adobe mostra anche la Confidence, che è una misura probabilistica di quanta prova ci sia che un dato trattamento è lo stesso del trattamento di base. Una maggiore affidabilità indica meno prove dell&#39;ipotesi che i trattamenti di base e quelli non di base abbiano prestazioni uguali. Più precisamente, l&#39;affidabilità mostrata è una probabilità (espressa in percentuale) che avremmo osservato una differenza minore nei tassi di conversione tra un dato trattamento e la linea di base, se in realtà non c&#39;è alcuna differenza nei tassi di conversione reali sottostanti. In termini di valori p, l’affidabilità visualizzata è 1 - valore p.

In Adobe vengono utilizzati valori p-value &quot;Valido ogni volta&quot; e &quot;Valido ogni volta&quot; coerenti con le sequenze di affidabilità descritte in precedenza.

### 4. Rilevanza statistica

Durante l&#39;esecuzione di Esperimenti, un risultato è considerato statisticamente significativo se era molto improbabile che sia stato osservato dato un&#39;ipotesi nulla che un dato trattamento e la linea di base hanno lo stesso tasso di conversione/prestazioni sottostanti.

L’Adobe dichiara un esperimento conclusivo quando la Affidabilità è superiore al 95%.

## Cosa fare dopo aver eseguito un esperimento

Dopo aver eseguito il tuo esperimento, ci sono diverse azioni di follow-up possibili:

* **Distribuire idee vincenti**

   Con un risultato non ambiguo, puoi implementare questa idea vincente, sia spingendo il trattamento più performante a tutti i tuoi clienti, o creando nuove campagne in cui viene replicata la struttura del trattamento con le prestazioni migliori.
   </br>In un ambiente dinamico, ciò che funziona bene una volta, potrebbe non funzionare bene in un secondo momento.

* **Eseguire test di follow-up**

   A volte i risultati dei vostri esperimenti possono essere inconcludenti, sia perché non vi erano abbastanza profili inclusi per rilevare eventuali differenze nei trattamenti, o perché i trattamenti definiti non erano sufficientemente diversi.

   Se l&#39;ipotesi che stavi testando è ancora rilevante, eseguire un test di follow-up su un pubblico più ampio o diverso, o modificare i tuoi trattamenti in modo che ci siano differenze più chiare potrebbe essere l&#39;azione di follow-up migliore.

* **Analisi più approfondite**

   Il trattamento che funziona bene per un pubblico può a volte non essere il miglior trattamento per un altro pubblico. Effettuare analisi più approfondite sul modo in cui i trattamenti si comportano per segmenti diversi aiuta a generare idee per nuovi test.

   Allo stesso modo, lo studio delle prestazioni di ogni trattamento con diverse metriche può anche dare una visione più completa dei tuoi esperimenti.

   >[!CAUTION]
   >
   >Ulteriori analisi indicano una maggiore probabilità di rilevare un effetto spurio o falso positivo.
