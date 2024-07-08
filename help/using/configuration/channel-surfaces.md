---
solution: Journey Optimizer
product: journey optimizer
title: Impostare le superfici di canale
description: Scopri come configurare e monitorare le superfici dei canali
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canale, superficie, tecnico, parametri, ottimizzatore
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9af49f0a47ad5bc1d2cea3e822ec20e2930140d3
workflow-type: tm+mt
source-wordcount: '1758'
ht-degree: 10%

---

# Impostare le superfici di canale {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="Superficie di canale"
>abstract="Una superficie di canale è una configurazione definita da un amministratore di sistema. Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via."

>[!CONTEXTUALHELP]
>id="ajo_admin_marketing_action"
>title="Azione di marketing"
>abstract="DA CONFERMARE"

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="ID app"
>abstract="DA CONFERMARE"

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Posizione sulla pagina"
>abstract="DA CONFERMARE"

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="Regola di corrispondenza pagine"
>abstract="DA CONFERMARE"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="URL predefinita"
>abstract="DA CONFERMARE"

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="URI di superficie"
>abstract="DA CONFERMARE"

Con [!DNL Journey Optimizer], puoi impostare le superfici dei canali (ad esempio i preset dei messaggi) che definiscono tutti i parametri tecnici richiesti per i tuoi messaggi: tipo di e-mail, e-mail e nome del mittente, app mobili, configurazione SMS e altro ancora.

