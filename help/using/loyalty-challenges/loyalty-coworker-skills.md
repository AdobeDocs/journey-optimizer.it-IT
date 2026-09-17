---
solution: Journey Optimizer
product: journey optimizer
title: Collaboratore per fedeltà
description: Scopri le competenze CX Enterprise Coworker disponibili per la creazione, la gestione e l’analisi delle sfide relative alla fidelizzazione in Adobe Journey Optimizer, con istruzioni approfondite e prompt di esempio.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 876b7770-9b11-4e3c-b426-5ffb06e093cf
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
    internal-label: Templates
source-git-commit: 85784fbe98b5347f86899ce7811017cd368745ff
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 2%
---

# Collaboratore per fedeltà {#loyalty-coworker-skills}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri le competenze CX Enterprise Coworker disponibili per le sfide di fedeltà in Adobe Journey Optimizer: creazione e gestione delle sfide e query sulle prestazioni del programma fedeltà con indicazioni dettagliate, prompt di esempio e best practice per ogni abilità.

Ulteriori informazioni:

* [Competenze del collaboratore per Journey Optimizer](../start/ai-features.md#cx-coworker-skills): panoramica delle competenze del collaboratore tra Percorsi, fidelizzazione e gestione dei contenuti in Journey Optimizer.
* [Documentazione di Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"}: panoramica delle funzionalità Campagne, Chat e Progetti di Coworker.
* [Guida all&#39;interfaccia utente di Chat con i collaboratori](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"}: come accedere e navigare in Chat con i collaboratori.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>In Collaboratore sono disponibili competenze in materia di fidelizzazione per le organizzazioni idonee. I clienti con una licenza Fedeltà possono accedere a queste competenze fedeltà, anche se non dispongono di una licenza Collaboratore aggiuntiva.

Le competenze in materia di fidelizzazione consentono agli amministratori e agli analisti di creare, gestire e analizzare programmi fedeltà utilizzando un linguaggio naturale. Grazie a queste competenze basate sull’intelligenza artificiale, puoi progettare rapidamente sfide di fidelizzazione coinvolgenti, monitorare le metriche delle prestazioni e prendere decisioni basate sui dati per ottimizzare il coinvolgimento dei membri e la redditività del programma. Sia che tu stia creando una nuova sfida o analizzando le tendenze dei programmi fedeltà, le abilità di fidelizzazione semplificano l’intero flusso di lavoro di gestione della fedeltà.

## Gestione delle sfide di fedeltà {#loyalty-challenge-management}

Loyalty Challenge Management consente agli utenti di Journey Optimizer di creare e gestire le sfide di fidelizzazione in Coworker utilizzando prompt in linguaggio naturale. Per la documentazione completa sulla creazione, la configurazione e la gestione delle sfide di fidelizzazione, incluse istruzioni di configurazione dettagliate, consulta la [guida sulle sfide di fidelizzazione](get-started.md).

### Casi d’uso principali

1. **Problema di onboarding in più passaggi**

   &quot;Crea una sfida denominata &quot;New Account Kickstart&quot; per i nuovi clienti iscritti che richiede di completare questi passaggi per: aprire un conto corrente, finanziarlo con almeno 500 $ e scaricare l’app mobile. Quando tutti i passaggi sono completati, premiali con 5.000 punti bonus. Esegui dal 1° settembre al 31 ottobre, fuso orario orientale.&quot;

1. **Richiesta soglia attività cumulativa**

   &quot;Crea una sfida denominata &quot;Spendi e guadagna l&#39;estate&quot; per i titolari di carte in cui i membri ottengono un credito di 50 $ una volta spesi 1.500 $ sulla loro carta di credito durante il terzo trimestre. Iniziate il 1 luglio, fuso orario orientale.&quot;

1. **Sfida per sequenza di frequenza**

   &quot;Crea una sfida denominata &quot;Frequent Flyer Sprint&quot; per i membri del livello elite che richiede 3 voli al mese per due mesi consecutivi. Premiare il completamento con un&#39;estensione di livello e 10.000 miglia bonus. Inizia il primo del prossimo mese, fuso orario del Pacifico.&quot;

1. **Sfida singola azione qualificata**

   &quot;Imposta una sfida denominata &quot;Go Paperless&quot; che premia gli abbonati pagati con 500 punti bonus dopo che si sono iscritti al pagamento automatico e sono passati alla fatturazione senza carta entro 30 giorni. Inizia il primo del prossimo mese, fuso orario centrale.&quot;

1. **Obiettivo di coinvolgimento/consumo**

   &quot;Creare una sfida denominata &quot;Badge Explorer&quot; per i membri che richiede di completare 5 attività in almeno 3 diverse categorie durante il mese di agosto. Premiali con 1.000 punti e un distintivo &quot;Explorer&quot; al termine. Inizia il 1° agosto, fuso orario Mountain.&quot;

1. **Azione giornaliera**

   &quot;Aiutatemi a creare una sfida per gli amanti del matcha che richiede loro di venire in negozio ogni giorno questa settimana e comprare un drink matcha. La loro ricompensa dovrebbe essere di 200 punti in più se completano la sfida. Chiamalo &quot;Mad about Matcha&quot;, usa SKU matcha-001, avvialo Lunedì prossima settimana, fuso orario orientale.&quot;

### Competenze in ambito

Le seguenti funzionalità sono supportate da Loyalty Challenge Management:

* **Creazione di una sfida**: crea la configurazione della sfida dal linguaggio naturale (pubblico, criteri di azione, tempistica, ricompensa, denominazione).
* **Aggiornamenti verifica**: modifica i dettagli della verifica tramite prompt iterativi.
* **Pubblicazione della richiesta di verifica**: pubblica le configurazioni di richiesta di verifica supportate direttamente dalla conversazione.
* **Visibilità del contesto di verifica**: recupera e rivedi le informazioni sulla verifica durante l&#39;iterazione.

### Competenze al di fuori dell’ambito

Attualmente, le seguenti funzonalità non sono supportate:

* Eliminazione della sfida
* Informazioni sulla fedeltà e competenze per i consigli
* Automazione completa dell’authoring dei contenuti per i messaggi di sfida in tutti i casi

### Best practice per la richiesta di informazioni

1. **Assegna un nome**: assegna alla sfida un titolo chiaro e facile da ricordare tra virgolette.
1. **Specifica il pubblico**: chi è idoneo (ad esempio, tutti i membri, un livello, un segmento, nuovi iscritti, titolari di carte, abbonati).
1. **Definire l&#39;azione e la quantità**: ciò che i membri devono fare e la frequenza, la soglia o la sequenza che conta come completamento.
1. **Impostare l&#39;intervallo di tempo**: una data di inizio (e una data di fine se di durata fissa) più il fuso orario.
1. **Dichiara il premio**: punti, miglia, crediti di rendiconto, estensioni di stato, voucher o privilegi concessi al completamento.
1. **Riferimento all&#39;evento qualificante**: puntare allo SKU specifico, al prodotto, all&#39;azione dell&#39;account o all&#39;evento di coinvolgimento tracciato dalla sfida.

## Abilità di Approfondimenti fedeltà {#loyalty-data-insight}

La competenza Loyalty Insights consente agli utenti di Journey Optimizer di analizzare e interrogare i dati sulle prestazioni del programma fedeltà utilizzando un linguaggio naturale. Questa abilità fornisce informazioni sui punti fedeltà, i livelli membro, i rimborsi e le metriche dei ricavi, consentendo ad amministratori e analisti di prendere decisioni basate sui dati in merito ai loro programmi fedeltà.

Casi d’uso principali:

1. **Analisi dei punti fedeltà**

   * Analizza i punti fedeltà concessi, guadagnati e rimborsati in periodi specifici.
   * Confronta le attività dei punti fedeltà tra diversi livelli e programmi fedeltà.
   * Tieni traccia del saldo dei punti fedeltà per segmento membro.

   Prompt di esempio:
   * &quot;Quanti punti fedeltà sono stati concessi durante agosto 2026?&quot;
   * &quot;Quanti punti fedeltà sono stati ottenuti dai membri in ogni livello fedeltà durante agosto 2026?&quot;
   * &quot;Mostra il totale dei punti fedeltà riscattati in base allo stato di fedeltà del membro, non al livello fedeltà, durante agosto 2026.&quot;
   * &quot;Mostra il saldo totale dei punti fedeltà suddiviso per livello fedeltà durante agosto 2026.&quot;

1. **Analisi ricavi e sconti**

   * Analizzare le tendenze dei ricavi degli ordini e dello sconto fedeltà per livello e programma.
   * Confrontare la generazione di ricavi tra programmi fedeltà e periodi di tempo.
   * Tieni traccia dell’impatto dello sconto sui ricavi e sul coinvolgimento dei membri.

   Prompt di esempio:
   * &quot;Quali sono stati i ricavi totali degli ordini per ogni livello fedeltà durante agosto 2026?&quot;
   * &quot;Quanto è stato applicato agli sconti fedeltà per ogni livello fedeltà durante agosto 2026?&quot;
   * &quot;Mostra gli sconti fedeltà totali suddivisi per programma fedeltà durante agosto 2026.&quot;
   * &quot;Quali sono stati i ricavi totali degli ordini generati da ciascun programma fedeltà durante agosto 2026?&quot;

1. **Informazioni sulle prestazioni del programma**

   * Analizzare le metriche delle prestazioni del programma su base giornaliera, settimanale e mensile.
   * Confrontare le prestazioni tra le categorie di prodotti e le strategie di sconto.
   * Identifica le tendenze nei modelli di coinvolgimento e rimborso dei membri.

   Prompt di esempio:
   * &quot;Mostra i ricavi totali del programma fedeltà suddivisi per giorno nel mese di agosto 2026.&quot;
   * &quot;Mostra gli sconti fedeltà totali suddivisi per categoria di prodotto nel mese di agosto 2026.&quot;
   * &quot;Mostrami il rapporto sulle prestazioni del programma fedeltà per il terzo trimestre 2026.&quot;

{{$include /help/_includes/do-not-localize/start/ai-augmented-loyalty-coworker-skills.md}}
