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
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%

---

# Progettare una notifica push {#design-push-notification}

## Titolo e corpo {#push-title-body}

>[!CONTEXTUALHELP]
>id="ajo-message-push-compose"
>title="Personalizza la notifica push."
>abstract="Per comporre il messaggio, immetti il contenuto nei campi Titolo e Corpo. Per includere i token di personalizzazione, apri la finestra di dialogo di personalizzazione."

Per comporre il messaggio, fai clic su **[!UICONTROL Titolo]** e **[!UICONTROL Corpo]** campi. Utilizza l’editor di personalizzazione per definire i contenuti, personalizzare i dati e aggiungere contenuti dinamici. Ulteriori informazioni su [personalizzazione](../personalization/personalize.md) e [contenuto dinamico](../personalization/get-started-dynamic-content.md) nell’editor di personalizzazione.

Utilizza la sezione di anteprima del dispositivo per visualizzare come viene visualizzata la notifica push sui dispositivi iOS e Android.

## Comportamento al clic {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Informazioni sul comportamento al clic"
>abstract="Seleziona il comportamento quando un destinatario fa clic sul corpo della notifica push."

Puoi selezionare il comportamento quando un utente fa clic sul corpo della notifica push.

![](assets/title-body-push.png)

* Per aprire l’app, seleziona la **[!UICONTROL Apri app]** opzione. L’app associata alla notifica è definita nella sezione [superficie di canale](../configuration/channel-surfaces.md) (ossia predefinito per messaggi).
* Per reindirizzare l’utente a uno specifico contenuto all’interno di un’app, seleziona la **[!UICONTROL Deeplink]** opzione.  Il contenuto specifico può essere una visualizzazione specifica, una sezione particolare di una pagina o una determinata scheda. Una volta selezionata l’opzione, inserisci il collegamento diretto nel campo associato.
* Per reindirizzare l’utente a un URL esterno, utilizza **[!UICONTROL URL web]** opzione. Una volta selezionata l’opzione, immetti l’URL nel campo associato.

## Aggiungi file multimediali {#add-media-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-media"
>title="Aggiungere contenuti multimediali alla notifica push"
>abstract="Puoi aggiungere un’immagine, un video o un GIF visualizzati all’interno della notifica."

Nella versione iOS della notifica push, puoi aggiungere un’immagine, un video o un GIF visualizzati all’interno della notifica.

Nella versione Android, puoi aggiungere solo un’icona immagine e un’immagine per le notifiche espanse.

![](assets/push-config-add-media.png)

Sono disponibili due opzioni. Puoi eseguire le seguenti operazioni:

* Utilizza il **[!UICONTROL Aggiungi file multimediali]** per selezionare una risorsa in **[!DNL Adobe Experience Manager Assets]**.

  Scopri come utilizzare **[!DNL Adobe Experience Manager Assets]** in [questa pagina](../content-management/assets.md).

* Oppure immetti l’URL del file multimediale in **[!UICONTROL Aggiungi file multimediali]** campo. In tal caso, puoi aggiungere la personalizzazione all’URL.

Una volta aggiunto, il contenuto multimediale viene visualizzato a destra del corpo della notifica.

## Aggiungi pulsanti {#add-buttons-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-buttons"
>title="Aggiungi i pulsanti per consentire agli utenti di interagire con la notifica push."
>abstract="Questa sezione ti consente di aggiungere pulsanti di invito all’azione al messaggio. Per iOS, specifica un identificatore di categoria di notifica. Per Android, puoi includere testo personalizzato e destinazioni per ogni pulsante."

Crea una notifica actionable aggiungendo pulsanti al contenuto push.

Se lo schermo del dispositivo è bloccato, questi pulsanti non vengono visualizzati: solo il **Titolo** e **Messaggio** della notifica. Se il dispositivo è sbloccato, i destinatari visualizzeranno i pulsanti.

Nella versione Android, puoi aggiungere fino a tre pulsanti.

