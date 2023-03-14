---
title: Creare esperienze web
description: Scopri come creare una pagina web e modificarne il contenuto in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 8%

---

# Creare esperienze web {#create-web}

>[!BEGINSHADEBOX]

Informazioni disponibili in questa documentazione:

* [Introduzione al canale Web](get-started-web.md)
* **[Creare esperienze web](create-web.md)**
* [Creare pagine web](author-web.md)
* [Estensione Helper per editing video](visual-editing-helper.md)
* [Generazione rapporti Web](web-report.md)

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] consente di personalizzare l’esperienza web fornita ai clienti tramite campagne web in entrata.

>[!CAUTION]
>
>Attualmente in [!DNL Journey Optimizer] puoi creare esperienze web solo utilizzando **campagne**.

## Prerequisiti {#prerequesites}

Per poter accedere e creare pagine web in [!DNL Journey Optimizer] nell&#39;interfaccia utente, seguire i prerequisiti seguenti:

* Per aggiungere modifiche al sito web, devi implementare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} sul tuo sito web.

* Per accedere al [!DNL Journey Optimizer] web designer, è necessario scaricare [Helper per editing video Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} estensione del browser su Chrome. [Ulteriori informazioni](visual-editing-helper.md)

>[!CAUTION]
>
>Google Chrome è attualmente l’unico browser che supporta l’authoring di pagine web in [!DNL Journey Optimizer].

Affinché l’esperienza web possa essere consegnata correttamente, è necessario definire le seguenti impostazioni:

* In [Raccolta dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}, assicurati di avere un flusso di dati definito, ad esempio sotto **[!UICONTROL Adobe Experience Platform]** servizio che hai sia **[!UICONTROL Segmentazione Edge]** e **[!UICONTROL Adobe Journey Optimizer]** opzioni abilitate.

   In questo modo gli eventi in entrata Journey Optimizer vengono gestiti correttamente da Adobe Experience Platform Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >Il **[!UICONTROL Adobe Journey Optimizer]** può essere attivata solo quando **[!UICONTROL Segmentazione Edge]** l&#39;opzione è già abilitata.

* In entrata [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   Questo criterio di unione è utilizzato da [!DNL Journey Optimizer] canali in entrata per attivare e pubblicare correttamente le campagne in entrata sul server Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

## Creare una campagna web {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definire una superficie web"
>abstract="Una superficie web può corrispondere a un singolo URL di pagina o a più pagine, consentendoti di apportare modifiche al contenuto in una o più pagine web."

Per iniziare a creare la tua esperienza web attraverso una campagna, segui i passaggi indicati di seguito.

1. Creare una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Seleziona la **[!UICONTROL Web]** azione.

   ![](assets/web-create-campaign.png)

1. Definite una superficie web.

   >[!NOTE]
   >
   >Una superficie web è una proprietà web identificata da un URL in cui verrà distribuito il contenuto. Può corrispondere a un singolo URL di pagina o a più pagine, consentendoti di apportare modifiche in una o più pagine web.

   È possibile immettere un valore **[!UICONTROL URL della pagina]** se desideri applicare le modifiche a una sola pagina.

   ![](assets/web-campaign-surface.png)

1. Oppure puoi creare una **[!UICONTROL Regola di corrispondenza pagine]** per eseguire il targeting di più URL che corrispondono alla stessa regola: ad esempio, se desideri applicare le modifiche a un banner hero in un intero sito web o aggiungere un’immagine superiore che venga visualizzata in tutte le pagine di prodotto di un sito web.

   A tale scopo, seleziona **[!UICONTROL Regola di corrispondenza pagine]** e fai clic su **[!UICONTROL Crea regola]**.

   ![](assets/web-campaign-matching-rule.png)

1. Definisci i criteri per il **[!UICONTROL Dominio]** e **[!UICONTROL Pagina]** campi.

   Ad esempio, se desideri modificare gli elementi visualizzati su tutte le pagine di prodotti donna del tuo sito web Luma, seleziona **[!UICONTROL Dominio]** > **[!UICONTROL Inizia con]** > `luma` e **[!UICONTROL Pagina]** > **[!UICONTROL Contiene]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Salva le modifiche. La regola viene visualizzata in **[!UICONTROL Crea campagna]** schermo.

   ![](assets/web-pages-matching-rule-example.png)

1. Una volta definita la superficie web, seleziona **[!UICONTROL Crea]**. Ora puoi configurare le proprietà e le impostazioni della campagna.

## Configurare la campagna web {#configure-web-campaign}

1. In **[!UICONTROL Proprietà]** , puoi modificare il nome della campagna e aggiungere una descrizione, se necessario.

   ![](assets/web-campaign-properties.png)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla campagna web, seleziona la **[!UICONTROL Gestisci accesso]** nella parte superiore dello schermo. [Ulteriori informazioni su OLAC (Object Level Access Control)](../administration/object-based-access.md)

1. Puoi selezionare **[!UICONTROL Esperimento sui contenuti]** per testare i trattamenti per contenuti con parti del pubblico, al fine di determinare quale trattamento funziona meglio rispetto a una metrica specifica. [Ulteriori informazioni](../campaigns/content-experiment.md)

   >[!AVAILABILITY]
   >
   >Il **Esperimento contenuti** Questa funzione è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

1. Dalla sezione **[!UICONTROL Azione]** scheda della campagna, seleziona **[!UICONTROL Modifica contenuto]** per iniziare a creare la tua campagna web. [Ulteriori informazioni](author-web.md)

   ![](assets/web-edit-content.png)

1. Dalla sezione **[!UICONTROL Pubblico]** , definisci chi potrà visualizzare la tua campagna web. Per impostazione predefinita, la campagna web sarà visibile a tutti i visitatori.

   ![](assets/web-campaign-audience.png)

   Puoi anche selezionare un pubblico specifico. Utilizza il **[!UICONTROL Seleziona pubblico]** per visualizzare l’elenco dei segmenti di Adobe Experience Platform disponibili. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

   >[!NOTE]
   >
   >Per le campagne attivate da API, il pubblico deve essere impostato tramite chiamata API. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md)

   ![](assets/web-campaign-select-audience.png)

