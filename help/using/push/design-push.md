---
solution: Journey Optimizer
product: journey optimizer
title: Progettare una notifica push
description: Scopri come progettare una notifica push in Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: 36056208cd1e435c4801bd178bdc5f2d74068dc5
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 17%

---

# Progettare una notifica push {#design-push-notification}

## Titolo e corpo {#push-title-body}

>[!CONTEXTUALHELP]
>id="ajo-message-push-compose"
>title="Personalizzare la notifica push."
>abstract="Per comporre il messaggio, immetti il contenuto nei campi **Titolo** e **Corpo**. Per includere i token di personalizzazione, apri la finestra di dialogo di personalizzazione."

Per comporre il messaggio, fai clic sui campi **[!UICONTROL Titolo]** e **[!UICONTROL Corpo]**. Utilizza l’editor di personalizzazione per definire i contenuti, personalizzare i dati e aggiungere contenuti dinamici. Ulteriori informazioni sulla [personalizzazione](../personalization/personalize.md) e sul [contenuto dinamico](../personalization/get-started-dynamic-content.md) nell&#39;editor di personalizzazione.

Utilizza la sezione anteprima dispositivo per visualizzare come viene visualizzata la notifica push sui dispositivi iOS e Android.

## Comportamento al clic {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Informazioni sul comportamento del clic"
>abstract="Seleziona il comportamento che si verifica quando un destinatario fa clic sul corpo della notifica push."

Puoi selezionare il comportamento quando un utente fa clic sul corpo della notifica push.

![](assets/title-body-push.png)

* Per aprire l&#39;app, selezionare l&#39;opzione **[!UICONTROL Apri app]**. L&#39;app associata alla notifica è definita nella [configurazione canale](../configuration/channel-surfaces.md) (ossia il predefinito per messaggi).
* Per reindirizzare l&#39;utente a un contenuto specifico all&#39;interno di un&#39;app, selezionare l&#39;opzione **[!UICONTROL Deeplink]**.  Il contenuto specifico può essere una visualizzazione specifica, una sezione particolare di una pagina o una determinata scheda. Una volta selezionata l’opzione, inserisci il collegamento diretto nel campo associato.
* Per reindirizzare l&#39;utente a un URL esterno, utilizzare l&#39;opzione **[!UICONTROL URL Web]**. Una volta selezionata l’opzione, immetti l’URL nel campo associato.

## Aggiungere file multimediali {#add-media-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-media"
>title="Aggiungere contenuti multimediali alla notifica push"
>abstract="Puoi aggiungere un’immagine, un video o una GIF da visualizzare all’interno della notifica."

Nella versione iOS della notifica push, puoi aggiungere un’immagine, un video o un GIF visualizzati all’interno della notifica.

Nella versione di Android, puoi aggiungere solo un’icona immagine e un’immagine per le notifiche espanse.

![](assets/push-config-add-media.png)

Sono disponibili due opzioni. Puoi eseguire le seguenti operazioni:

* Utilizza il pulsante **[!UICONTROL Aggiungi file multimediali]** per selezionare una risorsa in **[!DNL Adobe Experience Manager Assets]**.

  Scopri come utilizzare **[!DNL Adobe Experience Manager Assets]** in [questa pagina](../integrations/assets.md).

* In alternativa, immettere l&#39;URL del supporto nel campo **[!UICONTROL Aggiungi supporto]**. In tal caso, puoi aggiungere la personalizzazione all’URL.

Una volta aggiunto, il contenuto multimediale viene visualizzato a destra del corpo della notifica.

## Aggiungere pulsanti {#add-buttons-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-buttons"
>title="Aggiungi i pulsanti per consentire agli utenti di interagire con la notifica push."
>abstract="Da questa sezione, aggiungi i pulsanti di invito all’azione al messaggio. Per Apple iOS, specifica un identificatore di categoria di notifica. Per Google Android, per ciascun pulsante puoi specificare il testo personalizzato e le destinazioni."

Crea una notifica actionable aggiungendo pulsanti al contenuto push.

Se la schermata del dispositivo è bloccata, questi pulsanti non vengono visualizzati: solo allora sono visibili il **Titolo** e il **Messaggio** della notifica. Se il dispositivo è sbloccato, i destinatari visualizzeranno i pulsanti.

