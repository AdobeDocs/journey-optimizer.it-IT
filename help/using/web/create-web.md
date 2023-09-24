---
title: Creare esperienze web
description: Scopri come creare una pagina web e modificarne il contenuto in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: ec071392cec9933bb73ae9ab20618292b6089061
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 19%

---

# Creare esperienze web {#create-web}

[!DNL Journey Optimizer] consente di personalizzare l’esperienza web fornita ai clienti tramite campagne web in entrata.

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

Per iniziare a creare la tua esperienza web attraverso una campagna, segui i passaggi indicati di seguito.

>[!NOTE]
>
>Se questa è la prima volta che crei un’esperienza web, assicurati di seguire i prerequisiti descritti in [questa sezione](web-prerequisites.md).

1. Creare una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Seleziona la **[!UICONTROL Web]** azione.

1. Definire una superficie web.

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

1. Una volta definita la superficie web, seleziona **[!UICONTROL Crea]**.

1. Completa i passaggi per creare una campagna web, ad esempio le proprietà della campagna, [pubblico](../audience/about-audiences.md), e [pianificazione](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

## Testare la campagna web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Visualizzare l’esperienza web in anteprima"
>abstract="Ottieni una simulazione dell’aspetto che avrà l’esperienza web."

Una volta [ha creato la tua esperienza web](edit-web-content.md) tramite web designer, puoi visualizzare un’anteprima delle pagine web modificate prima di attivare la campagna. A questo scopo, segui i passaggi riportati qui sotto.

>[!CAUTION]
>
>Devi disporre di profili di test per simulare quali offerte verranno consegnate. Scopri come [creare profili di test](../audience/creating-test-profiles.md).

1. Dalla schermata di modifica del contenuto della campagna web o dal web designer, seleziona **[!UICONTROL Simula contenuto]**.

   <!--![](assets/web-designer-simulate.png)-->

   ![](assets/web-campaign-simulate.png)

1. Clic **[!UICONTROL Gestire i profili di test]** per selezionare uno o più profili di test.
1. Viene visualizzata un’anteprima della pagina web modificata.

   ![](assets/web-designer-preview.png)

1. Puoi anche aprirlo nel browser predefinito, oppure copiare l’URL di prova per incollarlo in qualsiasi browser. Questo ti consente di condividere il collegamento con il team e le parti interessate, che potranno visualizzare in anteprima la nuova esperienza web in qualsiasi browser prima che la campagna venga pubblicata.

   >[!NOTE]
   >
   >Durante la copia dell’URL di test, il contenuto visualizzato è quello personalizzato per il profilo di test utilizzato quando la simulazione del contenuto è stata generata in [!DNL Journey Optimizer].

## Attivare la campagna web {#activate-web-campaign}

Una volta definiti i [impostazioni della campagna web](#configure-web-campaign) e hai modificato il contenuto come desiderato utilizzando [web designer](edit-web-content.md#work-with-web-designer), puoi rivedere e attivare la tua campagna web. Effettua le seguenti operazioni.

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. Dalla campagna web, seleziona **[!UICONTROL Controlla per attivare]**.

1. Se necessario, seleziona e modifica il contenuto, le proprietà, la superficie, il pubblico e la pianificazione.

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

## Video introduttivo{#video}

Il video seguente mostra come creare una campagna web, configurarne le proprietà, rivederla e pubblicarla.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)