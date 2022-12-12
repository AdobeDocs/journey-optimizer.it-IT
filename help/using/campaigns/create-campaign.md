---
solution: Journey Optimizer
product: journey optimizer
title: Creare una campagna
description: Scopri come creare campagne in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: ef838945e0c3595de8ad920203b278bb51671d16
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 0%

---

# Creare una campagna {#create-campaign}

>[!NOTE]
>
>Prima di creare una nuova campagna, assicurati di disporre di un canale di superficie (ad es. un messaggio preimpostato) e di un segmento Adobe Experience Platform pronto per l’uso. Ulteriori informazioni in queste sezioni:
>
>* [Creare superfici di canale](../configuration/channel-surfaces.md)
>* [Introduzione ai segmenti](../segment/about-segments.md)


## Creare la prima campagna {#create}

1. Accedere al **[!UICONTROL Campaigns]** menu, quindi fai clic su **[!UICONTROL Create campaign]**.

   >[!NOTE]
   >
   >Puoi anche duplicare una campagna live esistente per crearne una nuova. [Ulteriori informazioni](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

1. In **[!UICONTROL Properties]** Specifica come eseguire la campagna:

   * **[!UICONTROL Scheduled]**
   * **[!UICONTROL API-triggered]**

   Per ulteriori informazioni sul tipo di campagna e i relativi coinvolgimenti, consulta [sezione](#campaigntype).

1. In **[!UICONTROL Actions]** sezione , scegli il canale e la superficie del canale da utilizzare per inviare il messaggio, quindi fai clic su **[!UICONTROL Create]**.

   Una superficie è una configurazione definita da un [Amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Nell’elenco a discesa sono elencate solo le superfici del canale compatibili con il tipo di campagna di marketing.

1. Specifica un titolo e una descrizione per la campagna.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Per assegnare etichette di utilizzo dati personalizzate o di base alla campagna, fai clic sul pulsante **[!UICONTROL Manage access]** pulsante . [Ulteriori informazioni sul controllo dell&#39;accesso a livello di oggetto (OLA)](../administration/object-based-access.md)

## Creare il messaggio {#content}

In **[!UICONTROL Actions]** crea il messaggio da inviare con la campagna.

1. Fai clic sul pulsante **[!UICONTROL Edit content]** , quindi crea e progetta il contenuto del messaggio.

   Scopri i passaggi dettagliati per la creazione del contenuto del messaggio nelle pagine seguenti:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Lead" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>Creare e-mail</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Infrequente" src="../assets/do-not-localize/push.jpg">
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

1. Una volta definito il contenuto, utilizza il **[!UICONTROL Simulate content]** per visualizzare in anteprima e testare il contenuto con i profili di test. [Ulteriori informazioni](../email/preview.md).

1. Fai clic sulla freccia per tornare alla schermata di creazione della campagna.

   ![](assets/create-campaign-design.png)

1. In **[!UICONTROL Actions tracking]** specifica se desideri tenere traccia delle reazioni dei destinatari alla consegna: puoi tenere traccia dei clic e/o delle aperture.

   I risultati del tracciamento saranno accessibili dal rapporto della campagna una volta che la campagna sarà stata eseguita. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report.md)

## Definire il pubblico {#audience}

1. Definisci il pubblico di cui eseguire il targeting. A questo scopo, fai clic sul pulsante **[!UICONTROL Select audience]** per visualizzare l’elenco dei segmenti disponibili di Adobe Experience Platform. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

   >[!NOTE]
   >
   >Per le campagne con attivazione API, il pubblico deve essere impostato tramite chiamata API. [Ulteriori informazioni](api-triggered-campaigns.md)

   In **[!UICONTROL Identity namespace]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Gli individui appartenenti a un segmento che non hanno l’identità selezionata (spazio dei nomi) tra le loro diverse identità non verranno presi di mira dalla campagna.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Pianificare la campagna {#schedule}

1. Per eseguire la campagna in una data specifica o con una frequenza ricorrente, configura la **[!UICONTROL Schedule]** sezione . [Scopri come pianificare le campagne](#schedule)

1. Per assegnare etichette di utilizzo dati personalizzate o di base alla campagna, fai clic sul pulsante **[!UICONTROL Manage access]** pulsante . [Ulteriori informazioni sul controllo dell&#39;accesso a livello di oggetto (OLA)](../administration/object-based-access.md)

Quando la campagna è pronta, puoi rivederla e pubblicarla. [Ulteriori informazioni](#review-activate)

## Tipo di campagna {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo di campagna"
>abstract="Per un messaggio di marketing specificando una data di invio, l’ **Pianificato** Il tipo è il più appropriato. Tuttavia, se desideri inviare messaggi transazionali come reimpostazione della password o abbandono della scheda, l’ **Attivazione dall’API** Il tipo è la scelta migliore."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Categoria campagna"
>abstract="Il valore della categoria è direttamente collegato al valore del tipo di campagna. Pianifica tipo di campagna per **Marketing** categoria e tipo attivato dall’API per la categoria **Transazionale**"

Sono disponibili due tipi di campagne:

* **[!UICONTROL Scheduled]**: esegue la campagna immediatamente o in una data specificata. Le campagne pianificate sono finalizzate all’invio di **marketing** digitare messaggi.

* **[!UICONTROL API-triggered]**: esegui la campagna utilizzando una chiamata API. Le campagne con attivazione API sono mirate all’invio di **transazionale** messaggi, ovvero messaggi inviati in seguito a un’azione eseguita da un singolo utente: reimpostazione della password, abbandono della scheda, ecc. [Scopri come attivare una campagna utilizzando le API](api-triggered-campaigns.md)
