---
solution: Journey Optimizer
product: journey optimizer
title: Guardrail e limitazioni di Journey Optimizer
description: Ulteriori informazioni sui guardrail di Journey Optimizer
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 2
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2:
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 26e1073e2fef79ecdfd72ff1c2e5247ec2d62f8a
workflow-type: tm+mt
source-wordcount: 4622
ht-degree: 64%

---


# Guardrail e limitazioni {#limitations}

Di seguito troverai ulteriori guardrail e limitazioni durante l’utilizzo di [!DNL Adobe Journey Optimizer].

I diritti, le limitazioni del prodotto e i guardrail relativi alle prestazioni sono elencati nella [pagina di descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

>[!CAUTION]
>
>* [I guardrail per i dati e la segmentazione del profilo cliente in tempo reale](https://experienceleague.adobe.com/it/docs/experience-platform/profile/guardrails){target="_blank"} vengono applicati anche a Adobe Journey Optimizer.
>
>* Consulta anche [Guardrail per l’acquisizione di dati nel Profilo cliente in tempo reale](https://experienceleague.adobe.com/it/docs/experience-platform/ingestion/guardrails){target="_blank"}

## Panoramica dei limiti chiave {#quick-reference}

Utilizzare questa tabella per cercare i limiti numerici più critici prima di generare o pubblicare. Per informazioni complete e contesto, consulta le sezioni seguenti.

| Area | Limite | Elemento “value” |
|---|---|---|
| **Percorsi** | [Attività massime al percorso](#journeys-guardrails-journeys) | **50** |
| **Percorsi** | [Numero massimo di percorsi attivi / in pausa / in prova](#journeys-guardrails-journeys) | **100** |
| **Percorsi** | [Dimensione Percorso istanza](#journeys-guardrails-journeys) | **1 MB** |
| **Percorsi** | [Dimensione Percorso payload (pubblicazione)](#journey-payload-size) | **2 MB** (avvertenza al 90%) |
| **Percorsi** | [Timeout percorso globale](#journeys-guardrails-journeys) | **91 giorni** |
| **Percorsi** | [Coda eventi in sospeso per profilo](#journeys-guardrails-journeys) | **10 eventi** |
| **Percorsi** | [Istanze del pubblico di lettura simultanee](#read-segment-g) | **5** in tutte le sandbox |
| **Percorsi** | [Velocità effettiva di lettura sandbox pubblico](#read-segment-g) | **20.000 profili/sec** (condivisi) |
| **Percorsi** | [Timeout processo di lettura pubblico](#read-segment-g) | **12 ore** |
| **Canali** | [Richieste in entrata al secondo](#inbound-guardrails) | **5.000 RPS** |
| **Canali** | [Numero massimo azioni in entrata attive](#inbound-guardrails) | **500** |
| **Canali** | [Messaggi transazionali/sec (campagne)](#transactional-message-guardrails) | **500** |
| **Canali** | [Eventi di percorso in entrata al secondo](#events-g) | **5,000** |
| **Azioni personalizzate** | [Chiamate al minuto (risposta &lt; 0,75 s)](#custom-actions-g) | **300.000 / min** per host/sandbox |
| **Azioni personalizzate** | [Chiamate ogni 30 secondi (risposta > 0,75 secondi)](#custom-actions-g) | **150.000 / 30 s** per host/sandbox |
| **Contenuto** | [Contenuto del messaggio di posta elettronica alla pubblicazione](#message-content-size) | **2 MB** (autore inferiore a 1 MB) |
| **Contenuto** | [Contenuto messaggio in-app](#in-app-activity-limitations) | **2 MB** |
| **Contenuto** | [Dimensione frammento visivo](#fragments-guardrails) | **100 KB** |
| **Contenuto** | [Dimensione frammento di espressione](#fragments-guardrails) | **200 KB** |
| **Contenuto** | [nodi frammento di Percorso](#fragments-journey-g) | **20 nodi/frammento**, 200 attivo/sandbox |
| **Tipi di pubblico** | [Composizioni pubblico per sandbox](#audience) | **10** |
| **Set di dati** | [TTL archivio profili (nuove organizzazioni/sandbox)](#datasets-guardrails) | **90 giorni** |
| **Set di dati** | [TTL del data lake (nuove organizzazioni/sandbox)](#datasets-guardrails) | **13 mesi** |


## Sistema e piattaforma {#system-platform}

### Browser supportati {#browsers}

L’interfaccia di Adobe [!DNL Journey Optimizer] è progettata per funzionare in modo ottimale nell’ultima versione di Google Chrome. L’utilizzo di versioni precedenti o di altri browser potrebbe comportare problemi durante l’utilizzo di alcune funzioni.

### Guardrail per set di dati {#datasets-guardrails}

A febbraio 2025 è stato introdotto un guardrail time-to-live (TTL) nei set di dati di Journey Optimizer generati dal sistema in **nuove sandbox e nuove organizzazioni** come segue:

* **90 giorni** per i dati nell&#39;archivio profili
* **13 mesi** per i dati nel data lake

Questa modifica verrà implementata nelle **sandbox della clientela esistente** in una fase successiva. [Ulteriori informazioni sui guardrail Time-To-Live (TTL) dei set di dati](../data/datasets-ttl.md)

## Messaggistica e canali {#channel-guardrails}

Questa sezione illustra i guardrail per tutti i canali di comunicazione, inclusi e-mail, SMS, canali in entrata (web, in-app, basati su codice, schede di contenuto) e messaggi transazionali.

>[!NOTE]
>
>In rare circostanze, interruzioni temporanee in una area geografica specifica possono comportare l’esclusione dai percorsi di profili validi oppure e-mail erroneamente contrassegnate come mancati recapiti. Una volta ripristinati i servizi, ricontrolla i registri del percorso, verifica i campi del profilo di consenso e, se necessario, ripubblica il percorso. In caso di interruzione di un ISP, scopri come rimuovere i profili dall’elenco di soppressione in [questa sezione](../configuration/manage-suppression-list.md#remove-from-suppression-list).

### Guardrail per e-mail {#message-guardrails}

Al [canale e-mail](../email/get-started-email.md) vengono applicati i seguenti guardrail:

* Non è possibile utilizzare lo stesso dominio di invio per inviare messaggi e-mail da [!DNL Adobe Journey Optimizer] e da un altro prodotto, come [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage] ad esempio.

Durante la progettazione dei messaggi e-mail, il sistema verifica le impostazioni chiave e mostra avvisi relativi ad avvertenze (consigli e best practice) ed errori (problemi critici che impediscono il test o l’attivazione). Scopri di più sugli avvisi e-mail e sui requisiti di convalida in [questa sezione](../email/create-email.md#check-email-alerts).

#### Dimensione del contenuto dei messaggi per la pubblicazione del percorso {#message-content-size}

Quando si pubblicano percorsi che contengono messaggi e-mail, la dimensione totale del contenuto del messaggio non deve superare **2 MB** dopo l&#39;elaborazione back-end. Durante la pubblicazione, il sistema elabora in automatico il contenuto dei messaggi applicando patch a collegamenti e immagini e utilizzando trasformazioni; queste operazioni aumentano la dimensione del payload oltre quella del contenuti creati.

>[!CAUTION]
>
>Se il contenuto finale del messaggio elaborato supera i **2 MB**, la pubblicazione del percorso avrà esito negativo. Mantieni il contenuto dei messaggi creati ben al di sotto di 2 MB, idealmente al di sotto di **1 MB**, per consentire un buffer di 300-400 KB per il sovraccarico di elaborazione del back-end.

**Best practice per evitare errori di pubblicazione:**

* Mantieni contenuto e-mail creato in **1 MB**
* Ridurre al minimo il numero di varianti di contenuto
* Ottimizzare e comprimere le immagini prima di aggiungerle ai messaggi
* Rimuovere le risorse inutilizzate e gli elementi HTML non necessari
* Verificare le dimensioni del messaggio prima di pubblicare i percorsi in produzione

Se la pubblicazione del percorso non riesce a causa delle dimensioni del contenuto, riduci il contenuto del messaggio e pubblica nuovamente il percorso.

### Guardrail per SMS {#sms-guardrails}

Al [canale SMS](../mobile/get-started-mobile.md) vengono applicati i seguenti guardrail:

* I file multimediali per MMS possono essere inclusi tramite un URL supportato. Assicurati che il file multimediale sia caricato separatamente.
* La sincronizzazione del feedback sui messaggi non è attualmente disponibile per gli MMS.
* La gestione del consenso funziona a livello del canale SMS per MMS.

### Guardrail per canali in entrata {#inbound-guardrails}

* Per utilizzare le azioni di [esperienza basate su codice](../code-based/get-started-code-based.md) in [!DNL Journey Optimizer] e distribuire il payload del contenuto del codice utilizzabile dalle applicazioni, segui i prerequisiti descritti in [questa pagina](../code-based/code-based-prerequisites.md).

* Per poter accedere e creare [pagine web](../web/get-started-web.md) nell’interfaccia utente di [!DNL Journey Optimizer], segui i prerequisiti elencati in [questa pagina](../web/web-prerequisites.md).

* Per inviare messaggi in-app nei tuoi percorsi e campagne con [!DNL Journey Optimizer], segui i prerequisiti di consegna elencati in [questa pagina](../in-app/inapp-configuration.md).

* Affinché Adobe Journey Optimizer mostri correttamente le schede contenuto, devi configurare le impostazioni di Adobe Experience Platform elencate in [questa pagina](../content-card/content-card-configuration-prereq.md).

* Journey Optimizer supporta un volume massimo di **5.000 richieste in entrata al secondo**. Questo guardrail si applica a tutte le richieste in entrata che possono provenire da qualsiasi canale in entrata supportato da Journey Optimizer ([web](../web/get-started-web.md), [in-app](../in-app/get-started-in-app.md), [esperienze basate su codice](../code-based/get-started-code-based.md), [schede di contenuto](../../rp_landing_pages/content-card-landing-page.md)).

* Journey Optimizer supporta un massimo di **500 azioni in entrata attive** in qualsiasi momento. Queste azioni in entrata vengono conteggiate se fanno parte di una campagna live o se sono un nodo utilizzato in un percorso live. Una volta raggiunto questo numero, è necessario disattivare le campagne o i percorsi precedenti che utilizzano azioni in entrata prima di poterne avviare di nuovi.

#### Gestione profilo con canali in entrata {#profile-management-inbound}

[!DNL Journey Optimizer] canali in entrata possono eseguire il targeting di profili identificati da pseudonimi, ovvero profili non autenticati o non ancora noti perché non sono stati precedentemente coinvolti su altri canali. È il caso, ad esempio, quando si esegue il targeting di tutti i visitatori o tipi di pubblico in base a ID temporanei come ECID.

In questo modo aumenta il conteggio totale dei profili coinvolti, il che potrebbe avere implicazioni sui costi se viene superato il numero contrattuale di profili coinvolti acquistati. Le metriche di licenza per ciascun pacchetto sono elencate nella pagina [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Puoi controllare il numero di profili coinvolti nella [dashboard di utilizzo delle licenze](../audience/license-usage.md).

Per mantenere i profili coinvoltii entro limiti ragionevoli, Adobe consiglia di impostare un valore TTL (Time-to-live) per eliminare automaticamente i profili identificati da pseudonimi dal Profilo cliente in tempo reale se non sono stati visualizzati o coinvolti in un intervallo di tempo specifico. Adobe consiglia di impostare il valore TTL su **14 giorni** per corrispondere al TTL del profilo Edge corrente.

>[!NOTE]
>
>Scopri come configurare la scadenza dei dati per i profili identificati da pseudonimi nella [documentazione di Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

### Guardrail di un messaggio transazionale {#transactional-message-guardrails}

Journey Optimizer supporta un volume massimo di **500 messaggi transazionali al secondo** nelle campagne.

## Contenuti e risorse {#content-assets}

Questa sezione illustra i guardrail per la creazione e la gestione dei contenuti, comprese le pagine di destinazione, i sottodomini e i frammenti.

### Guardrail dell’assistente AI {#ai-assistant-g}

I guardrail e le limitazioni per la **generazione di contenuti dell&#39;Assistente AI**, inclusi i canali supportati (e-mail, push, web, SMS) e le limitazioni dell&#39;editor di personalizzazione, sono elencati in [questa pagina](../content-management/gs-generative.md#generative-guardrails).

### Guardrail delle pagine di destinazione {#lp-guardrails}

Alle [pagine di destinazione](../landing-pages/get-started-lp.md) vengono applicati i seguenti guardrail:

* Solo un componente **Modulo** può essere utilizzato in una singola pagina principale.
* Il componente **Modulo** non può essere utilizzato nelle pagine secondarie.
* Non puoi aggiungere una preintestazione a una pagina di destinazione.
* Non è possibile selezionare l’opzione **Crea il codice** durante la progettazione di una pagina di destinazione principale.

### Guardrail per i sottodomini {#subdomain-guardrails}

I guardrail e le limitazioni applicabili alla delega di un sottodominio in Journey Optimizer sono descritti in dettaglio in [questa pagina](../configuration/delegate-subdomain.md#guardrails).

### Guardrail per i frammenti {#fragments-guardrails}

Ai [frammenti](../content-management/fragments.md) vengono applicati i seguenti guardrail:

* Per creare, modificare, archiviare e pubblicare frammenti sono necessarie le autorizzazioni **[!DNL Manage library items]** e **[Pubblica frammento]** incluse nel profilo del prodotto **[!DNL Content Library Manager]**. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)
* I frammenti visivi sono disponibili solo per il canale e-mail.
* I frammenti di espressione non sono disponibili per il canale in-app.
* I frammenti visivi non possono superare **100 KB**. I frammenti di espressione non possono superare **200 KB**.
* Per utilizzare un frammento in un percorso o in una campagna, ora è necessario che sia in stato **Live**.
* Gli [attributi contestuali](../personalization/personalization-build-expressions.md) non sono supportati nei frammenti.
* I frammenti visivi non sono compatibili tra le modalità Utilizza temi e Stile manuale. Per poter utilizzare un frammento in un contenuto in cui si desidera applicare un tema, è necessario creare il frammento in modalità Utilizza temi. [Ulteriori informazioni sui temi](../email/apply-email-themes.md)
* Quando il tracciamento è abilitato in un percorso o in una campagna, se aggiungi collegamenti a un frammento e quest’ultimo viene utilizzato in un messaggio, tali collegamenti vengono tracciati come tutti gli altri collegamenti inclusi nel messaggio. [Ulteriori informazioni su collegamenti e tracciamento](../email/message-tracking.md)

## Tipi di pubblico e profili {#audiences-profiles}

Questa sezione illustra i guardrail per la gestione del pubblico, la gestione del profilo e le considerazioni per i profili da coinvolgere.

### Guardrail del profilo e del pubblico {#audience}

* Puoi pubblicare fino a **10 composizioni di pubblico** in una data sandbox. Se hai raggiunto questa soglia, elimina una composizione per liberare spazio e pubblicarne una nuova.

  Per ulteriori informazioni sulle composizioni del pubblico, consulta [questa pagina](../audience/get-started-audience-orchestration.md).

* Durante l’acquisizione dei dati, negli indirizzi e-mail viene fatta distinzione tra maiuscole e minuscole. Ciò significa che è possibile creare profili duplicati (ad esempio, un profilo per John.Greene@luma.com e un altro profilo per john.greene@luma.com) e utilizzarli quando si esegue il targeting del destinatario corrispondente nei percorsi e nelle campagne [!DNL Journey Optimizer].

* Quando esegui il targeting di profili identificati da pseudonimi (visitatori non autenticati) con canali in entrata, puoi impostare un valore TTL (Time-to-live) per l’eliminazione automatica del profilo, in modo da gestire il conteggio dei profili coinvolti e i costi associati. [Ulteriori informazioni](#profile-management-inbound)

## Gestione delle decisioni {#decision-management}

### Guardrail per la funzione Decisioni e la gestione delle decisioni {#decisioning-guardrails}

I guardrail e le limitazioni da tenere presenti quando si lavora con la funzione Decisioni o la gestione delle decisioni sono descritti nelle seguenti sezioni:

* [Guardrail e limitazioni per la funzione Decisioni](../experience-decisioning/decisioning-guardrails.md)
* [Guardrail e limitazioni per la gestione delle decisioni](../offers/decision-management-guardrails.md)

## Percorsi {#journeys-guardrails}

Questa sezione illustra i guardrail e le limitazioni per i percorsi, incluse le limitazioni generali, i componenti (azioni, eventi, origini dati), le attività e funzioni specifiche come le azioni personalizzate e l’editor di espressioni.

### Guardrail di percorso generale {#journeys-guardrails-journeys}

* Il numero di attività in un percorso è limitato a **50**. Il numero di attività viene visualizzato nella sezione in alto a sinistra dell’area di lavoro del percorso.

  Poiché i percorsi si avvicinano a questo limite, le prestazioni di modifica e pubblicazione potrebbero peggiorare e potrebbero verificarsi errori di salvataggio o convalida. In questo caso, dividi il percorso in percorsi secondari più piccoli utilizzando [attività Salta](../building-journeys/jump.md) o ricrealo in una nuova versione. Il limite di attività non può essere aumentato.

* Per impostazione predefinita, il numero di percorsi di esecuzione live, in pausa o a secco è limitato a **100**. Il numero corrente di percorsi viene visualizzato sopra l’area di lavoro del percorso.

  Durante la pubblicazione dei percorsi, questi vengono scalati e regolati automaticamente per garantire la massima velocità effettiva e stabilità. In prossimità del traguardo di 100 percorsi live alla volta, nell’interfaccia utente verrà visualizzata una notifica di tale risultato. Se visualizzi questa notifica e hai la necessità di estendere i percorsi oltre ai 100 percorsi live alla volta, puoi creare un ticket per l’assistenza clienti e ti aiuteremo a raggiungere i tuoi obiettivi.

* Quando si utilizza una qualificazione del pubblico in un percorso, l&#39;attività di qualificazione del pubblico può richiedere fino a **10 minuti** per essere attiva e ascoltare i profili che entrano o escono dal pubblico.

* Un&#39;istanza di percorso per un profilo ha una dimensione massima di **1 MB**. Tutti i dati raccolti come parte dell’esecuzione del percorso vengono archiviati nella relativa istanza. Pertanto, i dati di un evento in arrivo, le informazioni sul profilo recuperate da Adobe Experience Platform, le risposte alle azioni personalizzate, ecc. vengono memorizzati in tale istanza del percorso, con un impatto sulle relative dimensioni. Quando un percorso inizia con un evento, è consigliabile limitare la dimensione massima del payload dell&#39;evento (ad esempio, al di sotto di **800 KB**) per evitare di raggiungere tale limite dopo alcune attività, nell&#39;esecuzione del percorso. Una volta raggiunto tale limite, il profilo è in stato di errore e verrà escluso dal percorso.

* Per ogni versione del profilo e del percorso, il runtime del percorso mantiene una coda interna di un massimo di **10 eventi in sospeso** durante l&#39;elaborazione di uno di essi. Se questo limite viene raggiunto, gli eventi aggiuntivi vengono eliminati con il motivo `maxInstanceStackEventsReached` fino allo svuotamento dello stack. Consulta [Eventi eliminati a causa di un’istanza di percorso bloccata](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached).

* Oltre al timeout utilizzato nelle attività di percorso, esiste anche un timeout di percorso globale che non viene visualizzato nell’interfaccia e non può essere modificato. Questo timeout globale interrompe l&#39;avanzamento dei singoli utenti nel percorso **91 giorni** dopo l&#39;immissione. [Ulteriori informazioni](../building-journeys/journey-properties.md#global_timeout)

>[!TIP]
>
>**Cosa significa per te:** Il limite di **50 attività** e il limite di **100 percorsi attivi** sono i due guardrail che la maggior parte dei team incontra prima durante il ridimensionamento. Pianifica la suddivisione del percorso in anticipo e distribuisci gli orari di inizio del Read Audience a distanza di almeno 5-10 minuti per evitare conflitti nella velocità effettiva delle sandbox.

#### Convalida della dimensione del payload del percorso {#journey-payload-size}

Quando salvi o pubblichi un percorso, Journey Optimizer convalida la dimensione totale del payload del percorso per mantenerne la stabilità e le prestazioni.

| Scenario | Soglia | Comportamento |
|---|---|---|
| Payload &lt; 90% del limite | Sotto avvertenza | Il percorso salva e pubblica correttamente. Nessun avviso o errore visualizzato. |
| Payload 90-99% del limite | Avvertenza (soft) | Il percorso salva e pubblica con un avviso: **Avviso**: le dimensioni del payload del Percorso sono prossime al limite. Nodo più grande: “[NodeName]” (tipo: “[NodeType]”, dimensione: [N] byte). |
| Payload ≥ 100% del limite | **Errore (rigido)** | Salvataggio o pubblicazione bloccato. Restituisce **Entità richiesta HTTP 413 troppo grande**. Errore: le dimensioni del payload di Percorso superano il limite consentito. Nodo più grande: “[NodeName]” (tipo: “[NodeType]”, dimensione: [N] byte). |

**Configurazione predefinita**

* **Dimensione massima predefinita richiesta**: **2 MB** (2.000.000 byte). Alcune organizzazioni possono avere limiti personalizzati configurati da Adobe.
* **Soglia di avvertenza**: 90% del limite massimo.
* **Soglia di errore**: 100% del limite massimo.

**Risoluzione di problemi e consigli**

* Rivedi il nodo più grande evidenziato nell’avvertenza o nell’errore.
* Semplifica le condizioni, riduci le mappature dei dati e rimuovi passaggi o parametri non necessari.
* Se necessario, potrebbe essere utile suddividere il percorso in percorsi più piccoli.
* Se ritieni che la tua organizzazione necessiti di un limite più alto, contatta il rappresentante Adobe.

Per monitorare le dimensioni correnti del payload del percorso prima della pubblicazione, utilizza l&#39;indicatore **[!UICONTROL Dimensioni correnti payload del percorso]** nel pannello delle proprietà del percorso. [Scopri come controllare le dimensioni del payload di percorso](../building-journeys/journey-properties.md#journey-payload-size)

### Confronto dei pacchetti di licenze {#select-package-limitations}

>[!NOTE]
>
>Le limitazioni del pacchetto Select riportate di seguito non sono applicabili ai percorsi Read Audience (Leggi pubblico) o Business Event (Evento aziendale). Se hai bisogno di una logica di percorso più complessa con più azioni, condizioni o attività di attesa, valuta l’aggiornamento del pacchetto di licenza o l’utilizzo di percorsi Leggi pubblico, se applicabile.

Per i clienti che utilizzano il pacchetto di licenza **Select**, le seguenti limitazioni aggiuntive si applicano in modo specifico ai percorsi unitari (percorsi che iniziano con un evento o una qualifica di pubblico):

| Limitazione | Codice errore | Descrizione |
|---|---|---|
| È consentita una sola azione | `ERR_PKG_SELECT_8` | I percorsi unitari possono contenere solo **una** attività di azione. Non sono consentite più attività e-mail, push, SMS o altre attività all’interno dello stesso percorso. |
| Nessuna condizione consentita | `ERR_PKG_SELECT_7` | Le attività di condizione non possono essere utilizzate in percorsi unitari. Il percorso deve seguire un unico percorso lineare senza logica di diramazione. |
| Nessuna attività di attesa | `ERR_PKG_SELECT_6` | Le attività di attesa non possono essere aggiunte a percorsi unitari. Le azioni devono essere eseguite immediatamente senza ritardi. |
| Le transizioni timeout/errore devono andare al nodo finale | `ERR_PKG_SELECT_2` | Se configuri le transizioni di timeout o errori per un’azione (ad esempio, un’azione e-mail), questi percorsi devono puntare direttamente a un nodo finale. Non possono connettersi ad altre attività o azioni nel percorso. |

>[!TIP]
>
>**Cosa significa per te:** se sei nel pacchetto Select e hai bisogno di logica di ramificazione, attività di attesa o più azioni, devi utilizzare un percorso Read Audience oppure contattare il rappresentante Adobe per informazioni sull&#39;aggiornamento del pacchetto.

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

| Guardrail | Elemento “value” | Note |
|---|---|---|
| Limite di limitazione — risposta &lt; 0,75 s | **300.000 chiamate / min** per host e per sandbox | Finestra scorrevole. Imposto per sandbox ed endpoint. |
| Limite di limitazione — risposta > 0,75 s | **150.000 chiamate / 30 s** per host e per sandbox | Finestra scorrevole. Limite separato applicato quando la latenza dell’endpoint supera 0,75 s. |
| Tipo di URL | Solo statico | I parametri dinamici nell’URL dell’azione personalizzata non sono supportati. |
| Metodi HTTP supportati | POST, PUT, GET | Altri metodi non sono supportati. |
| Formato del parametro di query/nome intestazione | Non deve iniziare con `.` o `$` | I nomi che iniziano con questi caratteri vengono rifiutati. |
| Indirizzi IP nell’URL | Non consentito | Utilizza nomi host invece di indirizzi IP. |
| Indirizzi interni di Adobe | Non consentito | Gli indirizzi `.adobe.*` non sono consentiti negli URL e nelle API. |
| Azioni personalizzate incorporate | Non può essere rimosso | Le azioni personalizzate incorporate sono permanenti. |
| Formato payload | Solo JSON | Il formato JSON è richiesto per i payload di richiesta e di risposta. Consulta [questa pagina](../action/about-custom-action-configuration.md#custom-actions-limitations). |
| Velocità effettiva minima dell’endpoint | 200 TPS | Qualsiasi endpoint interessato da un&#39;azione personalizzata deve supportare almeno 200 TPS. |

>[!TIP]
>
>**Cosa significa per te:** il limite predefinito di 300.000 chiamate/min protegge gli endpoint esterni dall&#39;essere sovraccaricati dal throughput del percorso. Se l&#39;endpoint è in grado di gestire un carico maggiore, è possibile aumentare questo limite utilizzando [API di limitazione](../configuration/capping.md) o [API di limitazione](../configuration/throttling.md). Se hai bisogno di un limite organizzativo più elevato, contatta il rappresentante Adobe.

Questo limite è stato impostato in base all’utilizzo da parte della clientela, per proteggere gli endpoint esterni interessati dalle azioni personalizzate. Se necessario, puoi ignorare questa impostazione definendo un limite di limitazione di utilizzo o di limitazione maggiore tramite le rispettive API. Consulta [questa pagina](../configuration/external-systems.md).

### Eventi {#events-g}

Agli [eventi](../event/about-events.md) nei tuoi percorsi vengono applicati i seguenti guardrail:

* Journey Optimizer supporta un volume massimo di **5.000 eventi di percorso in entrata al secondo** in tutte le sandbox. Ulteriori informazioni su questa limitazione [in questa pagina](../event/about-events.md#event-thoughput).
* I percorsi attivati da eventi possono richiedere fino a **5 minuti** per elaborare la prima azione nel percorso.
* Per gli eventi generati dal sistema, i dati in streaming utilizzati per avviare un percorso del cliente devono essere configurati prima in Journey Optimizer per ottenere un ID di orchestrazione univoco. Questo ID di orchestrazione deve essere aggiunto al payload di streaming in Adobe Experience Platform. Questa limitazione non si applica agli eventi basati su regole.
* Gli eventi di business non possono essere utilizzati in combinazione con eventi unitari o attività di qualificazione del pubblico.
* I percorsi unitari (a partire da un evento o da una qualificazione del pubblico) includono un guardrail che impedisce ai percorsi di essere attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo è bloccato temporaneamente per **5 minuti**. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.
* Journey Optimizer richiede che gli eventi vengano inviati in streaming al servizio core di raccolta dati (DCCS) per poter attivare un percorso. Eventi acquisiti in batch, eventi inseriti tramite **Query Service** o eventi provenienti da set di dati interni di Journey Optimizer (feedback messaggi, tracciamento e-mail, ecc.) non possono essere utilizzati per attivare un percorso. Per i casi d’uso in cui non è possibile ottenere eventi in streaming, è necessario creare un pubblico basato su tali eventi e utilizzare l’attività **Leggi pubblico**. Tecnicamente, è possibile usare la qualificazione del pubblico, ma non è consigliato poiché potrebbe causare delle problematiche a valle in base alle azioni utilizzate.

### Origini dati {#data-sources-g}

Alle [origini dati](../datasource/about-data-sources.md) nei tuoi percorsi vengono applicati i seguenti guardrail:

* Le origini dati esterne possono essere sfruttate all’interno di un percorso del cliente per ricercare dati esterni in tempo reale. Queste origini devono essere utilizzabili tramite API REST, supportare JSON ed essere in grado di gestire il volume delle richieste.
* Non sono consentiti indirizzi di Adobe interni (`.adobe.*`) negli URL e nelle API.

>[!NOTE]
>
>Poiché le risposte sono ora supportate, per i casi d’uso relativi a origini dati esterne devi utilizzare azioni personalizzate anziché origini dati.

### Creazione di percorsi e profili {#journeys-limitation-profile-creation}

In Adobe Experience Platform si verifica un ritardo associato alla creazione/aggiornamento dei profili basati su API. Il target del livello di servizio (Service Level Target, SLT) in termini di latenza è &lt; di 1 minuto dall&#39;acquisizione al profilo unificato per il 95° percentile delle richieste, con un volume di **20.000 richieste al secondo (RPS)**.

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

Ulteriori guardrail, tra cui consigli su tipi di pubblico in streaming e in batch e limitazioni del pubblico per la composizione, sono elencati in [questa pagina](../building-journeys/audience-qualification-events.md#audience-qualification-guardrails).

#### Attività di Campaign {#ac-g}

I seguenti guardrail si applicano alle attività di **[!UICONTROL Campaign v7/v8]** e di **[!UICONTROL Campaign Standard]**:

* Le attività di Adobe Campaign non possono essere utilizzate con un’attività Leggi pubblico o Qualificazione del pubblico.
* Le attività di **[!UICONTROL Campaign Standard]** non possono essere utilizzate con altre attività di canali: Scheda, Esperienza basata su codice, E-mail, Push, SMS, Messaggi in-app, Web.
* Le attività di **[!UICONTROL Campaign v7/v8]** possono essere utilizzate insieme alle attività native dei canal nello stesso percorso.

#### Eventi di reazione {#reaction-events-g}

Guardrail specifici si applicano agli eventi **[!UICONTROL Reazione]**, incluso il requisito di inserire l&#39;attività immediatamente dopo un&#39;azione del canale e l&#39;impossibilità di tenere traccia dei messaggi inviati in un percorso diverso. Sono elencati in [questa pagina](../building-journeys/reaction-events.md#guardrails-limitations).

#### Attività in-app {#in-app-activity-limitations}

All’azione **[!UICONTROL messaggio in-app]**, vengono applicati i seguenti guardrail: Ulteriori informazioni sui messaggi in-app sono disponibili in [questa pagina](../in-app/create-in-app.md).

* Questa funzione non è attualmente disponibile per la clientela del settore dell’assistenza sanitaria.

* La personalizzazione può contenere solo attributi di profilo.

* L’attività In-app non può essere utilizzata con le attività di **[!UICONTROL Campaign Standard]**.

* La visualizzazione in-app è legata alla durata del percorso, il che significa che quando il percorso termina per un profilo, tutti i messaggi in-app all’interno di quel percorso cesseranno di essere visualizzati per quel profilo. Di conseguenza, non è possibile interrompere un messaggio in-app direttamente da un’attività del percorso. Al contrario, per impedire la visualizzazione dei messaggi in-app nel profilo, devi terminare l’intero percorso.

* In modalità di test, la visualizzazione in-app dipende dalla durata del percorso. Per evitare che il percorso termini anticipatamente durante il test, regola il valore **[!UICONTROL Tempo di attesa]** per le attività di **[!UICONTROL Attesa]**.

* Le attività di **[!UICONTROL Reazione]** non possono essere utilizzate per reagire a un’apertura in-app o a un clic.

* È possibile che si verifichi un ritardo di attivazione tra il momento in cui un profilo utente raggiunge un’attività in-app nell’area di lavoro e il momento in cui inizia a visualizzare tale messaggio in-app.

* La dimensione del contenuto del messaggio in-app è limitata a **2 MB**. L’inclusione di immagini di grandi dimensioni può ostacolare il processo di pubblicazione.

#### Attività di decisione sui contenuti {#content-decision-g}

All&#39;attività **[!UICONTROL Content decision]** si applicano protezioni specifiche, incluso un ritardo di 48 ore prima che i criteri di consenso aggiornati diventino effettivi nei criteri di decisione. Sono elencati in [questa pagina](../building-journeys/content-decision.md#guardrails).

#### Attività Salta {#jump-g}

All’attività **[!UICONTROL Salta]** si applicano guardrail specifici. Sono elencati in [questa pagina](../building-journeys/jump.md#jump-limitations).

#### Attività Leggi pubblico {#read-segment-g}

All’attività del percorso [Leggi pubblico](../building-journeys/read-audience.md), vengono applicati i seguenti guardrail:

| Guardrail | Elemento “value” | Note |
|---|---|---|
| Istanze simultanee (tutte le sandbox + percorsi) | **5** | Evita di pianificare più di 5 percorsi con Read Audience che inizia contemporaneamente; distribuiscili a 5-10 minuti di distanza. |
| Velocità effettiva sandbox | **20.000 profili/sec** (condivisi) | Condiviso tra tutte le attività Read audience nella sandbox. Se vengono raggiunti i limiti, i processi possono essere messi in coda. |
| Throughput configurabile per attività | **500-20.000 profili/sec** | Configura per attività entro il limite condiviso della sandbox. |
| Timeout elaborazione processo | **12 ore** | I processi che non possono essere elaborati entro 12 ore vengono puliti automaticamente e non verranno eseguiti. |
| Finestra Riprova | Fino a **1 ora** (intervalli di 10 minuti) | I tentativi vengono applicati durante il recupero del processo di esportazione. I percorsi possono essere eseguiti fino a 1 ora dopo l’orario pianificato. |
| Percentuale di lettura ID supplementari | **500 profili/sec** per istanza di percorso | Applicabile quando sono in uso ID supplementari. |
| Leggi istanze di pubblico al percorso | **1** | Un percorso può avere una sola attività Read Audience. |
| Tipi di pubblico | Il pubblico in streaming è sempre aggiornato | I tipi di pubblico in batch vengono valutati solo una volta al giorno al momento della valutazione giornaliera in batch. |
| Aggiornamento degli attributi del profilo | Aggiornato alle **attività** | All’ingresso del percorso, i profili utilizzano i valori degli snapshot batch. Gli attributi vengono aggiornati quando un profilo raggiunge un’attività Attendi. |
| Posizionamento nel percorso | Prima attività o dopo un evento di business | L’attività Read Audience può essere utilizzata solo come prima attività in un percorso o dopo un’attività evento business. |
| Utilizzo con Adobe Campaign | Non supportato | L’attività Read Audience non può essere utilizzata con le attività di Adobe Campaign. |
| Più tipi di pubblico | Non supportato direttamente | L’attività Read Audience può eseguire il targeting di un solo pubblico al percorso. Per utilizzare più tipi di pubblico, devi prima unirli. [Scopri come](../audience/get-started-audience-orchestration.md) |

>[!TIP]
>
>**Ciò significa per te:** il limite di 5 istanze simultanee è un tetto massimo per l&#39;intera organizzazione. Se pianifichi più team Leggi percorsi di pubblico, coordina attentamente gli orari di inizio. I processi che non rientrano nella finestra di elaborazione di 12 ore vengono eliminati automaticamente. Confermare sempre l’esecuzione corretta nei registri del percorso.

Consulta anche [consigli e configurazione](../building-journeys/read-audience.md#must-read) per l’attività Leggi pubblico.

#### Attività Aggiorna profilo {#update-profile-g}

All’attività **[!UICONTROL Aggiorna profilo]** vengono applicati guardrail specifici. Sono elencati in [questa pagina](../building-journeys/update-profiles.md).

#### Pausa percorso {#pause-g}

Guardrail specifici si applicano a **percorsi di pausa**, inclusa una durata massima di pausa di **14 giorni** e un limite di **10 milioni di profili** in tutti i percorsi di pausa dell&#39;organizzazione. Sono elencati in [questa pagina](../building-journeys/journey-pause.md#journey-pause-guardrails).

#### Prova del percorso {#dry-run-g}

Guardrail specifici si applicano a **Percorso di esecuzione in prova**, incluso il conteggio per le quote di profilo e di percorso live. Sono elencati in [questa pagina](../building-journeys/journey-dry-run.md#journey-dry-run-limitations).

#### Frammenti percorso {#fragments-journey-g}

I guardrail specifici si applicano a **frammenti di Percorso**, inclusi un massimo di **20 nodi per frammento** e **200 frammenti attivi per sandbox**. Sono elencati in [questa pagina](../building-journeys/journey-fragments.md#guardrails).

#### Inviare utilizzando gli scaglioni {#waves-g}

Guardrail specifici si applicano all&#39;invio di **onde in percorsi**, inclusi un intervallo di 2-10 onde e un intervallo minimo di **30 minuti** tra le onde. Sono elencati in [questa pagina](../building-journeys/send-using-waves.md#limitations-guardrails).

#### Simulazione percorso {#simulation-g}

Guardrail specifici applicabili alla **simulazione percorso**. Sono elencati in [questa pagina](../building-journeys/simulate-journey.md#limitations).

## Orchestrazione della campagna {#campaign-orchestration}

### Guardrail per l’orchestrazione delle campagne {#orchestration-guardrails}

I guardrail e le limitazioni da tenere presenti quando utilizzi l’orchestrazione di una campagna sono descritti in questa sezione: [Guardrail e limitazioni](../orchestrated/guardrails.md).
