---
solution: Journey Optimizer
product: journey optimizer
title: Impostare le superfici di canale
description: Scopri come configurare e monitorare le superfici dei canali
feature: Application Settings, Surface
topic: Administration
role: Admin
level: Intermediate
keywords: canale, superficie, tecnica, parametri, ottimizzatore
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9555c37f8bac295a668f64990e229c6e0e5ceb8d
workflow-type: tm+mt
source-wordcount: '1607'
ht-degree: 8%

---

# Impostare le superfici di canale {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="Superficie"
>abstract="Una “superficie” è una configurazione definita da un amministratore di sistema. Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via."

Con [!DNL Journey Optimizer], puoi impostare le superfici del canale (ad esempio i predefiniti per messaggi) che definiscono tutti i parametri tecnici necessari per i messaggi: tipo di e-mail, e-mail e nome del mittente, app mobili, configurazione SMS e altro ancora.

>[!CAUTION]
>
> * Per creare, modificare ed eliminare le superfici dei canali, è necessario disporre della [Gestisci superficie canale](../administration/high-low-permissions.md#manage-channel-surface) autorizzazione.
>
> * È necessario eseguire le [Configurazione e-mail](../email/get-started-email-config.md), [Configurazione push](../push/push-configuration.md) e [Configurazione SMS](../sms/sms-configuration.md) prima di creare superfici del canale.


Una volta configurate le superfici del canale, potrai selezionarle quando crei messaggi da un percorso o da una campagna.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Creare una superficie del canale {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Impostazioni della superficie del canale"
>abstract="Quando imposti una superficie del canale, seleziona il canale a cui si applica e definisci tutti i parametri tecnici necessari per l’invio, ad esempio il tipo di e-mail, il nome del mittente, le app mobili, la configurazione degli SMS e altro ancora."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Impostazioni della superficie del canale"
>abstract="Per poter creare azioni quali e-mail da un percorso o da una campagna, devi innanzitutto creare una superficie del canale in cui sono definite tutte le impostazioni tecniche necessarie per i messaggi. Per creare, modificare ed eliminare le superfici del canale, devi disporre dell’autorizzazione Gestisci superficie canale."

Per creare una superficie del canale, effettuate le seguenti operazioni:

1. Accedere al **[!UICONTROL Canali]** > **[!UICONTROL Branding]** > **[!UICONTROL Superfici dei canali]** menu, quindi fai clic su **[!UICONTROL Crea superficie del canale]**.

   ![](assets/preset-create.png)

1. Immetti un nome e una descrizione (facoltativi) per la superficie, quindi seleziona i canali da configurare.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, punto`.` e trattino `-` caratteri.

1. Se hai selezionato la **[!UICONTROL E-mail]** canale, configura le impostazioni come descritto in [questa sezione](../email/email-settings.md).

   ![](assets/preset-email.png)

1. Per **[!UICONTROL Notifica push]** canale, selezionare almeno una piattaforma -  **iOS** e/o **Android** - e le applicazioni mobili da utilizzare per ciascuna piattaforma.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Per ulteriori informazioni su come configurare l’ambiente per l’invio di notifiche push, consulta [questa sezione](../push/push-gs.md).

1. Per **[!UICONTROL SMS]** definire le impostazioni come descritto in [questa sezione](../sms/sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Per ulteriori informazioni su come configurare l’ambiente per l’invio di messaggi SMS, consulta [questa sezione](../sms/sms-configuration.md).

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. È inoltre possibile salvare la superficie del canale come bozza e riprendere la configurazione in un secondo momento.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >Impossibile procedere con la creazione della superficie mentre il pool IP selezionato è in uso [edizione](ip-pools.md#edit-ip-pool) (**[!UICONTROL Elaborazione]** status) e non è mai stato associato al sottodominio selezionato. [Ulteriori informazioni](#subdomains-and-ip-pools)
   >
   >Salva la superficie come sformo e attendi che il pool IP disponga della **[!UICONTROL Completato]** stato per riprendere la creazione della superficie.

1. Una volta creata la superficie del canale, questa viene visualizzata nell’elenco con la **[!UICONTROL Elaborazione]** stato.

   Durante questo passaggio, verranno eseguiti diversi controlli per verificare che sia stato configurato correttamente. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   >Durante la creazione della prima superficie e-mail per un determinato sottodominio, il tempo di elaborazione può richiedere **da 10 a 10 giorni**. Se il sottodominio selezionato è già utilizzato in un’altra superficie e-mail, saranno necessarie solo fino a 3 ore.

   Questi controlli includono la configurazione e i test tecnici eseguiti dal team di Adobe:

   * Convalida SPF
   * Convalida DKIM
   * Convalida record MX
   * Controlla la inserire nell&#39;elenco Bloccati degli IP
   * Controllo host Helo
   * Verifica del pool IP
   * Record A/PTR, verifica del sottodominio t/m/res
   * Registrazione FBL (questo controllo verrà eseguito solo la prima volta che viene creata una superficie e-mail per un determinato sottodominio)

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-channel-surfaces).

1. Una volta eseguiti i controlli, la superficie del canale ottiene il **[!UICONTROL Attivo]** stato. È pronto per essere utilizzato per inviare messaggi.

   ![](assets/preset-active.png)

## Superfici dei canali di monitoraggio {#monitor-channel-surfaces}

Tutte le superfici del canale vengono visualizzate nel **[!UICONTROL Canali]** > **[!UICONTROL Superfici dei canali]** menu. Sono disponibili filtri per aiutarti a sfogliare l’elenco (canale, utente, stato).

![](assets/preset-filters.png)

Una volta create, le superfici del canale possono avere i seguenti stati:

* **[!UICONTROL Bozza]**: La superficie del canale è stata salvata come bozza e non è ancora stata inviata. Apri per riprendere la configurazione.
* **[!UICONTROL Elaborazione]**: La superficie del canale è stata inviata e sta attraversando diverse fasi di verifica.
* **[!UICONTROL Attivo]**: La superficie del canale è stata verificata e può essere selezionata per creare messaggi.
* **[!UICONTROL Non riuscito]**: Uno o più controlli non sono riusciti durante la verifica della superficie del canale.
* **[!UICONTROL Disattivato]**: La superficie del canale è disattivata. Non può essere utilizzato per creare nuovi messaggi.

In caso di errore nella creazione di una superficie del canale, di seguito sono descritti i dettagli relativi a ogni possibile motivo di errore.

Se si verifica uno di questi errori, contatta [Adobe Customer Care](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} per ottenere assistenza.

* **Convalida SPF non riuscita**: SPF (Sender Policy Framework) è un protocollo di autenticazione e-mail che consente di specificare gli IP autorizzati che possono inviare e-mail da un determinato sottodominio. Un errore di convalida SPF indica che gli indirizzi IP nel record SPF non corrispondono agli indirizzi IP utilizzati per l’invio di e-mail ai provider di cassette postali.

* **Convalida DKIM non riuscita**: DKIM (DomainKeys Identified Mail) consente al server destinatario di verificare che il messaggio ricevuto sia stato inviato dal mittente originale del dominio associato e che il contenuto del messaggio originale non sia stato modificato. Un errore di convalida DKIM indica che i server di posta riceventi non sono in grado di verificare l’autenticità del contenuto del messaggio e la sua associazione al dominio di invio:

* **Convalida record MX non riuscita**: Un errore di convalida del record MX (Mail eXchange) indica che i server di posta elettronica responsabili dell’accettazione di e-mail in entrata per conto di un determinato sottodominio non sono configurati correttamente.

* **Configurazioni del recapito messaggi non riuscite**: Un errore di configurazione del recapito messaggi può verificarsi a causa di uno dei motivi seguenti:
   * Inserire nell&#39;elenco Bloccati degli IP allocati
   * Non valido `helo` name
   * E-mail inviate da IP diversi da quelli specificati nel pool IP della superficie corrispondente
   * Impossibile inviare e-mail alle caselle in entrata dei principali ISP

## Modificare una superficie del canale {#edit-channel-surface}

Per modificare una superficie di un canale, segui i passaggi riportati di seguito.

>[!NOTE]
>
>Non è possibile modificare il **[!UICONTROL Impostazioni delle notifiche push]**. Se una superficie del canale è configurata solo per il canale di notifica push, non è modificabile.

1. Dall’elenco, fare clic sul nome di una superficie del canale per aprirla.

   ![](assets/preset-name.png)

1. Modifica le proprietà desiderate.

   >[!NOTE]
   >
   >Se una superficie del canale ha **[!UICONTROL Attivo]** lo stato **[!UICONTROL Nome]**, **[!UICONTROL Seleziona canale]** e **[!UICONTROL Sottodominio]** i campi sono disattivati e non possono essere modificati.

1. Fai clic su **[!UICONTROL Invia]** per confermare le modifiche.

   >[!NOTE]
   >
   >È inoltre possibile salvare la superficie del canale come bozza e riprendere l&#39;aggiornamento in un secondo momento.

Una volta inviate le modifiche, la superficie del canale attraverserà un ciclo di convalida simile a quello esistente quando [creazione di una superficie del canale](#create-channel-surface). Il tempo di elaborazione dell&#39;edizione può richiedere fino a **3 ore**.

>[!NOTE]
>
>Se si modifica solo il **[!UICONTROL Descrizione]**, **[!UICONTROL Tipo e-mail]** e/o **[!UICONTROL Parametri di esecuzione di un nuovo tentativo e-mail]** campi, l&#39;aggiornamento è istantaneo.

### Dettagli di aggiornamento {#update-details}

Per le superfici del canale che hanno **[!UICONTROL Attivo]** puoi controllare i dettagli dell’aggiornamento. Per eseguire questa operazione:

Fai clic sul pulsante **[!UICONTROL Ultimo aggiornamento]** icona visualizzata accanto al nome della superficie attiva.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

Sulla **[!UICONTROL Ultimo aggiornamento]** è possibile visualizzare informazioni quali lo stato dell’aggiornamento e l’elenco delle modifiche richieste.

<!--![](assets/preset-recent-update-screen.png)-->

### Aggiorna stati {#update-statuses}

Un aggiornamento della superficie del canale può presentare i seguenti stati:

* **[!UICONTROL Elaborazione]**: L&#39;aggiornamento della superficie del canale è stato inviato e sta attraversando diverse fasi di verifica.
* **[!UICONTROL Completato]**: La superficie del canale aggiornata è stata verificata e può essere selezionata per creare messaggi.
* **[!UICONTROL Non riuscito]**: Uno o più controlli non sono riusciti durante la verifica dell&#39;aggiornamento della superficie del canale.

Ogni stato è descritto di seguito.

#### Elaborazione {#surface-processing}

Verranno eseguiti diversi controlli di recapito per verificare che la superficie sia stata aggiornata correttamente.

>[!NOTE]
>
>Se si modifica solo il **[!UICONTROL Descrizione]**, **[!UICONTROL Tipo e-mail]** e/o **[!UICONTROL Parametri di esecuzione di un nuovo tentativo e-mail]** campi, l&#39;aggiornamento è istantaneo.

Il tempo di elaborazione può richiedere fino a **3 ore**. Ulteriori informazioni sui controlli eseguiti durante il ciclo di convalida in [questa sezione](#create-channel-surface).

Se modificate una superficie già attiva:

* Il suo status rimane invariato **[!UICONTROL Attivo]** mentre il processo di convalida è in corso.

* La **[!UICONTROL Ultimo aggiornamento]** accanto al nome della superficie nell&#39;elenco delle superfici del canale viene visualizzata l&#39;icona.

* Durante il processo di convalida, i messaggi configurati utilizzando questa superficie utilizzano ancora la versione precedente della superficie.

>[!NOTE]
>
>Non è possibile modificare una superficie del canale mentre è in corso l&#39;aggiornamento. È comunque possibile fare clic sul suo nome, ma tutti i campi sono disattivati. Le modifiche verranno applicate solo dopo il completamento dell&#39;aggiornamento.

#### Operazione riuscita {#success}

Una volta che il processo di convalida ha esito positivo, la nuova versione della superficie viene utilizzata automaticamente in tutti i messaggi che utilizzano questa superficie. Tuttavia, potrebbe essere necessario attendere:
* alcuni minuti prima che sia consumata dai messaggi unitari,
* fino al batch successivo affinché la superficie sia efficace nei messaggi batch.

#### Non riuscito {#failed}

Se il processo di convalida non riesce, verrà comunque utilizzata la versione precedente della superficie.

Ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-channel-surfaces).

Quando l&#39;aggiornamento non riesce, la superficie diventa nuovamente modificabile. È possibile fare clic sul suo nome e aggiornare le impostazioni che devono essere corrette.

## Disattivare una superficie del canale {#deactivate-a-surface}

Per creare un **[!UICONTROL Attivo]** la superficie del canale non disponibile per creare nuovi messaggi, è possibile disattivarla. Tuttavia, i messaggi dei percorsi che utilizzano attualmente questa superficie non saranno interessati e continueranno a funzionare.

>[!NOTE]
>
>Non è possibile disattivare una superficie del canale durante l&#39;elaborazione di un aggiornamento. Attendere il completamento dell&#39;aggiornamento oppure l&#39;operazione non è riuscita. Ulteriori informazioni su [modifica delle superfici dei canali](#edit-channel-surface) e [aggiorna stati](#update-statuses).

1. Accedi all&#39;elenco delle superfici del canale.

1. Per la superficie attiva selezionata, fai clic sul pulsante **[!UICONTROL Altre azioni]** pulsante .

1. Seleziona **[!UICONTROL Disattiva]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Le superfici del canale disattivate non possono essere eliminate per evitare problemi nei percorsi che utilizzano queste superfici per inviare messaggi.

Non è possibile modificare direttamente una superficie del canale disattivata. Tuttavia, puoi duplicarla e modificare la copia per creare una nuova versione da utilizzare per creare nuovi messaggi. È inoltre possibile attivarlo nuovamente e attendere che l&#39;aggiornamento abbia esito positivo per modificarlo.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
