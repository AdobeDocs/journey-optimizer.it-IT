---
title: Creare una campagna
description: Scopri come creare campagne in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 13%

---

# Creare una campagna {#create-campaign}

>[!NOTE]
>
>Prima di creare una nuova campagna, assicurati di disporre di un canale di superficie (ad es. un messaggio preimpostato) e di un segmento Adobe Experience Platform pronto per l’uso. Ulteriori informazioni in queste sezioni:
>
>* [Creare superfici di canale](../configuration/channel-surfaces.md)
>* [Introduzione ai segmenti](../segment/about-segments.md)


I passaggi per creare una campagna sono i seguenti:

1. Accedere al **[!UICONTROL Campaigns]** menu, quindi fai clic su **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

   >[!NOTE]
   >
   >Puoi anche duplicare una campagna live esistente per crearne una nuova. [Ulteriori informazioni](modify-stop-campaign.md#duplicate) <!-- check if only live campaigns-->

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. In **[!UICONTROL Actions]** sezione , scegli il canale e la superficie del canale da utilizzare per inviare il messaggio, quindi fai clic su **[!UICONTROL Create]**.

   ![](assets/create-campaign-action.png)

   Una “superficie” è una configurazione definita da un [amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni](../configuration/channel-surfaces.md).

   >[!NOTE]
   >
   >Nell’elenco a discesa sono elencate solo le superfici del canale compatibili con il tipo di campagna (marketing o transazionale).

1. Specifica un titolo e una descrizione per la campagna.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. In **[!UICONTROL Actions]** configura il messaggio da inviare con la campagna:

   1. Fai clic sul pulsante **[!UICONTROL Edit content]** , quindi configura e progetta il contenuto del messaggio. [Ulteriori informazioni sui messaggi](../messages/get-started-content.md).

      Scopri i passaggi dettagliati per creare il contenuto del messaggio nella pagina seguente:

      * [Creare un messaggio e-mail](../messages/create-email.md)
      * [Creare una notifica push](../messages/create-push.md)
      * [Creare un messaggio SMS](../messages/create-sms.md)
   1. Una volta definito il contenuto, utilizza **[!UICONTROL Simulate content]** per visualizzare in anteprima e testare il contenuto con i profili di test. [Ulteriori informazioni](../design/preview.md).
   1. Fai clic sulla freccia per tornare alla schermata di creazione della campagna.

      ![](assets/create-campaign-design.png)

   1. In **[!UICONTROL Actions tracking]** specifica se desideri tenere traccia delle reazioni dei destinatari alla consegna: puoi tenere traccia dei clic e/o delle aperture.

      I risultati del tracciamento saranno accessibili dal rapporto della campagna una volta che la campagna sarà stata eseguita. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report.md)


1. Definisci il pubblico di cui eseguire il targeting. A questo scopo, fai clic sul pulsante **[!UICONTROL Select audience]** per visualizzare l’elenco dei segmenti Adobe Experience Platform disponibili. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

   <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

   In **[!UICONTROL Identity namespace]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Gli individui appartenenti a un segmento che non hanno l’identità selezionata (spazio dei nomi) tra le loro diverse identità non verranno presi di mira dalla campagna.

1. Configura la pianificazione della campagna nei campi delle date di inizio e di fine. Per impostazione predefinita, le campagne iniziano una volta attivate manualmente e terminano non appena il messaggio è stato inviato una volta.

1. Inoltre, puoi specificare una frequenza per l’esecuzione dell’azione configurata nella campagna.

   <!-- NOTE For API-triggered campaigns, scheduling at a specific date and time with recurrence is not available as action is triggered via API. However, start and end date are relevant to ensure that, if an API call is made prior of after the window, then those get errored.-->

   ![](assets/create-campaign-schedule.png)

<!--1. If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

Quando la campagna è pronta, puoi rivederla e pubblicarla. [Ulteriori informazioni](#review-activate);

## Rivedere e attivare una campagna {#review-activate}

Una volta configurata la campagna, devi rivederne il parametro e il contenuto prima di attivarlo. Per farlo, esegui questi passaggi:

1. Nella schermata di configurazione della campagna, fai clic su **[!UICONTROL Review to activate]** per visualizzare un riepilogo della campagna.

   Il riepilogo consente di modificare la campagna se necessario e di verificare se è presente un parametro errato o mancante.

   >[!IMPORTANT]
   >
   >In caso di errori, non è possibile attivare la campagna. Risolvi gli errori prima di procedere.

   ![](assets/create-campaign-alerts.png)

1. Verifica che la campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Activate]**.

   ![](assets/create-campaign-review.png)

1. La campagna viene ora attivata. Il suo status è **[!UICONTROL Live]** oppure **[!UICONTROL Scheduled]** se hai inserito una data di inizio. [Ulteriori informazioni sugli stati delle campagne](get-started-with-campaigns.md#statuses).

   Il messaggio configurato nella campagna viene inviato immediatamente o alla data specificata.

   >[!NOTE]
   >
   >La **[!UICONTROL Completed]** lo stato viene assegnato automaticamente a una campagna 3 giorni dopo l’attivazione o alla data di fine, se presenta un’esecuzione ricorrente.
   >
   >Se non è stata specificata alcuna data di fine, la campagna manterrà il **[!UICONTROL Live]** stato. Per modificarla, è necessario arrestare manualmente la campagna. [Scopri come interrompere una campagna](modify-stop-campaign.md)

1. Una volta che una campagna è stata attivata, puoi controllarne in qualsiasi momento le informazioni aprendole. Il riepilogo ti consente di ottenere statistiche sul numero di profili target e azioni consegnate e non riuscite.

   È inoltre possibile ottenere statistiche aggiuntive nei rapporti dedicati facendo clic sul pulsante **[!UICONTROL Reports]** pulsante . [Ulteriori informazioni](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)
