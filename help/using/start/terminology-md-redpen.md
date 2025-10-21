---
solution: Journey Optimizer
product: journey optimizer
title: Terminologia chiave
description: Terminologia chiave in AJO
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: d4c968d2-5eae-4fff-9b67-427ac9d9d74c
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 2%

---

# Terminologia

Ti diamo il benvenuto nella guida alla terminologia di Adobe Journey Optimizer. Questa risorsa fornisce definizioni chiare e semplici dei termini chiave che si incontrano durante l’utilizzo della piattaforma. Comprendere questi termini consente di navigare in Adobe Journey Optimizer in tutta sicurezza, implementare strategie di marketing in modo efficace e collaborare in modo efficiente con i membri del team e il supporto Adobe.

## Termini della piattaforma core

| Termine | Definizione |
|------|------------|
| **Adobe Journey Optimizer (AJO)** | Strumento che consente di creare e inviare messaggi personalizzati ai clienti su più canali, ad esempio e-mail, messaggi di testo e notifiche tramite app mobile. Consente di progettare percorsi di clienti che rispondono alle azioni dei clienti in tempo reale. Ad esempio, la conferma via e-mail viene attivata immediatamente dopo che un cliente ha effettuato un acquisto sul sito web. |
| **Adobe Experience Platform (AEP)** | La base di Adobe Journey Optimizer. Raccoglie e organizza tutti i dati dei clienti in un’unica posizione, creando profili cliente completi che Adobe Journey Optimizer utilizza per inviare messaggi personalizzati. Considera AEP come l’hub centrale che guida le strategie di coinvolgimento dei clienti. |
| **Sandbox** | Un’area di lavoro separata in cui eseguire test e prove senza influire sulle comunicazioni live dei clienti. Una sandbox funziona come area di esercitazione o ambiente di test. Adobe Journey Optimizer fornisce fino a cinque sandbox, consentendo ai team di testare scenari come percorsi di onboarding o campagne promozionali. |

## Termini di percorso e campagna

| Termine | Definizione |
|------|------------|
| **Percorso** | Una serie di passaggi collegati che guidano i clienti attraverso esperienze con il tuo marchio. Un percorso di benvenuto include, ad esempio, un’e-mail di benvenuto, un promemoria per il download dell’app e consigli di prodotti personalizzati. Ogni passaggio si verifica dopo il completamento del precedente, abilitando interazioni sequenziali e personalizzate. |
| **Campaign** | Una singola comunicazione o un insieme di comunicazioni identiche inviate contemporaneamente a uno specifico gruppo di clienti. A differenza dei percorsi, che si svolgono nel tempo, le campagne distribuiscono i messaggi simultaneamente, immediatamente o in un orario pianificato. Ad esempio, puoi pianificare una campagna e-mail promozionale per una vendita nel fine settimana. |
| **Canale** | Il metodo utilizzato per comunicare con i clienti, ad esempio e-mail, messaggi di testo (SMS), notifiche push (avvisi delle app mobili), messaggi in-app o siti web. Ogni canale richiede una configurazione specifica, ad esempio la verifica di un dominio e-mail o la connessione di un provider SMS. |
| **Messaggio** | Il contenuto inviato ai clienti, inclusi testo, immagini ed elementi personalizzati. Puoi creare messaggi per vari formati, ad esempio e-mail, messaggi di testo e notifiche push. Ad esempio, un messaggio potrebbe essere un’e-mail di ringraziamento con nomi dei clienti inseriti in modo dinamico e dettagli dell’ordine. |
| **Evento** | Un&#39;occorrenza che attiva o fa avanzare un percorso. Gli eventi includono le azioni dei clienti, ad esempio l’acquisto, oppure eventi di sistema, come l’iscrizione di un nuovo cliente. Gli eventi consentono ai percorsi di rispondere alle azioni dei clienti in tempo reale. Ad esempio, il compleanno di un cliente attiva un’e-mail di sconto speciale. |

## Termini cliente e pubblico

