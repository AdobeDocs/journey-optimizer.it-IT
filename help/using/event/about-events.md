---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare gli eventi del percorso
description: Scopri come utilizzare gli eventi nei tuoi percorsi
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: eventi, evento, percorso, definizione, inizio
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
TQID: https://experienceleague.adobe.com/xvLSBd-rwKKNqwQNDa4D8GfFzc-ND1FkC3EdstufkIY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: d08afb72-92f6-4856-88e3-11ec34313c2fid: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 6657a77a27455643fa0fb3d94a4d7e3ab83e6843
workflow-type: tm+mt
source-wordcount: 2407
ht-degree: 15%

---

# Utilizzare gli eventi del percorso {#about-events}

>[!BEGINSHADEBOX]

**In questa pagina:** Comprendi i tre tipi di eventi, i loro requisiti di schema, i vincoli chiave e come scegliere quello giusto per il tuo caso d&#39;uso.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventi del percorso"
>abstract="Journey Optimizer supporta tre tipi di eventi nei percorsi: eventi unitari, collegati al comportamento di una persona specifica (ad esempio un acquisto o una milestone fedeltà); eventi di business, attivati da un’occorrenza globale (ad esempio una cancellazione di un volo o un aggiornamento delle scorte); ed eventi di qualificazione del pubblico, attivati quando un profilo entra o esce da un pubblico. Utilizza gli eventi per attivare i percorsi e orchestrare le azioni corrette per i profili."

Utilizza gli eventi per attivare i singoli percorsi, distribuendo messaggi in tempo reale a ogni utente che entra nel percorso. Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. All’interno dei vari passaggi di un percorso puoi utilizzare più eventi, e uno stesso evento può essere utilizzato in più percorsi.

La configurazione dell&#39;evento è **obbligatoria** e deve essere eseguita da un tecnico dati.

