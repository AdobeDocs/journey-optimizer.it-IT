---
title: Migrazione dalla gestione delle decisioni a Decisioning
description: Scopri i vantaggi della migrazione dalla gestione delle decisioni a Decisioning
feature: Decisioning
topic: Integrations
role: User
level: Experienced
source-git-commit: 48d7d6e9e92c6bcd35cf0b88e5383aa068cdefd0
workflow-type: tm+mt
source-wordcount: '1208'
ht-degree: 4%

---

# Migrazione dalla gestione delle decisioni a Decisioning {#migrate-to-decisioning}

## Che cos’è Decisioning? {#what-is-decisioning}

Journey Optimizer Decisioning è un’espansione della funzionalità decisionale che getta le basi per le decisioni su altri oggetti (come i percorsi) in futuro. Questa nuova funzionalità unisce i concetti chiave del flusso di lavoro per semplificare l’authoring e la gestione, introduce la sperimentazione nel processo decisionale e sposta gli elementi decisionali in un approccio basato su schema per il rendering dinamico degli elementi.

La struttura decisionale di nuova generazione e il set di funzioni in Adobe Journey Optimizer consentono ai brand di utilizzare i dati disponibili, le informazioni e il contesto di un cliente per determinare la migliore esperienza per ogni cliente al fine di ottimizzare il valore aziendale. [Ulteriori informazioni](gs-experience-decisioning.md)

## Perché effettuare la migrazione a Decisioning? {#why-migrate}

Decisioning offre funzionalità e vantaggi significativi rispetto al framework di gestione delle decisioni legacy:

### Funzionalità di intelligenza artificiale e apprendimento automatico

* **Metriche personalizzate**: possibilità di utilizzare metriche di ottimizzazione personalizzate per i modelli AI. Questo fornisce interoperabilità per la generazione di rapporti con [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview){target="_blank"}, standardizza la generazione di rapporti su entrambe le piattaforme e migliora la coerenza e l&#39;affidabilità dei dati. L’integrazione diretta fornisce una visualizzazione più chiara delle metriche delle prestazioni e aggiunge nuove funzionalità, come la creazione di metriche semplici, la pubblicazione di tipi di pubblico, l’esecuzione di domande ad hoc tramite Insight Builder e la pianificazione di rapporti.

* **Misurazione dell&#39;incremento**: possibilità di visualizzare il traffico di esplorazione e di sfruttamento nei modelli AI. Questo consente agli esperti di marketing e ai data scientist di quantificare in che modo l’esplorazione basata su IA migliora le prestazioni dei modelli a lungo termine e la reperibilità di nuove offerte vincenti. La trasparenza nell’allocazione del traffico crea fiducia nelle decisioni di intelligenza artificiale e consente ai team di ottimizzare sia l’apprendimento che le prestazioni nel tempo. [Ulteriori informazioni](ranking/auto-optimization-model.md#lift)

* **Generatore di formule AI**: possibilità di applicare output di punteggio modello IA alle funzionalità formula esistenti. Questo consente agli esperti di marketing di combinare facilmente gli output di IA con regole e pesi deterministici per strategie di ottimizzazione più sfumate, aumentando il controllo e la flessibilità e sfruttando al contempo l’intelligenza dell’apprendimento automatico. [Ulteriori informazioni](ranking/ranking-formulas.md)

### Sperimentazione

Possibilità di sperimentare le offerte, gli aspetti di una determinata offerta e/o i metodi di classificazione. Questo consente agli addetti al marketing di eseguire esperimenti controllati sulla logica creativa, di idoneità e di classificazione per identificare varianti dalle prestazioni elevate, accelerare i cicli di apprendimento e favorire l’ottimizzazione continua del sistema decisionale.

### Generazione rapporti migliorata

Dashboard che documenta le prestazioni degli elementi decisionali e delle strategie di selezione rispetto agli elementi chiave del funnel di coinvolgimento. Una dashboard decisionale intuitiva e pronta all’uso mostra rapidamente il valore delle prestazioni di campagna e percorso per i KPI chiave per l’offerta e la distribuzione dei contenuti, il coinvolgimento di visualizzazione e clic, i tassi di utilizzo di fallback e l’incremento dai modelli di classificazione AI e di apprendimento automatico. [Ulteriori informazioni](cja-reporting.md)

