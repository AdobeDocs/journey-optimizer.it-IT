---
solution: Journey Optimizer
product: journey optimizer
title: Allegare un file PDF a un’e-mail
description: Scopri come allegare file PDF statici o personalizzati a un messaggio e-mail
feature: Email Design
topic: Content Management
role: User
level: Beginner
keywords: e-mail, messaggio, allegato, pdf, editor, personalizzato, attivato da API
exl-id: 71e218d0-5b3b-4db5-8b7b-d08df8f088c4
TQID: https://experienceleague.adobe.com/9IgYERskcUrIAhTb3xlNgWTRyY-04O58ZB8I0lYFh4g
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: bfbdc1c88c1cc73f79eee0672d0d6708def69abc
workflow-type: tm+mt
source-wordcount: 916
ht-degree: 7%

---

# Allegare un file PDF a un’e-mail {#pdf-attachments}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come allegare alle e-mail file PDF statici o personalizzati, inclusi i tipi di campagna supportati e i limiti di conteggio, dimensione e volume applicabili.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_pdf_attachments"
>title="Aggiungi un allegato PDF"
>abstract="Sfoglia per selezionare un file PDF da allegare all’e-mail.</br>Puoi inviare fino a 6 messaggi all&#39;anno con un allegato PDF per profilo. La dimensione massima consentita del file per ogni allegato è di 5 MB.</br>Per ulteriori dimensioni o volumi è possibile acquistare il componente aggiuntivo Allegati di PDF. Per ulteriori informazioni, contatta il rappresentante Adobe."

