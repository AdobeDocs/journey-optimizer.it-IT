---
solution: Journey Optimizer
product: journey optimizer
title: Creare una pagina di destinazione
description: Scopri come configurare e pubblicare una pagina di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: landing, pagina di destinazione, creazione, pubblicazione
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 28%

---

# Creare e pubblicare pagine di destinazione {#create-lp}

## Accedere alle pagine di destinazione {#access-landing-pages}

Per accedere all’elenco delle pagine di destinazione, seleziona **[!UICONTROL Gestione dei percorsi]** > **[!UICONTROL Pagine di destinazione]** dal menu a sinistra.

![](assets/lp_access-list.png)

La **[!UICONTROL Pagine di destinazione]** visualizza tutti gli elementi creati. Puoi filtrarli in base al loro stato o alla data di modifica.

![](assets/lp_access-list-filter.png)

Da questo elenco è possibile accedere al [report live della pagina di destinazione](../reports/lp-report-live.md) o [report globale della pagina di destinazione](../reports/lp-report-global.md) per gli elementi pubblicati.

Puoi anche eliminare, duplicare e annullare la pubblicazione di una pagina di destinazione.

>[!CAUTION]
>
>Se annulli la pubblicazione di una pagina di destinazione a cui viene fatto riferimento in un messaggio, il collegamento alla pagina di destinazione non funziona e viene visualizzata una pagina di errore.

Fai clic sui tre punti accanto a una pagina di destinazione per selezionare l’azione desiderata.

![](assets/lp_access-list-actions.png)

>[!NOTE]
>
>Non è possibile eliminare un [pubblicato](#publish-landing-page) pagina di destinazione. Per eliminarlo, devi prima annullarne la pubblicazione.

## Creare una pagina di destinazione {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_create"
>title="Definire e configurare la pagina di destinazione"
>abstract="Per creare una pagina di destinazione, devi selezionare un predefinito; configurare la pagina principale e le pagine secondarie; e infine verificare la pagina prima di pubblicarla."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=it#lp-create-preset" text="Creare i predefiniti per pagine di destinazione"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/create-lp.html?lang=it#publish-landing-page" text="Pubblicare la pagina di destinazione"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_management_labels"
>title="Assegnare etichette alla pagina di destinazione"
>abstract="Per proteggere le risorse digitali sensibili, puoi definire autorizzazioni con cui gestire l’accesso ai dati per a pagina di destinazione utilizzando specifiche etichette."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/access-control/object-based-access.html?lang=it" text="Controllo dell’accesso a livello di oggetto"

I passaggi principali per creare pagine di destinazione sono i seguenti:

![](assets/lp-creation-process.png)

1. Dall’elenco della pagina di destinazione, fai clic su **[!UICONTROL Creare una pagina di destinazione]**.

   ![](assets/lp_create-lp.png)

1. Aggiungi un titolo. Se necessario, puoi aggiungere una descrizione.

   ![](assets/lp_create-lp-details.png)

1. Per assegnare etichette di utilizzo dati personalizzate o di base alla pagina di destinazione, seleziona **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni su Object Level Access Control (OLAC)](../administration/object-based-access.md)

   <!--You can add a tag. See AEP documentation?-->

