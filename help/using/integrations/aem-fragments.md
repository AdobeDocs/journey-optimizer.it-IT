---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti di contenuto di AEM
description: Scopri come accedere e gestire i frammenti di contenuto di AEM
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '1272'
ht-degree: 0%

---

# Utilizzare i frammenti di contenuto di Adobe Experience Manager {#aem-fragments}

>[!AVAILABILITY]
>
>Questa integrazione si applica a **Adobe Experience Manager as a Cloud Service Sites**, solo per **Frammenti di contenuto**. Journey Optimizer legge i frammenti dal livello **Pubblica** (non Autore).

L’integrazione tra Adobe Experience Manager e Journey Optimizer segue questo flusso di dati:

1. **[Configura Dispatcher](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer#dispatcher-configuration){target="_blank"}**: per consentire a Journey Optimizer di accedere ai frammenti di contenuto di Adobe Experience Manager tramite l&#39;API di gestione dei frammenti di contenuto, è necessario prima configurare Dispatcher. Questo è un prerequisito per l’integrazione.

1. **[Crea e crea](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)**: il contenuto viene creato e configurato in Adobe Experience Manager come frammenti di contenuto.

1. **[Assegnazione tag](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)**: i frammenti di contenuto devono essere contrassegnati con il tag specifico di Journey Optimizer (`ajo-enabled:{OrgId}/{SandboxName}`).

1. **[Pubblicazione](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)**: i frammenti di contenuto vengono pubblicati in Adobe Experience Manager, rendendoli disponibili in Journey Optimizer.

1. **[Accesso](#aem-add)**: Journey Optimizer recupera e visualizza in tempo reale i frammenti di contenuto disponibili dall&#39;istanza Adobe Experience Manager Publish.

1. **[Integrazione](#aem-add)**: i frammenti di contenuto sono selezionati e integrati in campagne o percorsi.

Quando un frammento di contenuto viene pubblicato in Adobe Experience Manager, viene inviato un evento per aggiornare il contenuto sul lato Journey Optimizer. Se l’aggiornamento ha esito positivo, il frammento di contenuto diventa disponibile entro circa 5 minuti per i percorsi unitari e nel batch di elaborazione successivo per i casi di utilizzo batch. Quando l’aggiornamento è disponibile in Journey Optimizer, il contenuto pubblicato più recente viene utilizzato in tutte le campagne e i percorsi applicabili.

>[!AVAILABILITY]
>
>Per i clienti del settore sanitario, l&#39;integrazione è abilitata solo dopo aver concesso in licenza le offerte aggiuntive Journey Optimizer Healthcare Shield e Adobe Experience Manager Extended Security for Healthcare.

## Creare e assegnare un tag in Experience Manager

>[!IMPORTANT]
>
>Per consentire a Journey Optimizer di accedere ai frammenti di contenuto di Adobe Experience Manager tramite l&#39;API di gestione dei frammenti di contenuto, devi prima [configurare Dispatcher](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer#dispatcher-configuration){target="_blank"}.

Prima di utilizzare il frammento di contenuto in Journey Optimizer, è necessario creare un tag specifico per Journey Optimizer:

1. Accedi al tuo ambiente **Experience Manager**.

1. Dal menu **Strumenti**, seleziona **Assegnazione tag**.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Fare clic su **Crea tag**.

1. Verificare che l&#39;ID sia conforme alla sintassi seguente: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

1. Fai clic su **Crea**.

1. Definisci il modello per frammenti di contenuto come descritto nella [documentazione di Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"} e assegna il nuovo tag Journey Optimizer creato.

Questa connessione in tempo reale garantisce che il contenuto sia sempre aggiornato, ma significa anche che eventuali modifiche ai frammenti pubblicati influiranno immediatamente sulle campagne e sui percorsi attivi.

Ora puoi iniziare a creare e configurare il frammento di contenuto per un utilizzo successivo in Journey Optimizer. Ulteriori informazioni sono disponibili nella [documentazione di Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}.

## Aggiungere frammenti di contenuto Experience Manager {#aem-add}

Dopo aver creato e personalizzato i frammenti di contenuto di AEM, puoi importarli nella campagna o nel percorso di ottimizzazione del Percorso.

1. Crea la tua [campagna](../campaigns/create-campaign.md) o [Percorso](../building-journeys/journey-gs.md).

1. Per accedere al frammento di contenuto AEM, fai clic sull&#39;![icona Personalization](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) in un campo di testo qualsiasi oppure apri il codice sorgente tramite un componente di contenuto HTML.

   ![](assets/aem_campaign_2.png)

1. Dal menu **[!UICONTROL Frammento di contenuto di AEM]** nel riquadro a sinistra, fare clic su **[!UICONTROL Apri selettore CF di AEM]**.

   ![](assets/aem_campaign_3.png)

1. Sfoglia l&#39;elenco e seleziona un **[!UICONTROL frammento di contenuto]** da importare nel contenuto di Journey Optimizer.

   >[!NOTE]
   >
   > Se il frammento contiene una o più varianti di **published**, nel selettore viene visualizzato il menu a discesa **[!UICONTROL Variante]**. Se non è selezionata alcuna **[!UICONTROL variante]**, la variante **principale** viene utilizzata automaticamente. Ulteriori informazioni in [Utilizzo delle varianti di frammenti di contenuto](#aem-variations).

1. Fai clic su **[!UICONTROL Mostra filtri]** per ottimizzare l&#39;elenco dei frammenti di contenuto.

   Per impostazione predefinita, il filtro Frammento di contenuto è predefinito per visualizzare solo il contenuto approvato.

   ![](assets/aem_campaign_4.png)

1. Dopo aver selezionato il **[!UICONTROL frammento di contenuto]**, fai clic su **[!UICONTROL Seleziona]** per aggiungerlo.

   ![](assets/aem_campaign_5.png)

1. Fai clic su **[!UICONTROL Visualizza frammento]** per visualizzare le informazioni sul frammento. L&#39;apertura del menu **[!UICONTROL Informazioni frammento]** comporta l&#39;attivazione della modalità di sola lettura per l&#39;editor.

   Seleziona **[!UICONTROL Anteprima]** dal menu di destra per visualizzare il frammento in Adobe Experience Manager.

   ![](assets/aem_campaign_7.png)

1. Fai clic sull&#39;![icona Altre azioni](assets/do-not-localize/Smock_MoreSmallList_18_N.svg) per accedere al menu avanzato del frammento:

   * **[!UICONTROL Scambia frammento]**
   * **[!UICONTROL Esplora riferimenti]**
   * **[!UICONTROL Apri in AEM]**

   ![](assets/aem_campaign_8.png)

1. Scegli i campi desiderati dal **[!UICONTROL frammento]** da aggiungere al contenuto.

   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. Per rendere visibile un URL immagine memorizzato in un attributo del frammento di contenuto, ad esempio un percorso o un campo URL dal modello del frammento, inseriscilo nel HTML con un tag `<img>` e l’attributo del frammento come origine, ad esempio:

   ```html
   <img src="[insert your AEM Content Fragment attribute here]">
   ```

   >[!NOTE]
   >
   >Gli URL relativi dell&#39;immagine da Adobe Experience Manager non sono supportati, utilizza **URL assoluti**.

1. Seleziona **Pillole: disattivato** per abilitare l&#39;esperienza pillole per migliorare la leggibilità nascondendo percorsi attributo lunghi.

   ![](assets/aem_campaign_10.png)

1. Per utilizzare **segnaposto di personalizzazione** creati in Adobe Experience Manager all&#39;interno del testo del frammento, definirli nel frammento di contenuto in Adobe Experience Manager nel modo seguente: `{{name}}`.

   In Journey Optimizer, questi token sono segnaposto. Con l&#39;esperienza **pillole** attivata, vengono visualizzate nella sezione **[!UICONTROL Frammento di contenuto di AEM]** della barra a destra insieme ai campi del frammento.

1. Per abilitare la personalizzazione in tempo reale, tutti i segnaposto utilizzati all&#39;interno di un **[!UICONTROL frammento di contenuto]** devono essere dichiarati esplicitamente dall&#39;utente come parametri nel tag helper del frammento. Mappa tali segnaposto agli attributi di profilo, agli attributi contestuali, alle stringhe statiche o alle variabili predefinite come segue:

   1. **Mappatura attributi contestuali o di profilo**: assegnare il segnaposto a un attributo contestuale o di profilo, ad esempio nome = profile.person.name.firstName.

   1. **Mappatura stringa statica**: assegna un valore stringa fisso inserendolo tra virgolette doppie, ad esempio nome = &quot;John&quot;.

   1. **Mappatura variabile**: fare riferimento a una variabile dichiarata in precedenza all&#39;interno dello stesso HTML, ad esempio name = &#39;variableName&#39;.
In questo caso, assicurati che **_variableName_** sia dichiarato prima di aggiungere l&#39;ID frammento, utilizzando la seguente sintassi:

      ```html
      {% let variableName = attribute name %} 
      ```

   Nell&#39;esempio seguente, il segnaposto **_mese_** è mappato all&#39;attributo **_profile.person.bornDate_** all&#39;interno del frammento.

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**. Ora puoi testare e controllare il contenuto del messaggio come descritto in [questa sezione](../content-management/preview.md).

   <!--Note that the Content Fragment you selected stays active for this message. When you open the Personalization Editor in another field or content block, you can keep working with the same fragment from the **[!UICONTROL AEM Content Fragment]** section and add more fields without reopening **[!UICONTROL Open AEM CF selector]**.-->

Dopo aver eseguito i test e convalidato il contenuto, puoi [inviare la tua campagna](../campaigns/review-activate-campaign.md) o [pubblicare il percorso](../building-journeys/publish-journey.md) al tuo pubblico.

Adobe Experience Manager consente di identificare le campagne o i percorsi Journey Optimizer in cui viene utilizzato un frammento di contenuto. Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references){target="_blank"}.

## Utilizzo delle varianti di frammenti di contenuto {#aem-variations}

In Adobe Experience Manager, ogni frammento di contenuto è costituito dai seguenti elementi:

* **Principale**: il contenuto principale del frammento, che esiste sempre, non può essere eliminato e costituisce la base per tutte le varianti.
* **Varianti**: una o più permutazioni di **Principale** create dagli autori per canali o scenari specifici. Le varianti risiedono all&#39;interno del frammento non come risorse separate e possono essere confrontate e sincronizzate con **Principale**.

➡️ [Ulteriori informazioni nella documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-variations)

Esempi di casi di utilizzo di varianti:

* Una versione breve della copia per una notifica push e una versione più lunga per l’e-mail.
* Regolazioni del tono regionali senza creare un frammento separato.
* Messaggistica specifica per il canale (ad esempio, web rispetto a mobile).

Journey Optimizer consente di scegliere la variante da utilizzare quando si inserisce un frammento, in modo che campagne o percorsi diversi possano fare affidamento su rappresentazioni diverse dello stesso contenuto sorgente in Adobe Experience Manager senza duplicare i frammenti.

Per selezionare una variante:

1. Apri una [campagna](../campaigns/create-campaign.md) o [percorso](../building-journeys/journey-gs.md).

1. Fai clic sull&#39;icona ![Personalization](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) in un campo di testo oppure apri l&#39;origine HTML da un componente di contenuto HTML.

1. Da **[!UICONTROL Frammento di contenuto AEM]**, fare clic su **[!UICONTROL Apri selettore CF]**.

   ![](assets/aem_campaign_3.png)

1. Per selezionare un frammento di contenuto di Adobe Experience Manager specifico per le impostazioni internazionali nella vista tabella, utilizzare **[!UICONTROL Personalizza tabella]** per aggiungere la colonna **[!UICONTROL Lingua]**. I valori delle impostazioni internazionali vengono visualizzati nella tabella, consentendo di identificare e selezionare il frammento appropriato.

   ![](assets/cf-variation-2.png)

1. Seleziona il **[!UICONTROL frammento di contenuto]**.

1. Fai clic sull&#39;icona ![informazioni](assets/do-not-localize/info-icon.svg) per aprire il menu **[!UICONTROL Dettagli]**. Se il frammento ha una o più varianti pubblicate, accanto ai dettagli del frammento viene visualizzato un menu a discesa **[!UICONTROL Variante]**.

   ![](assets/cf-variation-5.png)

1. Dal menu **[!UICONTROL Dettagli rapidi]**, fai clic su **[!UICONTROL Esplora riferimenti]** per aprire le opzioni correlate in Adobe Experience Manager per i dettagli della variante, l&#39;anteprima e la bozza, se disponibili.

1. Scegli la tua variante, quindi fai clic su **[!UICONTROL Seleziona]**.

   >[!NOTE]
   >
   > Se non selezioni una variante o se il frammento è stato aggiunto prima che il supporto della variante fosse disponibile, Journey Optimizer utilizza automaticamente la variante **Principale** al momento della consegna.

Dopo aver inserito un frammento con una variante, la ripubblicazione in Adobe Experience Manager aggiorna automaticamente ogni **variante a cui si fa riferimento** nelle campagne o nei percorsi attivi. Le anteprime e le bozze utilizzano ancora la variante scelta, con il contenuto pubblicato più recente per tale variante.
