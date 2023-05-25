---
solution: Journey Optimizer
product: journey optimizer
title: Configurazione della notifica push
description: Scopri come configurare l’ambiente per inviare notifiche push con Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7099d44e-5d5d-4eef-9477-f68f4eaa1983
source-git-commit: 60adbc8ad4c49b9282502d26a9a9aac73693d049
workflow-type: tm+mt
source-wordcount: '1588'
ht-degree: 3%

---

# Configurare il canale di notifica push {#push-notification-configuration}

[!DNL Journey Optimizer] consente di creare percorsi e inviare messaggi a un pubblico mirato. Prima di iniziare a inviare notifiche push con [!DNL Journey Optimizer], devi assicurarti che le configurazioni e le integrazioni siano attive nell’app mobile e per i tag in Adobe Experience Platform. Comprendere il flusso di dati delle notifiche push in [!DNL Adobe Journey Optimizer] fare riferimento a [questa pagina](push-gs.md).

>[!AVAILABILITY]
>
>Il nuovo **flusso di lavoro di avvio rapido per l’onboarding per dispositivi mobili** è ora disponibile. Utilizza questa nuova funzione del prodotto per configurare rapidamente l’SDK di Mobile per iniziare a raccogliere e convalidare i dati dell’evento mobile e per inviare notifiche push per dispositivi mobili. Questa funzionalità è accessibile come Beta pubblica tramite la pagina Home di raccolta dati. [Ulteriori informazioni](mobile-onboarding-wf.md)


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

Prima di creare un’app mobile, è necessario assicurarsi di disporre delle autorizzazioni utente corrette per i tag in Adobe Experience Platform o assegnarle. Ulteriori informazioni in [Documentazione sui tag](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}.

>[!CAUTION]
>
>La configurazione push deve essere eseguita da un utente esperto. A seconda del modello di implementazione e degli utenti tipo coinvolti nell&#39;implementazione, potrebbe essere necessario assegnare l&#39;intero set di autorizzazioni a un singolo profilo di prodotto o condividere le autorizzazioni tra lo sviluppatore di app e **Adobe Journey Optimizer** amministratore. Ulteriori informazioni su **Tag** autorizzazioni in [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}.

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

Da assegnare **Proprietà** e **Azienda** diritti, segui i passaggi seguenti:

1. Accedere a **[!DNL Admin Console]**.

1. Dalla sezione **[!UICONTROL Prodotti]** , seleziona la scheda **[!UICONTROL Raccolta dati di Adobe Experience Platform]** Card.

   ![](assets/push_product_1.png)

1. Seleziona un elemento esistente **[!UICONTROL Profilo prodotto]** o creane una nuova con **[!UICONTROL Nuovo profilo]** pulsante. Scopri come creare una nuova **[!UICONTROL Nuovo profilo]** nel [Documentazione di Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui){target="_blank"}.

1. Dalla sezione **[!UICONTROL Autorizzazioni]** , seleziona **[!UICONTROL Diritti di proprietà]**.

   ![](assets/push_product_2.png)

1. Clic **[!UICONTROL Aggiungi tutto]**. Questo aggiungerà il seguente diritto al tuo profilo di prodotto:
   * **[!UICONTROL Approvazione]**
   * **[!UICONTROL Sviluppa]**
   * **[!UICONTROL Gestisci ambienti]**
   * **[!UICONTROL Gestire le estensioni]**
   * **[!UICONTROL Pubblica]**

   Queste autorizzazioni sono necessarie per installare e pubblicare l&#39;estensione Adobe Journey Optimizer e pubblicare la proprietà dell&#39;app nell&#39;SDK di Adobe Experience Platform Mobile.

1. Quindi, seleziona **[!UICONTROL Diritti aziendali]** nel menu di sinistra.

   ![](assets/push_product_4.png)

