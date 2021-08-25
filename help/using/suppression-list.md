---
title: Elenco di eliminazione
description: Scopri cosa è l’elenco di soppressione, il suo scopo e ciò che è incluso in esso.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# Elenco di eliminazione {#suppression-list}

Un elenco di soppressione è costituito da indirizzi e-mail che si desidera escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione dell’invio e i tassi di consegna.

L’elenco di soppressione [!DNL Journey Optimizer] viene gestito a livello di ambiente.

Raccoglie indirizzi e-mail e domini soppressi in tutti gli invii in un unico ambiente client, il che significa specifico per un ID organizzazione IMS associato a un ID sandbox.

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## Perché una lista di soppressione? {#why-suppression-list}

Per controllare i messaggi e-mail ricevuti dai rispettivi proprietari e assicurarsi che ricevano solo quelli che desiderano, i provider di servizi Internet (ISP) e i filtri anti-spam commerciali hanno i loro algoritmi proprietari per tenere traccia della reputazione complessiva dei mittenti e-mail in base agli indirizzi IP e al o ai domini di invio che utilizzano.

Se non prendi il loro feedback (come reclami di spam, rimbalzi, ecc.) in considerazione, valuteranno la tua reputazione in basso. L&#39;elenco di soppressione ti aiuta a rispettare il feedback degli ISP.

I destinatari i cui indirizzi e-mail sono soppressi vengono automaticamente esclusi dalla consegna dei messaggi. In questo modo le consegne sono più rapide, poiché il tasso di errore ha un effetto significativo sulla velocità di consegna.

## Cosa c&#39;è nella lista di soppressione? {#what-s-on-suppression-list}

Gli indirizzi e-mail vengono aggiunti all’elenco di eliminazione come segue:

* Tutti i **messaggi non recapitati** e **messaggi spam** inviano automaticamente gli indirizzi e-mail corrispondenti all&#39;elenco di soppressione dopo una singola occorrenza.

* **I** <!--and temporary **ignored** errors--> messaggi non recapitati morbidi non inviano immediatamente un indirizzo e-mail all’elenco di soppressione, ma incrementano un contatore di errori. Vengono quindi eseguiti diversi [tentativi](configuration/retries.md) e, quando il contatore di errori raggiunge la soglia, l&#39;indirizzo viene aggiunto all&#39;elenco di soppressione.

* È inoltre possibile [**aggiungere manualmente** un indirizzo o un dominio](configuration/manage-suppression-list.md#add-addresses-and-domains) all&#39;elenco di soppressione.

Ulteriori informazioni sui rimbalzi rigidi e sui mancati recapiti morbidi in [questa sezione](#delivery-failures).

>[!NOTE]
>
>Gli indirizzi degli utenti non abbonati non possono essere inviati all’elenco di soppressione in quanto non ricevono e-mail da [!DNL Journey Optimizer]. La loro scelta viene gestita a livello di Experience Platform. Ulteriori informazioni su [rinuncia](../using/consent.md).
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Per ogni indirizzo, il motivo di base della soppressione e la categoria di soppressione (morbido, duro, ecc.) sono visualizzate nell&#39;elenco di soppressione. Ulteriori informazioni sull&#39;accesso e la gestione dell&#39;elenco di soppressione in [questa sezione](configuration/manage-suppression-list.md).

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

>[!NOTE]
>
>I profili con stato **[!UICONTROL Suppressed]** sono esclusi durante il processo di invio del messaggio. Pertanto, mentre i **rapporti sul Percorso** mostreranno questi profili come spostati attraverso il percorso ([Leggi segmento](building-journeys/read-segment.md) e [Messaggio](building-journeys/journeys-message.md)), i **Rapporti e-mail** non li includeranno nelle metriche **[!UICONTROL Sent]** in quanto vengono filtrati prima dell’invio dell’e-mail.
>
>Ulteriori informazioni sul [Live Report](reports/live-report.md) e sul [Report globale](reports/global-report.md). Per scoprire il motivo di tutti i casi di esclusione, puoi utilizzare il [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.

### Errori di consegna {#delivery-failures}

Esistono due tipi di errori quando una consegna non riesce:

* **Rimbalzo** duro. Un messaggio non recapitato indica un indirizzo e-mail non valido (ovvero un indirizzo e-mail inesistente). Questo comporta un messaggio non recapitato dal server e-mail ricevente che indica esplicitamente che l’indirizzo non è valido.
* **Rimbalzo morbido**. Si tratta di un messaggio non recapitato temporaneo per un indirizzo e-mail valido.
<!--* **Ignored**. This is an email bounce that occurred for a valid email address but is known to be temporary, such as a failed connection attempt, a temporary Spam-related issue (email reputation), or a temporary technical issue.-->

Un **rimbalzo rigido** aggiunge automaticamente l&#39;indirizzo e-mail all&#39;elenco di soppressione.

Un **messaggio non recapitato** <!--or an **ignored** error--> che si verifica troppo spesso invia anche l&#39;indirizzo e-mail all&#39;elenco di eliminazione dopo diversi tentativi. [Ulteriori informazioni sui nuovi tentativi](configuration/retries.md)

Se continui a inviare a questi indirizzi, potrebbe influenzare i tassi di consegna, perché comunica agli ISP che potresti non seguire le best practice di manutenzione dell’elenco indirizzi e-mail e quindi potrebbe non essere un mittente affidabile.

### Disturbi dello spam {#spam-complaints}

L’elenco di soppressione raccoglie gli indirizzi e-mail che contrassegnano il messaggio come spam. Ad esempio, se qualcuno scrive a un servizio clienti richiedendo di non ricevere mai più e-mail da te, l’indirizzo e-mail di tale persona verrà soppresso nell’istanza e non potrai più recapitare a tale indirizzo.

L’invio ai destinatari dopo aver inviato un reclamo di posta indesiderata può avere un impatto enorme sulla tua reputazione di invio, perché informa gli ISP che potresti inviare e-mail indesiderate e potrebbe non ascoltare i tuoi destinatari.

Questo potrebbe comportare il blocco dell’indirizzo IP o del dominio di invio, che può essere evitato con questi indirizzi nell’elenco di soppressione.

<!--### Unsubscriptions {#unsubscriptions}

Every email sent to recipients must include an unsubscribe link. Upon clicking this link, if a recipient confirms [opting out](consent.md), the corresponding email address is immediately sent to the suppression list. This user must not receive communication from your brand until subscribed again.
NOT TRUE > "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

<!--MOVED to Configuration/Retries section

The threshold is set at three errors:
* For the same delivery, at the third attempt, the address is suppressed.
* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.
When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are ///managed by the Enhanced MTA/// based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->
