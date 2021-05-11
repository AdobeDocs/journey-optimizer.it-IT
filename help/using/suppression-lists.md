---
title: Monitoraggio dell’esecuzione dei messaggi
description: Informazioni sul monitoraggio e sulle linee guida per il recapito messaggi
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 3%

---

# Gestisci elenchi di eliminazione {#manage-suppression-lists}

![](assets/do-not-localize/badge.png)

Un elenco di soppressione è costituito da indirizzi e-mail che si desidera escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione dell’invio e i tassi di consegna.

L&#39;elenco di soppressione **Journey Optimizer** viene gestito a livello di ambiente. Raccoglie lamentele di spam, rimbalzi duri e rimbalzi morbidi che si verificano costantemente.

## Perché gli elenchi di soppressione? {#why-suppression-lists}

Per controllare i messaggi e-mail ricevuti dai rispettivi proprietari e assicurarsi che ricevano solo quelli che desiderano, i provider di servizi Internet (ISP) e i filtri anti-spam commerciali hanno i loro algoritmi proprietari per tenere traccia della reputazione complessiva dei mittenti e-mail in base agli indirizzi IP e al o ai domini di invio che utilizzano.

Se non prendi il loro feedback (come reclami di spam, rimbalzi, ecc.) in considerazione, valuteranno la tua reputazione in basso. L&#39;elenco di soppressione ti aiuta a rispettare il feedback degli ISP.

I destinatari i cui indirizzi e-mail sono soppressi vengono automaticamente esclusi dalla consegna dei messaggi. In questo modo le consegne sono più rapide, poiché il tasso di errore ha un effetto significativo sulla velocità di consegna.

### Disturbi dovuti a spam {#spam-complaints}

L’elenco di soppressione raccoglie gli indirizzi e-mail che contrassegnano il messaggio come spam. L’invio ai destinatari dopo aver inviato un reclamo di posta indesiderata può avere un impatto enorme sulla tua reputazione di invio, perché informa gli ISP che potresti inviare e-mail indesiderate e potrebbe non ascoltare i tuoi destinatari.

Questo potrebbe comportare il blocco dell’indirizzo IP o del dominio di invio, che può essere evitato con questi indirizzi nell’elenco di soppressione.

### E-mail non consegnate {#bounces}

Inoltre, l’elenco di soppressione contiene indirizzi e-mail che rimbalzano duro o che rimbalzano morbido troppe volte. Se continui a inviare a questi indirizzi, potrebbe influenzare i tassi di consegna, perché comunica agli ISP che potresti non seguire le best practice di manutenzione dell’elenco indirizzi e-mail e quindi potrebbe non essere un mittente affidabile.

## Gestione degli elenchi di eliminazione {#suppression-list-management}

L&#39;elenco di soppressione di Journey Optimizer raccoglie gli indirizzi e-mail e i domini che vengono soppressi in tutte le comunicazioni **in un singolo ambiente client**, ovvero specifici per un ID organizzazione IMS associato a un ID sandbox.

L’elenco di soppressione consente di raccogliere automaticamente:
* Indirizzi e-mail non validi o costantemente non recapitati e che potrebbero influenzare negativamente la reputazione dell’e-mail se continui a includerli nelle consegne.
* Destinatari che emettono una denuncia di spam di qualche tipo contro uno dei tuoi messaggi e-mail.

Ad esempio, se qualcuno scrive a un servizio clienti richiedendo di non ricevere mai più e-mail da te, l’indirizzo e-mail di tale persona verrà soppresso nell’istanza e non potrai più recapitare a tale indirizzo.

<!--For each address, the basic reason for suppression (soft bounces, a hard bounce or a spam complaint) will be shown in the Suppression list.-->

### Errori di consegna {#delivery-failures}

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

Se una consegna non riesce, possono verificarsi tre tipi di errori:

* **Rimbalzo** duro. Un messaggio non recapitato indica un indirizzo e-mail non valido (ovvero un indirizzo e-mail inesistente). Questo comporta un messaggio non recapitato dal server e-mail ricevente che indica esplicitamente che l’indirizzo non è valido, ad esempio &quot;utente sconosciuto&quot;.
* **Rimbalzo morbido**. Si tratta di un messaggio non recapitato temporaneo per un indirizzo e-mail valido.
* **Ignorato**. Si tratta di un messaggio non recapitato per un indirizzo e-mail valido ma noto come temporaneo, ad esempio un tentativo di connessione non riuscito, un problema temporaneo relativo allo Spam (reputazione e-mail) o un problema tecnico temporaneo.

I rimbalzi rigidi e i rimbalzi morbidi possono essere un motivo per l’aggiunta automatica di un indirizzo e-mail all’elenco di soppressione.

### Cosa c&#39;è nella lista di soppressione? {#what-s-on-suppression-list}

Gli indirizzi e-mail vengono aggiunti all’elenco di eliminazione come segue:

* Tutti i **messaggi non recapitati** e **messaggi spam** inviano automaticamente gli indirizzi e-mail corrispondenti all&#39;elenco di soppressione dopo una singola occorrenza.

* **I** messaggi non recapitati morbidi non inviano immediatamente un indirizzo e-mail all’elenco di soppressione, ma incrementano un contatore di errori. Quando il contatore degli errori raggiunge la soglia, l’indirizzo viene quindi aggiunto all’elenco di soppressione.

   La soglia è impostata su tre errori:
   * Per la stessa consegna, al terzo tentativo, l’indirizzo viene soppresso.
   * Se ci sono consegne diverse e due errori si verificano almeno a 24 ore di distanza, il contatore degli errori viene incrementato a ogni errore e l’indirizzo viene eliminato anche al terzo tentativo.

   Quando una consegna ha esito positivo dopo un nuovo tentativo, il contatore di errori dell’indirizzo viene reinizializzato.

### Nuovi tentativi {#retries}

Se un messaggio non riesce a causa di un messaggio non recapitato temporaneo del tipo **Ignored** , verranno eseguiti nuovi tentativi per **3,5 giorni** dal momento in cui il messaggio è stato aggiunto alla coda e-mail.

Il ritardo minimo tra i nuovi tentativi e il numero massimo di tentativi da eseguire è <!--managed by the Enhanced MTA,--> in base alle prestazioni di un IP, sia storicamente che attualmente in un determinato dominio.

Dopo 3,5 giorni, qualsiasi messaggio nella coda dei nuovi tentativi verrà rimosso dalla coda e inviato nuovamente come messaggio non recapitato.