1. Aggiungi i seguenti diritti:

   * **[!UICONTROL Gestire le configurazioni dell’app]**
   * **[!UICONTROL Gestisci proprietà]**

   Queste autorizzazioni sono necessarie per consentire allo sviluppatore di app mobili di impostare le credenziali push in **Raccolta dati di Adobe Experience Platform** e definire le superfici di canale per le notifiche push (ossia i predefiniti per messaggi) in **Adobe Journey Optimizer**.

   ![](assets/push_product_5.png)

1. Fai clic su **[!UICONTROL Salva]**.

Per assegnare questo **[!UICONTROL Profilo di prodotto]** per gli utenti, effettua le seguenti operazioni:

1. Accedere a **[!DNL Admin Console]**.

1. Dalla sezione **[!UICONTROL Prodotti]** , seleziona la scheda **[!UICONTROL Raccolta dati di Adobe Experience Platform]** Card.

1. Seleziona la configurata in precedenza **[!UICONTROL Profilo di prodotto]**.

1. Dalla sezione **[!UICONTROL Utenti]** , fare clic su **[!UICONTROL Aggiungi utente]**.

   ![](assets/push_product_6.png)

1. Digita il nome o l’indirizzo e-mail dell’utente e selezionalo. Quindi, fai clic su **[!UICONTROL Salva]**.

   >[!NOTE]
   >
   >Se l’utente non è stato creato in precedenza in Admin Console, consulta [Aggiungi documentazione utenti](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)

### Configurare l’app {#configure-app}

La configurazione tecnica prevede una stretta collaborazione tra lo sviluppatore dell’app e l’amministratore aziendale. Prima di iniziare a inviare notifiche push con [!DNL Journey Optimizer], è necessario definire le impostazioni in [!DNL Adobe Experience Platform Data Collection] e integra la tua app mobile con gli SDK di Adobe Experience Platform Mobile.

Segui i passaggi di implementazione descritti nei collegamenti seguenti:

* Per **Apple iOS**: scopri come registrare l’app con i numeri APN in [Documentazione di Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}
* Per **Google Android**: scopri come configurare un’app client Firebase Cloud Messaging su Android in [Documentazione di Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}

### Integrare la tua app mobile con l’SDK di Adobe Experience Platform {#integrate-mobile-app}

L’SDK di Adobe Experience Platform Mobile fornisce API di integrazione lato client per i dispositivi mobili tramite SDK compatibili con Android e iOS. Segui [Documentazione di Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} per eseguire la configurazione con gli SDK di Adobe Experience Platform Mobile nella tua app.

