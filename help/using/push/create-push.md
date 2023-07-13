---
solution: Journey Optimizer
product: journey optimizer
title: Configurare una notifica push
description: Scopri come creare una notifica push in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 16%

---

# Creare una notifica push {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Creazione di messaggi push"
>abstract="Aggiungi il messaggio push e inizia a personalizzarlo con l’editor di espressioni."

## Creare la notifica push in un percorso o in una campagna {#create}

Per creare una notifica push, effettua le seguenti operazioni:

>[!BEGINTABS]

>[!TAB Aggiungere un messaggio push a un Percorso]

1. Apri il percorso, quindi trascina e rilascia un’attività Push dalla sezione Azioni della palette.

   ![](assets/push_create_1.png)

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria), quindi scegli la superficie del messaggio da utilizzare. Il **[!UICONTROL Superficie]** Il campo è precompilato, per impostazione predefinita, con l’ultima superficie utilizzata dall’utente per quel canale.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >Se invii una notifica push da un percorso, puoi sfruttare la funzione di ottimizzazione dell’ora di invio di Adobe Journey Optimizer per prevedere il momento migliore per inviare il messaggio in modo da massimizzare il coinvolgimento in base alle percentuali storiche di apertura e clic. [Scopri come utilizzare l’ottimizzazione dell’ora di invio](../building-journeys/journeys-message.md#send-time-optimization)

   Per ulteriori informazioni su come configurare un percorso, consulta [questa pagina](../building-journeys/journey-gs.md)

1. Dalla schermata di configurazione del percorso, fai clic su **[!UICONTROL Modifica contenuto]** per configurare il contenuto push. [Progettare una notifica push](design-push.md)

1. Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo.

1. Quando il push è pronto, completa la configurazione del [percorso](../building-journeys/journey-gs.md) per inviarlo.

   Per tenere traccia del comportamento dei destinatari attraverso le aperture push e/o le interazioni, assicurati che le opzioni dedicate nella sezione di tracciamento siano abilitate nel [attività e-mail](../building-journeys/journeys-message.md).

>[!TAB Aggiungere una notifica push a una campagna]

1. Crea una nuova campagna pianificata o attivata da API, seleziona **[!UICONTROL Notifica push]** come azione e scegli il **[!UICONTROL Superficie app]** da utilizzare. [Ulteriori informazioni sulla configurazione push](push-configuration.md).

   ![](assets/push_create_3.png)

1. Fai clic su **[!UICONTROL Crea]**.

1. Dalla sezione **[!UICONTROL Proprietà]** , modifica i **[!UICONTROL Titolo]** e **[!UICONTROL Descrizione]**.

   ![](assets/push_create_4.png)

1. Fai clic su **[!UICONTROL Seleziona pubblico]** per definire il pubblico di destinazione dall’elenco dei tipi di pubblico di Adobe Experience Platform disponibili. [Maggiori informazioni](../audience/about-audiences.md).

1. In **[!UICONTROL Spazio dei nomi dell’identità]** , scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti del pubblico selezionato. [Maggiori informazioni](../event/about-creating.md#select-the-namespace).

   ![](assets/push_create_5.png)

1. Clic **[!UICONTROL Crea esperimento]** per iniziare a configurare l’esperimento sui contenuti e creare trattamenti per misurarne le prestazioni e identificare l’opzione migliore per il pubblico di destinazione. [Ulteriori informazioni](../campaigns/content-experiment.md)

1. Le campagne sono progettate per essere eseguite in una data specifica o con una frequenza ricorrente. Scopri come configurare **[!UICONTROL Pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

1. Dalla sezione **[!UICONTROL Trigger azione]** scegliere il menu **[!UICONTROL Frequenza]** della notifica push:

   * Una volta
   * Giornaliero
   * Settimanale
   * Mensile

1. Dalla schermata di configurazione della campagna, fai clic su **[!UICONTROL Modifica contenuto]** per configurare il contenuto push. [Progettare una notifica push](design-push.md)

1. Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo.

1. Quando il push è pronto, completa la configurazione del [campagna](../campaigns/create-campaign.md) per inviarlo.

   Per tenere traccia del comportamento dei destinatari attraverso le aperture push e/o le interazioni, assicurati che le opzioni dedicate nella sezione di tracciamento siano abilitate nel [campagna](../campaigns/create-campaign.md).

>[!ENDTABS]

**Argomenti correlati**

* [Configurare il canale push](push-gs.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)

## Modalità di consegna rapida {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Modalità di consegna rapida"
>abstract="La modalità di consegna rapida consente di inviare messaggi ad alta velocità sul canale push a un pubblico di dimensione inferiore a 30 milioni."

La modalità Consegna rapida, precedentemente nota come modalità Burst in percorsi, è una [!DNL Journey Optimizer] componente aggiuntivo che consente l’invio molto rapido di messaggi push in volumi elevati tramite campagne.

La consegna rapida viene utilizzata quando il ritardo nella consegna dei messaggi è di importanza critica per l’azienda, quando si desidera inviare un avviso push urgente sui telefoni cellulari, ad esempio una notizia straordinaria agli utenti che hanno installato la tua app per il canale news.

Per ulteriori informazioni sulle prestazioni quando si utilizza la modalità Consegna rapida, consulta [Descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html).

### Prerequisiti {#prerequisites}

I messaggi di consegna rapida sono forniti con i seguenti requisiti:

* La consegna rapida è disponibile per **[!UICONTROL Pianificato]** solo campagne e non è disponibile per le campagne attivate da API,
* Nel messaggio push non è consentita alcuna personalizzazione,
* Il pubblico di destinazione deve contenere meno di 30 milioni di profili,
* Puoi eseguire fino a 5 campagne simultaneamente utilizzando la modalità Consegna rapida.

### Attiva modalità Consegna rapida

1. Creare una campagna di notifica push e attivare **[!UICONTROL Consegna rapida]** opzione.

![](assets/create-campaign-burst.png)

1. Configura il contenuto del messaggio e seleziona il pubblico di destinazione. [Scopri come creare una campagna](#create)

   >[!IMPORTANT]
   >
   >Assicurati che il contenuto del messaggio non includa alcuna personalizzazione e che il pubblico contenga meno di 30 milioni di profili.

1. Rivedi e attiva la campagna come di consueto. Tieni presente che, in modalità di test, i messaggi non vengono inviati tramite la modalità Consegna rapida.