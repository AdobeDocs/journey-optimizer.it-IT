---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio SMS
description: Scopri come creare un messaggio SMS in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 13%

---

# Creare un messaggio SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creare un messaggio SMS"
>abstract="Aggiungi il messaggio SMS e inizia a personalizzarlo con l’editor di espressioni."

## Aggiungere un messaggio SMS {#create-sms-journey-campaign}

Sfoglia le schede seguenti per scoprire come aggiungere un messaggio SMS in una campagna o in un percorso.

>[!BEGINTABS]

>[!TAB Aggiungere un messaggio SMS a un Percorso]

1. Apri il percorso, quindi trascina e rilascia un’attività SMS da **Azioni** della palette.

   ![](assets/sms_create_1.png)

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria), quindi scegli l’area del messaggio da utilizzare.

   ![](assets/sms_create_2.png)

   Per ulteriori informazioni su come configurare un percorso, consulta [questa pagina](../building-journeys/journey-gs.md)

   La **[!UICONTROL Superficie]** Il campo è precompilato, per impostazione predefinita, con l’ultima superficie utilizzata dall’utente per quel canale.

Ora puoi iniziare a progettare il contenuto del messaggio SMS dal **[!UICONTROL Modifica contenuto]** pulsante . [Definire il contenuto SMS](#sms-content)

>[!TAB Aggiungere un messaggio SMS a una campagna]

1. Crea una nuova campagna pianificata o attivata dall’API, seleziona **[!UICONTROL SMS]** come azione e scegli la **[!UICONTROL Superficie dell&#39;app]** da utilizzare. [Ulteriori informazioni sulla configurazione degli SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Fai clic su **[!UICONTROL Crea]**.

1. Da **[!UICONTROL Proprietà]** , modifica la **[!UICONTROL Titolo]** e **[!UICONTROL Descrizione]**.

   ![](assets/sms_create_4.png)

1. In **[!UICONTROL Tracciamento delle azioni]** specifica se desideri tenere traccia dei clic sui collegamenti presenti nel messaggio SMS.

1. Fai clic sul pulsante **[!UICONTROL Selezionare il pubblico]** per definire il pubblico di cui eseguire il targeting dall’elenco dei segmenti Adobe Experience Platform disponibili. [Maggiori informazioni](../segment/about-segments.md).

1. In **[!UICONTROL Spazio dei nomi identità]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Maggiori informazioni](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Le campagne sono progettate per essere eseguite in una data specifica o su una frequenza ricorrente. Scopri come configurare il **[!UICONTROL Pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

1. Da **[!UICONTROL Trigger delle azioni]** scegliere il menu **[!UICONTROL Frequenza]** del messaggio SMS:

   * Una volta
   * Giornaliero
   * Settimanale
   * Mese

Ora puoi iniziare a progettare il contenuto del messaggio SMS dal **[!UICONTROL Modifica contenuto]** pulsante . [Progettazione del contenuto SMS](#sms-content)

>[!ENDTABS]

## Definire il contenuto SMS{#sms-content}

1. Dalla schermata di configurazione del percorso o della campagna, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** per configurare il contenuto SMS.

1. Fai clic sul pulsante **[!UICONTROL Messaggio]** per aprire l’editor espressioni.

   ![](assets/sms-content.png)

1. Utilizza l’editor espressioni per definire il contenuto e aggiungere contenuto dinamico. Puoi utilizzare qualsiasi attributo, ad esempio il nome del profilo o la città. Ulteriori informazioni [personalizzazione](../personalization/personalize.md) e [contenuto dinamico](../personalization/get-started-dynamic-content.md) nell’editor espressioni.

1. Dopo aver definito il contenuto, puoi aggiungere al messaggio gli URL di tracciamento. A questo scopo, accedi al **[!UICONTROL Funzioni di supporto]** menu e seleziona **[!UICONTROL Helper]**.

   Per utilizzare la funzione di abbreviazione degli URL, devi prima configurare un sottodominio da collegare alla tua superficie. [Ulteriori informazioni](sms-subdomains.md)

   ![](assets/sms_tracking_1.png)

1. All&#39;interno di **[!UICONTROL Funzioni di supporto]** menu, fai clic su **[!UICONTROL funzione URL]** quindi seleziona **[!UICONTROL Aggiungi URL]**.

   ![](assets/sms_tracking_2.png)

1. In `originalUrl` , incolla l’URL da accorciare.

1. Fai clic su **[!UICONTROL Salva]** e controlla il messaggio nell’anteprima. È possibile utilizzare **[!UICONTROL Simulazione del contenuto]** per visualizzare in anteprima gli URL abbreviati o contenuti personalizzati.

   ![](assets/sms-content-preview.png)

Ora puoi testare e inviare il messaggio SMS al tuo pubblico. [Ulteriori informazioni](send-sms.md)
Dopo l’invio, puoi misurare l’impatto dell’SMS nei rapporti Campaign o Percorso. Per ulteriori informazioni sul reporting, consulta [questa sezione](../reports/campaign-global-report.md#sms-tab).

>[!NOTE]
>
>In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. A tal fine, i destinatari SMS possono rispondere con parole chiave di consenso e rinuncia. [Scopri come gestire la rinuncia](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Argomenti correlati**

* [Anteprima, verifica e invia il messaggio SMS](send-sms.md)
* [Configurare il canale SMS](sms-configuration.md)
* [Rapporto SMS](../reports/journey-global-report.md#sms-global)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
* [Aggiungere un messaggio in una campagna](../campaigns/create-campaign.md)
