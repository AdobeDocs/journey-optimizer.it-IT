---
solution: Journey Optimizer
product: journey optimizer
title: Creare una campagna
description: Scopri come creare campagne in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: crea, ottimizzatore, campagna, superficie, messaggi
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 22%

---

# Creare una campagna {#create-campaign}

Per creare una nuova campagna, passa al menu **[!UICONTROL Campagne]** nella barra a sinistra, quindi fai clic su **[!UICONTROL Crea campagna]**. Puoi anche duplicare una campagna live esistente per crearne una nuova. [Scopri come](modify-stop-campaign.md#duplicate).

Prima di iniziare, leggi i prerequisiti della campagna in [questa pagina](get-started-with-campaigns.md#before-starting-campaign-prerequisites).

## Seleziona il tipo di campagna {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo di campagna"
>abstract="Le **Campagne pianificate** vengono eseguite immediatamente o in una data specificata e hanno lo scopo di inviare messaggi di tipo marketing. Le campagne **attivate da API** vengono eseguite utilizzando una chiamata API. Hanno lo scopo di inviare messaggi di marketing (messaggi promozionali che richiedono il consenso dell’utente) o messaggi transazionali (messaggi non commerciali, che possono essere inviati anche a profili non abbonati in contesti specifici)."

Quando crei una nuova campagna, devi innanzitutto selezionare il tipo di campagna. Sono disponibili tre tipi di campagne:

1. **[!UICONTROL Pianificato - Marketing]** - Queste campagne vengono eseguite immediatamente o in una data specificata. Le campagne pianificate hanno lo scopo di inviare **messaggi di marketing** o creare azioni in entrata. Vengono configurati ed eseguiti dall’interfaccia utente di.

1. **[!UICONTROL Attivato da API - Marketing]** - Queste campagne vengono eseguite utilizzando una chiamata API. Seleziona questo tipo di campagna per inviare comunicazioni di marketing personalizzate a tipi di pubblico mirati.  [Scopri come attivare una campagna utilizzando le API](api-triggered-campaigns.md)

1. **[!UICONTROL Attivato da API - Transazionale]** - Come per le campagne di marketing attivate da API, queste campagne vengono eseguite utilizzando una chiamata API. Le campagne transazionali attivate da API hanno lo scopo di inviare **messaggi transazionali**, ovvero messaggi inviati in seguito a un&#39;azione eseguita da un individuo: richiesta di reimpostazione della password, acquisto del carrello, ecc.  [Scopri come attivare una campagna utilizzando le API](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

## Definire le proprietà della campagna {#create}

Una volta creata la campagna, devi definirne le proprietà. Segui i passaggi seguenti:

1. Nella sezione **[!UICONTROL Proprietà]**, immetti il nome e una descrizione per la campagna.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. (facoltativo) Utilizza il campo **Tag** per assegnare alla campagna i tag unificati di Adobe Experience Platform. Questo consente di classificarle facilmente e migliorare la ricerca dall’elenco delle campagne. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags).

1. (facoltativo) Puoi limitare l’accesso a questa campagna in base alle etichette di accesso. Per aggiungere un limite di accesso, seleziona il pulsante **[!UICONTROL Gestisci accesso]** nella parte superiore della pagina. Assicurati di selezionare solo le etichette per le quali disponi dell’autorizzazione. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

## Definire il pubblico della campagna {#audience}

Ora puoi selezionare il pubblico della campagna. Un pubblico è un insieme di persone che condividono comportamenti e/o caratteristiche simili.

>[!IMPORTANT]
>
>* L&#39;utilizzo dei tipi di pubblico e degli attributi di [composizione del pubblico](../audience/get-started-audience-orchestration.md) non è attualmente disponibile per l&#39;utilizzo con Healthcare Shield o Privacy and Security Shield.
>
>* Per le campagne attivate da API, il pubblico deve essere impostato tramite chiamata API.

Per definire la popolazione target di una campagna di marketing pianificata, effettua le seguenti operazioni:

1. Nella sezione **Pubblico**, fai clic sul pulsante **[!UICONTROL Seleziona pubblico]** per visualizzare l&#39;elenco dei tipi di pubblico di Adobe Experience Platform disponibili. Ulteriori informazioni sui tipi di pubblico in [questa sezione](../audience/about-audiences.md).

1. Nel campo **[!UICONTROL Tipo di identità]**, scegli il tipo di chiave da utilizzare per identificare i singoli utenti del pubblico selezionato. Puoi utilizzare un tipo di identità esistente o crearne uno nuovo utilizzando il servizio Adobe Experience Platform Identity. Gli spazi dei nomi di identità standard sono elencati in [questa pagina](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   È consentito un solo tipo di identità per campagna. Gli individui appartenenti a un segmento che non ha il tipo di identità selezionato tra le loro diverse identità non possono essere targetizzati dalla campagna.

   ![](assets/create-campaign-namespace.png){width="80%"}

   Ulteriori informazioni sui tipi di identità e sugli spazi dei nomi sono disponibili nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=it){target="_blank"}.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->


## Seleziona il canale {#channel}

Ora puoi selezionare il canale e la relativa configurazione. Segui i passaggi seguenti:

1. Nella sezione **[!UICONTROL Azione]**, seleziona il canale di comunicazione.

   L&#39;elenco dei canali disponibili dipende dal modello di licenza e dai componenti aggiuntivi. Per le campagne attivate da API, sono disponibili solo i canali e-mail, SMS e di notifica push.

1. Seleziona la configurazione del canale.

   Configurazione definita da un [amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni](../configuration/channel-surfaces.md).

   Nell’elenco a discesa sono elencate solo le configurazioni di canale compatibili con il tipo di campagna di marketing.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Se si sta creando una campagna di notifica push, è possibile abilitare la **[!UICONTROL modalità Consegna rapida]**, un componente aggiuntivo di Journey Optimizer che consente l&#39;invio molto rapido di messaggi push in volumi elevati. [Ulteriori informazioni](../push/create-push.md#rapid-delivery)

## Modificare il contenuto {#content}

È ora possibile definire il contenuto del messaggio dal pulsante **[!UICONTROL Modifica contenuto]**. Il processo di creazione dei contenuti dipende dal canale selezionato.

Scopri i passaggi dettagliati per creare il contenuto del messaggio nelle pagine seguenti:


<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="e-mail" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>E-mail</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>Notifica push</strong></a></div></td>
<td><a href="../direct-mail/create-direct-mail.md"><img alt="direct mail" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><a href="../direct-mail/create-direct-mail.md"><strong>Direct mail</strong></a></div></td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../in-app/create-in-app.md"><img alt="in-app" src="../channels/assets/do-not-localize/inapp.jpg"></a>
<div align="center"><a href="../in-app/create-in-app.md"><strong>In-app</strong></a></div></td>
<td><a href="../web/create-web.md"><img alt="web" src="../channels/assets/do-not-localize/web.jpg"></a>
<div align="center"><a href="../web/create-web.md"><strong>Web</strong></a></div></td>
<td><a href="../code-based/create-code-based.md"><img alt="esperienza basata su codice" src="../channels/assets/do-not-localize/code.png"></a>
<div align="center"><a href="../code-based/create-code-based.md"><strong>Esperienza basata su codice</strong></a></div></td>
<td><a href="../content-card/create-content-card.md"><img alt="schede contenuto" src="../channels/assets/do-not-localize/cards.png"></a>
<div align="center"><a href="../content-card/create-content-card.md"><strong>Schede contenuto</strong></a></div></td>
</tr></table>

Una volta definito il contenuto, utilizza il pulsante **[!UICONTROL Simula contenuto]** per visualizzare in anteprima e verificare il contenuto con profili di test o dati di input di esempio caricati da un file CSV/JSON, oppure aggiunti manualmente. [Ulteriori informazioni](../content-management/preview-test.md). Per tornare alla schermata di creazione della campagna, fai clic sulla freccia sinistra.

![](assets/create-campaign-design.png)

Oltre al contenuto del messaggio stesso, puoi configurare le seguenti impostazioni:

1. (facoltativo) Nella sezione **[!UICONTROL Esperimento sui contenuti]**, puoi utilizzare il pulsante **[!UICONTROL Crea esperimento]** per verificare quale contenuto funziona meglio. Le funzionalità di sperimentazione dei contenuti sono descritte in [questa sezione](../content-management/content-experiment.md).

1. Nella sezione **[!UICONTROL Tracciamento azioni]**, specifica se desideri tenere traccia della reazione dei destinatari alla consegna: puoi tenere traccia dei clic e/o delle aperture.

   I risultati del tracciamento sono accessibili dal rapporto della campagna una volta eseguita la campagna. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report-cja.md)

## Pianificare la campagna {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Pianificazione della campagna"
>abstract="Per impostazione predefinita, le campagne iniziano al momento dell’attivazione manuale e terminano immediatamente dopo l’invio del messaggio. Puoi impostare una data e un’ora specifiche per l’invio del messaggio. Inoltre, puoi specificare una data di fine per le campagne ricorrenti o attivate da API. Nei trigger di Azione, puoi anche configurare la frequenza di invio del messaggio in base alle tue preferenze."

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

Per impostazione predefinita, le campagne pianificate iniziano una volta attivate manualmente e terminano non appena il messaggio viene inviato.

Se non desideri eseguire la campagna subito dopo l&#39;attivazione, puoi specificare la data e l&#39;ora dell&#39;invio del messaggio utilizzando l&#39;opzione **[!UICONTROL Inizio campagna]**. L&#39;opzione **[!UICONTROL Fine campagna]** consente di specificare quando interrompere l&#39;esecuzione di una campagna.

![](assets/create-campaign-schedule.png)

Per le campagne di notifica e-mail, SMS e push, puoi definire una frequenza con cui inviare il messaggio della campagna. A questo scopo, utilizza le opzioni **[!UICONTROL Action triggers]** nella schermata di creazione della campagna per specificare se la campagna deve essere eseguita ogni giorno, ogni settimana o ogni mese.

>[!NOTE]
>
>Quando pianifichi campagne in [!DNL Adobe Journey Optimizer], assicurati che la data/ora di inizio sia allineata alla prima consegna desiderata. Per le campagne ricorrenti, se l’ora pianificata iniziale è già passata, le campagne passeranno alla successiva fascia oraria disponibile in base alle relative regole di ricorrenza.

## Altre impostazioni {#settings}

Alcune impostazioni sono specifiche per il canale di comunicazione selezionato per la campagna o utilizzato per casi d’uso specifici. Sono descritte di seguito.

* Per le e-mail, puoi creare campagne di attivazione del piano di riscaldamento IP specifiche. Ulteriori informazioni in [questa sezione](../configuration/ip-warmup-campaign.md).
* Per il canale web, in-app e basato su codice, puoi assegnare un punteggio di priorità alla campagna. Ulteriori informazioni in [questa sezione](../conflict-prioritization/priority-scores.md).
* Per le campagne basate su schede di contenuto, puoi abilitare regole di consegna aggiuntive per scegliere gli eventi e i criteri di attivazione del messaggio. Ulteriori informazioni in [questa sezione](../content-card/create-content-card.md).
* Per i messaggi in-app, puoi utilizzare il pulsante **[!UICONTROL Modifica trigger]** per scegliere gli eventi e i criteri che attivano il messaggio. Ulteriori informazioni in [questa sezione](../in-app/create-in-app.md).

## Passaggi successivi {#next}

Una volta che la configurazione e il contenuto della campagna sono pronti, puoi rivederli e attivarli. [Ulteriori informazioni](review-activate-campaign.md)
