---
solution: Journey Optimizer
product: journey optimizer
title: Flusso delle notifiche push in Adobe Journey Optimizer
description: Comprendere il flusso di dati e i componenti delle notifiche push
topic: Mobile
feature: Push, Overview
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 2%

---

# Flusso di dati e componenti delle notifiche push {#get-started-push}

Questa pagina consente di impostare e comprendere i servizi e i flussi di lavoro chiave coinvolti nelle notifiche push in [!DNL Journey Optimizer].


>[!AVAILABILITY]
>
>Il nuovo **flusso di lavoro di avvio rapido per l’onboarding per dispositivi mobili** è ora disponibile. Utilizza questa nuova funzione del prodotto per configurare rapidamente l’SDK di Mobile per iniziare a raccogliere e convalidare i dati dell’evento mobile e per inviare notifiche push per dispositivi mobili. Questa funzionalità è accessibile tramite la home page di Data Collection come versione beta pubblica. [Ulteriori informazioni](mobile-onboarding-wf.md)
>

Scopri come creare notifiche push su [questa pagina](create-push.md).

Passaggi per configurare il canale push in [!DNL Adobe Journey Optimizer] sono dettagliate su [questa pagina](push-configuration.md).

L’immagine seguente mostra i sistemi e i servizi coinvolti nei flussi di dati associati, evidenziando il modo in cui le notifiche push vengono distribuite dal punto di vista del servizio end-to-end.

![](assets/push-flow.png)

1. Registrazione dell’app mobile di marca (Android o iOS) con i servizi di messaggistica push APNs di Apple e Google FCM
1. I servizi di messaggistica generano un token push, che è un identificatore che [!DNL Adobe Journey Optimizer] utilizzerà per eseguire il targeting del dispositivo specifico con una notifica push.
1. Il token push generato in precedenza viene passato a Adobe Experience Platform e sincronizzato con Real-time Customer Profile; questa operazione viene eseguita OOTB con un SDK client di facile integrazione
1. I messaggi push vengono creati in [!DNL Adobe Journey Optimizer], i messaggi push vengono creati rispetto a una superficie di canale (ossia un predefinito per messaggi)
1. I messaggi push possono essere inclusi nell’area di lavoro di orchestrazione in Percorsi
1. Al momento della pubblicazione del Percorso, i profili cliente basati sulle condizioni del Percorso sono qualificati per ricevere notifiche push, e in questo passaggio i payload dei messaggi push sono personalizzati
1. I payload push personalizzati vengono inoltrati a un servizio di consegna di messaggi push interno
1. Questo servizio interno convalida quindi le credenziali dell’app associata al messaggio, e
1. Invia il messaggio ai servizi di messaggistica di Apple e Google per la consegna finale
1. I feedback dai servizi di messaggistica vengono annotati, gli errori e i successi vengono registrati per la generazione di rapporti nel Percorso Live &amp; Global
1. Le notifiche push vengono inviate ai dispositivi dell’utente finale
1. Le interazioni delle notifiche push per l’utente finale vengono inviate come eventi esperienza dal client dell’utente finale tramite l’integrazione SDK

## Ruoli dei servizi chiave nelle notifiche push {#roles-of-key-services}

* **Provider di servizi di notifica push** sono i servizi web dei componenti core che inviano notifiche da server remoti alle app mobili.

  [!DNL Adobe Journey Optimizer]  supporta sia le piattaforme Android che iOS e di conseguenza si integra con:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) - per inviare notifiche all’app mobile Android
   * [Servizio di notifica push di Apple (APNs)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - per inviare notifiche all’app mobile di iOS

* **SDK di Adobe Experience Platform Mobile** che fornisce API di integrazione lato client per i dispositivi mobili tramite SDK compatibili con Android e iOS. L’SDK fornisce un’ [!DNL Adobe Journey Optimizer] estensione che espone una varietà di API specifiche per i messaggi push e abilita il flusso di dati, come la registrazione del token push o l’invio di eventi di tracciamento push o qualsiasi altro evento di esperienza personalizzato a Adobe Experience Platform. L’SDK fornisce anche una serie di altre estensioni che consentono altre funzionalità di Adobe Experience Cloud e di partner di terze parti.

  L’integrazione dell’SDK richiede anche la configurazione di Adobe Experience Platform [Raccolta dati](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=it){target="_blank"} servizi quali:

   * Creazione di un flusso di dati per configurare il profilo e i set di dati evento di esperienza rispetto ai quali i dati fluiscono in Adobe Experience Platform
   * Creazione di proprietà mobili lato client e aggiunta di estensioni. L’SDK si integra strettamente con queste estensioni per fornire un’esperienza di raccolta dati fluida.
   * Registrazione dell’identificatore del bundle per app mobili e delle credenziali dell’app

* **Profilo cliente in tempo reale di Adobe Experience Platform**  mantiene una visione olistica di ogni singolo cliente combinando dati provenienti da più canali, inclusi web, mobile, CRM e di terze parti. Il profilo ti consente di consolidare i dati dei clienti in una visualizzazione unificata che offre un account utilizzabile e con marca temporale per ogni interazione con il cliente. Il token push per un determinato utente dell’app viene memorizzato sul profilo dell’utente come dati record, mentre le interazioni che l’utente effettua con le notifiche push vengono tracciate come dati di eventi di serie temporale. [Ulteriori informazioni su Adobe Experience Platform Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}.

* **[!DNL Adobe Journey Optimizer]** : una volta che le integrazioni dell’app mobile con i componenti sopra menzionati sono implementate e i profili cliente in Adobe Experience Platform, puoi creare e orchestrare le notifiche push in [!DNL Adobe Journey Optimizer] per interagire con i tuoi utenti.

## Eseguire il push della configurazione tecnica e dei flussi di lavoro degli utenti {#push-technical-setup}

La figura seguente mostra i vari passaggi, end-to-end, coinvolti nella configurazione dei componenti che formano l’ossatura del flusso di dati push. Le azioni sono state suddivise in categorie in base al ruolo che esegue la configurazione e al componente configurato.

![](assets/user-flow.png)

**Argomenti correlati**

* [Configurare il canale push](push-configuration.md)
* [Rapporto notifiche push](../reports/journey-global-report.md#push-global)
* [Creare una notifica push](create-push.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
* [Aggiungere un messaggio in una campagna](../campaigns/create-campaign.md)