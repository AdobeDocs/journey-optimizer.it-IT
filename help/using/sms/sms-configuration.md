---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale SMS
description: Scopri come configurare il tuo ambiente per l’invio di SMS con Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 33dccf32b60a6afb58931823016821fc1effcbd8
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 19%

---

# Configurare il canale SMS {#sms-configuration}

[!DNL Journey Optimizer] consente di creare i percorsi e inviare messaggi a un pubblico di destinazione.

Prima di inviare SMS, configura l’istanza. Devi [integrare le impostazioni del provider](#create-api) con Journey Optimizer e [creare una superficie SMS](#message-preset-sms) (ovvero predefinito SMS). Questi passaggi devono essere eseguiti da un [amministratore di sistema di Adobe Journey Optimizer](../start/path/administrator.md).

## Prerequisiti{#sms-prerequisites}

Adobe Journey Optimizer attualmente si integra con fornitori di terze parti come Sinch e Twilio, che offrono servizi SMS indipendenti da Adobe Journey Optimizer.

Prima della configurazione di SMS, devi creare un account con uno di questi provider SMS per ricevere il token API e l’ID servizio che ti consenta di stabilire la connessione tra Adobe Journey Optimizer e il provider SMS applicabile.

L’utilizzo dei servizi SMS sarà soggetto a termini e condizioni aggiuntivi da parte del provider di SMS applicabile. Dato che Sinch e Twilio sono prodotti di terze parti disponibili per gli utenti Adobe Journey Optimizer tramite un’integrazione, per qualsiasi problema o richiesta relativa ai servizi SMS, gli utenti di Sinch o Twilio dovranno contattare il provider SMS applicabile per assistenza. L&#39;Adobe non controlla e non è responsabile dei prodotti di terze parti.

>[!CAUTION]
>
>Per accedere e modificare i sottodomini SMS, devi disporre dei **[!UICONTROL Gestire i sottodomini SMS]** autorizzazione per la sandbox di produzione.

## Creare nuove credenziali API {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurare il fornitore di SMS con Journey Optimizer"
>abstract="Seleziona il fornitore e compila le credenziali API SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurare il fornitore di SMS con Journey Optimizer"
>abstract="Prima di inviare SMS, devi integrare le impostazioni del provider con Journey Optimizer. Al termine, dovrai creare una superficie SMS. Questi passaggi devono essere eseguiti da un amministratore di sistema di Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=it#message-preset-sms" text="Creare una superficie del canale SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selezionare la configurazione del fornitore di SMS"
>abstract="Seleziona le credenziali API configurate per il fornitore di SMS."

Per configurare il fornitore di SMS con Journey Optimizer, procedi come segue:

1. Nella barra a sinistra, cerca **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona la **[!UICONTROL Credenziali API]** menu. Fai clic sul pulsante **[!UICONTROL Creare nuove credenziali API]** pulsante .

   ![](assets/sms_6.png)

1. Seleziona la tua **[!UICONTROL Fornitore di SMS]**:

   * **[!DNL Sinch]**

      Per trovare il tuo **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]**, accedi al menu SMS > API dal tuo account Sinch.

   * **[!DNL Twilio]**

      Per trovare il tuo **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]**, accedi al riquadro Informazioni account della pagina Dashboard di console.


1. Inserisci un **[!UICONTROL Nome]** per le credenziali API.

1. Inserisci il tuo **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]**.

   ![](assets/sms_7.png)

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, è ora necessario creare una superficie del canale (ad es. un predefinito per messaggi) per i messaggi SMS.

## Creare una superficie SMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definire la categoria di SMS"
>abstract="Seleziona il tipo di messaggi SMS utilizzando questa superficie: Marketing per messaggi SMS promozionali, che richiedono il consenso dell’utente; oppure Transazionale per messaggi SMS non commerciali, come la reimpostazione della password."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=it#sms-opt-out-management" text="Rinuncia nei messaggi SMS di marketing"

Una volta configurato il tuo canale SMS, devi creare una superficie del canale da cui poter inviare messaggi SMS **[!DNL Journey Optimizer]**.

Per creare una superficie del canale, effettuate le seguenti operazioni:

1. Nella barra a sinistra, cerca **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona **[!UICONTROL Branding]** > **[!UICONTROL Superfici dei canali]**. Fai clic sul pulsante **[!UICONTROL Crea superficie del canale]** pulsante .

   ![](assets/preset-create.png)

1. Immetti un nome e una descrizione (facoltativi) per la superficie, quindi seleziona il canale SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, punto`.` e trattino `-` caratteri.

1. Definisci la **Impostazioni SMS**.

   ![](assets/preset-sms.png)

   * Seleziona la **[!UICONTROL Tipo SMS]** che verrà inviato con la superficie: **[!UICONTROL Transazionale]** o **[!UICONTROL Marketing]**.

      * Scegli **Marketing** per SMS promozionali: questi messaggi richiedono il consenso dell’utente.
      * Scegli **Transazionale** per messaggi non commerciali, ad esempio conferma dell’ordine, notifiche di reimpostazione della password o informazioni di consegna.

      >[!CAUTION]
      >
      >**Transazionale** I messaggi SMS possono essere inviati a profili che hanno annullato l’abbonamento a comunicazioni di marketing. Questi messaggi possono essere inviati solo in contesti specifici.

      Quando crei un messaggio SMS, devi scegliere una superficie del canale valida corrispondente alla categoria selezionata per il messaggio.

   * Seleziona la **[!UICONTROL Configurazione SMS]** da associare alla superficie.

      Per ulteriori informazioni su come configurare l’ambiente per l’invio di messaggi SMS, consulta [questa sezione](#create-api).

   * Inserisci il **[!UICONTROL Numero mittente]** &#x200B; che desideri utilizzare per le tue comunicazioni.

   * Seleziona la tua **[!UICONTROL Campo di esecuzione SMS]** per selezionare **[!UICONTROL Attributo profilo]** associati ai numeri di telefono dei profili.


1. Se desideri utilizzare la funzione di abbreviazione degli URL nei messaggi SMS, seleziona un elemento dalla **[!UICONTROL Sottodominio]** elenco.

   >[!NOTE]
   >
   >Per poter selezionare un sottodominio, accertati di aver configurato in precedenza almeno un sottodominio SMS. [Scopri come](sms-subdomains.md)

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

* [Creare un messaggio SMS](create-sms.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
* [Aggiungere un messaggio in una campagna](../campaigns/create-campaign.md)