| Termine | Definizione |
|------|------------|
| **Profilo** | Una visualizzazione completa di ogni cliente che combina informazioni quali dettagli di contatto, cronologia acquisti, preferenze e comportamenti. Per &quot;profilo coinvolgibile&quot; si intende un cliente contattato tramite Adobe Journey Optimizer negli ultimi 12 mesi. I profili sono essenziali per creare esperienze personalizzate e basate su dati. |
| **Pubblico** | Un gruppo di clienti che condividono caratteristiche o comportamenti comuni. Ad esempio, &quot;clienti che hanno acquistato negli ultimi 30 giorni&quot; o &quot;clienti interessati ai prodotti per esterni&quot;. I tipi di pubblico vengono creati in Adobe Experience Platform e utilizzati in Adobe Journey Optimizer per eseguire il targeting di segmenti specifici. |
| **Qualificazione del pubblico** | Processo che si verifica quando un cliente si unisce o lascia un pubblico. Adobe Journey Optimizer attiva automaticamente le azioni quando qualcuno entra o esce da un pubblico. Ad esempio, invia un messaggio di benvenuto ai nuovi membri del programma fedeltà, garantendo comunicazioni tempestive e pertinenti. |
| **Pubblico di riferimento** | Numero totale di profili cliente potenzialmente raggiungibili. Il tuo account consente un pubblico indirizzabile che è il 25% più grande del pubblico coinvolgibile previsto dal contratto, fornendo flessibilità man mano che la tua base di clienti cresce. |
| **Pubblico coinvolgibile** | Il numero di clienti con cui si comunica attivamente tramite Adobe Journey Optimizer in base al contratto. In questo modo puoi rispettare i limiti di licenza concentrandoti sulle interazioni di alto valore. |
| **Definizione segmento** | Le regole che determinano quali clienti appartengono a un pubblico. Queste regole si basano su attributi, comportamenti o altri criteri. Ad esempio, una definizione del segmento potrebbe includere &quot;clienti che hanno speso più di $ 500 negli ultimi sei mesi&quot;. |

## Termini di gestione delle decisioni

| Termine | Definizione |
|------|------------|
| **Gestione delle decisioni** | Funzione che seleziona automaticamente il contenuto o l’offerta migliore per ciascun cliente. Ad esempio, consiglia un’offerta di spedizione gratuita a un cliente che abbandona spesso il carrello. Questo garantisce interazioni personalizzate e pertinenti. |
| **Offerta** | Uno specifico messaggio di marketing o promozione presentato ai clienti. Alcuni esempi includono uno sconto del 20%, un’offerta di spedizione gratuita o un consiglio per un prodotto. Adobe Journey Optimizer include fino a 10 offerte per e-mail, consentendo contenuti diversificati e personalizzati. |
| **API decisioning** | Connessione tecnica che consente ad altri sistemi di chiedere a Adobe Journey Optimizer &quot;Qual è l’offerta migliore per questo cliente in questo momento?&quot; L’offerta selezionata viene visualizzata su siti web, app o altri canali. Questa integrazione estende le funzionalità di Journey Optimizer oltre l’e-mail e gli SMS. |
| **Libreria di offerte** | Una raccolta centralizzata in cui tutte le offerte di marketing vengono memorizzate e gestite. Ciò garantisce la coerenza tra i canali e semplifica gli aggiornamenti alle strategie promozionali. |
| **Regole di idoneità** | Condizioni che determinano se un cliente può ricevere una particolare offerta. Ad esempio, &quot;Mostra questo sconto solo ai clienti che non hanno acquistato da 60 giorni&quot;. Queste regole aiutano a evitare messaggi eccessivi o offerte irrilevanti. |

## Dati e termini tecnici

