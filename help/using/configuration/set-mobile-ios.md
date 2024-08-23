---
solution: Journey Optimizer
product: journey optimizer
title: Configurare iOS Mobile
description: Scopri come configurare e monitorare i canali mobili di iOS
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canale, superficie, tecnico, parametri, ottimizzatore
hide: true
hidefromtoc: true
source-git-commit: f0273d24a85488d406b836bee8c2300d189d83e9
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 3%

---

# Configurare la configurazione di iOS per dispositivi mobili {#set-mobile-ios}

>[!IMPORTANT]
>
>Per garantire compatibilità e prestazioni ottimali, assicurati di utilizzare le seguenti versioni SDK:
>
> * SDK di base: 5.2.0 o versione successiva
> * SDK per messaggistica: 5.1.1 o versione successiva

Questa configurazione di iOS semplifica la configurazione rapida dei canali di marketing, rendendo immediatamente disponibili tutte le risorse essenziali nelle app Experience Platform, Journey Optimizer e Data Collection. Questo consente al team marketing di iniziare rapidamente a creare campagne e percorsi.

## Creare una nuova configurazione di iOS {#new-setup-ios}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_swift_dependencies_add"
>title="Aggiungere dipendenze"
>abstract="In Xcode, aggiungi il pacchetto Assurance per verificare, verificare, simulare e convalidare la raccolta dati e le esperienze nell’app. Inoltre, aggiungi Messaggistica AEP per inviare token di notifica push e feedback click-through a Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks#swift-package-manager" text="Consulta la documentazione sulla raccolta dati"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_swift_initialization_code"
>title="Aggiungere il codice di inizializzazione"
>abstract="Per inizializzare correttamente l&#39;app, inserire il codice di inizializzazione fornito nel metodo **didFinishLaunchingWithOptions** del file AppDelegate. In questo modo l’app verrà eseguita al momento opportuno durante il suo processo di avvio."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_swift_dependencies_import"
>title="Importare dipendenze"
>abstract="Nella classe **AppDelegate** dell&#39;applicazione, importare le dipendenze seguenti: AEPCore, AEPAssurance, AEPEdge, AEPEdgeIdentity e AEPMessaging."
>additional-url="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks#import-extensions" text="Consulta la documentazione sulla raccolta dati"

1. Dalla home page di Journey Optimizer, fai clic su **[!UICONTROL Inizia]** dalla scheda **[!UICONTROL Configura canali Web e mobili]**.

   ![](assets/guided-setup-config-1.png)

1. Crea una configurazione **[!UICONTROL New]**.

   Se disponi già di configurazioni esistenti, puoi sceglierne una o crearne una nuova.

   ![](assets/guided-setup-config-2.png)

1. Immetti un **[!UICONTROL Nome]** per la nuova configurazione e seleziona o crea il **[!UICONTROL Stream di dati]**. **[!UICONTROL Name]** verrà utilizzato per ogni risorsa creata automaticamente.

1. Se la tua organizzazione dispone di più flussi di dati, selezionane uno dalle opzioni esistenti. Se non disponi di uno stream di dati, ne verrà creato uno automaticamente.

1. Seleziona la piattaforma iOS e fai clic su **[!UICONTROL Creazione automatica risorse]**.

   ![](assets/guided-setup-config-3.png)

1. Per semplificare il processo di configurazione, vengono create automaticamente le risorse necessarie per iniziare. Ciò include la creazione di una nuova **[!UICONTROL proprietà tag mobile]** e l&#39;installazione di estensioni.

   Di seguito è riportato un elenco completo di tutte le risorse generate automaticamente:

+++ Risorse create

   <table>
    <thead>
    <tr>
    <th><strong>Soluzione</strong></th>
    <th><strong>Risorse create automaticamente</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>
    <p>Journey Optimizer</p>
    </td>
    <td>
    <ul>
    <li>Configurazione canale</li>
    <li>Credenziali push (solo messaggi push per dispositivi mobili)</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Tag</p>
    </td>
    <td>
    <ul>
    <li>Mobile Tag, proprietà</li>
    <li>Regole</li>
    <li>Elementi dati</li>
    <li>Libreria</li>
    <li>Ambienti (staging, produzione, sviluppo)</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Estensioni tag</p>
    </td>
    <td>
    <ul>
    <li>Edge Network Adobe Experience Platform</li>
    <li>Adobe Journey Optimizer</li>
    <li>AEP Assurance</li>
    <li>Consenso (con i criteri di consenso predefiniti abilitati)</li>
    <li>Identità (con ECID predefinito, con regole di unione predefinite)</li>
    <li>Core mobile</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Assurance</p>
    </td>
    <td>
    <p>Sessione Assurance</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Stream di dati</p>
    </td>
    <td>
    <p>Stream di dati con servizi</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Experience Platform</p>
    </td>
    <td>
    <ul>
    <li>Set di dati</li>
    <li>Schema</li>
    </ul>
    </td>
    </tr>
    </tbody>
    </table>

+++

1. Al termine della generazione delle risorse, fai clic su **[!UICONTROL Configura]** per iniziare a configurare l&#39;SDK.

   ![](assets/guided-setup-config-ios-1.png)

1. Devi innanzitutto aggiungere e importare le dipendenze come descritto nell’interfaccia utente. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks).

1. Inserire il codice di inizializzazione nel metodo `onCreate()` dell&#39;applicazione. Questo codice di test ti consente di connetterti a Assurance e convalidare la configurazione dell’app prima di passare alla produzione.

   ![](assets/guided-setup-config-ios-2.png){zoomable="yes"}

1. Per convalidare l&#39;SDK direttamente sull&#39;app mobile, è sufficiente aprire l&#39;app mobile e consentire l&#39;accesso a [Adobe Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home). Assurance è uno strumento potente che consente di testare e convalidare in modo approfondito l’implementazione, garantendo il corretto funzionamento di tutto.

   Una volta connesso, il dispositivo verrà automaticamente rilevato ed elencato nel menu a discesa **[!UICONTROL Dispositivo disponibile]**, che consente di monitorare e risolvere i problemi di installazione in tempo reale.

   ![](assets/guided-setup-config-ios-3.png){zoomable="yes"}

1. Fai clic su **[!UICONTROL Connetti]**.

   ![](assets/guided-setup-config-ios-4.png){zoomable="yes"}

