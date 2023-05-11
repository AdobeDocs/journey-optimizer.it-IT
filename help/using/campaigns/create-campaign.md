---
solution: Journey Optimizer
product: journey optimizer
title: Creare una campagna
description: Scopri come creare campagne in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: creare, ottimizzatore, campagna, superficie, messaggi
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 21%

---

# Creare una campagna {#create-campaign}

>[!NOTE]
>
>Prima di creare una nuova campagna, assicurati di disporre di un canale di superficie (ad es. un messaggio preimpostato) e di un segmento Adobe Experience Platform pronto per l’uso. Ulteriori informazioni in queste sezioni:
>
>* [Creare superfici di canale](../configuration/channel-surfaces.md)
>* [Introduzione ai segmenti](../segment/about-segments.md)


Per creare una nuova campagna, accedi al **[!UICONTROL Campagne]** menu, quindi fai clic su **[!UICONTROL Creare una campagna]**. Puoi anche duplicare una campagna live esistente per crearne una nuova. [Ulteriori informazioni](modify-stop-campaign.md#duplicate)

## Scegli il tipo di campagna e il canale {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo di campagna"
>abstract="Per un messaggio di marketing con data di invio specificata, il tipo **Pianificato** è il più appropriato. Tuttavia, se desideri inviare messaggi transazionali, relativi ad esempio alla reimpostazione della password o all’abbandono del carrello, il tipo di campagna **Attivata da API** è la scelta migliore."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Categoria della campagna"
>abstract="Il valore della categoria è direttamente associato al valore del tipo di campagna. Il tipo di campagna Pianificato per la categoria **Marketing** e il tipo Attivata da API per la categoria **Transazionale**."

1. In **[!UICONTROL Proprietà]** Specifica come eseguire la campagna. Sono disponibili due tipi di campagne:

   * **[!UICONTROL Pianificato]**: esegue la campagna immediatamente o in una data specificata. Le campagne pianificate sono finalizzate all’invio di **marketing** digitare messaggi.

   * **[!UICONTROL Attivazione dall’API]**: esegui la campagna utilizzando una chiamata API. Le campagne con attivazione API sono mirate all’invio di **transazionale** messaggi, ovvero messaggi inviati in seguito a un’azione eseguita da un singolo utente: reimpostazione della password, abbandono del carrello, ecc. [Scopri come attivare una campagna utilizzando le API](api-triggered-campaigns.md)

1. In **[!UICONTROL Azioni]** scegli il canale e la superficie del canale da utilizzare per inviare il messaggio.

   Una “superficie” è una configurazione definita da un [amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni](../configuration/channel-surfaces.md).

   Nell’elenco a discesa sono elencate solo le superfici del canale compatibili con il tipo di campagna di marketing.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Se stai creando una campagna di notifica push, puoi abilitare il **[!UICONTROL Modalità di consegna rapida]**, componente aggiuntivo di Journey Optimizer che consente l’invio rapido di messaggi push in grandi volumi. [Ulteriori informazioni](../push/create-push.md#rapid-delivery)

1. Fai clic su **[!UICONTROL Crea]** per creare la campagna.

## Definire le proprietà della campagna {#create}

1. In **[!UICONTROL Proprietà]** Specifica un nome e una descrizione per la campagna.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. La **Tag** consente di assegnare tag unificati Adobe Experience Platform alla campagna. Questo consente di classificarli facilmente e migliorare la ricerca dall’elenco delle campagne. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags)

1. Per assegnare etichette di utilizzo dati personalizzate o di base alla campagna, fai clic sul pulsante **[!UICONTROL Gestisci accesso]** pulsante . [Ulteriori informazioni sul controllo dell&#39;accesso a livello di oggetto (OLA)](../administration/object-based-access.md)

## Creare il messaggio e configurare il tracciamento {#content}

In **[!UICONTROL Azioni]** crea il messaggio da inviare con la campagna.

1. Fai clic sul pulsante **[!UICONTROL Modifica contenuto]** , quindi crea e progetta il contenuto del messaggio.

   Scopri i passaggi dettagliati per la creazione del contenuto del messaggio nelle pagine seguenti:

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

1. Una volta definito il contenuto, utilizza il **[!UICONTROL Simulazione del contenuto]** per visualizzare in anteprima e testare il contenuto con i profili di test. [Maggiori informazioni](../email/preview.md).

1. Fai clic sulla freccia per tornare alla schermata di creazione della campagna.

   ![](assets/create-campaign-design.png)

1. In **[!UICONTROL Tracciamento delle azioni]** specifica se desideri tenere traccia delle reazioni dei destinatari alla consegna: puoi tenere traccia dei clic e/o delle aperture.

   I risultati del tracciamento saranno accessibili dal rapporto della campagna una volta che la campagna sarà stata eseguita. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report.md)

## Definire il pubblico {#audience}

Fai clic sul pulsante **[!UICONTROL Selezionare il pubblico]** per visualizzare l’elenco dei segmenti Adobe Experience Platform disponibili. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

>[!NOTE]
>
>Per le campagne con attivazione API, il pubblico deve essere impostato tramite chiamata API. [Ulteriori informazioni](api-triggered-campaigns.md)

In **[!UICONTROL Spazio dei nomi identità]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

    >[!NOTE]
    >
    >Gli utenti appartenenti a un segmento che non hanno l’identità selezionata (namespace) tra le diverse identità non verranno interessati dalla campagna.

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

Per impostazione predefinita, le campagne iniziano una volta attivate manualmente e terminano non appena il messaggio è stato inviato una volta.

Puoi definire la frequenza con cui deve essere inviato il messaggio della campagna. Per eseguire questa operazione, utilizza la variabile **[!UICONTROL Trigger delle azioni]** nella schermata di creazione della campagna per specificare se la campagna deve essere eseguita ogni giorno, settimanalmente o mensilmente.

Se non desideri eseguire la campagna subito dopo l’attivazione, puoi specificare una data e un’ora in cui inviare il messaggio utilizzando **[!UICONTROL Inizio campagna]** opzione . La **[!UICONTROL Fine campagna]** consente di specificare quando interrompere l’esecuzione di una campagna ricorrente.

![](assets/create-campaign-schedule.png)

Quando la campagna è pronta, puoi rivederla e pubblicarla. [Ulteriori informazioni](review-activate-campaign.md)
