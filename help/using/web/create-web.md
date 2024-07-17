---
title: Creare esperienze web
description: Scopri come creare una pagina web e modificarne il contenuto in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 18%

---

# Creare esperienze web {#create-web}

[!DNL Journey Optimizer] ti consente di personalizzare l&#39;esperienza web che fornisci ai tuoi clienti tramite campagne web in entrata.

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
>Se è la prima volta che crei un’esperienza web, assicurati di seguire i prerequisiti descritti in [questa sezione](web-prerequisites.md).

1. Creare una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Selezionare l&#39;azione **[!UICONTROL Web]**.

1. Definite una superficie web.

   >[!NOTE]
   >
   >Una superficie web è una proprietà web identificata da un URL in cui verrà distribuito il contenuto. Può corrispondere a un singolo URL di pagina o a più pagine, consentendoti di apportare modifiche in una o più pagine web.

   È possibile immettere un **[!UICONTROL URL pagina]** se si desidera applicare le modifiche solo a una singola pagina.

   ![](assets/web-campaign-surface.png)

1. Oppure puoi creare una **[!UICONTROL regola di corrispondenza pagine]** per eseguire il targeting di più URL che corrispondono alla stessa regola, ad esempio, se desideri applicare le modifiche a un banner principale in un intero sito Web o aggiungere un&#39;immagine superiore che viene visualizzata in tutte le pagine di prodotto di un sito Web.

   A tale scopo, selezionare **[!UICONTROL Pagine corrispondenti alla regola]** e fare clic su **[!UICONTROL Crea regola]**.

   ![](assets/web-campaign-matching-rule.png)

1. Definisci i criteri per i campi **[!UICONTROL Dominio]** e **[!UICONTROL Pagina]**.

   Ad esempio, se desideri modificare gli elementi visualizzati in tutte le pagine del sito Web Luma relative alle donne, seleziona **[!UICONTROL Dominio]** > **[!UICONTROL Inizia con]** > `luma` e **[!UICONTROL Pagina]** > **[!UICONTROL Contiene]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Salva le modifiche. La regola viene visualizzata nella schermata **[!UICONTROL Crea campagna]**.

   ![](assets/web-pages-matching-rule-example.png)

1. Una volta definita la superficie Web, selezionare **[!UICONTROL Crea]**.

1. Completa i passaggi per creare una campagna web, ad esempio le proprietà della campagna, [pubblico](../audience/about-audiences.md) e [pianificazione](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

## Verificare la campagna web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Visualizzare l’esperienza web in anteprima"
>abstract="Ottieni una simulazione dell’aspetto che avrà l’esperienza web."

Dopo aver [creato la tua esperienza Web](edit-web-content.md) utilizzando il designer Web, puoi utilizzare i profili di test per visualizzare in anteprima le pagine Web modificate. Se hai inserito dei contenuti personalizzati, puoi verificare come vengono visualizzati, utilizzando i dati del profilo di test.

A tale scopo, fare clic su **[!UICONTROL Simula contenuto]** nella schermata Modifica contenuto della campagna Web o nella finestra di progettazione Web, quindi aggiungere un profilo di test per controllare la pagina Web utilizzando i dati del profilo di test.

![](assets/web-designer-preview.png)

Puoi anche aprirlo nel browser predefinito, oppure copiare l’URL di prova per incollarlo in qualsiasi browser. Questo ti consente di condividere il collegamento con il team e le parti interessate, che potranno visualizzare in anteprima la nuova esperienza web in qualsiasi browser prima che la campagna venga pubblicata.

>[!NOTE]
>
>Durante la copia dell&#39;URL di test, il contenuto visualizzato è quello personalizzato per il profilo di test utilizzato quando la simulazione del contenuto è stata generata in [!DNL Journey Optimizer].

Informazioni dettagliate su come selezionare profili di test e visualizzare in anteprima il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

## Attivare la campagna web {#activate-web-campaign}

Dopo aver definito le [impostazioni della campagna Web](#configure-web-campaign) e aver modificato il contenuto come desiderato utilizzando il [Web Designer](edit-web-content.md#work-with-web-designer), puoi rivedere e attivare la campagna Web. Segui i passaggi seguenti.

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. Dalla tua campagna Web, seleziona **[!UICONTROL Verifica per attivare]**.

1. Se necessario, seleziona e modifica il contenuto, le proprietà, la superficie, il pubblico e la pianificazione.

1. Seleziona **[!UICONTROL Attiva]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Dopo aver fatto clic su **[!UICONTROL Attiva]**, potrebbero essere necessari fino a 15 minuti perché le modifiche alle campagne Web siano disponibili in tempo reale sul sito Web.

La tua campagna Web assume lo stato **[!UICONTROL Live]** ed è ora visibile al pubblico selezionato. Ogni destinatario della campagna può visualizzare le modifiche aggiunte al sito Web utilizzando il Web Designer [!DNL Journey Optimizer].

>[!NOTE]
>
>Se hai definito una pianificazione per la tua campagna Web, questa avrà lo stato **[!UICONTROL Pianificato]** fino al raggiungimento della data e dell&#39;ora di inizio.
>
>Se attivi una campagna web che influisce sulle stesse pagine di un’altra campagna già live, tutte le modifiche verranno applicate alle pagine web.

Ulteriori informazioni sull&#39;attivazione delle campagne in [questa sezione](../campaigns/review-activate-campaign.md).

## Interrompere una campagna web {#stop-web-campaign}

Quando una campagna web è in diretta, puoi interromperla per impedire al pubblico di visualizzare le modifiche. Segui i passaggi seguenti.

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