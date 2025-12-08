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
source-git-commit: 54ed4dec71703a0444920baf4fb0a2d8318034cd
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Decisioning delle domande frequenti {#decisioning-faq}

Questa pagina fornisce le risposte alle domande più frequenti sulle funzionalità Decisioning in Adobe Journey Optimizer.

## Regole di limitazione {#capping-rules}

+++**Cosa succede quando più regole di limite vengono applicate a una singola offerta?**

Il limite massimo di un&#39;offerta viene raggiunto non appena **viene soddisfatta una singola condizione**. In presenza di più regole di limite, l’offerta non viene più visualizzata quando una regola raggiunge la soglia.

**Esempio:**
Se definisci due regole di limite per un’offerta:
* 5 volte per profilo a settimana
* 100 volte il totale per tutti gli utenti

L’offerta cesserà di essere visualizzata a un utente che l’abbia vista 5 volte in una settimana, anche se il limite totale di 100 non è ancora stato raggiunto. Allo stesso modo, una volta raggiunto il totale di 100 impression, l’offerta non viene più visualizzata da tutti gli utenti.

Ulteriori informazioni sulle [regole per la limitazione dei limiti](items.md#capping).

+++

## Formule di classificazione {#ranking-formulas}

+++**Qual è il ruolo dei tipi di pubblico rispetto a un set di dati completo nei modelli di IA?**

Durante la configurazione di [modelli AI](ranking/ai-models.md), sia i set di dati che i tipi di pubblico hanno scopi distinti.

* **Set di dati**: acquisisce eventi di conversione (clic, ordini, ricavi) che fungono da target di ottimizzazione per il modello.
* **Tipi di pubblico**: funge da variabile predittiva che consente al modello di personalizzare i consigli in base all&#39;iscrizione al segmento del cliente.

I tipi di pubblico non limitano né espandono l’ambito del modello. Al contrario, forniscono attributi contestuali che migliorano la capacità del modello di effettuare previsioni personalizzate tra diversi segmenti di clienti.

Entrambi i componenti sono necessari per le prestazioni effettive del modello [modelli di ottimizzazione personalizzati](ranking/personalized-optimization-model.md).

+++

+++**In che modo le modifiche alle raccolte di offerte influiscono sui modelli di ottimizzazione automatica o personalizzata?**

Il modello di ottimizzazione automatica indirizza il traffico alla migliore offerta disponibile successiva in base ai dati di traffico degli ultimi 14 giorni, indipendentemente dal fatto che il modello di ottimizzazione personalizzata utilizzi i dati di traffico degli ultimi 30 giorni.

Quando diverse offerte vengono rimosse simultaneamente e le offerte rimanenti presentano dati di traffico minimi entro la finestra di 14 o 30 giorni, il modello può mostrare un comportamento non ottimale, inclusi pattern di distribuzione casuali o distorsioni verso offerte con tassi di conversione più elevati basati su dati di impression limitati.

**Best practice**: quando modifichi in modo significativo le raccolte di offerte, verifica che le offerte rimanenti dispongano di dati cronologici sulle prestazioni sufficienti per mantenere l&#39;efficacia del modello.

+++

+++**Con quale rapidità i modelli AI incorporano le nuove offerte?**

I modelli di intelligenza artificiale identificano e iniziano a testare le nuove offerte disponibili sul loro prossimo ciclo di formazione:

* **Ottimizzazione automatica**: ogni giorno
* **Ottimizzazione personalizzata**: settimanale

Una volta identificati, entrambi i modelli inizieranno a fornire le nuove offerte ad alcuni visitatori immediatamente per testarne le prestazioni e raccogliere dati sulla loro efficacia.

Ulteriori informazioni sui modelli [ottimizzazione automatica](ranking/auto-optimization-model.md) e [ottimizzazione personalizzata](ranking/personalized-optimization-model.md).

+++

+++**Come vengono ottimizzati i modelli AI senza gruppi di controllo?**

Sia i modelli di ottimizzazione automatica che quelli di ottimizzazione personalizzata utilizzano una strategia di &quot;esplorazione e sfruttamento&quot; che elimina la necessità di gruppi di controllo dedicati.

* **Fase iniziale**: i modelli iniziano con un&#39;esplorazione del 100%, eseguendo test su offerte diverse per stabilire i dati delle prestazioni di base.
* **Ottimizzazione adattiva**: con l&#39;accumularsi degli eventi comportamentali e il miglioramento della precisione delle previsioni, i modelli bilanciano automaticamente l&#39;esplorazione e lo sfruttamento.
* **Apprendimento in corso**: il sistema alloca progressivamente più traffico alle offerte ad alte prestazioni, continuando a testare le alternative.

Questo garantisce l’apprendimento continuo e l’ottimizzazione di tutto il traffico senza richiedere gruppi di controllo separati.

+++

+++**Quali sono i requisiti minimi di traffico per le prestazioni ottimali del modello di intelligenza artificiale?**

Adobe consiglia le seguenti soglie minime per garantire prestazioni efficaci del modello:
* 1.000 impression per offerta/oggetto a settimana
* 100 eventi di conversione per offerta/articolo a settimana

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Per impostazione predefinita, il sistema non tenta di generare modelli personalizzati per offerte/articoli con meno di 1.000 impression o 50 eventi di conversione.

>[!NOTE]
>
>In ambienti di produzione con cataloghi di offerte di grandi dimensioni (~300 offerte) e regole aziendali restrittive, alcune offerte potrebbero avvicinarsi a soglie assolute più basse (250 impression e 25 conversioni ogni 30 giorni). Questi rappresentano i requisiti minimi di dati per la formazione dei modelli, ma potrebbero non garantire prestazioni ottimali.

Ulteriori informazioni su [requisiti raccolta dati](data-collection/data-collection.md).

+++

+++**In che modo offerte simili influiscono sulle prestazioni del modello di IA?**

I modelli AI generano vantaggi di personalizzazione maggiori quando le offerte interessano segmenti di clienti distinti. Quando le offerte sono molto simili, sono tipici due risultati:

* **Prestazioni equivalenti**: le offerte hanno prestazioni identiche e ricevono una distribuzione del traffico approssimativamente uguale.
* **Offerta dominante**: differenze minori causano prestazioni migliori di un&#39;offerta su tutti i segmenti, con la maggior parte del traffico generato.

>[!NOTE]
>
>La differenziazione delle offerte non garantisce una distribuzione equilibrata del traffico. Le offerte con proposte di valore oggettivamente superiori (ad esempio, sconto di €100 rispetto a €50) solitamente dominano su tutti i segmenti di clienti indipendentemente dalle attività di personalizzazione.

**Best practice**: progetta offerte con differenziazioni significative che si allineano con preferenze distinte del segmento di clienti per massimizzare l&#39;efficacia del modello di intelligenza artificiale.

+++

+++**In che modo le anomalie del traffico influiscono sulle prestazioni del modello di IA?**

Le anomalie di traffico vengono incorporate nel modello in modo proporzionale nell&#39;intervallo continuo di 30 giorni, che fornisce stabilità al modello durante fluttuazioni temporanee del traffico. Picchi o cadute a breve termine non compromettono in modo significativo le previsioni o le prestazioni dei modelli.

Un picco di traffico temporaneo (ad esempio, il doppio del traffico giornaliero) ha un effetto minimo sulle prestazioni complessive del modello, perché il traffico anomalo rappresenta una piccola frazione del set di dati di 30 giorni.

+++
