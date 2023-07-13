---
solution: Journey Optimizer
product: journey optimizer
title: Anteprima e test della notifica push
description: Scopri come visualizzare in anteprima e testare le notifiche push in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 9%

---

# Anteprima e test della notifica push {#send-push}

## Anteprima della notifica push {#preview-push}

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo. Se hai inserito dei contenuti personalizzati, puoi verificare come vengono visualizzati nel messaggio, utilizzando i dati del profilo di test.

1. Clic **[!UICONTROL Simula contenuto]**.

1. Clic **[!UICONTROL Gestire i profili di test]** per aggiungere un profilo di test.

1. Trova il tuo profilo di test con **[!UICONTROL Spazio dei nomi dell’identità]** e **[!UICONTROL Valore identità]** campi. Quindi, fai clic su **[!UICONTROL Aggiungi profilo]**.

   ![](assets/push_preview_1.png)

1. Dopo aver selezionato il profilo di test, puoi chiudere **[!UICONTROL Aggiungi profilo di test]** finestra.

1. Dalla sezione **Anteprima e prova** I dati del profilo di test vengono aggiunti al contenuto del messaggio.

   Seleziona il tipo di dispositivo per l&#39;anteprima del contenuto: **[!UICONTROL iOS]** o **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Convalidare la notifica push {#push-validate}


È necessario controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** consulta consigli e best practice.

* **Errori** impedisci di testare o attivare il percorso finché non viene risolto, ad esempio:

   * **[!UICONTROL La versione push del messaggio è vuota]**: questo errore viene visualizzato quando manca il corpo o il titolo della notifica push. Scopri come definire il contenuto delle notifiche push in [questa sezione](create-push.md).

   * **[!UICONTROL La superficie non esiste]**: non puoi utilizzare il messaggio se la superficie selezionata viene eliminata dopo la creazione del messaggio. Se si verifica questo errore, seleziona un’altra superficie nel messaggio **[!UICONTROL Proprietà]**. Ulteriori informazioni sulle superfici di canale in [questa sezione](../configuration/channel-surfaces.md).

   * **[!UICONTROL Il payload push iOS/Android ha superato il limite di 4 KB]**: la dimensione della notifica push non può superare i 4 KB. Per rispettare questo limite, prova a ridurre l’uso di immagini o emoji. Scopri come gestire il contenuto delle notifiche push in [questa sezione](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> Per una migliore consegna dei messaggi, è consigliabile utilizzare sempre i numeri di telefono nei formati supportati dal provider. Ad esempio, Twilio e Sinch supportano solo i numeri di telefono in formato E.164.

## Inviare una notifica push{#push-send}

Quando il messaggio push è pronto, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) per inviarlo.

**Argomenti correlati**

* [Configurare il canale push](push-configuration.md)
* [Rapporto notifiche push](../reports/journey-global-report.md#push-global)
* [Creare una notifica push](create-push.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
* [Aggiungere un messaggio in una campagna](../campaigns/create-campaign.md)

