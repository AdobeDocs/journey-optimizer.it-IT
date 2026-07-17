---
solution: Journey Optimizer
product: journey optimizer
title: Fine percorso
description: Scopri come termina un percorso in Journey Optimizer
feature: Journeys
role: User
level: Intermediate
keywords: reenter, percorsi, end, live, stop
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-mknoNfkNCnfnLD1UCiA6C88NjookKqGr5tQdJ-f3T4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d7dd6f7f-9e2a-47ee-a2bc-b7b9caaefc1d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4d4656744a775cbe1ac5e7e6789ad98ef28cc219
workflow-type: tm+mt
source-wordcount: 2131
ht-degree: 1%

---

# Termina un percorso {#journey-ending}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come terminano i percorsi sia per i singoli profili che per l&#39;insieme e come chiudere o interrompere un percorso live quando devi interrompere le nuove entrate o tutta l&#39;elaborazione.

>[!ENDSHADEBOX]

>[!TIP]
>
>Cerchi indicazioni pratiche su quando e come i profili devono uscire dai percorsi? Consulta la [guida completa ai criteri di entrata e uscita dal percorso](entry-exit-criteria-guide.md), che include scenari di uscita reali, best practice e indicazioni sulla configurazione.

## Come termina un percorso live

I percorsi vengono chiusi al raggiungimento del timeout del percorso globale o dopo l’ultima occorrenza di un percorso ricorrente basato su pubblico. [Informazioni sulla chiusura dei percorsi](#close-journey).

Se devi terminare un percorso live, ti consigliamo di [chiuderlo](#close-to-new-entrances) manualmente. L&#39;arrivo di nuovi clienti nel percorso viene quindi bloccato. I profili che sono già entrati nel percorso possono provarlo fino alla fine.

Puoi anche [interrompere un percorso](#stop-journey), solo in caso di emergenza e se l&#39;elaborazione di tutto il percorso deve essere interrotta immediatamente. Le persone che sono già entrate in un percorso sono tutte fermate nel loro avanzamento.

>[!IMPORTANT]
>
>* Impossibile riavviare o eliminare un percorso [chiuso](#close-journey) o [interrotto](#stop-journey). Puoi [creare una nuova versione](publish-journey.md#journey-versions) di essa o [duplicarla](journey-ui.md#duplicate-a-journey).
>
>* È possibile eliminare solo i percorsi finiti.

## Terminazione di un percorso con i profili

Un percorso termina per un individuo in due contesti specifici:

* Il singolo raggiunge l&#39;ultima attività di un percorso, quindi si sposta sul tag [End](#end-tag).
* L&#39;individuo raggiunge un&#39;attività **Condition** (o un&#39;attività **Wait** con una condizione) e non corrisponde a nessuna delle condizioni.

L’individuo può quindi rientrare nel percorso se il rientro è consentito. [Ulteriori informazioni sulla gestione dell&#39;ingresso/rientro](../building-journeys/journey-properties.md#entrance)

## Tag di fine percorso {#end-tag}

Durante la creazione di un percorso, alla fine di ciascun percorso viene visualizzato un tag di fine. Questo nodo non può essere aggiunto da un utente, non può essere rimosso e solo la relativa etichetta può essere modificata. Segna la fine di ogni percorso del percorso.

Se il percorso dispone di diversi percorsi, si consiglia di aggiungere un’etichetta a ogni estremità per facilitare la lettura dei rapporti. Ulteriori informazioni sui [report percorso](../reports/live-report.md).

![Pulsante azione Fine percorso nella barra degli strumenti percorso](assets/journey-end.png)

## Chiudi un percorso {#close-journey}

Un percorso può essere chiuso per i motivi seguenti:

* Un percorso Read Audience non ricorrente **si arresta automaticamente** dopo un buffer di sicurezza dopo la sua esecuzione pianificata. [Ulteriori informazioni](#auto-stop-non-recurring)
* Dopo l’ultima occorrenza di un percorso ricorrente basato su pubblico.
* Il percorso viene chiuso manualmente tramite il pulsante [**[!UICONTROL Chiudi ai nuovi ingressi]**](#close-to-new-entrances).
* È stato raggiunto il timeout di percorso globale di 91 giorni.

Dopo il timeout globale del percorso di **91 giorni**, un percorso Read audience passa allo stato **Finished**. Questo comportamento è impostato per 91 giorni, in quanto tutte le informazioni sui profili che sono entrati nel percorso vengono rimosse 91 giorni dopo l’ingresso. Le persone ancora nel percorso sono automaticamente interessate. Uscono dal percorso dopo il timeout di 91 giorni.  Ulteriori informazioni sul [timeout globale del percorso](../building-journeys/journey-properties.md#global_timeout).

### Interruzione automatica del percorso per tipi di pubblico non ricorrenti {#auto-stop-non-recurring}

Un **percorso Read Audience non ricorrente** passa automaticamente allo stato **[!UICONTROL Arrestato]** dopo un buffer di sicurezza dopo l&#39;esecuzione pianificata. Questo elimina il comportamento precedente in cui i percorsi Read Audience non ricorrenti rimanevano nello stato **Live** fino alla scadenza del timeout globale di 91 giorni, anche se non vi scorrevano profili attivamente.

**Funzionamento:**

1. Il percorso viene eseguito e tutti i profili del pubblico vengono elaborati.
1. Quando ogni profilo raggiunge la fine del percorso, esce normalmente.
1. Dopo l&#39;esecuzione pianificata, il percorso rimane nello stato **[!UICONTROL Live]** durante un periodo di buffer di sicurezza.
1. Trascorso il buffer di sicurezza (~96 ore dopo l&#39;ora di esecuzione pianificata del percorso), il percorso passa automaticamente allo stato **[!UICONTROL Interrotto]** poco dopo.

Questo comportamento si applica solo a **percorsi di pubblico di lettura non ricorrenti**. Non influisce sui percorsi ricorrenti.

* **Intervallo di arresto automatico:** Il buffer di sicurezza tiene conto di due finestre: una finestra di inattività di **24 ore** per consentire il completamento di qualsiasi invio in-flight e una tolleranza di **72 ore per le ore non interattive** (le ore non interattive possono differire gli invii fino a 72 ore). Il buffer totale è di circa **96 ore (~4 giorni)** dopo l&#39;ora di esecuzione pianificata del percorso. Il percorso rimane nello stato **[!UICONTROL Live]** durante questo periodo. Questo è il comportamento previsto e non indica un problema.

* **I percorsi basati su scaglioni sono esclusi:** Questo comportamento di arresto automatico non si applica ai percorsi basati su scaglioni e ai percorsi che utilizzano l&#39;ottimizzazione del tempo di invio. Questi percorsi rimangono attivi in tutte le ondate pianificate e vengono interrotti solo dal timeout globale standard di [91 giorni](../building-journeys/journey-properties.md#global_timeout), a meno che non vengano chiusi o interrotti manualmente.

* Questo comportamento di arresto automatico **not** si applica ai percorsi non ricorrenti che includono nodi che causano periodi di attesa, ad esempio **Wait** nodi (basati su timer), **Reaction** nodi (in attesa di eventi come apertura e-mail o clic) o transizioni attivate da eventi. Questi percorsi rimangono soggetti al timeout globale standard di [91 giorni](../building-journeys/journey-properties.md#global_timeout).

* Puoi comunque chiudere manualmente un percorso di tipi di pubblico di lettura non ricorrenti in qualsiasi momento utilizzando l&#39;opzione [**[!UICONTROL Chiudi ai nuovi ingressi]**](#close-to-new-entrances). Il comportamento di arresto automatico assicura semplicemente che il percorso si arresti automaticamente quando non è più necessario, senza richiedere un intervento manuale.

### Quando un percorso viene considerato &quot;completato&quot;? {#journey-finished-definition}

La definizione di &quot;finito&quot; varia a seconda del tipo di percorso:

| Tipo di percorso | Ricorrente? | Ha una data di fine? | Definizione di &quot;finito&quot; |
|--------------|------------|---------------|--------------------------|
| Leggi pubblico | No | n/d | ~96 ore dopo l&#39;esecuzione pianificata (buffer di arresto automatico) |
| Leggi pubblico | Sì | No | 91 giorni dopo l’inizio dell’ultima occorrenza |
| Leggi pubblico | Sì | Sì | Quando viene raggiunta la data di fine |
| Percorso attivato da eventi | n/d | Sì | Quando viene raggiunta la data di fine |
| Percorso attivato da eventi | n/d | No | Quando è chiuso nell’interfaccia o tramite API |

### Chiudi ai nuovi ingressi {#close-to-new-entrances}

La chiusura manuale di un percorso consente ai clienti che sono già entrati nel percorso di completare il percorso, ma ai nuovi utenti di non accedere al percorso. Quando un percorso viene chiuso (per uno dei motivi di cui sopra), avrà lo stato **[!UICONTROL Chiuso]**. Il percorso non consente più l&#39;ingresso di nuovi individui nel percorso. I profili già presenti nel percorso possono completare il percorso normalmente. Dopo il timeout globale predefinito di 91 giorni, il percorso passerà allo stato **Completato**.

È possibile interrompere un percorso dallo stato **Live** o **Paused**. Quando il percorso è **In pausa**, non è necessario riprenderlo prima in **Live**. [Ulteriori informazioni sull&#39;arresto di un percorso in pausa](journey-pause.md#stop-close-paused).

Per chiudere un percorso dall&#39;elenco dei percorsi, fare clic sul pulsante **[!UICONTROL Puntini di sospensione]** a destra del nome del percorso e selezionare **[!UICONTROL Chiudi ai nuovi ingressi]**.

![Menu a discesa Fine azione nel menu Azioni rapide per il percorso finale](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. Nell&#39;elenco **[!UICONTROL Percorsi]** selezionare il percorso che si desidera chiudere.
1. In alto a destra, fare clic sulla freccia giù.

   ![Menu Opzioni fine che mostra il percorso finale e le azioni alternative](assets/finish_drop_down_list.png){width="50%" zoomable="yes"}

1. Fai clic su **[!UICONTROL Chiudi ai nuovi ingressi]** e conferma nella finestra di dialogo.


## Interrompi un percorso {#stop-journey}

Nel caso in cui si debba fermare il progresso di tutti i singoli individui nel percorso, è possibile fermarlo. Interruzione del timeout del percorso per tutti gli utenti del percorso. Tuttavia, l&#39;arresto di un percorso implica che le persone che sono già entrate in un percorso sono tutte ferme nel loro progresso. Il percorso è spento. Se desideri terminare con un percorso, è consigliabile [chiuderlo](#close-journey).

Puoi anche interrompere direttamente un percorso **In pausa**, senza riprenderlo prima a **Live**. [Ulteriori informazioni](journey-pause.md#stop-close-paused).

Puoi interrompere un percorso, ad esempio, se un addetto marketing si rende conto che il percorso esegue il targeting del pubblico sbagliato o che un’azione personalizzata destinata a consegnare i messaggi non funziona correttamente. Per interrompere un percorso dall&#39;elenco dei percorsi, fare clic sul pulsante **[!UICONTROL Puntini di sospensione]** a destra del nome del percorso e selezionare **[!UICONTROL Interrompi]**.

![Menu a discesa Fine azione nel menu Azioni rapide per il percorso finale](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. Nell&#39;elenco **[!UICONTROL Percorsi]** fare clic sul percorso che si desidera interrompere.
1. In alto a destra, fare clic sulla freccia giù.

   ![Altre opzioni di fine, tra cui chiusura percorso e pulizia](assets/finish_drop_down_list2.png){width="50%" zoomable="yes"}

1. Fai clic su **[!UICONTROL Interrompi]** e conferma nella finestra di dialogo.

Quando viene interrotto, lo stato del percorso è impostato su **[!UICONTROL Arrestato]**.

>[!CAUTION]
>
>L&#39;arresto di un percorso richiede l&#39;autorizzazione **[!DNL Manage journeys]**. Se il percorso include campagne in linea o nodi di messaggistica, gli utenti dovranno disporre anche di autorizzazioni **Campagne > Pubblica campagne**. Se il percorso utilizza le risorse (ad esempio nelle e-mail), gli utenti devono avere accesso a tali cartelle di risorse. Ulteriori informazioni sulla gestione dei diritti di accesso degli utenti [!DNL Journey Optimizer] in [questa sezione](../administration/permissions-overview.md).

## Argomenti correlati

* [Guida ai criteri di entrata e uscita del Percorso](entry-exit-criteria-guide.md) - Guida completa con esempi reali e best practice
* [Gestione dell&#39;ingresso del profilo](entry-management.md) - Configura l&#39;accesso dei profili ai percorsi
* [Configura criteri di uscita](journey-properties.md#exit-criteria) - Imposta la rimozione automatica del profilo dai percorsi
* [Sospendi un percorso](journey-pause.md) - Interrompi temporaneamente l&#39;esecuzione del percorso

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina vengono illustrati i diversi modi in cui un percorso live può terminare, inclusi il timeout globale di 91 giorni, la chiusura manuale di nuovi ingressi e l&#39;arresto di emergenza, insieme ai relativi effetti sui profili in esecuzione.

**Intenti:**

* Chiudi un percorso attivo ai nuovi ingressi consentendo ai profili correnti di completarlo
* Interrompere immediatamente un percorso per arrestare tutti i profili in esecuzione
* Comprendere la differenza tra gli stati di percorso Chiuso, Arrestato e Finito
* Determinare quando un percorso è considerato &quot;completato&quot; in base al tipo e alla configurazione
* Eliminare un percorso quando ha raggiunto lo stato Finito

**Glossario:**

* **Tag finale**: nodo non rimovibile generato automaticamente visualizzato alla fine di ogni percorso di percorso durante la creazione. L&#39;etichetta può essere modificata *(specifico per prodotto)*
* **Vicino ai nuovi ingressi**: azione manuale che impedisce ai nuovi profili di entrare in un percorso consentendo ai profili esistenti di completare il loro percorso *(specifico per prodotto)*
* **Timeout percorso globale**: la durata massima di 91 giorni dopo la quale un percorso passa automaticamente allo stato Finito e tutti i dati del profilo vengono rimossi *(specifico per prodotto)*
* **Stato interrotto**: uno stato del percorso in cui tutti i profili in corso vengono immediatamente interrotti; utilizzato solo per le emergenze *(specifico per prodotto)*

**Guardrail:**

* I percorsi chiusi e interrotti non possono essere riavviati o eliminati; è possibile creare solo una nuova versione o un duplicato.
* È possibile eliminare solo i percorsi con lo stato Finito.
* L’arresto di un percorso richiede l’autorizzazione Gestione percorsi; anche i percorsi con campagne in linea o nodi di messaggistica richiedono l’autorizzazione Campagne > Pubblica campagne.
* Dopo il timeout globale di 91 giorni, tutti i dati del percorso di profili vengono rimossi e i profili rimanenti vengono chiusi automaticamente.
* Un percorso Read Audience non ricorrente senza nodi di attesa, reazione o attivati da eventi a esecuzione prolungata passa automaticamente a Interrotto circa 96 ore (~4 giorni) dopo l’esecuzione pianificata. Il percorso rimane in stato Live durante questo buffer. I percorsi basati su scaglioni e i percorsi che utilizzano l’ottimizzazione del tempo di invio sono esclusi da questo arresto automatico e rimangono soggetti al timeout globale di 91 giorni a meno che non vengano chiusi o arrestati manualmente.

**Terminologia:**

* Nome canonico: vicino ai nuovi ingressi — Acronimo: n/d — varianti: chiudi percorso, chiudi manualmente
* Sinonimi: percorso &quot;Interrotto&quot; ≠ percorso &quot;Chiuso&quot; — interrotto interrompe immediatamente tutti i profili; chiuso solo blocca i nuovi ingressi
* Da non confondere: &quot;Tag finale&quot; ≠ &quot;End activity&quot; - il tag finale viene generato automaticamente e non può essere rimosso; l&#39;attività finale è un nodo di area di lavoro posizionabile

**Domande frequenti:**

* **D: qual è la differenza tra la chiusura e l&#39;arresto di un percorso?** — La chiusura blocca i nuovi ingressi, ma consente il completamento dei profili esistenti; l&#39;interruzione immediata interrompe tutti i profili presenti nelle tracce.
* **Q: perché un percorso non ricorrente rimane in stato Live per diversi giorni dopo la sua esecuzione?** — Questo è previsto. AJO applica un buffer di sicurezza di circa 96 ore (~4 giorni): 24 ore per consentire il completamento degli invii in-flight, più 72 ore per i differimenti delle ore di silenzio. Il percorso passa a Arrestato poco dopo la fine del buffer.
* **Q: i percorsi basati su scaglioni si arrestano automaticamente dopo circa 96 ore?** — No I percorsi basati su scaglioni e i percorsi che utilizzano l’ottimizzazione del tempo di invio sono esclusi da questa interruzione automatica in modo che possano rimanere attivi per tutte le scaglioni pianificate. Essi seguono il timeout standard di percorso di 91 giorni a meno che non vengano chiusi o arrestati manualmente.
* **Q: quando un percorso di pubblico lettura raggiunge lo stato Finito?** — Per un percorso Read Audience non ricorrente: si arresta automaticamente in Arresto circa 96 ore (~4 giorni) dopo l&#39;esecuzione programmata (buffer di sicurezza: finestra inattiva 24 ore + 72 ore di tolleranza per le ore non interrotte). Il percorso rimane in stato Live durante questo buffer. Se i nodi Wait (Attesa), Reaction (Reazione) o event (Evento) mantengono i profili attivi, viene applicato il timeout globale standard di 91 giorni. Il termine terminato viene raggiunto quando un percorso chiuso raggiunge il timeout globale di 91 giorni o le regole per percorso ricorrente nella tabella di definizione finito.
* **Q: posso eliminare un percorso chiuso?** — No, è possibile eliminare solo i percorsi finiti.
* **D: cosa succede ai profili ancora in un percorso quando arriva il timeout di 91 giorni?** — A quel punto, vengono automaticamente eliminate dal percorso.
* **Q: sono necessarie autorizzazioni speciali per arrestare un percorso?** — Sì, è necessaria l&#39;autorizzazione Gestisci percorsi, più Campagne > Pubblica campagne se il percorso contiene campagne in linea o nodi di messaggistica.

+++
