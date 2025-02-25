---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sull’editor di personalizzazione
description: Scopri come utilizzare l’editor di personalizzazione.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, about, start
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: fe22eef1e1d74101ba7c046fca28a5a95007dd81
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 10%

---

# Introduzione all’editor di personalizzazione {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Informazioni sull’editor di personalizzazione"
>abstract="L’editor di personalizzazione consente di selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione dei contenuti."

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Completamento automatico"
>abstract="L&#39;attivazione di questa opzione consente al sistema di completare automaticamente il codice e di formulare suggerimenti durante la digitazione dell&#39;espressione. Questa opzione è disponibile solo per il formato HTML."

L&#39;editor di personalizzazione è il fulcro della personalizzazione in [!DNL Journey Optimizer]. È disponibile in ogni contesto in cui è necessario definire la personalizzazione, ad esempio e-mail, push e offerte.

Nell’interfaccia dell’editor di personalizzazione, seleziona, disponi, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

## Origini di personalizzazione disponibili {#sources}

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine per la personalizzazione. Le origini disponibili sono:

* **[!UICONTROL Attributi profilo]** : elenca tutti i riferimenti associati allo schema profilo descritto nella [documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.
* **[!UICONTROL Tipi di pubblico]**: elenca tutti i tipi di pubblico creati nel servizio di segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione sono disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"}.
* **[!UICONTROL Decisioni di offerta]** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa su come gestire le offerte, consulta [questa sezione](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Attributi contestuali]**: quando un&#39;attività di azione canale (e-mail, push, SMS) viene utilizzata in un percorso o in una campagna, gli attributi contestuali relativi a eventi e proprietà sono disponibili per la personalizzazione. Un esempio di personalizzazione che sfrutta gli attributi contestuali è presentato in [questa sezione](personalization-use-case.md).
* **[!UICONTROL Funzioni helper]** : elenca tutte le funzioni helper disponibili per eseguire operazioni sui dati, ad esempio calcoli, formattazione o conversioni di dati, condizioni e manipolarle nel contesto della personalizzazione. Ulteriori informazioni in [questa sezione](functions/functions.md).

## Aggiungere attributi di personalizzazione {#add}

Fai clic sul pulsante + per aggiungere un attributo all’espressione di personalizzazione.

Il menu con i puntini di sospensione accanto all’icona &quot;+&quot; ti consente di ottenere più dettagli per ciascuna variabile e di aggiungere ai preferiti gli attributi utilizzati più di frequente. [Scopri come aggiungere attributi ai preferiti](personalization-favorites.md)

>[!NOTE]
>
>Se esegui il targeting di un pubblico con attributi di arricchimento generati utilizzando un flusso di lavoro di composizione, puoi sfruttare questi attributi di arricchimento per personalizzare il messaggio. [Scopri come utilizzare gli attributi di arricchimento del pubblico](../audience/about-audiences.md#enrichment)

Inoltre, puoi definire il testo di fallback predefinito che verrà visualizzato se un attributo di profilo di tipo stringa è vuoto. A tale scopo, fare clic sul pulsante con i puntini di sospensione accanto all&#39;attributo e selezionare **[!UICONTROL Inserisci con testo di fallback]**. Scrivere il testo da visualizzare per impostazione predefinita se il valore dell&#39;attributo è vuoto per un profilo, quindi fare clic su **[!UICONTROL Aggiungi]**.

![](assets/attribute-details.png)

Nell’esempio seguente, l’editor di personalizzazione ti consente di selezionare i profili che hanno il compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a quel giorno.

![](assets/perso_ee2.png)

Una volta che l’espressione di personalizzazione è pronta, devi farla convalidare dall’editor di personalizzazione. Ulteriori informazioni in [questa sezione](personalization-validation.md).
