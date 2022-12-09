---
solution: Journey Optimizer
product: journey optimizer
title: Elenco consentito
description: Scopri come utilizzare l’elenco Consentiti
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 0%

---

# Elenco consentito {#allow-list}

È possibile definire un elenco di invio sicuro specifico nella [sandbox](../administration/sandboxes.md) livello.

Questo elenco di indirizzi e-mail consentiti ti consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica.

>[!NOTE]
>
>Questa funzione è disponibile nelle sandbox di produzione e non di produzione.

Ad esempio, in un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti assicura di non rischiare di inviare messaggi indesiderati agli indirizzi reali del cliente e fornisce quindi un ambiente protetto a scopo di test.

Inoltre, quando l’elenco consentito è attivo ma vuoto, non verrà inviata alcuna posta. Quindi, se incontri qualche problema importante, puoi utilizzare questa funzione per interrompere tutte le comunicazioni in uscita da [!DNL Journey Optimizer] finché non risolvi il problema. Per saperne di più sul [logica di elenco consentita](#logic).

>[!CAUTION]
>
>Questa funzione si applica solo al canale e-mail.

## Accedere all’elenco Consentiti {#access-allowed-list}

Per accedere all’elenco dettagliato degli indirizzi e-mail e dei domini consentiti, vai a **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]**, quindi seleziona **[!UICONTROL Allowed list]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>Le autorizzazioni per visualizzare, esportare e gestire l’elenco consentito sono limitate a [Amministratori del percorso](../administration/ootb-product-profiles.md#journey-administrator). Ulteriori informazioni sulla gestione [!DNL Journey Optimizer] diritti di accesso degli utenti in [questa sezione](../administration/permissions-overview.md).

Per esportare l’elenco Consentiti come file CSV, seleziona la **[!UICONTROL Download CSV]** pulsante .

Utilizza la **[!UICONTROL Delete]** per rimuovere definitivamente una voce.

Puoi cercare gli indirizzi e-mail o i domini e filtrare i **[!UICONTROL Address type]**. Una volta selezionato, puoi cancellare il filtro visualizzato in alto nell’elenco.

![](assets/allowed-list-filtering-example.png)

## Attiva l&#39;elenco consentito {#enable-allow-list}

Per attivare l’elenco Consentiti, segui i passaggi riportati di seguito.

1. Accedere al  **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** menu.

1. Seleziona il pulsante di attivazione/disattivazione.

   ![](assets/allow-list-edit.png)

1. Seleziona **[!UICONTROL Activate allowed list]**. L&#39;elenco consentito è ora attivo.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >Dopo aver attivato l’elenco Consentiti, è disponibile una latenza di 5 minuti affinché diventi effettiva nei percorsi e nelle campagne.

La logica di elenco consentita si applica quando la funzione è attiva. Ulteriori informazioni in [questa sezione](#logic).

>[!NOTE]
>
>Quando attivata, la funzione di elenco consentita viene rispettata durante l’esecuzione dei percorsi, ma anche durante il test dei messaggi con [bozze](../email/preview.md#send-proofs) e il test dei percorsi utilizzando [modalità di prova](../building-journeys/testing-the-journey.md).

## Disattivare l’elenco Consentiti {#deactivate-allow-list}

Per disattivare l’elenco Consentiti, effettua le seguenti operazioni.

1. Accedere al  **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** menu.

1. Seleziona il pulsante di attivazione/disattivazione.

   ![](assets/allow-list-edit-active.png)

1. Seleziona **[!UICONTROL Deactivate allowed list]**. L&#39;elenco consentito non è più attivo.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >Dopo aver disattivato l’elenco consentiti, la latenza effettiva nell’elenco è di 5 minuti nei percorsi e nelle campagne.

La logica di elenco consentita non si applica quando la funzione è disattivata. Ulteriori informazioni in [questa sezione](#logic).

## Aggiungi entità all’elenco Consentiti {#add-entities}

Per aggiungere nuovi indirizzi e-mail o domini all’elenco dei consentiti per una sandbox specifica, puoi effettuare le seguenti operazioni: [compilare manualmente l’elenco](#manually-populate-list)o utilizzare un [Chiamata API](#api-call-allowed-list).

>[!NOTE]
>
>L’elenco consentito può contenere fino a 1.000 voci.

### Compilazione manuale dell’elenco consentito {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="Aggiungi indirizzi o domini all’elenco Consentiti"
>abstract="Puoi aggiungere manualmente nuovi indirizzi e-mail o domini all’elenco Consentiti selezionandoli uno per uno."

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="Aggiungi indirizzi o domini all’elenco Consentiti"
>abstract="Puoi aggiungere manualmente nuovi indirizzi e-mail o domini all’elenco Consentiti selezionandoli uno per uno."

È possibile compilare manualmente i [!DNL Journey Optimizer] elenco Consentiti aggiungendo un indirizzo e-mail o un dominio tramite l’interfaccia utente.

>[!NOTE]
>
>Puoi aggiungere un solo indirizzo e-mail o dominio alla volta.

A questo scopo, segui i passaggi seguenti.

1. Seleziona la **[!UICONTROL Add email or domain]** pulsante .

   ![](assets/allowed-list-add-email.png)

1. Scegli il tipo di indirizzo: **[!UICONTROL Email address]** o **[!UICONTROL Domain address]**.

1. Immetti l’indirizzo e-mail o il dominio a cui desideri inviare le e-mail.

   >[!NOTE]
   >
   >Assicurati di inserire un indirizzo e-mail valido (ad esempio abc@company.com) o un dominio (ad esempio abc.company.com).

1. Se necessario, specifica un motivo.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >Tutti i caratteri ASCII compresi tra 32 e 126 sono consentiti nella variabile **[!UICONTROL Reason]** campo . L&#39;elenco completo è disponibile all&#39;indirizzo [questa pagina](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target=&quot;_blank&quot;} per esempio.

1. Fai clic su **[!UICONTROL Submit]**.

### Aggiungere entità utilizzando una chiamata API {#api-call-allowed-list}

Per compilare l’elenco consentito, puoi anche chiamare l’API di soppressione con `ALLOWED` valore per `listType` attributo. Ad esempio:

![](assets/allow-list-api.png)

È possibile eseguire le **Aggiungi**, **Elimina** e **Get** operazioni.

Ulteriori informazioni sull’esecuzione di chiamate API in [API di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html)Documentazione di riferimento di {target=&quot;_blank&quot;}.

## Logica elenco consentita {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="Gestire l’elenco Consentiti"
>abstract="Quando l’elenco Consentiti viene attivato, solo i destinatari inclusi nell’elenco Consentiti riceveranno messaggi e-mail da questa sandbox. Quando è disattivato, tutti i destinatari riceveranno e-mail."

Quando l’elenco è consentito [attivo](#enable-allow-list), si applica la logica seguente:

* Se l’elenco è consentito **vuoto**, non verrà inviata alcuna e-mail.

* Se un’entità è **nell’elenco Consentiti** e non nell’elenco di soppressione, l’e-mail viene inviata ai destinatari corrispondenti. Tuttavia, se l’entità fa parte anche della [elenco a discesa](../reports/suppression-list.md), i destinatari corrispondenti non riceveranno l’e-mail, poiché **[!UICONTROL Suppressed]**.

* Se un’entità è **non nell&#39;elenco consentito** (e non nell’elenco di soppressione), i destinatari corrispondenti non riceveranno l’e-mail, poiché **[!UICONTROL Not allowed]**.

>[!NOTE]
>
>I profili con **[!UICONTROL Not allowed]** lo stato viene escluso durante il processo di invio del messaggio. Pertanto, mentre **Rapporti sul percorso** mostrerà questi profili come spostati nel percorso ([Leggi segmento](../building-journeys/read-segment.md) e [attività messaggio](../building-journeys/journeys-message.md)), **Rapporti e-mail** non li includerà nella **[!UICONTROL Sent]** le metriche vengono filtrate prima dell’invio dell’e-mail.
>
>Per saperne di più sul [Report live](../reports/live-report.md) e [Report globale](../reports/global-report.md).

Quando l’elenco è consentito [disattivato](#deactivate-allow-list), tutte le e-mail che invii dalla sandbox corrente vengono inviate a tutti i destinatari (purché non siano nell’elenco di soppressione), inclusi gli indirizzi effettivi dei clienti.

## Generazione di rapporti di esclusione {#reporting}

Quando l’elenco Consentiti è attivo, puoi recuperare gli indirizzi e-mail o i domini esclusi da un invio perché non erano nell’elenco Consentiti. A questo scopo, puoi utilizzare la funzione [Servizio query di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} per effettuare le chiamate API riportate di seguito.

Per ottenere **numero di e-mail** che non sono stati inviati perché i destinatari non erano nell’elenco consentiti, utilizza la seguente query:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Per ottenere **elenco degli indirizzi e-mail** che non sono stati inviati perché i destinatari non erano nell’elenco consentiti, utilizza la seguente query:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
