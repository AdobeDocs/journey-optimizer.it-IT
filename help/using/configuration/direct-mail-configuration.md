---
title: Configurazione direct mailing
description: Scopri come configurare il canale direct mailing in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: f64a6571609c69262670ac45a88cda0112aea5fa
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 3%

---

# Configurazione direct mailing {#direct-mail-configuration}

[!DNL Journey Optimizer] ti consente di personalizzare e generare i file richiesti dai provider di direct mailing per inviare messaggi ai clienti.

Quando prepari una consegna di direct mailing, [!DNL Journey Optimizer] genera un file contenente tutti i profili target e le informazioni di contatto selezionate (ad esempio l’indirizzo postale). Potrai quindi inviare questo file al provider di direct mailing, che si occuperà dell’invio effettivo.

Per inviare un messaggio di direct mailing, devi creare un file e caricarlo su un server. Prima di poterlo fare, devi creare un [configurazione del routing dei file](#file-routing-configuration) e [superficie della direct mailing](#direct-mail-surface) che fa riferimento alla configurazione del routing dei file.

## Configurare il routing dei file {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definire le impostazioni della configurazione del routing dei file"
>abstract="È necessario definire dove verrà esportato e caricato il file per consentire al provider di direct mailing di utilizzare."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definire le impostazioni della configurazione del routing dei file"
>abstract="Durante la creazione del messaggio di direct mailing, verrà generato il file contenente tutte le informazioni di profilo richieste. Questo file deve essere esportato e caricato su un server in modo che il provider di direct mailing possa accedere e utilizzare tale file per la consegna della direct mailing."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configurazione dell’indirizzamento dei file"
>abstract="Seleziona la configurazione di routing dei file desiderata, che definisce dove verranno esportati e caricati i file da utilizzare per il provider di direct mailing."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Selezionare il tipo di server per il routing dei file"
>abstract="Seleziona il server da utilizzare per caricare e memorizzare i file di direct mailing."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Scegli l’area geografica di AWS"
>abstract="Seleziona il server da utilizzare per caricare e memorizzare i file di direct mailing. Attualmente sono supportati solo Amazon S3 e SFTP."

1. Accedere al **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Configurazione dell’indirizzamento dei file]** > **[!UICONTROL Indirizzamento file]** menu, quindi fai clic su **[!UICONTROL Creare la configurazione di indirizzamento]**.

   ![](assets/file-routing-config-button.png)

1. Imposta un nome per la configurazione.

1. Seleziona la configurazione **[!UICONTROL Tipo]**, ovvero il server che desideri utilizzare per caricare e memorizzare i file di direct mailing.<!--why is it Type and not Server or Server type? asked to PM-->

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >Attualmente sono disponibili solo Amazon S3 e SFTP.

   Durante la creazione del messaggio di direct mailing, verrà generato il file contenente tutte le informazioni di profilo richieste. Questo file deve essere esportato e caricato su un server in modo che il provider di direct mailing possa accedere e utilizzare tale file per la consegna della direct mailing.

1. Compila i dettagli e le credenziali specifici del tipo di configurazione selezionato, ad esempio l’indirizzo del server, la chiave di accesso, ecc. <!--need to detail more?-->

   <!--![](assets/file-routing-config-aws-details.png)-->

   ![](assets/file-routing-config-sftp-details.png)

1. Se hai selezionato **[!UICONTROL Amazon S3]**, puoi scegliere l’area AWS in cui esportare e caricare i file di direct mailing.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >Le aree geografiche AWS sono aree geografiche separate distribuite in tutto il mondo che AWS utilizza per ospitare la propria infrastruttura. Per un utilizzo ottimale, si consiglia di scegliere l’area più vicina per ospitare l’infrastruttura cloud.

1. Seleziona **[!UICONTROL Invia]**. La configurazione di routing dei file viene creata con **[!UICONTROL Attivo]** stato. È ora pronto per essere utilizzato in un&#39;area direct mailing per inviare direct mailing da [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >Puoi anche selezionare **[!UICONTROL Salva come bozza]** per creare la configurazione di routing dei file, ma non sarà possibile selezionarla in una superficie finché non sarà **[!UICONTROL Attivo]**.

## Creare una superficie direct mailing {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Definire le impostazioni della direct mailing"
>abstract="Una superficie direct mailing contiene le impostazioni relative alla formattazione del file contenente i dati di profilo per la direct mailing. È possibile (definire la configurazione di ordinamento), rimuovere le righe duplicate, suddividere i record in più file e selezionare la configurazione di routing dei file."

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Definire l’ordinamento"
>abstract="Se selezioni questa opzione, l’ordinamento viene effettuato in base all’ID profilo, crescente o decrescente. Se la deselezioni, la configurazione di ordinamento definita durante la creazione del messaggio di direct mailing all’interno di un percorso o di una campagna."

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Definire la soglia di suddivisione del file"
>abstract="Devi impostare il numero massimo di record per ogni file contenente i dati di profilo. Una volta raggiunta la soglia specificata, verrà creato un altro file per i record rimanenti."

Una volta configurato il routing dei file, è necessario creare una superficie del canale per poter inviare direct mailing da [!DNL Journey Optimizer]. In ogni superficie, sarà necessario selezionare una configurazione di indirizzamento file.

1. Create una superficie del canale. [Ulteriori informazioni](channel-surfaces.md)

1. Seleziona la **[!UICONTROL Direct mail]** canale.

   ![](assets/surface-direct-mail-channel.png)

1. Definisci le impostazioni di direct mailing nella sezione dedicata della configurazione della superficie del canale.

   ![](assets/surface-direct-mail-settings.png)

1. Selezionare il formato del file: **[!UICONTROL CSV]** o **[!UICONTROL Testo delimitato]**.

1. In **[!UICONTROL Inserimento]** è possibile scegliere di rimuovere automaticamente le righe duplicate.

1. Definisci il numero massimo di record (righe) per ciascun file contenente i dati del profilo. Una volta raggiunta la soglia specificata, verrà creato un altro file per i record rimanenti.

   ![](assets/surface-direct-mail-split.png)

   Ad esempio, se nel file sono presenti 100.000 record e il limite di soglia è impostato su 60.000, i record verranno suddivisi in due file. Il primo file conterrà 60.000 righe e il secondo file conterrà le restanti 40.000 righe.

   >[!NOTE]
   >
   >È possibile impostare un numero qualsiasi compreso tra 1 e 200.000 record, il che significa che ogni file deve contenere almeno 1 riga e non più di 200.000 righe.

1. Infine, seleziona la [configurazione del routing dei file](#file-routing-configuration) tra quelli creati. Questo definisce dove verrà esportato e caricato il file da utilizzare per il provider di direct mailing.

   >[!CAUTION]
   >
   >Se non hai configurato alcuna opzione di routing dei file, non potrai creare una superficie di direct mailing. [Ulteriori informazioni](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)