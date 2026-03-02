---
solution: Journey Optimizer
product: journey optimizer
title: Accesso a Adobe Experience Manager Content Advisor
description: Scopri come accedere e utilizzare Adobe Experience Manager Content Advisor per individuare risorse e frammenti di contenuto mediante la ricerca semantica basata sull’intelligenza artificiale in Adobe Journey Optimizer.
feature: Content Management
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4576362dc6e5cd75fa19a8d4e9403db8f1e025af
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---


# Utilizzare Adobe Experience Manager Content Advisor {#aem-content-advisor}

>[!AVAILABILITY]
>
>Adobe Experience Manager Content Advisor è disponibile solo nei flussi di lavoro di authoring dei canali.

Adobe Experience Manager Content Advisor sostituisce l&#39;individuazione deterministica con l&#39;individuazione standardizzata basata sulle finalità da una superficie unificata. Consente l’individuazione unificata e basata sull’intelligenza artificiale di Assets e frammenti di contenuto direttamente all’interno dei flussi di lavoro di authoring di Journey Optimizer, migliorando la produttività degli addetti al marketing e l’efficienza delle campagne.

## Funzioni disponibili

### Per Assets {#asset-features}

Adobe Experience Manager Content Advisor offre le seguenti funzionalità per le risorse:

* 
  +++ Ricerca semantica IA

  Cerca le risorse utilizzando il linguaggio naturale invece di parole chiave o nomi di file esatti. Descrivi ciò di cui hai bisogno in un linguaggio semplice, ad esempio &quot;il caffè in montagna&quot;, e l’intelligenza artificiale trova risorse contestualmente rilevanti in base al significato e al contenuto, non solo alle corrispondenze testuali.

  ![](assets/content-advisor-2.png){zoomable="yes"}

  +++

* 
  +++ Cronologia ricerche recenti

  Accedi alle ricerche recenti per riutilizzare rapidamente parole chiave e contesti. Questo consente di risparmiare tempo quando lavori su campagne simili o quando devi perfezionare le ricerche precedenti.

  ![](assets/content-advisor-4.png){zoomable="yes"}

  +++ 

* 
  +++ Descrizione del caricamento

  Carica un documento di riepilogo di marketing per rendere automaticamente visibili le risorse in base al contesto della campagna. L’intelligenza artificiale analizza il tuo resoconto e suggerisce le risorse rilevanti in base al contenuto e ai requisiti descritti nel documento.

  ![](assets/content-advisor-5.png){zoomable="yes"}

  +++

* 
  +++ Pannello Informazioni risorsa

  Visualizza metadati e proprietà dettagliati per qualsiasi risorsa utilizzando l&#39;icona **Info**. Ciò include dimensioni della risorsa, dimensioni del file, data di creazione, tag e altre informazioni rilevanti per aiutarti a prendere decisioni informate.

  ![](assets/content-advisor-6.png){zoomable="yes"}

  +++

* 
  +++ Pannello Dynamic Media

  Accesso a rappresentazioni dinamiche, ritagli avanzati e modifiche rapide in base alla configurazione dell’archivio.

  ![](assets/content-advisor-1.png){zoomable="yes"}

  Il pannello Dynamic Media consente di accedere a rappresentazioni dinamiche, ritagli avanzati e modifiche rapide. Potete immettere i modificatori direttamente nel pannello per creare rappresentazioni personalizzate.

  **Disponibilità**

  La disponibilità di Dynamic Media dipende dalla configurazione dell’archivio:

   * **Scene7**: disponibile per le risorse pubblicate (eccetto Video e PDF). [Ulteriori informazioni sui modificatori Dynamic Media Scene7](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-is-http-modifiers.html){target="_blank"}

   * **OpenAPI**: disponibile per le risorse approvate (eccetto video). [Ulteriori informazioni su Dynamic Media con modificatori OpenAPI](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/image-profiles.html){target="_blank"}

   * **Sia Scene7 che OpenAPI**: disponibile quando esistono entrambe le configurazioni e la risorsa soddisfa i criteri.

  **Selezione dello stack**

  I pulsanti visualizzati dipendono dalla configurazione dell’archivio:

   * **Solo pulsante Scene7**: l&#39;archivio include la configurazione Scene7 e la risorsa è pubblicata in Dynamic Media.
   * **Solo pulsante OpenAPI**: l&#39;archivio dispone di una configurazione OpenAPI e la risorsa è approvata.
   * **Entrambi i pulsanti**: l&#39;archivio dispone di entrambe le configurazioni e la risorsa è pubblicata e approvata.
  +++

