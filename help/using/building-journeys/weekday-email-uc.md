---
solution: Journey Optimizer
product: journey optimizer
title: Invia e-mail solo nei giorni feriali
description: Scopri come configurare un percorso per l’invio di e-mail solo nei giorni feriali in Adobe Journey Optimizer
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: percorso, caso d’uso, giorni feriali, condizione, e-mail, pianificazione
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: ad902c1055ea2e883c028172297aab878a898b94
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 0%

---

# Invia e-mail solo nei giorni feriali {#send-emails-only-on-weekdays}

Questo caso d’uso illustra come configurare un percorso in Adobe Journey Optimizer che invia e-mail solo nei giorni feriali (dal lunedì al venerdì). Per i profili che entrano nel percorso nei fine settimana (sabato o domenica), le e-mail vengono automaticamente messe in coda e inviate il lunedì a un’ora specificata. Questo assicura un coinvolgimento ottimale distribuendo messaggi durante la settimana lavorativa.

## Panoramica del caso d’uso

**La sfida**: assicurati che le e-mail vengano inviate solo nei giorni feriali, anche se i profili possono entrare nel percorso durante il fine settimana. Per gli inserimenti nel fine settimana, le e-mail devono essere messe in coda e inviate il lunedì a un’ora specifica.

**Soluzione**: utilizzare un&#39;attività condizione per identificare il giorno della settimana. Per le voci del weekend, le attività Attendi con formule personalizzate ritardano il messaggio e-mail fino a lunedì. Le voci del giorno feriale procedono direttamente al passaggio di invio dell’e-mail.

Questo approccio mostra come utilizzare un’attività condizione per verificare se il giorno corrente è sabato o domenica, implementare attività di attesa con formule personalizzate per gli invii nel weekend, mettere in coda le e-mail nel weekend per la consegna del lunedì a un’ora specifica e inviare immediatamente le e-mail per gli invii nei giorni feriali (dal lunedì al venerdì).

Questo approccio è ideale per le campagne e-mail business-to-business (B2B), newsletter e comunicazioni professionali, annunci aziendali, aggiornamenti dei prodotti relativi al lavoro e qualsiasi campagna di marketing in cui non si desidera la consegna nel fine settimana.

