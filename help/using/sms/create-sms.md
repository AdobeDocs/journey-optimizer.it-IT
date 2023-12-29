---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio SMS/MMS
description: Scopri come creare un messaggio SMS/MMS in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 227cdb77b0db40c59fa089789c444c2364fd062e
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 4%

---

# Creare un messaggio di testo (SMS/MMS){#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creare un messaggio SMS"
>abstract="Per creare un messaggio di testo (SMS/MMS), aggiungi un’azione SMS in un percorso o in una campagna e inizia a personalizzarla con l’editor espressioni."

È possibile progettare e inviare messaggi di testo (SMS) e multimediali (MMS) con Adobe Journey Optimizer. Devi innanzitutto aggiungere un’azione SMS in un percorso o in una campagna e quindi definire il contenuto del messaggio di testo, come descritto di seguito. Adobe Journey Optimizer offre inoltre funzionalità per testare i messaggi di testo prima dell’invio, in modo da poter controllare il rendering, gli attributi di personalizzazione e tutte le altre impostazioni.

>[!NOTE]
>
>In conformità agli standard e alle normative del settore, tutti i messaggi SMS/MMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. A questo scopo, i destinatari di SMS possono rispondere con parole chiave di consenso e rinuncia. [Scopri come gestire la rinuncia](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)


## Aggiungi un SMS {#create-sms-journey-campaign}

Sfoglia le schede seguenti per scoprire come aggiungere un messaggio di testo (SMS/MMS) in una campagna o in un percorso.

>[!BEGINTABS]

>[!TAB Aggiungere un SMS a un Percorso]

1. Apri il percorso, quindi trascina e rilascia un’attività SMS dal file **Azioni** nella palette.

   ![](assets/sms_create_1.png)

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria), quindi scegli la superficie del messaggio da utilizzare.

   ![](assets/sms_create_2.png)

   Per ulteriori informazioni su come configurare un percorso, consulta [questa pagina](../building-journeys/journey-gs.md)

   Il **[!UICONTROL Superficie]** Il campo è precompilato, per impostazione predefinita, con l’ultima superficie utilizzata dall’utente per quel canale.

Ora puoi iniziare a progettare il contenuto del messaggio SMS dalla sezione **[!UICONTROL Modifica contenuto]** come descritto di seguito.

>[!TAB Aggiungere un messaggio di testo a una campagna]

1. Crea una nuova campagna pianificata o attivata da API, seleziona **[!UICONTROL SMS]** come azione e scegli il **[!UICONTROL Superficie app]** da utilizzare. Ulteriori informazioni sulla configurazione degli SMS in [questa pagina](sms-configuration.md).

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

Ora puoi iniziare a progettare il contenuto del messaggio di testo dalla sezione **[!UICONTROL Modifica contenuto]** come descritto di seguito.

>[!ENDTABS]

## Definire il contenuto degli SMS{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="Definire il contenuto degli SMS"
>abstract="Personalizza e personalizza i messaggi di testo (SMS/MMS) utilizzando l’editor di espressioni per definire il contenuto e incorporare elementi dinamici."

