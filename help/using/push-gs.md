---
title: Guida introduttiva alla configurazione push
description: Comprendere il flusso di dati e i componenti della notifica push
hide: true
hidefromtoc: true
source-git-commit: a2eee802f82552e56ced00f93e5e4c8a7b3feb7a
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---

# Guida introduttiva alla configurazione push {#get-started-push}

![](assets/do-not-localize/badge.png)

Le notifiche push fungono da canale di comunicazione rapida e consentono di inviare messaggi, offerte o altre informazioni agli utenti dell’app mobile. In genere, l’utente finale deve acconsentire alla ricezione di notifiche push; l’opt-in di solito avviene durante il processo di installazione e agli utenti finali viene fornito un modo per gestire le notifiche se cambiano idea in un secondo momento. Un importante vantaggio delle notifiche push nel mobile computing è che la tecnologia non richiede l&#39;apertura di applicazioni specifiche su un dispositivo mobile per poter ricevere un messaggio. Questo consente a uno smartphone di ricevere e visualizzare notifiche anche quando lo schermo del dispositivo è bloccato e l&#39;app mobile è in background o chiusa.

**[!DNL Adobe Journey Optimizer]**  ti consente di inviare messaggi push su larga scala sensibili a fattori di tempo, rilevanti e personalizzati. Un segmento di profili cliente può essere indirizzato per ricevere notifiche push potenziate sui propri dispositivi mobili iOS e Android. Questi segmenti possono essere creati sulla base di eventi di esperienza passati o live degli utenti, dati dei record degli utenti o una combinazione di interazioni e dati degli utenti. Una volta attivato un percorso, puoi visualizzare rapporti dettagliati sul numero di messaggi inviati, sui motivi dell’errore e anche sulle informazioni di tracciamento push, come il numero di utenti che vi hanno fatto clic.

Questo documento illustra un flusso di dati end-to-end di notifiche push di base utilizzando [!DNL Journey Optimizer] e un diagramma di flusso utente per spiegare come ogni ruolo adempie alle proprie responsabilità e collabora per unire il flusso di dati push.


## Componenti e servizi interessati

* **I** provider di messaggi cloud sono servizi di terze parti che ci consentono di inviare notifiche dai server remoti alle app mobili.

   [!DNL Adobe Journey Optimizer]  supporta sia le piattaforme Android che iOS e si occupa di due servizi di messaggistica cloud primari:
   * FCM (Firebase Cloud Messaging) - per inviare notifiche all’app mobile Android
   * APN (Apple Push Notification Service) - per inviare notifiche all’app mobile iOS

* **App mobile integrata con Adobe Mobile** SDK che consente di integrare le app mobili con le soluzioni Adobe Experience Cloud. L’SDK di Mobile è composto da varie estensioni della soluzione Experience Cloud per fornire funzionalità specifiche del servizio che rappresentano. Queste estensioni espongono varie API per abilitare il flusso di dati, come la registrazione del token push o l’invio di eventi di tracciamento push o qualsiasi altro evento di esperienza personalizzato a Adobe Experience Platform.

* **Adobe Launch**  (o Raccolta dati) è la nuova generazione di funzionalità di gestione SDK per dispositivi mobili che consente il flusso di dati dall’SDK mobile a  [!DNL Adobe Experience Platform]. Fornisce funzionalità per registrare le estensioni, creare regole ed elementi dati per inviare dati dall&#39;app mobile alle soluzioni Adobe Experience Cloud. Per quanto riguarda il flusso di dati delle notifiche push, le configurazioni principali richieste in Adobe Launch sono:

   * Creazione di un datastream per configurare i set di dati evento di profilo ed esperienza in base ai quali i dati scorrono in experience platform.
   * Creazione di una proprietà mobile lato client e aggiunta di estensioni. L’SDK di Mobile si integra strettamente con queste estensioni per fornire un’esperienza di raccolta dati fluida.
   * Registrazione dell’identificatore del bundle dell’app mobile e delle credenziali dell’app che faciliterebbero l’identificazione e la convalida univoche dell’app al momento della consegna della notifica push.

