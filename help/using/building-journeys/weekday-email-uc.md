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
source-git-commit: 46a46fb25c1ef985a0bdea8974aa009e3699c7a3
workflow-type: tm+mt
source-wordcount: '1833'
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

1. Configura le proprietà del percorso:
   * **Nome**: campagna e-mail del giorno feriale
   * **Descrizione**: invia e-mail solo nei giorni feriali (dal lunedì al venerdì)
   * Imposta lo spazio dei nomi appropriato per il caso d’uso

[Ulteriori informazioni sulle proprietà del percorso](journey-properties.md)

1. Scegliere il punto di ingresso percorso:
   * **[Read Audience](read-audience.md)**: per campagne batch indirizzate a un pubblico specifico
   * **[Evento](../event/about-events.md)**: per percorsi attivati in tempo reale in base al comportamento del cliente

### Passaggio 2: aggiungi un’attività Condizione per controllare il giorno della settimana

Subito dopo l&#39;inizio del percorso, aggiungi un&#39;attività **[!UICONTROL Condizione]** per verificare se il giorno corrente è sabato o domenica. In questo modo il flusso di lavoro verrà diramato di conseguenza.

1. Trascina e rilascia un&#39;attività **[!UICONTROL Condition]** nell&#39;area di lavoro dopo il punto di ingresso. [Ulteriori informazioni sulle attività condizionali](condition-activity.md)

1. Fai clic sull’attività Condizione per aprire il relativo pannello di configurazione.

