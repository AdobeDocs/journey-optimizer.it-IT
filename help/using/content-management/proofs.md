---
title: Inviare bozze e-mail
description: Scopri come inviare bozze e-mail.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: f874456748a8bd7fce69c7ad2a7e69380d5336a6
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 10%

---

# Inviare bozze utilizzando i dati dei profili di test {#send-proofs}

Una bozza è un messaggio specifico che consente di testare un messaggio prima che venga inviato al pubblico principale. I destinatari della bozza hanno il compito di approvare il messaggio: rendering, contenuto, impostazioni di personalizzazione, configurazione.

>[!NOTE]
>
>[!DNL Journey Optimizer] consente inoltre di testare diverse varianti del contenuto visualizzandolo in anteprima e inviando bozze utilizzando dati di input di esempio caricati da un file CSV / JSON o aggiunti manualmente. [Scopri come simulare varianti di contenuto](../test-approve/simulate-sample-input.md)

## Da leggere {#must-read}

**Regole di quota limite** - Tutte le regole di quota limite esistenti si applicano alle bozze. Se hai impostato [regole di quota limite](../conflict-prioritization/channel-capping.md) (ad esempio, numero massimo di invii per profilo), questi limiti si applicano anche quando invii bozze. Se un profilo di test ha già raggiunto il limite di frequenza, le bozze verranno visualizzate come completate, ma non verrà consegnata alcuna e-mail. Per test ripetuti, è consigliabile utilizzare profili di test univoci o regolare i limiti di frequenza per gli scenari di verifica in base alle esigenze.

**Pagina mirror** - Nella bozza inviata, il collegamento alla pagina mirror non è attivo. Viene attivato solo nei messaggi finali.

**Assets** - Assets e le immagini dispongono di regole di accessibilità specifiche:

* Assets/Immagini sono accessibili nei contenuti consegnati o nei contenuti della bozza per un massimo di 2 anni (730 giorni) dalla loro prima pubblicazione in qualsiasi frammento/messaggio in linea.
* È necessaria una ripubblicazione dopo questo periodo di scadenza (ogni volta dopo 730 giorni) per mantenerli accessibili per altri 2 anni.
* Qualsiasi ripubblicazione effettuata entro 730 giorni dalla prima pubblicazione non prolunga la scadenza delle risorse/immagini ai successivi 730 giorni.

## Inviare bozze {#send-proofs-steps}

Per inviare bozze delle e-mail utilizzando i dati dei profili di test, devi prima selezionare [profili di test](test-profiles.md). Quindi, segui questi passaggi:

1. Nella schermata **[!UICONTROL Simula]**, fai clic sul pulsante **[!UICONTROL Invia bozza]**.

   ![Pulsante Invia bozza nella schermata di simulazione](../email/assets/send-proof-button.png)

1. Dalla finestra **[!UICONTROL Invia bozza]**, digita nell&#39;e-mail del destinatario e fai clic su **[!UICONTROL Aggiungi]** per inviare la bozza a te stesso o a membri della tua organizzazione.

   Puoi aggiungere fino a dieci destinatari per la consegna della bozza.

   ![Aggiungi destinatari alla consegna della bozza](../email/assets/send-proof-add.png)

1. Seleziona i **Profili di test** da utilizzare per personalizzare il contenuto del messaggio.

   Ogni destinatario della bozza riceve tanti messaggi quanti sono i profili di test selezionati. Ad esempio, se hai aggiunto cinque e-mail dei destinatari e hai selezionato dieci profili di test, invierai cinquanta messaggi di bozza. Ogni destinatario ne riceverà dieci.

1. Se necessario, puoi aggiungere un prefisso alla riga dell’oggetto della bozza. Solo caratteri alfanumerici e caratteri speciali come . - _ ( ) [ ] sono consentiti come prefisso per la riga dell&#39;oggetto.

1. Fai clic su **[!UICONTROL Invia bozza]**.

   ![Seleziona i profili di test e invia la bozza](../email/assets/send-proof-select.png)

1. Nella schermata **[!UICONTROL Simula]**, fai clic sul pulsante **[!UICONTROL Visualizza bozze]** per verificare lo stato.

   ![Pulsante Visualizza bozze per controllare lo stato della consegna](../email/assets/send-proof-view.png)

Si consiglia di inviare le bozze dopo ogni modifica al contenuto del messaggio.