1. Seleziona un predefinito. Scopri come creare i predefiniti per le pagine di destinazione in [questa sezione](../landing-pages/lp-presets.md#lp-create-preset).

   ![](assets/lp_create-lp-presets.png)

1. Fai clic su **[!UICONTROL Crea]**.

1. Viene visualizzata la pagina principale e le relative proprietà. Scopri come configurare le impostazioni della pagina principale [qui](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. Fai clic sull’icona + per aggiungere una pagina secondaria. Scopri come configurare le impostazioni della pagina secondaria [qui](#configure-subpages).

   ![](assets/lp_add-subpage.png)

Una volta configurati e progettati i [pagina principale](#configure-primary-page)e [sottopagine](#configure-subpages) se presente, puoi [test](#test-landing-page) e [pubblicare](#publish-landing-page) la pagina di destinazione.

## Configurare la pagina principale {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_primary_page"
>title="Definire le impostazioni della pagina principale"
>abstract="La pagina principale viene visualizzata immediatamente dagli utenti dopo aver fatto clic sul collegamento alla pagina di destinazione, ad esempio da un’e-mail o da un sito web."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html?lang=it" text="Progettare il contenuto della pagina di destinazione"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings"
>title="Definire l’URL della pagina di destinazione"
>abstract="In questa sezione, definisci un URL univoco per la pagina di destinazione. Per la prima parte dell’URL, devi aver già impostato un sottodominio della pagina di destinazione come parte del predefinito selezionato."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html?lang=it" text="Configurare i sottodomini della pagina di destinazione"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=it#lp-create-preset" text="Creare i predefiniti per pagine di destinazione"

La pagina principale è quella immediatamente visualizzata dagli utenti dopo aver fatto clic sul collegamento alla pagina di destinazione, ad esempio da un’e-mail o da un sito web.

Per definire le impostazioni della pagina principale, segui la procedura seguente.

1. È possibile modificare il nome della pagina, ovvero **[!UICONTROL Pagina principale]** per impostazione predefinita.

1. Modifica il contenuto della pagina utilizzando la finestra di progettazione dei contenuti. Scopri come definire il contenuto della pagina di destinazione [qui](design-lp.md).

   ![](assets/lp_open-designer.png)

1. Definire l’URL della pagina di destinazione. La prima parte dell’URL richiede la configurazione di un sottodominio della pagina di destinazione come parte del [predefinito](../landing-pages/lp-presets.md#lp-create-preset) selezionato. [Ulteriori informazioni](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >L’URL della pagina di destinazione deve essere univoco.

   ![](assets/lp_access-url.png)

   >[!NOTE]
   >
   >Non puoi accedere alla pagina di destinazione semplicemente copiando e incollando questo URL in un browser web, anche se pubblicato. Puoi invece testarlo utilizzando la funzione di anteprima come descritto in [questa sezione](#test-landing-page).

1. Se si desidera che la pagina di destinazione precarichi i dati del modulo già disponibili, selezionare la **[!UICONTROL Precompilare i campi del modulo con le informazioni sul profilo]**.

   ![](assets/lp_prefill-form-fields.png)

   Quando questa opzione è abilitata, se un profilo ha già rinunciato o è già stato aggiunto a un elenco di sottoscrizioni, le relative scelte verranno applicate alla visualizzazione della pagina di destinazione.

   Ad esempio, se un profilo ha acconsentito alla ricezione di comunicazioni su eventi futuri, la casella di controllo corrispondente verrà già selezionata al successivo accesso alla pagina di destinazione a tale profilo.

   ![](assets/lp_prefill-form-ex.png)

1. Puoi definire una data di scadenza per la pagina. In tal caso, è necessario selezionare un’azione alla scadenza della pagina:

   * **[!UICONTROL URL di reindirizzamento]**: Inserisci l’URL della pagina a cui verranno reindirizzati gli utenti alla scadenza della pagina.
   * **[!UICONTROL Pagina personalizzata]**: [Configurare una pagina secondaria](#configure-subpages) e selezionalo dall’elenco a discesa visualizzato.
   * **[!UICONTROL Errore del browser]**: Digita il testo di errore che verrà visualizzato al posto della pagina.

   ![](assets/lp_expiry-date.png)

1. In **[!UICONTROL Dati aggiuntivi]** , definisci una o più chiavi e i relativi valori di parametro. Potrai sfruttare queste chiavi nel contenuto della pagina principale e nelle pagine secondarie utilizzando [Editor espressioni](../personalization/personalization-build-expressions.md). Ulteriori informazioni in [questa sezione](lp-content.md#use-form-component#use-additional-data).

   ![](assets/lp_create-lp-additional-data.png)

1. Se hai selezionato uno o più elenchi di sottoscrizioni quando [progettazione della pagina principale](design-lp.md), vengono visualizzati nella **[!UICONTROL Lista di sottoscrizione]** sezione .

   ![](assets/lp_subscription-list.png)

1. Dalla pagina di destinazione, puoi [creare un percorso](../building-journeys/journey-gs.md#jo-build) che invierà un messaggio di conferma agli utenti al momento dell’invio del modulo. Scopri come creare un tale percorso alla fine di questo [caso d&#39;uso](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   Fai clic su **[!UICONTROL Crea percorso]** da reindirizzare al **[!UICONTROL Gestione dei percorsi]** > **[!UICONTROL Percorsi]** elenco.

## Configurare le pagine secondarie {#configure-subpages}

>[!CONTEXTUALHELP]
>id="ajo_lp_subpage"
>title="Definire le impostazioni delle pagine secondarie"
>abstract="Puoi aggiungere fino a 2 pagine secondarie. Ad esempio, puoi creare una pagina di ringraziamento da visualizzare dopo l’invio di un modulo, e definire una pagina di errore da richiamare in caso di problemi relativi alla pagina di destinazione."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html?lang=it" text="Progettare il contenuto della pagina di destinazione"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings-subpage"
>title="Definire l’URL della pagina di destinazione"
>abstract="In questa sezione, definisci un URL univoco per la pagina di destinazione. Per la prima parte dell’URL, devi aver già impostato un sottodominio della pagina di destinazione come parte del predefinito selezionato."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html?lang=it" text="Configurare i sottodomini della pagina di destinazione"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=it#lp-create-preset" text="Creare i predefiniti per pagine di destinazione"

Puoi aggiungere fino a 2 pagine secondarie. Ad esempio, puoi creare una pagina di ringraziamento da visualizzare dopo l’invio di un modulo, e definire una pagina di errore da richiamare in caso di problemi relativi alla pagina di destinazione.

Per definire le impostazioni della pagina secondaria, segui la procedura seguente.

1. È possibile modificare il nome della pagina, ovvero **[!UICONTROL Pagina secondaria 1]** per impostazione predefinita.

1. Modifica il contenuto della pagina utilizzando la finestra di progettazione dei contenuti. Scopri come definire il contenuto della pagina di destinazione [qui](design-lp.md).

   >[!NOTE]
   >
   >Puoi inserire un collegamento alla pagina principale da qualsiasi pagina secondaria della stessa pagina di destinazione. Ad esempio, per reindirizzare gli utenti che hanno commesso un errore e desiderano effettuare di nuovo l’abbonamento, puoi aggiungere un collegamento dalla pagina secondaria di conferma alla pagina principale dell’abbonamento. Scopri come inserire collegamenti in [questa sezione](../email/message-tracking.md#insert-links).

1. Definire l’URL della pagina di destinazione. La prima parte dell’URL richiede la configurazione di un sottodominio della pagina di destinazione. [Ulteriori informazioni](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >L’URL della pagina di destinazione deve essere univoco.

![](assets/lp_subpage-settings.png)

## Verificare la pagina di destinazione {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ac_preview_lp_profiles"
>title="Visualizzare l’anteprima e testare la pagina di destinazione"
>abstract="Una volta definite le impostazioni e il contenuto della pagina di destinazione, puoi utilizzare i profili di test per visualizzarli in anteprima."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/segment/profiles/creating-test-profiles.html?lang=it" text="Selezionare i profili di test"

Una volta definite le impostazioni e il contenuto della pagina di destinazione, puoi utilizzare i profili di test per visualizzarli in anteprima. Se hai inserito [contenuti personalizzati](../personalization/personalize.md), potrai controllare la modalità di visualizzazione del contenuto nella pagina di destinazione utilizzando i dati del profilo di test.

>[!CAUTION]
>
>Per visualizzare l’anteprima dei messaggi e inviare le bozze, devi disporre dei profili di test. Scopri come [creare profili di test](../segment/creating-test-profiles.md).

1. Nell’interfaccia della pagina di destinazione, fai clic sul pulsante **[!UICONTROL Simulazione del contenuto]** per accedere alla selezione del profilo di test.

   ![](assets/lp_simulate-button.png)

   >[!NOTE]
   >
   >La **[!UICONTROL Simulazione del contenuto]** accessibile anche dal designer del contenuto.

1. Da **[!UICONTROL Simula]** seleziona uno o più profili di test.

   ![](assets/lp_test-profiles.png)

   I passaggi per selezionare i profili di test sono gli stessi che per testare un messaggio. Essi sono descritti in [questa sezione](../email/preview.md#select-test-profiles).

1. Seleziona la **[!UICONTROL Anteprima]** e fai clic su **[!UICONTROL Apri anteprima]** per verificare la pagina di destinazione.

   ![](assets/lp_open-preview.png)

1. L’anteprima della pagina di destinazione viene visualizzata in una nuova scheda. Gli elementi personalizzati vengono sostituiti dai dati del profilo di test selezionati.

   ![](assets/lp_preview.png)

1. Seleziona altri profili di test per visualizzare in anteprima il rendering per ogni variante della pagina di destinazione.

## Controllare gli avvisi {#check-alerts}

Durante la creazione della pagina di destinazione, gli avvisi ti avvisano quando devi eseguire azioni importanti prima di pubblicare.

Gli avvisi vengono visualizzati in alto a destra dello schermo, come illustrato di seguito:

![](assets/lp_alerts.png)

>[!NOTE]
>
>In caso contrario, non è stato rilevato alcun avviso.

Possono verificarsi due tipi di avvisi:

* **Avvisi** consulta consigli e best practice. <!--For example, a message will display if -->

* **Errori** impedisce la pubblicazione della pagina di destinazione purché non siano state risolte. Ad esempio, se manca l’URL della pagina principale riceverai un avviso.

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> Risolvere tutti i problemi **errore** avvisi prima della pubblicazione.

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you must resolve all **error** alerts.
-->

## Pubblicare la pagina di destinazione {#publish-landing-page}

Quando la pagina di destinazione è pronta, puoi pubblicarla per renderla disponibile per l’utilizzo in un messaggio.

![](assets/lp_publish.png)

>[!CAUTION]
>
>Prima della pubblicazione, controlla e risolvi gli avvisi. [Ulteriori informazioni](#check-alerts)

Una volta pubblicata, la pagina di destinazione viene aggiunta all’elenco della pagina di destinazione con la **[!UICONTROL Pubblicato]** stato.

È ora attivo e pronto per essere utilizzato in un [!DNL Journey Optimizer] messaggio che verrà inviato tramite un [percorso](../building-journeys/journey.md).

>[!NOTE]
>
>Puoi monitorare l’impatto della pagina di destinazione tramite report specifici. [Ulteriori informazioni](../reports/lp-report-live.md)

