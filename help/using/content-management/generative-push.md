---
solution: Journey Optimizer
product: journey optimizer
title: Generazione di push con l’assistente IA
description: Inizia a generare contenuti push con l’Assistente AI
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: a9f9d8af-c762-4038-8bbc-bbd519e0ef3a
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 13%

---

# Generazione di push con l’assistente IA {#generative-push}

>[!BEGINSHADEBOX]

**Sommario**

* [Introduzione all’assistente IA](gs-generative.md)
* [Generazione di e-mail con l’assistente IA](generative-email.md)
* [Generazione di SMS con l’assistente IA](generative-sms.md)
* Generazione di push con l’assistente IA
* [Esperimento contenuti con l’assistente IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Prima di iniziare a utilizzare questa funzionalità, leggi l’articolo sui relativi [Guardrail e limitazioni](gs-generative.md#generative-guardrails).

Dopo aver creato e personalizzato i messaggi, porta il contenuto delle notifiche push al livello successivo con l’Assistente AI in Adobe Journey Optimizer.

Esplora le schede seguenti per scoprire come utilizzare l’Assistente IA in Journey Optimizer.

>[!BEGINTABS]

>[!TAB Generazione push completa]

In questo esempio particolare, scopri come inviare una notifica push coinvolgente utilizzando l’Assistente AI.

Segui questi passaggi:

1. Dopo aver creato e configurato la campagna di notifica push, fai clic su **[!UICONTROL Modifica contenuto]**.

   Per ulteriori informazioni su come configurare la campagna di notifica push, consulta [questa pagina](../push/create-push.md).

1. Compila i **[!UICONTROL Dettagli di base]** per la tua campagna. Al termine, fai clic su **[!UICONTROL Modifica contenuto]**.

1. Personalizza la notifica push in base alle esigenze. [Ulteriori informazioni](../push/design-push.md)

1. Accedere al menu **[!UICONTROL Mostra Assistente AI]**.

   ![](assets/push-genai-full-1.png){zoomable="yes"}

1. Abilita l&#39;opzione **[!UICONTROL Usa contenuto originale]** affinché l&#39;Assistente AI personalizzi nuovi contenuti in base al contenuto della campagna, al nome e al pubblico selezionato.

   La richiesta deve essere sempre associata a un contesto specifico.

1. Ottimizzare il contenuto descrivendo cosa si desidera generare nel campo **[!UICONTROL Prompt]**.

   Se stai cercando assistenza per creare il prompt, accedi alla **[!UICONTROL Libreria prompt]** che fornisce una vasta gamma di idee per migliorare le campagne.

   ![](assets/push-genai-full-2.png){zoomable="yes"}

1. Seleziona **[!UICONTROL Carica risorsa marchio]** per aggiungere qualsiasi risorsa marchio contenente contenuto che possa fornire ulteriore contesto all&#39;Assistente IA.

1. Scegli il campo da generare: **[!UICONTROL Titolo]** e/o **[!UICONTROL Messaggio]**.

1. Personalizza il prompt con le diverse opzioni:

   * **[!UICONTROL Strategia di comunicazione]**: scegli lo stile di comunicazione più adatto al testo generato.
   * **[!UICONTROL Lingua]**: seleziona la lingua in cui desideri generare il contenuto.
   * **[!UICONTROL Tono]**: il tono dell&#39;e-mail dovrebbe risuonare con il pubblico. Che tu voglia essere informativo, giocoso o persuasivo, l’Assistente AI può adattare il messaggio di conseguenza.

   ![](assets/push-genai-full-3.png){zoomable="yes"}

1. Una volta completato il prompt, fai clic su **[!UICONTROL Genera]**.

1. Sfoglia le **[!UICONTROL Varianti]** generate e fai clic su **[!UICONTROL Anteprima]** per visualizzare una versione a schermo intero della variante selezionata.

1. Passa all&#39;opzione **[!UICONTROL Perfeziona]** nella finestra **[!UICONTROL Anteprima]** per accedere ad altre funzioni di personalizzazione:

   * **[!UICONTROL Utilizza come contenuto di riferimento]**: la variante scelta fungerà da contenuto di riferimento per generare altri risultati.

   * **[!UICONTROL Riformula]**: l&#39;Assistente di intelligenza artificiale può riformulare il messaggio in diversi modi, mantenendo la scrittura fresca e coinvolgente per diversi tipi di pubblico.

   * **[!UICONTROL Usa linguaggio semplice]**: sfrutta l&#39;Assistente AI per semplificare la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

   ![](assets/push-genai-full-4.png){zoomable="yes"}

1. Una volta trovato il contenuto appropriato, fai clic su **[!UICONTROL Seleziona]**.

   Puoi anche abilitare l’esperimento per il contenuto. [Ulteriori informazioni](generative-experimentation.md)

1. Inserisci campi di personalizzazione per personalizzare il contenuto delle e-mail in base ai dati dei profili. Quindi, fai clic sul pulsante **[!UICONTROL Simula contenuto]** per controllare il rendering e controlla le impostazioni di personalizzazione con i profili di test. [Ulteriori informazioni](../personalization/personalize.md)

Una volta definiti il contenuto, il pubblico e la pianificazione, sei pronto per preparare la tua campagna push. [Ulteriori informazioni](../campaigns/review-activate-campaign.md)

>[!TAB Generazione testo]

In questo particolare esempio, scopri come utilizzare l’Assistente IA per contenuti specifici. Segui questi passaggi:

1. Dopo aver creato e configurato la campagna di notifica push, fai clic su **[!UICONTROL Modifica contenuto]**.

   Per ulteriori informazioni su come configurare la campagna push, consulta [questa pagina](../push/create-push.md).

1. Compila i **[!UICONTROL Dettagli di base]** per la tua campagna. Al termine, fai clic su **[!UICONTROL Modifica contenuto]**.

1. Personalizza la notifica push in base alle esigenze. [Ulteriori informazioni](../push/design-push.md)

1. Accedi al menu **[!UICONTROL Mostra Assistente AI]** accanto ai tuoi campi **[!UICONTROL Titolo]** o **[!UICONTROL Messaggio]**.

   ![](assets/push-genai-1.png){zoomable="yes"}

1. Abilita l&#39;opzione **[!UICONTROL Usa contenuto di riferimento]** per l&#39;Assistente AI per personalizzare nuovi contenuti in base al contenuto della campagna, al nome e al pubblico selezionato.

   La richiesta deve essere sempre associata a un contesto specifico.

1. Ottimizzare il contenuto descrivendo cosa si desidera generare nel campo **[!UICONTROL Prompt]**.

   Se stai cercando assistenza per creare il prompt, accedi alla **[!UICONTROL Libreria prompt]** che fornisce una vasta gamma di idee per migliorare le campagne.

   ![](assets/push-genai-2.png){zoomable="yes"}

1. Seleziona **[!UICONTROL Carica risorsa marchio]** per aggiungere qualsiasi risorsa marchio contenente contenuto che possa fornire ulteriore contesto all&#39;Assistente IA.

   ![](assets/push-genai-3.png){zoomable="yes"}

1. Personalizza il prompt con le diverse opzioni:

   * **[!UICONTROL Strategia di comunicazione]**: scegli lo stile di comunicazione più adatto al testo generato.
   * **[!UICONTROL Lingua]**: seleziona la lingua in cui desideri generare il contenuto.
   * **[!UICONTROL Tono]**: il tono dell&#39;e-mail dovrebbe risuonare con il pubblico. Che tu voglia essere informativo, giocoso o persuasivo, l’Assistente AI può adattare il messaggio di conseguenza.
   * **[!UICONTROL Lunghezza]**: seleziona la lunghezza del contenuto utilizzando il cursore di intervallo.

   ![](assets/push-genai-4.png){zoomable="yes"}

1. Una volta completato il prompt, fai clic su **[!UICONTROL Genera]**.

1. Sfoglia le **[!UICONTROL Varianti]** generate e fai clic su **[!UICONTROL Anteprima]** per visualizzare una versione a schermo intero della variante selezionata.

1. Passa all&#39;opzione **[!UICONTROL Perfeziona]** nella finestra **[!UICONTROL Anteprima]** per accedere ad altre funzioni di personalizzazione:

   * **[!UICONTROL Utilizza come contenuto di riferimento]**: la variante scelta fungerà da contenuto di riferimento per generare altri risultati.

   * **[!UICONTROL Elaborare]**: l&#39;Assistente AI può aiutarti a espandere argomenti specifici, fornendo ulteriori dettagli per una migliore comprensione e coinvolgimento.

   * **[!UICONTROL Riepiloga]**: informazioni lunghe possono sovraccaricare i destinatari delle e-mail. Utilizza l’Assistente per l’intelligenza artificiale per condensare i punti chiave in riepiloghi chiari e concisi che catturino l’attenzione e li incoraggino a leggere ulteriormente.

   * **[!UICONTROL Riformula]**: l&#39;Assistente AI può riformulare il messaggio in diversi modi, mantenendo la scrittura fresca e coinvolgente per diversi tipi di pubblico.

   * **[!UICONTROL Usa un linguaggio più semplice]**: sfrutta l&#39;Assistente AI per semplificare la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

   ![](assets/push-genai-5.png){zoomable="yes"}

1. Una volta trovato il contenuto appropriato, fai clic su **[!UICONTROL Seleziona]**.

   Puoi anche abilitare l’esperimento per il contenuto. [Ulteriori informazioni](generative-experimentation.md)

1. Inserisci campi di personalizzazione per personalizzare il contenuto delle e-mail in base ai dati dei profili. Quindi, fai clic sul pulsante **[!UICONTROL Simula contenuto]** per controllare il rendering e controlla le impostazioni di personalizzazione con i profili di test. [Ulteriori informazioni](../personalization/personalize.md)

Una volta definiti il contenuto, il pubblico e la pianificazione, sei pronto per preparare la tua campagna push. [Ulteriori informazioni](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
