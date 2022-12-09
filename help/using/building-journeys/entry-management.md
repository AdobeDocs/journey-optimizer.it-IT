---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle voci di profilo
description: Scopri come gestire l’accesso al profilo
feature: Journeys
role: User
level: Intermediate
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Gestione delle voci di profilo {#entry-management}

Per impostazione predefinita, i nuovi percorsi consentono il rientro. Puoi deselezionare l’opzione per i percorsi &quot;una tantum&quot;, ad esempio se desideri offrire un regalo una tantum quando una persona entra in un negozio. In tal caso, non vuoi che il cliente sia in grado di rientrare nel percorso e ricevere nuovamente l’offerta.

![](assets/journey-re-entrance.png)

Al termine di un percorso, il suo stato è **[!UICONTROL Closed]**. TNew individui non possono più entrare nel viaggio. Le persone già in viaggio finiscono il viaggio normalmente.

Dopo il timeout globale predefinito di 30 giorni, il percorso passa alla **Completato** stato.  [Ulteriori informazioni](journey-gs.md#global_timeout).


## Viaggi unitari{#entry-unitary}

I percorsi unitari (a partire da un evento o da una qualifica di segmento) includono una guardrail che impedisce l’attivazione errata dei percorsi più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non verrà più avviato per questo profilo.

Inoltre:

* Se l’opzione di rientro è abilitata, un profilo può accedere a un percorso diverse volte, ma non può farlo finché non esce completamente dall’istanza precedente del percorso.

* Se l’opzione di rientro è disabilitata, un profilo non può accedere più volte allo stesso percorso

## Lettura dei percorsi dei segmenti{#entry-read-segment}

In un percorso di segmento letto:

* Per i percorsi non ricorrenti: il profilo entra una sola volta nel percorso.

* Per i percorsi ricorrenti: il profilo accede al percorso di ogni ricorrenza, se si trova nello stato del segmento o previsto. Se era ancora nel percorso da una precedente ricorrenza, lo riavvierà dall&#39;inizio.

Nei percorsi degli eventi aziendali che iniziano con un **Leggi segmento** attività: sapendo che questo percorso si basa sulla ricezione di un evento di business, se il profilo è qualificato nel segmento previsto, entrerà nel percorso per ogni evento di business ricevuto, il che significa che questo profilo può essere più volte nello stesso percorso, allo stesso tempo, ma nel contesto di eventi di business diversi.
