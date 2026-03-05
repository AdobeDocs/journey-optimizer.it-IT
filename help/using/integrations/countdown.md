---
solution: Journey Optimizer
product: journey optimizer
title: Dynamic Media
description: Utilizzare Dynamic Media con Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4c1d39c4-3154-4bec-ac3c-c2ead7164d69
source-git-commit: c9856234149c0f377e625a789c96f1f1f0453000
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Inserisci timer conto alla rovescia {#countdown}

Crea un’urgenza e massimizza le conversioni con i timer di conto alla rovescia di Dynamic Media che vengono aggiornati in tempo reale quando i destinatari aprono le e-mail. Questa funzione è ideale per vendite flash, offerte a tempo limitato e promozioni sensibili al tempo.

Ad esempio, come addetto al marketing per un marchio per la vendita al dettaglio, hai una vendita flash di 48 ore. Utilizzando il timer del conto alla rovescia nelle e-mail promozionali:

* Per i destinatari che aprono immediatamente, vedere &quot;47 ore rimanenti&quot;
* Per i destinatari che aprono 24 ore dopo, vedere &quot;23 ore rimanenti&quot;
* I destinatari che aprono dopo il termine della vendita vedono &quot;Vendita conclusa&quot;

Per ulteriori informazioni su come aggiungere timer di conto alla rovescia al modello Dynamic Media in Adobe Experience Manager, consulta [questo documento](assets/do-not-localize/countdown.pdf).


1. In **[!DNL Adobe Experience Manager]** creare un modello Dynamic Media e aggiungervi un componente timer per il conto alla rovescia.

   ![](assets/timer-1.png)

1. In **[!DNL Journey Optimizer]**, creare una nuova campagna o aprirne una esistente, quindi accedere al Designer e-mail.

1. Trascina e rilascia un componente **HTML** o **Asset** nel contenuto dell&#39;e-mail.

1. Passa il puntatore del mouse sul componente e fai clic su **[!UICONTROL Mostra il codice sorgente]** (per i componenti di HTML) o su **[!UICONTROL Sfoglia]** (per i componenti di Asset).

   ![](assets/timer-2.png)

1. Dal menu **[!UICONTROL Modifica HTML]**, passa a **[!UICONTROL Assets]** e fai clic su **[!UICONTROL Apri selettore risorse]** per sfogliare e selezionare il modello Dynamic Media pubblicato.

   ![](assets/timer-3.png)

1. Nel menu **[!UICONTROL Attributi personalizzati]**, configura eventuali parametri URL personalizzabili in base alle esigenze del modello.

   Al termine, fai clic su **[!UICONTROL Salva]**.

   ![](assets/timer-4.png)

1. Seleziona la risorsa nel Designer e-mail, quindi accedi al menu **[!UICONTROL Impostazioni]**.

   Configura quanto segue:

   * **Testo banner**: il testo visualizzato con il timer
   * **Ora di fine**: la data e l&#39;ora in cui scade il conto alla rovescia. Immetti l’ora solo in GMT (ora di Greenwich). Il sistema non accetta altri fusi orari.
   * **Testo di fallback**: messaggio visualizzato al termine del timer

   ![](assets/timer-5.png)

1. Fai clic su **[!UICONTROL Anteprima]** per visualizzare il timer con aggiornamenti del conto alla rovescia in tempo reale e verificare la configurazione.

Quando i destinatari aprono l’e-mail, visualizzano il tempo rimanente esatto per la vendita flash. Se riaprono l’e-mail in un secondo momento, il conto alla rovescia si aggiorna automaticamente per riflettere l’ora corrente rimanente. Dopo la data di fine, il messaggio predefinito viene visualizzato automaticamente.
