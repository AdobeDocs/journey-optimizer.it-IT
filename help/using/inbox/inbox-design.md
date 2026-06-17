---
title: Casella in entrata progettazione
description: Progettare l’elenco della casella in entrata e le viste espanse, i modelli e il comportamento di interazione per i messaggi della casella in entrata in Adobe Journey Optimizer.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 0ab71b21-0085-4a93-b319-3c960bd8f7dd
source-git-commit: 8ef401e6c92d94631f02762e4dc9ffab60657cb4
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Progettare una casella in entrata {#inbox-design}

>[!BEGINSHADEBOX]

**In questa pagina:** configura il layout, la capacità, gli indicatori non letti e lo stato vuoto del canale Posta in arrivo in modo che i messaggi vengano visualizzati nel marchio e siano leggibili, offrendo ai profili di destinazione un&#39;esperienza chiara e coerente nelle modalità chiara e scura.

>[!ENDSHADEBOX]

La progettazione della casella in entrata governa il modo in cui ogni messaggio viene riprodotto sui profili di destinazione all’interno della superficie della casella in entrata. La configurazione include il modello della casella in entrata, elenchi e presentazioni espanse e indicatori di stato di lettura che distinguono i nuovi messaggi da quelli già visualizzati.

Per la procedura completa per la creazione di una campagna casella in entrata, fare riferimento a [Creare una casella in entrata](inbox-create.md).

1. Apri la scheda **[!UICONTROL Contenuto]** della [campagna Posta in arrivo creata](inbox-create.md).

1. Imposta il **[!UICONTROL titolo contenitore]**.

1. Seleziona un layout casella in entrata:

   * **[!UICONTROL Layout elenco]**: mostra ogni scheda di contenuto in un elenco verticale in modo che i profili possano scorrere i messaggi e aprirli uno alla volta.

   * **[!UICONTROL Layout carosello]**: mostra le schede in un carosello orizzontale in modo che i profili possano scorrere o spostarsi lateralmente tra le evidenziazioni senza uscire dalla superficie della casella in entrata.

   ![](assets/inbox-design-1.png)

1. Specifica la **capacità** della casella in entrata, il numero massimo di schede di contenuto che la casella in entrata è configurata per contenere.

1. Attiva **[!UICONTROL Impostazioni non lette]** e configura la modalità di visualizzazione dei messaggi non letti:

   * **[!UICONTROL URL immagine icona non letta]**: fornisci l&#39;immagine visualizzata accanto o su elementi non letti; aggiungi un URL in modalità scura in modo che l&#39;icona rimanga visibile e nel marchio quando l&#39;app o il sito utilizza un tema scuro.

   * **[!UICONTROL Colori di sfondo]**: imposta i colori per la modalità chiara e, se necessario, scura in modo che il trattamento da leggere corrisponda al tuo marchio e rimanga leggibile sullo sfondo della casella in entrata.

   * **[!UICONTROL Posizionamento]**: utilizza l&#39;elenco a discesa per scegliere dove l&#39;icona da leggere deve essere allineata al layout.

   ![](assets/inbox-design-2.png)

1. In **[!UICONTROL Stato vuoto]**, configura i profili visualizzati in assenza di messaggi:

   * **[!UICONTROL Testo del messaggio]**: testo breve che indica che la casella in entrata è vuota o suggerisce un passaggio successivo.

   * **[!UICONTROL URL immagine]**: illustrazione o elemento grafico facoltativo per la modalità chiara che rafforza lo stato vuoto invece di mostrare un&#39;area vuota.

   * **[!UICONTROL URL immagine scura]**: immagine facoltativa ottimizzata per la modalità scura in modo che lo stato vuoto appaia corretto senza contrasto minimo o bordi netti.

   ![](assets/inbox-design-3.png)

1. Fai clic sull&#39;![icona della barra](assets/do-not-localize/Smock_Rail_18_N.svg) per aprire il pannello di anteprima e controllare come viene visualizzata la casella in entrata vuota.

   ![](assets/inbox-design-3.png)

1. Nella sezione **[!UICONTROL Dati]**, fai clic su **[!UICONTROL Aggiungi meta]** per aggiungere coppie chiave/valore personalizzate al payload.

1. Fai clic sull&#39;icona ![](assets/do-not-localize/Smock_StarOutline_18_N.svg) per aprire un&#39;anteprima in modalità scura della casella in entrata e confermare i colori e le immagini del tema scuro.

   ![](assets/inbox-design-4.png)

Quando sei pronto, controlla le impostazioni e attiva la casella in entrata. Dopo l&#39;attivazione, potrai utilizzarlo con [schede di contenuto](../content-card/create-content-card.md).

