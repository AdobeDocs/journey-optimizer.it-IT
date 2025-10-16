---
title: Progettare schede contenuto
description: Scopri come progettare i contenuti delle schede di contenuto
topic: Content Management
feature: Content Cards
role: User
level: Beginner
exl-id: b83bdade-7275-4eef-9c49-fc1d157cee0d
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 1%

---

# Progettare i contenuti delle schede di contenuto {#design-content-card}

Il costrutto di authoring per le schede fornisce un’esperienza di authoring basata su moduli che fornisce agli addetti al marketing input di base di cui gli sviluppatori possono eseguire il rendering.

Una volta definito e personalizzato il contenuto, puoi rivederlo e attivarlo. La campagna verrà inviata in base alla pianificazione impostata. [Ulteriori informazioni su questa pagina](../campaigns/review-activate-campaign.md).

## Layout scheda contenuto

![](assets/content-card-image.png)

Dalla sezione **[!UICONTROL Layout scheda contenuto]**, scegli una delle tre opzioni di layout immagine in base ai requisiti di messaggistica.

* **[!UICONTROL Immagine piccola]**: visualizza un&#39;immagine compatta accanto al testo, ideale per i messaggi in cui il contenuto ha la priorità sugli elementi visivi.

  Per ulteriori informazioni, consulta la documentazione di Adobe Developer [per iOS](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/content-card-ui/iOS/templates/smallimage-template/) e [per Android](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/content-card-ui/Android/public-classes/state/smallimagecarduistate/).

* **[!UICONTROL Immagine grande]**: presenta un&#39;immagine prominente sopra o accanto al testo, rendendo gli elementi visivi l&#39;elemento attivo principale del messaggio.

  Per ulteriori informazioni, consulta la documentazione di Adobe Developer [per iOS](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/content-card-ui/iOS/templates/largeimage-template/) e [per Android](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/content-card-ui/Android/public-classes/state/largeimagecarduistate/).

* **[!UICONTROL Solo immagine]**: mostra l&#39;immagine senza testo di accompagnamento, ideale per messaggi guidati da immagini o immagini autonome.

  Per ulteriori informazioni, consulta la documentazione di Adobe Developer [per iOS](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/content-card-ui/iOS/templates/imageonly-template/) e [per Android](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/content-card-ui/Android/public-classes/state/imageonlycarduistate/).

## Scheda Contenuto {#content-tab}

Dalla scheda **[!UICONTROL Contenuto]** è possibile personalizzare le schede di contenuto definendo il contenuto e aggiungendo supporti multimediali e pulsanti di azione direttamente da questa scheda.

### Contenuto testo {#title-body}

![](assets/content-card-design-2.png)

Per comporre il messaggio, immetti il testo nei campi **[!UICONTROL Titolo]** e **[!UICONTROL Corpo]**.

Se desideri personalizzare ulteriormente il messaggio, utilizza l&#39;icona **[!UICONTROL Personalization]** per aggiungere elementi personalizzati. Per istruzioni dettagliate su come utilizzare le funzionalità di personalizzazione, consulta [questa sezione](../personalization/personalize.md).

### Media {#add-media}

![](assets/content-card-design-3.png)

Il campo **[!UICONTROL Media]** consente di migliorare le schede di contenuto aggiungendo supporti, il che può rendere la presentazione più coinvolgente per gli utenti finali.

Per includere i file multimediali, digita l&#39;URL del file multimediale che desideri utilizzare o fai clic sull&#39;icona **[!UICONTROL Seleziona Assets]** per scegliere tra le risorse memorizzate nella libreria Assets. [Ulteriori informazioni sulla gestione delle risorse](../integrations/assets.md).

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL modalità di formattazione avanzata]** è attivata, puoi aggiungere un **[!UICONTROL testo alternativo]** per le applicazioni di lettura dello schermo e un&#39;altra risorsa nel campo **[!UICONTROL URL contenuto multimediale in modalità scura]**.

+++

### Pulsanti {#add-buttons}

![](assets/content-card-design-4.png)

Aggiungi i pulsanti per consentire agli utenti di interagire con le tue schede di contenuto.

1. Fai clic su **[!UICONTROL Aggiungi pulsante]** per creare un nuovo pulsante di azione.

1. Modifica il campo **[!UICONTROL Titolo]** del pulsante per specificare l&#39;etichetta che verrà visualizzata sul pulsante.

1. Seleziona un **[!UICONTROL evento di interazione]** per definire l&#39;azione che verrà attivata quando gli utenti fanno clic sul pulsante o interagiscono con esso.

1. Nel campo **[!UICONTROL Target]**, immetti l&#39;URL web o il collegamento diretto al quale gli utenti verranno indirizzati dopo aver interagito con il pulsante.

<!--
+++More options with advanced formatting

If the **[!UICONTROL Advanced formatting mode]** is switched on, you can choose for your **[!UICONTROL Buttons]**:

* the **[!UICONTROL Font]**
* the **[!UICONTROL Pt size]**
* the **[!UICONTROL Font Color]**
* the **[!UICONTROL Alignment]**

+++
-->

### Pulsante Ignora {#close-button}

![](assets/content-card-design-1.png)

Scegli lo **[!UICONTROL stile]** per il **[!UICONTROL pulsante Ignora]** per personalizzarne l&#39;aspetto.

Puoi scegliere uno dei seguenti stili:

* **[!UICONTROL Nessuno]**
* **[!UICONTROL Semplice]**
* **[!UICONTROL Cerchio]**



<!--
+++More options with advanced formatting

If the **[!UICONTROL Advanced formatting mode]** is switched on, you can choose for your **[!UICONTROL Header]** and **[!UICONTROL Body]**:

* the **[!UICONTROL Font]**
* the **[!UICONTROL Pt size]**
* the **[!UICONTROL Font Color]**
* the **[!UICONTROL Alignment]**
+++
-->



### Comportamento al clic

![](assets/content-card-design-5.png)

Nel campo **[!UICONTROL URL di destinazione]**, immetti l&#39;URL web o il collegamento diretto che indirizzerà gli utenti alla destinazione desiderata dopo che interagiranno con la scheda di contenuto. Potrebbe trattarsi di un sito web esterno, di una pagina specifica all’interno dell’app o di qualsiasi altra posizione in cui si desidera che gli utenti vengano indirizzati in base alla loro interazione.

## Scheda Dati

## Dati personalizzati {#custom-data}

![](assets/content-card-design-6.png)

Nella sezione **[!UICONTROL Dati personalizzati]**, fai clic su **[!UICONTROL Aggiungi coppia chiave/valore]** per includere le variabili personalizzate nel payload. Queste coppie chiave/valore ti consentono di trasmettere dati aggiuntivi, a seconda della configurazione specifica. Questo ti consente di aggiungere contenuti personalizzati o dinamici, informazioni di tracciamento o qualsiasi altro dato rilevante per la tua configurazione.
