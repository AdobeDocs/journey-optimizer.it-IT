---
solution: Journey Optimizer
product: journey optimizer
title: Generazione di SMS con l’assistente IA
description: Inizia a generare contenuti SMS con l’Assistente AI
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 5fd1cc3a-c023-4e8e-bfac-9a86bd33bbb3
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 15%

---

# Generazione di SMS con l’assistente IA {#generative-sms}

>[!BEGINSHADEBOX]

**Sommario**

* [Introduzione all’assistente IA](gs-generative.md)
* [Generazione di e-mail con l’assistente IA](generative-email.md)
* Generazione di SMS con l’assistente IA
* [Generazione di push con l’assistente IA](generative-push.md)
* [Esperimento contenuti con l’assistente IA](generative-experimentation.md)

>[!ENDSHADEBOX]

Dopo aver creato e personalizzato i messaggi SMS in base alle preferenze del pubblico, eleva la comunicazione con l’Assistente AI in Journey Optimizer.

Questa risorsa offre consigli dettagliati per ottimizzare i contenuti, aiutando la riproduzione dei messaggi e massimizzando il coinvolgimento.

Esplora le schede seguenti per scoprire come utilizzare l’Assistente IA in Journey Optimizer.

>[!NOTE]
>
>Prima di iniziare a utilizzare questa funzionalità, leggi l’articolo sui relativi [Guardrail e limitazioni](gs-generative.md#generative-guardrails).

>[!BEGINTABS]

>[!TAB Generazione SMS completa]

1. Dopo aver creato e configurato la tua campagna SMS, fai clic su **[!UICONTROL Modifica contenuto]**.

   Per ulteriori informazioni su come configurare la campagna SMS, consulta [questa pagina](../sms/create-sms.md).

1. Compila i **[!UICONTROL Dettagli di base]** per la tua campagna. Al termine, fai clic su **[!UICONTROL Modifica contenuto]**.

1. Personalizza il messaggio SMS in base alle esigenze. [Ulteriori informazioni](../sms/create-sms.md)

1. Accedere al menu **[!UICONTROL Mostra Assistente AI]**.

   ![](assets/sms-genai-1.png){zoomable="yes"}

1. Abilita l&#39;opzione **[!UICONTROL Usa contenuto originale]** affinché l&#39;Assistente AI personalizzi nuovi contenuti in base al contenuto della campagna, al nome e al pubblico selezionato.

   La richiesta deve essere sempre associata a un contesto specifico.

1. Ottimizzare il contenuto descrivendo cosa si desidera generare nel campo **[!UICONTROL Prompt]**.

   Se stai cercando assistenza per creare il prompt, accedi alla **[!UICONTROL Libreria prompt]** che fornisce una vasta gamma di idee per migliorare le campagne.

   ![](assets/sms-genai-2.png){zoomable="yes"}

1. Seleziona **[!UICONTROL Carica risorsa marchio]** per aggiungere qualsiasi risorsa marchio contenente contenuto che possa fornire ulteriore contesto all&#39;Assistente IA.

1. Personalizza il prompt con le diverse opzioni:

   * **[!UICONTROL Strategia di comunicazione]**: selezionare l&#39;approccio di comunicazione desiderato per il testo generato.
   * **[!UICONTROL Lingua]**: scegli la lingua per il contenuto della variante.
   * **[!UICONTROL Tono]**: verifica che il testo sia appropriato per il pubblico e lo scopo.
   * **[!UICONTROL Lunghezza]**: seleziona la lunghezza del contenuto utilizzando il cursore di intervallo.

   ![](assets/sms-genai-3.png){zoomable="yes"}

1. Una volta completato il prompt, fai clic su **[!UICONTROL Genera]**.

1. Sfoglia le **[!UICONTROL Varianti]** generate e fai clic su **[!UICONTROL Anteprima]** per visualizzare una versione a schermo intero della variante selezionata.

1. Passa all&#39;opzione **[!UICONTROL Perfeziona]** nella finestra **[!UICONTROL Anteprima]** per accedere ad altre funzioni di personalizzazione e perfezionare la variante in base alle tue preferenze:

   * **[!UICONTROL Utilizza come contenuto di riferimento]**: la variante scelta fungerà da contenuto di riferimento per generare altri risultati.

   * **[!UICONTROL Riformula]**: l&#39;Assistente AI può riformulare il messaggio in diversi modi, mantenendo la scrittura fresca e coinvolgente per diversi tipi di pubblico.

   * **[!UICONTROL Usa un linguaggio più semplice]**: sfrutta l&#39;Assistente AI per semplificare la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

   ![](assets/sms-genai-4.png){zoomable="yes"}

1. Una volta trovato il contenuto appropriato, fai clic su **[!UICONTROL Seleziona]**.

   Puoi anche abilitare l’esperimento per il contenuto. [Ulteriori informazioni](generative-experimentation.md)

1. Inserisci campi di personalizzazione per personalizzare il contenuto SMS in base ai dati dei profili. [Ulteriori informazioni sulla personalizzazione dei contenuti](../personalization/personalize.md)

1. Dopo aver definito il contenuto del messaggio, fai clic sul pulsante **[!UICONTROL Simula contenuto]** per controllare il rendering e verifica le impostazioni di personalizzazione con i profili di test. [Ulteriori informazioni](../personalization/personalize.md)

Una volta definiti il contenuto, il pubblico e la pianificazione, sei pronto per preparare la tua campagna SMS. [Ulteriori informazioni](../campaigns/review-activate-campaign.md)

>[!TAB Generazione testo]

1. Dopo aver creato e configurato la tua campagna SMS, fai clic su **[!UICONTROL Modifica contenuto]**.

   Per ulteriori informazioni su come configurare la campagna SMS, consulta [questa pagina](../sms/create-sms.md).

1. Compila i **[!UICONTROL Dettagli di base]** per la tua campagna. Al termine, fai clic su **[!UICONTROL Modifica contenuto]**.

1. Personalizza il messaggio SMS in base alle esigenze. [Ulteriori informazioni](../sms/create-sms.md)

1. Accedi al menu **[!UICONTROL Modifica testo con Assistente AI]** accanto al campo **[!UICONTROL Messaggio]**.

   ![](assets/sms-text-genai-1.png){zoomable="yes"}

1. Abilita l&#39;opzione **[!UICONTROL Usa contenuto di riferimento]** per l&#39;Assistente AI per personalizzare nuovi contenuti in base al contenuto della campagna, al nome e al pubblico selezionato.

   La richiesta deve essere sempre associata a un contesto specifico.

1. Ottimizzare il contenuto descrivendo cosa si desidera generare nel campo **[!UICONTROL Prompt]**.

   Se stai cercando assistenza per creare il prompt, accedi alla **[!UICONTROL Libreria prompt]** che fornisce una vasta gamma di idee per migliorare le campagne.

   ![](assets/sms-text-genai-1.png){zoomable="yes"}

1. Seleziona **[!UICONTROL Carica risorsa marchio]** per aggiungere qualsiasi risorsa marchio contenente contenuto che possa fornire ulteriore contesto all&#39;Assistente IA.

1. Personalizza il prompt con le diverse opzioni:

   * **[!UICONTROL Strategia di comunicazione]**: selezionare l&#39;approccio di comunicazione desiderato per il testo generato.
   * **[!UICONTROL Lingua]**: scegli la lingua per il contenuto della variante.
   * **[!UICONTROL Tono]**: verifica che il testo sia appropriato per il pubblico e lo scopo.
   * **[!UICONTROL Lunghezza]**: seleziona la lunghezza del contenuto utilizzando il cursore di intervallo.

   ![](assets/sms-text-genai-3.png){zoomable="yes"}

1. Una volta completato il prompt, fai clic su **[!UICONTROL Genera]**.

1. Sfoglia le **[!UICONTROL Varianti]** generate e fai clic su **[!UICONTROL Anteprima]** per visualizzare una versione a schermo intero della variante selezionata.

1. Passa all&#39;opzione **[!UICONTROL Perfeziona]** nella finestra **[!UICONTROL Anteprima]** per accedere ad altre funzioni di personalizzazione e perfezionare la variante in base alle tue preferenze:

   * **[!UICONTROL Utilizza come contenuto di riferimento]**: la variante scelta fungerà da contenuto di riferimento per generare altri risultati.

   * **[!UICONTROL Riformula]**: l&#39;Assistente AI può riformulare il messaggio in diversi modi, mantenendo la scrittura fresca e coinvolgente per diversi tipi di pubblico.

   * **[!UICONTROL Usa un linguaggio più semplice]**: sfrutta l&#39;Assistente AI per semplificare la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

   ![](assets/sms-text-genai-4.png){zoomable="yes"}

1. Una volta trovato il contenuto appropriato, fai clic su **[!UICONTROL Seleziona]**.

   Puoi anche abilitare l’esperimento per il contenuto. [Ulteriori informazioni](generative-experimentation.md)

1. Inserisci campi di personalizzazione per personalizzare il contenuto SMS in base ai dati dei profili. [Ulteriori informazioni sulla personalizzazione dei contenuti](../personalization/personalize.md)

1. Dopo aver definito il contenuto del messaggio, fai clic sul pulsante **[!UICONTROL Simula contenuto]** per controllare il rendering e controlla le impostazioni di personalizzazione con i profili di test.

Una volta definiti il contenuto, il pubblico e la pianificazione, sei pronto per preparare la tua campagna SMS. [Ulteriori informazioni](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
