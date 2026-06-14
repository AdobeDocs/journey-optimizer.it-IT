---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti di contenuto di AEM
description: Scopri come accedere e gestire i frammenti di contenuto di AEM
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
TQID: https://experienceleague.adobe.com/QFZt5R2bGJMIwT9okjkcGWxN9cj56Mi77XdCgddCleU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 1780
ht-degree: 0%

---

# Utilizzare i frammenti di contenuto di Adobe Experience Manager {#aem-fragments}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come assegnare tag, aggiungere e personalizzare frammenti di contenuto Adobe Experience Manager nelle campagne e nei percorsi Journey Optimizer, incluso l&#39;utilizzo delle varianti e di Experience Decisioning.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Le esperienze esistenti del **selettore risorse** e del **selettore frammento di contenuto** nei flussi di lavoro di Adobe Journey Optimizer verranno sostituite da **Contenuto verificato**. Contenuto verificato fornisce un’interfaccia unificata basata sull’intelligenza artificiale per individuare e selezionare Assets, frammenti di contenuto e elementi multimediali dinamici direttamente nei flussi di lavoro di authoring di AJO. Le integrazioni esistenti continueranno a funzionare durante il periodo di transizione.

>[!ENDSHADEBOX]

>[!NOTE]
>
>**I frammenti di contenuto di AEM** sono creati in Adobe Experience Manager e utilizzati in [!DNL Journey Optimizer]. Sono diversi da:
>
>* **[Frammenti](../content-management/fragments.md)**: componenti di contenuto riutilizzabili creati in [!DNL Journey Optimizer] e utilizzati nelle e-mail tra campagne e percorsi.
>* **[Frammenti di Percorso](../building-journeys/journey-fragments.md)**: set riutilizzabili di nodi di percorso inseriti in percorsi.

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

## Creare e assegnare un tag in Experience Manager {#create-tag}

>[!IMPORTANT]
>
>Per consentire a Journey Optimizer di accedere ai frammenti di contenuto di Adobe Experience Manager tramite l&#39;API di gestione dei frammenti di contenuto, devi prima [configurare Dispatcher](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer#dispatcher-configuration){target="_blank"}.

Journey Optimizer visualizza un frammento di contenuto nel selettore Frammento di contenuto solo quando contiene un tag per la **organizzazione** e la **sandbox**. Tale requisito è intenzionale: mantiene fuori da Journey Optimizer contenuti Experience Manager non correlati o non approvati.

Assegna un tag il cui ID segue `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`, utilizzando l&#39;ID organizzazione Journey Optimizer e il nome della sandbox al posto dei segnaposto, ad esempio `ajo-enabled:123A12A123A123A12A@AdobeOrg/prod`.

Per creare il tag in Experience Manager:

1. Vai a **Strumenti** > **Assegnazione tag**.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Crea una struttura di tag nidificata in modo che l’ID tag completo corrisponda al formato precedente:

   1. A livello di radice, creare una cartella denominata `ajo-enabled`.

   1. In `ajo-enabled`, crea un tag per il tuo ID organizzazione, ad esempio `123A12A123A123A12A@AdobeOrg`.

   1. Crea un tag per la sandbox sotto tale tag organizzazione, ad esempio `prod`.

   Il percorso combinato restituisce un ID tag come `ajo-enabled:123A12A123A123A12A@AdobeOrg/prod`.

1. Per applicarlo a un frammento di contenuto, apri il frammento di contenuto nell’editor.

1. In **Proprietà**, aggiungi il tag creato.

1. Salva il frammento.

➡️ [Ulteriori informazioni sui tag nella documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)

## Aggiungere frammenti di contenuto Experience Manager {#aem-add}

Dopo aver creato e personalizzato i frammenti di contenuto di AEM, puoi importarli nella campagna o nel percorso di ottimizzazione del Percorso.

1. Crea la tua [campagna](../campaigns/create-campaign.md) o [Percorso](../building-journeys/journey-gs.md).

1. Per accedere al frammento di contenuto AEM, fai clic sull&#39;![icona Personalization](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) in un campo di testo qualsiasi oppure apri il codice sorgente tramite un componente di contenuto HTML.

   ![](assets/aem_campaign_2.png)

