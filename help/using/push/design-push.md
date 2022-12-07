---
solution: Journey Optimizer
product: journey optimizer
title: Progettazione di una notifica push
description: Scopri come progettare una notifica push in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 10%

---

# Progettazione di una notifica push {#design-push-notification}

## Titolo e corpo {#push-title-body}

Per comporre il messaggio, fai clic sul pulsante **[!UICONTROL Titolo]** e **[!UICONTROL Corpo]** campi. Utilizza l’editor espressioni per definire il contenuto, personalizzare i dati e aggiungere contenuto dinamico. Ulteriori informazioni [personalizzazione](../personalization/personalize.md) e [contenuto dinamico](../personalization/get-started-dynamic-content.md) nell’editor espressioni.

Utilizza la sezione di anteprima del dispositivo per visualizzare il modo in cui la notifica push viene visualizzata sui dispositivi iOS e Android.

## Comportamento del clic {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Informazioni sul comportamento del clic"
>abstract="Seleziona il comportamento quando un destinatario fa clic sul corpo della notifica push."

Puoi selezionare il comportamento quando un utente fa clic sul corpo della notifica push.

![](assets/title-body-push.png)

* Per aprire l’app, seleziona la **[!UICONTROL Apri app]** opzione . L’app associata alla notifica è definita nella [superficie del canale](../configuration/channel-surfaces.md) (ovvero predefinito per i messaggi).
* Per reindirizzare l’utente a uno specifico contenuto di un’app, seleziona la **[!UICONTROL Deeplink]** opzione .  Il contenuto specifico può essere una visualizzazione specifica, una particolare sezione di una pagina o una determinata scheda. Una volta selezionata l’opzione , immetti il collegamento diretto nel campo associato.
* Per reindirizzare l’utente a un URL esterno, utilizza il **[!UICONTROL URL web]** opzione . Una volta selezionata l’opzione , immetti l’URL nel campo associato.

## Aggiungi file multimediali {#add-media-push}

Nella versione iOS della notifica push, puoi aggiungere un’immagine, un video o un GIF che verrà visualizzato all’interno della notifica.

Nella versione Android, puoi aggiungere solo un’icona immagine e un’immagine per le notifiche estese.

![](assets/push-config-add-media.png)

Sono disponibili due opzioni. Puoi eseguire le seguenti operazioni:

* Utilizza la **[!UICONTROL Aggiungi file multimediali]** per selezionare una risorsa in **[!DNL Adobe Experience Manager Assets Essentials]**.

   Scopri come utilizzare **[!DNL Adobe Experience Manager Assets Essentials]** in [questa pagina](../email/assets-essentials.md).

* Oppure immetti l&#39;URL del contenuto multimediale nel **[!UICONTROL Aggiungi file multimediali]** campo . In tal caso, puoi aggiungere la personalizzazione all’URL.

Una volta aggiunto, il contenuto multimediale viene visualizzato a destra del corpo della notifica.

## Aggiungi pulsanti {#add-buttons-push}

Crea una notifica actionable aggiungendo pulsanti al contenuto push.

Se la schermata del dispositivo è bloccata, questi pulsanti non vengono visualizzati: solo il **Titolo** e **Messaggio** della notifica sono visibili. Se il dispositivo è sbloccato, i destinatari visualizzeranno i pulsanti.

Nella versione iOS è possibile aggiungere fino a quattro pulsanti. Nella versione Android, puoi aggiungere fino a tre pulsanti.

>[!NOTE]
>
>Per iOS, utilizza il **[!UICONTROL categoria iOS]** campo per associare azioni a una categoria di notifica.

