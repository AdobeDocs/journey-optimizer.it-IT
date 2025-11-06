---
solution: Journey Optimizer
product: journey optimizer
title: Riferimento codici di errore
description: Scopri i codici di errore comuni in Adobe Journey Optimizer e come risolverli
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: errore, codici, risoluzione dei problemi, percorso, campagna, messaggi
source-git-commit: 405c87f9ca138e4e92438704b5051ce89c73d726
workflow-type: tm+mt
source-wordcount: '2392'
ht-degree: 1%

---


# Riferimento codici di errore {#error-codes}

Adobe Journey Optimizer utilizza codici di errore standardizzati per aiutarti a identificare e risolvere rapidamente i problemi tra percorsi, campagne e configurazioni di messaggi. Comprendere questi codici di errore può ridurre in modo significativo i tempi di risoluzione dei problemi e aiutarti a mantenere prestazioni ottimali della campagna.

## Informazioni sulla struttura del codice di errore {#error-code-structure}

I codici di errore di Adobe Journey Optimizer seguono un pattern di denominazione coerente che consente di identificare il componente e il tipo di problema:

* **Prefisso servizio**: indica quale servizio Adobe Journey Optimizer ha generato l&#39;errore (ad esempio, CJMPTS per il servizio push/trasporto, CJMRT per il runtime di Percorso, CJMMAS per il servizio di authoring messaggi, CJMCMP per Campaign, CJMTL per il livello trasporto, CJMRPS per il servizio di reporting/provisioning)
* **Numero errore**: identificatore univoco per la condizione di errore specifica
* **Codice stato HTTP**: codice stato HTTP standard (ad esempio 400, 403, 422, 500)

Esempio: `CJMRT-030012-422` indica un errore di runtime del Percorso (CJMRT) con il numero di errore 030012 e lo stato HTTP 422 (entità non elaborabile).

## Dove trovare i codici di errore {#find-error-codes}

I codici di errore vengono visualizzati in diverse posizioni all’interno di Adobe Journey Optimizer:

* Rapporti e registri di esecuzione del percorso
* Schermate di attivazione della campagna
* Avvisi di convalida dei messaggi
* Notifiche e avvisi di sistema
* Risposte API (quando si utilizzano API REST)

Quando si verifica un errore, annota il codice di errore completo e l’eventuale ID richiesta associato, in quanto sono essenziali per la risoluzione dei problemi e per supportare l’escalation.

## Codici di errore comuni per servizio {#error-codes-by-service}

### CJMPTS: errori del servizio push e trasporto {#cjmpts-errors}

Questi errori si verificano durante le operazioni di consegna e trasporto delle notifiche push.

