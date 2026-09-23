---
solution: Journey Optimizer
product: journey optimizer
title: Migrazione di contenuti e percorsi
description: Scopri come migrare i modelli di contenuto e-mail e importare percorsi da piattaforme esterne.
feature: Get Started
topic: Content Management
role: User
level: Intermediate
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
    internal-label: Journeys
subfeature_v2: []
source-git-commit: 57b04ad2f74c5a0a1d836bac9a45c9efd84ceb96
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 8%
---
# Migrazione di contenuti e percorsi {#migrate-content-and-journeys}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

Se stai passando a [!DNL Journey Optimizer] da un&#39;altra piattaforma di marketing, non è necessario iniziare da una lavagna vuota. Journey Optimizer include un’area di lavoro dedicata che importa il contenuto e i percorsi e-mail esistenti. Vengono convertiti in [!DNL Journey Optimizer] modelli di contenuto e percorsi, in modo da poter scegliere il punto in cui si è interrotto invece di ricostruire tutto da zero.

Per migrare i contenuti e i percorsi a Journey Optimizer, devi disporre delle seguenti autorizzazioni: Gestisci campagne, Gestisci Percorsi, Gestisci messaggi, Gestisci segmenti, Gestisci elementi libreria, Visualizza e gestisci sandbox e Gestisci la configurazione dell’integrazione di AJO. [Ulteriori informazioni su ruoli e autorizzazioni](../administration/permissions.md)

È possibile accedere a questa area di lavoro direttamente dalla home page di [!DNL Journey Optimizer].

