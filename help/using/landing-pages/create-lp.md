---
title: Creare una pagina di destinazione
description: Scopri come configurare e pubblicare una pagina di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 1%

---

# Creare e pubblicare pagine di destinazione {#create-lp}

## Accedere alle pagine di destinazione {#access-landing-pages}

Per accedere all’elenco delle pagine di destinazione, seleziona **[!UICONTROL Journey Management]** > **[!UICONTROL Landing pages]** dal menu a sinistra.

![](assets/lp_access-list.png)

La **[!UICONTROL Landing Pages]** visualizza tutti gli elementi creati. Puoi filtrarli in base al loro stato o alla data di modifica.

![](assets/lp_access-list-filter.png)

Da questo elenco è possibile accedere al [report live della pagina di destinazione](../reports/lp-report-live.md) o [report globale della pagina di destinazione](../reports/lp-report-global.md) per gli elementi pubblicati.

Puoi anche eliminare, duplicare e annullare la pubblicazione di una pagina di destinazione.

>[!CAUTION]
>
>Se annulli la pubblicazione di una pagina di destinazione a cui viene fatto riferimento in un messaggio non pubblicato, non potrai più pubblicare il messaggio finché la pagina di destinazione non viene pubblicata nuovamente. Se il messaggio è già stato pubblicato, il collegamento alla pagina di destinazione non funzionerà e verrà visualizzata una pagina di errore.

Fai clic sui tre punti accanto a una pagina di destinazione per selezionare l’azione desiderata.

![](assets/lp_access-list-actions.png)

>[!NOTE]
>
>Non è possibile eliminare una pagina di destinazione pubblicata. Per eliminarlo, devi prima annullarne la pubblicazione.

## Creare una pagina di destinazione {#create-landing-page}

I passaggi per creare una pagina di destinazione sono i seguenti:

1. Dall’elenco della pagina di destinazione, fai clic su **[!UICONTROL Create landing page]**.

   ![](assets/lp_create-lp.png)

1. Aggiungi un titolo. Se necessario, puoi aggiungere una descrizione.

   ![](assets/lp_create-lp-details.png)

