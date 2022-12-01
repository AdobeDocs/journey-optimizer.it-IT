---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio SMS
description: Scopri come creare un messaggio SMS in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b7b333e96e0f4b32a0f94c3f1e67f0f3d3fc2816
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 7%

---

# Creare un messaggio SMS {#create-sms-bis}

>[!NOTE]
>
>In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. A tal fine, i destinatari SMS possono rispondere con parole chiave di consenso e rinuncia.

## Creare un messaggio SMS in un percorso o in una campagna {#sms-content}

Per iniziare a personalizzare il messaggio SMS, segui questi passaggi:

>[!BEGINTABS]

>[!TAB Aggiungere un messaggio SMS a un Percorso]

1. Apri il percorso, quindi trascina e rilascia un’attività SMS dalla sezione Azioni della palette.

1. Fornisci informazioni di base sul messaggio (etichetta, descrizione, categoria), quindi scegli l’area del messaggio da utilizzare.

   Per ulteriori informazioni su come configurare un percorso, consulta .

Ora puoi iniziare a progettare il contenuto del messaggio SMS dal **[!UICONTROL Modifica contenuto]** pulsante .

>[!TAB Aggiungere un messaggio SMS a una campagna]

1. Crea una nuova campagna pianificata o attivata dall’API, seleziona **[!UICONTROL SMS]** come azione e scegli la **[!UICONTROL Superficie dell&#39;app]** da utilizzare.

1. Fai clic su **[!UICONTROL Crea]**.

1. Da **[!UICONTROL Proprietà]** , modifica la **[!UICONTROL Titolo]** e **[!UICONTROL Descrizione]**.

1. In **[!UICONTROL Tracciamento delle azioni]** specifica se desideri tenere traccia dei clic sui collegamenti presenti nel messaggio SMS.

1. Fai clic sul pulsante **[!UICONTROL Selezionare il pubblico]** per definire il pubblico di cui eseguire il targeting dall’elenco dei segmenti Adobe Experience Platform disponibili.

1. In **[!UICONTROL Spazio dei nomi identità]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato.

1. Le campagne sono progettate per essere eseguite in una data specifica o su una frequenza ricorrente. Scopri come configurare il **[!UICONTROL Pianificazione]** della campagna in.

1. Da **[!UICONTROL Trigger delle azioni]** scegliere il menu **[!UICONTROL Frequenza]** del messaggio SMS:

   * Una volta
   * Giornaliero
   * Settimanale
   * Mese

Ora puoi iniziare a progettare il contenuto del messaggio SMS dal **[!UICONTROL Modifica contenuto]** pulsante .

>[!ENDTABS]

## Definire il contenuto SMS{#sms-content}

1. Dalla schermata di configurazione del percorso o della campagna, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** per configurare il contenuto SMS.

1. Fai clic sul pulsante **[!UICONTROL Messaggio]** per aprire l’editor espressioni.

1. Utilizza l’editor espressioni per definire il contenuto e aggiungere contenuto dinamico. Puoi utilizzare qualsiasi attributo, ad esempio il nome del profilo o la città.

1. Fai clic su **[!UICONTROL Salva]** e controlla il messaggio nell’anteprima.

1. Quando il messaggio SMS è pronto, completa la configurazione del tuo per inviarlo.

## Convalidare l’SMS{#sms-preview}

>[!NOTE]
>
> Per una migliore consegna, è sempre necessario utilizzare i numeri di telefono nei formati supportati dal provider. Ad esempio, Twilio e Sinch supportano solo i numeri di telefono in formato E.164.

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo. Se hai inserito, puoi controllare come questo contenuto viene visualizzato nel messaggio, utilizzando i dati del profilo di test.

Per visualizzare la modalità di visualizzazione del messaggio SMS sui dispositivi mobili, fai clic sul pulsante **[!UICONTROL Simulazione del contenuto]** scheda . Ulteriori informazioni sulla simulazione dei contenuti in.

È inoltre necessario controllare gli avvisi nella sezione superiore dell’editor.  Alcuni sono semplici avvisi, altri possono impedire l’utilizzo del messaggio. Ulteriori informazioni in.
