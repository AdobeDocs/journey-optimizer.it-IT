---
solution: Journey Optimizer
product: journey optimizer
title: Sospendi un percorso
description: Scopri come mettere in pausa e riprendere un percorso live
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Disponibilità limitata" type="Informative"
keywords: pubblicazione, percorso, live, validità, verifica
source-git-commit: bb881f0257408ad70f3737c24d1caa28deea96e0
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 3%

---

# Sospendi un percorso {#journey-pause}

Puoi mettere in pausa i percorsi live, apportare tutte le modifiche necessarie e riprenderli in qualsiasi momento. <!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Il percorso viene ripreso automaticamente al termine del periodo di pausa. Puoi anche [riprenderla manualmente](#journey-resume-steps).


>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.


## Vantaggi chiave {#journey-dry-run-benefits}

I percorsi di pausa e ripresa offrono ai professionisti del percorso maggiore controllo e flessibilità, consentendo la sospensione temporanea dei percorsi live senza interrompere l’esperienza del cliente. Quando è in pausa, non vengono inviate comunicazioni e i profili rimangono in stato di sospensione fino alla ripresa del percorso.

Questa funzionalità riduce i rischi di invio di messaggi non desiderati durante errori o aggiornamenti (ad esempio, modifiche al contenuto dei messaggi), supporta una gestione più sicura del percorso e aumenta la fiducia degli utenti. La visibilità nei percorsi in pausa e il loro stato direttamente nell’interfaccia utente migliorano ulteriormente la trasparenza e l’agilità operativa.

>[!CAUTION]
>
>Le autorizzazioni per la sospensione e la ripresa dei percorsi sono limitate agli utenti con l&#39;autorizzazione di alto livello **[!DNL Publish journeys]**. Ulteriori informazioni sulla gestione dei diritti di accesso degli utenti [!DNL Journey Optimizer] in [questa sezione](../administration/permissions-overview.md).

## Guardrail e consigli

* Una versione di percorso può essere sospesa per un massimo di 14 giorni.
* I percorsi in pausa vengono considerati in tutte le regole aziendali, come se fossero in diretta.
* I profili vengono &quot;scartati&quot; in un percorso in pausa quando raggiungono un’attività di azione. Se rimangono in attesa durante il periodo di pausa e di uscita di un percorso dopo che è stato ripreso, continueranno il percorso e non verranno eliminati.
* Anche dopo la pausa, man mano che gli eventi continuano a essere elaborati, questi eventi verrebbero conteggiati nella quota relativa al numero di eventi di Percorso al secondo, dopo di che la limitazione viene visualizzata per l’impostazione unitaria.
* I profili che sono entrati nel percorso ma sono stati scartati durante la pausa vengono comunque conteggiati come profili coinvolgibili.
* Quando i profili rimangono in un percorso in pausa, al momento della ripresa gli attributi del profilo vengono aggiornati
* Le condizioni vengono comunque eseguite nei percorsi in pausa, quindi se un percorso è stato sospeso a causa di problemi di qualità dei dati, qualsiasi condizione precedente a un nodo di azione può essere valutata con dati errati.
* Per il percorso di pubblico di lettura incrementale basato sul pubblico, viene presa in considerazione la durata di pausa. Ad esempio, per un percorso giornaliero, se è stato messo in pausa il 2 e ripreso il 5 del mese, l’esecuzione il 6 prenderà tutti i profili qualificati dal 1° al 6. Questo non avviene per la qualificazione del pubblico o i percorsi basati su eventi (se una qualificazione del pubblico o un evento vengono ricevuti durante una pausa, tali eventi vengono scartati).
* I percorsi in pausa vengono conteggiati ai fini della quota di percorsi vivi.
* Il timeout globale del percorso si applica ancora ai percorsi in pausa. Ad esempio, se un profilo è rimasto in un percorso per 90 giorni e il percorso è in pausa, questo profilo uscirà comunque dal percorso il 91° giorno.
* Se i profili vengono mantenuti in un percorso e questo percorso riprende automaticamente dopo alcuni giorni, i profili continuano il percorso e non vengono eliminati. Se vuoi farli cadere, devi fermare il percorso.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Come sospendere un percorso {#journey-pause-steps}

Puoi mettere in pausa qualsiasi percorso live.

Per mettere in pausa il percorso, effettuare le seguenti operazioni:

1. Aprire il percorso che si desidera sospendere.
1. Fai clic sul pulsante **...More** nella sezione superiore destra dell&#39;area di lavoro del percorso e seleziona **Pause**.

   ![Pausa pulsante percorso](assets/pause-journey-button.png)

1. Seleziona la modalità di gestione dei profili attualmente presenti nel percorso.

   ![Opzioni di pausa percorso](assets/pause-confirm.png){width="50%" align="left"}

   Puoi eseguire le seguenti operazioni:

   * Profili blocco: i profili attendono la ripresa del percorso
   * Ignora profili: i profili verranno esclusi dal percorso nel nodo dell’azione successivo

1. Fai clic sul pulsante **Pausa** per confermare.

## Come riprendere un percorso in pausa {#journey-resume-steps}

I percorsi in pausa vengono ripresi automaticamente al termine del periodo massimo di pausa di 14 giorni. Possono essere ripresi manualmente in qualsiasi momento.

Per riprendere un percorso in pausa e ricominciare ad ascoltare gli eventi di percorso, effettuare le seguenti operazioni:

1. Aprire il percorso che si desidera riprendere.
1. Fai clic sul pulsante **...More** nella sezione superiore destra dell&#39;area di lavoro del percorso e seleziona **Riprendi**.

   Il percorso passa allo stato **Ripresa**. La transizione dallo stato **Ripresa** allo stato **Live** può richiedere un po&#39; di tempo: tutti i profili devono essere ripresi affinché il percorso sia di nuovo **Live**.




