---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai percorsi
description: Introduzione ai percorsi
feature: Journeys
role: User
level: Beginner
keywords: percorso, scopri, partenza
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: cd154b137d7b4e5a3b35948241d2bbbb18265903
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 28%

---


# Introduzione ai percorsi{#jo-general-principle}

Utilizzo [!DNL Journey Optimizer] per creare casi d’uso di orchestrazione in tempo reale utilizzando dati contestuali archiviati in eventi o origini dati.

Puoi progettare scenari avanzati a più passaggi basati sulle seguenti funzionalità:

* Invia in tempo reale una **consegna unitaria** attivata quando viene ricevuto un evento, oppure **in batch** utilizzando i segmenti di Adobe Experience Platform.

* Sfrutta **dati contestuali** da eventi, informazioni da Adobe Experience Platform o dati da servizi API di terze parti.

* Utilizza la **azioni integrate** per l’invio di messaggi progettati in [!DNL Journey Optimizer] o creare **azioni personalizzate** se utilizzi un sistema di terze parti per l’invio dei messaggi.

* Con il **designer percorsi**, genera i tuoi casi d’uso a più passaggi: trascina facilmente un evento di ingresso o un’attività di lettura segmento, aggiungi delle condizioni e invia messaggi personalizzati.

## Passaggi per creare un percorso{#steps-journey}

Utilizza Adobe Journey Optimizer per progettare e orchestrare percorsi personalizzati da un’unica area di lavoro. I passaggi principali per creare un percorso sono i seguenti:

![](assets/journey-creation-process.png)

Adobe Journey Optimizer include un’area di lavoro di orchestrazione omnicanale che consente agli esperti di marketing di armonizzare il pubblico marketing con il coinvolgimento di un singolo cliente. L’interfaccia utente ti consente di trascinare facilmente le attività dalla palette nell’area di lavoro per creare il percorso.

![](assets/interface-journeys.png)

Scopri come iniziare e creare il tuo primo percorso in [questa pagina](journey-gs.md).

Il designer del percorso omnicanale consente di creare percorsi con più passaggi con tipi di pubblico mirati, aggiornamenti basati sulle interazioni in tempo reale dei clienti o delle aziende e messaggi omnicanale tramite un’interfaccia intuitiva a trascinamento della selezione.

![](assets/journey38.png)

Ulteriori informazioni in [questa sezione](using-the-journey-designer.md).

In qualità di ingegnere dei dati, i passaggi per configurare i percorsi, incluse Origini dati, Eventi e Azioni, sono descritti in [questa sezione](../configuration/about-data-sources-events-actions.md).


## Casi d’uso{#uc-journey}

Scopri come generare percorsi nei seguenti casi d’uso end-to-end.

Casi d’uso aziendali:

* [Inviare messaggi multicanale](journeys-uc.md)
* [Inviare un messaggio con Campaign v7/v8](ajo-ac.md)
* [Inviare un messaggio agli abbonati](message-to-subscribers-uc.md)

Casi d’uso tecnico:

* [Passaggio dinamico delle raccolte tramite azioni personalizzate](collections.md)
* [Incrementare gradualmente le consegne](ramp-up-deliveries-uc.md)
* [Limite di trasmissione con origini dati esterne e azioni personalizzate](limit-throughput.md)

## Versioni del percorso{#journey-versions}

Nell’elenco percorso vengono visualizzate tutte le versioni del percorso con il numero di versione. Consulta [questa pagina](../building-journeys/using-the-journey-designer.md).

Quando cerchi un percorso, le versioni più recenti vengono visualizzate nella parte superiore dell’elenco al primo avvio dell’applicazione. Quindi, puoi definire l’ordinamento desiderato e l’applicazione lo manterrà come preferenza utente. La versione del percorso viene visualizzata anche nella parte superiore dell&#39;interfaccia dell&#39;edizione del percorso, sopra l&#39;area di lavoro.

![](assets/journeyversions1.png)

>[!NOTE]
>
>In genere, un profilo non può essere presente più volte nello stesso percorso contemporaneamente. Se è stato abilitato il rientro, un profilo può rientrare in un percorso, ma non può farlo fino a quando non è completamente uscito dall’istanza precedente del percorso. [Ulteriori informazioni](end-journey.md).

Per modificare un percorso live, crea una nuova versione del percorso.

1. Apri la versione più recente del percorso live e fai clic su **[!UICONTROL Creare una nuova versione]** e confermare.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Puoi creare una nuova versione solo dall’ultima versione di un percorso.

1. Apporta le modifiche desiderate, fai clic su **[!UICONTROL Pubblica]** e confermare.

   ![](assets/journeyversions3.png)

Dal momento in cui il percorso verrà pubblicato, i singoli inizieranno a scorrere nell&#39;ultima versione del percorso. Le persone che hanno già inserito una versione precedente vi rimangono fino a quando non finiscono il percorso. Se in seguito vengono reinseriti nello stesso percorso, passeranno alla versione più recente.

Le versioni di percorso possono essere arrestate singolarmente. Tutte le versioni dei percorsi hanno lo stesso nome.

Quando pubblichi una nuova versione di un percorso, la versione precedente termina automaticamente e passa alla **Chiuso** stato. Non può accadere alcuna entrata nel percorso. Anche se si interrompe l&#39;ultima versione, la versione precedente rimane chiusa.

>[!NOTE]
>
>Ulteriori informazioni sulle versioni di percorso protezioni e limitazioni, in [questa pagina](../start/guardrails.md#journey-versions-limitations)