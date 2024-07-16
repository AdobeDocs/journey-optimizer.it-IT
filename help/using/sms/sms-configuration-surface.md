---
solution: Journey Optimizer
product: journey optimizer
title: Configurare la superficie SMS
description: Scopri come configurare la superficie SMS/MMS per inviare messaggi di testo con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 080928d14a9d6ec116286386748b77a6a25e76f8
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 10%

---

# Creare una superficie SMS/MMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definire la categoria di messaggio"
>abstract="Seleziona il tipo di messaggi utilizzando questa superficie: Marketing per messaggi promozionali, che richiedono il consenso dell’utente; oppure Transazionale per messaggi non commerciali, come la reimpostazione della password."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=it#sms-opt-out-management" text="Rinuncia nei messaggi di testo di marketing"

Una volta configurato il canale SMS/MMS, è necessario creare una superficie di canale per poter inviare messaggi SMS e MMS da **[!DNL Journey Optimizer]**.

Per creare una superficie di canale, effettuate le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona **[!UICONTROL Marchio]** > **[!UICONTROL Superfici di canale]**. Fare clic sul pulsante **[!UICONTROL Crea superficie di canale]**.

   ![](assets/preset-create.png)

1. Immetti un nome e una descrizione (facoltativa) per la superficie, quindi seleziona il canale SMS.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri di sottolineatura `_`, punto`.` e trattino `-`.

1. Definisci le **impostazioni SMS**.

   ![](assets/sms-surface-settings.png)

   Inizia selezionando il tipo di SMS **[!UICONTROL 1} che verrà inviato con la superficie:**[!UICONTROL  Transazionale ]**o**[!UICONTROL  Marketing ]**.]**

   * Scegli **Marketing** per i messaggi promozionali: questi messaggi richiedono il consenso dell&#39;utente.
   * Scegli **Transazionale** per messaggi non commerciali quali ad esempio conferma di un ordine, notifiche di reimpostazione della password o informazioni di consegna.

   Quando crei un SMS/MMS, devi scegliere una superficie di canale valida che corrisponda alla categoria selezionata per il messaggio.

   >[!CAUTION]
   >
   >**I messaggi transazionali** possono essere inviati ai profili che hanno annullato l&#39;abbonamento alle comunicazioni di marketing. Questi messaggi possono essere inviati solo in contesti specifici.

1. Selezionare la **[!UICONTROL configurazione SMS]** da associare alla superficie.

   Per ulteriori informazioni su come configurare l&#39;ambiente per l&#39;invio di messaggi SMS, consulta [questa sezione](#create-api).

1. Immettere il **[!UICONTROL numero mittente]** &#x200B;che si desidera utilizzare per le comunicazioni.

1. Seleziona il **[!UICONTROL Campo di esecuzione SMS]** per selezionare l&#39;**[!UICONTROL attributo profilo]** associato ai numeri di telefono dei profili.

1. Se desideri utilizzare la funzione di abbreviazione URL nei messaggi SMS, seleziona un elemento dall&#39;elenco **[!UICONTROL Sottodominio]**.

   >[!NOTE]
   >
   >Per poter selezionare un sottodominio, accertati di aver configurato in precedenza almeno un sottodominio SMS/MMS. [Scopri come](sms-subdomains.md)

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. Potete anche salvare la superficie di canale come sformo e riprenderne la configurazione in un secondo momento.

   ![](assets/sms-submit-surface.png)

1. Una volta creata, la superficie di canale viene visualizzata nell&#39;elenco con lo stato **[!UICONTROL Elaborazione]**.

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi di errore in [questa sezione](#monitor-channel-surfaces).

1. Una volta completati i controlli, la superficie di canale ottiene lo stato **[!UICONTROL Attivo]**. È pronto per essere utilizzato per inviare messaggi.

   ![](assets/preset-active.png)

È ora possibile inviare messaggi di testo con Journey Optimizer.
