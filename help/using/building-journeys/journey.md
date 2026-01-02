---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai percorsi
description: Introduzione ai percorsi
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: percorsi, scopri, inizia
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: a4b6b048d60847531e0e61de702b48ebe82884d3
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 3%

---


# Introduzione ai percorsi{#jo-general-principle}

Adobe Journey Optimizer ti consente di creare percorsi di clienti personalizzati e a più passaggi che si adattano in tempo reale al comportamento e alle esigenze del pubblico. Utilizzando un’area di lavoro intuitiva basata su trascinamento, puoi orchestrare messaggi e azioni tra più canali, sfruttando i dati contestuali e il targeting del pubblico per il massimo impatto.

Questa guida fornisce una roadmap chiara per aiutarti a comprendere le nozioni di base del percorso, scegliere il tipo di percorso adatto al tuo caso d’uso e progettare con sicurezza percorsi che forniscano esperienze cliente significative e tempestive.

## Cosa sono i percorsi?

**Percorsi** sono esperienze cliente automatizzate e a più passaggi che orchestrano interazioni personalizzate tra canali in risposta al comportamento del cliente, a eventi di business o a campagne pianificate.

Utilizza [!DNL Journey Optimizer] per:

* Crea **orchestrazione in tempo reale** casi d&#39;uso utilizzando dati contestuali archiviati in eventi o origini dati
* Progetta **scenari avanzati a più passaggi** che rispondono in modo dinamico al comportamento del cliente e agli eventi di business
* Distribuisci **1:1 esperienze personalizzate** su larga scala tramite e-mail, push, SMS, in-app, web e altro ancora

![Interfaccia di Progettazione Percorsi con riquadro palette, area di lavoro e proprietà](assets/journey38.png)

➡️ **Inizio generazione?** [Crea il tuo primo percorso](journey-gs.md) in 5 minuti.

## Scegli il tipo di percorso {#journey-types}

**Prima di iniziare a generare**, è importante capire quale tipo di percorso si adatta al tuo caso d&#39;uso. Adobe Journey Optimizer supporta quattro tipi di percorsi, ciascuno progettato per diversi meccanismi di ingresso e scenari aziendali:

>[!BEGINTABS]

>[!TAB percorsi unitari]

**Quando utilizzare:** esperienze in tempo reale attivate da eventi

**I percorsi unitari** vengono attivati singolarmente quando si verifica un&#39;azione specifica (acquisto, accesso all&#39;app, invio di moduli). I profili vengono inseriti uno alla volta in tempo reale, rendendolo ideale per risposte immediate e basate sul comportamento.

**Ideale per:** ordinare conferme dopo l&#39;acquisto, e-mail di benvenuto quando qualcuno si abbona, abbandono del carrello attivato dalla navigazione e notifiche di reimpostazione della password.

➡️ [Informazioni sugli eventi](../event/about-events.md) | [Caso di utilizzo: messaggio agli abbonati](message-to-subscribers-uc.md)

>[!TAB Leggi percorsi di pubblico]

**Quando utilizzare:** campagne pianificate per i segmenti di pubblico

**Leggi percorsi di pubblico** inizia con un pubblico Adobe Experience Platform e invia messaggi in batch a tutti i profili contemporaneamente. Questo percorso è ideale per comunicazioni pianificate su larga scala.

**Ideale per:** newsletter mensili, campagne promozionali per segmenti di destinazione, annunci di prodotti e campagne di marketing stagionali.

➡️ [Scopri il pubblico in lettura](read-audience.md) | [Introduzione ai tipi di pubblico](../audience/about-audiences.md)

>[!TAB percorsi di qualificazione del pubblico]

**Quando utilizzare:** le risposte in tempo reale alle modifiche di iscrizione al pubblico

**I percorsi di qualificazione del pubblico** si attivano quando i profili si qualificano per un pubblico specifico (o ne escono). I profili vengono inseriti singolarmente in quanto soddisfano i criteri in tempo reale, consentendo un coinvolgimento immediato quando il comportamento del cliente cambia.

**Ideale per:** notifiche di aggiornamento a livello VIP, nuovo coinvolgimento quando i clienti diventano inattivi, messaggi di festeggiamento del primo acquisto e targeting geografico quando i clienti si spostano.

➡️ [Scopri le qualificazioni per il pubblico](audience-qualification-events.md) | [Creazione di tipi di pubblico](../audience/creating-a-segment-definition.md)

>[!TAB percorsi di eventi di business]

**Quando utilizzare:** condizioni aziendali che interessano più clienti

**I percorsi di eventi aziendali** sono attivati da eventi a livello aziendale (aggiornamenti delle scorte, avvisi meteo, variazioni di prezzo) che interessano più profili contemporaneamente. Questi rispondono a condizioni di business più ampie piuttosto che ad azioni individuali.

**Ideale per:** avvisi di inventario ridotti per i clienti interessati, annunci di vendita flash, promozioni basate su meteo, notifiche di calo dei prezzi e avvisi di back-in-stock dei prodotti.

➡️ [Informazioni sugli eventi di business](../event/about-creating-business.md) | [Gestione delle voci](entry-management.md)

