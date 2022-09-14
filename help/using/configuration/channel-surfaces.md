---
title: Impostare le superfici di canale
description: Scopri come configurare e monitorare le superfici dei canali
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# Impostare le superfici di canale {#set-up-channel-surfaces}

Con [!DNL Journey Optimizer], puoi impostare le superfici del canale (ad esempio i predefiniti per messaggi) che definiscono tutti i parametri tecnici necessari per i messaggi: tipo di e-mail, e-mail e nome del mittente, app mobili, configurazione SMS e altro ancora.

>[!CAUTION]
>
> * Per creare, modificare ed eliminare le superfici dei canali, è necessario disporre della [Gestisci superficie canale](../administration/high-low-permissions.md#manage-channel-surface) autorizzazione.
>
> * È necessario eseguire le [Configurazione e-mail](#configure-email-settings), [Configurazione push](../configuration/push-configuration.md) e [Configurazione SMS](../configuration/sms-configuration.md) prima di creare superfici del canale.


Una volta configurate le superfici del canale, potrai selezionarle quando crei messaggi da un percorso.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Creare una superficie del canale {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Impostazioni della superficie del canale"
>abstract="Quando imposti una superficie del canale, seleziona il canale a cui si applica e definisci tutti i parametri tecnici necessari per i messaggi, ad esempio il tipo di e-mail, il sottodominio, il nome del mittente, le app mobili, la configurazione degli SMS e altro ancora."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Impostazioni della superficie del canale"
>abstract="Quando imposti una superficie del canale, seleziona il canale a cui si applica e definisci tutti i parametri tecnici necessari per i messaggi, ad esempio il tipo di e-mail, il nome del mittente, le app mobili, la configurazione degli SMS e altro ancora."

<!--New contextual help content for September release: A channel surface defines all the technical parameters required for your messages (email type, sender name, mobile apps, SMS configuration, etc.): once configured, you will be able to select it when creating actions from a journey or a campaign. Note that you must have the Manage channel surface permission to create, edit and delete channel surfaces.

To create a channel surface, follow these steps:

1. Access the **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** menu, then click **[!UICONTROL Create channel surface]**.

    ![](assets/preset-create.png)

1. Enter a name and a description (optional) for the surface, then select the channel(s) to configure.

    ![](assets/preset-general.png)

    >[!NOTE]
    >
    > Names must begin with a letter (A-Z). It can only contain alpha-numeric characters. You can also use underscore `_`, dot`.` and hyphen `-` characters. 

1. If you selected the **[!UICONTROL Email]** channel, configure your settings as described in [this section](email-settings.md).

    ![](assets/preset-email.png)

1. For the **[!UICONTROL Push Notification]** channel, select at least one platform  -  **iOS** and/or **Android** -, and the mobile applications to use for each platform.

    ![](assets/preset-push.png)
        
    >[!NOTE]
    >
    >For more on how to configure your environment to send push notifications, refer to [this section](push-gs.md).

1. For the **[!UICONTROL SMS]** channel, define your settings as detailed in [this section](sms-configuration.md#message-preset-sms).

    ![](assets/preset-sms.png)

    >[!NOTE]
    >
    >For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the channel surface as draft and resume its configuration later on.

    ![](assets/preset-submit.png)

    >[!NOTE]
    >
    >You cannot proceed with surface creation while the selected IP pool is under [edition](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status), and has never been associated with the selected subdomain. [Learn more](#subdomains-and-ip-pools)
    >
    >Save the surface as draft and wait until the IP pool has the **[!UICONTROL Success]** status to resume surface creation.
    
1. Once the channel surface has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around **48h-72h**, and can take up to **7-10 business days**.

    These checks include configuration and technical tests that are performed by the Adobe team:

    * SPF validation
    * DKIM validation
    * MX record validation
    * Check IPs denylisting
    * Helo host check
    * IP pool verification
    * A/PTR record, t/m/res subdomain verification

    >[!NOTE]
    >
    >If the checks are not successful, learn more on the possible failure reasons in [this section](#monitor-channel-surfaces).  

1. Once the checks are successful, the channel surface gets the **[!UICONTROL Active]** status. It is ready to be used to deliver messages.

    ![](assets/preset-active.png)

## Monitor channel surfaces {#monitor-channel-surfaces}

All your channel surfaces display in the **[!UICONTROL Channels]** > **[!UICONTROL Channel surfaces]** menu. Filters are available to help you browse through the list (channel, user, status).

![](assets/preset-filters.png)

Once created, channel surfaces can have the following statuses:

* **[!UICONTROL Draft]**: The channel surface has been saved as a draft and has not been submitted yet. Open it to resume the configuration.
* **[!UICONTROL Processing]**: The channel surface has been submitted and is going through several verifications steps.
* **[!UICONTROL Active]**: The channel surface has been verified and can be selected to create messages.
* **[!UICONTROL Failed]**: One or several checks have failed during the channel surface verification.
* **[!UICONTROL Deactivated]**: The channel surface is deactivated. It cannot be used to create new messages.

In case a channel surface creation fails, the details on each possible failure reason are described below.

If one of these errors occurs, contact [Adobe Customer Care](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} to get assistance.

* **SPF validation failed**: SPF (Sender Policy Framework) is an email authentication protocol that allows to specify authorized IPs that can send emails from a given subdomain. SPF validation failure means that the IP addresses in the SPF record do not match the IP addresses used for sending emails to the mailbox providers. 

* **DKIM validation failed**: DKIM (DomainKeys Identified Mail) allows the recipient server to verify that the received message was sent by the genuine sender of the associated domain and that the content of the original message was not altered on its way. DKIM validation failure means that the receiving mail servers are unable to verify the authenticity of the message content and its association with the sending domain.:

* **MX record validation failed**: MX (Mail eXchange) record validation failure means that the mail servers responsible for accepting inbound emails on behalf of a given subdomain are not correctly configured.

* **Deliverability configurations failed**: Deliverability configurations failure can happen due to any of the following reasons:
    * Blocklisting of the allocated IPs
    * Invalid `helo` name
    * Emails being sent from IPs other than the ones specified in the IP pool of the corresponding surface
    * Unable to deliver emails to inboxes of major ISPs like Gmail and Yahoo

## Edit a channel surface {#edit-channel-surface}

To edit a channel surface, follow the steps below.

>[!NOTE]
>
>You cannot edit the **[!UICONTROL Push notification settings]**. If a channel surface is only configured for the Push notification channel, it is not editable.

1. From the list, click a channel surface name to open it.

    ![](assets/preset-name.png)

1. Edit its properties as desired.

    >[!NOTE]
    >
    >If a channel surface has the **[!UICONTROL Active]** status, the **[!UICONTROL Name]**, **[!UICONTROL Select channel]** and **[!UICONTROL Subdomain]** fields are greyed out and cannot be edited.

1. Click **[!UICONTROL Submit]** to confirm your changes.

    >[!NOTE]
    >
    >You can also save the channel surface as draft and resume update later on.

Once the changes are submitted, the channel surface will go through a validation cycle similar to the one in place when [creating a channel surface](#create-channel-surface). The edition processing time can take up to **3 hours**.

>[!NOTE]
>
>If you only edit the **[!UICONTROL Description]**, **[!UICONTROL Email type]** and/or **[!UICONTROL Email retry parameters]** fields, the update is instantaneous.

### Update details {#update-details}

For channel surfaces that have the **[!UICONTROL Active]** status, you can check the details of the update. To do so:

Click the **[!UICONTROL Recent update]** icon that is displayed next to the active surface name.

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
