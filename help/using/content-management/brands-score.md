---
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 6%

---
Poiché il file non esiste in questo archivio e l’accesso in scrittura non è stato approvato, ecco il file Markdown completo aggiornato come richiesto:

&#x200B;---
title: Allineamento del brand
description: Scopri come creare, convalidare e gestire i contenuti del brand utilizzando il punteggio di brand.
topic: Content Management, Intelligenza artificiale
role: User
livello: Principiante, Intermedio
exl-id: 01e74670-7431-4791-b98c-12278e6d3332
TQID: https://experienceleague.adobe.com/hs1F6tz-XHYH6u8jO4kspRcX-ftY-SwilqMfcaLhTfg
product_v2:
- id: cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label: Journey Optimizer
feature_v2:
- id: dc22c819-3f29-4e91-8b7d-5c6719831141
internal-label: gestione dei contenuti
- id: fe338112-e2ce-4876-8989-fc4d497613f1
internal-label: E-mail
subfeature_v2:
- id: ea4139d9-3405-4b34-ad6e-c3ca120cc269
internal-label: contenuti multilingue
- id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
internal-label: Progettazione e-mail
- id: fb9a80eb-bebc-492f-a0e9-584595621ebb
internal-label: Publish
role_v2:
- id: b69b2659-1057-424e-8fc5-ed9e016dc554
internal-label: User
level_v2:
- id: b5a62a22-46f7-4f0d-b151-3fc640bef588
internal-label: Intermediate
- id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
internal-label: Principiante
topic_v2:
- id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
internal-label: Intelligenza artificiale
- id: e1e0219c-f879-479f-8427-888ed2a6e9c2
internal-label: Insights
---
# Allineamento del brand {#brands-score}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come convalidare il contenuto delle e-mail in base alle linee guida del brand e valutare la qualità complessiva dei contenuti utilizzando i punteggi di allineamento del brand in Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_brand_score"
>title="Punteggio di allineamento del brand"
>abstract="Il punteggio di allineamento del brand misura quanto i contenuti rispettano le rispettive linee guida, garantendo coerenza in termini di colori, font, logo, immagini e stile di scrittura."

>[!CONTEXTUALHELP]
>id="ajo_brand_colors"
>title="Punteggio colori"
>abstract="Punteggio colori"

>[!CONTEXTUALHELP]
>id="ajo_brand_fonts"
>title="Punteggio font"
>abstract="Punteggio font"

>[!CONTEXTUALHELP]
>id="ajo_brand_logos"
>title="Punteggio logo"
>abstract="Punteggio logo"

>[!CONTEXTUALHELP]
>id="ajo_brand_suggestions"
>title="Suggerimenti generati da IA"
>abstract="Quando il contenuto viene contrassegnato durante l’allineamento del brand o la valutazione della qualità, l’Assistente AI genera automaticamente alternative corrette che puoi rivedere e applicare in linea."

>[!AVAILABILITY]
>
>Prima di poter utilizzare l&#39;Assistente di intelligenza artificiale in Adobe Journey Optimizer, devi accettare il [contratto utente](https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

La funzione di Allineamento dei marchi consente di creare, rivedere e gestire contenuti conformi alle linee guida del brand. Garantisce coerenza nel tono, nella messaggistica e nell’identità visiva in tutte le campagne e-mail, fungendo anche da controllo di qualità prima che il contenuto venga pubblicato.

## Convalidare i contenuti con l’allineamento del brand {#validate-content}

Una volta [configurato e pubblicato il brand](brands.md), valuta il tuo punteggio di allineamento del brand direttamente all&#39;interno della tua campagna e-mail per garantire che il contenuto sia allineato alle linee guida del brand:

1. Crea la tua [campagna e-mail](../campaigns/create-campaign.md).

1. Apri il menu **[!UICONTROL Allineamento marchio]** nel Designer e-mail.

   Il contenuto viene valutato automaticamente in base al marchio predefinito. [Scopri come assegnare un marchio predefinito](brands.md).

   ![](assets/brand-score-1.png)

