---
solution: Journey Optimizer
product: journey optimizer
title: Creare e utilizzare i moduli per le pagine di destinazione
description: Scopri come creare e utilizzare i moduli per le pagine di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: destinazione, pagina di destinazione, creazione, pagina, modulo
badge: label="Disponibilità limitata" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: dc47da081601fdb019ffd98aa47803672fdef198
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 3%

---

# Utilizzare i moduli nelle pagine di destinazione {#lp-forms}

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

Per acquisire i dati del profilo con le pagine di destinazione [!DNL Journey Optimizer] e arricchire i set di dati [!DNL Experience Platform], puoi sfruttare i moduli nelle pagine di destinazione.

## Creare un predefinito per moduli {#create-form-preset}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_connection"
>title="Seleziona l’endpoint da utilizzare"
>abstract="Definisci l’endpoint di streaming a cui vengono inviati i dati al momento dell’invio del modulo."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="Creare una connessione streaming API HTTP"

>[!CONTEXTUALHELP]
>id="ajo_lp_form_dataset"
>title="Selezionare un set di dati"
>abstract="Definisci un set di dati in cui memorizzare e riflettere le risposte del modulo. Puoi digitare per cercare un set di dati specifico o selezionarlo dall’elenco."

Prima di poter creare un modulo, devi creare un predefinito dedicato in cui selezionare l’endpoint di connessione in cui vengono inviati i dati di invio del modulo e il set di dati in cui verranno memorizzati i dati acquisiti tramite il modulo.

Quando i dati arrivano sull’endpoint di streaming, sono collegati alle informazioni del set di dati. Utilizzando le connessioni di origine/destinazione generate e il flusso di origine, i dati vengono quindi inviati al set di dati.

Durante la creazione di un predefinito:

* Puoi impostare più predefiniti utilizzando diverse combinazioni di set di dati e connessioni in streaming.
* Lo stesso set di dati o la stessa connessione in streaming possono essere riutilizzati in più predefiniti.
* Ogni connessione in streaming genera automaticamente risorse quali:
   * **Connessione Source** - origine dei dati.
   * **Connessione di destinazione** - in cui i dati vengono archiviati o utilizzati.
   * **Flusso di Source**: la pipeline che sposta i dati dalla connessione di origine in [!DNL Experience Platform], gestendo la mappatura, la trasformazione e la convalida.

>[!NOTE]
>
> Per accedere e modificare i predefiniti di modulo, è necessario disporre dell&#39;autorizzazione **[!UICONTROL Gestisci predefiniti di modulo]** per la sandbox di produzione. Ulteriori informazioni sulle autorizzazioni in [questa sezione](../administration/high-low-permissions.md#administration-permissions).<!--TBC-->

1. Per accedere all&#39;inventario **[!UICONTROL Predefiniti modulo]**, seleziona **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** >**[!UICONTROL Impostazioni modulo]** dal menu a sinistra.

1. Fare clic su **[!UICONTROL Crea predefinito modulo]**.

1. Aggiorna il nome per recuperarlo più facilmente e aggiungi una descrizione, se necessario.

   ![](assets/lp_create-form-preset.png){width=80%}

1. Selezionare la **[!UICONTROL connessione in streaming]** da utilizzare per il modulo. Questo è l’endpoint di streaming a cui vengono inviati i dati al momento dell’invio del modulo.

   >[!NOTE]
   >
   >Per ulteriori informazioni sulla creazione di una connessione sorgente in streaming, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/streaming/http){target="_blank"}.

1. Seleziona un **[!UICONTROL Set di dati]** da collegare al modulo. Qui verranno memorizzate e riflesse le risposte del modulo. Puoi digitare per cercare un set di dati specifico o selezionarlo dall’elenco.

   >[!NOTE]
   >
   >Al momento sono disponibili solo [!DNL Adobe Experience Platform] set di dati per la selezione. È possibile selezionare un solo set di dati alla volta.

1. Fai clic su **[!UICONTROL Pubblica]**. Il predefinito è ora pronto per essere utilizzato in un modulo.

## Accedere e gestire i moduli {#access-forms}

Per accedere all&#39;elenco dei moduli, seleziona **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Forms]** dal menu a sinistra.

Vengono visualizzati tutti i moduli esistenti. Puoi filtrare i moduli in base al loro stato, alla data di creazione o di modifica.

## Creare e progettare un modulo {#create-form}

Per creare un modulo, attieniti alla procedura seguente.

1. Nell&#39;elenco **[!UICONTROL Forms]** fare clic su **[!UICONTROL Crea modulo]**.

1. Aggiungi un nome. Se necessario, puoi aggiungere una descrizione.

   ![](assets/lp_create-form.png)

