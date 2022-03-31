---
title: Elenco di eliminazione
description: Scopri cosa è l’elenco di soppressione, il suo scopo e ciò che è incluso in esso.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# Elenco di eliminazione {#suppression-list}

Un elenco di soppressione è costituito da indirizzi e-mail che si desidera escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione dell’invio e i tassi di consegna.

La [!DNL Journey Optimizer] l&#39;elenco di soppressione viene gestito a livello di ambiente.

Raccoglie indirizzi e-mail e domini soppressi in tutti gli invii in un unico ambiente client, il che significa specifico per un ID organizzazione IMS associato a un ID sandbox.

## Perché una lista di soppressione? {#why-suppression-list}

Per controllare i messaggi e-mail ricevuti dai rispettivi proprietari e assicurarsi che ricevano solo quelli che desiderano, i provider di servizi Internet (ISP) e i filtri anti-spam commerciali hanno i loro algoritmi proprietari per tenere traccia della reputazione complessiva dei mittenti e-mail in base agli indirizzi IP e al o ai domini di invio che utilizzano.

Se non prendi il loro feedback (come reclami di spam, rimbalzi, ecc.) in considerazione, valuteranno la tua reputazione in basso. L&#39;elenco di soppressione ti aiuta a rispettare il feedback degli ISP.

I destinatari i cui indirizzi e-mail sono soppressi vengono automaticamente esclusi dalla consegna dei messaggi. In questo modo le consegne sono più rapide, poiché il tasso di errore ha un effetto significativo sulla velocità di consegna.

## Cosa c&#39;è nella lista di soppressione? {#what-s-on-suppression-list}

Gli indirizzi e-mail vengono aggiunti all’elenco di eliminazione come segue:

* Tutto **rimbalzi duri** e **disturbi da spam** invia automaticamente gli indirizzi e-mail corrispondenti all’elenco di soppressione dopo una singola occorrenza.

* **Rimbalzi morbidi** non inviare immediatamente un indirizzo e-mail all’elenco di soppressione, ma incrementa un contatore di errori. Diversi [tentativi](../configuration/retries.md) vengono quindi eseguiti e quando il contatore degli errori raggiunge la soglia, l’indirizzo viene aggiunto all’elenco di soppressione.

* È inoltre possibile [**manuale** aggiungere un indirizzo o un dominio](../configuration/manage-suppression-list.md#add-addresses-and-domains) all&#39;elenco di soppressione.

Per saperne di più su rimbalzi rigidi e rimbalzi morbidi in [questa sezione](#delivery-failures).

>[!NOTE]
>
>Gli indirizzi degli utenti non abbonati non possono essere inviati all’elenco di soppressione in quanto non ricevono e-mail da [!DNL Journey Optimizer]. La loro scelta viene gestita a livello di Experience Platform. Ulteriori informazioni su [rinuncia](../messages/consent.md).

Per ogni indirizzo, il motivo di base della soppressione e la categoria di soppressione (morbido, duro, ecc.) sono visualizzate nell&#39;elenco di soppressione. Ulteriori informazioni sull&#39;accesso e la gestione dell&#39;elenco di soppressione in [questa sezione](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>I profili con **[!UICONTROL Suppressed]** lo stato viene escluso durante il processo di invio del messaggio. Pertanto, mentre **Rapporti sui percorsi** mostrerà questi profili come spostati nel percorso ([Leggi segmento](../building-journeys/read-segment.md) e [Messaggio](../building-journeys/journeys-message.md) attività), **Rapporti e-mail** non li includerà nella **[!UICONTROL Sent]** le metriche vengono filtrate prima dell’invio dell’e-mail.
>
>Per saperne di più sul [Report live](../reports/live-report.md) e [Report globale](../reports/global-report.md). Per scoprire il motivo di tutti i casi di esclusione, puoi utilizzare il [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.

### Errori di consegna {#delivery-failures}

Esistono due tipi di errori quando una consegna non riesce:

* **Rimbalzo duro**. Un messaggio non recapitato indica un indirizzo e-mail non valido (ovvero un indirizzo e-mail inesistente). Questo comporta un messaggio non recapitato dal server e-mail ricevente che indica esplicitamente che l’indirizzo non è valido.
* **Rimbalzo morbido**. Si tratta di un messaggio non recapitato temporaneo per un indirizzo e-mail valido.

A **rimbalzo duro** aggiunge automaticamente l&#39;indirizzo e-mail all&#39;elenco di soppressione.

A **rimbalzo morbido** <!--or an **ignored** error--> che si verifica troppe volte invia anche l’indirizzo e-mail all’elenco di soppressione dopo diversi tentativi. [Ulteriori informazioni sui nuovi tentativi](../configuration/retries.md)

Se continui a inviare a questi indirizzi, potrebbe influenzare i tassi di consegna, perché comunica agli ISP che potresti non seguire le best practice di manutenzione dell’elenco indirizzi e-mail e quindi potrebbe non essere un mittente affidabile.

### Disturbi dello spam {#spam-complaints}

L’elenco di soppressione raccoglie gli indirizzi e-mail che contrassegnano il messaggio come spam. Ad esempio, se qualcuno scrive a un servizio clienti richiedendo di non ricevere mai più e-mail da te, l’indirizzo e-mail di tale persona verrà soppresso nell’istanza e non potrai più recapitare a tale indirizzo.

L’invio ai destinatari dopo aver inviato un reclamo di posta indesiderata può avere un impatto enorme sulla tua reputazione di invio, perché informa gli ISP che potresti inviare e-mail indesiderate e potrebbe non ascoltare i tuoi destinatari.

Questo potrebbe comportare il blocco dell’indirizzo IP o del dominio di invio, che può essere evitato con questi indirizzi nell’elenco di soppressione.
