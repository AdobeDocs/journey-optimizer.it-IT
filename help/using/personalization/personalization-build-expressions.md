---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sull’editor di espressioni
description: Scopri come utilizzare l’editor espressioni.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, informazioni, inizio
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 93e3ed9e1a9a437353b800aee58952b86eab9370
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 12%

---

# Guida introduttiva all’editor espressioni {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Informazioni sull’editor di espressioni"
>abstract="L’editor di espressioni consente di selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione per i contenuti."

L’editor espressioni è il fulcro della personalizzazione in [!DNL Journey Optimizer]. È disponibile in ogni contesto in cui devi definire la personalizzazione come e-mail, push e offerte.

Nell’interfaccia dell’editor di espressioni, seleziona, organizza, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

## Origini di personalizzazione disponibili {#sources}

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine da personalizzare. Le origini disponibili sono:

* **[!UICONTROL Attributi del profilo]** : elenca tutti i riferimenti associati allo schema di profilo descritto in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.
* **[!UICONTROL Iscrizioni dei segmenti]** : elenca tutti i segmenti creati nel servizio Segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.
* **[!UICONTROL Decisioni di offerta]** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa sulla gestione delle offerte, consulta [questa sezione](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Attributi contestuali]** : quando in un percorso viene utilizzata un’attività di azione canale (E-mail, push, SMS), i campi di percorso contestuali sono disponibili tramite questo menu. Ulteriori informazioni in [questa sezione](personalization-use-case.md).
* **[!UICONTROL Funzioni di supporto]** : elenca tutte le funzioni di supporto disponibili per eseguire operazioni sui dati, ad esempio calcoli, formattazione dei dati o conversioni, condizioni e manipolarle nel contesto della personalizzazione. Ulteriori informazioni in [questa sezione](functions/functions.md).

## Aggiungere attributi di personalizzazione {#add}

Fai clic sul pulsante + per aggiungere un attributo all’espressione di personalizzazione.

Il menu dei puntini di sospensione accanto all’icona &quot;+&quot; consente di ottenere ulteriori dettagli per ciascuna variabile e di aggiungere ai preferiti gli attributi più utilizzati. [Scopri come aggiungere attributi ai preferiti](personalization-favorites.md)

Inoltre, puoi definire il testo di fallback predefinito che verrà visualizzato se un attributo di profilo di tipo stringa è vuoto. A questo scopo, fai clic sul pulsante dei puntini di sospensione accanto all’attributo e seleziona **[!UICONTROL Inserisci con testo di riserva]**. Scrivi il testo che deve essere visualizzato per impostazione predefinita se il valore dell&#39;attributo è vuoto per un profilo, quindi fai clic su **[!UICONTROL Aggiungi]**.

![](assets/attribute-details.png)

Nell’esempio seguente, l’editor di espressioni ti consente di selezionare i profili che compiono il loro compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a questo giorno.

![](assets/perso_ee2.png)

Quando l’espressione di personalizzazione è pronta, è necessario che venga convalidata dall’editor espressioni. Ulteriori informazioni in [questa sezione](personalization-validation.md).
