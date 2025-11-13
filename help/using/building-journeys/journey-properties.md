---
solution: Journey Optimizer
product: journey optimizer
title: Definire le proprietà del percorso
description: Scopri come impostare le proprietà del percorso con Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: percorso, configurazione, proprietà
exl-id: 6c21371c-6cbc-4d39-8fe6-39f1b8b13280
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '2771'
ht-degree: 15%

---

# Impostare le proprietà del percorso {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Proprietà del percorso"
>abstract="Questa sezione mostra le proprietà del percorso. Per impostazione predefinita, i parametri di sola lettura sono nascosti. Le impostazioni disponibili dipendono dallo stato del percorso, dalle autorizzazioni e dalla configurazione del prodotto."

## Accedere alle proprietà di un percorso {#access-properties}

Le proprietà di un percorso sono centralizzate nella barra a destra. Questa sezione viene visualizzata per impostazione predefinita durante la creazione di un nuovo percorso. Per i percorsi esistenti, fai clic sull’icona della matita accanto al nome del percorso per aprirlo.

Da questa sezione, definisci il nome del percorso, aggiungi una descrizione e imposta le proprietà globali del percorso.

Puoi eseguire le seguenti operazioni:

* Assegna tag unificati Adobe Experience Platform al tuo percorso, per classificarli facilmente e migliorare la ricerca dall’elenco delle campagne. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags)
* Seleziona le metriche di percorso. [Scopri come configurare e tenere traccia delle metriche di percorso](success-metrics.md)
* Gestisci [ingresso e rientro](#entrance). La gestione dell’entrata del profilo dipende dal tipo di percorso. I dettagli sono disponibili su [questa pagina](entry-management.md)
* Gestisci [accesso ai dati](#manage-access)
* Seleziona il percorso e il profilo [fusi orari](#timezone)
* Scegli [date di inizio e fine](#dates) personalizzate
* Definisci una [durata timeout](#timeout) nelle attività di percorso (solo per utenti amministratori)
* Monitora i conflitti e assegna priorità ai percorsi utilizzando [strumenti di gestione dei conflitti](#conflict)

![riquadro di configurazione delle proprietà del Percorso con impostazioni generali e opzioni avanzate](assets/new-journey-properties.png){width="80%"}{zoomable="yes"}

>[!NOTE]
>
>Per i percorsi live, questa schermata mostra solo la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso.

L&#39;opzione **Copia dettagli tecnici** consente di copiare informazioni tecniche sul percorso che il team di supporto può utilizzare per la risoluzione dei problemi. Sono state copiate le seguenti informazioni: `JourneyVersion UID`, `OrgID`, `orgName`, `sandboxName`, `lastDeployedBy`, `lastDeployedAt`.

Ulteriori informazioni sui campi tecnici relativi a un percorso per un determinato profilo e su come utilizzarli [in questa pagina](expression/journey-properties.md).

## Ingresso e rientro {#entrance}

La modalità di immissione profilo è definita a livello di percorso, nel riquadro di configurazione di destra. Le impostazioni sono descritte di seguito.

La gestione dell’entrata del profilo dipende dal tipo di percorso. Ulteriori informazioni sulla gestione dell&#39;ingresso e del rientro del profilo, in [questa pagina](entry-management.md). Ulteriori informazioni sui tassi di elaborazione del percorso e sul modo in cui i profili passano attraverso i percorsi in [questa sezione](entry-management.md#journey-processing-rate).

### Consentire il reingresso  {#allow-reentrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="Consentire il reingresso"
>abstract="Per impostazione predefinita, i nuovi percorsi consentono il reingresso. È possibile deselezionare l’opzione **Consenti reingresso**, ad esempio se si desidera offrire un omaggio una tantum quando una persona entra in un negozio."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Gestione dell’ingresso del profilo"

Per impostazione predefinita, i nuovi percorsi consentono il reingresso. È possibile deselezionare l&#39;opzione **Consenti rientro** per i percorsi &quot;one shot&quot;, ad esempio se si desidera offrire un regalo occasionale quando una persona entra in un negozio.

### Periodo di attesa per reingresso  {#reentrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="Periodo di attesa per reingresso"
>abstract="Imposta il tempo di attesa prima di consentire a un profilo di entrare nuovamente in un percorso unitario. Questo impedisce il reingresso degli utenti nel percorso per una durata selezionata. Durata massima: 90 giorni."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Gestione dell’ingresso del profilo"

Quando l&#39;opzione **Consenti rientro** è attivata, viene visualizzato il campo **Periodo di attesa rientro**. Questo campo ti consente di definire il tempo di attesa prima di consentire a un profilo di accedere nuovamente al percorso in percorsi unitari (a partire da un evento o da una qualificazione del pubblico). In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti. La durata massima è di 90 giorni.

## Gestisci accesso {#manage-access}

Puoi limitare l’accesso a un percorso in base alle etichette di accesso.

Per assegnare etichette di utilizzo dati personalizzate al percorso, fare clic sull&#39;icona **[!UICONTROL Gestisci etichette di accesso]** e selezionare una o più etichette.

[Ulteriori informazioni su OLAC (Object Level Access Control)](../administration/object-based-access.md)

## Fusi orari di percorso e profilo {#timezone}

Il fuso orario è definito a livello di percorso. Puoi immettere un fuso orario fisso o utilizzare i profili Adobe Experience Platform per definire il fuso orario del percorso. Se nel profilo Adobe Experience Platform è definito un fuso orario, questo può essere recuperato nel percorso.

[Ulteriori informazioni sulla gestione del fuso orario](../building-journeys/timezone-management.md)

## Date di inizio e di fine {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="Start date (Data di inizio)"
>abstract="Seleziona la data in cui i profili possono iniziare a entrare nel percorso. Se non è impostata alcuna data di inizio, per impostazione predefinita viene utilizzata la data di pubblicazione del percorso."

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="End date (Data di fine)"
>abstract="Imposta la data di fine del percorso. In questa data, i profili attivi usciranno automaticamente dal percorso e non saranno consentiti nuovi ingressi."

Per impostazione predefinita, i profili possono entrare nel percorso non appena viene pubblicato e possono rimanere fino al raggiungimento del [timeout percorso globale](#global_timeout). L&#39;unica eccezione è rappresentata dai percorsi di pubblico di lettura ricorrenti con **Forza il rientro alla ricorrenza** attivata, che terminano alla data di inizio dell&#39;occorrenza successiva.

Se necessario, puoi definire **Data inizio** e **Data fine** personalizzate. Questo consente ai profili di entrare nel percorso in una data specifica e di uscire automaticamente una volta raggiunta la data di fine.

## Timeout {#timeout}

### Timeout nelle attività del percorso {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_timeout"
>title="Timeout o errore"
>abstract="Specifica per quanto tempo il percorso deve tentare di eseguire un’azione o valutare una condizione prima di considerarla scaduta. I valori consigliati sono compresi tra 1 e 30 secondi."

Quando modifichi un’attività di azione o condizione, puoi definire un percorso alternativo in caso di errore o timeout. Se l&#39;elaborazione dell&#39;attività di interrogazione di un sistema di terze parti supera la durata di timeout definita nel campo **[!UICONTROL Timeout o errore]** delle proprietà del percorso, verrà scelto il secondo percorso per eseguire una potenziale azione di fallback.

I valori consigliati sono compresi tra 1 e 30 secondi.

È consigliabile definire un valore di **[!UICONTROL Timeout o errore]** molto breve se il percorso è sensibile all&#39;ora (ad esempio, per reagire alla posizione in tempo reale di una persona) perché non è possibile ritardare l&#39;azione per più di alcuni secondi. Se il percorso è meno sensibile al tempo, è possibile utilizzare un valore più lungo per dare più tempo al sistema chiamato per inviare una risposta valida.

I percorsi utilizzano anche un timeout globale, come descritto di seguito.

### Timeout percorso globale {#global_timeout}

Oltre al [timeout](#timeout_and_error) utilizzato nelle attività di percorso, viene applicato un timeout di percorso globale. Non viene visualizzato nell’interfaccia e non può essere modificato.

Questo timeout globale interrompe l&#39;avanzamento dei singoli utenti nel percorso **91 giorni** dopo l&#39;immissione. Ciò significa che la durata del percorso di un individuo non può superare i 91 giorni. Dopo questo periodo di timeout, i dati dell’individuo vengono eliminati. Gli individui che ancora scorrono nel percorso alla fine del periodo di timeout verranno interrotti e non verranno presi in considerazione nella generazione dei rapporti. Potresti quindi vedere più persone entrare nel percorso che uscire.

A causa del timeout di 91 percorsi, quando il rientro del percorso non è consentito, non possiamo assicurarci che il blocco del rientro funzioni per più di 91 giorni. Infatti, poiché si eliminano tutte le informazioni sulle persone che sono entrate nel percorso 91 giorni dopo il loro ingresso, non è possibile conoscere la persona che è entrata in precedenza, più di 91 giorni fa.

Un singolo utente può accedere a un’attività di attesa solo se nel percorso gli è rimasto abbastanza tempo per completare la durata dell’attesa prima del timeout di 91 percorsi. Consulta [questa pagina](../building-journeys/wait-activity.md).

#### Time-to-Live (TTL) e domande frequenti sulla conservazione dei dati {#timeout-faq}

A partire dalla versione di Adobe Journey Optimizer di giugno 2024, il timeout globale del percorso è stato spostato da 30 a 91 giorni. Gli impatti sono elencati nelle domande frequenti riportate di seguito:

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
      <p>Il profilo avrà un TTL di 30 giorni (7 giorni per HIPAA), in linea con l’ora in cui il percorso è stato pubblicato originariamente.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo che è già entrato in un percorso quando viene avviata l’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo mantiene un TTL di 30 giorni (7 giorni per HIPAA), come da orario di pubblicazione originale del percorso.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo in una versione di percorso precedente che viene ripubblicata dopo l’avvio dell’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo manterrà un TTL di 30 giorni (7 giorni per HIPAA), allineato con l’orario di pubblicazione della versione originale del percorso.</p>
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

**Per Percorsi Trigger Segmento**

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
      <p>Il profilo avrà un TTL di 30 giorni (7 giorni per HIPAA), in linea con il tempo di pubblicazione originale. Per i percorsi ricorrenti con rientro forzato, il TTL corrisponderà al periodo di ricorrenza.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo in esecuzione in un percorso quando viene avviata l’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo mantiene un TTL di 30 giorni (7 giorni per HIPAA), come da orario di pubblicazione originale del percorso. Per i percorsi ricorrenti con rientro forzato, il TTL corrisponderà al periodo di ricorrenza.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Cosa succede a un profilo in esecuzione in una versione di percorso precedente che viene ripubblicata dopo l’avvio dell’estensione TTL?</p>
    </td>
    <td>
      <p>Il profilo manterrà un TTL di 30 giorni (7 giorni per HIPPA), in linea con l’orario di pubblicazione della versione originale del percorso. Per i percorsi ricorrenti con rientro forzato, il TTL corrisponderà al periodo di ricorrenza.</p>
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

## Criteri di unione {#merge-policies}

Adobe Journey Optimizer utilizza i criteri di unione per recuperare i dati del profilo da Adobe Experience Platform. A seconda del tipo di percorso, vengono utilizzati diversi criteri di unione:

* In percorsi di lettura del pubblico o di qualificazione del pubblico: viene utilizzato il criterio di unione del pubblico
* Nei percorsi di eventi unitari: viene utilizzato il criterio di unione predefinito
* Nei percorsi di eventi aziendali: viene utilizzato il criterio di unione del pubblico di destinazione nella seguente attività Read audience

Adobe Journey Optimizer applica il criterio di unione utilizzato in tutto il percorso. Pertanto, se in un percorso vengono utilizzati più tipi di pubblico (ad esempio utilizzando le funzioni di [`inAudience`](functions/functioninaudience.md)), si creano incoerenze con il criterio di unione utilizzato dal percorso, viene generato un errore e la pubblicazione viene bloccata. Tuttavia, se nella personalizzazione dei messaggi viene utilizzato un pubblico incoerente, non viene generato un avviso, nonostante l’incoerenza. Per questo motivo, si consiglia vivamente di controllare il criterio di unione associato al pubblico quando questo è utilizzato nella personalizzazione dei messaggi.

Per ulteriori informazioni sui criteri di unione, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

>[!NOTE]
>
>Quando viene aggiornato un criterio di unione dei tipi di pubblico, qualsiasi percorso attivo che fa riferimento a tale pubblico deve essere ripubblicato (o duplicato). La modifica del criterio di unione crea in modo efficace un pubblico &quot;nuovo&quot; a cui il percorso in corso non può accedere, garantendo la coerenza dei dati.

## Criteri di uscita {#exit-criteria}

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Criteri di uscita"
>abstract="In questa sezione sono illustrate le opzioni relative ai criteri di uscita. Puoi creare una o più regole e uno o più filtri per i criteri di uscita del percorso."

### Criteri di uscita dal percorso {#exit-criteria-desc}

Aggiungendo i criteri di uscita, fai in modo che i profili escano dal percorso non appena si verifica un evento (ad esempio, un acquisto) oppure se sono idonei per un pubblico. Questo impedirà all’utente di ricevere ulteriori comunicazioni dal percorso.

Puoi rimuovere i profili da un percorso quando non soddisfano più lo scopo del percorso. Ciò può essere ottenuto mediante **criteri di uscita globali**, strettamente associati alla gestione degli obiettivi.

**Caso d&#39;uso di esempio**

Un addetto al marketing dispone di un percorso promozionale con una serie di comunicazioni. Ciascuna di queste comunicazioni ha lo scopo di spingere il cliente ad effettuare un acquisto. Appena effettuato l&#39;acquisto, il cliente non deve ricevere il resto dei messaggi della serie. Definendo un criterio di uscita, tutti i profili che hanno effettuato un acquisto vengono rimossi dal percorso.

#### Configurazione e utilizzo {#exit-criteria-config}

I criteri di uscita sono impostati a livello di percorso. Un percorso può avere più criteri di uscita. Se hai impostato più criteri di uscita, la valutazione viene eseguita dall&#39;alto verso il basso con una logica `OR`. Pertanto, se si dispone del criterio di uscita A e del criterio di uscita B, verrà valutato come A **OR** B. I criteri vengono valutati in ogni fase del percorso.

Per **creare** un criterio di uscita, eseguire la procedura seguente:

1. Apri il percorso.

1. Fai clic sull&#39;icona ![Mostra criteri di uscita](assets/do-not-localize/Smock_UserCheckedOut_18_N.svg) **[!UICONTROL Mostra criteri di uscita]** nella sezione superiore destra dell&#39;area di lavoro del percorso.

1. Selezionare **[!UICONTROL Aggiungi criteri di uscita]**.

1. Immetti un **Etichetta** e seleziona se i criteri di uscita sono basati su un **Evento** o un **Pubblico**.

   * Per i criteri di uscita basati su un evento, come ad esempio il download di un’app o l’aggiunta di un prodotto a un carrello, scegli solo un evento unitario.
   * Per i criteri di uscita basati su un pubblico, ad esempio un pubblico che controlla se un cliente ha acquistato nelle ultime 24 ore, seleziona un pubblico. Nota: l’utilizzo dei criteri di uscita da un pubblico può richiedere fino a 10 minuti per essere efficace.

È possibile aggiungere più criteri di uscita.

![Il pannello dei criteri di uscita mostra le condizioni del pubblico per la cessazione del percorso](assets/exitcriteria-sample.png){width="40%" align="left"}


### Criteri di uscita basati su attributi di profilo {#profile-exit-criteria}

I criteri di uscita basati su attributi di profilo offrono un maggiore controllo sui percorsi in pausa, consentendo di definire regole che rimuovono automaticamente profili specifici prima che il percorso riprenda. È possibile impostare le condizioni di uscita in base agli attributi del profilo, ad esempio posizione, stato o preferenze, per garantire che solo i profili rilevanti continuino a essere presenti nel percorso dopo la ripresa.

Ad esempio, puoi [sospendere un percorso](journey-pause.md), aggiungere una condizione di uscita per rimuovere tutti i profili che si trovano in Francia e riprendere il percorso sapendo che tali profili saranno esclusi al passaggio successivo dell&#39;azione. Questa logica si applica sia ai profili già presenti nel percorso, sia a qualsiasi nuovo profilo idoneo dopo la ripresa del percorso.

Questa funzione si affianca alla funzionalità Pausa/Riprendi, che consente di gestire i percorsi in modo più sicuro e flessibile. Riduce al minimo gli interventi manuali, riduce i rischi di invio di comunicazioni irrilevanti o non conformi e mantiene la logica di percorso allineata ai requisiti aziendali correnti.

Consulta questa sezione per scoprire come [utilizzare i criteri di uscita degli attributi di profilo nei percorsi in pausa](journey-pause.md#journey-pause-sample).

### Guardrail e limitazioni {#exit-criteria-guardrails}

Le seguenti protezioni e limitazioni si applicano alla funzionalità [Criteri di uscita Percorsi](#exit-criteria-desc):

* I criteri di uscita sono definiti solo nello stato di bozza
* Coerenza dello spazio dei nomi del percorso tra eventi e criteri di uscita basati su eventi

Le seguenti protezioni si applicano quando si utilizza la funzionalità [Criteri di uscita basati su attributi di profilo](#profile-exit-criteria):

* **I criteri di uscita si applicano a livello di azione**\
  I criteri di uscita per &quot;Attributo profilo&quot; vengono valutati solo nei passaggi dell’azione. A differenza di altri tipi di criteri di uscita, non si applicano a livello globale in tutto il percorso.\
  Se riprendi un percorso e alcuni profili soddisfano la condizione di uscita, questi profili verranno esclusi nel nodo dell’azione successivo.\
  Anche i nuovi profili che entrano nel percorso dopo la ripresa verranno valutati ed esclusi al loro primo nodo di azione, se soddisfano la condizione.

* **Una regola di uscita basata su profilo al percorso**\
  Puoi definire un solo criterio di uscita &quot;Attributo profilo&quot; al percorso. Questa limitazione contribuisce a mantenere la chiarezza ed evita conflitti nella logica di percorso.

* **Disponibile solo nei percorsi in pausa**\
  Puoi aggiungere o modificare i criteri di uscita &quot;Attributo profilo&quot; solo quando il percorso viene messo in pausa.

   * In un **percorso 2D**, l&#39;opzione *Attributo profilo* è disabilitata (sola lettura), mentre le opzioni *Evento* e *Pubblico* rimangono attive.
   * In un **percorso sospeso**, l&#39;opzione *Attributo profilo* diventa modificabile e le opzioni *Evento* e *Pubblico* diventano di sola lettura.

## Pianificazione percorso {#schedule}

La sezione **[!UICONTROL Pianifica]** è disponibile solo quando un&#39;attività **[!UICONTROL Read Audience]** è stata eliminata nell&#39;area di lavoro. Consente di definire una data/ora e una frequenza specifiche per l&#39;esecuzione del percorso. [Scopri come pianificare un percorso Read-audience](../building-journeys/read-audience.md)

## Gestione dei conflitti {#conflict}

La sezione **[!UICONTROL Gestione dei conflitti]** nelle proprietà del percorso ti consente di monitorare i conflitti e assegnare un ordine di priorità ai percorsi. Puoi eseguire le seguenti operazioni:

* Applica un **set di regole** per escludere questo percorso da parte del pubblico in base alle regole di limitazione. [Scopri come utilizzare i set di regole](../conflict-prioritization/rule-sets.md)

* Assegna al percorso un **punteggio di priorità** compreso tra 0 e 100. Un numero più alto indica una priorità più alta. Il valore di priorità qui inserito viene ereditato da tutte le azioni in entrata (come in-app) contenute in questo percorso. [scopri come utilizzare i punteggi di priorità](../conflict-prioritization/priority-scores.md)

  Nelle situazioni in cui la stessa configurazione del canale in entrata viene utilizzata in altre campagne o percorsi, al destinatario viene mostrata l’azione in entrata con il punteggio di priorità più alto. Se più percorsi o campagne hanno lo stesso punteggio, viene scelto l’elemento modificato più di recente.

* **Visualizza i conflitti** con altri percorsi, campagne o configurazioni di canale. Se desideri identificare la sovrapposizione su pubblico, data di inizio e fine, configurazione del canale, canale o set di regole, puoi visualizzare i potenziali conflitti qui. [Scopri come identificare potenziali conflitti nel percorso](../conflict-prioritization/conflicts.md)
