---
solution: Journey Optimizer
product: journey optimizer
title: Convertire immagini in modelli di contenuto e-mail
description: Scopri come utilizzare il convertitore di immagini da AI a HTML per convertire le progettazioni di immagini in modelli di contenuto e-mail modificabili
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
keywords: e-mail, modello, immagine, HTML, AI, progettazione, convertitore
exl-id: d13467b7-2f3c-4707-a7e0-9b46cb6cafb1
feature_v2: []
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
source-git-commit: dc3ac795cd3cbfbd3dd3adfe6f220641d331081f
workflow-type: tm+mt
source-wordcount: 2126
ht-degree: 4%

---

# Convertire immagini in modelli di contenuto e-mail {#image-to-html}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare in Adobe Journey Optimizer il convertitore di immagini basate sull&#39;intelligenza artificiale in HTML per trasformare le progettazioni di immagini statiche in modelli di contenuto di e-mail modificabili e riutilizzabili.

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] consente di velocizzare notevolmente la creazione di e-mail convertendo le progettazioni di immagini statiche in modelli di contenuto e-mail modulari completamente personalizzabili.

>[!AVAILABILITY]
>
>Per utilizzare questa funzione, l&#39;organizzazione deve aver firmato l&#39;addendum [!DNL Generative AI] con Adobe. In caso di dubbi, contatta il rappresentante Adobe.
>
>Questa funzionalità è disponibile solo per il canale e-mail.

Sfruttando la tecnologia di intelligenza artificiale generativa, uno strumento integrato analizza il layout, la composizione tipografica, i colori e gli elementi visivi dell&#39;immagine e genera contenuti HTML puliti e modulari che mantengono la fedeltà di progettazione garantendo al contempo la piena modificabilità con [E-mail Designer](../email/get-started-email-design.md).