1. Ora puoi configurare i tuoi [canali in-app](#inapp-channel) e/o [push](#push-channel).

1. Al termine della configurazione, condividi la **[!UICONTROL Configurazione canale]** generata automaticamente con i membri del team responsabili della creazione di Percorsi e campagne.

   È necessario fare riferimento alla **[!UICONTROL Configurazione canale]** nell&#39;interfaccia Campagne o Percorsi per consentire una connessione senza soluzione di continuità tra la configurazione e l&#39;esecuzione di percorsi e campagne mirati per il pubblico.

   ![](assets/guided-setup-config-ios-8.png){zoomable="yes"}

## Modificare una configurazione esistente {#reconnect}

Dopo aver creato la configurazione, è possibile rivisitarla in qualsiasi momento per aggiungere altri canali o apportare ulteriori modifiche in base alle proprie esigenze

1. Dalla home page di Journey Optimizer, fai clic su **[!UICONTROL Inizia]** dalla scheda **[!UICONTROL Configura canali Web e mobili]**.

   ![](assets/guided-setup-config-1.png)

1. Seleziona **[!UICONTROL Esistente]** e scegli la tua **[!UICONTROL proprietà tag]** esistente dal menu a discesa.

   ![](assets/guided-setup-config-ios-9.png)

1. Quando accedi alla configurazione esistente, devi riconnetterti con Adobe Assurance. Dal menu di configurazione dell&#39;SDK, fare clic su **[!UICONTROL Riconnetti]**.

   ![](assets/guided-setup-config-ios-10.png)

1. Seleziona il tuo dispositivo dal menu a discesa **[!UICONTROL Dispositivi disponibili]** e fai clic su **[!UICONTROL Connetti]**.

   ![](assets/guided-setup-config-ios-11.png){zoomable="yes"}

1. Ora puoi aggiornare la configurazione in base alle esigenze.

## Configurare il canale in-app {#inapp-channel}

Il canale in-app non richiede alcuna configurazione aggiuntiva. Per verificare che la configurazione sia accurata, puoi inviare facilmente un messaggio di test utilizzando la funzione Assurance. In questo modo verrà fornito un feedback immediato sulla disponibilità del sistema a distribuire messaggi in-app in modo efficace.

A tale scopo, fare clic su **[!UICONTROL Visualizza messaggio in-app]**.

![](assets/guided-setup-config-ios-5.png){zoomable="yes"}

Per semplificare il processo di configurazione, vengono create automaticamente le risorse necessarie per iniziare. Ciò include la creazione di una configurazione del canale.

Ora puoi inviare messaggi in-app utilizzando la **[!UICONTROL Configurazione canale]** configurata in precedenza. [Scopri come creare messaggi in-app](../in-app/create-in-app.md)

## Configurare il canale push {#push-channel}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_certificate"
>title="Fornire un certificato push"
>abstract="Il file .p8 contiene una chiave privata utilizzata per autenticare l’app con i server di Apple per notifiche push sicure. Puoi acquisire questa chiave dalla pagina Certificati, Identificatori e Profili del tuo account sviluppatore."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_key_id"
>title="ID chiave"
>abstract="L&#39;ID chiave, una stringa di 10 caratteri assegnata durante la creazione della chiave di autenticazione p8, si trova nella scheda **Chiavi** della pagina Certificati, identificatori e profili del tuo account sviluppatore."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_team_id"
>title="ID team"
>abstract="L&#39;ID team, un valore stringa utilizzato per identificare il team, si trova nella scheda **Appartenenza** nell&#39;account sviluppatore."

1. Una volta configurato l&#39;SDK di Mobile, fai clic su **[!UICONTROL Aggiungi]** dalla scheda di notifica push.

1. Innanzitutto, all&#39;interno del metodo `didRegisterForRemoteNotificationsWithDeviceToken` di `AppDelegate`, aggiungi il seguente codice per sincronizzare il token push del dispositivo con il tuo profilo Adobe Experience Platform.

   ```
   MobileCore.setPushIdentifier(deviceToken)
   ```

1. Trascina e rilascia il file .p8 Apple Push Notification Authentication Key. Questa chiave può essere acquisita dalla pagina Certificati, identificatori e profili.

1. Fornisci le seguenti informazioni:

   * ID chiave: una stringa di 10 caratteri assegnata durante la creazione della chiave di autenticazione p8. È disponibile nella scheda Chiavi nella pagina Certificati, identificatori e profili.

   * ID team: un valore stringa che si trova nella scheda Appartenenza.

   ![](assets/guided-setup-config-ios-6.png){zoomable="yes"}

1. Per verificare che la configurazione sia accurata, puoi inviare facilmente un messaggio di test utilizzando la funzione Assurance. Questo fornirà un feedback immediato sulla preparazione del sistema per distribuire le notifiche push in modo efficace.

   A tale scopo, fare clic su **[!UICONTROL Invia messaggio push]**.

   ![](assets/guided-setup-config-ios-7.png){zoomable="yes"}

Per semplificare il processo di configurazione, vengono create automaticamente le risorse necessarie per iniziare. Ciò include la creazione di una **[!UICONTROL Configurazione canale]** e di **[!UICONTROL Credenziali push]**.

Ora puoi inviare notifiche push utilizzando la **[!UICONTROL Configurazione canale]** configurata in precedenza. [Scopri come creare una notifica push](../push/create-push.md)
