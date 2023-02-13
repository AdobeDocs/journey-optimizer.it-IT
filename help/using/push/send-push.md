---
solution: Journey Optimizer
product: journey optimizer
title: Anteprima e verifica la notifica push
description: Scopri come visualizzare in anteprima e testare la notifica push in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 5%

---

# Anteprima e verifica la notifica push {#send-push}

## Anteprima della notifica push {#preview-push}

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo. Se hai inserito contenuto personalizzato, puoi controllare come questo contenuto viene visualizzato nel messaggio, utilizzando i dati del profilo di test.

1. Fai clic su **[!UICONTROL Simulazione del contenuto]**.

1. Fai clic su **[!UICONTROL Gestire i profili di test]** per aggiungere un profilo di test.

1. Trova il tuo profilo di test con **[!UICONTROL Spazio dei nomi identità]** e **[!UICONTROL Valore identità]** campi. Quindi, fai clic su **[!UICONTROL Aggiungi profilo]**.

   ![](assets/push_preview_1.png)

1. Dopo aver selezionato il profilo di test, puoi chiudere la **[!UICONTROL Aggiungi profilo di test]** finestra.

1. Da **Anteprima e test** i dati del profilo di test vengono aggiunti al contenuto del messaggio.

   Seleziona il tipo di dispositivo per visualizzare in anteprima il contenuto: **[!UICONTROL iOS]** o **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Convalida la notifica push {#push-validate}


Devi controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedire l’invio del messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** consulta consigli e best practice.

* **Errori** impedisce il test o l’attivazione del percorso finché non vengono risolti, ad esempio:

   * **[!UICONTROL La versione push del messaggio è vuota]**: questo errore viene visualizzato quando manca il corpo o il titolo della notifica push. Scopri come definire il contenuto delle notifiche push in [questa sezione](create-push.md).

   * **[!UICONTROL La superficie non esiste]**: non puoi utilizzare il messaggio se la superficie selezionata viene eliminata dopo la creazione del messaggio. Se si verifica questo errore, seleziona un’altra superficie nel messaggio **[!UICONTROL Proprietà]**. Ulteriori informazioni sulle superfici dei canali in [questa sezione](../configuration/channel-surfaces.md).

   * **[!UICONTROL Il payload push iOS/Android ha superato il limite di 4 KB]**: la dimensione della notifica push non può superare i 4 KB. Per rispettare questo limite, prova a ridurre l’uso di immagini o emoticon. Scopri come gestire il contenuto delle notifiche push in [questa sezione](../push/create-push.md).

   ![](assets/push_alert.png)


>[!NOTE]
>
> Per una migliore consegna, è sempre necessario utilizzare i numeri di telefono nei formati supportati dal provider. Ad esempio, Twilio e Sinch supportano solo i numeri di telefono in formato E.164.

## Inviare una notifica push{#push-send}

Quando il messaggio push è pronto, completa la configurazione della [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) per inviarlo.

**Argomenti correlati**

* [Configurare il canale push](push-configuration.md)
* [Rapporto notifiche push](../reports/journey-global-report.md#push-global)
* [Creare una notifica push](create-push.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
* [Aggiungere un messaggio in una campagna](../campaigns/create-campaign.md)

