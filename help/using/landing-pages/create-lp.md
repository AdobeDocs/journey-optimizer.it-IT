---
solution: Journey Optimizer
product: journey optimizer
title: Creare una pagina di destinazione
description: Scopri come configurare e pubblicare una pagina di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: destinazione, pagina di destinazione, creazione, pubblicazione
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 0db7f514a2604ad09fbd9863a51d3c86d69eac41
workflow-type: tm+mt
source-wordcount: '1518'
ht-degree: 23%

---

# Creare e pubblicare pagine di destinazione {#create-lp}

Per indirizzare i clienti a una pagina Web definita che si desidera visualizzare quando fanno clic su un collegamento specifico, creare una pagina di destinazione in [!DNL Journey Optimizer], configurare la pagina principale e le eventuali pagine secondarie, testarla e pubblicarla.

I passaggi principali per creare pagine di destinazione sono i seguenti:

![](assets/lp-creation-process.png)

## Creare una pagina di destinazione {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_create"
>title="Definire e configurare la pagina di destinazione"
>abstract="Per creare una pagina di destinazione, devi selezionare un predefinito; configurare la pagina principale e le pagine secondarie; e infine verificare la pagina prima di pubblicarla."

>[!CONTEXTUALHELP]
>id="ajo_lp_access_management_labels"
>title="Assegnare etichette alla pagina di destinazione"
>abstract="Per proteggere le risorse digitali sensibili, puoi definire autorizzazioni con cui gestire l’accesso ai dati per a pagina di destinazione utilizzando specifiche etichette."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/access-control/object-based-access.html?lang=it" text="Controllo dell’accesso a livello di oggetto"


Per creare una pagina di destinazione, devi selezionare un predefinito, configurare la pagina principale e le pagine secondarie e infine testare la pagina prima di pubblicarla. Di seguito sono descritti i passaggi da eseguire:


1. Passa a **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Pagine di destinazione]** dal menu a sinistra.

1. Nell&#39;elenco delle pagine di destinazione fare clic su **[!UICONTROL Crea pagina di destinazione]**.

   ![](assets/lp_create-lp.png)

1. Aggiungi un titolo. Se necessario, puoi aggiungere una descrizione.

   ![](assets/lp_create-lp-details.png)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla pagina di destinazione, selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto (OLAC)](../administration/object-based-access.md)

