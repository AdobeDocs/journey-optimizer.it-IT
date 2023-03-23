---
title: Aggiungere vincoli a un’offerta
description: Scopri come definire le condizioni per la visualizzazione di un’offerta
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 47145e980c37f67b6981ffd9cc4300d29e179f45
workflow-type: tm+mt
source-wordcount: '2323'
ht-degree: 17%

---

# Aggiungere vincoli a un’offerta {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="Informazioni sui vincoli di offerta"
>abstract="Con i vincoli, puoi specificare in che modo l’offerta viene prioritizzata e presentata all’utente rispetto ad altre offerte."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="Informazioni sui vincoli di offerta"
>abstract="Con i vincoli, puoi specificare in che modo l’offerta viene prioritizzata e presentata all’utente rispetto ad altre offerte."

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="Informazioni sulla priorità delle offerte"
>abstract="In questo campo puoi specificare le impostazioni di priorità per l’offerta. La priorità è un numero utilizzato per classificare le offerte che soddisfano tutti i vincoli, quali idoneità, date e limiti."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="Impostare la priorità"
>abstract="La priorità consente di definire la priorità dell’offerta rispetto ad altre se l’utente è idoneo per più di un’offerta. Più alta sarà la priorità di un’offerta, maggiore sarà la sua priorità rispetto ad altre offerte."

I vincoli ti consentono di definire le condizioni in cui verrà visualizzata un’offerta.