Per configurare il contenuto SMS, segui i passaggi indicati di seguito. Le impostazioni per MMS sono descritte in dettaglio in [questa sezione](#mms-content).

1. Dalla schermata di configurazione del percorso o della campagna, fai clic su **[!UICONTROL Modifica contenuto]** per configurare il contenuto del messaggio di testo.

1. Fai clic su **[!UICONTROL Messaggio]** per aprire l’editor di espressioni.

   ![](assets/sms-content.png)

1. Utilizza l’editor espressioni per definire i contenuti, aggiungere personalizzazioni e contenuti dinamici. Puoi utilizzare qualsiasi attributo, ad esempio il nome del profilo o la città. È inoltre possibile definire regole condizionali. Per ulteriori informazioni, consulta le pagine seguenti [personalizzazione](../personalization/personalize.md) e [contenuto dinamico](../personalization/get-started-dynamic-content.md) nell’editor di espressioni.

1. Dopo aver definito il contenuto, puoi aggiungere URL tracciati al messaggio. A questo scopo, accedi a **[!UICONTROL Funzioni di supporto]** menu e seleziona **[!UICONTROL Helper]**.

   Per utilizzare la funzione di abbreviazione URL, devi prima configurare un sottodominio che verrà quindi collegato alla tua superficie. [Ulteriori informazioni](sms-subdomains.md)

   >[!CAUTION]
   >
   > Per accedere e modificare i sottodomini SMS, devi disporre del **[!UICONTROL Gestire i sottodomini SMS]** autorizzazione per la sandbox di produzione. Ulteriori informazioni sulle autorizzazioni sono disponibili in [questa sezione](../administration/high-low-permissions.md).

   ![](assets/sms_tracking_1.png)

1. All&#39;interno del **[!UICONTROL Funzioni di supporto]** menu, fai clic su **[!UICONTROL Funzione URL]** e quindi seleziona **[!UICONTROL Aggiungi URL]**.

   ![](assets/sms_tracking_2.png)

1. In `originalUrl` , incolla l’URL da abbreviare e fai clic su **[!UICONTROL Salva]**.

1. Clic **[!UICONTROL Salva]** e controlla il messaggio nell’anteprima. Ora puoi testare e controllare il contenuto del messaggio come descritto in [questa sezione](#sms-mms-test).


## Definire il contenuto MMS{#mms-content}

È possibile migliorare la comunicazione inviando messaggi MMS (Multimedia Message Service), consentendo la condivisione di file multimediali quali video, immagini, clip audio e GIF e altro ancora. Inoltre, MMS consente di inserire nel messaggio fino a 1600 caratteri di testo.


>[!NOTE]
>
>* Questa funzione è attualmente disponibile con **Sinch** solo.
>
>* Il canale MMS presenta alcune limitazioni elencate in [questa pagina](../start/guardrails.md#sms-guardrails).
>

Per creare contenuti MMS, effettua le seguenti operazioni:

1. Creare un SMS come descritto in [questa sezione](#create-sms-journey-campaign).

1. Modifica il contenuto SMS come descritto in [questa sezione](#sms-content).

1. Abilita l’opzione MMS per aggiungere contenuti multimediali al contenuto SMS.

   ![](assets/sms_create_6.png)

1. Aggiungi un **[!UICONTROL Titolo]** ai tuoi contenuti multimediali.

1. Immetti l’URL del file multimediale in **[!UICONTROL Contenuti multimediali]** campo.

   ![](assets/sms_create_7.png)

1. Clic **[!UICONTROL Salva]** e controlla il messaggio nell’anteprima. Ora puoi testare e verificare il contenuto del messaggio come descritto di seguito.

## Testare e inviare i messaggi {#sms-mms-test}

Utilizza il **[!UICONTROL Simula contenuto]** per visualizzare in anteprima il contenuto del messaggio di testo, gli URL abbreviati e il contenuto personalizzato.

![](assets/sms-content-preview.png)

Dopo aver eseguito i test e convalidato il contenuto, puoi inviare il messaggio di testo al pubblico. Questi passaggi sono descritti in [questa pagina](send-sms.md)

Una volta inviato, puoi misurare l’impatto del tuo SMS all’interno dei rapporti della campagna o del Percorso. Per ulteriori informazioni sul reporting, consulta [questa sezione](../reports/campaign-global-report.md#sms-tab).

**Argomenti correlati**

* [Anteprima, verifica e invio del messaggio di testo](send-sms.md)
* [Configurare il canale SMS](sms-configuration.md)
* [Rapporti SMS/MMS](../reports/journey-global-report.md#sms-global)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
* [Aggiungere un messaggio in una campagna](../campaigns/create-campaign.md)
