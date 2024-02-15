---
solution: Journey Optimizer
product: journey optimizer
title: Caso d'uso di personalizzazione&due punti; notifica stato ordine
description: Scopri come personalizzare un messaggio con informazioni su profilo, decisione di offerta e contesto.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, caso d’uso, personalizzazione
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: 1deb04490e53cbd5d67abda229bb4f850055510f
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 3%

---

# Caso di utilizzo di personalizzazione: notifica dello stato dell’ordine {#personalization-use-case}

In questo caso d’uso, vedrai come utilizzare più tipi di personalizzazione in un singolo messaggio di notifica push. Verranno utilizzati tre tipi di personalizzazione:

* **Profilo**: personalizzazione dei messaggi basata su un campo del profilo
* **Decisione sull’offerta**: personalizzazione basata su variabili di gestione delle decisioni
* **Contesto**: personalizzazione basata su dati contestuali provenienti dal percorso

L’obiettivo di questo esempio è quello di inviare un evento a [!DNL Journey Optimizer] ogni volta che un ordine cliente viene aggiornato. Viene quindi inviata al cliente una notifica push con informazioni sull’ordine e un’offerta personalizzata.

Per questo caso d’uso, sono necessari i seguenti prerequisiti:

* configura un evento dell’ordine con il numero, lo stato e il nome dell’articolo. Consulta questa [sezione](../event/about-events.md).
* crea una decisione, fai riferimento a questo [sezione](../offers/offer-activities/create-offer-activities.md).

➡️ [Scopri un caso d’uso simile nel video](#video)

## Passaggio 1: creare il percorso {#create-journey}

1. Fai clic su **[!UICONTROL Percorsi]** e creare un nuovo percorso.

   ![](assets/perso-uc4.png)

1. Aggiungi l’evento di ingresso e un **Push** attività azione.

   ![](assets/perso-uc5.png)

1. Configura e progetta il messaggio di notifica push. Consulta questa [sezione](../push/create-push.md).

## Passaggio 2: aggiungere la personalizzazione al profilo {#add-perso}

1. In **Push** attività, fai clic su **Modifica contenuto**.

1. Fai clic su **Titolo** campo.

   ![](assets/perso-uc2.png)

1. Inserisci l’oggetto e aggiungi la personalizzazione del profilo. Utilizza la barra di ricerca per trovare il campo del nome del profilo. Nel testo dell’oggetto, posiziona il cursore nel punto in cui desideri inserire il campo di personalizzazione e fai clic sul pulsante **+** icona. Fai clic su **Salva**.

   ![](assets/perso-uc3.png)

## Passaggio 3: aggiungere la personalizzazione ai dati contestuali {#add-perso-contextual-data}

1. In **Push** attività, fai clic su **Modifica contenuto** e fai clic su **Titolo** campo.

   ![](assets/perso-uc9.png)

1. Seleziona la **Attributi contestuali** menu. Gli attributi contestuali sono disponibili solo se un percorso ha trasmesso dati contestuali al messaggio. Clic **Journey Orchestration**. Vengono visualizzate le seguenti informazioni contestuali:

   * **Eventi**: questa categoria raggruppa tutti i campi degli eventi inseriti prima dell’attività di azione del canale nel percorso.
   * **Proprietà percorso**: i campi tecnici relativi al percorso per un determinato profilo, ad esempio l’ID percorso o gli errori specifici rilevati. Ulteriori informazioni in [Documentazione del Journey Orchestration](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Espandi **Eventi** e cercare il campo relativo al numero d&#39;ordine relativo all&#39;evento. È inoltre possibile utilizzare la casella di ricerca. Fai clic su **+** per inserire il campo di personalizzazione nel testo dell’oggetto. Fai clic su **Salva**.

   ![](assets/perso-uc11.png)

1. Ora fai clic su **Corpo** campo.

   ![](assets/perso-uc12.png)

1. Digita il messaggio e inserisci, dalla **[!UICONTROL Attributi contestuali]** il nome della voce dell&#39;ordine e l&#39;avanzamento dell&#39;ordine.

   ![](assets/perso-uc13.png)

1. Dal menu a sinistra, seleziona **Decisioni di offerta** per inserire una variabile di decisione. Seleziona il posizionamento e fai clic su **+** accanto alla decisione di aggiungerla al corpo.

   ![](assets/perso-uc14.png)

1. Fai clic su Convalida per verificare che non siano presenti errori, quindi fai clic su **Salva**.

   ![](assets/perso-uc15.png)

## Passaggio 4: testare e pubblicare il percorso {#test-publish}

1. Fai clic su **Test** , quindi fare clic su **Attivare un evento**.

   ![](assets/perso-uc17.png)

1. Immettere i diversi valori da passare nel test. La modalità di test funziona solo con i profili di test. L’identificatore del profilo deve corrispondere a un profilo di test. Fai clic su **Invia**.

   ![](assets/perso-uc18.png)

   La notifica push viene inviata e visualizzata sul telefono cellulare del profilo di test.

   ![](assets/perso-uc19.png)

1. Verifica che non vi sia alcun errore e pubblica il percorso.

## Video introduttivo {#video}

Il video seguente mostra un caso d’uso simile, sfruttando i dati contestuali provenienti da un percorso per personalizzare un’e-mail.

>[!VIDEO](https://video.tv.adobe.com/v/3425027?quality=12)
