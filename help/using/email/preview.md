---
solution: Journey Optimizer
product: journey optimizer
title: Anteprima dei messaggi e invio delle bozze
description: Scopri come visualizzare in anteprima e verificare i messaggi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: a7c9cbcc23e4a2ef8a3acd887c0f51e51c5befc0
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 4%

---

# Anteprima e verifica dei messaggi {#preview-and-proof}

Una volta definito il contenuto dell’e-mail, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo. Se hai inserito [contenuti personalizzati](../personalization/personalize.md), puoi controllare come questo contenuto viene visualizzato nel messaggio, utilizzando i dati del profilo di test.

Per rilevare eventuali errori nel contenuto delle e-mail o nelle impostazioni di personalizzazione, invia delle bozze ai profili di test. È necessario inviare una prova ogni volta che viene apportata una modifica per convalidare il contenuto più recente.

>[!CAUTION]
>
>Per visualizzare l’anteprima dei messaggi e inviare delle bozze, devi disporre dei profili di test.
>
>Scopri come creare profili di test in [questa pagina](../segment/creating-test-profiles.md).

Per testare il contenuto delle e-mail, devi:

* [Selezionare i profili di test](#select-test-profiles)
* [Controlla l’anteprima del messaggio](#preview-your-messages)

Potrai quindi [inviare bozze](#send-proofs) ai profili di test.

Inoltre, utilizza in [!DNL Journey Optimizer] le informazioni del tuo account **Litmus** per visualizzare all’istantante l’anteprima del **rendering di e-mail** nei client e-mail più diffusi. Puoi quindi verificare che il contenuto dell’e-mail si presenti e funzioni correttamente in ogni casella in entrata. Scopri come sbloccare le anteprime e-mail di Litmus in [questa sezione](#email-rendering).

>[!CAUTION]
>
>Quando visualizzi in anteprima un messaggio o invii bozze, vengono visualizzati solo i dati di personalizzazione del profilo. La personalizzazione basata sui dati contestuali, ad esempio le informazioni sull’evento, può essere testata solo nel contesto di un percorso. Scopri come verificare la personalizzazione in [questo caso d&#39;uso](../personalization/personalization-use-case.md).

➡️ [Scopri come visualizzare in anteprima e verificare il tuo messaggio e-mail in questo video](#video-preview)

## Selezionare i profili di test {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Anteprima e verifica dei messaggi"
>abstract="Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/preview.html?lang=en#email-rendering" text="Rendering di e-mail"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/preview.html?lang=en#preview-email" text="Anteprima"

Utilizzo [Profili di test](../segment/creating-test-profiles.md) per eseguire il targeting di altri destinatari che non soddisfano i criteri di targeting definiti.

Per selezionare i profili di test, segui i passaggi seguenti:

1. In [Modifica contenuto](create-email.md#define-email-content) In E-mail Designer, fai clic sul pulsante **[!UICONTROL Simulazione del contenuto]** per accedere alla selezione del profilo di test.

   ![](assets/email-preview-button.png)

1. Seleziona **[!UICONTROL Gestire i profili di test]**.

   ![](assets/email-preview_manage-test-profiles.png)

1. Seleziona lo spazio dei nomi da utilizzare per identificare i profili di test facendo clic sul pulsante **[!UICONTROL Spazio dei nomi identità]** icona di selezione.

   ![](assets/previewselect-namespace.png)

   Ulteriori informazioni sui namespace delle identità Adobe Experience Platform [in questa sezione](../segment/get-started-identity.md).

   Nell’esempio seguente, utilizzeremo il **E-mail** spazio dei nomi.

1. Utilizza il campo di ricerca per trovare lo spazio dei nomi, selezionalo e fai clic su **[!UICONTROL Seleziona]**

   ![](assets/preview-email-namespace.png)

1. In **[!UICONTROL Valore identità]** inserisci il valore (qui l’indirizzo e-mail) per identificare il profilo di test e fai clic su **[!UICONTROL Aggiungi profilo]**.

   <!--![](assets/preview-identity-value.png)-->

1. Se hai aggiunto la personalizzazione al messaggio, aggiungi altri profili in modo da poter testare diverse varianti del messaggio in base ai dati del profilo. Una volta aggiunti, i profili sono elencati nei campi selezionati.

   ![](assets/preview-profile-list.png)

   In base agli elementi di personalizzazione dei messaggi, questo elenco visualizza i dati per ciascun profilo di test nelle colonne correlate.

### Anteprima e-mail {#preview-email}

Una volta [profili di test](#select-test-profiles) sono selezionati e puoi visualizzare in anteprima il contenuto dell’e-mail. Effettua le seguenti operazioni:

1. In [Modifica contenuto](create-email.md#define-email-content) In E-mail Designer, fai clic sul pulsante **[!UICONTROL Simulazione del contenuto]** pulsante .

1. Seleziona un profilo di test. Puoi controllare i valori disponibili nelle colonne. Utilizza le frecce destra/sinistra per sfogliare i dati.

   ![](assets/preview-select-profile.png)

   >[!NOTE]
   >
   >Per aggiungere altri profili di test, seleziona **[!UICONTROL Gestire i profili di test]**. [Ulteriori informazioni](#select-test-profiles)

1. Fai clic sul pulsante **[!UICONTROL Seleziona dati]** , sopra l’elenco per aggiungere o rimuovere colonne.

   ![](assets/preview-select-data.png)

   Puoi visualizzare i campi di personalizzazione specifici per il messaggio corrente alla fine dell’elenco. In questo esempio, la città del profilo, il nome e il cognome. Seleziona tali campi e assicurati che questi valori siano popolati nei profili di test.

1. Nell’anteprima dei messaggi, gli elementi personalizzati vengono sostituiti dai dati del profilo di test selezionati.

   Ad esempio, per questo messaggio, sia il contenuto dell’e-mail che l’oggetto dell’e-mail sono personalizzati:

   ![](assets/preview-test-profile.png)

1. Seleziona altri profili di test per visualizzare in anteprima il rendering delle e-mail per ogni variante del messaggio.

## Invia bozze {#send-proofs}

Una bozza è un messaggio specifico che ti consente di testare un messaggio prima di inviarlo al pubblico principale. I destinatari della bozza hanno il compito di approvare il messaggio: rendering, contenuto, impostazioni di personalizzazione, configurazione.

Una volta [profili di test](#select-test-profiles) sono selezionati, è possibile inviare bozze.

1. In **[!UICONTROL Simula]** fai clic su **[!UICONTROL Invia bozza]** pulsante .

   ![](assets/send-proof-button.png)

1. Da **[!UICONTROL Invia bozza]** finestra, digita l’e-mail del destinatario e fai clic su **[!UICONTROL Aggiungi]** per inviare la bozza a te stesso o ai membri delle tue organizzazioni.

   Puoi aggiungere fino a dieci destinatari per la consegna delle prove.

   ![](assets/send-proof-add.png)

1. Quindi, seleziona la **Profili di test** che verrà utilizzato per personalizzare il contenuto del messaggio.

   Ogni destinatario della bozza riceverà altrettanti messaggi del numero di profili di test selezionati. Ad esempio, se hai aggiunto cinque e-mail del destinatario e hai selezionato dieci profili di test, invierai cinquanta messaggi a prova di errore e ogni destinatario ne riceverà dieci.

1. Se necessario, puoi aggiungere un prefisso alla riga dell’oggetto della bozza. Solo caratteri alfanumerici e caratteri speciali come . - _ ( ) [ ] sono consentiti come prefisso alla riga dell’oggetto.

1. Fai clic su **[!UICONTROL Invia bozza]**.

   ![](assets/send-proof-select.png)

1. Indietro nel  **[!UICONTROL Simula]** fai clic su  **[!UICONTROL Visualizza bozze]** per controllare lo stato.

   ![](assets/send-proof-view.png)

È consigliabile inviare bozze dopo ogni modifica al contenuto del messaggio.

>[!NOTE]
>
>Nella bozza inviata, il collegamento alla pagina speculare non è attivo. Viene attivato solo nei messaggi finali.

## Utilizzare il rendering di e-mail {#email-rendering}

Puoi sfruttare **Litmo** tenere conto [!DNL Journey Optimizer] per visualizzare istantaneamente l&#39;anteprima del **rendering di e-mail** nei client e-mail popolari.

Per accedere alle funzionalità di rendering di e-mail, devi:

* Avere un account Litmus
* [Selezionare i profili di test](#select-test-profiles)

Quindi, segui i passaggi seguenti:

1. In [Modifica contenuto](create-email.md#define-email-content) In E-mail Designer, fai clic sul pulsante **[!UICONTROL Simulazione del contenuto]** pulsante .

1. Seleziona la **[!UICONTROL Invia e-mail di rendering]** pulsante .

   ![](assets/email-rendering-button.png)

1. Fai clic su **Collegare l&#39;account Litmus** nella parte superiore destra.

   ![](assets/email-rendering-litmus.png)

1. Immetti le tue credenziali e accedi.

   ![](assets/email-rendering-credentials.png)

1. Fai clic sul pulsante **Esegui test** per generare anteprime e-mail.

1. Controlla il contenuto delle tue e-mail nei popolari client desktop, mobili e basati su web.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>Quando si collega il **Litmo** account con [!DNL Journey Optimizer], l’utente accetta che i messaggi di prova siano inviati a Litmus: una volta inviate, queste e-mail non vengono più gestite da Adobe. Di conseguenza, i criteri di conservazione dei dati Litmus si applicano a queste e-mail, compresi i dati di personalizzazione che possono essere inclusi in questi messaggi di test.

## Video introduttivo {#video-preview}

Scopri come testare il rendering delle e-mail tra le caselle in entrata, come visualizzare in anteprima le e-mail personalizzate rispetto ai profili di test e come inviare bozze.

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)