1. Nella sezione **[!UICONTROL Tipo di condizione]**, selezionare **[!UICONTROL Condizione Source dati]**. [Ulteriori informazioni sui tipi di condizione](condition-activity.md#data_source_condition)

   ![Configurazione della condizione Saturday nell&#39;editor espressioni](assets/weekday-email-uc-condition-expression.png)


### Passaggio 3: configurare la condizione per identificare sabato

Crea il primo percorso condizione per identificare le voci del sabato.

1. Fai clic su **[!UICONTROL Modalità avanzata]** per aprire l&#39;editor espressioni. [Ulteriori informazioni sull&#39;editor espressioni](expression/expressionadvanced.md)

1. Immettere l&#39;espressione seguente per verificare se il giorno corrente è sabato:

   ```javascript
   dayOfWeek(now()) == 7
   ```

   Questa opzione utilizza la funzione `dayOfWeek()` con `now()` per ottenere il giorno corrente. [Ulteriori informazioni sulle funzioni data](functions/date-functions.md)


1. Fare clic su **[!UICONTROL Ok]** per salvare la condizione.

1. Etichetta questo percorso come &quot;sabato&quot;.

### Passaggio 4: aggiungi un secondo percorso di condizione per domenica

1. Nell&#39;attività Condizione fare clic su **[!UICONTROL Aggiungi un percorso]** per creare una seconda condizione.

1. Nell’editor espressioni per il secondo percorso, immetti:

   ```javascript
   dayOfWeek(now()) == 1
   ```

   Questo controlla se il giorno corrente è domenica.

1. Etichetta questo percorso come &quot;Domenica&quot;.

1. Seleziona **[!UICONTROL Mostra percorso per casi diversi da quelli sopra]** per creare un percorso per le voci dei giorni feriali (dal lunedì al venerdì).


>[!NOTE]
>
>La funzione `dayOfWeek()` restituisce un numero intero che rappresenta il giorno della settimana, dove 1 corrisponde alla domenica e 7 al sabato. Questo segue lo standard ISO-8601 per la numerazione dei giorni.

### Passaggio 5: configurare le attività di attesa per le voci del fine settimana

Per i profili che entrano il sabato o la domenica, utilizza Attività di attesa con formule personalizzate per ritardare l’e-mail fino a lunedì nell’ora desiderata.


**Per il percorso del sabato:**

1. Aggiungi un&#39;attività **[!UICONTROL Wait]**. [Ulteriori informazioni sulle attività Attendi](wait-activity.md)

1. Seleziona **[!UICONTROL Durata]** come tipo di attesa.

1. Fare clic su **[!UICONTROL Modalità avanzata]** per immettere una formula personalizzata.

1. Immetti la seguente formula per attendere fino a lunedì alle 9:

   ```javascript
   toDuration("PT" + (48 - getHourOfDay(now())) + "H")
   ```

   In alternativa, utilizzare la formula seguente:

   ```javascript
   setHours(nowWithDelta(2, "days"), 9)
   ```

   ![Percorso con tre percorsi di condizione: sabato, domenica e giorni feriali](assets/weekday-email-uc-paths.png)

   **Spiegazione**: questa formula calcola il tempo di attesa da sabato a lunedì alle 9. Il valore X=2 rappresenta 2 giorni avanti (sabato + 2 giorni = lunedì). [Ulteriori informazioni sulle funzioni data](functions/date-functions.md#nowWithDelta)

**Per il percorso della domenica:**

1. Aggiungi un&#39;attività **[!UICONTROL Wait]**.

1. Seleziona **[!UICONTROL Durata]** come tipo di attesa.

1. Fare clic su **[!UICONTROL Modalità avanzata]** per immettere una formula personalizzata.

1. Immetti la seguente formula per attendere fino a lunedì alle 9:

   ```javascript
   setHours(nowWithDelta(1, "days"), 9)
   ```

   **Spiegazione**: questa formula attende 1 giorno (domenica + 1 giorno = lunedì) e imposta l&#39;ora sulle 9. Il valore X=1 rappresenta 1 giorno in avanti e H=9 rappresenta 9.

>[!TIP]
>
>Puoi personalizzare il parametro dell’ora (H) in base all’orario in cui desideri che l’e-mail venga inviata lunedì. Ad esempio, modificare da 9 a 10 per le ore 10 o a 14 per le ore 14.

### Passaggio 6: configurare il percorso del giorno feriale

Per il percorso **Giorno feriale** (da lunedì a venerdì):

1. Procedi direttamente per aggiungere un&#39;attività di azione **[!UICONTROL E-mail]**. Non è necessaria alcuna attività Attendi per i movimenti nei giorni feriali. [Ulteriori informazioni sulle azioni e-mail](journeys-message.md)

1. Configura il messaggio e-mail:
   * Seleziona o crea il [contenuto e-mail](../email/get-started-email-design.md)
   * Configura i [parametri e-mail](../email/email-settings.md)
   * Configura [personalization](../personalization/personalize.md) in base alle esigenze

1. Aggiungi un&#39;attività **[!UICONTROL End]** dopo l&#39;e-mail.

### Passaggio 7: unire i percorsi del fine settimana all’e-mail

Dopo le attività Attendi nei percorsi Sabato e Domenica, uniscili alla stessa attività Azione e-mail:

1. Dall&#39;attività Attesa sabato, aggiungi un&#39;azione **[!UICONTROL E-mail]**.

1. Dall’attività Sunday Wait (Attesa domenica), connettiti alla stessa azione E-mail.

1. Anche il percorso del giorno feriale deve passare a questa azione E-mail.

### Passaggio 8: verifica del percorso

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
>Prima di pubblicare in produzione, verifica sempre accuratamente la logica di percorso. Utilizza la modalità di test per simulare diversi scenari di immissione e verificare che le voci del fine settimana siano correttamente inserite nella coda per la consegna del lunedì. [Ulteriori informazioni sulle best practice per i test di percorso](testing-the-journey.md)

### Passaggio 9: pubblicare il percorso

Una volta completato il test:

1. Fai clic su **[!UICONTROL Pubblica]** nell&#39;angolo superiore destro.

1. Conferma la pubblicazione. [Ulteriori informazioni sulla pubblicazione dei percorsi](publish-journey.md)

1. Monitora le prestazioni del percorso utilizzando [rapporti sul Percorso](report-journey.md) e [rapporti live](../reports/journey-live-report.md).

## Best practice e considerazioni

+++**Ottimizza flusso di lavoro con formule migliorate**

Per migliorare il flusso di lavoro e gestire requisiti aziendali più complessi, è possibile estendere le formule per tenere conto di festività, fusi orari o orari di lavoro specifici oltre il controllo base del giorno feriale. Regola il parametro dell’ora (H) nella formula Attendi in modo che corrisponda all’ora di invio ottimale, ad esempio, se alle ore 10 vengono mostrate percentuali di coinvolgimento migliori, modifica la formula in modo da utilizzare l’ora 10. Per il supporto di più fusi orari, è consigliabile creare percorsi separati per aree geografiche diverse per garantire la consegna del lunedì nel fuso orario locale di ciascun destinatario.

+++

+++**Gestione del fuso orario**

La funzione `now()` e l&#39;esecuzione del percorso utilizzano il fuso orario configurato a livello di percorso. Assicurati che il fuso orario del percorso corrisponda alle tue esigenze configurandolo nelle proprietà del percorso prima di pubblicarlo ([Ulteriori informazioni sulla gestione del fuso orario](timezone-management.md)). Se il pubblico si estende su più fusi orari, tieni presente che il controllo del giorno della settimana si verifica nel fuso orario configurato del percorso, non in quello locale del destinatario. Per la consegna specifica per il fuso orario, crea percorsi separati per aree geografiche diverse o utilizza le impostazioni del fuso orario nell’attività Read Audience.

+++

+++**voce Percorso e tempistica**

Per i percorsi batch, [pianifica l&#39;attivazione di Read Audience](read-audience.md#schedule) in un momento appropriato per il pubblico. Le esecuzioni nelle prime ore del mattino (ad esempio, le ore 6:00) sono comuni per le comunicazioni aziendali. Per i percorsi basati su eventi, la condizione verrà valutata immediatamente alla ricezione dell&#39;evento e i profili che entrano nei fine settimana attenderanno automaticamente fino a lunedì ([Ulteriori informazioni sugli eventi](../event/about-events.md)). Assicurati che le [impostazioni di timeout del percorso](journey-properties.md#timeout) soddisfino il periodo di attesa massimo (fino a 2 giorni da sabato a lunedì).

+++

+++**Il test è essenziale**

Come sottolineato nella guida all’implementazione, verifica sempre la logica di percorso per verificare che tutto funzioni come previsto. Utilizza la **modalità test** per simulare diversi scenari di ingresso senza inviare e-mail reali. Test di tutti e tre i percorsi (voci di sabato, domenica e giorni feriali), verifica che i calcoli della durata di attesa siano corretti, conferma che la consegna del lunedì avvenga all’ora specificata e controlla la visualizzazione del percorso per garantire un percorso corretto.

+++

+++**Rientro e frequenza**

Per le campagne ricorrenti, configura le impostazioni di **[!UICONTROL Rientro]** in modo appropriato ([Ulteriori informazioni sulle impostazioni di rientro](entry-management.md)). Se i profili possono rientrare nel percorso, saranno soggetti al controllo del giorno della settimana ogni volta, garantendo che le voci del fine settimana siano sempre in coda per lunedì. Valuta l&#39;aggiunta di [regole di quota limite](../conflict-prioritization/journey-capping.md) per evitare messaggi eccessivi se i profili possono rientrare frequentemente.

+++

## Varianti avanzate

+++**Impostazione destinazione giorno specifica**

Per inviare e-mail solo in giorni specifici (ad esempio, martedì e giovedì), modifica la condizione:

```javascript
dayOfWeek(now()) == 3 or dayOfWeek(now()) == 5
```

Per tutti gli altri giorni, aggiungi un’attività Attendi che calcola il numero di giorni mancanti al martedì o giovedì successivo.

+++

+++**Orari di invio diversi per giorni diversi**

Puoi creare più percorsi con diverse formule di attesa per diversi comportamenti durante il fine settimana. Utilizzare ad esempio `nowWithDelta(4, "days")` per la consegna da sabato a mercoledì o `nowWithDelta(2, "days")` per la consegna da domenica a martedì. Ciò consente una maggiore flessibilità nella pianificazione degli invii.

+++

+++**Consegna in orario d&#39;ufficio**

Per garantire la consegna durante l’orario di lavoro, regola il parametro dell’ora nella formula Attendi. Ad esempio, per la consegna alle 14 invece delle 9:

```javascript
setHours(nowWithDelta(1, "days"), 14)
```

Puoi anche aggiungere una seconda condizione dopo Attendi per verificare se l’ora corrente è entro l’orario di lavoro prima dell’invio.

+++

+++**Esclusione festività**

Per escludere le festività, aggiungi un percorso di condizione aggiuntivo che verifichi la presenza di date specifiche:

```javascript
toDateTimeOnly(now()) == toDateTimeOnly("2024-12-25T00:00:00")
```

Se la condizione corrisponde a una festività, aggiungi un’attività Attendi per rimandare al giorno lavorativo successivo. [Ulteriori informazioni sulle funzioni di confronto delle date](functions/date-functions.md)

+++

## Argomenti correlati

* [Informazioni sulle attività condizionali](condition-activity.md) - Scopri come creare percorsi diversi nel percorso
* [Condizioni di utilizzo in un percorso](conditions.md) - Guida dettagliata sulle condizioni del percorso
* [Attività attendi](wait-activity.md) - Configurare le durate di attesa e le formule
* [Funzioni data](functions/date-functions.md) - Riferimento completo per le funzioni data e ora
* [Editor espressioni](expression/expressionadvanced.md) - Genera espressioni complesse
* [Verifica il percorso](testing-the-journey.md) - Convalida logica di percorso prima della pubblicazione
* [Gestione del fuso orario](timezone-management.md) - Gestione di fusi orari diversi in percorsi
* [Best practice per i Percorsi](journey-gs.md#best-practices) - Approcci consigliati per la progettazione dei percorsi

## Video dimostrativo

Scopri come inviare e-mail solo nei giorni feriali utilizzando Adobe Journey Optimizer. Questo video illustra l’implementazione passo passo delle attività relative alle condizioni e delle formule di attesa per mettere in coda le voci del fine settimana per la consegna del lunedì.

>[!VIDEO](https://video.tv.adobe.com/v/3469388?captions=ita&quality=12&learn=on)

## Risorse aggiuntive

* [Documentazione dell&#39;editor espressioni](expression/expressionadvanced.md) - Creare e convalidare le espressioni di percorso
* [Guida alla progettazione dei Percorsi](using-the-journey-designer.md) - Eseguire il master dell&#39;area di lavoro del percorso
* [Panoramica sui casi d&#39;uso per i Percorsi](jo-use-cases.md) - Esplora altri modelli ed esempi per i percorsi
* [Post di blog della community: come inviare e-mail solo nei giorni feriali](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400){target="_blank"} - Post di blog originale con esempi dettagliati