Nella versione di Android, puoi aggiungere fino a tre pulsanti.

Nella versione di iOS, è specificato un identificatore di categoria di notifica. Le categorie di notifica devono essere preconfigurate nell’app iOS che definirà i pulsanti da visualizzare e le azioni da intraprendere. Per ulteriori dettagli, consulta la [documentazione di Apple](https://developer.apple.com/documentation/usernotifications/declaring_your_actionable_notification_types).

1. Utilizza il **[!UICONTROL pulsante Aggiungi]** per definire le impostazioni: l&#39;etichetta e l&#39;azione associata. Le azioni possibili sono le stesse del [comportamento al clic](#on-click-behavior).

1. Utilizza l&#39;icona **[!UICONTROL Espandi visualizzazione]** sotto l&#39;immagine di anteprima centrale per visualizzare l&#39;anteprima dei pulsanti personalizzati.

   ![](assets/push_buttons.png)

## Inviare una notifica silenziosa {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Informazioni sulla notifica silenziosa"
>abstract="Invia notifiche senza disturbare l’utente: le notifiche non verranno visualizzate nel centro notifiche o nella barra delle notifiche."

Una notifica push invisibile all’utente (o notifica in background) è un’istruzione nascosta distribuita all’applicazione. Viene utilizzato ad esempio per notificare all’applicazione la disponibilità di nuovo contenuto o per avviare un download in background.

Selezionare l&#39;opzione **[!UICONTROL Notifica invisibile all&#39;utente]** per inviare una notifica invisibile all&#39;utente: in questo caso, la notifica viene trasferita direttamente all&#39;applicazione. Sullo schermo del dispositivo non viene visualizzato alcun avviso.

Utilizza la sezione **[!UICONTROL Dati personalizzati]** per aggiungere coppie chiave-valore.

## Dati personalizzati {#custom-data}

>[!CONTEXTUALHELP]
>id="ajo-message-push-custom"
>title="Configura i dati personalizzati per la notifica push."
>abstract="Aggiungi variabili personalizzate al payload, a seconda della configurazione dell’app mobile."

Nella sezione **[!UICONTROL Dati personalizzati]** puoi aggiungere variabili personalizzate al payload, a seconda della configurazione dell&#39;app mobile. Per ulteriori informazioni su come impostare le notifiche push in Adobe Experience Platform, consulta [questa sezione](push-gs.md)

## Opzioni avanzate {#advanced-options-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-advanced"
>title="Configura le opzioni avanzate per la notifica push."
>abstract="Questa sezione ti permette di migliorare la personalizzazione della notifica push."

Puoi configurare **[!UICONTROL Opzioni avanzate]** per la notifica push. I parametri disponibili sono elencati di seguito:

| Parametro | Descrizione |
|---------|---------|
| **[!UICONTROL Comprimibile]** (iOS/Android) | Un messaggio comprimibile è un messaggio che può essere sostituito da un nuovo messaggio se è diventato obsoleto. Un caso d’uso comune di messaggi comprimibili è rappresentato dai messaggi utilizzati per indicare a un’app mobile di sincronizzare i dati dal server. Un esempio potrebbe essere un’app sportiva che aggiorna gli utenti con il punteggio più recente. È rilevante solo il messaggio più recente. D’altra parte, con i messaggi non comprimibili, ogni messaggio è importante per l’app client e deve essere consegnato. |
| **[!UICONTROL Audio personalizzato]** (iOS/Android) | Il suono che il terminale mobile deve riprodurre quando viene ricevuta la notifica. L&#39;audio deve essere incluso nell&#39;app. |
| **[!UICONTROL Distintivi]** (iOS/Android) | Un badge viene utilizzato per visualizzare direttamente sull’icona dell’applicazione il numero di nuove informazioni non lette. <br/>Il valore del badge scompare non appena l&#39;utente apre o legge il nuovo contenuto dall&#39;applicazione. Quando viene ricevuta una notifica su un dispositivo, quest’ultimo può aggiornare o aggiungere un valore di badge per l’app correlata.<br/>Ad esempio, se memorizzi il numero di articoli non letti dei tuoi clienti, puoi sfruttare la personalizzazione per inviare il valore univoco del badge degli articoli non letti per ciascun cliente. Per ulteriori informazioni sulla personalizzazione, consulta [questa sezione](../personalization/personalize.md). |
| **[!UICONTROL Gruppo di notifica]** (solo iOS) | Associa un gruppo di notifiche alla notifica push.<br/>A partire da iOS 12, i gruppi di notifica consentono di consolidare i thread di messaggi e gli argomenti delle notifiche in ID thread. Ad esempio, un brand può inviare notifiche di marketing con un ID gruppo, mantenendo più notifiche di tipo operativo con uno o più ID diversi.<br/>Per illustrare questa situazione, è possibile avere i gruppi di notifica groupID: 123 &quot;check out the new spring collection of sweaters&quot; e groupID: 456 &quot;your package was deliver&quot;. In questo esempio, tutte le notifiche di consegna sono raggruppate in ID gruppo: 456. |
| **[!UICONTROL Canale di notifica]** (solo Android) | Associa un canale di notifica alla notifica push.<br/>A partire da Android 8.0 (livello API 26), tutte le notifiche devono essere assegnate a un canale per poter essere visualizzate. Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Aggiungi flag di disponibilità del contenuto]** (solo iOS) | Invia il flag di contenuto disponibile nel payload push per garantire che l’app venga riattivata non appena riceve la notifica push, il che significa che l’app sarà in grado di accedere ai dati del payload.<br/> Questo funziona anche se l&#39;app è in esecuzione in background e non richiede alcuna interazione da parte dell&#39;utente (ad esempio, toccando la notifica push). Tuttavia, questo non si applica se l’app non è in esecuzione. Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Aggiungi flag di contenuto mutabile]** (solo iOS) | Invia il flag di contenuto mutabile nel payload push e consentirà la modifica del contenuto della notifica push da parte di un’estensione dell’applicazione del servizio di notifica fornita in iOS SDK. Per ulteriori informazioni, consulta la [documentazione per sviluppatori di Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Puoi quindi sfruttare le estensioni dell&#39;app mobile per modificare ulteriormente il contenuto o la presentazione delle notifiche push in arrivo inviate da [!DNL Journey Optimizer]. Ad esempio, gli utenti possono sfruttare questa opzione per decrittografare i dati, modificare il testo del corpo o del titolo di una notifica, aggiungere un identificatore di thread a una notifica e così via. |
| **[!UICONTROL Aggiungi scadenza push]** (solo iOS) | Scegli la **data e ora** della scadenza push. In iOS, la scadenza delle notifiche viene applicata come arresto rigido, ovvero qualsiasi messaggio che raggiunge il servizio APNS (Apple Push Notification Service) dopo la scadenza non viene consegnato, garantendo ai clienti di non ricevere mai notifiche obsolete o irrilevanti. Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Apple](https://developer.apple.com/documentation/usernotifications/sending-notification-requests-to-apns). |
| **[!UICONTROL Visibilità notifica]** (solo Android) | Definisce la visibilità della notifica push. <br/><b>Privato</b> mostrerà la notifica su tutte le schermate di blocco, ma nasconderà informazioni riservate o private su schermate di blocco sicure. <br/><b>Pubblico</b> mostrerà la notifica nella sua interezza su tutte le schermate di blocco. <br/><b>Segreto</b> non rivelerà alcuna parte della notifica in una schermata di blocco protetta. <br/>Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Priorità notifica]** (solo Android) | Definisce l’importanza della notifica push da Bassa a Max. Questo determina il grado di &quot;intrusività&quot; della notifica push quando viene distribuita. Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Priorità di consegna]** (solo Android) | Imposta una priorità alta o normale per le notifiche push. Per ulteriori informazioni sulla priorità dei messaggi, consulta la [documentazione per gli sviluppatori di Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
| **[!UICONTROL Durata]** (solo Android) | Imposta il numero di secondi dopo i quali il messaggio scadrà. In Android, la scadenza viene trattata come una finestra di consegna: Firebase Cloud Messaging (FCM) converte il tempo di scadenza in un valore TTL (time-to-live) che inizia al momento della ricezione del messaggio, il che significa che le campagne non consegnate possono essere inviate più tardi del previsto o anche al di fuori dell’intervallo temporale desiderato. Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Android](https://firebase.google.com/docs/cloud-messaging/concept-options#ttl). |
