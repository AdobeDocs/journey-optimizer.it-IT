---
title: Gestione dei conflitti e assegnazione delle priorità
description: Scopri come sfruttare gli strumenti per i conflitti e l’assegnazione delle priorità di Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
TQID: https://experienceleague.adobe.com/vx-CmsYwj7QyN2sVMrpJ9VUNDgnXq8qt1nT9lHOFV3s
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fd59660e-de8a-4bfb-85dc-7fa546030c49
subfeature_v2:
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: f3fe4813-f254-4f8f-99cc-24bd67f119e1
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
source-git-commit: 49542ca70e8899061bc79772cf96069ab2587ab2
workflow-type: tm+mt
source-wordcount: 896
ht-degree: 96%

---

# Gestione dei conflitti e assegnazione delle priorità {#conflict-prioritization}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come funzionano insieme il rilevamento dei conflitti, i punteggi di priorità e i set di regole in modo da evitare la sovrapposizione delle comunicazioni e controllare la frequenza con cui vengono inviati messaggi ai clienti.

>[!ENDSHADEBOX]

In Journey Optimizer, è essenziale gestire il volume e le tempistiche delle campagne e dei percorsi per evitare di sopraffare le persone con troppe interazioni. La gestione dei conflitti e gli strumenti per l’assegnazione delle priorità in Adobe Journey Optimizer consentono di fornire comunicazioni ponderate e puntuali, evitando una sollecitazione eccessiva delle persone e assicurando che il pubblico riceva sempre i messaggi giusti. Tramite il rilevamento di conflitti, i punteggi di priorità e i set di regole, puoi semplificare le campagne e i percorsi per evitare sovrapposizioni e bilanciarne la frequenza su tutti i canali.

Questi strumenti sono disponibili per le campagne e per i percorsi unitari, di qualificazione del pubblico e di tipo “Leggi pubblico”. Queste funzioni lavorano in sinergia per semplificare il processo decisionale e ottimizzare la strategia di marketing, sia per impostare limiti sulla frequenza di invio dei messaggi o di decidere quali campagne abbiano la precedenza.

## Da dove iniziare {#where-to-start}

| Il tuo obiettivo | Strumento | Azione |
|-----------|------|--------|
| Verificare se i percorsi o le campagne presentano sovrapposizioni (timeline, pubblico, canale) | **Rilevamento di conflitti** | [Identificare conflitti potenziali](conflicts.md) |
| Stabilire il messaggio vincitore quando un profilo si qualifica per più messaggi | **Punteggi di priorità** | [Assegnare punteggi di priorità](priority-scores.md) |
| Limitare la frequenza o il numero di messaggi ricevuti da un profilo | **Set di regole** (quota limite, limitazione del percorso, ore di silenzio) | [Impostare le regole di limitazione dei messaggi e dei percorsi](../../rp_landing_pages/capping-rules-landing-page.md) |

**Flusso tipico:** utilizza il rilevamento dei conflitti per individuare le sovrapposizioni, quindi applica punteggi di priorità e set di regole per controllare quali messaggi vengono inviati e con quale frequenza.

## Strumenti per l’assegnazione delle priorità e la gestione dei conflitti {#tools}

### Strumento di rilevamento dei conflitti

Con lo **strumento di rilevamento dei conflitti**, è possibile identificare potenziali sovrapposizioni in percorsi e campagne. Questo è fondamentale, in quanto troppe comunicazioni simultanee possono causare un affaticamento della clientela. Journey Optimizer consente di monitorare elementi quali timeline, sovrapposizione del pubblico e configurazioni del canale. Identificando i conflitti per tempo, puoi perfezionare le campagne per evitare di inviare ai clienti troppi messaggi allo stesso tempo.

[Scopri come rilevare potenziali conflitti in percorsi e campagne](conflicts.md)

### Punteggi di priorità

I **punteggi di priorità** ti aiutano a controllare quali campagne o percorsi hanno la precedenza nei casi cui una persona risulti idonea a più comunicazioni. Questa funzione è particolarmente utile per i canali in entrata, come web e mobile, dove è possibile presentare una sola campagna in un dato momento. Assegnando un punteggio di priorità a ogni percorso o campagna, puoi garantire che venga consegnato per primo il messaggio più importante.

[Scopri come assegnare punteggi di priorità a percorsi e campagne](priority-scores.md)

