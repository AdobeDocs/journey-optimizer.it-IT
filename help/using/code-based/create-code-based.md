---
title: Creare esperienze basate su codice
description: Scopri come creare esperienze basate su codice in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 9%

---

# Creare esperienze basate su codice {#create-code-based}

Attualmente in [!DNL Journey Optimizer] puoi creare esperienze basate su codice solo in **campagne**.

I dettagli su guardrail e consigli specifici per esperienze basate su codice sono disponibili in [questa pagina](code-based-prerequisites.md).

## Creare una campagna basata su codice {#create-code-based-campaign}

Per iniziare a creare l’esperienza basata su codice tramite una campagna, segui i passaggi indicati di seguito.

1. Creare una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Seleziona la **[!UICONTROL Esperienza basata su codice]** azione.

1. Immetti la superficie esperienza basata su codice. [Ulteriori informazioni](#surface-definition)

   ![](assets/code-based-campaign-surface.png)

   >[!CAUTION]
   >
   >Assicurati che l’URI di superficie utilizzato nella campagna basata su codice corrisponda a quello utilizzato nella tua implementazione. In caso contrario, le modifiche non verranno consegnate.

1. Seleziona **[!UICONTROL Crea]**.

1. Completa i passaggi per creare una campagna, ad esempio le proprietà, [pubblico](../audience/about-audiences.md), e [pianificazione](../campaigns/create-campaign.md#schedule). Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

1. Modifica il contenuto come desideri utilizzando l’editor di espressioni. [Ulteriori informazioni](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## Modificare il contenuto del codice {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="Utilizzare l’editor di espressioni"
>abstract="Inserisci e modifica il codice che desideri consegnare come parte di questa azione di esperienza basata su codice."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html?lang=it" text="Introduzione all’editor di espressioni"

1. Dalla schermata dell’edizione della campagna, seleziona **[!UICONTROL Modifica codice]**.

   ![](assets/code-based-campaign-edit-code.png)

1. Il [Editor espressioni](../personalization/personalization-build-expressions.md) viene aperto. Si tratta di un’interfaccia non visiva per la creazione di esperienze che consente di creare il codice.

1. Puoi passare dalla modalità di authoring di HTML a JSON e viceversa.

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >La modifica della modalità di authoring comporterà la perdita di tutto il codice corrente; assicurati quindi di cambiare modalità prima di iniziare l’authoring.

1. Immetti il codice in base alle esigenze. Puoi sfruttare [!DNL Journey Optimizer] Editor espressioni con tutte le sue funzionalità di personalizzazione e authoring. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

1. Se necessario, puoi aggiungere frammenti di espressione HTML o JSON. [Scopri come](../personalization/use-expression-fragments.md)

   Puoi anche salvare parte del contenuto del codice come frammento. [Scopri come](../content-management/fragments.md#save-as-expression-fragment)

1. Nelle campagne basate su codice, puoi utilizzare la funzione Experience Decisioning. Seleziona la **[!UICONTROL Decisioni]** dalla barra a sinistra e fai clic su **[!UICONTROL Crea decisione]**. [Ulteriori informazioni](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >La funzione Experience Decisioning è attualmente disponibile come versione beta solo per alcuni utenti.


1. Clic **[!UICONTROL Salva e chiudi]** per confermare le modifiche.

Ora, non appena lo sviluppatore effettua una chiamata API o SDK per recuperare il contenuto per la superficie selezionata, le modifiche verranno applicate alla pagina web o all’app.

## Testare la campagna basata sul codice {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Visualizzare l’esperienza basata su codice in anteprima"
>abstract="Ottieni una simulazione dell’aspetto che avrà l’esperienza basata su codice."

Per visualizzare un’anteprima dell’esperienza basata su codice modificata, segui i passaggi indicati di seguito. Informazioni dettagliate su come selezionare i profili di test e visualizzare in anteprima i contenuti sono disponibili nella sezione [Anteprima e verifica della pagina di contenuto](../content-management/preview-test.md).

>[!CAUTION]
>
>Devi disporre di profili di test per simulare quali offerte verranno consegnate. Scopri come [creare profili di test](../audience/creating-test-profiles.md).

1. Dall’editor espressioni o dalla schermata Modifica contenuto, seleziona **[!UICONTROL Simula contenuto]**.

   ![](assets/code-based-campaign-simulate.png)

1. Clic **[!UICONTROL Gestire i profili di test]** per selezionare uno o più profili di test.

1. Viene visualizzata un’anteprima dell’esperienza basata su codice modificata.

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## Attivare la campagna basata su codice {#activate-code-based-campaign}

Dopo aver definito la campagna basata su codice e aver modificato il contenuto come desiderato utilizzando [editor basato su codice](#edit-code), puoi rivederlo e attivarlo. Segui i passaggi seguenti.

>[!NOTE]
>
>Puoi anche visualizzare in anteprima il contenuto della campagna prima di attivarla. [Ulteriori informazioni](#test-code-based-campaign)

1. Dalla campagna basata su codice, seleziona **[!UICONTROL Controlla per attivare]**.

   ![](assets/code-based-campaign-review.png)

1. Se necessario, seleziona e modifica il contenuto, le proprietà, la superficie, il pubblico e la pianificazione.

1. Seleziona **[!UICONTROL Attiva]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Dopo aver fatto clic su **[!UICONTROL Attiva]**, le modifiche alle campagne basate su codice possono richiedere fino a 1 minuto per essere disponibili in tempo reale sulla tua posizione.

La campagna basata su codice accetta **[!UICONTROL Live]** ed è ora visibile al pubblico selezionato. Ogni destinatario della campagna può visualizzare le modifiche apportate.

>[!NOTE]
>
>Se hai definito una pianificazione per la campagna basata su codice, questa presenta **[!UICONTROL Pianificato]** fino al raggiungimento della data e dell’ora di inizio.
>
>Se attivi una campagna basata su codice che influisce sulle stesse posizioni di un’altra campagna già live, tutte le modifiche verranno applicate alle posizioni.

Ulteriori informazioni sull’attivazione delle campagne in [questa sezione](../campaigns/review-activate-campaign.md).

## Interrompere una campagna basata su codice {#stop-code-based-campaign}

Quando una campagna basata su codice è attiva, puoi interromperla per impedire al pubblico di visualizzare le modifiche. Segui i passaggi seguenti.

1. Seleziona una campagna live dall’elenco.

1. Dal menu principale, seleziona **[!UICONTROL Interrompi campagna]**.

   ![](assets/code-based-campaign-stop.png)

1. Le modifiche aggiunte non saranno più visibili al pubblico definito.

>[!NOTE]
>
>Una volta interrotta una campagna basata su codice, non puoi più modificarla o attivarla. Puoi solo duplicarlo e attivare la campagna duplicata.

## Rapporti sulle campagne basati su codice

Puoi accedere ai rapporti delle campagne basati su codice dalla schermata di riepilogo della campagna.

I report globali visualizzano gli eventi che si sono verificati almeno due ore fa e coprono gli eventi in un periodo di tempo selezionato. Al confronto, i rapporti live si concentrano sugli eventi che si sono verificati nelle ultime 24 ore, con un intervallo di tempo minimo di due minuti dall’occorrenza dell’evento.

### Report live basato su codice {#live-report-code-based}

Dalla campagna **[!UICONTROL Rapporto live]**, il **[!UICONTROL Esperienza basata su codice]** Questa scheda contiene le informazioni principali relative alle app o alle pagine web. [Ulteriori informazioni sui report live](../reports/campaign-live-report.md)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto di esperienza basato sul codice.

Il **[!UICONTROL Prestazioni delle esperienze basate su codice]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con le esperienze basate su codice, ad esempio:

* **[!UICONTROL Impression]**: numero totale di esperienze consegnate a tutti gli utenti.

* **[!UICONTROL Interazioni]**: numero totale di impegni con l’app o la pagina. Ciò include qualsiasi azione eseguita dagli utenti, ad esempio clic o altre interazioni.

Il **[!UICONTROL Riepilogo dell’esperienza basata su codice]** il grafico mostra l’evoluzione delle tue esperienze (impression, impression e interazioni uniche) nelle ultime 24 ore.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### Rapporto globale basato su codice {#global-report-code-based}

Il rapporto globale della campagna basato su codice è accessibile direttamente dalla campagna con **[!UICONTROL Visualizza rapporto]** pulsante. [Ulteriori informazioni sul rapporto globale](../reports/campaign-global-report.md)

Dalla campagna **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Esperienza basata su codice]** Questa scheda contiene le informazioni principali relative alle app o alle pagine web.

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto di esperienza basato sul codice.

Il **[!UICONTROL Prestazioni delle esperienze basate su codice]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con le esperienze, ad esempio:

* **[!UICONTROL Impression univoche]**: numero di utenti univoci a cui è stata consegnata l’esperienza.

* **[!UICONTROL Impression]**: numero totale di esperienze consegnate a tutti gli utenti.

* **[!UICONTROL Interazioni]**: percentuale di accordi con l’app o la pagina. Ciò include qualsiasi azione eseguita dagli utenti, ad esempio clic o altre interazioni.

Il **[!UICONTROL Riepilogo dell’esperienza basata su codice]** il grafico mostra l’evoluzione delle tue esperienze (impression, impression e interazioni uniche) per il periodo in questione.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
