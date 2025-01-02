---
solution: Journey Optimizer
product: journey optimizer
title: Configurare le impostazioni e-mail
description: Scopri come configurare le impostazioni e-mail a livello di configurazione del canale
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: impostazioni, e-mail, configurazione
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 953adc90278a984ca8b73576274ec73fe98c08a1
workflow-type: tm+mt
source-wordcount: '2687'
ht-degree: 11%

---

# Configurare le impostazioni e-mail {#email-settings}

Per iniziare a creare un’e-mail, devi impostare le configurazioni del canale e-mail che definiscono tutti i parametri tecnici richiesti per i messaggi. [Scopri come creare le configurazioni](../configuration/channel-surfaces.md)

>[!NOTE]
>
>Per preservare la tua reputazione e migliorare il recapito dei messaggi, imposta i sottodomini da utilizzare per l’invio di e-mail prima di creare una configurazione e-mail. [Ulteriori informazioni](../configuration/about-subdomain-delegation.md)

Definisci le impostazioni e-mail nella sezione dedicata della configurazione del canale, come descritto di seguito.

![](assets/surface-email-settings.png){width="50%" align="left"}

La configurazione e-mail viene selezionata per l’invio di comunicazioni seguendo la logica seguente:

* Per i percorsi batch, non si applica all’esecuzione batch già avviata prima della configurazione della superficie e-mail. Le modifiche vengono rilevate alla successiva ricorrenza o alla nuova esecuzione.

* Per i messaggi transazionali, la modifica viene selezionata immediatamente per la comunicazione successiva (fino a cinque minuti di ritardo).

>[!NOTE]
>
>Le impostazioni di configurazione e-mail aggiornate vengono rilevate automaticamente nei percorsi o nelle campagne in cui viene utilizzata la configurazione.

## Tipo di e-mail {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definire il tipo di e-mail"
>abstract="Seleziona il tipo di e-mail da inviare quando utilizzi questa configurazione: marketing per e-mail promozionali, che richiedono il consenso dell’utente, oppure transazionale per e-mail non commerciali, che possono essere inviate anche a profili non iscritti in contesti specifici."

Nella sezione **Tipo di e-mail**, seleziona il tipo di messaggio per la configurazione: **[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]**.

* Seleziona **Marketing** per le e-mail promozionali, ad esempio le promozioni settimanali per un negozio al dettaglio. Questi messaggi richiedono il consenso dell’utente.

* Seleziona **Transazionale** per e-mail non commerciali, ad esempio conferma di un ordine, notifiche di reimpostazione della password o informazioni di consegna. Queste e-mail possono essere inviate ai profili che hanno **annullato l&#39;abbonamento** alle comunicazioni di marketing. Questi messaggi possono essere inviati solo in contesti specifici.

Quando crei un messaggio, devi scegliere una configurazione di canale valida che corrisponda alla categoria selezionata per l’e-mail.

## Subdomain {#subdomains}

Seleziona il sottodominio da utilizzare per inviare le e-mail.

Per preservare la reputazione del dominio, velocizza il processo di riscaldamento dell’IP e migliora il recapito messaggi, delega i sottodomini di invio ad Adobe. [Ulteriori informazioni](../configuration/about-subdomain-delegation.md)