1. Utilizza la **[!UICONTROL Pulsante Aggiungi]** per definire le impostazioni: l’etichetta e l’azione associata. Le azioni possibili sono le stesse di [comportamento con clic](#on-click-behavior).

1. Utilizza la **[!UICONTROL Espandi visualizzazione]** sotto l&#39;immagine di anteprima centrale per visualizzare in anteprima i pulsanti personalizzati.

![](assets/push_buttons.png)

## Invia una notifica silenziosa {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Informazioni sulla notifica silenziosa"
>abstract="Invia notifiche senza disturbare l&#39;utente, le notifiche non vengono visualizzate nel centro notifiche o nella barra delle notifiche."

Una notifica push silenziosa (o notifica in background) è un&#39;istruzione nascosta inviata all&#39;applicazione. Viene utilizzato, ad esempio, per notificare all’applicazione la disponibilità di nuovi contenuti o per avviare un download in background.

Seleziona la **[!UICONTROL Notifica silenziosa]** opzione per notificare silenziosamente la domanda: in questo caso, la notifica viene trasferita direttamente all&#39;applicazione. Sullo schermo del dispositivo non viene visualizzato alcun avviso.

Utilizza la **[!UICONTROL Dati personalizzati]** per aggiungere coppie chiave-valore.

## Dati personalizzati

In **[!UICONTROL Dati personalizzati]** Puoi aggiungere variabili personalizzate al payload, a seconda della configurazione dell’app mobile. Per ulteriori informazioni su come impostare le notifiche push in Adobe Experience Platform e Adobe Launch, consulta [questa sezione](push-gs.md)

## Opzioni avanzate {#advanced-options-push}

Puoi configurare **[!UICONTROL Opzioni avanzate]** per la notifica push. I parametri disponibili sono elencati di seguito:

| Parametro | Descrizione |
|---------|---------|
| **[!UICONTROL Comprimibile]** (iOS / Android) | Un messaggio comprimibile è un messaggio che può essere sostituito da un nuovo messaggio se non è più aggiornato. Un caso d’uso comune di messaggi comprimibili è rappresentato dai messaggi utilizzati per indicare a un’app mobile di sincronizzare i dati dal server. Ad esempio, un’app sportiva che aggiorna gli utenti con il punteggio più recente. Solo il messaggio più recente è rilevante. D’altro canto, con un messaggio non comprimibile, ogni messaggio è importante per l’app client e deve essere consegnato. |
| **[!UICONTROL Audio personalizzato]** (iOS / Android) | Il suono che deve essere riprodotto dal terminale mobile quando viene ricevuta la notifica. L&#39;audio deve essere incluso nell&#39;app. |
| **[!UICONTROL Badge]** (iOS / Android) | Un badge viene utilizzato per visualizzare direttamente sull’icona dell’applicazione il numero di nuove informazioni non lette. <br/>Il valore del badge scompare non appena l’utente apre o legge il nuovo contenuto dall’applicazione. Quando un dispositivo riceve una notifica, quest’ultima può aggiornare o aggiungere un valore di badge per l’app correlata.<br/>Ad esempio, se archivi il numero di articoli non letti dei clienti, puoi sfruttare la personalizzazione per inviare il valore univoco del badge degli articoli non letti per ciascun cliente. Per ulteriori personalizzazioni, consulta [questa sezione](../personalization/personalize.md). |
| **[!UICONTROL Gruppo di notifica]**  (Solo iOS) | Associa un gruppo di notifiche alla notifica push.<br/>A partire da iOS 12, i gruppi di notifica ti consentono di consolidare i thread di messaggio e gli argomenti relativi alle notifiche in ID thread. Ad esempio, un marchio potrebbe inviare notifiche di marketing sotto un ID gruppo, mantenendo al tempo stesso più notifiche di tipo operativo sotto uno o più ID diversi.<br/>A questo scopo, puoi disporre di groupID: 123 &quot;check out the new spring collection of sweaters&quot; e groupID: 456 Gruppi di notifica &quot;il tuo pacchetto è stato consegnato&quot;. In questo esempio, tutte le notifiche di consegna sarebbero raggruppate in ID gruppo: 456 |
| **[!UICONTROL Canale di notifica]** (Solo Android) | Associa un canale di notifica alla notifica push.<br/>A partire da Android 8.0 (livello API 26), tutte le notifiche devono essere assegnate a un canale per essere visualizzate. Per ulteriori informazioni, consulta la sezione [Documentazione per gli sviluppatori Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Aggiungi flag di disponibilità del contenuto]** (Solo iOS) | Invia il flag di contenuto disponibile nel payload push per garantire che l’app venga riattivata non appena riceve la notifica push, il che significa che l’app sarà in grado di accedere ai dati del payload.<br/> Questo funziona anche se l’app è in esecuzione in background e non richiede alcuna interazione da parte dell’utente (ad esempio, toccando la notifica push). Tuttavia, questo non si applica se l’app non è in esecuzione. Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Aggiungi flag di contenuto variabile]** (Solo iOS) | Invia il flag di contenuto variabile nel payload push e consente la modifica del contenuto della notifica push da parte di un’estensione dell’applicazione del servizio di notifica fornita nell’SDK di iOS. Per ulteriori informazioni, consulta la [documentazione per sviluppatori di Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Puoi quindi sfruttare le estensioni dell’app mobile per modificare ulteriormente il contenuto o la presentazione delle notifiche push in arrivo inviate da [!DNL Journey Optimizer]. Ad esempio, gli utenti possono sfruttare questa opzione per decrittografare i dati, modificare il testo del corpo o del titolo di una notifica, aggiungere un identificatore di thread a una notifica e così via. |
| **[!UICONTROL Visibilità delle notifiche]** (Solo Android) | Definisce la visibilità della notifica push. <br/><b>Privato</b> mostrerà la notifica su tutti gli schermi, ma nasconderà informazioni sensibili o private su serrature sicure. <br/><b>Pubblico</b> mostrerà la notifica nella sua interezza su tutti gli schermi di blocco. <br/><b>Segreto</b> non rivelerà alcuna parte della notifica su un blocco di sicurezza. <br/>Per ulteriori informazioni, consulta la [Documentazione per gli sviluppatori Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Priorità di notifica]** (Solo Android) | Definisce l’importanza della notifica push da Bassa a Max. Questo determina quanto sarà &quot;intrusiva&quot; la notifica push quando viene consegnata. Per ulteriori informazioni, consulta la sezione [Documentazione per gli sviluppatori Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Priorità di consegna]** (Solo Android) | Imposta una priorità alta o normale per le notifiche push. Per ulteriori informazioni sulla priorità dei messaggi, consulta la [documentazione per gli sviluppatori di Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |


