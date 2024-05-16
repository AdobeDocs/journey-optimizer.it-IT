---
title: Utilizzare il rapporto di posta indesiderata
description: Scopri come utilizzare il rapporto sulla posta indesiderata.
feature: Preview
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 8dacf28f4c3217a57e648b3c80e1724d9794c9ea
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Rapporto posta indesiderata {#spam-report}

[!DNL Journey Optimizer] consente di controllare le prestazioni del contenuto rispetto al filtro anti-spam e di assicurarsi che i messaggi arrivino nelle caselle in entrata dei clienti, non nella posta indesiderata.

Quando modifichi o visualizzi in anteprima il contenuto delle e-mail, il **[!UICONTROL Rapporto spam]** fornisce un punteggio e consigli per migliorare i punteggi di ogni singolo elemento elencato.

Ciò ti consente di determinare se un messaggio corre il rischio di essere considerato come spam dagli strumenti anti-spam utilizzati al momento della ricezione e di intraprendere azioni in caso contrario. Molti provider di posta in arrivo utilizzano gli strumenti come parte del processo di filtraggio della posta indesiderata. L’invio di e-mail con un punteggio errato può influire notevolmente sulla consegna dei messaggi.


>[!CAUTION]
>
>* Questa funzione è attualmente disponibile solo come versione beta privata.
>
>* Per il momento l’analisi del rapporto spam può essere eseguita solo per il contenuto in inglese.
>
>* >
>Il rapporto Spam è informativo e non impedisce l’invio di messaggi con un punteggio errato.

Per accedere al **[!UICONTROL Rapporto spam]**, segui la procedura indicata di seguito.

1. Dalla sezione **[!UICONTROL Simula]** , fare clic su **[!UICONTROL Rapporto spam]** pulsante.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Viene automaticamente eseguito un controllo anti-spam e **[!UICONTROL Rapporto spam]** visualizza i risultati. Mostra come funziona il contenuto in termini di layout del corpo, struttura, dimensioni dell’immagine, parole attivatrici di spam, se presenti, ecc.

   ![](assets/spam-report-high-score.png)

1. Controlla i punteggi e le descrizioni di ogni elemento.

   Più basso è il punteggio, meglio è. Se il punteggio è superiore a 5, viene visualizzato un avviso: indica che alcuni messaggi potrebbero essere bloccati o contrassegnati come spam al momento della ricezione.

1. In base a tale punteggio, se ritieni che alcuni elementi possano essere migliorati, modifica il contenuto in [E-mail Designer](../email/content-from-scratch.md) e apporta gli aggiornamenti necessari.

1. Al termine delle modifiche, torna a **[!UICONTROL Rapporto spam]** per garantire che il punteggio sia migliorato.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
