---
solution: Journey Optimizer
product: journey optimizer
title: Attività Attendi
description: Scopri come configurare l’attività Attendi
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attendi, attività, percorso, successivo, area di lavoro
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qWxnLiuHh-sJQyUOuRB6CgRIpZ6ud6eO-WNoWcv9JeU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1589
ht-degree: 8%

---

# Attività Attendi {#wait-activity}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come configurare l&#39;attività Attendi per sospendere un percorso per una durata relativa o fino a una data calcolata personalizzata prima dell&#39;esecuzione dell&#39;attività successiva.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Attività Attendi"
>abstract="L’attività Attendi ti consente di attendere prima di eseguire l’attività successiva nel percorso. Consente di stabilire il momento in cui verrà eseguita l’attività successiva. Sono disponibili due opzioni: durata e personalizzato."

Puoi utilizzare un&#39;attività **[!UICONTROL Wait]** per definire una durata prima di eseguire l&#39;attività successiva.  La durata massima di attesa è di **90 giorni**.

È possibile impostare due tipi di attività **Attendi**:

* Un’attesa basata su una durata relativa. [Ulteriori informazioni](#duration)
* Una data personalizzata, utilizzando le funzioni per calcolarla. [Ulteriori informazioni](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Consigli {#wait-recommendations}

Utilizza queste raccomandazioni per mantenere le attese prevedibili e sicure.

### Attività di attesa multiple {#multiple-wait-activities}

Quando utilizzi più attività **Wait** in un percorso, tieni presente che il [timeout globale](journey-properties.md#global_timeout) per i percorsi è di 91 giorni, il che significa che i profili vengono sempre eliminati dal massimo percorso 91 giorni dopo l&#39;immissione. Ulteriori informazioni sono disponibili in [questa pagina](journey-properties.md#global_timeout).

Una persona può accedere a un&#39;attività **Wait** solo se nel percorso è rimasto abbastanza tempo per completare la durata dell&#39;attesa prima del timeout di 91 percorsi.

### Attendere e rientrare {#wait-reentrance}

È consigliabile non utilizzare le attività **Wait** per bloccare il rientro. Utilizza invece l&#39;opzione **Consenti rientro** a livello di proprietà del percorso. Ulteriori informazioni sono disponibili in [questa pagina](../building-journeys/journey-properties.md#entrance).

### Modalità di attesa e test {#wait-test-mode}

In modalità di test, il parametro **[!UICONTROL Wait time in test]** (Tempo di attesa nel test) consente di definire la durata di ogni attività **Wait**. Il tempo predefinito è di 10 secondi. In questo modo potrai ottenere rapidamente i risultati del test. Ulteriori informazioni sono disponibili in [questa pagina](../building-journeys/testing-the-journey.md).

### Canali attendi e mobili {#wait-mobile-channels}

Se desideri visualizzare un [messaggio in-app](../in-app/create-in-app.md) poco dopo aver inviato una [notifica push](../../rp_landing_pages/push-landing-page.md), utilizza un&#39;attività **Attendi** per consentire la propagazione del tempo di payload del messaggio in-app. In genere si consiglia un’attesa di 5-15 minuti, ma i tempi esatti possono variare a seconda della complessità del payload e delle esigenze di personalizzazione.

## Configurazione {#wait-configuration}

Configura qui la durata e il tempo di attesa.

### Attesa durata {#duration}

Selezionare il tipo **Durata** per impostare la durata relativa dell&#39;attesa prima dell&#39;esecuzione dell&#39;attività successiva. La durata massima è di **90 giorni**.

![Definisci la durata dell&#39;attesa](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![Wait activity configuration panel with duration and fixed date options](assets/journey56.png)
-->

### Attesa personalizzata {#custom}

Seleziona il tipo **Personalizzato** per definire una data personalizzata, utilizzando un&#39;espressione avanzata basata su un campo proveniente da un evento o una risposta a un&#39;azione personalizzata. Non è possibile definire direttamente una durata relativa, ad esempio 7 giorni, ma è possibile utilizzare le funzioni per calcolarla se necessario (ad esempio, 2 giorni dopo l’acquisto).

![Definisci un&#39;attesa personalizzata con un&#39;espressione](assets/journey57.png)

L&#39;espressione nell&#39;editor deve fornire un formato `dateTimeOnly`. Consulta [questa pagina](expression/expressionadvanced.md). Per ulteriori informazioni sul formato dateTimeOnly, vedere [questa pagina](expression/data-types.md).

Si consiglia di utilizzare date personalizzate specifiche per i profili ed evitare di utilizzare la stessa data per tutti. Ad esempio, non definire `toDateTimeOnly('2024-01-01T01:11:00Z')`, ma `toDateTimeOnly(@event{Event.productDeliveryDate})` specifico per ciascun profilo. Tieni presente che l’utilizzo di date fisse può causare problemi nell’esecuzione del percorso. Ulteriori informazioni sull&#39;impatto delle attività Attendi sulla velocità di elaborazione del percorso in [questa sezione](entry-management.md#wait-activities-impact).


>[!CAUTION]
>
>Quando si utilizzano espressioni `dateTimeOnly`, tenere presente quanto segue:
>
>* È possibile utilizzare direttamente un&#39;espressione `dateTimeOnly` o convertirla utilizzando una funzione, ad esempio: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})` dove il valore del campo è nel formato `2023-08-12T09:46:06Z`.
>* Il **fuso orario** è definito nelle proprietà del percorso. Di conseguenza, non è possibile dall’interfaccia utente puntare a un timestamp ISO-8601 completo che combina l’offset di ora e fuso orario, ad esempio `2023-08-12T09:46:06.982-05`. [Ulteriori informazioni](../building-journeys/timezone-management.md)
>* Durante la creazione di un&#39;espressione di attesa personalizzata con `toDateTimeOnly()`, **not** aggiungere `Z` o un offset del fuso orario (ad esempio, `-05:00`). L’espressione deve fare riferimento al fuso orario configurato nel percorso senza indicatori di fuso orario espliciti, altrimenti i profili potrebbero bloccarsi nell’attività Attendi.
>
>| | Esempio |
>| --- | --- |
>| **Corretto** | `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00"))` |
>| **Errato** | `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00Z"))` ❌ (contiene `Z`) |

Per verificare che l’attività Attendi funzioni come previsto, puoi utilizzare gli eventi dei passaggi. [Ulteriori informazioni](../reports/query-examples.md#common-queries).

## Aggiornamento profilo dopo l’attesa {#profile-refresh}

Quando un profilo viene parcheggiato in un&#39;attività **Wait** in un percorso che inizia con un&#39;attività **Read Audience**, il percorso aggiorna automaticamente gli attributi del profilo da Servizio profili unificato (UPS) per recuperare i dati disponibili più recenti.

* **Alla voce percorso**: i profili utilizzano i valori degli attributi dello snapshot del pubblico valutato all&#39;avvio del percorso.
* **Dopo un nodo di attesa**: il percorso esegue una ricerca per recuperare i dati di profilo più recenti da UPS, non i dati snapshot precedenti. Ciò significa che gli attributi del profilo possono essere cambiati dall’inizio del percorso.

Questo comportamento assicura che le attività a valle utilizzino le informazioni correnti del profilo dopo un periodo di attesa. Tuttavia, potrebbero verificarsi risultati imprevisti se si prevede che il percorso utilizzi solo i dati snapshot originali durante l&#39;esecuzione.

Esempio: se un profilo è idoneo per un pubblico &quot;cliente silver&quot; all’inizio del percorso, ma viene aggiornato a &quot;cliente gold&quot; durante un’attesa di 3 giorni, le attività successive all’attesa visualizzeranno lo stato &quot;cliente gold&quot; aggiornato.

## Nodo di attesa automatico  {#auto-wait-node}

>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node"
>title="Informazioni sul nodo di attesa automatico"
>abstract="Un nodo di **attesa** viene inserito automaticamente dopo questa azione in entrata. Il valore predefinito è impostato su 3 giorni, garantendo che i profili rimangano nel percorso il tempo sufficiente per visualizzare il messaggio o l’esperienza. La durata dell’attesa può essere aggiornata, oppure il nodo può essere rimosso, se il caso d’uso lo richiede."

Ogni attività esperienza in entrata (messaggio in-app, esperienza basata su codice o scheda) viene fornita con un&#39;attività **Wait** di 3 giorni. Poiché i messaggi in entrata terminano automaticamente quando un profilo raggiunge la fine del percorso, si presume che gli utenti debbano visualizzarlo almeno per 3 giorni. Puoi rimuovere questa attività **Attendi** o modificarne la configurazione, se necessario.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come configurare l&#39;attività Attendi in un percorso per sospendere la progressione del profilo per una durata relativa o fino a una data calcolata personalizzata prima di eseguire il passaggio successivo.

**Intenti:**

* Aggiungi un’attività Attendi per sospendere un percorso per una durata relativa fissa (fino a 90 giorni)
* Configura un’attesa personalizzata utilizzando un’espressione avanzata per posticipare la data calcolata specifica per il profilo
* Comprendere come le attività di attesa interagiscono con il timeout globale del percorso (91 giorni)
* Utilizza il parametro Wait time in test (Tempo di attesa nel test) per velocizzare la convalida della modalità di test
* Scopri come gli attributi del profilo vengono aggiornati dopo un nodo Wait in Read Audience percorsi

**Glossario:**

* **Attività di attesa**: un&#39;attività di orchestrazione del percorso che mette in pausa la progressione del profilo per una durata specificata o fino a una data calcolata prima dell&#39;esecuzione dell&#39;attività successiva *(specifico per prodotto)*
* **Attesa durata**: tipo di attesa che imposta un periodo di tempo relativo da sospendere, con un massimo di 90 giorni *(specifico per prodotto)*
* **Attesa personalizzata**: tipo di attesa che utilizza un&#39;espressione `dateTimeOnly` derivata dai dati del profilo o dell&#39;evento per definire una data/ora futura specifica per la ripresa *(specifica per prodotto)*
* **Nodo di attesa automatico**: un&#39;attività di attesa di 3 giorni inserita automaticamente dopo le attività esperienza in entrata (in-app, basate su codice, scheda) per mantenere il profilo nel percorso abbastanza a lungo da visualizzare il contenuto *(specifico per prodotto)*
* **Tempo di attesa nel test**: un parametro della modalità di test del percorso che ignora le durate di attesa effettive (impostazione predefinita: 10 secondi), in modo che i risultati del test vengano restituiti rapidamente *(specifico per prodotto)*

**Guardrail:**

* La durata massima di attesa è di 90 giorni.
* I profili vengono eliminati da un percorso dopo 91 giorni (timeout globale), indipendentemente dalle attività di attesa in sospeso.
* Un profilo può entrare in un’attività Attendi solo se nel percorso rimane tempo sufficiente per completare l’attesa prima del timeout di 91 giorni.
* Non utilizzare le attività Attendi per bloccare il rientro; utilizza invece l’opzione Consenti rientro nelle proprietà del percorso.
* Le espressioni di attesa personalizzate devono utilizzare il formato `dateTimeOnly` e non devono includere un suffisso `Z` o uno scostamento fuso orario esplicito.
* L&#39;utilizzo di una data statica fissa (ad esempio, `toDateTimeOnly('2024-01-01T01:11:00Z')`) in un&#39;attesa personalizzata può causare problemi; utilizzare invece date dinamiche specifiche per il profilo.
* Gli attributi del profilo vengono aggiornati da Unified Profile Service dopo un nodo di attesa in Read Audience percorsi, che può produrre risultati imprevisti se si prevede la coerenza delle istantanee.

**Terminologia:**

* Nome canonico: Wait activity — Acronimo: none — varianti: Wait node, wait step
* Sinonimi: &quot;Attesa durata&quot; = &quot;Attesa relativa&quot;; &quot;Attesa personalizzata&quot; = &quot;Attesa basata su espressione&quot;
* Non confondere: &quot;Attesa durata&quot; (relativa, ad esempio 3 giorni da ora) ≠ &quot;Attesa personalizzata&quot; (data calcolata assoluta dai dati del profilo)

**Domande frequenti:**

* **Q: Qual è la durata massima di un&#39;attività Attendi?** — La durata massima di attesa è di 90 giorni; anche i profili sono soggetti al timeout di percorso globale di 91 giorni.
* **Q: in che modo la modalità di test gestisce le attività di attesa?** — In modalità di test, il parametro &quot;Wait time in test&quot; (Tempo di attesa nel test) ignora la durata di attesa effettiva; il valore predefinito è 10 secondi, pertanto i test vengono completati rapidamente.
* **Q: perché evitare di aggiungere Z a un&#39;espressione di attesa personalizzata?** — L&#39;aggiunta di una Z o di uno scostamento di fuso orario a un&#39;espressione `toDateTimeOnly()` può bloccare i profili nell&#39;attività di attesa. L&#39;espressione deve basarsi sul fuso orario configurato del percorso.
* **Q: gli attributi del profilo vengono aggiornati dopo un nodo Wait?** — Sì, nei percorsi che iniziano con Read Audience, il percorso aggiorna gli attributi del profilo da Unified Profile Service dopo l&#39;attesa, in modo che le attività a valle possano visualizzare valori aggiornati anziché i dati dell&#39;istantanea del pubblico originale.
* **D: Cos&#39;è il nodo di attesa automatico?** — Un’attività Attendi di 3 giorni inserita automaticamente dopo le attività esperienza in entrata (in-app, basate su codice, scheda) per garantire che i profili rimangano nel percorso abbastanza a lungo per visualizzare il messaggio; può essere rimossa o riconfigurata in base alle esigenze.

+++
