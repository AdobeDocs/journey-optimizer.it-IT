---
solution: Journey Optimizer
product: journey optimizer
title: Configurazione della notifica push
description: Scopri come configurare il tuo ambiente per l’invio di notifiche push con Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7099d44e-5d5d-4eef-9477-f68f4eaa1983
source-git-commit: c0358b039f038705aa67e6b779b6b8da228a603b
workflow-type: tm+mt
source-wordcount: '1536'
ht-degree: 3%

---

# Configurare il canale per notifiche push {#push-notification-configuration}

[!DNL Journey Optimizer] consente di creare i percorsi e inviare messaggi a un pubblico di destinazione. Prima di iniziare a inviare notifiche push con [!DNL Journey Optimizer], è necessario assicurarsi che le configurazioni e le integrazioni siano presenti nell’app mobile e per i tag in Adobe Experience Platform. Per comprendere il flusso di dati delle notifiche push in [!DNL Adobe Journey Optimizer] fare riferimento a [questa pagina](push-gs.md).

<!--
>[!AVAILABILITY]
>
>The new **mobile onboarding quick start workflow** is now available. Use this new product feature to rapidly configure the Mobile SDK to start collecting and validating mobile event data, and to send mobile push notifications. This capability is accessible via the Data Collection home page as a public beta. [Learn more](mobile-onboarding-wf.md)
>
-->

## Prima di iniziare {#before-starting}

<!--
### Check provisioning

Your Adobe Experience Platform account must be provisioned to contain following schemas and datasets for push notification data flow to function correctly:

| Schema <br>Dataset                                                                       | Group of fields                                                                                                                                                                         | Operation                                                |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| CJM Push Profile Schema <br>CJM Push Profile Dataset                                     | Push Notification Details<br>Adobe CJM ExperienceEvent - Message Profile Details<br>Adobe CJM ExperienceEvent - Message Execution Details<br>Application Details<br>Environment Details | Register Push Token                                      |
| CJM Push Tracking Experience Event Schema<br>CJM Push Tracking Experience Event Dataset | Push Notification Tracking                                                                                                                                                              | Track interactions and provide data for the reporting UI |
-->

### Impostare le autorizzazioni {#setup-permissions}

Prima di creare un’app mobile, è necessario assicurarsi di disporre o assegnare le autorizzazioni utente corrette per i tag in Adobe Experience Platform. Ulteriori informazioni in [Documentazione sui tag](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}.

>[!CAUTION]
>
>La configurazione push deve essere eseguita da un utente esperto. A seconda del modello di implementazione e degli utenti tipo coinvolti in questa implementazione, potrebbe essere necessario assegnare l’intero set di autorizzazioni a un singolo profilo di prodotto o condividere le autorizzazioni tra lo sviluppatore dell’app e l’ **Adobe Journey Optimizer** amministratore. Ulteriori informazioni **Tag** autorizzazioni in [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}.

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

Per assegnare **Proprietà** e **Azienda** diritti, segui i passaggi seguenti:

1. Accedere al **[!DNL Admin Console]**.

1. Da **[!UICONTROL Prodotti]** seleziona la scheda **[!UICONTROL Raccolta dati Adobe Experience Platform]** il Card.

   ![](assets/push_product_1.png)

1. Seleziona un **[!UICONTROL Profilo prodotto]** o creane uno nuovo con il **[!UICONTROL Nuovo profilo]** pulsante . Scopri come creare un nuovo **[!UICONTROL Nuovo profilo]** in [Documentazione di Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui){target="_blank"}.

1. Da **[!UICONTROL Autorizzazioni]** scheda , seleziona **[!UICONTROL Diritti di proprietà]**.

   ![](assets/push_product_2.png)

