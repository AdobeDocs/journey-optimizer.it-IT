---
title: Informazioni sull’editor espressioni
description: Scopri come utilizzare l’editor espressioni.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 7a07f2348f08b4582a1310fb65d431c55451d9b6
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 8%

---

# Informazioni sull’editor espressioni {#build-personalization-expressions}

L’editor di espressioni è il fulcro della personalizzazione in [!DNL Journey Optimizer]. È disponibile in ogni contesto in cui devi definire la personalizzazione come e-mail, push e offerte.

Nell’interfaccia dell’editor di espressioni, seleziona, organizza, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine da personalizzare.

![](assets/perso_ee3.png)

Le origini disponibili sono:

* **[!UICONTROL Profile attributes]** : elenca tutti i riferimenti associati allo schema di profilo descritto in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : elenca tutti i segmenti creati nel servizio Segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa sulla gestione delle offerte, consulta [questa sezione](../messages/deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : quando **Messaggio** in un percorso, i campi percorso contestuale sono disponibili tramite questo menu. [Ulteriori informazioni](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : elenca tutte le funzioni di supporto disponibili per eseguire operazioni sui dati, ad esempio calcoli, formattazione dei dati o conversioni, condizioni e manipolarle nel contesto della personalizzazione. [Ulteriori informazioni](functions/functions.md).

Una volta selezionato, il riferimento viene aggiunto nell’editor.

>[!NOTE]
>
>L’icona Info accanto all’icona &quot;+&quot; apre una descrizione comandi che fornisce ulteriori dettagli per ogni variabile.
>
>Puoi aggiungere gli attributi utilizzati più di frequenza ai preferiti. [Ulteriori informazioni](personalization-favorites.md).

Nell’esempio seguente, l’editor di espressioni ti consente di selezionare i profili che compiono il loro compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a questo giorno.

![](assets/perso_ee2.png)

Quando l’espressione di personalizzazione è pronta, è necessario che venga convalidata dall’editor espressioni. [Ulteriori informazioni](personalization-validation.md).
