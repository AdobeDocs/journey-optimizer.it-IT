---
solution: Journey Optimizer
product: journey optimizer
title: Elenco di soppressione
description: Scopri come utilizzare l’elenco di soppressione
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 11%

---

# Elenco di soppressione {#suppression-list}

Un elenco di soppressione è costituito da indirizzi e domini che desideri escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione del mittente e le percentuali di consegna.

L&#39;elenco di soppressione di [!DNL Journey Optimizer] viene gestito a livello dell&#39;ambiente, ovvero per una data sandbox.

Raccoglie indirizzi e-mail e domini che vengono soppressi in tutte le comunicazioni in un unico ambiente client, il che significa specifico per un ID organizzazione associato a un ID sandbox.

>[!NOTE]
>
>Adobe mantiene un elenco aggiornato degli indirizzi non validi noti che si sono dimostrati dannosi per il coinvolgimento e la reputazione della posta e garantisce che le e-mail non vengano inviate a tali utenti. Tale elenco viene gestito in un elenco di soppressione globale comune a tutti i clienti di Adobe. Gli indirizzi e i nomi di dominio contenuti nell’elenco di soppressione globale sono nascosti. Nei rapporti sulle consegne è indicato solo il numero di destinatari esclusi.

Inoltre, puoi sfruttare le **API REST di soppressione** di Journey Optimizer per controllare i messaggi in uscita utilizzando elenchi Consentiti e di soppressione. [Scopri come utilizzare l’API REST di soppressione](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## Perché un elenco di soppressione? {#why-suppression-list}

Per controllare i messaggi e-mail ricevuti dai proprietari della casella in entrata e assicurarsi di ricevere solo quelli desiderati, i provider di servizi Internet (ISP) e i filtri spam commerciali dispongono di algoritmi proprietari per tenere traccia della reputazione complessiva dei mittenti e-mail in base agli indirizzi IP e ai domini di invio utilizzati.

Se non prendi in considerazione il loro feedback (come reclami di spam, mancati recapiti, ecc.), la tua reputazione verrà valutata in modo negativo. L’elenco di soppressione ti aiuta a rispettare il feedback degli ISP.

I destinatari i cui indirizzi e-mail vengono soppressi vengono automaticamente esclusi dalla consegna dei messaggi. In questo modo le consegne sono più rapide, poiché il tasso di errore ha un effetto significativo sulla velocità di consegna.

## Cosa c’è nell’elenco di soppressione? {#what-s-on-suppression-list}

Gli indirizzi vengono aggiunti all’elenco di soppressione come segue:

* Tutti i **hard bounce** e i **reclami spam** inviano automaticamente gli indirizzi corrispondenti all&#39;elenco di soppressione dopo una singola occorrenza. Ulteriori informazioni sui reclami di posta indesiderata sono disponibili in [questa sezione](#spam-complaints).

* **Mancati recapiti non permanenti** non inviano immediatamente un indirizzo all&#39;elenco di soppressione, ma incrementano un contatore di errori. Vengono quindi eseguiti diversi [nuovi tentativi](../configuration/retries.md) e quando il contatore di errori raggiunge la soglia, l&#39;indirizzo viene aggiunto all&#39;elenco di soppressione.

* Puoi anche [**aggiungere manualmente** un indirizzo o un dominio](../configuration/manage-suppression-list.md#add-addresses-and-domains) all&#39;elenco di soppressione.

Ulteriori informazioni sui mancati recapiti permanenti e sui mancati recapiti non permanenti in [questa sezione](#delivery-failures).

>[!NOTE]
>
>Gli indirizzi degli utenti non iscritti non possono essere inviati all&#39;elenco di soppressione poiché non ricevono e-mail da [!DNL Journey Optimizer]. La loro scelta viene gestita a livello di Experience Platform. Ulteriori informazioni sulla [rinuncia](../privacy/opt-out.md).

Per ogni indirizzo, il motivo di base per l’eliminazione e la categoria di soppressione (soft, hard ecc.) vengono visualizzati nell’elenco di soppressione. Ulteriori informazioni sull&#39;accesso e la gestione dell&#39;elenco di soppressione in [questa sezione](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>I profili con stato **[!UICONTROL Eliminato]** sono esclusi durante il processo di invio dei messaggi. Pertanto, mentre nei **report Percorso** questi profili vengono visualizzati come spostati nel percorso ([Attività Read Audience](../building-journeys/read-audience.md) e [attività messaggio](../building-journeys/journeys-message.md)), i **report e-mail** non li includono nelle metriche **[!UICONTROL Inviati]** in quanto vengono filtrati prima dell&#39;invio di e-mail.
>
>Ulteriori informazioni sul [report live](../reports/live-report.md) e sul [report Customer Journey Analytics](../reports/report-gs-cja.md). Per individuare il motivo di tutti i casi di esclusione, è possibile utilizzare [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

### Errori di consegna {#delivery-failures}

Esistono due tipi di errori quando una consegna non riesce:

* **Mancato recapito permanente**. Un messaggio non recapitato indica un indirizzo e-mail non valido, ovvero un indirizzo e-mail inesistente. Ciò comporta un messaggio di mancato recapito dal server e-mail ricevente che indica esplicitamente che l’indirizzo non è valido.
* **Mancato recapito non permanente**. Questo è un messaggio e-mail non recapitato temporaneo che si è verificato per un indirizzo e-mail valido.

Un **messaggio non recapitato** aggiunge automaticamente l&#39;indirizzo di posta elettronica all&#39;elenco di soppressione.

Un **mancato recapito non permanente** <!--or an **ignored** error--> che si verifica troppe volte invia inoltre l&#39;indirizzo di posta elettronica all&#39;elenco di soppressione dopo diversi tentativi. [Ulteriori informazioni sui nuovi tentativi](../configuration/retries.md)

Se continui a inviare a questi indirizzi, potrebbe influenzare le percentuali di consegna, perché indica agli ISP che potresti non seguire le best practice di manutenzione dell’elenco di indirizzi e-mail e quindi potrebbe non essere un mittente affidabile.

### Reclami spam {#spam-complaints}

L’elenco di soppressione raccoglie gli indirizzi e-mail che contrassegnano il messaggio come spam. Ad esempio, se qualcuno scrive a un servizio clienti chiedendo di non ricevere più la posta da te, l’indirizzo e-mail di quella persona verrà soppresso nell’istanza e non potrai più recapitare a quell’indirizzo.

L’invio a destinatari dopo l’invio di un reclamo spam può avere un impatto enorme sulla reputazione del mittente, in quanto informa gli ISP che puoi inviare e-mail indesiderate e che non ascolti i destinatari.

Questo poteva causare il blocco dell’indirizzo IP o del dominio di invio, che poteva essere evitato inserendo tali indirizzi nell’elenco di soppressione.

Alcuni ISP offrono un ciclo di feedback (FBL) che consente al mittente dell’e-mail di ricevere automaticamente una notifica quando l’utente che riceve un’e-mail sceglie di contrassegnarla come spam. [Ulteriori informazioni](deliverability.md#feedback-loops)
