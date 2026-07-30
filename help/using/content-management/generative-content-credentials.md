---
solution: Journey Optimizer
product: journey optimizer
title: Content Credentials nell’Assistente AI
description: Scopri in che modo Adobe Journey Optimizer applica automaticamente Content Credentials alle immagini generate o modificate con l’Assistente AI e cosa significa per il contenuto.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
hide: true
source-git-commit: 556502a5c45ad920827785a9950bc5f7bbc4ca8f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# Content Credentials nell’Assistente AI {#generative-content-credentials}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri quali azioni dell&#39;Assistente di intelligenza artificiale allegano Content Credentials, cosa significa per le immagini che combinano diverse origini di intelligenza artificiale generative e cosa viene trasferito quando il contenuto si sposta tra le app.

>[!ENDSHADEBOX]

>[!INFO]
>
>Nuove leggi stanno emergendo sulla trasparenza generativa dell’intelligenza artificiale e Adobe sta lavorando per soddisfare i requisiti applicabili in tutte le giurisdizioni. Content Credentials è lo strumento di provenienza utilizzato da Adobe per soddisfare i requisiti di queste normative.

I Content Credentials sono metadati invisibili e duraturi che registrano il modo in cui un contenuto è stato creato o modificato. Quando si utilizza l&#39;Assistente IA in Adobe Journey Optimizer per generare o modificare un&#39;immagine con strumenti di intelligenza artificiale generativi, Content Credentials viene automaticamente associato a tale immagine, non è richiesta alcuna azione da parte dell&#39;utente.

## Azioni che associano Content Credentials {#cc-workflows}

La tabella seguente riepiloga quando Content Credentials viene allegato, in base all’azione dell’immagine eseguita nell’Assistente AI.

| Azione | Descrizione | Content Credentials allegato? | Esempio di caso d’uso |
| --- | --- | --- | --- |
| **Generare un&#39;immagine** | Creare una nuova immagine da un prompt di testo, da un&#39;immagine di riferimento o generare un&#39;immagine simile | Sempre. L’immagine viene generata dall’intelligenza artificiale generativa, quindi porta sempre con sé un Content Credential fresco. | Un’immagine del banner per una campagna e-mail viene generata da un prompt di testo che descrive l’elemento visivo desiderato. |
| **Ritagliare un&#39;immagine** (ritaglio centrato o avanzato) | Regolare un&#39;immagine alle dimensioni richieste | Solo se l&#39;immagine di origine aveva già un Content Credential. Con il ritaglio vengono ricreati i pixel dell&#39;immagine, che normalmente cancellano il Content Credential, per cui l&#39;Assistente AI legge l&#39;immagine dall&#39;immagine sorgente prima del ritaglio, quindi la ricostruisce e la ricollega al risultato ritagliato. Il ritaglio stesso non aggiunge una nuova azione di IA generativa, ma mantiene quella esistente. | Un’immagine del banner generata viene ritagliata per adattarla a una pagina web: il Content Credential viene mantenuto attraverso il ritaglio. </br> Una foto d’archivio caricata, utilizzata come sfondo di notifica push, viene ritagliata per adattarsi allo schermo: poiché la foto d’archivio non comporta alcuna azione AI generativa, non viene creato alcun Content Credential. |
| **Aggiungi una sovrapposizione di testo** | Rendering del testo generato sopra un&#39;immagine di sfondo | Solo se l&#39;immagine di sfondo aveva già un Content Credential. Il rendering della sovrapposizione produce una nuova immagine dallo sfondo più il testo, che normalmente cancella quel Content Credential, quindi AI Assistant lo legge anticipatamente dall&#39;immagine di sfondo, quindi lo ricostruisce e lo ricollega al risultato. Il passaggio di sovrapposizione non aggiunge una nuova azione di IA generativa. | Il rendering di un titolo promozionale viene eseguito come sovrapposizione di testo su un’immagine di sfondo generata per una pagina di destinazione: viene mantenuto il Content Credential dall’immagine di sfondo. |
| **Sovrapponi immagini** | Composito di due o più immagini | Se una delle immagini sorgente dispone di un Content Credential, l’immagine combinata le trasporta tutte, unite in un unico Content Credential. La composizione produce una nuova immagine dalle sorgenti, che normalmente cancellerebbe quelle Content Credentials, quindi AI Assistant legge ciascuna prima della composizione, quindi crea un singolo Content Credential combinato elencando ogni sorgente che ha contribuito a un&#39;azione di intelligenza artificiale generativa. | Un’immagine di prodotto generata è composta da uno sfondo generato per un’intestazione e-mail: il risultato è un Content Credential che riflette entrambe le sorgenti di intelligenza artificiale generative. <br> Due foto del brand caricate vengono composte in un unico collage: poiché nessuna delle due sorgenti porta un’azione di intelligenza artificiale generativa, non viene creato alcun Content Credential. |

## Tipi di contenuto e ambito {#cc-content-types}

* **Immagini**: coperte. I Content Credentials vengono allegati quando le immagini vengono generate con intelligenza artificiale generativa e vengono conservati mediante le operazioni di ritaglio, sovrapposizione del testo e sovrapposizione delle immagini eseguite dall’Assistente AI.
* **Testo**: non applicabile. Gli output di solo testo dell’Assistente AI, come la generazione di copie, la traduzione e i suggerimenti di allineamento del brand, non richiedono Content Credentials.

## Cosa succede quando il contenuto si sposta {#cc-content-moves}

Content Credentials utilizza il file di immagine. Quando un’immagine generata o modificata con IA generativa viene scaricata o esportata da Adobe Journey Optimizer, il relativo Content Credentials viene mantenuto. [Ulteriori informazioni su Content Credentials](https://helpx.adobe.com/it/firefly/using/content-credentials.html){target="_blank"}.

Alcuni modi di inserire immagini nel contenuto, come l’estrazione di un’immagine da un PDF o da un’origine incorporata (base64), potrebbero non mantenere il Content Credential originale. In questi casi, non è possibile leggere alcun Content Credential dall’origine e non ne viene creato alcuno per il risultato.

## Risorse aggiuntive

* [Adobe Content Credentials](https://helpx.adobe.com/it/firefly/using/content-credentials.html){target="_blank"}: ulteriori informazioni sul funzionamento di Content Credentials tra i prodotti Adobe.
* [Linee guida utente per l’intelligenza artificiale generativa di Adobe Experience Cloud](https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [Guardrail e limitazioni](gs-generative.md#generative-guardrails)
