---
solution: Journey Optimizer
product: journey optimizer
title: Configura provider Twilio
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 1%

---

# Configura provider Twilio {#sms-configuration-twilio}

Per configurare Twilio con Journey Optimizer, è necessario creare una nuova credenziale API utilizzata per Twilio:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona la **[!UICONTROL Credenziali API]** menu. Fai clic su **[!UICONTROL Crea nuove credenziali API]** pulsante.

   ![](assets/sms_6.png)

1. Configura le credenziali API SMS, come descritto di seguito:

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL SID account]** e **[!UICONTROL Token di autenticazione]**: accedi a **Informazioni account** per trovare le credenziali.

   * **[!UICONTROL SID messaggio]**: inserisci l’identificatore univoco assegnato a ogni messaggio creato dall’API di Twilio. Ulteriori informazioni in [Documentazione di Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. Clic **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una superficie di canale per i messaggi SMS e MMS. [Ulteriori informazioni](sms-configuration-surface.md)

