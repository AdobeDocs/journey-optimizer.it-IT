---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle voci di profilo
description: Scopri come gestire la voce di profilo
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: rientro, percorso, profilo, ricorrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 5%

---


# Gestione delle voci di profilo {#entry-management}

Esistono due tipi principali di percorsi:

* percorsi basati su eventi: a partire da un evento, questi percorsi sono unitari, sono associati a un singolo individuo. Quando l’evento viene ricevuto, l’utente entra nel percorso. [Ulteriori informazioni](#entry-unitary)
* percorsi di pubblico di lettura: a partire da un pubblico di lettura, si tratta di percorsi batch. I singoli utenti appartenenti al pubblico entrano tutti nello stesso percorso. Questi percorsi possono essere ricorrenti o one-shot. [Ulteriori informazioni](#entry-read-segment)

In entrambi i tipi di percorso, un profilo non può essere presente più volte nello stesso percorso, contemporaneamente.

## Percorsi unitari{#entry-unitary}

Nei percorsi unitari, puoi abilitare o disabilitare il rientro:

* Se è abilitato il rientro, un profilo può entrare in un percorso diverse volte, ma non può farlo finché non è completamente uscito dall’istanza precedente del percorso.

* Se il rientro è disattivato, un profilo non può entrare più volte nello stesso percorso.

Per impostazione predefinita, i nuovi percorsi consentono il rientro. È possibile deselezionare l’opzione per i percorsi &quot;one shot&quot; (una sola volta), ad esempio se si desidera offrire un regalo occasionale quando una persona visita un negozio. In tal caso, il cliente non deve essere in grado di rientrare nel percorso e ricevere nuovamente l’offerta. Quando un percorso termina, il suo stato è **[!UICONTROL Chiuso]**. I nuovi utenti non possono più accedere al percorso. Le persone già nel percorso finiscono normalmente il percorso. [Ulteriori informazioni](journey-gs.md#entrance)

Quando **Consenti rientro** è attivata, la **Periodo di attesa per rientro** Questo campo consente di definire il tempo di attesa prima che un profilo possa entrare nuovamente nel percorso. In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti. La durata massima è di 29 giorni.

![](assets/journey-re-entrance.png)

Dopo il valore predefinito [timeout globale](journey-gs.md#global_timeout) di 30 giorni, il percorso passa alla **Completato** stato. I profili già presenti nel percorso completano normalmente il percorso. I nuovi profili non possono più entrare nel percorso. Questo comportamento è impostato solo per 30 giorni (ossia per il valore predefinito di timeout del percorso), poiché tutte le informazioni sui profili che sono entrati nel percorso vengono rimosse 30 giorni dopo l’immissione. Dopo tale periodo, i profili possono rientrare nel percorso. Per evitare questo problema e disabilitare completamente il rientro per tali profili, puoi aggiungere una condizione per verificare se il profilo è già stato inserito o meno, utilizzando i dati del profilo o del pubblico.

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. -->

La chiave viene utilizzata per verificare che una persona appartenga a un percorso. Infatti, una persona non può trovarsi in due luoghi diversi nello stesso percorso. Di conseguenza, il sistema non consente che la stessa chiave, ad esempio la chiave CRMID=3224, si trovi in luoghi diversi nello stesso percorso.

## Leggi percorsi di pubblico{#entry-read-segment}

In un percorso di pubblico lettura:

* Per percorsi non ricorrenti: il profilo entra una volta e solo una volta il percorso.

* Per i percorsi ricorrenti: per impostazione predefinita, tutti i profili appartenenti al pubblico entrano nel percorso per ogni ricorrenza. Devono terminare il percorso prima di poter rientrare in un&#39;altra occorrenza.

>[!NOTE]
>
>Sono disponibili due opzioni per percorsi di pubblico ricorrenti di lettura. Il **Forza rientro in caso di ricorrenza** fa in modo che tutti i profili ancora presenti nel percorso lo abbandonino automaticamente all’esecuzione successiva. Il **Lettura incrementale** L’opzione esegue il targeting solo delle persone che sono entrate nel pubblico dall’ultima esecuzione del percorso. Consulta questa [sezione](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

Nei percorsi di evento business che iniziano con **Read audience** attività: sapendo che questo percorso si basa sulla ricezione di un evento di business, se il profilo è qualificato nel pubblico previsto, entreranno nel percorso per ogni evento di business ricevuto, il che significa che questo profilo può essere più volte nello stesso percorso, allo stesso tempo, ma nel contesto di diversi eventi di business.