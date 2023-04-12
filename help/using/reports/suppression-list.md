---
solution: Journey Optimizer
product: journey optimizer
title: Elenco di soppressione
description: Scopri come utilizzare l’elenco di soppressione è
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 8%

---

# Elenco di soppressione {#suppression-list}

Un elenco di soppressione è costituito da indirizzi e domini che desideri escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione e i tassi di consegna dell’invio.

La [!DNL Journey Optimizer] l’elenco di soppressione viene gestito a livello di ambiente, ovvero per una data sandbox.

Raccoglie indirizzi e-mail e domini soppressi in tutti gli invii in un unico ambiente client, il che significa specifici per un ID organizzazione associato a un ID sandbox.

>[!NOTE]
>
>In Adobe viene conservato un elenco aggiornato degli indirizzi danneggiati noti, che si sono dimostrati dannosi per l’impegno e la reputazione dell’invio di e-mail e garantisce che le e-mail non vengano recapitate a tali indirizzi. Tale elenco viene gestito in un elenco di soppressione globale comune a tutti i clienti di Adobe. Gli indirizzi e i nomi di dominio contenuti nell’elenco di soppressione globale sono nascosti. Nei rapporti sulle consegne è indicato solo il numero di destinatari esclusi.

## Perché una lista di soppressione? {#why-suppression-list}

Per controllare i messaggi e-mail ricevuti dai rispettivi proprietari e assicurarsi che ricevano solo quelli che desiderano, i provider di servizi Internet (ISP) e i filtri anti-spam commerciali hanno i loro algoritmi proprietari per tenere traccia della reputazione complessiva dei mittenti e-mail in base agli indirizzi IP e al o ai domini di invio che utilizzano.

Se non prendi il loro feedback (come reclami di spam, rimbalzi, ecc.) in considerazione, valuteranno la tua reputazione in basso. L&#39;elenco di soppressione ti aiuta a rispettare il feedback degli ISP.

I destinatari i cui indirizzi e-mail sono soppressi vengono automaticamente esclusi dalla consegna dei messaggi. In questo modo le consegne sono più rapide, poiché il tasso di errore ha un effetto significativo sulla velocità di consegna.

## Cosa c&#39;è nella lista di soppressione? {#what-s-on-suppression-list}

Gli indirizzi vengono aggiunti all’elenco di soppressione come segue:

* Tutto **rimbalzi duri** e **disturbi da spam** invia automaticamente gli indirizzi corrispondenti all’elenco di soppressione dopo una singola occorrenza.

* **Rimbalzi morbidi** non inviano immediatamente un indirizzo all&#39;elenco di soppressione, ma incrementano un contatore di errori. Diversi [tentativi](../configuration/retries.md) vengono quindi eseguiti e quando il contatore degli errori raggiunge la soglia, l’indirizzo viene aggiunto all’elenco di soppressione.

* È inoltre possibile [**manuale** aggiungere un indirizzo o un dominio](../configuration/manage-suppression-list.md#add-addresses-and-domains) all&#39;elenco di soppressione.

Per saperne di più su rimbalzi rigidi e rimbalzi morbidi in [questa sezione](#delivery-failures).

>[!NOTE]
>
>Gli indirizzi degli utenti non abbonati non possono essere inviati all’elenco di soppressione in quanto non ricevono e-mail da [!DNL Journey Optimizer]. La loro scelta viene gestita a livello di Experience Platform. Ulteriori informazioni su [rinuncia](../privacy/opt-out.md).

Per ogni indirizzo, il motivo di base della soppressione e la categoria di soppressione (morbido, duro, ecc.) sono visualizzate nell&#39;elenco di soppressione. Ulteriori informazioni sull&#39;accesso e la gestione dell&#39;elenco di soppressione in [questa sezione](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>I profili con **[!UICONTROL Soppresso]** lo stato viene escluso durante il processo di invio del messaggio. Pertanto, mentre **Rapporti sui percorsi** mostrerà questi profili come spostati nel percorso ([Leggi segmento](../building-journeys/read-segment.md) e [attività messaggio](../building-journeys/journeys-message.md)), **Rapporti e-mail** non li includerà nella **[!UICONTROL Inviato]** le metriche vengono filtrate prima dell’invio dell’e-mail.
>
>Per saperne di più sul [Report live](../reports/live-report.md) e [Report globale](../reports/global-report.md). Per scoprire il motivo di tutti i casi di esclusione, puoi utilizzare il [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

### Errori di consegna {#delivery-failures}

Esistono due tipi di errori quando una consegna non riesce:

* **Rimbalzo duro**. Un messaggio non recapitato indica un indirizzo e-mail non valido (ovvero un indirizzo e-mail inesistente). Questo comporta un messaggio non recapitato dal server e-mail ricevente che indica esplicitamente che l’indirizzo non è valido.
* **Rimbalzo morbido**. Si tratta di un messaggio non recapitato temporaneo per un indirizzo e-mail valido.

A **rimbalzo duro** aggiunge automaticamente l&#39;indirizzo e-mail all&#39;elenco di soppressione.

A **rimbalzo morbido** <!--or an **ignored** error--> che si verifica troppe volte invia anche l’indirizzo e-mail all’elenco di soppressione dopo diversi tentativi. [Ulteriori informazioni sui nuovi tentativi](../configuration/retries.md)

Se continui a inviare a questi indirizzi, potrebbe influenzare i tassi di consegna, perché comunica agli ISP che potresti non seguire le best practice di manutenzione dell’elenco indirizzi e-mail e quindi potrebbe non essere un mittente affidabile.

### Segnalazioni di spam {#spam-complaints}

L’elenco di soppressione raccoglie gli indirizzi e-mail che contrassegnano il messaggio come spam. Ad esempio, se qualcuno scrive a un servizio clienti richiedendo di non ricevere mai più e-mail da te, l’indirizzo e-mail di tale persona verrà soppresso nell’istanza e non potrai più recapitare a tale indirizzo.

L’invio ai destinatari dopo aver inviato un reclamo di posta indesiderata può avere un impatto enorme sulla tua reputazione di invio, perché informa gli ISP che potresti inviare e-mail indesiderate e potrebbe non ascoltare i tuoi destinatari.

Questo potrebbe comportare il blocco dell’indirizzo IP o del dominio di invio, che può essere evitato con questi indirizzi nell’elenco di soppressione.