| Termine | Definizione |
|------|------------|
| **Area di destinazione dati** | Area di archiviazione temporanea in cui inserire i file di dati prima di spostarli in Adobe Experience Platform. Considerala un’area di gestione temporanea per i dati. Ad esempio, puoi caricare qui un file CSV delle transazioni dei clienti prima di integrarlo nel sistema. |
| **Servizio query** | Strumento che consente di eseguire query in stile database per convalidare i dati dopo l&#39;importazione in Adobe Journey Optimizer. Ad esempio, si esegue una query su &quot;Quanti clienti si sono iscritti nell&#39;ultima settimana?&quot; per garantire la precisione della segmentazione del pubblico. |
| **Attributo calcolato** | Una caratteristica del cliente calcolata dal suo comportamento. Ad esempio, &quot;valore medio di acquisto&quot; o &quot;totale visite al sito web questo mese&quot;. Questi attributi consentono di personalizzare i messaggi in base ai pattern dei clienti, ad esempio indirizzando i clienti di alto valore con offerte esclusive. |
| **Campi di personalizzazione** | Segnaposto nei messaggi sostituiti con informazioni specifiche del cliente, ad esempio nome, acquisti recenti o livello di iscrizione. Adobe Journey Optimizer supporta fino a cinque campi di personalizzazione per messaggio. Ad esempio, &quot;Ciao [Nome], il tuo recente acquisto di [Nome prodotto] è in arrivo!&quot; |
| **Schema** | Il blueprint che definisce come vengono organizzati i dati dei clienti. Vengono mappati i tipi di informazioni archiviate e le relative relazioni. Uno schema chiaro garantisce l’integrazione perfetta e l’utilizzo accurato dei dati nei vari flussi di lavoro. |
| **Set di dati** | Raccolta di dati correlati organizzati in base a uno schema. Ad esempio, potresti avere set di dati separati per la cronologia degli acquisti, l’attività sul sito web e le interazioni con il servizio clienti. Questi set di dati ti consentono di analizzare e agire su diversi aspetti del comportamento del cliente. |

## Contenuto e termini risorsa

| Termine | Definizione |
|------|------------|
| **Assistente IA** | Funzione integrata che utilizza l’intelligenza artificiale per facilitare la creazione di contenuti. Genera testo, progetta le e-mail o crea varianti di messaggio per diversi canali. Ad esempio, gli chiedi di redigere un messaggio e-mail promozionale in base alle preferenze del pubblico. |
| **Assets Essentials** | Libreria inclusa in Adobe Journey Optimizer per l&#39;archiviazione e la gestione di file digitali quali immagini, loghi e documenti. Include l’archiviazione per le risorse di marketing e supporta fino a cinque utenti con autorizzazioni complete e 100 utenti con accesso in visualizzazione. Ciò semplifica la collaborazione e garantisce la coerenza del brand. |
| **Frammento di contenuto** | Contenuto riutilizzabile utilizzato in più messaggi. Ad esempio, un piè di pagina standard con le informazioni di contatto visualizzate in tutte le e-mail. Ciò garantisce coerenza e riduce il tempo impiegato per ricreare gli elementi condivisi. |
| **Modello** | Layout di messaggio predefinito personalizzato con un contenuto specifico. I modelli consentono di mantenere un aspetto coerente nelle comunicazioni, ad esempio nelle progettazioni di e-mail con marchio o nei formati SMS. |

## Termini di Reporting &amp; Analysis

| Termine | Definizione |
|------|------------|
| **Rapporto globale** | Panoramica completa che mostra le prestazioni di tutti i percorsi e le campagne. Consente di comprendere le tendenze nei tassi di coinvolgimento tra i canali e valutare l’efficacia complessiva del marketing. |
| **Report live** | Dati in tempo reale su percorsi e campagne attualmente in esecuzione. Se necessario, è possibile effettuare regolazioni immediate. Ad esempio, sospendi una campagna con un coinvolgimento ridotto e rivedi i messaggi. |
| **Rapporto Percorso** | Informazioni dettagliate sulle prestazioni in un percorso specifico. Mostra come i clienti passano attraverso ogni passaggio e identifica dove potrebbero lasciare. Questo consente di ottimizzare le esperienze dei clienti. |
| **Rapporto messaggi** | Statistiche su un messaggio specifico, ad esempio il numero di messaggi consegnati, aperti e su cui è stato fatto clic. Queste informazioni consentono di perfezionare le comunicazioni future mostrando come i clienti rispondono ai contenuti. |

## Documentazione correlata

* [Introduzione a Adobe Journey Optimizer](get-started.md)
* [Architettura e concetti](architecture-concepts-redpen.md)
* [Guida alle aree funzionali](functional-areas-redpen.md)
