---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Twilio
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 2%

---

# Configurare il provider Twilio {#sms-configuration-twilio}

## Configurare le credenziali API per SMS/MMS

Per configurare Twilio con Journey Optimizer, è necessario creare nuove credenziali API per Twilio:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** `>` **[!UICONTROL Impostazioni SMS]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API SMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: Twilio.

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL SID account]** e **[!UICONTROL Token autenticazione]**: accedere al riquadro **Informazioni account** della pagina del dashboard di Twilio Console per trovare le credenziali.

   * **[!UICONTROL SID messaggio]**: immettere l&#39;identificatore univoco assegnato a ogni messaggio creato dall&#39;API di Twilio. Ulteriori informazioni sono disponibili nella [documentazione di Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Numero in entrata]**: aggiungi il tuo numero univoco in entrata. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

1. Fai clic su **[!UICONTROL Verifica connessione SMS]**, dalle credenziali API esistenti, per verificare le credenziali API SMS inviando un messaggio di esempio a un dispositivo designato.

1. Compila i campi **Numero** e **Messaggio** e fai clic su **[!UICONTROL Verifica connessione]**.

   >[!IMPORTANT]
   >
   >Il messaggio deve essere strutturato in modo da essere allineato al formato di payload del provider.

   ![](assets/verify-connection.png)

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS e MMS. [Ulteriori informazioni](sms-configuration-surface.md)

## Configurare le credenziali API per RCS

La messaggistica RCS è supportata in Adobe Journey Optimizer tramite Twilio utilizzando la funzionalità [Provider SMS personalizzato](sms-configuration-custom.md). Ciò consente la distribuzione di messaggi avanzati e interattivi tramite profili aziendali verificati, incorporando elementi quali caroselli, pulsanti e contenuti multimediali.

➡️ [Scopri come Twilio supporta RCS nella documentazione di Twilio](https://www.twilio.com/docs/rcs)

Per abilitare la messaggistica RCS con Twilio, è necessario configurare le nuove credenziali API tramite un provider SMS personalizzato. Le credenziali SMS Twilio esistenti non sono compatibili, in quanto RCS richiede un formato di payload distinto.

Per configurare RCS con Twilio:

1. **Registrati per ricevere messaggi RCS in Twilio**

   Inizia completando il processo di registrazione RCS nella piattaforma Twilio. Ciò include la configurazione del profilo aziendale e l’abilitazione delle funzionalità RCS per il tuo account.

1. **Creare un webhook SMS**

   [Configura un webhook SMS](sms-configuration-custom.md#webhook) in grado di ricevere le risposte ai messaggi RCS in arrivo o gli aggiornamenti di consegna. Questo webhook deve essere collegato correttamente alla configurazione Twilio per la comunicazione bidirezionale.

1. **Crea credenziali API utilizzando Personalizzato come fornitore SMS**

   In Journey Optimizer, [definisci nuove credenziali API](sms-configuration-custom.md#api-credential) specificatamente per RCS utilizzando &quot;Personalizzato&quot; come fornitore di SMS. Utilizza il metodo di autenticazione dell’endpoint RCS appropriato, l’URL di base e le intestazioni.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi RCS. [Ulteriori informazioni](sms-configuration-surface.md)







