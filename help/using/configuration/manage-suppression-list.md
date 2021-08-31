---
title: Gestire l’elenco di soppressione
description: 'Scopri come accedere e gestire l’elenco di soppressione di Journey Optimizer '
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 260513cd966ab8e579fa0af0fec0376110d0b53f
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 2%

---


# Gestire l’elenco di soppressione {#manage-suppression-list}

Con [!DNL Journey Optimizer] puoi monitorare tutti gli indirizzi e-mail che vengono automaticamente esclusi dall’invio in un percorso, ad esempio:

* Indirizzi non validi (rimbalzi rigidi).
* Gli indirizzi non recapitati in modo coerente e possono influenzare negativamente la reputazione delle e-mail se continui a includerli nelle consegne.
* Destinatari che emettono una denuncia di spam di qualche tipo contro uno dei tuoi messaggi e-mail.

Tali indirizzi e-mail vengono raccolti automaticamente nell&#39;elenco di eliminazione di Journey Optimizer ****. Ulteriori informazioni sul concetto e sull&#39;utilizzo dell&#39;elenco di soppressione in [questa sezione](../suppression-list.md).

## Accedere all&#39;elenco di soppressione {#access-suppression-list}

Per accedere all’elenco dettagliato degli indirizzi e-mail esclusi, vai su **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** e seleziona **[!UICONTROL Suppression list]**.

>[!CAUTION]
>
>Le autorizzazioni per visualizzare, esportare e gestire l&#39;elenco di soppressione sono limitate a [Amministratori di Percorso](../administration/ootb-product-profiles.md#journey-administrator). Ulteriori informazioni sulla gestione dei diritti di accesso degli utenti [!DNL Journey Optimizer] in [questa sezione](../administration/permissions-overview.md).

<!--![](../assets/suppression-list-link.png)

You can also display the suppression list content using the **[!UICONTROL View suppression list]** link through the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** menu, but this view does not allow you to edit the list.-->

![](../assets/suppression-list-access.png)

Sono disponibili filtri che consentono di sfogliare l’elenco.

<!--![](../assets/suppression-list-filters-temp.png)-->

![](../assets/suppression-list-filters.png)

Puoi filtrare i valori **[!UICONTROL Suppression category]**, **[!UICONTROL Address type]** o **[!UICONTROL Reason]**. Seleziona le opzioni desiderate per ciascun criterio. Una volta selezionato, puoi cancellare ogni filtro o tutti i filtri visualizzati in cima all’elenco.

![](../assets/suppression-list-filtering-example.png)

Se aggiungi manualmente un indirizzo e-mail o un dominio per errore, il pulsante **[!UICONTROL Delete]** ti consente di rimuovere tale voce.

>[!CAUTION]
>
>Non utilizzare mai il pulsante **[!UICONTROL Delete]** per rimuovere gli indirizzi e-mail o i domini soppressi.

![](../assets/suppression-list-delete.png)

Se elimini un indirizzo e-mail o un dominio dall&#39;elenco di soppressione significa che inizierai di nuovo a consegnare a questo indirizzo o dominio. Di conseguenza, questo può avere gravi ripercussioni sulla consegna e sulla reputazione dell’IP, il che potrebbe comportare il blocco dell’indirizzo IP o del dominio di invio. Ulteriori informazioni sull&#39;importanza di mantenere un elenco di soppressione in [questa sezione](../suppression-list.md).

>[!NOTE]
>
>Procedi con molta attenzione quando consideri di eliminare qualsiasi indirizzo e-mail o dominio. In caso di dubbio, contatta un esperto di recapito.

Dalla vista **[!UICONTROL Suppression list]** è inoltre possibile modificare le regole di soppressione. [Ulteriori informazioni](retries.md)

Per esportare l’elenco di soppressione come file CSV, seleziona il pulsante **[!UICONTROL Download CSV]** .

![](../assets/suppression-list-download-csv.png)

## Categorie e motivi di soppressione {#suppression-categories-and-reasons}