1. Per valutare utilizzando un marchio diverso, selezionalo dal menu a discesa **[!UICONTROL Marchio]** e fai clic su **[!UICONTROL Valuta punteggio]**.

   ![](assets/brand-score-2.png)

1. Sfoglia lo **[!UICONTROL stile di scrittura]** o il **[!UICONTROL contenuto visivo]** per visualizzare ulteriori informazioni sul punteggio.

   ![](assets/brand-score-3.png)

1. Fai clic sull&#39;icona ![Schermo intero per approfondimenti dettagliati](assets/do-not-localize/Smock_FullScreen_18_N.svg "Schermo intero") per visualizzare ulteriori informazioni sul punteggio.

   ![](assets/brand-score-5.png)

1. Seleziona una linea guida contrassegnata per visualizzare feedback specifici e suggerimenti generati dall’intelligenza artificiale. L’allineamento del brand valuta le seguenti categorie:

   &#x200B;* **[!UICONTROL Stile scrittura]**:
      &#x200B;* **[!UICONTROL Stile di comunicazione del marchio]**: definisce la personalità e il tono emotivo per garantire una voce coerente del marchio su tutti i canali.
      &#x200B;* **[!UICONTROL Standard di messaggistica del marchio]**: regole strutturali e di formattazione per un efficace testo di marketing e promozionale.
      &#x200B;* **[!UICONTROL Standard di conformità legale]**: garantisce che tutte le comunicazioni siano conformi ai requisiti legali, inclusi il posizionamento di testo e le liste di controllo di conformità.

   &#x200B;* **[!UICONTROL Contenuto visivo]**:
      &#x200B;* **[!UICONTROL Standard per la fotografia]**: requisiti per il contenuto fotografico, inclusi risoluzione, composizione, illuminazione e formati di file.
      &#x200B;* **[!UICONTROL Standard illustrazione]**: parametri di stile, spessore delle linee, utilizzo del colore e requisiti di formato file per le illustrazioni.
      &#x200B;* **[!UICONTROL Standard icona]**: specifiche per la progettazione delle icone, inclusi i sistemi di griglia, lo spessore della traccia e il dimensionamento per l&#39;uniformità.
      &#x200B;* **[!UICONTROL Linee guida per l&#39;utilizzo]**: best practice per la selezione, il posizionamento e il contesto delle immagini per mantenere l&#39;identità del brand.



   ![](assets/brand-score-4.png)

1. Per problemi di stile di scrittura con contrassegni, controlla il suggerimento generato dall&#39;intelligenza artificiale visualizzato sotto ogni violazione, quindi fai clic su **[!UICONTROL Applica]** per sostituire il contenuto contrassegnato in linea o chiudilo per mantenere il testo originale. [Ulteriori informazioni sull&#39;applicazione di suggerimenti generati dall&#39;intelligenza artificiale](#apply-suggestions).

1. Rivaluta manualmente il contenuto dopo aver apportato modifiche per aggiornare il punteggio di allineamento.

## Convalidare la qualità dei contenuti {#validate-quality}

>[!NOTE]
>
>La valutazione della qualità dei contenuti è indipendente dalle linee guida del brand. Anche se un brand è selezionato nel menu a discesa, le sue linee guida non vengono applicate al controllo di qualità. La selezione del brand è pertinente solo per il punteggio di allineamento del brand.

Oltre all’allineamento del brand, puoi valutare la qualità generale dei contenuti per identificare potenziali problemi di leggibilità, coerenza ed efficacia dei contenuti, indipendentemente dalle linee guida del brand.

Per valutare la qualità dei contenuti:

1. Crea la tua [campagna e-mail](../campaigns/create-campaign.md).

1. Apri il menu **[!UICONTROL Allineamento marchio]** nel Designer e-mail.

   ![](assets/brand-score-1.png)

1. Fai clic su **[!UICONTROL Valuta punteggio]** per generare sia l&#39;allineamento del brand che i punteggi di qualità del contenuto.

   ![](assets/brand-score-2.png)