### Efficienza operativa

* **Copia sandbox**: possibilità di copiare oggetti tra sandbox diverse (ad esempio, da sviluppo a produzione). Questo semplifica l’implementazione e i flussi di lavoro di test consentendo la migrazione fluida di logica decisionale, offerte e oggetti di configurazione tra gli ambienti, riducendo i tempi di configurazione e gli errori umani. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md)

* **Gestione catalogo elementi basata su schema**: possibilità di definire e gestire elementi decisionali direttamente in set di dati collegati a schema, consentendo aggiornamenti dinamici e governance semplificata. Ciò semplifica la gestione del catalogo sincronizzando gli elementi decisionali con le origini dati sottostanti, garantendo l’accuratezza dei contenuti, consentendo aggiornamenti più veloci e supportando la governance su larga scala. [Ulteriori informazioni](items.md)

* **Decisioning indipendente dalla posizione**: possibilità di riutilizzare la logica decisionale tra posizionamenti/posizioni, separando la selezione delle decisioni dalla consegna. Questo promuove la riutilizzabilità e l’efficienza consentendo a un singolo modello decisionale di alimentare più posizionamenti o superfici (ad esempio, web, app, e-mail), centralizzando la logica e accelerando le attività di personalizzazione tra canali. [Ulteriori informazioni](placements.md)

* **Frammenti di contenuto riutilizzabili**: possibilità di definire blocchi di contenuto JSON o HTML (ad esempio titoli, intestazioni, piè di pagina, CTA) una volta e di farvi riferimento all&#39;interno di più oggetti di offerta. Questo semplifica l’authoring e la governance dei contenuti, consentendo la gestione centralizzata e l’aggiornamento automatico dei componenti condivisi tra le diverse offerte. [Ulteriori informazioni](../content-management/fragments.md)

### Funzionalità future

* **Decisioning canale**: possibilità di utilizzare la logica decisionale per determinare il canale migliore per il coinvolgimento (ad esempio, e-mail vs. push vs. web), anziché solo l’offerta migliore all’interno di un singolo canale. Ciò migliora l’esperienza del cliente ottimizzando dove viene consegnato un messaggio, non solo ciò che viene consegnato.

* **Ottimizzazione dei messaggi**: possibilità di utilizzare l&#39;intelligenza artificiale o approcci basati su regole per ottimizzare il contenuto dei messaggi per ciascun profilo, migliorando i risultati di coinvolgimento e conversione. Questo consente agli esperti di marketing di personalizzare il tono, le immagini e il layout in modo dinamico in base agli attributi del pubblico e ai dati sulle prestazioni.

* **Ottimizzazione percorso Percorso**: possibilità di determinare quale percorso di percorso deve seguire un profilo, in base ai risultati sperimentali, al contesto in tempo reale, alle regole e/o alla propensione alla conversione. Questo consente ai team di indirizzare in modo intelligente i profili attraverso il ramo di percorso ottimale, garantendo la cadenza e il contenuto corretti per ogni utente.

* **Decisioning Percorso**: possibilità di effettuare l&#39;arbitrato tra più percorsi quando un profilo è idoneo per più di uno, assicurandosi che venga selezionato il percorso più prezioso o rilevante. In questo modo si evitano conflitti di messaggi e messaggi eccessivi, classificando e selezionando il percorso con priorità più elevata per ciascun profilo.

### Funzioni aggiuntive

