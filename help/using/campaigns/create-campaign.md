---
solution: Journey Optimizer
product: journey optimizer
title: Creare una campagna
description: Scopri come creare campagne in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 9%

---

# Creare una campagna {#create-campaign}

>[!NOTE]
>
>Prima di creare una nuova campagna, assicurati di disporre di un canale di superficie (ad es. un messaggio preimpostato) e di un segmento Adobe Experience Platform pronto per l’uso. Ulteriori informazioni in queste sezioni:
>
>* [Creare superfici di canale](../configuration/channel-surfaces.md)
>* [Introduzione ai segmenti](../segment/about-segments.md)


## Creare la prima campagna {#create}

1. Accedere al **[!UICONTROL Campagne]** menu, quindi fai clic su **[!UICONTROL Creare una campagna]**.

   >[!NOTE]
   >
   >Puoi anche duplicare una campagna live esistente per crearne una nuova. [Ulteriori informazioni](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

1. In **[!UICONTROL Proprietà]** specifica quando eseguire la campagna:

   * **[!UICONTROL Pianificato]**: esegue la campagna immediatamente o in una data specificata. Le campagne pianificate sono finalizzate all’invio di **marketing** digitare messaggi.
   * **[!UICONTROL Attivazione dall’API]**: esegui la campagna utilizzando una chiamata API. Le campagne con attivazione API sono mirate all’invio di **transazionale** messaggi, ovvero messaggi inviati in seguito a un’azione eseguita da un singolo utente: reimpostazione della password, abbandono della scheda, ecc. [Scopri come attivare una campagna utilizzando le API](api-triggered-campaigns.md)

1. In **[!UICONTROL Azioni]** sezione , scegli il canale e la superficie del canale da utilizzare per inviare il messaggio, quindi fai clic su **[!UICONTROL Crea]**.

   Una “superficie” è una configurazione definita da un [amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Nell’elenco a discesa sono elencate solo le superfici del canale compatibili con il tipo di campagna di marketing.

1. Specifica un titolo e una descrizione per la campagna.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. In **[!UICONTROL Azioni]** configura il messaggio da inviare con la campagna:

   1. Fai clic sul pulsante **[!UICONTROL Modifica contenuto]** , quindi configura e progetta il contenuto del messaggio. [Ulteriori informazioni sui messaggi](../messages/get-started-content.md).

      Scopri i passaggi dettagliati per creare il contenuto del messaggio nella pagina seguente:

      * [Creare un messaggio e-mail](../messages/create-email.md)
      * [Creare una notifica push](../messages/create-push.md)
      * [Creare un messaggio SMS](../messages/create-sms.md)
   1. Una volta definito il contenuto, utilizza il **[!UICONTROL Simulazione del contenuto]** per visualizzare in anteprima e testare il contenuto con i profili di test. [Ulteriori informazioni](../design/preview.md).

   1. Fai clic sulla freccia per tornare alla schermata di creazione della campagna.

      ![](assets/create-campaign-design.png)

   1. In **[!UICONTROL Tracciamento delle azioni]** specifica se desideri tenere traccia delle reazioni dei destinatari alla consegna: puoi tenere traccia dei clic e/o delle aperture.

      I risultati del tracciamento saranno accessibili dal rapporto della campagna una volta che la campagna sarà stata eseguita. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report.md)


1. Definisci il pubblico di cui eseguire il targeting. A questo scopo, fai clic sul pulsante **[!UICONTROL Selezionare il pubblico]** per visualizzare l’elenco dei segmenti Adobe Experience Platform disponibili. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

   >[!NOTE]
   >
   >Per le campagne con attivazione API, il pubblico deve essere impostato tramite chiamata API. [Ulteriori informazioni](api-triggered-campaigns.md)

   In **[!UICONTROL Spazio dei nomi identità]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Gli individui appartenenti a un segmento che non hanno l’identità selezionata (spazio dei nomi) tra le loro diverse identità non verranno presi di mira dalla campagna.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

1. Per eseguire la campagna in una data specifica o con una frequenza ricorrente, configura la **[!UICONTROL Pianificazione]** sezione . [Scopri come pianificare le campagne](#schedule)

1. Per assegnare etichette di utilizzo dati personalizzate o di base alla campagna, fai clic sul pulsante **[!UICONTROL Gestisci accesso]** pulsante . [Ulteriori informazioni sul controllo dell&#39;accesso a livello di oggetto (OLA)](../administration/object-based-access.md)

Quando la campagna è pronta, puoi rivederla e pubblicarla. [Ulteriori informazioni](#review-activate)

## Pianificare una campagna {#schedule}

Per impostazione predefinita, le campagne iniziano una volta attivate manualmente e terminano non appena il messaggio è stato inviato una volta.

Puoi definire la frequenza con cui deve essere inviato il messaggio della campagna. Per eseguire questa operazione, utilizza la variabile **[!UICONTROL Trigger delle azioni]** nella schermata di creazione della campagna per specificare se la campagna deve essere eseguita ogni giorno, settimanalmente o mensilmente.

Se non desideri eseguire la campagna subito dopo l’attivazione, puoi specificare la data e l’ora in cui il messaggio deve essere inviato utilizzando **[!UICONTROL Inizio campagna]** opzione . La  **[!UICONTROL Fine campagna]** consente di specificare quando interrompere l’esecuzione di una campagna ricorrente.

![](assets/create-campaign-schedule.png)

## Modalità di consegna rapida {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Modalità di consegna rapida"
>abstract="La modalità di consegna rapida consente di inviare messaggi ad alta velocità sul canale push a una dimensione di pubblico inferiore a 30M."

La modalità di consegna rapida, precedentemente nota come modalità Burst nei percorsi, è una [!DNL Journey Optimizer] add-on che consente l&#39;invio rapido di messaggi push in grandi volumi attraverso le campagne.

La consegna rapida viene utilizzata quando il ritardo nella consegna dei messaggi è di importanza critica per l’azienda, quando si desidera inviare un avviso push urgente sui telefoni cellulari, ad esempio una notizia di emergenza per gli utenti che hanno installato la tua app di canale di notizie.

Per ulteriori informazioni sulle prestazioni quando si utilizza la modalità di consegna rapida, consulta [Descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html).

### Prerequisiti {#prerequisites}

I messaggi di consegna rapida sono forniti con i seguenti requisiti:

* La consegna rapida è disponibile per **[!UICONTROL Pianificato]** solo per le campagne e non è disponibile per le campagne con attivazione API,
* Nel messaggio push non è consentita alcuna personalizzazione,
* Il pubblico di destinazione deve contenere meno di 30 milioni di profili,
* Puoi eseguire fino a 5 campagne contemporaneamente utilizzando la modalità di consegna rapida.

### Attiva modalità di consegna rapida

1. Creare una campagna di notifica push e attivare **[!UICONTROL Consegna rapida]** opzione .

![](assets/create-campaign-burst.png)

1. Configura il contenuto del messaggio e seleziona il pubblico di cui eseguire il targeting. [Scopri come creare una campagna](#create)

   >[!IMPORTANT]
   >
   >Assicurati che il contenuto del messaggio non includa alcuna personalizzazione e che il pubblico contenga meno di 30M profili.

1. Rivedi e attiva la campagna come di consueto. In modalità di test i messaggi non vengono inviati tramite la modalità di consegna rapida. [Scopri come rivedere e attivare una campagna](review-activate-campaign.md)
