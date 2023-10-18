---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai percorsi
description: Introduzione ai percorsi
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: percorsi, discovery, get-start
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 27%

---


# Introduzione ai percorsi{#jo-general-principle}

Utilizza [!DNL Journey Optimizer] per generare l’orchestrazione in tempo reale per diversi casi d’uso, sfruttando i dati contestuali provenienti da eventi od origini dati.

Puoi progettare scenari avanzati a più passaggi basati sulle seguenti funzionalità:

* Invia in tempo reale una **consegna unitaria** attivata quando viene ricevuto un evento o **in batch** utilizzando i tipi di pubblico di Adobe Experience Platform.

* Sfrutta **dati contestuali** da eventi, informazioni da Adobe Experience Platform o dati da servizi API di terze parti.

* Utilizza il **azioni incorporate** per inviare messaggi progettati in [!DNL Journey Optimizer] o creare **azioni personalizzate** se utilizzi un sistema di terze parti per l’invio dei messaggi.

* Con **journey designer**, genera casi d’uso a più passaggi: trascina facilmente un evento di ingresso o un’attività Leggi pubblico, aggiungi delle condizioni e invia messaggi personalizzati.


>[!NOTE]
>
>I guardrail e le limitazioni del percorso sono descritti in [questa pagina](../start/guardrails.md)

## Passaggi per creare un percorso{#steps-journey}

Utilizza Adobe Journey Optimizer per progettare e orchestrare percorsi personalizzati da un’unica area di lavoro. I passaggi principali per la creazione di un percorso sono i seguenti:

![](assets/journey-creation-process.png)

Adobe Journey Optimizer include un’area di lavoro di orchestrazione omnicanale che consente agli addetti al marketing di armonizzare l’attività di marketing con il coinvolgimento dei clienti uno a uno. L’interfaccia utente ti consente di trascinare facilmente le attività dalla palette all’interno dell’area di lavoro per creare il percorso.

![](assets/interface-journeys.png)

Scopri come iniziare e creare il primo percorso in [questa pagina](journey-gs.md).

La finestra di progettazione di percorsi omnichannel consente di creare percorsi con più passaggi, con tipi di pubblico mirati, aggiornamenti basati su interazioni cliente o business in tempo reale e messaggi omnichannel tramite un’interfaccia intuitiva basata su trascinamento.

![](assets/journey38.png)

Ulteriori informazioni in [questa sezione](using-the-journey-designer.md).

In qualità di ingegnere dati, i passaggi per configurare i percorsi, inclusi Origini dati, Eventi e Azioni, sono descritti in [questa sezione](../configuration/about-data-sources-events-actions.md).


## Casi d’uso{#uc-journey}

Scopri come creare percorsi nei seguenti casi d’uso end-to-end.

Casi d’uso aziendali:

* [Inviare messaggi multicanale](journeys-uc.md)
* [Inviare un messaggio con Campaign v7/v8](ajo-ac.md)
* [Inviare un messaggio agli abbonati](message-to-subscribers-uc.md)

Casi d’uso tecnico:

* [Passaggio dinamico delle raccolte tramite azioni personalizzate](collections.md)
* [Incrementare gradualmente le consegne](ramp-up-deliveries-uc.md)
* [Limite di trasmissione con origini dati esterne e azioni personalizzate](limit-throughput.md)

## Versioni del percorso{#journey-versions}

Nell&#39;elenco percorso vengono visualizzate tutte le versioni del percorso con il numero di versione. Consulta [questa pagina](../building-journeys/using-the-journey-designer.md).

Quando si cerca un percorso, le versioni più recenti vengono visualizzate nella parte superiore dell&#39;elenco la prima volta che l&#39;applicazione viene aperta. È quindi possibile definire l&#39;ordinamento desiderato, che verrà mantenuto dall&#39;applicazione come preferenza utente. La versione del percorso viene visualizzata anche nella parte superiore dell’interfaccia dell’edizione del percorso, sopra l’area di lavoro.

![](assets/journeyversions1.png)

>[!NOTE]
>
>In genere, un profilo non può essere presente più volte nello stesso percorso contemporaneamente. Se è abilitato il rientro, un profilo può rientrare in un percorso, ma non può farlo finché non è completamente uscito dall’istanza precedente del percorso. [Ulteriori informazioni](end-journey.md).

Se devi apportare delle modifiche a un percorso live, crea una nuova versione del percorso.

1. Apri la versione più recente del percorso live e fai clic su **[!UICONTROL Crea una nuova versione]** e confermare.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >È possibile creare una nuova versione solo a partire dalla versione più recente di un percorso.

1. Apporta le modifiche necessarie, quindi fai clic su **[!UICONTROL Pubblica]** e confermare.

   ![](assets/journeyversions3.png)

Dal momento in cui il percorso viene pubblicato, i singoli utenti inizieranno a passare all&#39;ultima versione del percorso. Le persone che hanno già inserito una versione precedente vi rimangono fino alla fine del percorso. Se in un secondo momento vengono reinseriti nello stesso percorso, verranno inseriti nella versione più recente.

Le versioni di percorso possono essere arrestate singolarmente. Tutte le versioni dei percorsi hanno lo stesso nome.

Quando si pubblica una nuova versione di un percorso, la versione precedente termina automaticamente e passa alla **Chiuso** stato. Nessun ingresso nel percorso può capitare. Anche se si interrompe la versione più recente, la versione precedente rimane chiusa.
