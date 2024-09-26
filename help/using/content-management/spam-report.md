---
title: Utilizzare il rapporto di posta indesiderata
description: Scopri come utilizzare il rapporto sullo spam delle e-mail.
feature: Preview
role: User
level: Beginner
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 9d95c3cf5c7f9a0da98654795370f40e84611dc9
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 17%

---

# Rapporto e-mail di spam {#spam-report}

>[!CONTEXTUALHELP]
>id="ajo_simulate_spam_report"
>title="Rapporto e-mail di spam"
>abstract="Il rapporto spam consente di controllare il relativo punteggio del contenuto delle e-mail. Questo punteggio indica se gli ISP o i provider di posta elettronica considereranno il messaggio come spam oppure no. Minore è il punteggio, meglio è. Se il punteggio del contenuto dell’e-mail è superiore a 2, è consigliabile risolvere i problemi che impediscono il corretto funzionamento dei test."

Puoi controllare il punteggio di posta indesiderata in un report spam dedicato. Utilizzando [SpamAssassin](https://spamassassin.apache.org/){target="_blank"}, Adobe Journey Optimizer può testare il contenuto delle e-mail e assegnargli un punteggio per indicare se gli ISP o i provider di cassette postali lo considereranno come spam o meno.

Quando modifichi o visualizzi in anteprima il contenuto delle e-mail, il pulsante **[!UICONTROL Rapporto spam]** fornisce un punteggio e consigli per migliorare i punteggi di ogni singolo elemento elencato.

Questa funzionalità ti consente di determinare se un messaggio può essere considerato come spam dagli strumenti anti-spam utilizzati al momento della ricezione e di intraprendere azioni in tal caso. Molti provider di posta in arrivo utilizzano gli strumenti come parte del processo di filtraggio della posta indesiderata. L’invio di e-mail con un punteggio errato può influire notevolmente sulla consegna dei messaggi.

Per accedere al **[!UICONTROL rapporto spam]**, segui la procedura riportata di seguito.

1. Dalla schermata **[!UICONTROL Simula]**, fai clic sul pulsante **[!UICONTROL Rapporto spam]**.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Viene eseguito automaticamente un controllo anti-spam e la finestra **[!UICONTROL Rapporto spam]** visualizza i risultati. Mostra come funziona il contenuto in termini di layout del corpo, struttura, dimensioni dell’immagine, parole attivatrici di spam, se presenti, ecc.

   ![](assets/spam-report-high-score.png)

1. Controlla i punteggi e le descrizioni di ogni elemento.

   Minore è il punteggio, meglio è. Se il punteggio è superiore a 5, viene visualizzato un avviso: indica che alcuni messaggi potrebbero essere bloccati o contrassegnati come spam al momento della ricezione. Si consiglia di avere un punteggio inferiore a 2.

   >[!NOTE]
   >
   >Il punteggio spam è derivato tramite [SpamAssassin](https://spamassassin.apache.org/){target="_blank"} e le regole non sono di proprietà di Adobe. Per ulteriori dettagli su queste regole, consulta la documentazione di SpamAssassin.
   >

1. In base a tale punteggio, se si ritiene che alcuni elementi possano essere migliorati, modificare il contenuto in [E-mail Designer](../email/content-from-scratch.md) e apportare gli aggiornamenti necessari.

1. Al termine delle modifiche, torna alla schermata **[!UICONTROL Rapporto spam]** per verificare che il punteggio sia migliorato.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
