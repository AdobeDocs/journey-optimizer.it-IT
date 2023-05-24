---
solution: Journey Optimizer
product: journey optimizer
title: Creare una campagna
description: Scopri come creare campagne in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: crea, ottimizzatore, campagna, superficie, messaggi
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 23%

---

# Creare una campagna {#create-campaign}

>[!NOTE]
>
>Prima di creare una nuova campagna, accertati di disporre di un canale di superficie (ossia un predefinito per messaggi) e di un segmento Adobe Experience Platform pronto per l’uso. Per ulteriori informazioni, consulta le sezioni seguenti:
>
>* [Creare superfici di canale](../configuration/channel-surfaces.md)
>* [Introduzione ai segmenti](../segment/about-segments.md)


Per creare una nuova campagna, accedi a **[!UICONTROL Campagne]** , quindi fai clic su **[!UICONTROL Crea campagna]**. Puoi anche duplicare una campagna live esistente per crearne una nuova. [Ulteriori informazioni](modify-stop-campaign.md#duplicate)

## Scegli il tipo di campagna e il canale {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo di campagna"
>abstract="Per un messaggio di marketing con data di invio specificata, il tipo **Pianificato** è il più appropriato. Tuttavia, se desideri inviare messaggi transazionali, relativi ad esempio alla reimpostazione della password o all’abbandono del carrello, il tipo di campagna **Attivata da API** è la scelta migliore."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Categoria della campagna"
>abstract="Il valore della categoria è direttamente associato al valore del tipo di campagna. Il tipo di campagna Pianificato per la categoria **Marketing** e il tipo Attivata da API per la categoria **Transazionale**."

1. In **[!UICONTROL Proprietà]** , specifica come eseguire la campagna. Sono disponibili due tipi di campagne:

   * **[!UICONTROL Pianificato]**: esegui la campagna immediatamente o in una data specificata. Le campagne pianificate hanno lo scopo di inviare **marketing** digita i messaggi.

   * **[!UICONTROL Attivato da API]**: esegui la campagna utilizzando una chiamata API. Le campagne attivate da API hanno lo scopo di inviare **transazionale** messaggi, ovvero messaggi inviati in seguito a un’azione eseguita da un individuo: reimpostazione della password, abbandono del carrello, ecc. [Scopri come attivare una campagna utilizzando le API](api-triggered-campaigns.md)

1. In **[!UICONTROL Azioni]** , scegli il canale e la superficie di canale da utilizzare per inviare il messaggio.

   Una “superficie” è una configurazione definita da un [amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni](../configuration/channel-surfaces.md).

   Nell’elenco a discesa sono elencate solo le superfici di canale compatibili con il tipo di campagna di marketing.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Se stai creando una campagna di notifica push, puoi abilitare **[!UICONTROL Modalità Consegna rapida]**, componente aggiuntivo di Journey Optimizer che consente l’invio molto rapido di messaggi push in volumi elevati. [Ulteriori informazioni](../push/create-push.md#rapid-delivery)

1. Clic **[!UICONTROL Crea]** per creare la campagna.

## Definire le proprietà della campagna {#create}

1. In **[!UICONTROL Proprietà]** , specifica un nome e una descrizione per la campagna.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Il **Tag** consente di assegnare alla campagna i tag unificati Adobe Experience Platform. Questo consente di classificarle facilmente e migliorare la ricerca dall’elenco delle campagne. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla campagna, fai clic sul pulsante **[!UICONTROL Gestisci accesso]** pulsante. [Ulteriori informazioni su OLE (Object Level Access Control)](../administration/object-based-access.md)

## Creare il messaggio e configurare il tracciamento {#content}

In **[!UICONTROL Azioni]** sezione, crea il messaggio da inviare con la campagna.

1. Fai clic su **[!UICONTROL Modifica contenuto]** , quindi crea e progetta il contenuto del messaggio.

   Scopri i passaggi dettagliati per creare il contenuto del messaggio nelle pagine seguenti:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Lead" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>Creare le e-mail</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Non frequente" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>Creare notifiche push</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="Convalida" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>Creare messaggi SMS</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. Una volta definito il contenuto, utilizza **[!UICONTROL Simula contenuto]** per visualizzare in anteprima e verificare il contenuto con i profili di test. [Maggiori informazioni](../email/preview.md).

1. Fai clic sulla freccia per tornare alla schermata di creazione della campagna.

   ![](assets/create-campaign-design.png)

1. In **[!UICONTROL Tracciamento delle azioni]** , specifica se desideri tenere traccia della reazione dei destinatari alla consegna: puoi tenere traccia dei clic e/o delle aperture.

   I risultati del tracciamento saranno accessibili dal rapporto della campagna una volta eseguita la campagna. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report.md)

## Definire il pubblico {#audience}

Fai clic su **[!UICONTROL Seleziona pubblico]** per visualizzare l’elenco dei segmenti di Adobe Experience Platform disponibili. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

>[!NOTE]
>
>Per le campagne attivate da API, il pubblico deve essere impostato tramite chiamata API. [Ulteriori informazioni](api-triggered-campaigns.md)

In **[!UICONTROL Spazio dei nomi dell’identità]** , scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti dal segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

    >[!NOTA]
    >
    >Gli utenti appartenenti a un segmento che non dispone dell’identità selezionata (spazio dei nomi) tra le loro diverse identità non verranno targetizzati dalla campagna.

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Pianificare la campagna {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Inizio della campagna"
>abstract="Specifica la data e l’ora in cui il messaggio deve essere inviato."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fine della campagna"
>abstract="Specifica quando interrompere l’esecuzione di una campagna ricorrente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Trigger delle azioni della campagna"
>abstract="Definisci la frequenza con cui deve essere inviato il messaggio della campagna."

Per impostazione predefinita, le campagne iniziano una volta attivate manualmente e terminano non appena il messaggio viene inviato.

Puoi definire una frequenza con cui inviare il messaggio della campagna. A tale scopo, utilizza **[!UICONTROL Trigger azione]** opzioni nella schermata di creazione della campagna per specificare se la campagna deve essere eseguita giornalmente, settimanalmente o mensilmente.

Se non desideri eseguire la campagna subito dopo la sua attivazione, puoi specificare la data e l’ora dell’invio del messaggio utilizzando **[!UICONTROL Inizio campagna]** opzione. Il **[!UICONTROL Fine campagna]** consente di specificare quando deve terminare l’esecuzione di una campagna ricorrente.

![](assets/create-campaign-schedule.png)

Una volta che la campagna è pronta, puoi rivederla e pubblicarla. [Ulteriori informazioni](review-activate-campaign.md)