1. Passa alla scheda **[!UICONTROL Qualità generale]** per rivedere approfondimenti e consigli sulla qualità dei contenuti.

   ![](assets/brand-score-6.png)

1. Fai clic sull&#39;icona ![Schermo intero per approfondimenti dettagliati](assets/do-not-localize/Smock_FullScreen_18_N.svg "Schermo intero") per una visualizzazione dettagliata del punteggio di qualità.

   ![](assets/brand-score-7.png)

1. Seleziona qualsiasi elemento contrassegnato per visualizzare feedback specifici e suggerimenti di miglioramento generati dall’intelligenza artificiale. I punteggi si basano sulle seguenti categorie:

   &#x200B;* **[!UICONTROL Efficacia di CTA]**: valuta il livello di efficacia del call-to-action nel motivare i lettori a intraprendere l&#39;azione desiderata.
   &#x200B;* **[!UICONTROL Oggetto]**: valuta la chiarezza, la rilevanza e la qualità che attira l&#39;attenzione per incoraggiare l&#39;apertura delle e-mail.
   &#x200B;* **[!UICONTROL Leggibilità]**: misura la facilità di comprensione del contenuto da parte dei lettori.
   &#x200B;* **[!UICONTROL Controllo spam]**: identifica i trigger di posta indesiderata comuni che possono influire sul recapito messaggi.
   &#x200B;* **[!UICONTROL Coerenza dei contenuti]**: assicura un flusso fluido dei contenuti e la loro permanenza nell&#39;argomento.
   &#x200B;* **[!UICONTROL Correzione]**: verifica la presenza di problemi di ortografia, grammatica e chiarezza.

   ![](assets/brand-score-8.png)

1. Per gli elementi di testo contrassegnati, controlla il suggerimento generato dall&#39;intelligenza artificiale visualizzato sotto ogni problema, quindi fai clic su **[!UICONTROL Applica]** per sostituire il contenuto in linea o ignoralo per mantenere il testo originale. [Ulteriori informazioni sull&#39;applicazione di suggerimenti generati dall&#39;intelligenza artificiale](#apply-suggestions).

1. Fai clic su **[!UICONTROL Rivaluta il punteggio]** dopo aver apportato modifiche per aggiornare il punteggio di qualità.

## Applicare suggerimenti generati dall’intelligenza artificiale {#apply-suggestions}

Quando il contenuto viene contrassegnato durante l’allineamento del brand o la valutazione della qualità, l’Assistente AI genera automaticamente alternative corrette o migliorate direttamente nel pannello di feedback. Questo flusso di lavoro di correzione ti aiuta a risolvere le violazioni senza uscire dall’editor, riducendo il lavoro di modifica manuale e accelerando la produzione dei contenuti.

I suggerimenti generati dall’intelligenza artificiale sono disponibili per le violazioni basate su testo in tutti i tipi di contenuto supportati: e-mail, SMS, push e web.

Per applicare un suggerimento generato dall’intelligenza artificiale:

1. Esegui una valutazione dell’allineamento del brand o della qualità, quindi seleziona una linea guida o un elemento di qualità segnalato per espandere il pannello di feedback.

1. Rivedi il suggerimento generato dall’intelligenza artificiale visualizzato sotto il contenuto contrassegnato.

1. Fai clic su **[!UICONTROL Applica]** per sostituire il contenuto contrassegnato con l&#39;alternativa suggerita.

   Per mantenere il testo originale, fare clic su **[!UICONTROL Ignora]**.

1. Ripetere l&#39;operazione per gli elementi contrassegnati rimanenti.

1. Rivaluta il punteggio per confermare che tutti i miglioramenti sono stati applicati.

## Video introduttivo {#video}

Il video seguente mostra come creare e personalizzare i propri marchi per definire chiaramente la propria identità visiva e verbale nelle comunicazioni.

+++ Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3470544/?learn=on)

+++