![Accesso all&#39;area di lavoro di migrazione](assets/onboarding-hub-15.png)

## Configurare una connessione {#set-up-a-connection}

>[!CONTEXTUALHELP]
>id="ajo_migration_connection_name"
>title="Nome connessione"
>abstract="Un nome descrittivo che identifica il sistema di origine (ad es. “Marketing-Automation-Prod”). Deve iniziare con una lettera e contenere solo caratteri alfanumerici, trattini bassi o trattini (4-50 caratteri)."


>[!CONTEXTUALHELP]
>id="ajo_migration_base_api_url"
>title="URL API di base"
>abstract="L’URL principale dell’API, senza percorsi di risorse o stringhe di query, ad esempio https://api.esempio.com."

>[!CONTEXTUALHELP]
>id="ajo_migration_authentication_method"
>title="Scelta di un metodo di autenticazione"
>abstract="La chiave API invia una singola credenziale con ciascuna richiesta, mentre OAuth 2.0 utilizza un protocollo basato su token più adatto per le API aziendali e di terze parti."

>[!CONTEXTUALHELP]
>id="ajo_migration_client_id"
>title="ID client"
>abstract="L’identificatore pubblico dell’applicazione, emesso al momento della registrazione al server di autorizzazione."

>[!CONTEXTUALHELP]
>id="ajo_migration_client_secret"
>title="Segreto client"
>abstract="Credenziali riservate note solo all’app e al server di autorizzazione. Non esporlo mai nel codice lato client."


>[!CONTEXTUALHELP]
>id="ajo_migration_token_url"
>title="URL token"
>abstract="Endpoint del server di autorizzazione che emette i token di accesso per il flusso di credenziali del client, che in genere termina in /oauth/token o /token."


>[!NOTE]
>
>Se carichi file HTML o screenshot anziché importarli tramite un’API, non è necessaria alcuna connessione.

Per importare contenuto o percorsi tramite un&#39;API, connettere [!DNL Journey Optimizer] alla piattaforma di origine:

1. Nell&#39;area di lavoro, selezionare **[!UICONTROL Gestisci connessioni]**.

   ![Pulsante Gestisci connessioni](assets/onboarding-hub-14.png)

1. Fare clic su **[!UICONTROL Nuova connessione]**.

   ![Finestra Gestisci connessioni con il pulsante Nuova connessione evidenziato](assets/onboarding-hub-1.png)

1. Compila i dettagli seguenti:

   * **[!UICONTROL Nome connessione]**: nome che identifica il sistema di origine, ad esempio `Marketing-Automation-Prod`. I nomi devono iniziare con una lettera e possono contenere solo lettere, numeri, trattini bassi o trattini, compresi tra 4 e 50 caratteri.
   * **[!UICONTROL URL API di base]**: URL radice dell&#39;API del sistema di origine, senza percorso di risorsa o stringa di query, ad esempio `https://api.example.com`.
   * **[!UICONTROL Descrizione]**: contesto facoltativo per aiutare te e altri utenti a identificare lo scopo della connessione.
   * **[!UICONTROL Metodo di autenticazione]**: modalità di autenticazione di [!DNL Journey Optimizer] nel sistema di origine. Scegliere **Chiave API** per inviare una singola credenziale a ogni richiesta. Scegliere **OAuth 2.0** per utilizzare un protocollo basato su token più adatto alle API aziendali e di terze parti.
   * **[!UICONTROL ID client]**: l&#39;identificatore pubblico assegnato all&#39;applicazione al momento della registrazione con il server autorizzazioni. Richiesto per le connessioni OAuth 2.0.
   * **[!UICONTROL Segreto client]**: le credenziali riservate associate all&#39;ID client. Tienilo privato, in quanto è noto solo alla tua applicazione e al server di autorizzazione. Richiesto per le connessioni OAuth 2.0.
   * **[!UICONTROL URL token]**: l&#39;endpoint del server autorizzazioni che emette i token di accesso per il flusso di credenziali client, in genere con fine in `/oauth/token` o `/token`. Richiesto per le connessioni OAuth 2.0.

     ![Nuovo modulo di connessione con campi per il nome della connessione, l&#39;URL API di base e i dettagli di autenticazione](assets/onboarding-hub-2.png)

1. Seleziona **[!UICONTROL Crea]**.

1. Una volta configurata la connessione, utilizza il menu avanzato per eliminarla o per contrassegnarla come predefinita in modo che venga preselezionata alla successiva importazione di contenuto o percorsi.

   ![Menu avanzato con opzioni per eliminare una connessione o contrassegnarla come predefinita](assets/onboarding-hub-3.png)

## Importa contenuto e-mail {#import-email-content}

Dopo aver creato un&#39;origine per il contenuto, un file HTML o una connessione alla piattaforma di origine, importarla nell&#39;area di lavoro per convertirla in un modello di contenuto [!DNL Journey Optimizer].

1. Dalla scheda **[!UICONTROL Contenuto e-mail]**, scegli come desideri importare il contenuto delle e-mail:

   * **[!UICONTROL Carica HTML]**: seleziona uno o più file di posta elettronica di HTML dal computer.

   * **[!UICONTROL Sfoglia dalla connessione]**: sfoglia e seleziona le e-mail direttamente dalla piattaforma di marketing connessa, senza dover esportare e caricare i file manualmente.

   ![Scheda Contenuto e-mail con opzioni per caricare HTML o sfogliare da una connessione](assets/onboarding-hub-6.png)

1. Per un caricamento HTML, cerca il file o trascinalo nell’area di caricamento. Al termine, fai clic su **[!UICONTROL Carica]**.

   I file devono essere in formato `.html` o `.htm` e non devono superare i 10 MB.

   ![Area di caricamento file HTML per contenuto e-mail](assets/onboarding-hub-7.png)

1. Per importare dalla connessione, scegliere dall&#39;elenco E-mail e fare clic su **[!UICONTROL Importa]**.

1. Accedi all’e-mail importata e controlla il HTML importato.

1. Aggiungi la **[!UICONTROL riga dell&#39;oggetto]** e mappa ogni segnaposto di personalizzazione all&#39;attributo di profilo corrispondente.

   L&#39;area di lavoro converte automaticamente la sintassi di script di origine in sintassi Handlebars. Per un elenco degli operatori supportati, vedere [Operatori](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/personalization/functions/operators).

   ![Editor e-mail importato con campo oggetto e mappatura segnaposto personalizzazione](assets/onboarding-hub-8.png)

   >[!NOTE]
   >
   >Alcuni token di data di origine vengono mappati automaticamente e non vengono visualizzati come segnaposto di personalizzazione da mappare. Sono state migliorate anche l’individuazione e la mappatura dei token per una maggiore precisione.

1. Se l’e-mail fa riferimento a qualsiasi blocco di contenuto, risolvilo come frammento. Vedi [Importa frammenti](#import-fragments).

1. Seleziona una cartella per caricare le immagini dell&#39;e-mail in [!DNL Experience Manager Assets] e fai clic su **[!UICONTROL Carica risorse]**.

   ![Finestra di selezione delle cartelle per il caricamento di immagini di posta elettronica in Experience Manager Assets](assets/onboarding-hub-9.png)

1. Quando l&#39;e-mail è pronta, seleziona **[!UICONTROL Esegui migrazione]**, quindi seleziona **Visualizza e-mail** per aprire il nuovo modello di contenuto.

   ![Pulsante Esegui migrazione e opzione Visualizza in Journey Optimizer per un&#39;e-mail completata](assets/onboarding-hub-10.png)

Il modello di contenuto è ora disponibile in [!DNL Journey Optimizer] e pronto per essere utilizzato nei percorsi.

➡️ [Ulteriori informazioni sul modello di contenuto](../content-management/use-content-templates.md)

## Importa frammenti {#import-fragments}

I frammenti sono blocchi predefiniti riutilizzabili all’interno di un’e-mail, come intestazioni, piè di pagina o blocchi promozionali, che puoi creare una sola volta e riutilizzare in più e-mail per coerenza e authoring più rapido. Durante la migrazione di un&#39;e-mail, [!DNL Journey Optimizer] identifica tutti i blocchi di contenuto a cui fa riferimento e li inserisce come elemento azione, in modo da poterli migrare insieme all&#39;e-mail.

1. Dalla scheda **[!UICONTROL Frammenti]**, scegli come desideri importare il frammento:

   * **[!UICONTROL Carica HTML]**: seleziona uno o più file di frammenti di HTML dal computer.

   * **[!UICONTROL Sfoglia dalla connessione]**: sfoglia e seleziona i frammenti direttamente dalla piattaforma di marketing connessa, senza dover esportare e caricare i file manualmente.

   ![Scheda Frammenti con opzioni per caricare HTML o sfogliare da una connessione](assets/onboarding-fragment-1.png)

1. Puoi anche importare frammenti durante la migrazione di un’e-mail. Durante la migrazione del messaggio e-mail, [!DNL Journey Optimizer] lo analizza, identifica eventuali blocchi di contenuto di riferimento e li rende elementi di azione frammento nel messaggio e-mail, in modo da poterli risolvere senza uscire dal flusso di migrazione dei messaggi e-mail.

   ![Elemento azione frammento in un messaggio e-mail, che mostra un blocco di contenuto rilevato in attesa di risoluzione](assets/onboarding-fragment-2.png)

1. Per importare dalla connessione, scegliere dall&#39;elenco Frammenti e fare clic su **[!UICONTROL Importa]**.

1. Apri il frammento importato e risolvi le azioni rimanenti, ad esempio le risorse o gli attributi di profilo corrispondenti.

   ![Frammento importato con gli elementi azione rimanenti da risolvere](assets/onboarding-fragment-3.png)

1. Quando il frammento è pronto, seleziona **[!UICONTROL Esegui migrazione]**, quindi seleziona **Visualizza frammento** per aprirlo.


## Importa percorsi {#import-journeys}

Ricreare i percorsi importando una schermata del flusso di percorso o connettendosi alla piattaforma di origine. I percorsi vengono preparati come bozze modificabili che è possibile esaminare su un&#39;area di lavoro visiva prima che vengano migrati, in modo da ottenere una lista di controllo guidata di tutto ciò che richiede il tuo input per primo, invece di eseguire la migrazione alla modalità non visibile.

1. Dalla scheda **[!UICONTROL Percorsi]**, scegli come desideri importare i tuoi percorsi:

   * **[!UICONTROL Carica screenshot]**: seleziona uno o più screenshot dei percorsi dal computer.

   * **[!UICONTROL Sfoglia dalla connessione]**: sfoglia e seleziona i percorsi direttamente dalla piattaforma di marketing connessa, senza dover esportare e caricare manualmente le schermate.

   Scheda ![Percorsi con opzioni per caricare schermate o sfogliare da una connessione](assets/onboarding-hub-11.png)

1. Per il caricamento di uno screenshot, cerca il file o trascinalo nell’area di caricamento. Al termine, fai clic su **[!UICONTROL Carica]**.

   I file devono essere in formato png, jpg, gif, webp e non devono superare i 5 MB.

   ![Area di caricamento schermata per le immagini del percorso](assets/onboarding-hub-13.png)

1. Per importare dalla connessione, scegliere dall&#39;elenco percorsi e fare clic su **[!UICONTROL Importa]**.

1. Apri il percorso per visualizzarne l’anteprima sull’area di lavoro interattiva. Viene eseguito il rendering dell’intero percorso come area di lavoro nodo e bordo e i nodi che richiedono attenzione vengono contrassegnati in linea.

1. Dal pannello **[!UICONTROL Azioni]**, risolvi ogni elemento prima di eseguire la migrazione. L’intestazione del pannello mostra un numero live di elementi risolti sul totale e, selezionando un elemento di azione, viene evidenziato il nodo corrispondente nell’area di lavoro. Le azioni includono:

   * **[!UICONTROL Nome Percorso]**: impostare il nome del percorso prima della migrazione.
   * **[!UICONTROL Modelli di contenuto]**: selezionare il modello di contenuto appropriato per le azioni di percorso che ne richiedono uno. I modelli e-mail vengono convalidati man mano che vengono selezionati, con eventuali problemi di convalida visualizzati direttamente sull’elemento azione.
   * **[!UICONTROL Configurazioni canale]**: seleziona la configurazione richiesta per i canali, ad esempio e-mail e SMS.
   * **[!UICONTROL Segmenti di pubblico]**: mappa i tipi di pubblico di origine con i tipi di pubblico [!DNL Journey Optimizer] appropriati.

   ![Riquadro Azioni con attività risolte e pulsante Applica modifiche](assets/onboarding-hub-12.png)

1. Una volta risolto ogni elemento azione, seleziona **[!UICONTROL Migra]**.

   [!DNL Journey Optimizer] esegue un controllo finale sul percorso, riconvalida i modelli e-mail e conferma dell&#39;impostazione del nome del percorso. Eventuali informazioni mancanti o non valide bloccano la migrazione e vengono visualizzate in linea sulle azioni pertinenti. Una volta superato il controllo, un passaggio di conferma impedisce la migrazione accidentale e la pagina riflette quindi lo stato di elaborazione.

1. Se non è più necessaria una migrazione di percorso, eliminarla dall&#39;elenco dei percorsi o dal menu all&#39;interno di un percorso aperto.

   ![Riquadro Azioni con attività risolte e pulsante Applica modifiche](assets/onboarding-hub-16.png)

Il tuo percorso è ora disponibile in [!DNL Journey Optimizer], dove puoi rivedere l&#39;area di lavoro, apportare le modifiche finali e attivarla quando sei pronto per andare &quot;live&quot;. Selezionare **[!UICONTROL Visualizza percorso]** per aprire il percorso migrato direttamente in [!DNL Journey Optimizer]. Se la migrazione è stata completata ma non è stato possibile applicare alcuni elementi di azione, viene indicato esattamente il numero di elementi e viene indicato [!DNL Journey Optimizer] per completarli.

➡️ [Ulteriori informazioni sulla creazione di Percorsi](../building-journeys/journey-gs.md)

## Tracciare la migrazione {#track-migration-progress}

La panoramica di Workspace consente di tenere traccia di ogni e-mail o percorso importato e di trovare rapidamente quelli ancora in attesa di azione. Un set di KPI nella parte superiore dello schermo fornisce un conteggio immediato degli elementi in ogni stato:

* **Totale**: numero complessivo di elementi importati nell&#39;area di lavoro.
* **In corso**: elementi ancora in fase di revisione o mappatura prima della migrazione.
* **Migrazione effettuata**: elementi convertiti correttamente e disponibili in [!DNL Journey Optimizer].
* **Non riuscito**: elementi di cui non è stato possibile eseguire la migrazione e che richiedono attenzione.

![Panoramica di Workspace con KPI per gli elementi totali, in corso, migrati e con errori](assets/onboarding-hub-4.png)

Un set di filtri ti consente di restringere l’elenco dei contenuti importati in modo da poter concentrarti su un sottoinsieme specifico invece di scorrere ogni elemento. Combina uno o più dei seguenti filtri per trovare quello che stai cercando:

* **[!UICONTROL Azione richiesta]**: l&#39;elemento contiene elementi azione non risolti e richiede l&#39;input prima di poter essere migrato.
* **[!UICONTROL Elaborazione]**: è in corso la migrazione dell&#39;elemento.
* **[!UICONTROL Migrazione effettuata]**: l&#39;elemento è stato correttamente migrato ed è disponibile in [!DNL Journey Optimizer].
* **[!UICONTROL Non riuscito]**: la migrazione non è stata completata e richiede attenzione.

![Opzioni filtro per stato, data di creazione e data di aggiornamento nell&#39;area di lavoro](assets/onboarding-hub-5.png)

{{$include /help/_includes/do-not-localize/start/ai-augmented-migrate-content-and-journeys.md}}
