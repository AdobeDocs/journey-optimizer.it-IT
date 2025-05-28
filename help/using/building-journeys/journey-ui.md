---
solution: Journey Optimizer
product: journey optimizer
title: Sfogliare e filtrare i percorsi
description: Sfogliare e filtrare i percorsi in Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: percorso, primo, inizio, avvio rapido, pubblico, evento, azione
exl-id: 770bdbf2-560d-4127-bdb9-1f82495a566f
source-git-commit: 29d12b6190f49e7f3f6fd2760e522a5a62c0de87
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 9%

---

# Sfogliare e filtrare i percorsi {#browse-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_view"
>title="Visualizzazioni elenco percorsi e calendario"
>abstract="Oltre all&#39;elenco percorsi, [!DNL Journey Optimizer] fornisce una visualizzazione calendario dei percorsi, offrendo una chiara rappresentazione visiva delle loro pianificazioni. È possibile passare dalla visualizzazione elenco alla visualizzazione calendario in qualsiasi momento utilizzando questi pulsanti."

## Dashboard del percorso {#dashboard-jo}

Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Percorsi]**. Sono disponibili due schede: **[!UICONTROL Panoramica]** e **[!UICONTROL Sfoglia]**.

### Panoramica sui percorsi

Nella scheda **[!UICONTROL Panoramica]** è visualizzata una dashboard con le metriche chiave correlate ai percorsi.

![Dashboard di percorso che evidenzia la scheda Panoramica](assets/journeys-dashboard.png)

* **Profili elaborati**: numero totale di profili elaborati nelle ultime 24 ore
* **percorsi live**: numero totale di percorsi live con traffico nelle ultime 24 ore. I percorsi attivi includono **percorsi unitari** (basati su eventi) e **percorsi batch** (pubblico di lettura).
* **Frequenza errori**: rapporto tra tutti i profili con errore e il numero totale di profili immessi nelle ultime 24 ore.
* **Percentuale di eliminazione**: rapporto tra tutti i profili eliminati e il numero totale di profili immessi nelle ultime 24 ore. Un profilo scartato rappresenta un utente non idoneo per l’accesso al percorso, ad esempio a causa di uno spazio dei nomi errato o di regole di rientro.

>[!NOTE]
>
>Questa dashboard tiene conto dei percorsi con traffico nelle ultime 24 ore. Vengono visualizzati solo i percorsi a cui hai accesso. Le metriche vengono aggiornate ogni 30 minuti e solo quando sono disponibili nuovi dati.

### Elenco percorsi

La scheda **[!UICONTROL Sfoglia]** mostra l&#39;elenco dei percorsi esistenti. Puoi cercare percorsi, utilizzare filtri ed eseguire azioni di base su ciascun elemento. Ad esempio, è possibile duplicare o eliminare un elemento.

![Dashboard di percorso che evidenzia la scheda Sfoglia](assets/journeys-browse.png)

### Calendario percorsi {#calendar}

Oltre all&#39;elenco percorsi, [!DNL Journey Optimizer] fornisce una visualizzazione calendario dei percorsi, offrendo una chiara rappresentazione visiva delle loro pianificazioni.

>[!AVAILABILITY]
>
>La vista Calendario è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per richiedere l&#39;accesso, usa [questo modulo](https://forms.cloud.microsoft/r/FC49afuJVi){target=”_blank”}.
>
>Questa funzione è in fase di sviluppo attivo. L&#39;input e le richieste vengono accolti con favore utilizzando il pulsante **[!UICONTROL Feedback Beta]** nel menu principale.

Per accedere alla vista calendario, aprire l&#39;elenco percorsi e fare clic sull&#39;icona ![icona calendario](assets/do-not-localize/timeline-icon.svg).

Nel calendario vengono visualizzati tutti i percorsi programmati per la settimana corrente. Utilizza i pulsanti freccia sopra il calendario per spostarti tra le settimane.

![visualizzazione calendario con percorsi attivi](assets/timeline-journeys.png)

Modalità di rappresentazione dei percorsi:

* Per impostazione predefinita, la griglia calendario mostra tutti i percorsi attivi e pianificati per la settimana selezionata. Altre opzioni di filtro possono mostrare attivazioni o attivazioni completate, interrotte e terminate.
* I percorsi 2D e i percorsi in modalità di test non vengono visualizzati.
* I percorsi che si estendono su più giorni vengono visualizzati nella parte superiore della griglia del calendario.
* Se non viene specificato alcun orario di inizio, viene utilizzato il tempo di attivazione manuale più vicino per posizionarlo nel calendario.
* I percorsi vengono visualizzati come intervalli di 1 ora, ma questo non riflette l’ora effettiva di invio o completamento.

Per ulteriori dettagli su un percorso, fai clic sul relativo blocco visivo per aprirne ed esplorarne i dettagli.

