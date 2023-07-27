---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle voci di profilo
description: Scopri come gestire la voce di profilo
feature: Journeys
role: User
level: Intermediate
keywords: rientro, percorso, profilo, ricorrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 14%

---


# Gestione delle voci di profilo {#entry-management}

Esistono due tipi principali di percorsi:

* percorsi basati su eventi: a partire da un evento, questi percorsi sono unitari, sono associati a un singolo individuo. Quando l’evento viene ricevuto, l’utente entra nel percorso. [Ulteriori informazioni](#entry-unitary)
* percorsi di pubblico di lettura: a partire da un pubblico di lettura, si tratta di percorsi batch. I singoli utenti appartenenti al pubblico entrano tutti nello stesso percorso. Questi percorsi possono essere ricorrenti o one-shot. [Ulteriori informazioni](#entry-read-segment)

In entrambi i tipi di percorso, un profilo non può essere presente più volte nello stesso percorso, contemporaneamente.

## Percorsi unitari{#entry-unitary}

Nei percorsi unitari, puoi abilitare o disabilitare il rientro:

* Se è abilitato il rientro, un profilo può entrare in un percorso diverse volte, ma non può farlo finché non è completamente uscito dall’istanza precedente del percorso.

* Se il rientro è disattivato, un profilo non può entrare più volte nello stesso percorso

Per impostazione predefinita, i nuovi percorsi consentono il rientro. È possibile deselezionare l’opzione per i percorsi &quot;one shot&quot; (una sola volta), ad esempio se si desidera offrire un regalo una tantum quando una persona entra in un negozio. In tal caso, non vuoi che il cliente possa reinserire il percorso e ricevere nuovamente l’offerta. Quando un percorso termina, il suo stato è **[!UICONTROL Chiuso]**. I nuovi utenti non possono più accedere al percorso. Le persone già nel percorso finiscono normalmente il percorso. [Ulteriori informazioni](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

Dopo il timeout globale predefinito di 30 giorni, il percorso passa alla **Completato** stato. I nuovi utenti non possono più accedere al percorso. Le persone già nel percorso finiscono normalmente il percorso.A causa del timeout del percorso di 30 giorni, quando il rientro del percorso non è consentito, non possiamo assicurarci che il blocco del rientro funzioni più di 30 giorni. Infatti, poiché si eliminano tutte le informazioni sulle persone che sono entrate nel percorso 30 giorni dopo il loro ingresso, non è possibile conoscere la persona che è entrata in precedenza, più di 30 giorni fa. [Ulteriori informazioni](journey-gs.md#global_timeout).

I percorsi unitari (a partire da un evento o da una qualificazione del pubblico) includono un guardrail che impedisce ai percorsi di essere attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.

La chiave viene utilizzata anche per verificare che una persona appartenga a un percorso. Infatti, una persona non può trovarsi in due luoghi diversi nello stesso percorso. Di conseguenza, il sistema non consente che la stessa chiave, ad esempio la chiave CRMID=3224, si trovi in luoghi diversi nello stesso percorso.

## Leggi percorsi di pubblico{#entry-read-segment}

In un percorso di pubblico lettura:

* Per percorsi non ricorrenti: il profilo entra una volta e solo una volta il percorso.

* Per i percorsi ricorrenti: per impostazione predefinita, tutti i profili appartenenti al pubblico entrano nel percorso per ogni ricorrenza. Devono terminare il percorso prima di poter rientrare in un&#39;altra occorrenza.

>[!NOTE]
>
>Sono disponibili due opzioni per percorsi di pubblico ricorrenti di lettura. Il **Forza rientro in caso di ricorrenza** fa in modo che tutti i profili ancora presenti nel percorso lo abbandonino automaticamente all’esecuzione successiva. Il **Lettura incrementale** L’opzione esegue il targeting solo delle persone che sono entrate nel pubblico dall’ultima esecuzione del percorso. Consulta questa [sezione](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

Nei percorsi di evento business che iniziano con **Read audience** attività: sapendo che questo percorso si basa sulla ricezione di un evento di business, se il profilo è qualificato nel pubblico previsto, entreranno nel percorso per ogni evento di business ricevuto, il che significa che questo profilo può essere più volte nello stesso percorso, allo stesso tempo, ma nel contesto di diversi eventi di business.