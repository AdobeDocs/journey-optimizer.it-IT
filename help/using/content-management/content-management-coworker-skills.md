---
solution: Journey Optimizer
product: journey optimizer
title: Collaboratore per la gestione dei contenuti
description: Scopri gli strumenti di gestione dei contenuti CX Enterprise Coworker disponibili per individuare, creare e gestire le risorse di contenuti Journey Optimizer, con istruzioni approfondite e prompt di esempio.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 9f23a6f5-7221-4f87-95cd-047955ca33d5
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
    internal-label: Templates
source-git-commit: faea09992ef91725f52fed718a893f3a32198dd7
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 1%
---

# Collaboratore per la gestione dei contenuti {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri gli strumenti di gestione dei contenuti di CX Coworker disponibili in Adobe Journey Optimizer: per sfogliare, creare, aggiornare, clonare e pubblicare modelli di contenuto, frammenti, pagine di destinazione e contenuti in linea di percorso/campagna; per pianificare la strategia della campagna e generare copie e immagini sul marchio tra canali, lingue, tipi di pubblico e varianti; per creare, rivedere e distribuire HTML e-mail accessibili, con indicazioni dettagliate, prompt di esempio e best practice.

Ulteriori informazioni:

* [Competenze del collaboratore per Journey Optimizer](../start/ai-features.md#cx-coworker-skills): panoramica delle competenze del collaboratore tra Percorsi, fidelizzazione e gestione dei contenuti in Journey Optimizer.
* [Documentazione di Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"}: panoramica delle funzionalità Campagne, Chat e Progetti di Coworker.
* [Guida all&#39;interfaccia utente di Chat con i collaboratori](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"}: come accedere e navigare in Chat con i collaboratori.

>[!ENDSHADEBOX]

## Strumenti di gestione dei contenuti {#content-management}

>[!AVAILABILITY]
>
>La gestione dei contenuti è disponibile per tutti i clienti che hanno accesso a Collaborator.

Gli utenti di Journey Optimizer possono scoprire e gestire le risorse di contenuto (modelli di contenuto, frammenti, pagine di destinazione e contenuti di messaggi in linea del percorso/campagna) direttamente da Coworker utilizzando prompt in linguaggio naturale. Ti consente di passare da &quot;parlami dei miei contenuti&quot; a &quot;andare a crearli, aggiornarli e pubblicarli&quot;, senza uscire dalla conversazione. Questa funzionalità è alimentata da 15 strumenti MCP in lettura e scrittura per contenuti Journey Optimizer.

### Casi d’uso principali

1. **Sfogliare e controllare il contenuto**

   * Elenca i modelli di contenuto, i frammenti o le pagine di destinazione disponibili e recuperane struttura, metadati e stato.
   * Recupera il contenuto del messaggio in linea configurato su un nodo di azione di percorso o campagna.

   Prompt di esempio:
   * &quot;Elencare i modelli di contenuto delle e-mail.&quot;
   * &quot;Mostrami i frammenti disponibili per la campagna estiva&quot;.
   * &quot;Ottieni i dettagli della pagina di destinazione pagina-123.&quot;
   * &quot;Quale contenuto è configurato per la variante e-mail del nodo di azione in campaign camp-789?&quot;

1. **Crea modelli di contenuto**

   * Crea un nuovo modello di contenuto per qualsiasi canale.

   Prompt di esempio:
   * &quot;Crea un modello di e-mail denominato Summer Sale con questo contenuto HTML.&quot;
   * &quot;Crea un nuovo modello SMS denominato Avviso Flash&quot;

1. **Aggiorna modelli di contenuto**

   * Sostituisci completamente il contenuto di un modello esistente.

   Prompt di esempio:
   * &quot;Aggiornare il modello abc-123 con questo nuovo corpo HTML.&quot;

1. **Crea, aggiorna, clona e pubblica frammenti**

   * Crea un nuovo frammento di HTML o di espressione.
   * Aggiornare il contenuto o i metadati di un frammento esistente.
   * Clona un frammento esistente con un nuovo nome.
   * Invia una bozza di frammento per la pubblicazione.

   Prompt di esempio:
   * &quot;Crea un frammento di HTML denominato Banner promozionale con questo markup.&quot;
   * &quot;Aggiorna il frammento frag-456 per cambiarne il nome in Promo Banner V2.&quot;
   * &quot;Clona il frammento abc-123 come Banner promozionale - Estate (variante B).&quot;
   * &quot;Pubblica frammento frag-456.&quot;

1. **Aggiorna contenuto messaggio in linea**

   * Sostituisci una variante di canale nel messaggio in linea di un nodo di azione campagna o percorso.
   * Elencare le varianti di canale definite in un nodo di azione di percorso o campagna.

   Prompt di esempio:
   * &quot;Aggiorna la variante e-mail del nodo di azione in campaign camp-789 con questo nuovo contenuto.&quot;
   * &quot;Quali varianti di canale sono definite in questo nodo di azione?&quot;

### In ambito

Le seguenti funzionalità sono supportate da Content Management:

* **Elenca e ottieni modelli di contenuto**: sfoglia i modelli di contenuto e recuperane la struttura e i metadati.
* **Elenca e ottieni frammenti**: sfoglia i frammenti di contenuto ed espressione e recuperane i dettagli.
* **Elenca e ottieni pagine di destinazione**: sfoglia le pagine di destinazione e recupera i relativi metadati e il contenuto della pagina.
* **Ottieni contenuto in linea campagna/percorso**: recupera il contenuto del messaggio in linea configurato in un nodo di azione campagna o percorso, incluse le varianti multilingue.
* **Crea modelli di contenuto**: crea un nuovo modello per qualsiasi canale.
* **Aggiorna modelli di contenuto**: sostituisci completamente il contenuto di un modello esistente.
* **Crea, aggiorna, clona e pubblica frammenti**: crea nuovi frammenti, aggiorna quelli esistenti, clona un frammento con un nuovo nome e invia una bozza di frammento per la pubblicazione.
* **Aggiorna contenuto messaggio in linea**: sostituisci una variante di canale nel messaggio in linea di un nodo di azione campagna/percorso, incluse le varianti multilingue, ed elenca le varianti di canale definite in un nodo di azione.

### Fuori ambito

Attualmente, le seguenti funzonalità non sono supportate:

* **Ricerca full-text in modelli o frammenti**
* **Convalida modello o frammento** (riferimenti orfani, collegamenti interrotti, componenti obsoleti)
* **Creazione o pubblicazione di pagine di destinazione**
* **Eliminazione di modelli di contenuto, frammenti o pagine di destinazione**

### Best practice per la richiesta di informazioni

1. **ID di riferimento quando noti**: fornisci l&#39;ID del modello, del frammento, della pagina di destinazione o della campagna/percorso quando ti viene richiesto di ottenere, aggiornare, clonare o pubblicare una risorsa specifica.
1. **Informazioni esplicite sul canale**: durante la creazione di un modello o di un frammento, specifica il tipo di canale o di contenuto (e-mail, frammento di HTML, frammento di espressione).
1. **Conferma prima della pubblicazione**: rivedi il contenuto di un frammento dopo averlo creato o aggiornato prima di chiedere a Collaboratore di pubblicarlo.
1. **Fornire il contenuto sostitutivo completo**: le operazioni di aggiornamento sostituiscono il contenuto completo, quindi includere il contenuto completo del corpo o della variante di HTML nella richiesta.

## Contenuto canale {#ce-channel-content}

>[!AVAILABILITY]
>
>Il contenuto del canale è disponibile per tutti i clienti che hanno accesso a CX Coworker. La generazione di immagini con un modello personalizzato e personalizzato richiede l&#39;accesso ai sistemi di produzione Firefly Services.

Il contenuto del canale prende una breve descrizione, un percorso, una campagna o un prompt e la trasforma in una copia pianificata sul marchio e in immagini per canali, impostazioni internazionali, tipi di pubblico e varianti, inclusa la versione finale, accessibile e assemblata di e-mail HTML. I contenuti possono essere esaminati e pianificati, creati, valutati per verificarne la fattibilità, rivisti e salvati nella soluzione attiva (Adobe Journey Optimizer o un’altra soluzione di attivazione supportata).

### Competenze disponibili

Le seguenti abilità sono disponibili nel plug-in **Contenuto canale**:

* **Orchestrare l&#39;authoring dei contenuti** (`orchestrate-content-authoring`)

  Esegue l’intero ciclo di vita di authoring da un breve, percorso, campagna o prompt, ideando, generando, rivedendo e salvando contenuti, incluse copie, immagini e controlli di conformità, accessibilità e fedeltà tra i canali supportati.

* **Esplora strategia contenuti** (`explore-content-strategy`)

  Calcola cosa deve dire una campagna o un messaggio prima che venga scritta la copia, confrontando le mappe dei messaggi e la sequenza di punti di contatto a livello di campagna e decidendo l’ordine delle sezioni, l’enfasi e CTA a livello di messaggio.

* **Riepilogo dei contenuti** (`content-brief`)

  Trasforma una direzione di campagna approvata in requisiti di scrittura concreti, tra cui tono, messaggi chiave, offerta, punti obbligatori, canale, lingua e varianti, oltre a un piano per la produzione del contenuto.

* **Genera contenuto** (`generate-content`)

  Redige un singolo messaggio di marketing o una nuova variante di copia per un canale, in base a un pubblico, un’offerta, un tono, un CTA e una lunghezza dichiarati. Solo creazione di prima bozza.

* **Verifica preparazione contenuto** (`check-content-readiness`)

  Valuta i contenuti esistenti, inclusa un’e-mail assemblata, per la voce del brand, la qualità editoriale, l’accessibilità e la conformità, quindi espone bloccanti spiegabili e i passaggi successivi.

* **Rivedi e rigenera contenuto** (`revise-regenerate-content`)

  Applica una modifica specifica e confermata al contenuto esistente, ad esempio la correzione di un risultato di revisione, la regolazione del tono, la traduzione o lo scambio di un oggetto o di un CTA, mantenendo l’artefatto.

* **Genera immagine** (`generate-image`)

  Produce e manipola gli elementi visivi per un posizionamento approvato, tra cui immagini protagonista, ritagli, sovrapposizioni, varianti o risorse firmate, confermando il piano prima di applicarlo.

* **Valuta progettazione contenuto** (`assess-content-design`)

  Valuta il modo in cui viene eseguito il rendering del contenuto, inclusi gerarchia, spaziatura, immagini, posizionamento del CTA e reattività, e consiglia di copiare o modificare le immagini per colmare le lacune.

* **Salva contenuto canale** (`save-channel-content`)

  Salva il contenuto approvato della campagna come risorsa in stato di bozza o lo inserisce nel modello di origine in Adobe Journey Optimizer o in un’altra soluzione supportata.

* **Genera e-mail da Figma** (`build-email-from-figma`)

  Crea un HTML e-mail finale direttamente da un frame Figma live quando la copia, il layout e le immagini sono quelli che dovrebbero essere consegnati invariati, senza alcun piano di layout separato.

  +++Come utilizzare questa abilità

  1. Accedi a Collaboratore e vai a **[!UICONTROL Impostazioni]** > **[!UICONTROL Segreti]**.

     ![](assets/coworker-1.png)

  1. In **[!UICONTROL I tuoi segreti]**, fai clic su **[!UICONTROL Aggiungi]**.

  1. In **[!UICONTROL Name]**, immetti `FIGMA_ACCESS_TOKEN`.

  1. Genera un PAT (Personal Access Token) di Figma con almeno l&#39;ambito **File: sola lettura**. [Scopri come generare un token di accesso personale Figma](https://help.figma.com/hc/en-us/articles/8085703771159-Manage-personal-access-tokens#h_01JHJXYMB9CREBR8PB5VJ1Q5ME).

  1. Incolla il PAT in **[!UICONTROL Valore]**, quindi fai clic su **[!UICONTROL Salva]**.

  +++

* **Ricerca marchio** (`brand-lookup`)

  Trova, risolve e applica le linee guida approvate per il brand, incluse quelle per voce, immagini e legali, prima di qualsiasi flusso di lavoro che generi o valuti contenuti on-brand.

### Best practice per la richiesta di informazioni

1. **Inizia con la descrizione**: fornisci prima l&#39;obiettivo della campagna, il pubblico e i canali in modo che il piano dei contenuti rifletta l&#39;ambito previsto.
1. **Specificare le dimensioni del piano**: chiamare i canali, i punti di contatto, le impostazioni internazionali, i tipi di pubblico e le varianti che si desidera rappresentare nel piano dei contenuti.
1. **Includi il contesto del brand**: fai riferimento al kit del brand o alle linee guida vocali in modo che le copie e le immagini generate rimangano sul brand.
1. **Limiti per i caratteri dello stato**: specifica esplicitamente i limiti per i caratteri del canale e controlla la copia generata per confermarne l&#39;adattamento prima di pubblicarla.
1. **Richiedi tutte le recensioni pertinenti**: chiedi una revisione su marchio, conformità, progettazione e accessibilità prima di trattare i contenuti come pronti per l&#39;invio.
1. **Rivedi prima di salvare**: valuta e modifica i contenuti generati prima di chiedere a Coworker di salvarli nuovamente in Adobe Journey Optimizer o in un&#39;altra soluzione di attivazione supportata.

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
