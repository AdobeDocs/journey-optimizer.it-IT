---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider personalizzato
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con un provider personalizzato
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 37313ca8a9527c934d8aeaf265e9674219726636
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 9%

---

# Configurare un provider SMS personalizzato {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="URL del provider"
>abstract="Specifica l’URL dell’API esterna a cui intendi connetterti. Questo URL funge da endpoint per accedere alle funzioni e alle funzionalità dell’API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="Parametri per intestazione"
>abstract="Specifica l’etichetta, il tipo e il valore delle intestazioni aggiuntive per consentire la corretta autenticazione, la formattazione del contenuto e una comunicazione API efficace. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="Payload del provider"
>abstract="Fornisci il payload richiesto per garantire che vengano inviati i dati corretti per l’elaborazione e la generazione di risposte."

Questa funzione ti consente di integrare e configurare i tuoi provider SMS, offrendo flessibilità oltre i provider predefiniti (Sinch, Twilio e Infobip). Questo consente di gestire in modo semplice l’authoring, la distribuzione, il reporting e il consenso degli SMS.

Con la configurazione del provider personalizzato per SMS, puoi configurare provider SMS personalizzati direttamente in Journey Optimizer, utilizzare la personalizzazione avanzata del payload per la messaggistica dinamica e gestire le preferenze di consenso (consenso/rinuncia) per garantire la conformità.

Per configurare il provider SMS personalizzato, effettua le seguenti operazioni:

