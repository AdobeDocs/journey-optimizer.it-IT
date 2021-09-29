---
title: Anteprima dei messaggi e invio delle bozze
description: Scopri come visualizzare in anteprima e verificare i messaggi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: 5c4aca7666987ed188e69f3b5772950c0bf96488
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 2%

---

# Anteprima e verifica dei messaggi{#preview-and-proof}

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo. Se hai inserito [contenuto personalizzato](personalization/personalize.md), potrai controllare come questo contenuto viene visualizzato nel messaggio, sfruttando i dati del profilo di test.

Per rilevare eventuali errori nel contenuto delle e-mail o nelle impostazioni di personalizzazione, invia delle bozze ai profili di test. Per convalidare il contenuto più recente, è necessario inviare una bozza ogni volta che viene apportata una modifica.

>[!CAUTION]
>
>Per visualizzare l’anteprima dei messaggi e inviare delle bozze, devi disporre dei profili di test.
>
>Scopri come creare profili di test in [questa pagina](building-journeys/creating-test-profiles.md).

Per testare il contenuto del messaggio, devi:

* [seleziona profili di test](#select-test-profiles)
* [controlla l’anteprima del messaggio](#preview-your-messages)

Potrai quindi [inviare bozze](#send-proofs) ai profili di test.

Inoltre, sfrutta il tuo account **Litmus** in [!DNL Journey Optimizer] per visualizzare immediatamente l&#39;anteprima del **rendering delle e-mail** nei popolari client e-mail. Puoi quindi verificare che il contenuto dell’e-mail sia eccellente e funzioni correttamente in ogni casella in entrata. Scopri come sbloccare le anteprime e-mail di Litmus in [questa sezione](#email-rendering)

>[!CAUTION]
>
>Quando visualizzi in anteprima un messaggio o invii bozze, vengono visualizzati solo i dati di personalizzazione del profilo. La personalizzazione basata sui dati contestuali, ad esempio le informazioni sull’evento, può essere testata solo nel contesto di un percorso. Scopri come verificare la personalizzazione in [questo caso d’uso](personalization/personalization-use-case.md).

➡️ [Scopri come visualizzare in anteprima, provare e pubblicare il tuo messaggio e-mail in questo video](#video-preview)

## Selezionare i profili di test{#select-test-profiles}

Utilizza [Profili di test](building-journeys/creating-test-profiles.md) per eseguire il targeting di destinatari aggiuntivi che non soddisfano i criteri di targeting definiti.

Per selezionare i profili di test, segui i passaggi seguenti:

1. Nell’interfaccia dei messaggi o nella finestra di progettazione e-mail, fai clic sul pulsante **[!UICONTROL Show preview]** per accedere alla selezione del profilo di test.

   ![](assets/email-preview-button.png)

1. Seleziona lo spazio dei nomi da utilizzare per identificare i profili di test facendo clic sull’icona di selezione **[!UICONTROL Identity namespace]** .

   ![](assets/previewselect-namespace.png)

   Ulteriori informazioni sugli spazi dei nomi delle identità Adobe Experience Platform [in questa sezione](get-started-identity.md){target=&quot;_blank&quot;}.

   Nell’esempio seguente, utilizzeremo lo spazio dei nomi **Email** .

1. Usa il campo di ricerca per trovare lo spazio dei nomi, selezionalo e fai clic su **[!UICONTROL Select]**

   ![](assets/preview-email-namespace.png)

1. Immetti il valore per identificare il profilo di test e fai clic su **[!UICONTROL Find test profile]**.

   ![](assets/preview-identity-value.png)

1. Se hai aggiunto la personalizzazione nel messaggio, aggiungi altri profili in modo da poter testare diverse varianti del messaggio in base ai dati del profilo. Una volta aggiunti, i profili sono elencati nei campi di selezione.

   ![](assets/preview-profile-list.png)

   In base agli elementi di personalizzazione dei messaggi, questo elenco visualizza i dati per ciascun profilo di test nelle colonne correlate.

## Anteprima dei messaggi{#preview-your-messages}

Una volta selezionati i [profili di test](#select-test-profiles), puoi visualizzare in anteprima i messaggi e controllarne il contenuto.

1. Fai clic sulla scheda **[!UICONTROL Preview]** per verificare il messaggio.

1. Seleziona un profilo di test. Puoi controllare i valori disponibili nelle colonne. Utilizza le frecce destra/sinistra per sfogliare i dati.

   ![](assets/preview-tab-select-profile.png)

1. Fai clic sull’icona **[!UICONTROL Select data]** sopra l’elenco per aggiungere o rimuovere colonne.

   ![](assets/preview-select-data.png)

   Puoi visualizzare i campi di personalizzazione specifici per il messaggio corrente alla fine dell’elenco. In questo esempio, la città del profilo, il nome e il cognome. Seleziona tali campi e assicurati che questi valori siano popolati nei profili di test.

1. Nell’anteprima dei messaggi, gli elementi personalizzati vengono sostituiti dai dati del profilo di test selezionati.

   Ad esempio, per questo messaggio, sia il contenuto dell’e-mail che l’oggetto dell’e-mail sono personalizzati:

   ![](assets/preview-test-profile.png)

1. Seleziona altri profili di test per visualizzare in anteprima il rendering delle e-mail per ogni variante del messaggio.

Per un&#39;anteprima di notifica push:

1. Passa al canale **[!UICONTROL Push]** dall&#39;elenco a discesa **[!UICONTROL Channels]** in alto a destra nella schermata **[!UICONTROL Preview]**.

   ![](assets/preview-select-channel.png)

1. Applica gli stessi passaggi descritti in precedenza per selezionare un profilo di test e seleziona il tipo di dispositivo per visualizzare in anteprima il contenuto: **[!UICONTROL iOS]** o **[!UICONTROL Android]**

   ![](assets/preview-iOS.png)

1. Nell’anteprima push, i dati del profilo di test vengono utilizzati nel contenuto del messaggio.

   Ad esempio, per questa notifica push, titolo e corpo sono personalizzati:

   ![](assets/preview-android.png)

## Invia bozze{#send-proofs}

Una bozza è un messaggio specifico che ti consente di testare un messaggio prima di inviarlo al pubblico principale. I destinatari della bozza hanno il compito di approvare il messaggio: rendering, contenuto, impostazioni di personalizzazione, configurazione.

Una volta selezionati i [profili di test](#select-test-profiles), puoi inviare le bozze.

1. Nella schermata **[!UICONTROL Preview]**, fai clic sul pulsante **[!UICONTROL Send proof]** .

   ![](assets/send-proof-button.png)

1. Dalla finestra **[!UICONTROL Send proof]**, oltre ai profili di test, digita l’e-mail del destinatario e fai clic su **[!UICONTROL Add]** per inviare la bozza a te stesso o ai membri delle organizzazioni.

   Puoi aggiungere fino a 10 destinatari per la consegna delle prove.

   ![](assets/send-proof-button_2.png)

1. Quindi, seleziona i profili di test che riceveranno la bozza e fai clic su **[!UICONTROL Send proof]**. Se necessario, puoi aggiungere un prefisso alla riga dell’oggetto della bozza. Solo caratteri alfanumerici e caratteri speciali, ad esempio . - _ ( ) [ ], sono consentiti come prefisso alla riga dell’oggetto.

   ![](assets/send-proof-select.png)

1. Nella schermata **[!UICONTROL Preview]** , fai clic sul pulsante **[!UICONTROL View proofs]** per controllare lo stato.

   ![](assets/send-proof-view.png)

Devi inviare bozze dopo qualsiasi modifica al contenuto del messaggio.

>[!NOTE]
>
> Nella bozza inviata ai profili di test, il collegamento alla pagina speculare non è attivo. Viene attivato solo nei messaggi finali.

## Rendering di e-mail{#email-rendering}

Puoi sfruttare il tuo account **Litmus** in [!DNL Journey Optimizer] per visualizzare immediatamente l&#39;anteprima del **rendering delle e-mail** nei client e-mail più popolari.

Per accedere alle funzionalità di rendering di e-mail, devi:

* Avere un account Litmus
* [Selezionare i profili di test](#select-test-profiles)

Quindi, segui i passaggi seguenti:

1. In E-mail Designer, fai clic sul pulsante **[!UICONTROL Preview]** e seleziona la scheda **[!UICONTROL Email rendering]** .

1. Fai clic su **Collega l&#39;account Litmus** nella sezione in alto a destra.

   ![](assets/email-rendering-litmus.png)

1. Immetti le tue credenziali e accedi.

   ![](assets/email-rendering-credentials.png)

1. Fai clic sul pulsante **Esegui test** per generare anteprime e-mail.

1. Controlla il contenuto delle tue e-mail nei popolari client desktop, mobili e basati su web.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>Quando connetti l&#39;account **Litmus** con [!DNL Journey Optimizer], accetti l&#39;invio di messaggi di prova a Litmus: una volta inviate, queste e-mail non vengono più gestite da Adobe. Di conseguenza, i criteri di conservazione dei dati Litmus si applicano a queste e-mail, compresi i dati di personalizzazione che possono essere inclusi in questi messaggi di test.

## Video introduttivo{#video-preview}

Scopri come verificare il rendering delle e-mail nelle caselle in entrata, visualizzare in anteprima le e-mail personalizzate rispetto ai profili di test, inviare bozze e pubblicare le e-mail.

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)
