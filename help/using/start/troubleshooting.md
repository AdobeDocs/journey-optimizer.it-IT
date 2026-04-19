---
solution: Journey Optimizer
product: journey optimizer
title: Articoli sulla risoluzione dei problemi di Journey Optimizer
description: Articoli sulla risoluzione dei problemi di Journey Optimizer
feature: Get Started, Monitoring
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: 7755e29c4ad07319dadfb3426c8093199b4f843b
workflow-type: tm+mt
source-wordcount: '4652'
ht-degree: 0%

---

# Domande frequenti sulla risoluzione dei problemi {#ajo-troubleshooting}

Di seguito è riportato un elenco di articoli per la risoluzione dei problemi relativi a Adobe Journey Optimizer. Ogni sezione relativa alla risoluzione dei problemi fornisce le risposte alle domande frequenti e alle soluzioni ai problemi.

Quando si contatta il supporto Adobe per i problemi non risolti, includere dettagli sull’ambiente, livello di impatto, passaggi di replica, registri o schermate e ID rilevanti. [Scopri cosa includere nei ticket di supporto](user-interface.md#support-ticket-guidelines).

## Canale e-mail {#ajo-troubleshooting-email}

+++ Come evitare problemi di formattazione delle e-mail in Adobe Journey Optimizer utilizzando i temi?

In Adobe Journey Optimizer (AJO), la modifica dei blocchi CSS predefiniti nell’intestazione e-mail può causare problemi di formattazione imprevisti, soprattutto dopo la rimozione dei frammenti di contenuto. Questi problemi sono più evidenti sui dispositivi mobili e possono causare spostamenti di layout o incoerenze di stile. Per evitare questo problema, utilizza la funzione Temi per applicare CSS personalizzati in modo sicuro senza modificare gli stili CSS generati dal sistema.

Ulteriori informazioni sulla formattazione delle e-mail [ in questa pagina](../email/get-started-email-design.md).

+++


+++ Perché i frammenti con campi modificabili non funzionano?

In Adobe Journey Optimizer, i frammenti con campi modificabili potrebbero non essere caricati correttamente o duplicati in modo imprevisto quando vengono aggiunti ai modelli. Il problema interessa in genere frammenti specifici in ambienti diversi. Per risolvere questo problema, verifica la configurazione del frammento, verifica la presenza di definizioni di campi modificabili in conflitto ed esegui il test in una sandbox di sviluppo prima di ripubblicare.

Ulteriori informazioni sui frammenti personalizzabili [in questa pagina](../content-management/customizable-fragments.md).

+++

+++ Perché i frammenti di HTML non vengono visualizzati correttamente nelle e-mail?

I frammenti di HTML potrebbero non essere visualizzati correttamente nelle e-mail, spesso visualizzati come **ID frammento** anziché come contenuto effettivo. A differenza dei frammenti visivi, i frammenti di HTML richiedono un’attenta configurazione. Per risolvere questo problema, segui le best practice per l&#39;utilizzo di **frammenti di espressione visivi e HTML** nelle campagne e-mail.

Ulteriori informazioni sui frammenti di HTML [in questa pagina](../content-management/fragments.md).

+++

+++ Perché i modelli e i contenuti delle e-mail scompaiono dai percorsi non pubblicati?

Quando si modificano modelli e-mail in un percorso non pubblicato, il contenuto e i modelli di alcuni messaggi e-mail potrebbero scomparire in modo imprevisto. Questo può causare rilavorazione e ritardi. Per ridurre il rischio di questo problema, evita modifiche simultanee, limita il numero di schede aperte e salva le modifiche frequentemente.

Ulteriori informazioni sui modelli [in questa pagina](../email/use-email-templates.md).

+++

+++ Perché il campo Preheader e-mail non viene visualizzato in modalità &quot;Code your own&quot; (Crea il codice)? 

Nella modalità **&#39;Crea codice personalizzato&#39;** nella funzionalità **Modifica corpo e-mail**, il campo di input Preheader non viene visualizzato. Per includere il testo di preintestazione, gli utenti devono **codificare manualmente il preintestazione** all&#39;interno del contenuto HTML personalizzato.

Ulteriori informazioni sulla configurazione del preheader e-mail [in questa pagina](../email/header-parameters.md).

+++

+++ Perché esiste una discrepanza nel comportamento dei collegamenti quando si utilizza un componente HTML nei modelli e-mail?  

Quando si aggiunge un **componente HTML** a un modello di e-mail, i collegamenti possono comportarsi in modo diverso a seconda del **client e-mail**, della **modalità di visualizzazione** o del **dispositivo/browser**. Ad esempio, i collegamenti di ancoraggio possono funzionare in modo diverso in **Outlook affiancato** rispetto alla visualizzazione a schermo intero. Tieni presente queste varianti durante la progettazione di modelli e-mail e il test su più client e dispositivi.

Consulta anche le best practice per la progettazione di e-mail [in questa pagina](../email/get-started-email-design.md).

+++


+++ Come evitare la perdita di collegamenti di tracciamento e-mail nei rapporti?

Il tracciamento dei collegamenti mancanti in Adobe Journey Optimizer si verifica quando gli URL e-mail utilizzano variabili dinamiche e non iniziano con http o quando le istruzioni logiche vengono inserite nel campo URL. Per risolvere questo problema, assicurati che tutti gli URL inizino con http, evita di utilizzare la logica nel campo URL e sposta la logica di personalizzazione complessa nel contenuto di HTML o negli attributi pre-elaborati.

Ulteriori informazioni sul tracciamento delle e-mail [ in questa pagina](../email/message-tracking.md).

+++

+++ Come si risolve un errore di Mail Exchanger durante la configurazione di campagne e-mail transazionali attivate da API? 

Se durante la creazione di una configurazione del canale per una campagna e-mail transazionale attivata da API in Adobe Journey Optimizer si verifica un errore Mail Exchanger (MX), la causa potrebbe essere **Errori di configurazione DNS** o **Limitazioni dei criteri di DMARC**. Per risolvere il problema, verificare che il DNS sia configurato correttamente e che il dominio sia conforme ai requisiti di **autenticazione, reporting e conformità dei messaggi basati sul dominio (DMARC)**.

Ulteriori informazioni sui criteri di DMARC per la posta elettronica [in questa pagina](../configuration/dmarc-record-update.md).

Consulta anche la [documentazione sulle campagne attivate da API](../campaigns/api-triggered-campaigns.md).
+++

## Canale push {#ajo-troubleshooting-push}

+++ Un profilo può avere più token push in Adobe Journey Optimizer?

Quando implementi le notifiche push in Journey Optimizer, un singolo profilo può effettivamente avere più token push associati a dispositivi diversi. Durante una campagna di notifica push, Journey Optimizer è progettato per gestire questi token e garantire che il profilo di destinazione possa essere raggiunto su tutti i dispositivi associati.

Ulteriori informazioni sulla configurazione push [in questa pagina](../push/push-configuration.md).

Consulta anche [flusso di dati di notifica push](../push/push-gs.md) per informazioni sulla registrazione e la gestione end-to-end dei token.

+++

+++ Perché quando fai clic su un messaggio push non mi reindirizza all’URL web configurato?  

Se i messaggi push non vengono reindirizzati all’URL web desiderato, la causa potrebbe essere una configurazione non corretta dell’azione di clic o impostazioni disabilitate della notifica push. Per risolvere il problema, verifica che l&#39;**azione clic** per il messaggio push sia impostata correttamente e che **siano abilitati la visualizzazione e il tracciamento automatici** delle notifiche push.

Ulteriori informazioni sulla configurazione push [in questa pagina](../push/push-configuration.md).

+++

+++ Perché le notifiche push non riescono dopo l’aggiornamento delle credenziali dell’app?

Le credenziali push scadute o non configurate correttamente, ad esempio un certificato APNs per iOS o una chiave FCM per Android, causano errori di consegna in modo invisibile all’utente. Journey Optimizer non può inviare notifiche se le credenziali memorizzate nella configurazione del canale push non corrispondono più a quelle registrate con la piattaforma del dispositivo. Aggiorna le credenziali nella configurazione del canale push e verifica che la superficie dell’app mobile associata sia ripubblicata.

Scopri come configurare le credenziali push [in questa pagina](../push/push-gs.md).

Consulta anche la [documentazione sulla configurazione del canale push](../push/push-configuration.md).

+++


## Canale SMS {#ajo-troubleshooting-sms}

+++ Perché il mio SMS transazionale non viene consegnato anche se il consenso è impostato su `marketing.sms.value=y`?

Se un destinatario risponde **STOP** a un SMS, tutti i messaggi futuri provenienti da tale numero breve vengono bloccati, inclusi i messaggi transazionali. Per garantire il recapito ininterrotto degli SMS transazionali, configurali e inviali tramite un **numero breve separato** da cui i destinatari non hanno precedentemente rinunciato.

Ulteriori informazioni sulla configurazione della rinuncia SMS [in questa pagina](../sms/sms-opt-out.md).

+++

+++ Perché la consegna di SMS non riesce anche se il canale è configurato?

Gli errori di consegna SMS dopo la configurazione del canale sono solitamente causati da credenziali API del provider errate, una mancata corrispondenza tra l’ID mittente e ciò che il provider ha registrato o restrizioni di indirizzamento a livello di provider. Verifica che la chiave API, la password e i dettagli del mittente immessi in Journey Optimizer corrispondano esattamente a quelli forniti dal provider SMS. Quindi invia un messaggio di prova per confermare la connettività prima di avviare una campagna.

Scopri come configurare il provider SMS [in questa pagina](../sms/sms-configuration.md).

+++

+++ Come posso verificare che un profilo abbia rinunciato alle comunicazioni SMS?

Quando un profilo invia un SMS STOP (INTERROMPI), Journey Optimizer aggiorna l’attributo di consenso SMS del profilo. Per verificare lo stato di rinuncia corrente, apri il profilo nell&#39;interfaccia utente di Experience Platform e controlla i campi di consenso in **Privacy** > **Consensi**. Per la risoluzione dei problemi relativi alla campagna, controlla anche i motivi di esclusione nel rapporto della campagna. I profili di rinuncia vengono visualizzati nel conteggio **Esclusi** con il motivo &quot;Rinuncia&quot;.

Ulteriori informazioni sulla gestione della rinuncia agli SMS [in questa pagina](../sms/sms-opt-out.md).

+++

## Canale in-app {#ajo-troubleshooting-inapp}

+++ Perché non posso creare rapporti sul canale in-app in Customer Journey Analytics?

Le difficoltà di generazione rapporti sul **canale in-app** in Adobe Customer Journey Analytics spesso derivano da **visualizzazioni dati**, **set di dati** o **aggiornamenti schema** non configurati correttamente. Assicurati che queste configurazioni siano applicate correttamente per risolvere il problema.

Consulta anche la [documentazione di Journey Optimizer All-Time Reports](../reports/report-gs-cja.md).

+++

+++ Perché il mio messaggio in-app non viene visualizzato agli utenti?

I messaggi in-app richiedono la corretta installazione di Adobe Experience Platform Mobile SDK e la registrazione dell’estensione Messaging nell’app. Se il messaggio non viene visualizzato, verifica che SDK sia inizializzato prima che l&#39;app tenti di recuperare i messaggi in-app, che la superficie corretta dell&#39;app (ID bundle) sia configurata in Journey Optimizer e che la campagna sia nello stato **Live**. Inoltre, verifica che il profilo soddisfi i criteri di pubblico e non sia già stato limitato da una regola di frequenza.

Scopri come configurare il canale in-app [in questa pagina](../in-app/inapp-configuration.md).

+++

+++ Perché la mia campagna in-app non viene attivata sull’evento previsto?

Le campagne in-app si attivano in base ai nomi degli eventi che devono corrispondere esattamente tra l’implementazione SDK dell’app e la condizione di attivazione definita in Journey Optimizer. Una mancata corrispondenza nella struttura del payload per maiuscole, ortografia o evento impedirà l’attivazione del trigger. Utilizza lo strumento Adobe Experience Platform Assurance per ispezionare gli eventi live di SDK e confrontarli con la configurazione del trigger della tua campagna.

Scopri come creare e configurare un messaggio in-app [in questa pagina](../in-app/create-in-app.md).

+++


## Schede contenuto {#ajo-troubleshooting-content-cards}

+++ Perché le schede di contenuto non vengono visualizzate nell’app?

Le schede di contenuto richiedono l&#39;installazione, la registrazione e la configurazione nell&#39;app di Adobe Experience Platform Mobile SDK e di **Messaging SDK**. A differenza dei messaggi push o in-app, le schede di contenuto non vengono sottoposte a rendering automaticamente. L’app deve chiamare esplicitamente le API SDK di messaggistica per recuperare le schede disponibili e quindi eseguirne il rendering nell’interfaccia utente. Se le schede non vengono visualizzate, utilizza **Adobe Experience Platform Assurance** per verificare che le richieste di decisione vengano eseguite quando viene attivato l&#39;evento di destinazione e che le risposte vengano restituite da Edge Network.

Scopri come configurare il supporto per le schede di contenuto nel SDK mobile [in questa pagina](../content-card/content-card-configuration-sdk.md).

+++

+++ Le schede di contenuto richiedono all’utente di concedere le autorizzazioni per le notifiche push?

No. Le schede di contenuto sono silenziose e persistenti: non si basano su autorizzazioni push a livello di sistema operativo e non sono influenzate dallo stato di consenso alla notifica di un utente. Questo li rende un canale di fallback utile per raggiungere gli utenti che hanno disabilitato le notifiche push. Le schede vengono recuperate da Edge Network durante la sessione dell’utente e visualizzate nell’interfaccia utente dell’app.

Ulteriori informazioni sul canale della scheda di contenuto [in questa pagina](../content-card/get-started-content-card.md).

+++

+++ Perché le impression della scheda dei contenuti non vengono visualizzate nei rapporti della campagna?

Le impression e le interazioni delle schede di contenuto (clic, chiusure) non vengono tracciate automaticamente. L’app deve inviare esplicitamente gli eventi di tracciamento ad Adobe tramite Messaging SDK dopo il rendering di una scheda e dopo ogni interazione dell’utente con essa. Se queste chiamate di tracciamento non sono presenti nell’implementazione, i rapporti mostreranno zero impression anche quando le schede vengono servite correttamente. Prima di analizzare la configurazione della campagna, verifica che le chiamate di tracciamento vengano attivate in **Assurance**.

Scopri come accedere ai report della scheda dei contenuti [in questa pagina](../content-card/content-card-report.md).

Vedi anche la [configurazione SDK della scheda di contenuto](../content-card/content-card-configuration-sdk.md) per le chiamate di tracciamento richieste.

+++

## WhatsApp {#ajo-troubleshooting-whatsapp}

+++ Perché i miei messaggi WhatsApp non vengono inviati?

La consegna dei messaggi WhatsApp richiede che siano soddisfatte due condizioni: il destinatario deve aver acconsentito esplicitamente a ricevere comunicazioni WhatsApp dal tuo marchio e il messaggio deve utilizzare un **modello di messaggio preapprovato** registrato con l&#39;API aziendale WhatsApp. Se una delle due condizioni non viene soddisfatta, il messaggio verrà bloccato automaticamente dalla piattaforma WhatsApp prima della consegna. Verifica lo stato di consenso esplicito negli attributi di consenso del profilo del destinatario e conferma che il modello sia nello stato **Approvato** nell&#39;account WhatsApp Business.

Scopri come configurare il canale WhatsApp [in questa pagina](../whatsapp/whatsapp-configuration.md).

+++

+++ Perché il mio messaggio WhatsApp viene rifiutato con un errore di modello?

L’API aziendale WhatsApp consente solo modelli di messaggio preapprovati per i messaggi in uscita avviati dall’azienda. I messaggi in formato libero sono consentiti solo entro una finestra del servizio clienti di **24 ore**, ovvero entro 24 ore dall&#39;invio di un messaggio al brand. Se il messaggio viene rifiutato, verifica che il modello sia stato inviato e approvato da Meta, che le variabili di modello (segnaposto) nel messaggio di Journey Optimizer corrispondano esattamente alla struttura del modello approvata e che il modello corretto sia selezionato nell’azione della campagna o del percorso.

Scopri come creare messaggi WhatsApp [su questa pagina](../whatsapp/create-whatsapp.md).

+++

+++ Come posso raccogliere e verificare il consenso WhatsApp da parte degli utenti?

WhatsApp richiede il consenso esplicito prima di poter inviare messaggi di marketing. Il consenso può essere raccolto tramite qualsiasi canale controllato dal brand, ad esempio un modulo web, un SMS con doppio consenso o una schermata di consenso in-app, purché il processo sia chiaro e documentato. Una volta raccolto, aggiorna l’attributo di consenso WhatsApp del profilo in Adobe Experience Platform. Per verificare lo stato del consenso corrente per un profilo, apri il profilo nell&#39;interfaccia utente di Experience Platform e controlla la sezione **Consensi**. L’invio a profili senza consenso valido viola i criteri aziendali WhatsApp e può causare la sospensione dell’account.

Scopri come iniziare a utilizzare il canale WhatsApp [ in questa pagina](../whatsapp/get-started-whatsapp.md).

+++

## Gestione dati {#ajo-troubleshooting-data-management}

+++ Come si applicano le impostazioni Time-to-Live (TTL) ai set di dati Profilo e Data Lake quando crei una nuova sandbox?

Le organizzazioni che eseguono il provisioning di nuove sandbox in Adobe Journey Optimizer hanno sollevato domande su come le impostazioni TTL (Time-to-Live) si applicano ai set di dati profilo e data lake. Le impostazioni TTL non influiscono sulle sandbox esistenti e vengono applicate automaticamente solo a quelle con provisioning recente.

Ulteriori informazioni sul set di dati Time-to-live [ in questa pagina](../data/datasets-ttl.md).

+++

+++ Perché non viene abilitato un set di dati per Real-time Customer Profile?

Affinché un set di dati possa alimentare la personalizzazione basata su profili e le condizioni di percorso in Journey Optimizer, è necessario soddisfare entrambi due requisiti: lo schema XDM sottostante deve avere **Profilo** abilitato e il set di dati stesso deve essere attivato per **Profilo cliente in tempo reale** nell&#39;interfaccia utente di Experience Platform. Se manca una delle due, i dati verranno acquisiti nel Data Lake ma non verranno uniti in profili unificati. Inoltre, assicurati che il set di dati contenga almeno un campo di identità mappato a uno spazio dei nomi riconosciuto.

Scopri come configurare i set di dati [ in questa pagina](../data/get-started-datasets.md).

Per l&#39;elenco di controllo dell&#39;installazione completa, vedere anche la [panoramica sulla gestione dei dati](../data/gs-data.md).

+++

+++ Come posso monitorare e risolvere gli errori di acquisizione dei dati?

Gli errori di acquisizione vengono visualizzati nel dashboard **Monitoraggio** di Adobe Experience Platform in **Origini** > **Flussi dati**. Le cause comuni includono errori di convalida dello schema (un campo nei dati di origine non corrisponde allo schema XDM), campi di identità richiesti mancanti o payload JSON non validi. Aprire il record batch non riuscito per visualizzare il codice di errore specifico e le righe interessate. Correggi i dati di origine e riacquisisci, oppure regola la mappatura dello schema se il formato di origine è stato modificato.

Ulteriori informazioni sugli schemi e sulla configurazione dei dati [in questa pagina](../data/gs-data.md).

+++


## Gestione di profili e pubblico {#ajo-troubleshooting-audiences}

+++ Come risolvere le discrepanze di conteggio del pubblico?

Il numero di voci elaborate nella funzionalità **Read Audience** di Adobe Journey Optimizer può essere inferiore al conteggio del pubblico previsto. Questo problema si verifica spesso a causa di configurazioni errate dello spazio dei nomi, che determinano l’esclusione dei profili dai percorsi. La risoluzione prevede il controllo e la correzione delle configurazioni dello spazio dei nomi, l’esame della documentazione pertinente e l’adeguamento delle priorità per garantire operazioni più fluide in Adobe Journey Optimizer.

Ulteriori informazioni sull&#39;attività **Read Audience** nei percorsi [in questa pagina](../building-journeys/read-audience.md).

+++

+++ Perché gli aggiornamenti del profilo non riescono?

In Adobe Journey Optimizer, alcuni valori di campo potrebbero non essere aggiornati correttamente dopo l&#39;esecuzione di un&#39;attività **Aggiorna profilo** in un percorso. In alcuni casi, i campi aggiornati possono scomparire o tornare allo stato precedente. Per risolvere questo problema, verificare la presenza di regole o condizioni in conflitto, esaminare le impostazioni delle autorizzazioni, utilizzare un set di dati univoco per l&#39;attività **Aggiorna profilo** e assicurarsi che nessun altro processo di acquisizione stia scrivendo contemporaneamente sullo stesso profilo.

Ulteriori informazioni sull&#39;attività **Aggiorna profilo** nei percorsi [in questa pagina](../building-journeys/update-profiles.md).

+++

+++ Perché c’è una mancata corrispondenza nel conteggio dei profili che entrano in un percorso rispetto al pubblico associato?

La discrepanza può verificarsi quando il percorso utilizza uno snapshot del profilo del giorno precedente se lo snapshot del giorno corrente non è disponibile al momento dell&#39;esecuzione del percorso. Per eseguire un’indagine, controlla quando è stato eseguito l’ultimo processo di segmentazione giornaliero e se il percorso è stato attivato prima che l’istantanea fosse pronta.

Ulteriori informazioni sull&#39;attività **Read Audience** e sul comportamento di pianificazione [in questa pagina](../building-journeys/read-audience.md).

+++

+++ Perché il selettore del pubblico mostra conteggi di profili diversi in Campagne rispetto a Percorsi?

Potresti notare che lo stesso pubblico mostra conteggi di profili diversi quando viene visualizzato in Campagne rispetto ai Percorsi. Questo accade perché ogni funzione utilizza API diverse per recuperare i dati sul pubblico, che possono restituire valori diversi.

Si tratta di un comportamento previsto che non influisce sull’esecuzione della campagna; i profili corretti saranno comunque oggetto di targeting. Per verificare la dimensione effettiva del pubblico, vai a **[!UICONTROL Cliente]** > **[!UICONTROL Tipi di pubblico]** e seleziona il tuo pubblico.

+++


+++ Come si risolvono i problemi di popolazione del pubblico?

I problemi di popolazione del pubblico possono verificarsi quando mancano componenti o risorse, spesso a causa di configurazioni errate di adesione, provisioning o autorizzazioni. Per risolvere questi problemi, inizia verificando i diritti, assicurando il provisioning corretto e rivedendo le autorizzazioni. Se il problema persiste, inoltra il caso e coordinati con i team di supporto per una risoluzione completa.

Ulteriori informazioni sulla gestione dei tipi di pubblico [in questa pagina](../audience/about-audiences.md).

+++

+++ Perché il conteggio dei profili coinvolgibili è aumentato in modo significativo in un breve periodo? 

La metrica **Profili coinvolgibili** riflette il numero di profili univoci coinvolti da percorsi o campagne negli ultimi 12 mesi. Un aumento improvviso può derivare da percorsi o campagne rivolti a tipi di pubblico di grandi dimensioni che non sono stati coinvolti di recente, oppure da modifiche nei set di dati abilitati per il servizio Profilo.

Per indagare e risolvere questo problema, è necessario comprendere la logica di conteggio dei profili, analizzare percorsi e campagne indirizzati a tipi di pubblico di grandi dimensioni, filtrare i tipi di pubblico in modo appropriato, monitorare le modifiche ai set di dati e, potenzialmente, ridurre le dimensioni del pubblico indirizzabile.

Scopri come risolvere i problemi relativi agli aumenti dei profili Engageable e monitorare l&#39;utilizzo delle licenze da parte della tua organizzazione nella [documentazione del dashboard Utilizzo licenze](../audience/license-usage.md#troubleshooting-engageable-profiles).

+++

+++ Perché le e-mail vengono inviate a persone esterne al pubblico previsto in base a funzioni data?

Le e-mail possono essere inviate a destinatari che **non soddisfano i criteri di pubblico specificati**. Ad esempio, i membri con date di rimborso **precedenti al 4 luglio 2025** possono ricevere e-mail destinate solo a coloro che sono successivi a tale data. Questo comportamento può essere dovuto a **segmentazione del pubblico non configurata correttamente** o a **modifiche impreviste nella logica di qualifica del profilo**. Rivedi la definizione del pubblico e testa con profili di esempio per verificare che la logica della data sia applicata correttamente.

Ulteriori informazioni sulle funzioni data [in questa pagina](../building-journeys/functions/date-functions.md).

+++

+++ Perché le consegne + esclusioni superano le dimensioni del pubblico target nei rapporti delle campagne?

Nei rapporti delle campagne, potresti notare che la somma di **Delivered** e **Exclusions** supera la dimensione del pubblico di destinazione originale. Ciò si verifica perché la metrica **Esclusioni** conta tutti gli eventi di esclusione, compresi gli eventi di esclusione duplicati per lo stesso profilo. Se un profilo viene escluso più volte durante una campagna, ogni evento viene conteggiato separatamente.

**Esempio**: una campagna con targeting di 94.000 profili mostra 69.000 invii e 37.000 esclusioni, per un totale di 106.000, che supera i 94.000 profili di destinazione originali. Questo è il comportamento previsto.

Per comprendere la differenza tra eventi di esclusione totali ed esclusioni di profilo univoche, consulta la [spiegazione del conteggio delle esclusioni](../reports/exclusion-list.md#exclusion-list).

Ulteriori informazioni sui [report campagna](../reports/campaign-global-report-cja.md) e sulle [metriche report](../reports/global-report-components-cja.md).

+++

+++ Come posso risolvere i problemi di selezione del pubblico e gli errori di Chrome durante il salvataggio dei percorsi?

L&#39;aggiunta di tipi di pubblico alle condizioni del percorso può talvolta causare **arresti anomali dell&#39;applicazione** o la visualizzazione di un **errore Aw Snap** in Chrome, inclusi errori durante il salvataggio dei percorsi. Questi problemi sono spesso correlati ai **servizi Chromium**. Per risolverli, applica un **aggiornamento del browser**, cancella la cache del browser o prova un&#39;altra sessione del browser.

Ulteriori informazioni sulla [navigazione nell&#39;interfaccia di Journey Optimizer](user-interface.md).

+++

## Percorsi {#ajo-troubleshooting-journeys}

Per Percorsi, consulta le seguenti sezioni per la risoluzione dei problemi:

* [Risolvere i problemi prima di testare il percorso](../building-journeys/troubleshooting.md)
* [Risoluzione dei problemi relativi alle azioni in entrata nei percorsi](../building-journeys/troubleshooting-inbound.md)
* [Risolvere i problemi relativi all&#39;esecuzione di Live percorsi](../building-journeys/troubleshooting-execution.md)
* [Risolvere i problemi relativi alle azioni personalizzate](../action/troubleshoot-custom-action.md)


+++ Perché le espressioni vengono perse durante la creazione di una nuova versione del percorso?  

Durante la creazione di una nuova versione di un percorso, **le espressioni nei passaggi specifici** potrebbero andare perse, causando errori e richiedendo il reinserimento manuale. Per risolvere il problema, **duplica il percorso**, verifica la riproducibilità, **evita ricariche del browser** e utilizza l&#39;**area di lavoro aggiornata** per i percorsi precedenti.

Scopri come duplicare un percorso [in questa pagina](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Perché i profili escono anticipatamente dai percorsi? 

I profili possono uscire da un percorso in modo imprevisto senza passare da un nodo designato quando lo stato di **verifica delle condizioni** dei messaggi inviati non è configurato correttamente. Per risolvere il problema, controlla la **logica della condizione**, implementa **logica alternativa** oppure rivolgiti al tuo **team di implementazione**.

Consulta anche [Linee guida per la progettazione dei Percorsi](../building-journeys/using-the-journey-designer.md).

+++


+++ Perché i profili stanno uscendo dai percorsi in modo imprevisto?

I profili possono uscire da un percorso in modo imprevisto quando si verifica il limite **evento**, causando l&#39;eliminazione di alcuni profili se il numero di eventi elaborati supera la capacità del sistema. Per ridurre le uscite di profilo, individua i **limiti di sistema**, monitora i **picchi di eventi** e ottimizza il **flusso di dati** per evitare il superamento delle soglie.

Vedi anche [guardrail di Percorso](../start/guardrails.md#decisioning-guardrails).

+++


+++ Perché il mio evento non attiva il percorso previsto?  

Gli eventi potrebbero non riuscire ad attivare un percorso anche se tutti i criteri sono soddisfatti quando vengono **creati tramite i servizi di query** anziché essere inviati in streaming al **Servizio di base raccolta dati (DCCS)**. Per risolvere questo problema, controlla la configurazione dell&#39;evento, assicurati che gli eventi siano **inviati direttamente in streaming a DCCS** e verifica la funzionalità utilizzando la **modalità di test**.

Ulteriori informazioni sugli eventi [in questa pagina](../event/about-events.md).

Vedi anche [Guardrail evento Percorso](../start/guardrails.md#events-g).

+++


+++ Come posso risolvere i problemi di attivazione del percorso dopo le modifiche del pubblico in Adobe Journey Optimizer? 

Se un percorso smette di attivarsi dopo aver apportato modifiche al pubblico associato, ad esempio modifiche al criterio di unione, si potrebbero verificare flussi interrotti. Per risolvere il problema, **duplica e ripubblica il percorso** con le impostazioni aggiornate per il pubblico, in modo che i trigger funzionino correttamente.

Scopri come duplicare un percorso [in questa pagina](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Perché un’azione personalizzata che chiama un endpoint esterno di terze parti riceve un timeout?

Gli errori di timeout possono verificarsi quando un&#39;azione personalizzata **** chiama un endpoint esterno di terze parti. Per risolvere il problema, verifica che l&#39;endpoint **sia accessibile**, controlla **i registri del server**, assicurati che **non vi sia alcun blocco da Adobe**, aggiorna le configurazioni dell&#39;endpoint in base alle esigenze e **verifica dopo gli aggiornamenti**. Inoltre, ricorda le **specifiche di timeout della chiamata API**.

Ulteriori informazioni sull&#39;API di limitazione del Percorso [in questa pagina](../configuration/throttling.md).

Consulta anche la [documentazione sull&#39;integrazione con sistemi esterni](../configuration/external-systems.md).

+++

+++ Quali operazioni è necessario eseguire se si verifica un errore 403 con il messaggio **invalid_access** o **Nessun accesso a questo dataId=XX concesso** durante la pubblicazione di un pubblico da un percorso?

Per risolvere questo errore, chiedi all’amministratore di verificare che il tuo profilo utente abbia accesso alle visualizzazioni dati richieste per la pubblicazione di tipi di pubblico, quindi prova di nuovo a pubblicare il pubblico.

Consulta [la documentazione sulle autorizzazioni](../administration/permissions.md) per scoprire i passaggi per risolvere il problema.

+++

## Regole {#ajo-troubleshooting-rules}

+++ Perché il menu a discesa Regole di limitazione non funziona?

I problemi relativi al menu a discesa **Regole di limitazione** si verificano spesso quando i set di regole sono **non configurati correttamente** o **inaccessibili**. Assicurati che tutti i set di regole siano configurati e disponibili correttamente per risolvere il problema.

Scopri come applicare le regole di limitazione di utilizzo [ in questa sezione](../conflict-prioritization/rule-sets.md).

+++

+++ Perché una regola di quota limite non viene applicata alla campagna o al percorso?

Le regole di quota limite hanno effetto solo quando il set di regole è esplicitamente associato alla campagna o al percorso. Se il limite non funziona, verifica che il set di regole corretto sia selezionato nelle impostazioni della campagna o del percorso, che il tipo di canale della regola corrisponda al canale utilizzato e che la regola sia nello stato **Attivo**. Controlla anche se il profilo ha già raggiunto il limite in un’esecuzione precedente, impedendo ulteriori messaggi anche se la regola appare configurata correttamente.

Scopri come configurare le regole di limitazione dei canali [ in questa pagina](../conflict-prioritization/channel-capping.md).

+++

+++ Come si configurano le ore non interattive per impedire l’invio dei messaggi di notte?

Le ore non interattive sono regole di esclusione basate sul tempo configurate in un **set di regole di canale**. Definisci la finestra di sospensione attività (ad esempio, dalle 22:00 alle 8:00) e applica il set di regole alle campagne o ai percorsi pertinenti. Quando è pianificato l’invio di un messaggio nelle ore non interattive, Journey Optimizer lo conserva fino alla successiva finestra consentita o lo elimina, a seconda della configurazione della regola.

Scopri come impostare le ore non interattive [ in questa pagina](../conflict-prioritization/quiet-hours.md).

+++

## Funzione Decisioni {#ajo-troubleshooting-decisioning}

+++ Come posso risolvere i problemi durante la creazione delle raccolte di offerte?

Le difficoltà nella creazione delle raccolte di offerte spesso si verificano quando **non è stato eseguito il provisioning dei cataloghi** per la tua organizzazione. Per risolvere questo problema, verifica che sia stato eseguito correttamente il provisioning di tutti i cataloghi richiesti prima di tentare di creare le raccolte di offerte.

Ulteriori informazioni sulle raccolte di offerte [in questa pagina](../offers/offer-library/creating-collections.md).

+++

+++ Perché non riesco ad accedere ad Offer Decisioning?  

Durante l&#39;integrazione di Adobe Target in un&#39;applicazione tramite Adobe Journey Optimizer, l&#39;opzione **Offer Decisioning** potrebbe non essere accessibile nella configurazione dello stream di dati. Ciò si verifica in genere a causa di **impostazioni delle autorizzazioni** o **vincoli di provisioning**. Per risolvere il problema, verifica le autorizzazioni utente e assicurati che sia attivo il provisioning necessario.

Ulteriori informazioni sulle autorizzazioni richieste per Offer Decisioning [in questa pagina](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++

+++ Perché un’offerta non viene restituita anche se soddisfa i criteri di idoneità?

Se un&#39;offerta idonea non appare in una risposta decisionale, verifica quanto segue nell&#39;ordine: verifica che l&#39;offerta sia nello stato **Approvata** (non Bozza); conferma che l&#39;ID posizionamento nella richiesta corrisponda alla superficie di rappresentazione dell&#39;offerta; verifica che sia stato raggiunto il limite di limitazione (totale o per profilo) per tale offerta e assicurati che la raccolta e l&#39;ambito decisionale siano configurati correttamente. Utilizza lo strumento **Simulazione** in Experience Decisioning per testare le risposte delle offerte rispetto a un profilo specifico senza inviare traffico in tempo reale.

Scopri come iniziare a utilizzare Experience Decisioning [in questa pagina](../experience-decisioning/gs-experience-decisioning.md).

+++


## Multilingue {#ajo-troubleshooting-multilingual}

+++ Come risolvere il problema `Message validation error (CJMMAS - 1069-500)`?

In Adobe Journey Optimizer, un errore di convalida del messaggio (CJMMAS - 1069-500) collegato alla funzione multilingue impedisce che i percorsi vengano impostati sulla modalità di test o pubblicati. Prima di tentare la pubblicazione, verificare che tutto il contenuto delle impostazioni internazionali sia completo, che la lingua principale sia impostata correttamente e che nessun campo di traduzione richiesto sia vuoto.

Ulteriori informazioni sul contenuto multilingue [in questa pagina](../content-management/multilingual-gs.md).

+++

+++ Perché il provider di traduzione non si connette in Journey Optimizer?

Gli errori di connessione del provider di traduzione sono in genere causati da credenziali API errate o da una configurazione del provider mancante nelle impostazioni multilingue. Verifica che la chiave API, l’URL dell’endpoint e tutti i token di autenticazione richiesti immessi in Journey Optimizer corrispondano esattamente a ciò che è stato fornito dal fornitore di traduzione. Se le credenziali sono corrette, verificare se l&#39;account del provider dispone di una quota sufficiente o dello stato di sottoscrizione attivo, quindi salvare e verificare nuovamente la connessione.

Scopri come configurare un provider di traduzione [in questa pagina](../content-management/multilingual-provider.md).

+++

+++ Cosa succede quando manca una traduzione per una lingua?

Se non è stata fornita una traduzione per una lingua specifica, Journey Optimizer utilizza come fallback il contenuto definito nella **lingua primaria** (lingua di fallback) configurata nelle impostazioni della lingua. Se non è configurato alcun fallback, il messaggio potrebbe risultare vuoto o non essere convalidato prima dell’invio. Per evitare questo problema, definisci sempre una lingua di fallback nelle impostazioni multilingue del progetto e verifica che tutte le lingue abbiano approvato le traduzioni prima di attivare la campagna o il percorso.

Ulteriori informazioni sulla configurazione del contenuto multilingue [in questa pagina](../content-management/multilingual-gs.md).

+++


## Configurazione {#ajo-troubleshooting-config}

+++ Come si abilita TLS v1.3 per le azioni personalizzate?  

Per mantenere l&#39;integrità e la sicurezza dei dati di **1} durante la connessione a sistemi di terze parti, assicurati che Transport Layer Security (** TLS **) v1.3 sia abilitato per le azioni personalizzate.** Questo aiuta a proteggere le comunicazioni e previene potenziali vulnerabilità di sicurezza.

Ulteriori informazioni sulla configurazione delle azioni personalizzate [in questa pagina](../action/about-custom-action-configuration.md).

+++

+++ Perché non è possibile creare un dashboard direttamente da una query in Adobe Journey Optimizer? 

In Adobe Journey Optimizer non è possibile creare dashboard direttamente dalle query. Per creare dashboard, utilizza le **funzionalità di creazione dashboard** disponibili in Adobe Experience Platform, che consentono di visualizzare e analizzare i dati delle query in modo efficace.

Ulteriori informazioni sulle query in Journey Optimizer [in questa pagina](../data/get-started-queries.md).

+++

+++ Perché i miei messaggi vengono bloccati dall’elenco di soppressione?

Gli indirizzi vengono aggiunti automaticamente all’elenco di soppressione dopo mancati recapiti permanenti, segnalazioni di posta indesiderata o aggiunte manuali da parte di un amministratore. Una volta eliminato, un profilo non riceverà alcun messaggio da quel canale, indipendentemente dal targeting della campagna o del percorso. Per approfondire, apri **Amministrazione** > **Canali** > **Elenco di soppressione** e cerca l&#39;indirizzo. Se la soppressione è stata aggiunta per errore, può essere rimossa direttamente dall’interfaccia. Per le eliminazioni definitive, controlla anche il problema di recapito sottostante prima di rimuovere l’indirizzo.

Scopri come gestire l’elenco di soppressione [ in questa pagina](../configuration/manage-suppression-list.md).

+++

## API {#ajo-troubleshooting-apis}

+++ Come posso risolvere i problemi di accesso con l’API di Query Service?  

Gli errori di accesso quando si utilizza l&#39;API **Query Service API** tramite Postman o strumenti simili sono in genere causati da **autorizzazioni insufficienti**. Per risolvere questo problema, verifica le autorizzazioni utente, confronta le credenziali API con i ruoli configurati nella tua organizzazione e fornisci informazioni dettagliate da supportare, se necessario.

Ulteriori informazioni sulle autorizzazioni in Journey Optimizer [in questa pagina](../administration/permissions.md).

+++

+++ Come posso risolvere gli errori 429 Too Many Requests (Troppe richieste 429) quando richiamo le API di Journey Optimizer?

Una risposta 429 indica che l’integrazione ha superato il limite di velocità API per l’endpoint. Ogni API di Journey Optimizer ha definito le soglie di velocità effettiva. Per risolvere questo problema, implementa la logica **backoff esponenziale** nell&#39;integrazione: attendi la durata specificata nell&#39;intestazione di risposta `Retry-After` prima di riprovare. Per casi di utilizzo di volumi elevati e prolungati, controlla la configurazione della limitazione e del limite per le azioni personalizzate e le origini dati per allineare le percentuali di chiamate API ai limiti del sistema.

Ulteriori informazioni sulla limitazione di Journey Optimizer [in questa pagina](../configuration/throttling.md).

Consulta anche la [documentazione sull&#39;integrazione dei sistemi esterni](../configuration/external-systems.md).

+++

+++ Perché la mia campagna attivata da API non viene eseguita dopo la chiamata API?

Se una campagna attivata da API non è in esecuzione, verificare quanto segue: la campagna è nello stato **Live** (non bozza o interrotta); la chiamata API include l&#39;ID campagna corretto nel percorso dell&#39;endpoint; il payload della richiesta corrisponde allo schema dell&#39;identificatore del profilo previsto dalla campagna; le credenziali API utilizzate dispongono dell&#39;autorizzazione **Gestisci campagne**. Controlla i registri di esecuzione della campagna nel dashboard di reporting per identificare se il profilo è stato ricevuto ma escluso o se la chiamata non ha raggiunto la campagna.

Ulteriori informazioni sulle campagne attivate da API [in questa pagina](../campaigns/api-triggered-campaigns.md).

+++
