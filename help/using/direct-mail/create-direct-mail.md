---
title: Creare un messaggio direct mail
description: Scopri come creare un messaggio di direct mailing in Journey Optimizer
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: direct mail, messaggio, campagna
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 18%

---

# Creare un messaggio direct mail {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Creazione di direct mail"
>abstract="Crea messaggi di direct mail in campagne pianificate e progetta i file di estrazione richiesti dai provider di direct mail che desideri inviare ai tuoi clienti."

Per creare messaggi di direct mailing, crea una campagna pianificata e configura il file di estrazione. Questo file è richiesto dai provider di direct mailing per inviare e-mail ai clienti.

>[!IMPORTANT]
>
>Prima di creare un messaggio di direct mailing, assicurati di aver configurato:
>
>1. Una [configurazione di indirizzamento file](../direct-mail/direct-mail-configuration.md#file-routing-configuration) che specifica il server in cui deve essere caricato e memorizzato il file di estrazione,
>1. Una [superficie messaggi di direct mailing](../direct-mail/direct-mail-configuration.md#direct-mail-surface) che farà riferimento alla configurazione di indirizzamento dei file.


## Creare una campagna di direct mailing{#create-dm-campaign}

Per creare una campagna di direct mailing, effettua le seguenti operazioni:

1. Crea una nuova campagna pianificata e scegli **[!UICONTROL Direct mail]** come azione.

1. Selezionare la **[!UICONTROL superficie di direct mailing]** da utilizzare e fare clic su **[!UICONTROL Crea]**. [Scopri come creare una superficie per direct mailing](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. Nella sezione **[!UICONTROL Proprietà]**, modifica il **[!UICONTROL Titolo]** e la **[!UICONTROL Descrizione]** della tua campagna.

1. Per definire il pubblico di destinazione, fai clic sul pulsante **[!UICONTROL Seleziona pubblico]** e scegli uno dei tipi di pubblico di Adobe Experience Platform disponibili. [Ulteriori informazioni](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >Per il momento, la selezione del pubblico è limitata a 3 milioni di profili. Questa limitazione può essere revocata su richiesta del rappresentante del tuo Adobe.

1. Nel campo **[!UICONTROL Spazio dei nomi identità]**, seleziona lo spazio dei nomi appropriato per identificare i singoli utenti all&#39;interno del pubblico scelto. [Ulteriori informazioni](../event/about-creating.md#select-the-namespace).

   ![](assets/direct-mail-campaign-properties.png){width="800" align="center"}

1. Le campagne possono essere pianificate per una data specifica o impostate per essere ricorrenti a intervalli regolari. Scopri come configurare la **[!UICONTROL pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

Ora puoi iniziare a configurare il file di estrazione da inviare al provider di direct mailing.

## Configurare il file di estrazione {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="Campi dati"
>abstract="Aggiungi e configura le colonne e le informazioni da visualizzare nel file di estrazione richieste dai provider di direct mail per inviare e-mail alla clientela. Puoi aggiungere fino a 50 colonne."

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="Formattazione del file di estrazione"
>abstract="Per ogni campo, specifica un’etichetta e le informazioni da visualizzare utilizzando l’editor di personalizzazione. <br/><br/> L’opzione <b>Ordina per</b> consente di utilizzare il campo selezionato per ordinare le colonne del file di estrazione."

1. Configura le colonne e le informazioni da visualizzare nel file di estrazione:

   1. Fai clic sul pulsante **[!UICONTROL Aggiungi]** per creare una nuova colonna.

   1. Il riquadro **[!UICONTROL Formattazione]** viene visualizzato sul lato destro e consente di impostare la colonna selezionata. Specificare un **[!UICONTROL etichetta]** per la colonna.

   1. Nel campo **[!UICONTROL Dati]**, seleziona gli attributi del profilo da visualizzare utilizzando l&#39;[editor di personalizzazione](../personalization/personalization-build-expressions.md).

   1. Per ordinare il file di estrazione utilizzando una colonna, selezionare la colonna e attivare l&#39;opzione **[!UICONTROL Ordina per]**. Accanto all&#39;etichetta della colonna nella sezione **[!UICONTROL Campi dati]** viene visualizzata l&#39;icona **[!UICONTROL Ordina per]**.







Il file di estrazione è richiesto dai provider di direct mailing per inviare e-mail ai clienti. Per definire la configurazione del file di estrazione, effettua le seguenti operazioni:

1. Dalla schermata di configurazione della campagna, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** per configurare il contenuto del file di estrazione.

1. Regola le proprietà del file di estrazione:

   1. Specifica il **[!UICONTROL Nome file]** desiderato per il file di estrazione.

   1. Se si desidera aggiungere una marca temporale automatica al nome file specificato, attivare l&#39;opzione **[!UICONTROL Aggiungi marca temporale per esportare il nome file]**.

   1. A volte potresti aver bisogno di aggiungere informazioni all’inizio o alla fine del file di estrazione. A questo scopo, utilizza il campo **[!UICONTROL Note]** e specifica se includere la nota come intestazione o piè di pagina.

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. Configura le colonne e le informazioni da visualizzare nel file di estrazione:

   1. Fai clic sul pulsante **[!UICONTROL Aggiungi]** per creare una nuova colonna.

   1. Il riquadro **[!UICONTROL Formattazione]** viene visualizzato sul lato destro e consente di impostare la colonna selezionata. Specificare un **[!UICONTROL etichetta]** per la colonna.

   1. Nel campo **[!UICONTROL Dati]**, seleziona gli attributi del profilo da visualizzare utilizzando l&#39;[editor di personalizzazione](../personalization/personalization-build-expressions.md).

   1. Per ordinare il file di estrazione utilizzando una colonna, selezionare la colonna e attivare l&#39;opzione **[!UICONTROL Ordina per]**. Accanto all&#39;etichetta della colonna nella sezione **[!UICONTROL Campi dati]** viene visualizzata l&#39;icona **[!UICONTROL Ordina per]**.

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. Ripeti questi passaggi per aggiungere tutte le colonne necessarie per il file di estrazione. Puoi aggiungere fino a 50 colonne.

      Per modificare la posizione di una colonna, trascinarla nella posizione desiderata nella sezione **[!UICONTROL Campo dati]**. Per eliminare una colonna, selezionarla e fare clic sul pulsante **[!UICONTROL Rimuovi]** nel riquadro **[!UICONTROL Formattazione]**.

Ora puoi testare il messaggio direct mailing e inviarlo al pubblico. [Scopri come testare e inviare messaggi di direct mailing](test-send-direct-mail.md)
