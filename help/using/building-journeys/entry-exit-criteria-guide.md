---
solution: Journey Optimizer
product: journey optimizer
title: Criteri percorsi di entrata e di uscita
description: Scopri come gestire in modo efficace il momento in cui i profili entrano nei percorsi e ne escono, con esempi reali e best practice
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: entrata, uscita, criteri, percorso, profilo, rientro, best practice
version: Journey Orchestration
source-git-commit: 970712614b0d4da37d9ecbe45701f93147b1428c
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 1%

---


# Utilizzare i criteri di ingresso e uscita del percorso {#entry-exit-criteria-guide}

Nell’orchestrazione dell’esperienza del cliente, la distribuzione del messaggio giusto al momento giusto richiede un controllo preciso su quando i clienti entrano nei percorsi e ne escono. Comprendere e configurare correttamente i criteri di ingresso e uscita può fare la differenza tra una campagna di successo e coinvolgente e le opportunità mancate o l’eccesso di messaggi.

Questa guida fornisce indicazioni pratiche, esempi pratici e best practice per la gestione dei criteri di entrata e uscita dal percorso in Adobe Journey Optimizer.

## Quali sono i criteri di entrata e di uscita? {#what-are-criteria}

**I criteri di ingresso** determinano le condizioni in cui un [profilo cliente](../audience/get-started-profiles.md) è idoneo per l&#39;immissione di un percorso specifico. I profili possono essere immessi in base a:

* **[Comportamento del cliente](../event/about-events.md)** - Le azioni intraprese dai clienti attivano l&#39;immissione del percorso in tempo reale, ad esempio effettuando un acquisto, abbandonando un carrello o aprendo la tua app mobile.

* **[Attributi del profilo](../audience/get-started-profiles.md)** - Le caratteristiche del cliente determinano l&#39;idoneità in base ai dati memorizzati nel suo profilo, come il livello di fedeltà, la posizione, l&#39;età o le preferenze di comunicazione.

* **[Eventi esterni](../event/about-creating-business.md)** - Trigger aziendali o ambientali che interessano più clienti contemporaneamente, ad esempio avvisi di inventario ridotti, condizioni meteorologiche o variazioni di prezzo.

* **[Iscrizione al pubblico](../audience/about-audiences.md)** - L&#39;appartenenza a un segmento di pubblico specifico abilita percorsi mirati per gruppi come clienti di alto valore, utenti inattivi o nuovi abbonati.

**Criteri di uscita** definiscono quando e come un profilo lascia o viene rimosso da un percorso:

* **Completamento Percorso** - I profili escono automaticamente quando raggiungono la [fine di tutti i percorsi di percorso](end-journey.md), completando l&#39;esperienza progettata.

* **Metrica di successo**: i profili vengono chiusi quando completano l&#39;obiettivo di [percorso](success-metrics.md), ad esempio effettuando un acquisto o scaricando un&#39;app, eliminando le comunicazioni di follow-up non necessarie.

* **Basato su condizione** - I profili vengono chiusi quando vengono soddisfatte [condizioni specifiche](condition-activity.md), ad esempio inattività in un periodo impostato o modifiche negli attributi del profilo.

* **Basato su evento** - I profili vengono chiusi quando si verificano [eventi specifici](../event/about-events.md), ad esempio l&#39;annullamento della sottoscrizione o la restituzione del prodotto.

* **Squalifica del pubblico** - I profili escono quando non soddisfano più i [criteri del pubblico di destinazione](../audience/about-audiences.md), garantendo che i messaggi rimangano pertinenti.

## Perché i criteri di entrata e di uscita contano {#why-they-matter}

La corretta definizione dei criteri di entrata e uscita offre un valore aziendale significativo:

* **Rilevanza**: solo i clienti giusti entrano nel percorso, aumentando i tassi di coinvolgimento e conversione eseguendo il targeting del pubblico più appropriato al momento ottimale.

* **Efficienza**: impedisce ai clienti di rimanere in percorsi irrilevanti, riducendo comunicazioni non necessarie, costi operativi e fastidio per i clienti.

* **Personalization**: consente la personalizzazione dinamica delle esperienze in base a dati e comportamenti in tempo reale, creando interazioni cliente più significative.

