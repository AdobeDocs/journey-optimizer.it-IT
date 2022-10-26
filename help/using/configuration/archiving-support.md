---
solution: Journey Optimizer
product: journey optimizer
title: Supporto per l'archiviazione in Journey Optimizer
description: Scopri come archiviare i messaggi
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 3%

---

# Supporto per l’archiviazione {#archiving-support}

## Come archiviare i messaggi {#about-archiving}

Regolamenti come l&#39;HIPAA richiedono che [!DNL Journey Optimizer] dovrebbe fornire un modo per archiviare i messaggi inviati a singoli utenti. Infatti, se i clienti sollevano un reclamo, dovrebbero avere la possibilità di ottenere una copia del messaggio inviato a scopo di verifica.

* Per il canale e-mail, [!DNL Journey Optimizer] fornisce una funzionalità e-mail CCN integrata. [Ulteriori informazioni](#bcc-email)

* Inoltre, per tutti i canali, puoi utilizzare il campo &quot;Modello&quot; nella sezione **Set di dati di entità**, che contiene i dettagli dei modelli di messaggio non personalizzati. Esporta il set di dati con questo campo per salvare metadati quali: che ha inviato il messaggio, a chi e quando. I dati personalizzati non vengono esportati, viene preso in considerazione solo il modello (formato e struttura del messaggio). [Ulteriori informazioni](../start/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] non possiede il supporto per i requisiti di archiviazione SMS. Per un supporto di archiviazione dedicato, collabora con il tuo fornitore SMS (Synch o Twilio).

## Come utilizzare CCN per le e-mail {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Definire un indirizzo e-mail CCN"
>abstract="Puoi conservare una copia delle e-mail inviate inviandole a una casella in entrata CCN. Inserisci l’indirizzo e-mail desiderato in modo che ogni e-mail inviata venga copiata in modalità cieca in questo indirizzo CCN. Il dominio dell’indirizzo CCN non deve essere lo stesso di qualsiasi sottodominio delegato ad Adobe. Questa funzione è facoltativa."

Puoi inviare una copia identica (o copia cieca in carbonio) di un’e-mail inviata da [!DNL Journey Optimizer] a una casella in entrata CCN. Questa funzione opzionale ti consente di conservare copie delle comunicazioni e-mail inviate agli utenti per scopi di conformità e/o archiviazione. Questo sarà invisibile ai destinatari della consegna.

### Abilita e-mail CCN {#enable-bcc}

Per abilitare **[!UICONTROL E-mail CCN]** inserisci l’indirizzo e-mail desiderato nel campo dedicato della [superficie del canale](channel-surfaces.md) (ovvero predefinito per i messaggi). Puoi specificare qualsiasi indirizzo esterno nel formato corretto, ad eccezione di un indirizzo e-mail definito in un sottodominio delegato ad Adobe. Ad esempio, se hai delegato il *marketing.luma.com* sottodominio ad Adobe, qualsiasi indirizzo come *abc@marketing.luma.com* è vietato.

>[!CAUTION]
>
>Puoi definire un solo indirizzo e-mail CCN. Assicurati che l’indirizzo CCN abbia una capacità di ricezione sufficiente per memorizzare tutte le e-mail inviate utilizzando la superficie del canale corrente.
>
>Ulteriori raccomandazioni sono elencate in [questa sezione](#bcc-recommendations-limitations).

>[!NOTE]
>
>Se hai acquistato l’offerta del componente aggiuntivo Healthcare Shield, devi assicurarti che l’ISP dell’indirizzo CCN supporti il protocollo TLS 1.2.

![](assets/preset-bcc.png)

Tutti i messaggi e-mail che utilizzano questa superficie verranno copiati in modalità cieca nell’indirizzo e-mail CCN inserito. Da lì, possono essere elaborati e archiviati utilizzando un sistema esterno.

>[!CAUTION]
>
>L’utilizzo delle funzioni CCN verrà conteggiato in base al numero di messaggi per i quali si dispone della licenza. Quindi, abilitalo solo nelle superfici utilizzate per le comunicazioni critiche che desideri archiviare. Controlla il tuo contratto per i volumi con licenza.

L’impostazione dell’indirizzo e-mail CCN viene immediatamente salvata ed elaborata a livello di superficie. Quando [creare un nuovo messaggio](../messages/get-started-content.md) utilizzando questa superficie, l’indirizzo e-mail CCN viene visualizzato automaticamente.

![](assets/preset-bcc-in-msg.png)

Tuttavia, l’indirizzo CCN viene selezionato per l’invio di comunicazioni secondo la logica seguente:

* Per i percorsi batch e burst, non si applica all&#39;esecuzione batch o burst che era già iniziato prima dell&#39;impostazione CCN. La modifica verrà rilevata alla ricorrenza successiva o alla nuova esecuzione.

* Per i messaggi transazionali, la modifica viene selezionata immediatamente per la comunicazione successiva (fino a un minuto di ritardo).

>[!NOTE]
>
>Non è necessario ripubblicare il percorso per selezionare l’impostazione CCN.

### Recommendations e limitazioni {#bcc-recommendations-limitations}

* Per garantire la conformità ai requisiti di privacy, le e-mail CCN devono essere elaborate da un sistema di archiviazione in grado di memorizzare informazioni personali (PII) sicure.

* Poiché i messaggi possono contenere dati riservati o privati, ad esempio informazioni personali identificabili (PII), assicurati che l’indirizzo CCN sia corretto e proteggi l’accesso ai messaggi.

* La casella in entrata utilizzata per CCN deve essere gestita correttamente per lo spazio e la consegna. Se la casella in entrata restituisce messaggi non recapitati, è possibile che alcune e-mail non vengano ricevute e quindi che non vengano archiviate.

* I messaggi possono essere inviati all’indirizzo e-mail CCN prima dei destinatari. I messaggi CCN possono anche essere inviati anche se i messaggi originali possono avere [rimbalzato](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Non aprire o fare clic sulle e-mail inviate all’indirizzo CCN in quanto vengono prese in considerazione nelle aperture totali e nei clic dall’analisi di invio, il che potrebbe causare alcuni calcoli errati in [rapporti](../reports/global-report.md).

* Non contrassegnare i messaggi come spam nella casella in entrata CCN, in quanto avranno effetto su tutte le altre e-mail inviate a questo indirizzo.


>[!CAUTION]
>
>Non fare clic sul collegamento di annullamento dell’abbonamento nelle e-mail inviate all’indirizzo CCN, in quanto cancellerai immediatamente l’abbonamento ai destinatari corrispondenti.

### Conformità ai requisiti RGPD {#gdpr-compliance}

Regolamenti come il RGPD stabiliscono che gli interessati devono poter modificare il loro consenso in qualsiasi momento. Poiché le e-mail CCN che invii con Journey Optimizer includono informazioni personali (PII, Security Personally Identifiable Information), devi modificare il **[!UICONTROL Schema evento feedback CCN di CJM E-mail]** essere in grado di gestire questi PII in conformità con il RGPD e con normative simili.

Per farlo, segui la procedura indicata di seguito.

1. Vai a **[!UICONTROL Gestione dati]** > **[!UICONTROL Schemi]** > **[!UICONTROL Sfoglia]** e seleziona **[!UICONTROL Schema evento feedback CCN di CJM E-mail]**.

   ![](assets/preset-bcc-schema.png)

1. Fare clic per espandere **[!UICONTROL _esperienza]**, **[!UICONTROL customerJourneyManagement]** then **[!UICONTROL secondarioRecipientDetail]**.

1. Seleziona **[!UICONTROL originalRecipientAddress]**.

1. In **[!UICONTROL Proprietà campo]** a destra, scorri verso il basso fino al **[!UICONTROL Identità]** casella di controllo.

1. Selezionalo e seleziona anche **[!UICONTROL Identità principale]**.

1. Seleziona uno spazio dei nomi dall’elenco a discesa.

   ![](assets/preset-bcc-schema-identity.png)

1. Fai clic su **[!UICONTROL Applica]**.

>[!NOTE]
>
>Per ulteriori informazioni sulla gestione della privacy e sulle normative applicabili, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=it){target=&quot;_blank&quot;}.

### Dati di reporting per CCN {#bcc-reporting}

La generazione di rapporti in quanto tale su CCN non è disponibile nei rapporti sul percorso e sui messaggi. Tuttavia, le informazioni vengono memorizzate in un set di dati di sistema denominato **[!UICONTROL Set di dati evento feedback CCN AJO]**. È possibile eseguire query su questo set di dati per trovare informazioni utili, ad esempio, a scopo di debug.

Puoi accedere a questo set di dati tramite l’interfaccia utente di . Seleziona **[!UICONTROL Gestione dati]** > **[!UICONTROL Set di dati]** > **[!UICONTROL Sfoglia]** e **[!UICONTROL Mostra set di dati di sistema]** attiva/disattiva il filtro per visualizzare i set di dati generati dal sistema. Ulteriori informazioni su come accedere ai set di dati in [questa sezione](../start/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

Per eseguire query su questo set di dati, puoi utilizzare l’Editor query fornito da [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}. Per accedervi, seleziona **[!UICONTROL Gestione dati]** > **[!UICONTROL Query]** e fai clic su **[!UICONTROL Crea query]**. [Ulteriori informazioni](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

A seconda delle informazioni che stai cercando, puoi eseguire le seguenti query.

1. Per tutte le altre query riportate di seguito, è necessario l’ID azione percorso. Esegui questa query per recuperare tutti gli ID azione associati a un particolare ID di versione del percorso negli ultimi 2 giorni:

       &quot;
       SELEZIONA
       DISTINTO
       CAST(TIMESTAMP AS DATE) AS EventTime,
       _experience.journeyOrchestration.stepEvents.journeyVersionID,
       _experience.journeyOrchestration.stepEvents.actionName,
       _experience.journeyOrchestration.stepEvents.actionID
       FROM percorso_step_events
       DOVE
       _experience.journeyOrchestration.stepEvents.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; E
       _experience.journeyOrchestration.stepEvents.actionID non è NULL AND
       TIMESTAMP > NOW() - INTERVALLO &#39;2&#39; GIORNO
       ORDER BY EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >Per ottenere `<journey version id>`, seleziona il corrispondente [Versione percorso](../building-journeys/journey-versions.md) dal **[!UICONTROL Gestione dei percorsi]** > **[!UICONTROL Percorsi]** menu. L’ID della versione del percorso viene visualizzato alla fine dell’URL visualizzato nel browser web.
   >
   >![](assets/preset-bcc-action-id.png)

1. Esegui questa query per recuperare tutti gli eventi di feedback dei messaggi (in particolare lo stato di feedback) generati per un particolare messaggio destinato a un utente specifico negli ultimi 2 giorni:

       &quot;
       SELEZIONA
       _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
       _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID,
       timestamp AS EventTime,
       _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
       _experience.customervarineymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
       CASE _experience.customervarineymanagement.messagedeliveryfeedback.feedbackStatus
       QUANDO &#39;inviato&#39; ALLORA &#39;Inviato&#39;
       QUANDO &#39;delay&#39; ALLORA &#39;Retry&#39;
       QUANDO &#39;out_of_band&#39; THEN &#39;Bounce&#39;
       QUANDO &#39;rimbalzo&#39; ALLORA &#39;rimbalzo&#39;
       END AS FeedbackStatusCategory
       FROM cjm_message_feedback_event_dataset
       DOVE
       timestamp > now() - INTERVAL &#39;2&#39; day AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; E
       _experience.customerJourneyManagement.messageExecution.journeyActionID = &#39;&lt;journey action=&quot;&quot; id=&quot;&quot;>&#39; E
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email=&quot;&quot; address=&quot;&quot;>&#39;
       ORDER BY EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >Per ottenere `<journey action id>` , esegui la prima query descritta sopra utilizzando l&#39;ID versione percorso. La `<recipient email address>` è l&#39;indirizzo e-mail del destinatario di destinazione o effettivo.

1. Esegui questa query per recuperare tutti gli eventi di feedback dei messaggi CCN generati per un particolare messaggio destinato a un utente specifico negli ultimi 2 giorni:

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

1. Esegui questa query per recuperare tutti gli indirizzi dei destinatari che non hanno ricevuto il messaggio, mentre la relativa voce CCN esiste negli ultimi 30 giorni:

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