1. In **[!UICONTROL Spazio dei nomi dell’identità]** , scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti dal segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

1. Definisci un **[!UICONTROL Pianificazione]** per la tua campagna web. [Ulteriori informazioni](../campaigns/create-campaign.md#schedule)

   ![](assets/web-campaign-schedule.png)

   Per impostazione predefinita, inizia quando viene attivata manualmente e termina quando viene interrotta manualmente, ma puoi anche definire date e ore specifiche per rendere visibili le modifiche.

   ![](assets/web-campaign-schedule-start.png)

## Attivare la campagna web {#activate-web-campaign}

Una volta definiti i [impostazioni della campagna web](#configure-web-campaign) e hai modificato il contenuto come desiderato utilizzando [web designer](author-web.md), puoi rivedere e attivare la tua campagna web. Effettua le seguenti operazioni.

>[!NOTE]
>
>Puoi anche visualizzare in anteprima il contenuto della campagna web prima di attivarlo. [Ulteriori informazioni](author-web.md#test-web-campaign)

1. Dalla campagna web, seleziona **[!UICONTROL Controlla per attivare]**.

   ![](assets/web-campaign-review.png)

1. Se necessario, rivedi e modifica il contenuto, le proprietà, la superficie, il pubblico e la pianificazione.

1. Seleziona **[!UICONTROL Attiva]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Dopo aver fatto clic su **[!UICONTROL Attiva]**, possono essere necessari fino a 15 minuti affinché le modifiche alle campagne web siano disponibili in diretta sul sito web.

La tua campagna web accetta **[!UICONTROL Live]** ed è ora visibile al pubblico selezionato. Ogni destinatario della campagna può visualizzare le modifiche aggiunte al sito web utilizzando [!DNL Journey Optimizer] web designer.

>[!NOTE]
>
>Se hai definito una pianificazione per la campagna web, questa presenta **[!UICONTROL Pianificato]** fino al raggiungimento della data e dell’ora di inizio.
>
>Se attivi una campagna web che influisce sulle stesse pagine di un’altra campagna già live, tutte le modifiche verranno applicate alle pagine web.

Ulteriori informazioni sull’attivazione delle campagne in [questa sezione](../campaigns/review-activate-campaign.md).

## Interrompere una campagna web {#stop-web-campaign}

Quando una campagna web è in diretta, puoi interromperla per impedire al pubblico di visualizzare le modifiche. Effettua le seguenti operazioni.

1. Seleziona una campagna live dall’elenco.

1. Dal menu principale, seleziona **[!UICONTROL Interrompi campagna]**.

   ![](assets/web-campaign-stop.png)

1. Le modifiche aggiunte non saranno più visibili al pubblico definito.

>[!NOTE]
>
>Una volta interrotta una campagna web, non puoi più modificarla o attivarla. Puoi solo duplicarlo e attivare la campagna duplicata.
