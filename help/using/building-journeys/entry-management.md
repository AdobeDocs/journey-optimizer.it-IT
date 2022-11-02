---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle voci di profilo
description: Scopri come gestire l’accesso al profilo
feature: Journeys
role: User
level: Intermediate
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Gestione delle voci di profilo {#entry-management}

In un percorso unitario:

* Se la reintroduzione è abilitata, un profilo può entrare più volte in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso.

* Se l’opzione di rientro è disabilitata, un profilo non può entrare più volte nello stesso percorso

Per ulteriori informazioni sul rientro del profilo, consulta questo [sezione](../building-journeys/journey-gs.md#change-properties).

In un percorso di segmenti letto:

* Per percorsi non ricorrenti: il profilo entra una volta e una sola volta il percorso.
* per percorsi ricorrenti: il profilo entra nel percorso per ogni ricorrenza, se si trova nello stato del segmento o previsto. Se era ancora nel percorso da una precedente ricorrenza, lo riavvierà dall&#39;inizio.

In percorsi di eventi aziendali che iniziano con un segmento di lettura :

Sapendo che questo percorso è basato sulla ricezione di un evento aziendale, se il profilo è qualificato nel segmento previsto, entrerà nel percorso per ogni evento aziendale ricevuto, il che significa che questo profilo può essere più volte nello stesso percorso, allo stesso tempo, ma nel contesto di eventi commerciali diversi.

I percorsi unitari (a partire da un evento o da una qualifica di segmento) includono una guardrail che impedisce l’attivazione errata dei percorsi più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.
