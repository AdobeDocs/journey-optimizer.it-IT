---
solution: Journey Optimizer
product: journey optimizer
title: Inviare e-mail solo nei giorni feriali
description: Scopri come configurare un percorso per inviare e-mail solo nei giorni feriali in [!DNL Adobe Journey Optimizer]
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: percorso, caso d’uso, giorni feriali, condizione, e-mail, pianificazione
version: Journey Orchestration
exl-id: 2f313e59-ee50-473c-9346-8859889346ec
TQID: https://experienceleague.adobe.com/qUt7t5LTYSQW278Pafx2-1t-DboRz9tU5IRpVhuEqLc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1622
ht-degree: 0%

---

# Inviare e-mail solo nei giorni feriali {#send-emails-only-on-weekdays}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come configurare un percorso che invia e-mail solo nei giorni feriali, accodando le voci del fine settimana per la consegna di lunedì utilizzando un&#39;attività condizione e le attività Attendi con formule personalizzate.

>[!ENDSHADEBOX]

Questo caso d&#39;uso illustra come configurare un percorso in [!DNL Adobe Journey Optimizer] che invia e-mail solo nei giorni feriali (dal lunedì al venerdì). Per i profili che entrano nel percorso nei fine settimana (sabato o domenica), le e-mail vengono automaticamente messe in coda e inviate il lunedì a un’ora specificata. Questo assicura un coinvolgimento ottimale distribuendo messaggi durante la settimana lavorativa.

## Panoramica del caso d’uso

**La sfida**: assicurati che le e-mail vengano inviate solo nei giorni feriali, anche se i profili possono entrare nel percorso durante il fine settimana. Per gli inserimenti nel fine settimana, le e-mail devono essere messe in coda e inviate il lunedì a un’ora specifica.

**Soluzione**: utilizzare un&#39;attività condizione per identificare il giorno della settimana. Per le voci del weekend, le attività Attendi con formule personalizzate ritardano il messaggio e-mail fino a lunedì. Le voci del giorno feriale procedono direttamente al passaggio di invio dell’e-mail.

Questo approccio mostra come utilizzare un’attività condizione per verificare se il giorno corrente è sabato o domenica, implementare attività di attesa con formule personalizzate per gli invii nel weekend, mettere in coda le e-mail nel weekend per la consegna del lunedì a un’ora specifica e inviare immediatamente le e-mail per gli invii nei giorni feriali (dal lunedì al venerdì).

Questo approccio è ideale per le campagne e-mail business-to-business (B2B), newsletter e comunicazioni professionali, annunci aziendali, aggiornamenti dei prodotti relativi al lavoro e qualsiasi campagna di marketing in cui non si desidera la consegna nel fine settimana.

>[!NOTE]
>
>Per implementare questo caso d&#39;uso, è necessaria un&#39;istanza di Adobe Journey Optimizer attiva con una [superficie del canale e-mail](../configuration/channel-surfaces.md) configurata, un [pubblico](../audience/about-audiences.md) o un [evento](../event/about-events.md) per attivare il percorso e una conoscenza di base delle [condizioni del percorso](conditions.md) e delle [espressioni](expression/expressionadvanced.md).

## Passaggi di implementazione

Utilizza questi passaggi per generare il flusso e-mail solo per i giorni feriali.

### Passaggio 1: creare il percorso

1. Passa a **[!UICONTROL Gestione Percorsi]** > **[!UICONTROL Percorsi]** in [!DNL Adobe Journey Optimizer].

1. Fare clic su **[!UICONTROL Crea Percorso]** per [creare un nuovo percorso](journey-gs.md).

1. Configura le [proprietà percorso](journey-properties.md).

1. Scegliere il punto di ingresso percorso:
   * **[Read Audience](read-audience.md)**: per campagne batch indirizzate a un pubblico specifico
   * **[Evento](../event/about-events.md)**: per percorsi attivati in tempo reale in base al comportamento del cliente

### Passaggio 2: aggiungi un’attività condizione per controllare il giorno della settimana

Subito dopo l&#39;inizio del percorso, aggiungi un&#39;attività **[!UICONTROL Condizione]** per verificare se il giorno corrente è sabato o domenica. In questo modo il flusso di lavoro verrà diramato di conseguenza.

1. Trascina e rilascia un&#39;attività [**[!UICONTROL Ottimizza ]**](optimize.md) nell&#39;area di lavoro dopo il punto di ingresso.

1. Fai clic sull&#39;attività **[!UICONTROL Condizione]** per aprire il relativo pannello di configurazione.

1. Seleziona **[!UICONTROL Condizione temporale]** come tipo di condizione.

1. Seleziona **[!UICONTROL Giorno della settimana]** come opzione di filtro dell&#39;ora.

1. Per il **primo percorso (sabato)**, seleziona solo **Sabato**. Etichetta questo percorso come &quot;sabato&quot;.

1. Fai clic su **[!UICONTROL Aggiungi un percorso]** per creare una seconda condizione.

