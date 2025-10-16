---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio LINE
description: Scopri come creare un messaggio LINE in Journey Optimizer
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: a93d4dc9-f0e9-400c-b9a4-6cdac84390fd
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 5%

---

# Creare un messaggio LINE {#create-line}

## Aggiungi un messaggio LINE {#create-line-journey-campaign}

Sfoglia le schede seguenti per scoprire come aggiungere un messaggio LINE in una campagna o in un percorso.

>[!BEGINTABS]

>[!TAB Aggiungere un messaggio LINE a un Percorso]

1. Apri il percorso, quindi trascina e rilascia un&#39;attività **LINE** dalla sezione **Actions** della palette.

   ![](assets/jo-line-1.png)

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria), quindi scegli la configurazione del messaggio da utilizzare.

   Per ulteriori informazioni su come configurare un percorso, fare riferimento a [questa pagina](../building-journeys/journey-gs.md)

   Il campo **[!UICONTROL configuration]** è precompilato, per impostazione predefinita, con l&#39;ultima configurazione utilizzata per quel canale dall&#39;utente.

Puoi iniziare a progettare il contenuto del messaggio LINE dal pulsante **[!UICONTROL Modifica contenuto]**, come descritto di seguito.

>[!TAB Aggiungere un messaggio LINE a una campagna]

1. Accedi al menu **[!UICONTROL Campagne]**, quindi fai clic su **[!UICONTROL Crea campagna]**.

1. Seleziona il tipo di campagna da eseguire

   * **Pianificato - Marketing**: esegui la campagna immediatamente o in una data specificata. Le campagne pianificate hanno lo scopo di inviare messaggi di marketing. Vengono configurati ed eseguiti dall’interfaccia utente di.

   * **Attivato da API - Marketing/Transazionale**: esegui la campagna utilizzando una chiamata API. Le campagne attivate da API hanno lo scopo di inviare messaggi di marketing o transazionali, ovvero messaggi inviati in seguito a un’azione eseguita da un individuo: reimpostazione della password, acquisto del carrello, ecc.

1. Dalla sezione **[!UICONTROL Proprietà]**, modifica il **[!UICONTROL Titolo]** e la **[!UICONTROL Descrizione]** della tua campagna.

1. Fai clic sul pulsante **[!UICONTROL Seleziona pubblico]** per definire il pubblico di destinazione dall&#39;elenco dei tipi di pubblico di Adobe Experience Platform disponibili. [Ulteriori informazioni](../audience/about-audiences.md).

1. Nel campo **[!UICONTROL Spazio dei nomi identità]**, scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti del pubblico selezionato. [Ulteriori informazioni](../event/about-creating.md#select-the-namespace).

1. Nella sezione **[!UICONTROL Azioni]**, scegli la **[!UICONTROL RIGA]** e seleziona o crea una nuova configurazione.

   Ulteriori informazioni sulla configurazione LINE in [questa pagina](line-configuration.md).

   ![](assets/campaign-line-1.png)

1. Fai clic su **[!UICONTROL Crea esperimento]** per iniziare a configurare l&#39;esperimento sui contenuti e creare trattamenti per misurarne le prestazioni e identificare l&#39;opzione migliore per il pubblico di destinazione. [Ulteriori informazioni](../content-management/content-experiment.md)

1. Nella sezione **[!UICONTROL Tracciamento azioni]**, specifica se desideri tenere traccia dei clic sui collegamenti nel messaggio SMS.

1. Le campagne sono progettate per essere eseguite in una data specifica o con una frequenza ricorrente. Scopri come configurare la **[!UICONTROL pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

1. Dal menu **[!UICONTROL Trigger azione]**, scegli la **[!UICONTROL Frequenza]** del messaggio SMS:

   * Una volta
   * Giornaliera
   * Settimanale
   * Month

Puoi iniziare a progettare il contenuto del messaggio di testo dal pulsante **[!UICONTROL Modifica contenuto]**, come descritto di seguito.

>[!ENDTABS]

## Definire il contenuto LINE{#line-content}

Adobe Journey Optimizer supporta i seguenti tipi di messaggi per LINE:

* **Testo**: invia messaggi di testo normale o formattato.
* **Adesivi**: incorpora gli adesivi nativi di LINE per aggiungere carattere ed espressività.
* **Immagini**: allega immagini per migliorare l&#39;aspetto visivo.
* **Video**: condividi contenuti video per la comunicazione dinamica.
* **Percorsi**: invia informazioni sulla posizione con le mappe.
* **Modelli**: utilizza modelli predefiniti per messaggi coerenti.
* **Messaggi Flex**: crea layout complessi con contenuti avanzati utilizzando messaggi Flex basati su JSON.

Questi tipi di messaggi possono essere configurati modificando direttamente il contenuto JSON, consentendo strategie di messaggistica dinamiche e personalizzate.

Per configurare il contenuto LINE, effettua le seguenti operazioni.

1. Dalla schermata di configurazione del percorso o della campagna, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** per configurare il contenuto dell&#39;SMS.

1. Fai clic su **[!UICONTROL Modifica codice]** per modificare il contenuto JSON.

1. Utilizza l’editor di personalizzazione per definire i contenuti, aggiungere personalizzazioni e contenuti dinamici. Puoi utilizzare qualsiasi attributo, ad esempio il nome del profilo o la città. È inoltre possibile definire regole condizionali. Per ulteriori informazioni sulla [personalizzazione](../personalization/personalize.md) e sul [contenuto dinamico](../personalization/get-started-dynamic-content.md) nell&#39;editor di personalizzazione, consulta le pagine seguenti.

1. Fai clic su **[!UICONTROL Salva]** e verifica il messaggio nell’anteprima.

1. Utilizza il pulsante **[!UICONTROL Simula contenuto]** per visualizzare in anteprima il contenuto del messaggio LINE e il contenuto personalizzato.

Dopo aver eseguito i test e convalidato il contenuto, puoi inviare il messaggio LINE al pubblico. Questi passaggi sono descritti in [questa pagina](send-line.md)

Una volta inviato, puoi misurare l’impatto della tua LINE all’interno dei rapporti della campagna o del Percorso. Per ulteriori informazioni sul reporting, consulta [questa sezione](../reports/campaign-global-report-cja.md).
