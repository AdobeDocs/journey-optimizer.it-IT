---
title: Aggiungere vincoli a un’offerta
description: Scopri come definire le condizioni per la visualizzazione di un’offerta
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: ccaad8c4d9d26c0fd968e627e7a6bf853f232000
workflow-type: tm+mt
source-wordcount: '1735'
ht-degree: 2%

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
>abstract="In questo campo puoi specificare le impostazioni di priorità per l’offerta. Priorità è un numero utilizzato per classificare le offerte che soddisfano tutti i vincoli quali idoneità, date e limiti."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="Imposta priorità"
>abstract="La priorità consente di definire la priorità dell’offerta rispetto ad altre se l’utente è idoneo per più di un’offerta. Più alta sarà la priorità di un’offerta, maggiore sarà la sua priorità rispetto ad altre offerte."

I vincoli ti consentono di definire le condizioni in cui verrà visualizzata un’offerta.

1. Configurare **[!UICONTROL Idoneità dell’offerta]**. [Ulteriori informazioni](#eligibility)

   ![](../assets/offer-eligibility.png)

1. Definisci il **[!UICONTROL Priorità]** dell’offerta rispetto ad altre se l’utente è idoneo per più di un’offerta. Più alta sarà la priorità di un’offerta, maggiore sarà la sua priorità rispetto ad altre offerte.

   ![](../assets/offer-priority.png)

1. Specifica dell’offerta **[!UICONTROL Limitazione]**, ovvero il numero di volte in cui verrà presentata l’offerta. [Ulteriori informazioni](#capping)

   ![](../assets/offer-capping.png)

1. Clic **[!UICONTROL Successivo]** per confermare tutti i vincoli definiti.

Ad esempio, se impostate i seguenti vincoli:

![](../assets/offer-constraints-example.png)

* L’offerta verrà considerata solo per gli utenti che corrispondono alla regola di decisione &quot;Clienti Gold Loyalty&quot;.
* La priorità dell’offerta è impostata su &quot;50&quot;, il che significa che l’offerta sarà presentata prima delle offerte con priorità tra 1 e 49 e dopo quelle con priorità di almeno 51.
* L’offerta verrà presentata una sola volta per utente in tutti i posizionamenti.

## Idoneità {#eligibility}

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
>title="Stima profilo totale"
>abstract="Quando selezioni segmenti o regole di decisione, puoi visualizzare informazioni sui profili qualificati stimati."

Il **[!UICONTROL Idoneità dell’offerta]** Questa sezione ti consente di limitare l’offerta a profili specifici definiti utilizzando segmenti o regole di decisione.

>[!NOTE]
>
>Ulteriori informazioni sull’utilizzo di **segmenti** rispetto a **regole di decisione** in [questa sezione](#segments-vs-decision-rules).

* Per impostazione predefinita, il **[!UICONTROL Tutti i visitatori]** L’opzione è selezionata, il che significa che qualsiasi profilo sarà idoneo per ricevere l’offerta.

   ![](../assets/offer-eligibility-default.png)

* Puoi anche limitare la presentazione dell’offerta ai membri di uno o più [Segmenti Adobe Experience Platform](../../segment/about-segments.md).

   A questo scopo, attiva il **[!UICONTROL Visitatori che rientrano in uno o più segmenti]** , quindi aggiungi uno o più segmenti dal riquadro a sinistra e combinali utilizzando il comando **[!UICONTROL E]** / **[!UICONTROL Oppure]** operatori logici.

   ![](../assets/offer-eligibility-segment.png)

* Se si desidera associare un [regola di decisione](../offer-library/creating-decision-rules.md) all’offerta, seleziona **[!UICONTROL Per regola di decisione definita]**, quindi trascina la regola desiderata dal riquadro di sinistra a **[!UICONTROL Regola di decisione]** area.

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >Le offerte basate su eventi non sono attualmente supportate in [!DNL Journey Optimizer]. Se crei una regola di decisione basata su un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}, non potrai sfruttarlo in un’offerta.

Quando selezioni segmenti o regole di decisione, puoi visualizzare informazioni sui profili qualificati stimati. Clic **[!UICONTROL Aggiorna]** per aggiornare i dati.

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>Le stime del profilo non sono disponibili quando i parametri della regola includono dati non presenti nel profilo, come i dati contestuali. Ad esempio, una regola di idoneità che richiede che il tempo corrente sia di ≥80 gradi.

### Utilizzo di segmenti e regole di decisione {#segments-vs-decision-rules}

Per applicare un vincolo, è possibile limitare la selezione delle offerte ai membri di uno o più **Segmenti Adobe Experience Platform**, oppure puoi utilizzare una **regola di decisione**, entrambe le soluzioni corrispondono a utilizzi diversi.

Fondamentalmente, l’output di un segmento è un elenco di profili, mentre una regola di decisione è una funzione eseguita su richiesta su un singolo profilo durante il processo decisionale. La differenza tra questi due utilizzi è descritta di seguito.

* **Segmenti**

   Da un lato, i segmenti sono un gruppo di profili Adobe Experience Platform che corrispondono a una determinata logica basata sugli attributi del profilo e sugli eventi di esperienza. Tuttavia, Gestione offerte non ricalcola il segmento, che potrebbe non essere aggiornato al momento della presentazione dell’offerta.

   Ulteriori informazioni sui segmenti in [questa sezione](../../segment/about-segments.md).

* **Regole di decisione**

   D’altra parte, una regola di decisione si basa sui dati disponibili in Adobe Experience Platform e determina a chi può essere visualizzata un’offerta. Una volta selezionata in un’offerta o in una decisione per un determinato posizionamento, la regola viene eseguita ogni volta che viene presa una decisione, in modo che ogni profilo ottenga l’offerta più recente e migliore.

   Ulteriori informazioni sulle regole di decisione in [questa sezione](creating-decision-rules.md).

## Limitazione {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Informazioni sul limite delle offerte"
>abstract="In questo campo puoi specificare quante volte può essere presentata l’offerta."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="Usa limite"
>abstract="Per evitare di sollecitare eccessivamente i clienti, utilizza il limite per definire il numero massimo di volte in cui è possibile presentare un’offerta."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="Impostare la frequenza di limitazione"
>abstract="Puoi scegliere di reimpostare il contatore del limite di offerta su base giornaliera, settimanale o mensile."

[!CONTEXTUALHELP]
>id=&quot;ajo_decisioning_frequency_capping_impression&quot;
>title=&quot;Impression&quot;
>abstract=&quot;L’utilizzo delle impression come eventi di limitazione è disponibile solo per i canali in entrata.&quot;

Il limite viene utilizzato come vincolo per definire il numero massimo di volte in cui è possibile presentare un’offerta.

Limitare il numero di volte in cui gli utenti ricevono offerte specifiche consente di evitare di sollecitare eccessivamente i clienti e quindi di ottimizzare ogni punto di contatto con l’offerta migliore.

Per impostare i limiti, effettuare le seguenti operazioni.

1. Definisci il numero di volte in cui è possibile presentare l’offerta.

   ![](../assets/offer-capping-times.png)

   >[!NOTE]
   >
   >Il numero deve essere un numero intero maggiore di 0.

1. Specifica se desideri che il limite venga applicato a tutti gli utenti o a un profilo specifico:

   ![](../assets/offer-capping-total.png)

   * Seleziona **[!UICONTROL In totale]** per definire quante volte un’offerta può essere proposta al pubblico target combinato, ovvero a tutti gli utenti.

      Ad esempio, se sei un rivenditore di elettronica e hai concluso un&#39;operazione &quot;TV Doorbuster&quot;, vuoi che l&#39;offerta venga restituita solo 200 volte in tutti i profili.

   * Seleziona **[!UICONTROL Per profilo]** per definire quante volte un’offerta può essere proposta allo stesso utente.

      Ad esempio, se sei una banca con un&#39;offerta &quot;Carta di credito Platino&quot;, non vuoi che questa offerta venga visualizzata più di 5 volte per profilo. In effetti, si ritiene che se l&#39;utente ha visto l&#39;offerta 5 volte e non ha agito di conseguenza, ha una maggiore possibilità di agire sulla migliore offerta successiva.
   <!--
    Set the **[!UICONTROL Frequency]** to define how often the capping count is reset. To do so, define the time period for the counting (daily, weekly or monthly) and enter the number of days/weeks/months of your choice.
    ![](../assets/offer-capping-frequency.png)
    >[!NOTE]
    >
    >The reset happens at 12am UTC, on the day that you defined or on the first day of the week/month when applicable. The week start day is Sunday.
    
    For example, if you want the capping count to be reset every 2 weeks, select **[!UICONTROL Weekly]** from the **[!UICONTROL Repeat]** drop-down list and type **2** in the other field. The reset will happen every other Sunday at 12pm UTC.
    -->

1. Se hai definito diversi [rappresentazioni](add-representations.md) per l’offerta, specifica se desideri applicare il limite **[!UICONTROL In tutti i posizionamenti]** o **[!UICONTROL Per ogni posizionamento]**.

   ![](../assets/offer-capping-placement.png)

   * **[!UICONTROL In tutti i posizionamenti]**: i conteggi dei limiti calcolano il totale di tutte le decisioni relative ai posizionamenti associati all’offerta.

      Ad esempio, se un’offerta presenta **E-mail** posizionamento e **Web** e impostate la quota limite in corrispondenza di **2 per profilo in tutti i posizionamenti**, quindi ogni profilo potrebbe ricevere l’offerta fino a 2 volte in totale, indipendentemente dal mix di posizionamento.

   * **[!UICONTROL Per ogni posizionamento]**: i conteggi dei limiti applicheranno separatamente i conteggi delle decisioni per ciascun posizionamento.

      Ad esempio, se un’offerta presenta **E-mail** posizionamento e **Web** e impostate la quota limite in corrispondenza di **2 per profilo per ciascun posizionamento**, quindi ogni profilo potrebbe ricevere l’offerta fino a 2 volte per il posizionamento dell’e-mail e altre 2 volte per il posizionamento web.

1. Una volta salvata e approvata, se l’offerta è stata presentata il numero di volte che hai specificato in questo campo in base ai criteri e all’arco temporale definito, la sua consegna si interrompe.

Il numero di volte in cui viene proposta un’offerta viene calcolato al momento della preparazione dell’e-mail. Ad esempio, se prepari un’e-mail contenente una serie di offerte, questi numeri vengono conteggiati in base al tetto massimo, indipendentemente dal fatto che l’e-mail venga inviata o meno.

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>I contatori dei limiti vengono ripristinati alla scadenza dell’offerta o 2 anni dopo la data di inizio dell’offerta, a seconda di quale dei due eventi si verifica per primo. Scopri come definire la data di un’offerta in [questa sezione](creating-personalized-offers.md#create-offer).

### Impatto della modifica delle date sui limiti {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="La modifica delle date può influire sui limiti"
>abstract="Se a questa offerta viene applicato un limite, questo può essere influenzato quando modifichi la data di inizio o di fine."

Devi procedere con cautela quando modifichi la data di un’offerta, perché ciò può avere un impatto sui limiti se vengono soddisfatte le seguenti condizioni:

* L’offerta è [approvato](#review).
* [Limitazione](#capping) è già applicato all’offerta.
* Il limite è definito per profilo.

>[!NOTE]
>
>Scopri come definire la data di un’offerta in [questa sezione](creating-personalized-offers.md#create-offer).

Il limite per profilo memorizza i conteggi dei limiti su ciascun profilo. Quando modifichi la data di inizio e di fine di un’offerta approvata, il conteggio dei limiti per alcuni profili potrebbe essere influenzato in base ai diversi scenari descritti di seguito.

![](../assets/offer-capping-change-date.png)

Di seguito sono riportati gli scenari possibili in cui **modifica della data di inizio di un’offerta**:

| Scenario<br>Se... | Cosa succede:<br>allora... | Possibile impatto sul numero di limiti |
|--- |--- |--- |
| ... la data di inizio dell’offerta viene aggiornata prima della data di inizio dell’offerta originale, | ... il conteggio dei limiti inizierà nella nuova data di inizio. | No |
| ... la nuova data di inizio è precedente alla data di fine corrente, | ... il limite continuerà con una nuova data di inizio e il conteggio dei limiti precedente per ciascun profilo verrà riportato avanti. | No |
| ... la nuova data di inizio è successiva alla data di fine corrente, | ... il limite corrente scadrà e il nuovo conteggio dei limiti ricomincerà da 0 per tutti i profili nella nuova data di inizio. | Sì |

Di seguito sono riportati gli scenari possibili in cui **estensione di una data di fine offerta**:

| Scenario<br>Se... | Cosa succede:<br>allora... | Possibile impatto sul numero di limiti |
|--- |--- |--- |
| ... una richiesta di decisioni si verifica prima della data di fine dell’offerta originale, | ... il conteggio dei limiti verrà aggiornato e il conteggio dei limiti precedente per ciascun profilo verrà riportato avanti. | No |
| ... non si verifica alcuna richiesta di decisioni prima della data di fine originale, | ... il conteggio dei limiti verrà reimpostato sulla data di fine originale per ciascun profilo. Il nuovo conteggio dei limiti riprenderà quindi da 0 per tutte le nuove richieste di decisioni che si verificheranno dopo la data di fine originale. | Sì |

**Esempio**

Supponiamo che tu abbia un’offerta con una data di inizio originale impostata su **Gennaio 1**, scadenza il **31 gennaio**.

1. Ai profili X, Y e Z viene presentata l’offerta.
1. On **10 gennaio**, la data di fine dell’offerta viene modificata in **15 febbraio**.
1. **Dall’11 gennaio al 31 gennaio**, all’offerta viene presentato solo il profilo Z.

   * Perché una richiesta di decisioni si è verificata prima della data di fine originale **per il profilo Z**, la data di fine dell’offerta può essere estesa a **15 febbraio**.
   * Tuttavia, poiché non si è verificata alcuna attività prima della data di fine originale per **profili X e Y**, i contatori scadranno e i conteggi dei limiti verranno reimpostati su 0 il **31 gennaio**.

![](../assets/offer-capping-change-date-ex.png)