* **Applicazione dei criteri**: autorizzazione degli utenti aziendali a utilizzare funzionalità come [Etichettatura e applicazione dell&#39;utilizzo dati (DULE)](https://experienceleague.adobe.com/it/docs/experience-platform/data-governance/labels/overview){target="_blank"} e [Consenso](../action/consent.md) all&#39;interno di Decisioning, abilitando la protezione dello scudo per la privacy nel flusso di lavoro decisionale. In questo modo le decisioni rispettano automaticamente i criteri di utilizzo dei dati e le preferenze di consenso dei clienti.

* **Supporto del canale di messaggistica nativa**: messaggistica integrata e decisioning in un singolo framework su più canali ([Esperienza basata su codice](../code-based/get-started-code-based.md) e [E-mail](../email/get-started-email.md) attualmente disponibili, altri canali in arrivo nella prima metà del 2026). Il supporto intuitivo dell’interfaccia utente consente agli utenti di inserire componenti decisionali direttamente nei flussi di lavoro di authoring dei messaggi.

* **Ricerca set di dati di Experience Platform**: possibilità di caricare e fare riferimento a [set di dati di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"} direttamente nelle regole di selezione delle offerte, nella classificazione e nel contenuto delle offerte personalizzate. Questo aumenta la flessibilità per la personalizzazione e il targeting consentendo alla logica decisionale di utilizzare origini di dati esterne dinamiche. [Ulteriori informazioni](../data/lookup-aep-data.md)

* **Scalabilità e prestazioni**: miglioramento architettonico che sposta il calcolo delle decisioni dall&#39;hub all&#39;edge, riducendo in modo significativo la latenza e migliorando la velocità effettiva per i casi di utilizzo con traffico elevato.

## Casi d’uso di esempio {#use-cases}

| Caso d’uso | Gestione delle decisioni | Funzione Decisioni |
|----------|---------------------|-------------|
| **Strategia di posizionamento multiplo** | Una singola strategia potenzia sia la home page che l’app mobile | Logica decisionale associata a un posizionamento specifico (ad esempio, percorso web o e-mail) |
| **Attributi di offerta coerenti** | Un addetto al marketing definisce &quot;discountType&quot; e &quot;offerValue&quot; una volta; ogni offerta eredita automaticamente questi campi | Ogni offerta gestisce i propri attributi manualmente, senza alcuna coerenza a livello di schema |
| **Classificazione IA dinamica** | Un addetto al marketing può regolare la ponderazione (ad esempio, 60% di punteggio di conversione IA + 40% di margine di profitto) per bilanciare i ricavi e gli obiettivi di coinvolgimento | Le classificazioni si basano esclusivamente sull’output del modello o su regole statiche |
| **Strategie di test A/B** | Un team può testare A/B se &quot;IA + regole di business&quot; fornisce prestazioni migliori rispetto al &quot;posizionamento basato sulla priorità&quot; | Nessun supporto integrato per la sperimentazione |
| **Metriche di IA personalizzate** | Retailer addestra un modello di &quot;probabilità di acquisto&quot; e monitora l&#39;incremento tra i prodotti nuovi e quelli noti | Ottimizza solo in base alla propensione al clic; nessuna visibilità nell&#39;esplorazione o nell&#39;incremento del modello |
| **Riutilizzabilità dei contenuti** | L’aggiornamento di un’intestazione o di un CTA si propaga automaticamente a centinaia di offerte | Ogni offerta memorizza il contenuto completo in modo indipendente |
| **Authoring integrato** | Un addetto al marketing inserisce offerte personalizzate in un messaggio e-mail senza uscire dall’editor di messaggi | Decisioning e messaggistica live in framework separati con integrazione limitata |
| **Conformità in materia di privacy** | Un addetto al marketing crea una regola di offerta sapendo che le preferenze di consenso escludono automaticamente alcuni profili | Richiede il coordinamento manuale con i team tecnici e di dati per l’applicazione |
| **Inventario in tempo reale** | Utilizza un set di dati di inventario dei prodotti per eliminare in tempo reale le offerte per articoli esauriti | Dati statici; flessibilità limitata per l’utilizzo di set di dati esterni o contestuali |
| **Scalabilità prestazioni** | Personalizzazione in tempo reale per milioni di richieste in arrivo con tempo di risposta inferiore a 100 ms | Decisioni prese nell&#39;hub con latenza più elevata |

## Strumenti di migrazione {#migration-tooling}

Il team Journey Optimizer sta attualmente lavorando sulle API per gli strumenti di migrazione per migrare le entità di gestione delle decisioni a Decisioning. Questo strumento consente una migrazione semplice tra sandbox con risoluzione delle dipendenze e funzionalità di rollback. Se ti interessa, contatta il tuo rappresentante Adobe.

## Argomenti correlati {#related-topics}

* [Introduzione alla funzione Decisioni](gs-experience-decisioning.md)
* [Guardrail e limitazioni decisionali](decisioning-guardrails.md)
* [Domande frequenti su Decisioning](decisioning-faq.md)

