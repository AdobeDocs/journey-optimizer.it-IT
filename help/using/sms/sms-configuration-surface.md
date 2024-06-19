---
solution: Journey Optimizer
product: journey optimizer
title: Configurare la superficie SMS
description: Scopri come configurare la superficie SMS/MMS per inviare messaggi di testo con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 8%

---

# Creare una superficie SMS/MMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definire la categoria di messaggio"
>abstract="Seleziona il tipo di messaggi utilizzando questa superficie: Marketing per messaggi promozionali, che richiedono il consenso dell’utente; oppure Transazionale per messaggi non commerciali, come la reimpostazione della password."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=it#sms-opt-out-management" text="Rinuncia nei messaggi di testo di marketing"

Una volta configurato il canale SMS/MMS, è necessario creare una superficie di canale per poter inviare messaggi SMS e MMS da **[!DNL Journey Optimizer]**.

Per creare una superficie di canale, effettuate le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona **[!UICONTROL Marchio]** > **[!UICONTROL Superfici di canale]**. Fai clic su **[!UICONTROL Crea superficie di canale]** pulsante.

   ![](assets/preset-create.png)

1. Immetti un nome e una descrizione (facoltativa) per la superficie, quindi seleziona il canale SMS.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, punto`.` e trattino `-` caratteri.

1. Definisci il **Impostazioni SMS**.

   ![](assets/sms-surface-settings.png)

   Per iniziare, seleziona la **[!UICONTROL Tipo di SMS]** che verrà inviato con la superficie: **[!UICONTROL Transazionale]** o **[!UICONTROL Marketing]**.

   * Scegli **Marketing** messaggi di testo promozionali: questi messaggi richiedono il consenso dell’utente.
   * Scegli **Transazionale** per messaggi non commerciali come ad esempio la conferma di un ordine, le notifiche di reimpostazione della password o le informazioni di consegna.

   Quando crei un SMS/MMS, devi scegliere una superficie di canale valida che corrisponda alla categoria selezionata per il messaggio.

   >[!CAUTION]
   >
   >**Transazionale** è possibile inviare messaggi ai profili che hanno annullato l’abbonamento alle comunicazioni di marketing. Questi messaggi possono essere inviati solo in contesti specifici.

1. Seleziona la **[!UICONTROL Configurazione SMS]** per associarlo alla superficie.

   Per ulteriori informazioni su come configurare l’ambiente per l’invio di messaggi SMS, consulta [questa sezione](#create-api).

1. Inserisci il **[!UICONTROL Numero mittente]** &#x200B;si desidera utilizzare per le comunicazioni.

1. Seleziona il **[!UICONTROL Campo di esecuzione SMS]** per selezionare **[!UICONTROL Attributo profilo]** associati ai numeri di telefono dei profili.

1. Se desideri utilizzare la funzione di abbreviazione URL nei messaggi SMS, seleziona un elemento da **[!UICONTROL Sottodominio]** elenco.

   >[!NOTE]
   >
   >Per poter selezionare un sottodominio, accertati di aver configurato in precedenza almeno un sottodominio SMS/MMS. [Scopri come](sms-subdomains.md)

1. Inserisci il **[!UICONTROL Numero di rinuncia]** si desidera utilizzare per questa superficie. Quando i profili rinunciano a questo numero, puoi comunque inviare loro messaggi da altri numeri con cui stai utilizzando l’invio di messaggi di testo [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >In entrata [!DNL Journey Optimizer], la rinuncia ai messaggi di testo non viene più gestita a livello di canale. Ora è specifico per un numero.

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. Potete anche salvare la superficie di canale come sformo e riprenderne la configurazione in un secondo momento.

   ![](assets/sms-submit-surface.png)

1. Una volta creata la superficie di canale, questa viene visualizzata nell’elenco con **[!UICONTROL Elaborazione]** stato.

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi dell’errore in [questa sezione](#monitor-channel-surfaces).

1. Quando i controlli hanno esito positivo, la superficie di canale riceve **[!UICONTROL Attivo]** stato. È pronto per essere utilizzato per inviare messaggi.

   ![](assets/preset-active.png)

È ora possibile inviare messaggi di testo con Journey Optimizer.
