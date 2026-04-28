---
solution: Journey Optimizer
product: journey optimizer
title: Set up an allowed list
description: Learn how to set up and manage an allowed list in Journey Optimizer to restrict email sending to trusted addresses and domains at the sandbox level.
feature: Deliverability
role: Admin
level: Intermediate
keywords: allowed list, safe list, email, deliverability, sandbox, domains, suppression, configuration
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 12%

---

# Set up an allowed list {#allow-list}

The allowed list is a sending-safe list you can define at the [sandbox](../administration/sandboxes.md) level. It restricts email sending to specific addresses or domains, ensuring that only explicitly listed recipients can receive messages from a given sandbox.

>[!CAUTION]
>
>This feature only applies to the email channel. It is available on production and non-production sandboxes.

On non-production sandboxes, where accidental sends can occur, the allowed list prevents unwanted messages from reaching real customer addresses, providing a secure environment for testing purposes.

When the allowed list is active but empty, no emails are sent. This makes it a useful emergency brake: if a critical issue arises, you can activate an empty allowed list to halt all outgoing communications from [!DNL Journey Optimizer] until the problem is resolved. Learn more about the [allowed list logic](#logic).

You can also use the Journey Optimizer **Suppression REST API** to manage outgoing messages programmatically through suppression and allow lists. [Scopri come utilizzare l’API REST di soppressione](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"}

## Access the allowed list {#access-allowed-list}

To access the detailed list of allowed email addresses and domains, go to **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]**, and select **[!UICONTROL Allowed list]**.

![Allowed list page showing the list of allowed email addresses and domains](assets/allow-list-access.png)

>[!CAUTION]
>
>Permissions to view, export and manage the allowed list are restricted to [Journey Administrators](../administration/ootb-product-profiles.md#journey-administrator). Learn more about managing [!DNL Journey Optimizer] users&#39; access rights in [this section](../administration/permissions-overview.md).

To export the allowed list as a CSV file, select the **[!UICONTROL Download CSV]** button.

Use the **[!UICONTROL Delete]** button to permanently remove an entry.

You can search on the email addresses or domains, and filter on the **[!UICONTROL Address type]**. Once selected, you can clear the filter displayed on top of the list.

![Allowed list filtered by address type](assets/allowed-list-filtering-example.png)

## Activate the allowed list {#enable-allow-list}

To activate the allowed list, follow the steps below.

1. Access the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** menu.

1. Select the toggle button.

   ![Toggle button to activate the allowed list](assets/allow-list-edit.png)

1. Select **[!UICONTROL Activate allowed list]**. The allowed list is now active.

   ![Confirmation that the allowed list is now active](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >* After activation, there is a 10-minute delay before the allowed list takes effect in journeys and campaigns. Updates to both the allowed list and suppression list can also take up to 10 minutes to reflect.
   >* When active, the allowed list is enforced not only in live journeys, but also when testing messages with [proofs](../content-management/proofs.md) and journeys in [test mode](../building-journeys/testing-the-journey.md).

The allowed list logic applies when the feature is active. Ulteriori informazioni in [questa sezione](#logic).

## Deactivate the allowed list {#deactivate-allow-list}

To deactivate the allowed list, follow the steps below.

1. Access the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** menu.

1. Select the toggle button.

   ![Toggle button to deactivate the allowed list](assets/allow-list-edit-active.png)

1. Select **[!UICONTROL Deactivate allowed list]**. The allowed list is no longer active.

   ![Confirmation that the allowed list is now inactive](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >After you deactivate the allowed list, there is a 10-minute delay before it takes effect in your journeys and campaigns. Similarly, updates to both the allowed list and suppression list can take up to 10 minutes to reflect.

The allowed list logic does not apply when the feature is deactivated. Ulteriori informazioni in [questa sezione](#logic).

## Aggiungere entità all’elenco Consentiti {#add-entities}

Per aggiungere nuovi indirizzi e-mail o domini all&#39;elenco Consentiti per una sandbox specifica, puoi [compilare manualmente l&#39;elenco](#manually-populate-list) o utilizzare una [chiamata API](#api-call-allowed-list).

>[!NOTE]
>
>L’elenco Consentiti può contenere fino a 1.000 voci.

### Compila manualmente l’elenco Consentiti {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="Aggiungere indirizzi o domini all’elenco Consentiti"
>abstract="Puoi aggiungere manualmente nuovi indirizzi e-mail o domini all’elenco Consentiti selezionandoli uno per uno."

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="Aggiungere indirizzi o domini all’elenco Consentiti"
>abstract="Puoi aggiungere manualmente nuovi indirizzi e-mail o domini all’elenco Consentiti selezionandoli uno per uno."

È possibile popolare manualmente l&#39;elenco Consentiti [!DNL Journey Optimizer] aggiungendo un indirizzo e-mail o un dominio tramite l&#39;interfaccia utente.

>[!NOTE]
>
>Puoi aggiungere un solo indirizzo e-mail o dominio alla volta.

Per farlo, segui la procedura indicata di seguito.

1. Selezionare il pulsante **[!UICONTROL Aggiungi e-mail o dominio]**.

   ![Pulsante Aggiungi e-mail o dominio nella pagina di elenco Consentiti](assets/allowed-list-add-email.png)

1. Scegli il tipo di indirizzo: **[!UICONTROL Indirizzo e-mail]** o **[!UICONTROL Indirizzo di dominio]**.

1. Immetti l’indirizzo e-mail o il dominio a cui desideri inviare le e-mail.

   >[!NOTE]
   >
   >Assicurati di inserire un indirizzo e-mail valido (ad esempio abc@company.com) o un dominio (ad esempio abc.company.com).

1. Se necessario, specifica un motivo.

   ![Modulo per aggiungere un indirizzo e-mail o un dominio all&#39;elenco Consentiti, con un campo motivo facoltativo](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >Tutti i caratteri ASCII compresi tra 32 e 126 sono consentiti nel campo **[!UICONTROL Reason]**. L’elenco completo è disponibile su [questa pagina](https://en.wikipedia.org/wiki/ASCII#Printable_characters){target="_blank"} di esempio.

1. Fai clic su **[!UICONTROL Invia]**.

### Aggiungere entità utilizzando una chiamata API {#api-call-allowed-list}

Per popolare l’elenco Consentiti, puoi anche chiamare l’API di soppressione con il valore `ALLOWED` per l’attributo `listType`. Ad esempio:

![Chiamata API di esempio per aggiungere una voce all&#39;elenco Consentiti utilizzando l&#39;API di soppressione](assets/allow-list-api.png)

Puoi eseguire le operazioni **Aggiungi**, **Elimina** e **Ottieni**.

Per ulteriori informazioni sull&#39;esecuzione di chiamate API, consulta la documentazione di riferimento sulle [API Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=it){target="_blank"}.

## Scarica l’elenco Consentiti {#download-allowed-list}

Per esportare l’elenco Consentiti come file CSV, effettua le seguenti operazioni:

1. Selezionare il pulsante **[!UICONTROL Scarica CSV]**.

   ![Pulsante Scarica CSV nella pagina di elenco Consentiti](assets/allowed-list-download-csv.png)

1. Attendi che il file venga generato.

   ![Notifica che indica che il file CSV è in fase di generazione](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >Il tempo di download dipende dalla dimensione del file, ovvero dal numero di indirizzi presenti nell’elenco Consentiti.
   >
   >È possibile elaborare una richiesta di download alla volta per una determinata sandbox.

1. Una volta generato il file, riceverai una notifica. Fai clic sull’icona a forma di campana in alto a destra dello schermo per visualizzarla.

1. Fai clic sulla notifica stessa per scaricare il file.

   ![Notifica con un collegamento di download per il file CSV generato](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >Il collegamento è valido per 24 ore.

## Logica dell’elenco Consentiti {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="Gestire l’elenco Consentiti"
>abstract="Quando l’elenco Consentiti viene attivato, solo i destinatari inclusi nell’elenco Consentiti riceveranno messaggi e-mail da questa sandbox. Quando è disattivato, tutti i destinatari riceveranno le e-mail."

Quando l&#39;elenco Consentiti è [attivo](#enable-allow-list), si applica la logica seguente:

* Se l&#39;elenco Consentiti è **vuoto**, non verrà inviata alcuna e-mail.

* Se un&#39;entità è **nell&#39;elenco Consentiti** e non nell&#39;elenco di soppressione, l&#39;e-mail viene inviata ai destinatari corrispondenti. Tuttavia, se l&#39;entità è presente anche nell&#39;[elenco di soppressione](../reports/suppression-list.md), i destinatari corrispondenti non riceveranno l&#39;e-mail, per il motivo **[!UICONTROL Eliminato]**.

* Se un&#39;entità è **non presente nell&#39;elenco Consentiti** (e non nell&#39;elenco di soppressione), i destinatari corrispondenti non riceveranno l&#39;e-mail. Motivo: **[!UICONTROL Non consentito]**.

>[!NOTE]
>
>I profili con stato **[!UICONTROL Non consentito]** sono esclusi durante il processo di invio dei messaggi. Pertanto, mentre nei **report Percorso** questi profili vengono visualizzati come spostati nel percorso ([Attività Read Audience](../building-journeys/read-audience.md) e [attività messaggio](../building-journeys/journey-action.md)), i **report e-mail** non li includono nelle metriche **[!UICONTROL Inviati]** in quanto vengono filtrati prima dell&#39;invio di e-mail.
>
>Ulteriori informazioni sul [report live](../reports/live-report.md) e sul [report Customer Journey Analytics](../reports/report-gs-cja.md).

Quando l&#39;elenco Consentiti è [disattivato](#deactivate-allow-list), tutte le e-mail che invii dalla sandbox corrente vengono inviate a tutti i destinatari (purché non siano inclusi nell&#39;elenco di soppressione), inclusi gli indirizzi dei clienti reali.

## Generazione di rapporti di esclusione {#reporting}

Quando l’elenco Consentiti è attivo, puoi recuperare gli indirizzi e-mail o i domini esclusi da un invio perché non erano presenti nell’elenco Consentiti. A tale scopo, è possibile utilizzare [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=it){target="_blank"} per effettuare le seguenti chiamate API.

Per ottenere il **numero di e-mail** non inviate perché i destinatari non erano inclusi nell&#39;elenco Consentiti, utilizzare la query seguente:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Per ottenere l&#39;**elenco di indirizzi di posta elettronica** non inviati perché i destinatari non erano inclusi nell&#39;elenco Consentiti, utilizzare la query seguente:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
