---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle attività live
description: Scopri come inviare attività live in Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: df4183e15b2907bfb669e7e2e8eb88771627dcf4
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 21%

---

# Introduzione alle attività live {#get-started-mobile-live}


Le attività live sono elementi persistenti e facilmente visualizzabili dell’interfaccia utente visualizzati nella schermata di blocco del dispositivo. Consentono all’app di presentare informazioni aggiornate in tempo reale, mantenendo gli utenti informati durante un evento continuo senza dover aprire l’app o ricevere notifiche push ripetute.

>[!AVAILABILITY]
>
>L’attività live in Adobe Journey Optimizer è compatibile solo con Apple iOS.

A differenza delle notifiche push tradizionali, le attività live rappresentano **il coinvolgimento basato sullo stato**: anziché inviare avvisi una tantum, mantengono una presenza continua e contestuale che si aggiorna dinamicamente con l&#39;evolversi degli eventi.


![](assets/do-not-localize/live-activity.jpeg){width="30%" align="left"}

Con Adobe Journey Optimizer, puoi **avviare**, **aggiornare** e **terminare** attività live in modalità remota tramite campagne attivate da API, supportando casi d&#39;uso sia individuali che basati su pubblico su larga scala.

L&#39;attività live può essere **only** avviata tramite **campagne attivate da API**, consentendo di fornire payload personalizzati ed eseguire tutte le personalizzazioni tramite il proprio payload.
Il tipo di campagna **Attivato da API** appropriato deve essere selezionato in base al caso d&#39;uso dell&#39;attività Live prevista:

* Seleziona **Marketing attivato da API** per i casi di utilizzo di trasmissioni. Aggiornamenti basati sul pubblico inviati su larga scala:

   * Punteggi sportivi e conteggi di eventi live
   * Aggiornamenti dello stato dei voli per tutti i passeggeri di una rotta
   * Esperienze condivise in un segmento di utenti

* Seleziona **Transazionale attivato da API** per singoli casi d&#39;uso - 1:1 aggiornamenti in tempo reale per utente:

   * Tracciamento degli ordini e avanzamento della consegna
   * Aggiornamenti dello stato di guida o del servizio
   * Conferme di prenotazione e appuntamento in tempo reale

## Vantaggi chiave

Le attività live passano dal coinvolgimento mobile basato su notifiche a quello basato sullo stato, consentendo ai brand di:

* Mantenere una **presenza continua** nella schermata di blocco durante gli eventi di valore elevato
* **Aggiorna le informazioni in modo dinamico** senza sopraffare gli utenti con notifiche ripetute
* Distribuisci **momenti mobili più ricchi e contestuali** legati a eventi reali
* **Aumenta il coinvolgimento e la fidelizzazione** durante le transazioni attive o le esperienze live

## Guida introduttiva

Completa i passaggi seguenti per configurare e implementare l’attività Live nella tua applicazione:

1. **[Configurare Adobe Journey Optimizer](mobile-live-configuration.md)**

   Imposta l’ambiente creando una configurazione mobile.

1. **[Integrare Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   Integra Adobe Experience Platform Mobile SDK per abilitare gli aggiornamenti dinamici in tempo reale sulla schermata di blocco e sulla Dynamic Island.

1. **[Crea attività live in Journey Optimizer](create-mobile-live.md)**

   Utilizza le campagne attivate da API in Journey Optimizer per avviare la tua attività Live.

1. **[Tracciare le campagne](../reports/campaign-global-report-cja-activity.md)**

   Inizia a misurare l’impatto della tua attività Live con i rapporti incorporati.

## Video introduttivo

Scopri come configurare iOS Live Activities con Adobe Journey Optimizer per distribuire aggiornamenti avanzati e in tempo reale nella schermata di blocco di iPhone e su Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