| Codice di errore | Descrizione | Causa principale | Risoluzione |
|------------|-------------|-----------|-----------|
| **CJMPTS-1410-500** | Errore interno del server nell’azione di invio push/canale | Interruzione del back-end del canale, credenziali scadute, configurazione errata o bug del provider | &#x200B;1. Riprova dopo il ritardo<br/>2. Verificare le configurazioni e le quote del provider<br/>3. Verificare che le credenziali push siano valide<br/>4. Test con un canale alternativo<br/>5. Se persiste, contatta il supporto Adobe con ID richiesta <br/><br/>**Documentazione correlata**: [Configurazione push](../push/push-configuration.md) |
| **CJMPTS-1006-404** | Errore di invio push/SMS con &quot;risorsa non trovata&quot; | Il provider o il canale a cui si fa riferimento non esiste, è stato digitato in modo errato o il provisioning è stato annullato | &#x200B;1. Rivedi e correggi i riferimenti e gli ID provider/canale<br/>2. Verifica configurazione sandbox/organizzazione<br/>3. Verificare che le configurazioni del canale siano attive<br/>4. Ricrea la configurazione del canale, se necessario <br/><br/>**Documentazione correlata**: [Superfici di canale](../configuration/channel-surfaces.md) |
| **CJMPTS-1510-500** | Errore interno del server nell’invio del canale push | Malfunzionamento del trasporto/push back-end; errore del provider o dell’infrastruttura | &#x200B;1. Controllare le impostazioni di provisioning dei canali<br/>2. Verificare che le credenziali push siano valide<br/>3. Ripetere l&#39;operazione<br/>4. Se persiste, contatta il supporto Adobe con ID richiesta <br/><br/>**Documentazione correlata**: [Configurazione push](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Errore interno del server durante l’invio/elaborazione push (gateway di terze parti) | Errore temporaneo di malfunzionamento del cloud o errore sconosciuto del servizio | &#x200B;1. Verificare la configurazione del provider/canale<br/>2. Verificare lo stato del gateway di terze parti<br/>3. Riprova tra qualche minuto<br/>4. Controlla i registri per il contesto aggiuntivo <br/><br/>**Documentazione correlata**: [Notifiche push](../push/create-push.md) |
| **CJMPTS-1310-500** | Errore interno del servizio di rendering (anteprima o invio live) | Rendering del modello a valle non riuscito, in genere a causa di problemi di sintassi JSON/modello | &#x200B;1. Convalidare la sintassi e la struttura del modello<br/>2. Verifica che tutte le variabili di personalizzazione siano valide<br/>3. Utilizza un payload di test per identificare il problema<br/>4. Semplifica la complessità del modello se necessario <br/><br/>**Documentazione correlata**: [Modelli di messaggio](../content-management/content-templates.md), [Sintassi Personalization](../personalization/personalization-syntax.md) |

### CJMRT: errori di runtime di Percorso e API {#cjmrt-errors}

Questi errori si verificano durante l’esecuzione del percorso, l’elaborazione degli eventi e le operazioni API.