➡️ Guarda il [tutorial video](#how-to-video) dettagliato

>[!NOTE]
>
>Per implementare questo caso d&#39;uso, è necessaria un&#39;istanza di Adobe Journey Optimizer attiva con una [superficie del canale e-mail](../configuration/channel-surfaces.md) configurata, un [pubblico](../audience/about-audiences.md) o un [evento](../event/about-events.md) per attivare il percorso e una conoscenza di base delle [condizioni del percorso](condition-activity.md) e delle [espressioni](expression/expressionadvanced.md).


## Passaggi di implementazione

### Passaggio 1: creare il percorso

1. Passa a **[!UICONTROL Gestione Percorsi]** > **[!UICONTROL Percorsi]** in Adobe Journey Optimizer.

1. Fare clic su **[!UICONTROL Crea Percorso]** per creare un nuovo percorso. [Ulteriori informazioni sulla creazione di percorsi](journey-gs.md)

1. Configura le [proprietà percorso](journey-properties.md).

1. Scegliere il punto di ingresso percorso:
   * **[Read Audience](read-audience.md)**: per campagne batch indirizzate a un pubblico specifico
   * **[Evento](../event/about-events.md)**: per percorsi attivati in tempo reale in base al comportamento del cliente

### Passaggio 2: aggiungi un’attività Condizione per controllare il giorno della settimana

Subito dopo l’inizio del percorso, aggiungi una condizione per verificare se il giorno corrente è sabato o domenica. In questo modo il flusso di lavoro verrà diramato di conseguenza.

1. Trascina e rilascia un&#39;attività **[!UICONTROL Condition]** nell&#39;area di lavoro dopo il punto di ingresso. [Ulteriori informazioni sulle attività condizionali](condition-activity.md)

1. Fai clic sull’attività Condizione per aprire il relativo pannello di configurazione.

1. Seleziona **[!UICONTROL Condizione temporale]** come tipo di condizione.

1. Seleziona **Giorno della settimana** come opzione di filtro dell&#39;ora.

1. Per il **primo percorso (sabato)**, seleziona solo **Sabato**. Etichetta questo percorso come &quot;sabato&quot;.

1. Fai clic su **[!UICONTROL Aggiungi un percorso]** per creare una seconda condizione.

1. Per il **secondo percorso (domenica)**, seleziona **Giorno della settimana** e scegli solo **Domenica**. Etichetta questo percorso come &quot;Domenica&quot;.

   ![Configurazione delle condizioni di sabato e domenica nell&#39;editor espressioni](assets/weekday-email-uc-condition-expression.png)


1. Seleziona **[!UICONTROL Mostra percorso per casi diversi da quelli sopra]** per creare un percorso per le voci dei giorni feriali (dal lunedì al venerdì).

>[!NOTE]
>
>Il fuso orario utilizzato per la valutazione del giorno della settimana è definito a livello di percorso nelle proprietà del percorso e non a livello di condizione. Il fuso orario del percorso utilizzato nella formula è quello configurato dal percorso, non quello del destinatario. [Ulteriori informazioni sulla gestione del fuso orario](timezone-management.md).

### Passaggio 3: configurare le attività di attesa per le voci del fine settimana

Per i profili che entrano il sabato o la domenica, utilizza Attività di attesa con formule personalizzate per ritardare l’e-mail fino a lunedì nell’ora desiderata.

Nell’attività Attendi, utilizza la seguente formula:

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

1. Nel percorso **Giorno feriale** (il percorso &quot;Altri casi&quot;), procedi direttamente per aggiungere un&#39;attività di azione **[!UICONTROL E-mail]**. Non è necessaria alcuna attività Attendi per i movimenti nei giorni feriali.

1. Configura il messaggio e-mail in base alle esigenze.

### Passaggio 5: completare il flusso di percorso

Dopo le attività Attendi nei percorsi sia di sabato che di domenica, tutti e tre i percorsi (sabato, domenica e giorni feriali) devono scorrere nella stessa attività di azione E-mail. Aggiungi un&#39;attività **[!UICONTROL End]** dopo l&#39;e-mail.

### Panoramica del flusso di lavoro visivo

Il flusso di lavoro di percorso completo segue questa logica:

* **Inizio** → **Condizione: è sabato o domenica?**
   * **Sì (sabato):** Attendi fino a lunedì 9 → Invia e-mail
   * **Sì (domenica):** Attendi fino a lunedì 9 → Invia e-mail
   * **No (lunedì-venerdì):** Invia immediatamente un&#39;e-mail

In questo modo, tutte le e-mail vengono inviate solo nei giorni feriali, con le voci del fine settimana messe automaticamente in coda per la consegna del lunedì.

### Passaggio 6: verifica del percorso

Prima di pubblicare, verifica accuratamente la logica di percorso nella modalità di test di Adobe Journey Optimizer per verificare che tutto funzioni come previsto:

1. Fai clic sul pulsante **[!UICONTROL Test]** nell&#39;angolo superiore destro.

1. Abilita la modalità di test. [Scopri come verificare il percorso](testing-the-journey.md)

1. Crea [profili di test](../audience/creating-test-profiles.md) con orari di immissione simulati in giorni diversi della settimana:
   * **Voce sabato**: verifica che il profilo segua il percorso del sabato, attendi e riceva e-mail il lunedì all&#39;ora specificata
   * **Domenica**: verifica che il profilo segua il percorso della domenica, attende e riceve un&#39;e-mail il lunedì all&#39;ora specificata
   * **Voci dal lunedì al venerdì**: verifica che le e-mail vengano inviate immediatamente senza attendere

1. Rivedi la visualizzazione percorso per garantire che i profili seguano i percorsi condizionali corretti (sabato, domenica o giorno feriale).

1. Controllare eventuali errori o avvisi nel percorso. [Informazioni sulla risoluzione dei problemi dei percorsi](troubleshooting.md)

1. Verifica che le formule di attesa calcolino la durata corretta per l’ora di consegna di lunedì desiderata.

>[!IMPORTANT]
>
>Verifica sempre la logica di percorso in modalità di test per garantire che le attività Attendi si comportino come previsto. Utilizza la modalità di test per simulare diversi scenari di immissione e verificare che le voci del fine settimana siano correttamente inserite nella coda per la consegna del lunedì. [Ulteriori informazioni sulle best practice per i test di percorso](testing-the-journey.md)

### Passaggio 7: pubblicare il percorso

Una volta completato il test:

1. Fai clic su **[!UICONTROL Pubblica]** nell&#39;angolo superiore destro.

1. Conferma la pubblicazione. [Ulteriori informazioni sulla pubblicazione dei percorsi](publish-journey.md)

1. Monitora le prestazioni del percorso utilizzando [rapporti sul Percorso](report-journey.md) e [rapporti live](../reports/journey-live-report.md).


## Argomenti correlati

* [Informazioni sulle attività condizionali](condition-activity.md) - Scopri come creare percorsi diversi nel percorso
* [Condizioni di utilizzo in un percorso](conditions.md) - Guida dettagliata sulle condizioni del percorso
* [Attività attendi](wait-activity.md) - Configurare le durate di attesa e le formule
* [Funzioni data](functions/date-functions.md) - Riferimento completo per le funzioni data e ora
* [Editor espressioni](expression/expressionadvanced.md) - Genera espressioni complesse
* [Best practice per i Percorsi](journey-gs.md#best-practices) - Approcci consigliati per la progettazione dei percorsi
* [Post di blog della community: come inviare e-mail solo nei giorni feriali](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400){target="_blank"} - Post di blog originale con esempi dettagliati

