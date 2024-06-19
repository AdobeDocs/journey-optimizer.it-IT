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
source-git-commit: 6ff54583c729175c74b3a7ea4ab9188505fde897
workflow-type: tm+mt
source-wordcount: '2623'
ht-degree: 12%

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
* **Completato**: il percorso passa automaticamente a questo stato dopo 91 giorni [timeout predefinito](journey-gs.md#global_timeout). I profili già presenti nel percorso completano normalmente il percorso. I nuovi profili non possono più entrare nel percorso.
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

## Creare il percorso{#jo-build}

Questo passaggio viene eseguito da **utente aziendale**. Qui è dove si creano i percorsi. Combina le diverse attività relative a eventi, orchestrazioni e azioni per creare scenari cross-channel con più passaggi.

➡️ [Scopri questa funzione nel video](journey.md#video)

Di seguito sono riportati i passaggi principali per l’invio di messaggi tramite percorsi:

1. Dalla sezione **Sfoglia** , fare clic su **[!UICONTROL Crea Percorso]** per creare un nuovo percorso.

1. Modifica le proprietà del percorso nel riquadro di configurazione visualizzato sul lato destro. Ulteriori informazioni [sezione](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Per iniziare, trascina e rilascia un evento o una **Read Audience** dalla palette all’area di lavoro. Per ulteriori informazioni sulla progettazione del percorso, fare riferimento a [questa sezione](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Trascina e rilascia i passaggi successivi che il singolo utente seguirà. Ad esempio, puoi aggiungere una condizione seguita da un’azione di canale. Per ulteriori informazioni sulle attività, consulta [questa sezione](using-the-journey-designer.md).

1. Verifica il percorso utilizzando i profili di test. Ulteriori informazioni [sezione](testing-the-journey.md)

1. Pubblica il percorso per attivarlo. Ulteriori informazioni [sezione](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitora il tuo percorso utilizzando gli strumenti di reporting dedicati per misurare l’efficacia del percorso. Ulteriori informazioni [sezione](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Definire le proprietà del percorso {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Proprietà del percorso"
>abstract="Questa sezione mostra le proprietà del percorso. Per impostazione predefinita, i parametri di sola lettura sono nascosti. Le impostazioni disponibili dipendono dallo stato del percorso, dalle autorizzazioni e dalla configurazione del prodotto."

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Criteri di uscita dal percorso"
>abstract="In questa sezione sono illustrate le opzioni relative ai criteri di uscita. Puoi creare una o più regole di criteri di uscita per il percorso."

Fai clic sull’icona della matita, accanto al nome del percorso, per accedere alle relative proprietà.

Puoi modificare il nome del percorso, aggiungere una descrizione, consentire il rientro, scegliere le date di inizio e di fine e, in qualità di utente amministratore, definire un’ **[!UICONTROL Timeout ed errore]** durata. Puoi anche assegnare tag unificati Adobe Experience Platform al tuo percorso. Questo consente di classificarle facilmente e migliorare la ricerca dall’elenco delle campagne. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags)

Per i percorsi live, questa schermata mostra la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso.

Il **Copia dettagli tecnici** consente di copiare le informazioni tecniche sul percorso che il team di supporto può utilizzare per la risoluzione dei problemi. Vengono copiate le seguenti informazioni: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Ingresso e rientro {#entrance}

Per impostazione predefinita, i nuovi percorsi consentono il rientro. È possibile deselezionare **Consenti rientro** opzione per percorsi &quot;one shot&quot;, ad esempio per offrire un regalo una tantum quando una persona entra in un negozio.

Quando **Consenti rientro** è attivata, la **Periodo di attesa per rientro** viene visualizzato. Questo campo ti consente di definire il tempo di attesa prima di consentire a un profilo di accedere nuovamente al percorso in percorsi unitari (a partire da un evento o da una qualificazione del pubblico). In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti. La durata massima è di 29 giorni.

Ulteriori informazioni sulla gestione dell’entrata e del rientro del profilo, in [questa sezione](entry-management.md).

### Gestisci accesso {#manage-access}

Per assegnare al percorso etichette di utilizzo dei dati personalizzate o di base, fai clic su **[!UICONTROL Gestisci accesso]** pulsante. [Ulteriori informazioni su OLE (Object Level Access Control)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### Fusi orari di percorso e profilo {#timezone}

Fuso orario definito a livello di percorso. Puoi immettere un fuso orario fisso o utilizzare i profili Adobe Experience Platform per definire il fuso orario del percorso. Se nel profilo Adobe Experience Platform è definito un fuso orario, questo può essere recuperato nel percorso.

Per ulteriori informazioni sulla gestione del fuso orario, consulta [questa pagina](../building-journeys/timezone-management.md).

### Date di inizio e fine {#dates}

È possibile definire un **Data di inizio**. Se non ne hai specificato uno, verrà definito automaticamente al momento della pubblicazione.

Puoi anche aggiungere una **Data di fine**. Questo consente ai profili di uscire automaticamente quando viene raggiunta la data. Se non viene specificata una data di fine, i profili possono rimanere fino al [timeout percorso globale](#global_timeout) (che è generalmente di 91 giorni, e ridotto a 7 giorni con l’offerta aggiuntiva Healthcare Shield). L’unica eccezione è rappresentata dai percorsi di pubblico ricorrenti in lettura con **Forza rientro in caso di ricorrenza** attivato, che termina alla data di inizio dell’occorrenza successiva.

### Timeout ed errore nelle attività del percorso {#timeout_and_error}

Quando modifichi un’attività di azione o condizione, puoi definire un percorso alternativo in caso di errore o timeout. Se l’elaborazione dell’attività che richiede l’interrogazione di un sistema di terze parti supera la durata di timeout definita nelle proprietà del percorso (**[!UICONTROL Timeout ed errore]** ), verrà scelto il secondo percorso per eseguire una potenziale azione di fallback.

I valori autorizzati sono compresi tra 1 e 30 secondi.

È consigliabile definire un valore molto breve **[!UICONTROL Timeout ed errore]** valore se il percorso è sensibile all’ora (ad esempio: reagire alla posizione in tempo reale di una persona) perché non è possibile ritardare l’azione per più di alcuni secondi. Se il percorso è meno sensibile al tempo, è possibile utilizzare un valore più lungo per dare più tempo al sistema chiamato per inviare una risposta valida.

I percorsi utilizzano anche un timeout globale. Consulta la [sezione successiva](#global_timeout).

### Timeout percorso globale {#global_timeout}

Oltre al [timeout](#timeout_and_error) utilizzato nelle attività di percorso, esiste anche un timeout di percorso globale che non viene visualizzato nell’interfaccia e non può essere modificato.

Questo timeout globale arresta il progresso dei singoli utenti nel percorso **91 giorni** dopo che sono entrati. Questo timeout è ridotto a **7 giorni** con il componente aggiuntivo Healthcare Shield. Ciò significa che la durata del percorso di un individuo non può superare i 91 giorni (o 7 giorni). Dopo questo periodo di timeout, i dati dell’individuo vengono eliminati. Gli individui che ancora scorrono nel percorso alla fine del periodo di timeout verranno interrotti e non verranno presi in considerazione nella generazione dei rapporti. Potresti quindi vedere più persone entrare nel percorso che uscire.

>[!NOTE]
>
>I percorsi non reagiscono direttamente alle richieste di rinuncia, accesso o cancellazione della privacy. Tuttavia, il timeout globale assicura che gli individui non rimangano più di 91 giorni in un percorso qualsiasi.

A causa del timeout di 91 percorsi, quando il rientro del percorso non è consentito, non possiamo assicurarci che il blocco del rientro funzioni per più di 91 giorni. Infatti, poiché si eliminano tutte le informazioni sulle persone che sono entrate nel percorso 91 giorni dopo il loro ingresso, non è possibile conoscere la persona che è entrata in precedenza, più di 91 giorni fa.

Un singolo utente può accedere a un’attività di attesa solo se nel percorso gli è rimasto abbastanza tempo per completare la durata dell’attesa prima del timeout di 91 percorsi. Consulta [questa pagina](../building-journeys/wait-activity.md).


#### Time-to-Live (TTL) e domande frequenti sulla conservazione dei dati {#timeout-faq}

**Per Percorsi unitari**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Cosa succederà al percorso pubblicato dopo il rollout dell’estensione TTL?</p>
    </td>
    <td>
      <p>I profili che entrano nel nuovo percorso avranno automaticamente un TTL di 91 giorni.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo che entra in un percorso pubblicato prima dell’avvio dell’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo avrà un TTL di 91 percorsi (7 giorni per HIPAA), in linea con l’ora di pubblicazione originaria.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo che è già entrato in un percorso quando viene avviata l’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo mantiene un TTL di 91 giorni (7 giorni per HIPAA), come da orario di pubblicazione originale del percorso.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo in una versione di percorso precedente che viene ripubblicata dopo l’avvio dell’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo manterrà un TTL di 91 giorni (7 giorni per HIPAA), allineato con l’orario di pubblicazione della versione originale del percorso.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un nuovo profilo che entra in una versione di percorso ripubblicata dopo il lancio dell’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo avrà un TTL di 91 giorni, corrispondente al TTL della versione di percorso appena ripubblicata.</p>
    </td>
  </tr>
</table>

**Per Percorsi di attivazione segmento**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Cosa succederà ai nuovi percorsi una tantum pubblicati dopo l’estensione TTL?</p>
    </td>
    <td>
      <p>I profili che entrano nel nuovo percorso avranno automaticamente un TTL di 91 giorni.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succederà ai nuovi percorsi ricorrenti senza rientro forzato pubblicati dopo l’estensione TTL?</p>
    </td>
    <td>
      <p>I profili che entrano nel nuovo percorso avranno automaticamente un TTL di 91 giorni.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succederà ai nuovi percorsi ricorrenti con rientro forzato pubblicati dopo l’estensione TTL?</p>
    </td>
    <td>
      <p>I profili che entrano nel nuovo percorso avranno un TTL uguale al periodo di ricorrenza. Ad esempio, se il percorso viene eseguito ogni giorno, il TTL sarà di 1 giorno.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo che entra in un percorso pubblicato prima dell’avvio dell’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo avrà un TTL di 91 giorni (7 giorni per HIPAA), in linea con il tempo di pubblicazione originale. Per i percorsi ricorrenti con rientro forzato, il TTL corrisponderà al periodo di ricorrenza.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo in esecuzione in un percorso quando viene avviata l’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo mantiene un TTL di 91 giorni (7 giorni per HIPAA), come da orario di pubblicazione originale del percorso. Per i percorsi ricorrenti con rientro forzato, il TTL corrisponderà al periodo di ricorrenza.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo in esecuzione in una versione di percorso precedente che viene ripubblicata dopo l’avvio dell’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo manterrà un TTL di 91 giorni (7 giorni per HIPPA), in linea con l’orario di pubblicazione della versione originale del percorso. Per i percorsi ricorrenti con rientro forzato, il TTL corrisponderà al periodo di ricorrenza.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un nuovo profilo che entra in una versione di percorso ripubblicata dopo il lancio dell’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo avrà un TTL di 91 giorni, corrispondente al TTL della versione di percorso appena ripubblicata. Per i percorsi ricorrenti con rientro forzato, il TTL corrisponderà al periodo di ricorrenza.</p>
    </td>
  </tr>
</table>

### Criteri di unione {#merge-policies}

Il percorso utilizza i criteri di unione per recuperare i dati del profilo da Adobe Experience Platform. A seconda del tipo di percorso, vengono utilizzati diversi criteri di unione:

* In percorsi di lettura del pubblico o di qualificazione del pubblico: viene utilizzato il criterio di unione del pubblico
* Nei percorsi attivati da eventi: viene utilizzato il criterio di unione predefinito

Il percorso rispetterà il criterio di unione utilizzato in tutto il percorso. Pertanto, se in un percorso vengono utilizzati più tipi di pubblico (ad esempio, nelle funzioni &quot;inAudience&quot;), creando incoerenze con il criterio di unione utilizzato dal percorso, viene generato un errore e la pubblicazione viene bloccata. Tuttavia, se nella personalizzazione dei messaggi viene utilizzato un pubblico incoerente, non viene generato un avviso, nonostante l’incoerenza. Per questo motivo, si consiglia vivamente di controllare il criterio di unione associato al pubblico quando questo è utilizzato nella personalizzazione dei messaggi.

Per ulteriori informazioni sui criteri di unione, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

## Duplicare un percorso {#duplicate-a-journey}

È possibile duplicare un percorso esistente da **Sfoglia** scheda. Tutti gli oggetti e le impostazioni vengono duplicati nella copia di percorso.

Per farlo, segui la procedura indicata di seguito:

1. Passare al percorso che si desidera copiare, fare clic sul pulsante **Altre azioni** (i tre punti accanto al nome del percorso).
1. Seleziona **Duplica**.

   ![Duplicare un percorso](assets/duplicate-jo.png)

1. Inserisci il nome del percorso e conferma. È inoltre possibile modificare il nome nella schermata delle proprietà del percorso. Per impostazione predefinita, il nome viene impostato come segue: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. Il nuovo percorso viene creato e disponibile nell&#39;elenco percorso.
