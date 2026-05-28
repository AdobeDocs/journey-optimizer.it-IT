---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle attività live
description: Scopri come inviare le attività live in Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
TQID: https://experienceleague.adobe.com/IB00r0QSfCthvgvyqubGwsaUoiJKBL-E96duLn4R5i0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909id: ed2fba79-65cb-4680-96d2-2ad5d851714did: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 404
ht-degree: 94%

---

# Introduzione alle attività live {#get-started-mobile-live}


Le attività live sono elementi dell’interfaccia utente persistenti e facilmente consultabili mostrati nella schermata di blocco del dispositivo. Consentono all’app di presentare informazioni aggiornate in tempo reale, mantenendo gli utenti informati durante un evento continuo, senza che debbano aprire l’app o ricevere notifiche push ripetute.

>[!AVAILABILITY]
>
>Le attività live in Journey Optimizer sono compatibili solo con Apple iOS.

A differenza delle notifiche push tradizionali, le attività live rappresentano un **coinvolgimento basato sullo stato**: anziché inviare avvisi una tantum, mantengono una presenza continua e contestuale che si aggiorna dinamicamente con l’evolversi degli eventi.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="iOS Live Activities su schermata di blocco e Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Vantaggi chiave</strong></p>
<p>Le attività live spostano il coinvolgimento su dispositivi mobili dalle notifiche allo stato, consentendo ai brand di:</p>
<ul>
<li>Mantenere una <strong>presenza continua</strong> nella schermata di blocco durante gli eventi di valore elevato</li>
<li><strong>Aggiornare le informazioni in modo dinamico</strong> senza sopraffare gli utenti con notifiche ripetute</li>
<li>Offrire momenti su dispositivi mobili <strong>più ricchi e contestuali</strong> legati a eventi reali</li>
<li><strong>Aumentare il coinvolgimento e la fidelizzazione</strong> durante le transazioni attive o le esperienze live</li>
</ul>
</td>
</tr>
</table>

Con Adobe Journey Optimizer, puoi **avviare**, **aggiornare** e **terminare** le attività live da remoto in modo programmatico tramite campagne attivate da API, supportando casi d’uso sia individuali che basati sul pubblico su larga scala.

Le attività live possono **solo** essere avviate tramite **campagne attivate da API**, consentendoti di fornire payload personalizzati ed eseguire tutte le personalizzazioni tramite il tuo payload.
Il tipo di campagna **Attivato da API** appropriato deve essere selezionato in base al caso di utilizzo dell&#39;attività Live prevista:

* Seleziona **Marketing attivato da API** per i casi d’uso di trasmissioni; aggiornamenti basati sul pubblico inviati su larga scala:

   * Punteggi sportivi e conti alla rovescia di eventi live
   * Aggiornamenti dello stato dei voli per tutti i passeggeri di una tratta
   * Esperienze condivise in un segmento di utenti

* Seleziona **Transazionale attivato da API** per singoli casi d’uso; aggiornamenti in tempo reale per utente 1:1:

   * Tracciamento degli ordini e avanzamento della consegna
   * Aggiornamenti sullo stato della corsa o del servizio
   * Conferme di prenotazione e appuntamento in tempo reale

## Guida introduttiva

Completa i passaggi di seguito per configurare e implementare le attività live nella tua applicazione:

1. **[Configurare Adobe Journey Optimizer](mobile-live-configuration.md)**

   Imposta l’ambiente creando una configurazione mobile.

1. **[Integrare Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   Integra Adobe Experience Platform Mobile SDK per abilitare gli aggiornamenti dinamici in tempo reale sulla schermata di blocco e sulla Dynamic Island.

1. **[Creare attività live in Journey Optimizer](create-mobile-live.md)**

   Utilizza le campagne attivate da API in Journey Optimizer per iniziare le attività live.

1. **[Tracciare le campagne](../reports/campaign-global-report-cja-activity.md)**

   Inizia a misurare l’impatto della tua attività live con i rapporti incorporati.

## Video dimostrativo

Scopri come configurare iOS Live Activities con Adobe Journey Optimizer per offrire aggiornamenti avanzati e in tempo reale nella schermata di blocco di iPhone e su Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
