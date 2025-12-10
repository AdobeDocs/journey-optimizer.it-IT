---
solution: Journey Optimizer
product: journey optimizer
title: Notifica agli utenti la disponibilità del prodotto
description: Notifica agli utenti la disponibilità del prodotto
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 3%

---

# Notifica agli utenti la disponibilità del prodotto {#product-availability-uc}

>[!BEGINSHADEBOX]

Questo caso d’uso mostra l’invio a più livelli: genera un’e-mail distinta per ogni voce della lista dei desideri utilizzando l’indirizzo e-mail memorizzato con il singolo elemento anziché con il record del destinatario. Questo consente ai clienti di ricevere notifiche separate per ogni prodotto nella lista dei desideri anche se utilizzano indirizzi e-mail diversi per elementi diversi.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

Progettare una notifica di back-in-stock per informare i clienti quando gli articoli dalla loro lista dei desideri diventano nuovamente disponibili. Questo messaggio consente di coinvolgere nuovamente i clienti interessati e li incoraggia a completare l’acquisto mentre l’inventario è rifornito.

1. Per iniziare, crea una nuova campagna mirata specificamente al coinvolgimento nella lista dei desideri. In questo modo, il messaggio sarà incentrato sui clienti che hanno già dimostrato di avere intenzione di acquisto, salvando i prodotti nella propria lista dei desideri.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Compila le **[!UICONTROL Impostazioni campagna]**, ad esempio il nome della campagna, la descrizione, le date di inizio e fine e i tag pertinenti.

1. Aggiungi un&#39;attività **[!UICONTROL Genera pubblico]** con Elenco desideri come **[!UICONTROL Dimensione targeting]**.

   ![](assets/notify-1.png){zoomable="yes"}

1. Aggiungi la condizione per includere solo le liste dei desideri create negli ultimi 36 mesi.

   ![](assets/notify-2.png){zoomable="yes"}

1. Aggiungi un&#39;attività **[!UICONTROL Modifica dimensione]** per tornare dalla lista dei desideri al rispettivo set di clienti per il targeting.

   ![](assets/notify-3.png){zoomable="yes"}

1. Dopo aver avviato la modalità bozza, visualizza l’anteprima del pubblico con i dettagli della lista dei desideri. Per approfondimenti, fai clic su un risultato e seleziona **[!UICONTROL Anteprima risultati]**.

   In questo caso, i dati mostrano sia i destinatari che le voci della lista dei desideri. Alcuni clienti hanno più elementi della lista dei desideri e, tramite un invio multilivello, ricevono un’e-mail separata per ogni elemento. In alcuni casi, i clienti utilizzano indirizzi e-mail diversi per richieste back-in-stock separate.

   ![](assets/notify-4.png){zoomable="yes"}

1. Per poter inviare un&#39;e-mail separata per ogni elemento, assicurati che [la tua configurazione e-mail](../orchestrated/target-dimension.md) sia impostata con `Recipients - email` come **[!UICONTROL Dimension di destinazione profilo]** e `Wishlistitems` come **[!UICONTROL dimensione secondaria]**.

   Dal menu **[!UICONTROL Indirizzo di esecuzione]**, selezionare `wishlist.email` come **[!UICONTROL Dimensione secondaria]**. Ogni voce della lista dei desideri attiva un’e-mail separata, utilizzando l’indirizzo e-mail memorizzato nei dati della lista dei desideri come dimensione secondaria.

   ![](assets/notify-5.png){zoomable="yes"}

1. Aggiungi un&#39;attività **[!UICONTROL Email]** per creare un messaggio di disponibilità del prodotto. Fai clic su **[!UICONTROL Modifica contenuto]** per iniziare a progettare il contenuto.

   ➡️ [Ulteriori informazioni sulla personalizzazione delle e-mail](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. Una volta che la campagna è testata e pronta, fai clic su **[!UICONTROL Pubblica]** per renderla disponibile.

Con questa campagna orchestrata, il cliente riceve un’e-mail separata per ogni elemento della propria lista dei desideri. Ogni messaggio viene inviato all’indirizzo e-mail specifico associato a quella lista dei desideri, con contenuto personalizzato tratto dai dettagli di quella particolare voce della lista dei desideri.

