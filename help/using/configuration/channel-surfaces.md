---
solution: Journey Optimizer
product: journey optimizer
title: Impostare le superfici di canale
description: Scopri come configurare e monitorare le superfici di canale
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
>title="Regola di corrispondenza delle pagine"
>abstract="DA CONFERMARE"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="URL predefinito"
>abstract="DA CONFERMARE"

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="URI di superficie"
>abstract="DA CONFERMARE"

Con [!DNL Journey Optimizer] è possibile impostare le superfici di canale (ossia i predefiniti per messaggi) che definiscono tutti i parametri tecnici richiesti per i messaggi: tipo di e-mail, e-mail e nome del mittente, app mobili, configurazione di SMS e altro ancora.

>[!CAUTION]
>
> * Per creare, modificare ed eliminare superfici di canale, è necessario disporre dell&#39;autorizzazione [Gestione predefiniti messaggi](../administration/high-low-permissions.md#administration-permissions).
>
> * Prima di creare superfici di canale, è necessario eseguire i passaggi [Configurazione e-mail](../email/get-started-email-config.md), [Configurazione push](../push/push-configuration.md), [Configurazione SMS](../sms/sms-configuration.md) e [Configurazione direct mail](../direct-mail/direct-mail-configuration.md).

Una volta configurate le superfici di canale, potrai selezionarle durante la creazione di messaggi da un percorso o da una campagna.

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

Per creare una superficie di canale, effettuate le seguenti operazioni:

1. Accedi al menu **[!UICONTROL Canali]** > **[!UICONTROL Marchio]** > **[!UICONTROL Superfici di canale]**, quindi fai clic su **[!UICONTROL Crea superficie di canale]**.

   ![](assets/preset-create.png)

1. Immettete un nome e una descrizione (facoltativa) per la superficie, quindi selezionate i canali da configurare.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri di sottolineatura `_`, punto`.` e trattino `-`.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla superficie, è possibile selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

1. Se hai selezionato il canale **[!UICONTROL Email]**, configura le impostazioni come descritto in [questa sezione](../email/email-settings.md).

   ![](assets/preset-email.png)

1. Per il canale **[!UICONTROL Notifica push]**, seleziona almeno una piattaforma - **iOS** e/o **Android** - e le app mobili da utilizzare per ogni piattaforma.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Per ulteriori informazioni su come configurare l&#39;ambiente per l&#39;invio di notifiche push, consulta [questa sezione](../push/push-gs.md).

1. Per il canale **[!UICONTROL SMS]**, definisci le impostazioni come descritto in [questa sezione](../sms/sms-configuration.md).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Per ulteriori informazioni su come configurare l&#39;ambiente per l&#39;invio di messaggi SMS, consulta [questa sezione](../sms/sms-configuration.md).

1. Selezionare una **[!UICONTROL azione di marketing]** per associare i criteri di consenso ai messaggi che utilizzano questa superficie. Tutti i criteri di consenso associati a tale azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

   >[!NOTE]
   >
   >I criteri di consenso sono attualmente disponibili solo per le organizzazioni che hanno acquistato i componenti aggiuntivi **Healthcare Shield** e **Privacy and Security Shield**.

   ![](assets/surface-marketing-action.png)

   >[!NOTE]
   >
   >Puoi selezionare una sola azione di marketing.

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. Potete anche salvare la superficie di canale come sformo e riprenderne la configurazione in un secondo momento.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >Non è possibile procedere con la creazione della superficie e-mail mentre il pool IP selezionato è in [edizione](ip-pools.md#edit-ip-pool) (**[!UICONTROL Elaborazione]** stato) e non è mai stato associato al sottodominio selezionato. [Ulteriori informazioni](#subdomains-and-ip-pools)
   >
   >Salva la superficie come bozza e attendi che lo stato del pool IP **[!UICONTROL Riuscito]** riprenda la creazione della superficie.

1. Una volta creata, la superficie di canale viene visualizzata nell&#39;elenco con lo stato **[!UICONTROL Elaborazione]**.

   Durante questo passaggio, verranno eseguiti diversi controlli per verificare che sia stato configurato correttamente. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   > Quando crei una superficie e-mail per un sottodominio, il tempo di elaborazione varia come descritto di seguito:
   >
   > * Per **nuovi sottodomini**, il processo di creazione della prima superficie di canale può richiedere da **10 minuti a 10 giorni**.
   > * Per **sandbox non di produzione** o se il sottodominio selezionato è **già utilizzato** in un&#39;altra superficie di canale approvata, il processo richiede solo fino a **3 ore**.


   Questi controlli includono la configurazione e i test tecnici eseguiti dal team di Adobi:

   * Convalida SPF
   * Convalida DKIM
   * Convalida record MX
   * Controlla l’inserire nell&#39;elenco Bloccati degli IP in corso...
   * Verifica host Helo
   * Verifica del pool IP
   * Record A/PTR, verifica del sottodominio t/m/res
   * Registrazione FBL (questo controllo verrà eseguito solo la prima volta che viene creata una superficie e-mail per un determinato sottodominio)

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-channel-surfaces).

