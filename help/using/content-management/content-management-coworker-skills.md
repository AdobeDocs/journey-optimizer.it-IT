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
source-git-commit: 85784fbe98b5347f86899ce7811017cd368745ff
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%
---

# Collaboratore per la gestione dei contenuti {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri gli strumenti di gestione dei contenuti di CX Enterprise Coworker disponibili in Adobe Journey Optimizer per sfogliare, creare, aggiornare, clonare e pubblicare modelli di contenuto, frammenti, pagine di destinazione e contenuti in linea di percorso/campagna con indicazioni dettagliate, prompt di esempio e best practice.

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

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
