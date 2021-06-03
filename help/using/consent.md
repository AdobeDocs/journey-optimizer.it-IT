---
title: Gestire la rinuncia
description: Scopri come gestire la rinuncia e la privacy
source-git-commit: 738d72e8f3ba204219086f19252220ff833369cb
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 1%

---

# Gestire la rinuncia {#consent}

![](assets/do-not-localize/badge.png)

Utilizza [!DNL Journey Optimizer] per tenere traccia del consenso dei destinatari alla comunicazione e capire in che modo desiderano interagire con il tuo marchio gestendo le loro preferenze e abbonamenti. <!--Their preferences and subscriptions are handled through Consent management.-->

Regolamenti come il RGPD stabiliscono che devi soddisfare requisiti specifici prima di poter utilizzare le informazioni degli interessati. Inoltre, gli interessati dovrebbero poter modificare il loro consenso in qualsiasi momento.

**Perché è importante?**

* Il mancato rispetto di queste normative introduce rischi legali normativi per il tuo marchio.
* Ti aiuta a evitare l’invio di comunicazioni non richieste ai destinatari, il che potrebbe far sì che contrassegnino i tuoi messaggi come spam e danneggino la tua reputazione.

Ulteriori informazioni sulla gestione della privacy e sulle normative applicabili nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=it).

<!--* Recipients should be able to opt-in/opt-out from receiving electronic communication through one or more channel
* Recipients expect the brand to offer preference centre capability that controls how brand should engage with them (example: channel of communication, invasive and non-invasive tracking etc). This helps to fulfil regulatory obligations and also facilitates quality engagement with recipient. 
* The third category is the capability to offer subscription to recipients (newsletter, etc)-->

## Gestione delle rinunce {#opt-out-management}

Fornire ai destinatari la possibilità di annullare l’iscrizione alla ricezione di comunicazioni da un marchio è un requisito legale. Ulteriori informazioni sulla legislazione applicabile sono disponibili nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=en#regulations).

Pertanto, devi sempre includere un **collegamento per l’annullamento dell’abbonamento** in ogni e-mail inviata ai destinatari:
* Facendo clic su questo collegamento, i destinatari verranno indirizzati a una pagina di destinazione con un pulsante per confermare la rinuncia.
* Facendo clic sul pulsante di rinuncia, viene effettuata un Adobe I/O di chiamata per aggiornare i dati del profilo con queste informazioni. [Ulteriori informazioni](#consent-service-api).

Per aggiungere un collegamento per l’annullamento dell’abbonamento, effettua le seguenti operazioni:

1. Crea la pagina di destinazione per l’annullamento dell’abbonamento.
1. Ospita la pagina di destinazione nel sistema di terze parti desiderato.
1. [Crea un ](../../help/using/create-message.md) messaggio  [!DNL Journey Optimizer].

   <!--The link to your landing page should contain a static URL and the profile ID.-->

1. Seleziona il testo nel contenuto e inserisci un collegamento utilizzando la barra degli strumenti contestuale.

   ![](assets/opt-out-insert-link.png)

1. Seleziona **[!UICONTROL Unsubscription link]** dall&#39;elenco a discesa **[!UICONTROL Link type]**.

   ![](assets/opt-out-link-type.png)

1. Nel frame **[!UICONTROL Unsubscription page URL]** , copia il collegamento alla pagina di destinazione.

   ![](assets/opt-out-link-url.png)

1. Fai clic su **[!UICONTROL Save]**.

1. Salva il contenuto e [pubblica il messaggio](../../help/using/publish-manage-message.md).

   >[!NOTE]
   >
   >L’URL della pagina di destinazione di terze parti includerà tre parametri che verranno utilizzati per aggiornare le preferenze dei profili tramite una chiamata di Adobe I/O. &#x200B; [Ulteriori informazioni in questa sezione](#consent-service-api).

1. Invia il messaggio con il collegamento alla pagina di destinazione tramite un [percorso](building-journeys/journey.md).

1. Una volta ricevuto il messaggio, se il destinatario fa clic sul collegamento di annullamento dell’abbonamento, viene visualizzata la pagina di destinazione.

   ![](assets/opt-out-lp-example.png)

1. Se il destinatario fa clic sul pulsante di rinuncia nella pagina di destinazione (qui, il pulsante **Annulla sottoscrizione**), i dati del profilo vengono aggiornati tramite una chiamata di Adobe I/O [](#opt-out-api).

   Il destinatario con rinuncia viene quindi reindirizzato a una schermata di messaggio di conferma che indica che la rinuncia è avvenuta con successo.

   ![](assets/opt-out-confirmation-example.png)

   Di conseguenza, questo utente non riceverà comunicazioni dal tuo marchio a meno che non abbia effettuato nuovamente l’abbonamento.

Per verificare che la scelta del profilo corrispondente sia stata aggiornata, passa ad Experience Platform e accedi al profilo selezionando uno spazio dei nomi di identità e un valore di identità corrispondente. Ulteriori informazioni sono disponibili nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=en#getting-started).

![](assets/opt-out-profile-choice.png)

Nella scheda **[!UICONTROL Attributes]** , puoi vedere che il valore di **[!UICONTROL choice]** è stato modificato in **[!UICONTROL no]**.

<!--The opt-out URL is resolved upon each recipient receiving the message. It is then personalized with the relevant encrypted parameters (profile ID, profile name, journey ID, sandbox ID, and message execution ID).-->

## Chiamata API per rinuncia {#opt-out-api}

Una volta che il destinatario ha rinunciato facendo clic sul collegamento di annullamento dell’abbonamento, viene chiamata un’API di Adobe I/O <!--Consent service API to capture the encrypted data and-->per aggiornare le preferenze del profilo corrispondente.

Questo Adobe I/O di chiamata POST è il seguente:

Endpoint: cjm.adobe.io/imp/consent/preferences

Parametri query:
* **parametri**: contiene il payload crittografato
* **sig**: signature  <!--which signature?-->
* **pid**: ID profilo crittografato

Questi parametri sono disponibili dal collegamento di annullamento dell’abbonamento inviato al destinatario, ovvero l’URL che aprirà la pagina di destinazione di terze parti per un determinato destinatario:

![](assets/opt-out-parameters.png)

<!--QUESTION: How do you get the URL built for each recipient? Do you have to wait until each targeted recipient receives the unsubscribe link or can you deduce it in advance? Is it done automatically upon the API call or do you have to do something manually for each profile? In other words will the LP automatically include the 3 parameters or do you have to insert something manually? Still not completely clear-->

Requisiti dell’intestazione:
* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorizzazione (token utente dal tuo account tecnico) <!--How do you find this information? And other header elements?-->

Corpo della richiesta:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

<!--The Consent service /-->[!DNL Journey Optimizer] will <!--decrypt and-->use these parameters to update the corresponding profile's choice. <!--and provide an answer back to the landing page.-->

## Gestione della rinuncia push {#push-opt-out-management}

I destinatari push possono annullare l’iscrizione tramite i propri dispositivi.

Ad esempio, al momento del download o dell’utilizzo dell’app, possono scegliere di interrompere le notifiche. Analogamente, possono modificare le impostazioni di notifica tramite il sistema operativo mobile.