### Per frammento di contenuto {#content-fragment-features}

Adobe Experience Manager Content Advisor offre le seguenti funzionalità per i frammenti di contenuto:

* 
  +++ Elenco delle visualizzazioni modello 

  Passa dalla visualizzazione delle miniature alla visualizzazione della tabella per sfogliare i frammenti di contenuto nel formato più adatto al tuo flusso di lavoro. La visualizzazione Anteprime fornisce un contesto visivo, mentre la visualizzazione Tabella mostra informazioni dettagliate in un formato strutturato.

  ![](assets/content-advisor-7.png){zoomable="yes"}

  +++

* 
  +++ Pannello Info 

  Fai clic sull&#39;icona **[!UICONTROL Info]** per aprire un pannello a destra con varianti di frammento, proprietà e **[!UICONTROL dettagli con riferimento da]**. La sezione **[!UICONTROL Con riferimento da]** mostra tutte le entità Adobe Experience Manager in cui viene utilizzato il frammento, con collegamenti per visualizzare questi riferimenti direttamente in Adobe Experience Manager.

  ![](assets/content-advisor-8.png){zoomable="yes"}

  +++

* 
  +++ Apri in Adobe Experience Manager

  Apri rapidamente qualsiasi frammento di contenuto direttamente in Adobe Experience Manager per la modifica utilizzando l’icona accanto al titolo. Questa integrazione perfetta consente di passare da Journey Optimizer a Adobe Experience Manager senza perdere contesto.

  ![](assets/content-advisor-9.png){zoomable="yes"}

  +++

* 
  +++ Anteprima JSON

  Visualizza l’anteprima della struttura JSON dei frammenti di contenuto in un formato tabulare ordinato e organizzato. Questo ti aiuta a comprendere la struttura dati del frammento e a verificarne il contenuto prima di utilizzarlo nelle campagne.

  ![](assets/content-advisor-10.png){zoomable="yes"}

  +++

## Accesso a Adobe Experience Manager Content Advisor {#access}

Per accedere a Adobe Experience Manager Content Advisor in Journey Optimizer, effettuare le seguenti operazioni:

1. Crea una campagna in Adobe Journey Optimizer e aggiungi un’azione del canale, ad esempio E-mail.

1. Fai clic su **[!UICONTROL Modifica contenuto]**, quindi su **[!UICONTROL Modifica corpo e-mail]** per aprire l&#39;editor di contenuti.

1. Trascina e rilascia un componente HTML o Testo nel contenuto dell’e-mail.

1. Passa il puntatore del mouse sul componente e fai clic su **[!UICONTROL Mostra il codice sorgente]** (per i componenti HTML) o su **[!UICONTROL Aggiungi Personalization]** (per i componenti Testo).

1. Nell&#39;editor di Personalization, scegliere il punto di ingresso del contenuto:

   * Per aggiungere una risorsa, fai clic su **[!UICONTROL Assets]** e quindi su **[!UICONTROL Apri selettore risorse]**.

     ![](assets/content-advisor-11.png){zoomable="yes"}

   * Per aggiungere un frammento di contenuto Adobe Experience Manager, fai clic su **[!UICONTROL Frammento di contenuto AEM]** e quindi su **[!UICONTROL Apri selettore CF AEM]**.

     ![](assets/content-advisor-12.png){zoomable="yes"}

1. Seleziona l’archivio Adobe Experience Manager.

   ![](assets/content-advisor-13.png){zoomable="yes"}

1. Sfoglia e seleziona la risorsa o il frammento di contenuto che desideri utilizzare, quindi inseriscilo nel contenuto.