Questa funzionalità senza codice consente agli addetti al marketing di trasformare le risorse visive da designer grafici o strumenti di progettazione in modelli e-mail dinamici e modificabili che possono essere salvati e riutilizzati in più percorsi e campagne, senza richiedere competenze tecniche.

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare questa funzione, leggi le [protezioni e raccomandazioni correlate](#limitations).

I principali vantaggi sono i seguenti:

* **Codifica più veloce di quella manuale**: il convertitore trasforma le immagini in contenuto modificabile in pochi minuti, così da poter saltare il flusso di lavoro manuale da mockup a HTML.
* **Non sono necessarie competenze tecniche** - Gli addetti al marketing possono produrre e modificare modelli senza supporto per progettazione o sviluppo.
* **Riutilizzabile in più campagne** - Salva i modelli nella libreria e utilizzali in qualsiasi percorso o campagna.
* **Fedeltà alla progettazione** - L&#39;output corrisponde al layout e allo stile dell&#39;utente, pur essendo completamente compatibile con E-mail Designer.

<!--
* **Design fidelity**: Maintain visual consistency with your original design while creating fully editable content
* **Email compatibility**: Generate HTML that works seamlessly with the Email Designer and across email clients
-->

+++ Casi d’uso comuni

Il convertitore immagine-HTML è ideale per:

* **Migrazione piattaforma**: migrazione da un&#39;altra piattaforma di e-mail marketing? Converti le progettazioni e-mail esistenti in modelli HTML pronti per [!DNL Journey Optimizer] senza ricompilare da zero.
* **Conversione di modelli di progettazione**: trasforma i modelli di progettazione da strumenti come Photoshop, Figma o altri software di progettazione in modelli e-mail funzionali.
* **Creazione rapida di modelli**: genera rapidamente modelli e-mail per campagne sensibili al tempo senza attendere risorse per sviluppatori.
* **Creazione di librerie di modelli**: crea una libreria completa di modelli coerenti con il marchio che i membri del team non tecnici possono personalizzare e distribuire.
* **Riduzione delle dipendenze tecniche**: consenti agli addetti al marketing di creare e ripetere in modo indipendente i modelli e-mail, velocizzando l&#39;esecuzione della campagna.

+++

## Accedi al convertitore HTML per l’immagine {#access-image-to-html}

**Addendum con Adobe**

Per accedere a questa funzione, la tua organizzazione deve aver firmato l&#39;addendum [!DNL Generative AI] con Adobe. In caso di dubbi, contatta il rappresentante Adobe.

**Autorizzazioni**

* Per accedere e creare i modelli, il ruolo deve includere l&#39;autorizzazione **[!UICONTROL Gestisci modelli di contenuto]** (nella risorsa **Gestione contenuto**). [Ulteriori informazioni sulle autorizzazioni](../administration/permissions.md)

* Per utilizzare l&#39;immagine nel convertitore HTML, è necessario disporre dell&#39;autorizzazione **Genera contenuto**. Scopri come assegnare le autorizzazioni relative alla generazione di contenuti in [questa sezione](../content-management/gs-generative.md#generative-access).

**Contratto**

Prima di poter utilizzare questa funzione, devi accettare un contratto utente che visualizzi la prima volta che utilizzi l&#39;intelligenza artificiale generativa in [!DNL Journey Optimizer]. Per ulteriori informazioni, consulta le [Linee guida per l&#39;utente di Adobe Experience Cloud Generative AI](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

## Guardrail e consigli {#limitations}

Tieni presente le seguenti limitazioni e raccomandazioni durante la conversione di immagini in modelli di contenuto e-mail.

**Adeguatezza**

* **Interpretazione IA**: l&#39;intelligenza artificiale genera contenuto HTML statico in base all&#39;interpretazione visiva dell&#39;immagine. Fornisce un punto di partenza importante per la creazione di e-mail, ma deve essere rivisto e perfezionato utilizzando E-mail Designer per garantire che soddisfi esattamente le tue esigenze. Se necessario, aggiungi manualmente personalizzazione, contenuto dinamico e tracciamento dopo la conversione.

* **Precisione del testo**: mentre l&#39;intelligenza artificiale tenta di riconoscere e riprodurre il testo con precisione, verifica sempre il contenuto del testo e apporta le correzioni necessarie. Controlla le [linee guida per l&#39;utente di Adobe Generative AI](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

**Selezione immagine**

* **PII e dati sensibili**: assicurarsi di selezionare un&#39;immagine che non contenga dati personali o altri dati sensibili.

* **Dimensioni immagine**: impossibile caricare immagini di dimensioni superiori a 10 MB.

* **Immagini di alta qualità**: per risultati ottimali, utilizza immagini chiare e di alta qualità: elementi visivi nitidi, testo leggibile ed elementi di layout ben definiti. Immagini sfocate, scure o poco nitide riducono la qualità di conversione. Le immagini dovrebbero idealmente avere una larghezza compresa tra 600 e 800 pixel, in modo da corrispondere alle dimensioni standard delle e-mail.

* **Layout semplici**: le progettazioni molto complesse con livelli complessi, forme insolite o elementi non standard potrebbero non convertirsi perfettamente. Le progettazioni più semplici danno generalmente risultati migliori.

**Elaborazione**

* **Aggiorna la pagina**: il risultato non viene visualizzato automaticamente fino all&#39;aggiornamento.

* **Tempo di elaborazione**: la conversione spesso termina entro **circa 5 minuti**, a seconda della complessità e delle dimensioni dell&#39;immagine. Le immagini molto grandi o complesse a volte possono richiedere fino a 10 minuti; attendi di conseguenza, quindi aggiorna per visualizzare il risultato.

<!--
* **Background processing**: The AI processing happens in the background, so you can work on other tasks without keeping the screen open. The template is automatically saved as a draft once the conversion is complete.

**Feedback is welcome!** Use the dedicated section to share your thoughts and suggestions with Adobe to help us improve the feature.
-->

## Convertire un&#39;immagine in un modello HTML {#convert-image}

Per convertire una progettazione di immagini in un modello di contenuto e-mail completamente personalizzabile, segui i passaggi seguenti.

1. Assicurati di disporre di un file di immagine in formato JPEG o PNG contenente la progettazione dell’e-mail.

   >[!IMPORTANT]
   >
   >La dimensione dell&#39;immagine non può superare **10MB**. Per ottenere risultati ottimali, utilizza un&#39;immagine **chiara e di alta qualità** con elementi visivi nitidi, testo leggibile ed elementi di layout ben definiti.

1. Accedere all&#39;elenco dei modelli di contenuto selezionando **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli di contenuto]** dal menu a sinistra.

1. Fare clic su **[!UICONTROL Crea modello]**.

1. Inserisci i dettagli del modello e seleziona **[!UICONTROL E-mail]** come canale, quindi fai clic su **[!UICONTROL Crea]**.

1. Nella sezione **[!UICONTROL Converti immagine in modello]** eseguire la procedura seguente:

   * (Facoltativo) Se nell’organizzazione sono definiti dei temi del brand, puoi selezionare un tema come input in modo che il HTML generato abbia uno stile in base ai parametri del tema del brand. [Ulteriori informazioni sui temi](../email/apply-email-themes.md)

     Al modello generato verranno applicati stili quali il colore di sfondo, il colore del pulsante, i caratteri, l’interlinea, i margini e la spaziatura interna, riducendo il lavoro di progettazione aggiuntivo e creando un modello pronto all’uso con modifiche minime.

   * Per caricare un’immagine, accertati che non contenga dati personali (PII, personally identifiable information) né altri dati sensibili. Seleziona l’opzione corrispondente per confermare di aver rivisto il file.

   * Fai clic sul pulsante **[!UICONTROL Carica immagine]** per selezionare il file di immagine.

     ![Editor modello di contenuto e-mail Journey Optimizer con sezione Converti immagine in modello](../email/assets/email_designer_convert_img.png){width=80%}

     >[!CAUTION]
     >
     >Quando carichi un’immagine per la conversione, tutto il contenuto attualmente aggiunto all’e-mail verrà eliminato e sostituito con il modello generato.

1. Se si utilizza l&#39;intelligenza artificiale generativa per la prima volta in [!DNL Journey Optimizer], verrà richiesto di accettare il contratto utente. Per ulteriori informazioni, consulta le [Linee guida per l&#39;utente di Adobe Generative AI](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Finestra di dialogo del contratto utente Generative AI in Journey Optimizer](../email/assets/email_designer_convert_agreement.png){width=50%}

   Fai clic su **[!UICONTROL Accetto]** per continuare.

1. Dopo aver selezionato l&#39;immagine, fai clic su **[!UICONTROL Apri]** per avviare il processo di conversione basato sull&#39;intelligenza artificiale, che spesso viene completato entro **circa 5 minuti**, a seconda della complessità e delle dimensioni della progettazione dell&#39;immagine.

   >[!NOTE]
   >
   >In alcuni casi, le immagini molto grandi possono richiedere fino a 10 minuti. Mentre la conversione è in corso, puoi spostarti da questa schermata e lavorare su altre attività.

1. **Aggiorna la pagina** per visualizzare l&#39;output. Una volta completata la conversione, il contenuto generato viene visualizzato e salvato automaticamente come bozza.

   >[!IMPORTANT]
   >
   >Il risultato non viene visualizzato automaticamente fino all&#39;aggiornamento.

   ![Modello di contenuto e-mail che mostra la bozza generata dalla conversione dell&#39;immagine](../email/assets/email_designer_converted_img.png){width=90%}

1. Utilizza la sezione **[!UICONTROL Immagine per modellare il feedback del convertitore]** per condividere i tuoi pensieri e suggerimenti con Adobe per aiutarci a migliorare la funzione.
   ![Sezione Feedback in Journey Optimizer con un&#39;area di testo per condividere i tuoi pensieri e suggerimenti](../email/assets/email_designer_converter_feedback.png){width=70%}

1. Fai clic su **[!UICONTROL Modifica corpo dell&#39;e-mail]**. Il modello convertito si apre in [E-mail Designer](../email/get-started-email-design.md) con funzionalità di modifica complete. Ora puoi:

   * Rivedere, modificare il contenuto di testo e applicare la personalizzazione
   * Modificare le immagini e aggiungere collegamenti
   * Regolazione di colori, caratteri e stile
   * Aggiungere, rimuovere o ridisporre i componenti di contenuto
   * Sfrutta tutte le funzioni di E-mail Designer come con qualsiasi altro modello

   ![Invia un&#39;e-mail a Designer in Journey Optimizer visualizzando il modello convertito come componente di contenuto modulare per la modifica](../email/assets/email_designer_html_components.png)

   Apporta le modifiche necessarie per perfezionare il modello e allinearlo alle linee guida del tuo marchio.

1. Una volta completato il modello, fai clic su **[!UICONTROL Salva]**.

Il modello è ora disponibile nella libreria dei modelli di contenuto e può essere utilizzato durante la creazione di e-mail in percorsi o campagne. [Scopri come utilizzare i modelli di contenuto](../email/use-email-templates.md)

## Best practice {#best-practices}

Per ottenere risultati ottimali durante la conversione di immagini in modelli di contenuto e-mail, segui queste raccomandazioni.

+++Prima di iniziare

* **Salva contenuto esistente**: la conversione di un&#39;immagine sostituisce tutto il contenuto esistente nel modello e-mail. Salvare sempre il lavoro corrente prima di utilizzare questa funzione.
* **Pianifica il flusso di lavoro**: utilizza questa funzione all&#39;inizio del processo di creazione dell&#39;e-mail oppure assicurati di essere pronto a sostituire tutto il contenuto corrente.

+++

+++Preparazione immagine

* **Risoluzione**: utilizza immagini ad alta risoluzione per migliorare il riconoscimento del testo e il rilevamento degli elementi.
* **Chiarezza**: utilizza un&#39;immagine chiara: il testo deve essere di facile lettura e gli elementi visivi devono essere ben definiti; evita file di origine sfocati, a basso contrasto o rumorosi.
* **Larghezza**: progettare immagini con larghezze di posta elettronica standard (600-800 px) corrispondenti ai requisiti tipici del client di posta elettronica.
* **Formato file**: usa il formato JPEG o PNG. Evita immagini compresse o di bassa qualità.
* **Progettazione completa**: include la progettazione completa delle e-mail in un&#39;unica immagine, dall&#39;intestazione al piè di pagina.

+++

+++Considerazioni di progettazione

* **Layout semplici**: i layout più semplici e ben strutturati vengono convertiti in modo più accurato rispetto alle progettazioni molto complesse.
* **Elementi standard**: utilizza pattern comuni per la progettazione di e-mail (intestazione, sezioni del corpo, CTA, piè di pagina).
* **Leggibilità del testo**: garantire un contrasto sufficiente tra testo e sfondi.
* **Tipi di carattere sicuri per il Web**: le progettazioni che utilizzano tipi di carattere comuni per il Web avranno una maggiore fedeltà.
* **Evita elementi sovrapposti**: separa chiaramente gli elementi di progettazione per un migliore riconoscimento della struttura.

+++

+++Dopo la conversione

* **Aggiorna per visualizzare i risultati**: dopo circa 5 minuti (o fino a 10 minuti per le immagini molto grandi), aggiorna la pagina in modo che venga visualizzata la conversione completata.
* **Rivedi la bozza**: una volta completata la conversione, il modello viene salvato automaticamente come bozza. Prenditi del tempo per esaminare attentamente i contenuti generati per verificarne l’accuratezza.
* **Verifica approfondita**: verifica l&#39;e-mail tra client e dispositivi diversi. [Scopri come visualizzare in anteprima e verificare il contenuto](preview-test.md).
* **Perfeziona manualmente**: apporta le modifiche necessarie utilizzando le funzionalità di modifica completa di [E-mail Designer](../email/get-started-email-design.md).
* **Allineamento marchio**: verifica che colori, font e stile corrispondano alle linee guida del tuo marchio, utilizzando i temi, se disponibili. [Ulteriori informazioni sui temi delle e-mail](../email/apply-email-themes.md).
* **Personalization**: aggiungi contenuto dinamico e token di personalizzazione secondo le esigenze. [Ulteriori informazioni sulla personalizzazione](../personalization/personalize.md).
* **Accessibilità**: se necessario, rivedere e migliorare le funzioni di accessibilità. [Ulteriori informazioni sul contenuto delle e-mail accessibili](../email/accessible-content.md).

+++

+++Il feedback è il benvenuto!

Utilizza la sezione dedicata per condividere i tuoi pensieri e suggerimenti con Adobe per aiutarci a migliorare questa funzione.

+++






## Domande frequenti {#faq}

+++Cosa succede al contenuto e-mail esistente quando converto un’immagine in un modello di contenuto?

Tutto il contenuto esistente nel messaggio e-mail verrà eliminato e sostituito con il modello appena generato quando carichi un’immagine per la conversione. Prima di utilizzare questa funzione, assicurati di salvare tutti i contenuti importanti. È consigliabile utilizzare questa funzionalità all’inizio del processo di creazione delle e-mail.

+++

+++Quali formati di file sono supportati?

Il convertitore supporta i formati di immagine JPEG (.jpg, .jpeg) e PNG (.png).

+++

+++Quanto tempo ci vuole per il processo di conversione?

La conversione spesso termina entro circa 5 minuti, a seconda della complessità e delle dimensioni del design dell’immagine. Le immagini molto grandi possono talvolta richiedere fino a 10 minuti; si consiglia di dedicare più tempo e di aggiornare la visualizzazione. L’elaborazione basata su intelligenza artificiale avviene in background, per consentirti di spostarti e lavorare su altre attività, senza dover tenere aperta la schermata. Una volta completata la conversione, il file viene automaticamente salvato come bozza da rivedere e modificare.

+++

+++Posso modificare il modello generato?

Sì! Il modello di contenuto generato si apre in E-mail Designer con funzionalità di modifica complete. È possibile modificare tutti gli aspetti del modello, inclusi testo, immagini, stile, layout e struttura.

+++

+++Cosa succede se la conversione non corrisponde esattamente al mio progetto?

L’intelligenza artificiale fa del suo meglio per interpretare accuratamente il tuo progetto, ma potrebbe essere necessario un qualche perfezionamento manuale. Utilizza E-mail Designer per modificare tutti gli elementi che richiedono un’ottimizzazione.

+++

+++Posso utilizzare questa funzione per pagine di destinazione o altri tipi di contenuto?

Il convertitore da immagine a HTML è attualmente progettato in modo specifico per i modelli di contenuto e-mail. Per altri tipi di contenuto, utilizza le opzioni standard di progettazione e importazione disponibili in E-mail Designer.

+++

+++Sono necessarie autorizzazioni speciali per utilizzare questa funzione?

Questa funzionalità è disponibile per tutti i clienti che hanno firmato l&#39;addendum [!DNL Gen AI] con Adobe. Se non sei sicuro se la tua organizzazione abbia firmato l’addendum, contatta il tuo rappresentante Adobe.

+++

+++È possibile riutilizzare i modelli convertiti in più campagne?

Sì! I modelli creati con l’immagine nel convertitore HTML vengono salvati automaticamente nella libreria Modelli di contenuto. Puoi accedervi e riutilizzarli in qualsiasi e-mail nei tuoi percorsi e campagne. [Ulteriori informazioni](content-templates.md)

+++

+++Posso utilizzarlo per la migrazione della piattaforma?

Sì! L’immagine al convertitore HTML è ideale per la migrazione da altre piattaforme di e-mail marketing. È sufficiente esportare o visualizzare le progettazioni delle e-mail esistenti dalla piattaforma precedente e convertirle in modelli HTML pronti per AJO senza doverle ricreare da zero.

+++

## Argomenti correlati {#related-topics}

* [Introduzione ai modelli di contenuto](content-templates.md)
* [Creare modelli di contenuto](create-content-templates.md)
* [Utilizzare modelli di e-mail](../email/use-email-templates.md)
* [Sfruttare i temi delle e-mail](../email/apply-email-themes.md)
* [Introduzione alla progettazione delle e-mail](../email/get-started-email-design.md)
