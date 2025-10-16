---
solution: Journey Optimizer
product: journey optimizer
title: Risoluzione dei problemi di Journey Optimizer
description: Domande sulla risoluzione dei problemi di Journey Optimizer
feature: Get Started
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: 6c73a1ee024ca61b30d71e77268e51b93576ae62
workflow-type: tm+mt
source-wordcount: '2746'
ht-degree: 2%

---

# Risoluzione dei problemi {#ajo-troubleshooting}

Di seguito è riportato un elenco di articoli per la risoluzione dei problemi relativi a Adobe Journey Optimizer. Ogni sezione relativa alla risoluzione dei problemi fornisce le risposte alle domande frequenti e alle soluzioni ai problemi.

Consulta anche le [Domande frequenti su Adobe Experience Platform e la documentazione sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-platform/landing/troubleshooting){target="_blank"}.

## Canale e-mail {#ajo-troubleshooting-email}

+++ Come evitare problemi di formattazione delle e-mail in Adobe Journey Optimizer utilizzando i temi?

In Adobe Journey Optimizer (AJO), la modifica dei blocchi CSS predefiniti nell’intestazione e-mail può causare problemi di formattazione imprevisti, soprattutto dopo la rimozione dei frammenti di contenuto. Questi problemi sono più evidenti sui dispositivi mobili e possono causare spostamenti di layout o incoerenze di stile. Per evitare questo problema, utilizza la funzione Temi per applicare CSS personalizzati in modo sicuro senza modificare gli stili CSS generati dal sistema.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"}.

Ulteriori informazioni sulla formattazione delle e-mail [&#x200B; in questa pagina](../email/get-started-email-design.md).

+++


+++ Perché i frammenti con campi modificabili non funzionano?

In Adobe Journey Optimizer, i frammenti con campi modificabili potrebbero non essere caricati correttamente o duplicati in modo imprevisto quando vengono aggiunti ai modelli. Il problema interessa in genere frammenti specifici in ambienti diversi.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"}.

Ulteriori informazioni sui frammenti personalizzabili [in questa pagina](../content-management/customizable-fragments.md).

+++

+++ Perché i frammenti di HTML non vengono visualizzati correttamente nelle e-mail?

I frammenti di HTML potrebbero non essere visualizzati correttamente nelle e-mail, spesso visualizzati come **ID frammento** anziché come contenuto effettivo. A differenza dei frammenti visivi, i frammenti di HTML richiedono un’attenta configurazione. Per risolvere questo problema, segui le best practice per l&#39;utilizzo di **frammenti di espressione visivi e HTML** nelle campagne e-mail.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"}.

Ulteriori informazioni sui frammenti di HTML [in questa pagina](../content-management/fragments.md).

+++

+++ Perché i modelli e i contenuti delle e-mail scompaiono dai percorsi non pubblicati?

Quando si modificano modelli e-mail in un percorso non pubblicato, il contenuto e i modelli di alcuni messaggi e-mail potrebbero scomparire in modo imprevisto. Questo può causare rilavorazione e ritardi. Per ridurre il rischio di questo problema, evita modifiche simultanee, limita il numero di schede aperte e salva le modifiche frequentemente.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}.

Ulteriori informazioni sui modelli [in questa pagina](../email/use-email-templates.md).

+++

+++ Perché il campo Preheader e-mail non viene visualizzato in modalità &quot;Code your own&quot; (Crea il codice)? 

Nella modalità **&#39;Crea codice personalizzato&#39;** nella funzionalità **Modifica corpo e-mail**, il campo di input Preheader non viene visualizzato. Per includere il testo di preintestazione, gli utenti devono **codificare manualmente il preintestazione** all&#39;interno del contenuto HTML personalizzato.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"}.

Ulteriori informazioni sulla configurazione del preheader e-mail [in questa pagina](../email/header-parameters.md).

+++

+++ Perché esiste una discrepanza nel comportamento dei collegamenti quando si utilizza un componente HTML nei modelli e-mail?  

