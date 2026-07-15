---
title: Creare esperienze di canale personalizzate
description: Scopri come utilizzare un canale personalizzato in un percorso, una campagna o una campagna orchestrata in Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: User
level: Experienced
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 5%

---


# Creare esperienze di canale personalizzate {#create-custom-channel}

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

In [!DNL Journey Optimizer] è possibile inviare messaggi utilizzando canali personalizzati in campagne, percorsi e campagne orchestrate. Segui i passaggi seguenti per configurare la tua esperienza di canale personalizzata.

>[!NOTE]
>
>Prima di creare un’esperienza di canale personalizzata, accertati che l’amministratore abbia configurato un canale personalizzato. [Ulteriori informazioni](configure-custom-channel.md)

## Aggiungere un’azione personalizzata tramite un percorso o una campagna {#create-custom-channel-experience}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_channel"
>title="Azione canale personalizzata"
>abstract="Un’azione di canale personalizzata invia un messaggio ai profili quando raggiungono questo passaggio del percorso. L’etichetta identifica l’attività nell’area di lavoro del percorso e l’azione fa riferimento a una configurazione di canale personalizzata che definisce l’endpoint, il payload e le credenziali utilizzati per consegnare il messaggio. La sezione **Ottimizzazione** può includere esperimenti di contenuto o regole di targeting e la sezione **Timeout o errore** può definire un percorso alternativo se l&#39;azione non riesce."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="Introduzione ai canali personalizzati"



>[!BEGINTABS]

>[!TAB Aggiungere un canale personalizzato a un percorso]

I canali personalizzati vengono visualizzati nella sezione **[!UICONTROL Azioni]** della tavolozza dell&#39;area di lavoro del percorso, elencati in base al nome visualizzato e all&#39;icona personalizzata definiti nel Generatore di canali.

Per aggiungere un&#39;azione del canale personalizzata a un percorso:

1. [Crea un percorso](../building-journeys/journey-gs.md).

1. Avvia il percorso con un&#39;attività [Event](../building-journeys/general-events.md) o [Read Audience](../building-journeys/read-audience.md).

1. Trascina e rilascia un&#39;attività **[!UICONTROL Action]** dalla sezione **[!UICONTROL Actions]** della palette. Ulteriori informazioni sull&#39;[attività Azione](../building-journeys/journey-action.md).

1. Nel menu a discesa **[!UICONTROL Azione]**, seleziona il canale personalizzato che desideri utilizzare. I canali personalizzati sono elencati in base al nome e all’icona assegnati nel Channel Builder.

   ![](assets/custom_channel_journey_action.png){width="80%"}

1. Aggiungi un&#39;etichetta all&#39;azione, fai clic su **[!DNL Configure action]** nel pannello di destra e seleziona la **[!UICONTROL configurazione canale]** da utilizzare. [Scopri come creare una configurazione di canale personalizzata](custom-channel-configuration.md#create-channel-config)

1. Nella sezione **[!UICONTROL Messaggio]**, fai clic su **[!UICONTROL Modifica contenuto]** per aprire l&#39;editor payload e creare il messaggio. [Scopri come creare i contenuti](#author-content)

1. Completa il flusso di percorso aggiungendo i passaggi aggiuntivi necessari, quindi pubblica il percorso. [Ulteriori informazioni](../building-journeys/journey-gs.md)

>[!TAB Crea una campagna canale personalizzata]

Per utilizzare un canale personalizzato in una campagna:

1. [Crea una campagna](../campaigns/create-campaign.md).

1. Seleziona il tipo di campagna:

   * **[!UICONTROL Pianificato - Marketing]** - Eseguito immediatamente o in una data specificata. Progettato per i messaggi di marketing, configurato dall’interfaccia utente di.
   * **[!UICONTROL Attivato da API - Marketing/Transazionale]** - Eseguito tramite una chiamata API. Progettato per messaggi attivati da eventi (ad esempio, conferme d’ordine o reimpostazioni di password). [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md)

