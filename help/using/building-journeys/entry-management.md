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
version: Journey Orchestration
source-git-commit: 5eddbb1f9ab53f1666ccd8518785677018e10f6f
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 3%

---


# Gestione dell’ingresso del profilo {#entry-management}

La gestione dell’entrata del profilo dipende dal tipo di percorso.

## Tipi di percorsi {#types-of-journeys}

Con Adobe Journey Optimizer è possibile creare i seguenti tipi di percorsi:

* **Evento unitario** percorsi: questi percorsi iniziano con un evento unitario. Quando l’evento viene ricevuto, il profilo associato entra nel percorso. [Ulteriori informazioni](#entry-unitary)

* **Evento di business** percorsi: questi percorsi iniziano con un evento di business immediatamente seguito da un&#39;attività **Read audience**. Quando l’evento viene ricevuto, i profili appartenenti al pubblico di destinazione entrano nel percorso. Viene creata un’istanza di questo percorso per ogni profilo. [Ulteriori informazioni](#entry-business)

* **Read audience** percorsi: questi percorsi iniziano con un&#39;attività **Read audience**. Quando il percorso viene eseguito, i profili appartenenti al pubblico di destinazione entrano nel percorso. Viene creata un’istanza di questo percorso per ogni profilo. Questi percorsi possono essere ricorrenti o &quot;one-shot&quot;. [Ulteriori informazioni](#entry-read-audience)

* **Qualificazione del pubblico** percorsi: questi percorsi iniziano con un evento di qualificazione del pubblico. Questi percorsi ascoltano le entrate e le uscite dei profili nei tipi di pubblico. In questo caso, il profilo associato entra nel percorso. [Ulteriori informazioni](#entry-unitary)

In tutti i tipi di percorso, un profilo non può essere presente più volte nello stesso percorso, contemporaneamente, per tutte le [versioni attive del percorso](publishing-the-journey.md#journey-versions-journey-versions). Per verificare che una persona appartenga a un percorso, viene utilizzata come chiave l’identità del profilo. La stessa chiave, ad esempio la chiave `CRMID=3224`, non può trovarsi in posizioni diverse nello stesso percorso.

## Velocità di elaborazione percorso {#journey-processing-rate}

La velocità di elaborazione del percorso è influenzata da diversi fattori che determinano il modo in cui i profili passano attraverso un percorso:

### Percentuale di ingresso profilo {#profile-entrance-rate}

Il modo in cui i profili entrano nei percorsi e il loro tasso previsto dipende dalla prima attività utilizzata:

* **Leggi pubblico** percorsi (scenario batch, in cui si esegue il targeting di un pubblico di profili e si attiva un percorso per tale pubblico completo): il massimo è 20.000 TPS (transazioni al secondo), che è la quota disponibile a un **livello sandbox**. Se in tale sandbox sono in esecuzione più percorsi contemporaneamente, 20.000 TPS potrebbero non essere raggiungibili. Considera questo massimo come il migliore scenario possibile.

* **Qualificazione del pubblico** percorsi (scenario unitario, in cui si desidera attivare un percorso quando un profilo si qualifica o non si qualifica per un pubblico in streaming): il massimo è 5.000 TPS. Si tratta di un limite condiviso con i percorsi che iniziano con gli eventi e condiviso anche tra i percorsi a un **livello di organizzazione**.

* **Evento unitario** percorsi (scenario unitario, in cui si desidera attivare un percorso quando un evento viene emesso da un profilo): come sopra, entrambi condividono lo stesso limite di 5.000 TPS. Ulteriori informazioni sulla velocità effettiva degli eventi di percorso sono disponibili in [questa sezione](../event/about-events.md#event-thoughput).

* **Evento di business** percorsi (che è essenzialmente uno scenario unitario da batch in quanto un evento di business è sempre seguito da Read audience): gli eventi di business vengono conteggiati anche nella quota di 5.000 TPS, ma l&#39;attività Read audience immediatamente dopo avrà lo stesso limite dei percorsi che iniziano con Read audience (20.000 TPS).

### Eventi e qualifiche del pubblico all’interno dei percorsi {#events-inside-journeys}

Dopo l&#39;ingresso, puoi utilizzare **le attività evento unitario** o **qualificazione del pubblico** all&#39;interno del percorso. Un profilo può entrare in uno qualsiasi dei 4 tipi di percorsi descritti sopra e attendere che venga emesso un evento oppure aspettare che questo profilo sia idoneo per un pubblico. Tali eventi unitari e qualifiche del pubblico saranno conteggiati nel contingente descritto sopra. Ad esempio: se inizi un percorso con un pubblico Read (con un massimo di 20.000 TPS) e subito dopo hai un evento, questo non sarà superiore a 5.000 TPS.

### Impatto delle attività di attesa {#wait-activities-impact}

Le attività **Wait** in percorsi possono anche avere un impatto sul numero di profili che attraversano un percorso alla volta. In genere, un’attività Attendi si basa su un tempo relativo (ad esempio: uscita 2 ore dopo l’immissione dell’attesa, così tutti i profili non escono contemporaneamente). Tuttavia, se per l’attività Attendi è definito un tempo fisso, è possibile che più profili escano da quel percorso esattamente nello stesso momento. Questa non è una pratica consigliata. Si possono quindi vedere enormi volumi e il TPS da questo momento in poi può superare i 20.000 TPS.

### Attività di azione {#action-activities-impact}

Infine, le attività **action** (canali nativi come E-mail, SMS, Push e così via, in uscita o in entrata, Azioni personalizzate, Salti che inviano profili ad altri percorsi, Aggiorna profili che inviano dati al servizio profili unificato e così via) possono essere influenzate dal caricamento del profilo proveniente dai percorsi, ma anche dalla velocità di elaborazione. Ad esempio, un’azione personalizzata mirata a un endpoint esterno con un tempo di risposta elevato rallenterà la velocità di elaborazione del percorso.

Per le azioni personalizzate, il limite predefinito è di 300.000 chiamate al minuto, che possono essere modificate con un criterio di limite personalizzato. Ulteriori informazioni sulla limitazione delle azioni personalizzate in [questa sezione](../configuration/external-systems.md#capping).

## Percorsi unitari di qualificazione di eventi e pubblico{#entry-unitary}

In **Evento unitario** e **Qualificazione del pubblico** percorsi, puoi abilitare o disabilitare il rientro:

* Se la rientrata è abilitata, un profilo può entrare in un percorso diverse volte, ma non può farlo fino a quando non è completamente uscito dall&#39;istanza precedente del percorso.

* Se il rientro è disattivato, un profilo non può entrare più volte nello stesso percorso, entro il periodo di timeout del percorso globale. Consulta questa [sezione](../building-journeys/journey-properties.md#global_timeout).

Per impostazione predefinita, i percorsi consentono il rientro. Quando l&#39;opzione **Consenti rientro** è attivata, viene visualizzato il campo **Periodo di attesa rientro**. Consente di definire il tempo di attesa prima che un profilo possa entrare nuovamente nel percorso. In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti. La durata massima è di 91 giorni ([timeout globale](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

Dopo il periodo di rientro, i profili possono rientrare nel percorso. Per evitare questo problema e disabilitare completamente il rientro per tali profili, puoi aggiungere una condizione per verificare se il profilo è già stato inserito o meno, utilizzando i dati del profilo o del pubblico.

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## Percorsi lavorativi {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

In **percorsi lavorativi**, per consentire più esecuzioni di eventi aziendali, attiva l&#39;opzione corrispondente nella sezione **[!UICONTROL Esecuzione]** delle proprietà del percorso.

![](assets/business-entry.png)

Nel caso di eventi di business, per un determinato percorso, i dati sul pubblico recuperati alla prima esecuzione vengono riutilizzati durante un intervallo di tempo di 1 ora.

Un profilo può essere presente più volte nello stesso percorso, allo stesso tempo, ma nel contesto di diversi eventi di business.

Per ulteriori informazioni, consulta questa [sezione](../event/about-creating-business.md)

## Leggi percorsi di pubblico {#entry-read-audience}

**Read audience** i percorsi possono essere ricorrenti o &quot;one-shot&quot;:

* Per percorsi non ricorrenti/&quot;one-shot&quot;: il profilo entra una sola volta nel percorso.

* Per i percorsi ricorrenti: per impostazione predefinita, tutti i profili appartenenti al pubblico entrano nel percorso per ogni ricorrenza. Devono terminare il percorso prima di poter rientrare in un&#39;altra occorrenza.

Sono disponibili diverse opzioni per percorsi di pubblico Read ricorrenti. Per ulteriori informazioni, consulta la sezione [Utilizzare un pubblico in un percorso](../building-journeys/read-audience.md).

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