Nell’elenco dei percorsi vengono visualizzate tutte le versioni dei percorsi e i relativi numeri di versione. Quando cerchi un percorso, la prima volta che apri l’applicazione le versioni più recenti vengono visualizzate nella parte superiore dell’elenco. Successivamente, puoi definire l’ordinamento desiderato, che verrà mantenuto dall’applicazione come preferenza utente. La versione del percorso viene visualizzata anche nella parte superiore dell’interfaccia dell’edizione del percorso, sopra l’area di lavoro. Ulteriori informazioni sulla [gestione versione percorso](publishing-the-journey.md#journey-versions-journey-versions).



## Filtrare i percorsi {#journey-filter}

Nell’elenco dei percorsi, utilizza vari filtri per perfezionare l’elenco dei percorsi.

![Schermata che mostra un esempio di filtro percorso con due tipi di percorsi selezionati](assets/filter-journeys.png)

Puoi filtrare i percorsi in base al loro [stato](#journey-statuses), [tipo](#journey-types), [versione](publishing-the-journey.md#journey-versions-journey-versions) e assegnare [tag](../start/search-filter-categorize.md#tags) dai **[!UICONTROL filtri di stato e versione]**.

Utilizza **[!UICONTROL Creation filters]** per filtrare i percorsi in base alla data di creazione o all&#39;utente che li ha creati.

Visualizza percorsi che utilizzano un evento, un gruppo di campi o un&#39;azione specifica dei **[!UICONTROL Filtri di attività]** e **[!UICONTROL Filtri di dati]**.

Utilizza **[!UICONTROL Filtri di pubblicazione]** per selezionare una data di pubblicazione o un utente. Ad esempio, puoi scegliere di visualizzare le versioni più recenti dei percorsi live pubblicati ieri.

Per filtrare i percorsi in base a un intervallo di date specifico, seleziona **[!UICONTROL Personalizzato]** dall&#39;elenco a discesa **[!UICONTROL Pubblicato]**.

Inoltre, nei riquadri di configurazione dell&#39;evento, dell&#39;origine dati e dell&#39;azione, il campo **[!UICONTROL Usato in]** mostra il numero di percorsi che utilizzano quel particolare evento, gruppo di campi o azione. Per visualizzare l’elenco dei percorsi corrispondenti, puoi fare clic sul pulsante **[!UICONTROL Visualizza percorsi]**.

![](assets/journey3bis.png)

## Tipi di percorso {#journey-types}

Il tipo di percorso dipende dalle attività utilizzate in tale percorso. Può essere:

* **[!UICONTROL Evento unitario]** - I percorsi di eventi unitari sono collegati a un profilo specifico. Gli eventi si riferiscono al comportamento di una persona o a qualcosa che si verifica in relazione a una persona (ad esempio, una persona ha raggiunto 10.000 punti fedeltà). [Ulteriori informazioni](../event/about-events.md).
* **[!UICONTROL Evento di business]**. Il percorso degli eventi di business inizia con un evento non correlato al profilo. La configurazione dell’evento viene eseguita da un utente tecnico e non può essere modificata. [Ulteriori informazioni](../event/about-events.md).
* **[!UICONTROL Qualificazione del pubblico]** - I percorsi di qualificazione del pubblico ascoltano le entrate e le uscite dei profili nei tipi di pubblico di Adobe Experience Platform per consentire a singoli utenti di entrare o proseguire in un percorso. [Ulteriori informazioni](audience-qualification-events.md).
* **[!UICONTROL Read audience]** - Nei percorsi Read audience, tutti i singoli utenti del pubblico entrano nel percorso e ricevono i messaggi inclusi nel percorso.  [Ulteriori informazioni](read-audience.md).


Ulteriori informazioni sui tipi di percorso e sulla gestione delle voci associate in [questa pagina](entry-management.md).

## Stati percorso {#journey-statuses}

Lo stato del percorso dipende dal suo ciclo di vita. Può essere:

* **Chiuso**: il percorso è stato chiuso utilizzando il pulsante **Chiudi ai nuovi ingressi**. Il percorso non consente più l&#39;ingresso di nuovi individui nel percorso. Le persone già nel percorso possono finire il percorso normalmente.
* **Bozza**: il percorso è nella prima fase. Non è ancora stato pubblicato.
* **Bozza (Test)**: la modalità di test è stata attivata utilizzando il pulsante **Modalità di test**.
* **Fine**: il percorso passa automaticamente a questo stato dopo il [timeout globale](journey-properties.md#global_timeout) di 91 giorni. I profili già presenti nel percorso completano normalmente il percorso. I nuovi profili non possono più entrare nel percorso.
* **Live**: il percorso è stato pubblicato utilizzando il pulsante **Pubblica**.
* **Interrotto**: il percorso è stato disattivato utilizzando il pulsante **Interrompi**. Tutti gli individui escono immediatamente dal percorso.

>[!NOTE]
>
>* Il ciclo di vita di authoring del Percorso include anche un set di stati intermedi che non sono disponibili per il filtro: &quot;Pubblicazione&quot; (tra &quot;Bozza&quot; e &quot;Live&quot;), &quot;Attivazione modalità di test&quot; o &quot;Disattivazione modalità di test&quot; (tra &quot;Bozza&quot; e &quot;Bozza (test)&quot;) e &quot;Interruzione&quot; (tra &quot;Live&quot; e &quot;Interrotto&quot;). Quando un percorso si trova in uno stato intermedio, è di sola lettura.
>
>* Se devi modificare un percorso **live**, [crea una nuova versione](#journey-versions) del percorso.


## Duplicare un percorso {#duplicate-a-journey}

Puoi duplicare un percorso esistente dalla scheda **Sfoglia**. Tutti gli oggetti e le impostazioni vengono duplicati nella copia di percorso.

Per farlo, segui la procedura indicata di seguito:

1. Passa al percorso da copiare, fai clic sull&#39;icona **Altre azioni** (i tre punti accanto al nome del percorso).
1. Seleziona **Duplica**.

   ![Duplica un percorso](assets/duplicate-jo.png)

1. Inserisci il nome del percorso e conferma. È inoltre possibile modificare il nome nella schermata delle proprietà del percorso. Per impostazione predefinita, il nome è impostato come segue: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. Il nuovo percorso viene creato e disponibile nell&#39;elenco percorso.
