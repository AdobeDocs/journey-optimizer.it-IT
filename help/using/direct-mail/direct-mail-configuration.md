---
solution: Journey Optimizer
product: journey optimizer
title: Configurazione direct mail
description: Scopri come configurare il canale di direct mailing in Journey Optimizer
feature: Direct Mail, Surface
topic: Content Management
role: User
level: Experienced
keyword: direct, mail, configuration, direct-mail, provider
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
TQID: https://experienceleague.adobe.com/3eyBGqw-gCAWi-SYSq5DoyDiFos5HUIIfMFKH3aZBo8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: e7702a4706509a8181ee39cccc510656c5230a16
workflow-type: tm+mt
source-wordcount: 1994
ht-degree: 20%

---

# Configurazione direct mail {#direct-mail-configuration}

>[!BEGINSHADEBOX]

**In questa pagina:** configura l&#39;indirizzamento dei file e una configurazione del canale di direct mailing in modo che i file di estrazione vengano esportati nel server appropriato affinché il provider di direct mailing possa recuperarli.

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] consente di personalizzare e generare i file necessari ai provider di direct mailing per inviare messaggi ai clienti.

Quando [crei un messaggio di direct mailing](../direct-mail/create-direct-mail.md), definisci i dati del pubblico di destinazione, incluse le informazioni di contatto scelte (ad esempio l&#39;indirizzo postale). Un file contenente questi dati verrà quindi generato ed esportato automaticamente in un server, dove il provider di direct mailing sarà in grado di recuperarli e occuparsi dell’invio effettivo.

Prima di poter generare questo file, devi creare:

1. [Configurazione di indirizzamento file](#file-routing-configuration) per specificare il server in cui verrà esportato il file e crittografare il file, se necessario.

1. [Configurazione di direct mailing](#direct-mail-configuration) che fa riferimento alla configurazione di indirizzamento dei file. Se non hai configurato alcuna opzione di indirizzamento dei file, non potrai creare una configurazione di direct mailing.


>[!CAUTION]
>
>* Per creare una configurazione di indirizzamento dei file, è necessario disporre dell&#39;autorizzazione incorporata **[!DNL Manage file routing]**. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)
>
>* I file di direct mailing vengono generati solo al momento dell’esportazione; il sistema non memorizza a tempo indefinito le esportazioni meno recenti. Per un backup più lungo o permanente, configura un’opzione di indirizzamento dei file (SFTP o archiviazione cloud).

## Configurare l’indirizzamento dei file {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Configurare l’indirizzamento dei file"
>abstract="Dopo aver creato un messaggio di direct mail, il file contenente i dati del pubblico target verrà generato ed esportato in un server. Devi specificare i dettagli del server in modo che il provider di direct mail possa accedere e utilizzare tale file per la consegna della direct mail."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/direct-mail/create-direct-mail" text="Creare un messaggio direct mail"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Configurare l’indirizzamento dei file"
>abstract="Devi definire dove esportare il file che verrà utilizzato dal provider di direct mail."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configurazione di indirizzamento dei file"
>abstract="Seleziona la configurazione di indirizzamento dei file desiderata, che definisce dove verrà esportato il file che verrà utilizzato dal provider di direct mail."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Selezionare il tipo di server per il file"
>abstract="Scegli il tipo di server da utilizzare per esportare i file di direct mail: Amazon S3, SFTP, Azure o Data Landing Zone."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Scegliere l’area geografica di AWS"
>abstract="Seleziona l’area geografica del server AWS in cui desideri esportare i file di direct mail. In genere, è preferibile scegliere quella più vicina al luogo in cui si trova il provider di direct mail."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_frequency"
>title="Scegliere l’area geografica di AWS"
>abstract="Se la configurazione di indirizzamento dei file verrà inviata utilizzando i percorsi, è possibile specificare la frequenza con cui il file verrà inviato al server."

>[!NOTE]
>
>Al momento Amazon S3, SFTP, Azure e Data Landing Zone sono supportati in [!DNL Journey Optimizer].

Per inviare un messaggio di direct mailing, [!DNL Journey Optimizer] genera ed esporta in un server il file contenente i dati del pubblico di destinazione.

È necessario specificare i dettagli del server in modo che il provider di direct mailing possa accedere al file e utilizzarlo per la consegna della posta.

Per configurare l’indirizzamento dei file, segui la procedura riportata di seguito.

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni direct mailing]** > **[!UICONTROL Indirizzamento file]**, quindi fai clic su **[!UICONTROL Crea configurazione indirizzamento file]**.

   ![Pulsante Crea configurazione di indirizzamento file nelle impostazioni di direct mailing](assets/file-routing-config-button.png){width="800" align="center"}

1. Imposta un nome per la configurazione.

1. Seleziona il tipo di server che desideri utilizzare per esportare i file di direct mailing: Amazon S3, SFTP, Azure o Data Landing Zone.

   ![Selezione del tipo di server per una configurazione di indirizzamento dei file di direct mailing](assets/file-routing-config-type.png){width="800" align="center"}

1. Compila i campi specifici per ogni tipo di server, come descritto nelle schede seguenti.

### Scegli il tipo di server {#server-type}

>[!BEGINTABS]

>[!TAB Amazon S3]

Se hai selezionato **[!UICONTROL Amazon S3]** come **[!UICONTROL tipo di server]**, compila i dettagli e le credenziali per il server:

* **Nome bucket AWS**:To sa dove trovare il nome del bucket AWS. Fai riferimento a [questa pagina](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html).

* **Chiave di accesso AWS**: per sapere dove trovare l&#39;ID della chiave di accesso AWS, fai riferimento a [questa pagina](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html#access-keys-and-secret-access-keys).

* **Chiave segreta AWS**: per sapere dove trovare la chiave segreta AWS, consulta [questa pagina](https://aws.amazon.com/fr/blogs/security/wheres-my-secret-access-key/).

* **Area geografica AWS**: scegliere l&#39;**[!UICONTROL Area geografica AWS]** in cui si troverà l&#39;infrastruttura server. Le aree geografiche di AWS sono aree geografiche che AWS utilizza per ospitare la propria infrastruttura cloud. Come pratica generale, è preferibile scegliere l’area più vicina alla posizione del provider di direct mailing.

![Selezione dell&#39;area AWS per una configurazione di indirizzamento dei file Amazon S3](assets/file-routing-config-aws-region.png){width="800" align="center"}

>[!TAB SFTP]

Se hai selezionato **[!UICONTROL SFTP]** come **[!UICONTROL tipo di server]**, compila i dettagli e le credenziali per il server:

* **[!UICONTROL Tipo di autenticazione]**: selezionare il tipo di autenticazione utilizzato per connettersi al server (password o chiave SSH).

* **[!UICONTROL Account]**: nome account utilizzato per connettersi al server SFTP.

* **[!UICONTROL Indirizzo server]**: &#x200B;URL del server SFTP.

* **[!UICONTROL Porta]**: numero porta di connessione SFTP.

* **[!UICONTROL Password]** / **[!UICONTROL Chiave SSH]**:&#x200B; password o chiave SSH utilizzata per connettersi al server SFTP.

![Dettagli di connessione al server SFTP per la configurazione di indirizzamento dei file](assets/file-routing-config-sftp-detail.png)

>[!TIP]
>
>Quando si utilizza l&#39;autenticazione con chiave SSH, la chiave deve essere una chiave privata OpenSSH **con codifica** Base64. Se si tratta di un file in formato PPK, utilizzare lo strumento PuTTY per convertirlo in formato OpenSSH. Per istruzioni dettagliate, vedere [questa sezione](#ssh-key-generation).

>[!NOTE]
>
>Per specificare un percorso sul server per il salvataggio del file, aggiorna il campo **[!UICONTROL Nome file]** della campagna di direct mailing per includere il percorso desiderato. [Ulteriori informazioni](create-direct-mail.md#extraction-file)

>[!TAB Azure]

Se hai selezionato **[!UICONTROL Azure]** come **[!UICONTROL tipo di server]**, compila i dettagli e le credenziali per il server:

* **Stringa di connessione Azure**: per trovare la **stringa di connessione Azure**, fare riferimento a [questa pagina](https://learn.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string#configure-a-connection-string-for-an-azure-storage-account).

  La **stringa di connessione Azure** deve seguire il formato seguente:

  `DefaultEndpointsProtocol=[http|https];AccountName=myAccountName;AccountKey=myAccountKey`

* **Nome contenitore**: per trovare il **Nome contenitore**, consultare [questa pagina](https://learn.microsoft.com/en-us/azure/storage/blobs/blob-containers-portal).

  Il **nome contenitore** deve contenere solo il nome del contenitore senza barre.

  >[!NOTE]
  >
  >Per specificare un percorso all&#39;interno del contenitore per il salvataggio del file, aggiorna il campo **[!UICONTROL Nome file]** della campagna di direct mailing per includere il percorso desiderato. [Ulteriori informazioni](create-direct-mail.md#extraction-file)

  ![Dettagli della connessione di archiviazione Azure per la configurazione di indirizzamento dei file](assets/file-routing-config-azure-detail.png)

>[!TAB Area di destinazione dati]

Se hai selezionato **[!UICONTROL Area di destinazione dati]** come **[!UICONTROL Tipo server]**, non sono richiesti dettagli specifici.

![Configurazione di indirizzamento dei file della zona di destinazione dati senza campi server aggiuntivi](assets/file-routing-config-dlz-detail.png)

Per tutti i clienti di [!DNL Adobe Experience Platform] viene eseguito il provisioning con un contenitore Data Landing Zone per sandbox. Ulteriori informazioni sull&#39;area di destinazione dati sono disponibili nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}.

>[!ENDTABS]

Per crittografare il file, copia e incolla la chiave di crittografia nel campo **[!UICONTROL Chiave di crittografia PGP/GPG]**.

Se la configurazione di indirizzamento dei file verrà inviata utilizzando i percorsi, è possibile specificare la frequenza con cui il file verrà inviato al server.

![Impostazioni di frequenza di esportazione Percorso per una configurazione di indirizzamento file](assets/file-routing-journey.png)

Dopo aver inserito i dettagli per il tipo di server, seleziona **[!UICONTROL Invia]**. La configurazione di indirizzamento dei file è stata creata con lo stato **[!UICONTROL Attivo]**. Ora può essere utilizzato in una [configurazione direct mailing](#direct-mail-surface).

Puoi anche selezionare **[!UICONTROL Salva come bozza]** per creare la configurazione di indirizzamento dei file, ma non potrai selezionarla in una configurazione finché non sarà **[!UICONTROL Attiva]**.

### Genera chiave SSH per l’autenticazione SFTP {#ssh-key-generation}

Se utilizzi SFTP con autenticazione a chiave SSH, devi disporre di una chiave privata OpenSSH con codifica Base64. Se la chiave non è formattata correttamente, è possibile che si verifichino errori di connessione durante la configurazione dell&#39;indirizzamento dei file.

+++Generare una chiave privata OpenSSH con codifica Base64

1. In PuTTYgen, genera la coppia di chiavi. Si consiglia RSA con 2048 bit o superiore.
1. Seleziona **Conversioni** > **Esporta chiave OpenSSH** dal menu.
1. Quando richiesto, scegliere di salvare la chiave privata **senza protezione passphrase**.
1. Nella finestra di dialogo Salva, seleziona **Tutti i file (*.*)** come tipo di file per garantire che la chiave venga salvata come testo normale e non come file ppk.
1. Apri il file salvato con un editor di testo e verificane il formato:
   * Il file deve iniziare con `-----BEGIN RSA PRIVATE KEY-----` (cinque trattini prima e dopo).
   * Non dovrebbe esserci alcuna dicitura che indichi la crittografia.
   * Il file deve terminare con `-----END RSA PRIVATE KEY-----` (cinque trattini prima e dopo).
1. Copiare l&#39;**intero contenuto del file** (inclusi i marcatori `-----BEGIN/END RSA PRIVATE KEY-----`) e codificarlo in Base64 utilizzando uno strumento quale [Codifica e decodifica Base64](https://www.base64encode.org/).

   >[!NOTE]
   >
   >Nell’output di codifica Base64, rimuovi eventuali formattazioni MIME. La chiave codificata deve essere una singola stringa continua.

1. Ora puoi incollare la chiave SSH con codifica Base64 nel campo dedicato in Journey Optimizer.

>[!CAUTION]
>
>Dopo la codifica Base64, la chiave non conterrà più i marcatori `-----BEGIN/END RSA PRIVATE KEY-----` e non deve includere interruzioni di riga. La chiave pubblica corrispondente deve essere aggiunta al file delle chiavi autorizzate del server SFTP.

Per ulteriori informazioni sulla connessione dell&#39;account SFTP ad Experience Platform, consulta [questa documentazione](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/sftp).

+++

## Creare una configurazione direct mailing {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Definire le impostazioni per direct mail"
>abstract="Una configurazione di direct mailing contiene le impostazioni per la formattazione del file che contiene i dati del pubblico e viene utilizzata dal provider e-mail. È inoltre necessario definire la posizione in cui il file verrà esportato selezionando la configurazione di indirizzamento del file."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/direct-mail/direct-mail-configuration#file-routing-configuration" text="Configurare l’indirizzamento dei file"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."
-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Definire la soglia di divisione dei file"
>abstract="Devi impostare il numero massimo di record per ogni file contenente i dati del pubblico. Puoi selezionare un numero qualsiasi compreso tra 1 e 200.000 record. Una volta raggiunta la soglia specificata, verrà creato un altro file per i record rimanenti."

Per poter inviare direct mailing con [!DNL Journey Optimizer], è necessario creare una configurazione di canale per definire le impostazioni per la formattazione del file che verrà utilizzato dal provider di posta.

Una configurazione di direct mailing deve includere anche la configurazione di indirizzamento dei file che definisce il server in cui verrà esportato il file di direct mailing.

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**. Fare clic sul pulsante **[!UICONTROL Crea configurazione canale]**. [Ulteriori informazioni](../configuration/channel-surfaces.md)

   ![Crea schermata di configurazione del canale in Amministrazione](assets/direct-mail-config-1.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione, quindi seleziona il canale da configurare.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri trattino basso `_`, punto `.` e trattino `-`.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla configurazione, è possibile selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

1. Selezionare il canale **[!UICONTROL Direct mail]**.

   ![Canale direct mail selezionato durante la creazione di una configurazione di canale](assets/direct-mail-config-2.png)

1. Seleziona **[!UICONTROL Azione di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

1. Definisci le impostazioni della direct mailing nella sezione dedicata della configurazione del canale.

   ![Impostazioni della superficie di direct mailing, inclusi il formato file e il routing](assets/surface-direct-mail-settings.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. Selezionare il formato del file: **[!UICONTROL CSV]** o **[!UICONTROL Testo delimitato]**.

1. Se si seleziona **[!UICONTROL Testo delimitato]**, definire il separatore di colonne desiderato: tabulazione, punto e virgola, barra verticale o e commerciale.

   ![Opzioni separatore colonne delimitate da testo per i file di esportazione della direct mailing](assets/surface-direct-mail-column-separator.png)

1. Selezionare la **[!UICONTROL configurazione di indirizzamento file]** tra quelle create. Questo definisce dove verrà esportato il file che il provider di direct mailing potrà utilizzare.

   >[!CAUTION]
   >
   >Se non hai configurato alcuna opzione di indirizzamento dei file, non potrai creare una configurazione di direct mailing. [Ulteriori informazioni](#file-routing-configuration)

   ![Configurazione di indirizzamento file selezionata in una configurazione del canale direct mailing](assets/surface-direct-mail-file-routing.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. Invia la configurazione di direct mailing.

Ora puoi [creare un messaggio di direct mailing](../direct-mail/create-direct-mail.md) all&#39;interno di una campagna. Una volta avviata la campagna, il file contenente i dati del pubblico di destinazione viene esportato automaticamente nel server definito. Il provider di direct mailing sarà quindi in grado di recuperare tale file e procedere con la consegna di direct mailing.

>[!NOTE]
>
>Le righe duplicate in cui tutti i valori nella riga sono uguali vengono rimosse automaticamente dal file.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.
-->

## Argomenti correlati {#related-topics}

* [Introduzione alle direct mail](get-started-direct-mail.md)
* [Creare un messaggio direct mail](create-direct-mail.md)
* [Testare e inviare direct mailing](test-send-direct-mail.md)
* [Configurazione del canale](../configuration/channel-surfaces.md)

Per domande frequenti sulla direct mailing, consulta [Introduzione alla direct mailing](get-started-direct-mail.md).