1. Dal menu **[!UICONTROL Frammento di contenuto di AEM]** nel riquadro a sinistra, fare clic su **[!UICONTROL Apri AEM Content Advisor]**.

   ![](assets/cf-variation-1.png)

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
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.
    
    -->

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

   Il frammento di contenuto selezionato rimane attivo per questo messaggio. Quando si apre l&#39;Editor di Personalization in un altro campo o blocco di contenuto, è possibile continuare a utilizzare lo stesso frammento dalla sezione **[!UICONTROL Frammento di contenuto di AEM]** e aggiungere altri campi senza riaprire **[!UICONTROL Apri AEM Content Advisor]**.

Dopo aver eseguito i test e convalidato il contenuto, puoi [inviare la tua campagna](../campaigns/review-activate-campaign.md) o [pubblicare il percorso](../building-journeys/publish-journey.md) al tuo pubblico.

Adobe Experience Manager consente di identificare le campagne o i percorsi Journey Optimizer in cui viene utilizzato un frammento di contenuto. Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references){target="_blank"}.

## Utilizzare Frammenti di contenuto di AEM con Experience Decisioning {#aem-decisioning}

>[!AVAILABILITY]
>
>Questa funzione è disponibile in Disponibilità limitata per i canali in uscita con supporto Decisioning. Per richiedere l’accesso, contatta il tuo rappresentante Adobe.

I frammenti di contenuto di AEM possono essere utilizzati anche come attributi di elementi dell&#39;offerta in **Experience Decisioning**. Mappando i campi del frammento di contenuto agli attributi dell’elemento decisione, puoi utilizzare modelli decisionali, formule e criteri di classificazione di Journey Optimizer per ottimizzare quale frammento viene distribuito a ciascun profilo.

### Prerequisiti e guardrail

* I frammenti di contenuto devono essere contrassegnati in Adobe Experience Manager con il tag `ajo-enabled:{OrgId}/{SandboxName}` prima di essere visualizzati nel selettore delle decisioni. [Scopri come creare e assegnare un tag](#create-tag)
* Sono disponibili solo frammenti di contenuto con stato **pubblicato**.
* Puoi aggiungere fino a **cinque** frammenti di contenuto AEM a un singolo elemento decisionale.

### Sfruttare i frammenti di contenuto di AEM in Decisioning

Dopo la creazione e la pubblicazione del frammento di contenuto di AEM, è necessario:

1. Legarlo a un elemento di decisione selezionandolo negli attributi dell’elemento di decisione.
1. Sfruttarla in una policy decisionale per fornire il contenuto giusto al cliente giusto.

➡️ [Associare un frammento di contenuto AEM a un elemento di decisione](../experience-decisioning/items.md#aem-fragments)

➡️ [Sfruttare i frammenti di contenuto di AEM in un criterio decisionale](../experience-decisioning/fragments-decision-policies.md#aem-fragments-decisioning)

## Utilizzo delle varianti di frammenti di contenuto {#aem-variations}

In Adobe Experience Manager, ogni frammento di contenuto è costituito dai seguenti elementi:

* **Principale**: il contenuto principale del frammento, che esiste sempre, non può essere eliminato e costituisce la base per tutte le varianti.
* **Varianti**: una o più permutazioni di **Principale** create dagli autori per canali o scenari specifici. Le varianti risiedono all&#39;interno del frammento non come risorse separate e possono essere confrontate e sincronizzate con **Principale**.

Esempi di casi di utilizzo di varianti:

* Una versione breve della copia per una notifica push e una versione più lunga per l’e-mail.
* Regolazioni del tono regionali senza creare un frammento separato.
* Messaggistica specifica per il canale (ad esempio, web rispetto a mobile).

➡️ [Ulteriori informazioni nella documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-variations)

Journey Optimizer consente di scegliere la variante da utilizzare quando si inserisce un frammento, in modo che campagne o percorsi diversi possano fare affidamento su rappresentazioni diverse dello stesso contenuto sorgente in Adobe Experience Manager senza duplicare i frammenti.

Per selezionare una variante:

1. Apri una [campagna](../campaigns/create-campaign.md) o [percorso](../building-journeys/journey-gs.md).

1. Fai clic sull&#39;icona ![Personalization](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) in un campo di testo oppure apri l&#39;origine HTML da un componente di contenuto HTML.

1. Da **[!UICONTROL Frammento di contenuto di AEM]**, fare clic su **[!UICONTROL Apri AEM Content Advisor]**.

   ![](assets/cf-variation-1.png)

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