1. Fai clic su **[!UICONTROL Aggiungi tutto]**. Questo aggiungerà il seguente diritto al tuo profilo di prodotto:
   * **[!UICONTROL Approvazione]**
   * **[!UICONTROL Sviluppa]**
   * **[!UICONTROL Gestire gli ambienti]**
   * **[!UICONTROL Gestire le estensioni]**
   * **[!UICONTROL Pubblica]**

   Queste autorizzazioni sono necessarie per installare e pubblicare l&#39;estensione Adobe Journey Optimizer e pubblicare la proprietà dell&#39;app nell&#39;SDK di Adobe Experience Platform Mobile.

1. Quindi, seleziona **[!UICONTROL Diritti aziendali]** nel menu a sinistra.

   ![](assets/push_product_4.png)

1. Aggiungi i seguenti diritti:

   * **[!UICONTROL Gestire le configurazioni dell’app]**
   * **[!UICONTROL Gestisci proprietà]**

   Queste autorizzazioni sono necessarie affinché lo sviluppatore di app mobili possa impostare le credenziali push in **Raccolta dati Adobe Experience Platform** e definisci le superfici del canale di notifica push (ad esempio i predefiniti per messaggi) in **Adobe Journey Optimizer**.

   ![](assets/push_product_5.png)

1. Fai clic su **[!UICONTROL Salva]**.

Per assegnare questo **[!UICONTROL Profilo di prodotto]** per gli utenti, segui i passaggi seguenti:

1. Accedere al **[!DNL Admin Console]**.

1. Da **[!UICONTROL Prodotti]** seleziona la scheda **[!UICONTROL Raccolta dati Adobe Experience Platform]** il Card.

1. Seleziona la configurazione **[!UICONTROL Profilo di prodotto]**.

1. Da **[!UICONTROL Utenti]** scheda , fai clic su **[!UICONTROL Aggiungi utente]**.

   ![](assets/push_product_6.png)

1. Digita il nome o l’indirizzo e-mail dell’utente e seleziona l’utente. Quindi, fai clic su **[!UICONTROL Salva]**.

   >[!NOTE]
   >
   >Se l’utente non è stato creato in precedenza in Admin Console, consulta la [Aggiungere la documentazione degli utenti](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)

### Configurare l’app {#configure-app}

La configurazione tecnica prevede una stretta collaborazione tra lo sviluppatore dell’app e l’amministratore aziendale. Prima di iniziare a inviare notifiche push con [!DNL Journey Optimizer], è necessario definire le impostazioni in [!DNL Adobe Experience Platform Data Collection] e integra la tua app mobile con gli SDK di Adobe Experience Platform Mobile.

Segui i passaggi di implementazione descritti nei collegamenti seguenti:

* Per **Apple iOS**: Scopri come registrare l’app con APN in [Documentazione di Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}
* Per **Google Android**: Scopri come configurare un’app client Firebase Cloud Messaging su Android in [Documentazione di Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}

### Integrare la tua app mobile con l’SDK di Adobe Experience Platform {#integrate-mobile-app}

