---
title: Progettare una pagina di destinazione
description: Scopri come progettare il contenuto di una pagina di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: c61b8d80-17e1-4fdd-a739-efcee032dc23
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Progettazione del contenuto della pagina di destinazione {#design-lp-content}

Per iniziare a creare contenuti per la destinazione [pagina principale](create-lp.md#configure-primary-page) o [sottopagine](create-lp.md#configure-subpages), passa il mouse sul contenuto della pagina principale e fai clic su **[!UICONTROL Open Designer]**. Puoi anche fare clic sul pulsante corrispondente nella palette a destra.

![](../assets/lp_open-designer.png)

Da qui puoi:

* **Progettare da zero la pagina di destinazione** tramite l’interfaccia di content designer e sfruttando le immagini di [Adobe Experience Manager Assets Essentials](../messages/assets-essentials.md). Scopri come progettare i contenuti o utilizzare modelli incorporati [in questa sezione](../messages/create-email-content.md).

* **Codice o incolla di HTML raw** direttamente nella finestra di progettazione dei contenuti. Scopri come codificare i contenuti personalizzati [in questa sezione](../messages/existing-content.md#import-raw-html-code).

* **Importare contenuto HTML esistente** da un file o da una cartella .zip. Scopri come importare il contenuto [in questa sezione](../messages/existing-content.md#import-html-content-from-file).

>[!NOTE]
>
>La finestra di progettazione del contenuto della pagina di destinazione è simile per lo più alla finestra di progettazione e-mail. Ulteriori informazioni su [progettazione di contenuti con [!DNL Journey Optimizer]](../messages/design-emails.md).

## Definire il contenuto specifico per la pagina di destinazione {#define-lp-specific-content}

Per definire contenuti specifici che consentano agli utenti di selezionare e inviare le proprie scelte dalla pagina di destinazione, effettua le seguenti operazioni.

1. Trascina e rilascia la pagina di destinazione specifica **[!UICONTROL Form]** dalla palette a sinistra nell’area di lavoro principale.

   ![](../assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >La **[!UICONTROL Form]** può essere utilizzato solo una volta sulla stessa pagina.

1. Selezionala. La **[!UICONTROL Form content]** nella palette a destra viene visualizzata la scheda che consente di modificare i diversi campi del modulo.

   ![](../assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Passa alla **[!UICONTROL Form style]** in qualsiasi momento per modificare gli stili del contenuto del componente modulo. [Ulteriori informazioni](#define-lp-styles)

1. Da **[!UICONTROL Checkbox 1]** Puoi modificare l’etichetta corrispondente a questa casella di controllo.

1. Definisci se questa casella di controllo è per consentire agli utenti di accedere o uscire: acconsentono a ricevere comunicazioni o chiedono di non essere più contattati?

   ![](../assets/lp_designer-form-update.png)

1. Scegli cosa verrà aggiornato tra le tre opzioni seguenti:

   ![](../assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Subscription list]**: Seleziona l’elenco di sottoscrizioni da aggiornare se il profilo seleziona questa casella di controllo. Ulteriori informazioni su [elenchi di abbonamenti](subscription-list.md).

      ![](../assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Channel (email)]**: L&#39;opt-in o l&#39;opt-out si applica all&#39;intero canale. Ad esempio, se un profilo che effettua la rinuncia ha due indirizzi e-mail, entrambi gli indirizzi saranno esclusi da tutte le tue comunicazioni.

   * **[!UICONTROL Email identity]**: L’opzione di consenso o rinuncia si applica solo all’indirizzo e-mail utilizzato per accedere alla pagina di destinazione. Ad esempio, se un profilo ha due indirizzi e-mail, solo quello utilizzato per il consenso riceverà le comunicazioni dal tuo marchio.

1. Fai clic su **[!UICONTROL Add field]** > **[!UICONTROL Checkbox]** per aggiungere un’altra casella di controllo. Ripeti i passaggi precedenti per definirne le proprietà.

   ![](../assets/lp_designer-form-checkbox-2.png)

1. Dopo aver aggiunto tutte le caselle di controllo desiderate, fai clic su **[!UICONTROL Call to action]** per espandere la sezione corrispondente. Ti consente di definire il comportamento del pulsante nel **[!UICONTROL Form]** componente.

   ![](../assets/lp_designer-form-call-to-action.png)

1. Definisci cosa accade quando fai clic sul pulsante :

   * **[!UICONTROL Redirect URL]**: Inserisci l’URL della pagina a cui verranno reindirizzati gli utenti.
   * **[!UICONTROL Confirmation text]**: Digita il testo di conferma che verrà visualizzato.
   * **[!UICONTROL Link to a subpage]**: Configura un [sottopagine](create-lp.md#configure-subpages) e selezionalo dall’elenco a discesa visualizzato.

   ![](../assets/lp_designer-form-confirmation-action.png)

1. Definisci cosa accade quando fai clic sul pulsante in caso di errore:

   * **[!UICONTROL Redirect URL]**: Inserisci l’URL della pagina a cui verranno reindirizzati gli utenti.
   * **[!UICONTROL Error text]**: Digitare il testo di errore che verrà visualizzato. Puoi visualizzare in anteprima il testo dell’errore durante la definizione della [stili di modulo](#define-lp-styles).

   * **[!UICONTROL Link to a subpage]**: Configura un [sottopagine](create-lp.md#configure-subpages) e selezionalo dall’elenco a discesa visualizzato.

   ![](../assets/lp_designer-form-error.png)

1. Se si desidera eseguire aggiornamenti aggiuntivi al momento dell’invio del modulo, selezionare **[!UICONTROL Opt in]** o **[!UICONTROL Opt out]** e definisci se desideri aggiornare un elenco di abbonamenti, il canale o solo l’indirizzo e-mail utilizzato.

   ![](../assets/lp_designer-form-additionnal-update.png)

1. Salva il contenuto e fai clic sulla freccia accanto al nome della pagina per tornare alla pagina [proprietà della pagina di destinazione](create-lp.md#configure-primary-page).

   ![](../assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## Definire gli stili del modulo della pagina di destinazione {#define-lp-styles}

1. Per modificare gli stili del contenuto del componente modulo, passare in qualsiasi momento al **[!UICONTROL Form style]** scheda .

   ![](../assets/lp_designer-form-style.png)

1. Espandi la **[!UICONTROL Checkboxes]** per definire l’aspetto delle caselle di controllo e del testo corrispondente. Ad esempio, è possibile modificare la famiglia o la dimensione del font e il colore del bordo della casella di controllo.

   ![](../assets/lp_designer-form-style-checkboxes.png)

1. Espandi la **[!UICONTROL Buttons]** per modificare l’aspetto del pulsante nel modulo del componente. Ad esempio, è possibile aggiungere un bordo, modificare il colore dell’etichetta al passaggio del mouse o regolare l’allineamento del pulsante.

   ![](../assets/lp_designer-form-style-buttons.png)

   Puoi visualizzare in anteprima alcune delle impostazioni, ad esempio il colore dell’etichetta del pulsante al passaggio del mouse utilizzando **[!UICONTROL Preview]** pulsante . Ulteriori informazioni sul test delle pagine di destinazione [qui](create-lp.md#test-landing-page).

   ![](../assets/lp_designer-form-style-buttons-preview.png)

1. Espandi la **[!UICONTROL Form layout]** per modificare le impostazioni di layout, ad esempio il colore di sfondo, la spaziatura o il margine.

   ![](../assets/lp_designer-form-style-layout.png)

1. Espandi la **[!UICONTROL Form error]** per regolare la visualizzazione del messaggio di errore visualizzato in caso di problemi. Selezionare l’opzione corrispondente per visualizzare in anteprima il testo di errore sul modulo.

   ![](../assets/lp_designer-form-error-preview.png)

