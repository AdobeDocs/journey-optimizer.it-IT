---
solution: Journey Optimizer
product: journey optimizer
title: Guardrail e limitazioni di Journey Optimizer
description: Ulteriori informazioni sui guardrail di Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: b8af73485227dc102b5b190b58a5d4341ffb2708
workflow-type: tm+mt
source-wordcount: '3530'
ht-degree: 83%

---

# Guardrail e limitazioni {#limitations}

Di seguito troverai ulteriori guardrail e limitazioni durante l’utilizzo di [!DNL Adobe Journey Optimizer].

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

<!--The following guardrails apply to the [email channel](../../rp_landing_pages/email-landing-page.md):-->

Al [canale e-mail](../email/get-started-email.md) vengono applicati i seguenti guardrail:

* Non è possibile utilizzare lo stesso dominio di invio per inviare messaggi e-mail da [!DNL Adobe Journey Optimizer] e da un altro prodotto, come [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage] ad esempio.

Durante la progettazione dei messaggi e-mail, il sistema verifica le impostazioni chiave e mostra avvisi relativi ad avvertenze (consigli e best practice) ed errori (problemi critici che impediscono il test o l’attivazione). Scopri di più sugli avvisi e-mail e sui requisiti di convalida in [questa sezione](../email/create-email.md#check-email-alerts).

#### Dimensione del contenuto dei messaggi per la pubblicazione del percorso {#message-content-size}

Quando si pubblicano percorsi che contengono messaggi e-mail, la dimensione totale del contenuto del messaggio non deve superare **2 MB** dopo l&#39;elaborazione back-end. Durante la pubblicazione, il sistema elabora in automatico il contenuto dei messaggi applicando patch a collegamenti e immagini e utilizzando trasformazioni; queste operazioni aumentano la dimensione del payload oltre quella del contenuto creato.

>[!CAUTION]
>
>Se il contenuto finale del messaggio elaborato supera i 2 MB, la pubblicazione del percorso non riuscirà. Per evitare errori di pubblicazione, mantieni il contenuto del messaggio creato ben al di sotto di 2 MB, idealmente al di sotto di **1 MB**, per consentire un buffer di 300-400 KB per il sovraccarico di elaborazione del back-end.

**Best practice per evitare errori di pubblicazione:**

* Mantienere i contenuti e-mail creati al di sotto di 1 MB
* Ridurre al minimo il numero di varianti di contenuto
* Ottimizzare e comprimere le immagini prima di aggiungerle ai messaggi
* Rimuovere le risorse inutilizzate e gli elementi HTML non necessari
* Verificare la dimensione del messaggio prima di pubblicare i percorsi in produzione

Se la pubblicazione del percorso non riesce a causa della dimensione del contenuto, riduci il contenuto del messaggio e ripubblica il percorso.

### Guardrail per SMS {#sms-guardrails}

Al [canale SMS](../sms/get-started-sms.md) vengono applicati i seguenti guardrail:

* I file multimediali per MMS possono essere inclusi tramite un URL supportato. Assicurati che il file multimediale sia caricato separatamente.
* La sincronizzazione del feedback sui messaggi non è attualmente disponibile per gli MMS.
* La gestione del consenso funziona a livello del canale SMS per MMS.

### Guardrail per canali in entrata {#inbound-guardrails}

* Per utilizzare le azioni di [esperienza basate su codice](../code-based/get-started-code-based.md) in [!DNL Journey Optimizer] e distribuire il payload del contenuto del codice utilizzabile dalle applicazioni, segui i prerequisiti descritti in [questa pagina](../code-based/code-based-prerequisites.md).

* Per poter accedere e creare [pagine Web](../web/get-started-web.md) nell&#39;interfaccia utente [!DNL Journey Optimizer], seguire i prerequisiti elencati in [questa pagina](../web/web-prerequisites.md).

* Per inviare messaggi in-app nei tuoi percorsi e campagne con [!DNL Journey Optimizer], segui i prerequisiti di consegna elencati in [questa pagina](../in-app/inapp-configuration.md).

* Affinché Adobe Journey Optimizer visualizzi correttamente le schede di contenuto, devi configurare le impostazioni di Adobe Experience Platform elencate in [questa pagina](../content-card/content-card-configuration-prereq.md).

* Journey Optimizer supporta un volume massimo di 5.000 richieste in entrata al secondo. Questo guardrail si applica a tutte le richieste in entrata che possono provenire da qualsiasi canale in entrata supportato da Journey Optimizer ([web](../web/get-started-web.md), [in-app](../in-app/get-started-in-app.md), [esperienze basate su codice](../code-based/get-started-code-based.md), [schede di contenuto](../../rp_landing_pages/content-card-landing-page.md)).

* Journey Optimizer supporta un massimo di 500 azioni attive in entrata in qualsiasi momento. Queste azioni in entrata vengono conteggiate se fanno parte di una campagna live o se sono un nodo utilizzato in un percorso live. Una volta raggiunto questo numero, è necessario disattivare le campagne o i percorsi precedenti che utilizzano azioni in entrata prima di poterne avviare di nuovi.

#### Gestione dei profili con canali in entrata {#profile-management-inbound}

[!DNL Journey Optimizer] canali in entrata possono eseguire il targeting di profili pseudonimi, ovvero profili non autenticati o non ancora noti perché non sono stati precedentemente coinvolti su altri canali. Questo è il caso, ad esempio, quando si esegue il targeting di tutti i visitatori o tipi di pubblico in base a ID temporanei come ECID.

Questo aumenta il numero totale di profili coinvolgibili, il che può avere implicazioni di costo se viene superato il numero contrattuale di profili coinvolgibili acquistati. Le metriche di licenza per ciascun pacchetto sono elencate nella pagina [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Puoi controllare il numero di profili coinvolgibili nel [dashboard di utilizzo delle licenze](../audience/license-usage.md).

Per mantenere i profili coinvolgibili entro limiti ragionevoli, Adobe consiglia di impostare un valore TTL (Time-To-Live) per eliminare automaticamente i profili pseudonimi dal profilo cliente in tempo reale se non sono stati visualizzati o coinvolti in un intervallo di tempo specifico.

>[!NOTE]
>
>Scopri come configurare la scadenza dei dati per i profili pseudonimi nella [documentazione di Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

Adobe consiglia di impostare il valore TTL su 14 giorni, in modo che corrisponda al valore TTL del profilo Edge corrente.

### Guardrail di un messaggio transazionale {#transactional-message-guardrails}

Journey Optimizer supporta un volume massimo di 500 messaggi transazionali al secondo nelle campagne.

## Guardrail delle pagine di destinazione {#lp-guardrails}

Alle [pagine di destinazione](../landing-pages/get-started-lp.md) vengono applicati i seguenti guardrail:

* Solo un componente **Modulo** può essere utilizzato in una singola pagina principale.
* Il componente **Modulo** non può essere utilizzato nelle pagine secondarie.
* Non puoi aggiungere una preintestazioni  a una pagina di destinazione.
* Non è possibile selezionare l’opzione **Crea il codice** durante la progettazione di una pagina di destinazione principale.

## Guardrail per i sottodomini {#subdomain-guardrails}

I guardrail e le limitazioni applicabili alla delega di un sottodominio in Journey Optimizer sono descritti in dettaglio in [questa pagina](../configuration/delegate-subdomain.md#guardrails).

## Guardrail per i frammenti {#fragments-guardrails}

Ai [frammenti](../content-management/fragments.md) vengono applicati i seguenti guardrail:

* Per creare, modificare, archiviare e pubblicare frammenti sono necessarie le autorizzazioni **[!DNL Manage library items]** e **[Pubblica frammento]** incluse nel profilo del prodotto **[!DNL Content Library Manager]**. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)
* I frammenti visivi sono disponibili solo per il canale e-mail.
* I frammenti di espressione non sono disponibili per il canale in-app.
* I frammenti visivi non possono superare i 100 KB. I frammenti di espressioni non possono superare i 200 KB.
* Per utilizzare un frammento in un percorso o in una campagna, ora è necessario che sia in stato **Live**.
* Gli [attributi contestuali](../personalization/personalization-build-expressions.md) non sono supportati nei frammenti.
* I frammenti visivi non sono compatibili tra le modalità Utilizza temi e Stile manuale. Per poter utilizzare un frammento in un contenuto in cui si desidera applicare un tema, è necessario creare il frammento in modalità Utilizza temi. [Ulteriori informazioni sui temi](../email/apply-email-themes.md)
* Quando il tracciamento è abilitato in un percorso o in una campagna, se aggiungi collegamenti a un frammento e quest’ultimo viene utilizzato in un messaggio, tali collegamenti vengono tracciati come tutti gli altri collegamenti inclusi nel messaggio. [Ulteriori informazioni su collegamenti e tracciamento](../email/message-tracking.md)

## Guardrail del profilo e del pubblico {#audience}

* Puoi pubblicare fino a 10 composizioni di pubblico in una determinata sandbox. Se hai raggiunto questa soglia, elimina una composizione per liberare spazio e pubblicarne una nuova.

  Per ulteriori informazioni sulle composizioni del pubblico, consulta [questa pagina](../audience/get-started-audience-orchestration.md).

* Durante l’acquisizione dei dati, negli indirizzi e-mail viene fatta distinzione tra maiuscole e minuscole. Ciò significa che è possibile creare profili duplicati (ad esempio, un profilo per John.Greene@luma.com e un altro profilo per john.greene@luma.com) e utilizzarli quando si esegue il targeting del destinatario corrispondente nei percorsi e nelle campagne [!DNL Journey Optimizer].

* Quando esegui il targeting di profili pseudonimi (visitatori non autenticati) con canali in entrata, puoi impostare un valore TTL (Time-To-Live) per l’eliminazione automatica del profilo, in modo da gestire il conteggio dei profili coinvolgibili e i costi associati. [Ulteriori informazioni](#profile-management-inbound)

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

### Seleziona le limitazioni del pacchetto per i percorsi unitari {#select-package-limitations}

>[!NOTE]
>
>Queste limitazioni non si applicano ai percorsi Read Audience o Business Event con il pacchetto **Select**. Se hai bisogno di una logica di percorso più complessa con più azioni, condizioni o attività di attesa, valuta l’aggiornamento del pacchetto di licenze o l’utilizzo di percorsi Read Audience, se applicabile.

Per i clienti che utilizzano il pacchetto di licenza **Select**, le seguenti limitazioni aggiuntive si applicano in modo specifico ai percorsi unitari, ai percorsi che iniziano con un evento o a una qualifica di pubblico:

* **Pacchetto SELECT: nel percorso unitario è consentita una sola azione (ERR_PKG_SELECT_8)**: i percorsi unitari possono contenere una sola attività di azione. Non puoi aggiungere più attività e-mail, push, SMS o altre attività all’interno dello stesso percorso.

* **Pacchetto SELECT: nessuna condizione consentita nel percorso unitario (ERR_PKG_SELECT_7)**: le attività condizione non possono essere utilizzate nei percorsi unitari. Il percorso deve seguire un unico percorso lineare senza logica di diramazione.

* **Pacchetto SELECT: nessuna attesa consentita nel percorso unitario (ERR_PKG_SELECT_6)**: impossibile aggiungere attività di attesa ai percorsi unitari. Le azioni devono essere eseguite immediatamente senza ritardi.

* **Pacchetto SELECT: la transizione timeout/errore dal nodo deve puntare solo al nodo finale (ERR_PKG_SELECT_2)**: se configuri le transizioni timeout o errore per un&#39;azione, ad esempio un&#39;azione e-mail, questi percorsi devono puntare direttamente a un nodo finale. Non possono connettersi ad altre attività o azioni nel percorso.


### Azioni generali {#general-actions-g}

Alle [azioni](../building-journeys/about-journey-activities.md) nei tuoi percorsi, vengono applicati i seguenti guardrail:

* In caso di errore vengono eseguiti sistematicamente tre tentativi. Non è possibile regolare il numero di tentativi in base al messaggio di errore ricevuto. Vengono eseguiti nuovi tentativi per tutti gli errori HTTP eccetto HTTP 401, 403 e 404.
* L’evento **Reazione** incorporato consente di reagire alle azioni predefinite. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/reaction-events.md). Se desideri reagire a un messaggio inviato tramite un’azione personalizzata, devi configurare un evento dedicato.
* Non è possibile inserire due azioni in parallelo, è necessario aggiungerle una dopo l’altra.
* Un profilo non può essere presente più volte nello stesso percorso contemporaneamente per tutte le [versioni attive del percorso](../building-journeys/publish-journey.md#journey-create-new-version). Se è stato abilitato il reingresso, un profilo può entrare nuovamente in un percorso, ma solo dopo essere uscito completamente dalla precedente istanza del percorso. [Ulteriori informazioni](../building-journeys/end-journey.md)

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

* Per tutte le azioni personalizzate, viene definito un limite massimo di 300.000 chiamate in un minuto per host e per sandbox. Il limite &quot;per host&quot; si applica a livello di dominio (ad esempio, example.com). Questo limite viene applicato come finestra scorrevole per sandbox e per endpoint per gli endpoint con tempi di risposta inferiori a 0,75 secondi. Per gli endpoint con tempi di risposta superiori a 0,75 secondi, si applica un limite separato di 150.000 chiamate per 30 secondi (anche una finestra scorrevole). Consulta [questa pagina](../action/about-custom-action-configuration.md). Questo limite è stato impostato in base all’utilizzo da parte della clientela, per proteggere gli endpoint esterni interessati dalle azioni personalizzate. Se necessario, puoi ignorare questa impostazione definendo un limite di limitazione di utilizzo o di limitazione maggiore tramite le rispettive API. Consulta [questa pagina](../configuration/external-systems.md).
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

* Journey Optimizer supporta un volume massimo di 5.000 eventi di percorso in entrata al secondo, su tutte le sandbox. Ulteriori informazioni su questa limitazione [in questa pagina](../event/about-events.md#event-thoughput).
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


### Identificatori supplementari {#supplemental}

Guardrail specifici si applicano all’utilizzo di identificatori supplementari nei percorsi. Sono elencati in [questa pagina](../building-journeys/supplemental-identifier.md#guardrails).

### Editor di espressioni {#expression-editor}

All’[editor di espressioni del percorso](../building-journeys/expression/expressionadvanced.md) si applicano i seguenti guardrail:

* I gruppi di campo di evento esperienza non possono più essere utilizzati nei percorsi che iniziano con un’attività Leggi pubblico, Qualificazione del pubblico o Evento di business. È necessario creare un nuovo pubblico e utilizzare una condizione `inaudience` nel percorso.
* Non è possibile utilizzare gli attributi `timeSeriesEvents` nell’editor di espressioni. Per accedere agli eventi di esperienza a livello di profilo, crea un nuovo gruppo di campi basato su uno schema `XDM ExperienceEvent`.

### Attività del percorso {#activities}

#### Attività Qualificazione del pubblico {#audience-qualif-g}

All’attività del percorso [qualificazione del pubblico](../building-journeys/audience-qualification-events.md) viene applicato il seguente guardrail:

* L’attività Qualificazione del pubblico non può essere utilizzata con le attività di Adobe Campaign.
* Gli identificatori supplementari non sono supportati per i percorsi di qualificazione del pubblico.

Scopri di più sui tassi di elaborazione dei percorsi e sui limiti della velocità effettiva in [questa sezione](../building-journeys/entry-management.md#journey-processing-rate).

#### Attività di Campaign {#ac-g}

I seguenti guardrail si applicano alle attività di **[!UICONTROL Campaign v7/v8]** e di **[!UICONTROL Campaign Standard]**:

* Le attività di Adobe Campaign non possono essere utilizzate con un’attività Leggi pubblico o Qualificazione del pubblico.
* Le attività di Campaign non possono essere utilizzate con le attività degli altri canali: schede, esperienze basate su codice, e-mail, push, SMS, messaggi in-app, web.

#### Attività in-app {#in-app-activity-limitations}

All’azione **[!UICONTROL messaggio in-app]**, vengono applicati i seguenti guardrail: Ulteriori informazioni sui messaggi in-app sono disponibili in [questa pagina](../in-app/create-in-app.md).

* Questa funzione non è attualmente disponibile per la clientela del settore dell’assistenza sanitaria.

* La personalizzazione può contenere solo attributi di profilo.

* L’attività in-app non può essere utilizzata con le attività di Adobe Campaign.

* La visualizzazione in-app è legata alla durata del percorso, il che significa che quando il percorso termina per un profilo, tutti i messaggi in-app all’interno di quel percorso cesseranno di essere visualizzati per quel profilo.  Di conseguenza, non è possibile interrompere un messaggio in-app direttamente da un’attività del percorso. Al contrario, per impedire la visualizzazione dei messaggi in-app nel profilo, devi terminare l’intero percorso.

* In modalità di test, la visualizzazione in-app dipende dalla durata del percorso. Per evitare che il percorso termini anticipatamente durante il test, regola il valore **[!UICONTROL Tempo di attesa]** per le attività di **[!UICONTROL Attesa]**.

* Le attività di **[!UICONTROL Reazione]** non possono essere utilizzate per reagire a un’apertura in-app o a un clic.

* È possibile che si verifichi un ritardo di attivazione tra il momento in cui un profilo utente raggiunge un’attività in-app nell’area di lavoro e il momento in cui inizia a visualizzare tale messaggio in-app.

* La dimensione del contenuto del messaggio in-app è limitata a 2 MB. L’inclusione di immagini di grandi dimensioni può ostacolare il processo di pubblicazione.

#### Attività Salta {#jump-g}

All’attività **[!UICONTROL Salta]** si applicano guardrail specifici. Sono elencati in [questa pagina](../building-journeys/jump.md#jump-limitations).

#### Attività Leggi pubblico {#read-segment-g}

All’attività del percorso [Leggi pubblico](../building-journeys/read-audience.md), vengono applicati i seguenti guardrail:

* I tipi di pubblico in streaming sono sempre aggiornati, ma i tipi di pubblico in batch non verranno calcolati al momento del recupero. Vengono valutati ogni giorno solo al momento della valutazione giornaliera del batch.
* Per i percorsi che utilizzano un’attività **Leggi pubblico** esiste un numero massimo di percorsi che è possibile avviare contemporaneamente. I nuovi tentativi verranno eseguiti dal sistema, ma evita di creare più di cinque percorsi (con l’attività **Leggi pubblico**, programmata o che inizia “non appena possibile”) che si avviano nello stesso momento distribuendoli nel tempo, ad esempio a 5-10 minuti di distanza. Scopri di più sui tassi di elaborazione dei percorsi in [questa sezione](../building-journeys/entry-management.md#journey-processing-rate).
* L’attività **Leggi pubblico** non può essere utilizzata con le attività di Adobe Campaign.
* L’attività **Leggi pubblico** può essere utilizzata solo come prima attività in un percorso o dopo un’attività evento di business.
* Un percorso può disporre di una sola attività **Leggi pubblico**.
* Consulta anche i consigli su come utilizzare l’attività **Leggi pubblico** in [questa pagina](../building-journeys/read-audience.md).
* I nuovi tentativi vengono ora applicati per impostazione predefinita ai percorsi attivati dal pubblico (a partire da **Leggi pubblico** o **Evento di business**) durante il recupero del processo di esportazione. Se si verifica un errore durante la creazione del processo di esportazione, verranno eseguiti nuovi tentativi ogni 10 minuti, per un massimo di 1 ora. Dopo i tentativi, verrà considerato come un errore. Questi tipi di percorsi possono quindi essere eseguiti fino a 1 ora dopo l’orario pianificato.
* Per i percorsi che utilizzano ID supplementari, il tasso di lettura dell’attività Leggi pubblico per ogni istanza del percorso è limitata a un massimo di 500 profili al secondo.

Consulta anche [questa pagina](../building-journeys/read-audience.md#must-read).

#### Attività Aggiorna profilo {#update-profile-g}

All’attività **[!UICONTROL Aggiorna profilo]** vengono applicati guardrail specifici. Sono elencati in [questa pagina](../building-journeys/update-profiles.md).

## Guardrail per l’orchestrazione delle campagne {#orchestration-guardrails}

I guardrail e le limitazioni da tenere presenti quando utilizzi l’orchestrazione di una campagna sono descritti in questa sezione: [Guardrail e limitazioni](../orchestrated/guardrails.md).