<!--If needed, you can define dynamic subdomains. [Learn more](../email/surface-personalization.md#dynamic-subdomains)-->


## Dettagli del pool IP {#ip-pools}


Selezionare il pool IP da associare alla configurazione. [Ulteriori informazioni](../configuration/ip-pools.md)

![](assets/surface-subdomain-ip-pool.png){width="50%" align="left"}

Non è possibile procedere con la creazione della configurazione mentre il pool IP selezionato è in stato [edizione](../configuration/ip-pools.md#edit-ip-pool) (**[!UICONTROL Elaborazione]**) e non è mai stato associato al sottodominio selezionato. In caso contrario, verrà comunque utilizzata la versione meno recente dell’associazione pool IP/sottodominio. In questo caso, salva la configurazione come bozza e riprova una volta che il pool IP è nello stato **[!UICONTROL Operazione riuscita]**.

>[!NOTE]
>
>Per gli ambienti non di produzione, Adobe non crea sottodomini di test predefiniti né concede l’accesso a un pool IP di invio condiviso. Devi [delegare i tuoi sottodomini](../configuration/delegate-subdomain.md) e utilizzare gli IP del pool assegnato alla tua organizzazione.

Dopo aver selezionato un pool IP, le informazioni PTR sono visibili quando si passa il puntatore del mouse sugli indirizzi IP visualizzati sotto l&#39;elenco a discesa del pool IP. [Ulteriori informazioni sui record PTR](../configuration/ptr-records.md)

>[!NOTE]
>
>Se non è configurato alcun record PTR, contatta il rappresentante del tuo Adobe.

## Intestazione Annulla iscrizione elenco{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->


Quando [selezioni un sottodominio](#subdomains-and-ip-pools) dall&#39;elenco, viene visualizzata l&#39;opzione **[!UICONTROL Abilita annullamento sottoscrizione a elenco]**.

Questa opzione è abilitata per impostazione predefinita per includere un URL con un solo clic per annullare l’iscrizione nell’intestazione dell’e-mail, ad esempio:

![](assets/preset-list-unsubscribe-header.png)

Se disattivi questa opzione, nell’intestazione dell’e-mail non viene visualizzato alcun URL con un solo clic per annullare l’iscrizione.

Puoi selezionare il livello di consenso dall&#39;elenco a discesa **[!UICONTROL Livello di consenso]**. Può essere specifico per il canale o per l’identità del profilo. In base a questa impostazione, quando un utente annulla l’iscrizione utilizzando l’URL per l’annullamento dell’iscrizione all’elenco nell’intestazione di un’e-mail, il consenso viene aggiornato in Adobe Journey Optimizer a livello di canale o di ID.

L’intestazione Annulla iscrizione elenco offre due funzioni (Mailto e URL di annullamento iscrizione con un solo clic, come spiegato di seguito) che sono abilitate per impostazione predefinita, a meno che tu non deselezioni una o entrambe le funzioni:

* Un indirizzo **Invia a (annulla iscrizione)**, che è l&#39;indirizzo di destinazione a cui vengono indirizzate le richieste di annullamento iscrizione per l&#39;elaborazione automatica.

  In Journey Optimizer, l&#39;indirizzo e-mail per l&#39;annullamento dell&#39;iscrizione è l&#39;indirizzo predefinito **Invia a (annulla iscrizione)** visualizzato nella configurazione del canale, in base al [sottodominio selezionato](#subdomains-and-ip-pools).

  ![](assets/surface-list-unsubscribe-mailto.png){width="80%" align="left"}


* L&#39;**URL per l&#39;annullamento dell&#39;iscrizione con un solo clic**, che per impostazione predefinita è l&#39;intestazione per l&#39;annullamento dell&#39;iscrizione generata dall&#39;URL con un solo clic, in base al sottodominio impostato e configurato nelle impostazioni di configurazione del canale.

<!--
    >[!AVAILABILITY]
    >
    >One-click Unsubscribe URL Header will be available in Adobe Journey Optimizer starting June 3, 2024.
    >
-->

La funzionalità **[!UICONTROL Invia a (annulla sottoscrizione)]** e la funzionalità **[!UICONTROL URL annullamento sottoscrizione con un solo clic]** sono facoltative. Se non desideri utilizzare l’URL predefinito generato con un solo clic per annullare l’abbonamento, puoi deselezionare la funzione. Nel caso in cui l&#39;opzione **[!UICONTROL Configurazione rinuncia]** sia attivata e la funzionalità **[!UICONTROL URL annullamento iscrizione]** con un solo clic non sia selezionata, se si aggiunge un [collegamento di rinuncia con un solo clic](../privacy/opt-out.md#one-click-opt-out) a un messaggio creato utilizzando questa configurazione, l&#39;intestazione di annullamento iscrizione dell&#39;elenco sceglierà il collegamento di rinuncia con un solo clic inserito nel corpo dell&#39;e-mail e lo utilizzerà come valore URL di annullamento iscrizione con un solo clic.

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>Se non aggiungi un collegamento di rinuncia con un solo clic nel contenuto del messaggio e l’URL predefinito per l’annullamento dell’iscrizione con un solo clic non è selezionato nelle Impostazioni di configurazione del canale, nessun URL verrà trasmesso nell’intestazione e-mail come parte dell’intestazione per l’annullamento dell’iscrizione all’elenco.

Ulteriori informazioni sulla gestione delle funzionalità di annullamento dell&#39;iscrizione nei messaggi sono disponibili in [questa sezione](../email/email-opt-out.md#unsubscribe-header).

## Parametri intestazione {#email-header}

Nella sezione **[!UICONTROL Parametri intestazione]**, immetti i nomi del mittente e gli indirizzi e-mail associati al tipo di e-mail inviate utilizzando tale configurazione.

* **[!UICONTROL Nome mittente]**: il nome del mittente, ad esempio il nome del tuo marchio.
* **[!UICONTROL E-mail mittente]**: l&#39;indirizzo e-mail che desideri utilizzare per le tue comunicazioni.
* **[!UICONTROL Rispondi a (nome)]**: nome che verrà utilizzato quando il destinatario farà clic sul pulsante **Rispondi** nel software client di posta elettronica.
* **[!UICONTROL Rispondi a (e-mail)]**: l&#39;indirizzo e-mail che verrà utilizzato quando il destinatario farà clic sul pulsante **Rispondi** nel software client e-mail. [Ulteriori informazioni](#reply-to-email)
* **[!UICONTROL E-mail di errore]**: tutti gli errori generati dagli ISP dopo alcuni giorni di recapito della posta (mancati recapiti asincroni) vengono ricevuti su questo indirizzo. Su questo indirizzo vengono inoltre ricevute le notifiche fuori sede e le risposte alle richieste di verifica.

  Se desideri ricevere le notifiche di fuori sede e le risposte di richiesta di verifica su un indirizzo e-mail specifico non delegato ad Adobe, devi impostare una [procedura di inoltro](#forward-email). In tal caso, assicurati di disporre di una soluzione manuale o automatizzata per elaborare le e-mail che verranno inviate a questa casella in entrata.

>[!CAUTION]
>
>Gli indirizzi di posta elettronica **[!UICONTROL Sender]** e **[!UICONTROL Error]** devono utilizzare il [sottodominio delegato](../configuration/about-subdomain-delegation.md) corrente selezionato. Ad esempio, se il sottodominio delegato è *marketing.luma.com*, puoi utilizzare *contact@marketing.luma.com* e *error@marketing.luma.com*.

![](assets/preset-header.png)

>[!NOTE]
>
>Gli indirizzi devono iniziare con una lettera (A-Z) e possono contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri di sottolineatura `_`, punto`.` e trattino `-`.

### Rispondi a e-mail {#reply-to-email}

Durante la definizione dell&#39;indirizzo **[!UICONTROL Reply to (email)]**, è possibile specificare qualsiasi indirizzo e-mail a condizione che sia valido, nel formato corretto e senza errori di battitura.

La casella in entrata utilizzata per le risposte riceverà tutte le e-mail di risposta, ad eccezione delle notifiche fuori sede e delle risposte di richiesta di verifica, ricevute all&#39;indirizzo **[!UICONTROL E-mail di errore]**.

Per garantire una corretta gestione delle risposte, segui le raccomandazioni seguenti:

* Assicurati che la casella in entrata dedicata disponga di una capacità di ricezione sufficiente per ricevere tutte le e-mail di risposta inviate utilizzando la configurazione e-mail. Se la casella in entrata restituisce mancati recapiti, è possibile che alcune risposte dei clienti non vengano ricevute.

* Le risposte devono essere elaborate tenendo presenti gli obblighi in materia di privacy e conformità, in quanto possono contenere informazioni personali (PII, personally identifiable information).

* Non contrassegnare i messaggi come spam nella casella in entrata delle risposte, in quanto ciò influirà su tutte le altre risposte inviate a questo indirizzo.

Inoltre, quando definisci l&#39;indirizzo **[!UICONTROL Reply to (email)]**, assicurati di utilizzare un sottodominio con una configurazione di record MX valida, altrimenti l&#39;elaborazione della configurazione e-mail non riuscirà.

Se ricevi un errore durante l’invio della configurazione e-mail, significa che il record MX non è configurato per il sottodominio dell’indirizzo inserito. Contatta l’amministratore per configurare il record MX corrispondente o utilizza un altro indirizzo con una configurazione di record MX valida.

>[!NOTE]
>
>Se il sottodominio dell&#39;indirizzo immesso è un dominio con [delega completa](../configuration/delegate-subdomain.md#full-subdomain-delegation) ad Adobe, contatta il responsabile dell&#39;account Adobe.

### Inoltra e-mail {#forward-email}

Per inoltrare a un indirizzo e-mail specifico tutte le e-mail ricevute da [!DNL Journey Optimizer] per il sottodominio delegato, contatta l&#39;Assistenza clienti di Adobe.

>[!NOTE]
>
>Se il sottodominio utilizzato per l&#39;indirizzo **[!UICONTROL Reply to (email)]** non è delegato ad Adobe, l&#39;inoltro non può funzionare per questo indirizzo.

Devi fornire:

* L’indirizzo e-mail di inoltro desiderato. Il dominio dell’indirizzo e-mail di inoltro non può corrispondere ad alcun sottodominio delegato ad Adobe.
* Nome della sandbox.
* Il nome della configurazione o il sottodominio per cui verrà utilizzato l’indirizzo e-mail di inoltro.
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel configuration level.-->

>[!NOTE]
>
>Può essere presente un solo indirizzo e-mail di inoltro per sottodominio. Di conseguenza, se più configurazioni utilizzano lo stesso sottodominio, è necessario utilizzare lo stesso indirizzo e-mail di inoltro per tutte.

L’indirizzo e-mail di inoltro è configurato da Adobe. Questa operazione può richiedere da 3 a 4 giorni.

Al termine, tutti i messaggi ricevuti il **[!UICONTROL Indirizzo di risposta a (e-mail)]** e il **[!UICONTROL Indirizzo di posta elettronica di errore]** vengono inoltrati all&#39;indirizzo di posta elettronica specificato.

## E-mail Ccn {#bcc-email}

È possibile inviare una copia identica (o copia per conoscenza nascosta) delle e-mail inviate da [!DNL Journey Optimizer] a una casella in entrata Ccn in cui verranno archiviate per scopi di conformità o archiviazione.

Per eseguire questa operazione, abilitare la funzionalità facoltativa **[!UICONTROL E-mail Ccn]** a livello di configurazione del canale. [Ulteriori informazioni](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

Inoltre, quando definisci l&#39;indirizzo e-mail **[!UICONTROL Ccn]**, assicurati di utilizzare un sottodominio con una configurazione del record MX valida, altrimenti l&#39;elaborazione della configurazione e-mail non riuscirà.

Se ricevi un errore durante l’invio della configurazione e-mail, significa che il record MX non è configurato per il sottodominio dell’indirizzo inserito. Contatta l’amministratore per configurare il record MX corrispondente o utilizza un altro indirizzo con una configurazione di record MX valida.

## Invio a indirizzi e-mail soppressi {#send-to-suppressed-email-addresses}

>[!CONTEXTUALHELP]
>id="ajo_surface_suppressed_addresses"
>title="Sostituire la precedenza dell’elenco di soppressione"
>abstract="Puoi decidere di inviare messaggi transazionali ai profili anche se i loro indirizzi e-mail sono presenti nell’elenco di soppressione di Adobe Journey Optimizer a causa di un reclamo spam. Questa opzione è disabilitata per impostazione predefinita."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html?lang=it" text="Gestire l’elenco di soppressione"

>[!IMPORTANT]
>
>Questa opzione è disponibile solo se hai selezionato il tipo di e-mail **[!UICONTROL Transazionale]**. [Ulteriori informazioni](#email-type)

In [!DNL Journey Optimizer], tutti gli indirizzi e-mail contrassegnati come mancati recapiti permanenti, mancati recapiti non permanenti e segnalazioni di posta indesiderata vengono raccolti automaticamente nell&#39;[elenco di soppressione](../configuration/manage-suppression-list.md) ed esclusi dall&#39;invio in un percorso o in una campagna.

Tuttavia, puoi decidere di continuare a inviare messaggi del tipo **transazionale** ai profili anche se i loro indirizzi e-mail sono presenti nell&#39;elenco di soppressione a causa di un reclamo spam da parte dell&#39;utente.

In effetti, i messaggi transazionali generalmente contengono informazioni utili e attese, come una conferma di un ordine o una notifica di reimpostazione della password. Pertanto, anche se hanno segnalato uno dei tuoi messaggi di marketing come spam, nella maggior parte dei casi desideri che i tuoi clienti ricevano questo tipo di e-mail non commerciale.

Per includere gli indirizzi e-mail soppressi a causa di un reclamo spam nel pubblico dei messaggi transazionali, seleziona l&#39;opzione corrispondente dalla sezione **[!UICONTROL Invia a indirizzi e-mail soppressi]**.

![](assets/preset-suppressed-email-addresses.png)

>[!NOTE]
>
>Questa opzione è disabilitata per impostazione predefinita.

Come best practice per la consegna dei messaggi, questa opzione è disabilitata per impostazione predefinita per garantire che i clienti che hanno rinunciato non vengano contattati. Tuttavia, puoi modificare questa opzione predefinita, che ti consente quindi di inviare messaggi transazionali ai clienti.

Una volta abilitata questa opzione, anche se un cliente ha contrassegnato l’e-mail di marketing come spam, potrà ricevere i messaggi transazionali utilizzando la configurazione corrente. Assicurati sempre di gestire le preferenze di rinuncia in conformità alle best practice per la consegna dei messaggi.

## Elenco seed {#seed-list}

>[!CONTEXTUALHELP]
>id="ajo_surface_seed_list"
>title="Aggiungere un elenco seed"
>abstract="Seleziona l’elenco seed desiderato per aggiungere automaticamente indirizzi interni specifici ai tipi di pubblico. Questi indirizzi seed verranno inclusi al momento dell’esecuzione della consegna e riceveranno una copia esatta del messaggio a scopo di garanzia."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html?lang=it#use-seed-list" text="Cosa sono gli elenchi seed?"

Un elenco di seed in [!DNL Journey Optimizer] consente di includere automaticamente indirizzi di seed e-mail specifici nelle consegne. [Ulteriori informazioni](../configuration/seed-lists.md)

>[!CAUTION]
>
>Attualmente questa funzione si applica solo al canale e-mail.

Nella sezione **[!UICONTROL Elenco seed]** selezionare l&#39;elenco desiderato. Scopri come creare un elenco di seed in [questa sezione](../configuration/seed-lists.md#create-seed-list).

![](../configuration/assets/seed-list-surface.png)

>[!NOTE]
>
>È possibile selezionare un solo elenco di seed alla volta.

Quando la configurazione corrente viene utilizzata in una campagna o in un percorso, gli indirizzi e-mail nell’elenco di seed selezionato vengono inclusi al momento dell’esecuzione della consegna, il che significa che riceveranno una copia della consegna a scopo di garanzia.

Scopri come utilizzare l&#39;elenco di seed in una campagna o in un percorso in [questa sezione](../configuration/seed-lists.md#use-seed-list).

## Parametri di ripetizione delle e-mail {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Regolare il periodo di tempo per i tentativi"
>abstract="Quando la consegna di un’e-mail ha esito negativo a causa di un errore temporaneo di mancato recapito dei messaggi, vengono eseguiti nuovi tentativi per 3,5 giorni (84 ore). Puoi regolare questo periodo di tempo predefinito per i tentativi in base alle tue esigenze."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html?lang=it" text="Informazioni sui tentativi"

È possibile configurare i **parametri per i tentativi e-mail**.

![](assets/preset-retry-parameters.png)

Per impostazione predefinita, il periodo di tempo [per i tentativi](../configuration/retries.md#retry-duration) è impostato su 84 ore, ma puoi regolare questa impostazione per soddisfare meglio le tue esigenze.

È necessario immettere un valore intero (in ore o minuti) compreso nel seguente intervallo:

* Per le e-mail di marketing, il periodo minimo di nuovi tentativi è di 6 ore.
* Per le e-mail transazionali, il periodo minimo di nuovi tentativi è di 10 minuti.
* Per entrambi i tipi di e-mail, il periodo massimo di nuovi tentativi è di 84 ore (o 5040 minuti).

Ulteriori informazioni sui nuovi tentativi in [questa sezione](../configuration/retries.md).

## Tracciamento URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Definire i parametri di tracciamento degli URL"
>abstract="Usa questa sezione per aggiungere automaticamente i parametri di tracciamento agli URL presenti nel contenuto dell’e-mail. Questa funzione è facoltativa."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Anteprima dei parametri di tracciamento degli URL"
>abstract="Verifica il modo in cui i parametri di tracciamento verranno aggiunti agli URL presenti nel contenuto dell’e-mail."

Puoi utilizzare **[!UICONTROL Parametri di tracciamento URL]** per misurare l&#39;efficacia delle tue attività di marketing su tutti i canali. Questa funzione è facoltativa.

I parametri definiti in questa sezione verranno aggiunti alla fine degli URL inclusi nel contenuto del messaggio e-mail. Puoi quindi acquisire questi parametri negli strumenti di analisi web come Adobe Analytics o Google Analytics e creare vari rapporti sulle prestazioni.

Puoi aggiungere fino a 10 parametri di tracciamento utilizzando il pulsante **[!UICONTROL Aggiungi nuovo parametro]**.

![](assets/preset-url-tracking.png)

Per configurare un parametro di tracciamento URL, puoi immettere direttamente i valori desiderati nei campi **[!UICONTROL Nome]** e **[!UICONTROL Valore]**.

Puoi anche modificare ogni campo **[!UICONTROL Valore]** utilizzando l&#39;[editor di personalizzazione](../personalization/personalization-build-expressions.md). Fai clic sull’icona dell’edizione per aprire l’editor. Da qui, puoi selezionare gli attributi contestuali disponibili e/o modificare direttamente il testo.

![](assets/preset-url-tracking-editor.png)

I seguenti valori predefiniti sono disponibili tramite l’editor di personalizzazione:

* **ID azione Source**: ID dell&#39;azione E-mail aggiunta al percorso o alla campagna.

* **Nome azione Source**: nome dell&#39;azione Email aggiunta al percorso o alla campagna.

* **Source id**: ID del percorso o della campagna con cui è stata inviata l&#39;e-mail.

* **Nome Source**: nome del percorso o della campagna con cui è stata inviata l&#39;e-mail.

* **ID versione Source**: ID del percorso o della versione della campagna con cui è stata inviata l&#39;e-mail.

* **ID offerta**: ID dell&#39;offerta utilizzato nell&#39;e-mail.

>[!NOTE]
>
>Puoi combinare la digitazione di valori di testo e l’utilizzo di attributi contestuali dall’editor di personalizzazione. Ogni campo **[!UICONTROL Valore]** può contenere un numero di caratteri fino al limite di 5 KB.

<!--You can drag and drop the parameters to reorder them.-->

Di seguito sono riportati alcuni esempi di URL compatibili con Adobe Analytics e Google Analytics.

* URL compatibile con Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatibile con Google Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

Puoi visualizzare in anteprima dinamica l’URL di tracciamento risultante. Ogni volta che aggiungi, modifichi o rimuovi un parametro, l’anteprima viene aggiornata automaticamente.

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>Puoi anche aggiungere parametri di tracciamento dinamici personalizzati ai collegamenti presenti nel contenuto dell’e-mail, ma ciò non è possibile a livello di configurazione. È necessario eseguire questa operazione quando crei il messaggio utilizzando e-mail designer. [Ulteriori informazioni](message-tracking.md#url-tracking)

## Indirizzo di esecuzione {#execution-address}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="Definire l’indirizzo da utilizzare"
>abstract="Quando nel database sono disponibili diversi indirizzi e-mail o numeri di telefono (personali, professionali, ecc.), puoi scegliere a quale assegnare la priorità per l’invio."

Quando esegui il targeting di un profilo, nel database potrebbero essere disponibili diversi indirizzi e-mail (indirizzo e-mail professionale, indirizzo e-mail personale, ecc.).

In tal caso, [!DNL Journey Optimizer] utilizza l&#39;indirizzo specificato nei **[!UICONTROL campi di esecuzione]** a livello di sandbox per determinare quale indirizzo e-mail utilizzare dal servizio profilo in priorità. [Ulteriori informazioni](../configuration/primary-email-addresses.md)

>[!NOTE]
>
>Per verificare i campi attualmente utilizzati per impostazione predefinita, accedere al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Campi di esecuzione]**.

Tuttavia, puoi modificare questo campo di esecuzione predefinito a livello di configurazione del canale e-mail.

A questo scopo, modifica il campo **[!UICONTROL Indirizzo di consegna]** e seleziona un elemento dall&#39;elenco dei campi XDM di tipo e-mail disponibili.

![](assets/email-config-delivery-address.png)

Il campo di esecuzione viene aggiornato e viene quindi utilizzato come indirizzo principale. Sostituisce l’impostazione generale a livello di sandbox.