1. Completa la configurazione della campagna: proprietà della campagna, [pubblico](../audience/about-audiences.md) e [pianificazione](../campaigns/create-campaign.md#schedule).

1. Nella sezione **[!UICONTROL Azioni]**, seleziona il canale personalizzato dal selettore di canale. Tutti i canali personalizzati configurati nella sandbox vengono visualizzati insieme ai canali nativi.

   ![](assets/custom_channel_campaign_action.png){width="80%"}

1. Selezionare o creare la **[!UICONTROL configurazione canale]** da utilizzare. [Scopri come creare una configurazione di canale](custom-channel-configuration.md#create-channel-config)

1. Facoltativamente, abilita **[!UICONTROL Tracciamento azioni]** per tenere traccia automaticamente dei collegamenti inclusi nel payload del messaggio (richiede un sottodominio configurato per i canali personalizzati). [Scopri come delegare un sottodominio per i canali personalizzati](custom-channel-subdomains.md#subdomain-delegation)

1. Nella sezione **[!UICONTROL Ottimizzazione]** è possibile:

   * **[!UICONTROL Crea regole di targeting]** per inviare messaggi diversi a segmenti diversi del pubblico. [Ulteriori informazioni](../campaigns/create-campaign.md#targeting)
   * Fai clic su **[!UICONTROL Crea esperimento]** per eseguire test A/B sui messaggi del canale personalizzati. [Ulteriori informazioni](../campaigns/create-campaign.md#content-experiment)

1. Fai clic su **[!UICONTROL Modifica contenuto]** per aprire l&#39;editor payload e creare il messaggio. [Scopri come creare i contenuti](#author-content)

1. Rivedi e attiva la campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

<!--
>[!TAB Add a custom channel to an orchestrated campaign]

Custom channels appear in the channel selection list in the orchestrated Campaigns canvas, below the native channels, with their custom icon and display name.

To add a custom channel in an orchestrated campaign:

1. Open or create an orchestrated campaign.

1. In the canvas, add a channel action node and select your custom channel from the list.

1. Select the **[!UICONTROL Channel configuration]** to use. Ensure the configuration includes the **[!UICONTROL Execution details]** section required for orchestrated campaigns.

1. Click **[!UICONTROL Edit content]** to open the payload editor and author your message. [Learn how to author content](#author-content)
-->

>[!ENDTABS]

## Creare contenuti di canale personalizzati {#author-content}

L’editor di contenuto riflette la struttura del payload definita durante la configurazione del canale personalizzato. Fai clic su **[!UICONTROL Modifica codice]** per aprire l&#39;editor payload e immettere il contenuto del messaggio.

![](assets/custom_channel_payload_editor.png){width="80%"}

Vengono visualizzati i campi che puoi creare e personalizzare. Puoi sfruttare l&#39;editor di personalizzazione [!DNL Journey Optimizer] con tutte le sue funzionalità di personalizzazione e authoring. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

>[!NOTE]
>
>Sono supportati solo i payload JSON. Se il payload del canale personalizzato non è JSON, puoi utilizzare un wrapper JSON per incapsulare il contenuto. Ad esempio, se il payload è XML, puoi racchiuderlo in un oggetto JSON come segue:
>
>```json
>{
>   "payload": "<xml>...</xml>"
>}
>```

### Personalizzare il payload {#personalize}

Le funzionalità di personalizzazione completa di [!DNL Journey Optimizer] sono disponibili nell&#39;editor di payload:

* **Attributi profilo** - Inserisci eventuali attributi di profilo XDM, ad esempio `{{profile.person.name.firstName}}` o un&#39;identità personalizzata come un ID utente della piattaforma di messaggistica memorizzato in uno spazio dei nomi personalizzato.
* **Attributi contestuali** - Utilizza attributi evento di percorso o dati contestuali della campagna risolti al momento dell&#39;invio.
* **Funzioni helper** - Formatta i valori utilizzando le funzioni predefinite stringa, data o aritmetica. [Ulteriori informazioni](../personalization/functions/helpers.md)
* **Frammenti di espressione** - Riutilizza la logica di personalizzazione condivisa su più canali e campagne. [Ulteriori informazioni](../content-management/customizable-fragments.md)

>[!CAUTION]
>
>Al momento non è presente alcuna convalida del payload al momento dell’authoring. Puoi usare la funzione **[!UICONTROL Simula contenuto]** per verificare che il payload sia in formato JSON corretto e che tutte le espressioni di personalizzazione vengano risolte correttamente per i profili di test. [Ulteriori informazioni](test-custom-channel.md#simulate-content)

### Esempio di payload {#example-payload}

L&#39;esempio seguente mostra un payload JSON con personalizzazione del profilo per un canale di messaggistica personalizzato<!--(to be replaced with a meaningful realistic example)-->:

```json
{
  "recipient_id": "{{profile.mobilePhone.number}}",
  "message_text": "Hello {{profile.person.name.firstName}}, your order {{context.journey.events.0.commerce.order.purchaseID}} has been confirmed.",
  "channel": "my-custom-channel",
  "image": {
    "id": "{{profile.preferences.imageId | default('default-image-001')}}"
  }
}
```

### Tracciare i collegamenti nel payload {#track-links}

Per includere un collegamento tracciato nel payload del canale personalizzato, in modo che i clic vengano tracciati automaticamente e visibili nelle dashboard di reporting del canale, racchiudi l’URL utilizzando la seguente sintassi a manubrio:

```
{{url trackedUrl='' originalUrl='https://example.com/' type='TRACKED'}}
```

* `originalUrl` - URL di destinazione a cui si desidera reindirizzare il destinatario.
* `trackedUrl` - Lascia vuoto; [!DNL Journey Optimizer] lo popola automaticamente con l&#39;URL di reindirizzamento abilitato per il tracciamento al momento dell&#39;invio.
* `type` - Deve essere impostato su `TRACKED`.

>[!NOTE]
>
>Il tracciamento dei collegamenti richiede un sottodominio configurato per i canali personalizzati. [Scopri come delegare un sottodominio per i canali personalizzati](custom-channel-subdomains.md#subdomain-delegation)

**Esempio - collegamento tracciato in un payload LINE:**

```json
{
  "to": "{{profile.mobilePhone.number}}",
  "messages": [
    {
      "type": "text",
      "text": "Hello! Check out our latest offer: {{url trackedUrl='' originalUrl='https://example.com/' type='TRACKED'}}"
    }
  ]
}
```

<!--
### Strict JSON mode {#strict-json}

The editor supports a **[!UICONTROL Strict JSON]** toggle:

* **Strict JSON: Off (default)** – The editor accepts any payload content, including personalization helpers and functions that may temporarily produce non-JSON syntax. A warning is displayed at the **Review to Activate** step if the payload is not well-formed JSON, prompting you to simulate and proof before publishing.
* **Strict JSON: On** – The editor validates that the payload is well-formed JSON as you type. At the **Review to Activate** step, [!DNL Journey Optimizer] validates the payload against the channel schema and flags missing required fields or type mismatches as errors that must be resolved before activation.
-->

## Attiva la tua esperienza di canale personalizzata {#activate}

>[!IMPORTANT]
>
>Visualizza l’anteprima e verifica il payload del canale personalizzato prima dell’attivazione. [Scopri come](test-custom-channel.md)
>
>Se la campagna o il percorso è soggetto a una policy di approvazione, devi richiedere l’approvazione prima dell’attivazione. [Ulteriori informazioni](../test-approve/gs-approval.md)

* **Da un percorso** - Fai clic su **[!UICONTROL Pubblica]** in alto a destra. Il percorso entra in funzione e inizia a chiamare l’endpoint esterno per i profili idonei.
* **Da una campagna** - Fai clic su **[!UICONTROL Controlla per attivare]**, controlla le impostazioni, quindi fai clic su **[!UICONTROL Attiva]**. La campagna accetta lo stato **[!UICONTROL Live]** (o **[!UICONTROL Pianificato]** se è stata definita una data di inizio futura).