* **Conformità**: consente di gestire i limiti di frequenza ed evitare comunicazioni eccessive, rispettando le preferenze dei clienti e i requisiti normativi e mantenendo al contempo la reputazione del marchio.

## Esempi reali di entrata e uscita dal percorso {#real-world-examples}

Di seguito sono riportati scenari comuni che dimostrano come i criteri di entrata e di uscita funzionano nella pratica:

**Campagna di benvenuto per i nuovi abbonati**

* **Voce**: i profili entrano nel percorso quando si abbonano a una newsletter
* **Uscita**: i profili escono una volta completata una serie di e-mail di benvenuto o dopo un determinato periodo di tempo se non interagiscono
* **Vantaggio**: assicura che i nuovi abbonati ricevano l&#39;onboarding tempestivo evitando messaggi ripetitivi

**Ripristino carrello abbandonato**

* **Voce**: i clienti entrano nel percorso se aggiungono elementi a un carrello ma non completano l&#39;estrazione entro 24 ore
* **Uscita**: i profili escono quando completano l&#39;acquisto o dopo 7 giorni se non viene effettuato alcun acquisto
* **Vantaggio**: guida le conversioni tramite promemoria tempestivi senza inviare spam a clienti non interessati

**Programma fedeltà**

* **Voce**: i clienti partecipano al percorso dopo aver raggiunto una determinata soglia di punti fedeltà
* **Uscita**: i profili escono dopo aver rimborsato i premi o se sono inattivi per 60 giorni
* **Vantaggio**: mantiene i clienti di alto valore coinvolti in offerte personalizzate ed evita l&#39;affaticamento della comunicazione

**Raccolta feedback prodotto**

* **Voce**: i clienti entrano nel percorso dopo aver ricevuto un evento di conferma della consegna del prodotto
* **Uscita**: i profili escono una volta inviato il feedback o dopo 10 giorni in assenza di risposta
* **Vantaggio**: acquisisce tempestivamente un feedback prezioso senza disturbare i clienti con richieste persistenti

## Come configurare i criteri di immissione percorsi {#configure-entry}

>[!BEGINSHADEBOX]

**Scopri tutto quello che devi sapere sui criteri di ingresso qui:**