È possibile allegare un file PDF statico ai messaggi di posta elettronica inviati con [!DNL Journey Optimizer]. Se utilizzi [campagne attivate da API](../campaigns/api-triggered-campaigns.md), puoi anche allegare un [file PDF personalizzato per ogni destinatario](#personalized-attachments).

Gli allegati personalizzati di PDF richiedono ulteriori operazioni di recupero ed elaborazione dei file. Le campagne che le utilizzano possono avere una latenza di elaborazione più elevata e una velocità effettiva inferiore rispetto alle campagne senza allegati, in particolare quando si utilizzano più o più file PDF.

>[!IMPORTANT]
>
>* Puoi inviare fino a 6 messaggi all’anno con un allegato PDF per profilo, sia che l’allegato sia statico che personalizzato.
>
>* La dimensione massima del file consentita per ciascun allegato è di 5 MB. Per le e-mail con [allegati personalizzati](#personalized-attachments), per impostazione predefinita tutti gli allegati PDF statici e personalizzati dell&#39;e-mail condividono un limite combinato di 5 MB.
>
> Per qualsiasi volume o dimensione aggiuntiva, è possibile acquistare il componente aggiuntivo Allegati di PDF, che aumenta il limite combinato per gli allegati personalizzati a 10 MB. Per ulteriori informazioni, contatta il rappresentante Adobe.

Per allegare un file PDF a un messaggio e-mail, segui i passaggi seguenti.

1. Crea un messaggio e-mail in un percorso o in una campagna. [Ulteriori informazioni](create-email.md)

1. Dalla scheda **[!UICONTROL Contenuto]** del percorso o della campagna, seleziona **[!UICONTROL Aggiungi risorsa]** dalla sezione **[!UICONTROL Allegato]**.

   ![](assets/email-select-pdf.png)

1. Viene visualizzato l’archivio Assets Essentials.

   >[!NOTE]
   >
   >Durante la progettazione dei messaggi, puoi accedere all’archivio Assets Essentials direttamente dall’interfaccia di Journey Optimizer. Per ulteriori informazioni sull&#39;interfaccia utente [!DNL Assets Essentials] incorporata, consulta [Documentazione di Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. Utilizza il filtro **[!UICONTROL PDF]** nella sezione **[!UICONTROL Tipo MIME]** per limitare la selezione al formato di file corretto.

   ![](assets/email-assets-pdf.png)

   >[!NOTE]
   >
   >Per gli allegati è consentito solo il formato PDF.

1. Selezionare il file desiderato.

   * È possibile selezionare un solo file alla volta.
   * La dimensione massima del file consentita per ciascun allegato è di 5 MB.

1. Al termine, il nome e le dimensioni del file selezionato vengono visualizzati nella sezione **[!UICONTROL Allegato]**.

   È possibile rimuovere il file selezionato utilizzando l&#39;icona Altre azioni accanto al nome del file.

   ![](assets/email-remove-attachment.png)

>[!NOTE]
>
>Quando salvi il messaggio come [modello di contenuto](../content-management/create-content-templates.md), l&#39;allegato PDF non viene mantenuto con il modello. Se crei una nuova e-mail dal modello di contenuto salvato, devi allegare nuovamente il file.

## Allegare file PDF personalizzati per campagne attivate da API {#personalized-attachments}

È inoltre possibile allegare file PDF specifici del destinatario a un&#39;unica e-mail inviata tramite una [campagna attivata da API](../campaigns/api-triggered-campaigns.md). A differenza di un allegato statico, ogni destinatario può ricevere un file diverso, ad esempio una fattura, una carta d&#39;imbarco, un contratto o un&#39;etichetta di spedizione.

Per impostazione predefinita, la dimensione combinata di tutti gli allegati PDF statici e personalizzati in un messaggio e-mail è limitata a 5 MB. Le organizzazioni con il componente aggiuntivo Allegati PDF applicabile possono utilizzare un limite combinato massimo di 10 MB.

>[!IMPORTANT]
>
>* Gli allegati personalizzati di PDF sono supportati solo per le campagne e-mail transazionali attivate da API.
>
>* È possibile includere fino a cinque allegati PDF in un messaggio e-mail. Questo limite include sia allegati statici che personalizzati. Ad esempio, un’e-mail contenente un PDF statico può includere fino a quattro PDF personalizzati. Se devi inviarne di più, suddividili in più comunicazioni.
>
>* Gli allegati PDF personalizzati e statici vengono conteggiati per la stessa quota. [Ulteriori informazioni](#pdf-attachments)

Gli allegati PDF personalizzati devono essere caricati nel contenitore [Data Landing Zone](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"} specifico dell&#39;allegato, a cui viene fatto riferimento nel payload API. Data Landing Zone è attualmente l’unica posizione di archiviazione supportata per gli allegati personalizzati di PDF.

1. Recupera le credenziali della zona di destinazione dati per la sandbox utilizzando `type=ajoemailattachments` per la stessa organizzazione IMS e sandbox della richiesta di esecuzione, come descritto nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}. A seconda del provider di cloud, utilizza il contenitore Azure o il bucket e la cartella AWS restituiti dall’API.

1. Genera i file PDF con lo strumento desiderato e caricali nel contenitore Data Landing Zone.

   Tieni presente che Data Landing Zone elimina automaticamente i file dopo sette giorni, assicurati che i file PDF rimangano disponibili nel contenitore fino alla consegna del messaggio e al completamento di eventuali nuovi tentativi.

1. Nel payload API, per ogni destinatario, aggiungi un array `attachments` contenente il nome del file, il tipo di contenuto e il percorso della Data Landing Zone del PDF da inviare. [Scopri come personalizzare il contenuto della campagna attivata da API](../campaigns/api-triggered-campaign-content.md#contextual)

   ```json
   "attachments": [
     {
       "name": "invoice-12345.pdf",
       "contentType": "application/pdf",
       "source": {
         "type": "dlzPath",
         "path": "attachments/invoice-12345.pdf"
       }
     }
   ]
   ```

   `source.path` è il percorso dell&#39;oggetto relativo al contenitore della zona di destinazione dati specifico dell&#39;allegato recuperato con `type=ajoemailattachments`. Non includere il nome del contenitore Azure, il bucket o la cartella AWS, le credenziali o un URL di archiviazione completo.

Al momento dell&#39;invio, [!DNL Journey Optimizer] recupera il file dalla posizione specificata e lo allega al messaggio per quel destinatario. Gli allegati personalizzati di PDF sono supportati per le campagne [High Throughput](../campaigns/api-triggered-high-throughput.md) nell&#39;area principale. Non sono supportate durante il failover regionale.

Per il riferimento completo al payload API, consulta la [documentazione dell&#39;API di esecuzione interattiva dei messaggi](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution){target="_blank"}.

{{$include /help/_includes/do-not-localize/email/ai-augmented-pdf-attachments.md}}