1. Configura le **[!UICONTROL Idoneità offerta]**. [Ulteriori informazioni](#eligibility)

   ![](../assets/offer-eligibility.png)

1. Definisci la **[!UICONTROL Priorità]** dell’offerta rispetto alle altre se l’utente è idoneo per più di un’offerta. Più alta sarà la priorità di un’offerta, maggiore sarà la sua priorità rispetto ad altre offerte.

   ![](../assets/offer-priority.png)

1. Specifica le offerte **[!UICONTROL Limitazione]**, ovvero il numero di volte in cui verrà presentata l’offerta. [Ulteriori informazioni](#capping)

   ![](../assets/offer-capping.png)

1. Fai clic su **[!UICONTROL Successivo]** per confermare tutti i vincoli definiti.

Ad esempio, se imposti i vincoli seguenti:

![](../assets/offer-constraints-example.png)

* L’offerta verrà considerata solo per gli utenti che corrispondono alla regola di decisione &quot;Clienti Gold Loyalty&quot;.
* La priorità dell&#39;offerta è impostata su &quot;50&quot;, il che significa che l&#39;offerta sarà presentata prima delle offerte con una priorità compresa tra 1 e 49 e dopo quelle con una priorità di almeno 51.
* L’offerta verrà presentata una sola volta al mese per utente in tutti i posizionamenti.

## Ammissibilità {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="Definire l’idoneità"
>abstract="Per impostazione predefinita, qualsiasi profilo è idoneo alla presentazione dell’offerta, ma puoi utilizzare segmenti o regole di decisione per limitare l’offerta a profili specifici."

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="Informazioni sull’idoneità delle offerte"
>abstract="In questa sezione puoi utilizzare le regole di decisione per determinare quali utenti sono idonei per l’offerta."
>additional-url="https://video.tv.adobe.com/v/329373" text="Guarda il video dimostrativo"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="Stima totale profili"
>abstract="Quando selezioni segmenti o regole di decisione, puoi visualizzare informazioni sui profili qualificati stimati."

La **[!UICONTROL Idoneità offerta]** La sezione ti consente di limitare l’offerta a profili specifici definiti utilizzando segmenti o regole decisionali.

>[!NOTE]
>
>Ulteriori informazioni sull&#39;utilizzo di **segmenti** contro **norme decisionali** in [questa sezione](#segments-vs-decision-rules).

* Per impostazione predefinita, la **[!UICONTROL Tutti i visitatori]** viene selezionata, il che significa che qualsiasi profilo sarà idoneo per la presentazione dell’offerta.

   ![](../assets/offer-eligibility-default.png)

* Puoi anche limitare la presentazione dell’offerta ai membri di uno o più [Segmenti Adobe Experience Platform](../../segment/about-segments.md).

   Per eseguire questa operazione, attiva il **[!UICONTROL Visitatori che rientrano in uno o più segmenti]** , quindi aggiungi uno o più segmenti dal riquadro a sinistra e combinali utilizzando la **[!UICONTROL E]** / **[!UICONTROL Oppure]** operatori logici.

   ![](../assets/offer-eligibility-segment.png)

* Per associare uno specifico [norma decisionale](../offer-library/creating-decision-rules.md) all’offerta, seleziona **[!UICONTROL Per regola decisionale definita]**, quindi trascina la regola desiderata dal riquadro di sinistra nel **[!UICONTROL Regola decisionale]** area.

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >Le offerte basate su eventi non sono attualmente supportate in [!DNL Journey Optimizer]. Se crei una regola decisionale basata su un [event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}, non potrai sfruttarlo in un’offerta.

Quando selezioni segmenti o regole di decisione, puoi visualizzare informazioni sui profili qualificati stimati. Fai clic su **[!UICONTROL Aggiorna]** per aggiornare i dati.

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>Le stime del profilo non sono disponibili quando i parametri delle regole includono dati non presenti nel profilo, ad esempio dati contestuali. Ad esempio, una regola di idoneità che richiede che il tempo corrente sia ≥ 80 gradi.

### Utilizzo di segmenti e regole decisionali {#segments-vs-decision-rules}

Per applicare un vincolo, è possibile limitare la selezione delle offerte ai membri di uno o più **Segmenti Adobe Experience Platform** oppure puoi utilizzare un **norma decisionale**, entrambe le soluzioni corrispondenti a diversi utilizzi.

In sostanza, l’output di un segmento è un elenco di profili, mentre una regola decisionale è una funzione eseguita su richiesta rispetto a un singolo profilo durante il processo decisionale. La differenza tra questi due utilizzi è illustrata di seguito.

* **Segmenti**

   Da un lato, i segmenti sono un gruppo di profili Adobe Experience Platform che corrispondono a una determinata logica in base agli attributi di profilo e agli eventi di esperienza. Tuttavia, Gestione delle offerte non esegue il calcolo del segmento, che potrebbe non essere aggiornato al momento della presentazione dell’offerta.

   Ulteriori informazioni sui segmenti in [questa sezione](../../segment/about-segments.md).

* **Regole di decisione**

   D’altra parte, una regola decisionale si basa sui dati disponibili in Adobe Experience Platform e determina a chi può essere visualizzata un’offerta. Una volta selezionata in un’offerta o in una decisione per un determinato posizionamento, la regola viene eseguita ogni volta che viene presa una decisione, in modo che ogni profilo ottenga l’ultima e l’offerta migliore.

   Ulteriori informazioni sulle regole decisionali in [questa sezione](creating-decision-rules.md).

## Limitazione {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Informazioni sul limite delle offerte"
>abstract="In questo campo puoi specificare quante volte può essere presentata l’offerta."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="Utilizzare il limite"
>abstract="Per evitare di sollecitare eccessivamente i clienti, utilizza il limite per definire il numero massimo di volte in cui è possibile presentare un’offerta."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints.html?lang=it#capping-change-date" text="La modifica delle date può influire sui limiti"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="Impostare la frequenza di limitazione"
>abstract="Puoi scegliere di reimpostare il contatore del limite di offerta su base giornaliera, settimanale o mensile. Dopo aver salvato l’offerta, non potrai modificare la frequenza selezionata."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping_impression"
>title="Impression"
>abstract="L’utilizzo delle impression come eventi di limitazione è disponibile solo per i canali in entrata."

La limitazione di utilizzo viene utilizzata per definire il numero massimo di volte in cui è possibile presentare un’offerta.

Limitare il numero di volte in cui gli utenti ricevono offerte specifiche ti consente di evitare di sollecitare eccessivamente i clienti e, quindi, di ottimizzare ogni punto di contatto con l’offerta migliore.

Per impostare il limite, segui i passaggi principali riportati di seguito.

1. Assicurati che **[!UICONTROL Includi limite]** il pulsante di attivazione/disattivazione è selezionato. Per impostazione predefinita, la limitazione è inclusa.

   >[!CAUTION]
   >
   >Non è possibile abilitare o disabilitare il limite di frequenza per le offerte create in precedenza. A questo scopo, devi duplicare l’offerta o crearne una nuova.

1. Definisci quali **[!UICONTROL Evento di limitazione]** verrà preso in considerazione per aumentare il contatore. [Ulteriori informazioni](#capping-event)

1. Imposta il numero di volte in cui può essere presentata l’offerta. [Ulteriori informazioni](#capping-count)

1. Scegli se applicare il limite a tutti gli utenti o a un solo profilo. [Ulteriori informazioni](#capping-type)

1. Imposta la **[!UICONTROL Frequenza]** per definire la frequenza con cui viene reimpostato il conteggio dei limiti. [Ulteriori informazioni](#frequency-capping)

1. Se ne hai definiti diversi [rappresentazioni](add-representations.md) per l’offerta, specifica se applicare il limite **[!UICONTROL In tutti i posizionamenti]** o **[!UICONTROL Per ogni posizionamento]**. [Ulteriori informazioni](#placements)

1. Una volta salvata e approvata, se all’offerta è stato presentato il numero di volte specificato in questo campo in base ai criteri e al periodo di tempo definito, la consegna verrà interrotta.

Il numero di volte in cui viene proposta un’offerta viene calcolato al momento della preparazione dell’e-mail. Ad esempio, se prepari un’e-mail contenente una serie di offerte, questi numeri vengono conteggiati in base al tetto massimo, indipendentemente dal fatto che l’e-mail venga inviata o meno.

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>I contatori di maschiatura vengono reimpostati quando l’offerta scade o due anni dopo la data di inizio dell’offerta, a seconda di quale dei due eventi si verifica per primi. Scopri come definire la data di un’offerta in [questa sezione](creating-personalized-offers.md#create-offer).

### Evento di limitazione {#capping-event}

La **[!UICONTROL Evento di limitazione]** consente di definire quale campo **[!UICONTROL Evento di limitazione]** sarà preso in considerazione per aumentare il contatore:

![](../assets/offer-capping-event.png)

* **[!UICONTROL Evento decisionale]** (valore predefinito): Numero massimo di volte in cui è possibile presentare un’offerta.
* **[!UICONTROL Impression]**: Numero massimo di volte in cui l’offerta può essere visualizzata a un utente.

   >[!NOTE]
   >
   >L’utilizzo delle impression come eventi di limitazione è disponibile per **canali in entrata** solo.

* **[!UICONTROL Clic]**: Numero massimo di volte in cui un utente può fare clic sull’offerta.
* **[!UICONTROL Evento personalizzato]**: Puoi definire un evento personalizzato da utilizzare per limitare il numero di offerte inviate. Ad esempio, puoi limitare il numero di rimborsi fino a quando non sono pari a 10000, o fino a quando un determinato profilo non ha rimborsato 1 volta. Per farlo, utilizza [Adobe Experience Platform XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"} schemi per creare una regola evento personalizzata.

   <!--For example, you can cap on the number of redemptions so that the offer can be shown until redemptions equal 10000. You can only select XDM ExperienceEvents. -->

   Nell’esempio seguente, desideri limitare il numero di checkout.

   1. Seleziona **[!UICONTROL Evento personalizzato]** dall&#39;elenco e utilizza **[!UICONTROL Aggiungi evento personalizzato]** pulsante .

      ![](../assets/offer-capping-custom-event-add.png)

   1. Utilizza la **[!UICONTROL Creare regole evento personalizzate]** Generatore per selezionare l’evento rilevante. Puoi scegliere qualsiasi azione dell’utente su cui desideri limitare il limite delle offerte.

      Qui scegli **[!UICONTROL Commerce]** > **[!UICONTROL Pagamenti]** > **[!UICONTROL Valore]** e seleziona **[!UICONTROL esiste]** dall’elenco a discesa.

      ![](../assets/offer-capping-custom-event.png)

   1. Una volta creata la regola, questa viene visualizzata nella **[!UICONTROL Query evento personalizzata]** campo .

      ![](../assets/offer-capping-custom-event-query.png)
   >[!CAUTION]
   >
   >Per tutti gli eventi di limitazione, ad eccezione dell’evento decisionale, il feedback della gestione delle decisioni potrebbe non essere raccolto automaticamente, quindi assicurati che i dati siano in arrivo. [Ulteriori informazioni sulla raccolta dati](../data-collection/data-collection.md)

### Conteggio {#capping-count}

La **[!UICONTROL Conteggio]** consente di specificare il numero di volte in cui può essere presentata l’offerta.

![](../assets/offer-capping-times.png)

>[!NOTE]
>
>Il numero deve essere un numero intero maggiore di 0.

Ad esempio, hai definito un evento di limitazione personalizzata, ad esempio il numero di checkout, che viene preso in considerazione. Se immetti 10 nel campo **[!UICONTROL Conteggio]** campo , non verranno più inviate offerte dopo 10 checkout.

### Tipo di aggancio {#capping-type}

Puoi anche specificare se desideri che il limite sia applicato a tutti gli utenti o a un profilo specifico:

![](../assets/offer-capping-total.png)

* Seleziona **[!UICONTROL Totale]** per definire quante volte un’offerta può essere proposta tra il pubblico di destinazione combinato, ovvero tra tutti gli utenti.

   Ad esempio, se sei un rivenditore di elettronica con un&#39;offerta di porta TV, vuoi che l&#39;offerta venga restituita solo 200 volte in tutti i profili.

* Seleziona **[!UICONTROL Per profilo]** per definire quante volte può essere proposta un’offerta allo stesso utente.

   Ad esempio, se sei una banca con un&#39;offerta &quot;Carta di credito Platinum&quot;, non vuoi che questa offerta venga visualizzata più di 5 volte per profilo. In effetti, si ritiene che se l&#39;utente ha visto l&#39;offerta 5 volte e non ha agito su di essa, ha una maggiore possibilità di agire sulla prossima offerta migliore.

### Limite di frequenza {#frequency-capping}

La **[!UICONTROL Frequenza]** La sezione ti consente di definire la frequenza con cui viene reimpostato il conteggio dei limiti. A questo scopo, definisci il periodo di tempo per il conteggio (giornaliero, settimanale o mensile) e inserisci il numero di giorni/settimane/mesi desiderato.

![](../assets/offer-capping-frequency.png)

>[!NOTE]
>
>La reimpostazione avviene alle 12:00 UTC, nel giorno definito o il primo giorno della settimana/mese, se applicabile. Il giorno di inizio della settimana è domenica. La durata scelta non può superare i 2 anni (cioè il numero corrispondente di mesi, settimane o giorni).

Ad esempio, se desideri reimpostare il conteggio dei limiti ogni 2 settimane, seleziona **[!UICONTROL Settimanale]** dal **[!UICONTROL Ripeti]** elenco a discesa e tipo **2** nell&#39;altro campo. Il reset avverrà ogni due domenica alle 12 UTC.

>[!CAUTION]
>
>Dopo aver salvato l’offerta, non potrai modificare il periodo di tempo (mensile, settimanale o giornaliero) selezionato per la frequenza.

### Blocco e posizionamenti {#placements}

Se ne hai definiti diversi [rappresentazioni](add-representations.md) per l’offerta, specifica se applicare il limite **[!UICONTROL In tutti i posizionamenti]** o **[!UICONTROL Per ogni posizionamento]**.

![](../assets/offer-capping-placement.png)

* **[!UICONTROL In tutti i posizionamenti]**: i conteggi dei massimali totalizzeranno tutte le decisioni nei posizionamenti associati all’offerta.

   Ad esempio, se un’offerta ha una **E-mail** posizionamento e **Web** e si imposta il limite su **2 per profilo in tutti i posizionamenti**, ogni profilo potrebbe ricevere l’offerta fino a 2 volte in totale, indipendentemente dal mix di posizionamento.

* **[!UICONTROL Per ogni posizionamento]**: i conteggi dei limiti applicheranno separatamente i conteggi delle decisioni per ogni posizionamento.

   Ad esempio, se un’offerta ha una **E-mail** posizionamento e **Web** e si imposta il limite su **2 per profilo per ogni posizionamento**, allora ogni profilo potrebbe ricevere l’offerta fino a 2 volte per il posizionamento dell’e-mail e un ulteriore 2 volte per il posizionamento web.

### Impatto della modifica delle date sul massimale {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="La modifica delle date può influire sui limiti"
>abstract="Se a questa offerta viene applicato un limite, questo può essere influenzato quando modifichi la data di inizio o di fine."

È necessario prestare attenzione quando si modifica la data di un’offerta, perché questo può avere un impatto sui limiti se vengono soddisfatte le seguenti condizioni:

* L&#39;offerta è [approvato](#review).
* [Limitazione](#capping) è già applicato all’offerta.
* La limitazione di utilizzo è definita in base al profilo.

>[!NOTE]
>
>Scopri come definire la data di un’offerta in [questa sezione](creating-personalized-offers.md#create-offer).

L’applicazione a capo per profilo memorizza i conteggi dei limiti su ciascun profilo. Quando modifichi la data di inizio e di fine di un’offerta approvata, il conteggio dei limiti per alcuni profili potrebbe essere interessato in base ai diversi scenari descritti di seguito.

![](../assets/offer-capping-change-date.png)

Di seguito sono riportati gli scenari possibili quando **modifica di una data di inizio offerta**:

| Scenario:<br>Se... | Cosa succede:<br>allora... | Possibile impatto sul conteggio dei limiti |
|--- |--- |--- |
| ... la data di inizio dell’offerta viene aggiornata prima dell’inizio della data di inizio dell’offerta originale, | ... il conteggio dei limiti inizierà alla nuova data di inizio. | No |
| ... la nuova data di inizio è anteriore alla data di fine corrente, | ... il limite continuerà con una nuova data di inizio e il precedente conteggio dei limiti per ciascun profilo verrà riportato. | No |
| ... la nuova data di inizio è successiva alla data di fine corrente, | ... il limite attuale scade e il nuovo conteggio dei limiti ripartirà da 0 per tutti i profili alla nuova data di inizio. | Sì |

Di seguito sono riportati gli scenari possibili quando **estensione di una data di fine offerta**:

| Scenario:<br>Se... | Cosa succede:<br>allora... | Possibile impatto sul conteggio dei limiti |
|--- |--- |--- |
| ... una richiesta di decisione si verifica prima della data di fine dell’offerta originale, | ... il conteggio dei limiti verrà aggiornato e il conteggio dei limiti precedente per ciascun profilo verrà riportato. | No |
| ... nessuna richiesta di decisione viene effettuata prima della data di fine originale, | ... il conteggio dei limiti verrà reimpostato sulla data di fine originale per ciascun profilo. Il nuovo conteggio dei limiti inizia da 0 per tutte le nuove richieste di decisione che verranno effettuate dopo la data di fine originale. | Sì |

**Esempio**

Supponiamo di avere un&#39;offerta con una data di inizio originale impostata su **Gennaio 1**, in scadenza **31 gennaio**.

1. Vengono presentati i profili X, Y e Z.
1. On **Gennaio 10**, la data di fine dell’offerta viene modificata in **15 febbraio**.
1. **Dall&#39;11 gennaio al 31 gennaio**, l’offerta viene presentata solo al profilo Z.

   * Perché una richiesta di decisione si è verificata prima della data di fine originale **per il profilo Z**, la data di fine dell’offerta può essere estesa a **15 febbraio**.
   * Tuttavia, poiché non si è verificata alcuna attività prima della data di fine originale per **profili X e Y**, i loro contatori scadranno e i loro conteggi dei limiti saranno reimpostati a 0 su **31 gennaio**.

![](../assets/offer-capping-change-date-ex.png)
