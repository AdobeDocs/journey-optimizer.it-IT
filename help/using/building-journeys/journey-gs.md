---
solution: Journey Optimizer
product: journey optimizer
title: Creare il primo percorso
description: Passaggi chiave per creare il primo percorso con Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 978751263ba2ed21e35e41e767f1e31ddbe59d53
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 0%

---

# Creare il primo percorso{#jo-quick-start}

## Prerequisiti{#start-prerequisites}

Per inviare messaggi con i percorsi, sono necessarie le seguenti configurazioni:

1. **Configurare un evento**: se desideri attivare i tuoi percorsi in modo unitario quando viene ricevuto un evento, devi configurare un evento. Puoi definire le informazioni previste e come elaborarle. Questo passaggio viene eseguito da un **utente tecnico**. [Leggi tutto](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Creare un segmento**: il percorso può anche ascoltare i segmenti di Adobe Experience Platform per inviare messaggi in batch a un set specifico di profili. A questo scopo, devi creare dei segmenti. [Leggi tutto](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **Configurare l’origine dati**: puoi definire una connessione a un sistema per recuperare informazioni aggiuntive che verranno utilizzate nei tuoi percorsi, ad esempio nelle tue condizioni. Al momento del provisioning viene configurata anche un’origine dati integrata di Adobe Experience Platform. Questo passaggio non è necessario se sfrutti solo i dati degli eventi nel percorso. Questo passaggio viene eseguito da un **utente tecnico**. [Leggi tutto](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurare un’azione**: Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni [sezione](../action/action.md). Questo passaggio viene eseguito da un **utente tecnico**. Se utilizzi le funzionalità integrate dei messaggi di Journey Optimizer, devi solo aggiungere un’azione del canale al percorso e progettare il contenuto.

   ![](assets/custom2.png)

## Creare un percorso{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Creare un percorso"
>abstract="In questa schermata viene visualizzato l’elenco dei percorsi esistenti. Apri un percorso o fai clic su &quot;Crea percorso&quot; e combina le diverse attività di evento, orchestrazione e azione per creare scenari tra canali con più passaggi."

Questo passaggio viene eseguito da **utente aziendale**. Qui puoi creare i tuoi percorsi. Combina le diverse attività di evento, orchestrazione e azione per creare scenari multicanale con più passaggi.

Di seguito sono riportati i passaggi principali per l’invio dei messaggi attraverso i percorsi:

1. Nella sezione del menu JOURNEY MANAGEMENT fare clic su **[!UICONTROL Journeys]**. Viene visualizzato l’elenco dei percorsi.

   ![](assets/interface-journeys.png)

1. Fai clic su **[!UICONTROL Create Journey]** per creare un nuovo percorso.

1. Modifica le proprietà del percorso nel riquadro di configurazione visualizzato sul lato destro. Ulteriori informazioni [sezione](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Inizia trascinando un evento o un **Leggi segmento** attività dalla palette all’area di lavoro. Per ulteriori informazioni sulla progettazione del percorso, consulta [questa sezione](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Trascina e rilascia i passaggi successivi che verranno seguiti dall’utente. Ad esempio, puoi aggiungere una condizione seguita da un’azione canale. Per ulteriori informazioni sulle attività, consulta [questa sezione](using-the-journey-designer.md).

1. Verifica il percorso utilizzando i profili di test. Ulteriori informazioni [sezione](testing-the-journey.md)

1. Pubblica il percorso per attivarlo. Ulteriori informazioni [sezione](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitora il percorso utilizzando gli strumenti di reporting dedicati per misurare l’efficacia del percorso. Ulteriori informazioni [sezione](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Definire le proprietà del percorso {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Proprietà del percorso"
>abstract="Questa sezione mostra le proprietà del percorso. Per impostazione predefinita, i parametri di sola lettura sono nascosti. Le impostazioni disponibili dipendono dallo stato del percorso, dalle autorizzazioni e dalla configurazione del prodotto."

Fai clic sull’icona a forma di matita, in alto a destra, per accedere alle proprietà del percorso.

Puoi modificare il nome del percorso, aggiungere una descrizione, consentire il rientro, scegliere le date di inizio e di fine e, come utente amministratore, definire un **[!UICONTROL Timeout and error]** durata.

Per i percorsi live, questa schermata mostra la data di pubblicazione e il nome dell’utente che ha pubblicato il percorso.

La **Copia dettagli tecnici** consente di copiare le informazioni tecniche sul percorso che il team di supporto può utilizzare per la risoluzione dei problemi. Vengono copiate le seguenti informazioni: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Ingresso{#entrance}

Per impostazione predefinita, i nuovi percorsi consentono il rientro. Puoi deselezionare l’opzione per i percorsi &quot;una tantum&quot;, ad esempio se desideri offrire un regalo una tantum quando una persona entra in un negozio.

Ulteriori informazioni sulla gestione dell’ingresso del profilo, in [questa sezione](entry-management.md).

### Timeout ed errore nelle attività del percorso {#timeout_and_error}

Quando modifichi un’attività di azione o condizione, puoi definire un percorso alternativo in caso di errore o timeout. Se l’elaborazione dell’attività che esegue l’interrogazione a un sistema di terze parti supera la durata di timeout definita nelle proprietà del percorso (**[!UICONTROL Timeout and  error]** (campo ), verrà scelto il secondo percorso per eseguire una potenziale azione di fallback.

I valori autorizzati sono compresi tra 1 e 30 secondi.

È consigliabile definire un valore molto breve **[!UICONTROL Timeout and error]** se il percorso è sensibile all’ora (ad esempio: reagire alla posizione in tempo reale di una persona) perché non è possibile ritardare l&#39;azione per più di pochi secondi. Se il percorso è meno sensibile al tempo, puoi utilizzare un valore più lungo per dare più tempo al sistema chiamato per inviare una risposta valida.

I percorsi utilizzano anche un timeout globale. Consulta la sezione [sezione successiva](#global_timeout).

### Timeout del percorso globale {#global_timeout}

Oltre al [timeout](#timeout_and_error) utilizzato nelle attività di percorso, esiste anche un timeout del percorso globale che non viene visualizzato nell’interfaccia e che non può essere modificato. Questo timeout interrompe il progresso delle persone nel percorso 30 giorni dopo l’accesso. Questo significa che il viaggio di un individuo non può durare più di 30 giorni. Dopo il periodo di timeout di 30 giorni, i dati del singolo utente vengono eliminati. Le persone che continuano a fluire nel percorso alla fine del periodo di timeout verranno arrestate e verranno prese in considerazione come errori nel reporting.

>[!NOTE]
>
>I percorsi non rispondono direttamente alle richieste di rinuncia alla privacy, accesso o cancellazione. Tuttavia, il timeout globale assicura che gli individui non rimangano mai più di 30 giorni in un qualsiasi percorso.

A causa del timeout del percorso di 30 giorni, quando il rientro del percorso non è consentito, non possiamo assicurarci che il blocco del rientro funzioni per più di 30 giorni. Infatti, poiché rimuoviamo tutte le informazioni sulle persone che sono entrate nel viaggio 30 giorni dopo il loro ingresso, non possiamo sapere che la persona è entrata in precedenza, più di 30 giorni fa.

### Fuso orario e fuso orario del profilo {#timezone}

Il fuso orario è definito a livello di percorso.

Puoi immettere un fuso orario fisso oppure utilizzare i profili Adobe Experience Platform per definire il fuso orario del percorso.

Se un fuso orario è definito nel profilo di Adobe Experience Platform, può essere recuperato nel percorso.

Per ulteriori informazioni sulla gestione del fuso orario, vedi [questa pagina](../building-journeys/timezone-management.md).

### Gestisci accesso {#access}

Per assegnare etichette di utilizzo dati personalizzate o di base al percorso, fai clic sul pulsante **[!UICONTROL Manage access]** pulsante . [Ulteriori informazioni sul controllo dell&#39;accesso a livello di oggetto (OLA)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)
