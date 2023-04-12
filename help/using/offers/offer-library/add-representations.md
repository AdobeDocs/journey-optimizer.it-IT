---
title: Aggiungere rappresentazioni a un’offerta
description: Scopri come aggiungere rappresentazioni alle offerte
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# Aggiungere rappresentazioni a un’offerta {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="Rappresentazioni"
>abstract="Aggiungi delle rappresentazioni per definire dove verrà visualizzata l’offerta nel messaggio. Più rappresentazioni sono disponibili, più opportunità esistono per utilizzare l’offerta in contesti di posizionamento diversi."

Un’offerta può essere visualizzata in posizioni diverse all’interno di un messaggio: in un banner superiore con un’immagine, come testo in un paragrafo, come blocco di HTML, ecc. Più rappresentazioni di un’offerta, più opportunità esistono per utilizzare l’offerta in contesti di posizionamento diversi.

## Configurare le rappresentazioni dell’offerta {#representations}

Per aggiungere una o più rappresentazioni all’offerta e configurarle, effettua le seguenti operazioni.

1. Per la prima rappresentazione, inizia selezionando la **[!UICONTROL Canale]** verrà utilizzato.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Vengono visualizzati solo i posizionamenti disponibili per il canale selezionato nel **[!UICONTROL Posizionamento]** elenco a discesa.

1. Seleziona un posizionamento dall’elenco.

   Puoi inoltre utilizzare il pulsante accanto al **[!UICONTROL Posizionamento]** elenco a discesa per sfogliare tutti i posizionamenti.

   ![](../assets/browse-button-placements.png)

   È comunque possibile filtrare i posizionamenti in base al relativo canale e/o tipo di contenuto. Scegli un posizionamento e fai clic su **[!UICONTROL Seleziona]**.

   ![](../assets/browse-placements.png)

1. Aggiungi contenuto alla tua rappresentazione. Scopri come in [questa sezione](#content).

1. Quando aggiungi contenuto, ad esempio un’immagine o un URL, puoi specificare un **[!UICONTROL Collegamento di destinazione]**: gli utenti che fanno clic sull’offerta verranno indirizzati alla pagina corrispondente.

   ![](../assets/offer-destination-link.png)

1. Infine, seleziona la lingua scelta per identificare e gestire gli elementi da visualizzare agli utenti.

1. Per aggiungere un&#39;altra rappresentazione, utilizza la **[!UICONTROL Aggiungi rappresentazione]** e aggiungi tutte le rappresentazioni necessarie.

   ![](../assets/offer-add-representation.png)

1. Dopo aver aggiunto tutte le rappresentazioni, seleziona **[!UICONTROL Successivo]**.

## Definire il contenuto per le rappresentazioni {#content}

È possibile aggiungere diversi tipi di contenuto a una rappresentazione.

>[!NOTE]
>
>È disponibile per l’uso solo il contenuto corrispondente al tipo di contenuto del posizionamento.

### Aggiungere immagini {#images}

Se la posizione selezionata è di tipo immagine, puoi aggiungere contenuto proveniente da **Risorsa Adobe Experience Cloud** libreria, un archivio centralizzato di risorse fornito da [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> Per lavorare con [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, you need to deploy [!DNL Assets Essentials] for your organization and make sure that users are a part of the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. Learn more on [this page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html?lang=it){target="_blank"}.

1. Scegli la **[!UICONTROL Libreria risorse]** opzione .

1. Seleziona **[!UICONTROL Sfoglia]**.

   ![](../assets/offer-browse-asset-library.png)

1. Sfoglia le risorse per selezionare l&#39;immagine desiderata

1. Fai clic su **[!UICONTROL Seleziona]**.

   ![](../assets/offer-select-asset.png)

### Aggiungere file HTML o JSON {#html-json}

Se il posizionamento selezionato è di tipo HTML, puoi anche aggiungere contenuto HTML o JSON proveniente da [Libreria risorse Adobe Experience Cloud](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}).

Ad esempio, hai creato un modello e-mail di HTML in [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} e desideri utilizzare tale file per il contenuto dell’offerta. Invece di creare un nuovo file, puoi semplicemente caricare il modello nel **Libreria risorse** per riutilizzarlo nelle rappresentazioni dell’offerta.

Per riutilizzare il contenuto in una rappresentazione, sfoglia **Libreria risorse** come descritto in [questa sezione](#images) e seleziona il file HTML o JSON desiderato.

![](../assets/offer-browse-asset-library-json.png)

### Aggiungi URL {#urls}

Per aggiungere contenuto da una posizione pubblica esterna, seleziona **[!UICONTROL URL]**, quindi immetti l’indirizzo URL del contenuto da aggiungere.

Puoi personalizzare gli URL utilizzando l’editor espressioni. Ulteriori informazioni su [personalizzazione](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

Ad esempio, vuoi personalizzare l’immagine mostrata come offerta. Vuoi che gli utenti che favoriscono le vacanze in città vedano lo skyline NYC e gli utenti che favoriscono le vacanze in spiaggia per vedere le Hawaii northshore.

Utilizza l’editor espressioni per recuperare gli attributi del profilo memorizzati in Adobe Experience Platform utilizzando schemi di unione. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

Se specifichi una **[!UICONTROL Collegamento di destinazione]**, puoi anche personalizzare l’URL a cui verranno indirizzati gli utenti che fanno clic sull’offerta.

### Aggiungi testo personalizzato {#custom-text}

È inoltre possibile inserire contenuto di tipo testo quando si seleziona una posizione compatibile.

1. Seleziona la **[!UICONTROL Personalizzato]** e fai clic su **[!UICONTROL Aggiungi contenuto]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Questa opzione non è disponibile per i posizionamenti di tipo immagine.

1. Digita il testo che verrà visualizzato nell’offerta.

   ![](../assets/offer-text-content.png)

   Puoi personalizzare il contenuto utilizzando l’editor espressioni. Ulteriori informazioni su [personalizzazione](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Solo il **[!UICONTROL Attributi del profilo]**, **[!UICONTROL Iscrizioni dei segmenti]** e **[!UICONTROL Funzioni di supporto]** le fonti sono disponibili per la gestione delle decisioni.

