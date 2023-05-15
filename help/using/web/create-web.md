---
title: Creare esperienze web
description: Scopri come creare una pagina web e modificarne il contenuto in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 18%

---

# Creare esperienze web {#create-web}

[!DNL Journey Optimizer] ti consente di personalizzare l’esperienza web che distribuisci ai clienti tramite campagne web in entrata.

>[!CAUTION]
>
>Attualmente in [!DNL Journey Optimizer] puoi creare esperienze web solo utilizzando le **campagne**.

[Scopri come creare una campagna web in questo video](#video)

## Creare una campagna web {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definire una superficie web"
>abstract="Una superficie web può corrispondere all’URL di una sola pagina o più pagine, consentendoti di apportare modifiche al contenuto in una o più pagine web."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Creare una regola di corrispondenza delle pagine"
>abstract="Una regola di corrispondenza delle pagine consente di eseguire il targeting di più URL che corrispondono alla stessa regola. Può servire, ad esempio, per applicare a un intero sito web le modifiche apportate a un banner principale oppure per aggiungere un’immagine nella parte superiore da visualizzare su tutte le pagine dei prodotti di un sito web."

Per iniziare a creare l’esperienza web tramite una campagna, segui i passaggi riportati di seguito.

>[!NOTE]
>
>Se questa è la prima volta che crei un’esperienza web, assicurati di seguire i prerequisiti descritti in [questa sezione](web-prerequisites.md).

1. Creare una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Seleziona la **[!UICONTROL Web]** azione.

1. Definire una superficie web.

   >[!NOTE]
   >
   >Una superficie web è una proprietà web identificata da un URL in cui verrà distribuito il contenuto. Può corrispondere a uno o più URL di pagina, consentendoti di apportare modifiche in una o più pagine web.

   Puoi immettere un **[!UICONTROL URL della pagina]** per applicare le modifiche a una sola pagina.

   ![](assets/web-campaign-surface.png)

1. Oppure puoi creare un **[!UICONTROL Regola corrispondente alle pagine]** per eseguire il targeting di più URL che corrispondono alla stessa regola, ad esempio, se desideri applicare le modifiche a un banner eroe in un intero sito web o aggiungere un’immagine principale che viene visualizzata su tutte le pagine di prodotto di un sito web.

   A questo scopo, seleziona **[!UICONTROL Regola corrispondente alle pagine]** e fai clic su **[!UICONTROL Crea regola]**.

   ![](assets/web-campaign-matching-rule.png)

1. Definisci i criteri per la **[!UICONTROL Dominio]** e **[!UICONTROL Pagina]** campi.

   Ad esempio, se desideri modificare gli elementi che vengono visualizzati su tutte le pagine di prodotto donna del sito web Luma, seleziona **[!UICONTROL Dominio]** > **[!UICONTROL Inizia con]** > `luma` e **[!UICONTROL Pagina]** > **[!UICONTROL Contiene]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Salva le modifiche. La regola viene visualizzata nella **[!UICONTROL Creare una campagna]** schermo.

   ![](assets/web-pages-matching-rule-example.png)

1. Una volta definita la superficie web, seleziona **[!UICONTROL Crea]**.

1. Completa i passaggi per creare una campagna web, ad esempio le proprietà della campagna, [pubblico](../segment/about-segments.md)e [pianificazione](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

## Attivare la campagna web {#activate-web-campaign}

Una volta definiti i [impostazioni campagna web](#configure-web-campaign) e il contenuto viene modificato come desiderato utilizzando la [web designer](author-web.md), puoi rivedere e attivare la tua campagna web. Effettua le seguenti operazioni.

>[!NOTE]
>
>Puoi anche visualizzare in anteprima il contenuto della campagna web prima di attivarlo. [Ulteriori informazioni](author-web.md#test-web-campaign)

1. Dalla campagna web, seleziona **[!UICONTROL Rivedi per attivare]**.

1. Se necessario, seleziona e modifica il contenuto, le proprietà, la superficie, il pubblico e la pianificazione.

1. Seleziona **[!UICONTROL Attiva]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Dopo aver fatto clic su **[!UICONTROL Attiva]**, potrebbero essere necessari fino a 15 minuti perché le modifiche alle campagne web siano disponibili in diretta sul sito web.

La tua campagna web prende il **[!UICONTROL Live]** ed è ora visibile al pubblico selezionato. Ogni destinatario della campagna può vedere le modifiche aggiunte al sito web utilizzando [!DNL Journey Optimizer] web designer.

>[!NOTE]
>
>Se hai definito una pianificazione per la campagna web, la **[!UICONTROL Pianificato]** fino al raggiungimento della data e dell&#39;ora di inizio.
>
>Se attivate una campagna web che interessa le stesse pagine di un’altra campagna già attiva, tutte le modifiche verranno applicate alle pagine web.

Ulteriori informazioni sull’attivazione delle campagne in [questa sezione](../campaigns/review-activate-campaign.md).

## Interrompere una campagna web {#stop-web-campaign}

Quando una campagna web è attiva, puoi interromperla per impedire al pubblico di visualizzare le modifiche. Effettua le seguenti operazioni.

1. Seleziona una campagna live dall’elenco.

1. Dal menu principale, seleziona **[!UICONTROL Interrompi campagna]**.

   ![](assets/web-campaign-stop.png)

1. Le modifiche aggiunte non saranno più visibili al pubblico definito.

>[!NOTE]
>
>Una volta interrotta una campagna web, non puoi modificarla o attivarla nuovamente. Puoi duplicarla e attivare la campagna duplicata.

## Video introduttivo{#video}

Il video seguente mostra come creare una campagna web, configurarne le proprietà, rivederla e pubblicarla.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)