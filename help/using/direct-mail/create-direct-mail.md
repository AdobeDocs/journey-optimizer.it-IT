---
title: Creare un messaggio di direct mailing
description: Scopri come creare un messaggio di direct mailing in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 3%

---

# Creare un messaggio di direct mailing {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Creazione di direct mailing"
>abstract="Crea messaggi di direct mailing in campagne pianificate e progetta i file di estrazione richiesti dai provider di direct mailing per inviare la posta ai tuoi clienti."

La direct mailing è un canale offline che ti consente di personalizzare e generare i file di estrazione richiesti dai provider di direct mailing per inviare la posta ai tuoi clienti.

Quando crei una direct mailing, Journey Optimizer genera un file contenente tutti i profili target e i dati selezionati (ad esempio l’indirizzo postale, gli attributi del profilo). Il provider di direct mailing sarà quindi in grado di recuperare tale file e si occuperà dell’invio effettivo.

I messaggi di direct mailing possono essere creati solo nel contesto di campagne pianificate. Non sono disponibili per l’utilizzo in campagne con attivazione API o in percorsi.

>[!IMPORTANT]
>
>Prima di inviare un messaggio di direct mail, accertati di aver configurato:
>
>1. A [configurazione del routing dei file](../direct-mail/direct-mail-configuration.md#file-routing-configuration) specifica il server in cui deve essere caricato e memorizzato il file di estrazione,
>1. A [superficie messaggio direct mail](../direct-mail/direct-mail-configuration.md#direct-mail-surface) che fa riferimento alla configurazione del routing dei file.


## Creare il messaggio di direct mailing {#create}

I passaggi per creare e inviare un messaggio di direct mailing sono i seguenti:

1. Crea una nuova campagna pianificata, seleziona **[!UICONTROL Direct mail]** come azione e scegliere la superficie del canale da utilizzare. [Scopri come creare un’area direct mailing](../direct-mail/direct-mail-configuration.md#direct-mail-surface)

   ![](assets/direct-mail-campaign.png)

1. Fai clic su **[!UICONTROL Crea]** quindi definisci le informazioni di base sulla campagna (nome, descrizione). [Scopri come configurare una campagna](../campaigns/create-campaign.md)

   ![](assets/direct-mail-edit.png)

1. Fai clic sul pulsante **[!UICONTROL Modifica contenuto]** per configurare il file di estrazione da inviare al provider di direct mailing.

1. Definisci il nome del file di estrazione nel **[!UICONTROL Nome file]** campo .

   A volte potresti aver bisogno di aggiungere informazioni all’inizio o alla fine del file di estrazione. Per eseguire questa operazione, utilizza la variabile **[!UICONTROL Note]** specificare quindi se si desidera includere la nota come intestazione o piè di pagina.

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. Utilizza l’area a sinistra per definire le informazioni da visualizzare come colonne nel file di estrazione:

   1. Fai clic sul pulsante **[!UICONTROL Aggiungi]** per aggiungere una nuova colonna, selezionala dall’elenco.

   1. In **[!UICONTROL Formattazione]** specifica un’etichetta per la colonna, quindi definisci gli attributi del profilo da visualizzare utilizzando [Editor espressioni](../personalization/personalization-build-expressions.md).

      ![](assets/direct-mail-content.png)

   1. Per ordinare il file di estrazione utilizzando la colonna selezionata, attiva la **[!UICONTROL Ordina per]** su . La **[!UICONTROL Ordina per]** accanto all’etichetta della colonna nella struttura del file viene quindi visualizzata l’icona .

1. Ripeti questi passaggi per aggiungere tutte le colonne necessarie per creare il file di estrazione. È possibile aggiungere fino a 50 colonne.

   ![](assets/direct-mail-complete.png)

   Puoi eliminare una colonna in qualsiasi momento selezionandola e facendo clic sul pulsante **[!UICONTROL Rimuovi]** dal pulsante **[!UICONTROL Formattazione]** sezione .

1. Una volta definito il contenuto della direct mailing, completa la configurazione della campagna.

   All’avvio della campagna, il file di estrazione viene generato automaticamente ed esportato sul server specificato nel [configurazione del routing dei file](../direct-mail/direct-mail-configuration.md).
