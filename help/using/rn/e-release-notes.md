---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 2eb1ffff7101362b52ae91f1a7277188664b2954
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 31%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di maggio 2024 {#e-2024}

**Data di rilascio**: 21-22 maggio 2024

### Nuove funzionalità {#e-features}

Questa versione include le nuove funzionalità elencate di seguito.


<table>
<thead>
<tr>
<th><strong>Decisioni per le esperienze: disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione Decisioni per le esperienze semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti.</p>
<p>Questi elementi decisionali vengono integrati direttamente in un’ampia gamma di superfici in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne Journey Optimizer. I criteri decisionali di Experience Decisioning sono disponibili solo per l’utilizzo in campagne di esperienza basate su codice.</p>
<p>La funzione Decisioni per le esperienze è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/gs-experience-decisioning.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Flusso di lavoro di riscaldamento IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se invii un’e-mail con un nuovo indirizzo IP, ora puoi eseguire facilmente i flussi di lavoro di riscaldamento IP direttamente dall’interfaccia utente. Adobe Journey Optimizer offre un modo standardizzato ed efficiente di riscaldare gli indirizzi IP seguendo le best practice per una consegna ottimale.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/ip-warmup-gs.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Regole aziendali - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare regole granulari di quota limite e applicarle a diversi tipi di comunicazioni di marketing tramite set di regole. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Dati di personalizzazione estesa - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi cercare e recuperare valori di dati nei set di dati di Adobe Experience Platform e utilizzarli per creare condizioni in Adobe Journey Optimizer. Puoi sfruttare i dati di un set di dati di ricerca quando una relazione è stata definita utilizzando un attributo all’interno di un array di oggetti. Puoi specificare set di dati non abilitati per il profilo per la ricerca. Una volta abilitata, puoi utilizzare un attributo di profilo come chiave di unione al set di dati specificato per recuperare ulteriori dati per la personalizzazione.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Experience Decisioning**

Dalla versione beta a LA, sono stati aggiunti i seguenti miglioramenti:

* **Experience Decisioning + Esperienze basate su codice (LA)**: ora puoi sfruttare la funzione Experience Decisioning per utilizzare gli elementi decisionali nelle campagne basate su codice. Nota: il canale di esperienza basato sul codice e Experience Decisioning non sono disponibili per le organizzazioni che hanno acquistato le offerte aggiuntive Adobe Healthcare Shield e Privacy and Security Shield. [Ulteriori informazioni](../code-based/get-started-code-based.md)
* Ora puoi sfruttare i dati contestuali provenienti da Adobe Experience Platform nelle regole di decisione e nelle formule di classificazione. [Ulteriori informazioni](../experience-decisioning/context-data.md)
* È ora disponibile la nuova autorizzazione “Gestisci decisioni esperienza” per la risorsa Gestione delle decisioni. Consente di gestire i diritti relativi ad Experience Decisioning. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md)
* Ora in Decisione per le esperienze è possibile aggiungere più regole di limitazione per un determinato elemento decisionale. Ciò ti consente di aumentare il livello di controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../experience-decisioning/items.md#capping)
* Ora puoi creare dashboard di reporting personalizzate delle campagne Experience Decisioning tramite [!DNL Customer Journey Analytics]. [Ulteriori informazioni](../experience-decisioning/cja-reporting.md)


**Offer Decisioning**

* **Supporto di più regole** - È ora possibile aggiungere fino a 10 regole di limite per una determinata offerta in Gestione delle decisioni. Questo offre maggiore controllo sulla modalità di invio delle offerte.
* **Audit** - Il **Registro modifiche** Questa scheda ti consente di visualizzare tutte le modifiche apportate a un’offerta o a una decisione che sono state rimosse. Le modifiche relative alle offerte e alle decisioni ora sono visibili nel menu **Audit**.


**Canale e-mail**

* **Annullamento iscrizione mailing list** - A seguito dei recenti annunci Gmail e Yahoo per mittenti in blocco, Journey Optimizer supporta l’opzione &quot;post/1 clic&quot; List-Unsubscribe.
* **Punteggio spam** (Beta) - Ora puoi controllare il punteggio di posta indesiderata del contenuto in un rapporto spam dedicato. Utilizzando SpamAssassin, Adobe Journey Optimizer può ora testare il contenuto delle e-mail e assegnargli un punteggio per indicare se i provider ISP lo considereranno come spam o meno. [Ulteriori informazioni](../content-management/spam-report.md)


**Tipi di pubblico**

* L’utilizzo di tipi di pubblico e attributi dalla composizione del pubblico e dal caricamento personalizzato (file CSV) è ora disponibile con Healthcare Shield o Privacy and Security Shield.

**Personalizzazione**

* **Frammento di espressione** - I frammenti di espressione sono ora disponibili per **Canale in-app**. [Ulteriori informazioni](../personalization/use-expression-fragments.md)

**Percorsi**

* **Criteri di unione** - È ora possibile configurare e utilizzare i criteri di unione nei percorsi.
* **Supporto mTLS** - Il protocollo mTLS è ora supportato nelle API e nelle azioni personalizzate di Journey Optimizer.
* **Ricercare tabelle negli eventi** - È ora possibile sfruttare i dati di un set di dati di ricerca quando una relazione è stata definita utilizzando un attributo all’interno di un array di oggetti. I valori di ricerca saranno disponibili in percorsi (condizioni, azioni personalizzate, ecc.) e la personalizzazione dei messaggi.
