---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti di contenuto di AEM
description: Scopri come accedere e gestire i frammenti di contenuto di AEM
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 2%

---

# Frammenti di contenuto di Adobe Experience Manager {#aem-fragments}

Integrando Adobe Experience Manager con Adobe Journey Optimizer, ora puoi incorporare facilmente i frammenti di contenuto AEM nel contenuto dell’e-mail Journey Optimizer. Questa connessione semplificata semplifica il processo di accesso e utilizzo dei contenuti AEM, consentendo la creazione di campagne e percorsi personalizzati e dinamici.

Per ulteriori informazioni sul frammento di contenuto di AEM, consulta la [documentazione di Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments).

## Limitazioni {#limitations}

* Disponibile solo per il canale e-mail.

* Al momento gli utenti non possono cambiare l’istanza di AEM a cui sono connessi, in quanto ogni sandbox è limitata a una singola istanza.

* Per ridurre il rischio di errori accidentali nelle e-mail, si consiglia di limitare il numero di utenti con accesso alla pubblicazione di frammenti di contenuto.

* Per i contenuti multilingue, è supportato solo il flusso manuale.

* Varianti non supportate.

* Devi creare un tag specifico per Journey Optimizer.

+++ Scopri come creare il tag Journey Optimizer

   1. Accedi al tuo ambiente **Experience Manager**.

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

1. Dal menu **[!UICONTROL Frammento di contenuto di AEM]** nel riquadro a sinistra, fare clic su **[!UICONTROL Apri selettore CF di AEM]**.

   ![](assets/aem_campaign_3.png)

1. Seleziona un **[!UICONTROL frammento di contenuto]** dall&#39;elenco disponibile per l&#39;importazione nel contenuto di Journey Optimizer.

1. Fai clic su **[!UICONTROL Mostra filtri]** per ottimizzare l&#39;elenco dei frammenti di contenuto.

   Per impostazione predefinita, il filtro Frammento di contenuto è predefinito per visualizzare solo il contenuto approvato.

   ![](assets/aem_campaign_4.png)

1. Dopo aver selezionato il **[!UICONTROL frammento di contenuto]**, fai clic su **[!UICONTROL Seleziona]** per aprirlo.

   ![](assets/aem_campaign_5.png)

1. Scegli i campi desiderati dal **[!UICONTROL frammento di contenuto]** da aggiungere al contenuto. Puoi aggiungere il contenuto o copiarne il valore.

   Se scegli di copiare il valore, eventuali aggiornamenti futuri al **[!UICONTROL frammento di contenuto]** non verranno inclusi nella campagna o nel percorso.

   ![](assets/aem_campaign_6.png)

1. Fai clic su **[!UICONTROL Salva]** e controlla il messaggio nell&#39;anteprima. Ora puoi testare e controllare il contenuto del messaggio come descritto in [questa sezione](../content-management/preview.md).

Dopo aver eseguito i test e convalidato il contenuto, puoi inviare la tua e-mail al pubblico con la tua [campagna](../campaigns/review-activate-campaign.md) o [Percorso](../building-journeys/publishing-the-journey.md).
