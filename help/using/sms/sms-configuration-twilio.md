---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Twilio
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# Configurare il provider Twilio {#sms-configuration-twilio}

Per configurare Twilio con Journey Optimizer, è necessario creare una nuova credenziale API utilizzata per Twilio:

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

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS e MMS. [Ulteriori informazioni](sms-configuration-surface.md)
