---
title: Inviare bozze e-mail
description: Scopri come inviare bozze e-mail.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: 80935cc31ef88a322c2dd555fc8998935c6e5621
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 15%

---

# Inviare bozze e-mail {#send-proofs}

Una bozza è un messaggio specifico che consente di testare un messaggio prima che venga inviato al pubblico principale. I destinatari della bozza hanno il compito di approvare il messaggio: rendering, contenuto, impostazioni di personalizzazione, configurazione.

[!DNL Journey optimizer] consente inoltre di testare diverse varianti del contenuto visualizzandolo in anteprima e inviando bozze utilizzando dati di input di esempio caricati da un file CSV / JSON o aggiunti manualmente. [Scopri come verificare il contenuto utilizzando dati di input di esempio](../test-approve/simulate-sample-input.md)

>[!PREREQUISITES]
>
>Per inviare le bozze, devi disporre delle autorizzazioni **Approva e pubblica** per la risorsa specifica (campagna o percorso) associata all&#39;e-mail. Inoltre, per inviare bozze in un percorso, è necessaria anche l&#39;autorizzazione **Pubblica percorso**. [Ulteriori informazioni sulle autorizzazioni](../administration/ootb-permissions.md).


Per inviare le bozze delle e-mail, devi prima selezionare [profili di test](test-profiles.md). Quindi, segui questi passaggi:

1. Nella schermata **[!UICONTROL Simula]**, fai clic sul pulsante **[!UICONTROL Invia bozza]**.

   ![](../email/assets/send-proof-button.png)

1. Dalla finestra **[!UICONTROL Invia bozza]**, digita nell&#39;e-mail del destinatario e fai clic su **[!UICONTROL Aggiungi]** per inviare la bozza a te stesso o a membri delle tue organizzazioni.

   Puoi aggiungere fino a dieci destinatari per la consegna della bozza.

   ![](../email/assets/send-proof-add.png)

1. Seleziona i **Profili di test** da utilizzare per personalizzare il contenuto del messaggio.

   Ogni destinatario della bozza riceve tanti messaggi quanti sono i profili di test selezionati. Ad esempio, se hai aggiunto cinque e-mail dei destinatari e hai selezionato dieci profili di test, invierai cinquanta messaggi di bozza e ogni destinatario ne riceverà dieci.

1. Se necessario, puoi aggiungere un prefisso alla riga dell’oggetto della bozza. Solo caratteri alfanumerici e caratteri speciali come . - _ ( ) [ ] sono consentiti come prefisso per la riga dell&#39;oggetto.

1. Fai clic su **[!UICONTROL Invia bozza]**.

   ![](../email/assets/send-proof-select.png)

1. Nella schermata **[!UICONTROL Simula]**, fai clic sul pulsante **[!UICONTROL Visualizza bozze]** per verificare lo stato.

   ![](../email/assets/send-proof-view.png)

Si consiglia di inviare le bozze dopo ogni modifica al contenuto del messaggio.

>[!NOTE]
>
>Nella bozza inviata, il collegamento alla pagina speculare non è attivo. Viene attivato solo nei messaggi finali.
