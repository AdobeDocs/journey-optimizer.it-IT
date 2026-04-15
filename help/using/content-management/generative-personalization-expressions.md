---
solution: Journey Optimizer
product: journey optimizer
title: Assistente AI per le espressioni Personalization
description: Scopri come utilizzare l’Assistente IA in Journey Optimizer Personalization Editor per generare nuove espressioni dal linguaggio naturale, spiegare o correggere il codice esistente e perfezionare le selezioni.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
mini-toc-levels: 1
source-git-commit: 0a2c384faea70dcbc9b99596740e375d85b2bc64
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 2%

---

# Assistente AI per le espressioni di personalizzazione{#generative-personalization-expressions}

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare questa funzionalità, leggi l’articolo sui relativi [Guardrail e limitazioni](gs-generative.md#generative-guardrails).
></br>
>
>Prima di poter utilizzare l&#39;Assistente di intelligenza artificiale in Journey Optimizer, devi accettare un [contratto utente](https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

## Panoramica {#where-available}

In [!UICONTROL Personalization Editor], [!UICONTROL AI Assistant] consente di generare nuove personalizzazioni dal linguaggio semplice, spiegare le funzioni delle espressioni esistenti e risolvere i problemi nel codice selezionato, in modo da dedicare meno tempo alla sintassi e all&#39;individuazione manuale dei campi. Puoi anche eseguire iterazioni su una selezione o chiedere altre modifiche nella conversazione.

* Per una configurazione e lingue più ampie dell&#39;Assistente di intelligenza artificiale, vedere [Introduzione all&#39;Assistente di intelligenza artificiale](gs-generative.md).
* Per ulteriori informazioni sulla personalizzazione in [!DNL Journey Optimizer], vedere [Introduzione alla personalizzazione](../personalization/personalize.md).
* Per suggerimenti, vedere [Best practice per la richiesta di IA](ai-assistant-prompting-guide.md).

È possibile utilizzare [!UICONTROL Assistente AI] nell&#39;[!UICONTROL Editor Personalization] ovunque sia disponibile l&#39;editor, ad esempio nella riga dell&#39;oggetto, nel corpo e in altri campi che lo aprono. Per sapere dove e come aprire l&#39;editor, consulta [Aggiungi personalizzazione](../personalization/personalization-build-expressions.md#where).

A seconda del contesto della campagna o del percorso, l&#39;assistente può lavorare con i dati e costruisce l&#39;[!UICONTROL Editor Personalization] già esposto, ad esempio attributi di profilo, appartenenza ai segmenti, funzioni di assistenza e origini di personalizzazione correlate.

>[!NOTE]
>
>L&#39;assistente mantiene il contesto dalle richieste solo mentre [!UICONTROL Assistente AI] rimane aperto nella sessione dell&#39;editor. Se si chiude l&#39;assistente o l&#39;[!UICONTROL Editor Personalization], la conversazione non verrà salvata. Alla successiva apertura dell&#39;assistente, verrà avviata una nuova conversazione.

## Generare espressioni di personalizzazione {#generate}

Questi passaggi descrivono come generare espressioni di personalizzazione da zero. Per utilizzare il codice già presente nell&#39;editor, vedere [Modifica, correzione o spiegazione del codice esistente](#edit-existing).

1. Nel messaggio o nel contenuto, apri **[!UICONTROL Personalization Editor]**.

1. Posiziona il cursore nell&#39;editor in cui desideri inserire il codice di personalizzazione generato, quindi fai clic sul pulsante **[!UICONTROL Assistente AI]**.

   ![](assets/ai-perso-access.png)

1. Nel campo di testo, descrivere l&#39;espressione di personalizzazione desiderata in linguaggio semplice, ad esempio gli attributi di profilo, i segmenti o la logica necessari, quindi fare clic su **[!UICONTROL Genera]**.

   È inoltre possibile utilizzare i prompt pronti all&#39;uso della sezione **[!UICONTROL Prompt rapidi]**, ad esempio messaggi di saluto personalizzati, generazione di codice promozionale e altro ancora.

   ![](assets/ai-perso-generate.png)

   >[!NOTE]
   >
   >Qualsiasi richiesta o domanda non correlata restituisce un errore fuori ambito. Regola il prompt e poni una domanda rilevante sulla personalizzazione necessaria.

1. Puoi continuare a discutere con l’assistente in una conversazione a più turni: mantiene il contesto dalle tue richieste in modo da poter perfezionare la stessa espressione passo dopo passo. Per ricominciare, fai clic sul pulsante **[!UICONTROL Nuova sessione]**.

   ![](assets/ai-perso-question.png)

1. Dopo aver generato un&#39;espressione, fare clic su **[!UICONTROL Mostra anteprime per i profili di esempio]** per vedere come l&#39;espressione viene valutata con i dati di esempio e per visualizzare il payload associato come JSON. Per questo controllo, l’assistente genera un set limitato di profili di esempio sintetici che non vengono salvati o memorizzati nell’organizzazione.

   Se hai bisogno di profili di esempio personalizzati o aggiuntivi, descrivi ciò che ti serve nella discussione con l&#39;assistente e includi la parola chiave **preview** nel prompt in modo che possa generare i profili di anteprima corretti per l&#39;assegno.

   ![](assets/ai-perso-preview-button.png)

   +++Esempio di anteprima

   ![](assets/ai-perso-preview.png)

   >[!NOTE]
   >
   >Ulteriori anteprime sono per il controllo a campione. L’assistente è sintonizzato in modo da generare approssimativamente da uno a cinque profili, richiedendo un numero molto elevato potrebbe causare un errore nella richiesta.

   +++

   >[!NOTE]
   >
   >Questo controllo serve per controllare rapidamente il codice di personalizzazione nell’editor e non per visualizzare un’anteprima completa dei messaggi relativi al contenuto. Per la convalida completa dell’esperienza, utilizza il flusso di simulazione abituale. [Scopri come visualizzare in anteprima e verificare il contenuto](../content-management/preview-test.md)

1. Per implementare l&#39;output nell&#39;espressione di personalizzazione, fare clic su **[!UICONTROL Applica]**. L’output dell’assistente viene inserito nella posizione del cursore nell’editor di personalizzazione. Per sostituire il codice già presente, selezionalo prima nell&#39;editor, quindi utilizza **[!UICONTROL Modifica con Assistente AI]** (vedi [Modifica, correggi o spiega il codice esistente](#edit-existing)).

   Puoi anche copiare l&#39;output e incollarlo dove necessario utilizzando l&#39;icona ![Copia](../orchestrated/assets/do-not-localize/activity-copy.svg).

## Modifica, correggi o spiega il codice esistente {#edit-existing}

Puoi selezionare un’espressione di personalizzazione esistente e utilizzare l’Assistente AI per risolvere i problemi di personalizzazione, spiegare cosa fa il codice o richiedere altre modifiche.

1. Seleziona il codice di personalizzazione esistente nell’editor.

1. Fare clic con il pulsante destro del mouse sulla selezione e scegliere **[!UICONTROL Modifica con Assistente IA]** in modo che l&#39;assistente utilizzi la selezione come contesto.

   ![](assets/ai-perso-right-click.png)

1. **[!UICONTROL Assistente AI]** verrà aperto. In **[!UICONTROL Comandi rapidi]**, fare clic su **[!UICONTROL Spiega]** o **[!UICONTROL Correggi]** oppure utilizzare il campo di testo per richiedere altre modifiche e avviare una conversazione.

   ![](assets/ai-perso-edit.png)

1. Quando utilizzi **[!UICONTROL Correzione]**, fai clic su **[!UICONTROL Mostra dettagli correzione]** nella discussione per visualizzare una spiegazione della correzione e una riga per riga prima e dopo l&#39;anteprima.

   ![](assets/ai-perso-fix.png)

1. Come quando generi un&#39;espressione di personalizzazione, fai clic su **[!UICONTROL Applica]** per implementare l&#39;output dell&#39;assistente. Sostituisce il codice selezionato nell’editor di personalizzazione. Ad esempio, se hai richiesto una spiegazione del codice, applicando aggiungerai commenti nell’espressione che descrivono ciò che fa.
