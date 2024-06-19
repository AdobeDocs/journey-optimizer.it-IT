---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Twilio
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 4%

---

# Configurare il provider Twilio {#sms-configuration-twilio}

Per configurare Twilio con Journey Optimizer, è necessario creare una nuova credenziale API utilizzata per Twilio:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona la **[!UICONTROL Credenziali API]** menu. Fai clic su **[!UICONTROL Crea nuove credenziali API]** pulsante.

1. Configura le credenziali API SMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: Twilio.

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL SID account]** e **[!UICONTROL Token di autenticazione]**: accedi a **Informazioni account** per trovare le credenziali.

   * **[!UICONTROL SID messaggio]**: inserisci l’identificatore univoco assegnato a ogni messaggio creato dall’API di Twilio. Ulteriori informazioni in [Documentazione di Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Numero in entrata]**: aggiungi il tuo numero univoco in entrata. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata.

1. Clic **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una superficie di canale per i messaggi SMS e MMS. [Ulteriori informazioni](sms-configuration-surface.md)