1. Per il **secondo percorso (domenica)**, seleziona **[!UICONTROL Giorno della settimana]** e scegli solo **Domenica**. Etichetta questo percorso come &quot;Domenica&quot;.

   ![Configurazione delle condizioni di sabato e domenica nell&#39;editor espressioni](assets/weekday-email-uc-condition-expression.png)


1. Seleziona **[!UICONTROL Mostra percorso per casi diversi da quelli sopra]** per creare un percorso per le voci dei giorni feriali (dal lunedì al venerdì).

>[!NOTE]
>
>Il fuso orario utilizzato per la valutazione del giorno della settimana è definito a livello di percorso nelle proprietà del percorso e non a livello di condizione. Il percorso [fuso orario](timezone-management.md) utilizzato nella formula è il fuso orario configurato del percorso, non quello del destinatario.

### Passaggio 3: configurare le attività di attesa per le voci del fine settimana

Per i profili che entrano sabato o domenica, utilizza le attività **[!UICONTROL Attendi]** con formule personalizzate per posticipare l&#39;e-mail a lunedì nell&#39;ora desiderata.

Nell&#39;attività **[!UICONTROL Attendi]** utilizzare la formula seguente:

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

Dove:

* **X** è il numero di giorni di attesa:
   * Utilizza **2** per sabato (attendi fino a lunedì)
   * Utilizza **1** per domenica (attendi fino a lunedì)
* **H** è l&#39;ora che desideri inviare (ad esempio **9** per le 9)


**Esempio di sabato:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**Esempio di domenica:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

Per implementarlo nel percorso:

1. Nel percorso **Saturday**, aggiungi un&#39;attività **[!UICONTROL Wait]** dopo la condizione.

1. Seleziona **[!UICONTROL Durata]** come tipo di attesa.

1. Fare clic su **[!UICONTROL Modalità avanzata]** per immettere la formula personalizzata.

1. Immetti: `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![Percorso con tre percorsi di condizione: sabato, domenica e giorni feriali](assets/weekday-email-uc-paths.png)

1. Ripeti gli stessi passaggi per il **percorso domenica**, utilizzando: `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>Per orari di lavoro più complessi (ad esempio, per inviare solo tra le 9 e le 17 nei giorni feriali), puoi migliorare ulteriormente la formula e le condizioni.

### Passaggio 4: filiale del giorno feriale

Per i profili che entrano dal lunedì al venerdì, procedi come di consueto al passaggio di invio dell’e-mail.

1. Nel percorso **Giorno feriale** (il percorso &quot;Altri casi&quot;), procedi direttamente per aggiungere un&#39;attività di azione **[!UICONTROL E-mail]**. Non è necessaria alcuna attività **[!UICONTROL Attendi]** per le voci nei giorni feriali.

1. Configura il messaggio e-mail in base alle esigenze.

### Passaggio 5: completare il flusso di percorso

Dopo le attività **[!UICONTROL Attendi]** nei percorsi sabato e domenica, tutti e tre i percorsi (sabato, domenica e giorni feriali) devono scorrere nella stessa attività azione **[!UICONTROL E-mail]**. Aggiungi un&#39;attività **[!UICONTROL End]** dopo l&#39;e-mail.

### Panoramica del flusso di lavoro visivo

Il flusso di lavoro di percorso completo segue questa logica:

* **Inizio** → **[!UICONTROL Condizione]**: è sabato o domenica?
   * **Sì (sabato):** **[!UICONTROL Attendi]** fino a lunedì 9 → **[!UICONTROL Invia e-mail]**
   * **Sì (domenica):** **[!UICONTROL Attendi]** fino a lunedì 9 → **[!UICONTROL Invia e-mail]**
   * **No (lunedì-venerdì):** **[!UICONTROL Invia immediatamente e-mail]**

In questo modo, tutte le e-mail vengono inviate solo nei giorni feriali, con le voci del fine settimana messe automaticamente in coda per la consegna del lunedì.

### Passaggio 6: verifica del percorso

Prima di pubblicare, verifica accuratamente la logica di percorso nella modalità di test di [!DNL Adobe Journey Optimizer] per verificare che tutto funzioni come previsto:

1. Fai clic sul pulsante **[!UICONTROL Test]** nell&#39;angolo superiore destro.

1. Abilita [modalità di test](testing-the-journey.md).

1. Crea [profili di test](../audience/creating-test-profiles.md) con orari di immissione simulati in giorni diversi della settimana:
   * **Voce sabato**: verifica che il profilo segua il percorso del sabato, attendi e riceva e-mail il lunedì all&#39;ora specificata
   * **Domenica**: verifica che il profilo segua il percorso della domenica, attende e riceve un&#39;e-mail il lunedì all&#39;ora specificata
   * **Voci dal lunedì al venerdì**: verifica che le e-mail vengano inviate immediatamente senza attendere

1. Rivedi la visualizzazione percorso per garantire che i profili seguano i percorsi condizionali corretti (sabato, domenica o giorno feriale).

1. Verifica la presenza di [errori o avvisi](troubleshooting.md) nel percorso.

1. Verifica che le formule di attesa calcolino la durata corretta per l’ora di consegna di lunedì desiderata.

>[!IMPORTANT]
>
>Verifica sempre la logica di percorso in modalità di test per garantire che le attività Attendi si comportino come previsto. Utilizza la modalità di test per simulare diversi scenari di immissione e verificare che le voci del fine settimana siano correttamente inserite nella coda per la consegna del lunedì. Per ulteriori dettagli, consulta [Best practice per i test di percorso](testing-the-journey.md).

### Passaggio 7: pubblicare il percorso

Una volta completato il test:

1. Fai clic su **[!UICONTROL Pubblica]** nell&#39;angolo superiore destro.

1. Conferma la [pubblicazione](publish-journey.md).

1. Monitora le prestazioni del percorso utilizzando [rapporti sul Percorso](report-journey.md) e [rapporti live](../reports/journey-live-report.md).


## Argomenti correlati

* [Ottimizza attività](optimize.md) - Scopri come creare percorsi diversi nel tuo percorso
* [Condizioni di utilizzo in un percorso](conditions.md) - Guida dettagliata sulle condizioni del percorso
* [Attività attendi](wait-activity.md) - Configurare le durate di attesa e le formule
* [Funzioni data](functions/date-functions.md) - Riferimento completo per le funzioni data e ora
* [Editor espressioni](expression/expressionadvanced.md) - Genera espressioni complesse
* [Best practice per i Percorsi](journey-gs.md#best-practices) - Approcci consigliati per la progettazione dei percorsi

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene fornito un caso d&#39;uso dettagliato per la configurazione di un percorso che invia e-mail solo nei giorni feriali utilizzando una condizione di giorno della settimana e formule di attesa personalizzate per ritardare le immissioni nel fine settimana fino a lunedì.

**Intenti:**

* Configurare un’attività Condizione per diramare un percorso in base al giorno della settimana (sabato, domenica o giorno feriale)
* Scrivi espressioni di attesa personalizzate utilizzando `toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))` per ritardare i profili del fine settimana a lunedì
* Crea un percorso a tre percorsi che unisce tutti i percorsi in un’unica azione e-mail
* Test della logica e-mail valida solo per i giorni feriali utilizzando profili di test con giorni di ingresso simulati diversi
* Pubblicare e monitorare un percorso che sopprime la consegna e-mail del fine settimana

**Glossario:**

* **Condizione temporale**: tipo di attività condizione in Journey Optimizer che suddivide i percorsi del percorso in base a criteri di data/ora quali il giorno della settimana *(specifico per prodotto)*
* **nowWithDelta**: funzione di espressione che restituisce l&#39;offset di data/ora corrente di un numero specificato di giorni o di altre unità *(specifiche del prodotto)*
* **setHours**: funzione di espressione che imposta un&#39;ora specifica in un valore data/ora specificato *(specifico per prodotto)*
* **toDateTimeOnly**: funzione di espressione che converte un valore nel formato `dateTimeOnly` richiesto dalle attività di attesa personalizzate *(specifiche del prodotto)*

**Guardrail:**

* Il fuso orario utilizzato per la valutazione giornaliera della settimana è quello configurato dal percorso (impostato nelle proprietà del percorso), non quello del singolo destinatario.
* Per implementare questo caso d’uso sono necessari una superficie di canale e-mail attiva e un pubblico o un evento per attivare il percorso.
* Una conoscenza di base delle condizioni di percorso e dell’editor di espressioni avanzate è un prerequisito.
* Prima della pubblicazione, verifica sempre il percorso in modalità di test per verificare che le formule Wait producano il tempo di consegna corretto di lunedì.

**Terminologia:**

* Nome canonico: programmazione e-mail per giorno della settimana — Acronimo: none — varianti: e-mail solo per giorno della settimana, consegna e-mail per orario di lavoro
* Sinonimi: &quot;Percorso sabato&quot; / &quot;Percorso domenica&quot; = &quot;Percorsi weekend&quot;; &quot;Percorso altri casi&quot; = &quot;Percorso giorno feriale&quot;
* Non confondere: fuso orario del percorso (utilizzato per la valutazione giornaliera della settimana) ≠ fuso orario locale del destinatario

**Domande frequenti:**

* **Q: quale formula ritarda un&#39;immissione di sabato a lunedì alle 9?** — Utilizza `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))` nel percorso del sabato (2 giorni dopo arriva il lunedì).
* **Q: quale formula ritarda un&#39;immissione domenicale a lunedì alle 9?** — Utilizza `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))` nel percorso della domenica (1 giorno dopo arriva il lunedì).
* **Q: quale fuso orario viene utilizzato durante la valutazione della condizione del giorno della settimana?** — Il fuso orario configurato del percorso definito nelle proprietà del percorso; non è il fuso orario locale del destinatario.
* **Q: gli inserimenti nei giorni feriali richiedono un&#39;attività Attendi?** — No, i profili che entrano dal lunedì al venerdì procedono direttamente all’attività di azione E-mail senza alcuna attesa.
* **D: come posso verificare che le voci del fine settimana siano correttamente in coda?** — In modalità di test, creare profili di test con orari di ingresso simulati per sabato e domenica e verificare che seguano il percorso condizionale corretto e ricevano l&#39;e-mail il lunedì all&#39;ora configurata.

+++
