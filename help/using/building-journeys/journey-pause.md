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
source-git-commit: cd85b58350b4f8829aa1bc925c151be9b061b170
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 3%

---

# Sospendi un percorso {#journey-pause}

Puoi mettere in pausa i percorsi live, apportare tutte le modifiche necessarie e riprenderli in qualsiasi momento. Un percorso può essere sospeso per un massimo di 14 giorni. È possibile scegliere se riprendere il percorso alla fine del periodo di pausa o se arrestarlo completamente.


>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.


## Vantaggi chiave {#journey-dry-run-benefits}

I percorsi di pausa e ripresa offrono agli addetti al marketing maggiore controllo e flessibilità, consentendo la sospensione temporanea dei percorsi live senza interrompere la customer experience. Quando è in pausa, non vengono inviate comunicazioni e i profili rimangono in stato di sospensione fino alla ripresa del percorso.

Questa funzionalità riduce i rischi di invio di messaggi non desiderati durante errori o aggiornamenti (ad esempio, modifiche al contenuto dei messaggi), supporta una gestione più sicura del percorso e aumenta la fiducia degli utenti. La visibilità nei percorsi in pausa e il loro stato direttamente nell’interfaccia utente migliorano ulteriormente la trasparenza e l’agilità operativa.

>[!CAUTION]
>
>Le autorizzazioni per la sospensione e la ripresa dei percorsi sono limitate agli utenti con l&#39;autorizzazione di alto livello **[!DNL Publish journeys]**. Ulteriori informazioni sulla gestione dei diritti di accesso degli utenti [!DNL Journey Optimizer] in [questa sezione](../administration/permissions-overview.md).

## Guardrail e consigli

* Una versione di percorso può essere sospesa per un massimo di 14 giorni.
* I percorsi in pausa vengono considerati in tutte le regole aziendali, come se fossero in diretta.
* I profili vengono &quot;scartati&quot; in un percorso in pausa quando raggiungono un’attività di azione. Se rimangono in attesa durante il periodo di pausa e di uscita di un percorso che viene ripreso, continueranno il percorso e non verranno scartati.
* Anche dopo la pausa, man mano che gli eventi continuano a essere elaborati, questi eventi verrebbero conteggiati verso una quota di 5 ktps, dopodiché la limitazione verrà visualizzata per unitaria.
* I profili che sono entrati nel percorso ma sono stati scartati durante la pausa vengono comunque conteggiati come profili coinvolgibili.
* Quando i profili rimangono in un percorso in pausa, al momento della ripresa gli attributi del profilo vengono aggiornati
* Le condizioni vengono comunque eseguite nei percorsi in pausa, quindi se un percorso è stato sospeso a causa di problemi di qualità dei dati, qualsiasi condizione precedente a un nodo di azione può essere valutata con dati errati.
* Per il percorso di pubblico di lettura incrementale basato sul pubblico, viene presa in considerazione la durata di pausa. Ad esempio, per un percorso giornaliero, se è stato messo in pausa il 2 e ripreso il 5 del mese, l’esecuzione il 6 prenderà tutti i profili qualificati dal 1° al 6. Questo non avviene per la qualificazione del pubblico o i percorsi basati su eventi (se una qualificazione del pubblico o un evento vengono ricevuti durante una pausa, tali eventi vengono scartati).
* I percorsi in pausa vengono conteggiati ai fini della quota di percorsi vivi.
* Il timeout globale del percorso si applica ancora ai percorsi in pausa. Ad esempio, se un profilo è rimasto in un percorso per 90 giorni e il percorso è in pausa, questo profilo uscirà comunque dal percorso il 91° giorno.
* Al momento della ripresa di un percorso è disponibile un nuovo stato di **Ripresa** percorso. L&#39;ascolto degli eventi di percorso viene riavviato quando si fa clic su **Riprendi**.  Si verificano alcuni ritardi nella ripresa dei profili nel percorso. Quando il percorso passa da **Ripresa** a **Live**, significa che tutti i profili sono stati ripresi. **La ripresa** può quindi richiedere del tempo.
* Se i profili vengono mantenuti in un percorso e questo percorso riprende automaticamente dopo XX giorni, i profili continuano il percorso e non vengono eliminati. Se si desidera eliminarli, è necessario riprendere manualmente il percorso.
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

   * Profili blocco
   * Ignora profili

1. Fai clic sul pulsante **Pausa** per confermare.

Un percorso può essere sospeso per un massimo di 14 giorni.

## Come riprendere un percorso in pausa {#journey-resume-steps}

I percorsi in pausa possono essere ripresi manualmente in qualsiasi momento.

Per riprendere un percorso, effettuare le seguenti operazioni:

1. Aprire il percorso che si desidera riprendere.
1. Fai clic sul pulsante **...More** nella sezione superiore destra dell&#39;area di lavoro del percorso e seleziona **Riprendi**.




