---
title: Utilizzare i componenti di contenuto di e-mail designer
description: Scopri come utilizzare i componenti di contenuto nelle e-mail
feature: Panoramica
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 2%

---

# Utilizzare i componenti contenuto di E-mail designer {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="Informazioni sui componenti Contenuto"
>abstract="I componenti contenuto sono segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di un’e-mail."

![](assets/do-not-localize/badge.png)

Quando crei il contenuto dell’e-mail da zero, **[!UICONTROL Content components]** ti consente di personalizzare ulteriormente l’e-mail con componenti vuoti e non elaborati che puoi utilizzare una volta inseriti in un messaggio e-mail.
Puoi aggiungere tutte le **[!UICONTROL Content components]** necessarie all’interno di un **[!UICONTROL Structure component]** che definisce il layout del messaggio e-mail.

## Pulsante {#buttons}

Utilizza il componente **[!UICONTROL Button]** per inserire più pulsanti nell’e-mail e reindirizzare il pubblico dell’e-mail a un’altra pagina.

1. Da **[!UICONTROL Content components]**, trascina **[!UICONTROL Button]** in un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_13.png)

1. Fai clic sul pulsante appena aggiunto per personalizzare il testo e accedere al **[!UICONTROL Components Settings]** nel riquadro a destra del designer dell’e-mail.

   ![](assets/email_designer_14.png)

1. Nel campo **[!UICONTROL Link]** di **[!UICONTROL Components Settings]** , aggiungi l’URL a cui desideri reindirizzare il pubblico quando fai clic sul pulsante .

1. Scegli come verrà reindirizzato il pubblico con il menu a discesa **[!UICONTROL Target]** :

   * **[!UICONTROL None]**: apre il collegamento nello stesso frame in cui è stato fatto clic (impostazione predefinita).
   * **[!UICONTROL Blank]**: apre il collegamento in una nuova finestra o scheda.
   * **[!UICONTROL Self]**: apre il collegamento nello stesso frame in cui è stato fatto clic.
   * **[!UICONTROL Parent]**: apre il collegamento nel frame principale.
   * **[!UICONTROL Top]**: apre il collegamento nel corpo completo della finestra.

   ![](assets/email_designer_15.png)

1. Ora puoi personalizzare ulteriormente il pulsante modificando ad esempio **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]**.

## Testo {#text}

Utilizza il componente **[!UICONTROL Text]** per inserire testo nel messaggio e-mail. È possibile regolare il colore, lo stile e le dimensioni del testo in **[!UICONTROL Component Settings]**.

1. In **[!UICONTROL Content Components]**, trascina **[!UICONTROL Text]** in un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_11.png)

1. Fai clic sul componente appena aggiunto per personalizzare il testo e accedere al **[!UICONTROL Components Settings]** nel riquadro a destra di e-mail designer.

1. Modifica il testo con le seguenti opzioni disponibili nella barra degli strumenti:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**: applicare al testo in grassetto, corsivo, sottolineato o barrato.
   * **Modifica allineamento**: scegliere tra allineamento a sinistra, a destra, al centro o giustificato per il testo.
   * **[!UICONTROL Create list]**: aggiungere al testo un elenco puntato o un elenco di numeri.
   * **[!UICONTROL Set heading]**: aggiungi fino a sei livelli di intestazione al testo.
   * **Dimensione** font: selezionare la dimensione del font del testo in pixel.
   * **[!UICONTROL Edit image]**: aggiungi un’immagine o una risorsa al componente testo. [Ulteriori informazioni sulla gestione](assets-essentials.md) delle risorse.
   * **[!UICONTROL Show the source code]**: visualizza il codice sorgente del testo. Non può essere modificato.
   * **[!UICONTROL Duplicate]**: aggiungi una copia del componente testo.
   * **[!UICONTROL Delete]**: elimina il componente di testo selezionato dal messaggio e-mail.
   * **[!UICONTROL Add personalization]**: aggiungi campi di personalizzazione per personalizzare il contenuto dai dati dei profili. [Ulteriori informazioni sulla personalizzazione dei contenuti](personalization/personalize.md).

1. Per una migliore esperienza utente, puoi aggiungere campi di personalizzazione per rivolgerti al pubblico. Per ulteriori informazioni, consulta questa [sezione](personalization/personalize.md).

1. Regolare i valori **[!UICONTROL Text color]**, **[!UICONTROL Font family]** e **[!UICONTROL Size]** in **[!UICONTROL Components Settings]**.

   ![](assets/email_designer_12.png)

## Divider {#divider}

Utilizza il componente **[!UICONTROL Divider]** per inserire una linea di divisione per organizzare il layout e il contenuto dell’e-mail.
È possibile selezionare il colore, lo stile e le dimensioni della linea di interruzione in **[!UICONTROL Component Settings]**.

![](assets/email_designer_16.png)

## HTML {#HTML}

Utilizza **[!UICONTROL HTML]** per copiare e incollare le diverse parti del codice HTML esistente. Questo consente di creare componenti HTML modulari gratuiti.