Nella versione di iOS, è specificato un identificatore di categoria di notifica. Le categorie di notifica devono essere preconfigurate nell’app iOS che definirà i pulsanti da visualizzare e le azioni da intraprendere. Consulta la [Documentazione di Apple](https://developer.apple.com/documentation/usernotifications/declaring_your_actionable_notification_types) per ulteriori dettagli.

1. Utilizza il **[!UICONTROL Pulsante Aggiungi]** per definire le impostazioni: l’etichetta e l’azione associata. Le azioni possibili sono le stesse di [comportamento al clic](#on-click-behavior).

1. Utilizza il **[!UICONTROL Espandi visualizzazione]** sotto l’immagine di anteprima centrale per visualizzare in anteprima i pulsanti personalizzati.

   ![](assets/push_buttons.png)

## Inviare una notifica invisibile all’utente {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Informazioni sulla notifica invisibile all’utente"
>abstract="Invia notifiche senza disturbare l’utente; le notifiche non vengono visualizzate nel centro notifiche o nella barra delle notifiche."

Una notifica push invisibile all’utente (o notifica in background) è un’istruzione nascosta distribuita all’applicazione. Viene utilizzato ad esempio per notificare all’applicazione la disponibilità di nuovo contenuto o per avviare un download in background.

Seleziona la **[!UICONTROL Notifica silenziosa]** opzione di notifica silenziosa della domanda: in questo caso, la notifica viene trasferita direttamente alla domanda. Sullo schermo del dispositivo non viene visualizzato alcun avviso.

Utilizza il **[!UICONTROL Dati personalizzati]** per aggiungere coppie chiave-valore.

## Dati personalizzati {#custom-data}

>[!CONTEXTUALHELP]
>id="ajo-message-push-custom"
>title="Configura dati personalizzati per la notifica push."
>abstract="Aggiungi variabili personalizzate al payload, a seconda della configurazione dell’app mobile."

In **[!UICONTROL Dati personalizzati]** , puoi aggiungere variabili personalizzate al payload, a seconda della configurazione dell’app mobile. Per ulteriori informazioni su come impostare le notifiche push in Adobe Experience Platform e Adobe Launch, consulta [questa sezione](push-gs.md)

## Opzioni avanzate {#advanced-options-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-advanced"
>title="Configura le opzioni avanzate per la notifica push."
>abstract="Questa sezione ti permette di migliorare la personalizzazione della notifica push."

Puoi configurare **[!UICONTROL Opzioni avanzate]** per la notifica push. I parametri disponibili sono elencati di seguito:

| Parametro | Descrizione |
|---------|---------|
| **[!UICONTROL Comprimibile]** (iOS/Android) | Un messaggio comprimibile è un messaggio che può essere sostituito da un nuovo messaggio se è diventato obsoleto. Un caso d’uso comune di messaggi comprimibili è rappresentato dai messaggi utilizzati per indicare a un’app mobile di sincronizzare i dati dal server. Un esempio potrebbe essere un’app sportiva che aggiorna gli utenti con il punteggio più recente. È rilevante solo il messaggio più recente. D’altra parte, con un messaggio non comprimibile, ogni messaggio è importante per l’app client e deve essere consegnato. |
| **[!UICONTROL Audio personalizzato]** (iOS/Android) | Il suono che il terminale mobile deve riprodurre quando viene ricevuta la notifica. L&#39;audio deve essere incluso nell&#39;app. |
| **[!UICONTROL Distintivi]** (iOS/Android) | Un badge viene utilizzato per visualizzare direttamente sull’icona dell’applicazione il numero di nuove informazioni non lette. <br/>Il valore del badge scompare non appena l’utente apre o legge il nuovo contenuto dall’applicazione. Quando viene ricevuta una notifica su un dispositivo, quest’ultimo può aggiornare o aggiungere un valore di badge per l’app correlata.<br/>Ad esempio, se memorizzi il numero di articoli non letti dei clienti, puoi sfruttare la personalizzazione per inviare a ciascun cliente il valore univoco del badge degli articoli non letti. Per ulteriori informazioni sulla personalizzazione, consulta [questa sezione](../personalization/personalize.md). |
| **[!UICONTROL Gruppo di notifica]**  (Solo iOS) | Associa un gruppo di notifiche alla notifica push.<br/>A partire da iOS 12, i gruppi di notifica consentono di consolidare i thread di messaggi e gli argomenti di notifica in ID thread. Ad esempio, un brand può inviare notifiche di marketing con un ID gruppo, mantenendo più notifiche di tipo operativo con uno o più ID diversi.<br/>Per illustrare questo, puoi avere groupID: 123 &quot;check out the new spring collection of sweaters&quot; e groupID: 456 &quot;your package was deliver&quot; gruppi di notifiche. In questo esempio, tutte le notifiche di consegna sono raggruppate in ID gruppo: 456. |
| **[!UICONTROL Canale di notifica]** (solo Android) | Associa un canale di notifica alla notifica push.<br/>A partire da Android 8.0 (livello API 26), tutte le notifiche devono essere assegnate a un canale per poter essere visualizzate. Per ulteriori informazioni, consulta [Documentazione per gli sviluppatori Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Aggiungi flag di disponibilità del contenuto]** (Solo iOS) | Invia il flag di contenuto disponibile nel payload push per garantire che l’app venga riattivata non appena riceve la notifica push, il che significa che l’app sarà in grado di accedere ai dati del payload.<br/> Questo funziona anche se l’app è in esecuzione in background e non richiede alcuna interazione da parte dell’utente (ad esempio, toccando la notifica push). Tuttavia, questo non si applica se l’app non è in esecuzione. Per ulteriori informazioni, consulta [Documentazione per gli sviluppatori di Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Aggiungi flag per contenuto mutabile]** (Solo iOS) | Invia il flag di contenuto mutabile nel payload push e consentirà la modifica del contenuto della notifica push da parte di un’estensione dell’applicazione del servizio di notifica fornita nell’SDK di iOS. Per ulteriori informazioni, consulta [Documentazione per gli sviluppatori di Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Puoi quindi sfruttare le estensioni dell’app mobile per modificare ulteriormente il contenuto o la presentazione delle notifiche push in arrivo inviate da [!DNL Journey Optimizer]. Ad esempio, gli utenti possono sfruttare questa opzione per decrittografare i dati, modificare il testo del corpo o del titolo di una notifica, aggiungere un identificatore di thread a una notifica e così via. |
| **[!UICONTROL Visibilità delle notifiche]** (solo Android) | Definisce la visibilità della notifica push. <br/><b>Privato</b> mostrerà la notifica su tutti gli schermi a chiave, ma nasconderà informazioni riservate o private su schermi a chiave protetti. <br/><b>Pubblico</b> mostrerà la notifica nella sua interezza su tutte le schermate di blocco. <br/><b>Segreto</b> non mostrerà alcuna parte della notifica su una schermata di blocco protetta. <br/>Per ulteriori informazioni, consulta [Documentazione per gli sviluppatori Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Priorità di notifica]** (solo Android) | Definisce l’importanza della notifica push da Bassa a Max. Questo determina il grado di &quot;intrusività&quot; della notifica push quando viene distribuita. Per ulteriori informazioni, consulta [Documentazione per gli sviluppatori Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Priorità di consegna]** (solo Android) | Imposta una priorità alta o normale per le notifiche push. Per ulteriori informazioni sulla priorità dei messaggi, consulta [Documentazione per sviluppatori Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
