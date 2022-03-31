---
title: Avvisi nei messaggi
description: Scopri come verificare la convalida del contenuto dei messaggi e risolvere i problemi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Controllare gli avvisi sui messaggi {#publish-manage-messages}

## Controlli prima della pubblicazione {#message-alerting}

Durante la creazione del messaggio, gli avvisi ti avvisano quando devi intraprendere azioni importanti prima di pubblicarlo.

Gli avvisi vengono visualizzati in alto a destra dello schermo, come illustrato di seguito:

![](assets/message-alerts.png)

>[!NOTE]
>
>In caso contrario, non è stato rilevato alcun avviso.

Possono verificarsi due tipi di avvisi:

* **Avvisi** consulta consigli e best practice. Ad esempio, se manca il collegamento di rinuncia, viene visualizzato un messaggio.

* **Errori** impedisce la pubblicazione del messaggio fintanto che non sono stati risolti. Ad esempio, un messaggio ti avviserà che manca l’oggetto.

Tutti i possibili avvisi ed errori sono descritti in dettaglio [di seguito](#alerts-and-warnings).

>[!CAUTION]
>
> È necessario risolvere tutti **errore** avvisi prima della pubblicazione.

## Elenco degli avvisi e degli errori {#alerts-and-warnings}

Le impostazioni e gli elementi controllati dal sistema sono elencati di seguito. Troverai anche informazioni su come adattare la configurazione per risolvere i problemi corrispondenti.

**Avvisi**:

* **[!UICONTROL The opt-out link is not present in the email body.]**: è consigliabile aggiungere un collegamento per l’annullamento dell’abbonamento al corpo dell’e-mail. Scopri come configurarlo in [questa sezione](consent.md).

* **[!UICONTROL Text version of HTML is empty.]**: non dimenticare di definire una versione testuale del corpo dell’e-mail, in quanto verrà utilizzata quando non è possibile visualizzare il contenuto di HTML. Scopri come creare la versione di testo in [questa sezione](../design/text-version-email.md).

* **[!UICONTROL Empty link is present in email body.]**: controlla che tutti i collegamenti presenti nell’e-mail siano corretti. Scopri come gestire contenuti e collegamenti in [questa sezione](../design/create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB.]**: per una consegna ottimale, assicurati che la dimensione dell’e-mail non superi i 100 KB. Scopri come modificare il contenuto delle e-mail in [questa sezione](../design/create-email-content.md).

**Errori**:

* **[!UICONTROL The subject line is missing.]**: la riga dell’oggetto dell’e-mail è obbligatoria. Scopri come definirlo e personalizzarlo in [questa sezione](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL The push version of the message is empty.]**: questo errore viene visualizzato quando manca il corpo o il titolo della notifica push. Scopri come definire il contenuto delle notifiche push in [questa sezione](create-push.md).

* **[!UICONTROL The email version of the message is empty.]**: questo errore viene visualizzato quando il contenuto dell’e-mail non è stato configurato. Scopri come progettare il contenuto delle e-mail in [questa sezione](../design/design-emails.md).

* **[!UICONTROL Preset doesn’t exist.]**: non puoi pubblicare il messaggio se il predefinito selezionato viene eliminato dopo la creazione del messaggio. Se si verifica questo errore, seleziona un altro predefinito nel messaggio **[!UICONTROL Properties]**. Ulteriori informazioni sul branding in [questa sezione](../configuration/about-subdomain-delegation.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB.]**: la dimensione della notifica push non può superare i 4 KB. Per rispettare questo limite, prova a ridurre l’uso di immagini o emoticon. Scopri come gestire il contenuto delle notifiche push in [questa sezione](create-push.md).

>[!CAUTION]
>
> Per pubblicare il messaggio, devi risolvere tutti i problemi **errore** avvisi

<!--Other issues can stop publication such as:
* The push notification title is empty-->
