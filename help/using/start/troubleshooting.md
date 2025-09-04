---
solution: Journey Optimizer
product: journey optimizer
title: Risoluzione dei problemi di Journey Optimizer
description: Domande sulla risoluzione dei problemi di Journey Optimizer
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3ab8957d0aec6f30853de5537e03f0e7bec2017c
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 2%

---

# Risoluzione dei problemi {#ajo-troubleshooting}


Di seguito è riportato un elenco di articoli per la risoluzione dei problemi relativi a Adobe Journey Optimizer. Ogni sezione relativa alla risoluzione dei problemi fornisce le risposte alle domande frequenti e alle soluzioni ai problemi.

Consulta anche le [Domande frequenti su Adobe Experience Platform e la documentazione sulla risoluzione dei problemi](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}.

## Canale e-mail {#ajo-troubleshooting-email}

### Progettazione e-mail {#ajo-troubleshooting-design}

+++ Come evitare problemi di formattazione delle e-mail in Adobe Journey Optimizer utilizzando i temi?

In Adobe Journey Optimizer (AJO), la modifica dei blocchi CSS predefiniti nell’intestazione e-mail può causare problemi di formattazione imprevisti, soprattutto dopo la rimozione dei frammenti di contenuto. Questi problemi sono più evidenti sui dispositivi mobili e possono causare spostamenti di layout o incoerenze di stile. Per evitare questo problema, utilizza la funzione Temi per applicare CSS personalizzati in modo sicuro senza modificare gli stili CSS generati dal sistema.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"}.

Ulteriori informazioni sulla formattazione delle e-mail [ in questa pagina](../email/get-started-email-design.md).

+++


+++ Perché i frammenti con campi modificabili non funzionano?

In Adobe Journey Optimizer, i frammenti con campi modificabili potrebbero non essere caricati correttamente o duplicati in modo imprevisto quando vengono aggiunti ai modelli. Il problema interessa in genere frammenti specifici in ambienti diversi.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"}.

Ulteriori informazioni sui frammenti personalizzabili [in questa pagina](../content-management/customizable-fragments.md).

+++

+++ Perché i modelli e i contenuti delle e-mail scompaiono dai percorsi non pubblicati?

Quando si modificano modelli e-mail in un percorso non pubblicato, il contenuto e i modelli di alcuni messaggi e-mail potrebbero scomparire in modo imprevisto. Questo può causare rilavorazione e ritardi. Per ridurre il rischio di questo problema, evita modifiche simultanee, limita il numero di schede aperte e salva le modifiche frequentemente.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}.

Ulteriori informazioni sui modelli [in questa pagina](../email/use-email-templates.md).

+++

+++ Un profilo può avere più token push in Adobe Journey Optimizer?

Quando implementi le notifiche push in Journey Optimizer, un singolo profilo può effettivamente avere più token push associati a dispositivi diversi. Durante una campagna di notifica push, Journey Optimizer è progettato per gestire questi token e garantire che il profilo di destinazione possa essere raggiunto su tutti i dispositivi associati.

Per ulteriori informazioni sulla gestione dei token push, consulta [questo articolo per la risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}.

Ulteriori informazioni sulla configurazione push [in questa pagina](../push/push-configuration.md).

+++

### Tracciamento e reporting delle e-mail {#ajo-troubleshooting-tracking}

+++ Come evitare la perdita di collegamenti di tracciamento e-mail nei rapporti?

Il tracciamento dei collegamenti mancanti in Adobe Journey Optimizer si verifica quando gli URL e-mail utilizzano variabili dinamiche e non iniziano con http o quando le istruzioni logiche vengono inserite nel campo URL. Per risolvere questo problema, assicurati che tutti gli URL inizino con http, evita di utilizzare la logica nel campo URL e sposta la logica di personalizzazione complessa nel contenuto di HTML o negli attributi pre-elaborati.


Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"}.

Ulteriori informazioni sul tracciamento delle e-mail [ in questa pagina](../email/message-tracking.md).

+++

### Invio e-mail {#ajo-troubleshooting-sending}

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


## Gestione dati {#ajo-troubleshooting-data-management}

+++ Come si applicano le impostazioni Time-to-Live (TTL) ai set di dati Profilo e Data Lake quando crei una nuova sandbox?

Le organizzazioni che eseguono il provisioning di nuove sandbox in Adobe Journey Optimizer hanno sollevato domande su come le impostazioni TTL (Time-to-Live) si applicano ai set di dati profilo e data lake. Questo articolo chiarisce che le impostazioni TTL non influiscono sulle sandbox esistenti e vengono applicate automaticamente solo a quelle con provisioning recente.

Per informazioni su come gestire il TTL, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}.

Ulteriori informazioni sul set di dati Time-to-live [ in questa pagina](../data/datasets-ttl.md).

+++


## Gestione di profili e pubblico {#ajo-troubleshooting-audiences}

+++ Come si risolvono le discrepanze nel conteggio del pubblico?

Il numero di voci elaborate nella funzionalità **Read Audience** di Adobe Journey Optimizer può essere inferiore al numero di tipi di pubblico previsto. Questo problema si verifica spesso a causa di configurazioni errate dello spazio dei nomi, che determinano l’esclusione dei profili dai percorsi. La risoluzione prevede il controllo e la correzione delle configurazioni dello spazio dei nomi, l’esame della documentazione pertinente e l’adeguamento delle priorità per garantire operazioni più fluide in Adobe Journey Optimizer.

Per informazioni su come risolvere il problema, consultare [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}.

