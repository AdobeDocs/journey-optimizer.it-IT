---
solution: Journey Optimizer
product: journey optimizer
title: Coinvolgi i clienti tramite l’attività di navigazione
description: Coinvolgi i clienti tramite l’attività di navigazione
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 2%

---

# Coinvolgi i clienti tramite l’attività di navigazione {#engage-customers-uc}

>[!BEGINSHADEBOX]

Tieni presente che questo caso d’uso inizia con un pubblico che esiste già in Experience Platform, in particolare un pubblico di comportamento web in tempo reale che raccoglie l’attività di navigazione mentre si verifica. [Ulteriori informazioni in Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

**Schemi necessari per questo caso d&#39;uso:**

* **Destinatari**: utilizzato come dimensione di targeting, con campi: `email`, `churnprop`
* **Elenco desideri**: con campi: `description`, `priceref`, `imageurl`

➡️ [Scopri come configurare gli schemi basati su modelli](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

Questa campagna è destinata ai clienti che hanno navigato nella categoria attrezzatura da allenamento. Il pubblico viene deduplicato e segmentato in base al rischio di abbandono, alla probabilità che qualcuno smetta di coinvolgersi o di acquistare.

I clienti ad alto rischio si riuniscono in un nuovo pubblico separato che verrà successivamente utilizzato per una comunicazione specifica, mentre i clienti a basso e medio rischio seguono un percorso in più passaggi con e-mail e follow-up personalizzati.

1. Per iniziare, imposta una nuova campagna mirata in modo specifico al **reengagement della lista dei desideri**. In questo modo, il messaggio sarà incentrato sui clienti che hanno già dimostrato di avere intenzione di acquisto, salvando i prodotti nella propria lista dei desideri.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Compila le **[!UICONTROL Impostazioni campagna]**, ad esempio il nome della campagna, la descrizione, le date di inizio e fine e i tag pertinenti.

1. Aggiungi un&#39;attività **[!UICONTROL Read audience]** per selezionare un pubblico predefinito da Adobe Experience Platform, in questo caso, i clienti che hanno navigato nella categoria Attrezzature sul tuo sito Web.

   I destinatari sono identificati con i loro indirizzi e-mail selezionati dal campo **[!UICONTROL Entità]**.

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. Aggiungi un&#39;attività **[!UICONTROL Deduplicazione]** per rimuovere gli indirizzi e-mail duplicati dal pubblico, assicurandoti che ogni cliente riceva un solo messaggio.

1. Fare clic su **[!UICONTROL Aggiungi attributo]** e selezionare e-mail come attributo per la deduplicazione.

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. Quindi, aggiungi un&#39;attività **[!UICONTROL Dividi]** per segmentare i clienti in base alla loro probabilità di abbandono, consentendoti di fornire esperienze personalizzate su misura per ogni gruppo di clienti.

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. Fai clic su **[!UICONTROL Aggiungi segmento]** per creare tre gruppi:

   * Rischio ridotto

   * Rischio Medium

   * Rischio elevato

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. Fai clic su **[!UICONTROL Crea filtro]** per definire la probabilità di abbandono per ogni gruppo.

   Utilizza l&#39;**Editor condizioni** per impostare i valori specifici che determinano il rischio di abbandono di ogni cliente.

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. Ogni segmento viene gestito in modo diverso:

   * [Rischio basso/medio](#low-medium-risk)
   * [Rischio elevato](#high-risk)

1. Una volta che la campagna è testata e pronta, fai clic su **[!UICONTROL Pubblica]** per renderla disponibile.

Dopo l’esecuzione della campagna, esplora il dashboard di reporting per rivedere le metriche delle prestazioni e le informazioni chiave.

➡️ [Ulteriori informazioni sul reporting](../reports/campaign-global-report-cja.md)

## Segmenti ad alto rischio {#high-risk}

Per i clienti che presentano un rischio elevato di abbandono, crea un segmento di pubblico dedicato. Questo pubblico viene successivamente utilizzato per comunicazioni separate e mirate.

1. Aggiungi **[!UICONTROL Salva pubblico]**.

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. Aggiungi una **[!UICONTROL etichetta]** al tuo pubblico e scegli il **[!UICONTROL campo di mappatura profilo]**, qui **destinatari-e-mail**.

   ![](assets/uc-interest-8.png){zoomable="yes"}

Questo pubblico viene quindi salvato in Experience Cloud, dove può essere successivamente utilizzato per una specifica campagna mirata.

## Segmenti di rischio medio/basso {#low-medium-risk}

Per i clienti a basso e medio rischio di abbandono, configura una campagna in più fasi volta a rafforzare il coinvolgimento:

1. Combina i rischi Basso e Medium con un&#39;attività **[!UICONTROL Unione]**.

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. Aggiungi un&#39;attività **[!UICONTROL Enrichment]** per personalizzare la campagna con la lista dei desideri e le informazioni sul prodotto.

1. Fare clic su **[!UICONTROL Aggiungi attributo]** per creare i tre attributi seguenti:

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   Questo arricchisce il messaggio con informazioni dettagliate sulla lista dei desideri.

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. Crea un nuovo pubblico per il retargeting basato sul coinvolgimento con le e-mail.

   Qui creiamo un pubblico basato su eventi di clic e-mail, per eseguire il retargeting di tutte le persone che hanno interagito con un’e-mail inviata in precedenza e, in particolare, hanno fatto clic su un collegamento all’interno di quel messaggio.

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. Dividi uniformemente il coinvolgimento per inviare un follow-up tramite SMS o notifiche push per incoraggiare le conversioni.

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. Crea il contenuto del messaggio per ogni canale, inclusi gli attributi del profilo, come il nome del destinatario, e dati di arricchimento come gli elementi della lista dei desideri, per personalizzare ogni messaggio.

   ![](assets/uc-interest-13.png){zoomable="yes"}
