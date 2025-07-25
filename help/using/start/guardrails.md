---
solution: Journey Optimizer
product: journey optimizer
title: Guardrail e limitazioni di Journey Optimizer
description: Ulteriori informazioni sui guardrail di Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 598cffda92b27f89a752d6fb0ebc032f9017c43e
workflow-type: ht
source-wordcount: '2541'
ht-degree: 100%

---

# Guardrail e limitazioni {#limitations}

Di seguito sono riportati ulteriori guardrail e limitazioni relativi all’utilizzo di [!DNL Adobe Journey Optimizer].

I diritti, le limitazioni del prodotto e i guardrail relativi alle prestazioni sono elencati nella [pagina di descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.


>[!CAUTION]
>
>* [I guardrail per i dati e la segmentazione del profilo cliente in tempo reale](https://experienceleague.adobe.com/it/docs/experience-platform/profile/guardrails){target="_blank"} vengono applicati anche a Adobe Journey Optimizer.
>
>* Consulta anche [Guardrail per l’acquisizione di dati nel Profilo cliente in tempo reale](https://experienceleague.adobe.com/it/docs/experience-platform/ingestion/guardrails){target="_blank"}


## Browser supportati {#browsers}

L’interfaccia di Adobe [!DNL Journey Optimizer] è progettata per funzionare in modo ottimale nell’ultima versione di Google Chrome. L’utilizzo di versioni precedenti o di altri browser potrebbe comportare problemi durante l’utilizzo di alcune funzioni.

## Guardrail per set di dati {#datasets-guardrails}

A febbraio 2025 è stato introdotto un guardrail time-to-live (TTL) nei set di dati di Journey Optimizer generati dal sistema in **nuove sandbox e nuove organizzazioni** come segue:

* 90 giorni per i dati nell’archivio dei profili
* 13 mesi per i dati nel data lake

Questa modifica verrà implementata nelle **sandbox della clientela esistente** in una fase successiva. [Ulteriori informazioni sui guardrail Time-To-Live (TTL) dei set di dati](../data/datasets-ttl.md)

## Guardrail per canali {#channel-guardrails}

>[!NOTE]
>
>In rare circostanze, interruzioni temporanee in una area geografica specifica possono comportare l’esclusione dai percorsi di profili validi oppure e-mail erroneamente contrassegnate come mancati recapiti. Una volta ripristinati i servizi, ricontrolla i registri del percorso, verifica i campi del profilo di consenso e, se necessario, ripubblica il percorso. In caso di interruzione di un ISP, scopri come rimuovere i profili dall’elenco di soppressione in [questa sezione](../configuration/manage-suppression-list.md#remove-from-suppression-list).
>

### Guardrail per e-mail {#message-guardrails}

Al [canale e-mail](../email/get-started-email.md) vengono applicati i seguenti guardrail:

* Con [!DNL Journey Optimizer] non è possibile aggiungere allegati a un messaggio e-mail.
* Non è possibile utilizzare lo stesso dominio di invio per inviare messaggi da [!DNL Adobe Journey Optimizer] e da un altro prodotto, come [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage] ad esempio.

### Guardrail per SMS {#sms-guardrails}

Al [canale SMS](../sms/get-started-sms.md) vengono applicati i seguenti guardrail:

* I file multimediali per MMS possono essere inclusi tramite un URL supportato. Assicurati che il file multimediale sia caricato separatamente.
* La sincronizzazione del feedback sui messaggi non è attualmente disponibile per gli MMS.
* La gestione del consenso funziona a livello del canale SMS per MMS.

### Guardrail per il canale Web {#web-guardrails}

Le [campagne web](../web/get-started-web.md) [!DNL Journey Optimizer] eseguono il targeting di nuovi profili che non sono stati precedentemente coinvolti su altri canali. In questo modo, il conteggio totale dei profili coinvolgibili verrà aumentato, il che potrebbe avere implicazioni di costo qualora si superi il numero contrattuale di profili coinvolgibili acquistati.

Le metriche di licenza per ciascun pacchetto sono elencate nella pagina [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

### Guardrail per canali basati su codice {#code-based-guardrails}

Per utilizzare le azioni di esperienza basate su codice in [!DNL Journey Optimizer] e distribuire il payload del contenuto del codice utilizzabile dalle applicazioni, segui i prerequisiti descritti in [questa pagina](../code-based/code-based-prerequisites.md).

## Guardrail delle pagine di destinazione {#lp-guardrails}

Alle [pagine di destinazione](../landing-pages/get-started-lp.md) vengono applicati i seguenti guardrail:

* Solo un componente **Modulo** può essere utilizzato in una singola pagina principale.
* Il componente **Modulo** non può essere utilizzato nelle pagine secondarie.
* Non puoi aggiungere una preintestazioni  a una pagina di destinazione.
* Non è possibile selezionare l’opzione **Crea il codice** durante la progettazione di una pagina di destinazione principale.

## Guardrail di sottodomini {#subdomain-guardrails}

Per impostazione predefinita, [!DNL Journey Optimizer] consente di delegare fino a 10 sottodomini in totale (che coprono sia i canali e-mail che i canali web).

Tuttavia, a seconda del contratto di licenza, puoi delegare fino a 100 sottodomini. Per ulteriori informazioni sul numero di sottodomini a cui hai diritto, rivolgiti al tuo referente Adobe.

Ulteriori informazioni sulla delega del dominio sono disponibili in [questa pagina](../configuration/delegate-subdomain.md).

## Guardrail per i frammenti {#fragments-guardrails}

Ai [frammenti](../content-management/fragments.md) vengono applicati i seguenti guardrail:

* I frammenti visivi sono disponibili solo per il canale e-mail.
* I frammenti di espressione non sono disponibili per il canale in-app.

## Guardrail dei tipi di pubblico {#audience}

Puoi pubblicare fino a 10 composizioni di pubblico in una determinata sandbox. Se hai raggiunto questa soglia, elimina una composizione per liberare spazio e pubblicarne una nuova.

Per ulteriori informazioni sulle composizioni del pubblico, consulta [questa pagina](../audience/get-started-audience-orchestration.md).

## Guardrail per la funzione Decisioni e la gestione delle decisioni {#decisioning-guardrails}

I guardrail e le limitazioni da tenere presenti quando si lavora con la funzione Decisioni o la gestione delle decisioni sono descritti nelle seguenti sezioni:

* [Guardrail e limitazioni per la funzione Decisioni](../experience-decisioning/decisioning-guardrails.md)
* [Guardrail e limitazioni per la gestione delle decisioni](../offers/decision-management-guardrails.md)


## Guardrail di percorso {#journeys-guardrails}

### Guardrail di percorso generale {#journeys-guardrails-journeys}

* Il numero di attività in un percorso è limitato a 50. Il numero di attività viene visualizzato nella sezione in alto a sinistra dell’area di lavoro del percorso. Questo aiuterà a migliorare la leggibilità, il controllo qualità e la risoluzione dei problemi.
* Per impostazione predefinita, il numero di percorsi di esecuzione live/in pausa/di prova è limitato a 100.  Il numero corrente di percorsi viene visualizzato sopra l’area di lavoro del percorso.
* Durante la pubblicazione dei percorsi, questi vengono scalati e regolati automaticamente per garantire la massima velocità effettiva e stabilità. In prossimità del traguardo di 100 percorsi live alla volta, nell’interfaccia utente verrà visualizzata una notifica di tale risultato. Se visualizzi questa notifica e hai la necessità di estendere i percorsi oltre ai 100 percorsi live alla volta, puoi creare un ticket per l’assistenza clienti e ti aiuteremo a raggiungere i tuoi obiettivi.
* Quando si utilizza la qualificazione del pubblico in un percorso, questa può richiedere fino a 10 minuti prima di essere attiva e poter ascoltare i profili che entrano o escono dal pubblico.
* Un&#39;istanza percorso per un profilo ha una dimensione massima di 1 MB. Tutti i dati raccolti come parte dell’esecuzione del percorso vengono archiviati nella relativa istanza. Pertanto, i dati di un evento in arrivo, le informazioni sul profilo recuperate da Adobe Experience Platform, le risposte alle azioni personalizzate, ecc. vengono archiviati in quell’istanza percorso e influiscono sulle sue dimensioni. Quando un percorso inizia con un evento, si consiglia di limitare la dimensione massima del relativo payload (ad esempio: inferiore a 800 KB) per evitare di raggiungere tale limite nell’esecuzione del percorso, dopo poche attività. Una volta raggiunto tale limite, il profilo è in stato di errore e verrà escluso dal percorso.
* Oltre al timeout utilizzato nelle attività di percorso, esiste anche un timeout di percorso globale che non viene visualizzato nell’interfaccia e non può essere modificato. Questo timeout globale interrompe l’avanzamento dei singoli utenti nel percorso 91 giorni dopo il loro ingresso. [Ulteriori informazioni](../building-journeys/journey-properties.md#global_timeout)

### Azioni generali {#general-actions-g}

Alle [azioni](../building-journeys/about-journey-activities.md) nei tuoi percorsi, vengono applicati i seguenti guardrail:

* In caso di errore vengono eseguiti sistematicamente tre tentativi. Non è possibile regolare il numero di tentativi in base al messaggio di errore ricevuto. Vengono eseguiti nuovi tentativi per tutti gli errori HTTP eccetto HTTP 401, 403 e 404.
* L’evento **Reazione** incorporato consente di reagire alle azioni predefinite. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/reaction-events.md). Se desideri reagire a un messaggio inviato tramite un’azione personalizzata, devi configurare un evento dedicato.
* Non è possibile inserire due azioni in parallelo, è necessario aggiungerle una dopo l’altra.
* Un profilo non può essere presente più volte nello stesso percorso contemporaneamente per tutte le [versioni attive del percorso](../building-journeys/publishing-the-journey.md#create-a-new-version-of-a-journey-journey-create-new-version). Se è stato abilitato il reingresso, un profilo può entrare nuovamente in un percorso, ma solo dopo essere uscito completamente dalla precedente istanza del percorso. [Ulteriori informazioni](../building-journeys/end-journey.md)

### Versioni del percorso {#journey-versions-g}

Alle [versioni del percorso](../start/user-interface.md) vengono applicati i seguenti guardrail:

* Un percorso che inizia con un’attività evento nella versione v1, nelle altre versioni non può iniziare con un elemento diverso. Non è possibile avviare un percorso con un evento **Qualificazione del pubblico**.
* Un percorso che inizia con un’attività di **Qualificazione del pubblico** nella versione v1 deve sempre iniziare con una **Qualificazione del pubblico** nelle altre versioni.
* Il pubblico e lo spazio dei nomi scelti nella **Qualificazione del pubblico** (primo nodo) non possono essere modificati nelle nuove versioni.
* La regola di reingresso deve essere la stessa in tutte le versioni del percorso.
* Un percorso che inizia con un’attività di **Leggi pubblico** non può iniziare con un altro evento nelle versioni successive.
* Non puoi creare una nuova versione di un percorso di Leggi pubblico con lettura incrementale. Devi duplicare il percorso.

### Azioni personalizzate {#custom-actions-g}

Alle [azioni personalizzate](../action/action.md) nei tuoi percorsi vengono applicati i seguenti guardrail:

* Per tutte le azioni personalizzate, viene definito un limite massimo di 300.000 chiamate in un minuto per host e per sandbox. Consulta [questa pagina](../action/about-custom-action-configuration.md). Questo limite è stato impostato in base all’utilizzo da parte della clientela, per proteggere gli endpoint esterni interessati dalle azioni personalizzate. Devi tenerne conto nei percorsi basati sul pubblico definendo una velocità di lettura appropriata (5.000 profili al secondo quando vengono utilizzate le azioni personalizzate). Se necessario, puoi ignorare questa impostazione definendo un limite di limitazione di utilizzo o di limitazione maggiore tramite le rispettive API. Consulta [questa pagina](../configuration/external-systems.md).
* L’URL dell’azione personalizzata non supporta i parametri dinamici.
* Sono supportati i metodi di chiamata POST, PUT e GET
* Il nome del parametro o dell’intestazione della query non deve iniziare con “.” oppure “$”
* Gli indirizzi IP non sono consentiti
* Non sono consentiti indirizzi di Adobe interni (`.adobe.*`) negli URL e nelle API.
* Non è possibile rimuovere le azioni personalizzate incorporate.
* Le azioni personalizzate supportano il formato JSON solo quando si utilizzano payload di richiesta o risposta. Consulta [questa pagina](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Quando scegli un endpoint per il targeting utilizzando un’azione personalizzata, assicurati che:

   * Questo endpoint possa supportare la velocità effettiva del percorso utilizzando le configurazioni della [API di limitazione](../configuration/throttling.md) o [API di limitazione di utilizzo](../configuration/capping.md) per limitarlo. Fai attenzione che una configurazione di limitazione non può scendere al di sotto di 200 TPS. Qualsiasi endpoint di destinazione dovrà supportare almeno 200 TPS.
   * Questo endpoint deve avere un tempo di risposta il più basso possibile. A seconda della velocità effettiva prevista, avere un tempo di risposta elevato potrebbe influire sulla velocità effettiva.

### Eventi {#events-g}

Agli [eventi](../event/about-events.md) nei tuoi percorsi vengono applicati i seguenti guardrail:

* Journey Optimizer supporta un volume massimo di 5.000 eventi di percorso in entrata al secondo.
* I percorsi attivati da eventi possono richiedere fino a 5 minuti per elaborare la prima azione nel percorso.
* Per gli eventi generati dal sistema, i dati in streaming utilizzati per avviare un percorso del cliente devono essere configurati prima in Journey Optimizer per ottenere un ID di orchestrazione univoco. Questo ID di orchestrazione deve essere aggiunto al payload di streaming in Adobe Experience Platform. Questa limitazione non si applica agli eventi basati su regole.
* Gli eventi di business non possono essere utilizzati in combinazione con eventi unitari o attività di qualificazione del pubblico.
* I percorsi unitari (a partire da un evento o da una qualificazione del pubblico) includono un guardrail che impedisce ai percorsi di essere attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il reingresso del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.
* Journey Optimizer richiede che gli eventi vengano inviati in streaming al servizio core di raccolta dati (DCCS) per poter attivare un percorso. Eventi acquisiti in batch o eventi da set di dati interni di Journey Optimizer (feedback messaggi, tracciamento e-mail, ecc.) non possono essere utilizzati per attivare un percorso. Per i casi d’uso in cui non è possibile ricevere eventi in streaming, devi creare un pubblico basato su tali eventi e utilizzare l’attività **Leggi pubblico**. Tecnicamente, è possibile usare la qualificazione del pubblico, ma non è consigliato, perché potrebbe causare problemi a valle in base alle azioni utilizzate.

### Origini dati {#data-sources-g}

Alle [origini dati](../datasource/about-data-sources.md) nei tuoi percorsi vengono applicati i seguenti guardrail:

* Le origini dati esterne possono essere sfruttate all’interno di un percorso del cliente per ricercare dati esterni in tempo reale. Queste origini devono essere utilizzabili tramite API REST, supportare JSON ed essere in grado di gestire il volume delle richieste.
* Non sono consentiti indirizzi di Adobe interni (`.adobe.*`) negli URL e nelle API.

>[!NOTE]
>
>Poiché le risposte sono ora supportate, per i casi d’uso relativi a origini dati esterne devi utilizzare azioni personalizzate anziché origini dati.

### Creazione di percorsi e profili {#journeys-limitation-profile-creation}

In Adobe Experience Platform si verifica un ritardo associato alla creazione/aggiornamento dei profili basati su API. Il target livello di servizio (Service Level Target, SLT) in termini di latenza è &lt; di 1 minuto dall’acquisizione al profilo unificato per il 95° percentile delle richieste, con un volume di 20.000 richieste al secondo (RPS).

Se un percorso viene attivato simultaneamente per la creazione di un profilo e immediatamente controlla/recupera le informazioni dal Servizio profili, potrebbe non funzionare correttamente.

Puoi scegliere una delle due soluzioni seguenti:

* Aggiungi un’attività di attesa dopo il primo evento, per dare ad Adobe Experience Platform il tempo necessario per eseguire l’acquisizione nel servizio profilo.

* Impostare un percorso che non sfrutta immediatamente il profilo. Ad esempio, se il percorso è progettato per confermare la creazione di un account, l’evento esperienza potrebbe contenere le informazioni necessarie per inviare il primo messaggio di conferma (nome, cognome, indirizzo e-mail, ecc.).

### Aggiorna il profilo {#update-profile-g}

All’attività **[!UICONTROL Aggiorna profilo]** vengono applicati guardrail specifici. Sono elencati in [questa pagina](../building-journeys/update-profiles.md).

### Leggi pubblico {#read-segment-g}

All’attività del percorso [Leggi pubblico](../building-journeys/read-audience.md), vengono applicati i seguenti guardrail:

* I tipi di pubblico in streaming sono sempre aggiornati, ma i tipi di pubblico in batch non verranno calcolati al momento del recupero. Vengono valutati ogni giorno solo al momento della valutazione giornaliera del batch.
* Per i percorsi che utilizzano un’attività **Leggi pubblico** esiste un numero massimo di percorsi che è possibile avviare contemporaneamente. I tentativi verranno eseguiti dal sistema, ma evita di disporre di più di cinque percorsi (con **Leggi pubblico**, programmato o che inizia “non appena possibile”) che si avviano nello stesso momento distribuendoli nel tempo, ad esempio a 5-10 minuti di distanza.
* L’attività **Leggi pubblico** non può essere utilizzata con le attività di Adobe Campaign.
* L’attività **Leggi pubblico** può essere utilizzata solo come prima attività in un percorso o dopo un’attività evento di business.
* Un percorso può disporre di una sola attività **Leggi pubblico**.
* Consulta anche i consigli su come utilizzare l’attività **Leggi pubblico** in [questa pagina](../building-journeys/read-audience.md).
* I nuovi tentativi vengono ora applicati per impostazione predefinita ai percorsi attivati dal pubblico (a partire da **Leggi pubblico** o **Evento di business**) durante il recupero del processo di esportazione. Se si verifica un errore durante la creazione del processo di esportazione, verranno eseguiti nuovi tentativi ogni 10 minuti, per un massimo di 1 ora. Dopo i tentativi, verrà considerato come un errore. Questi tipi di percorsi possono quindi essere eseguiti fino a 1 ora dopo l’orario pianificato.

### Qualificazione del pubblico {#audience-qualif-g}

All’attività del percorso [qualificazione del pubblico](../building-journeys/audience-qualification-events.md) viene applicato il seguente guardrail:

* L’attività Qualificazione del pubblico non può essere utilizzata con le attività di Adobe Campaign.

### Editor espressioni {#expression-editor}

All’[editor di espressioni del percorso](../building-journeys/expression/expressionadvanced.md) si applicano i seguenti guardrail:

* I gruppi di campo di evento esperienza non possono più essere utilizzati nei percorsi che iniziano con un’attività Leggi pubblico, Qualificazione del pubblico o Evento di business. È necessario creare un nuovo pubblico e utilizzare una condizione `inaudience` nel percorso.
* Non è possibile utilizzare gli attributi `timeSeriesEvents` nell’editor di espressioni. Per accedere agli eventi di esperienza a livello di profilo, crea un nuovo gruppo di campi basato su uno schema `XDM ExperienceEvent`.


### Attività in-app {#in-app-activity-limitations}

All’azione **[!UICONTROL messaggio in-app]**, vengono applicati i seguenti guardrail: Ulteriori informazioni sui messaggi in-app sono disponibili in [questa pagina](../in-app/create-in-app.md).

* Questa funzione non è attualmente disponibile per la clientela del settore dell’assistenza sanitaria.

* La personalizzazione può contenere solo attributi di profilo.

* L’attività in-app non può essere utilizzata con le attività di Adobe Campaign.

* La visualizzazione in-app è legata alla durata del percorso, il che significa che quando il percorso termina per un profilo, tutti i messaggi in-app all’interno di quel percorso cesseranno di essere visualizzati per quel profilo.  Di conseguenza, non è possibile interrompere un messaggio in-app direttamente da un’attività del percorso. Al contrario, per impedire la visualizzazione dei messaggi in-app nel profilo, devi terminare l’intero percorso.

* In modalità di test, la visualizzazione in-app dipende dalla durata del percorso. Per evitare che il percorso termini anticipatamente durante il test, regola il valore **[!UICONTROL Tempo di attesa]** per le attività di **[!UICONTROL Attesa]**.

* Le attività di **[!UICONTROL Reazione]** non possono essere utilizzate per reagire a un’apertura in-app o a un clic.

* È possibile che si verifichi un ritardo di attivazione tra il momento in cui un profilo utente raggiunge un’attività in-app nell’area di lavoro e il momento in cui inizia a visualizzare tale messaggio in-app.

* La dimensione del contenuto del messaggio in-app è limitata a 2 MB. L’inclusione di immagini di grandi dimensioni può ostacolare il processo di pubblicazione.

### Attività Salta {#jump-g}

All’attività **[!UICONTROL Salta]** si applicano guardrail specifici. Sono elencati in [questa pagina](../building-journeys/jump.md#jump-limitations).

### Attività di Campaign {#ac-g}

I seguenti guardrail si applicano alle attività di **[!UICONTROL Campaign v7/v8]** e di **[!UICONTROL Campaign Standard]**:

* Le attività di Adobe Campaign non possono essere utilizzate con un’attività Leggi pubblico o Qualificazione del pubblico.
* Le attività di Campaign non possono essere utilizzate con le attività degli altri canali: schede, esperienze basate su codice, e-mail, push, SMS, messaggi in-app, web.
