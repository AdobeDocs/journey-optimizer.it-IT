---
title: Creare regole di decisione
description: Scopri come creare regole decisionali per definire a chi visualizzare le offerte
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 12%

---

# Creare regole di decisione {#create-decision-rules}

Puoi creare regole decisionali per le offerte in base ai dati disponibili in Adobe Experience Platform. Le regole decisionali determinano a chi visualizzare un’offerta.

Ad esempio, puoi specificare che desideri che venga visualizzata solo “Offerta di abbigliamento invernale per le donne” quando (Genere = ‘Femmina’) e (Area geografica = ‘Nord Est’). 

➡️ [Scopri questa funzione nel video](#video)

L&#39;elenco delle regole decisionali create è accessibile nella **[!UICONTROL Components]** menu.

![](../../assets/decision_rules_list.png)

Per creare una regola decisionale, effettua le seguenti operazioni:

1. Vai a **[!UICONTROL Rules]** scheda , quindi fai clic su **[!UICONTROL Create rule]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. Denomina la regola e fornisci una descrizione, quindi configura la regola in base alle tue esigenze.

   Per eseguire questa operazione, **Generatore di segmenti** è disponibile per creare le condizioni della regola. [Ulteriori informazioni](../../segment/about-segments.md)

   In questo esempio, la regola eseguirà il targeting dei clienti con il livello di fedeltà &quot;Gold&quot;.

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Il Generatore di segmenti fornito per creare regole decisionali presenta alcune specificità rispetto a quella utilizzata con il **[!UICONTROL Audience Destinations]** servizio. Ad esempio, il **[!UICONTROL Segments]** scheda non disponibile per l’uso. Tuttavia, il processo globale descritto nella documentazione di Segment Builder è ancora valido per creare regole decisionali per le offerte.

1. Fai clic su **[!UICONTROL Save]** per confermare.

1. Una volta creata, la regola viene visualizzata nell’elenco delle regole. È possibile selezionarlo per visualizzarne le proprietà e modificarlo o eliminarlo.

   ![](../../assets/rule_created.png)

>[!CAUTION]
>
>Le offerte basate su eventi non sono attualmente supportate in [!DNL Journey Optimizer]. Se crei una regola decisionale basata su un [event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}, non potrai sfruttarlo in un&#39;offerta.

## Video tutorial {#video}

>[!NOTE]
>
>Questo video si applica al servizio di applicazione Offer Decisioning integrato in Adobe Experience Platform. Tuttavia, fornisce indicazioni generiche per utilizzare Offerta nel contesto di Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