| Codice di errore | Descrizione | Causa principale | Risoluzione |
|------------|-------------|-----------|-----------|
| **CJMRT-110001-500** | È stato superato il numero massimo di esecuzioni per il passaggio del flusso di lavoro (ad esempio, timeout del passaggio di provisioning dell’affinità IP) | Il processo di flusso di lavoro/provisioning non è stato completato entro i tentativi/i tempi consentiti, spesso a causa di un ritardo dell’infrastruttura/del servizio o di un problema di back-end temporaneo | &#x200B;1. Riprovare tra poco<br/>2. Controlla [Stato Adobe](https://status.adobe.com/it) per informazioni sulle interruzioni<br/>3. Inoltra al supporto Adobe con dettagli su flusso di lavoro/processo/organizzazione<br/>4. Fornisci registri e acquisizioni di rete se disponibili <br/><br/>**Documentazione correlata**: [Risoluzione dei problemi di Percorso](troubleshooting.md) |
| **CJMRT-000071-400** | Richiesta non valida durante l’evento di percorso/test o la chiamata API | Il payload o i parametri non sono formattati correttamente o sono mancanti; l’input fa riferimento a una risorsa inesistente o inattiva | &#x200B;1. Esaminare il corpo della richiesta per i dettagli sull&#39;errore<br/>2. Riferimento/parametro corretto<br/>3. Rimuovi la configurazione avanzata e riprova<br/>4. Aggiungi le funzionalità una alla volta per identificare il problema <br/><br/>**Documentazione correlata**: [Risoluzione dei problemi di Percorso](troubleshooting.md), [Configurazione degli eventi](../event/about-events.md) |
| **CJMRT-000013-401** | Errore non autorizzato durante l’operazione di runtime del messaggio/evento API | Errore di autenticazione: token scaduto, autorizzazioni mancanti oppure integrazione/utente ha perso l’accesso all’ambiente | &#x200B;1. Verificare autorizzazioni e ruoli<br/>2. Aggiorna token di autenticazione<br/>3. Utilizza un account utente/servizio valido noto<br/>4. Rivedi assegnazioni profilo prodotto <br/><br/>**Documentazione correlata**: [Autorizzazioni](../administration/permissions.md) |
| **CJMRT-080605-400** | Richiesta non valida dal runtime del percorso (ad esempio, trigger di nodo, azione, ecc.) | La configurazione fa riferimento a una funzione/modello/canale rimosso/rinominato o non aggiornato | &#x200B;1. Convalidare tutti i riferimenti alle risorse<br/>2. Controlla la configurazione del percorso e i flag di funzionalità<br/>3. Aggiorna riferimenti interrotti<br/>4. Verifica aggiornamenti e migrazioni di sistema recenti <br/><br/>**Documentazione correlata**: [Creazione Percorso](journey-gs.md) |
| **CJMRT-030012-422** | Entità non elaborabile: azione non riuscita, evento non valido o payload non valido | Dati di input non validi (ad esempio pubblico, evento o attributo inesistenti) | &#x200B;1. Controllare nuovamente la struttura del payload di input/evento<br/>2. Verificare che gli oggetti a cui si fa riferimento (tipi di pubblico, set di dati) esistano e siano attivi<br/>3. Convalida che tutti i campi obbligatori sono presenti<br/>4. Test con payload valido noto <br/><br/>**Documentazione correlata**: [Risoluzione dei problemi di Percorso](troubleshooting.md), [Configurazione eventi](../event/about-events.md) |
| **CJMRT-130004-400** | Richiesta non valida: input non valido nel nodo di percorso o nella configurazione del canale | riferimenti di configurazione o payload di percorso rimossi/risorsa non valida | &#x200B;1. Rivedere la configurazione del nodo di percorso<br/>2. Verifica che siano presenti tutte le risorse a cui si fa riferimento (messaggi, tipi di pubblico, azioni)<br/>3. Correggi o aggiorna i riferimenti interrotti<br/>4. Ricompila la configurazione del percorso se necessario <br/><br/>**Documentazione correlata**: [Creazione del Percorso](journey-gs.md), [Azioni personalizzate](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | Conflitto - la risorsa esiste già | Tentativo di creare una risorsa con ID o nome duplicato | &#x200B;1. Usa ID e nomi univoci per tutte le risorse<br/>2. Verificare la presenza di risorse esistenti con lo stesso identificatore<br/>3. Eliminare o rinominare gli oggetti in conflitto<br/>4. Rivedi convenzioni di denominazione <br/><br/>**Documentazione correlata**: [Versioni Percorso](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | Richiesta non valida durante la configurazione/anteprima del percorso | Nel payload manca il collegamento della dipendenza richiesta o del modello interrotto | &#x200B;1. Convalida che tutte le risorse richieste sono attive<br/>2. Assicurati che i modelli e i blocchi di contenuto siano pubblicati<br/>3. Verificare che tutte le dipendenze siano collegate correttamente<br/>4. Rivedi risultati modalità test percorso <br/><br/>**Documentazione correlata**: [percorsi di test](testing-the-journey.md), [dipendenze Percorso](journey-gs.md) |
| **CJMRT-080608-400** | Richiesta non valida in dominio/canale/delega | Record DNS richiesti o configurazione e-mail/SMS mancante | &#x200B;1. Completare la configurazione DNS per i domini e-mail<br/>2. Verifica delega sottodominio completata<br/>3. Eseguire di nuovo le procedure guidate di configurazione<br/>4. Consenti propagazione DNS (fino a 72 ore)<br/><br/>**Documentazione correlata**: [Superfici di canale](../configuration/channel-surfaces.md), [Delega sottodominio](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | Errore interno nel payload | Errore di configurazione/dati back-end o configurazione non supportata | &#x200B;1. Riprovare l&#39;operazione<br/>2. Semplifica la configurazione se utilizzi funzionalità avanzate<br/>3. Inoltra al supporto Adobe con ID richiesta e payload esatto<br/>4. Verifica la presenza di problemi noti nelle note sulla versione <br/><br/>**Documentazione correlata**: [Risoluzione dei problemi di Percorso](troubleshooting.md) |

### CJMMAS: errori del servizio di authoring dei messaggi {#cjmmas-errors}

