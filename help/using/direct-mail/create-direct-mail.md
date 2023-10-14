---
title: Creare un messaggio direct mail
description: Scopri come creare un messaggio di direct mailing in Journey Optimizer
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: direct mail, messaggio, campagna
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 8%

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
>1. A [configurazione di indirizzamento dei file](../direct-mail/direct-mail-configuration.md#file-routing-configuration) che specifica il server in cui il file di estrazione deve essere caricato e memorizzato,
>1. A [superficie del messaggio direct mail](../direct-mail/direct-mail-configuration.md#direct-mail-surface) che farà riferimento alla configurazione di indirizzamento dei file.


## Creare una campagna di direct mailing{#create-dm-campaign}

Per creare una campagna di direct mailing, effettua le seguenti operazioni:

1. Crea una nuova campagna pianificata e scegli **[!UICONTROL Direct mail]** come azione.

1. Seleziona la **[!UICONTROL Superficie direct mail]** per utilizzare e fare clic su **[!UICONTROL Crea]**. [Scopri come creare una superficie per direct mailing](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. In **[!UICONTROL Proprietà]** , modifica i **[!UICONTROL Titolo]** e **[!UICONTROL Descrizione]**.

1. Per definire il pubblico di destinazione, fai clic su **[!UICONTROL Seleziona pubblico]** e scegliere tra i tipi di pubblico di Adobe Experience Platform disponibili. [Ulteriori informazioni](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >Per il momento, la selezione del pubblico è limitata a 3 milioni di profili. Questa limitazione può essere revocata su richiesta del rappresentante del tuo Adobe.

1. In **[!UICONTROL Spazio dei nomi dell’identità]** , seleziona lo spazio dei nomi appropriato per identificare i singoli utenti all’interno del pubblico scelto. [Ulteriori informazioni](../event/about-creating.md#select-the-namespace).

   ![](assets/direct-mail-campaign-properties.png){width="800" align="center"}

1. Le campagne possono essere pianificate per una data specifica o impostate per essere ricorrenti a intervalli regolari. Scopri come configurare **[!UICONTROL Pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

Ora puoi iniziare a configurare il file di estrazione da inviare al provider di direct mailing.

## Configurare il file di estrazione {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="Campi dati"
>abstract="Aggiungi e configura le colonne e le informazioni da visualizzare nel file di estrazione richiesto dai provider di direct mailing per inviare e-mail ai clienti. Puoi aggiungere fino a 50 colonne."

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="Formattazione file di estrazione"
>abstract="Per ogni campo, specifica un’etichetta e le informazioni da visualizzare utilizzando l’Editor espressioni. <br/><br/> Il <b>Ordina per</b> consente di utilizzare il campo selezionato per ordinare le colonne del file di estrazione."

1. Configura le colonne e le informazioni da visualizzare nel file di estrazione:

   1. Fai clic su **[!UICONTROL Aggiungi]** per creare una nuova colonna.

   1. Il **[!UICONTROL Formattazione]** Il riquadro di destra consente di impostare la colonna selezionata. Specifica un **[!UICONTROL Etichetta]** per la colonna.

   1. In **[!UICONTROL Dati]** , selezionare gli attributi di profilo da visualizzare utilizzando [Editor espressioni](../personalization/personalization-build-expressions.md).

   1. Per ordinare il file di estrazione utilizzando una colonna, seleziona la colonna e attiva **[!UICONTROL Ordina per]** opzione. Il **[!UICONTROL Ordina per]** viene visualizzata accanto all’etichetta della colonna nel **[!UICONTROL Campi dati]** sezione.







Il file di estrazione è richiesto dai provider di direct mailing per inviare e-mail ai clienti. Per definire la configurazione del file di estrazione, effettua le seguenti operazioni:

1. Dalla schermata di configurazione della campagna, fai clic su **[!UICONTROL Modifica contenuto]** per configurare il contenuto del file di estrazione.

1. Regola le proprietà del file di estrazione:

   1. Specifica il **[!UICONTROL Nome file]** per il file di estrazione.

   1. Facoltativamente, abilita **[!UICONTROL Aggiungi la marca temporale al nome del file di esportazione]** se si desidera aggiungere una marca temporale automatica al nome file specificato.

   1. A volte potresti aver bisogno di aggiungere informazioni all’inizio o alla fine del file di estrazione. A tale scopo, utilizza **[!UICONTROL Note]** specificare se si desidera includere la nota come intestazione o piè di pagina.

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. Configura le colonne e le informazioni da visualizzare nel file di estrazione:

   1. Fai clic su **[!UICONTROL Aggiungi]** per creare una nuova colonna.

   1. Il **[!UICONTROL Formattazione]** Il riquadro di destra consente di impostare la colonna selezionata. Specifica un **[!UICONTROL Etichetta]** per la colonna.

   1. In **[!UICONTROL Dati]** , selezionare gli attributi di profilo da visualizzare utilizzando [Editor espressioni](../personalization/personalization-build-expressions.md).

   1. Per ordinare il file di estrazione utilizzando una colonna, seleziona la colonna e attiva **[!UICONTROL Ordina per]** opzione. Il **[!UICONTROL Ordina per]** viene visualizzata accanto all’etichetta della colonna nel **[!UICONTROL Campi dati]** sezione.

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. Ripeti questi passaggi per aggiungere tutte le colonne necessarie per il file di estrazione. Puoi aggiungere fino a 50 colonne.

      Per modificare la posizione di una colonna, trascinarla nella posizione desiderata in **[!UICONTROL Campo dati]** sezione. Per eliminare una colonna, selezionarla e fare clic sul pulsante **[!UICONTROL Rimuovi]** pulsante in **[!UICONTROL Formattazione]** riquadro.

Ora puoi testare il messaggio direct mailing e inviarlo al pubblico. [Scopri come testare e inviare messaggi di direct mailing](test-send-direct-mail.md)
