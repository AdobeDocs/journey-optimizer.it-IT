---
solution: Journey Optimizer
product: journey optimizer
title: Scegli un metodo di convalida
description: Confrontare Simulazione Percorso, Modalità test Percorso ed Esecuzione Percorso in prova e scegliere il metodo di convalida corretto per il percorso prima della pubblicazione.
feature: Journeys, Get Started, Test Profiles
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: test, simulazione, simulazione, modalità test, esecuzione in prova, percorso, convalida, confronto, scelta, guida alle decisioni
version: Journey Orchestration
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 0%

---


# Scegli un metodo di convalida {#choose-validation-method}

>[!BEGINSHADEBOX]

**In questa pagina:** confrontare simulazione Percorso, modalità Test Percorso ed esecuzione Percorso in prova. Scopri quale si adatta alla tua fase attuale di creazione di un percorso: da un’iterazione rapida durante la progettazione a un controllo pre-lancio finale rispetto al pubblico in tempo reale.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] offre tre modi per convalidare un percorso prima della pubblicazione. Non sono intercambiabili: ognuno usa un tipo di dati diverso, si adatta a una fase diversa della tua build e comporta conseguenze diverse nel mondo reale. Comprendere la differenza fin dall’inizio ti aiuta a evitare due errori comuni. Il primo consiste nel trascorrere del tempo a creare profili di test quando una simulazione rapida può funzionare. Il secondo presuppone che un passaggio di convalida sia completamente &quot;sicuro&quot; quando può ancora contattare caselle in entrata reali o effettuare chiamate in uscita reali.

Questa pagina si concentra sulla convalida del flusso di percorso e della logica di diramazione. Per un quadro completo delle funzionalità di test e approvazione, inclusi anteprima del contenuto, rendering di e-mail e controlli di posta indesiderata, esperimenti A/B e flussi di lavoro di approvazione, vedere [Test, convalida e approvazione](../../rp_landing_pages/test-landing-page.md).

## Sei nuovo alla convalida? Inizia qui {#quick-pick}

Se non sei sicuro del metodo applicabile, rispondi a questa domanda:

* **Sto ancora progettando il mio percorso e desidero convalidare rapidamente la logica di un ramo, senza creare profili di test.** → Utilizzare **[Simulazione Percorso](simulate-journey-gs.md)**.
* **Desidero convalidare manualmente la logica del percorso bozza passo dopo passo, utilizzando profili di test reali (ma designati).** → Utilizzare **[Modalità test Percorso](testing-the-journey.md)**.
* **Sto per pubblicare e voglio un controllo finale dei volumi previsti rispetto al mio pubblico di produzione reale, senza contattare nessuno.** → Usare **[Percorso di prova](journey-dry-run.md)**.

Non sei ancora sicuro, o vuoi il quadro completo? Continua a leggere — ogni metodo è descritto in dettaglio di seguito.

## I tre metodi di convalida {#validation-methods}

>[!BEGINTABS]

>[!TAB Simulazione Percorsi]

**Quando utilizzare:** Iterazione rapida durante la progettazione del percorso, in particolare prima di una scadenza o durante il test di nuovi rami o percorsi. Inoltre, funziona bene come metodo di convalida continuo quando la creazione di un profilo di test appropriato per il tuo caso d’uso non è pratica.

[La simulazione dei Percorsi](simulate-journey-gs.md) convalida il percorso con utenti simulati temporanei. Non è necessario creare o attendere la propagazione di profili di test Adobe Experience Platform (AEP) reali. Puoi creare manualmente gli utenti simulati, oppure consentire all’intelligenza artificiale di generare automaticamente gli eventi di test di cui il percorso ha bisogno e di farli corrispondere agli utenti simulati giusti, attivando il percorso in pochi secondi.

Meccanica chiave:

* Gli utenti simulati non sono profili reali in AEP; puoi anche salvarli nel [inventario](simulate-journey.md#test-users) per riutilizzarli nelle simulazioni future invece di crearli ogni volta da zero.
* I criteri di uscita, i criteri di consenso, la limitazione di frequenza/percorso, la rinuncia/soppressione e le ore non interattive non vengono valutati.
* Le azioni personalizzate e le chiamate a origini dati esterne effettuano ancora vere chiamate in uscita, non vengono beffate.

>[!IMPORTANT]
>
>La simulazione invia messaggi reali agli [indirizzi di esecuzione](simulate-journey.md#test-users) (e-mail, telefono, token push) configurati sugli utenti simulati, ad esempio il tuo indirizzo e-mail. Utilizza la stessa pipeline di consegna della produzione. Non contatta clienti reali o aggiorna i dati del profilo live, ma i messaggi stessi sono reali.

**Ideale per:** Convalida di un nuovo ramo (ad esempio, due nuovi percorsi dei criteri di decisione) senza attendere la propagazione del profilo di test di AEP.

➡️ [Introduzione alla simulazione del percorso](simulate-journey-gs.md) | [Simula il tuo percorso](simulate-journey.md)

>[!TAB Modalità test Percorsi]

**Quando utilizzare:** verifica manuale della logica di ramo e messaggio passo dopo passo, con profili di test reali (ma designati) che attraversano il percorso di bozze.

[Modalità di test Percorsi](testing-the-journey.md) consente di convalidare un percorso bozza utilizzando [Profili di test AEP](../audience/creating-test-profiles.md) persistenti. Per confermare che la logica di ramificazione e la meccanica di consegna dei messaggi funzionino come progettato prima che qualsiasi pubblico di produzione tocchi il percorso, attiva manualmente gli eventi dall’interfaccia.

Meccanica chiave:

* Solo i profili contrassegnati come &quot;profili di test&quot; in Real-Time Customer Profile possono accedere a un percorso in modalità di test Percorso.
* La modalità Test percorso è disponibile solo per i percorsi bozza che utilizzano uno spazio dei nomi [&#128279;](../audience/get-started-identity.md), poiché deve verificare in AEP se una persona è un profilo di test.
* Un massimo di 100 profili di test può entrare in un percorso durante una singola sessione di test e gli eventi possono essere attivati solo dall’interfaccia, non da sistemi esterni tramite API.
* La disattivazione della modalità di test Percorso rimuove tutti i profili che sono entrati nel percorso e cancella i rapporti.

>[!IMPORTANT]
>
>La modalità di test del percorso invia messaggi reali alle caselle in entrata effettive dei profili di test, utilizzando la stessa pipeline di consegna della produzione. Non contatta clienti reali, ma non si tratta neanche di una simulazione &quot;a secco&quot;: assicurati che i profili di test utilizzino gli indirizzi che controlli.

**Punto critico:** La creazione e la propagazione di nuovi profili di test di AEP richiede tempo. [Simulazione Percorso](simulate-journey-gs.md) offre un&#39;alternativa rapida che non richiede alcun profilo di test. È utile non solo in attesa che i profili si propaghino, ma non è pratico creare in qualsiasi momento un profilo di test appropriato per il caso d’uso.

➡️ [Verifica il percorso](testing-the-journey.md)

>[!TAB Percorso di prova]

**Quando utilizzare:** un controllo finale e realistico della produzione subito prima della pubblicazione.

[Percorso di prova](journey-dry-run.md) è una modalità speciale di pubblicazione del percorso che esegue il percorso rispetto al pubblico di produzione reale e ai dati di segmentazione, senza contattare clienti reali o aggiornare le informazioni del profilo. Il percorso si attiva come un percorso live e i profili passano attraverso rami e nodi esattamente come farebbero in produzione. Tuttavia, [nodi azione](about-journey-activities.md) quali e-mail, SMS e azioni personalizzate vengono ignorati.

Meccanica chiave:

* Utilizza il pubblico di produzione effettivo, in modo da visualizzare la portata reale e il targeting su larga scala (ad esempio, individuare un bug in cui un intero ramo riceve inaspettatamente zero profili).
* A ogni attivazione, per recuperare più rapidamente le metriche puoi disabilitare le attività di attesa e mantenere il percorso completamente isolato puoi disabilitare le chiamate a origini dati esterne.
* La funzionalità **Disponibilità limitata** è attualmente in fase di rollout a livello globale nel tempo.

**Ideale per:** Rilevare problemi come nodi di condizione digitati in modo errato o tipi di pubblico che non raggiungono in modo imprevisto un ramo, immediatamente prima di capovolgere il percorso dal vivo.

➡️ [Esecuzione in prova per Percorsi](journey-dry-run.md)

>[!ENDTABS]

## Quale metodo si deve utilizzare? {#decision-guide}

Inizia con una semplice domanda: hai già profili di test adatti al tuo caso d’uso? In caso affermativo, la modalità di test **Percorso** ti consente di convalidarla passo dopo passo. In caso contrario, o se non è possibile crearli per questo particolare caso d&#39;uso, **la simulazione dei Percorsi** ti fa convalidare in secondi.

Al di là di questa scelta, la risposta in genere si riduce a un&#39;altra domanda: *quanto è vicino alla produzione questo test?*

Se stai ancora **iterando nella progettazione del percorso** — testando un nuovo ramo, lavorando in base a una scadenza — utilizza **Simulazione del Percorso**. Non ha bisogno di profili reali ed è in esecuzione in secondi. Resta inoltre una scelta valida in un secondo momento della build, ogni volta che non è pratico creare profili di test adatti al tuo caso d’uso. Ricordati che invia messaggi reali agli indirizzi di esecuzione configurati sugli utenti simulati.

Se devi **verificare manualmente il ramo e la logica dei messaggi passo dopo passo** e sei disposto a creare o riutilizzare i profili di test di AEP, utilizza **Modalità test Percorso**. Ricorda solo che invia messaggi reali alle caselle in entrata reali dei profili di test.

Se stai per **pubblicare** e desideri un controllo finale dei volumi previsti rispetto al pubblico di produzione effettivo, utilizza **Percorso di prova**. Non contatta mai nessuno o modifica i dati del profilo.

>[!TIP]
>
>**Non sei sicuro di dove iniziare?** La maggior parte dei team utilizza la **simulazione Percorso** durante la generazione, quindi un&#39;esecuzione di prova di **Percorso** immediatamente prima della pubblicazione. Raggiungi **Modalità test Percorso** quando devi eseguire manualmente la logica di ramo con profili di test reali anziché simulati.

## Confronto rapido {#quick-comparison}

| Metodo | Dati utilizzati | Invia messaggi reali? | Ideale per |
|---|---|---|---|
| [Simulazione Percorsi](simulate-journey-gs.md) | Utenti simulati temporanei, creati manualmente o generati automaticamente | Sì: agli indirizzi di esecuzione configurati sugli utenti simulati | Iterazione rapida su nuovi rami o percorsi, senza attendere la propagazione del profilo di test reale |
| [Modalità test Percorsi](testing-the-journey.md) | Profili di test di AEP persistenti | Sì: per passare alle caselle in entrata effettive dei profili di test, utilizzando la pipeline di consegna di produzione | Verifica manuale della logica di ramo/messaggio passo dopo passo in un percorso in versione bozza |
| [Percorso di prova](journey-dry-run.md) | Pubblico/dati di produzione reale | No (azioni ignorate) | Verifica finale, prima del lancio, della portata del pubblico, del targeting e della logica di ramo effettivi su scala reale |

Nessuno di questi metodi contatta clienti reali. Anche i dati di profilo vengono lasciati intatti in ogni caso, con la differenza che la modalità Test di Percorso aggiorna i profili di test utilizzati per eseguirli (non i profili cliente reali).

## Errori comuni da evitare {#common-mistakes}

* **La simulazione del Percorso è completamente &quot;sicura&quot;.** È il modo più veloce per eseguire il test, ma invia comunque messaggi reali all’indirizzo di esecuzione configurato su ogni utente simulato, di solito la tua casella in entrata. Non presumere che non venga inviato nulla.
* **Creazione dei profili di test di AEP quando dovrebbe essere eseguita la simulazione del Percorso.** Se devi solo convalidare rapidamente un nuovo ramo o percorso di criteri decisionali, la simulazione evita completamente l’attesa della propagazione del profilo di test, salvando la modalità di test Percorso per i casi in cui siano effettivamente necessari profili di test reali.
* **Trattamento della modalità di test Percorso come &quot;dry&quot;** I profili della modalità di test del percorso ricevono messaggi reali tramite la pipeline di consegna della produzione. Assicurati che i profili di test utilizzino solo gli indirizzi controllati.
* **Prevista esecuzione di prova del Percorso per rilevare il contenuto o problemi di consegna.** L’esecuzione a secco ignora completamente i nodi di azione: convalida la logica di diffusione e diramazione del pubblico, non il contenuto dei messaggi o la meccanica di consegna. Utilizza la modalità Simulazione o Test Percorso.
* **Dimenticamento del requisito dello spazio dei nomi per la modalità Test Percorso.** La modalità Test percorso funziona solo su percorsi bozza che utilizzano uno spazio dei nomi, perché Journey Optimizer necessita di uno spazio dei nomi per verificare se un profilo è contrassegnato come profilo di test.

## Passaggi successivi {#next-steps}

* **[Introduzione alla simulazione di percorso](simulate-journey-gs.md)** — Eseguire la prima simulazione
* **[Verifica il percorso](testing-the-journey.md)** - Attiva la modalità di test del Percorso con i profili di test di AEP
* **[Percorso di esecuzione di prova](journey-dry-run.md)** — Esecuzione di un&#39;esecuzione di prova realistica per la produzione
* **[Pubblicare il percorso](publish-journey.md)** — Prerequisiti e processo di pubblicazione
* **[Introduzione ai percorsi](journey.md)**: panoramica su nozioni di base e funzionalità
* **[Domande frequenti su Journey Orchestration](journey-faq.md)** — Risposte alle domande comuni
* **[Test, convalida e approvazione](../../rp_landing_pages/test-landing-page.md)**: scenario completo di test e approvazione, inclusi anteprima del contenuto, controlli di rendering/posta indesiderata, esperimenti e flussi di lavoro di approvazione

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-choose-validation-method.md}}