Al termine di questa fase, avresti anche dovuto creare e configurare una proprietà mobile in [!DNL Adobe Experience Platform Data Collection]. In genere si crea una proprietà mobile per ogni applicazione mobile che si desidera gestire. Scopri come creare e configurare una proprietà mobile in [Documentazione di Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.


## Passaggio 1: aggiungere le credenziali push dell’app in Raccolta dati di Adobe Experience Platform {#push-credentials-launch}

Dopo aver concesso le autorizzazioni utente corrette, ora devi aggiungere le credenziali push dell’app mobile in [!DNL Adobe Experience Platform Data Collection].

La registrazione delle credenziali push dell’app mobile è necessaria per autorizzare l’Adobe a inviare notifiche push per tuo conto. Consulta i passaggi descritti di seguito:

1. Da [!DNL Adobe Experience Platform Data Collection], seleziona la **[!UICONTROL Superfici app]** nel pannello a sinistra.

1. Clic **[!UICONTROL Crea superficie app]** per creare una nuova configurazione.

   ![](assets/add-app-config.png)

1. Immetti un **[!UICONTROL Nome]** per la configurazione.

1. Da **[!UICONTROL Configurazione applicazione mobile]**, selezionare il sistema operativo:

   * **Per iOS**

      ![](assets/add-app-config-ios.png)

      1. Immetti l’app mobile **ID bundle** nel **[!UICONTROL ID app (ID bundle iOS)]** campo. L’ID del bundle dell’app si trova nella sezione **Generale** scheda della destinazione principale in **Xcode**.

      1. Attivato il **[!UICONTROL Credenziali push]** per aggiungere le credenziali.

      1. Trascina e rilascia il file .p8 Apple Push Notification Authentication Key. Questa chiave può essere acquisita da **Certificati**, **Identificatori** e **Profili** pagina.

      1. Fornisci **ID chiave**. Si tratta di una stringa di 10 caratteri assegnata durante la creazione del tasto di autenticazione p8. È disponibile in **Chiavi** scheda in **Certificati**, **Identificatori** e **Profili** pagina.

      1. Fornisci **ID team**. Si tratta di un valore stringa che si trova nella scheda Appartenenza.
   * **Per Android**

      ![](assets/add-app-config-android.png)

      1. Fornisci **[!UICONTROL ID app (nome pacchetto Android)]**: in genere il nome del pacchetto corrisponde all’id dell’app nel `build.gradle` file.

      1. Attivato il **[!UICONTROL Credenziali push]** per aggiungere le credenziali.

      1. Trascina e rilascia le credenziali push FCM. Per ulteriori dettagli su come ottenere le credenziali push, consulta [Documentazione di Google](https://firebase.google.com/docs/admin/setup#initialize-sdk){target="_blank"}.



1. Clic **[!UICONTROL Salva]** per creare la configurazione dell’app.

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

## Passaggio 2: configurare l’estensione Adobe Journey Optimizer nella proprietà mobile {#configure-journey-optimizer-extension}

Il **Estensione Adobe Journey Optimizer** per Adobe Experience Platform Mobile, l&#39;SDK potenzia le notifiche push per le app mobili e ti aiuta a raccogliere i token push degli utenti e a gestire la misurazione delle interazioni con i servizi Adobe Experience Platform.

Scopri come configurare l’estensione Journey Optimizer in [Documentazione di Adobe Experience Platform Mobile SDK](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-journey-optimizer){target="_blank"}.


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

## Passaggio 3: testare l’app mobile con un evento {#mobile-app-test}

Dopo aver configurato l’app mobile sia in Adobe Experience Platform che in [!DNL Adobe Experience Platform Data Collection], ora puoi testarlo prima di inviare notifiche push ai profili. In questo caso d’uso, creiamo un percorso per eseguire il targeting della nostra app mobile e impostare un evento che attiva la notifica push.

<!--
You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).
-->

Affinché questo percorso funzioni, devi creare uno schema XDM. Per ulteriori informazioni, consulta [Documentazione XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schemas-and-data-ingestion){target="_blank"}.

1. Nel menu a sinistra, passa a **[!UICONTROL Schemi]**.

1. Clic **[!UICONTROL Crea schema]** quindi seleziona **[!UICONTROL XDM ExperienceEvent]**.

   ![](assets/test_push_2.png)

1. Seleziona **[!UICONTROL Crea un nuovo gruppo di campi]**.

1. Immetti un **[!UICONTROL Nome visualizzato]** e un **[!UICONTROL Descrizione]**. Clic **[!UICONTROL Aggiungi gruppi di campi]** al termine. Per ulteriori informazioni su come creare gruppi di campi, consulta [Documentazione del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=it){target="_blank"}.


   ![](assets/test_push_4.png)

1. Sul lato sinistro, seleziona lo schema. Nel riquadro di destra, immettere il nome dello schema e la descrizione. Abilita questo schema per **[!UICONTROL Profilo]**.

   ![](assets/test_push_4b.png)


1. Sul lato sinistro, seleziona il gruppo di campi, quindi fai clic sull’icona + per creare un nuovo campo. In **[!UICONTROL Proprietà dei gruppi di campi]**, a destra, digita **[!UICONTROL Nome campo]**, **[!UICONTROL Nome visualizzato]** e seleziona **[!UICONTROL Stringa]** as **[!UICONTROL Tipo]**.

   ![](assets/test_push_5.png)

1. Verifica **[!UICONTROL Obbligatorio]** e fai clic su **[!UICONTROL Applica]**.

1. Fai clic su **[!UICONTROL Salva]**. Ora lo schema viene creato e può essere utilizzato in un evento.

Quindi devi impostare un evento.

1. Dal menu a sinistra della home page, in AMMINISTRAZIONE, selezionare **[!UICONTROL Configurazioni]**. Il clic **[!UICONTROL Gestisci]** nel **[!UICONTROL Eventi]** per creare il nuovo evento.

1. Clic **[!UICONTROL Crea evento]**, il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

   ![](assets/test_push_6.png)

1. Inserisci il nome dell’evento. Puoi anche aggiungere una descrizione.

1. In **[!UICONTROL Tipo ID evento]** campo, seleziona **[!UICONTROL Basato su regole]**.

1. In **[!UICONTROL Parametri]**, seleziona lo schema creato in precedenza.

   ![](assets/test_push_7.png)

1. Nell’elenco dei campi, verifica che sia selezionato il campo creato nel gruppo di campi dello schema.

   ![](assets/test_push_7b.png)

1. Clic **[!UICONTROL Modifica]** nel **[!UICONTROL Condizione ID evento]** campo. Trascina e rilascia il campo aggiunto in precedenza per definire la condizione che verrà utilizzata dal sistema per identificare gli eventi che attivano il percorso.

   ![](assets/test_push_8.png)

1. Digita la sintassi da utilizzare per attivare la notifica push nell’app di prova, in questo esempio **conferma dell’ordine**.

   ![](assets/test_push_9.png)

1. Seleziona **[!UICONTROL ECID]** come **[!UICONTROL Namespace]**.

1. Clic **[!UICONTROL Ok]** allora **[!UICONTROL Salva]**.

L&#39;evento è stato creato e ora può essere utilizzato in un percorso.

1. Nel menu a sinistra, fai clic su **[!UICONTROL Percorsi]**.

1. Clic **[!UICONTROL Crea Percorso]** per creare un nuovo percorso.

1. Modifica le proprietà del percorso nel riquadro di configurazione visualizzato sul lato destro. Ulteriori informazioni [sezione](../building-journeys/journey-gs.md#change-properties).

1. Per iniziare, trascina l’evento creato nei passaggi precedenti dalla sezione **[!UICONTROL Eventi]** a discesa.

   ![](assets/test_push_11.png)

1. Dalla sezione **[!UICONTROL Azioni]** a discesa, trascina e rilascia una **[!UICONTROL Push]** al tuo percorso.

1. Configura la notifica push. Per ulteriori informazioni su come creare notifiche push, consulta questa [pagina](create-push.md).

1. Fai clic su **[!UICONTROL Test]** attiva per avviare il test delle notifiche push e fai clic su **[!UICONTROL Attivare un evento]**.

   ![](assets/test_push_12.png)

1. Immetti il tuo ECID in **[!UICONTROL Chiave]** campo, quindi digita **conferma dell’ordine** nel secondo campo.

   ![](assets/test_push_13.png)

1. Clic **[!UICONTROL Invia]**.

L’evento verrà attivato e riceverai la notifica push all’app mobile.

## Passaggio 4: creare una superficie di canale per il push{#message-preset}

Una volta impostata l’app mobile in in [!DNL Adobe Experience Platform Data Collection], è necessario creare una superficie per poter inviare notifiche push da **[!DNL Journey Optimizer]**.

Scopri come creare e configurare una superficie di canale in [questa sezione](../configuration/channel-surfaces.md).

Ora puoi inviare notifiche push con Journey Optimizer.

* Scopri come creare un messaggio push in [questa pagina](create-push.md).
* Scopri come aggiungere un messaggio a un percorso in [questa sezione](../building-journeys/journeys-message.md).
