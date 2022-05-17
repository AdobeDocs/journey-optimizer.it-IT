---
title: Configurare le impostazioni e-mail
description: Scopri come configurare le impostazioni e-mail a livello di predefinito messaggio
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: a485c58366f0690fb2515139658224d59468a24f
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 1%

---

# Configurare le impostazioni e-mail {#email-settings}

Definisci le impostazioni e-mail nella sezione dedicata della configurazione del predefinito del messaggio. Scopri come creare i predefiniti per i messaggi in [questa sezione](message-presets.md).

![](assets/preset-email.png)

## Tipo di e-mail {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definire la categoria e-mail"
>abstract="Seleziona il tipo di messaggi che verranno inviati quando utilizzi questo predefinito: Marketing per i messaggi promozionali, che richiedono il consenso dell’utente, o transazionali per i messaggi non commerciali, che possono anche essere inviati a profili non abbonati in contesti specifici."

In **TIPO E-MAIL** seleziona il tipo di messaggio da inviare con il predefinito: **Marketing** o **Transazionale**.

* Scegli **Marketing** per messaggi promozionali: questi messaggi richiedono il consenso dell’utente.

* Scegli **Transazionale** per messaggi non commerciali, ad esempio conferma dell’ordine, notifiche di reimpostazione della password o informazioni di consegna.

>[!CAUTION]
>
>**Transazionale** I messaggi possono essere inviati a profili che hanno annullato l’abbonamento a comunicazioni di marketing. Questi messaggi possono essere inviati solo in contesti specifici.

