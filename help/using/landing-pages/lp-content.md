---
solution: Journey Optimizer
product: journey optimizer
title: Definire il contenuto specifico della pagina di destinazione
description: Scopri come progettare contenuti specifici per le pagine di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: destinazione, pagina di destinazione, creazione, pagina, modulo, componente
exl-id: 5bf023b4-4218-4110-b171-3e70e0507fca
source-git-commit: a5dd21377a26debb0aa3174fafb29c0532562c63
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 9%

---

# Definire il contenuto specifico della pagina di destinazione {#lp-content}

>[!CONTEXTUALHELP]
>id="ac_lp_components"
>title="Utilizzare i componenti di contenuto"
>abstract="I componenti dei contenuti sono dei segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di una pagina di destinazione. Per definire contenuti specifici che consentano agli utenti di selezionare e inviare le proprie scelte, utilizza il componente modulo."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Aggiungere componenti per contenuti"

Per progettare il contenuto di una pagina di destinazione, puoi utilizzare gli stessi componenti utilizzati per un’e-mail. [Ulteriori informazioni](../email/content-components.md#add-content-components)

Per progettare contenuto specifico che consenta agli utenti di selezionare e inviare le scelte, [utilizza il componente modulo](#use-form-component) e definisci i relativi [stili specifici per le pagine di destinazione](#lp-form-styles).

>[!NOTE]
>
>Puoi anche creare una pagina di destinazione click-through senza un componente **[!UICONTROL Modulo]**. In tal caso, gli utenti visualizzeranno la pagina di destinazione, ma non dovranno inviare alcun modulo. Questa funzione può essere utile se desideri visualizzare una pagina di destinazione solo senza richiedere alcuna azione da parte dei destinatari, ad esempio consenso o rinuncia, oppure se desideri fornire informazioni che non richiedono l’input dell’utente.

Utilizzando la finestra di progettazione del contenuto della pagina di destinazione, puoi anche sfruttare i dati contestuali provenienti dalla pagina principale di una pagina secondaria. [Ulteriori informazioni](#use-primary-page-context)

>[!NOTE]
>
>Il [European Accessibility Act](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"} stabilisce che tutte le comunicazioni digitali devono essere accessibili. Durante la progettazione del contenuto in [, assicurati di seguire le linee guida specifiche elencate in ](../email/accessible-content.md)questa pagina[!DNL Journey Optimizer].

## Utilizzare il componente modulo {#use-form-component}

>[!CONTEXTUALHELP]
>id="ac_lp_formfield"
>title="Impostare i campi del componente modulo"
>abstract="Definisci in che modo i destinatari visualizzeranno e invieranno le loro scelte dalla pagina di destinazione."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/landing-pages/landing-pages-design/lp-content#lp-form-styles" text="Definire gli stili del modulo della pagina di destinazione"

>[!CONTEXTUALHELP]
>id="ac_lp_submission"
>title="Eventi successivi al clic sul pulsante"
>abstract="Definisci gli eventi che si verificheranno dopo l’invio del modulo della pagina di destinazione."

Per definire contenuti specifici che consentano agli utenti di selezionare e inviare le scelte effettuate dalla pagina di destinazione, utilizza il componente **[!UICONTROL Modulo]**. A questo scopo, segui i passaggi riportati qui sotto.

1. Trascina il componente **[!UICONTROL Modulo]** specifico per la pagina di destinazione dalla palette a sinistra all&#39;area di lavoro principale.

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >Il componente **[!UICONTROL Modulo]** può essere utilizzato una sola volta sulla stessa pagina.

1. Selezionala. La scheda **[!UICONTROL Contenuto modulo]** viene visualizzata nella tavolozza di destra per consentire la modifica dei diversi campi del modulo.

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Passa alla scheda **[!UICONTROL Stili]** in qualsiasi momento per modificare gli stili del contenuto del componente modulo. [Ulteriori informazioni](#define-lp-styles)

1. Dalla sezione **[!UICONTROL Casella di controllo 1]** è possibile modificare l&#39;etichetta corrispondente a questa casella di controllo.

1. Definisci se questa casella di controllo deve consentire o meno agli utenti di ricevere comunicazioni: accettano di ricevere comunicazioni o chiedono di non essere più contattati?

   ![](assets/lp_designer-form-update.png)

   Seleziona una delle tre opzioni seguenti:

   * **[!UICONTROL Consenso se selezionato]**: gli utenti devono selezionare la casella per il consenso (consenso).
   * **[!UICONTROL Rinuncia se selezionata]**: gli utenti devono selezionare la casella per rimuovere il consenso (rinuncia).
   * **[!UICONTROL Consenso se selezionata, rinuncia se deselezionata]**: questa opzione consente di inserire una singola casella di controllo per il consenso/la rinuncia. Gli utenti devono selezionare la casella per il consenso (opt-in) e deselezionarla per la rimozione del consenso (opt-out).

1. Scegli cosa verrà aggiornato tra le tre opzioni seguenti:

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Elenco iscrizioni]**: è necessario selezionare l&#39;elenco di iscrizioni che verrà aggiornato se il profilo seleziona questa casella di controllo. Ulteriori informazioni sugli [elenchi di abbonamenti](subscription-list.md).

     <!--![](assets/lp_designer-form-subs-list.png)-->

   * **[!UICONTROL Canale (e-mail)]**: il consenso o la rinuncia si applica all&#39;intero canale. Ad esempio, se un profilo che rinuncia ha due indirizzi e-mail, entrambi gli indirizzi saranno esclusi da tutte le tue comunicazioni.

   * **[!UICONTROL Identità e-mail]**: il consenso o la rinuncia si applica solo all&#39;indirizzo e-mail utilizzato per accedere alla pagina di destinazione. Ad esempio, se un profilo ha due indirizzi e-mail, solo quello utilizzato per il consenso riceverà le comunicazioni dal tuo marchio.

1. Fai clic su **[!UICONTROL Aggiungi campo]** > **[!UICONTROL Casella di controllo]** per aggiungere un&#39;altra casella di controllo. Ripeti i passaggi precedenti per definirne le proprietà.

   ![](assets/lp_designer-form-checkbox-2.png)

1. Puoi anche aggiungere un **[!UICONTROL Campo di testo]**.

   ![](assets/lp_designer-form-add-text-field.png)

   * Immetti l&#39;**[!UICONTROL Etichetta]** che verrà visualizzata sopra il campo nel modulo.

   * Immetti un testo **[!UICONTROL Segnaposto]**. Viene visualizzato all’interno del campo prima che l’utente lo riempia.

   * Se necessario, seleziona l&#39;opzione **[!UICONTROL Rendi obbligatorio il campo modulo]**. In tal caso, la pagina di destinazione può essere inviata solo se l’utente ha compilato questo campo. Se non viene compilato un campo obbligatorio, quando l’utente invia la pagina viene visualizzato un messaggio di errore.

   ![](assets/lp_designer-form-text-field.png)

1. Dopo aver aggiunto tutte le caselle di controllo e/o i campi di testo desiderati, fare clic su **[!UICONTROL Call to action]** per espandere la sezione corrispondente. Consente di definire il comportamento del pulsante nel componente **[!UICONTROL Modulo]**.

   ![](assets/lp_designer-form-call-to-action.png)

1. Definisci cosa accade quando fai clic sul pulsante:

   * **[!UICONTROL URL di reindirizzamento]**: immettere l&#39;URL della pagina a cui verranno reindirizzati gli utenti.
   * **[!UICONTROL Testo di conferma]**: digitare il testo di conferma che verrà visualizzato.
   * **[!UICONTROL Collega a una pagina secondaria]**: configura una [pagina secondaria](create-lp.md#configure-subpages) e selezionala dall&#39;elenco a discesa visualizzato.

   ![](assets/lp_designer-form-confirmation-action.png)

1. Definisci cosa accade quando fai clic sul pulsante in caso di errore:

   * **[!UICONTROL URL di reindirizzamento]**: immettere l&#39;URL della pagina a cui verranno reindirizzati gli utenti.
   * **[!UICONTROL Testo errore]**: digitare il testo dell&#39;errore che verrà visualizzato. È possibile visualizzare in anteprima il testo dell&#39;errore durante la definizione degli [stili modulo](#define-lp-styles).

   * **[!UICONTROL Collega a una pagina secondaria]**: configura una [pagina secondaria](create-lp.md#configure-subpages) e selezionala dall&#39;elenco a discesa visualizzato.

   ![](assets/lp_designer-form-error.png)

1. Se desideri apportare ulteriori aggiornamenti al momento dell&#39;invio del modulo, seleziona **[!UICONTROL Consenso]** o **[!UICONTROL Rinuncia]** e definisci se desideri aggiornare un elenco di iscrizioni, il canale o solo l&#39;indirizzo e-mail utilizzato.

   ![](assets/lp_designer-form-additionnal-update.png)

1. Salva il contenuto e fai clic sulla freccia accanto al nome della pagina per tornare alle [proprietà della pagina di destinazione](create-lp.md#configure-primary-page).

   ![](assets/lp_designer-form-save.png)

## Definire gli stili del modulo della pagina di destinazione {#lp-form-styles}

1. Per modificare gli stili del contenuto del componente modulo, passa in qualsiasi momento alla scheda **[!UICONTROL Stile]**.

   ![](assets/lp_designer-form-style.png)

1. La sezione **[!UICONTROL Campi]** è espansa per impostazione predefinita e consente di modificare l&#39;aspetto del campo di testo, ad esempio il tipo di carattere dell&#39;etichetta e del segnaposto, la posizione dell&#39;etichetta, il colore di sfondo del campo o il bordo del campo.

   ![](assets/lp_designer-form-style-fields.png)

1. Espandere la sezione **[!UICONTROL Caselle di controllo]** per definire l&#39;aspetto delle caselle di controllo e del testo corrispondente. Ad esempio, è possibile regolare la famiglia o la dimensione del carattere o il colore del bordo della casella di controllo.

   ![](assets/lp_designer-form-style-checkboxes.png)

1. Espandere la sezione **[!UICONTROL Pulsanti]** per modificare l&#39;aspetto del pulsante nel modulo del componente. È ad esempio possibile modificare il tipo di carattere, aggiungere un bordo, modificare il colore dell&#39;etichetta al passaggio del mouse o regolare l&#39;allineamento del pulsante.

   ![](assets/lp_designer-form-style-buttons.png)

   Puoi visualizzare in anteprima alcune impostazioni, ad esempio il colore dell&#39;etichetta del pulsante al passaggio del mouse, utilizzando il pulsante **[!UICONTROL Simula contenuto]**. Ulteriori informazioni sulla verifica delle pagine di destinazione [qui](create-lp.md#test-landing-page).

   <!--![](assets/lp_designer-form-style-buttons-preview.png)-->

1. Espandere la sezione **[!UICONTROL Layout modulo]** per modificare le impostazioni di layout, ad esempio il colore di sfondo, la spaziatura interna o il margine.

   ![](assets/lp_designer-form-style-layout.png)

1. Espandere la sezione **[!UICONTROL Errore modulo]** per modificare la visualizzazione del messaggio di errore visualizzato in caso di problemi. Seleziona l’opzione corrispondente per visualizzare in anteprima il testo dell’errore nel modulo.

   ![](assets/lp_designer-form-error-preview.png)

## Usa contesto pagina principale {#use-primary-page-context}

Puoi utilizzare dati contestuali provenienti da un’altra pagina all’interno della stessa pagina di destinazione.

Ad esempio, se colleghi una casella di controllo <!-- or the submission of the page--> a un [elenco iscrizioni](subscription-list.md) nella pagina di destinazione principale, puoi utilizzare tale elenco iscrizioni nella pagina secondaria di ringraziamento.

Supponiamo che tu colleghi due caselle di controllo nella pagina principale a due diversi elenchi di abbonamento. Se un utente si abbona a uno di questi, desideri visualizzare un messaggio specifico al momento dell’invio del modulo, a seconda della casella di controllo selezionata.

A questo scopo, segui i passaggi riportati qui sotto:

1. Nella pagina principale, collega ogni casella di controllo del componente **[!UICONTROL Modulo]** all&#39;elenco di iscrizioni pertinente. [Ulteriori informazioni](#use-form-component).

   ![](assets/lp_designer-form-luma-newsletter.png)

1. Nella pagina secondaria posizionare il puntatore del mouse nel punto in cui si desidera inserire il testo e selezionare **[!UICONTROL Aggiungi personalizzazione]** dalla barra degli strumenti contestuale.

   ![](assets/lp_designer-form-subpage-perso.png)

1. Nella finestra **[!UICONTROL Modifica personalizzazione]**, seleziona **[!UICONTROL Attributi contestuali]** > **[!UICONTROL Pagine di destinazione]** > **[!UICONTROL Contesto pagina principale]** > **[!UICONTROL Sottoscrizione]**.

1. Vengono elencati tutti gli elenchi di iscrizioni selezionati nella pagina principale. Seleziona gli elementi rilevanti utilizzando l’icona +.

   ![](assets/lp_designer-form-add-subscription.png)

1. Aggiungi le condizioni rilevanti utilizzando le funzioni di assistenza dell’editor di personalizzazione. [Ulteriori informazioni](../personalization/functions/functions.md)

   ![](assets/lp_designer-form-add-subscription-condition.png)

   >[!CAUTION]
   >
   >Se nell’espressione è presente un carattere speciale, ad esempio un trattino, è necessario applicare l’escape al testo, incluso il trattino.

1. Salva le modifiche.

Ora, quando gli utenti selezionano una delle caselle di controllo,

![](assets/lp_designer-form-preview-checked-box.png)

all’invio del modulo viene visualizzato il messaggio corrispondente alla casella di controllo selezionata.

![](assets/lp_designer-form-thankyou-preview.png)

<!--![](assets/lp_designer-form-subscription-preview.png)-->

>[!NOTE]
>
>Se un utente seleziona le due caselle di controllo, verranno visualizzati entrambi i testi.

<!--
## Use landing page additional data {#use-additional-data}

When [configuring the primary page](create-lp.md#configure-primary-page), you can create additional data to enable storing information when the landing page is being submitted.

>[!NOTE]
>
>This data may not be visible to users who visit the page.

If you defined one or more keys with their corresponding values when [configuring the primary page](create-lp.md#configure-primary-page), you can leverage these keys in the content of your primary page and subpages using the [personalization editor](../personalization/personalization-build-expressions.md).

///When you reuse the same text on a page, this enables you to dynamically change that text if needed, without going through each occurrence.

For example, if you define the company name as a key, you can quickly update it everywhere (on all the pages of a given landing page) by changing it only once in the [primary page settings](create-lp.md#configure-primary-page).///

To leverage these keys in a landing page, follow the steps below:

1. When configuring the primary page, define a key and its corresponding value in the **[!UICONTROL Additional data]** section. [Learn more](create-lp.md#configure-primary-page)

    ![](assets/lp_create-lp-additional-data.png)

1. When editing your primary page with the designer, place the pointer of your mouse where you want to insert your key and select **[!UICONTROL Add personalization]** from the contextual toolbar.

    ![](assets/lp_designer-context-add-perso.png)

1. In the **[!UICONTROL Edit Personalization]** window, select **[!UICONTROL Contextual attributes]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Additional Context]**.

    ![](assets/lp_designer-contextual-attributes.png)

1. All the keys that you created when configuring the primary page are listed. Select the key of your choice using the + icon.

    ![](assets/lp_designer-context-select-key.png)

1. Save your changes and repeat the steps above as many times as needed.

    ![](assets/lp_designer-context-keys-inserted.png)

    You can see that the personalization item corresponding to your key is now displayed everywhere you inserted it.
-->