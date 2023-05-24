---
title: Creare un messaggio di direct mailing
description: Scopri come creare un messaggio di direct mailing in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: direct mail, messaggio, campagna
hide: true
hidefromtoc: true
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
badge: label="Beta" type="Informative"
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---

# Creare un messaggio di direct mailing {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Creazione di direct mail"
>abstract="Crea messaggi di direct mail in campagne pianificate e progetta i file di estrazione richiesti dai provider di direct mail che desideri inviare ai tuoi clienti."

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* **[Creare una direct mail](create-direct-mail.md)**
* [Configurare la direct mail](direct-mail-configuration.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La direct mailing è attualmente disponibile come versione beta privata e può essere soggetta ad aggiornamenti frequenti senza preavviso.

La direct mailing è un canale offline che ti consente di personalizzare e generare i file di estrazione necessari ai provider di direct mailing per inviare e-mail ai clienti.

Quando crei una direct mailing, Journey Optimizer genera un file che include tutti i profili target e i dati scelti (ad esempio indirizzo postale, attributi del profilo). Il provider di direct mailing sarà quindi in grado di recuperare tale file e si occuperà dell’invio effettivo.

I messaggi direct mail possono essere creati solo nel contesto di campagne pianificate. Non sono disponibili per l’utilizzo in campagne attivate da API o in percorsi.

>[!IMPORTANT]
>
>Prima di inviare un messaggio di direct mailing, assicurati di aver configurato:
>
>1. A [configurazione di indirizzamento dei file](../direct-mail/direct-mail-configuration.md#file-routing-configuration) che specifica il server in cui il file di estrazione deve essere caricato e memorizzato,
>1. A [superficie del messaggio direct mail](../direct-mail/direct-mail-configuration.md#direct-mail-surface) che farà riferimento alla configurazione di indirizzamento dei file.


## Creare il messaggio di direct mailing {#create}

I passaggi per creare e inviare un messaggio di direct mailing sono i seguenti:

1. Crea una nuova campagna pianificata, seleziona **[!UICONTROL Direct mail]** come azione e scegliere la superficie di canale da utilizzare. [Scopri come creare una superficie per direct mailing](../direct-mail/direct-mail-configuration.md#direct-mail-surface)

   ![](assets/direct-mail-campaign.png)

1. Clic **[!UICONTROL Crea]** quindi definisci le informazioni di base sulla campagna (nome, descrizione). [Scopri come configurare una campagna](../campaigns/create-campaign.md)

1. Fai clic su **[!UICONTROL Modifica contenuto]** per configurare il file di estrazione da inviare al provider di direct mailing.

1. Definisci il nome del file di estrazione in **[!UICONTROL Nome file]** campo.

   A volte potresti aver bisogno di aggiungere informazioni all’inizio o alla fine del file di estrazione. A tale scopo, utilizza **[!UICONTROL Note]** specificare se si desidera includere la nota come intestazione o piè di pagina.

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. Utilizza l’area a sinistra per definire le informazioni da visualizzare come colonne nel file di estrazione:

   1. Fai clic su **[!UICONTROL Aggiungi]** per aggiungere una nuova colonna, quindi selezionarla dall&#39;elenco.

   1. In **[!UICONTROL Formattazione]** , specificare un&#39;etichetta per la colonna, quindi definire gli attributi di profilo da visualizzare utilizzando [Editor espressioni](../personalization/personalization-build-expressions.md).

      ![](assets/direct-mail-content.png)

   1. Per ordinare il file di estrazione utilizzando la colonna selezionata, attiva/disattiva **[!UICONTROL Ordina per]** opzione attivata. Il **[!UICONTROL Ordina per]** viene quindi visualizzata accanto all’etichetta della colonna nella struttura del file.

1. Ripeti questi passaggi per aggiungere tutte le colonne necessarie per generare il file di estrazione. Puoi aggiungere fino a 50 colonne.

   È possibile eliminare una colonna in qualsiasi momento selezionandola e facendo clic sul pulsante **[!UICONTROL Rimuovi]** dal pulsante **[!UICONTROL Formattazione]** sezione.

   ![](assets/direct-mail-complete.png)

1. Una volta definito il contenuto della direct mailing, completa la configurazione della campagna.

   All’avvio della campagna, il file di estrazione viene generato ed esportato automaticamente sul server specificato nella [configurazione di indirizzamento dei file](../direct-mail/direct-mail-configuration.md).