Quando [creazione di un messaggio](../messages/get-started-content.md#create-new-message), devi scegliere un predefinito di messaggio valido corrispondente alla categoria selezionata per il messaggio.

## Sottodominio e pool IP {#subdomains-and-ip-pools}

In **DETTAGLI DEL SOTTODOMINIO E DEL POOL IP** sezione , devi:

1. Seleziona il sottodominio da utilizzare per inviare le e-mail. [Ulteriori informazioni](about-subdomain-delegation.md)

1. Seleziona il pool IP da associare al predefinito. [Ulteriori informazioni](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

Impossibile procedere con la creazione dei predefiniti mentre il pool IP selezionato è in [edizione](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** e non è mai stato associato al sottodominio selezionato. In caso contrario, verrà comunque utilizzata la versione più vecchia dell’associazione pool/sottodominio IP. In questo caso, salva il predefinito come bozza e riprova una volta che il pool IP dispone del **[!UICONTROL Success]** stato.

>[!NOTE]
>
>Per gli ambienti non di produzione, Adobe non crea sottodomini di test preconfigurati né concede l’accesso a un pool IP di invio condiviso. Devi [delegare i tuoi sottodomini](delegate-subdomain.md) e utilizza gli IP del pool assegnato alla tua organizzazione.

## Annulla sottoscrizione elenco {#list-unsubscribe}

Su [selezione di un sottodominio](#subdomains-and-ip-pools) dall&#39;elenco, **[!UICONTROL Enable List-Unsubscribe]** viene visualizzata l&#39;opzione .

![](assets/preset-list-unsubscribe.png)

Questa opzione è attivata per impostazione predefinita.

Se lo lasci abilitato, nell’intestazione dell’e-mail verrà automaticamente incluso un collegamento per l’annullamento dell’abbonamento, ad esempio:

![](assets/preset-list-unsubscribe-header.png)

Se disattivi questa opzione, nell’intestazione dell’e-mail non verrà visualizzato alcun collegamento di annullamento all’abbonamento.

Il collegamento per l’annullamento dell’abbonamento è costituito da due elementi:

* Un **cancella indirizzo e-mail**, a cui vengono inviate tutte le richieste di annullamento dell’abbonamento.

   In [!DNL Journey Optimizer], l’indirizzo e-mail per l’annullamento dell’abbonamento è quello predefinito **[!UICONTROL Mailto (unsubscribe)]** l&#39;indirizzo visualizzato nel predefinito del messaggio, in base al [sottodominio selezionato](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* La **annulla sottoscrizione URL**, URL della pagina di destinazione in cui l’utente verrà reindirizzato una volta annullato l’abbonamento.

   Se aggiungi una [collegamento di rinuncia con un clic](../messages/consent.md#one-click-opt-out) per un messaggio creato utilizzando questo predefinito, l’URL di annullamento della sottoscrizione sarà l’URL definito per il collegamento di rinuncia con un solo clic.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >Se non aggiungi un collegamento di rinuncia con un solo clic al contenuto del messaggio, all’utente non verrà visualizzata alcuna pagina di destinazione.

Ulteriori informazioni sull’aggiunta di un collegamento di annullamento dell’abbonamento dell’intestazione ai messaggi in [questa sezione](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Parametri di intestazione{#email-header}

In **[!UICONTROL HEADER PARAMETERS]** , inserisci i nomi del mittente e gli indirizzi e-mail associati al tipo di messaggi inviati utilizzando tale predefinito.

>[!CAUTION]
>
>Gli indirizzi e-mail devono utilizzare il [sottodominio delegato](about-subdomain-delegation.md).

* **[!UICONTROL Sender name]**: Nome del mittente, ad esempio il nome del brand.

* **[!UICONTROL Sender email]**: L&#39;indirizzo e-mail che desideri utilizzare per le tue comunicazioni. Ad esempio, se il sottodominio delegato è *marketing.luma.com*, puoi utilizzare *contact@marketing.luma.com*.

* **[!UICONTROL Reply to (name)]**: Nome che verrà utilizzato quando il destinatario fa clic sul pulsante **Rispondi** nel loro software client e-mail.

* **[!UICONTROL Reply to (email)]**: L’indirizzo e-mail che verrà utilizzato quando il destinatario fa clic sul pulsante **Rispondi** nel loro software client e-mail. È necessario utilizzare un indirizzo definito nel sottodominio delegato (ad esempio, *reply@marketing.luma.com*), altrimenti le e-mail verranno eliminate.

* **[!UICONTROL Error email]**: Tutti gli errori generati dagli ISP dopo alcuni giorni di consegna della posta (mancati recapiti asincroni) vengono ricevuti su questo indirizzo.

![](assets/preset-header.png)

>[!NOTE]
>
>Gli indirizzi devono iniziare con una lettera (A-Z) e possono contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, punto`.` e trattino `-` caratteri.

## Parametri di esecuzione di un nuovo tentativo e-mail {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Regolare il periodo di tempo per l’esecuzione dei nuovi tentativi"
>abstract="I tentativi vengono eseguiti per 3,5 giorni (84 ore) quando un messaggio e-mail non riesce a causa di un errore temporaneo di messaggio non recapitato. È possibile regolare questo periodo di tempo predefinito per l&#39;esecuzione di un nuovo tentativo in base alle proprie esigenze."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="Informazioni sui nuovi tentativi"

Puoi configurare le **Parametri di esecuzione di un nuovo tentativo e-mail**.

![](assets/preset-retry-parameters.png)

Per impostazione predefinita, la [periodo di tempo di nuovo](retries.md#retry-duration) è impostato su 84 ore, ma è possibile regolare questa impostazione in base alle proprie esigenze.

È necessario immettere un valore intero (in ore o minuti) entro il seguente intervallo:

* Per le e-mail di marketing, il periodo minimo di esecuzione dei nuovi tentativi è di 6 ore.
* Per le e-mail transazionali, il periodo minimo di esecuzione dei tentativi è di 10 minuti.
* Per entrambi i tipi di e-mail, il periodo massimo di esecuzione dei nuovi tentativi è di 84 ore (o 5040 minuti).

Ulteriori informazioni sui nuovi tentativi in [questa sezione](retries.md).

## Tracciamento URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Parametri di tracciamento URL"
>abstract="Usa questa sezione per aggiungere automaticamente i parametri di tracciamento agli URL della campagna presenti nel contenuto dell’e-mail."

È possibile utilizzare **[!UICONTROL URL Tracking Parameters]** per misurare l’efficacia delle attività di marketing su tutti i canali. Questa funzione è facoltativa.

I parametri definiti in questa sezione verranno aggiunti alla fine degli URL inclusi nel contenuto del messaggio e-mail. Puoi quindi acquisire questi parametri in strumenti di analisi web come Adobe Analytics o Google Analytics e creare vari rapporti sulle prestazioni.

![](assets/preset-url-tracking.png)

Tre parametri di tracciamento URL vengono compilati automaticamente come esempio quando crei un predefinito per messaggi. Puoi modificarli e aggiungere fino a 10 parametri di tracciamento utilizzando **[!UICONTROL Add new parameter]** pulsante .

Per configurare un parametro di tracciamento URL, puoi immettere direttamente i valori desiderati nel **[!UICONTROL Name]** e **[!UICONTROL Value]** oppure scegliere da un elenco di valori predefiniti passando ai seguenti oggetti:

* Attributi del percorso: **ID sorgente**, **Nome origine**, **ID versione sorgente**
* Attributi del messaggio: **ID azione**, **Nome azione**
* Attributi di Offer decisioning: **ID offerta**, **Nome offerta**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Non selezionare una cartella: assicurati di passare alla cartella necessaria e seleziona un attributo di profilo da utilizzare come valore del parametro di tracciamento.

Di seguito sono riportati alcuni esempi di URL compatibili con Adobe Analytics e Google Analytics.

* URL compatibile con Adobe Analytics: www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}_immagine_{{context.system.source.name}}

* Google Analytics URL compatibile: www.YourLandingURL.com?utm_medium=email&amp;utm_source=AJO&amp;utm_campaign={{context.system.source.id}}&amp;utm_content=image

>[!NOTE]
>
>È possibile combinare la digitazione di valori di testo e la selezione di valori predefiniti. Ogni **[!UICONTROL Value]** Il campo può contenere fino a 255 caratteri in totale.
