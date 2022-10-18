---
solution: Journey Optimizer
product: journey optimizer
title: Avvisi nei messaggi
description: Scopri come verificare la convalida del contenuto dei messaggi e risolvere i problemi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 7%

---

# Controllare gli avvisi sui messaggi {#messages-alerts}

## Controlli prima dell’invio {#message-alerting}

Durante la progettazione dei messaggi, gli avvisi vengono visualizzati nell’interfaccia quando mancano le impostazioni chiave.

Gli avvisi vengono visualizzati in alto a destra dello schermo durante la modifica del contenuto del messaggio.

![](assets/alerts-details.png)

>[!NOTE]
>
>In caso contrario, non è stato rilevato alcun avviso.

Possono verificarsi due tipi di avvisi:

* **Avvisi** consulta consigli e best practice. Ad esempio, se manca il collegamento di rinuncia, viene visualizzato un messaggio.

* **Errori** impedisce di testare o attivare il percorso purché non siano risolti. Ad esempio, un messaggio ti avviserà che manca l’oggetto.

Tutti i possibili avvisi ed errori sono descritti in dettaglio [di seguito](#alerts-and-warnings).

>[!CAUTION]
>
> È necessario risolvere tutti **errore** avvisa prima di testare o attivare il percorso utilizzando il messaggio.

## Elenco degli avvisi e degli errori {#alerts-and-warnings}

Le impostazioni e gli elementi controllati dal sistema sono elencati di seguito. Troverai anche informazioni su come adattare la configurazione per risolvere i problemi corrispondenti.

**Avvisi**:

* **[!UICONTROL Il collegamento di rinuncia non è presente nel corpo dell’e-mail]**: è consigliabile aggiungere un collegamento per l’annullamento dell’abbonamento al corpo dell’e-mail. Scopri come configurarlo in [questa sezione](../privacy/opt-out.md#opt-out-management).

   >[!NOTE]
   >
   >I messaggi e-mail di tipo marketing devono includere un collegamento di rinuncia, che non è necessario per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]**) è definita per la [superficie di canale](../configuration/channel-surfaces.md#email-type) (ossia per il predefinito del messaggio) e durante la [creazione del messaggio](get-started-content.md#create-new-message).

* **[!UICONTROL La versione del testo di HTML è vuota]**: non dimenticare di definire una versione testuale del corpo dell’e-mail, in quanto verrà utilizzata quando non è possibile visualizzare il contenuto di HTML. Scopri come creare la versione di testo in [questa sezione](../design/text-version-email.md).

* **[!UICONTROL Il collegamento vuoto è presente nel corpo dell’e-mail]**: controlla che tutti i collegamenti presenti nell’e-mail siano corretti. Scopri come gestire contenuti e collegamenti in [questa sezione](../design/create-email-content.md).

* **[!UICONTROL La dimensione dell’e-mail ha superato il limite di 100 KB]**: per una consegna ottimale, assicurati che la dimensione dell’e-mail non superi i 100 KB. Scopri come modificare il contenuto delle e-mail in [questa sezione](../design/create-email-content.md).

**Errori**:

* **[!UICONTROL Riga oggetto mancante]**: la riga dell’oggetto dell’e-mail è obbligatoria. Scopri come definirlo e personalizzarlo in [questa sezione](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL La versione push del messaggio è vuota]**: questo errore viene visualizzato quando manca il corpo o il titolo della notifica push. Scopri come definire il contenuto delle notifiche push in [questa sezione](create-push.md).

* **[!UICONTROL La versione del messaggio e-mail è vuota]**: questo errore viene visualizzato quando il contenuto dell’e-mail non è stato configurato. Scopri come progettare il contenuto delle e-mail in [questa sezione](../design/design-emails.md).

* **[!UICONTROL La superficie non esiste]**: non puoi utilizzare il messaggio se la superficie selezionata viene eliminata dopo la creazione del messaggio. Se si verifica questo errore, seleziona un’altra superficie nel messaggio **[!UICONTROL Proprietà]**. Ulteriori informazioni sulle superfici dei canali in [questa sezione](../configuration/channel-surfaces.md).

* **[!UICONTROL Il payload push iOS/Android ha superato il limite di 4 KB]**: la dimensione della notifica push non può superare i 4 KB. Per rispettare questo limite, prova a ridurre l’uso di immagini o emoticon. Scopri come gestire il contenuto delle notifiche push in [questa sezione](create-push.md).

>[!CAUTION]
>
> Per poter utilizzare il messaggio, è necessario risolvere tutti i problemi **errore** avvisi

<!--Other issues can stop publication such as:
* The push notification title is empty-->