1. Una volta completati i controlli, la superficie di canale ottiene lo stato **[!UICONTROL Attivo]**. È pronto per essere utilizzato per inviare messaggi.

   ![](assets/preset-active.png)

## Monitorare le superfici di canale {#monitor-channel-surfaces}

Tutte le superfici di canale vengono visualizzate nel menu **[!UICONTROL Canali]** > **[!UICONTROL Superfici di canale]**. Sono disponibili filtri per aiutarti a sfogliare l’elenco (canale, utente, stato).

![](assets/preset-filters.png)

Una volta create, le superfici di canale possono avere i seguenti stati:

* **[!UICONTROL Bozza]**: la superficie di canale è stata salvata come bozza e non è stata ancora inviata. Aprila per riprendere la configurazione.
* **[!UICONTROL Elaborazione]**: la superficie di canale è stata inviata e sta attraversando diversi passaggi di verifica.
* **[!UICONTROL Attivo]**: la superficie di canale è stata verificata e può essere selezionata per la creazione di messaggi.
* **[!UICONTROL Non riuscito]**: uno o più controlli non sono riusciti durante la verifica della superficie di canale.
* **[!UICONTROL Disattivato]**: superficie di canale disattivata. Non può essere utilizzato per creare nuovi messaggi.

In caso di errore durante la creazione di una superficie di canale, di seguito vengono descritti i dettagli di ogni possibile motivo di errore.

Se si verifica uno di questi errori, contatta l&#39;[Assistenza clienti Adobe](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} per ottenere assistenza.

* **Convalida SPF non riuscita**: SPF (Sender Policy Framework) è un protocollo di autenticazione e-mail che consente di specificare IP autorizzati in grado di inviare e-mail da un determinato sottodominio. In caso di errore di convalida SPF, gli indirizzi IP nel record SPF non corrispondono agli indirizzi IP utilizzati per l’invio di e-mail ai provider delle cassette postali.

* **Convalida DKIM non riuscita**: DKIM (DomainKeys Identified Mail) consente al server di destinazione di verificare che il messaggio ricevuto sia stato inviato dal mittente autentico del dominio associato e che il contenuto del messaggio originale non sia stato modificato durante la consegna. In caso di errore di convalida DKIM, i server di posta riceventi non sono in grado di verificare l&#39;autenticità del contenuto del messaggio e la sua associazione al dominio di invio.

* **Convalida record MX non riuscita**: errore di convalida del record MX (Mail eXchange) indica che i server di posta responsabili dell&#39;accettazione delle e-mail in entrata per conto di un determinato sottodominio non sono configurati correttamente.

* **Configurazioni di recapito non riuscite**: le configurazioni di recapito non riuscite possono verificarsi per uno dei motivi seguenti:
   * Inserire nell&#39;elenco Bloccati gli IP assegnati
   * Nome `helo` non valido
   * Messaggi e-mail inviati da IP diversi da quelli specificati nel pool IP della superficie corrispondente
   * Impossibile inviare e-mail alle caselle in entrata dei principali ISP

## Modificare una superficie di canale {#edit-channel-surface}

Per modificare una superficie di canale, effettuate le seguenti operazioni.

>[!NOTE]
>
>Impossibile modificare le **[!UICONTROL impostazioni notifiche push]**. Se una superficie di canale è configurata solo per il canale di notifica push, non è modificabile.

1. Nell&#39;elenco, fate clic sul nome di una superficie di canale per aprirla.

   ![](assets/preset-name.png)

1. Modificane le proprietà come desiderato.

   >[!NOTE]
   >
   >Se una superficie di canale ha lo stato **[!UICONTROL Attivo]**, i campi **[!UICONTROL Nome]**, **[!UICONTROL Seleziona canale]** e **[!UICONTROL Sottodominio]** sono disattivati e non possono essere modificati.

1. Fai clic su **[!UICONTROL Invia]** per confermare le modifiche.

   >[!NOTE]
   >
   >Potete anche salvare la superficie di canale come sformo e riprendere l&#39;aggiornamento in un secondo momento.

