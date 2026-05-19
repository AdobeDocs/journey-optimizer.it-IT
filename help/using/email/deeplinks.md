---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare e configurare i collegamenti diretti nei messaggi e-mail e SMS
description: Scopri come aggiungere collegamenti diretti ai contenuti e-mail e SMS e come implementare la gestione dei collegamenti diretti nelle app iOS e Android.
feature: Email, SMS
topic: Content Management
role: User, Developer
level: Intermediate
keywords: deep link, collegamento profondo, collegamenti universali, collegamenti alle app, e-mail, sms
source-git-commit: 3d3218e24074ffb8ec36f1ec14ff8a6c45950d90
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 1%

---


# Utilizzare e configurare i collegamenti diretti nelle e-mail e negli SMS {#deeplinks}

I collegamenti diretti consentono di portare i destinatari da un messaggio e-mail o SMS a uno schermo o contenuto specifico nell’app mobile. Aiuta a portare le persone direttamente all&#39;esperienza in-app prevista, senza indirizzarle tramite un browser web o un app store, in modo che il percorso rimanga rilevante e sul marchio.

Quando i destinatari fanno clic sul collegamento diretto, vengono indirizzati direttamente al contenuto in-app desiderato - **a condizione che tu abbia completato**:

* [passaggi di configurazione](#configuration) in Journey Optimizer;

* i passaggi per l&#39;[implementazione dell&#39;app mobile](#mobile-implementation) per iOS e Android nella tua app mobile.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer] supporta il deep link per iOS e Android utilizzando URL tracciati (`/ee/v1/mclick/*`) per garantire la compatibilità e il tracciamento dei clic.

## Authoring dei deep link {#authoring}

### E-mail {#authoring-email}

Per i messaggi e-mail, puoi inserire un collegamento diretto in due modi:

* **Invia un&#39;e-mail a Designer**: assicurati che il tracciamento dei collegamenti [sia abilitato](message-tracking.md#enable-tracking). Seleziona l&#39;elemento da collegare (testo, pulsante o immagine), fai clic su **[!UICONTROL Inserisci collegamento]** nella barra degli strumenti contestuale e scegli **[!UICONTROL Collegamento diretto]** per immettere l&#39;URL del collegamento diretto. [Ulteriori informazioni sull&#39;inserimento di collegamenti](message-tracking.md#insert-links)

* **Editor Personalization (codice)**: inserire il collegamento diretto in HTML utilizzando lo snippet seguente:

  ```html
  <a class="arc-link" data-nl-type="DEEPLINK" href="<<deeplink_url>>" id="acr-link-7821368" style="text-decoration:underline;" target="_blank" data-tracking-type="DEEPLINK">Click Here</a>
  ```

  Sostituisci `<<deeplink_url>>` con l&#39;URL di collegamento diretto effettivo e utilizza un `id` univoco per ogni blocco per evitare conflitti.

### SMS {#authoring-sms}

Per gli SMS, i deep link vengono creati utilizzando la funzione helper **Url** nell&#39;editor di personalizzazione. Ulteriori informazioni sull&#39;aggiunta di collegamenti al contenuto SMS in [questa sezione](../sms/create-sms.md#sms-content).

Per inserire collegamenti diretti nel contenuto degli SMS, utilizza la sintassi seguente:

```
{{url originalUrl='<<url>>' type='DEEPLINK' action='CLICK'}}
```

Sostituisci `<<url>>` con l&#39;URL di collegamento diretto effettivo.

## Configurazione in Journey Optimizer {#configuration}

Per poter utilizzare i collegamenti profondi nelle e-mail e negli SMS per le app mobili, completa i passaggi di configurazione riportati di seguito.

>[!NOTE]
>
>Questa sezione si applica quando si utilizzano **collegamenti universali (iOS)** e **collegamenti alle app (Android)** (collegamenti diretti basati su HTTPS).

1. In Journey Optimizer, delega il sottodominio in cui è abilitato il deep linking. [Ulteriori informazioni](../configuration/delegate-subdomain.md)

1. Ospita il file AASA per iOS e il file assetLinks.json per Android sul tuo sottodominio. Contatta l&#39;[Assistenza clienti Adobe](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} o il tuo rappresentante Adobe con i dettagli seguenti:

   * **Per iOS (AASA)**:
      * Sottodominio delegato
      * ID bundle dell’app
   * **Per Android (assetLinks.json)**:
      * Sottodominio delegato
      * ID bundle dell’app
      * Impronta digitale del certificato SHA-256

>[!IMPORTANT]
>
>La creazione di collegamenti tramite l&#39;infrastruttura Adobe si applica quando il tracciamento dei collegamenti è abilitato per il messaggio, nelle[impostazioni di tracciamento e-mail](message-tracking.md#enable-tracking) o nella sezione **[!UICONTROL Tracciamento azioni]** per le campagne SMS. I clic di collegamento profondo tracciati utilizzano gli URL in `/ee/v1/mclick/*`, che Adobe ospita e risolve.
>
>Per **collegamenti non tracciati**, l&#39;URL non viene riscritto tramite i sistemi Adobe. Devi configurare i collegamenti universali o i collegamenti alle app sui tuoi domini e hosting in modo che tali collegamenti aprano l’app come previsto.

## Implementazione di un’app mobile {#mobile-implementation}

Questa sezione spiega come implementare i collegamenti diretti per dispositivi mobili con [!DNL Adobe Journey Optimizer] in modo che, in una configurazione tipica di **HTTPS** (collegamenti universali e collegamenti alle app), un singolo URL possa:

* Apri una schermata specifica all’interno dell’app mobile quando questa è installata, oppure
* Apri il sito web come fallback quando l’app non è installata.

Quando il tracciamento dei collegamenti è abilitato per il messaggio, [!DNL Journey Optimizer] continua a tenere traccia di questi clic, li include nel reporting e può utilizzarli in [esperimenti di contenuto](../content-management/content-experiment.md) se vengono eseguiti sul messaggio.

Questa sezione fornisce modelli di implementazione comuni per i collegamenti diretti. La configurazione esatta dipende dall’architettura dell’app e dal framework di routing.

### iOS (collegamenti universali) {#ios-implementation}

1. In Xcode, seleziona la destinazione tramite **[!UICONTROL Firma e funzionalità]** > **[!UICONTROL + funzionalità]** > **[!UICONTROL Domini associati]**.
1. Aggiungi voci per i sottodomini delegati, ad esempio:

   ```text
   applinks:www.mybusiness.com
   applinks:data.email.mybusiness.com
   ```

1. Gestisci i collegamenti universali nell’app e ottieni il collegamento originale dall’intestazione di risposta.

   +++ Esempio: iOS 13+ con scene

   ```swift
   class SceneDelegate: UIResponder, UIWindowSceneDelegate {
   
       func scene(_ scene: UIScene,
                 continue userActivity: NSUserActivity) {
           guard userActivity.activityType == NSUserActivityTypeBrowsingWeb,
                 let incomingURL = userActivity.webpageURL else {
               return
           }
   
           handleUniversalLink(url: incomingURL)
       }
   
       private func handleUniversalLink(url: URL) {
           // Only handle AJO tracked mobile clicks
           guard url.host == "data.email.mybusiness.com",
                 url.path.hasPrefix("/ee/v1/mclick") else {
               // Could also handle direct www.mybusiness.com links here
               return
           }
   
           resolveTrackedUrlAndRoute(url)
       }
   
       private func resolveTrackedUrlAndRoute(_ trackedUrl: URL) {
           var request = URLRequest(url: trackedUrl)
           request.httpMethod = "GET"
   
           URLSession.shared.dataTask(with: request) { _, response, error in
               guard error == nil,
                     let httpResponse = response as? HTTPURLResponse,
                     let locationValue = httpResponse.allHeaderFields["Location"] as? String,
                     let finalUrl = URL(string: locationValue) else {
                   return
               }
   
               DispatchQueue.main.async {
                   self.routeToDestination(finalUrl)
               }
           }.resume()
       }
   
       private func routeToDestination(_ url: URL) {
           // Example: map URL paths to screens
           // https://www.mybusiness.com/dashboard/offers/coupons
           // → OffersViewController for Coupons
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>L&#39;app deve eseguire un **GET** sull&#39;URL `mclick` e leggere l&#39;intestazione **`Location`**, quindi indirizzare in base all&#39;URL **final**.
>
>Non aprire semplicemente l&#39;URL `mclick` in Safari; in questo modo si vanifica lo scopo del deep linking.

### Android (collegamenti alle app) {#android-implementation}

1. Aggiungi il filtro delle finalità del collegamento all’app nell’app Android.

   ```xml
   <activity
       android:name=".DeepLinkActivity"
       android:exported="true">
   
       <intent-filter android:autoVerify="true">
           <action android:name="android.intent.action.VIEW" />
           <category android:name="android.intent.category.DEFAULT" />
           <category android:name="android.intent.category.BROWSABLE" />
   
           <data
               android:scheme="https"
               android:host="data.email.mybusiness.com"
               android:pathPrefix="/ee/v1/mclick" />
       </intent-filter>
   
   </activity>
   ```

1. Implementa il gestore di collegamenti profondi.

   +++ A Cotlino:

   ```kotlin
   class DeepLinkActivity : AppCompatActivity() {
   
       override fun onCreate(savedInstanceState: Bundle?) {
           super.onCreate(savedInstanceState)
   
           val trackedUri = intent?.data
           if (trackedUri == null ||
               trackedUri.host != "data.email.mybusiness.com" ||
               !trackedUri.path.orEmpty().startsWith("/ee/v1/mclick")) {
               finish()
               return
           }
   
           resolveTrackedUrlAndRoute(trackedUri)
       }
   
       private fun resolveTrackedUrlAndRoute(trackedUri: Uri) {
           lifecycleScope.launch(Dispatchers.IO) {
               try {
                   val finalUrl = followRedirect(trackedUri.toString())
                   withContext(Dispatchers.Main) {
                       routeToDestination(finalUrl)
                       finish()
                   }
               } catch (e: Exception) {
                   // Optionally log error, fallback to browser
                   finish()
               }
           }
       }
   
       private fun followRedirect(trackedUrl: String): Uri {
           val client = OkHttpClient.Builder()
               .followRedirects(false) // We want to read Location ourselves
               .build()
   
           val request = Request.Builder()
               .url(trackedUrl)
               .get()
               .build()
   
           client.newCall(request).execute().use { response ->
               val location = response.header("Location")
                   ?: throw IllegalStateException("Missing Location header")
               return Uri.parse(location)
           }
       }
   
       private fun routeToDestination(finalUri: Uri) {
           // Example: interpret https://www.mybusiness.com/dashboard/offers/coupons
           // and open the correct Activity / Fragment
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>Come iOS, l&#39;app deve chiamare l&#39;URL `mclick` e utilizzare l&#39;intestazione **`Location`** per determinare la destinazione finale.
>
>Utilizza `followRedirects(false)` per controllare la gestione dei reindirizzamenti e registrare accuratamente le analisi se necessario.
>
>La logica di indirizzamento è specifica per l’app; definisci una chiara mappatura dagli URL alle schermate.

## Procedure consigliate {#deeplink-best-practices}

* **Usa percorsi stabili**: preferisci route resilienti alle modifiche dell&#39;interfaccia utente dell&#39;app (ad esempio `/account/orders` anziché `/tab/3/view/2`).
* **Account per percorsi tracciati**: quando è abilitato il tracciamento dei collegamenti, il collegamento su cui è stato fatto clic può utilizzare modelli di percorsi tracciati (ad esempio `/ee/v1/mclick/`). Assicurati che il router possa analizzare l’URL finale dopo aver risolto il collegamento tracciato.
* **Mantieni i parametri prevedibili**: definisci uno schema di parametri coerente (ad esempio `?orderId=12345`).
* **Evita di inserire dati sensibili negli URL**: non inserire segreti o dati personali direttamente nell&#39;URL del collegamento diretto.
* **Verifica il collegamento diretto**: invia una bozza e fai clic sul collegamento diretto in un dispositivo in cui è installata l&#39;app.
* **Convalida su dispositivi reali**: i collegamenti universali e i comportamenti di risoluzione dei collegamenti tracciati sono più affidabili per la convalida su dispositivi fisici anziché su simulatori.
* **Convalida il routing lato app**: se il collegamento diretto non apre la schermata prevista, convalida il routing lato app e il formato URL (host/percorso/query e codifica URL).
* **Tieni presente l&#39;inizializzazione dell&#39;app**: il comportamento Collegamenti app/Collegamenti universali è più affidabile dopo che l&#39;app è stata installata e aperta almeno una volta.

## Risoluzione dei problemi e domande frequenti {#troubleshooting-faq}

+++ L&#39;app non si apre quando tocco il collegamento profondo.

* Verificare che l&#39;URL corrisponda ai pattern di host e percorso che l&#39;app è registrata per gestire, inclusi i percorsi di clic tracciati quando è abilitato il tracciamento dei collegamenti (ad esempio, percorsi in `/ee/v1/mclick/`).
* Per i collegamenti universali iOS e i collegamenti alle app Android, l&#39;associazione del dominio (AASA / `assetlinks.json`) è configurata correttamente ed è raggiungibile.
* Eseguire il test su un dispositivo reale (i simulatori/emulatori possono comportarsi in modo diverso per l’associazione dei collegamenti).

+++

+++ L’app si apre ma non passa alla schermata prevista.

* Conferma che il router lato app analizzi correttamente il percorso/query dell’URL.
* Verifica codifica URL: i caratteri riservati devono essere codificati in URL.
* Verificare che i nomi e i valori dei parametri corrispondano a quanto previsto dal router.

+++

+++ Cosa succede se l’app non è installata?

* Se lo stesso URL HTTPS può essere servito dal sito web, il collegamento può aprire una pagina web come fallback quando l’app non è installata (configura di conseguenza la destinazione web e il routing).

+++

+++ Come posso includere in modo sicuro i caratteri speciali nei parametri?

Valori dei parametri di query con codifica URL. Questo riduce i problemi di consegna e rendering e aiuta a prevenire gli errori di analisi nell’app.

+++

+++ Come dovremmo eseguire il test end-to-end?

* Crea una bozza con un deep link, fai clic su di essa sui dispositivi iOS e Android (scenari installati e non installati).
* Convalida:
   * Il valore finale del collegamento e-mail o SMS (host/percorso/query)
   * Associazione a livello di sistema operativo (se si utilizzano collegamenti universali/collegamenti alle app)
   * Risultato del routing in-app

+++

+++ Ho un’app ma diversi sottodomini per l’organizzazione. Devo richiedere la creazione di AASA e assetLinks.json per ogni sottodominio?

Sì. Se desideri un deep link su ogni sottodominio delegato, richiedi la configurazione di AASA e `assetlinks.json` per ogni sottodominio che deve supportare la funzione.

+++

+++ L&#39;URL configurato deve utilizzare un formato di collegamento diretto (ad esempio `appname://path`)?

È possibile utilizzare uno schema URL personalizzato (ad esempio `appname://path`), ma l&#39;approccio consigliato è un collegamento universale o un collegamento all&#39;app (`https://`), che corrisponde alla configurazione basata su HTTPS nelle sezioni di configurazione e implementazione di questa pagina.

+++

+++ I parametri UTM sull’URL saranno disponibili nell’app mobile per l’analisi?

Sì. I parametri UTM configurati in [!DNL Journey Optimizer] sono inclusi nell&#39;URL finale restituito nell&#39;intestazione `Location` quando l&#39;app esegue un GET sull&#39;URL `mclick`, quindi puoi utilizzarli per l&#39;analisi in-app.

+++

+++ Qual è l&#39;esperienza utente per `/ee/v1/click/` URL?

Il collegamento viene aperto nel browser Web predefinito del dispositivo (comportamento standard di tracciamento dei clic), anziché essere gestito come collegamento profondo nell&#39;app tramite il flusso `mclick` descritto in questa pagina.

+++
