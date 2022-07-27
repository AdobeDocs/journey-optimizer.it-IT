---
title: Creare una campagna
description: Scopri come creare campagne in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 5%

---

# Creare una campagna {#create-campaign}

>[!NOTE]
>
>Prima di creare una nuova campagna, assicurati di disporre di un canale di superficie (ad es. un messaggio preimpostato) e di un segmento Adobe Experience Platform pronto per l’uso. Ulteriori informazioni in queste sezioni:
>
>* [Creare superfici di canale](../configuration/channel-surfaces.md)
>* [Introduzione ai segmenti](../segment/about-segments.md)


## Configurare una campagna {#configure}

I passaggi per creare una campagna sono i seguenti:

1. Accedere al **[!UICONTROL Campaigns]** menu, quindi fai clic su **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

1. In **[!UICONTROL Properties]** specifica quando eseguire la campagna:

   * **[!UICONTROL Scheduled]**: esegue la campagna immediatamente o in una data specificata. Le campagne pianificate sono finalizzate all’invio di **marketing** digitare messaggi.
   * **[!UICONTROL API-triggered]**: esegui la campagna utilizzando una chiamata API. Le campagne con attivazione API sono mirate all’invio di **transazionale** messaggi, ovvero messaggi inviati in seguito a un’azione eseguita da un singolo utente: reimpostazione della password, abbandono della scheda, ecc. [Scopri come attivare una campagna utilizzando le API](api-triggered-campaigns.md)

1. In **[!UICONTROL Actions]** sezione , scegli il canale e la superficie del canale da utilizzare per inviare il messaggio, quindi fai clic su **[!UICONTROL Create]**.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Nell’elenco a discesa sono elencate solo le superfici del canale compatibili con il tipo di campagna (marketing o transazionale).

1. Specifica un titolo e una descrizione per la campagna.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. In **[!UICONTROL Actions]** configura il messaggio da inviare con la campagna:

   1. Fai clic sul pulsante **[!UICONTROL Edit content]** , quindi configura e progetta il contenuto del messaggio. [Ulteriori informazioni sui messaggi](../messages/get-started-content.md).

      Quando il contenuto è pronto, fai clic sulla freccia per tornare alla schermata di creazione della campagna.

      ![](assets/create-campaign-design.png)

   1. In **[!UICONTROL Actions tracking]** specifica se desideri tenere traccia della reazione dei destinatari alla consegna.

      I risultati del tracciamento saranno accessibili dal rapporto della campagna una volta che la campagna sarà stata eseguita. [Ulteriori informazioni sui report delle campagne](campaign-global-report.md)

1. Definisci il pubblico di cui eseguire il targeting. A questo scopo, fai clic sul pulsante **[!UICONTROL Select audience]** per visualizzare l’elenco dei segmenti Adobe Experience Platform disponibili. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

   >[!NOTE]
   >
   >Per le campagne con attivazione API, il pubblico deve essere impostato tramite chiamata API. [Ulteriori informazioni](api-triggered-campaigns.md)

   In **[!UICONTROL Identity namespace]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Gli individui appartenenti a un segmento che non hanno l’identità selezionata (spazio dei nomi) tra le loro diverse identità non verranno presi di mira dalla campagna.

1. Configura le date di inizio e di fine della campagna. Per impostazione predefinita, le campagne vengono configurate per avviarsi una volta attivate manualmente e per terminare non appena il messaggio è stato inviato una volta.

1. Inoltre, puoi specificare una frequenza per l’esecuzione dell’azione configurata nella campagna.

   >[!NOTE]
   >
   >Per le campagne attivate dall’API, la pianificazione a una data e a un’ora specifiche con ricorrenza non è disponibile in quanto l’azione viene attivata tramite API. Tuttavia, la data di inizio e la data di fine sono rilevanti per garantire che, se una chiamata API viene effettuata prima di dopo la finestra, queste vengano ignorate.

   ![](assets/create-campaign-schedule.png)

1. Se stai creando una campagna con attivazione API, la **[!UICONTROL cURL request]** consente di recuperare **[!UICONTROL Campaign ID]** da utilizzare nella chiamata API. [Ulteriori informazioni](api-triggered-campaigns.md)

Quando la campagna è pronta, puoi rivederla e pubblicarla (vedi [Rivedere e attivare una campagna](#review-activate)).

## Rivedere e attivare una campagna {#review-activate}

Una volta configurata la campagna, devi rivederne il parametro e il contenuto prima di attivarlo. Per farlo, esegui questi passaggi:

1. Nella schermata di configurazione della campagna, fai clic su **[!UICONTROL Review to activate]** per visualizzare un riepilogo della campagna.

   Il riepilogo consente di modificare la campagna se necessario e di verificare se è presente un parametro errato o mancante.

   >[!IMPORTANT]
   >
   >In caso di errori, non potrai attivare la campagna. Risolvi gli errori prima di procedere.

   ![](assets/create-campaign-alerts.png)

1. Verifica che la campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Activate]**.

   ![](assets/create-campaign-review.png)

1. La campagna è ora attivata e presenta la variabile **[!UICONTROL Live]** status (o **[!UICONTROL Scheduled]**  se è stata specificata una data di inizio). [Ulteriori informazioni sugli stati delle campagne](get-started-with-campaigns.md#statuses)

   Il messaggio configurato nella campagna viene eseguito immediatamente o alla data specificata.

   >[!NOTE]
   >
   >Una volta che una campagna è stata attivata, manterrà lo stato &quot;Live&quot; anche dopo l’esecuzione del messaggio. Per modificarne lo stato, è necessario interromperlo manualmente. [Scopri come interrompere una campagna](modify-stop-campaign.md)

1. Una volta che una campagna è stata attivata, puoi controllarne in qualsiasi momento le informazioni aprendole. Il riepilogo ti consente di ottenere statistiche sul numero di profili target e azioni consegnate e non riuscite.

   È inoltre possibile ottenere statistiche aggiuntive nei rapporti dedicati facendo clic sul pulsante **[!UICONTROL Reports]** pulsante . [Ulteriori informazioni](campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

## Risorse aggiuntive

* [Introduzione alle campagne](get-started-with-campaigns.md)
* [Creare campagne con attivazione API](api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](modify-stop-campaign.md)
* [Rapporto live della campagna](campaign-live-report.md)
* [Rapporto globale della campagna](campaign-global-report.md)
