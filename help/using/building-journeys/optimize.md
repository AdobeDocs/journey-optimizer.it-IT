---
solution: Journey Optimizer
product: journey optimizer
title: Attività Condizione
description: Scopri l’attività condizione
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attività, condizione, area di lavoro, percorso, ottimizzazione
badge: label="Disponibilità limitata" type="Informative"
hidefromtoc: true
hide: true
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
source-git-commit: 19130e9eb5a2144afccab9fa8e5632de67bc7157
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 3%

---

# Ottimizza attività {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Ottimizza attività"
>abstract="L&#39;attività **Ottimizza** consente di definire il modo in cui i singoli utenti avanzano nel percorso creando più percorsi in base a criteri specifici, tra cui sperimentazione, targeting e condizioni specifiche."

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

L&#39;attività **Ottimizza** consente di definire il modo in cui i singoli utenti avanzano nel percorso creando più **percorsi** in base a criteri specifici, tra cui sperimentazione, targeting e condizioni specifiche, garantendo il massimo coinvolgimento e successo nella creazione di percorsi altamente personalizzati ed efficaci.

Un percorso di **percorso** può essere costituito dai seguenti elementi:

* sequenziamento delle comunicazioni;
* il tempo che intercorre tra di essi;
* numero di comunicazioni;
* o una combinazione di queste tre variabili.

Ad esempio, un percorso potrebbe contenere un messaggio e-mail, un altro potrebbe contenere due messaggi SMS e un terzo potrebbe contenere un messaggio e-mail, un nodo [Wait](wait-activity.md) di due ore e quindi un messaggio SMS.

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

Tramite l&#39;attività **Ottimizza** è possibile:

