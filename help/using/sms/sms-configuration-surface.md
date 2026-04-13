---
solution: Journey Optimizer
product: journey optimizer
title: Configurare la configurazione SMS
description: Scopri come configurare la configurazione SMS/MMS per inviare messaggi di testo con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: fc12ee65fc773c70b88504a951e5f5c5b2b3b0e6
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 13%

---

# Creare una configurazione SMS/MMS/RCS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definire la categoria di messaggio"
>abstract="Seleziona il tipo di messaggi di testo utilizzando questa configurazione: marketing, per messaggi promozionali che richiedono il consenso dell’utente oppure transazionale, per messaggi non commerciali, come la reimpostazione della password."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=it#sms-opt-out-management" text="Rinuncia nei messaggi di testo di marketing"

Una volta configurato il tuo canale SMS/MMS/RCS, devi creare una configurazione di canale per poter inviare messaggi SMS, RCS e MMS da **[!DNL Journey Optimizer]**.

Per creare una configurazione di canale, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**. Fare clic sul pulsante **[!UICONTROL Crea configurazione canale]**.

   ![](assets/preset-create.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione, quindi seleziona il canale SMS.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri trattino basso `_`, punto `.` e trattino `-`.

1. Definisci le **impostazioni SMS**.

   ![](assets/sms-surface-settings.png){width=80%}

   Inizia selezionando il tipo di SMS **[!UICONTROL 1&rbrace; che verrà inviato con la configurazione:]** Transazionale **[!UICONTROL o]** Marketing **[!UICONTROL .]**

   * Scegli **Marketing** per i messaggi promozionali: questi messaggi richiedono il consenso dell&#39;utente.
   * Scegli **Transazionale** per messaggi non commerciali quali ad esempio conferma di un ordine, notifiche di reimpostazione della password o informazioni di consegna.

   Quando crei un SMS/MMS, devi scegliere una configurazione di canale valida che corrisponda alla categoria selezionata per il messaggio.

   >[!CAUTION]
   >
   >**I messaggi transazionali** possono essere inviati ai profili che hanno annullato l&#39;abbonamento alle comunicazioni di marketing. Questi messaggi possono essere inviati solo in contesti specifici.

1. Selezionare la **[!UICONTROL configurazione SMS]** da associare alla configurazione.

   Per ulteriori informazioni su come configurare l&#39;ambiente per l&#39;invio di messaggi SMS, consulta [questa sezione](#create-api).

1. Immettere il **[!UICONTROL numero mittente]** &#x200B;che si desidera utilizzare per le comunicazioni.

1. Se desideri utilizzare la funzione di abbreviazione URL nei messaggi SMS, seleziona un elemento dall&#39;elenco **[!UICONTROL Sottodominio]**.

   >[!NOTE]
   >
   >Per poter selezionare un sottodominio, accertati di aver configurato in precedenza almeno un sottodominio SMS/MMS. [Scopri come](sms-subdomains.md)

1. Nella sezione **[!UICONTROL Dimensione di esecuzione]**, utilizza il **[!UICONTROL Campo di esecuzione SMS]** per selezionare tra gli attributi del profilo il numero di telefono da utilizzare in priorità se nel database sono disponibili più numeri. [Ulteriori informazioni](../configuration/primary-email-addresses.md#override-execution-address-channel-config)

   >[!NOTE]
   >
   >Per impostazione predefinita, [!DNL Journey Optimizer] utilizza il numero di telefono specificato nelle [impostazioni generali](../configuration/primary-email-addresses.md) a livello di sandbox. L’aggiornamento di questo campo sovrascrive il valore predefinito per i percorsi e le campagne che utilizzano questa configurazione.

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. Puoi anche salvare la configurazione del canale come bozza e riprenderla in un secondo momento.

   ![](assets/sms-submit-surface.png)

1. Una volta creata, la configurazione del canale viene visualizzata nell&#39;elenco con lo stato **[!UICONTROL Elaborazione]**.

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi di errore in [questa sezione](../configuration/channel-surfaces.md).

1. Una volta completati i controlli, la configurazione del canale ottiene lo stato **[!UICONTROL Attivo]**. È pronto per essere utilizzato per inviare messaggi.

   ![](assets/preset-active.png)

È ora possibile inviare messaggi di testo con Journey Optimizer.
