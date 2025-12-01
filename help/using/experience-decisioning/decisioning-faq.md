---
title: Decisioning delle domande frequenti
description: Risposte alle domande comuni sulle funzionalità Decisioning
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: 59e85eb7a14f88d95b2ef97e3ace11a65f115b75
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# Decisioning delle domande frequenti {#decisioning-faq}

Questa pagina fornisce le risposte alle domande più frequenti sulle funzionalità Decisioning in Adobe Journey Optimizer.

## Regole di limitazione {#capping-rules}

+++**Cosa succede quando si creano più regole di limite per un&#39;offerta? La visualizzazione dell&#39;offerta verrà interrotta quando si abbina una qualsiasi delle regole di limite o tutte?**

Il limite dell&#39;offerta viene raggiunto non appena viene soddisfatta **una condizione**. Ciò significa che una qualsiasi delle regole di limite impedirà la visualizzazione dell’offerta una volta raggiunta la soglia.

Ad esempio, in presenza di due regole di limite:
* 5 volte per profilo a settimana
* 100 volte il totale per tutti gli utenti

L’offerta cesserà di essere visualizzata a un utente che l’abbia vista 5 volte in una settimana, anche se il limite totale di 100 non è ancora stato raggiunto. Allo stesso modo, una volta raggiunto il totale di 100 impression, l’offerta non viene più visualizzata da tutti gli utenti.

