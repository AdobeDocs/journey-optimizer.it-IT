---
solution: Journey Optimizer
product: journey optimizer
title: Assistente AI per le espressioni Personalization
description: Scopri come utilizzare l’Assistente AI in Journey Optimizer per generare espressioni di personalizzazione dal linguaggio naturale, dall’Editor Personalization o in linea nel Designer e-mail.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
mini-toc-levels: 1
source-git-commit: 8a905fd7e51c2dac60f4edccb9e9dd790a0dd424
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 1%

---

# Assistente AI per le espressioni di personalizzazione{#generative-personalization-expressions}

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare questa funzionalità, leggi l’articolo sui relativi [Guardrail e limitazioni](gs-generative.md#generative-guardrails).
></br>
>
>Prima di poter utilizzare l&#39;Assistente di intelligenza artificiale in Journey Optimizer, devi accettare un [contratto utente](https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

## Panoramica {#where-available}

[!UICONTROL Assistente AI] consente di generare nuove personalizzazioni dal linguaggio semplice, spiegare le funzioni delle espressioni esistenti e risolvere i problemi nel codice selezionato, in modo da dedicare meno tempo alla sintassi e all&#39;individuazione manuale dei campi. Puoi anche eseguire iterazioni su una selezione o chiedere altre modifiche nella conversazione. È disponibile da due punti di ingresso:

* **[!UICONTROL Editor di Personalization]** - ovunque sia disponibile l&#39;editor (oggetto, corpo e altri campi che lo aprono). Per sapere dove e come aprire l&#39;editor, consulta [Aggiungi personalizzazione](../personalization/personalization-build-expressions.md#where).
* **Modifica del testo in linea di Designer tramite e-mail** direttamente dal popover di modifica in linea durante la modifica di un componente testo. Vedi [Genera da e-mail Designer](#generate-email-designer).

Per una configurazione e lingue più ampie dell&#39;Assistente di intelligenza artificiale, vedere [Introduzione all&#39;Assistente di intelligenza artificiale](gs-generative.md). Per i concetti di personalizzazione, consulta [Introduzione alla personalizzazione](../personalization/personalize.md). Per suggerimenti, vedere [Best practice per la richiesta di IA](ai-assistant-prompting-guide.md).

A seconda del contesto della campagna o del percorso, l&#39;assistente può lavorare con i dati e costruisce l&#39;[!UICONTROL Editor Personalization] già esposto, ad esempio attributi di profilo, appartenenza ai segmenti, funzioni di assistenza e origini di personalizzazione correlate.

>[!NOTE]
>
>L&#39;assistente mantiene il contesto dalle richieste solo mentre [!UICONTROL Assistente IA] rimane aperto nella sessione. Se si chiude l&#39;assistente o l&#39;editor, la conversazione verrà annullata. Alla successiva apertura dell&#39;assistente, verrà avviata una nuova conversazione.

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

## Genera da E-mail Designer {#generate-email-designer}

[!UICONTROL L&#39;Assistente AI per le espressioni di personalizzazione] è disponibile anche direttamente dall&#39;esperienza di modifica in linea in E-mail Designer, senza aprire l&#39;[!UICONTROL Editor Personalization] completo. L’espressione generata viene inserita nella posizione del cursore nel componente testo.

1. In E-mail Designer, seleziona un componente di testo e inizia a modificarlo in linea.

1. Apri il popover di personalizzazione in linea in uno dei due modi seguenti:

   * Digitare `{{` nella posizione in cui si desidera inserire l&#39;espressione. Il popover si apre automaticamente.
   * Fare clic su **[!UICONTROL Utilizza IA per generare]** nel popover di modifica in linea, se è già aperto.

   ![](assets/ai-perso-email-entry.png)

1. Nel campo di testo, descrivi l&#39;espressione di personalizzazione desiderata in linguaggio semplice, quindi fai clic su **[!UICONTROL Genera]**.

1. Controlla il risultato nella scheda **[!UICONTROL Espressione]** per visualizzare l&#39;espressione generata.

   Passa alla scheda **[!UICONTROL Anteprima]** per vedere come l&#39;espressione viene valutata utilizzando valori di profilo di esempio, in modo da poter verificare l&#39;output prima di inserirlo.

   ![](assets/ai-perso-email-result.png)

1. Fare clic su **[!UICONTROL Inserisci]** per applicare l&#39;espressione in corrispondenza della posizione del cursore nel componente testo. Utilizza **[!UICONTROL Rigenera]** per produrre un nuovo suggerimento o **[!UICONTROL Reimposta]** per ricominciare.

>[!NOTE]
>
>La sessione [!UICONTROL Assistente AI per le espressioni di personalizzazione] nel popopover Inline Email Designer è indipendente dalle sessioni in [!UICONTROL Personalization Editor]. La chiusura del popover cancella la conversazione.
