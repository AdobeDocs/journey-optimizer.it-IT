---
solution: Journey Optimizer
product: journey optimizer
title: Collaboratore per Decisioning
description: Scopri le competenze CX Enterprise Coworker disponibili per Decisioning in Adobe Journey Optimizer, tra cui Esplora decisioni e Rules & Ranking, con istruzioni approfondite e prompt di esempio.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 8ac4ba8290929e31cd9f7494b63362bc2613d68c
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 1%
---

# Collaboratore per Decisioning {#experience-decisioning-coworker-skills}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri le competenze CX Enterprise Coworker disponibili per prendere decisioni in Adobe Journey Optimizer: scopri perché un&#39;offerta è stata o non è stata mostrata a un profilo o a un segmento e come creare, spiegare, simulare e ottimizzare le regole di idoneità e le formule di classificazione, con istruzioni dettagliate, prompt di esempio e best practice.

Ulteriori informazioni:

* [Competenze dei collaboratori per Journey Optimizer](../start/ai-features.md#cx-coworker-skills): panoramica delle competenze dei collaboratori tra Percorsi, fedeltà, gestione dei contenuti e decisioni in Journey Optimizer.
* [Documentazione di Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"}: panoramica delle funzionalità Campagne, Chat e Progetti di Coworker.
* [Guida all&#39;interfaccia utente di Chat con i collaboratori](https://experienceleague.adobe.com/it/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"}: come accedere e navigare in Chat con i collaboratori.

>[!ENDSHADEBOX]

## Esplora decisioni {#decisioning-explainer}

>[!AVAILABILITY]
>
>Decisioning Explainer è disponibile per tutti i clienti che hanno accesso a Coworker and Decisioning.

Decisioning Explainer risponde, in linguaggio naturale, al motivo per cui un’offerta specifica è stata o non è stata mostrata a un determinato profilo — o, più in generale, al motivo per cui un segmento di profili non visualizza un’offerta. Percorre l’intero stack decisionale per il profilo (o segmento) e l’intervallo di tempo richiesti: quali offerte erano idonee, quale regola di idoneità ha incluso o escluso ciascuna di esse, se la limitazione della frequenza o dell’affaticamento ha eliminato l’offerta, i punteggi di classificazione finali e quale strategia o modello di intelligenza artificiale le ha prodotte e su quale pool di candidati (raccolta di elementi) è stato valutato il profilo.

Questo affronta una sfida comune per gli esperti di marketing: spiegare perché un’offerta si è classificata al di sopra di un’altra o perché una decisione di offerta specifica è avvenuta nello stesso modo. Decisioning Explainer è di sola lettura: spiega le decisioni ma non modifica le regole, le formule di classificazione o le strategie di selezione.

### Casi d’uso principali

* **Perché un&#39;offerta specifica è stata o non è stata visualizzata**

  Prompt di esempio:
  * &quot;Perché il profilo 12345 visto l’offerta X il 15 maggio?&quot;
  * &quot;Il profilo X non era idoneo per questa offerta?&quot;
  * &quot;Quale regola di idoneità ha escluso questo cliente?&quot;
  * &quot;Mostra le offerte per le quali il profilo X era idoneo il 3 giugno.&quot;

* **Perché la visibilità di un&#39;offerta è cambiata nel tempo**

  Prompt di esempio:
  * &quot;Perché l’offerta Y non viene più visualizzata ai clienti fidelizzati negli ultimi 7 giorni?&quot;
  * &quot;Quante volte il cliente ha visto questa offerta?&quot;
  * &quot;Questa offerta era limitata al profilo X?&quot;
  * &quot;Quali offerte vengono attualmente soppresse per il profilo X a causa di vincoli di limite?&quot;

* **Classificazione o selezione di un&#39;offerta**

  Prompt di esempio:
  * &quot;Descrivi esattamente come è stata selezionata l’offerta Z rispetto alle altre offerte idonee per questo profilo.&quot;
  * &quot;Qual è stato il punteggio di classificazione per ogni offerta in questa decisione?&quot;
  * &quot;Perché l’offerta ha superato l’offerta B per questo profilo?&quot;
  * &quot;Quali fattori hanno influenzato maggiormente il risultato della classificazione?&quot;

* **Spiegazioni a livello di segmento**

  Decisioning Explainer può aggregare questa logica in un segmento anziché in un singolo profilo, evidenziando il motivo principale per cui un gruppo di profili non visualizza un’offerta.

  Prompt di esempio:
  * &quot;Qual è il motivo più comune per cui i clienti di questo pubblico vengono esclusi?&quot;
  * &quot;Quali offerte sta ricevendo questo segmento?&quot;
  * &quot;Perché il mio segmento di fedeltà non vede questa offerta?&quot;

### Best practice per la richiesta di informazioni

* **ID di riferimento quando noti**: fornisci l&#39;ID profilo, il nome dell&#39;offerta o del segmento per ottenere una traccia precisa anziché una risposta generale.
* **Includi un intervallo di tempo**: specifica una data o un intervallo di date quando ti chiedi perché la visibilità di un&#39;offerta è cambiata, in modo che il collaboratore possa eseguire correttamente l&#39;ambito della traccia.
* **Richiedi direttamente la suddivisione della classificazione**: se desideri ottenere dettagli sul punteggio, chiedi esplicitamente il punteggio della classificazione o i fattori che hanno influenzato il risultato.
* **Utilizza le domande a livello di segmento per le tendenze**: quando indaghi il motivo per cui un gruppo di profili non visualizza un&#39;offerta, chiedi informazioni sul segmento anziché su un singolo profilo per ottenere il motivo principale.

## Regole e classificazione {#rules-ranking}

>[!AVAILABILITY]
>
>Rules &amp; Ranking è disponibile per tutti i clienti che hanno accesso a Coworker and Decisioning.

Rules &amp; Ranking offre agli esperti di marketing assistenza basata sull’intelligenza artificiale per creare, comprendere e testare la logica decisionale, senza dover scrivere o convalidare manualmente la sintassi PQL. Include quattro funzionalità di base: creazione di regole in linguaggio naturale, spiegazione di regole e formule di classificazione in inglese semplice, simulazione rispetto a un massimo di 3 profili di test e ottimizzazione PQL. Ha l’ambito delle regole di idoneità e delle formule di classificazione, non crea né modifica strategie di selezione o criteri di decisione.

### Casi d’uso principali

* **Creazione regola linguaggio naturale**

  Converti una descrizione in linguaggio semplice in sintassi per le regole di idoneità di PQL, sia per le regole nuove che per quelle esistenti.

  Prompt di esempio:
  * &quot;È possibile creare una regola di idoneità che esegua il targeting degli utenti che soddisfano le condizioni XYZ?&quot;
  * &quot;Creare una regola di idoneità per i membri fedeltà di livello 2 o superiore.&quot;
  * &quot;Scrivere una regola PQL che escluda i clienti che hanno effettuato un acquisto negli ultimi 7 giorni.&quot;
  * &quot;Modificare questa regola per escludere anche i clienti nell’elenco di soppressione.&quot;

* **Spiegazione regola e formula in inglese semplice**

  Spiega cosa fa una regola di idoneità o una formula di classificazione esistente, cosa include o esclude e cosa significa ogni condizione, senza dover leggere la sintassi PQL.

  Prompt di esempio:
  * &quot;Potete spiegarmi questa regola nel linguaggio naturale?&quot;
  * &quot;Cosa fa realmente questa formula di classificazione?&quot;
  * &quot;A chi è destinata e a chi esclude questa regola di idoneità?&quot;
  * &quot;Riassumi questa regola in una frase.&quot;
  * &quot;Perché l’offerta di un livello superiore all’offerta B per questo cliente?&quot;
  * &quot;Questa regola è troppo restrittiva per una vasta campagna di sensibilizzazione?&quot;
  * &quot;Quale condizione in questa regola filtra il maggior numero di profili?&quot;

* **Simulazione**

  Esegui una regola di idoneità o una formula di classificazione rispetto a un massimo di 3 profili di test, inseriti manualmente o generati dall’intelligenza artificiale, inclusi i casi limite, e ottieni risultati di esito positivo/negativo con la condizione di errore specifica o un elenco classifica di offerte con punteggi numerici.

  Prompt di esempio:
  * &quot;Simula questa regola con i profili di test.&quot;
  * &quot;Questa regola viene applicata a un profilo in cui loyalty_tier = gold?&quot;
  * &quot;Quali profili superano questa regola di idoneità: [profilo A, profilo B, profilo C]?&quot;
  * &quot;Perché questo profilo non ha superato il controllo di idoneità?&quot;
  * &quot;Genera profili di test per questa regola di idoneità.&quot;
  * &quot;Genera profili di casi edge che sottopongono a test di stress questa condizione&quot;.
  * &quot;Simula questa formula di classificazione tra queste offerte e profili.&quot;
  * &quot;Quale offerta risulterebbe più elevata per questo profilo data questa formula?&quot;
  * &quot;Confrontare il comportamento di questa regola di idoneità per un cliente di livello Gold rispetto a un cliente di livello Silver rispetto a un cliente di livello Basic.&quot;

* **Ottimizzazione PQL**

  Riscrivi una regola o una formula esistente con una sintassi più concisa per soddisfare i limiti di dimensione PQL di Journey Optimizer, senza modificarne la logica o il risultato.

  Prompt di esempio:
  * &quot;Ottimizza questa regola PQL per me.&quot;
  * &quot;Questa regola sta raggiungendo i limiti di dimensione di PQL — puoi abbreviarla?&quot;

### Best practice per la richiesta di informazioni

* **Fornisci la condizione di destinazione in modo esplicito**: durante la creazione o la modifica di una regola, specifica il pubblico, l&#39;attributo o la condizione di esclusione desiderati.
* **Fai riferimento direttamente alla regola o alla formula**: quando chiedi una spiegazione, una simulazione o un&#39;ottimizzazione, assicurati che la regola o la formula che intendi sia aperta o chiaramente identificata.
* **Richiedi casi limite**: durante la simulazione, chiedi a Coworker di generare profili di casi limite per testare una condizione, non solo quelle tipiche.
* **Rivedi prima di pubblicare**: controlla la logica e i risultati della simulazione di una regola generata o ottimizzata prima di pubblicarla.

{{$include /help/_includes/do-not-localize/start/ai-augmented-experience-decisioning-coworker-skills.md}}