Per rendere semplicemente un contenuto esterno conforme a E-mail Designer, Adobe consiglia di creare un messaggio da zero e di copiare il contenuto dell’e-mail esistente nei componenti.

1. In **[!UICONTROL Content Components]**, trascina **[!UICONTROL HTML]** in un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_22.png)

1. Fai clic sul componente appena aggiunto, quindi **[!UICONTROL Show the source code]** per aggiungere il codice HTML.

   ![](assets/email_designer_23.png)

1. Copia e incolla il codice HTML da aggiungere all&#39;e-mail e fai clic su **[!UICONTROL Save]**.

   ![](assets/email_designer_24.png)

1. Ora puoi personalizzare ulteriormente il codice HTML modificando ad esempio **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]** oppure aggiungendo un collegamento per reindirizzare il pubblico a un altro contenuto.

## Immagine {#image}

Utilizza il componente **[!UICONTROL Image]** per inserire un file immagine dal computer nell’e-mail.

1. In **[!UICONTROL Content Components]**, trascina **[!UICONTROL Image]** in un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_9.png)

1. Fare clic su **[!UICONTROL Browse]** per scegliere un file immagine dal computer.

   Puoi anche fare clic su **[!UICONTROL Asset Picker]** per aggiungere una risorsa all’e-mail. Per ulteriori informazioni sulle risorse, consulta questa [sezione](assets-essentials.md).

1. Fai clic sul componente appena aggiunto per iniziare a configurare il **[!UICONTROL Content Components]** e per accedere al **[!UICONTROL Components Settings]** nel riquadro a destra di e-mail designer.

1. Imposta le proprietà dell&#39;immagine:

   * **[!UICONTROL Image Title]** consente di definire un titolo per l’immagine.
   * **[!UICONTROL Alt text]** consente di definire la didascalia collegata all’immagine. Questo corrisponde all’attributo HTML alt.

   ![](assets/email_designer_10.png)

1. È ora possibile personalizzare ulteriormente l&#39;immagine modificando ad esempio **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]** oppure aggiungendo un collegamento per reindirizzare il pubblico a un altro contenuto.

## Video {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="Impostazioni video"
>abstract="Utilizza questo componente per inserire un video nel messaggio e-mail. I video non funzionano su tutti i client e-mail. È consigliabile impostare un’immagine di fallback."
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="Informazioni aggiuntive"

Utilizza il componente **[!UICONTROL Video]** per inserire un video nell’e-mail tramite un collegamento URL.

1. In **[!UICONTROL Content Components]**, trascina **[!UICONTROL Video]** in un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_17.png)

1. Fai clic sul componente appena aggiunto per iniziare a configurare il **[!UICONTROL Content Components]** e per accedere al **[!UICONTROL Components Settings]** nel riquadro a destra di e-mail designer.

1. Nel campo **[!UICONTROL Video link]** di **[!UICONTROL Components Settings]** , aggiungi l’URL del video.

   ![](assets/email_designer_18.png)

1. Puoi aggiungere un **[!UICONTROL Poster image]** al video per specificare un’immagine da visualizzare finché il pubblico non fa clic sul pulsante di riproduzione.

1. È ora possibile personalizzare ulteriormente l&#39;immagine modificando ad esempio **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]**.

## Social {#social}

Utilizza il componente **[!UICONTROL Social]** per inserire collegamenti alle pagine dei social media nel tuo messaggio e-mail.

1. In **[!UICONTROL Content Components]**, trascina **[!UICONTROL Social]** in un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_19.png)

1. Fai clic sul componente appena aggiunto per iniziare a configurare il **[!UICONTROL Content Components]** e per accedere al **[!UICONTROL Components Settings]** nel riquadro a destra di e-mail designer.

1. Nel campo **[!UICONTROL Social]** di **[!UICONTROL Components Settings]** , scegli quale social media desideri aggiungere o rimuovere.

   ![](assets/email_designer_20.png)

1. Scegli le dimensioni delle icone nel campo **[!UICONTROL Size of images]** .

1. Fai clic su ciascuna delle icone dei social media per configurare il **[!UICONTROL URL]** a cui verrà reindirizzato il pubblico.

   ![](assets/email_designer_21.png)

1. Se necessario, puoi anche modificare le icone di ciascuno dei tuoi social media nel campo **[!UICONTROL Image]** .

1. Ora puoi personalizzare ulteriormente le icone dei social media modificando i valori **[!UICONTROL Style]**, **[!UICONTROL Margin]** e **[!UICONTROL Border]**.

## Decisione offerta {#offer-decision}

Utilizza il componente **[!UICONTROL Offer decision]** per inserire nei messaggi le decisioni (precedentemente note come attività di offerta). Decisioni sfrutterà la Gestione delle decisioni per scegliere l&#39;offerta migliore da consegnare ai tuoi clienti.

Argomenti correlati:

* [Introduzione alla gestione delle decisioni](offers/get-started/starting-offer-decisioning.md).
* [Aggiungi offerte personalizzate ai messaggi](deliver-personalized-offers.md).

