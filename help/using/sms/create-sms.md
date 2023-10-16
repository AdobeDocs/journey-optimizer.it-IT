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
source-git-commit: b4e3d0ac51ffcabfd7168b9a01e9446adc61ff53
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 18%

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

1. Apri il percorso, quindi trascina e rilascia un’attività SMS dal file **Azioni** nella palette.

   ![](assets/sms_create_1.png)

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria), quindi scegli la superficie del messaggio da utilizzare.

   ![](assets/sms_create_2.png)

   Per ulteriori informazioni su come configurare un percorso, consulta [questa pagina](../building-journeys/journey-gs.md)

   Il **[!UICONTROL Superficie]** Il campo è precompilato, per impostazione predefinita, con l’ultima superficie utilizzata dall’utente per quel canale.

Ora puoi iniziare a progettare il contenuto del messaggio SMS dalla sezione **[!UICONTROL Modifica contenuto]** pulsante. [Definire il contenuto degli SMS](#sms-content)

>[!TAB Aggiungere un messaggio SMS a una campagna]

1. Crea una nuova campagna pianificata o attivata da API, seleziona **[!UICONTROL SMS]** come azione e scegli il **[!UICONTROL Superficie app]** da utilizzare. [Ulteriori informazioni sulla configurazione degli SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Fai clic su **[!UICONTROL Crea]**.

1. Dalla sezione **[!UICONTROL Proprietà]** , modifica i **[!UICONTROL Titolo]** e **[!UICONTROL Descrizione]**.

   ![](assets/sms_create_4.png)

1. Fai clic su **[!UICONTROL Seleziona pubblico]** per definire il pubblico di destinazione dall’elenco dei tipi di pubblico di Adobe Experience Platform disponibili. [Ulteriori informazioni](../audience/about-audiences.md).

1. In **[!UICONTROL Spazio dei nomi dell’identità]** , scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti del pubblico selezionato. [Ulteriori informazioni](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Clic **[!UICONTROL Crea esperimento]** per iniziare a configurare l’esperimento sui contenuti e creare trattamenti per misurarne le prestazioni e identificare l’opzione migliore per il pubblico di destinazione. [Ulteriori informazioni](../campaigns/content-experiment.md)

1. In **[!UICONTROL Tracciamento delle azioni]** , specifica se desideri tenere traccia dei clic sui collegamenti nel messaggio SMS.

1. Le campagne sono progettate per essere eseguite in una data specifica o con una frequenza ricorrente. Scopri come configurare **[!UICONTROL Pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

1. Dalla sezione **[!UICONTROL Trigger azione]** scegliere il menu **[!UICONTROL Frequenza]** del messaggio SMS:

   * Una volta
   * Giornaliero
   * Settimanale
   * Mese

Ora puoi iniziare a progettare il contenuto del messaggio SMS dalla sezione **[!UICONTROL Modifica contenuto]** pulsante. [Progettare i contenuti SMS](#sms-content)

>[!ENDTABS]

## Definire il contenuto degli SMS{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="Definire il contenuto degli SMS"
>abstract="Personalizza i messaggi SMS utilizzando l’editor di espressioni per definire il contenuto e incorporare elementi dinamici."

1. Dalla schermata di configurazione del percorso o della campagna, fai clic su **[!UICONTROL Modifica contenuto]** per configurare il contenuto SMS.

1. Fai clic su **[!UICONTROL Messaggio]** per aprire l’editor di espressioni.

   ![](assets/sms-content.png)

1. Utilizza l’editor espressioni per definire il contenuto e aggiungere contenuto dinamico. Puoi utilizzare qualsiasi attributo, ad esempio il nome del profilo o la città. Ulteriori informazioni su [personalizzazione](../personalization/personalize.md) e [contenuto dinamico](../personalization/get-started-dynamic-content.md) nell’editor di espressioni.

1. Dopo aver definito il contenuto, puoi aggiungere gli URL di tracciamento al messaggio. A questo scopo, accedi a **[!UICONTROL Funzioni di supporto]** menu e seleziona **[!UICONTROL Helper]**.

   Per utilizzare la funzione di abbreviazione URL, devi prima configurare un sottodominio che verrà quindi collegato alla tua superficie. [Ulteriori informazioni](sms-subdomains.md)

   >[!CAUTION]
   >
   > Per accedere e modificare i sottodomini SMS, devi disporre del **[!UICONTROL Gestire i sottodomini SMS]** autorizzazione per la sandbox di produzione.

   ![](assets/sms_tracking_1.png)

1. All&#39;interno del **[!UICONTROL Funzioni di supporto]** menu, fai clic su **[!UICONTROL Funzione URL]** e quindi seleziona **[!UICONTROL Aggiungi URL]**.

   ![](assets/sms_tracking_2.png)

1. In `originalUrl` , incollare l&#39;URL che si desidera ridurre.

1. Fai clic su **[!UICONTROL Salva]** e verifica il messaggio nell’anteprima. È possibile utilizzare **[!UICONTROL Simula contenuto]** per visualizzare in anteprima gli URL abbreviati o i contenuti personalizzati.

   ![](assets/sms-content-preview.png)

Ora puoi testare e inviare il messaggio SMS al pubblico. [Ulteriori informazioni](send-sms.md)
Una volta inviato, puoi misurare l’impatto del tuo SMS all’interno dei rapporti della campagna o del Percorso. Per ulteriori informazioni sul reporting, consulta [questa sezione](../reports/campaign-global-report.md#sms-tab).

>[!NOTE]
>
>In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. A questo scopo, i destinatari di SMS possono rispondere con parole chiave di consenso e rinuncia. [Scopri come gestire la rinuncia](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Argomenti correlati**

* [Visualizzare l’anteprima, testare e inviare il messaggio SMS](send-sms.md)
* [Configurare il canale SMS](sms-configuration.md)
* [Rapporto SMS](../reports/journey-global-report.md#sms-global)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
* [Aggiungere un messaggio in una campagna](../campaigns/create-campaign.md)