Quando un messaggio non viene recapitato a un indirizzo e-mail, [!DNL Journey Optimizer] determina il motivo per cui la consegna non è riuscita e lo associa a **[!UICONTROL Suppression category]**.

Le categorie di soppressione sono le seguenti:

* **Rigido**: L’indirizzo e-mail viene inviato immediatamente all’elenco di eliminazione.

   >[!NOTE]
   >
   >Quando l&#39;errore è il risultato di un reclamo di spam, rientra anche nella categoria **Hard**. L&#39;indirizzo e-mail del destinatario che ha emesso il reclamo viene inviato immediatamente all&#39;elenco di soppressione.

* **Morbido**: Gli errori morbidi inviano un indirizzo all’elenco di soppressione quando il contatore degli errori raggiunge la soglia limite. [Ulteriori informazioni sui nuovi tentativi](retries.md)

   <!--
    **Ignored**:
    * When the error occurred for a valid email address but is known to be temporary, such as a failed connection attempt or a temporary technical issue, the email address is added to the suppression list once the error counter reaches the limit threshold. [Learn more on retries](retries.md).
    * When the error is the result of a spam complaint, the email address of the recipient who issued the complaint is immediately sent to the suppression list.
    -->

* **Manuale**: Puoi anche aggiungere manualmente un indirizzo e-mail o un dominio all’elenco di eliminazione. [Ulteriori informazioni](#add-addresses-and-domains)

>[!NOTE]
>
>Ulteriori informazioni sui mancati recapiti e i mancati recapiti nella sezione [Tipi di errori di consegna](../suppression-list.md#delivery-failures) .

Per ogni indirizzo e-mail elencato, puoi anche controllare **[!UICONTROL Type]** (e-mail o dominio), **[!UICONTROL Reason]** per escluderlo, chi l’ha aggiunto e la data/ora in cui è stato aggiunto all’elenco di eliminazione.

![](../assets/suppression-list.png)

I possibili motivi di un errore di consegna sono:

| Motivo | Descrizione | Categoria di soppressione |
| --- | --- | --- |
| **[!UICONTROL Invalid Recipient]** | Il destinatario non è valido o non esiste. | Duro |
| **[!UICONTROL Soft Bounce]** | Il messaggio è stato rimbalzato per un motivo diverso dagli errori soft elencati in questa tabella, ad esempio quando si invia la velocità consentita consigliata da un ISP. | Morbido |
| **[!UICONTROL DNS Failure]** | Messaggio rimbalzato a causa di un errore DNS. | Morbido |
| **[!UICONTROL Mailbox Full]** | Il messaggio è stato rimbalzato perché la casella di posta del destinatario era piena e non poteva accettare altri messaggi. | Morbido |
| **[!UICONTROL Relaying Denied]** | Il messaggio è stato bloccato dal destinatario perché l&#39;invio non è consentito. | Morbido |
| **[!UICONTROL Challenge-Response]** | Il messaggio è una sonda di risposta alla sfida. | Morbido |
| **[!UICONTROL Spam Complaint]** | Il messaggio è stato bloccato perché contrassegnato come spam dal destinatario. | Duro |

>[!NOTE]
>
>Gli utenti non abbonati non ricevono e-mail da [!DNL Journey Optimizer], pertanto i loro indirizzi e-mail non possono essere inviati all’elenco di soppressione. La loro scelta viene gestita a livello di Experience Platform. [Ulteriori informazioni sulla rinuncia](../consent.md)

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Undetermined]** | The bounce reason received from the recipient domain Message Transfer Agent (MTA) could not be identified. | Ignored |
| **[!UICONTROL Too Large]** | The message bounced because it was too large for the recipient. [Retries](retries.md) will be performed: you can edit the message size and re-inject it for delivery. | Ignored |
| **[!UICONTROL Timeout]** | The message timed out, meaning it soft bounced and reached the message retry limit (3.5 days). | Ignored |
| **[!UICONTROL Admin Failure]** | The message was failed according to the policies configured by the sending system administrator. ///For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used. | Ignored |
| **[!UICONTROL Generic Bounce: No RCPT]** | No recipient could be determined for the message. | Ignored |
| **[!UICONTROL Generic Bounce]** | The message failed for unspecified reasons. | Ignored |
| **[!UICONTROL Mail Block]** | The message was blocked by the receiver (i.e. recipient MTA). | Ignored |
| **[!UICONTROL Spam Block]** | The message was blocked by the receiver as coming from a known spam source. It could be a sending IP block for example. | Ignored |
| **[!UICONTROL Spam Content]** | The message content was blocked by the receiver (recipient MTA) as spam. | Ignored |
| **[!UICONTROL Prohibited Attachment]** | The message was blocked by the receiver because it contained an attachment. | Ignored |
| **[!UICONTROL Auto-Reply]** | The message is an auto-reply/vacation mail. | Ignored |
| **[!UICONTROL Transient Failure]** | Message transmission has been temporarily delayed. | Ignored |
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list.-->

## Aggiungere manualmente indirizzi e domini {#add-addresses-and-domains}

Quando un messaggio non viene recapitato a un indirizzo e-mail, questo viene aggiunto automaticamente all’elenco di soppressione in base alla regola di soppressione o al conteggio dei messaggi non recapitati definiti.

Tuttavia, puoi anche compilare manualmente l’ [!DNL Journey Optimizer] elenco di soppressione per escludere specifici indirizzi e-mail e/o domini dall’invio.

Puoi aggiungere indirizzi e-mail o domini [uno alla volta](#add-one-address-or-domain), o [in modalità collettiva](#upload-csv-file) tramite un caricamento di file CSV.

A questo scopo, seleziona il pulsante **[!UICONTROL Add email or domain]** , quindi segui uno dei metodi seguenti.

![](../assets/suppression-list-add-email.png)

### Aggiungi un indirizzo o un dominio {#add-one-address-or-domain}

1. Seleziona l&#39;opzione **[!UICONTROL One by one]**.

   ![](../assets/suppression-list-add-email-address.png)

1. Scegli il tipo di indirizzo: **[!UICONTROL Email address]** o **[!UICONTROL Domain address]**.

1. Immetti l’indirizzo e-mail o il dominio da escludere dall’invio.

   >[!NOTE]
   >
   >Assicurati di inserire un indirizzo e-mail valido (ad esempio abc@company) o un dominio (ad esempio abc.company.com).

1. Se necessario, specifica un motivo.

1. Fai clic su **[!UICONTROL Submit]**.

### Caricare un file CSV {#upload-csv-file}

1. Seleziona l&#39;opzione **[!UICONTROL Upload CSV]**.

   ![](../assets/suppression-list-upload-csv.png)

1. Scarica il modello CSV da utilizzare, che include le colonne e il formato seguenti:

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```
   Puoi anche scaricare questo modello dalla vista principale **[!UICONTROL Suppression list]**.

   >[!CAUTION]
   >
   >Non modificare i nomi delle colonne nel modello CSV.
   >
   >La dimensione del file non deve superare 1 MB.

1. Compila il modello CSV con gli indirizzi e-mail e/o i domini che desideri aggiungere all’elenco di soppressione.

1. Al termine, trascina e rilascia il file CSV, quindi fai clic su **[!UICONTROL Upload file]**.

   ![](../assets/suppression-list-upload-file-button.png)

1. Fai clic su **[!UICONTROL Submit]**.

### Controlla lo stato dei caricamenti recenti {#recent-uploads}

Puoi controllare l’elenco dei file CSV più recenti caricati.

A questo scopo, nella visualizzazione **[!UICONTROL Suppression list]** fai clic sul pulsante **[!UICONTROL Recent uploads]** .

![](../assets/suppression-list-recent-uploads-button.png)

Vengono visualizzati gli ultimi caricamenti inviati e i relativi stati corrispondenti.

Se un report di errore è associato a un file, puoi scaricarlo per verificare gli errori rilevati.

![](../assets/suppression-list-recent-uploads-error.png)

Di seguito è riportato un esempio del tipo di voci che si possono trovare nel rapporto di errore:

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```



