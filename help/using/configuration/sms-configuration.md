---
title: Configurazione SMS
description: Scopri come configurare il tuo ambiente per l’invio di messaggi SMS con Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 2%

---

# Configurare il canale SMS {#sms-configuration}

[!DNL Journey Optimizer] consente di creare i percorsi e inviare messaggi a un pubblico di destinazione.

Prima di inviare SMS, configura l’istanza. Devi [integrare le impostazioni del provider](#create-api) con Journey Optimizer e [creare una superficie SMS](#message-preset-sms) (ovvero predefinito SMS). Questi passaggi devono essere eseguiti da un [Amministratore di sistema Adobe Journey Optimizer](../start/path/administrator.md).

>[!IMPORTANT]
>
>Adobe Journey Optimizer attualmente si integra con fornitori di terze parti come Sinch e Twilio, che offrono servizi SMS indipendenti da Adobe Journey Optimizer.  Prima della configurazione di SMS, devi creare un account con uno di questi provider SMS per ricevere il token API e l’ID servizio che ti consenta di stabilire la connessione tra Adobe Journey Optimizer e il provider SMS applicabile. L’utilizzo dei servizi SMS sarà soggetto a termini e condizioni aggiuntivi da parte del provider di SMS applicabile. Dato che Sinch e Twilio sono prodotti di terze parti disponibili per gli utenti Adobe Journey Optimizer tramite un’integrazione, per qualsiasi problema o richiesta relativa ai servizi SMS, gli utenti di Sinch o Twilio dovranno contattare il provider SMS applicabile per assistenza. L&#39;Adobe non controlla e non è responsabile dei prodotti di terze parti.

## Creare nuove credenziali API {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurare il fornitore di SMS con Journey Optimizer"
>abstract="Seleziona il fornitore e compila le credenziali API SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurare il fornitore di SMS con Journey Optimizer"
>abstract="Seleziona il tuo fornitore e compila le tue credenziali API SMS."

<!--New contextual help content for September release: >abstract="Before sending SMS, you must integrate the provider settings with Journey Optimizer. Once done, you will need to create an SMS surface. These steps must be performed by an Adobe Journey Optimizer system administrator."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/sms-configuration.html#message-preset-sms" text="Create an SMS channel surface"-->

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Seleziona la configurazione del fornitore SMS"
>abstract="Seleziona le credenziali API configurate per il fornitore SMS."

Per configurare il fornitore di SMS con Journey Optimizer, procedi come segue:

1. Accedere al **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Credenziali API]** menu, quindi fai clic su **[!UICONTROL Creare credenziali API]**.

   ![](assets/sms_4.png)

1. Seleziona la tua **[!UICONTROL Fornitore di SMS]**:

   * [!DNL Sinch]. Per trovare il tuo **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]**, accedi al menu SMS > API dal tuo account Sinch.
   * [!DNL Twilio]. Per trovare il tuo **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]**, accedi al riquadro Informazioni account della pagina Dashboard di console.

1. Inserisci un **[!UICONTROL Nome]** per le credenziali API.

1. Inserisci il tuo **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]**.

   ![](assets/sms_5.png)

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, è ora necessario creare una superficie del canale (ad es. un predefinito per messaggi) per i messaggi SMS.

## Creare una superficie del canale per i messaggi SMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definire la categoria SMS"
>abstract="Seleziona il tipo di messaggi SMS che verranno inviati quando utilizzi questa superficie: Marketing per messaggi SMS promozionali, che richiedono il consenso dell’utente, o transazionali per messaggi SMS non commerciali, che possono anche essere inviati a profili non abbonati in contesti specifici."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/create-sms.html#sms-opt-in-out" text="Rinuncia nei messaggi SMS di marketing"

Una volta configurato il tuo canale SMS, devi creare una superficie del canale per poter inviare messaggi SMS da **[!DNL Journey Optimizer]**.

Per creare una superficie del canale, effettuate le seguenti operazioni:

1. Accedere al **[!UICONTROL Canali]** > **[!UICONTROL Branding]** > **[!UICONTROL Superfici dei canali]** menu, quindi fai clic su **[!UICONTROL Crea superficie del canale]**.

   ![](assets/preset-create.png)

1. Immetti un nome e una descrizione (facoltativi) per la superficie, quindi seleziona il canale SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, punto`.` e trattino `-` caratteri.

1. Configura le **SMS** impostazioni.

   ![](assets/preset-sms.png)

   * Seleziona la **[!UICONTROL Tipo SMS]** che verrà inviato con la superficie: **[!UICONTROL Transazionale]** o **[!UICONTROL Marketing]**.

   * Seleziona la **[!UICONTROL Configurazione SMS]** da associare alla superficie.

      Per ulteriori informazioni su come configurare l’ambiente per l’invio di messaggi SMS, consulta [questa sezione](#create-api).

   * Inserisci il **[!UICONTROL Numero mittente]** &#x200B; che desideri utilizzare per le tue comunicazioni.

   * Seleziona la tua **[!UICONTROL Campo di esecuzione SMS]** per selezionare **[!UICONTROL Attributo profilo]** associati ai numeri di telefono dei profili.

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. È inoltre possibile salvare la superficie del canale come bozza e riprendere la configurazione in un secondo momento.

   ![](assets/sms_preset_2.png)

1. Una volta creata la superficie del canale, questa viene visualizzata nell’elenco con la **[!UICONTROL Elaborazione]** stato.

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-channel-surfaces).

1. Una volta eseguiti i controlli, la superficie del canale ottiene il **[!UICONTROL Attivo]** stato. È pronto per essere utilizzato per inviare messaggi.

   ![](assets/preset-active.png)

Ora puoi inviare messaggi SMS con Journey Optimizer.

**Argomenti correlati**

* [Creare un messaggio SMS](../messages/create-sms.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
