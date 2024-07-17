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

* Assicurati di utilizzare la versione più recente per l&#39;estensione **Adobe Experience Platform Web SDK**.

* Installa l&#39;estensione **Adobe Experience Platform Web SDK** nelle **proprietà tag** e abilita l&#39;opzione **Personalization Storage**.

  Questa configurazione è essenziale per l’archiviazione della cronologia degli eventi sul client, un prerequisito per l’implementazione delle Regole di frequenza nel Generatore di regole. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## Configurare la regola Dati inviati alla piattaforma {#configure-sent-data-trigger}

1. Accedi all&#39;istanza di **Adobe Experience Platform Data Collection** e passa a **Tag Properties** configurate con l&#39;estensione **Adobe Experience Platform Web SDK**.

1. Dal menu **Authoring**, seleziona **Regole**, quindi **Crea nuova regola** o **Aggiungi regola**.

   ![](assets/configure_web_inapp_2.png)

1. Nella sezione **Eventi**, fai clic su **Aggiungi** e configuralo come segue:

   * **Estensione**: Core

   * **Tipo evento**: libreria caricata (parte superiore della pagina).

   ![](assets/configure_web_inapp_3.png)

1. Fai clic su **Mantieni modifiche** per salvare la configurazione dell&#39;evento.

1. Nella sezione **Azioni**, fai clic su **Aggiungi** e configuralo come segue:

   * **Estensione**: Adobe Experience Platform Web SDK

   * **Tipo azione**: invia evento

   ![](assets/configure_web_inapp_4.png)

1. Nella sezione **Personalization** del tipo **Action**, abilita l&#39;opzione **Decisioni di personalizzazione visiva**.

   ![](assets/configure_web_inapp_5.png)

1. Nella sezione **Contesto decisionale**, definisci le coppie **Chiave** e **Valore** che determinano l&#39;esperienza da consegnare.

   ![](assets/configure_web_inapp_6.png)

1. Salva la configurazione di **Azione** facendo clic su **Mantieni modifiche**.

1. Passare al menu **Flusso di pubblicazione**. Crea una nuova **Libreria** o seleziona una **Libreria** esistente e aggiungi la **Regola** appena creata. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Dalla **libreria**, seleziona **Salva e genera in sviluppo**.

   ![](assets/configure_web_inapp_7.png)

## Configura regola manuale {#configure-manual-trigger}

1. Accedi all&#39;istanza di **Adobe Experience Platform Data Collection** e passa a **Tag Properties** configurate con l&#39;estensione **Adobe Experience Platform Web SDK**.

1. Dal menu **Authoring**, seleziona **Regole**, quindi **Crea nuova regola** o **Aggiungi regola**.

   ![](assets/configure_web_inapp_8.png)

1. Nella sezione **Eventi**, fai clic su **Aggiungi** e configuralo come segue:

   * **Estensione**: Core

   * **Tipo evento**: fare clic

   ![](assets/configure_web_inapp_9.png)

1. Nella **Configurazione clic**, definire il **Selettore** che verrà valutato.

   ![](assets/configure_web_inapp_10.png)

1. Fai clic su **Mantieni modifiche** per salvare la configurazione di **Evento**.

1. Nella sezione **Azioni**, fai clic su **Aggiungi** e configuralo come segue:

   * **Estensione**: Adobe Experience Platform Web SDK

   * **Tipo azione**: Valuta set di regole

   ![](assets/configure_web_inapp_11.png)

1. Nella sezione **Valuta azione set di regole** del tipo **Azione**, abilita l&#39;opzione **Esegui rendering decisioni di personalizzazione visiva**.

   ![](assets/configure_web_inapp_13.png)

1. Nella sezione **Contesto decisionale**, definisci le coppie **Chiave** e **Valore** che determinano l&#39;esperienza da consegnare.

1. Accedi al menu **Flusso di pubblicazione**, crea una nuova **Libreria** o seleziona una **Libreria** esistente e aggiungi la **Regola** appena creata. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Dalla **libreria**, seleziona **Salva e genera in sviluppo**.

   ![](assets/configure_web_inapp_14.png)

