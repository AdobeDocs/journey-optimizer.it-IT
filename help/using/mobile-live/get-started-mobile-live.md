---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle attività live
description: Scopri come inviare le attività live in Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 100%

---

# Introduzione alle attività live {#get-started-mobile-live}

>[!AVAILABILITY]
>
>L’attività live in Journey Optimizer è compatibile solo con iOS.

Le attività live forniscono aggiornamenti in tempo reale ed esperienze interattive all’interno delle app per dispositivi mobili, consentendo agli utenti di rimanere informati sugli eventi in corso o sulle attività direttamente sullo schermo del proprio dispositivo.

Questa funzione migliora il coinvolgimento fornendo informazioni in tempo reale, come tracciamento dell’avanzamento, aggiornamenti degli eventi o contenuti interattivi, senza richiedere agli utenti di aprire l’app.

Le attività live possono essere avviate **solo** tramite campagne **attivate da API**, consentendoti di fornire payload personalizzati ed eseguire tutte le personalizzazioni tramite il payload.
Il tipo di campagne **attivate da API** appropriato deve essere selezionato in base al caso d’uso dell’attività live prevista:

* Seleziona **Marketing attivato da API** per campagne basate su pubblico

  Progettato per comunicazioni basate su segmenti o tipi di pubblico in cui lo stesso aggiornamento viene inviato a più utenti, ad esempio punteggi sportivi, aggiornamenti di eventi, esperienze condivise.

* Seleziona **Transazionale attivato da API** per le campagne individuali

  Singoli utenti previsti identificati dal relativo profilo, ad esempio lo stato dell’ordine e il tracciamento della consegna.

## Guida introduttiva

Completa i passaggi di seguito per configurare e implementare le attività live nella tua applicazione:

1. **[Configurare Adobe Journey Optimizer](mobile-live-configuration.md)**

   Imposta l’ambiente creando una configurazione mobile.

1. **[Integrare Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   Integra Adobe Experience Platform Mobile SDK per abilitare gli aggiornamenti dinamici in tempo reale sulla schermata di blocco e sulla Dynamic Island.

1. **[Creare attività live in Journey Optimizer](create-mobile-live.md)**

   Utilizza le campagne attivate da API in Journey Optimizer per iniziare le attività live.

1. **[Tracciare le campagne](../reports/campaign-global-report-cja-activity.md)**

   Inizia a misurare l’impatto delle attività live con i rapporti incorporati.