* **[Attivatori basati su eventi](../event/about-events.md)**: utilizza eventi come &quot;creazione profilo&quot;, &quot;transazione completata&quot; o eventi personalizzati per avviare un percorso. [Configura gli eventi](../event/about-creating.md) in **[!UICONTROL Amministrazione]** > **[!UICONTROL Eventi]**, definisci [lo schema e i campi dell&#39;evento](../event/experience-event-schema.md), quindi aggiungi l&#39;evento dalla palette **[!UICONTROL Eventi]** nella [finestra di progettazione del percorso](using-the-journey-designer.md).

* **[Voce basata sul pubblico](read-audience.md)**: esegui il targeting di percorsi di profili che appartengono a tipi di pubblico specifici, come batch occasionale o secondo una pianificazione ricorrente. [Crea tipi di pubblico](../audience/creating-a-segment-definition.md) nel menu **[!UICONTROL Tipi di pubblico]**, quindi aggiungi un&#39;attività **[!UICONTROL Read audience]** e [configura la pianificazione](journey-properties.md#schedule).

* **[Voce Qualificazione pubblico](audience-qualification-events.md)**: attiva i percorsi in cui i profili si qualificano o escono da un pubblico specifico in tempo reale. Definisci [tipi di pubblico in streaming](../audience/about-audiences.md), aggiungi un evento **[!UICONTROL Qualifica pubblico]** dalla palette **[!UICONTROL Eventi]** e scegli il tipo di trigger.

* **[Filtri per attributi](condition-activity.md)**: perfeziona i criteri di immissione combinando eventi o tipi di pubblico con attributi di profilo e contesto utilizzando la logica AND/OR. Utilizza [condizioni](conditions.md) per fare riferimento a [attributi di profilo](../audience/get-started-profiles.md), eventi o [dati esterni](../datasource/about-data-sources.md).

* **[Intervalli di tempo e pianificazione](journey-properties.md#schedule)**: impostare vincoli temporali per mantenere i percorsi aggiornati e rilevanti. Configura le [pianificazioni per le attività Read Audience](read-audience.md), utilizza le [attività Wait](wait-activity.md) e aggiungi [condizioni basate sul tempo](conditions.md) per controllare la tempistica.

>[!ENDSHADEBOX]

## Come impostare i criteri di uscita dal percorso {#configure-exit}

>[!BEGINSHADEBOX]

**Scopri tutto quello che devi sapere sui criteri di uscita qui:**

* **[Completamento Percorso](end-journey.md)**: i profili escono automaticamente dopo aver raggiunto il passaggio del percorso finale. Progetta i percorsi del percorso che termineranno alle **[!UICONTROL Attività finali]**.

* **[Success Metric Achievement](journey-properties.md#exit-criteria)**: definisci le metriche di successo (come acquisto o abbonamento) e i profili di uscita al termine. Fai clic sull&#39;icona **[!UICONTROL Mostra criteri di uscita]**, seleziona **[!UICONTROL Aggiungi criteri di uscita]**, quindi scegli un [Evento](../event/about-events.md) o [Pubblico](../audience/about-audiences.md) come trigger di uscita.

* **[Timeout inattività](wait-activity.md)**: uscire dai profili se non si verifica alcun coinvolgimento entro un intervallo di tempo impostato. Utilizza [Criteri di uscita](journey-properties.md#exit-criteria) con tipi di pubblico che controllano la data dell&#39;ultimo impegno, imposta [Attività di attesa](wait-activity.md) con durate definite e utilizza [condizioni](condition-activity.md) per verificare la presenza di attività.

* **[Regole di reinserimento](entry-management.md)**: decidere se i profili possono rientrare nel percorso più volte o una sola volta, a seconda della strategia della campagna. Configura le impostazioni di **[!UICONTROL Rientro]** nel percorso **[!UICONTROL Proprietà]** per impostare i periodi di attesa, abilitare il rientro forzato o utilizzare [identificatori supplementari](supplemental-identifier.md) per il rientro specifico del contesto.

>[!ENDSHADEBOX]

## Esempi dettagliati di percorso {#journey-examples}

Per istruzioni dettagliate sull’implementazione, complete di dettagli tecnici, consulta i seguenti casi d’uso documentati:

* **[percorso di onboarding clienti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** - Crea esperienze di benvenuto personalizzate con qualificazione del pubblico, timeout di eventi ed uscite basate su obiettivi

* **[Ripristino carrello abbandonato](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** - Recupero delle vendite perse con percorsi attivati da eventi, playbook e routing dei canali

* **[Campagne di ricoinvolgimento](https://experienceleague.adobe.com/it/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** - Recupera i clienti inattivi con targeting comportamentale e attivazione di elementi multimediali a pagamento

* **[Invia messaggi agli abbonati](message-to-subscribers-uc.md)** - Elenchi di abbonamenti di Target con pubblico di lettura e contenuti personalizzati

* **[Invio di messaggi multicanale](journeys-uc.md)** - Combina e-mail e push con eventi di reazione e logica a percorsi multipli

* **[Invia e-mail solo nei giorni feriali](weekday-email-uc.md)** - Pianifica le comunicazioni utilizzando condizioni basate sul tempo e formule di attesa

>[!TIP]
>
>Sfoglia tutti i casi d&#39;uso disponibili nella libreria dei casi d&#39;uso di [ Percorsi](jo-use-cases.md) per altri modelli e implementazioni, tra cui [aumento graduale delle consegne](ramp-up-deliveries-uc.md), [modelli di eventi esperienza](exp-event-lookup.md) e [rimozione di profili da percorsi live](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey).

## Best practice per la gestione di entrata e uscita {#best-practices}

**Cancella definizione**

* Documenta la logica di entrata e uscita prima di creare percorsi per allineare i team di marketing e analisi
* Creazione di diagrammi di flusso che mostrano punti di ingresso, percorsi di percorso e condizioni di uscita
* Definisci chiaramente le regole aziendali: &quot;I profili escono quando X si verifica O dopo Y giorni&quot;
* Utilizza etichette descrittive: &quot;Esci - Acquisto completato&quot; non &quot;Esci 1&quot;
* [Assegna tag ai percorsi](../start/search-filter-categorize.md#tags) in modo coerente per la generazione di rapporti e l&#39;applicazione di filtri

**Evita percorsi sovrapposti**

* [Controlla i percorsi attivi](journey-ui.md) prima di avviarne altri simili per evitare conflitti
* Sfrutta [gestione dei conflitti](../conflict-prioritization/conflicts.md) e [punteggi di priorità](../conflict-prioritization/priority-scores.md) per risolvere le sovrapposizioni e assegnare priorità ai percorsi
* Progettazione di percorsi complementari e non in concorrenza

>[!NOTE]
>
>Per scenari avanzati come la rimozione automatica dei profili quando sono idonei per percorsi con priorità più elevata, utilizza [Limitazione percorsi e arbitrato](../conflict-prioritization/journey-capping.md) invece dei criteri di uscita.

**Monitora e ottimizza**

* Tieni traccia della percentuale di ingresso, della percentuale di uscita e della percentuale di completamento per ogni percorso utilizzando [rapporti percorso](../reports/journey-global-report-cja.md)
* Monitora [metriche di successo](success-metrics.md): percentuale di uscita tramite completamento metrica di successo rispetto al timeout
* [Verifica i criteri di entrata e uscita](testing-the-journey.md) con vari scenari di profilo prima dell&#39;avvio
* Regolare in base ai dati: se si esce anticipatamente con un numero elevato di partecipanti, rivedi la rilevanza dei criteri di immissione; se la metrica di completamento ha un numero ridotto di partecipanti, analizza contenuto e tempistica
* Rivedi tutti i percorsi attivi trimestralmente

**Rispetta i limiti di frequenza**

* Imposta [periodi di attesa per il rientro](entry-management.md) appropriati o disattiva il rientro per percorsi occasionali
* Utilizza [regole di quota limite](../conflict-prioritization/rule-sets.md) per evitare comunicazioni eccessive
* Monitorare le metriche di frequenza nel reporting per garantire la conformità

>[!NOTE]
>
>Per gestire i limiti di frequenza e i limiti di ingresso del percorso in più percorsi, utilizzare [Limitazione percorsi e arbitrato](../conflict-prioritization/journey-capping.md) e [Limitazione frequenza per canale](../conflict-prioritization/channel-capping.md).

## Conclusione {#conclusion}

I criteri di ingresso e uscita dal percorso sono fondamentali per offrire ai clienti esperienze personalizzate, tempestive ed efficaci con Adobe Journey Optimizer. Creando attentamente queste condizioni, gli esperti di marketing possono incrementare il coinvolgimento, ridurre gli attriti e creare relazioni più solide con i clienti.

Inizia mappando chiaramente i trigger del cliente e i punti di uscita, eseguendo test approfonditi e monitorando i risultati per perfezionare continuamente l’orchestrazione del percorso.

## Risorse correlate {#related-resources}

**Documentazione tecnica**

* [Gestione dell&#39;ingresso al profilo](entry-management.md) - Guida tecnica dettagliata per i controlli di ingresso
* [Proprietà Percorso e criteri di uscita](journey-properties.md) - Riferimento completo alla configurazione
* [Fine dei percorsi](end-journey.md) - Gestione del ciclo di vita del Percorso
* [Identificatori supplementari](supplemental-identifier.md) - Scenari di rientro avanzati
* [Progettazione Percorsi](using-the-journey-designer.md) - Genera e progetta percorsi

**Esercitazioni ed esempi**

* [Casi d&#39;uso per i Percorsi](jo-use-cases.md) - Esempi e modelli di percorso completi
* [Video sull&#39;onboarding dei clienti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* [Video carrello abbandonato](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* [Blog della community: criteri di ingresso e uscita](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958)

**Funzionalità correlate**

* [Eventi di qualificazione del pubblico](audience-qualification-events.md)
* [Metriche e obiettivi di successo](success-metrics.md)
* [Gestione dei conflitti](../conflict-prioritization/conflicts.md)
* [Quota limite](../conflict-prioritization/rule-sets.md)
* [Percorsi di prova](testing-the-journey.md)
* [Attività Condizione](condition-activity.md)
* [Eventi di reazione](reaction-events.md)
* [Attività Attendi](wait-activity.md)
