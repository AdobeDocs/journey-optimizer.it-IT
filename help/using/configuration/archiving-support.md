---
solution: Journey Optimizer
product: journey optimizer
title: Supporto per l'archiviazione in Journey Optimizer
description: Scopri come archiviare i messaggi
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: archivio, messaggi, HIPAA, CCN, e-mail
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 8%

---

# Supporto per l’archiviazione {#archiving-support}

## Archiviare i messaggi {#about-archiving}

Normative come l&#39;HIPAA richiedono che [!DNL Journey Optimizer] deve fornire un modo per archiviare i messaggi inviati ai singoli utenti. In effetti, se i clienti presentano una richiesta, devono avere la possibilità di ottenere una copia del messaggio inviato a scopo di verifica.

* Per il canale e-mail, [!DNL Journey Optimizer] fornisce una funzionalità e-mail CCN integrata. [Ulteriori informazioni](#bcc-email)

* Inoltre, per tutti i canali, puoi utilizzare il campo &quot;Modello&quot; nel **Set di dati di entità**, che contiene i dettagli dei modelli di messaggio non personalizzati. Esporta il set di dati con questo campo per salvare metadati quali: chi ha inviato il messaggio, a chi e quando. Tieni presente che i dati personalizzati non vengono esportati, ma solo il modello (formato e struttura del messaggio). [Ulteriori informazioni](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] non dispone del supporto per i requisiti di archiviazione SMS. Per il supporto di archiviazione dedicato, collabora con il fornitore di SMS (Synch o Twilio).

## Come utilizzare Ccn per le e-mail {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Definire un indirizzo e-mail Ccn"
>abstract="Per conservare una copia delle e-mail inviate, puoi includere nell’invio un indirizzo e-mail in Ccn. Immetti l’indirizzo e-mail desiderato in modo che ogni e-mail venga inviata anche in copia per conoscenza nascosta a questo indirizzo Ccn. Il dominio dell’indirizzo Ccn non deve essere lo stesso di un sottodominio delegato ad Adobe. Questa funzione è facoltativa."

Puoi inviare una copia identica (o una copia per conoscenza nascosta) di un’e-mail inviata da [!DNL Journey Optimizer] in una casella in entrata Ccn. Questa funzione opzionale consente di conservare le copie delle comunicazioni e-mail inviate agli utenti per scopi di conformità e/o archiviazione. Questo sarà invisibile ai destinatari della consegna.

### Abilita e-mail Ccn {#enable-bcc}

Per attivare **[!UICONTROL E-mail Ccn]** , immetti l’indirizzo e-mail desiderato nel campo dedicato del [superficie di canale](channel-surfaces.md) (ossia predefinito per messaggi). Puoi specificare qualsiasi indirizzo esterno nel formato corretto, ad eccezione di un indirizzo e-mail definito in un sottodominio delegato ad Adobe. Ad esempio, se hai delegato *marketing.luma.com* sottodominio da Adobe, qualsiasi indirizzo come *abc@marketing.luma.com* è vietato.

>[!CAUTION]
>
>È possibile definire un solo indirizzo e-mail Ccn. Assicurati che l’indirizzo Ccn disponga di una capacità di ricezione sufficiente per memorizzare tutte le e-mail inviate utilizzando la superficie di canale corrente.
>
>Altri consigli sono elencati in [questa sezione](#bcc-recommendations-limitations).

>[!NOTE]
>
>Se hai acquistato il componente aggiuntivo Healthcare Shield, assicurati che l’ISP dell’indirizzo Ccn supporti il protocollo TLS 1.2.

![](assets/preset-bcc.png)

Tutti i messaggi e-mail che utilizzano questa superficie verranno copiati in modo cieco nell&#39;indirizzo e-mail Ccn immesso. Da lì, possono essere elaborati e archiviati utilizzando un sistema esterno.

>[!CAUTION]
>
>L’utilizzo della funzione Ccn verrà conteggiato rispetto al numero di messaggi per i quali disponi della licenza. Pertanto, abilitarla solo nelle superfici utilizzate per le comunicazioni critiche che si desidera archiviare. Verifica la disponibilità di volumi con licenza nel contratto.

L’impostazione dell’indirizzo e-mail Ccn viene immediatamente salvata ed elaborata a livello di superficie. Quando si crea un nuovo messaggio utilizzando questa superficie, l&#39;indirizzo e-mail Ccn viene visualizzato automaticamente.

![](assets/preset-bcc-in-msg.png)

Tuttavia, l’indirizzo Ccn viene selezionato per inviare comunicazioni seguendo la logica descritta [qui](../email/email-settings.md).

### Recommendations e limitazioni {#bcc-recommendations-limitations}

* Per garantire la conformità alla privacy, le e-mail in Ccn devono essere elaborate da un sistema di archiviazione in grado di memorizzare informazioni personali (PII, personally identifiable information) in modo sicuro.

* Poiché i messaggi possono contenere dati sensibili o privati, ad esempio informazioni personali (PII, personally identifiable information), accertati che l’indirizzo Ccn sia corretto e che l’accesso ai messaggi sia sicuro.

* La casella in entrata utilizzata per il campo Ccn deve essere gestita correttamente per quanto riguarda lo spazio e la consegna. Se la casella in entrata restituisce mancati recapiti, alcuni messaggi e-mail potrebbero non essere ricevuti e pertanto non verranno archiviati.

* I messaggi possono essere recapitati all’indirizzo e-mail Ccn prima dei destinatari target. I messaggi Ccn possono essere inviati anche se i messaggi originali [non recapitato](../reports/suppression-list.md#delivery-failures).

  <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Non aprire o scorrere le e-mail inviate all’indirizzo Ccn, in quanto vengono prese in considerazione nel totale delle aperture e dei clic dall’analisi di invio, il che potrebbe causare alcuni errori di calcolo in [rapporti](../reports/global-report.md).

* Non contrassegnare i messaggi come spam nella casella in entrata Ccn, in quanto influirà su tutte le altre e-mail inviate a questo indirizzo.

>[!CAUTION]
>
>Non fare clic sul collegamento per annullare l’abbonamento nelle e-mail inviate all’indirizzo in Ccn, in quanto l’abbonamento dei destinatari corrispondenti verrà immediatamente annullato.

### Conformità al RGPD {#gdpr-compliance}

Regolamenti come il RGPD stabiliscono che gli interessati devono essere in grado di modificare il loro consenso in qualsiasi momento. Poiché le e-mail in Ccn che stai inviando con Journey Optimizer includono informazioni personali (PII) protette, devi modificare i **[!UICONTROL Schema evento feedback CJM e-mail CCN]** essere in grado di gestire queste informazioni PII in conformità al RGPD e a normative simili.

Per farlo, segui la procedura indicata di seguito.

1. Vai a **[!UICONTROL Gestione dei dati]** > **[!UICONTROL Schemi]** > **[!UICONTROL Sfoglia]** e seleziona **[!UICONTROL Schema evento feedback CJM e-mail CCN]**.

   ![](assets/preset-bcc-schema.png)

1. Fai clic per espandere **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** allora **[!UICONTROL secondaryRecipientDetail]**.

1. Seleziona **[!UICONTROL originalRecipientAddress]**.

1. In **[!UICONTROL Proprietà campo]** a destra, scorri verso il basso fino al **[!UICONTROL Identità]** casella di controllo.

1. Selezionala e seleziona anche **[!UICONTROL Identità primaria]**.

1. Seleziona uno spazio dei nomi dall’elenco a discesa.

   ![](assets/preset-bcc-schema-identity.png)

1. Clic **[!UICONTROL Applica]**.

>[!NOTE]
>
>Per ulteriori informazioni sulla gestione della privacy e sulle normative applicabili, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=it){target="_blank"}.

### Dati di reporting Ccn {#bcc-reporting}

La generazione di rapporti in quanto tale in Ccn non è disponibile nei rapporti percorso e messaggio. Tuttavia, le informazioni vengono memorizzate in un set di dati di sistema denominato **[!UICONTROL Set di dati evento feedback Ccn AJO]**. Puoi eseguire query su questo set di dati per trovare informazioni utili, ad esempio a scopo di debug.

Puoi accedere a questo set di dati tramite l’interfaccia utente. Seleziona **[!UICONTROL Gestione dei dati]** > **[!UICONTROL Set di dati]** > **[!UICONTROL Sfoglia]** e abilita **[!UICONTROL Mostra set di dati di sistema]** attiva dal filtro per visualizzare i set di dati generati dal sistema. Scopri come accedere ai set di dati in [questa sezione](../data/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

Per eseguire query su questo set di dati, puoi utilizzare l’Editor query fornito da [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. Per accedervi, seleziona **[!UICONTROL Gestione dei dati]** > **[!UICONTROL Query]** e fai clic su **[!UICONTROL Crea query]**. [Ulteriori informazioni](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

A seconda delle informazioni che stai cercando, puoi eseguire le seguenti query.

1. Per tutte le altre query seguenti, è necessario l’ID azione di percorso. Esegui questa query per recuperare tutti gli ID azione associati a un particolare ID versione percorso negli ultimi 2 giorni:

   ```
   SELECT
   DISTINCT
   CAST(TIMESTAMP AS DATE) AS EventTime,
   _experience.journeyOrchestration.stepEvents.journeyVersionID,
   _experience.journeyOrchestration.stepEvents.actionName, 
   _experience.journeyOrchestration.stepEvents.actionID 
   FROM journey_step_events 
   WHERE 
   _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND 
   _experience.journeyOrchestration.stepEvents.actionID is not NULL AND 
   TIMESTAMP > NOW() - INTERVAL '2' DAY 
   ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >Per ottenere `<journey version id>`, seleziona il parametro corrispondente [Versione percorso](../building-journeys/journey.md#journey-versions) dal **[!UICONTROL Gestione dei percorsi]** > **[!UICONTROL Percorsi]** menu. L’ID della versione del percorso viene visualizzato alla fine dell’URL visualizzato nel browser web.
   >
   >![](assets/preset-bcc-action-id.png)

1. Esegui questa query per recuperare tutti gli eventi di feedback dei messaggi (in particolare lo stato di feedback) generati per un particolare messaggio destinato a un utente specifico negli ultimi 2 giorni:

   ```
   SELECT  
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       WHEN 'sent' THEN 'Sent'
       WHEN 'delay' THEN 'Retry'
       WHEN 'out_of_band' THEN 'Bounce' 
       WHEN 'bounce' THEN 'Bounce'
   END AS FeedbackStatusCategory
   FROM cjm_message_feedback_event_dataset 
   WHERE  
       timestamp > now() - INTERVAL '2' day  AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
       _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND  
       _experience.customerJourneyManagement.emailChannelContext.address = '<recipient email address>'
       ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >Per ottenere `<journey action id>` , eseguire la prima query descritta in precedenza utilizzando l&#39;id versione percorso. Il `<recipient email address>` Il parametro è l’indirizzo e-mail del destinatario effettivo o di destinazione.

1. Esegui questa query per recuperare tutti gli eventi di feedback dei messaggi Ccn generati per un particolare messaggio destinato a un utente specifico negli ultimi 2 giorni:

   ```
   SELECT   
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
               WHEN 'sent' THEN 'Sent'
               WHEN 'delay' THEN 'Retry'
               WHEN 'out_of_band' THEN 'Bounce' 
               WHEN 'bounce' THEN 'Bounce'
           END AS FeedbackStatusCategory 
   FROM ajo_bcc_feedback_event_dataset  
   WHERE  
   timestamp > now() - INTERVAL '2' day  AND
   _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
   ORDER BY EventTime DESC;
   ```

1. Esegui questa query per recuperare tutti gli indirizzi dei destinatari che non hanno ricevuto il messaggio mentre la relativa voce Ccn esiste negli ultimi 30 giorni:

   ```
    SELECT
        DISTINCT 
    bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
    FROM ajo_bcc_feedback_event_dataset bcc
    LEFT JOIN cjm_message_feedback_event_dataset mfe
    ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
            mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
    WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
   ```
