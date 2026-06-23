---
solution: Journey Optimizer
product: journey optimizer
title: Sfogliare e filtrare i percorsi
description: Sfoglia e filtra i percorsi in [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: percorso, primo, inizio, avvio rapido, pubblico, evento, azione
exl-id: 770bdbf2-560d-4127-bdb9-1f82495a566f
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 2066
ht-degree: 9%

---

# Sfogliare e filtrare i percorsi {#browse-journeys}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come sfogliare, cercare e filtrare i percorsi utilizzando le visualizzazioni Dashboard di percorso, Elenco e Calendario in Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_view"
>title="Visualizzazioni calendario ed elenco percorsi"
>abstract="Oltre all’elenco percorsi, [!DNL Journey Optimizer] fornisce una visualizzazione del calendario dei percorsi, offrendo una chiara rappresentazione visiva delle relative pianificazioni. Questi pulsanti consentono di passare in qualsiasi momento dalla visualizzazione elenco alla visualizzazione calendario."

## Dashboard del percorso {#dashboard-jo}

Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Percorsi]**. Sono disponibili due schede: **[!UICONTROL Panoramica]** e **[!UICONTROL Sfoglia]**.

### Panoramica sui percorsi

La scheda **[!UICONTROL Panoramica]** visualizza una dashboard con metriche chiave relative ai percorsi.

![Dashboard di Percorso che evidenzia la scheda Panoramica](assets/journeys-dashboard.png)

* **Profili elaborati**: numero totale di profili elaborati nelle ultime 24 ore
* **percorsi live**: numero totale di percorsi live con traffico nelle ultime 24 ore. I percorsi attivi includono **percorsi unitari** (basati su eventi) e **percorsi batch** (pubblico di lettura).
* **Frequenza errori**: rapporto tra tutti i profili con errore e il numero totale di profili immessi nelle ultime 24 ore.
* **Percentuale di eliminazione**: rapporto tra tutti i profili eliminati e il numero totale di profili immessi nelle ultime 24 ore. Un profilo scartato rappresenta un utente non idoneo per l’accesso al percorso, ad esempio a causa di uno spazio dei nomi o di regole di rientro non corrette.

>[!NOTE]
>
>Questa dashboard tiene conto dei percorsi con traffico nelle ultime 24 ore. Vengono visualizzati solo i percorsi a cui hai accesso. Le metriche vengono aggiornate ogni 30 minuti e solo quando sono disponibili nuovi dati.

### Elenco percorsi

La scheda **[!UICONTROL Sfoglia]** mostra l&#39;elenco dei percorsi esistenti. Puoi cercare percorsi, utilizzare filtri ed eseguire azioni di base su ciascun elemento. Ad esempio, è possibile duplicare o eliminare un elemento.

![Dashboard di percorso che evidenzia la scheda Sfoglia](assets/journeys-browse.png)

