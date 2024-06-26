---
title: Aggiungere rappresentazioni a un’offerta
description: Scopri come aggiungere rappresentazioni alle offerte
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Aggiungere rappresentazioni a un’offerta {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="Rappresentazioni"
>abstract="Aggiungi le rappresentazioni per definire dove verrà visualizzata l’offerta nel messaggio. Maggiore è il numero di rappresentazioni di un’offerta, maggiori sono le opportunità di utilizzarla in contesti di posizionamento diversi."

Un’offerta può essere visualizzata in posizioni diverse all’interno di un messaggio: in un banner superiore con un’immagine, come testo in un paragrafo, come blocco di HTML e così via. Maggiore è il numero di rappresentazioni di un’offerta, maggiori sono le opportunità di utilizzarla in contesti di posizionamento diversi.

## Configurare le rappresentazioni dell’offerta {#representations}

Per aggiungere una o più rappresentazioni all’offerta e configurarle, segui i passaggi seguenti.

1. Per la prima rappresentazione, inizia selezionando la **[!UICONTROL Canale]** che verrà utilizzato.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Solo i posizionamenti disponibili per il canale selezionato vengono visualizzati nel **[!UICONTROL Posizione]** elenco a discesa.

1. Selezionate un posizionamento dall&#39;elenco.

   Puoi anche utilizzare il pulsante accanto al **[!UICONTROL Posizione]** per sfogliare tutti i posizionamenti.

   ![](../assets/browse-button-placements.png)

   Lì è ancora possibile filtrare i posizionamenti in base al loro canale e/o tipo di contenuto. Scegliete un posizionamento e fate clic su **[!UICONTROL Seleziona]**.

   ![](../assets/browse-placements.png)

1. Aggiungi contenuto alla rappresentazione. Scopri come in [questa sezione](#content).

1. Quando aggiungi contenuto come un’immagine o un URL, puoi specificare un **[!UICONTROL Collegamento di destinazione]**: gli utenti che fanno clic sull’offerta verranno indirizzati alla pagina corrispondente.

   ![](../assets/offer-destination-link.png)

1. Infine, seleziona la lingua desiderata per identificare e gestire gli elementi da mostrare agli utenti.

1. Per aggiungere un&#39;altra rappresentazione, utilizzate **[!UICONTROL Aggiungi rappresentazione]** e aggiungi tutte le rappresentazioni necessarie.

   ![](../assets/offer-add-representation.png)

1. Dopo aver aggiunto tutte le rappresentazioni, selezionate **[!UICONTROL Successivo]**.

## Definire il contenuto per le rappresentazioni {#content}

È possibile aggiungere diversi tipi di contenuto a una rappresentazione.

>[!NOTE]
>
>È disponibile per l’uso solo il contenuto corrispondente al tipo di contenuto del posizionamento.

### Aggiungere immagini {#images}

Se il posizionamento selezionato è di tipo immagine, puoi aggiungere contenuto proveniente da **Risorsa Adobe Experience Cloud** libreria, un archivio centralizzato di risorse fornito da [!DNL Adobe Experience Manager Assets].

>[!NOTE]
>
> Per lavorare con [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, è necessario implementare [!DNL Assets Essentials] per la tua organizzazione e assicurati che gli utenti facciano parte **Assets Essentials utenti consumer** oppure/e **Utenti Assets Essentials** Profili di prodotto. Ulteriori informazioni su [questa pagina](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}.

1. Scegli la **[!UICONTROL Libreria risorse]** opzione.

1. Seleziona **[!UICONTROL Sfoglia]**.

   ![](../assets/offer-browse-asset-library.png)

1. Sfoglia le risorse per selezionare l’immagine desiderata

1. Clic **[!UICONTROL Seleziona]**.

   ![](../assets/offer-select-asset.png)

### Aggiungere file HTML o JSON {#html-json}

Se il posizionamento selezionato è di tipo HTML, puoi anche aggiungere contenuto HTML o JSON proveniente da [Libreria risorse Adobe Experience Cloud](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}).

Ad esempio, hai creato un modello e-mail di HTML in [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} e desideri utilizzare quel file per il contenuto dell’offerta. Invece di creare un nuovo file, puoi semplicemente caricare il modello in **Libreria risorse** per poterla riutilizzare nelle rappresentazioni dell’offerta.

Per riutilizzare il contenuto in una rappresentazione, sfogliate la **Libreria risorse** come descritto in [questa sezione](#images) e seleziona il file HTML o JSON desiderato.

![](../assets/offer-browse-asset-library-json.png)

### Aggiungi URL {#urls}

Per aggiungere contenuto da una posizione pubblica esterna, seleziona **[!UICONTROL URL]**, quindi inserisci l’indirizzo URL del contenuto da aggiungere.

Puoi personalizzare gli URL utilizzando l’editor di personalizzazione. Ulteriori informazioni su [personalizzazione](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

Ad esempio, desideri personalizzare l’immagine visualizzata come offerta. Vuoi che gli utenti che preferiscono le vacanze in città vedano lo skyline di New York e quelli che preferiscono le vacanze in spiaggia vedano la costa nord delle Hawaii.

Utilizza l’editor di personalizzazione per recuperare gli attributi del profilo memorizzati in Adobe Experience Platform utilizzando gli schemi di unione. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

Se si specifica un **[!UICONTROL Collegamento di destinazione]**, puoi anche personalizzare l’URL a cui verranno indirizzati gli utenti che fanno clic sull’offerta.

### Aggiungi testo personalizzato {#custom-text}

È inoltre possibile inserire contenuto di tipo testo quando si seleziona un posizionamento compatibile.

1. Seleziona la **[!UICONTROL Personalizzato]** e fai clic su **[!UICONTROL Aggiungi contenuto]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Questa opzione non è disponibile per i posizionamenti di tipo immagine.

1. Digita il testo che verrà visualizzato nell’offerta.

   ![](../assets/offer-text-content.png)

   Puoi personalizzare i contenuti utilizzando l’editor di personalizzazione. Ulteriori informazioni su [personalizzazione](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Solo il **[!UICONTROL Attributi del profilo]**, **[!UICONTROL Tipi di pubblico]** e **[!UICONTROL Funzioni di supporto]** Le fonti sono disponibili per la gestione delle decisioni.

## Personalizzare le rappresentazioni in base ai dati contestuali{#context-data}

Quando i dati contestuali vengono trasmessi nel [Decisioning Edge](../api-reference/offer-delivery-api/edge-decisioning-api.md) chiamata, puoi sfruttare questi dati per personalizzare dinamicamente le rappresentazioni. Ad esempio, puoi personalizzare la rappresentazione di un’offerta in base a fattori in tempo reale, come le condizioni meteo correnti al momento in cui viene presa la decisione.

A questo scopo, incorpora la variabile di dati di contesto direttamente all’interno del contenuto della rappresentazione utilizzando `profile.timeSeriesEvents.` spazio dei nomi.

Di seguito è riportato un esempio di sintassi utilizzato per personalizzare la rappresentazione di un’offerta in base ai sistemi operativi degli utenti:

```
 {%#if profile.timeSeriesEvents.device.model = "Apple"%}ios{%else%}android{%/if%} 
```

La richiesta di Edge decisioning corrispondente, inclusi i dati contestuali, è la seguente:

```
{
    "body": {
        "xdm": {
            "identityMap": {
                "Email": [
                    {
                        "id": "xyz@abc.com"
                    }
                ]
            },
            "device": {
                "model": "Apple"
            }
        },
        "extra": {
            "query": {
                "decisionScopes": [
                    "eyJ4ZG06..."
                ]
            }
        }
    }
}
```
