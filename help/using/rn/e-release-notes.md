---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
hide: true
hidefromtoc: true
source-git-commit: f957737aa741cc8b854912414d15154489d1b0b0
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 100%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di marzo 2024 {#e-2024}

**Data di rilascio**: 19-20 marzo 2024

### Nuova funzionalità {#e-features}

Questa versione include la nuova funzionalità descritta di seguito.

<table>
<thead>
<tr>
<th><strong>Esperienze basate su codice</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il nuovo canale di esperienza basato su codice, Adobe Journey Optimizer consente di eseguire personalizzazioni e test avanzati per qualsiasi proprietà in entrata, consentendo la distribuzione diretta di esperienze personalizzate in diversi punti di contatto come app web, app mobili, app desktop, console video, dispositivi connessi per TV, smart TV, chioschi, sportelli bancomat, dispositivi IoT e altro ancora.</p>
<P>Le funzionalità principali includono:</p>
<ul><li> Personalizzazione universale: estende le esperienze personalizzate in tutti i punti di contatto, garantendo un percorso utenti coeso e personalizzato</li>
<li>Precisione granulare nella modifica: modifica contenuti specifici in singole posizioni all’interno delle app o delle pagine web</li>
<li>Implementazione versatile: supporto per metodi di implementazione lato server, basati su API o SDK per l’integrazione diretta con l’ambiente di sviluppo.</li></ul></p>
<p>Per ulteriori informazioni, consulta la <a href="../code-based/get-started-code-based.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Modelli di contenuto**

* **Miniature**: per i modelli di contenuto è ora disponibile la modalità **Vista a griglia**, in cui vengono visualizzate miniature dei modelli per agevolarne l’accesso visivo. Al momento sono supportati solo i modelli per e-mail HTML. [Ulteriori informazioni](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Questa funzionalità viene rilasciata in Disponibilità limitata (LA) per un set limitato di clienti.

**Percorsi**

Sono stati aggiunti nuovi stati intermedi al ciclo di vita di authoring del percorso:

* Stato **Pubblicazione** tra gli stati **Bozza** e **Live**
* Stato **Interruzione** tra gli stati **Live** e **Interrotto**
* Stati **Attivazione modalità di test** o **Disattivazione modalità di test** tra gli stati **Bozza** e **Bozza (test)**

Quando un percorso si trova in uno stato intermedio, è di sola lettura.