---
title: Avvisi nei messaggi
description: Scopri come verificare la convalida del contenuto dei messaggi e risolvere i problemi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 3%

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

* **[!UICONTROL The opt-out link is not present in the email body]**: è consigliabile aggiungere un collegamento per l’annullamento dell’abbonamento al corpo dell’e-mail. Scopri come configurarlo in [questa sezione](consent.md#opt-out-management).

   >[!NOTE]
   >
   >I messaggi e-mail di tipo marketing devono includere un collegamento di rinuncia, che non è necessario per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transactional]**) è definita nella [superficie del canale](../configuration/channel-surfaces.md#email-type) (ad es. predefinito messaggio) e quando [creazione del messaggio](get-started-content.md#create-new-message).

* **[!UICONTROL Text version of HTML is empty]**: non dimenticare di definire una versione testuale del corpo dell’e-mail, in quanto verrà utilizzata quando non è possibile visualizzare il contenuto di HTML. Scopri come creare la versione di testo in [questa sezione](../design/text-version-email.md).

* **[!UICONTROL Empty link is present in email body]**: controlla che tutti i collegamenti presenti nell’e-mail siano corretti. Scopri come gestire contenuti e collegamenti in [questa sezione](../design/create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**: per una consegna ottimale, assicurati che la dimensione dell’e-mail non superi i 100 KB. Scopri come modificare il contenuto delle e-mail in [questa sezione](../design/create-email-content.md).

**Errori**:

* **[!UICONTROL The subject line is missing]**: la riga dell’oggetto dell’e-mail è obbligatoria. Scopri come definirlo e personalizzarlo in [questa sezione](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL The push version of the message is empty]**: questo errore viene visualizzato quando manca il corpo o il titolo della notifica push. Scopri come definire il contenuto delle notifiche push in [questa sezione](create-push.md).

* **[!UICONTROL The email version of the message is empty]**: questo errore viene visualizzato quando il contenuto dell’e-mail non è stato configurato. Scopri come progettare il contenuto delle e-mail in [questa sezione](../design/design-emails.md).

* **[!UICONTROL Surface doesn’t exist]**: non puoi utilizzare il messaggio se la superficie selezionata viene eliminata dopo la creazione del messaggio. Se si verifica questo errore, seleziona un’altra superficie nel messaggio **[!UICONTROL Properties]**. Ulteriori informazioni sulle superfici dei canali in [questa sezione](../configuration/channel-surfaces.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: la dimensione della notifica push non può superare i 4 KB. Per rispettare questo limite, prova a ridurre l’uso di immagini o emoticon. Scopri come gestire il contenuto delle notifiche push in [questa sezione](create-push.md).

>[!CAUTION]
>
> Per poter utilizzare il messaggio, è necessario risolvere tutti i problemi **errore** avvisi

<!--Other issues can stop publication such as:
* The push notification title is empty-->
