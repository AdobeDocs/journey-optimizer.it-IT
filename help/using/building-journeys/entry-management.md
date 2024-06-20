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
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 5%

---


# Gestione dell’ingresso nel profilo {#entry-management}

Esistono quattro tipi di percorsi:

* **Evento unitario** percorsi: questi percorsi iniziano con un evento Unitario. Quando l’evento viene ricevuto, il profilo associato entra nel percorso. [Ulteriori informazioni](#entry-unitary)

* **Evento di business** percorsi: questi percorsi iniziano con un evento Business immediatamente seguito da un pubblico Read. Quando l’evento viene ricevuto, i profili appartenenti al pubblico di destinazione entrano nel percorso. Verrà creata un’istanza di questo percorso per ogni profilo. [Ulteriori informazioni](#entry-business)

* **Read audience** percorsi: questi percorsi iniziano con un pubblico Read. Quando il percorso viene eseguito, i profili appartenenti al pubblico di destinazione entrano nel percorso. Verrà creata un’istanza di questo percorso per ogni profilo. Questi percorsi possono essere ricorrenti o one-shot. [Ulteriori informazioni](#entry-read-audience)

* **Qualificazione del pubblico** percorsi: questi percorsi iniziano con un evento di qualificazione del pubblico. Questi percorsi ascoltano le entrate e le uscite dei profili nei tipi di pubblico. In questo caso, il profilo associato entra nel percorso. [Ulteriori informazioni](#entry-unitary)

In tutti i tipi di percorso, un profilo non può essere presente più volte nello stesso percorso, contemporaneamente. Per verificare che una persona appartenga a un percorso, viene utilizzata come chiave l’identità del profilo. Il sistema non consente che la stessa chiave, ad esempio la chiave CRMID=3224, si trovi in posizioni diverse nello stesso percorso.

## Percorsi unitari di qualificazione di eventi e pubblico{#entry-unitary}

Nei percorsi di qualificazione Unitaria di eventi e pubblico, puoi abilitare o disabilitare il rientro:

* Se è abilitato il rientro, un profilo può entrare in un percorso diverse volte, ma non può farlo finché non è completamente uscito dall’istanza precedente del percorso.

* Se il rientro è disattivato, un profilo non può entrare più volte nello stesso percorso, entro il periodo di timeout del percorso globale. Consulta questa [sezione](../building-journeys/journey-properties.md#global_timeout).

Per impostazione predefinita, i percorsi consentono il rientro. Quando **Consenti rientro** è attivata, la **Periodo di attesa per rientro** viene visualizzato. Consente di definire il tempo di attesa prima che un profilo possa entrare nuovamente nel percorso. In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti. La durata massima è di 91 giorni ([timeout globale](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

Dopo il periodo di rientro, i profili possono rientrare nel percorso. Per evitare questo problema e disabilitare completamente il rientro per tali profili, puoi aggiungere una condizione per verificare se il profilo è già stato inserito o meno, utilizzando i dati del profilo o del pubblico.

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## Percorsi lavorativi{#entry-business}

<!--
Business events follow re-entrance rules in the same way as for unitary events. If a journey allows re-entrance, the next business event will be processed.
-->

Per consentire più esecuzioni di eventi business, attiva l’opzione corrispondente nella **[!UICONTROL Esecuzione]** della sezione delle proprietà del percorso.

![](assets/business-entry.png)

Nel caso di eventi di business, per un determinato percorso, i dati sul pubblico recuperati alla prima esecuzione vengono riutilizzati durante un intervallo di tempo di 1 ora.

Un profilo può essere presente più volte nello stesso percorso, allo stesso tempo, ma nel contesto di diversi eventi di business.

Per ulteriori informazioni, consulta questa [sezione](../event/about-creating-business.md)

## Leggi percorsi di pubblico{#entry-read-audience}

Leggi percorsi di pubblico può essere ricorrente o occasionale:

* Per percorsi non ricorrenti: il profilo entra una volta e solo una volta il percorso.

* Per i percorsi ricorrenti: per impostazione predefinita, tutti i profili appartenenti al pubblico entrano nel percorso per ogni ricorrenza. Devono terminare il percorso prima di poter rientrare in un&#39;altra occorrenza.

Per i percorsi di pubblico Leggi ricorrenti sono disponibili due opzioni:

* **Lettura incrementale** opzione: quando un percorso con un **Read audience** viene eseguito per la prima volta, tutti i profili nel pubblico entrano nel percorso. Questa opzione consente di eseguire il targeting, dopo la prima occorrenza, solo delle persone che sono entrate nel pubblico dall’ultima esecuzione del percorso.

  >[!NOTE]
  >
  >Se esegui il targeting di un [pubblico di caricamento personalizzato](../audience/about-audiences.md#segments-in-journey-optimizer) nel tuo percorso, i profili vengono recuperati solo alla prima ricorrenza se questa opzione è abilitata in un percorso ricorrente, in quanto questi tipi di pubblico sono fissi.

* **Forza rientro in caso di ricorrenza**: questa opzione ti consente di far uscire automaticamente tutti i profili ancora presenti nel percorso all’esecuzione successiva. Se la durata dei profili in questo percorso può essere più lunga della frequenza di ricorrenza (ad esempio, se utilizzi le attività Attendi), non attivare questa opzione per assicurarti che i profili possano terminare il percorso.

![](assets/read-audience-options.png)

Per ulteriori informazioni, consulta questa [sezione](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
