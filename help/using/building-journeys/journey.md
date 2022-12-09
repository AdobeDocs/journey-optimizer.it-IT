---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva ai percorsi
description: Guida introduttiva ai percorsi
feature: Journeys
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---


# Guida introduttiva ai percorsi{#jo-general-principle}

Utilizzo [!DNL Journey Optimizer] per creare casi d’uso di orchestrazione in tempo reale utilizzando dati contestuali archiviati in eventi o origini dati.

Progetta scenari avanzati a più passaggi basati sulle seguenti funzionalità:

* Invia in tempo reale **consegna unitaria** attivato quando viene ricevuto un evento, oppure **in batch** utilizzo dei segmenti di Adobe Experience Platform.

* Sfruttamento **dati contestuali** da eventi, informazioni da Adobe Experience Platform o dati da servizi API di terze parti.

* Utilizza la **azioni integrate** per l’invio di messaggi progettati in [!DNL Journey Optimizer] o creare **azioni personalizzate** se utilizzi un sistema di terze parti per l’invio dei messaggi.

* Con la **designer del percorso**, genera i casi di utilizzo con più passaggi: trascina e rilascia facilmente un evento di partecipazione o un’attività di segmento letto, aggiungi condizioni e invia messaggi personalizzati.

## Passaggi per creare un percorso{#steps-journey}

Utilizza Adobe Journey Optimizer per progettare e orchestrare percorsi personalizzati da un’unica area di lavoro.

Adobe Journey Optimizer include un’area di orchestrazione omnicanale che consente agli esperti di marketing di armonizzare il pubblico marketing con il coinvolgimento di un singolo cliente. L’interfaccia utente ti consente di trascinare facilmente le attività dalla palette nell’area di lavoro per creare il percorso.

![](assets/interface-journeys.png)

Scopri come iniziare e creare il tuo primo percorso in [questa pagina](journey-gs.md).

Il designer del percorso omnicanale consente di creare percorsi con più passaggi con tipi di pubblico mirati, aggiornamenti in base alle interazioni in tempo reale dei clienti o delle aziende e messaggi omnicanale tramite un’interfaccia intuitiva a trascinamento della selezione.

![](assets/journey38.png)

Ulteriori informazioni in [questa sezione](using-the-journey-designer.md).

In qualità di ingegnere dei dati, i passaggi per configurare i percorsi, comprese Origini dati, Eventi e Azioni, sono descritti in [questa sezione](../configuration/about-data-sources-events-actions.md).


## Casi d’uso{#uc-journey}

Scopri come generare i percorsi nei seguenti casi d’uso end-to-end.

Casi di utilizzo aziendale:

* [Inviare messaggi multicanale](journeys-uc.md)
* [Inviare un messaggio utilizzando Campaign v7/v8](ajo-ac.md)
* [Inviare un messaggio agli abbonati](message-to-subscribers-uc.md)

Casi d’uso tecnico:

* [Trasmettere dinamicamente le raccolte utilizzando azioni personalizzate](collections.md)
* [Incremento delle consegne](ramp-up-deliveries-uc.md)
* [Limitare il throughput con origini dati esterne e azioni personalizzate](limit-throughput.md)

## Versioni del percorso{#journey-versions}

Nell’elenco dei percorsi, vengono visualizzate tutte le versioni del percorso con il numero di versione. Vedi [questa pagina](../building-journeys/using-the-journey-designer.md).

Quando cerchi un percorso, le versioni più recenti vengono visualizzate nella parte superiore dell’elenco al primo avvio dell’applicazione. Quindi, puoi definire l’ordinamento desiderato e l’applicazione lo manterrà come preferenza utente. La versione del percorso viene visualizzata anche nella parte superiore dell’interfaccia di edizione del percorso, sopra l’area di lavoro.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Di solito, un profilo non può essere presente più volte nello stesso percorso, allo stesso tempo. Se l’opzione di rientro è abilitata, un profilo può rientrare in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso. [Leggi tutto](end-journey.md).

Se devi modificare un percorso live, crea una nuova versione del percorso.

1. Apri la versione più recente del percorso live e fai clic su **[!UICONTROL Create a new version]** e confermare.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Puoi creare una nuova versione solo dall’ultima versione di un percorso.

1. Apporta le modifiche desiderate, fai clic su **[!UICONTROL Publish]** e confermare.

   ![](assets/journeyversions3.png)

Dal momento in cui il percorso viene pubblicato, gli utenti inizieranno a scorrere nell’ultima versione del percorso. Le persone che sono già entrate in una versione precedente vi rimangono finché non terminano il percorso. In seguito, se accedono nuovamente allo stesso percorso, passeranno alla versione più recente.

Le versioni del percorso possono essere interrotte singolarmente. Tutte le versioni dei percorsi hanno lo stesso nome.

Quando pubblichi una nuova versione di un percorso, la versione precedente termina automaticamente e passa alla **Chiuso** stato. Non si può entrare nel viaggio. Anche se si interrompe l&#39;ultima versione, la versione precedente rimane chiusa.

>[!NOTE]
>
>Ulteriori informazioni sulle versioni del percorso protezioni e limitazioni, in [questa pagina](../start/guardrails.md#journey-versions-limitations)