---
title: Elenco consentiti
description: Scopri come utilizzare l’elenco Consentiti.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: a5c104539cae37197e0caa43cefcfed2bee23737
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 5%

---

# Elenco Consentiti {#allow-list}

È ora possibile definire un elenco di invio sicuro specifico nella pagina [sandbox](../administration/sandboxes.md) per disporre di un ambiente sicuro a scopo di test. In un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti ti assicura di non correre il rischio di inviare messaggi indesiderati ai clienti.

L’elenco Consentiti ti consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica. Questo può impedire l’invio accidentale di e-mail a veri indirizzi dei clienti in un ambiente di test.

>[!CAUTION]
>
>Questa funzione è **not** disponibile nelle sandbox di produzione. Si applica solo al canale e-mail.

## Abilitare l’elenco Consentiti {#enable-allow-list}

Per abilitare l’elenco Consentiti su una sandbox non di produzione, devi aggiornare le impostazioni generali utilizzando il corrispondente punto finale API nel servizio Messaggi predefiniti.

* Utilizzando questa API, puoi anche disabilitare la funzione in qualsiasi momento.

* È possibile aggiornare l’elenco Consentiti prima o dopo l’abilitazione della funzione.

* La logica di elenco Consentiti si applica quando la funzione è abilitata **e** se l&#39;elenco Consentiti è **not** vuoto. [Ulteriori informazioni](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>Quando è attivata, la funzione di elenco Consentiti viene rispettata durante l’esecuzione di percorsi, ma anche durante il test dei messaggi con [bozze](preview.md#send-proofs) e i percorsi di test che utilizzano [modalità di prova](../building-journeys/testing-the-journey.md).

## Aggiungi entità all’elenco Consentiti {#add-entities}

Per aggiungere nuovi indirizzi e-mail o domini all’elenco Consentiti per una sandbox specifica, devi chiamare l’API di soppressione con il `ALLOWED` valore per `listType` attributo. Esempio:

![](assets/allow-list-api.png)

È possibile eseguire le **Aggiungi**, **Elimina** e **Get** operazioni.

>[!NOTE]
>
>L’elenco Consentiti può contenere fino a 1.000 voci.

Ulteriori informazioni sull’esecuzione di chiamate API in [API di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html)Documentazione di riferimento di {target=&quot;_blank&quot;}.

## Logica Elenco Consentiti {#logic}

Quando l’elenco Consentiti è **vuoto**, la logica di elenco Consentiti non viene applicata. Ciò significa che puoi inviare e-mail a qualsiasi profilo, purché non siano nella [elenco a discesa](suppression-list.md).

Quando l’elenco Consentiti è **non vuoto**, viene applicata la logica di elenco Consentiti:

* Se un’entità è **non sull&#39;elenco Consentiti** e non nell’elenco di soppressione, il destinatario corrispondente non riceverà l’e-mail, poiché **[!UICONTROL Not allowed]**.

* Se un’entità è **sull&#39;elenco Consentiti**, e non nell’elenco di soppressione, l’e-mail può essere inviata al destinatario corrispondente. Tuttavia, se l’entità fa parte anche della [elenco a discesa](suppression-list.md), il destinatario corrispondente non riceverà l’e-mail, poiché **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>I profili con **[!UICONTROL Not allowed]** lo stato viene escluso durante il processo di invio del messaggio. Pertanto, mentre **Rapporti sui percorsi** mostrerà questi profili come spostati nel percorso ([Leggi segmento](../building-journeys/read-segment.md) e [Messaggio](../building-journeys/journeys-message.md) attività), **Rapporti e-mail** non li includerà nella **[!UICONTROL Sent]** le metriche vengono filtrate prima dell’invio dell’e-mail.
>
>Per saperne di più sul [Report live](../reports/live-report.md) e [Report globale](../reports/global-report.md).

## Generazione di rapporti di esclusione {#reporting}

Quando questa funzione è abilitata su una sandbox non di produzione, puoi recuperare indirizzi e-mail o domini che sono stati esclusi da un invio perché non erano nell’elenco Consentiti. A questo scopo, puoi utilizzare la funzione [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} per effettuare le chiamate API riportate di seguito.

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