Questi errori si verificano durante la creazione, la modifica o la pubblicazione di messaggi, predefiniti e contenuti.

| Codice di errore | Descrizione | Causa principale | Risoluzione |
|------------|-------------|-----------|-----------|
| **CJMMAS-1732-500** | Bozza non riuscita: tutte le risorse non vengono pubblicate quando si invia una bozza/prova con una risorsa AEM | La risorsa pubblicata di recente non è ancora in AJO; mancata corrispondenza nell’ID della risorsa; uso cross-repo; ritardo nella sincronizzazione di AEM | &#x200B;1. Utilizza solo ID di risorse pubblicati dall&#39;archivio/ambiente corretto<br/>2. Consenti tempo per la sincronizzazione tra AEM e AJO<br/>3. Riprova con una risorsa valida nota<br/>4. Verifica lo stato di pubblicazione delle risorse in AEM <br/><br/>**Documentazione correlata**: [Integrazione Assets](../content-management/assets.md) |
| **CJMMAS-1069-500** | Errore interno durante il salvataggio o la pubblicazione del modello di messaggio | Eccezione di back-end (bug di infrastruttura/servizio o problema di contenuto); markup/funzione non supportati | &#x200B;1. Semplificare o ridurre la complessità del modello<br/>2. Aggiungi nuovamente il contenuto nei passaggi incrementali per identificare il problema<br/>3. Controlla la [pagina Stato Adobe](https://status.adobe.com/it)<br/>4. Rimuovi funzioni o markup non supportati <br/><br/>**Documentazione correlata**: [Modelli di contenuto](../content-management/content-templates.md) |
| **CJMMAS-1149-400** | Richiesta non valida durante il salvataggio di un messaggio, un predefinito o una variante | Campi obbligatori mancanti nel messaggio o configurazione non valida | &#x200B;1. Completare tutti i campi obbligatori (contrassegnati da asterisco)<br/>2. Convalida la configurazione del messaggio/predefinito<br/>3. Verifica i formati e i vincoli dei valori dei campi<br/>4. Rivedi i messaggi di convalida nell&#39;interfaccia utente <br/><br/>**Documentazione correlata**: [Canale e-mail](../email/get-started-email.md), [Superfici di canale](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | Entità non elaborabile nella modifica del predefinito per messaggi | Errore di convalida, campo non supportato o sintassi non corretta | &#x200B;1. Correggere gli errori di sintassi/campo come indicato<br/>2. Confronta con una configurazione valida<br/>3. Usa la convalida dell&#39;interfaccia utente dei messaggi prima di salvare<br/>4. Controlla i requisiti dei campi nella documentazione <br/><br/>**Documentazione correlata**: [Predefiniti per messaggi](../configuration/channel-surfaces.md), [Impostazioni e-mail](../email/email-settings.md) |
| **CJMMAS-1300-500** | Errore interno nell’authoring dei messaggi | Arresto del back-end dovuto a problemi di infrastruttura, contenuti di grandi dimensioni o tempi di inattività del servizio | &#x200B;1. Semplificare modello/contenuto (ridurre dimensioni/complessità)<br/>2. Ripetere l&#39;operazione<br/>3. Salvare il lavoro in modo incrementale<br/>4. Se persiste, passa al supporto Adobe <br/><br/>**Documentazione correlata**: [Modelli di contenuto](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | Stato di successo ma banner di errore: collegamento di rinuncia mancante | Collegamento per l’annullamento dell’iscrizione richiesto mancante nella variante e-mail | &#x200B;1. Aggiungi il collegamento di rinuncia/annullamento iscrizione a tutte le varianti di e-mail<br/>2. Verifica che il collegamento sia presente in tutte le versioni linguistiche<br/>3. Utilizza l&#39;helper di personalizzazione per inserire il collegamento di rinuncia<br/>4. Verifica tutte le varianti prima di pubblicare <br/><br/>**Documentazione correlata**: [Gestione rinuncia](../privacy/opt-out.md), [Progettazione e-mail](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | Non consentito durante l’aggiornamento/pubblicazione di un modello o di un predefinito | L’utente non dispone delle autorizzazioni/del ruolo richiesti o l’azione non è consentita nello stato corrente | &#x200B;1. Verifica che l’utente disponga delle autorizzazioni appropriate (Message Manager, Author, ecc.)<br/>2. Verifica lo stato del predefinito/modello (bozza, pubblicato, archiviato)<br/>3. Richiedi l&#39;accesso all&#39;amministratore se necessario<br/>4. Rivedi assegnazioni profilo prodotto <br/><br/>**Documentazione correlata**: [Autorizzazioni](../administration/permissions.md), [Controllo dell&#39;accesso](../administration/permissions-overview.md) |