1. Selezionare un **[!UICONTROL predefinito]** contenente la connessione da utilizzare e un set di dati predefinito per il modulo. [Scopri come creare un predefinito per moduli](#create-form-preset)

1. Fai clic su **[!UICONTROL Crea]**.

   <!--![](assets/lp_create-form-filled.png){width=50%}-->

1. Verrà aperto lo strumento di progettazione dei moduli. Aggiungi [componenti](../email/content-components.md#add-content-components) per creare il contenuto del modulo. È possibile utilizzare [componenti testo](../email/content-components.md#text) e **[!UICONTROL componenti campo]**.

1. Con il componente **[!UICONTROL Field]**, puoi selezionare gli attributi in base allo schema del set di dati selezionato.

   >[!NOTE]
   >
   >Per mappare i dati raccolti con un profilo, seleziona un campo di identità del profilo. Per identificare i campi di identità dall&#39;elenco attributi, cercare i campi contrassegnati come **[!UICONTROL Obbligatori]**.<!--Explain-->

   Ad esempio, puoi impostare l’E-mail e l’ID persona. Quando gli utenti compilano questi campi, le informazioni immesse vengono salvate nel set di dati selezionato.

   ![](assets/lp_create-form-fields.png)

1. È possibile specificare ogni **[!UICONTROL Dettagli campo]**, ad esempio istruzioni, un valore predefinito, un messaggio di convalida, la durata massima e così via.

   ![](assets/lp_create-form-field-details.png)

1. Puoi regolare il layout, lo stile e le dimensioni del modulo in base alle esigenze utilizzando il riquadro **[!UICONTROL Stili]**. [Ulteriori informazioni sullo stile](../email/get-started-email-style.md)

1. Fai clic su **[!UICONTROL Salva e chiudi]**.

1. Configura la pagina di ringraziamento. [Scopri come](#thank-you-page)

1. **[!UICONTROL Pubblica]** il modulo per renderlo disponibile per la selezione nelle pagine di destinazione.

### Configurare la pagina di ringraziamento {#thank-you-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_forms_thankyou_page"
>title="Pagina di ringraziamento"
>abstract="Configurare l&#39;operazione da eseguire quando un utente compila o inoltra un modulo."

Nella sezione **[!UICONTROL Pagina di ringraziamento]**, configura cosa accade quando un utente compila il modulo.

![](assets/lp_create-form-thank-you.png){width=70%}

Imposta una delle azioni seguenti:

* **[!UICONTROL Resta a pagina]** - Questa opzione mantiene il visitatore sulla stessa pagina quando il modulo è stato inviato.
* **[!UICONTROL Pagina di destinazione]** - Seleziona una [pagina di destinazione](create-lp.md) pubblicata alla quale l&#39;utente viene reindirizzato dopo l&#39;invio del modulo.
* **[!UICONTROL URL esterno]** - Immettere l&#39;URL completo come pagina di follow-up. Una volta inviato il modulo, l’utente viene indirizzato all’URL specificato.
* **[!UICONTROL Reindirizzamento condizionale]**: imposta le regole per visualizzare in modo dinamico azioni di follow-up diverse in base alle risposte del modulo.

  Puoi definire una regola per ogni pubblico specifico. Ad esempio, puoi visualizzare una pagina di destinazione specifica per i residenti negli Stati Uniti, un’altra pagina per i residenti in Canada e così via. Infine, imposta un’azione predefinita per gli utenti che non rientrano in alcuna regola definita.

  >[!NOTE]
  >
  >Le condizioni definite in una regola vengono lette in sequenza.

  ![](assets/lp_create-form-thank-you-conditional.png){width=40%}

## Sfruttare il modulo in una pagina di destinazione {#leverage-form-in-lp}

Ora puoi incorporare questo modulo in una pagina di destinazione per acquisire i dati corrispondenti agli attributi definiti nel modulo e salvarli nel set di dati selezionato. Segui i passaggi seguenti.

1. Crea una pagina di destinazione. [Scopri come](create-lp.md#create-landing-page)

1. Seleziona **[!UICONTROL Acquisizione dati]** come tipo di pagina di destinazione e fai clic su **[!UICONTROL Crea]**.

   ![](assets/lp_create-lp-data-capture.png){width=65%}

1. Configura la pagina principale. [Scopri come](create-lp.md#configure-primary-page)

1. Apri [Progettazione pagine di destinazione](design-lp.md).

1. Trascina e rilascia un **[!UICONTROL componente struttura]** nel contenuto. Trascina e rilascia un componente **[!UICONTROL Modulo]** nella struttura.

   >[!NOTE]
   >
   >In una pagina di destinazione è possibile selezionare solo i moduli pubblicati.

1. Nella sezione **[!UICONTROL Incorpora modulo]**, seleziona il modulo creato.

   ![](assets/lp_embed-form.png)

   >[!NOTE]
   >
   >Puoi aggiornare il modulo selezionato utilizzando il pulsante **[!UICONTROL Modifica modulo]**. Il modulo viene aperto in una nuova scheda. I passaggi per modificare il contenuto del modulo sono gli stessi descritti in [questa sezione](#create-form).

1. Nella sezione **[!UICONTROL Tipo di completamento]**, configura cosa accade quando un utente compila il modulo:

   * Scegliere **[!UICONTROL Definito modulo]** per selezionare l&#39;azione definita nel modulo incorporato. [Ulteriori informazioni](#thank-you-page)

   * Puoi anche selezionare una [pagina di destinazione](create-lp.md) pubblicata a cui l&#39;utente viene reindirizzato dopo l&#39;invio del modulo.

   * Oppure definisci un **[!UICONTROL URL esterno]** come pagina di follow-up a cui gli utenti vengono indirizzati quando inviano il modulo.

1. Salva e verifica la pagina di destinazione. [Scopri come](create-lp.md#test-landing-page)

Una volta che la pagina di destinazione è [pubblicata](create-lp.md#publish-landing-page) e utilizzata in un percorso, quando gli utenti compilano il modulo, le informazioni immesse vengono acquisite nel set di dati selezionato.

>[!NOTE]
>
>Se annulli la pubblicazione di un modulo utilizzato in una pagina di destinazione, lo modifichi e lo pubblichi nuovamente, la pagina di destinazione utilizza sempre l’ultima versione pubblicata del modulo.
