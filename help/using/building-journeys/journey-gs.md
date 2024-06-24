---
solution: Journey Optimizer
product: journey optimizer
title: Creare il primo percorso
description: Passaggi chiave per creare il primo percorso con Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: percorso, primo, inizio, avvio rapido, pubblico, evento, azione
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 619bcbc16b4117c29c482c85323603a4281298e0
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 22%

---

# Creare il primo percorso{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Creare i percorsi"
>abstract="Utilizza **Adobe Journey Optimizer** per generare l’orchestrazione in tempo reale per diversi casi d’uso, sfruttando i dati contestuali provenienti da eventi od origini dati."


## Prerequisiti{#start-prerequisites}

Per inviare messaggi con i percorsi, sono necessarie le seguenti configurazioni:

1. **Configurare un evento**: se desideri attivare i percorsi in modo unitario quando viene ricevuto un evento, devi configurare un evento. È possibile definire le informazioni previste e le modalità di elaborazione. Questo passaggio viene eseguito da un **utente tecnico**. [Ulteriori informazioni](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Creare un pubblico**: il tuo percorso può anche ascoltare i tipi di pubblico di Adobe Experience Platform per inviare messaggi in batch a un set specifico di profili. A questo scopo, devi creare dei tipi di pubblico. [Ulteriori informazioni](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **Configurare l’origine dati**: è possibile definire una connessione a un sistema per il recupero di informazioni aggiuntive che verranno utilizzate nei percorsi, ad esempio nelle condizioni specificate. Al momento del provisioning, viene configurata anche un’origine dati integrata in Adobe Experience Platform. Se sfrutti solo i dati degli eventi del tuo percorso, questo passaggio non è necessario Questo passaggio viene eseguito da un **utente tecnico**. [Ulteriori informazioni](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurare un’azione**: se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni [sezione](../action/action.md). Questo passaggio viene eseguito da un **utente tecnico**. Se utilizzi le funzionalità per messaggi integrate di Journey Optimizer, devi solo aggiungere un’azione di canale al percorso e progettare il contenuto.

   ![](assets/custom2.png)

## Percorsi di accesso {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Percorsi"
>abstract="Progetta i percorsi cliente per offrire esperienze personalizzate e contestuali. Journey Optimizer consente di creare casi d’uso di orchestrazione in tempo reale sfruttando i dati contestuali archiviati negli eventi o nelle origini dati. La scheda **Panoramica** visualizza una dashboard con metriche chiave relative ai percorsi. La scheda **Sfoglia** presenta l’elenco dei percorsi esistenti."

### Elenco delle metriche chiave e dei percorsi {#access-metrics}

Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Percorsi]**. Sono disponibili due schede:

**Panoramica**: in questa scheda viene visualizzato un dashboard con le metriche chiave correlate ai percorsi:

* **Profili elaborati**: numero totale di profili elaborati nelle ultime 24 ore
* **Percorsi live**: numero totale di percorsi live con traffico nelle ultime 24 ore. I percorsi live includono **Percorsi unitari** (basato su eventi) e **Percorsi batch** (pubblico di lettura).
* **Percentuale di errori**: rapporto tra tutti i profili con errore e il numero totale di profili immessi nelle ultime 24 ore.
* **Percentuale di eliminazione**: rapporto tra tutti i profili scartati e il numero totale di profili immessi nelle ultime 24 ore. Un profilo scartato rappresenta un utente non idoneo per l’accesso al percorso, ad esempio a causa di uno spazio dei nomi errato o di regole di rientro.

>[!NOTE]
>
>Questa dashboard tiene conto dei percorsi con traffico nelle ultime 24 ore. Vengono visualizzati solo i percorsi a cui hai accesso. Le metriche vengono aggiornate ogni 30 minuti e solo quando sono disponibili nuovi dati.

![](assets/journeys-dashboard.png)

**Sfoglia**: in questa scheda viene visualizzato l’elenco dei percorsi esistenti. Puoi cercare percorsi, utilizzare filtri ed eseguire azioni di base su ciascun elemento. È ad esempio possibile duplicare o eliminare un elemento. Per ulteriori informazioni, consulta [questa sezione](../start/user-interface.md#filter-lists).

![](assets/journeys-browse.png)

### Filtra percorsi {#filter}

Nell’elenco dei percorsi, puoi sfruttare diversi filtri per perfezionare l’elenco dei percorsi in modo da migliorarne la leggibilità.

![](assets/filter-journeys.png)

Di seguito sono elencate le varie operazioni di filtro che è possibile eseguire:

Filtra i percorsi in base al loro stato, tipo, versione e tag assegnati dal **[!UICONTROL Filtri di stato e di versione]**.

Il tipo può essere: **[!UICONTROL Evento unitario]**, **[!UICONTROL Qualificazione del pubblico]**, **[!UICONTROL Read audience]** o **[!UICONTROL Evento di business]**.

Lo stato può essere:

* **Chiuso**: il percorso è stato chiuso utilizzando **Chiudi ai nuovi ingressi** pulsante. Il percorso non consente più l&#39;ingresso di nuovi individui nel percorso. Le persone già nel percorso possono finire il percorso normalmente.
* **Bozza**: il percorso è alla sua prima fase. Non è ancora stato pubblicato.
* **Bozza (prova)**: la modalità di test è stata attivata utilizzando **Modalità di test** pulsante.
* **Completato**: il percorso passa automaticamente a questo stato dopo 91 giorni [timeout globale](journey-properties.md#global_timeout). I profili già presenti nel percorso completano normalmente il percorso. I nuovi profili non possono più entrare nel percorso.
* **Live**: il percorso è stato pubblicato utilizzando **Pubblica** pulsante.
* **Interrotto**: il percorso è stato spento utilizzando **Interrompi** pulsante. Tutti gli individui escono immediatamente dal percorso.

>[!NOTE]
>
>Il ciclo di vita di authoring del Percorso include anche un set di stati intermedi che non sono disponibili per il filtro: &quot;Pubblicazione&quot; (tra &quot;Bozza&quot; e &quot;Live&quot;), &quot;Attivazione modalità di test&quot; o &quot;Disattivazione modalità di test&quot; (tra &quot;Bozza&quot; e &quot;Bozza (test)&quot;) e &quot;Interruzione&quot; (tra &quot;Live&quot; e &quot;Interrotto&quot;). Quando un percorso si trova in uno stato intermedio, è di sola lettura.

Utilizza il **[!UICONTROL Creazione di filtri]** per filtrare i percorsi in base alla data di creazione o all&#39;utente che li ha creati.

Visualizza i percorsi che utilizzano un evento, un gruppo di campi o un&#39;azione specifica del **[!UICONTROL Filtri di attività]** e **[!UICONTROL Filtri dati]**.

Utilizza il **[!UICONTROL Filtri di pubblicazione]** per selezionare una data di pubblicazione o un utente. Ad esempio, puoi scegliere di visualizzare le versioni più recenti dei percorsi live pubblicati ieri.

Per filtrare i percorsi in base a un intervallo di date specifico, seleziona **[!UICONTROL Personalizzato]** dal **[!UICONTROL Pubblicato]** elenco a discesa.

Inoltre, nei riquadri di configurazione Evento, Origine dati e Azione, il **[!UICONTROL Utilizzato in]** in questo campo viene visualizzato il numero di percorsi che utilizzano quel particolare evento, gruppo di campi o azione. Per visualizzare l’elenco dei percorsi corrispondenti, puoi fare clic sul pulsante **[!UICONTROL Visualizza percorsi]**.

![](assets/journey3bis.png)

## Creare il percorso {#jo-build}

Progetta percorsi per offrire esperienze personalizzate e contestuali. [!DNL Journey Optimizer] consente di creare casi di utilizzo di orchestrazione in tempo reale sfruttando i dati contestuali archiviati negli eventi o nelle origini dati. Puoi progettare scenari avanzati a più passaggi basati sulle seguenti funzionalità:

* Invia in tempo reale una **consegna unitaria** attivata quando viene ricevuto un evento o **in batch** utilizzando i tipi di pubblico di Adobe Experience Platform.

* Sfrutta **dati contestuali** da eventi, informazioni da Adobe Experience Platform o dati da servizi API di terze parti.

* Utilizza il **azioni del canale incorporate** (E-mail, SMS, push, inApp) per inviare messaggi progettati in [!DNL Journey Optimizer] o creare **azioni personalizzate** se utilizzi un sistema di terze parti per l’invio dei messaggi.

* Con **journey designer**, genera casi d’uso a più passaggi: trascina facilmente un evento di ingresso o un’attività Leggi pubblico, aggiungi delle condizioni e invia messaggi personalizzati.

➡️ [Scopri questa funzione nel video](journey.md#video)

Di seguito sono elencati i passaggi per l’invio di messaggi tramite percorsi:

1. Dalla sezione **Sfoglia** , fare clic su **[!UICONTROL Crea Percorso]** per creare un nuovo percorso.

1. Modifica le proprietà del percorso nel riquadro di configurazione visualizzato sul lato destro. Scopri come impostare le proprietà del percorso in questo [questa pagina](journey-properties.md).

   ![](assets/jo-properties.png)

1. Per iniziare, trascina e rilascia un evento o una **Read Audience** dalla palette all’area di lavoro. Per ulteriori informazioni sulla progettazione del percorso, fare riferimento a [questa sezione](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Trascina e rilascia i passaggi successivi che il singolo utente seguirà. Ad esempio, puoi aggiungere una condizione seguita da un’azione di canale. Per ulteriori informazioni sulle attività, consulta [questa sezione](using-the-journey-designer.md).

1. Verifica il percorso utilizzando i profili di test. Ulteriori informazioni [sezione](testing-the-journey.md)

1. Pubblica il percorso per attivarlo. Ulteriori informazioni [sezione](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitora il tuo percorso utilizzando gli strumenti di reporting dedicati per misurare l’efficacia del percorso. Ulteriori informazioni [sezione](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)


## Duplicare un percorso {#duplicate-a-journey}

È possibile duplicare un percorso esistente da **Sfoglia** scheda. Tutti gli oggetti e le impostazioni vengono duplicati nella copia di percorso.

Per farlo, segui la procedura indicata di seguito:

1. Passare al percorso che si desidera copiare, fare clic sul pulsante **Altre azioni** (i tre punti accanto al nome del percorso).
1. Seleziona **Duplica**.

   ![Duplicare un percorso](assets/duplicate-jo.png)

1. Inserisci il nome del percorso e conferma. È inoltre possibile modificare il nome nella schermata delle proprietà del percorso. Per impostazione predefinita, il nome viene impostato come segue: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. Il nuovo percorso viene creato e disponibile nell&#39;elenco percorso.