### Set di regole

I set di regole consentono di **raggruppare più regole** e di applicarle ai percorsi e alle campagne scelte. Questo fornisce una migliore granularità per limitare la frequenza e il numero di percorsi in cui può entrare una persona entro un determinato arco temporale o per controllare la frequenza con cui gli utenti ricevono un messaggio a seconda del tipo di comunicazione.

* **Limitazione dei percorsi e arbitrato**: limita la frequenza e il numero di percorsi a cui una persona può accedere entro un determinato arco temporale. Puoi limitare il numero di ingressi nei percorsi per un profilo oppure il numero di percorsi in quali una persona può essere iscritta contemporaneamente. Utilizza le impostazioni di arbitrato per decidere in quale percorso una persona può entrare, qualora si risulti idonea per più percorsi, utilizzando i punteggi di priorità per determinare quello più adatto. [Scopri come utilizzare la limitazione del percorso e l’arbitrato](journey-capping.md)

* **Quota limite per canale e tipo di comunicazione**: imposta la quota limite in base al tipo di comunicazione (ad esempio vendite, promozionale) per evitare di sovraccaricare i clienti con messaggi simili. Controlla la frequenza su più canali, escludendo automaticamente i profili eccessivamente sollecitati. [Scopri come impostare la quota limite per tipo di comunicazione e canale](channel-capping.md)

* **Ore di silenzio**: definisci le esclusioni basate sul tempo in modo che non vengano inviati messaggi durante periodi specifici (e-mail, SMS, push, WhatsApp). [Scopri come impostare le ore di silenzio](quiet-hours.md)

[Scopri come utilizzare i set di regole](rule-sets.md)

## Guardrail e limitazioni {#guardrails}

* **Campagne e punteggi di priorità** - Nelle campagne, il punteggio di priorità è disponibile solo per i canali in entrata **web**, **in-app** e **basati su codice**.

* **Latenza nell’aggiornamento del contatore di profili**: dopo l’ingresso di una persona in un percorso, l’aggiornamento del valore del contatore di profili può richiedere fino a 10 minuti. Se un profilo effettua l’ingresso in due percorsi in un breve intervallo di tempo, il secondo percorso potrebbe non rilevare correttamente che il limite di frequenza è già stato raggiunto, consentendo potenzialmente al profilo di accedere a entrambi.

* **Priorità dello spazio dei nomi per la limitazione degli ingressi nel percorso**: la limitazione degli ingressi è supportata solo se lo spazio dei nomi selezionato nel percorso è quello con la priorità più elevata definita nella sandbox. Se la priorità dello spazio dei nomi non è stata configurata in modo esplicito, la priorità più elevata predefinita è quella e-mail.

* **Attivazioni simultanee nei percorsi di qualificazione del pubblico**: quando più percorsi di qualificazione del pubblico vengono attivati dallo stesso evento di qualificazione, i conteggi per la limitazione degli ingressi non risulteranno accurati. Se i conteggi sono inferiori al limite, il percorso continuerà ad arbitrare, ma in caso di attivazioni simultanee non sarà in grado di ottenere i conteggi più aggiornati.

## Risorse aggiuntive

* **[Identificare potenziali conflitti](conflicts.md)**: scopri come rilevare e risolvere i conflitti tra le campagne e i percorsi sovrapposti.
* **[Assegnare punteggi di priorità](priority-scores.md)**: informazioni su come assegnare e utilizzare i punteggi di priorità per controllare la precedenza della consegna dei messaggi.
* **[Utilizzare set di regole](rule-sets.md)**: scopri come creare set di regole per la gestione dei conflitti e la governance dei messaggi.
* **[Limitazione del percorso e arbitrato](journey-capping.md)**: configura l’arbitrato e le regole di limitazione a livello di percorso.
* **[Quota limite per canale](channel-capping.md)**: imposta le quote limite a livello di canale per evitare l’invio eccessivo di messaggi.
* **[Impostare le ore di silenzio](quiet-hours.md)**: definisci le esclusioni basate sul tempo per la consegna dei messaggi.
* **[Tutorial sulla gestione dei conflitti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}**: tutorial video dettagliati.
* **[Casi d’uso di Journey Optimizer](../building-journeys/jo-use-cases.md)**: sfoglia i pattern pratici, incluse la quota limite e la logica di soppressione del percorso.
