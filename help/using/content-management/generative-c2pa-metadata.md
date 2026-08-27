---
solution: Journey Optimizer
product: journey optimizer
title: Metadati C2PA in Genera contenuto
description: Scopri come Adobe Journey Optimizer applica automaticamente i metadati C2PA alle immagini generate o modificate con Genera contenuto e cosa significa per il contenuto.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: 5a3b83eb2e92263a5fed39b9b3670cf1fb1e15ae
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# Metadati C2PA in Genera contenuto {#generative-content-credentials}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri quali azioni di generazione contenuto allegano metadati C2PA, cosa significa per le immagini che combinano diverse origini AI generative e cosa viene riportato quando il contenuto viene spostato tra le app.

>[!ENDSHADEBOX]

>[!INFO]
>
>Nuove leggi stanno emergendo sulla trasparenza generativa dell’intelligenza artificiale e Adobe sta lavorando per soddisfare i requisiti applicabili in tutte le giurisdizioni. I metadati C2PA sono lo strumento di provenienza utilizzato da Adobe per soddisfare i requisiti di queste normative.

I metadati C2PA sono metadati invisibili e duraturi che registrano il modo in cui un contenuto è stato creato o modificato. Quando si utilizza Genera contenuto in Adobe Journey Optimizer per generare o modificare un’immagine con strumenti di intelligenza artificiale generativi, i metadati C2PA vengono automaticamente allegati all’immagine, non è richiesta alcuna azione da parte dell’utente.

## Azioni che associano metadati C2PA {#cc-workflows}

La tabella seguente riepiloga quando vengono allegati metadati C2PA, in base all’azione dell’immagine eseguita in Generate content (Genera contenuto).

| Azione | Descrizione | Metadati C2PA allegati? | Esempio di caso d’uso |
| --- | --- | --- | --- |
| **Generare un&#39;immagine** | Creare una nuova immagine da un prompt di testo, da un&#39;immagine di riferimento o generare un&#39;immagine simile | Sempre. L’immagine viene generata dall’intelligenza artificiale generativa, in modo da trasportare sempre nuovi metadati C2PA. | Un’immagine del banner per una campagna e-mail viene generata da un prompt di testo che descrive l’elemento visivo desiderato. |
| **Ritagliare un&#39;immagine** (ritaglio centrato o avanzato) | Regolare un&#39;immagine alle dimensioni richieste | Solo se l’immagine sorgente disponeva già di metadati C2PA. Il ritaglio ricrea i pixel dell&#39;immagine, che normalmente cancellano i metadati C2PA, quindi Genera contenuto lo legge dall&#39;immagine sorgente prima del ritaglio, quindi lo ricostruisce e lo ricollega al risultato ritagliato. Il ritaglio stesso non aggiunge una nuova azione di IA generativa, ma mantiene quella esistente. | Un’immagine del banner generata viene ritagliata per adattarla a una pagina web: i metadati C2PA vengono conservati attraverso il ritaglio. </br> Una foto stock caricata, utilizzata come sfondo di notifica push, viene ritagliata per adattarsi allo schermo: poiché la foto stock non comporta alcuna azione AI generativa, non vengono creati metadati C2PA. |
| **Aggiungi una sovrapposizione di testo** | Rendering del testo generato sopra un&#39;immagine di sfondo | Solo se l’immagine di sfondo aveva già metadati C2PA. Il rendering della sovrapposizione produce una nuova immagine dallo sfondo più il testo, che normalmente cancella i metadati C2PA, quindi Genera contenuto lo legge prima dall&#39;immagine di sfondo, quindi lo ricostruisce e lo ricollega al risultato. Il passaggio di sovrapposizione non aggiunge una nuova azione di IA generativa. | Un titolo promozionale viene riprodotto come sovrapposizione di testo su un’immagine di sfondo generata per una pagina di destinazione: i metadati C2PA dell’immagine di sfondo vengono mantenuti. |
| **Sovrapponi immagini** | Composito di due o più immagini | Se una delle immagini sorgente ha metadati C2PA, l&#39;immagine combinata le trasporta tutte, unite in un unico metadati C2PA. La composizione produce una nuova immagine dalle sorgenti, che normalmente cancellerebbe quei metadati C2PA, quindi Genera contenuto legge ogni una prima della composizione, quindi crea un singolo metadati C2PA combinati elencando ogni sorgente che ha contribuito a un’azione di intelligenza artificiale generativa. | Un’immagine del prodotto generata viene composta con uno sfondo generato per un’intestazione e-mail: il risultato contiene metadati C2PA che riflettono entrambe le sorgenti di intelligenza artificiale generative. <br> Due foto del brand caricate vengono composte in un unico collage: poiché nessuna delle due origini è associata a un’azione di intelligenza artificiale generativa, non vengono creati metadati C2PA. |

## Tipi di contenuto e ambito {#cc-content-types}

* **Immagini**: coperte. I metadati C2PA vengono allegati quando le immagini vengono generate con IA generativa e vengono conservati mediante le operazioni di ritaglio, sovrapposizione di testo e sovrapposizione di immagini eseguite da Generate content.
* **Testo**: non applicabile. Gli output di solo testo di contenuti generati, come la generazione di copie, la traduzione e i suggerimenti di allineamento del brand, non richiedono metadati C2PA.

## Cosa succede quando il contenuto si sposta {#cc-content-moves}

I metadati C2PA viaggiano con il file di immagine. Quando un’immagine generata o modificata con IA generativa viene scaricata o esportata da Adobe Journey Optimizer, i relativi metadati C2PA vengono conservati. [Ulteriori informazioni sui metadati C2PA](https://helpx.adobe.com/it/firefly/using/content-credentials.html){target="_blank"}.

Alcuni modi di inserire immagini nel contenuto, come l’estrazione di un’immagine da un PDF o da una sorgente incorporata (base64), potrebbero non mantenere i metadati C2PA originali. In questi casi, non è possibile leggere metadati C2PA dalla sorgente e non ne viene creato alcuno per il risultato.

## Risorse aggiuntive

* [Linee guida utente per l’intelligenza artificiale generativa di Adobe Experience Cloud](https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [Guardrail e limitazioni](gs-generative.md#generative-guardrails)
* [Trasparenza dei contenuti di IA generativa](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency#related-links)