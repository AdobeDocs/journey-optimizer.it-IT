---
solution: Journey Optimizer
product: journey optimizer
title: Elenco Consentiti
description: Scopri come utilizzare l’elenco Consentiti
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: elenco Consentiti, elenco, sicuro, configurazione
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 2%

---

# Elenco Consentiti {#allow-list}

È possibile definire un elenco di invio sicuro specifico nella [sandbox](../administration/sandboxes.md) livello.

Questo elenco Consentiti ti consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica.

>[!NOTE]
>
>Questa funzione è disponibile nelle sandbox di produzione e non di produzione.

Ad esempio, in un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti garantisce di non rischiare di inviare messaggi indesiderati agli indirizzi reali del cliente e fornisce quindi un ambiente protetto a scopo di test.

Inoltre, quando l’elenco Consentiti è attivo ma vuoto, non verrà inviata alcuna posta. Quindi, se incontri qualche problema importante, puoi utilizzare questa funzione per interrompere tutte le comunicazioni in uscita da [!DNL Journey Optimizer] finché non risolvi il problema. Per saperne di più sul [Logica elenco Consentiti](#logic).

>[!CAUTION]
>
>Questa funzione si applica solo al canale e-mail.

## Accedere all’elenco Consentiti {#access-allowed-list}

Per accedere all’elenco dettagliato degli indirizzi e-mail e dei domini consentiti, vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Configurazione e-mail]**, quindi seleziona **[!UICONTROL Elenco Consentiti]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>Le autorizzazioni per visualizzare, esportare e gestire l’elenco Consentiti sono limitate a [Amministratori di percorso](../administration/ootb-product-profiles.md#journey-administrator). Ulteriori informazioni sulla gestione [!DNL Journey Optimizer] diritti di accesso degli utenti in [questa sezione](../administration/permissions-overview.md).

Per esportare l’elenco Consentiti come file CSV, seleziona il **[!UICONTROL Scarica CSV]** pulsante .

Utilizza la **[!UICONTROL Elimina]** per rimuovere definitivamente una voce.

Puoi cercare gli indirizzi e-mail o i domini e filtrare i **[!UICONTROL Tipo di indirizzo]**. Una volta selezionato, puoi cancellare il filtro visualizzato in alto nell’elenco.

![](assets/allowed-list-filtering-example.png)

## Attivare l’elenco Consentiti {#enable-allow-list}

Per attivare l’elenco Consentiti, segui i passaggi riportati di seguito.

1. Accedere al  **[!UICONTROL Canali]** > **[!UICONTROL Configurazione e-mail]** > **[!UICONTROL Elenco consentiti]** menu.

1. Seleziona il pulsante di attivazione/disattivazione.

   ![](assets/allow-list-edit.png)

1. Seleziona **[!UICONTROL Attiva elenco Consentiti]**. L&#39;elenco Consentiti è ora attivo.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >Dopo aver attivato l’elenco Consentiti, è disponibile una latenza di 5 minuti affinché diventi effettiva nei percorsi e nelle campagne.

La logica di elenco Consentiti si applica quando la funzione è attiva. Ulteriori informazioni in [questa sezione](#logic).

>[!NOTE]
>
>Quando è attivata, la funzione di elenco Consentiti viene rispettata durante l’esecuzione dei percorsi, ma anche durante il test dei messaggi con [bozze](../email/preview.md#send-proofs) e i percorsi di test che utilizzano [modalità di prova](../building-journeys/testing-the-journey.md).

## Disattiva l’elenco Consentiti {#deactivate-allow-list}

Per disattivare l’elenco Consentiti, segui i passaggi riportati di seguito.

1. Accedere al  **[!UICONTROL Canali]** > **[!UICONTROL Configurazione e-mail]** > **[!UICONTROL Elenco consentiti]** menu.

1. Seleziona il pulsante di attivazione/disattivazione.

   ![](assets/allow-list-edit-active.png)

1. Seleziona **[!UICONTROL Disattiva elenco Consentiti]**. L&#39;elenco Consentiti non è più attivo.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >Dopo aver disattivato l’elenco Consentiti, è disponibile una latenza di 5 minuti affinché diventi effettiva nei percorsi e nelle campagne.

La logica di elenco Consentiti non si applica quando la funzione è disattivata. Ulteriori informazioni in [questa sezione](#logic).

## Aggiungi entità all’elenco Consentiti {#add-entities}

Per aggiungere nuovi indirizzi e-mail o domini all’elenco Consentiti per una sandbox specifica, puoi effettuare le seguenti operazioni: [compilare manualmente l’elenco](#manually-populate-list)o utilizzare un [Chiamata API](#api-call-allowed-list).

>[!NOTE]
>
>L’elenco Consentiti può contenere fino a 1.000 voci.

### Compilare manualmente l’elenco Consentiti {#manually-populate-list}

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

Per farlo, segui la procedura indicata di seguito.

1. Seleziona la **[!UICONTROL Aggiungi e-mail o dominio]** pulsante .

   ![](assets/allowed-list-add-email.png)

1. Scegli il tipo di indirizzo: **[!UICONTROL Indirizzo e-mail]** o **[!UICONTROL Indirizzo di dominio]**.

1. Immetti l’indirizzo e-mail o il dominio a cui desideri inviare le e-mail.

   >[!NOTE]
   >
   >Assicurati di inserire un indirizzo e-mail valido (ad esempio abc@company.com) o un dominio (ad esempio abc.company.com).

1. Se necessario, specifica un motivo.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >Tutti i caratteri ASCII compresi tra 32 e 126 sono consentiti nella variabile **[!UICONTROL Motivo]** campo . L&#39;elenco completo è disponibile all&#39;indirizzo [questa pagina](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"} ad esempio.

1. Fai clic su **[!UICONTROL Invia]**.

### Aggiungere entità utilizzando una chiamata API {#api-call-allowed-list}

Per compilare l’elenco Consentiti, puoi anche chiamare l’API di soppressione con `ALLOWED` valore per `listType` attributo. Ad esempio:

![](assets/allow-list-api.png)

È possibile eseguire le **Aggiungi**, **Elimina** e **Get** operazioni.

Ulteriori informazioni sull’esecuzione di chiamate API in [API di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target="_blank"} documentazione di riferimento.

## Logica Elenco Consentiti {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="Gestire l’elenco Consentiti"
>abstract="Quando l’elenco Consentiti viene attivato, solo i destinatari inclusi nell’elenco Consentiti riceveranno messaggi e-mail da questa sandbox. Quando è disattivato, tutti i destinatari riceveranno e-mail."

Quando l’elenco Consentiti è [attivo](#enable-allow-list), si applica la logica seguente:

* Se l’elenco Consentiti è **vuoto**, non verrà inviata alcuna e-mail.

* Se un’entità è **sull&#39;elenco Consentiti** e non nell’elenco di soppressione, l’e-mail viene inviata ai destinatari corrispondenti. Tuttavia, se l’entità fa parte anche della [elenco a discesa](../reports/suppression-list.md), i destinatari corrispondenti non riceveranno l’e-mail, poiché **[!UICONTROL Soppresso]**.

* Se un’entità è **non sull&#39;elenco Consentiti** (e non nell’elenco di soppressione), i destinatari corrispondenti non riceveranno l’e-mail, poiché **[!UICONTROL Non consentito]**.

>[!NOTE]
>
>I profili con **[!UICONTROL Non consentito]** lo stato viene escluso durante il processo di invio del messaggio. Pertanto, mentre **Rapporti sui percorsi** mostrerà questi profili come spostati nel percorso ([Leggi segmento](../building-journeys/read-segment.md) e [attività messaggio](../building-journeys/journeys-message.md)), **Rapporti e-mail** non li includerà nella **[!UICONTROL Inviato]** le metriche vengono filtrate prima dell’invio dell’e-mail.
>
>Per saperne di più sul [Report live](../reports/live-report.md) e [Report globale](../reports/global-report.md).

Quando l’elenco Consentiti è [disattivato](#deactivate-allow-list), tutte le e-mail che invii dalla sandbox corrente vengono inviate a tutti i destinatari (purché non siano nell’elenco di soppressione), inclusi gli indirizzi effettivi dei clienti.

## Generazione di rapporti di esclusione {#reporting}

Quando l’elenco Consentiti è attivo, puoi recuperare indirizzi e-mail o domini che sono stati esclusi da un invio perché non erano nell’elenco Consentiti. A questo scopo, puoi utilizzare la funzione [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} effettua le chiamate API di seguito.

Per ottenere **numero di e-mail** che non sono stati inviati perché i destinatari non erano nell’elenco Consentiti, utilizza la seguente query:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Per ottenere **elenco degli indirizzi e-mail** che non sono stati inviati perché i destinatari non erano nell’elenco Consentiti, utilizza la seguente query:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
