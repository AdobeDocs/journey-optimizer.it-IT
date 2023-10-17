---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare i componenti di contenuto di e-mail designer
description: Scopri come utilizzare i componenti per contenuti nelle tue e-mail
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: componenti, e-mail designer, editor, e-mail
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 58%

---

# Utilizzare i componenti di contenuto di E-mail Designer {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti per contenuti sono dei segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di un’e-mail."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti per contenuti sono dei segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di una pagina di destinazione."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti per contenuti sono dei segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di un frammento."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti per contenuti sono dei segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di un modello."

Durante la creazione di contenuti e-mail, **[!UICONTROL Componenti contenuto]** consente di personalizzare ulteriormente l’e-mail con componenti non elaborati che possono essere modificati una volta inseriti in un messaggio e-mail.

Puoi aggiungere tutti i componenti di contenuto necessari all’interno di uno o più componenti struttura, che definiscono il layout dell’e-mail.

## Aggiungere componenti per contenuti {#add-content-components}

Per aggiungere componenti per contenuti all’e-mail e modificarli in base alle tue esigenze, segui la procedura seguente.

1. In E-mail Designer, utilizza un contenuto esistente oppure trascina i **[!UICONTROL componenti struttura]** desiderati nel contenuto vuoto per definire il layout dell’e-mail. [Scopri come](content-from-scratch.md)

1. Per accedere alla sezione **[!UICONTROL Componenti contenuto]**, seleziona il pulsante corrispondente dal riquadro a sinistra di E-mail Designer.

   ![](assets/email_designer_content_components.png)

1. Trascina i componenti per contenuti desiderati all’interno dei componenti struttura pertinenti.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >È possibile aggiungere più componenti in un singolo componente struttura e in ogni colonna di un componente struttura.

