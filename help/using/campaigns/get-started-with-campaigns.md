---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle campagne
description: Ulteriori informazioni sulle campagne in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: campagna, come fare, inizio, optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Introduzione alle campagne {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Pianificazione della campagna"
>abstract="Per impostazione predefinita, le campagne iniziano al momento dell’attivazione manuale e terminano immediatamente dopo l’invio del messaggio. Puoi impostare una data e un’ora specifiche per l’invio del messaggio. Inoltre, puoi specificare una data di fine per le campagne con azioni ricorrenti. Nei trigger di Azione, puoi anche configurare la frequenza di invio del messaggio in base alle tue preferenze."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Inizio della campagna"
>abstract="Specifica la data e l’ora in cui il messaggio deve essere inviato."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fine della campagna"
>abstract="Specifica quando interrompere l’esecuzione di una campagna ricorrente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Trigger delle azioni della campagna"
>abstract="Definisci la frequenza con cui deve essere inviato il messaggio della campagna."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Controllo della frequenza"
>abstract="Imposta il controllo della frequenza della tua campagna specificando i limiti di frequenza desiderati. Questa funzione è particolarmente utile per prevenire il sovraccarico sui sistemi a valle, come le pagine di destinazione o le piattaforme di assistenza clienti."

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Creare le campagne"
>abstract="Utilizza **Adobe Journey Optimizer** per distribuire contenuti una tantum a un pubblico specifico utilizzando vari canali. Quando si utilizzano i percorsi, le azioni vengono eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagne"
>abstract="Crea campagne per distribuire contenuti una tantum a un pubblico specifico su vari canali. Prima di creare una campagna, accertati di avere una configurazione dei canali e un pubblico di Adobe Experience Platform pronti per l’uso."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo di campagna"
>abstract="Seleziona il tipo di campagna. I canali disponibili variano a seconda del tipo selezionato. <br>**Campagne pianificate** (campagne con azioni): ideali per comunicazioni in batch semplici e una tantum da pianificare in modo che vengano eseguite in un momento specifico.<br>**Campagne attivate da API**: vengono attivate tramite una chiamata API e abilitano la messaggistica automatizzata basata su eventi direttamente da sistemi esterni.<br>**Campagne orchestrate**: forniscono un’area di lavoro visiva e basata su trascinamento per progettare e automatizzare flussi di lavoro di marketing complessi e in più passaggi, dalla segmentazione del pubblico alla consegna personalizzata dei messaggi su tutti i canali."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="Campagne"
>abstract="Crea il flusso di segmentazione, definisci i messaggi cross-channel e pianifica le campagne. Canali supportati: e-mail, SMS, notifiche push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Campagne"
>abstract="Consegne in uscita singole o ricorrenti o azioni in entrata continue."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Campagne"
>abstract="Consegna di azioni transazionali in uscita singole o ricorrenti."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Campagne"
>abstract="Consegna di comunicazioni di marketing personalizzate a un pubblico target. Canali supportati: e-mail, SMS, notifiche push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Campagne"
>abstract="Consegna di comunicazioni transazionali a singoli profili o a set di profili. Canali supportati: e-mail, SMS, notifiche push."

Adobe Journey Optimizer consente di fornire contenuti una tantum mirati a tipi di pubblico specifici su più canali. Utilizzando le campagne, puoi eseguire contemporaneamente azioni di marketing coordinate, raggiungendo il pubblico con il messaggio giusto al momento giusto.

Questa guida fornisce una roadmap chiara che ti aiuta a comprendere le nozioni di base della campagna, a scegliere il tipo di campagna adatto al tuo caso d’uso e a progettare con sicurezza campagne in grado di fornire esperienze cliente significative.

## Che cosa sono le campagne?

Le **campagne** sono azioni di marketing coordinate per la consegna di contenuti a un pubblico specifico su uno o più canali. A differenza dei percorsi in cui le azioni vengono eseguite in sequenza, le campagne eseguono le azioni contemporaneamente, immediatamente o secondo una pianificazione definita.

Utilizza [!DNL Journey Optimizer] campagne per:

* consegnare **contenuti una tantum o ricorrenti** ai segmenti di pubblico mirati;
* eseguire **comunicazioni multicanale coordinate** tramite e-mail, push, SMS, in-app, web e altro ancora;
* attivare **risposte automatizzate** tramite chiamate API per messaggi in tempo reale basati su eventi;
* progettare **flussi di lavoro di marketing complessi** con strumenti di orchestrazione visiva.

![](assets/gs-campaigns.png)

➡️ **Vuoi iniziare subito?** [Crea la prima campagna](create-campaign.md) in pochi minuti.

## Scegliere il tipo di campagna {#campaign-types}

**Prima di iniziare a creare**, è importante comprendere quale tipo di campagna si adatta al tuo caso d’uso. Adobe Journey Optimizer supporta tre tipi di campagne, ciascuno progettato per diversi scenari e meccanismi di attivazione:

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Campagne orchestrate]