Ulteriori informazioni sulle [regole per la limitazione dei limiti](items.md#capping).

+++

## Formule di classificazione {#ranking-formulas}

+++**Perché aggiungere un pubblico a un modello di IA? Quali vantaggi offre l’aggiunta di tipi di pubblico rispetto a un set di dati completo? Limiterà il modello o espanderà il modello?**

Quando si lavora con modelli AI (in particolare [modelli di ottimizzazione personalizzati](ranking/personalized-optimization-model.md)):

* **Set di dati** aggiunti per raccogliere i tuoi eventi di conversione (clic, ordini, ricavi). Questi sono i risultati che il modello cerca di ottimizzare.
* **I tipi di pubblico** sono stati aggiunti per essere utilizzati come variabili predittive nel modello. Consentono di personalizzare le previsioni per cercare di prevedere clic, ordini o ricavi per diversi segmenti di clienti.

Affinché il modello di ottimizzazione personalizzata funzioni efficacemente, sono necessari set di dati e tipi di pubblico. I tipi di pubblico **non limitano né espandono** il modello, ma forniscono un contesto aggiuntivo che consente al modello di prendere decisioni personalizzate migliori.

Ulteriori informazioni sui [modelli AI](ranking/ai-models.md).

+++

+++**L&#39;aggiunta o la rimozione di offerte in una raccolta avrà un impatto sul modello se si utilizzano modelli di ottimizzazione automatica o di ottimizzazione personalizzata?**

Entrambi i modelli distribuiranno il traffico alla migliore offerta disponibile successiva in base ai dati di traffico degli ultimi 30 giorni.

Se più offerte vengono rimosse in una sola volta e le offerte rimanenti hanno ricevuto un traffico molto ridotto negli ultimi 30 giorni, la distribuzione delle offerte potrebbe comportarsi in modo imprevisto. Questo potrebbe comportare una distribuzione casuale o una distorsione verso alcune offerte che hanno un tasso di conversione più elevato in base a poche impression.

**Best practice**: quando apporti modifiche significative alle raccolte di offerte, assicurati che le offerte rimanenti dispongano di dati sulle prestazioni cronologiche sufficienti per mantenere prestazioni ottimali del modello.

+++

+++**Quanto tempo ci vuole affinché i modelli AI comprendano che sono stati aggiunti nuovi contenuti e inizino ad aggiungerli al mix?**

Entrambi i modelli di intelligenza artificiale identificheranno le nuove offerte disponibili alla prossima esecuzione di formazione:

* **Ottimizzazione automatica**: esecuzioni di formazione giornaliere
* **Ottimizzazione personalizzata**: esecuzioni di formazione settimanali

Una volta identificati, entrambi i modelli inizieranno a fornire le nuove offerte ad alcuni visitatori immediatamente per testarne le prestazioni e raccogliere dati sulla loro efficacia.

Ulteriori informazioni sui modelli [ottimizzazione automatica](ranking/auto-optimization-model.md) e [ottimizzazione personalizzata](ranking/personalized-optimization-model.md).

+++

+++**Se nei modelli AI non sono presenti gruppi di controllo, stiamo apprendendo e ottimizzando tutto il traffico contemporaneamente?**

Sì.  Entrambi i modelli di intelligenza artificiale (ottimizzazione automatica e ottimizzazione personalizzata) utilizzano un approccio &quot;esplora e sfrutta&quot;:

* Inizialmente, entrambi i modelli sono **esplorazione al 100%**, il che significa che sottopongono a test offerte diverse per raccogliere dati sulle prestazioni.
* Nel tempo, i modelli **gestiscono automaticamente il compromesso tra esplorazione e sfruttamento**, man mano che gli eventi comportamentali vengono raccolti e le previsioni migliorano.
* I modelli spostano gradualmente più traffico verso offerte con prestazioni migliori, continuando al contempo a esplorare e testare altre opzioni.

Questo garantisce l’apprendimento continuo e l’ottimizzazione di tutto il traffico senza richiedere gruppi di controllo separati.

+++

+++**Quanti eventi di ottimizzazione devono essere statisticamente significativi? Esiste una soglia minima di traffico per una superficie?**

Per garantire prestazioni ottimali del modello, Adobe consiglia i seguenti valori minimi:

**Minimi consigliati (a settimana):**
* Almeno **1.000 impression** per offerta/elemento
* Almeno **100 eventi di conversione** per offerta/elemento

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Per impostazione predefinita, il sistema non tenta di generare modelli personalizzati per offerte/articoli con meno di 1.000 impression o 50 eventi di conversione.

**Importante**: in pratica, alcuni clienti hanno molte offerte (~300) in un unico modello e alcune offerte possono avere regole aziendali molto restrittive. I valori minimi assoluti (250 impression/25 conversioni ogni 30 giorni) rappresentano la soglia più bassa che il sistema è in grado di supportare per la creazione di modelli.

Ulteriori informazioni su [requisiti raccolta dati](data-collection/data-collection.md).

+++

+++**Il contenuto delle offerte deve essere chiaramente differenziato affinché i modelli AI funzionino correttamente? Cosa succede se dispongo di più offerte troppo simili tra loro?**

In generale, è più probabile che il modello di intelligenza artificiale generi vantaggi dalla personalizzazione quando **offerte sono adatte a diversi tipi di clienti**.

Quando le offerte sono molto simili, è probabile che si verifichi uno dei due risultati seguenti:

* **Prestazioni simili**: le prestazioni delle offerte saranno identiche e riceveranno una quota di traffico relativamente uniforme.
* **Dominanza**: piccole differenze possono far sì che un&#39;offerta domini le altre su tutti i tipi di clienti e riceverà la maggior parte del traffico.

>[!NOTE]
>
>Le differenze nelle offerte non sono una garanzia che un&#39;offerta non dominerà le altre. Ad esempio, un’offerta di sconto di €100 supererà quasi sempre un’offerta di sconto di €50 per tutti i tipi di clienti, indipendentemente dalla personalizzazione.

**Best practice**: assicurati che le offerte forniscano una differenziazione significativa che possa attrarre diversi segmenti di clienti per prestazioni ottimali del modello di intelligenza artificiale.

+++

+++**Cosa succede al modello se si verifica un&#39;anomalia di traffico, ad esempio un picco di traffico enorme? Questo causerà problemi o solleverà stranezze?**

Un picco di traffico verrebbe incluso nella modellazione in modo proporzionale al traffico degli ultimi 30 giorni.

Ad esempio, un picco di traffico giornaliero raddoppiato avrà un effetto relativamente modesto sul modello generale, perché ci sono 29 giorni di traffico normale che rappresentano una quantità significativamente maggiore dei dati comportamentali complessivi.

**Punto chiave**: la finestra continua di 30 giorni consente al modello di mantenere la stabilità durante le anomalie temporanee del traffico. Picchi o ribassi a breve termine non compromettono significativamente le prestazioni del modello.

+++

## Argomenti correlati {#related-topics}

<!--* [Get started with Decisioning](gs-experience-decisioning.md)-->
* [Creare elementi decisionali](items.md)
* [Panoramica dei modelli AI](ranking/ai-models.md)
* [Guardrail e limitazioni per la funzione Decisioni](decisioning-guardrails.md)

