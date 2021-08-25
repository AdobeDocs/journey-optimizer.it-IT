---
title: Elenco consentiti
description: Scopri come utilizzare l’elenco Consentiti.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 2edb3535c50f83d18ce4d6429a6d76f44b694ac6
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 1%

---

# Elenco Consentiti {#allow-list}

È ora possibile definire un elenco di sicurezza per l’invio specifico a livello di [sandbox](administration/sandboxes.md) per disporre di un ambiente sicuro a scopo di test. In un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti ti assicura di non correre il rischio di inviare messaggi indesiderati ai clienti.

L’elenco Consentiti ti consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica. Questo può impedire l’invio accidentale di e-mail a veri indirizzi dei clienti in un ambiente di test.

>[!CAUTION]
>
>Questa funzione è **non** disponibile nelle sandbox di produzione. Si applica solo al canale e-mail.

## Abilitare l’elenco Consentiti {#enable-allow-list}

Per abilitare l’elenco Consentiti su una sandbox non di produzione, devi aggiornare le impostazioni generali utilizzando il corrispondente punto finale API nel servizio Messaggi predefiniti.

* Utilizzando questa API, puoi anche disabilitare la funzione in qualsiasi momento.

* È possibile aggiornare l’elenco Consentiti prima o dopo l’abilitazione della funzione.

* La logica di elenco Consentiti si applica quando la funzione è abilitata **e** se l&#39;elenco Consentiti è **non** vuoto. [Ulteriori informazioni](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>Quando abilitata, la funzione di elenco Consentiti viene rispettata durante l&#39;esecuzione dei percorsi, ma anche durante il test dei messaggi con [bozze](preview.md#send-proofs) e i percorsi di test utilizzando la modalità [test](building-journeys/testing-the-journey.md).

## Aggiungi entità all’elenco Consentiti {#add-entities}

Per aggiungere nuovi indirizzi e-mail o domini all’elenco Consentiti per una sandbox specifica, devi chiamare l’API di soppressione con il valore `ALLOWED` per l’attributo `listType` . Esempio:

![](assets/allow-list-api.png)

È possibile eseguire le operazioni **Add**, **Delete** e **Get**.

>[!NOTE]
>
>L&#39;elenco Consentiti può contenere fino a 1.000 voci.

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## Logica Elenco Consentiti {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Quando l&#39;elenco Consentiti è **vuoto**, la logica di elenco Consentiti non viene applicata. Ciò significa che puoi inviare e-mail a qualsiasi profilo, purché non siano presenti nell’ [elenco di soppressione](suppression-list.md).

Quando l&#39;elenco Consentiti è **non vuoto**, viene applicata la logica di elenco Consentiti:

* Se un&#39;entità è **non nell&#39;elenco Consentiti** e non nell&#39;elenco di soppressione, il destinatario corrispondente non riceverà l&#39;e-mail, perché è **[!UICONTROL Not allowed]**.

* Se un&#39;entità è **sull&#39;elenco Consentiti** e non sull&#39;elenco di eliminazione, l&#39;e-mail può essere inviata al destinatario corrispondente. Tuttavia, se l’entità si trova anche nell’ [elenco di soppressione](suppression-list.md), il destinatario corrispondente non riceverà l’e-mail, perché è **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>I profili con stato **[!UICONTROL Not allowed]** sono esclusi durante il processo di invio del messaggio. Pertanto, mentre i **rapporti sul Percorso** mostreranno questi profili come spostati attraverso il percorso ([Leggi segmento](building-journeys/read-segment.md) e [Messaggio](building-journeys/journeys-message.md)), i **Rapporti e-mail** non li includeranno nelle metriche **[!UICONTROL Sent]** in quanto vengono filtrati prima dell’invio dell’e-mail.
>
>Ulteriori informazioni sul [Live Report](reports/live-report.md) e sul [Report globale](reports/global-report.md).

## Generazione di rapporti di esclusione {#reporting}

Quando questa funzione è abilitata su una sandbox non di produzione, puoi recuperare indirizzi e-mail o domini che sono stati esclusi da un invio perché non erano nell’elenco Consentiti. A questo scopo, puoi utilizzare [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html) per effettuare le chiamate API riportate di seguito.

Per ottenere il **numero di e-mail** che non sono state inviate perché i destinatari non erano nell&#39;elenco Consentiti, utilizza la seguente query:

```
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Per ottenere l’ **elenco di indirizzi e-mail** che non sono stati inviati perché i destinatari non erano nell’elenco Consentiti, utilizza la seguente query:

```
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

