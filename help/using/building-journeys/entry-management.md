---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle voci di profilo
description: Scopri come gestire l’accesso al profilo
feature: Journeys
role: User
level: Intermediate
keywords: rientro, percorso, profilo, ricorrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 22%

---

# Gestione delle voci di profilo {#entry-management}

Per impostazione predefinita, i nuovi percorsi consentono il rientro. È possibile deselezionare l&#39;opzione per percorsi &quot;una ripresa&quot;, ad esempio se si desidera offrire un regalo una tantum quando una persona entra in un negozio. In tal caso, non vuoi che il cliente sia in grado di reinserire il percorso e ricevere nuovamente l&#39;offerta.

![](assets/journey-re-entrance.png)

Al termine di un percorso, il suo stato è **[!UICONTROL Chiuso]**. I nuovi individui non possono più entrare nel percorso. Le persone già nel percorso finiscono il percorso normalmente.

Dopo il timeout globale predefinito di 30 giorni, il percorso passa alla **Completato** stato.  [Maggiori informazioni](journey-gs.md#global_timeout).


## Percorsi unitari{#entry-unitary}

I percorsi unitari (a partire da un evento o da una qualificazione del segmento) includono un guardrail che impedisce che i percorsi siano erroneamente attivati più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.

Inoltre:

* Se la reintroduzione è abilitata, un profilo può entrare più volte in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso.

* Se l’opzione di rientro è disabilitata, un profilo non può entrare più volte nello stesso percorso

## Leggi percorsi di segmenti{#entry-read-segment}

In un percorso di segmenti letto:

* Per percorsi non ricorrenti: il profilo entra una volta e una sola volta il percorso.

* Per percorsi ricorrenti: il profilo entra nel percorso per ogni ricorrenza, se si trova nello stato del segmento o previsto. Se era ancora nel percorso da una precedente ricorrenza, lo riavvierà dall&#39;inizio.

In percorsi di eventi aziendali che iniziano con un **Leggi segmento** attività: sapendo che questo percorso è basato sulla ricezione di un evento aziendale, se il profilo è qualificato nel segmento previsto, entrerà nel percorso per ogni evento aziendale ricevuto, il che significa che questo profilo può essere più volte nello stesso percorso, allo stesso tempo, ma nel contesto di eventi commerciali diversi.