**Quando utilizzarle:** flussi di lavoro di marketing complessi e con più passaggi

Le **campagne orchestrate** forniscono un’area di lavoro visiva e con trascinamento per progettare e automatizzare flussi di lavoro di marketing sofisticati. Dalla segmentazione del pubblico alla consegna personalizzata dei messaggi attraverso i canali, tutto avviene in un ambiente intuitivo costruito per velocità e controllo.

**Ideali per:** programmi di coinvolgimento della clientela in più passaggi, strategie di segmentazione e targeting complesse, orchestrazione di campagne cross-channel, marketing su larga scala avviato dal brand e automazione dei flussi di lavoro avanzata con più punti decisionali.

➡️ [Informazioni sulle campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md)

>[!TAB Campagne con azioni (pianificate)]

**Quando utilizzarle:** comunicazioni in batch semplici e pianificate

Le **campagne con azioni** (note anche come campagne pianificate) sono ideali per comunicazioni in batch semplici, una tantum o ricorrenti che vengono eseguite in un tempo specifico.

**Due categorie:**

* **Marketing**: offerte promozionali, campagne di coinvolgimento, annunci, notifiche legali o aggiornamenti dei criteri. Richiede il consenso dei destinatari.
* **Transazionale**: interruzioni, emergenze, annullamenti. Non richiede il consenso.

**Ideale per:** newsletter mensili a segmenti di clienti, annunci promozionali con scadenza precisa, campagne di marketing stagionali, comunicazioni sul lancio di prodotti e notifiche di interruzione del servizio.

➡️ [Informazioni sulle campagne con azioni](create-campaign.md)

>[!TAB Campagne attivate da API]

**Quando utilizzarle:** messaggistica basata su eventi in tempo reale con sistemi esterni

**Campagne attivate da API**: vengono attivate tramite chiamate API e abilitano la messaggistica automatizzata direttamente da sistemi esterni. Queste campagne supportano la personalizzazione utilizzando sia gli attributi del profilo che i dati contestuali in tempo reale dal payload API.

**Due categorie:**

* **Marketing**: comunicazioni di marketing personalizzate per tipi di pubblico mirati
* **Transazionale**: messaggi successivi a singole azioni (reimpostazione password, acquisti carrello, ecc.)

**Ideale per:** conferme di reimpostazione password, recupero dell’abbandono del carrello, conferme di ordini e aggiornamenti di spedizione, notifiche di attività dell’account e consigli personalizzati in tempo reale.

➡️ [Informazioni sulle campagne attivate da API](api-triggered-campaigns.md)

>[!ENDTABS]

>[!NOTE]
>
>Quale tipo scegliere? Inizia a usare le **campagne con azioni** per le comunicazioni in batch pianificate o le **campagne attivate da API** per la messaggistica in tempo reale. Queste campagne riguardano i casi d’uso più comuni.

## Prerequisiti {#prerequisites}

Prima di utilizzare le campagne, assicurati di aver rivisto quanto segue:

* **Tipi di pubblico**: i tipi di pubblico devono essere disponibili in Adobe Experience Platform prima della creazione delle campagne. [Introduzione ai tipi di pubblico →](../audience/about-audiences.md)

* **Configurazioni dei canali**: le configurazioni dei canali (predefiniti) devono essere create e disponibili per i canali che desideri utilizzare. [Imposta le configurazioni dei canali →](../configuration/channel-surfaces.md)

* **Autorizzazioni**: sono necessarie le autorizzazioni appropriate in base al tipo di campagna. Se non riesci ad accedere alle funzionalità della campagna, contatta l’amministratore. [Informazioni sui ruoli incorporati →](../administration/ootb-product-profiles.md)

  +++Elenco delle autorizzazioni delle campagne

  | Tipo di campagna | Autorizzazioni |
  |-------------|---------------|
  | **Campagne attivate da azioni** e **Campagne attivate da API** | Amministratore campagna<br>Approvatore campagna<br>Responsabile campagna<br>Visualizzatore campagna |
  | **Campagne orchestrate** | Amministratore campagna orchestrata<br>Approvatore campagna orchestrata<br>Responsabile campagna orchestrata<br>Visualizzatore campagna orchestrata |

  +++

  +++Come assegnare le autorizzazioni per la campagna

   1. Passa alla scheda **[!UICONTROL Ruoli]** nel prodotto [!DNL Permissions] e seleziona uno dei **[!UICONTROL Ruoli]** correlati alla campagna incorporata.

   1. Dalla scheda **[!UICONTROL Utenti]**, fai clic su **[!UICONTROL Aggiungi utente]**.

   1. Digita il nome o l’indirizzo e-mail dell’utente o selezionalo dall’elenco e fai clic su **[!UICONTROL Salva]**.

  Se l’utente non è stato creato in precedenza, consulta la [documentazione Aggiungere utenti](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/ui/users){target="_blank"}.

  L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

  +++

## Flusso di lavoro di creazione della campagna {#workflow}

La creazione di campagne di successo segue un processo chiaro e ripetibile. Di seguito è riportato il flusso di lavoro dettagliato:

+++&#x200B;1. Pianificare la campagna

Prima di iniziare, chiarisci i tuoi obiettivi:

* **Qual è l’obiettivo?** (ad esempio dai impulso alle conversioni, incrementa il coinvolgimento, notifica alla clientela)
* **Chi è il pubblico?** (ad esempio, da creare o selezionare da Adobe Experience Platform)
* **Quale tipo di campagna è adatto?** (consulta [tipi di campagna](#campaign-types) sopra)
* **Quali canali utilizzerai?** (e-mail, push, SMS, in-app, web, ecc.) → [Consulta i canali supportati per tipo di campagna](../channels/gs-channels.md#channels)
* **Quando deve essere eseguito?** (immediato, pianificato o attivato da API)

+++

+++&#x200B;2. Configurare le proprietà della campagna

Configura le basi della campagna:

1. **Denomina e descrivi** la campagna per una facile identificazione
2. **Seleziona il tipo di campagna** (azione, attivata da API od orchestrata)
3. **Scegli il pubblico**
4. **Imposta la priorità** se si utilizza la gestione dei conflitti
5. **Configura la pianificazione** (per campagne con azioni) o i dettagli API (per quelle attivate da API)

**Guide specifiche per tipo:** [Proprietà delle campagne con azioni](campaign-properties.md) | [Proprietà delle campagne attivate da API](api-triggered-campaign-properties.md) | [Configurazione delle campagne orchestrate](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;3. Progettare i contenuti

Crea messaggi convincenti per il pubblico:

* Utilizza **e-mail designer** per esperienze e-mail avanzate
* Configura **notifiche push** con immagini e collegamenti di approfondimento
* Progetta **messaggi SMS/MMS** con personalizzazione
* Crea **esperienze in-app** e **web**
* Aggiungi **personalizzazione** utilizzando gli attributi del profilo e i dati contestuali

**Guide specifiche per tipo:** [Contenuto delle campagne con azioni](campaign-content.md) | [Contenuto delle campagne attivate da API](api-triggered-campaign-content.md) | [Contenuto delle campagne orchestrate](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;4. Rivedere e testare

Rivedi sempre la campagna prima dell’attivazione:

* **Visualizza l’anteprima del contenuto** con profili di test
* **Controlla il targeting** per assicurarti che il pubblico sia quello giusto
* **Verifica la pianificazione** e le impostazioni di attivazione
* **Richiedi l’approvazione** se si utilizza il flusso di lavoro di approvazione
* **Verifica la recapitabilità** con elenchi di seed

**Guide specifiche per tipo:** [Rivedere le campagne con azioni](review-activate-campaign.md) | [Rivedere le campagne attivate da API](review-activate-api-triggered-campaign.md) | [Rivedere le campagne orchestrate](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;5. Attivare la campagna

Al termine della revisione, attiva la campagna:

* **Attivazione manuale**: attiva immediatamente o in un tempo pianificato
* **Attivazione API**: per le campagne attivate da API, utilizza l’endpoint di attivazione
* **Processo di approvazione**: se necessario, attendi l’approvazione degli stakeholder

Nota: non è possibile modificare le campagne attive (è necessario duplicarle per apportare modifiche)

**Guide specifiche per tipo:** [Attivare le campagne con azioni](review-activate-campaign.md) | [Attivare le campagne attivate da API](review-activate-api-triggered-campaign.md) | [Attivare le campagne orchestrate](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;6. Monitorare e analizzare

Tieni traccia delle prestazioni della campagna:

* Visualizza i rapporti e l’analisi della campagna
* Monitora i tassi di consegna e le metriche di coinvolgimento
* Tieni traccia degli errori e dei mancati recapiti
* Analizza la conversione e il ROI
* Utilizza le informazioni per l’ottimizzazione

**Guide specifiche per tipo:** [Rapporti per le campagne con azioni](../reports/campaign-global-report-cja.md) | [Monitoraggio delle campagne attivate da API](api-triggered-campaigns.md#monitor) | [Analisi delle campagne orchestrate](../orchestrated/create-orchestrated-campaign.md)

+++

## Approfondiamo {#get-started-types}

Ora che comprendi le campagne in [!DNL Journey Optimizer], scegli il tipo di campagna per iniziare:

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campagne con azioni" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campagne con azioni</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campagne attivate da API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campagne orchestrate</a></td>
</tr></table>

Man mano che acquisisci dimestichezza con le campagne, esplora queste potenti funzionalità:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=it)

**Pianificazione e tempistica**

Pianifica campagne per date/ore specifiche, imposta consegne ricorrenti e ottimizza gli orari di invio per il massimo impatto. (Campagne con azioni e attivate da API)

[Informazioni sulla pianificazione](campaign-schedule.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

**Controllo della velocità**

Limita la velocità effettiva dei messaggi per evitare il sovraccarico su sistemi a valle come pagine di destinazione o piattaforme di assistenza clienti. (Campagne con azioni e attivate da API)

[Controllare i limiti della velocità](create-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=it)

**Targeting del pubblico**

Come target della campagna, imposta specifici tipi di pubblico di Adobe Experience Platform e gestisci in modo dinamico le qualificazioni del pubblico.

[Selezionare il pubblico della campagna](campaign-audience.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=it)

**Flussi di lavoro di approvazione**

Implementa i processi di revisione e approvazione prima che le campagne vengano pubblicate, garantendo qualità e conformità. (Campagne con azioni e attivate da API)

[Rivedere e modificare](review-activate-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=it)

**Ore di silenzio**

Rispetta le preferenze del cliente evitando la consegna dei messaggi durante gli intervalli di tempo specifici. (Campagne con azioni e attivate da API)

[Configurare le ore di silenzio](quiet-hours.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=it)

**Ottimizzazione**

Utilizza le regole di targeting e gli esperimenti sui contenuti per fornire contenuti personalizzati e massimizzare il coinvolgimento.

[Ottimizzare le campagne](../content-management/gs-message-optimization.md)
:::

::::
