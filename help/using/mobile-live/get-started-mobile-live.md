---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle attività live
description: Scopri come inviare le attività live in Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: c6b36f31af29d21053cc455fd5dbba68ed5af63b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 20%

---

# Introduzione alle attività live {#get-started-mobile-live}


Le attività live sono elementi persistenti e facilmente visualizzabili dell’interfaccia utente visualizzati nella schermata di blocco del dispositivo. Consentono all’app di presentare informazioni aggiornate in tempo reale, mantenendo gli utenti informati durante un evento continuo senza dover aprire l’app o ricevere notifiche push ripetute.

>[!AVAILABILITY]
>
>Le attività live in Adobe Journey Optimizer sono compatibili solo con Apple iOS.

A differenza delle notifiche push tradizionali, le attività live rappresentano **il coinvolgimento basato sullo stato**: anziché inviare avvisi una tantum, mantengono una presenza continua e contestuale che si aggiorna dinamicamente con l&#39;evolversi degli eventi.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="Attività iOS Live su schermata di blocco e isola dinamica" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Vantaggi chiave</strong></p>
<p>Le attività live spostano il coinvolgimento mobile da basato su notifiche a basato su stato, consentendo ai brand di:</p>
<ul>
<li>Mantenere una <strong>presenza continua</strong> nella schermata di blocco durante gli eventi di valore elevato</li>
<li><strong>Aggiorna le informazioni in modo dinamico</strong> senza sopraffare gli utenti con notifiche ripetute</li>
<li>Distribuisci <strong>momenti mobili più ricchi e contestuali</strong> legati a eventi reali</li>
<li><strong>Aumenta il coinvolgimento e la fidelizzazione</strong> durante le transazioni attive o le esperienze live</li>
</ul>
</td>
</tr>
</table>

Con Adobe Journey Optimizer, puoi **avviare**, **aggiornare** e **terminare** attività live in modalità remota tramite campagne attivate da API, supportando casi d&#39;uso sia individuali che basati su pubblico su larga scala.

Le attività live possono **solo** essere avviate tramite **campagne attivate da API**, consentendoti di fornire payload personalizzati ed eseguire tutte le personalizzazioni tramite il tuo payload.
Il tipo di campagna **Attivato da API** appropriato deve essere selezionato in base al caso d&#39;uso dell&#39;attività Live prevista:

* Seleziona **Marketing attivato da API** per i casi di utilizzo di trasmissioni. Aggiornamenti basati sul pubblico inviati su larga scala:

   * Punteggi sportivi e conteggi di eventi live
   * Aggiornamenti dello stato dei voli per tutti i passeggeri di una rotta
   * Esperienze condivise in un segmento di utenti

* Seleziona **Transazionale attivato da API** per singoli casi d&#39;uso - 1:1 aggiornamenti in tempo reale per utente:

   * Tracciamento degli ordini e avanzamento della consegna
   * Aggiornamenti dello stato di guida o del servizio
   * Conferme di prenotazione e appuntamento in tempo reale

## Guida introduttiva

Completa i passaggi di seguito per configurare e implementare le attività live nella tua applicazione:

1. **[Configurare Adobe Journey Optimizer](mobile-live-configuration.md)**

   Imposta l’ambiente creando una configurazione mobile.

1. **[Integrare Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   Integra Adobe Experience Platform Mobile SDK per abilitare gli aggiornamenti dinamici in tempo reale sulla schermata di blocco e sulla Dynamic Island.

1. **[Crea un&#39;attività Live in Journey Optimizer](create-mobile-live.md)**

   Utilizza le campagne attivate da API in Journey Optimizer per avviare la tua attività Live.

1. **[Tracciare le campagne](../reports/campaign-global-report-cja-activity.md)**

   Inizia a misurare l’impatto della tua attività Live con i rapporti incorporati.

## Video introduttivo

Scopri come configurare le attività iOS Live con Adobe Journey Optimizer per distribuire aggiornamenti avanzati e in tempo reale sulla schermata di blocco di iPhone e su Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