1. [Crea credenziali API](#api-credential)
1. [Crea webhook](#webhook)
1. [Crea configurazione canale](sms-configuration-surface.md)
1. [Creare un Percorso o una campagna con un’azione del canale SMS](create-sms.md)

## Creare le credenziali API {#api-credential}

Per inviare messaggi in Journey Optimizer utilizzando un provider personalizzato non disponibile come predefinito da Adobe (ad esempio Sinch, Infobip, Twilio), procedi come segue:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]**, seleziona il menu **[!UICONTROL Credenziali API]** in **[!UICONTROL Impostazioni SMS]** e fai clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

   ![](assets/sms_byo_1.png)

1. Configura le credenziali API SMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: personalizzato.

   * **[!UICONTROL Nome]**: immetti un nome per le credenziali API.

   * **[!UICONTROL Provider AppId]**: immetti l&#39;ID applicazione fornito dal provider SMS.

   * **[!UICONTROL Nome provider]**: immetti il nome del provider SMS.

   * **[!UICONTROL URL provider]**: immetti l&#39;URL del provider SMS.

   * **[!UICONTROL Tipo di autenticazione&#x200B;]**: seleziona il tipo di autorizzazione e [completa i campi corrispondenti](#auth-options) in base al metodo di autenticazione scelto.

     ![](assets/sms-byop.png)

1. Nella sezione **[!UICONTROL Intestazioni]**, fai clic su **[!UICONTROL Aggiungi nuovo parametro]** per specificare le intestazioni HTTP per il messaggio di richiesta che verrà inviato al servizio esterno.

   I campi di intestazione **Content-Type** e **Charset** sono impostati per impostazione predefinita e non possono essere eliminati.

   ![](assets/sms_byo_2.png)

1. Aggiungi il **[!UICONTROL Payload provider]** per convalidare e personalizzare i payload della richiesta.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona ![raccoglitore](assets/do-not-localize/Smock_Delete_18_N.svg) per eliminare le credenziali API.

   ![](assets/sms_byo_3.png)

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

   ![](assets/sms_byo_4.png)

Dopo aver creato e configurato le credenziali API, devi ora impostare [le impostazioni in entrata per il webhook](#webhook) per i messaggi SMS.

### Opzioni di autenticazione per i provider SMS personalizzati {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Tipo di autenticazione"
>abstract="Specifica il metodo di autenticazione necessario per accedere all’API; in questo modo viene garantita una comunicazione sicura e autorizzata con il servizio esterno."

>[!BEGINTABS]

>[!TAB Chiave API]

Una volta create le credenziali API, completa i campi necessari per l’autenticazione della chiave API:

* **[!UICONTROL Nome]**&#x200B;: immetti un nome per la configurazione della chiave API.
* **[!UICONTROL Token API]**&#x200B;: immetti il token API fornito dal provider SMS.

![](assets/sms-byop-api-key.png)

>[!TAB Autenticazione MAC]

Una volta create le credenziali API, completa i campi richiesti per l’autenticazione MAC:

* **[!UICONTROL Nome]**&#x200B;: immetti un nome per la configurazione dell&#39;autenticazione MAC.
* **[!UICONTROL Token API]**&#x200B;: immetti il token API fornito dal provider SMS.
* **[!UICONTROL Chiave segreta API]**: immetti la chiave segreta API fornita dal provider SMS. Questa chiave viene utilizzata per generare il MAC (Message Authentication Code) per le comunicazioni protette.
* **[!UICONTROL Formato hash di autorizzazione Mac]**: scegliere il formato hash per l&#39;autenticazione MAC.

![](assets/sms-byop-mac.png)

>[!TAB Autenticazione OAuth]

Una volta create le credenziali API, completa i campi necessari per l’autenticazione OAuth:

* **[!UICONTROL Nome]**&#x200B;: immetti un nome per la configurazione dell&#39;autenticazione OAuth.

* **[!UICONTROL Token API]**&#x200B;: immetti il token API fornito dal provider SMS.

* **[!UICONTROL URL OAuth]**&#x200B;: immetti l&#39;URL per ottenere il token OAuth.

* **[!UICONTROL Corpo OAuth]**&#x200B;: fornisci il corpo della richiesta OAuth in formato JSON, inclusi parametri come `grant_type`, `client_id` e `client_secret`.

![](assets/sms-byop-oauth.png)

>[!TAB Autenticazione JWT]

Una volta create le credenziali API, completa i campi richiesti per l’autenticazione JWT:

* **[!UICONTROL Nome]**&#x200B;: immetti un nome per la configurazione dell&#39;autenticazione JWT.

* **[!UICONTROL Token API]**&#x200B;: immetti il token API fornito dal provider SMS.

* **[!UICONTROL Payload JWT]**&#x200B;: inserisci il payload JSON contenente le attestazioni richieste per JWT, ad esempio emittente, oggetto, pubblico e scadenza.

![](assets/sms-byop-jwt.png)

>[!ENDTABS]

## Crea webhook {#webhook}

>[!BEGINSHADEBOX]

Se non vengono fornite parole chiave di consenso o rinuncia, vengono utilizzati messaggi di consenso standard per rispettare la privacy dell’utente. L&#39;aggiunta di parole chiave personalizzate sostituisce automaticamente le impostazioni predefinite.

**Parole chiave predefinite:**

* **Consenso**: SOTTOSCRIVI, SÌ, RIPRENDI, AVVIA, CONTINUA, RIPRENDI, INIZIA
* **Rinuncia**: INTERROMPI, ESCI, ANNULLA, TERMINA, ANNULLA ISCRIZIONE, NO
* **Guida**: GUIDA

>[!ENDSHADEBOX]

Una volta create correttamente le credenziali API, il passaggio successivo consiste nel creare un webhook e configurare le impostazioni in entrata. Questa configurazione garantisce che il sistema possa ricevere ed elaborare correttamente i dati o i messaggi in arrivo.

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]**, seleziona il menu **[!UICONTROL Webhook SMS]** in **[!UICONTROL Impostazioni SMS]** e fai clic sul pulsante **[!UICONTROL Crea webhook]**.

   ![](assets/sms_byo_5.png)

1. Configura le impostazioni del webhook come descritto di seguito:

   * **[!UICONTROL Name]**: immetti un nome per il webhook.

   * **[!UICONTROL Seleziona fornitore SMS]**: personalizzato.

   * **[!UICONTROL Seleziona credenziali API]**: scegli dall&#39;elenco a discesa [le credenziali API configurate in precedenza](#api-credential).

   * **[!UICONTROL Parole chiave di consenso]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il messaggio di consenso. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio Opt-in]**: immetti la risposta personalizzata inviata automaticamente come messaggio Opt-in.

   * **[!UICONTROL Parole chiave di rinuncia]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il messaggio di rinuncia. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di rinuncia]**: immetti la risposta personalizzata inviata automaticamente come messaggio di rinuncia.

   ![](assets/sms_byo_6.png)

1. Fai clic su **[!UICONTROL Visualizza editor payload]** per convalidare e personalizzare i payload della richiesta.

   Puoi personalizzare dinamicamente il payload utilizzando gli attributi del profilo e garantire che vengano inviati dati accurati per l’elaborazione e la generazione di risposte con l’aiuto di funzioni di assistenza integrate.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione del webhook.

1. Nel menu **[!UICONTROL Webhook]**, fai clic sull&#39;icona ![bin](assets/do-not-localize/Smock_Delete_18_N.svg) per eliminare il tuo webhook.

1. Per modificare la configurazione esistente, individuare il webhook desiderato e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

1. Accedi e copia il nuovo **[!UICONTROL URL webhook]** dal **[!UICONTROL webhook]** inviato in precedenza.

   ![](assets/sms_byo_7.png)

Dopo aver creato e configurato le impostazioni in entrata per il webhook, è ora necessario creare una [configurazione del canale](sms-configuration-surface.md) per i messaggi SMS.

Una volta configurata, puoi sfruttare tutte le funzionalità di canale predefinite, come l’authoring dei messaggi, la personalizzazione, il tracciamento dei collegamenti e il reporting.

## Video dimostrativo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)

