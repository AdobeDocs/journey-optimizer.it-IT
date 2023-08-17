---
solution: Journey Optimizer
product: journey optimizer
title: Elenco di soppressione
description: Scopri come utilizzare l’elenco di soppressione
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 8%

---

# Elenco di soppressione {#suppression-list}

Un elenco di soppressione è costituito da indirizzi e domini che desideri escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione del mittente e le percentuali di consegna.

Il [!DNL Journey Optimizer] l’elenco di soppressione viene gestito a livello di ambiente, ovvero per una determinata sandbox.

Raccoglie indirizzi e-mail e domini che vengono soppressi in tutte le comunicazioni in un unico ambiente client, il che significa specifico per un ID organizzazione associato a un ID sandbox.

>[!NOTE]
>
>Adobe mantiene un elenco aggiornato di indirizzi non validi noti che hanno dimostrato di essere dannosi per il coinvolgimento e la reputazione di mailing e garantisce che le e-mail non vengano consegnate a loro. Tale elenco viene gestito in un elenco di soppressione globale comune a tutti i clienti di Adobe. Gli indirizzi e i nomi di dominio contenuti nell’elenco di soppressione globale sono nascosti. Nei rapporti sulle consegne è indicato solo il numero di destinatari esclusi.

## Perché un elenco di soppressione? {#why-suppression-list}

Per controllare i messaggi e-mail ricevuti dai proprietari della casella in entrata e assicurarsi di ricevere solo quelli desiderati, i provider di servizi Internet (ISP) e i filtri spam commerciali dispongono di algoritmi proprietari per tenere traccia della reputazione complessiva dei mittenti e-mail in base agli indirizzi IP e ai domini di invio utilizzati.

Se non ricevi i loro feedback (ad esempio, reclami e mancate consegne) In considerazione di ciò, la tua reputazione verrà valutata in base a un punteggio inferiore. L’elenco di soppressione ti aiuta a rispettare il feedback degli ISP.

I destinatari i cui indirizzi e-mail vengono soppressi vengono automaticamente esclusi dalla consegna dei messaggi. In questo modo le consegne sono più rapide, poiché il tasso di errore ha un effetto significativo sulla velocità di consegna.

## Cosa c’è nell’elenco di soppressione? {#what-s-on-suppression-list}

Gli indirizzi vengono aggiunti all’elenco di soppressione come segue:

* Tutti **mancati recapiti permanenti** e **reclami spam** invia automaticamente gli indirizzi corrispondenti all’elenco di soppressione dopo una singola occorrenza.

* **Mancati recapiti non permanenti** non inviare immediatamente un indirizzo all’elenco di soppressione, ma incrementa un contatore di errori. Diversi [nuovi tentativi](../configuration/retries.md) vengono quindi eseguiti e, quando il contatore di errori raggiunge la soglia, l’indirizzo viene aggiunto all’elenco di soppressione.

* È inoltre possibile [**manualmente** aggiungi un indirizzo o un dominio](../configuration/manage-suppression-list.md#add-addresses-and-domains) nell’elenco di soppressione.

Ulteriori informazioni sui mancati recapiti permanenti e sui mancati recapiti non permanenti in [questa sezione](#delivery-failures).

>[!NOTE]
>
>Gli indirizzi degli utenti non abbonati non possono essere inviati all’elenco di soppressione poiché non ricevono e-mail da [!DNL Journey Optimizer]. La loro scelta viene gestita a livello di Experience Platform. Ulteriori informazioni su [rinuncia](../privacy/opt-out.md).

Per ogni indirizzo, il motivo di base dell’eliminazione e la categoria di eliminazione (morbida, rigida, ecc.) vengono visualizzati nell’elenco di soppressione. Ulteriori informazioni sull’accesso e la gestione dell’elenco di soppressione in [questa sezione](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>I profili con **[!UICONTROL Soppresso]** Lo stato è escluso durante il processo di invio del messaggio. Pertanto, mentre il **Rapporti percorso** mostra questi profili come spostati nel percorso ([Read Audience](../building-journeys/read-audience.md) e [attività messaggio](../building-journeys/journeys-message.md)), il **Report e-mail** non li includerà nella **[!UICONTROL Inviato]** metriche poiché vengono escluse prima dell’invio e-mail.
>
>Ulteriori informazioni su [Rapporto live](../reports/live-report.md) e [Rapporto globale](../reports/global-report.md). Per scoprire il motivo di tutti i casi di esclusione, puoi utilizzare [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

### Errori di consegna {#delivery-failures}

Esistono due tipi di errori quando una consegna non riesce:

* **Mancato recapito permanente**. Un messaggio non recapitato indica un indirizzo e-mail non valido, ovvero un indirizzo e-mail inesistente. Ciò comporta un messaggio di mancato recapito dal server e-mail ricevente che indica esplicitamente che l’indirizzo non è valido.
* **Mancato recapito non permanente**. Questo è un messaggio e-mail non recapitato temporaneo che si è verificato per un indirizzo e-mail valido.

A **mancato recapito permanente** aggiunge automaticamente l’indirizzo e-mail all’elenco di soppressione.

A **mancato recapito non permanente** <!--or an **ignored** error--> che si verifica troppe volte invia anche l’indirizzo e-mail all’elenco di soppressione dopo diversi tentativi. [Ulteriori informazioni sui nuovi tentativi](../configuration/retries.md)

Se continui a inviare a questi indirizzi, potrebbe influenzare le percentuali di consegna, perché indica agli ISP che potresti non seguire le best practice di manutenzione dell’elenco di indirizzi e-mail e quindi potrebbe non essere un mittente affidabile.

### Segnalazioni di spam {#spam-complaints}

L’elenco di soppressione raccoglie gli indirizzi e-mail che contrassegnano il messaggio come spam. Ad esempio, se qualcuno scrive a un servizio clienti chiedendo di non ricevere più la posta da te, l’indirizzo e-mail di quella persona verrà soppresso nell’istanza e non potrai più recapitare a quell’indirizzo.

L’invio a destinatari dopo l’invio di un reclamo spam può avere un impatto enorme sulla reputazione del mittente, in quanto informa gli ISP che puoi inviare e-mail indesiderate e che non ascolti i destinatari.

Questo poteva causare il blocco dell’indirizzo IP o del dominio di invio, che poteva essere evitato inserendo tali indirizzi nell’elenco di soppressione.