>[!ENDTABS]

>[!NOTE]
>
>Non sei sicuro del tipo da scegliere? Inizia con **percorsi unitari** per le esperienze basate su eventi o **Leggi percorsi di pubblico** per le campagne pianificate; questi riguardano i casi d&#39;uso più comuni.

## Creare con il progettista del percorso {#journey-designer}

**[Progettazione percorsi](using-the-journey-designer.md)** è l&#39;area di lavoro visiva per la creazione di esperienze cliente. Grazie all&#39;intuitiva interfaccia di trascinamento, è possibile orchestrare ogni passaggio del percorso senza scrivere codice.

![Interfaccia di Progettazione Percorsi con riquadro palette, area di lavoro e proprietà](assets/journey38.png)

### Operazioni possibili nella finestra di progettazione:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Definisci i punti di ingresso**

Scegli come i clienti inseriscono: attraverso un evento, un segmento di pubblico o una qualificazione del pubblico.

[Informazioni sulla gestione delle voci](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Inviare messaggi**

Utilizza azioni di canale integrate per e-mail, push, SMS/MMS, in-app, web e altro, tutte progettate in Journey Optimizer.

[Inviare messaggi in percorsi](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Aggiungi logica e condizioni**

Crea un ramo del percorso in base agli attributi del profilo, all’iscrizione al pubblico o a eventi in tempo reale.

[Condizioni d’uso](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Sfruttare i dati**

Utilizza dati contestuali provenienti da eventi, Adobe Experience Platform o servizi API di terze parti.

[Utilizzare le origini dati](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Connetti sistemi esterni**

Crea azioni personalizzate per integrare sistemi di terze parti per l’invio di messaggi o l’attivazione di flussi di lavoro.

[Utilizzare le azioni personalizzate](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Aggiungi attività di orchestrazione**

Utilizza tempi di attesa, salti, aggiornamenti del profilo e gestione dell&#39;audience per creare flussi sofisticati.

[Esplora tutte le attività](about-journey-activities.md)
:::

::::

➡️ **Apprendimento pratico:** [Guarda il video di Progettazione percorsi](#video) o [esplora casi d&#39;uso end-to-end](jo-use-cases.md)

## Flusso di lavoro di creazione del percorso {#workflow}

La creazione di percorsi di successo segue un processo chiaro e ripetibile. Di seguito è riportato il flusso di lavoro dettagliato:

**1. Piano** → **2. Progettazione** → **3. Test** → **4. Pubblica** → **5. Monitora** → **6. Ottimizza**

### &#x200B;1. Pianificare il percorso {#plan}

Prima di aprire la finestra di progettazione, specificare gli obiettivi:

* **Qual è l&#39;obiettivo?** (ad esempio, per integrare nuovi clienti, coinvolgere nuovamente gli utenti inattivi)
* **Chi è il pubblico?** (segmento specifico, singoli utenti guidati da eventi)
* **Quale tipo di percorso è adatto?** (vedi [Tipi di percorso](#journey-types) sopra)
* **Quali canali utilizzerai?** (e-mail, push, SMS, ecc.)

### &#x200B;2. Progettazione nel quadro {#design}

Utilizza Progettazione percorsi per generare il flusso:

1. **Imposta condizioni di ingresso** - Definisci come entrano i profili (evento, pubblico, qualifica)
2. **Aggiungi logica di orchestrazione** - Include tempi di attesa, condizioni e punti decisionali
3. **Configura messaggi** - Progetta le comunicazioni o sfrutta i modelli esistenti
4. **Imposta azioni** - Configura azioni predefinite o personalizzate da eseguire
5. **Definisci i criteri di uscita** - Specifica quando e come i profili completano il percorso

[Scopri come utilizzare la → di Progettazione percorsi](using-the-journey-designer.md)

### &#x200B;3. Eseguire il test prima della pubblicazione {#test}

Esegui sempre il test del percorso per individuare eventuali problemi prima che si verifichino:

* Utilizza la **modalità di test** per simulare il percorso con profili di test
* Utilizza **prova** per visualizzare in anteprima l&#39;esecuzione del percorso senza influire sui dati reali o inviare messaggi
* Verifica che tutte le condizioni, i messaggi e le azioni funzionino come previsto
* Controllare tempistica, flussi di dati e personalizzazione

[Verifica il percorso →](testing-the-journey.md) | [Informazioni sull&#39;esecuzione →](journey-dry-run.md)

### &#x200B;4. Pubblicare il percorso {#publish}

Una volta completato il test, pubblica per rendere attivo il percorso:

* Verifica impostazioni e proprietà finali
* Pubblica per attivare per clienti reali
* Nota: i percorsi live possono essere interrotti ma non modificati (è necessario creare una nuova versione)

[Pubblicare il → di percorso](publish-journey.md)

### &#x200B;5. Monitorare le prestazioni {#monitor}

Monitora le prestazioni del percorso nel mondo reale:

* Visualizzare report e analisi di percorso
* Monitorare l&#39;immissione, il completamento e le percentuali di errore
* Impostare gli avvisi per i problemi critici

[Monitora e segnala →](report-journey.md) | [Configura avvisi →](../reports/alerts.md)

### &#x200B;6. Ottimizzare e ripetere {#optimize}

Utilizza le informazioni per migliorare:

* Analizzare le metriche di coinvolgimento e i tassi di conversione
* Ottimizzazione del tempo di invio dei test
* Creazione di nuove versioni di percorso con miglioramenti
* Utilizzare consigli basati sull’intelligenza artificiale

[Ottimizza i percorsi →](optimize.md) | [Ottimizzazione dell&#39;ora di invio →](send-time-optimization.md)

➡️ **Inizio?** [Crea il tuo primo percorso ora →](journey-gs.md)

## Casi d’uso reali {#use-cases}

Scopri dagli esempi pratici che mostrano come applicare concetti di percorso per risolvere le problematiche di marketing comuni:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Nuovi abbonati**

Quando un cliente si abbona al servizio, attiva un percorso di benvenuto che li incoraggia a completare i passaggi di onboarding.

[Visualizza → del caso d’uso](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**Ottimizzazione dell&#39;ora di invio**

Utilizza l’intelligenza artificiale per inviare e-mail quando è più probabile che ogni cliente si interessi, massimizzando le percentuali di apertura e clic.

[Visualizza → del caso d’uso](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Incrementa le consegne**

Aumenta gradualmente il volume dei messaggi per migliorare la reputazione del mittente ed evitare problemi di recapito dei messaggi.

[Visualizza → del caso d’uso](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Destinazione per giorno feriale**

Inviare contenuti diversi in base al giorno della settimana in cui i clienti inseriscono il percorso, per maggiore rilevanza.

[Visualizza → del caso d’uso](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Campagne multicanale**

Organizza esperienze senza soluzione di continuità tra canali e-mail, push, SMS e web in un unico percorso.

[Visualizza → del caso d’uso](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Tutti i casi d&#39;uso**

Esplora la libreria completa dei casi di utilizzo del percorso con implementazioni dettagliate.

[Sfoglia tutte le →](jo-use-cases.md) | [Libreria casi d&#39;uso →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Esplora le funzionalità del percorso {#capabilities}

Man mano che acquisisci dimestichezza con la creazione del percorso, esplora queste potenti funzionalità per creare esperienze cliente sofisticate:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Espressioni avanzate**

Crea condizioni dinamiche e personalizzazione utilizzando l’editor di espressioni per la manipolazione dei dati e la logica complessa.

[Informazioni sulle espressioni](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**Gestione del fuso orario**

Gestisci i tipi di pubblico globali con regolazioni automatiche del fuso orario e tempi di invio ottimali.

[Gestire i fusi orari](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**Modalità di test ed esecuzione a secco**

Convalida i percorsi con i profili di test prima della pubblicazione e visualizza l’esecuzione dell’anteprima senza influire sui dati reali.

[Utilizzare la prova a secco](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Copia nella sandbox**

Duplica i percorsi tra sandbox per semplificare i flussi di lavoro di test e distribuzione.

[Copia percorsi](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Tag e organizzazione**

Utilizza i tag per categorizzare e filtrare i percorsi per una migliore gestione su larga scala.

[Organizzazione con tag](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Controllo velocità effettiva**

Limita la velocità effettiva dei messaggi per gestire la reputazione di invio ed evitare di sovraccaricare i sistemi.

[Velocità effettiva di controllo](limit-throughput.md)
:::

::::

[Visualizza tutte le funzionalità di percorso →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Imparare guardando {#video}

Ottieni un’introduzione visiva ai componenti di percorso e scopri le nozioni di base sulla creazione di percorsi nell’area di lavoro:

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **Desideri altri video?** [Esplora i tutorial video sul percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Hai bisogno di aiuto? {#help}

### Collegamenti rapidi per le attività comuni

* **[Crea il tuo primo percorso](journey-gs.md)** - Guida dettagliata per principianti
* **[Domande frequenti sui Percorsi](journey-faq.md)** - Risposte alle domande comuni
* **[Risoluzione dei problemi](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnosi e risoluzione dei problemi
* **[Riferimento codici errore](error-codes-reference.md)** - Comprendere i messaggi di errore
* **[Guardrail e limitazioni](../start/guardrails.md)** - Limiti tecnici e best practice

### Ricevi notifiche sui problemi

Configura **[avvisi di percorso](../reports/alerts.md)** per ricevere notifiche in tempo reale quando i percorsi rilevano errori o pattern insoliti.

### Risorse aggiuntive

* **[Hub gestione Percorsi](/help/rp_landing_pages/manage-journey-landing-page.md)** - Strumenti per filtrare, ottimizzare e gestire profili
* **[Riferimento attività Percorso](/help/rp_landing_pages/about-journey-building-landing-page.md)** - Guida completa a tutti i tipi di attività
* **[Risoluzione dei problemi di esecuzione](troubleshooting-execution.md)** - Debug dei problemi di esecuzione del percorso
* **[Risoluzione dei problemi relativi alle attività in entrata](troubleshooting-inbound.md)** - Correzione dei problemi di immissione e qualificazione

**Creare il primo percorso?** [Introduzione →](journey-gs.md)