1. Seleziona un predefinito. Scopri come creare i predefiniti per le pagine di destinazione in [questa sezione](../configuration/lp-configuration.md#lp-create-preset).

   ![](assets/lp_create-lp-presets.png)

1. Fai clic su **[!UICONTROL Create]**.

1. Viene visualizzata la pagina principale e le relative proprietà. Scopri come configurare le impostazioni della pagina principale [qui](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. Fai clic sull’icona + per aggiungere una pagina secondaria. Scopri come configurare le impostazioni della pagina secondaria [qui](#configure-subpages).

   ![](assets/lp_add-subpage.png)

Una volta configurati e progettati i [pagina principale](#configure-primary-page)e [sottopagine](#configure-subpages) se presente, puoi [test](#test-landing-page) e [pubblicare](#publish-landing-page) la pagina di destinazione.

## Configurare la pagina principale {#configure-primary-page}

La pagina principale è quella immediatamente visualizzata dagli utenti dopo aver fatto clic sul collegamento alla pagina di destinazione, ad esempio da un’e-mail o da un sito web.

Per definire le impostazioni della pagina principale, segui la procedura seguente.

1. È possibile modificare il nome della pagina, ovvero **[!UICONTROL Primary page]** per impostazione predefinita.

1. Modifica il contenuto della pagina utilizzando la finestra di progettazione dei contenuti. Scopri come definire il contenuto della pagina di destinazione [qui](design-lp.md).

   ![](assets/lp_open-designer.png)

1. Definisci l’URL della pagina di destinazione. La prima parte dell’URL richiede la configurazione di un sottodominio della pagina di destinazione. [Ulteriori informazioni](../configuration/lp-configuration.md#lp-subdomains)

   >[!CAUTION]
   >
   >L’URL della pagina di destinazione deve essere univoco.

   ![](assets/lp_access-url.png)

   >[!NOTE]
   >
   >Non puoi accedere alla pagina di destinazione semplicemente copiando e incollando questo URL in un browser web, anche se pubblicato. Puoi invece testarlo utilizzando la funzione di anteprima come descritto in [questa sezione](#test-landing-page).

1. Puoi definire una data di scadenza per la pagina. In tal caso, è necessario selezionare un’azione alla scadenza della pagina:

   * **[!UICONTROL Redirect URL]**: Inserisci l’URL della pagina a cui verranno reindirizzati gli utenti alla scadenza della pagina.
   * **[!UICONTROL Custom page]**: [Configurare una pagina secondaria](#configure-subpages) e selezionalo dall’elenco a discesa visualizzato.
   * **[!UICONTROL Browser error]**: Digita il testo di errore che verrà visualizzato al posto della pagina.

   ![](assets/lp_expiry-date.png)

   <!--1. In the **[!UICONTROL Additional data]** section, define a **[!UICONTROL Key]** and the corresponding **[!UICONTROL Parameter value]**. // you can define how the data entered in the landing page is managed once it has been submitted by a user??-->

1. Se hai selezionato uno o più elenchi di sottoscrizioni quando [progettazione della pagina principale](design-lp.md), vengono visualizzati nella **[!UICONTROL Subscription list]** sezione .

   ![](assets/lp_subscription-list.png)

1. Dalla pagina di destinazione, puoi [creare un percorso](../building-journeys/journey-gs.md#jo-build) che invierà un messaggio di conferma agli utenti al momento dell’invio del modulo. Scopri come creare un tale percorso alla fine di questo [caso d&#39;uso](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   Fai clic su **[!UICONTROL Create journey]** da reindirizzare al **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** elenco.

## Configurare le pagine secondarie {#configure-subpages}

È possibile aggiungere fino a 2 sottopagine. Ad esempio, è possibile creare una pagina di ringraziamento che verrà visualizzata dopo l’invio del modulo da parte degli utenti, nonché definire una pagina di errore da chiamare in caso di problemi relativi alla pagina di destinazione.

Per definire le impostazioni della pagina secondaria, segui la procedura seguente.

1. È possibile modificare il nome della pagina, ovvero **[!UICONTROL Subpage 1]** per impostazione predefinita.

1. Modifica il contenuto della pagina utilizzando la finestra di progettazione dei contenuti. Scopri come definire il contenuto della pagina di destinazione [qui](design-lp.md).

1. Definisci l’URL della pagina di destinazione. La prima parte dell’URL richiede la configurazione di un sottodominio della pagina di destinazione. [Ulteriori informazioni](../configuration/lp-configuration.md#lp-subdomains)

   >[!CAUTION]
   >
   >L’URL della pagina di destinazione deve essere univoco.

![](assets/lp_subpage-settings.png)

## Verificare la pagina di destinazione {#test-landing-page}

Una volta definite le impostazioni e il contenuto della pagina di destinazione, puoi utilizzare i profili di test per visualizzarli in anteprima. Se hai inserito [contenuti personalizzati](../personalization/personalize.md), potrai controllare in che modo questo contenuto viene visualizzato nella pagina di destinazione, sfruttando i dati del profilo di test.

>[!CAUTION]
>
>Per visualizzare l’anteprima dei messaggi e inviare le bozze, devi disporre dei profili di test. Scopri come [creare profili di test](../segment/creating-test-profiles.md).

1. Nell’interfaccia della pagina di destinazione, fai clic sul pulsante **[!UICONTROL Preview & test]** per accedere alla selezione del profilo di test.

   ![](assets/lp_preview-button.png)

   >[!NOTE]
   >
   >La **[!UICONTROL Preview]** accessibile anche dal designer del contenuto.

1. Da **[!UICONTROL Preview & test]** seleziona uno o più profili di test.

   ![](assets/lp_test-profiles.png)

   I passaggi per selezionare i profili di test sono gli stessi che per testare un messaggio. Essi sono descritti in [questa sezione](../design/preview.md#select-test-profiles).

1. Seleziona la **[!UICONTROL Preview]** e fai clic su **[!UICONTROL Open preview]** per verificare la pagina di destinazione.

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

Una volta pubblicata, la pagina di destinazione viene aggiunta all’elenco della pagina di destinazione con la **[!UICONTROL Published]** stato.

È ora attivo e pronto per essere utilizzato in un [!DNL Journey Optimizer] [message](../messages/get-started-content.md) che verranno inviati attraverso un [percorso](../building-journeys/journey.md).

>[!NOTE]
>
>Puoi monitorare l’impatto della pagina di destinazione tramite report specifici. [Ulteriori informazioni](../reports/lp-report-live.md)

