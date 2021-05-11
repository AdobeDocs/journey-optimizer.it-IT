---
title: Importare o codificare le e-mail
description: Scopri come importare contenuti e-mail o codificare le e-mail
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 5%

---

# Importa o codifica il contenuto delle e-mail {#existing-content}

![](assets/do-not-localize/badge.png)

Journey Optimizer consente di importare contenuti HTML esistenti per progettare le e-mail. Questo contenuto può essere un codice HTML o contenuto non elaborato proveniente da un file HTML esistente o da una cartella zip.

Per codificare il contenuto HTML o importare il contenuto esistente, effettua le seguenti operazioni:

1. [Creare un messaggio](create-message.md)

1. Apri **[!UICONTROL Email Designer]** dalla sezione **[!UICONTROL Edit Content]** .

   ![](assets/import-html_1.png)

1. Seleziona **[!UICONTROL Code your own]** (Mostra origine dati) o **[!UICONTROL Import HTML]** (Blocca selezione). Per i passaggi successivi, fai riferimento alle sezioni seguenti.

## Codice personalizzato {#import-raw-html-code}

Utilizza la modalità **[!UICONTROL Code your own]** per importare codice HTML non elaborato e/o il contenuto dell’e-mail. Questo metodo richiede competenze HTML.

>[!CAUTION]
>
> Non è possibile fare riferimento alle immagini da [Adobe Experience Manager Assets Essentials](assets-essentials.md) quando si utilizza questo metodo. Le immagini a cui si fa riferimento nel codice HTML devono essere memorizzate in una posizione pubblica.

1. Nella home page di E-mail Designer, selezionare **[!UICONTROL Code your own]**.

   ![](assets/code-your-own.png)

1. Immetti o incolla il tuo codice HTML non elaborato.

1. Utilizza il riquadro a sinistra per sfruttare le funzionalità di personalizzazione [!DNL Journey Optimizer]. Per ulteriori informazioni al riguardo, consulta [questa sezione](personalization/personalize.md).

   ![](assets/code-editor.png)

1. Se desideri aprire E-mail Designer per avviare l’e-mail da una nuova progettazione, seleziona **[!UICONTROL Change your design]** dal menu delle opzioni.

   ![](assets/code-editor-change-design.png)

1. Fai clic sul pulsante **[!UICONTROL Preview]** per controllare la progettazione e la personalizzazione dei messaggi utilizzando i profili di test. Per ulteriori informazioni al riguardo, consulta [questa sezione](preview.md).

   ![](assets/code-editor-preview.png)

1. Quando il codice è pronto, fai clic su **[!UICONTROL Save]**, quindi torna alla schermata di creazione del messaggio per finalizzare il messaggio.

   ![](assets/code-editor-save.png)


## Importa HTML {#import-html-content-from-file}

È possibile importare contenuti HTML nella finestra di progettazione e-mail. Questo contenuto può essere:

* Un **file HTML** con un foglio di stile incorporato,
* Una cartella **.zip** con il file HTML, il foglio di stile (.css) e le immagini.

   >[!NOTE]
   >
   >Non ci sono vincoli alla struttura del file .zip. Tuttavia, i riferimenti devono essere relativi e adattati alla struttura ad albero della cartella .zip.

Per importare un file contenente contenuto HTML, effettua le seguenti operazioni:

1. Nella home page di E-mail Designer, selezionare **[!UICONTROL Import HTML]**.

   ![](assets/import-html_2.png)

1. Trascina e rilascia il file HTML o .zip contenente il contenuto HTML.

1. Una volta caricato il contenuto HTML, puoi sfruttare le funzionalità di E-mail Designer per modificare e visualizzare l’anteprima del messaggio e-mail. [Ulteriori informazioni in questa sezione](create-email-content.md).

   ![](assets/html-imported.png)