1. Seleziona o crea tag Adobe Experience Platform dal campo **[!UICONTROL Tag]** per categorizzare la pagina di destinazione ai fini di una ricerca migliorata. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Seleziona un predefinito. Scopri come creare predefiniti per pagine di destinazione in [questa sezione](../landing-pages/lp-presets.md#lp-create-preset).

   ![](assets/lp_create-lp-presets.png)

1. Fai clic su **[!UICONTROL Crea]**.

1. Viene visualizzata la pagina principale e le relative proprietà. Scopri come configurare le impostazioni della pagina principale [qui](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. Fai clic sull’icona + per aggiungere una pagina secondaria. Scopri come configurare le impostazioni della pagina secondaria [qui](#configure-subpages).

   ![](assets/lp_add-subpage.png)

Dopo aver configurato e progettato la [pagina principale](#configure-primary-page) e le [pagine secondarie](#configure-subpages), se presenti, puoi [testare](#test-landing-page) e [pubblicare](#publish-landing-page) la tua pagina di destinazione.

>[!CAUTION]
>
>Non puoi accedere alla pagina di destinazione semplicemente copiando e incollando l’URL definito in un browser web, anche se pubblicato. È invece possibile testarlo utilizzando la funzione di anteprima descritta in [questa sezione](#test-landing-page).

## Configurare la pagina principale {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_primary_page"
>title="Definire le impostazioni della pagina principale"
>abstract="La pagina principale viene visualizzata immediatamente dagli utenti dopo aver fatto clic sul collegamento alla pagina di destinazione, ad esempio da un’e-mail o da un sito web."
<!--
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html?lang=it" text="Design the landing page content"-->

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings"
>title="Definire l’URL della pagina di destinazione"
>abstract="In questa sezione, definisci un URL univoco per la pagina di destinazione. Per la prima parte dell’URL, devi aver già impostato un sottodominio della pagina di destinazione come parte del predefinito selezionato."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-subdomains" text="Configurare i sottodomini della pagina di destinazione"
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets#lp-create-preset" text="Creare i predefiniti per la pagina di destinazione"

La pagina principale è quella che viene visualizzata immediatamente dagli utenti dopo che hanno fatto clic sul collegamento alla pagina di destinazione, ad esempio da un’e-mail o da un sito web.

Per definire le impostazioni della pagina principale, effettua le seguenti operazioni.

1. È possibile modificare il nome della pagina, che è **[!UICONTROL Pagina principale]** per impostazione predefinita.

1. Modifica il contenuto della pagina utilizzando il designer contenuto. Scopri come definire il contenuto della pagina di destinazione [qui](design-lp.md).

   ![](assets/lp_open-designer.png)

1. Definisci l’URL della pagina di destinazione. La prima parte dell&#39;URL richiede la configurazione di un sottodominio della pagina di destinazione come parte del [predefinito](../landing-pages/lp-presets.md#lp-create-preset) selezionato. [Ulteriori informazioni](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >L’URL della pagina di destinazione deve essere univoco.
   >
   >Non puoi accedere alla pagina di destinazione semplicemente copiando e incollando questo URL in un browser web, anche se pubblicato. È invece possibile testarlo utilizzando la funzione di anteprima descritta in [questa sezione](#test-landing-page).

   ![](assets/lp_access-url.png)

1. Se si desidera che la pagina di destinazione precarichi i dati del modulo già disponibili, selezionare i **[!UICONTROL campi modulo precompilati con le informazioni del profilo]**.

   ![](assets/lp_prefill-form-fields.png)

   Quando questa opzione è abilitata, se un profilo ha già acconsentito o è già stato aggiunto a un elenco di abbonamenti, le sue scelte si rifletteranno sulla visualizzazione della pagina di destinazione.

   Ad esempio, se un profilo ha acconsentito alla ricezione di comunicazioni su eventi futuri, la casella di controllo corrispondente sarà già selezionata la prossima volta che la pagina di destinazione viene visualizzata su tale profilo.

   ![](assets/lp_prefill-form-ex.png)

1. Puoi definire una data di scadenza per la pagina. In tal caso, seleziona un’azione alla scadenza della pagina:

   * **[!UICONTROL URL di reindirizzamento]**: immetti l&#39;URL della pagina a cui verranno reindirizzati gli utenti alla scadenza della pagina.
   * **[!UICONTROL Pagina personalizzata]**: [Configura una pagina secondaria](#configure-subpages) e selezionala dall&#39;elenco a discesa visualizzato.
   * **[!UICONTROL Errore del browser]**: digitare il testo dell&#39;errore che verrà visualizzato al posto della pagina.

   ![](assets/lp_expiry-date.png)

<!--1. In the **[!UICONTROL Additional data]** section, define one or more keys and their corresponding parameter values. You will be able to leverage these keys in the content of your primary page and subpages using the [personalization editor](../personalization/personalization-build-expressions.md). Learn more in [this section](lp-content.md#use-form-component#use-additional-data).

    ![](assets/lp_create-lp-additional-data.png)-->

1. Se hai selezionato uno o più elenchi di iscrizioni durante la [progettazione della pagina principale](design-lp.md), questi verranno visualizzati nella sezione **[!UICONTROL Elenco di iscrizioni]**.

   ![](assets/lp_subscription-list.png)

1. Dalla pagina di destinazione, puoi [creare direttamente un percorso](../building-journeys/journey-gs.md#jo-build) che invierà un messaggio di conferma agli utenti quando inviano il modulo. Scopri come creare tale percorso alla fine di questo [caso d&#39;uso](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   Fare clic su **[!UICONTROL Crea percorso]** per reindirizzarlo all&#39;elenco **[!UICONTROL Gestione Percorsi]** > **[!UICONTROL Percorsi]**.

## Configurare le pagine secondarie {#configure-subpages}

>[!CONTEXTUALHELP]
>id="ajo_lp_subpage"
>title="Definire le impostazioni delle pagine secondarie"
>abstract="Puoi aggiungere fino a 2 pagine secondarie. Ad esempio, puoi creare una pagina di ringraziamento da visualizzare dopo l’invio di un modulo, e definire una pagina di errore da richiamare in caso di problemi relativi alla pagina di destinazione."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/landing-pages/landing-pages-design/design-lp" text="Progettare il contenuto della pagina di destinazione"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings-subpage"
>title="Definire l’URL della pagina di destinazione"
>abstract="In questa sezione, definisci un URL univoco per la pagina di destinazione. Per la prima parte dell’URL, devi aver già impostato un sottodominio della pagina di destinazione come parte del predefinito selezionato."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-subdomains" text="Configurare i sottodomini della pagina di destinazione"
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets#lp-create-preset" text="Creare i predefiniti per la pagina di destinazione"

Puoi aggiungere fino a 2 pagine secondarie. Ad esempio, puoi creare una pagina di ringraziamento da visualizzare dopo l’invio di un modulo, e definire una pagina di errore da richiamare in caso di problemi relativi alla pagina di destinazione.

Per definire le impostazioni delle pagine secondarie, effettuare le seguenti operazioni.

1. È possibile modificare il nome della pagina, che è **[!UICONTROL Pagina secondaria 1]** per impostazione predefinita.

1. Modifica il contenuto della pagina utilizzando il designer contenuto. Scopri come definire il contenuto della pagina di destinazione [qui](design-lp.md).

   >[!NOTE]
   >
   >Puoi inserire un collegamento alla pagina principale da qualsiasi pagina secondaria della stessa pagina di destinazione. Ad esempio, per reindirizzare gli utenti che hanno commesso un errore e desiderano effettuare nuovamente l’abbonamento, puoi aggiungere un collegamento dalla pagina secondaria di conferma alla pagina principale dell’abbonamento. Scopri come inserire collegamenti in [questa sezione](../email/message-tracking.md#insert-links).

1. Definisci l’URL della pagina di destinazione. La prima parte dell’URL richiede la configurazione precedente di un sottodominio della pagina di destinazione. [Ulteriori informazioni](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >L’URL della pagina di destinazione deve essere univoco.
   >
   >Non puoi accedere alla pagina secondaria semplicemente copiando e incollando questo URL in un browser web, anche se pubblicato. È invece possibile testarlo utilizzando la funzione di anteprima descritta in [questa sezione](#test-landing-page).

![](assets/lp_subpage-settings.png)

## Verificare la pagina di destinazione {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ac_preview_lp_profiles"
>title="Visualizzare l’anteprima e testare la pagina di destinazione"
>abstract="Una volta definite le impostazioni e il contenuto della pagina di destinazione, puoi utilizzare i profili di test per visualizzarli in anteprima."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/profiles/creating-test-profiles.html?lang=it" text="Selezionare i profili di test"

Una volta definiti le impostazioni e il contenuto della pagina di destinazione, puoi utilizzare i profili di test per visualizzarne l’anteprima. Se hai inserito [contenuti personalizzati](../personalization/personalize.md), potrai controllare come questi contenuti vengono visualizzati nella pagina di destinazione utilizzando i dati del profilo di test.

>[!CAUTION]
>
>Per poter testare le pagine di destinazione, devi disporre dell&#39;autorizzazione **[!UICONTROL Pubblica messaggi]**.
>
>Per poter visualizzare in anteprima i messaggi e inviare le bozze, è necessario disporre di profili di test. Scopri come [creare profili di test](../audience/creating-test-profiles.md).

1. Nell&#39;interfaccia della pagina di destinazione, fare clic sul pulsante **[!UICONTROL Simula contenuto]** per accedere alla selezione del profilo di test.

   ![](assets/lp_simulate-button.png)

   >[!NOTE]
   >
   >Il pulsante **[!UICONTROL Simula contenuto]** è accessibile anche dal designer contenuto.

1. Dalla schermata **[!UICONTROL Simula]**, selezionare uno o più profili di test.

   ![](assets/lp_test-profiles.png)

   I passaggi per selezionare i profili di test sono gli stessi utilizzati per testare un messaggio. Sono descritte in dettaglio nella sezione [Gestione dei contenuti](../content-management/test-profiles.md).

1. Seleziona **[!UICONTROL Apri anteprima]** per verificare la pagina di destinazione.

   ![](assets/lp_open-preview.png)

1. L’anteprima della pagina di destinazione viene visualizzata in una nuova scheda. Gli elementi personalizzati vengono sostituiti dai dati del profilo di test selezionati.

   <!--![](assets/lp_preview.png)-->

1. Seleziona altri profili di test per visualizzare in anteprima il rendering per ogni variante della pagina di destinazione.

## Controllare gli avvisi {#check-alerts}

Durante la creazione della pagina di destinazione, gli avvisi ti avvisano quando devi eseguire azioni importanti prima di pubblicarla.

Gli avvisi vengono visualizzati in alto a destra dello schermo, come illustrato di seguito:

![](assets/lp_alerts.png)

>[!NOTE]
>
>Se questo pulsante non è visualizzato, non è stato rilevato alcun avviso.

Possono verificarsi due tipi di avvisi:

* **Avvisi** fai riferimento a consigli e best practice. <!--For example, a message will display if -->

* **Gli errori** impediscono la pubblicazione della pagina di destinazione se non vengono risolti. Ad esempio, se manca l’URL della pagina principale, verrà visualizzato un avviso.

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> È necessario risolvere tutti gli avvisi di **errore** prima della pubblicazione.

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

-->

## Pubblicare la pagina di destinazione {#publish-landing-page}

>[!CAUTION]
>
>Per pubblicare le pagine di destinazione, gli utenti devono disporre dell&#39;autorizzazione **[!UICONTROL Pubblica messaggi]**.


Una volta che la pagina di destinazione è pronta, puoi pubblicarla per renderla disponibile per l’utilizzo in un messaggio.

![](assets/lp_publish.png)

>[!CAUTION]
>
>Prima di pubblicare, controlla e risolvi gli avvisi. [Ulteriori informazioni](#check-alerts)

Dopo la pubblicazione, la pagina di destinazione viene aggiunta all&#39;elenco delle pagine di destinazione con lo stato **[!UICONTROL Pubblicato]**.

Ora è attivo e pronto per essere utilizzato in un messaggio [!DNL Journey Optimizer] che verrà inviato tramite un [percorso](../building-journeys/journey.md).

>[!NOTE]
>
>Non puoi accedere alla pagina di destinazione semplicemente copiando e incollando in un browser l&#39;URL definito durante la [creazione della pagina](#create-landing-page), anche se pubblicato. È invece possibile testarlo utilizzando la funzione di anteprima descritta in [questa sezione](#test-landing-page).

Puoi monitorare l’impatto della pagina di destinazione tramite rapporti specifici. [Ulteriori informazioni](../reports/lp-report-live.md)