Nell’elenco dei percorsi vengono visualizzate tutte le versioni dei percorsi e i relativi numeri di versione. Quando cerchi un percorso, la prima volta che apri l’applicazione le versioni più recenti vengono visualizzate nella parte superiore dell’elenco. Successivamente, puoi definire l’ordinamento desiderato, che verrà mantenuto dall’applicazione come preferenza utente. La versione del percorso viene visualizzata anche nella parte superiore dell’interfaccia di modifica del percorso, sopra l’area di lavoro. Ulteriori informazioni sulla [gestione versione percorso](publish-journey.md#journey-versions).

### Calendario percorsi {#calendar}

Oltre all’elenco percorsi, [!DNL Journey Optimizer] fornisce una visualizzazione del calendario dei percorsi, offrendo una chiara rappresentazione visiva delle relative pianificazioni.

Modalità di rappresentazione dei percorsi:

* Per impostazione predefinita, la griglia del calendario mostra tutti i percorsi attivi e pianificati per la settimana selezionata. Altre opzioni di filtro possono mostrare attivazioni o attivazioni completate, interrotte e terminate.
* I percorsi 2D e i percorsi in modalità di test non vengono visualizzati.
* I percorsi che si estendono su più giorni vengono visualizzati nella parte superiore della griglia del calendario.
* Se non viene specificato alcun orario di inizio, viene utilizzato il tempo di attivazione manuale più vicino per posizionarlo nel calendario.
* I percorsi vengono visualizzati come intervalli di 1 ora, ma questo non riflette l’ora effettiva di invio o completamento.

Per spostarsi nel calendario dei Percorsi:

1. Per accedere alla vista calendario, aprire l&#39;elenco percorsi e fare clic sull&#39;icona ![Calendario per passare alla vista calendario](assets/do-not-localize/timeline-icon.svg).

1. Utilizza i pulsanti freccia o il selettore data sopra il calendario per spostarti tra le settimane.

   Nel calendario vengono visualizzati tutti i percorsi programmati per la settimana corrente.

   ![visualizzazione calendario con percorsi attivi](assets/timeline-journeys.png)

1. Fai clic sull&#39;icona ![Impostazioni per attivare/disattivare la visualizzazione di più percorsi](assets/do-not-localize/Smock_Gears_18_N.png) per attivare/disattivare la visualizzazione degli elementi che si estendono su più giorni o settimane.

   ![visualizzazione calendario con campagne live](assets/journey-calendar-1.png)

1. Fai clic sull&#39;icona ![Aggiungi calendario esterno](assets/do-not-localize/Smock_CalendarAdd_18_N.svg) per gestire e aggiungere fino a tre calendari esterni.

   ![visualizzazione calendario con calendari esterni](assets/journey-calendar-2.png)

1. Trascina e rilascia i file CSV contenenti i nomi degli eventi, le date di inizio e di fine.

   Gli eventi caricati vengono visualizzati per tutti gli utenti dell’organizzazione e sono visualizzati sia sul calendario di Percorso che su quello di Campaign.

   +++Il formato CSV deve essere il seguente:

   | Colonna1 | Colonna2 | Colonna3 |
   |-|-|-|
   | Nome evento | Data di inizio in formato mm/gg/aa | Data di fine in formato mm/gg/aa |

   +++

1. Se necessario, è possibile nascondere, visualizzare o rimuovere i calendari esterni aggiunti.

   ![visualizzazione calendario con calendari esterni](assets/journey-calendar-3.png)

1. Per ulteriori dettagli su un percorso, fai clic sul relativo blocco visivo per aprirne ed esplorarne i dettagli.

   ![elenco campagne con riquadro informazioni aperto](assets/journey-calendar-4.png)


## Filtrare i percorsi {#journey-filter}

Nell’elenco dei percorsi, utilizza vari filtri per perfezionare l’elenco dei percorsi.

![Schermata che mostra un esempio di filtro percorso con due tipi di percorsi selezionati](assets/filter-journeys.png)

Puoi filtrare i percorsi in base al loro [stato](#journey-statuses), [tipo](#journey-types), [versione](publish-journey.md#journey-versions) e assegnare [tag](../start/search-filter-categorize.md#tags) dai **[!UICONTROL filtri di stato e versione]**.

Utilizza **[!UICONTROL Creation filters]** per filtrare i percorsi in base alla data di creazione o all&#39;utente che li ha creati.

Visualizza percorsi che utilizzano un evento, un gruppo di campi o un&#39;azione specifica dei **[!UICONTROL Filtri di attività]** e **[!UICONTROL Filtri di dati]**.

Utilizza **[!UICONTROL Filtri di pubblicazione]** per selezionare una data di pubblicazione o un utente. Ad esempio, puoi scegliere di visualizzare le versioni più recenti dei percorsi live pubblicati ieri.

Per filtrare i percorsi in base a un intervallo di date specifico, seleziona **[!UICONTROL Personalizzato]** dall&#39;elenco a discesa **[!UICONTROL Pubblicato]**.

Inoltre, nei riquadri di configurazione dell&#39;evento, dell&#39;origine dati e dell&#39;azione, il campo **[!UICONTROL Usato in]** mostra il numero di percorsi che utilizzano quel particolare evento, gruppo di campi o azione. Per visualizzare l’elenco dei percorsi corrispondenti, puoi fare clic sul pulsante **[!UICONTROL Visualizza percorsi]**.

![Utilizzato nel campo che mostra il numero di percorsi utilizzando un evento o un&#39;azione](assets/journey3bis.png)

## Tipi di percorso {#journey-types}

Il tipo di percorso dipende dalle attività utilizzate in tale percorso. Può essere:

* **[!UICONTROL Evento unitario]** - I percorsi di eventi unitari sono collegati a un profilo specifico. Gli eventi si riferiscono al comportamento di una persona o a qualcosa che si verifica in relazione a una persona (ad esempio, una persona ha raggiunto 10.000 punti fedeltà). [Ulteriori informazioni](../event/about-events.md).
* **[!UICONTROL Evento di business]**. Il percorso degli eventi di business inizia con un evento non correlato al profilo. La configurazione dell’evento viene eseguita da un utente tecnico e non può essere modificata. [Ulteriori informazioni](../event/about-events.md).
* **[!UICONTROL Qualificazione del pubblico]** - I percorsi di qualificazione del pubblico ascoltano le entrate e le uscite dei profili in [!DNL Adobe Experience Platform] tipi di pubblico per consentire a singoli utenti di entrare o proseguire in un percorso. [Ulteriori informazioni](audience-qualification-events.md).
* **[!UICONTROL Read audience]** - Nei percorsi Read audience, tutti i singoli utenti del pubblico entrano nel percorso e ricevono i messaggi inclusi nel percorso.  [Ulteriori informazioni](read-audience.md).


Ulteriori informazioni sui tipi di percorso e sulla gestione delle voci associate in [questa pagina](entry-management.md).

## Stati percorso {#journey-statuses}

Lo stato del percorso dipende dal suo ciclo di vita. Può essere:

* **Bozza**: il percorso è nella prima fase. Non è ancora stata pubblicata.
* **Bozza (Test)**: la modalità di test è stata attivata utilizzando il pulsante **Modalità di test**. [Ulteriori informazioni](../building-journeys/testing-the-journey.md)
* **Completato**: il percorso passa automaticamente a questo stato in base al tipo e alla configurazione del percorso. I profili già presenti nel percorso completano normalmente il percorso. I nuovi profili non possono più entrare nel percorso. [Scopri quando i percorsi sono considerati finiti](end-journey.md#journey-finished-definition).
* **Live**: il percorso è stato pubblicato utilizzando il pulsante **Pubblica**. [Ulteriori informazioni](../building-journeys/publish-journey.md)
* **Sospeso**: il percorso live è stato messo in pausa utilizzando il pulsante **Sospendi**. [Ulteriori informazioni](../building-journeys/journey-pause.md)
* **Interrotto**: il percorso è stato disattivato utilizzando il pulsante **Interrompi**. Tutti gli individui escono immediatamente dal percorso. [Ulteriori informazioni](../building-journeys/end-journey.md#stop-journey)
* **Chiuso**: il percorso è stato chiuso utilizzando il pulsante **Chiudi ai nuovi ingressi**. Il percorso non consente più l&#39;ingresso di nuovi individui nel percorso. Le persone già nel percorso possono finire il percorso normalmente. [Ulteriori informazioni](../building-journeys/end-journey.md)

>[!NOTE]
>
>* Il ciclo di vita di authoring del Percorso include anche un set di stati intermedi che non sono disponibili per il filtro: **Pubblicazione** (tra &quot;Bozza&quot; e &quot;Live&quot;), **Attivazione modalità test** o **Disattivazione modalità test** (tra **Bozza** e **Bozza (test)**), **Interruzione** (tra **Live** e **Interrotto**), **Ripresa** (tra **In pausa** e **Live**), **In pausa** (tra **Live** e **In pausa**) Quando un percorso si trova in uno stato intermedio, è di sola lettura.
>
>* Se devi modificare un percorso **Live**, [crea una nuova versione](#journey-versions) del percorso. Puoi anche mettere in pausa i percorsi live, apportare tutte le modifiche necessarie e riprenderli in qualsiasi momento. [Ulteriori informazioni sulla sospensione dei percorsi](../building-journeys/journey-pause.md)


## Duplicare un percorso {#duplicate-a-journey}

Puoi duplicare un percorso esistente dalla scheda **Sfoglia**. Tutti gli oggetti e le impostazioni vengono duplicati nella copia di percorso.

Per farlo, segui la procedura indicata di seguito:

1. Passa al percorso da copiare, fai clic sull&#39;icona **Altre azioni** (i tre punti accanto al nome del percorso).
1. Seleziona **Duplica**.

   ![Duplica un percorso](assets/duplicate-jo.png)

1. Inserisci il nome del percorso e conferma. È inoltre possibile modificare il nome nella schermata delle proprietà del percorso. Per impostazione predefinita, il nome è impostato come segue: `[JOURNEY-NAME]_copy`

   ![Campo di input nome Percorso per percorso duplicato](assets/duplicate-jo2.png)

1. Il nuovo percorso viene creato e disponibile nell&#39;elenco percorso.


## Operazioni in blocco {#bulk-operations}

Dall&#39;elenco dei percorsi, puoi sospendere più di **Live** percorsi. Per mettere in pausa un gruppo di percorsi (_pausa collettiva_), selezionali nell&#39;elenco e fai clic sul pulsante **Pausa** nella barra blu nella parte inferiore della schermata. Il pulsante **Pausa** è disponibile solo quando sono selezionati **percorsi di disponibilità**.

![Sospendi in blocco due percorsi live dalla barra inferiore](assets/bulk-pause-journeys.png)

Puoi anche riprendere uno o più **percorsi in pausa**. Per riprendere un gruppo di percorsi (_Riprendi in blocco_), selezionali e fai clic sul pulsante **Riprendi** nella barra blu nella parte inferiore della schermata. Il pulsante **Riprendi** sarà disponibile solo quando sono selezionati **percorsi in pausa**.

[Ulteriori informazioni sui percorsi di pausa/ripresa](journey-pause.md).

>[!NOTE]
>
>Puoi sospendere/riprendere fino a 10 percorsi per operazione.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come sfogliare, filtrare, visualizzare (elenco e calendario), duplicare ed eseguire operazioni in blocco sui percorsi dal dashboard di Journey Optimizer.

**Intenti:**

* Sfogliare e cercare i percorsi dalle schede Panoramica e Sfoglia
* Filtra percorsi per stato, tipo, versione, tag, data di creazione o data di pubblicazione
* Passa dalla vista a elenco alla vista calendario per visualizzare le pianificazioni del percorso
* Aggiungere e gestire calendari esterni caricando file CSV
* Duplica un percorso esistente per riutilizzarne le impostazioni
* Sospendi o riprendi più percorsi live o in pausa contemporaneamente

**Glossario:**

* **Dashboard dei Percorsi**: interfaccia principale dei percorsi con una scheda Panoramica che mostra le metriche chiave e una scheda Sfoglia che elenca tutti i percorsi. *(specifico per prodotto)*
* **Percentuale di eliminazione**: il rapporto tra i profili non idonei a entrare nel percorso (ad esempio, a causa di spazi dei nomi o regole di rientro non corrette) e il totale dei profili che hanno tentato di entrare nelle ultime 24 ore. *(specifico per prodotto)*
* **Visualizzazione calendario Percorsi**: una rappresentazione visiva settimanale del calendario dei percorsi live e pianificati, accessibile facendo clic sull&#39;icona del calendario nell&#39;elenco dei percorsi. *(specifico per prodotto)*
* **Pausa collettiva**: operazione che mette in pausa più percorsi attivi contemporaneamente (fino a 10 per operazione) dall&#39;elenco percorsi. *(specifico per prodotto)*

**Guardrail:**

* Le metriche della dashboard vengono aggiornate ogni 30 minuti e solo quando sono disponibili nuovi dati; coprono solo le ultime 24 ore
* I percorsi bozza e i percorsi in modalità di test non vengono visualizzati nella vista calendario
* La pausa/ripresa in blocco è limitata a 10 percorsi per operazione
* Il pulsante Riprendi è attivo solo quando sono selezionati percorsi in pausa; il pulsante Pausa è attivo solo quando sono selezionati percorsi attivi
* Il calendario visualizza i percorsi come intervalli di tempo di 1 ora indipendentemente dall’ora di invio o di completamento effettiva

**Terminologia:**

* Nome canonico: dashboard Percorso — Acronimo: none — varianti: elenco percorsi, panoramica percorsi
* Sinonimi: &quot;Sfoglia scheda&quot; = &quot;Elenco percorsi&quot;
* Non confondere: &quot;Tasso di eliminazione&quot; ≠ &quot;Tasso di errore&quot; — Profili con conteggi di tasso di eliminazione non idonei a essere immessi; Tasso di errore: conteggi di profili che sono stati immessi ma hanno riscontrato un errore di elaborazione

**Domande frequenti:**

* **D: dove posso trovare le metriche chiave delle prestazioni del percorso in breve?** — nella scheda Panoramica del dashboard Percorso, che mostra i profili elaborati, i percorsi live, il tasso di errore e il tasso di eliminazione per le ultime 24 ore.
* **D: come è possibile trovare percorsi che utilizzano un evento o un&#39;azione specifica?** — Utilizzare i filtri attività e i filtri dati nell&#39;elenco percorso per visualizzare i percorsi che fanno riferimento a un evento, un gruppo di campi o un&#39;azione specifica.
* **Q: posso sospendere più percorsi contemporaneamente?** — Sì; seleziona più percorsi attivi nell’elenco e fai clic sul pulsante Pausa nella barra inferiore. È possibile mettere in pausa fino a 10 percorsi per operazione.
* **D: come si aggiungono eventi esterni al calendario di percorso?** — Fai clic sull&#39;icona di aggiunta del calendario, quindi trascina e rilascia un file CSV con il nome dell&#39;evento, la data di inizio e la data di fine; gli eventi caricati sono visibili a tutti gli utenti dell&#39;organizzazione.
* **Q: perché nel calendario viene visualizzato un percorso di 1 ora anche se è più lungo?** — Il calendario visualizza tutti i percorsi come intervalli di tempo di 1 ora per coerenza visiva; questo non riflette l&#39;ora effettiva di invio o completamento.

+++