### CJMCMP: errori della campagna {#cjmcmp-errors}

Questi errori si verificano durante la creazione, la configurazione e l’attivazione della campagna.

| Codice di errore | Descrizione | Causa principale | Risoluzione |
|------------|-------------|-----------|-----------|
| **CJMCMP-6003-400** | &quot;È presente almeno una campagna errata&quot; durante la pubblicazione/modalità di test percorso/messaggio | Il nodo fa riferimento a una campagna mancante, non pubblicata o non valida; il percorso legacy o clonato non crea inline | &#x200B;1. Aprire ogni nodo del messaggio e verificare la configurazione<br/>2. Ricollegare o aggiungere di nuovo i nodi del messaggio<br/>3. Attiva la modalità di test per forzare la creazione di campagne in linea<br/>4. Passa alla creazione guidata nuovo percorso se il problema è frequente <br/><br/>**Documentazione correlata**: [Creazione Percorso](journey-gs.md), [Verifica percorsi](testing-the-journey.md) |
| **CJMCMP-2003-400** | Banner dell’interfaccia utente: &quot;L’esperimento non è corretto&quot; in E-mail Designer | Provider di dati/esperimento non aggiornato o mancante; pulizia dell’esperimento non riuscita, mancata corrispondenza dello schema o bug di convalida dell’interfaccia utente | &#x200B;1. Rimuovere i campi dell&#39;esperimento non utilizzati<br/>2. Convalidare le connessioni a schemi e provider di dati<br/>3. Ricarica interfaccia utente e cancella cache del browser<br/>4. Ricrea nodo/e-mail se il problema non è stato risolto <br/><br/>**Documentazione correlata**: [Esperimenti di contenuto](../content-management/content-experiment.md) |
| **CJMCMP-3001-400** | Simulazione/anteprima &quot;filtro con tipo di superficie errato&quot; | Il nodo creato utilizzando la struttura legacy invia type=surfaceId, il backend prevede brandingPresetId | &#x200B;1. Eliminare e ricreare il nodo interessato<br/>2. Utilizza la nuova versione/modello del percorso<br/>3. Utilizza la modalità di test per cancellare la configurazione<br/>4. Ricrea in blocco nodi se il problema è diffuso <br/><br/>**Documentazione correlata**: [Superfici di canale](../configuration/channel-surfaces.md), [Simulazione messaggio](../content-management/preview.md) |
| **CJMCMP-2050-400** | Richiesta non valida nell’attivazione o nell’approvazione della campagna | La campagna fa riferimento a un criterio o a un segmento non valido/mancante | &#x200B;1. Controlla tutte le configurazioni dei nodi della campagna<br/>2. Verificare che i collegamenti ai criteri o ai segmenti siano correnti e validi<br/>3. Aggiornamento con configurazione corretta<br/>4. Verifica di nuovo la campagna prima dell&#39;attivazione <br/><br/>**Documentazione correlata**: [Creazione campagna](../campaigns/create-campaign.md), [Approvazione campagna](../test-approve/gs-approval.md) |

### CJMTL: errori del livello di trasporto {#cjmtl-errors}

Questi errori si verificano durante le operazioni di trasporto e consegna dei messaggi.

