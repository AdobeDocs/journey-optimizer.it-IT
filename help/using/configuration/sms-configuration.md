---
title: Configurazione SMS
description: Scopri come configurare il tuo ambiente per l’invio di messaggi SMS con Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 47b1c2832f82a5c168cd03f1d1b43a9223c945b3
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 3%

---

# Configurare il canale SMS {#sms-configuration}

[!DNL Journey Optimizer] consente di creare i percorsi e inviare messaggi a un pubblico di destinazione.

Prima di inviare SMS, configura l’istanza. Devi [integrare le impostazioni del provider](#create-api) con Journey Optimizer e [creare un predefinito SMS](#message-preset-sms). Questi passaggi devono essere eseguiti da un [Amministratore di sistema Adobe Journey Optimizer](../start/path/administrator.md).

>[!AVAILABILITY]
>
>Il canale SMS è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

## Creare nuove credenziali API {#create-api}

Per configurare il fornitore di SMS con Journey Optimizer, procedi come segue:

1. Accedere al **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** menu, quindi fai clic su **[!UICONTROL Create API credential]**.

   ![](assets/sms_4.png)

1. Seleziona la tua **[!UICONTROL SMS vendor]**:

   * [!DNL Sinch]. Per trovare il tuo **[!UICONTROL Service ID]** e **[!UICONTROL API Token]**, accedi al menu SMS > API dal tuo account Sinch.
   * [!DNL Twilio]. Per trovare il tuo **[!UICONTROL Service ID]** e **[!UICONTROL API Token]**, accedi al riquadro Informazioni account della pagina Dashboard di console.

1. Inserisci un **[!UICONTROL Name]** per le credenziali API.

1. Inserisci il tuo **[!UICONTROL Service ID]** e **[!UICONTROL API Token]**.

   ![](assets/sms_5.png)

1. Fai clic su **[!UICONTROL Submit]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, è ora necessario creare un predefinito per i messaggi SMS.

## Creare un predefinito di messaggio per i messaggi SMS {#message-preset-sms}

Una volta configurato il tuo canale SMS, devi creare un predefinito di messaggio per poter inviare messaggi SMS da **[!DNL Journey Optimizer]**.

Per creare un predefinito per messaggi, effettua le seguenti operazioni:

1. Accedere al **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** menu, quindi fai clic su **[!UICONTROL Create Message preset]**.

   ![](assets/preset-create.png)

1. Immetti un nome e una descrizione (facoltativi) per il predefinito, quindi seleziona il canale SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, punto`.` e trattino `-` caratteri.

1. Configura le **SMS** impostazioni.

   ![](assets/preset-sms.png)

   * Seleziona la **[!UICONTROL SMS Type]** che verrà inviato con il predefinito: **[!UICONTROL Transactional]** o **[!UICONTROL Marketing]**.

   * Seleziona la **[!UICONTROL SMS configuration]** da associare al predefinito.

      Per ulteriori informazioni su come configurare l’ambiente per l’invio di messaggi SMS, consulta [questa sezione](#create-api).

   * Inserisci il **[!UICONTROL Sender number]** &#x200B; che desideri utilizzare per le tue comunicazioni.

   * Seleziona la tua **[!UICONTROL SMS Execution Field]** per selezionare **[!UICONTROL Profile attribute]** associati ai numeri di telefono dei profili.

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Submit]** per confermare. Puoi anche salvare il predefinito del messaggio come bozza e ripristinarne la configurazione in un secondo momento.

   ![](assets/sms_preset_2.png)

1. Una volta creato il predefinito del messaggio, questo viene visualizzato nell’elenco con la **[!UICONTROL Processing]** stato.

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-message-presets).

1. Una volta eseguiti i controlli, il predefinito del messaggio ottiene il **[!UICONTROL Active]** stato. È pronto per essere utilizzato per inviare messaggi.

   ![](assets/preset-active.png)

Ora puoi inviare messaggi SMS con Journey Optimizer.

**Argomenti correlati**

* [Creare un messaggio SMS](../messages/create-sms.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
