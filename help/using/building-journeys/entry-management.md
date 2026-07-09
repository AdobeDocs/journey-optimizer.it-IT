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
TQID: https://experienceleague.adobe.com/li1WSyhVKq58N-FiTEL51gX-u911JVyZXcnBZtwNhDE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 2472bfde2c99dff384b11c66613370d369344f39
workflow-type: tm+mt
source-wordcount: 1875
ht-degree: 2%

---

# Gestione dell’ingresso del profilo {#entry-management}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come funzionano l&#39;entrata e la rientrata del profilo per ogni tipo di percorso in modo da poter controllare quando e con quale frequenza i profili entrano nei tuoi percorsi.

>[!ENDSHADEBOX]

La gestione dell’entrata del profilo dipende dal tipo di percorso.

>[!TIP]
>
>Cerchi indicazioni pratiche con esempi reali? Consulta la [guida completa ai criteri di entrata e di uscita dal percorso](entry-exit-criteria-guide.md), che include casi d&#39;uso come campagne di benvenuto, recupero del carrello abbandonato e programmi fedeltà con esempi completi di configurazione di entrata e uscita.

## Tipi di percorsi {#types-of-journeys}

Con [!DNL Adobe Journey Optimizer] è possibile creare i seguenti tipi di percorsi:

* **Evento unitario** percorsi: questi percorsi iniziano con un evento unitario. Quando l’evento viene ricevuto, il profilo associato entra nel percorso. [Ulteriori informazioni](#entry-unitary)

* **Evento di business** percorsi: questi percorsi iniziano con un evento di business immediatamente seguito da un&#39;attività **Read audience**. Quando l’evento viene ricevuto, i profili appartenenti al pubblico di destinazione entrano nel percorso. Viene creata un’istanza di questo percorso per ogni profilo. [Ulteriori informazioni](#entry-business)

* **Read audience** percorsi: questi percorsi iniziano con un&#39;attività **Read audience**. Quando il percorso viene eseguito, i profili appartenenti al pubblico di destinazione entrano nel percorso. Viene creata un’istanza di questo percorso per ogni profilo. Questi percorsi possono essere ricorrenti o &quot;one-shot&quot;. [Ulteriori informazioni](#entry-read-audience)

* **Qualificazione del pubblico** percorsi: questi percorsi iniziano con un evento di qualificazione del pubblico. Questi percorsi ascoltano le entrate e le uscite dei profili nei tipi di pubblico. In questo caso, il profilo associato entra nel percorso. [Ulteriori informazioni](#entry-unitary)

[Confronta tutti i tipi di percorso con casi d’uso →](journey.md#journey-types)

In tutti i tipi di percorso, un profilo non può essere presente più volte nello stesso percorso, contemporaneamente, per tutte le [versioni attive del percorso](publish-journey.md#journey-versions). Per verificare che una persona appartenga a un percorso, viene utilizzata come chiave l’identità del profilo. La stessa chiave, ad esempio la chiave `CRMID=3224`, non può trovarsi in posizioni diverse nello stesso percorso.

## Velocità di elaborazione percorso {#journey-processing-rate}

La velocità di elaborazione del percorso è influenzata da diversi fattori che determinano il modo in cui i profili passano attraverso un percorso:

### Percentuale di ingresso profilo {#profile-entrance-rate}

Il modo in cui i profili entrano nei percorsi e il loro tasso previsto dipende dalla prima attività utilizzata:

* **Leggi pubblico** percorsi (scenario batch, in cui si esegue il targeting di un pubblico di profili e si attiva un percorso per tale pubblico completo): il massimo è 20.000 TPS (transazioni al secondo). Questa è la quota disponibile a un **livello sandbox**. Se più percorsi vengono eseguiti contemporaneamente in quella sandbox, 20.000 TPS potrebbero non essere raggiungibili. Considera questo massimo come uno scenario migliore.

* **Qualificazione del pubblico** percorsi (scenario unitario, in cui si desidera attivare un percorso quando un profilo si qualifica o non si qualifica per un pubblico in streaming): il massimo è 5.000 TPS. Si tratta di un limite condiviso con i percorsi che iniziano con gli eventi e condiviso anche tra i percorsi a un **livello di organizzazione**.

* **Evento unitario** percorsi (scenario unitario, in cui si desidera attivare un percorso quando un evento viene emesso da un profilo): come sopra, entrambi condividono lo stesso limite di 5.000 TPS. Ulteriori informazioni sulla velocità effettiva degli eventi di percorso sono disponibili in [questa sezione](../event/about-events.md#event-thoughput).

* **Evento di business** percorsi (uno scenario unitario-batch perché un evento di business è sempre seguito da un Read audience): gli eventi di business vengono conteggiati per la quota di 5.000 TPS. L’attività Read audience che segue ha lo stesso limite dei percorsi che iniziano con Read audience (20.000 TPS).

### Eventi e qualifiche del pubblico all’interno dei percorsi {#events-inside-journeys}

Dopo l&#39;ingresso, puoi utilizzare **le attività evento unitario** o **qualificazione del pubblico** all&#39;interno del percorso. Un profilo può entrare in uno qualsiasi dei 4 tipi di percorsi descritti sopra e attendere che venga emesso un evento oppure aspettare che questo profilo sia idoneo per un pubblico. Tali eventi unitari e qualifiche del pubblico saranno conteggiati nel contingente descritto sopra. Ad esempio: se inizi un percorso con un pubblico Read (con un massimo di 20.000 TPS) e subito dopo hai un evento, questo non sarà superiore a 5.000 TPS.

### Impatto delle attività di attesa {#wait-activities-impact}

Le attività **Wait** in percorsi possono anche avere un impatto sul numero di profili che attraversano un percorso alla volta. In genere, un’attività Attendi si basa su un tempo relativo (ad esempio: uscita 2 ore dopo l’immissione dell’attesa, così tutti i profili non escono contemporaneamente). Tuttavia, se per l’attività Attendi è definito un tempo fisso, è possibile che più profili escano da quel percorso esattamente nello stesso momento. Questa non è una pratica consigliata. Si possono quindi vedere enormi volumi e il TPS da questo momento in poi può superare i 20.000 TPS.

### Attività di azione {#action-activities-impact}

Infine, le attività **action** possono essere influenzate dal caricamento del profilo proveniente dai percorsi e possono anche influenzare la velocità di elaborazione. Questi includono canali nativi come e-mail, SMS e push, azioni personalizzate, passaggi ad altri percorsi e attività di aggiornamento del profilo. Ad esempio, un’azione personalizzata mirata a un endpoint esterno con un tempo di risposta elevato rallenterà la velocità di elaborazione del percorso.

Per le azioni personalizzate, il limite predefinito è di 300.000 chiamate al minuto, che possono essere modificate con un criterio di limite personalizzato. Ulteriori informazioni sulla limitazione delle azioni personalizzate in [questa sezione](../configuration/external-systems.md#capping).

## Percorsi unitari di qualificazione di eventi e pubblico{#entry-unitary}

In **Evento unitario** e **Qualificazione del pubblico** percorsi, puoi abilitare o disabilitare il rientro:

* Se la rientrata è abilitata, un profilo può entrare in un percorso diverse volte, ma non può farlo fino a quando non è completamente uscito dall&#39;istanza precedente del percorso.

* Se il rientro è disattivato, un profilo non può entrare più volte nello stesso percorso, entro il periodo di timeout del percorso globale. Consulta questa [sezione](../building-journeys/journey-properties.md#global_timeout).

Per impostazione predefinita, i percorsi consentono il rientro. Quando l&#39;opzione **Consenti rientro** è attivata, viene visualizzato il campo **Periodo di attesa rientro**. Consente di definire il tempo di attesa prima che un profilo possa entrare nuovamente nel percorso. In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti. La durata massima è di 90 giorni ([timeout globale](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![Attivazione/disattivazione impostazioni rientro nelle proprietà del percorso](assets/journey-re-entrance.png)

Dopo il periodo di rientro, i profili possono rientrare nel percorso. Per evitare questo problema e disabilitare completamente il rientro per tali profili, puoi aggiungere una condizione per verificare se il profilo è già stato inserito o meno, utilizzando i dati del profilo o del pubblico.

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. 
-->

## Percorsi lavorativi {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

In **percorsi lavorativi**, per consentire più esecuzioni di eventi aziendali, attiva l&#39;opzione corrispondente nella sezione **[!UICONTROL Esecuzione]** delle proprietà del percorso.

![Opzioni di gestione voci evento business nella configurazione di percorso](assets/business-entry.png)

Nel caso di eventi di business, per un determinato percorso, i dati sul pubblico recuperati alla prima esecuzione vengono riutilizzati durante un intervallo di tempo di 1 ora.

Un profilo può essere presente più volte nello stesso percorso, allo stesso tempo, ma nel contesto di diversi eventi di business.

Per ulteriori informazioni, consulta questa [sezione](../event/about-creating-business.md)

## Leggi percorsi di pubblico {#entry-read-audience}

**Read audience** i percorsi possono essere ricorrenti o non ricorrenti:

* Per percorsi non ricorrenti: il profilo entra una volta e una sola volta nel percorso.

* Per i percorsi ricorrenti: per impostazione predefinita, tutti i profili appartenenti al pubblico entrano nel percorso per ogni ricorrenza. Devono terminare il percorso prima di poter rientrare in un&#39;altra occorrenza.

Sono disponibili diverse opzioni per percorsi di pubblico Read ricorrenti. Per ulteriori informazioni, consulta la sezione [Utilizzare un pubblico in un percorso](../building-journeys/read-audience.md).

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->

## Argomenti correlati

* [Guida ai criteri di entrata e uscita del Percorso](entry-exit-criteria-guide.md) - Guida completa con esempi reali e best practice
* [Configura i criteri di uscita](journey-properties.md#exit-criteria) - Definisci quando i profili devono lasciare il percorso
* [Termina un percorso](end-journey.md) - Comprendere come chiudono e finiscono i percorsi
* [Casi d&#39;uso Percorsi](jo-use-cases.md) - Vedi esempi completi con configurazioni di entrata e uscita

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato il funzionamento della gestione delle voci di profilo nei quattro tipi di percorso di Adobe Journey Optimizer, inclusi i limiti di velocità effettiva, le impostazioni di rientro e il comportamento delle attività Attesa e Azione sulla velocità di elaborazione.

**Intenti:**

* Comprendere il comportamento di ingresso e i limiti di velocità effettiva per ciascun tipo di percorso (evento unitario, evento di business, lettura del pubblico, qualificazione del pubblico)
* Abilita o disabilita il rientro del profilo e configura il periodo di attesa per il rientro
* Consenti più esecuzioni di eventi business per un percorso lavorativo
* Identificare in che modo le attività di attesa e le attività di azione influiscono sulla velocità di elaborazione del percorso
* Verificare che un profilo non sia presente nello stesso percorso contemporaneamente

**Glossario:**

* **Rientro**: possibilità per un profilo di accedere nuovamente allo stesso percorso dopo l&#39;uscita precedente; configurabile con un periodo di attesa *(specifico per prodotto)*
* **Periodo di attesa per il rientro**: il tempo minimo che deve trascorrere prima che un profilo possa rientrare in un percorso; il valore predefinito è 5 minuti, il valore massimo è 90 giorni nelle proprietà del percorso *(specifiche del prodotto)*
* **TPS (Transazioni al secondo)**: velocità effettiva alla quale i profili possono entrare o essere elaborati in un percorso *(specifico per prodotto)*
* **percorso di eventi unitario**: percorso attivato da un singolo evento associato a un profilo *(specifico per prodotto)*
* **Leggi percorso di pubblico**: percorso che elabora un batch di profili appartenenti a un pubblico definito, una volta o secondo una pianificazione ricorrente *(specifico per prodotto)*
* **percorso di eventi di business**: percorso attivato da un evento di business che esegue il targeting di un pubblico, creando un&#39;istanza di percorso per profilo *(specifico per prodotto)*
* **percorso di qualificazione del pubblico**: percorso attivato quando un profilo entra o esce da un pubblico in streaming in tempo reale *(specifico per prodotto)*

**Guardrail:**

* Un profilo non può essere presente più volte nello stesso percorso contemporaneamente in tutte le versioni attive.
* Leggi percorsi di pubblico: massimo 20.000 TPS (quota a livello di sandbox; condivisa tra tutti i percorsi simultanei Leggi pubblico nella stessa sandbox)
* Qualificazione del pubblico e percorsi di eventi unitari: massimo 5.000 TPS (quota a livello di organizzazione; condivisa tra di loro tra tutte le sandbox nell’organizzazione)
* Gli eventi di business vengono conteggiati ai fini della quota di 5.000 TPS a livello di organizzazione; la successiva attività Read audience condivide la quota di 20.000 TPS a livello di sandbox
* Il periodo di attesa di rientro predefinito è di 5 minuti; il valore massimo configurabile è di 90 giorni nelle proprietà del percorso
* Le attività di attesa a tempo fisso possono causare picchi di profilo superiori a 20.000 TPS e non sono consigliate.
* Il limite predefinito per le azioni personalizzate è di 300.000 chiamate al minuto.
* Per i percorsi lavorativi, i dati del pubblico della prima esecuzione vengono riutilizzati per 1 ora.

**Terminologia:**

* Nome canonico: Profile entrance management — Acronimo: n/d — Varianti: profile entry management, voce percorso
* Sinonimi: &quot;rientro&quot; = &quot;rientro&quot;
* Non confondere: &quot;percorso di eventi unitario&quot; ≠ &quot;percorso di qualificazione del pubblico&quot; — entrambi scenari unitari ma attivati in modo diverso (emissione di eventi vs. modifica dell’iscrizione al pubblico)

**Domande frequenti:**

* **Q: un profilo può entrare nello stesso percorso due volte contemporaneamente?** — No, il sistema utilizza l&#39;identità del profilo come chiave e impedisce che lo stesso profilo si trovi in luoghi diversi nello stesso percorso contemporaneamente.
* **D: qual è il periodo di attesa di rientro predefinito?** — 5 minuti, configurabili fino a un massimo di 90 percorsi nelle proprietà.
* **D: quanti profili al secondo è possibile elaborare un percorso Read audience?** — Fino a 20.000 TPS a livello di sandbox, anche se questo massimo potrebbe non essere raggiungibile se più percorsi vengono eseguiti contemporaneamente nella stessa sandbox.
* **D: cosa succede al throughput dopo un&#39;attività Attendi con un tempo fisso?** — Più profili possono uscire dall&#39;attesa contemporaneamente, superando potenzialmente i 20.000 TPS; per evitare questo problema, si consigliano attività di attesa in tempo relativo.
* **D: un profilo può essere visualizzato più volte in un percorso aziendale contemporaneamente?** — Sì, ma solo nel contesto di diversi eventi di business.

+++
