---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti di contenuto AEM
description: Scopri come accedere e gestire i frammenti di contenuto AEM
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 50b36446ff0e9f4aec9f28056c3c30cc2df3f530
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---

# Frammenti di contenuto Adobe Experience Manager {#aem-fragments}

Integrando Adobe Experience Manager con Adobe Journey Optimizer, ora puoi incorporare facilmente i frammenti di contenuto AEM nel contenuto dell’e-mail Journey Optimizer. Questa connessione semplificata semplifica l’accesso ai contenuti dell’AEM e la loro utilizzazione, consentendo la creazione di campagne e percorsi personalizzati e dinamici.

Per ulteriori informazioni sul frammento di contenuto AEM, consulta la [documentazione dell&#39;Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments).

## Limitazioni {#limitations}

* Disponibile solo per il canale e-mail.

* Al momento gli utenti non possono cambiare l’istanza AEM a cui sono connessi, poiché ogni sandbox è limitata a una singola istanza.

* Per ridurre il rischio di errori accidentali nelle e-mail, si consiglia di limitare il numero di utenti con accesso alla pubblicazione di frammenti di contenuto.

* Per i contenuti multilingue, è supportato solo il flusso manuale.

* Varianti non supportate.

* Devi creare un tag specifico per Journey Optimizer.

+++ Scopri come creare il tag Journey Optimizer

   1. Accedi all&#39;ambiente **Experience Manager**.

   1. Dal menu **Strumenti**, passare alla scheda **Generale** e selezionare **Assegnazione tag**.

   1. Fare clic su **Crea nuovo tag**.

   1. Verificare che l&#39;ID sia conforme alla sintassi seguente: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

   1. Fai clic su **Crea**.

  Ora puoi assegnare questo tag Journey Optimizer ai frammenti di contenuto.
+++

## Aggiungere frammenti di contenuto AEM {#aem-add}

Dopo aver creato e personalizzato i [Frammenti di contenuto AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments), puoi importarli nella campagna o nel percorso dell&#39;ottimizzatore di Percorso.

1. Dopo aver creato la [campagna](../email/create-email.md) o il [Percorso](../email/create-email.md) con un&#39;azione e-mail, accedi a e-mail designer per configurare il contenuto dell&#39;e-mail. [Ulteriori informazioni](../email/get-started-email-design.md)

1. Fare clic all&#39;interno di un blocco di testo o nella riga dell&#39;oggetto e selezionare **[!UICONTROL Aggiungi Personalization]** dalla barra degli strumenti contestuale.

   ![](assets/aem_campaign_2.png)

1. Dal menu **[!UICONTROL Frammento di contenuto AEM]** nel riquadro a sinistra, fare clic su **[!UICONTROL Apri selettore CF AEM]**.

   ![](assets/aem_campaign_3.png)

1. Seleziona un **[!UICONTROL frammento di contenuto]** dall&#39;elenco disponibile per l&#39;importazione nel contenuto di Journey Optimizer.

   >[!IMPORTANT]
   >
   >È possibile utilizzare solo i **[!UICONTROL frammenti di contenuto]** pubblicati.

1. Fai clic su **[!UICONTROL Mostra filtri]** per ottimizzare l&#39;elenco dei frammenti di contenuto.

   Il selettore Frammento di contenuto include filtri preconfigurati:

   * **[!UICONTROL Stato]**: pubblicato, modificato
   * **[!UICONTROL Tag]**: definito automaticamente in base all&#39;ambiente Journey Optimizer (ID organizzazione e sandbox)

   ![](assets/aem_campaign_4.png)

1. Dopo aver selezionato il **[!UICONTROL frammento di contenuto]**, fai clic su **[!UICONTROL Seleziona]** per aprirlo.

   ![](assets/aem_campaign_5.png)

1. Scegli i campi desiderati dal **[!UICONTROL frammento di contenuto]** da aggiungere al contenuto.

   ![](assets/aem_campaign_6.png)

1. Fai clic su **[!UICONTROL Salva]** e controlla il messaggio nell&#39;anteprima. Ora puoi testare e controllare il contenuto del messaggio come descritto in [questa sezione](preview.md).

Dopo aver eseguito i test e convalidato il contenuto, puoi inviare la tua e-mail al pubblico con la tua [campagna](../campaigns/review-activate-campaign.md) o [Percorso](../building-journeys/publishing-the-journey.md).

