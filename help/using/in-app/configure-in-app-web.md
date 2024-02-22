---
title: Creare un messaggio Web in-app in Journey Optimizer
description: Scopri come creare un messaggio in-app web in Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, inizio
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 2%

---


# Configurare il canale Web in-app {#configure-in-app-web}

## Prerequisiti {#prerequisites}

* Assicurati di utilizzare la versione più recente per **Adobe Experience Platform Web SDK** estensione.

* Installare **Adobe Experience Platform Web SDK** estensione nel tuo **Proprietà tag** e abilita **Archiviazione per personalizzazione** opzione.

  Questa configurazione è essenziale per l’archiviazione della cronologia degli eventi sul client, un prerequisito per l’implementazione delle Regole di frequenza nel Generatore di regole. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## Configurare la regola Dati inviati alla piattaforma {#configure-sent-data-trigger}

1. Accedi al tuo **Raccolta dati di Adobe Experience Platform** e passa a **Proprietà tag** configurato con **Adobe Experience Platform Web SDK** estensione.

1. Dalla sezione **Authoring** menu, seleziona **Regole** allora **Crea nuova regola** o **Aggiungi regola**.

   ![](assets/configure_web_inapp_2.png)

1. In **Eventi** , fare clic su **Aggiungi** e configuralo come segue:

   * **Estensione**: Core

   * **Tipo di evento**: Libreria caricata (parte superiore della pagina).

   ![](assets/configure_web_inapp_3.png)

1. Clic **Mantieni modifiche** per salvare la configurazione dell’evento.

1. In **Azioni** , fare clic su **Aggiungi** e configuralo come segue:

   * **Estensione**: Adobe Experience Platform Web SDK

   * **Tipo di azione**: invia evento

   ![](assets/configure_web_inapp_4.png)

1. In **Personalizzazione** sezione del tuo **Azione** tipo, abilita **Eseguire il rendering delle decisioni di personalizzazione visiva** opzione.

   ![](assets/configure_web_inapp_5.png)

1. In **Contesto decisionale** , definire la sezione **Chiave** e **Valore** coppie che determinano quale esperienza distribuire.

   ![](assets/configure_web_inapp_6.png)

1. Salva **Azione** configurazione facendo clic su **Mantieni modifiche**.

1. Accedi a **Flusso di pubblicazione** menu. Crea un nuovo **Libreria** o seleziona un elemento esistente **Libreria** e aggiungi il nuovo **Regola** ad esso. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Dal tuo **Libreria**, seleziona **Salva e genera in sviluppo**.

   ![](assets/configure_web_inapp_7.png)

## Configura regola manuale {#configure-manual-trigger}

1. Accedi al tuo **Raccolta dati di Adobe Experience Platform** e passa a **Proprietà tag** configurato con **Adobe Experience Platform Web SDK** estensione.

1. Dalla sezione **Authoring** menu, seleziona **Regole** allora **Crea nuova regola** o **Aggiungi regola**.

   ![](assets/configure_web_inapp_8.png)

1. In **Eventi** , fare clic su **Aggiungi** e configuralo come segue:

   * **Estensione**: Core

   * **Tipo di evento**: fai clic

   ![](assets/configure_web_inapp_9.png)

1. In **Configurazione clic**, definisci **Selettore** che verrà valutata.

   ![](assets/configure_web_inapp_10.png)

1. Clic **Mantieni modifiche** per salvare **Evento** configurazione.

1. In **Azioni** , fare clic su **Aggiungi** e configuralo come segue:

   * **Estensione**: Adobe Experience Platform Web SDK

   * **Tipo di azione**: valuta i set di regole

   ![](assets/configure_web_inapp_11.png)

1. In **Azione Valuta set di regole** sezione del tuo **Azione** tipo, abilita **Eseguire il rendering delle decisioni di personalizzazione visiva** opzione.

   ![](assets/configure_web_inapp_13.png)

1. In **Contesto decisionale** , definire la sezione **Chiave** e **Valore** coppie che determinano quale esperienza distribuire.

1. Accedere a **Flusso di pubblicazione** , crea un nuovo **Libreria** o seleziona un elemento esistente **Libreria** e aggiungi il nuovo **Regola**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Dal tuo **Libreria**, seleziona **Salva e genera in sviluppo**.

   ![](assets/configure_web_inapp_14.png)