>[!CAUTION]
>
> * Per creare, modificare ed eliminare le superfici dei canali, devi disporre dei predefiniti](../administration/high-low-permissions.md#administration-permissions) Gestione [messaggi autorizzazione.
>
> * Prima di creare le superfici di canale, devi eseguire i passaggi di [configurazione](../email/get-started-email-config.md) e-mail, [configurazione](../push/push-configuration.md) push, [configurazione](../sms/sms-configuration.md) SMS e [Direct](../direct-mail/direct-mail-configuration.md) mail.

Una volta configurate le superfici dei canali, sarà possibile selezionarle durante la creazione di messaggi da un percorso o da una campagna.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Creare una superficie di canale {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Impostazioni della superficie del canale"
>abstract="Quando imposti una superficie del canale, seleziona il canale a cui si applica e definisci tutti i parametri tecnici necessari per l’invio, ad esempio il tipo di e-mail, il nome del mittente, le app mobili, la configurazione degli SMS e altro ancora."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Impostazioni della superficie del canale"
>abstract="Per poter creare azioni quali e-mail da un percorso o da una campagna, devi innanzitutto creare una superficie del canale in cui sono definite tutte le impostazioni tecniche necessarie per i messaggi. Per creare, modificare ed eliminare le superfici del canale, devi disporre dell’autorizzazione Gestisci predefiniti messaggi."

>[!CONTEXTUALHELP]
>id="ajo_surface_marketing_action"
>title="Selezionare un’azione di marketing"
>abstract="Scegli un’azione di marketing nella superficie per associare al messaggio un criterio di consenso."

Per creare una superficie di canale, seguire seguenti operazioni:

1. Accedi al **[!UICONTROL menu Canali]** > **[!UICONTROL Branding]** > **[!UICONTROL Superfici]** canale, quindi fai clic su **[!UICONTROL Crea superficie]** canale.

   ![](assets/preset-create.png)

1. Immettete un nome e una descrizione (facoltativa) per la superficie, quindi selezionate i canali da configurare.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare caratteri di sottolineatura `_`, punti`.` e trattini `-` .

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla superficie, puoi selezionare **[!UICONTROL Gestisci accesso]**. [Scopri ulteriori informazioni sul controllo di accesso a livello di oggetto (OLAC, Object Level Access Control).](../administration/object-based-access.md)

1. Se hai selezionato il **[!UICONTROL canale e-mail]** , configura le impostazioni come descritto in [questa sezione](../email/email-settings.md).

   ![](assets/preset-email.png)

1. Per il canale di **[!UICONTROL notifica]** push, seleziona almeno una piattaforma -  **iOS** e/o **Android** - e le applicazioni mobili da utilizzare per ciascuna piattaforma.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Per ulteriori informazioni su come configurare l&#39;ambiente per l&#39;invio di notifiche push, consulta [questa sezione](../push/push-gs.md).

1. Per il **[!UICONTROL canale SMS]** , definisci le impostazioni come descritto in [questa sezione](../sms/sms-configuration.md).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Per ulteriori informazioni su come configurare l&#39;ambiente per l&#39;invio di messaggi SMS, fare riferimento a [questa sezione](../sms/sms-configuration.md).

1. Seleziona un&#39;azione **** di marketing per associare i criteri di consenso ai messaggi che usano questa superficie. Tutte le politiche di consenso associate a tale azione marketing vengono sfruttate al fine di rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

   >[!NOTE]
   >
   >Le policy sul consenso sono attualmente disponibili solo per le organizzazioni che hanno acquistato le **offerte aggiuntive Healthcare Shield** e **Privacy and Security Shield** .

   ![](assets/surface-marketing-action.png)

   >[!NOTE]
   >
   >È possibile selezionare solo un&#39;azione marketing.

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. È inoltre possibile salvare la superficie del canale come bozza e riprenderne la configurazione in un secondo momento.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >Non è possibile procedere con la creazione della superficie e-mail mentre il pool IP selezionato è in [edizione](ip-pools.md#edit-ip-pool) (**[!UICONTROL Stato elaborazione]** ) e non è mai stato associato al sottodominio selezionato. [Ulteriori informazioni](#subdomains-and-ip-pools)
   >
   >Salva la superficie come bozza e attendi che il pool IP abbia lo **[!UICONTROL stato Operazione riuscita]** per riprendere la creazione della superficie.

1. Una volta creata la superficie del canale, viene visualizzata nell&#39;elenco con lo stato di **[!UICONTROL elaborazione]** .

   Durante questo passaggio, verranno eseguiti diversi controlli per verificare che sia stato configurato correttamente. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   > Quando si crea una superficie di posta elettronica per un sottodominio, il tempo di elaborazione varia come descritto di seguito:
   >
   > * Per **i** nuovi sottodomini, il processo di creazione della prima superficie del canale può richiedere **da 10 minuti a 10 giorni**.
   > * Per **le** sandbox non di produzione o se il sottodominio selezionato è **già utilizzato** in un&#39;altra superficie di canale approvata, il processo richiede solo fino a **3 ore**.


   Questi controlli includono test tecnici e di configurazione eseguiti dal Adobe Systems team:

   * SPF convalida
   * DKIM convalida
   * Record MX convalida
   * Controlla IP che negano l&#39;elenco
   * Controllo host Helo
   * Verifica del pool IP
   * Record A/PTR, verifica del sottodominio t/m/res
   * FBL registrazione (questo controllo verrà eseguito solo la prima volta che viene creata una superficie email per un determinato sottodominio)

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, scopri ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-channel-surfaces).

1. Quando i controlli hanno esito positivo, la superficie del canale ottiene lo stato Attivo ****. È pronto per essere utilizzato per recapitare i messaggi.

   ![](assets/preset-active.png)

## Monitorare le superfici dei canali {#monitor-channel-surfaces}

Tutte le superfici dei canali vengono visualizzate nel **[!UICONTROL menu Canali]** > **[!UICONTROL Superfici]** canale. Sono disponibili filtri per facilitare la navigazione nell&#39;elenco (canale, utente, stato).

![](assets/preset-filters.png)

Una volta create, le superfici di canale possono avere i seguenti stati:

* **[!UICONTROL Bozza]**: la superficie del canale è stata salvata come bozza e non è ancora stata inviata. Aprilo per riprendere la configurazione.
* **[!UICONTROL Elaborazione]**: la superficie del canale è stata inviata ed è sottoposta a diverse fasi di verifica.
* **[!UICONTROL Attivo]**: la superficie del canale è stata verificata e può essere selezionata per creare messaggi.
* **[!UICONTROL Non riuscito]**: uno o più controlli non sono riusciti durante la verifica della superficie del canale.
* **[!UICONTROL Disattivato]**: la superficie del canale è disattivata. Non può essere utilizzato per creare nuovi messaggi.

Nel caso in cui la creazione di una superficie di canale fallisca, i dettagli su ogni possibile motivo di guasto sono descritti di seguito.

Se si verifica uno di questi errori, contatta [Adobe Systems l&#39;Assistenza](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} clienti per ottenere assistenza.

* **SPF convalida non riuscito**: SPF (Sender Policy Framework) è un protocollo di autenticazione della posta elettronica che consente di specificare gli IP autorizzati che possono inviare e-mail da un determinato sottodominio. SPF convalida errore significa che gli indirizzi IP nel record SPF non corrispondono agli indirizzi IP utilizzati per l&#39;invio di messaggi di posta elettronica ai provider di cassette postali.

* **DKIM convalida non riuscito**: DKIM (DomainKeys Identified Mail) consente al server destinatario di verificare che il messaggio ricevuto sia stato inviato dal mittente autentico del dominio associato e che il contenuto del messaggio originale non sia stato alterato durante il suo percorso. DKIM convalida errore significa che i server di posta riceventi non sono in grado di verificare l&#39;autenticità del messaggio contenuto e la sua associazione con il dominio di invio.:

* **Record MX convalida non riuscito**: record MX (Mail eXchange) convalida errore significa che i server di posta responsabili dell&#39;accettazione delle e-mail in entrata per conto di un determinato sottodominio non sono configurati correttamente.

* **Configurazioni di deliverability non riuscite**: un errore nelle configurazioni di deliverability può verificarsi a causa di uno dei seguenti motivi:
   * Blocklist degli IP assegnati
   * Nome non valido `helo`
   * Messaggi di posta elettronica inviati da IP diversi da quelli specificati nel pool di IP della superficie corrispondente
   * Impossibile recapitare e-mail alle caselle di posta in arrivo dei principali ISP

## Modifica superficie di un canale {#edit-channel-surface}

Per modificare la superficie di un canale, seguire i passaggi riportati di seguito.

>[!NOTE]
>
>Non è possibile modificare le impostazioni ]**del**[!UICONTROL  notifica push. Se una superficie di canale è configurata solo per il canale notifica push, non è modificabile.

1. Nell&#39;elenco, fai clic sul nome di una superficie canale per aprirlo.

   ![](assets/preset-name.png)

1. Modifica le sue proprietà come desiderato.

   >[!NOTE]
   >
   >Se la superficie di un canale ha lo stato Attivo ****, i **[!UICONTROL campi Nome]**, **[!UICONTROL Seleziona canale]** e **[!UICONTROL Sottodominio]** sono grigi e non possono essere modificati.

1. Fare clic su **[!UICONTROL Invia]** per confermare le modifiche.

   >[!NOTE]
   >
   >È inoltre possibile salvare la superficie del canale come bozza e riprendere l&#39;aggiornamento in un secondo momento.

Una volta inviate le modifiche, la superficie del canale passerà attraverso un ciclo convalida simile a quello in atto durante [la creazione di una superficie](#create-channel-surface) di canale. Il tempo di elaborazione dell&#39;edizione può richiedere fino a **3 ore**.

>[!NOTE]
>
>Se modifichi solo i **[!UICONTROL campi dei parametri]** Descrizione ]**,**[!UICONTROL  Tipo e-mail ]**e/o**[!UICONTROL  Riprova e-mail, l&#39;aggiornamento è istantaneo.

### Dettagli degli aggiornamenti {#update-details}

Per le superfici dei canali con stato Attivo ****, è possibile controllare i dettagli dell&#39;aggiornamento. Per eseguire questa operazione:

Fate clic sull&#39;icona Aggiornamento **[!UICONTROL recente]** visualizzata accanto al nome della superficie attiva.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

**[!UICONTROL Nella schermata Aggiornamento recente]** è possibile visualizzare informazioni quali lo stato dell&#39;aggiornamento e l&#39;elenco delle modifiche richieste.

<!--![](assets/preset-recent-update-screen.png)-->

### Aggiorna stati {#update-statuses}

Un aggiornamento della superficie del canale può avere i seguenti stati:

* **[!UICONTROL Elaborazione]**: l&#39;aggiornamento della superficie del canale è stato inviato ed è in corso diversi passaggi di verifica.
* **[!UICONTROL Riuscito]**: la superficie del canale aggiornata è stata verificata e può essere selezionata per creare messaggi.
* **[!UICONTROL Non riuscito]**: uno o più controlli hanno avuto esito negativo durante la verifica dell&#39;aggiornamento della superficie del canale.

Ogni stato è descritto di seguito.

#### Elaborazione {#surface-processing}

Verranno eseguiti diversi controlli di recapito per verificare che la superficie sia stata aggiornata correttamente.

>[!NOTE]
>
>Se modifichi solo i **[!UICONTROL campi dei parametri]** Descrizione ]**,**[!UICONTROL  Tipo e-mail ]**e/o**[!UICONTROL  Riprova e-mail, l&#39;aggiornamento è istantaneo.

Il tempo di elaborazione può richiedere fino a **3 ore**. Scopri maggiori informazioni sui controlli effettuati durante il ciclo di convalida in [questa sezione](#create-channel-surface).

Se modificate una superficie già attiva:

* Il suo stato rimane **[!UICONTROL attivo]** mentre il processo di convalida è in corso.

* L&#39;icona **[!UICONTROL Aggiornamento recente]** viene visualizzata accanto al nome della superficie nell&#39;elenco delle superfici dei canali.

* Durante il processo di convalida, i messaggi configurati utilizzando questa superficie utilizzano ancora la versione precedente della superficie.

>[!NOTE]
>
>Non è possibile modificare la superficie di un canale mentre è in corso l&#39;aggiornamento. È comunque possibile fare clic sul nome, ma tutti i campi sono disattivati. Le modifiche non verranno applicate fino al completamento dell&#39;aggiornamento.

#### Operazione riuscita {#success}

Al termine del processo di convalida, la nuova versione della superficie viene utilizzata automaticamente in tutti i messaggi che utilizzano questa superficie. Tuttavia, potrebbe essere necessario attendere:
* pochi minuti prima che venga consumato dai messaggi unitari,
* Fino al batch successivo affinché Surface sia efficace nei messaggi batch.

#### Non riuscito {#failed}

Se il processo di convalida non riesce, verrà comunque utilizzata la versione precedente della superficie.

Scopri ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-channel-surfaces).

Se l&#39;aggiornamento non riesce, la superficie diventa nuovamente modificabile. È possibile fare clic sul suo nome e aggiornare le impostazioni che devono essere corrette.

## Disattivare una superficie di canale {#deactivate-a-surface}

Per rendere indisponibile una **[!UICONTROL superficie di canale Attivo]** al fine di creare nuovi messaggi, è possibile disattivarla. Tuttavia, i messaggi dei viaggi che attualmente utilizzano questa superficie non saranno interessati e continueranno a funzionare.

>[!NOTE]
>
>Non è possibile disattivare una superficie di canale durante l&#39;elaborazione di un aggiornamento. È necessario attendere che l&#39;aggiornamento abbia esito positivo o negativo. Scopri ulteriori informazioni sulla [modifica delle superfici](#edit-channel-surface) dei canali e sugli stati di [aggiornamento](#update-statuses).

1. Accedere all&#39;elenco delle superfici dei canali.

1. Per la superficie attiva scelta, fare clic su **[!UICONTROL Altre azioni]** pulsante.

1. Seleziona **[!UICONTROL Disattiva.]**

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Le superfici dei canali disattivate non possono essere eliminate per evitare qualsiasi problema nei viaggi che utilizzano queste superfici per inviare messaggi.

Non è possibile modificare direttamente la superficie di un canale disattivato. Tuttavia, è possibile duplicarlo e modificare la copia per creare una nuova versione che verrà utilizzata per creare nuovi messaggi. Puoi anche attivarlo di nuovo e attendere che l&#39;aggiornamento abbia esito positivo per modificarlo.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
