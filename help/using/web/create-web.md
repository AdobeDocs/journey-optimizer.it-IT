---
title: Creare esperienze web
description: Scopri come creare una pagina web e modificarne il contenuto in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 0f69a47dccad20f3e978613b349a29f9daab94bd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Creare esperienze web {#create-web}

>[!AVAILABILITY]
>
>La funzione canale web è attualmente disponibile come versione beta solo per gli utenti selezionati.

[!DNL Journey Optimizer] ti consente di personalizzare l’esperienza web che distribuisci ai clienti tramite campagne web in entrata.

>[!CAUTION]
>
>Attualmente in [!DNL Journey Optimizer] puoi creare esperienze web solo utilizzando **campagne**.

## Prerequisiti {#prerequesites}

Per accedere e creare pagine web nel [!DNL Journey Optimizer] interfaccia utente, segui i prerequisiti seguenti:

* Per aggiungere modifiche al sito web, devi implementare la funzione [SDK per web di Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;} sul sito web.

* Per accedere al [!DNL Journey Optimizer] web designer, è necessario scaricare [Helper per l’editing visivo di Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca)Estensione del browser {target=&quot;_blank&quot;} su Chrome. [Ulteriori informazioni](visual-editing-helper.md)

>[!CAUTION]
>
>Google Chrome è attualmente l’unico browser che supporta l’authoring di pagine web in [!DNL Journey Optimizer].

Affinché l&#39;esperienza web possa essere consegnata correttamente, è necessario definire le seguenti impostazioni:

* In [Raccolta dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target=&quot;_blank&quot;}, assicurati che sia definito un datastream come sotto **[!UICONTROL Adobe Experience Platform]** il servizio **[!UICONTROL Edge Segmentation]** e **[!UICONTROL Adobe Journey Optimizer]** opzioni abilitate.

   In questo modo gli eventi in entrata di Journey Optimizer vengono gestiti correttamente da Adobe Experience Platform Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target=&quot;_blank&quot;}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >La **[!UICONTROL Adobe Journey Optimizer]** può essere attivata solo quando **[!UICONTROL Edge Segmentation]** opzione già abilitata.

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}, assicurati di disporre di un criterio di unione con **[!UICONTROL Active-On-Edge Merge Policy]** opzione abilitata. A questo scopo, seleziona un criterio nella sezione **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Menu Experience Platform. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target=&quot;_blank&quot;}

   Questo criterio di unione è utilizzato da [!DNL Journey Optimizer] canali in entrata per attivare e pubblicare correttamente le campagne in entrata sul bordo. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target=&quot;_blank&quot;}

   ![](assets/web-aep-merge-policy.png)

## Creare una campagna web {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definire una superficie web"
>abstract="Una superficie web può corrispondere a uno o più URL di pagina, consentendoti di apportare modifiche al contenuto in una o più pagine web."

Per iniziare a creare l’esperienza web tramite una campagna, segui i passaggi riportati di seguito.

1. Crea una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Seleziona la **[!UICONTROL Web]** azione.

   ![](assets/web-create-campaign.png)

1. Definire una superficie web.

   >[!NOTE]
   >
   >Una superficie web è una proprietà web identificata da un URL in cui verrà distribuito il contenuto. Può corrispondere a uno o più URL di pagina, consentendoti di apportare modifiche in una o più pagine web.

   Puoi immettere un **[!UICONTROL Page URL]** per applicare le modifiche a una sola pagina.

   ![](assets/web-campaign-surface.png)

1. Oppure puoi creare un **[!UICONTROL Pages matching rule]** per eseguire il targeting di più URL che corrispondono alla stessa regola, ad esempio, se desideri applicare le modifiche a un banner eroe in un intero sito web o aggiungere un’immagine principale che viene visualizzata su tutte le pagine di prodotto di un sito web.

   A questo scopo, seleziona **[!UICONTROL Pages matching rule]** e fai clic su **[!UICONTROL Create rule]**.

   ![](assets/web-campaign-matching-rule.png)

1. Definisci i criteri per la **[!UICONTROL Domain]** e **[!UICONTROL Page]** campi.

   Ad esempio, se desideri modificare gli elementi che vengono visualizzati su tutte le pagine di prodotto donna del sito web Luma, seleziona **[!UICONTROL Domain]** > **[!UICONTROL Starts with]** > `luma` e **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Salva le modifiche. La regola viene visualizzata nella **[!UICONTROL Create campaign]** schermo.

   ![](assets/web-pages-matching-rule-example.png)

1. Una volta definita la superficie web, seleziona **[!UICONTROL Create]**. Ora puoi configurare le proprietà e le impostazioni della campagna.

## Configurare la campagna web {#configure-web-campaign}

1. In **[!UICONTROL Properties]** È possibile modificare il nome della campagna e aggiungere una descrizione, se necessario.

   ![](assets/web-campaign-properties.png)

1. Per assegnare etichette di utilizzo dati personalizzate o di base alla campagna web, seleziona la **[!UICONTROL Manage access]** nella parte superiore dello schermo. [Ulteriori informazioni su Object Level Access Control (OLAC)](../administration/object-based-access.md)

1. È possibile selezionare **[!UICONTROL Content experiment]** per testare i trattamenti dei contenuti con parti del pubblico, al fine di determinare quale trattamento funziona meglio rispetto a una metrica specifica. [Ulteriori informazioni](../campaigns/content-experiment.md)

   >[!AVAILABILITY]
   >
   >La **Esperimento dei contenuti** al momento è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

1. Da **[!UICONTROL Action]** scheda della campagna, seleziona **[!UICONTROL Edit content]** per iniziare a creare la campagna web. [Ulteriori informazioni](author-web.md)

   ![](assets/web-edit-content.png)

1. Da **[!UICONTROL Audience]** definisci chi potrà visualizzare la tua campagna web. Per impostazione predefinita, la campagna web sarà visibile a tutti i visitatori.

   ![](assets/web-campaign-audience.png)

   Puoi anche selezionare un pubblico specifico. Utilizza la **[!UICONTROL Select audience]** per visualizzare l’elenco dei segmenti disponibili di Adobe Experience Platform. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

   >[!NOTE]
   >
   >Per le campagne con attivazione API, il pubblico deve essere impostato tramite chiamata API. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md)

   ![](assets/web-campaign-select-audience.png)

1. In **[!UICONTROL Identity namespace]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace)

1. Definire un **[!UICONTROL Schedule]** per la campagna web. [Ulteriori informazioni](../campaigns/create-campaign.md#schedule)

   ![](assets/web-campaign-schedule.png)

   Per impostazione predefinita viene avviato quando viene attivato manualmente e termina quando viene interrotto manualmente, ma puoi anche definire date e ore specifiche per rendere visibili le modifiche.

   ![](assets/web-campaign-schedule-start.png)

## Attivare la campagna web {#activate-web-campaign}

Una volta definiti i [impostazioni campagna web](#configure-web-campaign) e il contenuto viene modificato come desiderato utilizzando la [web designer](author-web.md), puoi rivedere e attivare la tua campagna web. Segui i passaggi riportati di seguito.

>[!NOTE]
>
>Puoi anche visualizzare in anteprima il contenuto della campagna web prima di attivarlo. [Ulteriori informazioni](author-web.md#test-web-campaign)

1. Dalla campagna web, seleziona **[!UICONTROL Review to activate]**.

   ![](assets/web-campaign-review.png)

1. Rivedi e modifica se necessario i contenuti, le proprietà, la superficie, il pubblico e la pianificazione.

1. Seleziona **[!UICONTROL Activate]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Dopo aver fatto clic su **[!UICONTROL Activate]**, potrebbero essere necessari fino a 15 minuti perché le modifiche alle campagne web siano disponibili in diretta sul sito web.

La tua campagna web prende il **[!UICONTROL Live]** ed è ora visibile al pubblico selezionato. Ogni destinatario della campagna può vedere le modifiche aggiunte al sito web utilizzando [!DNL Journey Optimizer] web designer.

>[!NOTE]
>
>Se hai definito una pianificazione per la campagna web, la **[!UICONTROL Scheduled]** fino al raggiungimento della data e dell&#39;ora di inizio.
>
>Se attivate una campagna web che interessa le stesse pagine di un’altra campagna già attiva, tutte le modifiche verranno applicate alle pagine web.

Ulteriori informazioni sull’attivazione delle campagne in [questa sezione](../campaigns/review-activate-campaign.md).

## Interrompere una campagna web {#stop-web-campaign}

Quando una campagna web è attiva, puoi interromperla per impedire al pubblico di visualizzare le modifiche. Segui i passaggi riportati di seguito.

1. Seleziona una campagna live dall’elenco.

1. Dal menu principale, seleziona **[!UICONTROL Stop campaign]**.

   ![](assets/web-campaign-stop.png)

1. Le modifiche aggiunte non saranno più visibili al pubblico definito.

>[!NOTE]
>
>Una volta interrotta una campagna web, non puoi modificarla o attivarla nuovamente. Puoi duplicarla e attivare la campagna duplicata.