* **Real-time Customer** Profile è il componente in Adobe Experience Platform che consente di visualizzare una visualizzazione olistica di ogni singolo cliente combinando dati provenienti da più canali, tra cui web, dispositivi mobili, CRM e terze parti. Il profilo ti consente di consolidare i dati dei clienti in una visualizzazione unificata che offre un account utilizzabile e con marca temporale per ogni interazione con il cliente. I dati statici che identificano l’utente dell’app mobile, ad esempio un token push, vengono memorizzati nel profilo dell’utente come dati di record, mentre le interazioni che l’utente esegue con le notifiche push vengono tracciate come dati di eventi della serie temporale.

* **[!DNL Adobe Journey Optimizer]** : una volta realizzate le integrazioni app mobili con i componenti sopra menzionati e i profili cliente sono disponibili come profili cliente in tempo reale, puoi sfruttare le potenti funzionalità di segmentazione del pubblico in  [!DNL Adobe Journey Optimizer]  per garantire un’esperienza ottimale per ogni persona.


## Flusso dati push

Questo diagramma mostra un flusso di dati di messaggistica push di base e fornisce un&#39;occhiata ai vari prodotti e componenti di Adobe coinvolti nel flusso.

![](assets/push-flow.png)


1. Il cliente sviluppa un’app mobile su Android o iOS che rilascerà ai propri utenti. Per utilizzare la funzionalità push fornita dai provider push, cioè APNS by Apple e FCM by Google, l’app mobile si registra e abilita la funzionalità push.
1. I provider push generano e inviano un token push all’app mobile. Un token push è un identificatore che i mittenti utilizzano per eseguire il targeting di dispositivi specifici con una notifica push.
1. L’app mobile è integrata con Adobe Mobile SDK che espone varie estensioni e API. L&#39;estensione Messaging espone un&#39;API per registrare il token push in Adobe Experience Platform rispetto al profilo del cliente.
1. Quando l&#39;app mobile è pronta, viene configurata in **[!DNL Journey Launch]** `>` **Configurazioni app** insieme alle credenziali.
L’addetto al marketing ora scrive una notifica push in **[!DNL Adone Journey Optimizer]** `>` **Messaggi** rispetto all’app mobile registrata.
1. L’addetto al marketing orchestra un percorso cliente che definisce il flusso di eventi e azioni. Per inviare una notifica push in una fase del percorso, l’addetto al marketing aggiunge un’azione di tipo &quot;Messaggio&quot; e la associa al messaggio creato nel passaggio precedente.
1. Ogni volta che un profilo cliente si qualifica per ricevere la notifica push per qualsiasi motivo, ad esempio all’attivazione di un evento o alla qualificazione di un segmento, il messaggio viene personalizzato in base al profilo, se applicabile.
1. Il messaggio push personalizzato viene inviato per un’ulteriore elaborazione al servizio di consegna push.
1. Il servizio di consegna push convalida le credenziali dell’app associata al messaggio.
1. Il messaggio viene inviato ai provider push per la consegna all’app mobile in base al token push e alle credenziali specifiche.
1. I provider push inviano un feedback che indica se il messaggio è stato recapitato correttamente al provider o meno. In caso contrario, il messaggio di errore pertinente fa parte del feedback. Questo feedback viene inviato ad Adobi di reporting per consentire al cliente di visualizzare nel proprio Percorso [Live](reports/live-report.md) e [Report globali](reports/global-report.md).
1. Nel frattempo, i provider push recapitano in modo asincrono la notifica push di successo all’app mobile.
1. Quando il cliente interagisce con la notifica, le impression come click/open possono essere tracciate come **Eventi esperienza**. L&#39;estensione Messaging espone le API per inviare eventi di tracciamento in Adobe Experience Platform in base al profilo del cliente.

## Flusso utente push

Questo diagramma mostra i vari passaggi necessari per configurare i componenti che formano lo scheletro del flusso di dati push. Gli elementi azione sono stati organizzati in categorie in base al ruolo che esegue la configurazione e al componente che viene configurato. Come puoi vedere, prima di iniziare a inviare notifiche push con **[!DNL Adobe Journey Optimizer]** , devi accertarti che le configurazioni e le integrazioni siano presenti nell’app mobile, **[!DNL Adobe Launch]** e **[!DNL Adobe Experience Platform]**.

![](assets/user-flow.png)

I passaggi dettagliati per la configurazione del canale push e l’abilitazione delle notifiche push in [!DNL Journey Optimizer] sono disponibili in [questa pagina](push-configuration.md).