>[!IMPORTANT]
>
>* Prima di configurare gli eventi, accertati di disporre: del ruolo **Amministratore Journey Optimizer** o **Ingegnere dati**, di uno schema XDM con **Profilo cliente in tempo reale** abilitato, di un endpoint di streaming attivo e di accedere alla sandbox corretta.
>
>* Per i requisiti e le limitazioni degli eventi (streaming, Query Service, acquisizione batch), consulta [Guardrail di Percorso - Eventi](../start/guardrails.md#events-g).

**Chi fa cosa:**

| Attività | Ruolo |
| --- | --- |
| Progettare e creare lo schema XDM | Ingegnere dati |
| Configurare l’endpoint di streaming | Ingegnere dati |
| Configura eventi unitari e aziendali (**Amministrazione > Eventi**) | Ingegnere dati o Amministratore |
| Utilizzare gli eventi in un percorso | Percorso |
| Configurare gli eventi di qualificazione del pubblico (selezionati nell’area di lavoro) | Percorso |

È possibile configurare tre tipi di eventi: **Eventi unitari**, **Eventi aziendali** e **Eventi di qualificazione del pubblico**.

➡️ [Scopri questa funzione nel video](#video)

➡️ [Scopri questa funzione nel video](#video)

## Eventi unitari {#unitary-events}

**Unitario** eventi collegati a una persona. Si riferiscono al comportamento di una persona (ad esempio, una persona ha acquistato un prodotto, ha visitato un negozio, è uscita da un sito web, ecc.) Oppure, indica qualcosa che si verifica in relazione a una persona, che può ad esempio aver raggiunto 10.000 punti fedeltà. Nell’ambito dei percorsi, [!DNL Journey Optimizer] farà da listener per questi dati, in modo da orchestrare le migliori azioni successive da eseguire. Gli eventi unitari possono essere basati su regole o generati dal sistema. [Scopri come creare un evento unitario](../event/about-creating.md).

**Requisito schema:** uno schema XDM ExperienceEvent con un&#39;identità primaria basata su persona e **Profilo cliente in tempo reale** abilitato.

**Esempio:** un cliente aggiunge elementi al carrello e chiude il browser. Un evento abbandonato dal carrello viene attivato, il profilo entra nel percorso in tempo reale e riceve un’e-mail di ripristino un’ora dopo.

>[!NOTE]
>
>I percorsi unitari includono un guardrail di rientro: il rientro del profilo viene bloccato per impostazione predefinita per 5 minuti dopo l’attivazione del percorso. Se ad esempio un evento attiva un percorso a 12:01 per un profilo e un altro arriva a 12:03, il percorso non viene riavviato per tale profilo.

## Eventi di business {#business-events}

Gli eventi **Business** non sono collegati a un profilo specifico. Ad esempio, può essere un avviso di notizie, un aggiornamento sportivo, una modifica o cancellazione di un volo, un aggiornamento di inventario, eventi meteo, ecc. Anche se questi eventi non sono specifici per un profilo, possono essere di interesse per un numero qualsiasi di profili: utenti abbonati a notizie particolari, passeggeri su un volo, acquirenti interessati a un prodotto esaurito, ecc. Gli eventi di business sono sempre basati su regole. Quando rilasci un evento di business in un percorso, aggiunge automaticamente un&#39;attività **Read audience** subito dopo. [Scopri come creare un evento di business](../event/about-creating-business.md).

**Requisito dello schema:** uno schema XDM di serie temporale con un&#39;identità primaria non persona e i campi `_id` e `timestamp` sono compilati. Pianifica un ritardo di esportazione del pubblico da 15 minuti a un’ora.

**Esempio:** una compagnia aerea annulla un volo. Un evento di business viene attivato, [!DNL Journey Optimizer] legge il pubblico dei passeggeri interessati e invia a ciascuno una notifica di rebooking.

## Eventi di qualificazione del pubblico {#audience-qualification-events}

Un evento di **qualificazione del pubblico** viene attivato quando un profilo entra o esce da un pubblico. Ad esempio, un cliente che supera una soglia di spesa fedeltà entra nel pubblico di livello Gold. Tale qualifica attiva il percorso per tale profilo in tempo reale (per i tipi di pubblico in streaming) o alla successiva valutazione batch. A differenza degli eventi unitari, la qualificazione del pubblico consente di creare una logica di attivazione complessa utilizzando tutta la potenza delle definizioni di pubblico, senza richiedere modifiche all’implementazione per inviare un nuovo evento. Ulteriori informazioni su [eventi di qualificazione del pubblico](../building-journeys/audience-qualification-events.md).

**Requisito schema:** Non è richiesto alcuno schema aggiuntivo. L&#39;evento si basa su definizioni di pubblico esistenti già integrate in Adobe Experience Platform.

**Esempio:** la spesa fedeltà di un cliente supera la soglia del livello Gold. Il loro profilo è idoneo per il pubblico Gold, il percorso si attiva automaticamente e invia un premio di benvenuto.

>[!NOTE]
>
>Gli eventi di qualificazione del pubblico non sono configurati in **Amministrazione > Eventi**, ma vengono selezionati direttamente nell&#39;area di lavoro del percorso come primo passaggio di un percorso.

## Tipi di eventi in breve {#event-comparison}

| | Evento unitario | Evento di business | Evento di qualificazione del pubblico |
| --- | --- | --- | --- |
| **Collegato a un profilo?** | Sì — attivato dall&#39;azione di un individuo specifico. | No — attivato da un evento esterno non associato a una persona. | Sì - viene attivato quando un profilo entra o esce da un pubblico. |
| **Comportamento di ingresso** | Un profilo entra nel percorso in tempo reale. | Più profili vengono immessi tramite un passaggio Read Audience automatico. | Un profilo entra quando cambia l’iscrizione al pubblico. |
| **Casi d&#39;uso tipici** | Recupero dell’abbandono del carrello, invio dei moduli, accesso all’app, milestone di fedeltà. | Cancellazione del volo, allarme rifornimento scorte, ultime notizie, evento meteo. | Nuovo coinvolgimento dei clienti obsoleti, modifiche del livello di fedeltà, flussi di offboarding di VIP. |
| **Avvio del percorso** | Voce basata su eventi: nessun pubblico necessario. | Evento business + Read Audience automatico (aggiunto da Journey Optimizer). | Il profilo entra o esce da un pubblico definito. |
| **Più per percorso?** | Sì - è possibile ascoltare diversi eventi unitari tra i passaggi del percorso. | No: solo un evento di business al percorso, all&#39;inizio. | Sì — può essere combinato con altre attività. |
| **Tipo ID evento** | Basato su regole o generato dal sistema. | Sempre basato su regole. | Nessun ID evento - in base alla valutazione dell’appartenenza a un pubblico. |
| **Configurato in Amministrazione?** | Sì | Sì | No — selezionato direttamente nell&#39;area di lavoro del percorso. |

>[!NOTE]
>
>Un percorso può contenere solo **un** evento di business, che deve essere la prima attività. Journey Optimizer aggiunge automaticamente un&#39;attività **Read Audience** dopo di essa per definire quali profili ricevono il percorso attivato da tale evento.

## Tipo ID evento {#event-id-type}

Per gli eventi **business**, il tipo di ID evento è sempre basato su regole.

Per gli eventi **unitari**, esistono due tipi di ID evento:

* **Eventi basati sulle regole**: questo tipo di evento non genera un eventID. Utilizzando l’editor di espressioni semplici, puoi semplicemente definire una regola che verrà utilizzata dal sistema per identificare gli eventi rilevanti che attiveranno i percorsi. Questa regola può essere basata su qualsiasi campo disponibile nel payload dell’evento, ad esempio la posizione del profilo o il numero di elementi aggiunti al carrello del profilo.

  >[!CAUTION]
  >
  >Per gli eventi basati su regole viene definita una regola di quota limite. Limita il numero di eventi qualificati che un percorso può elaborare a 5.000 al secondo per una determinata organizzazione. Corrisponde agli SLA di Journey Optimizer. Consulta le licenze Journey Optimizer e la [descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

* Eventi **generati dal sistema**: questi eventi richiedono un eventID. Questo campo eventID viene generato automaticamente durante la creazione dell’evento. Il sistema che trasmette l’evento non deve generare un ID, deve trasmettere quello disponibile nell’anteprima del payload.

>[!NOTE]
>
>Solo gli eventi in streaming possono attivare i percorsi. **impossibile** utilizzare il seguente per attivare un percorso:
>
>* Eventi acquisiti in batch
>* Eventi inseriti tramite **Query Service**
>* Eventi da [!DNL Journey Optimizer] set di dati interni (feedback messaggi, tracciamento e-mail e simili)
>
>Se non riesci a ricevere eventi in streaming, crea un pubblico basato su tali eventi e utilizza invece un&#39;attività **Read Audience**. Per utilizzare gli eventi solo per la segmentazione, abilita il set di dati per **Profilo cliente in tempo reale**.

## Come scegliere {#choose-event-type}

Utilizzare i criteri seguenti per selezionare il tipo di evento corretto per il percorso. La domanda chiave è: **si sta attivando un&#39;azione per una persona specifica o si sta trasmettendo a molti profili?** [Ulteriori informazioni sui tipi di percorso](../building-journeys/journey.md#journey-types).

Ogni tipo di evento è associato a un pattern di percorso specifico:

| Tipo di evento | pattern percorso |
| --- | --- |
| Evento unitario | Percorso a profilo singolo in tempo reale: si attiva immediatamente quando una persona agisce |
| Evento di business | Percorso di trasmissione: esegue il targeting di molti profili tramite un passaggio automatico Read Audience |
| Evento di qualificazione del pubblico | Percorso attivato da segmento: viene attivato quando un profilo entra o esce da un pubblico |

* **Scegli un evento unitario** quando il trigger è associato a un individuo specifico, ad esempio un acquisto, un invio di un modulo o un milestone di fedeltà. Gli eventi unitari richiedono un’identità primaria basata su persona nello schema e avviano il percorso immediatamente per tale profilo. [Scopri come configurare un evento unitario](../event/about-creating.md).

* **Scegliere un evento di business** quando il trigger è un evento globale, ad esempio un riassortimento del prodotto, un calo del prezzo o una cancellazione del volo, e si desidera trasmettere a un set di profili correlati a tale segnale. Gli eventi di business devono essere il primo passaggio del percorso ed eseguire automaticamente il targeting dei profili tramite un&#39;attività **Read Audience**. Richiedono uno schema di serie temporali con un&#39;identità primaria non-people e i campi `_id` e `timestamp`. Pianifica un ritardo di esportazione del pubblico da 15 minuti a un’ora. [Scopri come configurare un evento di business](../event/about-creating-business.md).

* **Scegli un evento di qualificazione del pubblico** quando il trigger è un profilo che accede o esce da un pubblico e hai bisogno di una logica di segmentazione più complessa di quella che può fornire un singolo evento, ad esempio, coinvolgendo nuovamente i clienti inattivi che hanno appena raggiunto una soglia di spesa o attivando un flusso di offboarding quando un membro di VIP abbandona il livello di fedeltà. [Ulteriori informazioni sugli eventi di qualificazione del pubblico](../building-journeys/audience-qualification-events.md).

>[!CAUTION]
>
>Gli eventi di business non possono essere utilizzati nello stesso percorso di eventi unitari o attività di qualificazione del pubblico.

## Vincoli chiave {#key-constraints}

Utilizza questo riepilogo per pianificare l’implementazione prima di configurare gli eventi.

| Vincolo | Dettagli |
| --- | --- |
| Limite di throughput | 5.000 eventi al secondo per organizzazione, in tutte le sandbox (percorsi unitari e Read Audience) |
| Blocco di rientro | Il rientro del profilo è bloccato per 5 minuti dopo l’attivazione di un percorso unitario |
| Eventi di business al percorso | Massimo 1, deve essere il primo passaggio |
| Combinazione di business e unitaria in un unico percorso | Non supportato |
| Eventi batch | Impossibile attivare i percorsi. Utilizza un&#39;attività **Read Audience** |
| Qualificazione del pubblico — Amministrazione | Non configurato in **Amministrazione > Eventi** — selezionato direttamente nell&#39;area di lavoro del percorso |
| Modificare un evento live | È possibile modificare solo il nome, la descrizione o aggiungere campi payload |

## Come raggiungono Journey Optimizer gli eventi {#data-cycle}

Gli eventi devono essere inviati a [!DNL Journey Optimizer] come chiamate POST tramite [API di acquisizione streaming di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=it){target="_blank"}. Il payload deve seguire la formattazione XDM e nello schema dell&#39;evento deve essere abilitato **Profilo cliente in tempo reale**.

Sono supportate sia le modalità di streaming autenticate che quelle non autenticate. Gli eventi e gli eventi acquisiti in batch dai set di dati interni [!DNL Journey Optimizer] (feedback dei messaggi, tracciamento e-mail e simili) non possono essere utilizzati per attivare i percorsi. Utilizza un&#39;attività **Read Audience** per questi casi d&#39;uso.


## Limiti di velocità effettiva degli eventi {#event-throughput}

Adobe Journey Optimizer applica limiti di velocità effettiva separati per tipo di evento, a livello di organizzazione in tutte le sandbox:

* **Eventi unitari**: 5.000 eventi al secondo
* **Leggi eventi di percorso basati sul pubblico**: 5.000 eventi al secondo

Questi limiti si applicano a tutti gli eventi utilizzati nei percorsi attivi, che includono **Live**, **Dry run**, **Closed** e **Paused** percorsi. Al raggiungimento di un limite, i nuovi eventi vengono messi in coda ed elaborati a 5.000 al secondo fino a quando la coda non viene svuotata.

Per ulteriori dettagli sulle velocità di elaborazione del percorso e sull&#39;impatto dei diversi tipi di percorso sulla velocità effettiva, [ulteriori informazioni sulle velocità di elaborazione del percorso](../building-journeys/entry-management.md#journey-processing-rate).

Per queste quote vengono conteggiati i seguenti tipi di eventi:

* **Eventi unitari esterni**: include eventi basati su regole e generati dal sistema. Se lo stesso evento non elaborato è idoneo per più definizioni di regola, ogni regola corrispondente viene conteggiata come un evento separato verso la quota.

* **Eventi di qualificazione del pubblico**: se lo stesso pubblico di streaming viene utilizzato in più percorsi, ogni utilizzo conta separatamente. Ad esempio, l’utilizzo dello stesso pubblico in un’attività di qualificazione del pubblico in due percorsi determina due eventi conteggiati.

* **Eventi di reazione**: eventi attivati dalle reazioni del profilo (e-mail aperta, e-mail selezionata, ecc.) entro un percorso.

* **Eventi aziendali**: eventi non associati a un profilo specifico, ma a un evento aziendale.

* **Eventi di Analytics**: se l&#39;integrazione [con Adobe Analytics per attivare i percorsi](about-analytics.md) è stata abilitata, vengono inclusi anche questi eventi.

* **Riprendi eventi**: evento tecnico attivato quando un profilo riprende da un percorso in pausa. Ulteriori informazioni sulla ripresa di [percorsi in pausa](../building-journeys/journey-pause.md#journey-resume-steps).

* **Eventi di completamento nodo di attesa**: quando un profilo esce da un nodo di attesa, viene generato un evento tecnico per riprendere il percorso.

>[!NOTE]
>
>Ad eccezione degli eventi di attesa e ripresa, anche tutti gli altri tipi di evento vengono conteggiati nella quota se utilizzati in percorsi basati su tipi di pubblico di lettura.

## Aggiornamento ed eliminazione di un evento {#update-event}


Per evitare di interrompere i percorsi esistenti, quando modifichi un evento utilizzato in un percorso **Bozza**, **Live** o **Chiuso**, puoi modificare solo il nome, la descrizione o aggiungere campi payload.

Qualsiasi evento utilizzato in **Live**, **Draft** o **Closed** percorsi non può essere eliminato. Per eliminare un evento utilizzato, è necessario interrompere i percorsi che lo utilizzano e/o rimuoverlo dai percorsi 2D in cui viene utilizzato. Puoi controllare il campo **[!UICONTROL Usato in]**. Viene visualizzato il numero di percorsi che utilizzano quel particolare evento. Per visualizzare l’elenco dei percorsi corrispondenti, puoi fare clic sul pulsante **[!UICONTROL Visualizza percorsi]**.

## Domande frequenti {#faq}

**Posso usare lo stesso evento in più percorsi?**
Sì — più percorsi possono ascoltare lo stesso evento contemporaneamente.

**È possibile combinare un evento business e un evento unitario nello stesso percorso?**
No - gli eventi di business non possono essere utilizzati nello stesso percorso degli eventi unitari o delle attività di qualificazione del pubblico.

**Devo configurare qualcosa per gli eventi di qualificazione del pubblico?**
No — gli eventi di qualificazione del pubblico non sono configurati in **Amministrazione > Eventi**. Come primo passaggio, seleziona il pubblico direttamente sull’area di lavoro del percorso.

**Posso utilizzare dati acquisiti in batch per attivare un percorso?**
No - solo gli eventi in streaming possono attivare i percorsi. Per i dati batch, genera un pubblico e utilizza invece un&#39;attività **Read Audience**.

**Il mio percorso non si attiva. Cosa devo controllare?**

* Verifica che nello schema dell&#39;evento sia abilitato **Profilo cliente in tempo reale**.
* Conferma che gli eventi vengano inviati in streaming; gli eventi acquisiti in batch non possono attivare i percorsi.
* Per gli eventi basati su regole, verifica che la condizione della regola corrisponda ai campi payload in ingresso.
* Verifica che il percorso sia nello stato **Live** e che il profilo soddisfi le condizioni di ingresso.

## Passaggi successivi {#next-steps}

* [Configurare un evento unitario](../event/about-creating.md)
* [Configurare un evento di business](../event/about-creating-business.md)
* [Ulteriori informazioni sugli eventi di qualificazione del pubblico](../building-journeys/audience-qualification-events.md)
* [Gestire l&#39;ingresso e il rientro del percorso](../building-journeys/entry-management.md)

>[!TIP]
>
>Se il percorso non viene attivato, verificare che nello schema dell&#39;evento sia abilitato **Profilo cliente in tempo reale** e che gli eventi vengano trasmessi in streaming. Gli eventi acquisiti in batch non possono attivare i percorsi.

## Video dimostrativi {#video}

Scopri come configurare un evento, specificare l’endpoint di streaming e il payload di un evento.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendere i casi d’uso applicabili per gli eventi di business. Scopri come creare un percorso utilizzando un evento di business e quali best practice applicare.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