Vedi anche [questo articolo sui conteggi dei tipi di pubblico obsoleti](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Ulteriori informazioni sull&#39;attività **Read Audience** nei percorsi [in questa pagina](../building-journeys/read-audience.md).

+++

+++ Perché gli aggiornamenti del profilo non riescono?

In Adobe Journey Optimizer, alcuni valori di campo potrebbero non essere aggiornati correttamente dopo l&#39;esecuzione di un&#39;attività **Aggiorna profilo** in un percorso. In alcuni casi, i campi aggiornati possono scomparire o tornare allo stato precedente. Per risolvere questo problema, verificare la presenza di regole o condizioni in conflitto, esaminare le impostazioni delle autorizzazioni, utilizzare un set di dati univoco per l&#39;attività **Aggiorna profilo** e assicurarsi che nessun altro processo di acquisizione stia scrivendo contemporaneamente sullo stesso profilo.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sull&#39;attività **Aggiorna profilo** nei percorsi [in questa pagina](../building-journeys/update-profiles.md).

Consulta anche la [documentazione di Adobe Experience Platform sull&#39;acquisizione dei dati](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}.

+++

+++ Perché c’è una mancata corrispondenza nel conteggio dei profili che entrano in un percorso rispetto al pubblico associato?

La discrepanza può verificarsi quando il percorso utilizza uno snapshot del profilo del giorno precedente se lo snapshot del giorno corrente non è disponibile al momento dell&#39;esecuzione del percorso.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni in [questo post della community Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}.

Consulta anche la [documentazione API delle pianificazioni di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"} per verificare quando è pianificato il processo giornaliero.

+++


+++ Come si risolvono i problemi di popolazione del pubblico?

I problemi di popolazione del pubblico possono verificarsi quando mancano componenti o risorse, spesso a causa di configurazioni errate di adesione, provisioning o autorizzazioni. Per risolvere questi problemi, inizia verificando i diritti, assicurando il provisioning corretto e rivedendo le autorizzazioni. Se il problema persiste, inoltra il caso e coordinati con i team di supporto per una risoluzione completa.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sull&#39;attività **Aggiorna profilo** nei percorsi [in questa pagina](../building-journeys/update-profiles.md).

Consulta anche la [documentazione del profilo Adobe Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}.

+++

+++ Come posso risolvere i problemi di attivazione del percorso dopo le modifiche del pubblico in Adobe Journey Optimizer? 

Se un percorso smette di attivarsi dopo aver apportato modifiche al pubblico associato, come le modifiche al criterio di unione, si potrebbero verificare flussi di campagna interrotti. Per risolvere il problema, **duplica e ripubblica il percorso** con le impostazioni aggiornate per il pubblico, in modo che i trigger funzionino correttamente.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} per scoprire i passaggi per risolvere il problema.

Scopri come duplicare un percorso [in questa pagina](../building-journeys/journey-ui.md#duplicate-a-journey).

+++


## Percorsi

### Eventi

+++ Perché il mio evento non attiva il percorso previsto?  

Gli eventi potrebbero non riuscire ad attivare un percorso anche se tutti i criteri sono soddisfatti quando vengono **creati tramite i servizi di query** anziché essere inviati in streaming al **Servizio di base raccolta dati (DCCS)**. Per risolvere questo problema, controlla la configurazione dell&#39;evento, assicurati che gli eventi siano **inviati direttamente in streaming a DCCS** e verifica la funzionalità utilizzando la **modalità di test**.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sugli eventi [in questa pagina](../event/about-events.md).

Vedi anche [Guardrail evento Percorso](../start/guardrails.md#events).

+++

## Funzione Decisioni {#ajo-troubleshooting-decisioning}

+++ Come posso risolvere i problemi durante la creazione delle raccolte di offerte?

Le difficoltà nella creazione delle raccolte di offerte spesso si verificano quando **non è stato eseguito il provisioning dei cataloghi** per la tua organizzazione. Per risolvere questo problema, verifica che sia stato eseguito correttamente il provisioning di tutti i cataloghi richiesti prima di tentare di creare le raccolte di offerte.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sulle raccolte di offerte [in questa pagina](../offers/offer-library/creating-collections.md).

+++


## Multilingue {#ajo-troubleshooting-multilingual}

+++ Come risolvere il problema `Message validation error (CJMMAS - 1069-500)`?

In Adobe Journey Optimizer, un errore di convalida del messaggio (CJMMAS - 1069-500) collegato alla funzione multilingue impedisce che i percorsi vengano impostati sulla modalità di test o pubblicati.

Consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} per scoprire i passaggi per risolvere il problema.

Ulteriori informazioni sul contenuto multilingue [in questa pagina](../content-management/multilingual-gs.md).

++


## Configurazione {#ajo-troubleshooting-config}

### Sicurezza {#ajo-troubleshooting-security}

+++ Come si abilita TLS v1.3 per le azioni personalizzate?  

Per mantenere l&#39;integrità e la sicurezza dei dati di **1&rbrace; durante la connessione a sistemi di terze parti, assicurati che Transport Layer Security (** TLS **) v1.3 sia abilitato per le azioni personalizzate.** Questo aiuta a proteggere le comunicazioni e previene potenziali vulnerabilità di sicurezza.


Per ulteriori informazioni, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"}.

Ulteriori informazioni sul contenuto multilingue [in questa pagina](../action/about-custom-action-configuration.md).

+++

### Dashboard {#ajo-troubleshooting-dashboards}

+++ Perché non è possibile creare un dashboard direttamente da una query in Adobe Journey Optimizer? 

In Adobe Journey Optimizer non è possibile creare dashboard direttamente dalle query. Per creare dashboard, utilizza le **funzionalità di creazione dashboard** disponibili in Adobe Experience Platform, che consentono di visualizzare e analizzare i dati delle query in modo efficace.

Per ulteriori informazioni, consulta [questo articolo sulla risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"}.

++