Una volta inviate le modifiche, la superficie di canale verrà sottoposta a un ciclo di convalida simile a quello in uso durante la [creazione di una superficie di canale](#create-channel-surface). Il tempo di elaborazione dell&#39;edizione può richiedere fino a **3 ore**.

>[!NOTE]
>
>Se modifichi solo i campi **[!UICONTROL Descrizione]**, **[!UICONTROL Tipo e-mail]** e/o **[!UICONTROL Parametri nuovi tentativi e-mail]**, l&#39;aggiornamento è istantaneo.

### Dettagli aggiornamento {#update-details}

Per le superfici di canale con stato **[!UICONTROL Attivo]**, è possibile controllare i dettagli dell&#39;aggiornamento. Per eseguire questa operazione:

Fai clic sull&#39;icona **[!UICONTROL Aggiornamento recente]** visualizzata accanto al nome della superficie attiva.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

Nella schermata **[!UICONTROL Aggiornamento recente]** è possibile visualizzare informazioni quali lo stato di aggiornamento e l&#39;elenco delle modifiche richieste.

<!--![](assets/preset-recent-update-screen.png)-->

### Aggiorna stati {#update-statuses}

Un aggiornamento della superficie di canale può avere i seguenti stati:

* **[!UICONTROL Elaborazione]**: l&#39;aggiornamento della superficie di canale è stato inviato ed è in corso diversi passaggi di verifica.
* **[!UICONTROL Operazione completata]**: la superficie di canale aggiornata è stata verificata e può essere selezionata per la creazione di messaggi.
* **[!UICONTROL Non riuscito]**: uno o più controlli non sono riusciti durante la verifica dell&#39;aggiornamento della superficie di canale.

Ciascuno stato è descritto di seguito.

#### Elaborazione {#surface-processing}

Verranno eseguiti diversi controlli di consegna per verificare che la superficie sia stata aggiornata correttamente.

>[!NOTE]
>
>Se modifichi solo i campi **[!UICONTROL Descrizione]**, **[!UICONTROL Tipo e-mail]** e/o **[!UICONTROL Parametri nuovi tentativi e-mail]**, l&#39;aggiornamento è istantaneo.

Il tempo di elaborazione può richiedere fino a **3 ore**. Ulteriori informazioni sui controlli eseguiti durante il ciclo di convalida in [questa sezione](#create-channel-surface).

Se modificate una superficie già attiva:

* Lo stato rimane **[!UICONTROL Attivo]** mentre il processo di convalida è in corso.

* L&#39;icona **[!UICONTROL Aggiornamento recente]** viene visualizzata accanto al nome della superficie nell&#39;elenco delle superfici di canale.

* Durante il processo di convalida, i messaggi configurati utilizzando questa superficie utilizzano ancora la versione precedente della superficie.

>[!NOTE]
>
>Impossibile modificare una superficie di canale mentre è in corso l&#39;aggiornamento. Puoi comunque fare clic sul nome, ma tutti i campi sono disattivati. Le modifiche verranno applicate solo dopo il completamento dell&#39;aggiornamento.

#### Operazione riuscita {#success}

Quando il processo di convalida ha esito positivo, la nuova versione della superficie viene utilizzata automaticamente in tutti i messaggi che la utilizzano. Tuttavia, potrebbe essere necessario attendere:
* pochi minuti prima di essere utilizzato dai messaggi unitari,
* fino al batch successivo affinché la superficie sia efficace nei messaggi batch.

#### Non riuscito {#failed}

Se il processo di convalida non riesce, verrà comunque utilizzata la versione precedente della superficie.

Ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-channel-surfaces).

Se l&#39;aggiornamento non riesce, la superficie diventa nuovamente modificabile. Fai clic sul nome e aggiorna le impostazioni da correggere.

## Disattivare una superficie di canale {#deactivate-a-surface}

Per rendere una superficie di canale **[!UICONTROL Attiva]** non disponibile per la creazione di nuovi messaggi, è possibile disattivarla. Tuttavia, i messaggi dei percorsi che attualmente utilizzano questa superficie non saranno interessati e continueranno a funzionare.

>[!NOTE]
>
>Non è possibile disattivare una superficie di canale durante l&#39;elaborazione di un aggiornamento. È necessario attendere che l’aggiornamento abbia esito positivo o negativo. Ulteriori informazioni sulla [modifica delle superfici di canale](#edit-channel-surface) e sugli [stati di aggiornamento](#update-statuses).

1. Accedere all&#39;elenco delle superfici di canale.

1. Per la superficie attiva desiderata, fare clic sul pulsante **[!UICONTROL Altre azioni]**.

1. Selezionare **[!UICONTROL Disattiva]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Le superfici di canale disattivate non possono essere eliminate per evitare problemi nei percorsi che le utilizzano per inviare messaggi.

Non è possibile modificare direttamente una superficie di canale disattivata. Tuttavia, puoi duplicarlo e modificarne la copia per creare una nuova versione da utilizzare per creare nuovi messaggi. Puoi anche attivarlo nuovamente e attendere che l’aggiornamento sia stato modificato correttamente.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