* Esegui [esperimenti percorso](#experimentation)
* Sfrutta le regole di [targeting](#targeting) in ogni percorso di percorso
* Applica [condizioni](#conditions) ai tuoi percorsi

![](assets/journey-optimize.png)

Una volta che il percorso è attivo, i profili vengono valutati in base ai criteri definiti e, in base ai criteri di corrispondenza, vengono inviati lungo il percorso appropriato dal percorso.

## Utilizzare la sperimentazione {#experimentation}

La sperimentazione consente di testare percorsi diversi in base a una suddivisione casuale per determinare quale funziona meglio in base a metriche di successo predefinite.

Per impostare la sperimentazione in un percorso, segui i passaggi riportati di seguito.

Supponiamo che tu voglia confrontare tre percorsi:

* un percorso con un messaggio e-mail;
* un secondo percorso con un nodo Attendi di due giorni e un messaggio e-mail;
* un terzo percorso con un’e-mail e quindi un messaggio SMS.

1. Rilascia l&#39;attività **[!UICONTROL Ottimizza]** nell&#39;area di lavoro del percorso.

1. Aggiungi un’etichetta opzionale per identificare l’attività nei rapporti e nei registri in modalità di test.

1. Selezionare **[!UICONTROL Esperimento]** dall&#39;elenco a discesa **[!UICONTROL Metodo]**.

   ![](assets/journey-optimize-experiment.png){width=85%}

1. Fare clic su **[!UICONTROL Impostazioni esperimento]**.

1. Progetta e configura l’esperimento come desiderato. [Scopri come](../content-management/content-experiment.md)

   <!--
    ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}
    Replace with appropriate screenshot
    The experiment applies to all the activities in the journey.TBC
   -->

Una volta che il percorso è attivo, gli utenti vengono assegnati in modo casuale per seguire percorsi diversi. [!DNL Journey Optimizer] tiene traccia del percorso che determina ulteriori acquisti e fornisce informazioni fruibili.

<!--Follow the success of your journey with the [Experimentation journey report](../reports/campaign-global-report-cja-experimentation.md). Is there a report specific to experimentation in journey?-->

### Casi di utilizzo con l’esperimento {#uc-experiment}

Gli esempi seguenti mostrano come utilizzare l&#39;attività **[!UICONTROL Ottimizza]** con il metodo **[!UICONTROL Esperimento]** per determinare quale percorso funziona meglio nel complesso.

**Efficacia del canale**

Verifica se l’invio del primo messaggio tramite e-mail rispetto agli SMS determina conversioni più elevate.

* Utilizza il tasso di conversione come metrica di ottimizzazione (ad esempio: acquisti, iscrizioni).

![](assets/journey-optimize-experiment-uc.png)

**Frequenza messaggi**

Esegui un esperimento per verificare se l’invio di un’e-mail rispetto a tre e-mail in una settimana comporta più acquisti.

* Utilizza gli acquisti o il tasso di annullamento dell’iscrizione come metrica di ottimizzazione.

**Tempo di attesa tra le comunicazioni**

Confronta un’attesa di 24 ore con un’attesa di 72 ore prima di un follow-up per determinare quale tempistica massimizza il coinvolgimento.

* Utilizza il tasso di click-through o i ricavi come metrica di ottimizzazione.

## Utilizzo del targeting {#targeting}

Il targeting consente di determinare regole o qualifiche specifiche che devono essere soddisfatte affinché un cliente possa accedere a uno dei percorsi di percorso, in base a segmenti di pubblico specifici<!-- depending on profile attributes or contextual attributes-->.

A differenza della sperimentazione, che è un’assegnazione casuale di un determinato percorso, il targeting è deterministico in termini di garantire che il pubblico o il profilo giusto entri nel percorso specificato.

Con il targeting è possibile definire regole specifiche in base a:

* **Attributi del profilo utente** come la posizione (esempio: geotargeting), età o preferenze. Ad esempio, negli Stati Uniti gli utenti possono vedere una promozione &quot;Golden Gate&quot;, mentre in Francia gli utenti possono vedere una promozione &quot;Eiffel Tower&quot;.

* **Dati contestuali** come tipo di dispositivo (esempio: device-targeting), l’ora del giorno o i dettagli della sessione. Ad esempio, gli utenti desktop ricevono contenuti ottimizzati per il desktop, mentre gli utenti mobili ricevono contenuti ottimizzati per il mobile.

* **Tipi di pubblico** che possono essere utilizzati per includere o escludere profili con una particolare appartenenza al pubblico.

Per impostare il targeting in un percorso, segui i passaggi indicati di seguito.

1. Rilascia l&#39;attività **[!UICONTROL Ottimizza]** nell&#39;area di lavoro del percorso.

1. Aggiungi un’etichetta opzionale per identificare l’attività nei rapporti e nei registri in modalità di test.

1. Selezionare **[!UICONTROL Targeting]** dall&#39;elenco a discesa **[!UICONTROL Metodo]**.

   ![](assets/journey-optimize-targeting.png){width=85%}

1. Fai clic su **[!UICONTROL Crea regola di targeting]**.

1. Utilizza il generatore di regole per definire i criteri. Ad esempio, definisci una regola per i residenti negli Stati Uniti, una regola per i residenti in Francia e una regola per i residenti in India.

   ![](assets/journey-targeting-rule.png)

1. Selezionare **[!UICONTROL Abilita contenuto di fallback]** in base alle esigenze. Il contenuto di fallback consente al pubblico di ricevere un contenuto predefinito quando non sono qualificate regole di targeting. Se non selezioni questa opzione, i tipi di pubblico non idonei per una regola di targeting definita sopra non immetteranno un percorso di fallback.

1. Salva le impostazioni della regola di targeting.

1. Sempre nel percorso, rilascia azioni specifiche per personalizzare ogni percorso. Ad esempio, puoi creare un’e-mail specifica per residenti negli Stati Uniti, un’altra e-mail per residenti in Francia e così via.

   ![](assets/journey-targeting-paths.png)

1. Progetta il contenuto appropriato per ogni gruppo definito dalle impostazioni delle regole di targeting. Puoi navigare facilmente tra i diversi percorsi.

   ![](assets/journey-targeting-design.png)

   In questo esempio, progetta un percorso specifico per i residenti negli Stati Uniti, un percorso diverso per i residenti francesi e un altro percorso per i residenti in India.

Una volta che il percorso è attivo, il percorso specificato per ogni segmento viene elaborato in modo che i residenti degli Stati Uniti immettano un percorso specifico, i residenti della Francia immettano un percorso diverso e così via.

### Casi d’uso con targeting {#uc-targeting}

Gli esempi seguenti mostrano come utilizzare l&#39;attività **[!UICONTROL Ottimizza]** con il metodo **[!UICONTROL Targeting]** per personalizzare i percorsi per diversi tipi di pubblico secondario.

**Canali specifici del segmento**

I membri fedeltà con stato Gold possono ricevere offerte personalizzate tramite e-mail, mentre tutti gli altri membri sono indirizzati a promemoria SMS.

* Utilizza il ricavo per profilo o il tasso di conversione come metrica di ottimizzazione.

![](assets/journey-optimize-targeting-uc.png)

**Destinazione basata sul comportamento**

Ai clienti che hanno aperto un’e-mail ma non hanno fatto clic su viene inviata una notifica push, mentre a quelli che non hanno aperto viene inviato un SMS.

* Utilizza il tasso di click-through o le conversioni a valle come metrica di ottimizzazione.

**Destinazione cronologia acquisti**

I clienti che hanno acquistato di recente possono entrare in un breve percorso di &quot;Grazie + Cross-selling&quot;, mentre quelli senza cronologia di acquisto entrano in un percorso di sviluppo più lungo.

* Utilizza il tasso di acquisto ripetuto o il tasso di coinvolgimento come metrica di ottimizzazione.

## Aggiungere una condizione {#conditions}

Puoi aggiungere una condizione per definire il modo in cui i singoli utenti avanzano nel percorso creando più percorsi in base a criteri specifici. Puoi anche configurare un percorso alternativo per gestire timeout o errori, garantendo un’esperienza fluida.

![](assets/journey-condition.png)

Scopri come definire una condizione in [questa sezione](conditions.md).

Sono disponibili i seguenti tipi di condizioni:

* [Condizione Data Source](condition-activity.md#data_source_condition)
* [Condizione temporale](condition-activity.md#time_condition)
* [Divisione percentuale](condition-activity.md#percentage_split)
* [Condizione data](condition-activity.md#date_condition)
* [Limite del profilo](condition-activity.md#profile_cap)