| Codice di errore | Descrizione | Causa principale | Risoluzione |
|------------|-------------|-----------|-----------|
| **CJMTL-010018-422** | &quot;Personalization non consentito nel nome di dominio&quot; durante il salvataggio/invio di contenuto | Una convalida eccessivamente rigida ha temporaneamente interrotto la personalizzazione del dominio href dinamico | &#x200B;1. Effettuare il refactoring dei collegamenti se si utilizzano le variabili di dominio<br/>2. Verificare che la versione più recente di AJO sia in uso<br/>3. Ripetere l&#39;operazione<br/>4. Usa i domini statici se il problema persiste <br/><br/>**Documentazione correlata**: [Sintassi Personalization](../personalization/personalization-syntax.md), [Progettazione e-mail](../email/content-from-scratch.md) |
| **CJMTL-010011-422** | Entità non elaborabile: l’invio push/SMS/e-mail non riesce, indica un &quot;campo non valido&quot; | Dati del payload o del destinatario/contatto mancanti o non validi | &#x200B;1. Esaminare i registri per individuare errori di campo specifici<br/>2. Correggi profilo/informazioni di contatto<br/>3. Convalida con profilo di test<br/>4. Reimposta il formato del payload come necessario <br/><br/>**Documentazione correlata**: [Gestione profili](../audience/get-started-profiles.md), [Profili di test](../audience/creating-test-profiles.md) |

### CJMRPS: errori Reporting and Provisioning Service {#cjmrps-errors}

Questi errori si verificano durante la configurazione della generazione rapporti e le operazioni di provisioning dei set di dati.

| Codice di errore | Descrizione | Causa principale | Risoluzione |
|------------|-------------|-----------|-----------|
| **CJMRPS-1047-409** | &quot;Conflitto. Set di dati già aggiunto&quot; quando si aggiunge un set di dati di reporting | Tentativo di aggiungere un set di dati per il quale è già stato eseguito il provisioning | &#x200B;1. Rivedi la configurazione del set di dati nelle impostazioni di reporting<br/>2. Non aggiungere nuovamente i set di dati già presenti<br/>3. Utilizza elenchi di controllo ufficiali per la migrazione per la generazione di rapporti<br/>4. Rimuovi riferimenti a set di dati duplicati <br/><br/>**Documentazione correlata**: [Report globali](../reports/global-report.md), [Report live](../reports/live-report.md) |

## Approccio generale per la risoluzione dei problemi {#troubleshooting-approach}

Quando incontri un codice di errore, segui questo approccio sistematico:

1. **Identificare l&#39;errore**: annotare il codice di errore completo, lo stato HTTP ed eventuali messaggi o ID di richiesta associati.

2. **Trova il servizio**: utilizza il prefisso del servizio (CJMPTS, CJMRT, CJMMAS, CJMCMP, CJMTL, CJMRPS) per identificare il componente interessato.

3. **Verifica il codice di stato**:
   * **400 (richiesta non valida)**: verifica dati e configurazione di input
   * **403 (non consentito)**: verifica autorizzazioni e diritti di accesso
   * **409 (conflitto)**: cercare risorse duplicate o in conflitto
   * **422 (entità non elaborabile)**: convalida dei dati in base ai requisiti dello schema
   * **500 (errore interno del server)**: riprova ed esegui potenzialmente l&#39;inoltro al supporto

4. **Rivedi modifiche recenti**: considera le modifiche recenti (aggiornamenti di percorso, nuove campagne, modifiche alla configurazione, ecc.).

5. **Consulta la documentazione**: utilizza i collegamenti forniti in questa guida per accedere alla documentazione dettagliata della funzione interessata.

6. **Riprova quando appropriato**: per gli errori della serie 500, un semplice nuovo tentativo dopo pochi minuti spesso risolve problemi transitori.

7. **Inoltra a nuovo quando necessario**: se l&#39;errore persiste dopo i seguenti passaggi di risoluzione, contatta il supporto Adobe con:
   * Codice di errore completo
   * ID richiesta (se disponibile)
   * Passaggi da riprodurre
   * Dettagli di configurazione rilevanti

