---
solution: Journey Optimizer
product: journey optimizer
title: Progettare contenuti da zero in Journey Optimizer
description: Scopri come progettare i contenuti da zero
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: contenuto, editor, e-mail, start
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 60%

---

# Crea contenuto da zero {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout del messaggio e-mail. Per iniziare a progettare il contenuto delle e-mail, trascina un componente **Struttura** nell’area di lavoro."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout della pagina di destinazione. Per iniziare a progettare il contenuto della pagina di destinazione, trascina un componente **Struttura** nell’area di lavoro."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout del frammento. Per iniziare a progettare il contenuto del frammento, trascina un componente **Struttura** nell’area di lavoro."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout del modello. Per iniziare a progettare il contenuto del modello, trascina un componente **Struttura** nell’area di lavoro."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definire le colonne di un’e-mail"
>abstract="E-mail designer consente di definire facilmente il layout delle e-mail definendone la struttura a colonne."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definire le colonne di una pagina di destinazione"
>abstract="Designer consente di definire facilmente il layout della pagina di destinazione definendone la struttura a colonne."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definire le colonne di un frammento"
>abstract="Designer consente di definire facilmente il layout del frammento definendone la struttura a colonne."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definire le colonne di un modello"
>abstract="Designer consente di definire facilmente il layout del modello definendone la struttura a colonne."


Utilizza Adobe Journey Optimizer Designer per definire facilmente la struttura del contenuto. Aggiungendo e spostando elementi strutturali con semplici azioni di trascinamento della selezione, è possibile progettare la forma del contenuto in pochi secondi.

Per iniziare a creare il contenuto delle , segui i passaggi seguenti:

1. Dalla pagina home di Designer, seleziona l’opzione **[!UICONTROL Progetta da zero]**.

   ![](assets/email_designer.png)

1. Inizia a progettare il contenuto trascinando la selezione **[!UICONTROL Strutture]** nell’area di lavoro per definire il layout dell’e-mail.

   >[!NOTE]
   >
   >L’utilizzo di colonne sovrapposte non è compatibile con tutti i programmi e-mail. Quando non è supportato, le colonne non vengono impilate.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Aggiungi tanti **[!UICONTROL Strutture]** in base alle esigenze e modificarne le impostazioni nel riquadro dedicato a destra.

   ![](assets/email_designer_structure_components.png)

   Seleziona il componente **[!UICONTROL Colonna n:n]** per definire il numero di colonne desiderato (tra 3 e 10). Per definire la larghezza di ogni colonna, sposta le frecce nella parte inferiore di ciascuna colonna.

   >[!NOTE]
   >
   >Le dimensioni di ogni colonna non possono essere inferiori al 10% della larghezza totale del componente struttura. Non è possibile rimuovere una colonna non vuota.

1. Espandi **[!UICONTROL Sommario]** e aggiungi tutti gli elementi necessari in uno o più componenti della struttura. [Ulteriori informazioni sui componenti contenuto](content-components.md)

1. Ogni componente può essere ulteriormente personalizzato utilizzando **[!UICONTROL Impostazioni]** o **[!UICONTROL Stile]** nel menu di destra. Ad esempio, puoi modificare lo stile del testo, la spaziatura o il margine di ciascun componente. [Ulteriori informazioni su allineamento e spaziatura](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. Dalla sezione **[!UICONTROL Selettore risorse]**, puoi selezionare direttamente le risorse memorizzate in **[!UICONTROL Libreria risorse]**. [Ulteriori informazioni sulla gestione delle risorse](assets-essentials.md)

   Fai doppio clic sulla cartella che contiene le risorse. Trascinali e rilasciali in un componente struttura.

   ![](assets/email_designer_asset_picker.png)

1. Inserisci campi di personalizzazione per personalizzare il contenuto da attributi di profili, appartenenze a segmenti, attributi contestuali e altro ancora. [Ulteriori informazioni sulla personalizzazione dei contenuti](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Clic **[!UICONTROL Abilita contenuto condizione]** per aggiungere contenuto dinamico e adattarlo ai profili target in base a regole condizionali. [Introduzione ai contenuti dinamici](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Fai clic su **[!UICONTROL Collegamenti]** dal riquadro a sinistra per visualizzare tutti gli URL del contenuto che verranno tracciati. È possibile modificare i **[!UICONTROL Tipo di tracciamento]** o **[!UICONTROL Etichetta]** e aggiungi **[!UICONTROL Tag]** se necessario. [Ulteriori informazioni su collegamenti e tracciamento](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Se necessario, puoi personalizzare ulteriormente l’e-mail facendo clic su **[!UICONTROL Passa all’editor di codice]** nel menu avanzato. Questo consente di modificare il codice sorgente dell’e-mail, ad esempio per aggiungere tag di tracciamento o HTML personalizzati. [Ulteriori informazioni sull’editor di codice](code-content.md)

   >[!CAUTION]
   >
   >Dopo il passaggio all’editor di codice, per l’e-mail corrente non è possibile tornare al designer visivo.

1. Quando il contenuto è pronto, fai clic su **[!UICONTROL Simula contenuto]** per controllare il rendering. È possibile scegliere la visualizzazione su desktop o dispositivo mobile. [Ulteriori informazioni sull’anteprima del messaggio e-mail](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Quando il contenuto è pronto, fai clic su **[!UICONTROL Salva]**.