1. Regola gli attributi e lo stile di ciascun componente utilizzando **[!UICONTROL Impostazioni]** e **[!UICONTROL Stile]** schede a destra. Ad esempio, puoi modificare lo stile del testo, la spaziatura o il margine di ciascun componente. [Ulteriori informazioni su allineamento e spaziatura](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

1. Dal menu avanzato del **[!UICONTROL Componente contenuto]**, puoi eliminare o duplicare facilmente qualsiasi componente di contenuto in base alle esigenze.

   ![](assets/email_designer_content_components_settings_2.png)

## Contenitore {#container}

Per applicare uno stile specifico a un gruppo di componenti di contenuto, puoi aggiungere una **[!UICONTROL Contenitore]** e quindi aggiungervi i componenti di contenuto desiderati. Questo consente di applicare uno stile distinto al contenitore, che sarà diverso dallo stile applicato ai componenti di contenuto all’interno.

Ad esempio, aggiungi un componente **[!UICONTROL Contenitore]** e quindi un componente [Pulsante](#button) all’interno del contenitore. Puoi utilizzare uno sfondo specifico per il contenitore e un altro per il pulsante.

![](assets/email_designer_container_component.png)

## Pulsante {#button}

Utilizza il componente **[!UICONTROL Pulsante]** per inserire uno o più pulsanti nell’e-mail e reindirizzare il pubblico dell’e-mail a un’altra pagina.

1. Da **[!UICONTROL Componenti contenuto]**, trascina il componente **[!UICONTROL Pulsante]** in un **[!UICONTROL Componente struttura]**.

1. Fai clic sul pulsante appena aggiunto per personalizzare il testo e accedere al **[!UICONTROL Impostazioni]** e **[!UICONTROL Stili]** schede nel riquadro a destra di E-mail Designer.

   ![](assets/email_designer_button_component.png)

1. Dalla sezione **[!UICONTROL Collegamento]** , aggiungi l&#39;URL a cui desideri reindirizzare quando fai clic sul pulsante.

1. Scegli come il pubblico verrà reindirizzato con **[!UICONTROL Target]** elenco a discesa:

   * **[!UICONTROL Nessuno]**: il collegamento viene aperto nello stesso frame in cui è stato fatto clic (impostazione predefinita).
   * **[!UICONTROL Vuoto]**: il collegamento viene aperto in una nuova finestra o scheda.
   * **[!UICONTROL Stesso]**: il collegamento viene aperto nello stesso frame in cui è stato fatto clic.
   * **[!UICONTROL Principale]**: il collegamento viene aperto nel frame principale.
   * **[!UICONTROL Superiore]**: il collegamento viene aperto nel corpo completo della finestra.

   ![](assets/email_designer_button_link.png)

1. Puoi personalizzare ulteriormente il pulsante modificando gli attributi di stile, ad esempio **[!UICONTROL Bordo]**, **[!UICONTROL Dimensione]**, **[!UICONTROL Margine]**, ecc. dal riquadro **[!UICONTROL Impostazioni componenti]**.

## Testo {#text}

Utilizza il componente **[!UICONTROL Testo]** per inserire testo nell’e-mail e regolarne lo stile (bordo, dimensione, spaziatura, ecc.) utilizzando la scheda **[!UICONTROL Stili]**.

![](assets/email_designer_text_component.png)

1. Da **[!UICONTROL Componenti contenuto]**, trascina e rilascia la **[!UICONTROL Testo]** componente in una **[!UICONTROL Componente struttura]**.

1. Fai clic sul componente appena aggiunto per personalizzare il testo e accedere al **[!UICONTROL Impostazioni]** e **[!UICONTROL Stili]** schede nel riquadro a destra di E-mail Designer.

1. Modifica il testo con le seguenti opzioni disponibili nella barra degli strumenti:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Modifica stile di testo]**: applica al testo lo stile grassetto, corsivo, sottolineato o barrato.
   * **Modifica l’allineamento**: applica al testo l’allineamento a sinistra, a destra, centrato o giustificato.
   * **[!UICONTROL Crea elenco]**: aggiungi al testo un elenco puntato o numerato.
   * **[!UICONTROL Imposta il titolo]**: aggiungi al testo fino a sei livelli di titolo.
   * **Dimensione font**: seleziona la dimensione del font in pixel.
   * **[!UICONTROL Cambia il colore del carattere]**: scegli il colore del carattere.
   * **[!UICONTROL Inserisci collegamento]**: aggiungi qualsiasi tipo di collegamento al contenuto.
   * **[!UICONTROL Modifica immagine]**: aggiungi un’immagine o una risorsa al componente testo. [Ulteriori informazioni sulla gestione delle risorse](../content-management/assets-essentials.md)
   * **[!UICONTROL Cambia il colore del carattere]**: scegli il colore del carattere.
   * **[!UICONTROL Aggiungi personalizzazione]**: aggiungi campi di personalizzazione per personalizzare il contenuto in base ai dati dei profili. [Ulteriori informazioni sulla personalizzazione dei contenuti](../personalization/personalize.md)
   * **[!UICONTROL Mostra il codice sorgente]**: visualizza il codice sorgente del testo. Non può essere modificato.
   * **[!UICONTROL Abilita contenuto condizionale]**: aggiungi contenuto condizionale per adattare il contenuto del componente ai profili target. [Ulteriori informazioni sui contenuti dinamici](../personalization/get-started-dynamic-content.md)
   * **[!UICONTROL Duplica]**: aggiungi una copia del componente di testo.
   * **[!UICONTROL Elimina]**: elimina dal messaggio e-mail il componente di testo selezionato.

1. Regola gli altri attributi di stile quali colore del testo, famiglia di font, bordo, spaziatura, margine, ecc. dalla scheda **[!UICONTROL Stili]**.

   ![](assets/email_designer_text_component_2.png)

## Divisore {#divider}

Utilizza il componente **[!UICONTROL Divisore]** per inserire una linea di divisione utile per organizzare il layout e il contenuto dell’e-mail.

È possibile regolare gli attributi di stile, ad esempio il colore, lo stile e lo spessore della linea, dalle schede **[!UICONTROL Impostazioni]** e **[!UICONTROL Stili]**.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Utilizza il componente **[!UICONTROL HTML]** per copiare e incollare le diverse parti di un codice HTML esistente. Questo consente di creare componenti modulari HTML a forma libera in modo da riutilizzare dei contenuti esterni.

1. Da **[!UICONTROL Componenti contenuto]**, trascina il componente **[!UICONTROL HTML]** in un **[!UICONTROL componente struttura]**.

1. Fai clic sul componente appena aggiunto, quindi seleziona **[!UICONTROL Mostra il codice sorgente]** dalla barra degli strumenti contestuale per aggiungere il codice HTML.

   ![](assets/email_designer_html_component.png)

1. Copia e incolla il codice HTML che desideri aggiungere all’e-mail e fai clic su **[!UICONTROL Salva]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Per rendere semplicemente un contenuto esterno conforme a E-mail Designer, Adobe consiglia di creare un messaggio da zero e di copiare il contenuto dell’e-mail esistente nei componenti.

## Immagine {#image}

Utilizza il **[!UICONTROL Immagine]** per inserire un file immagine dal computer nel contenuto dell’e-mail.

1. Da **[!UICONTROL Componenti contenuto]**, trascina e rilascia la **[!UICONTROL Immagine]** componente in una **[!UICONTROL Componente struttura]**.

   ![](assets/email_designer_image_content.png)

1. Fai clic su **[!UICONTROL Sfoglia]** per scegliere un file di immagine dalle risorse.

   Per ulteriori informazioni su [!DNL Assets Essentials], fare riferimento a [Documentazione di Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. Fai clic sul componente appena aggiunto e imposta le proprietà dell’immagine da **[!UICONTROL Impostazioni]** scheda:

   * **[!UICONTROL Titolo immagine]** consente di definire il titolo da assegnare all’immagine.
   * **[!UICONTROL Testo Alt]** consente di definire la didascalia collegata all’immagine. Questo corrisponde all’attributo HTML “alt”.

   ![](assets/email_designer_10.png)

1. Puoi anche scegliere di **[!UICONTROL Trova foto Stock simili]**. [Ulteriori informazioni](../content-management/stock.md)

1. Dalla sezione **[!UICONTROL Stili]** , regolare gli altri attributi di stile come margine, bordo e così via. oppure aggiungendo un collegamento per reindirizzare il pubblico a un altro contenuto, dal riquadro **[!UICONTROL Impostazioni componenti]**.

## Social {#social}

Utilizza il componente **[!UICONTROL Social]** per inserire nel contenuto dell’e-mail dei collegamenti a pagine social media.

1. Da **[!UICONTROL Componenti contenuto]**, trascina il componente **[!UICONTROL Social]** in un **[!UICONTROL componente struttura]**.

1. Seleziona il componente appena aggiunto.

1. Nel campo **[!UICONTROL Social]** della scheda **[!UICONTROL Impostazioni]**, scegli i social media da aggiungere o rimuovere.

   ![](assets/email_designer_20.png)

1. Scegli le dimensioni delle icone nel campo dedicato.

1. Fai clic su ciascuna icona dei social media per configurare il **[!UICONTROL URL]** al quale verrà reindirizzato il pubblico.

   ![](assets/email_designer_21.png)

1. Se necessario, puoi anche modificare le icone di ciascuno dei social media dalle risorse.

1. Regola gli altri attributi quali stile, margine, bordo, ecc. dalla scheda **[!UICONTROL Stili]**.

## Decisione sull’offerta {#offer-decision}

Utilizza il **[!UICONTROL Decisione sull’offerta]** per inserire offerte nei messaggi. Il [gestione delle decisioni](../offers/get-started/starting-offer-decisioning.md) Il motore sceglierà l’offerta migliore da consegnare ai clienti.

1. Da **[!UICONTROL Componenti contenuto]**, trascina e rilascia la **[!UICONTROL Decisione sull’offerta]** componente in una **[!UICONTROL Componente struttura]**.

1. Clic **[!UICONTROL Aggiungi]** per selezionare **[!UICONTROL Decisione sull’offerta]**.

   ![](assets/component_offers.png)

1. Dall’elenco a discesa, seleziona la tua **[!UICONTROL Posizionamenti]**.  Quindi, seleziona la **[!UICONTROL Decisione sull’offerta]** desideri aggiungere al contenuto e fai clic su **[!UICONTROL Aggiungi]**.

   ![](assets/component_offers_2.png)

1. Dalla sezione **[!UICONTROL Decisione sull’offerta]** , puoi visualizzare in anteprima o modificare l’offerta inserita.

Scopri come aggiungere offerte personalizzate in un messaggio e-mail in [questa sezione](add-offers-email.md).

>[!IMPORTANT]
>
>Se vengono apportate modifiche a una decisione di offerta utilizzata in un messaggio di un percorso, devi annullare la pubblicazione del percorso e ripubblicarlo.  In questo modo le modifiche verranno incorporate nel messaggio del percorso e il messaggio sarà coerente con gli ultimi aggiornamenti.