## Best practice per evitare errori comuni {#best-practices}

### Prima dell&#39;attivazione del percorso {#journey-best-practices}

* **Convalida tutte le risorse**: verifica che tutti i tipi di pubblico, gli eventi, le origini dati e le azioni personalizzate a cui si fa riferimento siano configurati correttamente
* **Verifica approfondita**: utilizza la modalità di test per identificare i problemi prima di pubblicare ([Ulteriori informazioni](testing-the-journey.md))
* **Convalida volumi**: utilizza l&#39;esecuzione in prova per convalidare la portata del pubblico e la logica di diramazione prima della pubblicazione ([Ulteriori informazioni](journey-dry-run.md))
* **Verifica autorizzazioni**: verifica di disporre dei diritti di accesso necessari per tutti i componenti
* **Verifica dipendenze**: verifica che tutti i messaggi e il contenuto collegati siano pubblicati

### Durante la creazione dei messaggi {#message-best-practices}

* **Compilare i campi obbligatori**: compilare sempre tutti i campi obbligatori prima di salvare
* **Includi collegamenti di rinuncia**: aggiungi collegamenti di annullamento iscrizione a tutte le varianti di e-mail ([Ulteriori informazioni](../privacy/opt-out.md))
* **Convalida personalizzazione**: verifica tutti i contenuti dinamici con profili di esempio ([Ulteriori informazioni](../personalization/personalization-build-expressions.md))
* **Mantieni i modelli gestibili**: evita modelli eccessivamente complessi che potrebbero causare problemi di rendering

### Per la gestione delle campagne {#campaign-best-practices}

* **Verifica dati pubblico**: assicurati che i tipi di pubblico di destinazione siano configurati e popolati correttamente
* **Verifica stato approvazione**: comprendi i requisiti di approvazione prima di tentare l&#39;attivazione ([Ulteriori informazioni](../test-approve/gs-approval.md))
* **Configurazioni monitor**: verifica regolarmente la validità delle superfici di canale e dei predefiniti
* **Pianificare le modifiche DNS**: attendi tempo sufficiente per la propagazione DNS durante l&#39;aggiornamento dei domini

## Risorse aggiuntive {#additional-resources}

* [Risoluzione dei problemi del percorso](troubleshooting.md)
* [Risoluzione dei problemi di esecuzione](troubleshooting-execution.md)
* [Risoluzione dei problemi relativi alle attività in entrata](troubleshooting-inbound.md)
* [Risoluzione dei problemi relativi alle azioni personalizzate](../action/troubleshoot-custom-action.md)
* [Domande frequenti sul percorso](journey-faq.md)
* [Guardrail e limitazioni](../start/guardrails.md)

## Ottenere supporto {#getting-support}

Se si verificano errori persistenti che non possono essere risolti utilizzando questa guida:

1. **Raccogli informazioni**: raccogli il codice di errore, l&#39;ID richiesta, i timestamp e i passaggi da riprodurre
2. **Verifica lo stato del sistema**: visita [Stato Adobe](https://status.adobe.com/it){target="_blank"} per problemi noti del servizio
3. **Documentazione di ricerca**: consulta [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=it){target="_blank"} per informazioni sulle soluzioni
4. **Coinvolgi community**: pubblica domande nella [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
5. **Contatta il supporto Adobe**: invia un ticket di supporto con tutti i dettagli pertinenti

>[!NOTE]
>
>Questo riferimento al codice di errore viene continuamente aggiornato man mano che vengono identificati e documentati nuovi codici. Per informazioni aggiornate, controlla regolarmente i [blog della community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs){target="_blank"}.

**Argomenti correlati**

* [Demistificazione dei codici di errore di Adobe Journey Optimizer: Parte 1](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [Demistificazione dei codici di errore di Adobe Journey Optimizer: Parte 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661){target="_blank"}

