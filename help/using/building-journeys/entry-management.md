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
source-git-commit: deb3646235377bf48b91b019e3442e4a3d6f0cf8
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 22%

---

# Gestione delle voci di profilo {#entry-management}

Per impostazione predefinita, i nuovi percorsi consentono il rientro. È possibile deselezionare l’opzione per i percorsi &quot;one shot&quot; (una sola volta), ad esempio se si desidera offrire un regalo una tantum quando una persona entra in un negozio. In tal caso, non vuoi che il cliente possa reinserire il percorso e ricevere nuovamente l’offerta.

![](assets/journey-re-entrance.png)

Quando un percorso termina, il suo stato è **[!UICONTROL Chiuso]**. I nuovi utenti non possono più accedere al percorso. Le persone già nel percorso finiscono normalmente il percorso.

Dopo il timeout globale predefinito di 30 giorni, il percorso passa alla **Completato** stato.  [Maggiori informazioni](journey-gs.md#global_timeout).


## Percorsi unitari{#entry-unitary}

I percorsi unitari (a partire da un evento o da una qualificazione del segmento) includono un guardrail che impedisce che i percorsi siano erroneamente attivati più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.

Inoltre:

* Se è abilitato il rientro, un profilo può entrare in un percorso diverse volte, ma non può farlo finché non è completamente uscito dall’istanza precedente del percorso.

* Se il rientro è disattivato, un profilo non può entrare più volte nello stesso percorso

## Leggi percorsi di segmenti{#entry-read-segment}

In un percorso Leggi segmento:

* Per percorsi non ricorrenti: il profilo entra una volta e solo una volta il percorso.

* Per i percorsi ricorrenti: il profilo entra nel percorso a ogni ricorrenza, se si trovano nello stato segmento/previsto. Se si trovavano ancora nel percorso dopo una precedente ricorrenza, lo riavvieranno dall’inizio.

Nei percorsi di evento business che iniziano con **Leggi segmento** attività: sapendo che questo percorso si basa sulla ricezione di un evento di business, se il profilo è qualificato nel segmento previsto, entreranno nel percorso per ogni evento di business ricevuto, il che significa che questo profilo può essere più volte nello stesso percorso, allo stesso tempo, ma nel contesto di diversi eventi di business.