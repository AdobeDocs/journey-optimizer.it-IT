---
solution: Journey Optimizer
product: journey optimizer
title: Verificare e inviare la notifica push
description: Scopri come controllare e inviare le notifiche push in Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
TQID: https://experienceleague.adobe.com/QXJ9G3btsn7ZEwSB2Bm0uGt89gsh8D7SnNZ-Vw2muXM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 28eeed0d2b5dc3054c57004ead01de32151ab743
workflow-type: tm+mt
source-wordcount: 411
ht-degree: 6%

---

# Verificare e inviare una notifica push {#send-push}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come visualizzare in anteprima, convalidare e inviare le notifiche push in Adobe Journey Optimizer.

>[!ENDSHADEBOX]

## Anteprima della notifica push {#preview-push}

Una volta definito il contenuto del messaggio, puoi visualizzarne l’anteprima utilizzando uno dei seguenti metodi di simulazione:

* Fai clic su **[!UICONTROL Simula contenuto]** per testare le varianti di contenuto con dati di input di esempio o con generazione automatica di IA. [Scopri come simulare varianti di contenuto](../test-approve/simulate-sample-input.md)
* Fai clic su **[!UICONTROL Simula contenuto]**, quindi seleziona **[!UICONTROL Simula contenuto (profili AEP)]** dal menu a discesa per visualizzare l&#39;anteprima con i profili di test. È quindi possibile selezionare il tipo di dispositivo per l&#39;anteprima del contenuto: **[!UICONTROL iOS]**, **[!UICONTROL Android]** o **[!UICONTROL Web]**.

![](assets/push_preview_3.png)

Informazioni dettagliate su come visualizzare in anteprima e testare il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

## Convalidare la notifica push {#push-validate}

È necessario controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** fai riferimento a consigli e best practice.

* **Gli errori** impediscono di testare o attivare il percorso finché non vengono risolti, ad esempio:

   * **[!UICONTROL La versione push del messaggio è vuota]**: questo errore viene visualizzato quando manca il titolo o il corpo della notifica push. Scopri come definire il contenuto delle notifiche push in [questa sezione](create-push.md).

   * **[!UICONTROL la configurazione non esiste]**: non puoi utilizzare il messaggio se la configurazione selezionata viene eliminata dopo la creazione del messaggio. Se si verifica questo errore, selezionare un&#39;altra configurazione nel messaggio **[!UICONTROL Proprietà]**. Ulteriori informazioni sulle configurazioni dei canali in [questa sezione](../configuration/channel-surfaces.md).

   * **[!UICONTROL Il payload push iOS/Android ha superato il limite di 4 KB]**: la dimensione della notifica push non può superare i 4 KB. Per rispettare questo limite, prova a ridurre l’uso di immagini o emoji. Scopri come gestire il contenuto delle notifiche push in [questa sezione](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> Per una migliore consegna dei messaggi, è consigliabile utilizzare sempre i numeri di telefono nei formati supportati dal provider. Ad esempio, Twilio e Sinch supportano solo i numeri di telefono in formato E.164.

## Inviare una notifica push{#push-send}

>[!IMPORTANT]
>
> Se la campagna è soggetta a una policy di approvazione, dovrai richiedere l’approvazione per poter inviare la notifica push. [Ulteriori informazioni](../test-approve/gs-approval.md)

Quando il messaggio push è pronto, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) per inviarlo.

**Argomenti correlati**

* [Configurare il canale push per dispositivi mobili](push-configuration.md)
* [Configurare il canale push per il web](push-configuration-web.md)
* [Rapporto notifiche push](../reports/journey-global-report-cja-push.md)
* [Creare una notifica push](create-push.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journey-action.md)
* [Aggiungere un messaggio in una campagna](../campaigns/create-campaign.md)

