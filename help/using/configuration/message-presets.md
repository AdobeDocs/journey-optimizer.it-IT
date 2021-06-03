---
title: Creare predefiniti per messaggi
description: Scopri come creare i predefiniti per i messaggi e-mail e di notifica push
source-git-commit: 4353b8f01bb4e47f6f2384e464341c0ee80ecaf2
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Creare predefiniti per messaggi

Con [!DNL Journey Optimizer], puoi impostare i predefiniti per i messaggi che definiscono tutti i parametri tecnici necessari per i messaggi e-mail e di notifica push (tipo di e-mail, nome e e-mail del mittente, app mobile, ecc.).

Puoi impostare quanti predefiniti di messaggio desideri, a seconda dei diversi marchi per i quali devi comunicare.

Una volta configurati i predefiniti per i messaggi, puoi selezionarli al momento della creazione dei messaggi dall’elenco **[!UICONTROL Presets]** .

## Creare un predefinito messaggio {#create-message-preset}

Per creare un predefinito per messaggi, effettua le seguenti operazioni:

1. Accedi al menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]**, quindi fai clic su **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Specifica un nome e una descrizione (facoltativi) per il predefinito, quindi specifica i canali da configurare.

   ![](../assets/preset-general.png)

1. Configura le impostazioni di notifica e-mail e push:

   Per il canale e-mail, specifica:

   * Il tipo di comunicazioni che verranno inviate con il predefinito (messaggi transazionali o di marketing),
   * Il [sottodominio](about-subdomain-delegation.md) da utilizzare per inviare le e-mail,
   * Il [pool IP](ip-pools.md) da associare al predefinito,
   * Parametri di intestazione da utilizzare per le e-mail inviate utilizzando il predefinito.

   ![](../assets/preset-email.png)

   Per il canale di notifica push, specifica le applicazioni mobili IOS e/o Android da utilizzare per i messaggi. Per ulteriori informazioni su come configurare l&#39;ambiente per l&#39;invio di notifiche push, consulta [questa sezione](../push-configuration.md).

   ![](../assets/preset-push.png)

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Submit]** per confermare. Puoi anche salvare il predefinito del messaggio come bozza e ripristinarne la configurazione in un secondo momento.

   ![](../assets/preset-submit.png)

1. Una volta creato, il predefinito del messaggio viene visualizzato nell’elenco con lo stato **[!UICONTROL Processing]** .

   Durante questo passaggio, verranno eseguiti diversi controlli per verificare che sia stato configurato correttamente. Il tempo di elaborazione è di circa 48h-72h e può richiedere fino a 7-10 giorni.

   Questi controlli includono test di recapito messaggi eseguiti dal team di recapito messaggi di Adobe:

   * convalida SPF,
   * Convalida DKIM,
   * convalida record MX,
   * Controlla la blacklist degli IP,
   * Controllo host Helo,
   * verifica del pool IP,
   * Record A/PTR, verifica del sottodominio t/m/res.

1. Una volta eseguiti i controlli, il predefinito del messaggio ottiene lo stato **[!UICONTROL Active]** . È pronto per essere utilizzato per inviare messaggi.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Monitorare i predefiniti per messaggi

Tutti i predefiniti per messaggi vengono visualizzati nel menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** . Sono disponibili filtri per aiutarti a sfogliare l’elenco (tipo di canale, utente, stato).

![](../assets/preset-filters.png)

I predefiniti per messaggi possono avere i seguenti stati:

* **[!UICONTROL Draft]**: Il predefinito del messaggio è stato salvato come bozza e non è ancora stato inviato. Apri per riprendere la configurazione.
* **[!UICONTROL Processing]**: Il predefinito del messaggio è stato inviato e sta attraversando diverse fasi di verifica.
* **[!UICONTROL Active]**: Il predefinito del messaggio è stato verificato e può essere selezionato per creare i messaggi.
* **[!UICONTROL Failed]**: Uno o più controlli non sono riusciti durante la verifica del predefinito del messaggio.
* **[!UICONTROL De-activated]**: Il predefinito del messaggio viene disattivato. Non può essere utilizzato per creare nuovi messaggi.

## Modificare i predefiniti per i messaggi

Per modificare un predefinito per messaggi, devi prima disattivarlo per renderlo non disponibile per la creazione di nuovi messaggi (i messaggi pubblicati con questo predefinito non saranno interessati e continueranno a funzionare). Devi quindi duplicare il predefinito per messaggi per creare una nuova versione da usare per creare nuovi messaggi:

1. Accedi all’elenco dei predefiniti per messaggi e disattiva il predefinito per messaggi da modificare.

   ![](../assets/preset-deactivate.png)

1. Duplica il predefinito di messaggio disattivato. All’elenco viene automaticamente aggiunta una copia con lo stato **[!UICONTROL Draft]** .

   ![](../assets/preset-duplicated.png)

1. Apri il predefinito di messaggio duplicato, modificalo in base alle tue esigenze, quindi invia le modifiche. Il predefinito per messaggi eseguirà lo stesso ciclo di convalida del passaggio di [creazione](#create-message-preset).

1. Una volta convalidato, ottiene lo stato **[!UICONTROL Active]** ed è pronto per essere utilizzato per creare nuovi messaggi.

   >[!NOTE]
   >
   >I predefiniti per messaggi disattivati non possono essere eliminati per evitare problemi nei percorsi che utilizzano questi predefiniti per inviare messaggi.