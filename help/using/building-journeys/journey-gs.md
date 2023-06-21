---
solution: Journey Optimizer
product: journey optimizer
title: Creare il primo percorso
description: Passaggi chiave per creare il primo percorso con Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: percorso, primo, inizio, avvio rapido, segmento, evento, azione
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: b0b65ad119b6939a6d65d6f05edc67b2f2b22a31
workflow-type: tm+mt
source-wordcount: '1549'
ht-degree: 26%

---

# Creare il primo percorso{#jo-quick-start}

## Prerequisiti{#start-prerequisites}

Per inviare messaggi con i percorsi, sono necessarie le seguenti configurazioni:

1. **Configurare un evento**: se desideri attivare i percorsi in modo unitario quando viene ricevuto un evento, devi configurare un evento. È possibile definire le informazioni previste e le modalità di elaborazione. e viene eseguita da un **utente tecnico**. [Ulteriori informazioni](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Creare un segmento**: il percorso può anche ascoltare i segmenti di Adobe Experience Platform per inviare messaggi in batch a un set specifico di profili. A questo scopo, devi creare dei segmenti. [Ulteriori informazioni](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **Configurare l’origine dati**: è possibile definire una connessione a un sistema per il recupero di informazioni aggiuntive che verranno utilizzate nei percorsi, ad esempio nelle condizioni specificate. Al momento del provisioning, viene configurata anche un’origine dati integrata in Adobe Experience Platform. Se sfrutti solo i dati degli eventi del tuo percorso, questo passaggio non è necessario e viene eseguita da un **utente tecnico**. [Maggiori informazioni](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurare un’azione**: se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni [sezione](../action/action.md). e viene eseguita da un **utente tecnico**. Se utilizzi le funzionalità per messaggi integrate di Journey Optimizer, devi solo aggiungere un’azione di canale al percorso e progettare il contenuto.

   ![](assets/custom2.png)

## Percorsi di accesso {#journey-access}

Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Percorsi]**. Sono disponibili due schede:

**Panoramica**: in questa scheda viene visualizzato un dashboard con le metriche chiave correlate ai percorsi:

* **Profili elaborati**: numero totale di profili elaborati nelle ultime 24 ore
* **Percorsi live**: numero totale di percorsi live con traffico nelle ultime 24 ore. I percorsi live includono **Percorsi unitari** (basato su eventi) e **Percorsi batch** (leggi segmento).
* **Percentuale di errori**: rapporto tra tutti i profili con errore e il numero totale di profili immessi nelle ultime 24 ore.
* **Percentuale di eliminazione**: rapporto tra tutti i profili scartati e il numero totale di profili immessi nelle ultime 24 ore. Un profilo scartato rappresenta un utente non idoneo per l’accesso al percorso, ad esempio a causa di uno spazio dei nomi errato o di regole di rientro.

>[!NOTE]
>
>Questa dashboard tiene conto dei percorsi con traffico nelle ultime 24 ore. Vengono visualizzati solo i percorsi a cui hai accesso.

![](assets/journeys-dashboard.png)

**Sfoglia**: in questa scheda viene visualizzato l’elenco dei percorsi esistenti. Puoi cercare percorsi, utilizzare filtri ed eseguire azioni di base su ciascun elemento. Ad esempio, è possibile duplicare o eliminare un elemento. Per ulteriori informazioni, consulta [questa sezione](../start/user-interface.md#filter-lists).

![](assets/journeys-browse.png)

Nell’elenco del percorsi, puoi filtrare i percorsi in base al loro stato, tipo e versione mediante i **[!UICONTROL filtri Stato e Versione]**. Il tipo può essere: **[!UICONTROL Evento unitario]**, **[!UICONTROL Qualificazione del segmento]**, **[!UICONTROL Leggi segmento]**, **[!UICONTROL Evento di business]** o **[!UICONTROL Burst]**.

Puoi scegliere di visualizzare solo i percorsi che utilizzano un evento, un gruppo di campi o un’azione particolare con **[!UICONTROL Filtri di attività]** e **[!UICONTROL Filtri di dati]**. Inoltre, il **[!UICONTROL Filtri di pubblicazione]** consente di selezionare una data di pubblicazione o un utente. Ad esempio, puoi scegliere di visualizzare le versioni più recenti dei percorsi live pubblicati ieri. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md).

![](assets/filter-journeys.png)

Utilizza le colonne **[!UICONTROL Ultimo aggiornamento]** e **[!UICONTROL Ultimo aggiornamento di]** per verificare quando è avvenuto l’ultimo aggiornamento dei percorsi e chi l’ha salvato.

Nei riquadri di configurazione dell’evento, dell’origine dati e dell’azione, il campo **[!UICONTROL Usato in]** mostra il numero di percorsi che utilizzano quel particolare evento, gruppo di campi o azione. Per visualizzare l’elenco dei percorsi corrispondenti, puoi fare clic sul pulsante **[!UICONTROL Visualizza percorsi]**.

![](assets/journey3bis.png)

## Creare il percorso{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Creare il percorso"
>abstract="In questa schermata viene visualizzato l’elenco dei percorsi esistenti. Apri un percorso o fai clic su “Crea percorso” e combina le diverse attività di evento, orchestrazione e azione per creare scenari multicanale con più passaggi."

Questo passaggio viene eseguito da **utente aziendale**. Qui è dove si creano i percorsi. Combina le diverse attività relative a un evento, un percorso e un’azione in modo da creare scenari tra canali con più passaggi.

Di seguito sono riportati i passaggi principali per l’invio di messaggi tramite percorsi:

1. Dalla sezione **Sfoglia** , fare clic su **[!UICONTROL Crea Percorso]** per creare un nuovo percorso.

1. Modifica le proprietà del percorso nel riquadro di configurazione visualizzato sul lato destro. Ulteriori informazioni [sezione](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Per iniziare, trascina e rilascia un evento o una **Leggi segmento** dalla palette all’area di lavoro. Per ulteriori informazioni sulla progettazione del percorso, fare riferimento a [questa sezione](using-the-journey-designer.md).

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

Fai clic sull’icona della matita, in alto a destra per accedere alle proprietà del percorso.

Puoi modificare il nome del percorso, aggiungere una descrizione, consentire il rientro, scegliere le date di inizio e di fine e, in qualità di utente amministratore, definire un’ **[!UICONTROL Timeout ed errore]** durata. Puoi anche assegnare tag unificati Adobe Experience Platform al tuo percorso. Questo consente di classificarle facilmente e migliorare la ricerca dall’elenco delle campagne. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags)

Per i percorsi live, questa schermata mostra la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso.

Il **Copia dettagli tecnici** consente di copiare le informazioni tecniche sul percorso che il team di supporto può utilizzare per la risoluzione dei problemi. Vengono copiate le seguenti informazioni: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Ingresso{#entrance}

Per impostazione predefinita, i nuovi percorsi consentono il rientro. È possibile deselezionare **Consenti rientro** opzione per percorsi &quot;one shot&quot;, ad esempio se si desidera offrire un regalo una tantum quando una persona entra in un negozio.

Quando **Consenti rientro** è attivata, la **Periodo di attesa per rientro** viene visualizzato. Questo campo ti consente di definire il tempo di attesa prima di consentire a un profilo di accedere nuovamente al percorso in percorsi unitari (a partire da un evento o una qualifica di segmento). In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti.

Ulteriori informazioni sulla gestione dell’ingresso del profilo, in [questa sezione](entry-management.md).

### Gestisci accesso {#access}

Per assegnare al percorso etichette di utilizzo dei dati personalizzate o di base, fai clic su **[!UICONTROL Gestisci accesso]** pulsante. [Ulteriori informazioni su OLE (Object Level Access Control)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### Fuso orario e fuso orario del profilo {#timezone}

Fuso orario definito a livello di percorso.

Puoi immettere un fuso orario fisso o utilizzare i profili Adobe Experience Platform per definire il fuso orario del percorso.

Se nel profilo Adobe Experience Platform è definito un fuso orario, questo può essere recuperato nel percorso.

Per ulteriori informazioni sulla gestione del fuso orario, consulta [questa pagina](../building-journeys/timezone-management.md).

### Date di inizio e fine {#dates}

È possibile definire un **Data di inizio**. Se non ne hai specificato uno, verrà definito automaticamente al momento della pubblicazione.

Puoi anche aggiungere una **Data di fine**. Questo consente ai profili di uscire automaticamente quando viene raggiunta la data. Se non specifichi una data di fine, i profili possono rimanere fino al timeout predefinito del percorso (in genere 30 giorni, 7 giorni con l’offerta aggiuntiva Healthcare Shield). L’unica eccezione è rappresentata dai percorsi di segmenti di lettura ricorrenti con **Forza rientro in caso di ricorrenza** attivato, che termina alla data di inizio dell’occorrenza successiva.

### Timeout ed errore nelle attività del percorso {#timeout_and_error}

Quando modifichi un’attività di azione o condizione, puoi specificare un percorso alternativo in caso di errore o timeout. Se l’elaborazione dell’attività, che comporta l’esecuzione di query su un sistema di terze parti, supera la durata specificata nelle proprietà del percorso per il timeout e la gestione degli errori (**[!UICONTROL Timeout ed errore]** ), verrà selezionato il secondo percorso per eseguire un’azione di fallback, se necessario.

I valori autorizzati sono compresi tra 1 e 30 secondi.

È consigliabile definire un valore molto breve **[!UICONTROL Timeout ed errore]** valore se il percorso è sensibile all’ora (ad esempio: reagire alla posizione in tempo reale di una persona) perché non è possibile ritardare l’azione per più di alcuni secondi. Se il percorso è meno sensibile al tempo, è possibile utilizzare un valore più lungo per dare più tempo al sistema chiamato per inviare una risposta valida.

I percorsi utilizzano anche un timeout globale. Consulta la [sezione successiva](#global_timeout).

### Timeout percorso globale {#global_timeout}

Oltre al [timeout](#timeout_and_error) utilizzato nelle attività di percorso, esiste anche un timeout di percorso globale che non viene visualizzato nell’interfaccia e non può essere modificato. Questo timeout interromperà l’avanzamento delle persone nel percorso 30 giorni dopo l’ingresso. Ciò significa che la durata del percorso di un individuo non può superare i 30 giorni. Dopo il periodo di timeout di 30 giorni, i dati dell’individuo vengono eliminati. Gli individui che ancora scorrono nel percorso alla fine del periodo di timeout verranno interrotti e verranno presi in considerazione come errori nella generazione dei rapporti.

>[!NOTE]
>
>I percorsi non reagiscono direttamente alle richieste di rinuncia, accesso o cancellazione della privacy. Tuttavia, il timeout globale assicura che gli individui non rimangano mai più di 30 giorni in qualsiasi percorso.

A causa del timeout di 30 percorsi, quando il rientro del percorso non è consentito, non possiamo assicurarci che il blocco del rientro funzioni per più di 30 giorni. Infatti, poiché si eliminano tutte le informazioni sulle persone che sono entrate nel percorso 30 giorni dopo il loro ingresso, non è possibile conoscere la persona che è entrata in precedenza, più di 30 giorni fa.

