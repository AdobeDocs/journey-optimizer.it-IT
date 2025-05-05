---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider personalizzato
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con un provider personalizzato
feature: SMS, Channel Configuration
badge: label="Beta" type="Informative"
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 201d7d367540f7b36f27ca4a09b6f0ce12e3e22f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 27%

---

# Configurare un provider personalizzato {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="URL del provider"
>abstract="Specifica l’URL dell’API esterna a cui intendi connetterti. Questo URL funge da endpoint per accedere alle funzioni e alle funzionalità dell’API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Tipo di autenticazione"
>abstract="Specifica il metodo di autenticazione necessario per accedere all’API, ad esempio token OAuth o Bearer. Questo garantisce una comunicazione sicura e autorizzata con il servizio esterno."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="Parametri per intestazione"
>abstract="Specifica l’etichetta, il tipo e il valore delle intestazioni aggiuntive per consentire la corretta autenticazione, la formattazione del contenuto e una comunicazione API efficace. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="Payload del provider"
>abstract="Fornisci il payload richiesto per garantire che vengano inviati i dati corretti per l’elaborazione e la generazione di risposte."

>[!AVAILABILITY]
>
>I provider personalizzati sono attualmente disponibili come versione beta solo per gli utenti selezionati. Contatta il tuo rappresentante Adobe per essere incluso in Beta.
>
>Tieni presente che questo Beta non supporta i messaggi in entrata per la gestione del consenso e la generazione di rapporti sulla consegna di consenso o rinuncia.

Per inviare messaggi in Journey Optimizer utilizzando un provider personalizzato non disponibile come predefinito da Adobe (ad esempio Sinch, Infobip, Twilio), procedi come segue:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona il menu **[!UICONTROL Credenziali API]**.

1. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

   ![](assets/sms_byo_1.png)

1. Configura le credenziali API SMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: personalizzato.

   * **[!UICONTROL Nome]**: immetti un nome per le credenziali API.

   * **[!UICONTROL Provider AppId]**: immetti l&#39;ID applicazione fornito dal provider SMS.

   * **[!UICONTROL Nome provider]**: immetti il nome del provider SMS.

   * **[!UICONTROL URL provider]**: immetti l&#39;URL del provider SMS.

   * **[!UICONTROL Tipo di autenticazione&#x200B;]**: seleziona il tipo di autorizzazione. I tipi di autorizzazione supportati sono **Bearer App** o **Basic**.

   * **[!UICONTROL Token API]**: immetti il token API fornito dal provider SMS.

   * **[!UICONTROL Payload provider]**: aggiungi il payload provider, ad esempio `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`.

     Assicurarsi che il payload includa `{{toNumber}}`, `{{fromNumber}}`, `{{message}}`.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una superficie di canale per i messaggi SMS. [Ulteriori informazioni](sms-configuration-surface.md)

Una volta configurata, puoi sfruttare tutte le funzionalità di canale predefinite, come l’authoring dei messaggi, la personalizzazione, il tracciamento dei collegamenti e il reporting.

## Video introduttivo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3443614?captions=ita)
