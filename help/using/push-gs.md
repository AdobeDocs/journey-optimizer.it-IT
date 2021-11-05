---
title: Introduzione alla configurazione push
description: Comprendere il flusso di dati e i componenti della notifica push
topic: Mobile
feature: Push
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 0f79d465dd5a63ced107614407de167c7d9dad5a
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 4%

---

# Introduzione alla configurazione push {#get-started-push}

Le notifiche push ti aiutano a raggiungere gli utenti dell’app mobile in qualsiasi momento, specialmente quando non stanno utilizzando attivamente l’app. Le notifiche push possono aiutarti a raggiungere una varietà di casi d’uso, come fornire aggiornamenti sul tuo servizio, chiedere a un utente di agire, avvisare l’utente di una nuova offerta, ecc. Le piattaforme di dispositivi richiedono l’opt-in prima che gli utenti finali possano ricevere o visualizzare le notifiche. È possibile ricevere l’opt-in dell’utente non appena l’app viene avviata per la prima volta dopo l’installazione o in una sessione o un flusso di lavoro successivi, a seconda dei casi. [!DNL Journey Optimizer] supporta le notifiche push e ti aiuta a inviare notifiche altamente pertinenti a velocità di throughput leader di settore. Le notifiche push possono includere la personalizzazione e il contesto basato su Percorsi per sfruttare le informazioni sui dati del tuo marchio con Adobe Experience Cloud.

Questa pagina ti aiuterà a configurare e comprendere i servizi e i flussi di lavoro chiave coinvolti nelle notifiche push in [!DNL Journey Optimizer].

Passaggi per configurare il canale push in [!DNL Adobe Journey Optimizer] sono descritti in dettaglio in [questa pagina](push-configuration.md).

## Notifiche push e [!DNL Adobe Journey Optimizer]

L’immagine seguente mostra i sistemi e i servizi coinvolti nei flussi di dati associati, evidenziando il modo in cui le notifiche push vengono distribuite da un punto di vista di servizio end-to-end.

![](assets/push-flow.png)

1. Registrazione della tua app mobile di marca (Android o iOS) con APN di Apple e i servizi di messaggistica push FCM di Google
1. I servizi di messaggistica generano un token push, che è un identificatore che [!DNL Adobe Journey Optimizer] utilizzerà per eseguire il targeting del dispositivo specifico con una notifica push.
1. Il token push generato in precedenza viene passato a Adobe Experience Platform e sincronizzato con il profilo cliente in tempo reale; questo viene fatto OOTB con un SDK client facile da integrare
1. I messaggi push vengono creati in [!DNL Adobe Journey Optimizer], i messaggi push vengono creati rispetto a un predefinito messaggio
1. I messaggi push possono essere inclusi nell’area di lavoro orchestrazione nei Percorsi
1. Alla pubblicazione del Percorso, i profili cliente basati sulle condizioni del Percorso sono qualificati per ricevere notifiche push, in questo passaggio i payload di messaggi push vengono personalizzati
1. I payload push personalizzati vengono inoltrati a un servizio di consegna messaggi push interno
1. Il servizio interno convalida quindi le credenziali dell’app associata al messaggio e
1. Invia il messaggio ai servizi di messaggistica Apple e Google per la consegna finale
1. I feedback dai servizi di messaggistica sono notati, gli errori e i successi vengono registrati per la generazione di rapporti in Percorsi Live &amp; Global
1. Le notifiche push vengono inviate ai dispositivi degli utenti finali
1. Le interazioni di notifica push degli utenti finali vengono inviate come eventi di esperienza dal client dell’utente finale tramite l’integrazione SDK

## Ruoli dei servizi chiave nelle notifiche push

* **Provider di servizi di notifica push** sono i servizi web componenti di base che forniscono notifiche dai server remoti alle app mobili.

   [!DNL Adobe Journey Optimizer]  supporta sia le piattaforme Android che iOS e di conseguenza si integra con i seguenti elementi:
   * [FCM (Firebase Cloud Messaging)](https://firebase.google.com/docs/cloud-messaging) - per inviare notifiche all’app mobile Android
   * [APN (Apple Push Notification Service)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - per inviare notifiche all’app mobile iOS

* **Adobe Experience Platform Mobile SDK** che fornisce API di integrazione lato client per i dispositivi mobili tramite SDK compatibili con Android e iOS. L&#39;SDK fornisce un [!DNL Adobe Journey Optimizer] estensione che espone una varietà di API specifiche per i messaggi push e abilita il flusso di dati come la registrazione del token push o l’invio di eventi di tracciamento push o qualsiasi altro evento di esperienza personalizzato a Adobe Experience Platform. L’SDK fornisce anche una varietà di altre estensioni che abilitano altre funzionalità di Adobe Experience Cloud e di partner di terze parti.

   L&#39;integrazione SDK richiede anche la configurazione di Adobe Experience Platform [Raccolta dati](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=it){target=&quot;_blank&quot;} servizi quali:

   * Creazione di un datastream per configurare i set di dati evento di profilo ed esperienza in base ai quali i dati scorrono in Adobe Experience Platform
   * Creazione di proprietà mobili lato client e aggiunta di estensioni. L’SDK si integra strettamente con queste estensioni per fornire un’esperienza di raccolta dati fluida.
   * Registrazione dell&#39;identificatore del bundle dell&#39;app mobile e delle credenziali dell&#39;app

* **Profilo cliente in tempo reale Adobe Experience Platform**  mantiene una visione olistica di ogni singolo cliente combinando dati provenienti da più canali, tra cui web, dispositivi mobili, CRM e terze parti. Il profilo ti consente di consolidare i dati dei clienti in una visualizzazione unificata che offre un account utilizzabile e con marca temporale per ogni interazione con il cliente. Il token push per un determinato utente dell’app viene memorizzato nel profilo dell’utente come dati di record, mentre le interazioni che l’utente esegue con le notifiche push vengono tracciate come dati di eventi della serie temporale. [Ulteriori informazioni sul profilo cliente in tempo reale di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target=&quot;_blank&quot;}.

* **[!DNL Adobe Journey Optimizer]** : una volta che le integrazioni app mobili con i componenti di cui sopra sono state implementate e i profili dei clienti in Adobe Experience Platform, puoi creare e orchestrare notifiche push in [!DNL Adobe Journey Optimizer] per interagire con i tuoi utenti.

## Flussi di lavoro push per l’installazione tecnica e il professionista

L’immagine seguente mostra i vari passaggi, end-to-end, necessari per configurare i componenti che formano l’ossatura del flusso di dati push. Gli elementi azione sono stati organizzati in categorie in base al ruolo che esegue la configurazione e al componente che viene configurato.

![](assets/user-flow.png)