Quando si aggiunge un **componente HTML** a un modello di e-mail, i collegamenti possono comportarsi in modo diverso a seconda del **client e-mail**, della **modalità di visualizzazione** o del **dispositivo/browser**. Ad esempio, i collegamenti di ancoraggio possono funzionare in modo diverso in **Outlook affiancato** rispetto alla visualizzazione a schermo intero. Tieni presente queste varianti durante la progettazione di modelli e-mail e il test su più client e dispositivi.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"}.

Consulta anche le best practice per la progettazione di e-mail [in questa pagina](../email/get-started-email-design.md).

+++


+++ Come evitare la perdita di collegamenti di tracciamento e-mail nei rapporti?

Il tracciamento dei collegamenti mancanti in Adobe Journey Optimizer si verifica quando gli URL e-mail utilizzano variabili dinamiche e non iniziano con http o quando le istruzioni logiche vengono inserite nel campo URL. Per risolvere questo problema, assicurati che tutti gli URL inizino con http, evita di utilizzare la logica nel campo URL e sposta la logica di personalizzazione complessa nel contenuto di HTML o negli attributi pre-elaborati.


Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"}.

Ulteriori informazioni sul tracciamento delle e-mail [&#x200B; in questa pagina](../email/message-tracking.md).

+++

+++ Come si risolve un errore di Mail Exchanger durante la configurazione di campagne e-mail transazionali attivate da API? 

Se durante la creazione di una configurazione del canale per una campagna e-mail transazionale attivata da API in Adobe Journey Optimizer si verifica un errore Mail Exchanger (MX), la causa potrebbe essere **Errori di configurazione DNS** o **Limitazioni dei criteri di DMARC**. Per risolvere il problema, verificare che il DNS sia configurato correttamente e che il dominio sia conforme ai requisiti di **autenticazione, reporting e conformità dei messaggi basati sul dominio (DMARC)**.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"}.

Ulteriori informazioni sui criteri di DMARC per la posta elettronica [in questa pagina](../configuration/dmarc-record-update.md).

Consulta anche la [documentazione sulle campagne attivate da API](../campaigns/api-triggered-campaigns.md).
+++

## Canale push {#ajo-troubleshooting-push}

+++ Un profilo può avere più token push in Adobe Journey Optimizer?

Quando implementi le notifiche push in Journey Optimizer, un singolo profilo può effettivamente avere più token push associati a dispositivi diversi. Durante una campagna di notifica push, Journey Optimizer è progettato per gestire questi token e garantire che il profilo di destinazione possa essere raggiunto su tutti i dispositivi associati.

Per ulteriori informazioni sulla gestione dei token push, consulta [questo articolo per la risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}.

Ulteriori informazioni sulla configurazione push [in questa pagina](../push/push-configuration.md).

+++

+++ Perché quando fai clic su un messaggio push non mi reindirizza all’URL web configurato?  

Se i messaggi push non vengono reindirizzati all’URL web desiderato, la causa potrebbe essere una configurazione non corretta dell’azione di clic o impostazioni disabilitate della notifica push. Per risolvere il problema, verifica che l&#39;**azione clic** per il messaggio push sia impostata correttamente e che **siano abilitati la visualizzazione e il tracciamento automatici** delle notifiche push.

Per ulteriori informazioni su questo problema, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"}.

Ulteriori informazioni sulla configurazione push [in questa pagina](../push/push-configuration.md).

+++


## Canale SMS {#ajo-troubleshooting-sms}

+++ Perché il mio SMS transazionale non viene consegnato anche se il consenso è impostato su `marketing.sms.value=y`?

Se un destinatario risponde **STOP** a un SMS, tutti i messaggi futuri provenienti da tale numero breve vengono bloccati, inclusi i messaggi transazionali. Per garantire il recapito ininterrotto degli SMS transazionali, configurali e inviali tramite un **numero breve separato** da cui i destinatari non hanno precedentemente rinunciato.

Per ulteriori informazioni su questo problema, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"}.

Ulteriori informazioni sulla configurazione della rinuncia SMS [in questa pagina](../sms/sms-opt-out.md).

+++

## Canale in-app

+++ Perché non posso creare rapporti sul canale in-app in Customer Journey Analytics?

Le difficoltà di generazione rapporti sul **canale in-app** in Adobe Customer Journey Analytics spesso derivano da **visualizzazioni dati**, **set di dati** o **aggiornamenti schema** non configurati correttamente. Assicurati che queste configurazioni siano applicate correttamente per risolvere il problema.

Per ulteriori informazioni su questo problema, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"}.

Ulteriori informazioni su come integrare i dati di analisi di Journey Optimizer in Customer Journey Analytics [in questa pagina](https://experienceleague.adobe.com/it/docs/analytics-platform/using/integrations/ajo?lang=en#automatically-configure-journey-optimizer-integration){target="_blank"}.

Consulta anche la [documentazione di Journey Optimizer All-Time Reports](../reports/report-gs-cja.md)

+++


## Gestione dati {#ajo-troubleshooting-data-management}

+++ Come si applicano le impostazioni Time-to-Live (TTL) ai set di dati Profilo e Data Lake quando crei una nuova sandbox?

Le organizzazioni che eseguono il provisioning di nuove sandbox in Adobe Journey Optimizer hanno sollevato domande su come le impostazioni TTL (Time-to-Live) si applicano ai set di dati profilo e data lake. Questo articolo chiarisce che le impostazioni TTL non influiscono sulle sandbox esistenti e vengono applicate automaticamente solo a quelle con provisioning recente.

Per informazioni su come gestire il TTL, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}.

Ulteriori informazioni sul set di dati Time-to-live [&#x200B; in questa pagina](../data/datasets-ttl.md).

+++


## Gestione di profili e pubblico {#ajo-troubleshooting-audiences}

+++ Come si risolvono le discrepanze nel conteggio del pubblico?

Il numero di voci elaborate nella funzionalità **Read Audience** di Adobe Journey Optimizer può essere inferiore al numero di tipi di pubblico previsto. Questo problema si verifica spesso a causa di configurazioni errate dello spazio dei nomi, che determinano l’esclusione dei profili dai percorsi. La risoluzione prevede il controllo e la correzione delle configurazioni dello spazio dei nomi, l’esame della documentazione pertinente e l’adeguamento delle priorità per garantire operazioni più fluide in Adobe Journey Optimizer.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}.

Vedi anche [questo articolo sui conteggi dei tipi di pubblico obsoleti](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Ulteriori informazioni sull&#39;attività **Read Audience** nei percorsi [in questa pagina](../building-journeys/read-audience.md).

+++

+++ Perché gli aggiornamenti del profilo non riescono?

In Adobe Journey Optimizer, alcuni valori di campo potrebbero non essere aggiornati correttamente dopo l&#39;esecuzione di un&#39;attività **Aggiorna profilo** in un percorso. In alcuni casi, i campi aggiornati possono scomparire o tornare allo stato precedente. Per risolvere questo problema, verificare la presenza di regole o condizioni in conflitto, esaminare le impostazioni delle autorizzazioni, utilizzare un set di dati univoco per l&#39;attività **Aggiorna profilo** e assicurarsi che nessun altro processo di acquisizione stia scrivendo contemporaneamente sullo stesso profilo.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sull&#39;attività **Aggiorna profilo** nei percorsi [in questa pagina](../building-journeys/update-profiles.md).

Consulta anche la [documentazione di Adobe Experience Platform sull&#39;acquisizione dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}.

+++

+++ Perché c’è una mancata corrispondenza nel conteggio dei profili che entrano in un percorso rispetto al pubblico associato?

La discrepanza può verificarsi quando il percorso utilizza uno snapshot del profilo del giorno precedente se lo snapshot del giorno corrente non è disponibile al momento dell&#39;esecuzione del percorso.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni in [questo post della community Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}.

Consulta anche la [documentazione API delle pianificazioni di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"} per verificare quando è pianificato il processo giornaliero.

+++


+++ Come si risolvono i problemi di popolazione del pubblico?

I problemi di popolazione del pubblico possono verificarsi quando mancano componenti o risorse, spesso a causa di configurazioni errate di adesione, provisioning o autorizzazioni. Per risolvere questi problemi, inizia verificando i diritti, assicurando il provisioning corretto e rivedendo le autorizzazioni. Se il problema persiste, inoltra il caso e coordinati con i team di supporto per una risoluzione completa.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sull&#39;attività **Aggiorna profilo** nei percorsi [in questa pagina](../building-journeys/update-profiles.md).

Consulta anche la [documentazione del profilo Adobe Real-Time CDP](https://experienceleague.adobe.com/it/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}.

+++

+++ Perché il conteggio dei profili coinvolgibili è aumentato in modo significativo in un breve periodo? 

La metrica **Profili coinvolgibili** riflette il numero di profili univoci coinvolti da percorsi o campagne negli ultimi 12 mesi. Un aumento improvviso può derivare dal targeting di pubblici di grandi dimensioni o da modifiche nei set di dati. Per gestire questo problema, controlla la **logica di conteggio dei profili**, indaga i percorsi che hanno come target tipi di pubblico di grandi dimensioni, **filtra i tipi di pubblico** a livello di percorso, riduci le **dimensioni del pubblico indirizzabile** e monitora **modifiche ai set di dati**.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"} per scoprire i passaggi per risolvere il problema.

Monitora l&#39;utilizzo delle licenze della tua organizzazione e i profili coinvolgibili utilizzando [Dashboard utilizzo licenze](../audience/license-usage.md)

Consulta anche la [Panoramica di Adobe Experience Platform Query Service](https://experienceleague.adobe.com/it/docs/experience-platform/query/home?lang=en){target="_blank"}.

+++

+++ Perché le e-mail vengono inviate a persone esterne al pubblico previsto in base a funzioni data?

Le e-mail possono essere inviate a destinatari che **non soddisfano i criteri di pubblico specificati**. Ad esempio, i membri con date di rimborso **precedenti al 4 luglio 2025** possono ricevere e-mail destinate solo a coloro che sono successivi a tale data. Questo comportamento può essere dovuto a **segmentazione del pubblico non configurata correttamente** o a **modifiche impreviste nella logica di qualifica del profilo**.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sulle funzioni data [in questa pagina](../../rp_landing_pages/date-landing-page.md).

+++

+++ Come posso risolvere i problemi di selezione del pubblico e gli errori di Chrome durante il salvataggio dei percorsi?

L&#39;aggiunta di tipi di pubblico alle condizioni del percorso può talvolta causare **arresti anomali dell&#39;applicazione** o la visualizzazione di un **errore Aw Snap** in Chrome, inclusi errori durante il salvataggio dei percorsi. Questi problemi sono spesso correlati ai **servizi Chromium**. Per risolverli, applica un **aggiornamento del browser** o utilizza una **soluzione alternativa** appropriata.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"} per scoprire i passaggi per risolvere il problema.

+++

## Percorsi {#ajo-troubleshooting-journeys}

Per Percorsi, consulta le seguenti sezioni per la risoluzione dei problemi:

* [Risolvere i problemi prima di testare il percorso](../building-journeys/troubleshooting.md)
* [Risoluzione dei problemi relativi alle azioni in entrata nei percorsi](../building-journeys/troubleshooting-inbound.md)
* [Risolvere i problemi relativi all&#39;esecuzione di Live percorsi](../building-journeys/troubleshooting-execution.md)
* [Risolvere i problemi relativi alle azioni personalizzate](../action/troubleshoot-custom-action.md)


+++ Perché le espressioni vengono perse durante la creazione di una nuova versione del percorso?  

Durante la creazione di una nuova versione di un percorso, **le espressioni nei passaggi specifici** potrebbero andare perse, causando errori e richiedendo il reinserimento manuale. Per risolvere il problema, **duplica il percorso**, verifica la riproducibilità, **evita ricariche del browser** e utilizza l&#39;**area di lavoro aggiornata** per i percorsi precedenti.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"} per scoprire i passaggi per risolvere il problema.

Scopri come duplicare un percorso [in questa pagina](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Perché i profili escono anticipatamente dai percorsi? 

I profili possono uscire da un percorso in modo imprevisto senza passare da un nodo designato quando lo stato di **verifica delle condizioni** dei messaggi inviati non è configurato correttamente. Per risolvere il problema, controlla la **logica della condizione**, implementa **logica alternativa** oppure rivolgiti al tuo **team di implementazione**.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"} per scoprire i passaggi per risolvere il problema.

Consulta anche [Linee guida per la progettazione dei Percorsi](../building-journeys/using-the-journey-designer.md).

+++


+++ Perché i profili stanno uscendo dai percorsi in modo imprevisto?

I profili possono uscire da un percorso in modo imprevisto quando si verifica il limite **evento**, causando l&#39;eliminazione di alcuni profili se il numero di eventi elaborati supera la capacità del sistema. Per ridurre le uscite di profilo, individua i **limiti di sistema**, monitora i **picchi di eventi** e ottimizza il **flusso di dati** per evitare il superamento delle soglie.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"} per scoprire i passaggi per risolvere il problema.

Vedi anche [guardrail di Percorso](../start/guardrails.md#journey-guardrails).

+++


+++ Perché il mio evento non attiva il percorso previsto?  

Gli eventi potrebbero non riuscire ad attivare un percorso anche se tutti i criteri sono soddisfatti quando vengono **creati tramite i servizi di query** anziché essere inviati in streaming al **Servizio di base raccolta dati (DCCS)**. Per risolvere questo problema, controlla la configurazione dell&#39;evento, assicurati che gli eventi siano **inviati direttamente in streaming a DCCS** e verifica la funzionalità utilizzando la **modalità di test**.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sugli eventi [in questa pagina](../event/about-events.md).

Vedi anche [Guardrail evento Percorso](../start/guardrails.md#events).

+++


+++ Come posso risolvere i problemi di attivazione del percorso dopo le modifiche del pubblico in Adobe Journey Optimizer? 

Se un percorso smette di attivarsi dopo aver apportato modifiche al pubblico associato, ad esempio modifiche al criterio di unione, si potrebbero verificare flussi interrotti. Per risolvere il problema, **duplica e ripubblica il percorso** con le impostazioni aggiornate per il pubblico, in modo che i trigger funzionino correttamente.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} per scoprire i passaggi per risolvere il problema.

Scopri come duplicare un percorso [in questa pagina](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Perché un’azione personalizzata che chiama un endpoint esterno di terze parti riceve un timeout?

Gli errori di timeout possono verificarsi quando un&#39;azione personalizzata **&#x200B;**&#x200B;chiama un endpoint esterno di terze parti. Per risolvere il problema, verifica che l&#39;endpoint **sia accessibile**, controlla **i registri del server**, assicurati che **non vi sia alcun blocco da Adobe**, aggiorna le configurazioni dell&#39;endpoint in base alle esigenze e **verifica dopo gli aggiornamenti**. Inoltre, ricorda le **specifiche di timeout della chiamata API**.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sull&#39;API di limitazione del Percorso [in questa pagina](../configuration/throttling.md).

Consulta anche la [documentazione sull&#39;integrazione con sistemi esterni](../configuration/external-systems.md).

+++

+++ Quali operazioni è necessario eseguire se si verifica un errore 403 con il messaggio **invalid_access** o **Nessun accesso a questo dataId=XX concesso** durante la pubblicazione di un pubblico da una freccia?

Per risolvere questo errore, chiedi all’amministratore di verificare che il tuo profilo utente abbia accesso alle visualizzazioni dati richieste per la pubblicazione di tipi di pubblico, quindi prova di nuovo a pubblicare il pubblico.

Consulta [la documentazione sulle autorizzazioni](../administration/permissions.md){target="_blank"} per scoprire i passaggi per risolvere il problema.

+++

## Regole {#ajo-troubleshooting-rules}

+++ Perché il menu a discesa Regole di limitazione non funziona?

I problemi relativi al menu a discesa **Regole di limitazione** si verificano spesso quando i set di regole sono **non configurati correttamente** o **inaccessibili**. Assicurati che tutti i set di regole siano configurati e disponibili correttamente per risolvere il problema.

Per ulteriori informazioni, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"}.

Scopri come applicare le regole di limitazione di utilizzo [&#x200B; in questa sezione](../conflict-prioritization/rule-sets.md).

+++

## Funzione Decisioni {#ajo-troubleshooting-decisioning}

+++ Come posso risolvere i problemi durante la creazione delle raccolte di offerte?

Le difficoltà nella creazione delle raccolte di offerte spesso si verificano quando **non è stato eseguito il provisioning dei cataloghi** per la tua organizzazione. Per risolvere questo problema, verifica che sia stato eseguito correttamente il provisioning di tutti i cataloghi richiesti prima di tentare di creare le raccolte di offerte.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sulle raccolte di offerte [in questa pagina](../offers/offer-library/creating-collections.md).

+++

+++ Perché non riesco ad accedere ad Offer Decisioning?  

Durante l&#39;integrazione di Adobe Target in un&#39;applicazione tramite Adobe Journey Optimizer, l&#39;opzione **Offer Decisioning** potrebbe non essere accessibile nella configurazione dello stream di dati. Ciò si verifica in genere a causa di **impostazioni delle autorizzazioni** o **vincoli di provisioning**. Per risolvere il problema, verifica le autorizzazioni utente e assicurati che sia attivo il provisioning necessario.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sulle autorizzazioni richieste per Offer Decisioning [in questa pagina](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++



## Multilingue {#ajo-troubleshooting-multilingual}

+++ Come risolvere il problema `Message validation error (CJMMAS - 1069-500)`?

In Adobe Journey Optimizer, un errore di convalida del messaggio (CJMMAS - 1069-500) collegato alla funzione multilingue impedisce che i percorsi vengano impostati sulla modalità di test o pubblicati.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sul contenuto multilingue [in questa pagina](../content-management/multilingual-gs.md).

+++


## Configurazione {#ajo-troubleshooting-config}

+++ Come si abilita TLS v1.3 per le azioni personalizzate?  

Per mantenere l&#39;integrità e la sicurezza dei dati di **1&rbrace; durante la connessione a sistemi di terze parti, assicurati che Transport Layer Security (** TLS **) v1.3 sia abilitato per le azioni personalizzate.** Questo aiuta a proteggere le comunicazioni e previene potenziali vulnerabilità di sicurezza.


Per ulteriori informazioni, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"}.

Ulteriori informazioni sul contenuto multilingue [in questa pagina](../action/about-custom-action-configuration.md).

+++

+++ Perché non è possibile creare un dashboard direttamente da una query in Adobe Journey Optimizer? 

In Adobe Journey Optimizer non è possibile creare dashboard direttamente dalle query. Per creare dashboard, utilizza le **funzionalità di creazione dashboard** disponibili in Adobe Experience Platform, che consentono di visualizzare e analizzare i dati delle query in modo efficace.

Per ulteriori informazioni, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"}.

+++

## API {#ajo-troubleshooting-apis}

+++ Come posso risolvere i problemi di accesso con l’API di Query Service?  

Gli errori di accesso quando si utilizza l&#39;API **Query Service API** tramite Postman o strumenti simili sono in genere causati da **autorizzazioni insufficienti**. Per risolvere questo problema, verifica le autorizzazioni utente, controlla le credenziali API e fornisci informazioni dettagliate da supportare, se necessario.

Per ulteriori informazioni, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"}.

Consulta anche la [Documentazione di gestione delle credenziali API](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/permissions?lang=en#manage-api-credentials-for-role){target="_blank"}.

+++
