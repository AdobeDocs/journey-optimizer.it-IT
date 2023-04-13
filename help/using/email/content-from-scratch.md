---
solution: Journey Optimizer
product: journey optimizer
title: Creare e-mail in Journey Optimizer
description: Scopri come creare contenuti e-mail da zero
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: contenuto, editor, e-mail, avvio
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 65%

---

# Inizia da zero {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Informazioni sui componenti struttura"
>abstract="I componenti struttura definiscono il layout del messaggio e-mail."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Informazioni sui componenti struttura"
>abstract="I componenti struttura definiscono il layout della pagina di destinazione."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Informazioni sui componenti struttura"
>abstract="I componenti struttura definiscono il layout del frammento."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Informazioni sui componenti struttura"
>abstract="I componenti struttura definiscono il layout del modello."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definizione delle colonne nell’e-mail"
>abstract="E-mail Designer consente di definire facilmente il layout dell’e-mail definendone la struttura a colonne."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definizione delle colonne nella pagina di destinazione"
>abstract="E-mail Designer consente di definire facilmente il layout della pagina di destinazione definendone la struttura a colonne."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definizione delle colonne in un frammento"
>abstract="E-mail Designer consente di definire facilmente il layout del frammento definendone la struttura a colonne."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definizione delle colonne nei modelli"
>abstract="E-mail Designer consente di definire facilmente il layout del modello definendone la struttura a colonne."


E-mail Designer consente di definire facilmente la struttura delle e-mail. Aggiungendo e spostando elementi strutturali con semplici azioni di trascinamento, puoi progettare la forma del messaggio e-mail in pochi secondi.

Per iniziare a creare il contenuto delle e-mail, segui i passaggi seguenti:

1. Dalla pagina home di E-mail Designer, seleziona l’opzione **[!UICONTROL Progetta da zero]**.

   ![](assets/email_designer.png)

1. Per iniziare a progettare il contenuto delle e-mail, trascina nell’area di lavoro i **[!UICONTROL componenti struttura]** necessari per definire il layout del messaggio e-mail.

   >[!NOTE]
   >
   >L’utilizzo di colonne sovrapposte non è compatibile con tutti i programmi e-mail. Se non è supportato, le colonne non verranno sovrapposte.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Aggiungi tutti i **[!UICONTROL componenti struttura]** necessari e modificane le impostazioni nel riquadro dedicato a destra.

   ![](assets/email_designer_structure_components.png)

   Seleziona il componente **[!UICONTROL Colonna n:n]** per definire il numero di colonne desiderato (tra 3 e 10). Per definire la larghezza di ogni colonna, sposta le frecce nella parte inferiore di ciascuna colonna.

   >[!NOTE]
   >
   >Le dimensioni di ogni colonna non possono essere inferiori al 10% della larghezza totale del componente struttura. Non è possibile rimuovere una colonna non vuota.

1. Da **[!UICONTROL Componenti contenuto]** aggiungi tutti gli elementi necessari in uno o più componenti struttura. [Ulteriori informazioni sui componenti contenuto](content-components.md)

1. Ogni componente può essere ulteriormente personalizzato utilizzando **[!UICONTROL Impostazioni]** o **[!UICONTROL Stile]** nel menu a destra. Ad esempio, puoi modificare lo stile del testo, la spaziatura o il margine di ciascun componente. [Ulteriori informazioni su allineamento e spaziatura](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. Da **[!UICONTROL Selettore risorse]**, puoi selezionare direttamente le risorse memorizzate in **[!UICONTROL Libreria risorse]**. [Ulteriori informazioni sulla gestione delle risorse](assets-essentials.md)

   Fai doppio clic sulla cartella contenente le risorse. Trascinali e rilasciali in un componente struttura.

   ![](assets/email_designer_asset_picker.png)

1. Inserisci campi di personalizzazione per personalizzare il contenuto delle e-mail in base ai dati dei profili. [Ulteriori informazioni sulla personalizzazione dei contenuti](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Fai clic su **[!UICONTROL Abilita contenuto condizione]** per aggiungere contenuti dinamici e adattare i contenuti ai profili di destinazione in base alle regole condizionali. [Introduzione ai contenuti dinamici](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Fai clic sul pulsante **[!UICONTROL Collegamenti]** scheda dal riquadro a sinistra per visualizzare tutti gli URL del contenuto che verranno tracciati. È possibile modificare le **[!UICONTROL Tipo di tracciamento]** o **[!UICONTROL Etichetta]** e aggiungere **[!UICONTROL Tag]** se necessario. [Ulteriori informazioni sui collegamenti e il tracciamento dei messaggi](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Puoi personalizzare ulteriormente l’e-mail facendo clic su **[!UICONTROL Passa all’editor di codice]** dal menu avanzato. [Ulteriori informazioni sull’editor di codice](code-content.md)

   ![](assets/email_designer_switch-to-code.png)

   >[!CAUTION]
   >
   >Dopo il passaggio all’editor di codice, non potrai tornare alla finestra di progettazione visiva per questa e-mail.

1. Quando il contenuto è pronto, fai clic su **[!UICONTROL Simula contenuto]** per verificare il rendering dell’e-mail. È possibile scegliere la visualizzazione su desktop o dispositivo mobile. [Ulteriori informazioni sull’anteprima del messaggio e-mail](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Quando l’e-mail è pronta, fai clic su **[!UICONTROL Salva]**.