L’SDK di Adobe Experience Platform Mobile fornisce API di integrazione lato client per i dispositivi mobili tramite SDK compatibili con Android e iOS. Segui [Documentazione di Adobe Experience Platform Mobile SDK](https://aep-sdks.gitbook.io/docs/getting-started/overview){target="_blank"} per effettuare la configurazione con gli SDK di Adobe Experience Platform Mobile nella tua app.

Alla fine di questo, avresti dovuto anche creare e configurare una proprietà mobile in [!DNL Adobe Experience Platform Data Collection]. In genere creerai una proprietà mobile per ogni app mobile che desideri gestire. Scopri come creare e configurare una proprietà mobile in [Documentazione di Adobe Experience Platform Mobile SDK](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property){target="_blank"}.


## Passaggio 1: Aggiungere le credenziali push dell&#39;app nella raccolta dati di Adobe Experience Platform {#push-credentials-launch}

Dopo aver concesso le autorizzazioni utente corrette, ora devi aggiungere le credenziali push dell’app mobile in [!DNL Adobe Experience Platform Data Collection].

La registrazione delle credenziali push dell’app mobile è necessaria per autorizzare l’Adobe a inviare notifiche push per tuo conto. Fai riferimento ai passaggi descritti di seguito:

1. Da [!DNL Adobe Experience Platform Data Collection], seleziona **[!UICONTROL Superfici app]** nel pannello a sinistra.

1. Fai clic su **[!UICONTROL Crea superficie dell&#39;app]** per creare una nuova configurazione.

   ![](assets/add-app-config.png)

1. Inserisci un **[!UICONTROL Nome]** per la configurazione.

1. Da **[!UICONTROL Configurazione di applicazioni mobili]**, selezionare il sistema operativo:

   * **Per iOS**

      ![](assets/add-app-config-ios.png)

      1. Immetti l’app mobile **Id Bundle** in **[!UICONTROL ID app (iOS Bundle ID)]** campo . L’ID bundle dell’app si trova nella sezione **Generale** scheda del target principale in **XCode**.

      1. Acceso il **[!UICONTROL Credenziali push]** per aggiungere le credenziali.

      1. Trascina e rilascia il file .p8 Apple Push Notification Authentication Key . Questa chiave può essere acquisita dalla **Certificati**, **Identificatori** e **Profili** pagina.

      1. Fornisci **ID chiave**. Si tratta di una stringa di 10 caratteri assegnata durante la creazione della chiave di autenticazione p8. Si trova in **Chiavi** scheda in **Certificati**, **Identificatori** e **Profili** pagina.

      1. Fornisci **ID team**. Questo è un valore di stringa che si trova nella scheda Appartenenza.
   * **Per Android**

      ![](assets/add-app-config-android.png)

      1. Fornisci **[!UICONTROL ID app (nome del pacchetto Android)]**: in genere il nome del pacchetto è l&#39;ID app nel tuo `build.gradle` file.

      1. Acceso il **[!UICONTROL Credenziali push]** per aggiungere le credenziali.

      1. Trascina e rilascia le credenziali push FCM. Per ulteriori dettagli su come ottenere le credenziali push, consulta [Documentazione di Google](https://firebase.google.com/docs/admin/setup#initialize-sdk){target="_blank"}.



1. Fai clic su **[!UICONTROL Salva]** per creare la configurazione dell’app.

<!--
## Step 2: Set up a mobile property in Adobe Experience Platform Launch {#launch-property}

Setting up a mobile property allows the mobile app developer or marketer to configure the mobile SDKs attributes such as Session Timeouts, the [!DNL Adobe Experience Platform] sandbox to be targeted and the **[!UICONTROL Adobe Experience Platform Datasets]** to be used for mobile SDK to send data to.

For further details and procedures on how to set up a **[!UICONTROL Platform Launch property]**, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property).


To get the SDKs needed for push notification to work you will need the following SDK extensions, for both Android and iOS:

* **[!UICONTROL Mobile Core]** (installed automatically)
* **[!UICONTROL Profile]** (installed automatically)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, optional but recommended to debug the mobile implementation.

Learn more about [!DNL Adobe Experience Platform Launch] extensions in [Adobe Experience Platform Launch documentation](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).
-->

## Passaggio 2: Configura estensione Adobe Journey Optimizer nella tua proprietà mobile {#configure-journey-optimizer-extension}

La **Estensione Adobe Journey Optimizer** per gli SDK di Adobe Experience Platform Mobile puoi abilitare le notifiche push per le tue app mobili e aiutarti a raccogliere i token push degli utenti e a gestire la misurazione delle interazioni con Adobe Experience Platform Services.

Scopri come impostare l’estensione Journey Optimizer in [Documentazione di Adobe Experience Platform Mobile SDK](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-journey-optimizer){target="_blank"}.


<!-- 
**[!UICONTROL Edge configuration]** is used by **[!UICONTROL Edge]** extension to send custom data from mobile device to [!DNL Adobe Experience Platform]. 
To configure [!DNL Adobe Experience Platform], you must provide the **[!UICONTROL Sandbox]** name and **[!UICONTROL Event Dataset]**.

For further details and procedures on how to create **[!UICONTROL Edge configuration]**, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)



1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. select the **[!UICONTROL Properties]** tab and click **[!UICONTROL New Property]**.

    ![](assets/push-config-6.png)

1. Enter a **[!UICONTROL Name]** for your new property.

1. Select **[!UICONTROL Mobile]** as **[!UICONTROL Platform]**.

    ![](assets/push-config-7.png)

1. Click **[!UICONTROL Save]** to create your new property.

To configure **[!UICONTROL Adobe Experience Platform Edge Extension]** to send custom data from mobile devices to [!DNL Adobe Experience Platform].

1. Select your previously created property and select the **[!UICONTROL Extensions]** tab to view the extensions for this property.

    ![](assets/push-config-8.png)

1. Click **[!UICONTROL Configure]** under the **[!UICONTROL Adobe Experience Platform Edge]** Network' extension.

1. From the **[!UICONTROL Edge Configuration]** drop-down list, select the **[!UICONTROL Edge Configuration]** created in the previous steps. For more information on **[!UICONTROL Edge Configuration]**, refer to this [section](#edge-configuration).

1. Click **[!UICONTROL Save]**.

To configure **[!UICONTROL Adobe Experience Platform Messaging]** extension to send push profile and push interactions to the correct datasets, follow the same steps as above. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** created in the [Adobe Experience Platform setup](#edge-configuration).
-->

<!--
## Step 4: Publish the Property {#publish-property}

You now need to publish the property to integrate your configuration and to use it in the mobile app. 

To publish your property, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)

## Step 5: Configure the ProfileDataSource {#configure-profiledatasource}

To configure the `ProfileDataSource`, use the `ProfileDCInletURL` from [!DNL Adobe Experience Platform] setup and add the following in the mobile app:

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

-->

## Passaggio 3: Testare l’app mobile con un evento {#mobile-app-test}

Dopo aver configurato l’app mobile sia in Adobe Experience Platform che in [!DNL Adobe Experience Platform Data Collection], ora puoi testarlo prima di inviare notifiche push ai profili. In questo caso d’uso, creiamo un percorso per eseguire il targeting della nostra app mobile e imposta un evento che attiva la notifica push.

<!--
You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).
-->

Affinché questo percorso funzioni, è necessario creare uno schema XDM. Per ulteriori informazioni, consulta [Documentazione di XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schemas-and-data-ingestion){target="_blank"}.

1. Nel menu a sinistra, cerca **[!UICONTROL Schemi]**.

1. Fai clic su **[!UICONTROL Creare uno schema]** quindi seleziona **[!UICONTROL ExperienceEvent XDM]**.

   ![](assets/test_push_2.png)

1. Seleziona **[!UICONTROL Crea un nuovo gruppo di campi]**.

1. Inserisci un **[!UICONTROL Nome visualizzato]** e **[!UICONTROL Descrizione]**. Fai clic su **[!UICONTROL Aggiungi gruppi di campi]** al termine. Per ulteriori informazioni su come creare gruppi di campi, consulta [Documentazione del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it){target="_blank"}.


   ![](assets/test_push_4.png)

1. Sul lato sinistro, seleziona lo schema. Nel riquadro a destra, immetti il nome dello schema e della descrizione. Abilita questo schema per **[!UICONTROL Profilo]**.

   ![](assets/test_push_4b.png)


1. Sul lato sinistro, seleziona il gruppo di campi, quindi fai clic sull’icona + per creare un nuovo campo. In **[!UICONTROL Proprietà dei gruppi di campi]**, a destra, digita un **[!UICONTROL Nome campo]**, **[!UICONTROL Nome visualizzato]** e seleziona **[!UICONTROL Stringa]** come **[!UICONTROL Tipo]**.

   ![](assets/test_push_5.png)

1. Controlla **[!UICONTROL Obbligatorio]** e fai clic su **[!UICONTROL Applica]**.

1. Fai clic su **[!UICONTROL Salva]**. Lo schema viene ora creato e può essere utilizzato in un evento.

È quindi necessario impostare un evento.

1. Dal menu a sinistra della home page, in AMMINISTRAZIONE, selezionare **[!UICONTROL Configurazioni]**. Fai clic su **[!UICONTROL Gestisci]** in **[!UICONTROL Eventi]** per creare il nuovo evento.

1. Fai clic su **[!UICONTROL Crea evento]**, il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

   ![](assets/test_push_6.png)

1. Inserisci il nome dell’evento. Puoi anche aggiungere una descrizione.

1. In **[!UICONTROL Tipo ID evento]** campo , seleziona **[!UICONTROL Basato su regole]**.

1. In **[!UICONTROL Parametri]**, seleziona lo schema creato in precedenza.

   ![](assets/test_push_7.png)

1. Nell’elenco dei campi, verifica che il campo creato nel gruppo di campi dello schema sia selezionato.

   ![](assets/test_push_7b.png)

1. Fai clic su **[!UICONTROL Modifica]** in **[!UICONTROL Condizione ID evento]** campo . Trascina e rilascia il campo aggiunto in precedenza per definire la condizione che verrà utilizzata dal sistema per identificare gli eventi che attivano il percorso.

   ![](assets/test_push_8.png)

1. Digita la sintassi da utilizzare per attivare la notifica push nell’app di prova, in questo esempio **conferma dell&#39;ordine**.

   ![](assets/test_push_9.png)

1. Seleziona **[!UICONTROL ECID]** come **[!UICONTROL Namespace]**.

1. Fai clic su **[!UICONTROL Ok]** then **[!UICONTROL Salva]**.

L’evento viene ora creato e può essere utilizzato in un percorso.

1. Nel menu a sinistra, fai clic su **[!UICONTROL Percorsi]**.

1. Fai clic su **[!UICONTROL Crea Percorso]** per creare un nuovo percorso.

1. Modifica le proprietà del percorso nel riquadro di configurazione visualizzato sul lato destro. Ulteriori informazioni [sezione](../building-journeys/journey-gs.md#change-properties).

1. Inizia trascinando l’evento creato nei passaggi precedenti dalla **[!UICONTROL Eventi]** a discesa.

   ![](assets/test_push_11.png)

1. Da **[!UICONTROL Azioni]** a discesa, trascina e rilascia una **[!UICONTROL Push]** attività nel tuo percorso.

1. Configura la notifica push. Per ulteriori informazioni su come creare le notifiche push, consulta questo [page](create-push.md).

1. Fai clic sul pulsante **[!UICONTROL Test]** per iniziare a testare le notifiche push e fai clic su **[!UICONTROL Attiva un evento]**.

   ![](assets/test_push_12.png)

1. Inserisci il tuo ECID nel **[!UICONTROL Chiave]** quindi digitare in **conferma dell&#39;ordine** nel secondo campo.

   ![](assets/test_push_13.png)

1. Fai clic su **[!UICONTROL Invia]**.

L’evento verrà attivato e riceverai la notifica push all’app mobile.

## Passaggio 4: Creare una superficie del canale per la pressione{#message-preset}

Una volta che l’app mobile è stata configurata in [!DNL Adobe Experience Platform Data Collection], devi creare una superficie per poter inviare notifiche push da **[!DNL Journey Optimizer]**.

Scopri come creare e configurare una superficie del canale in [questa sezione](../configuration/channel-surfaces.md).

Ora puoi inviare notifiche push con Journey Optimizer.

* Scopri come creare un messaggio push in [questa pagina](create-push.md).
* Scopri come aggiungere un messaggio a un percorso in [questa sezione](../building-journeys/journeys-message.md).
